---
title: Rakennetiedot – nimikeseurannan kirjauksen rakenne
description: Lisätietoja nimiketapahtumien käyttämisestä nimikkeen seurantanumeroiden ensisijaisina lähteinä nimikeseurannan kirjauksen rakenteessa.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, item tracking, posting, inventory'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-posting-structure"></a><a name="design-details-item-tracking-posting-structure"></a><a name="design-details-item-tracking-posting-structure"></a>Rakennetiedot: nimikkeen seurannan kirjauksen rakenne
Varaston arvostustoiminnon hyödyntämiseksi ja yksinkertaisen ja vakaan ratkaisun saavuttamiseksi nimikkeen seurantanumeroiden ensisijaisena lähteenä käytetään nimiketapahtumia.  
  
Tilausverkon yksiköiden ja tilausverkon ulkopuolisten yksiköiden nimikkeen seurantanumerot on määritetty **Varaustapahtuma**-taulukossa (T337). Historiatietoihin liittyvät nimikkeen seurantanumerot noudetaan suoraan nimiketapahtumista, jotka liittyvät kyseiseen tapahtumaan. Tämä tarkoittaa sitä, että nimiketapahtumat vaikuttavat kirjatun tilausrivin nimikeseurannan määrityksiin.  
  
**Nimikkeenseurantarivit**-sivu vastaanottaa tietoja kohteesta T337 ja nimikkeen pääkirjan kirjauksista ja näyttää ne väliaikaistaulukon välityksellä, **Seurantaerittely** (T336). T336 sisältää myös väliaikaiset tiedot **Nimikkeenseurantarivit-sivulla** koskien nimikkeenseurantamääriä, jotka ovat jäljellä laskutusta varten.  
  
## <a name="one-to-many-relation"></a><a name="one-to-many-relation"></a><a name="one-to-many-relation"></a>Yhden suhde moneen
**Nimikekirjauksen suhde** -taulukko, jota käytetään yhdistämään tiliöity asiakirjan rivi liittyviin nimikkeen pääkirjan kirjauksiin, käsittää kaksi pääosaa:  
  
* Osoitin kirjatulle asiakirjariville, **Rivinro** -kentässä.  
* Nimiketapahtumaan osoittava tapahtumanumero, **Nimiketapahtuman nro** kenttä.  
  
Olemassa olevan **Kirjausnro** -kentän toiminnallisuus, joka liittyy nimikkeen pääkirjan kirjaukseen tiliöityyn asiakirjariviin, käsittelee tyypillistä yksi yhteen -suhdetta, kun nimikkeen seurantanumeroita ei ole tiliöidyllä asiakirjarivillä. Jos nimikkeen seurantanumerot on olemassa, **Tapahtumanro**-kenttä jätetään tyhjäksi ja **Nimiketapahtuman suhde**-taulukko käsittelee yhden suhde moneen -suhdetta. Jos kirjatulla asiakirjarivillä on nimikkeen seurantanumeroita, mutta ne liittyvät vain yksittäiseen nimiketapahtumaan, **Tapahtumanro**-kenttä käsittelee suhteen ja **Nimiketapahtuman suhde**-taulukossa ei luoda tietuetta.  
  
## <a name="codeunits-80-and-90"></a><a name="codeunits-80-and-90"></a><a name="codeunits-80-and-90"></a>Koodiyksiköt 80 ja 90
Jos haluat jakaa nimiketapahtumat kirjauksen aikana, koodiyksikön 80 ja 90 koodi ympäröidään silmukoilla, jotka suoritetaan yleisen väliaikaisen tietueen muuttujien kautta. Tämä koodi kutsuu koodiyksikköä 22 ja nimikepäiväkirjan riviä. Nämä muuttujat alustetaan silloin, kun asiakirjan rivillä on nimikkeiden seurantanumerot. Kun tätä silmukkarakennetta käytetään aina, koodi pysyy yksinkertaisena. Jos asiakirjarivillä ei ole nimikkeen seurantanumeroita, yksittäinen tietue lisätään ja silmukka suoritetaan vain kerran.  
  
## <a name="posting-the-item-journal"></a><a name="posting-the-item-journal"></a><a name="posting-the-item-journal"></a>Nimikepäiväkirjan kirjaaminen
Nimikkeen seurantanumerot siirretään varaustapahtumien kautta, jotka liittyvät nimiketapahtumaan ja kierrätys nimikkeen seurantanumeroiden läpi tapahtuu koodiyksikössä 22. Tämä käsite toimii samalla tavalla kuin nimikepäiväkirjariviä käytetään epäsuorasti myynti- tai ostotilauksen kirjaamiseen samalla tavalla kuin nimikepäiväkirjariviä käytetään suoraan. Kun nimikepäiväkirjaa käytetään suoraan, **Lähderivin tunnus** -kenttä osoittaa nimikepäiväkirjan riviin.  
  
## <a name="code-unit-22"></a><a name="code-unit-22"></a><a name="code-unit-22"></a>Koodiyksikkö 22
Koodiyksiköt 80 ja 90 käyvät silmukassa läpi koodiyksikön 22 kutsun nimikkeen seurantanumeroiden laskujen kirjauksen aikana ja vastaanottojen olemassa olevien toimitusten laskutuksen aikana.  
  
Nimikkeen seurantanumeroiden määräkirjauksen aikana koodiyksikkö 22 noutaa seurantanumerot kirjaukseen liittyvistä tapahtumista kohteesta T337. Nämä tapahtumat asetetaan suoraan nimikepäiväkirjan riville.  
  
Koodiyksikkö 22 käy läpi silmukassa nimikkeen seurantanumerot ja jakaa kirjauksen vastaaviin nimiketapahtumiin, joilla on nimikkeen seurantanumerot. Tiedot siitä mitkä nimiketapahtumat luodaan palautetaan T337-taulukkoon käyttämällä väliaikaista T336-tietuetta, jota koodiyksikön 22 toiminto kutsuu. Tämä toiminto käynnistyy, kun koodiyksikön 22 suoritus on päättynyt, koska tässä vaiheessa koodiyksikön 22 objekti sisältää tiedot. Kun väliaikainen T336-tietue haetaan, koodiyksikkö 80 ja 90 luovat tietueet **Nimiketapahtuman suhde** -taulukkoon ja linkittävät luodun nimiketapahtuman luotuun toimitus- tai vastaanottoriviin. Koodiyksiköt 80 tai koodiyksikkö 90 muuntaa tämän jälkeen väliaikaiset T336-tietueet todellisiksi T336-tietueiksi, jotka liittyvät kyseiseen riviin. Tämä muuntaminen tapahtuu kuitenkin vain, jos kirjattua asiakirjariviä ei poisteta, koska se on kirjattu vain osittain.  
  
## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös
[Rakennetiedot: nimikkeen seuranta](design-details-item-tracking.md)   
[Rakennetiedot: nimikkeen seurannan rakenne](design-details-item-tracking-design.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
