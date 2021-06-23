---
title: Tuotantoraportit ja analytiikka
description: Katso, mitkä tuotantoraportit ja mikä analytiikka on saatavilla Business Centralin vakioversiossa, jotta voit seurata liiketoimintaasi.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 0cacf41f0a055267af5b0ce5a8b68b34d86a1cb5
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216347"
---
# <a name="production-reports-and-analytics-in-business-central"></a>Business Centralin tuotantoraportit ja analytiikka

[!INCLUDE [prod_short](includes/prod_short.md)] -tuotantoraporttien avulla tuotannon ja liiketoiminnan ammattilaiset voivat saada merkityksellistä tietoa ja analytiikkaa nykyisistä ja aiemmista tuotantotoiminnoista.  

## <a name="reports"></a>Raportit

Seuraavassa taulukossa kuvataan joitakin tuotantoraportoinnin keskeisiä raportteja.

|Raportti |Objektin tunnus|Kuvaus  |
|---------|---------|---------|
|**Tuoterak. määrän suuri kasvu**|99000753|Tämän raportin avulla tulostetaan sisennetty tuoterakenteen luettelointi suodattimissa määritettyjen nimikkeiden osalta. Tuotannon tuoterakenne puretaan kokonaan kaikilla tasoilla.|
|**Nimike – Mahdollista tehdä (Aika)**|5871|Näyttää, miten tuoterakennenimikkeen viisi erilaista tärkeää saatavuuslukua muuttuu ajan myötä. Nämä luvut muuttuvat odotettavissa olevien kysyntä- ja tarjontatapahtumien mukaan sekä sen kysynnän mukaan, joka perustuu käytettävissä oleviin osiin, jotka voidaan koota tai tuottaa.<br>Raportin avulla voit nähdä, voitko täyttää nimikkeen myyntitilauksen tiettynä päivämääränä tutkimalla sen nykyisen saatavuuden yhdessä mahdollisten määrien kanssa, jonka sen osat voivat toimittaa, jos kokoonpanotilaus on aloitettu. Tässä raportissa näkyy, milloin ja kuinka monta yksikköä kokoonpanon ja tuotannon nimikkeitä voit valmistaa osien saatavuuden ja nimikkeen senhetkisen saatavuuden perusteella. Tämä näkyy kokonaismääränä.<br>Tiedot näkyvät kaaviossa, jossa kutakin saatavuutta kuvaa viiva, joka etenee aikajanassa liikkuen ylös tai alas, kun määrät muuttuvat. Määräluvut tulevat samasta moottorista, joka tuottaa tietoja **Nimikkeen saatavuus tuoterakennetason mukaan** -ikkunaan. |
|**Tuoterakenteen kustannusjakauma**|5872|Näyttää graafisesti, kuinka kootun tai tuotetun nimikkeen kustannukset jakautuvat sen tuoterakenteessa.<br>Näistä tiedoista voi olla hyötyä päätettäessä esimerkiksi komponenttitoimittajan vaihtamisesta, sisäisen kapasiteetin ulkoistamisesta, ulkoistamisen päättämisestä tai tarkasteltaessa ja muutettaessa nimikkeen tuoterakennetta.<br>Raportin ensimmäisessä kaaviossa näytetään graafisesti eri värein päänimikkeen osien kokonaisyksikkökustannus sekä työresurssit viiteen eri kustannusjakaumaan eroteltuna.<br>Ympyräkaavio, jossa on kuvateksti *Materiaali/työ*, näyttää suhteellisen jakauman päänimikkeen materiaali- ja työkustannuksien välillä sekä sen oman tuotannon yleiskustannuksen. Materiaalien kustannusjaukauma sisältää nimikkeen materiaalikulut. Työn kustannukset sisältävät kapasiteetin, kapasiteetin yleiskustannukset ja alihankinnan kustannukset. Kustannusjakaumat näkyvät eri tavoin sen mukaan, mitä valintoja **Näytä vain** -kentässä on.<br>Ympyräkaavio, jossa on kuvateksti *Suora/epäsuora*, näyttää suhteellisen jakauman päänimikkeen suorien ja epäsuorien kustannusten välillä. Välitön kustannusjaukauma sisältää nimikkeen materiaali-, kapasiteetti-, ja alihankintakulut. Epäsuorien kustannusten osuuteen sisältyvät kapasiteetin ja tuotannon yleiskustannukset.<br>Raportin alaosassa oleva taulukko otetaan mukaan, kun **Sisällytä tiedot** -valintaruutu valitaan. Se näyttää valitut arvot Tuoterakenteen kustannusjakaumat -ikkunasta yhtenä tasona tai vyörytettyinä sen mukaan, mitä valintoja **Näytä kustannusjakaumat muodossa** -kentässä on.|
|**Eritelty laskenta**|99000756|Näyttää nimikkeen kustannusluettelon, jossa otetaan huomioon hukkatavara.|
|**Käyttökohde (ylin taso)**|99000757|Tässä raportissa näkyy, missä ja kuinka paljon nimikkeitä on käytetty tuoterakenteessa.<br>Raportissa näkyy vain käyttökohteena oleva nimike, kun perusnimikettä käytetään ylätason nimikkeenä. Jos esimerkiksi nimikettä "A" on käytetty nimikkeen "B" tuottamisessa ja nimikettä "B" käytetty nimikkeen "C" tuottamisessa, raportissa näkyy nimike B, jos raportti suoritetaan nimikkeelle A. Jos raportti suoritetaan nimikkeelle B, käyttökohteena näytetään nimikettä C.<br>**Käyttökohderivi**-sivun voi avata myös suoraan nimikkeestä.|
|**Nimikkeen tuoterakenteen vertailuluettelo**|99000758|Tämä raportti antaa sinulle mahdollisuuden verrata samankaltaisten lopputuotteiden kustannuksia. Näyttöön tulee luettelo, jossa ovat kaikki komponentit ja niiden kustannukset sekä tarvittavat määrät. Laskentapäiväksi määritetään tavallisesti käsittelypäivämäärä. |
|**Tuotantotilaustilastot**|99000791|Määrittää erilaisia kustannuksia, joita on kertynyt valitulle tuotantotilaukselle.<br>Raportin sisältö on hyvin samankaltainen kuin **Tuotantotilaustilastot**-sivulla.<br>Jos tuotantotilauksessa käytetään *Tilausohjattu*-tuotantotapaa, ikkunassa näkyy vain korkeimman tuoterakennetason nimikkeiden materiaali- ja kapasiteettikustannukset.|
|**Kapasiteetin tehtäväluettelo**|99000780|Tässä raportissa näkyvät tuotantotilaukset, jotka odottavat käsittelyä tuotantosoluissa ja kuormitusryhmissä. Tulosteissa näkyy tuotantosolun tai kuormitusryhmän kapasiteetti). Raportti sisältää tietoja, kuten aloitus- ja lopetusaika sekä päivämäärä tuotantotilausta ja panosmäärää kohti.|
|**Tuotantosolun kuormitus** tai **Kuormitusryhmän kuormitus**|99000783 tai 99000784|Molemmissa raporteissa näkyy luettelo tuotantosolun tai kuormitusryhmän kuormituksesta. Tuotantosolun tai kuormitusryhmän kuormitus on summa tarvittavista kerroista, jolloin kaikki suunnitellut ja todelliset tilaukset on suoritettu tuotantosolussa tiettynä ajanjaksona.|
|**Tuot.til. – Puuteluettelo**|99000788|Tämän raportin avulla saa näkyviin kaikki komponentit, joita ei ole saatavilla puuttuvan varaston vuoksi. Tästä yleiskatsauksesta voidaan siis tarkastella ajoissa, voidaanko suunnitellun tai julkaistun tuotantotilauksen aikajana pitää suunnitellusti.|


## <a name="tasks"></a>Tehtävät

Seuraavissa artikkeleissa kuvataan joitakin yrityksen tilan analysointiin liittyviä keskeisiä tehtäviä:

* [Tuotantosolujen ja kuormituskeskusten kuormituksen tarkasteleminen](production-how-to-view-the-load-on-work-centers.md)  
* [Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)

## <a name="see-also"></a>Katso myös

[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
