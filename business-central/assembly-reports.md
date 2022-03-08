---
title: Business Centralin kokoonpanoraportit ja analytiikka
description: Katso, mitkä kokoonpanoraportit ja mikä analytiikka on saatavilla Business Centralin vakioversiossa, jotta voit seurata liiketoimintaasi.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 91234cd02736d425116be40137efd9d068b5bd97
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216349"
---
# <a name="assembly-reports-and-analytics-in-business-central"></a>Business Centralin kokoonpanoraportit ja analytiikka

[!INCLUDE [prod_short](includes/prod_short.md)] -kokoonpanoraporttien avulla tuotannon ja liiketoiminnan ammattilaiset voivat saada merkityksellistä tietoa ja analytiikkaa nykyisistä ja aiemmista kokoonpanotoiminnoista.  

## <a name="reports"></a>Raportit

Seuraavassa taulukossa kuvataan joitakin kokoonpanoraportoinnin keskeisiä raportteja.

|Raportti |Objektin tunnus|Kuvaus  |
|---------|---------|---------|
|**Kokoonpanon tuoterakenteet**|801|Näyttää luettelon tuoterakenteista: nimi, tuoterakenteen numero, tuoterakenteen komponentit ja kaikki muut tuoterakenteet, jotka ovat osa tätä tuoterakennetta. Tuoterakenteen komponentit on määritelty tuoterakenteen komponenttitaulukossa. Tässä näkyy myös mittayksikkö ja tarvittava määrä kutakin komponenttia perusmittayksikköä kohti. |
|**Nimike – Mahdollista tehdä (Aika)**|5871|Näyttää, miten tuoterakennenimikkeen viisi erilaista tärkeää saatavuuslukua muuttuu ajan myötä. Nämä luvut muuttuvat odotettavissa olevien kysyntä- ja tarjontatapahtumien mukaan sekä sen kysynnän mukaan, joka perustuu käytettävissä oleviin osiin, jotka voidaan koota tai tuottaa.<br>Raportin avulla voit nähdä, voitko täyttää nimikkeen myyntitilauksen tiettynä päivämääränä tutkimalla sen nykyisen saatavuuden yhdessä mahdollisten määrien kanssa, jonka sen osat voivat toimittaa, jos kokoonpanotilaus on aloitettu. Tässä raportissa näkyy, milloin ja kuinka monta yksikköä kokoonpanon ja tuotannon nimikkeitä voit valmistaa osien saatavuuden ja nimikkeen senhetkisen saatavuuden perusteella. Tämä näkyy kokonaismääränä.<br>Tiedot näkyvät kaaviossa, jossa kutakin saatavuutta kuvaa viiva, joka etenee aikajanassa liikkuen ylös tai alas, kun määrät muuttuvat. Määräluvut tulevat samasta moottorista, joka tuottaa tietoja **Nimikkeen saatavuus tuoterakennetason mukaan** -ikkunaan. |
|**Tuoterakenteen kustannusjakauma**|5872|Näyttää graafisesti, kuinka kootun tai tuotetun nimikkeen kustannukset jakautuvat sen tuoterakenteessa.<br>Näistä tiedoista voi olla hyötyä päätettäessä komponenttitoimittajan vaihtamisesta, sisäisen kapasiteetin ulkoistamisesta, ulkoistamisen päättämisestä tai tarkasteltaessa ja muutettaessa esimerkiksi nimikkeen tuoterakennetta.<br>Raportin ensimmäisessä kaaviossa näytetään graafisesti eri värein päänimikkeen osien kokonaisyksikkökustannus sekä työresurssit viiteen eri kustannusjakaumaan eroteltuna.<br>Ympyräkaavio, jossa on kuvateksti *Materiaali/työ*, näyttää suhteellisen jakauman päänimikkeen materiaali- ja työkustannuksien välillä sekä sen oman tuotannon yleiskustannuksen. Materiaalien kustannusjaukauma sisältää nimikkeen materiaalikulut. Työn kustannukset sisältävät kapasiteetin, kapasiteetin yleiskustannukset ja alihankinnan kustannukset. Kustannusjakaumat näkyvät eri tavoin sen mukaan, mitä valintoja **Näytä vain** -kentässä on.<br>Ympyräkaavio kuvatekstillä *Suora/epäsuora* näyttää suhteellisen jakauman päänimikkeen suorien ja epäsuorien kustannusten välillä. Välitön kustannusjaukauma sisältää nimikkeen materiaali-, kapasiteetti-, ja alihankintakulut. Epäsuorien kustannusten osuuteen sisältyvät kapasiteetin ja tuotannon yleiskustannukset.<br>Raportin alaosassa oleva taulukko otetaan mukaan, kun Sisällytä tiedot -valintaruutu valitaan. Se näyttää valitut arvot Tuoterakenteen kustannusjakaumat -ikkunasta yhtenä tasona tai vyörytettyinä sen mukaan, mikä asetus on valittu Näytä kustannusjakaumat muodossa -kentässä.|
|**Käyttökohdeluettelo**|809|Näyttää luettelon tuoterakenteista, jonka komponentteja valitut nimikkeet ovat. Hyödyllinen yleiskuvaus siinä tapauksessa, että sinun täytyy muuttaa komponentti tuoterakenteessa, joka on lisätty kokoonpanonimikkeeseen. Esimerkiksi jos toimittaja ei voi enää toimittaa tiettyä nimikettä, jota käytit kokoonpanossa tai tuotannossa. Tällaisessa tapauksessa raportti antaa selkeän yleiskuvan siitä, mihin tuoterakenteisiin komponentti sisältyy. Komponentin numerolle voi asettaa suodattimen.|
|**Tuoterakenne – Raaka-aineet**|810|Tästä raportista saat yleiskuvan tarvittavista komponenteista sekä kokoonpanon että tuotannon osalta. Näet varaston, perusmittayksikön, päätoimittajan, jos toimittajan numero -kenttä on kirjoitettu nimikekorttiin, sekä toimitusajan laskennan.|
|**Tuoterakenne – Osakokoonpanot**|811|Jos tuotat ja/tai kokoat osakokoonpanoja, käytä tätä raporttia, niin saat yleiskuvan tämäntyyppisistä komponenteista. Tässä raportissa näkyvät perusmittayksikkö, varasto, yksikkökustannukset ja vaihtoehtoinen nimikenumero. |
|**Kokoonpanon tuoterakenne – Loppunimikkeet**|812|Näyttää luettelon nimikkeistä tai tuoterakenteista, jotka eivät ole tuoterakenteiden komponentteja. **Huomaa**: Tätä raporttia ei ole rajoitettu ainoastaan tuoterakenteille, joten muista asettaa suodatin **Kokoonpanon tuoterakenne** -kentässä tai **Täydennysjärjestelmä**-kentissä|
|**Kokoonpano tilausta varten – Myynti**|915|Näyttää myynnin tunnuslukuja kokoonpanon komponenttinimikkeille, jotka voidaan myydä sekä kokoonpanon osana "kokoonpano tilausta varten" -myynnissä että erillisenä nimikkeenä suoraan varastosta.<br>Tämän raportin avulla voit analysoida kokoonpanokomponenttien määrän, kustannukset, myynnin ja voittoluvut, jotka tukevat päätöksiäsi, kuten hinnoitellaanko paketti eri tavalla tai pysäytetäänkö tai aloitetaanko tietyn nimikkeen käyttö kokoonpanoissa.<br>**Kokoonpanossa**-rivillä näytetään kokoonpanon nimikkeessä myytävän kokonaismäärän myyntiluvut. Tämän kokonaissumman muodostava määritelty kokoonpanonimikkeiden myynti näkyy, jos **Näytä kokoonpanon tiedot** -kenttä valitaan.<br>Paino on kokoonpanokomponenteilla, mutta luvut lasketaan niiden päänimikkeen, eli kokoonpanon nimikkeen voittomarginaalista. Näin ollen kunkin komponentin myynnin summa lasketaan sen omasta kustannuksesta ja pääkohteensa tuottokatteesta seuraavalla kaavalla.<br>Raportti näyttää tiedot nimikkeistä, jotka täyttävät toisen tai molemmat seuraavista ehdoista:<br>- On olemassa Kokoonpano tilausta varten -kokoonpanokäytäntöä käyttävän nimikkeen kokoonpanon tuoterakenteessa.<br>- On myyty osana Kokoonpano tilausta varten -myyntiä.|

## <a name="tasks"></a>Tehtävät

Seuraavissa artikkeleissa kuvataan joitakin yrityksen tilan analysointiin liittyviä keskeisiä tehtäviä:

* [Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)

## <a name="see-also"></a>Katso myös

[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Tuoterakenteen käyttäminen](inventory-how-work-boms.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
