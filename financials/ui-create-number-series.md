---
title: Numerosarjan luominen | Microsoft Docs
description: "Lisätietoja siitä, miten määritetään numerosarjat, jotka määrittävät yksilölliset tunnuskoodit Finance and Operations, Business editionin tileille ja asiakirjoille."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3f50bc1153ccd6b58bc502974c042626ce696078
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="create-number-series"></a>Numerosarjojen luominen
Jokaiselle yritykselle on määritettävä yksilölliset tunnuskoodit esimerkiksi pääkirjanpidon tilejä, asiakas- ja toimittajatilejä, laskuja ja muita asiakirjoja varten. Numerointi ei ole tärkeää pelkästään tunnistamisen kannalta. Hyvin suunniteltu numerointijärjestelmä helpottaa myös yrityksen hallittavuutta ja analysointia ja voi vähentää tietojen syötössä tapahtuvien virheiden määrää.

> [!NOTE]  
>   On suositeltavaa käyttää niitä numerosarjan koodeja, jotka on mainittu CRONUS-esittely-yrityksen **Numerosarjaluettelo**-ikkunassa. Koodit, kuten *O-LASKU+*, eivät ehkä avaudu heti, mutta [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on tiettyjä oletusasetuksia, jotka perustuvat näihin numerosarjan koodeihin.

Numerointijärjestelmä luodaan määrittämällä koodeja kullekin perustietotyypille tai asiakirjalle. Voit määrittää koodin esimerkiksi asiakkaiden, myyntilaskujen ja yleisten päiväkirjojen numerointia varten. Kun olet määrittänyt koodin, sinun on määritettävä vähintään yksi numerosarjarivi. Numerosarjarivit sisältävät erilaisia tietoja, kuten sarjan ensimmäisen ja viimeisen numeron sekä alkupäivämäärän. Voit määrittää yhtä numerosarjakoodia kohti useita numerosarjarivejä, joilla kullakin on eri alkupäivämäärä. Numerosarjoja käytetään peräkkäin kulloisestakin alkupäivämäärästä alkaen.

Numerosarjat määritetään yleensä lisäämään seuraava peräkkäinen numero automaattisesti luotuihin uusiin kortteihin tai asiakirjoihin. Voit kuitenkin määrittää myös numerosarjoja, joissa uuden numeron voi antaa manuaalisesti. Se määritetään **Manuaaliset nrot** -valintaruudussa.

Jos haluat käyttää useita numerosarjakoodeja yhdelle perustietotyypille (esimerkiksi silloin, kun haluat eri numerosarjoja eri nimikeluokille), voit käyttää numerosarjasuhteita.

## <a name="to-create-a-new-number-series"></a>Uuden numerosarjan luominen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Nrosarja** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat uuden rivin kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**VIHJE**: Jos haluat sallia numeroiden antamisen manuaalisesti uusissa korteissa tai asiakirjoissa, poista **Oletusnrot**-valintaruudun valinta ja valitse **Manuaaliset nrot** -valintaruutu.

Kun nyt luot uuden kortin tai asiakirjan, joka on määritetty käyttämään kyseistä numerosarjaa, voit antaa **Nro**-kenttään sopivan arvon.  

## <a name="to-set-up-where-a-number-series-is-used"></a>Numerosarjan käyttökohteen määrittäminen
Seuraavaksi selitetään, miten myyntialueen numerosarja määritetään. Myös muut alueet määritetään vastaavasti.
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Nrosarja** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Myynnit ja myyntisaamiset** -ikkunan **Numerosarja**-pikavälilehdessä sopiva numerosarja kullekin myyntikortille tai -asiakirjalle.

Valitulla numerolla täytetään kyseisen kortin tai asiakirjan **Nro**-kenttä numerosarjarivillä tehtyjen asetusten mukaisesti.

## <a name="to-create-relationships-between-number-series"></a>Numerosarjojen suhteiden luonti
Jos tietylle perustiedolle tai tapahtumalle on luotu useampia numerosarjoja, näiden koodien välille voidaan luoda suhteita. Tämä toiminto auttaa koodien valinnassa kun käytetään numeroa.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Nrosarja** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse numerosarjoja sisältävä rivi, jolle haluat luoda suhteita. Valitse sitten **Suhteet**.
3. Kirjoita **Sarjakoodi**-kenttään sen numerosarjan koodi, johon haluat luoda suhteen vaiheessa 2 valitusta sarjasta.
4. Lisää rivi kullekin valittuun numerosarjaan liitettävälle koodille.
5. Sulje ikkuna.

Kun tarvitset numeron voit käyttää niitä suhteita, joita on luotu numerosarjojen valitsemiseksi.

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

