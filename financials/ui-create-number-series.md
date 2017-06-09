---
title: 'Toimintaohje: Numerosarjan luominen | Microsoft Docs'
description: "Lisätietoja numerosarjan luomisesta Dynamics 365 for Financialsissa."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d5a6da604634540abdb67dcf4a82737f2db58b0b
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-create-number-series"></a>Toimintaohje: Numerosarjan luominen
Jokaiselle yritykselle on määritettävä yksilölliset tunnuskoodit esimerkiksi pääkirjanpidon tilejä, asiakas- ja toimittajatilejä, laskuja ja muita asiakirjoja varten. Numerointi ei ole tärkeää pelkästään tunnistamisen kannalta. Hyvin suunniteltu numerointijärjestelmä helpottaa myös yrityksen hallittavuutta ja analysointia ja voi vähentää tietojen syötössä tapahtuvien virheiden määrää.

**Huomautus**: On suositeltavaa käyttää niitä numerosarjan koodeja, jotka on mainittu CRONUS-esittely-yrityksen **Numerosarjaluettelo**-ikkunassa. Koodit, kuten *O-LASKU+*, eivät ehkä avaudu heti, mutta [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on tiettyjä oletusasetuksia, jotka perustuvat näihin numerosarjan koodeihin.

Numerointijärjestelmä luodaan määrittämällä koodeja kullekin perustietotyypille tai asiakirjalle. Voit määrittää koodin esimerkiksi asiakkaiden, myyntilaskujen ja yleisten päiväkirjojen numerointia varten. Kun olet määrittänyt koodin, sinun on määritettävä vähintään yksi numerosarjarivi. Numerosarjarivit sisältävät erilaisia tietoja, kuten sarjan ensimmäisen ja viimeisen numeron sekä alkupäivämäärän. Voit määrittää yhtä numerosarjakoodia kohti useita numerosarjarivejä, joilla kullakin on eri alkupäivämäärä. Numerosarjoja käytetään peräkkäin kulloisestakin alkupäivämäärästä alkaen.

Numerosarjat määritetään yleensä lisäämään seuraava peräkkäinen numero automaattisesti luotuihin uusiin kortteihin tai asiakirjoihin. Voit kuitenkin määrittää myös numerosarjoja, joissa uuden numeron voi antaa manuaalisesti. Tässä määrityksessä on käytössä **Manuaaliset nrot** -valintaruutu.

Jos haluat käyttää useita numerosarjakoodeja yhdelle perustietotyypille (esimerkiksi silloin, kun haluat eri numerosarjoja eri nimikeluokille), voit käyttää numerosarjasuhteita.

## <a name="to-create-a-new-number-series"></a>Uuden numerosarjan luominen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nrosarja** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat uuden rivin kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**VIHJE**: Jos haluat, että uusiin kortteihin tai asiakirjoihin voi antaa numeron manuaalisesti, poista **Oletusnrot**-valintaruudun valinta ja valitse **Manuaaliset nrot** -valintaruutu.

Kun nyt luot uuden kortin tai asiakirjan, joka on määritetty käyttämään kyseistä numerosarjaa, voit antaa **Nro**-kenttään sopivan arvon.  

## <a name="to-set-up-where-a-number-series-is-used"></a>Numerosarjan käyttökohteen määrittäminen
Seuraavaksi selitetään, miten myyntialueen numerosarja määritetään. Myös muut alueet määritetään vastaavasti.
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Myynnit ja myyntisaamiset** ja valitse sitten liittyvä linkki.
2. Valitse **Myynnit ja myyntisaamiset** -ikkunan **Numerosarja**-pikavälilehdessä sopiva numerosarja kullekin myyntikortille tai -asiakirjalle.

Valitulla numerolla täytetään kyseisen kortin tai asiakirjan **Nro**-kenttä numerosarjarivillä tehtyjen asetusten mukaisesti.

## <a name="to-create-relationships-between-number-series"></a>Numerosarjojen suhteiden luonti
Jos tietylle perustiedolle tai tapahtumalle on luotu useampia numerosarjoja, näiden koodien välille voidaan luoda suhteita. Tämä toiminto auttaa koodien valinnassa kun käytetään numeroa.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nrosarja** ja valitse sitten liittyvä linkki.
2. Valitse numerosarjoja sisältävä rivi, jolle haluat luoda suhteita. Valitse sitten **Suhteet**.
3. Kirjoita **Sarjakoodi**-kenttään sen numerosarjan koodi, johon haluat luoda suhteen vaiheessa 2 valitusta sarjasta.
4. Lisää rivi kullekin valittuun numerosarjaan liitettävälle koodille.
5. Sulje ikkuna.

Kun tarvitset numeron voit käyttää niitä suhteita, joita on luotu numerosarjojen valitsemiseksi.

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  

