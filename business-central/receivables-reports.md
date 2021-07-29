---
title: Myyntisaatavien raportit ja analytiikka
description: Katso, mitkä tuotantoraportit ja mikä analytiikka on saatavilla Business Centralin vakioversiossa, jotta voit seurata myyntisaataviasi.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: 76de1625ee71b666b01d6b2fef1efe5605d9a418
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543335"
---
# <a name="accounts-receivable-reports-and-analytics-in-business-central"></a>Myyntisaatavien raportit ja analytiikka Business Centralissa

Jotta voit hallita myyntisaamisiasi helpommin [!INCLUDE [prod_short](includes/prod_short.md)]issa, vakioraportit ja analytiikka ovat sisään rakennettuina. Se ylittää perinteisen raportoinnin rajoitukset, jotta voit suunnitella tehokkaasti erityyppisiä raportteja.  

## <a name="reports"></a>Raportit

Seuraavassa taulukossa kuvataan joitakin myyntisaatavien keskeisiä raportteja.

| Raportti | Objektin tunnus | Kuvaus |
|--|--|--|
| **Myyntisaatavien tilanne** | 120 | Näyttää jäljellä olevan summan, ja asiakkaat on jaoteltu aikavälein erääntyneen ajan mukaan. Raportissa näkyy myös se osa asiakkaiden saldosta, joka ei ole erääntyvä ja joka voidaan näyttää kunkin asiakkaan asiakirjatietojen kanssa tai ilman. Tämä raportti on pääraportti asiakastapahtumien täsmäyttämiseksi KP:hen. Olettaen, että et ole sallinut suoraa kirjaamista tileille, joita käytetään asiakkaan kirjausryhmien myyntisaatavien tileillä, tämä raportti määrittää KP:stä löytyvät summat. |
| **Asiakkaan tiliote** | 1316 | Luo asiakkaan tiliotteen tietylle aikavälille. Se lähetetään yleensä asiakkaille antamaan heille yleiskuva maksamatta olevista summista ja myös muistutuksena erääntyneistä summista. Voit halutessasi näyttää erääntyneet summat erillisessä osassa. Voit sisällyttää erääntymisjakson, joka on samanlainen kuin **Erääntyneet myyntisaatavat** -raportissa. Erääntymisjaksolle asetetaan yleensä arvo *30D*, joka tarkoittaa 30 päivän aikavälejä, kuten 30, 60, 90 ja yli 90 päivän erääntyminen loppumispäivästä tai *1M+CM*, joka tarkoittaa nykyistä kuukautta eri aikavälillä ja sitten kuukausittaisia aikavälejä aiemmilta kuukausilta. **Huomautus** : Asiakasluettelossa tällä raportilla on myös erillinen toiminto, **Ajoitetut tiliotteet**. Tämä vaihtoehto ei suodatu valitsemallesi asiakkaalle. Se on sama raportti, mutta sitä käytetään silloin, kun haluat lähettää tiliotteen kaikille tai useammalle asiakkaalle. |
| **Asiakas – Saldo tähän mennessä** | 121 | Näyttää avoimet asiakastapahtumat loppupäivämäärään asti. Tässä raportissa näkyy samanlainen sisältö kuin asiakkaan tiliotteessa, mutta siinä ei ole mitään mainintaa siitä, onko tapahtuma erääntynyt. **Huomautus**: Päivämääräsuodatin kohdistetaan yksityiskohtaisiin asiakastapahtumiin. Tämä tarkoittaa sitä, että jos sinulla on loppupäivämäärää uudempia maksuja, jotka on kohdistettu laskuihin päivämäärävälin sisällä, laskut näkyvät raportissa, koska niitä ei ole suljettu loppupäivämäärän mukaan. |
| **Asiakas – Alustava saldo** | 129 | Näyttää asiakkaiden nettomuutokset päivämääräsuodattimessa määritetyltä ajanjaksolta sekä valittua aikaväliä vastaavan tilikauden tähänastisen nettomuutoksen. Raportti on ryhmitelty asiakkaan kirjausryhmien mukaan, ja se antaa erilaisen näkymän asiakastapahtumista kuin **Myyntisaatavien tilanne** -raportti. **Huomautus**: Jos et ole määrittänyt kirjanpitojaksoa, järjestelmä ei tiedä, mitä tilikautta käytetään, ja se näyttää joko vuoden alusta alkaen viimeksi määritetyn tilikauden tai valitsee vain kauden, joka voi olla vuoden alusta.|
| **Asiakas – Eritelty alustava saldo** | 104 | Näyttää kaikki määritetyn päivämääräsuodattimen asiakastapahtumat. Tätä raporttia käytetään yleensä tarkistamaan, että kaikki tietyn asiakkaan tapahtumat on tilitetty, tai muihin asiakastapahtumien sisäisiin tarkastuksiin. |
| **Asiakas - Maksukuitti** | 211 | Luo maksukuitin jokaiselle asiakastapahtumalle, joka on tyyppiä **Maksu**. Jos maksu on kohdistettu laskuihin, laskut määritetään. Muussa tapauksessa se vain kertoo maksusumman olevan kohdistamaton. Tätä raporttia käytetään lähetettäväksi asiakkaille, jotka haluavat dokumentaation maksun vastaanottamisesta.|
| **Täsmäytä asiakas- ja toimittajatilit** | 33 |Näyttää KP-tapahtumat, jotka johtuvat asiakas- ja toimittajatapahtumien kirjaamisesta KP-tiliä ja kirjausryhmiä kohden. Tätä raporttia käytetään asiakas- ja toimittajatapahtumien saldojen täsmäyttämiseen pääkirjanpidon saldoihin. |
| **As. - Yksink. eräänt.y&ht.veto**| 109 |Tämä on vanha versio myyntisaatavien erääntymisraportista. Suosittelemme, että käytät sen sijaan **Myyntisaatavien tilanne** -raporttia. |
| **Myynnin tilastot** |112  |[!INCLUDE [reports-sales-statistics](includes/reports-sales-statistics.md)]<br>Tätä raporttia voidaan käyttää myös myyntisaatavissa, koska on helpompaa tehdä nopea haku asiakkaan kirjatuista maksuista, alennuksista ja myynneistä.|
|**Asiakasluettelo**|101| Tässä raportissa näkyy monenlaisia perustietoja asiakkaasta, esimerkiksi asiakkaan kirjausryhmä, alennusryhmä, viivästyskulu- ja maksutietoja, myyjä, asiakkaan oletusvaluutta ja luottoraja paikallisessa valuutassa (PVA) sekä asiakkaan tämänhetkinen saldo (PVA:ssa). Raporttia voidaan käyttää esimerkiksi Asiakas-taulukon tietojen ylläpitämiseen.|

## <a name="see-also"></a>Katso myös

[Rahoituslaskelmien analysointi Microsoft Excel:issä](finance-analyze-excel.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Käyttöomaisuuden hallinta](fa-manage.md)  
[Paikallisten toiminnallisuuksien yleiskatsaus](about-localization.md)  
[Kirjanpitäjän käyttökokemukset [!INCLUDE[prod_long](includes/prod_long.md)]issa](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
