---
title: Rakennetiedot – nimikeseurannan kirjauksen rakenne
description: Lisätietoja nimiketapahtumien käyttämisestä nimikkeen seurantanumeroiden ensisijaisina lähteinä nimikeseurannan kirjauksen rakenteessa.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, item tracking, posting, inventory'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-item-tracking-posting-structure"></a>Rakennetiedot: nimikkeen seurannan kirjauksen rakenne
Varaston arvostustoiminnon hyödyntämiseksi ja yksinkertaisen ja vakaan ratkaisun saavuttamiseksi nimikkeen seurantanumeroiden ensisijaisena lähteenä käytetään nimiketapahtumia.  
  
Tilausverkon yksiköiden ja tilausverkon ulkopuolisten yksiköiden nimikkeen seurantanumerot on määritetty **Varaustapahtuma**-taulukossa (T337). Historiatietoihin liittyvät nimikkeen seurantanumerot noudetaan suoraan nimiketapahtumista, jotka liittyvät kyseiseen tapahtumaan. Tämä tarkoittaa sitä, että nimiketapahtumat vaikuttavat kirjatun tilausrivin nimikeseurannan määrityksiin.  
  
**Nimikkeenseurantarivit**-sivu vastaanottaa tietoja kohteesta T337 ja nimikkeen pääkirjan kirjauksista ja näyttää ne väliaikaistaulukon välityksellä, **Seurantaerittely** (T336). T336 sisältää myös väliaikaiset tiedot **Nimikkeenseurantarivit-sivulla** koskien nimikkeenseurantamääriä, jotka ovat jäljellä laskutusta varten.  
  
## <a name="one-to-many-relation"></a>Yhden suhde moneen
**Nimikekirjauksen suhde** -taulukko, jota käytetään yhdistämään tiliöity asiakirjan rivi liittyviin nimikkeen pääkirjan kirjauksiin, käsittää kaksi pääosaa:  
  
* Osoitin kirjatulle asiakirjariville, **Rivinro** -kentässä.  
* Nimiketapahtumaan osoittava tapahtumanumero, **Nimiketapahtuman nro** kenttä.  
  
Olemassa olevan **Kirjausnro** -kentän toiminnallisuus, joka liittyy nimikkeen pääkirjan kirjaukseen tiliöityyn asiakirjariviin, käsittelee tyypillistä yksi yhteen -suhdetta, kun nimikkeen seurantanumeroita ei ole tiliöidyllä asiakirjarivillä. Jos nimikkeen seurantanumerot on olemassa, **Tapahtumanro**-kenttä jätetään tyhjäksi ja **Nimiketapahtuman suhde**-taulukko käsittelee yhden suhde moneen -suhdetta. Jos kirjatulla asiakirjarivillä on nimikkeen seurantanumeroita, mutta ne liittyvät vain yksittäiseen nimiketapahtumaan, **Tapahtumanro**-kenttä käsittelee suhteen ja **Nimiketapahtuman suhde**-taulukossa ei luoda tietuetta.  
  
## <a name="codeunits-80-sales-post--and-90-purch-post"></a>Koodiyksikkö 80 (Myyntikirja) ja 90 (Ostokirja)
Jos haluat jakaa nimiketapahtumat kirjauksen aikana, koodiyksikön 80 ja 90 koodi ympäröidään silmukoilla, jotka suoritetaan yleisen väliaikaisen tietueen muuttujien kautta. Tämä koodi kutsuu koodiyksikköä 22 ja nimikepäiväkirjan riviä. Nämä muuttujat alustetaan silloin, kun asiakirjan rivillä on nimikkeiden seurantanumerot. Kun tätä silmukkarakennetta käytetään aina, koodi pysyy yksinkertaisena. Jos asiakirjarivillä ei ole nimikkeen seurantanumeroita, yksittäinen tietue lisätään ja silmukka suoritetaan vain kerran.  
  
## <a name="posting-the-item-journal"></a>Nimikepäiväkirjan kirjaaminen
Nimikeseurantanumeroita siirretään nimiketapahtumaan liittyvien varaustapahtumien kautta, ja nimikeseurantanumeroiden läpi silmukka tapahtuu koodiyksikössä 22 (Nimikkeen pvk-kirjausrivi). Tämä käsite toimii samalla tavalla kuin nimikepäiväkirjariviä käytetään epäsuorasti myynti- tai ostotilauksen kirjaamiseen samalla tavalla kuin nimikepäiväkirjariviä käytetään suoraan. Kun nimikepäiväkirjaa käytetään suoraan, **Lähderivin tunnus** -kenttä osoittaa nimikepäiväkirjan riviin.  
  
## <a name="code-unit-22--item-jnl-post-line"></a>Koodi yksikkö 22 (Nimikkeen pvk-kirjausrivi)
Koodiyksikkö 80 (Myyntikirja) ja 90 (Ostokirja) silmukka koodiyksikön 22 (Nimikkeen pvk-kirjausrivi) puhelu nimikeseurantanumeroiden laskun kirjauksen aikana sekä aiemmin luotujen toimitusten tai vastaanottojen laskutuksen aikana.  
  
Nimikeseurantanumeroiden määrän kirjauksen aikana koodiyksikkö 22 (Nimikkeen pvk-kirjausrivi) hakee nimikeseurantanumerot T337:n (Varaustapahtuma) tapahtumista, jotka liittyvät kirjaukseen. Nämä tapahtumat asetetaan suoraan nimikepäiväkirjan riville.  
  
Koodiyksikkö 22 (Nimikkeen pvk-kirjausrivi) silmukoi nimikkeen seurantanumerot ja jakaa kirjauksen vastaaviin nimiketapahtumiin, joilla on nimikkeen seurantanumerot. Tiedot siitä, mitkä nimiketapahtumat luodaan, palautetaan T337:ään (varaustapahtumaan) väliaikaisella T336-tietueella, jota kutsutaan koodiyksikön 22 menettelyllä. Tämä toiminto käynnistyy, kun koodiyksikön 22 suoritus on päättynyt, koska tässä vaiheessa koodiyksikön 22 objekti sisältää tiedot. Kun väliaikainen T336-tietue haetaan, koodiyksikkö 80 (Myyntikirjaus) ja 90 (ostokirjaus) luovat tietueita Nimiketapahtuman **suhde -** taulukkoon linkittääkseen luodut nimiketapahtumat luotuun toimituksen tai vastaanoton riviin. Koodiyksikkö 80 (Myyntikirja) ja 90 (Ostokirja) muuntavat sitten väliaikaiset T336 (Seurannan määrittely) -tietueet todellisiksi T336 (Seurannan määrittely) -tietueiksi, jotka liittyvät kyseessä olevaan riviin. Tämä muuntaminen tapahtuu kuitenkin vain, jos kirjattua asiakirjariviä ei poisteta, koska se on kirjattu vain osittain.  
  
## <a name="see-also"></a>Katso myös
[Rakennetiedot: nimikkeen seuranta](design-details-item-tracking.md)   
[Rakennetiedot: nimikkeen seurannan rakenne](design-details-item-tracking-design.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
