---
title: Ostovelkojen raportit ja analytiikka
description: Katso, mitkä raportit ja mikä analytiikka on saatavilla Business Centralin vakioversiossa, jotta voit seurata ostovelkojasi.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 347
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: edb3b32f88198d8e21aa2bfddafc1b7f319be9de
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953382"
---
# <a name="accounts-payable-reports-and-analytics-in-business-central"></a>Ostovelkojen raportit ja analytiikka Business Centralissa

Jotta voit hallita ostovelkojasi helpommin [!INCLUDE [prod_short](includes/prod_short.md)]issa, vakioraportit ja analytiikka ovat sisään rakennettuina. Se ylittää perinteisen raportoinnin rajoitukset, jotta voit suunnitella tehokkaasti erityyppisiä raportteja.  

## <a name="reports"></a>Raportit

Seuraavassa taulukossa kuvataan joitakin ostovelkojen keskeisiä raportteja.

| Raportti | Objektin tunnus | Kuvaus |
|--|--|--|
| **Ostovelkojen tilanne** | 322|Näyttää toimittajien erääntyneet saldot erääntymisaikavälien mukaan. Erääntyneet summat voidaan näyttää eräpäivän, kirjauspäivämäärän tai asiakirjapäivämäärän mukaan. Voit näyttää summat paikallisena valuuttana (PVA) ja tulostaa erääntyneiden asiakirjojen tiedot. Aikaväleillä voi olla otsikoita, joissa on päivämääriä tai viivästyspäivien lukumääriä, suhteessa määritettyyn erääntymiseen tyypin mukaan.<br>Tämä raportti on pääraportti toimittajatapahtumien täsmäyttämiseksi KP:hen. Olettaen, että et ole sallinut suoraa kirjaamista tileille, joita käytetään toimittajien kirjausryhmien ostovelkojen tileillä, tämä raportti määrittää pääkirjanpidosta löytyvät summat.|
| **Toimittaja - Saldo tähän menn.** | 321 | Näyttää toimittajan saldon määritetyn päivämäärävälin päättymispäivämäärän mukaan. Voit valita, näytetäänkö toimittajan saldo paikallisena valuuttana (PVA). Valitse **Sisällytä kohdistamattomat tapahtumat** -kenttä näyttääksesi tapahtumat, jotka on suljettu loppumispäivämäärään mennessä, mutta joita ei ole kohdistettu (avattu) myöhemmin. Valitse **Näytä tapahtumat, joiden saldo on nolla** näyttääksesi toimittajat, joiden saldo on nolla päivämääräsuodattimen loppumispäivämäärään mennessä. Päivämääräsuodatin koskee raportin tapahtumien yksityiskohtaisia toimittajatapahtumia. Jos sinulla on loppumispäivämäärää uudempia maksuja, jotka on kohdistettu laskuihin päivämäärävälin sisällä, laskut näkyvät raportissa, koska niitä ei ole suljettu loppumispäivämäärään mennessä. |
| **Toimittaja – Alustava saldo** | 329 | Näyttää toimittajien nettomuutokset päivämääräsuodattimessa määritetyltä ajanjaksolta sekä valittua aikaväliä vastaavan tilikauden tähänastisen nettomuutoksen. Raportti on ryhmitelty toimittajan kirjausryhmien mukaan, ja se antaa erilaisen näkymän toimittajatapahtumista kuin **Ostovelkojen tilanne** -raportti. **Huomautus**: Jos et ole määrittänyt kirjanpitojaksoa, järjestelmä ei tiedä, mitä tilikautta käytetään, ja se näyttää joko vuoden alusta alkaen viimeksi määritetyn tilikauden tai valitsee vain kauden, joka voi olla vuoden alusta.|
| **Toimittaja – Er. alust. saldo** | 304 | Näyttää kaikki määritetyn päivämääräsuodattimen toimittajatapahtumat. Raportissa näkyvät toimittajan alkusaldot suhteessa päivämääräsuodattimeen. |
| **Ostotilastot** |312 |[!INCLUDE [reports-purchase-statistics](includes/reports-purchase-statistics.md)]<br>Tätä raporttia voidaan käyttää myös ostoveloissa, koska on helpompaa tehdä nopea haku asiakkaan kirjatuista maksuista, alennuksista ja ja muista tapahtumista.|
|**Toimittaja – Eräänt.yht.veto**|305| Vanha raportti ostovelkojen tilanteesta. Suosittelemme, että käytät sen sijaan **Ostovelkojen tilanne** -raporttia. Voit valita kauden pituuden ja päivämäärän, jota käytetään määritettynä *erääntynyt*-päivämääränä.|
|**Pidätetyt maksut**|319|Näyttää toimittajatapahtumat, joissa **Pidossa**-kenttä ei ole tyhjä.|
|**Toimittajan maksupäiväkirjan esikatselu**|317|Näyttää maksupäiväkirjan, jossa on maksualennus- ja toleranssitiedot. Raporttia voidaan käyttää maksujen tarkistamiseen ennen maksutiedostojen luomista ja päiväkirjan kirjaamista. **Huomautus**: Raportissa näkyvät maksualennukset virheellisesti, jos sovelluksessa on käytetty useita hyvityslaskuja. Tässä tapauksessa ylimääräisten hyvityslaskujen maksualennus näytetään kohdistamattomana summana.|
|**Toimittaja – luettelo**|301|Tässä raportissa näkyy monenlaisia perustietoja toimittajista, esimerkiksi toimittajan kirjausryhmä, tietoja alennuksista ja maksuista, prioriteettitaso ja toimittajan oletusvaluutta sekä toimittajan nykyinen saldo (PVA:ssa). Raporttia voidaan käyttää esimerkiksi ylläpitämään Toimittaja-taulukon tietoja.|

## <a name="see-also"></a>Katso myös

[Rahoituslaskelmien analysointi Microsoft Excelissä](finance-analyze-excel.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Käyttöomaisuuden hallinta](fa-manage.md)  
[Paikallisten toiminnallisuuksien yleiskatsaus](about-localization.md)  
[Kirjanpitäjän käyttökokemukset [!INCLUDE[prod_long](includes/prod_long.md)]issa](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
