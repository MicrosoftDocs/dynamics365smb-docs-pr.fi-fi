---
title: Numerosarjan luominen | Microsoft Docs
description: "Katso, miten määritetään numerosarjat, jotka määrittävät yksilölliset tunnuskoodit Business Central -sovelluksen tileille ja asiakirjoille."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 46131d6ad5f77a02ffe33d24f1210a226c3041c1
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="create-number-series"></a>Numerosarjojen luominen
Jokaiselle yritykselle on määritettävä yksilölliset tunnuskoodit esimerkiksi pääkirjanpidon tilejä, asiakas- ja toimittajatilejä, laskuja ja muita asiakirjoja varten. Numerointi ei ole tärkeää pelkästään tunnistamisen kannalta. Hyvin suunniteltu numerointijärjestelmä helpottaa myös yrityksen hallittavuutta ja analysointia ja voi vähentää tietojen syötössä tapahtuvien virheiden määrää.

> [!NOTE]  
>   On suositeltavaa käyttää niitä numerosarjan koodeja, jotka on mainittu CRONUS-esittely-yrityksen **Numerosarjaluettelo**-sivulla. Koodit, kuten *O-LASKU+*, eivät ehkä avaudu heti, mutta [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on tiettyjä oletusasetuksia, jotka perustuvat näihin numerosarjan koodeihin.

Numerointijärjestelmä luodaan määrittämällä koodeja kullekin perustietotyypille tai asiakirjalle. Voit määrittää koodin esimerkiksi asiakkaiden, myyntilaskujen ja yleisten päiväkirjojen numerointia varten. Kun olet määrittänyt koodin, sinun on määritettävä vähintään yksi numerosarjarivi. Numerosarjarivit sisältävät erilaisia tietoja, kuten sarjan ensimmäisen ja viimeisen numeron sekä alkupäivämäärän. Voit määrittää yhtä numerosarjakoodia kohti useita numerosarjarivejä, joilla kullakin on eri alkupäivämäärä. Numerosarjoja käytetään peräkkäin kulloisestakin alkupäivämäärästä alkaen.

Numerosarjat määritetään yleensä lisäämään seuraava peräkkäinen numero automaattisesti luotuihin uusiin kortteihin tai asiakirjoihin. Voit kuitenkin määrittää myös numerosarjoja, joissa uuden numeron voi antaa manuaalisesti. Se määritetään **Manuaaliset nrot** -valintaruudussa.

Jos haluat käyttää useita numerosarjakoodeja yhdelle perustietotyypille (esimerkiksi silloin, kun haluat eri numerosarjoja eri nimikeluokille), voit käyttää numerosarjasuhteita.

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Nro-kentän toiminta asiakirjoissa ja korteissa
Myynti-, osto- ja siirtoasiakirjojen ja korttien **Nro** voidaan täyttää automaattisesti numerosarjasta tai manuaalisesti. Lisäksi voidaan määrittää näkymättömäksi.

**Nro**-kenttä voidaan täyttää kolmella tavalla:

1. Jos asiakirjantyypillä tai kortilla on vain yksi numerosarja, jossa **Oletusnrot**-valintaruutu on valittu mutta **Manuaaliset nrot** -valintaruutua ei ole valittu, kenttä täytetään automaattisesti sarjan seuraavalla numerolla. **Nro**-kenttä ei silloin näy.

    > [!NOTE]  
    > Jos numerosarja ei toimi esimerkiksi siksi, että sen numerot ovat loppuneet, tällöin **Nro**-kenttä on näkyvissä ja voit kirjoittaa numeron manuaalisesti tai ratkaista ongelmat **Numerosarjaluettelo**-sivulla.

2. Jos asiakirjatyypillä tai kortilla on useita numerosarjoja eikä nykyisen kohdistetun numerosarjan **Oletusnrot**-valintaruutua ole valittu, **Nro**-kenttä näkyy ja voit valita käytettävän numerosarjan **Numerosarjaluettelo**-sivulla. Sarjan seuraava numero lisätään sitten **Nro** -kentässä.

3. Jos asiakirjatyypin tai kortin numerosarjaa ei ole määritetty tai jos numerosarjoille on valittu **Manuaaliset nrot** -kenttä, **Nro**-kenttä näkyy ja numerot on annettava manuaalisesti. Voit kirjoittaa enintään 20 merkkiä, sekä numeroita että kirjaimia.

Kun uuden asiakirjan tai kortin, jolla on jo numerosarja, vastaava **Numerosarja-asetukset**-sivu avautuu. Voit määrittää tällä sivulla kyseisen asiakirjatyypin tai kortin numerosarjan, ennen kuin jatkat muiden tietojen antamista.

> [!NOTE]  
> Jos manuaalinen numerointi on otettava käyttöön esimerkiksi uusissa korteissa, jotka luoneessa tietojen siirtoprosessissa **Nro**-kenttä on oletusarvoisesti piilotettu, siirry **Varastonhallinnan asetukset** -sivulle ja valitse **Nimikenrot**-kenttä. Voit nyt avata ja määrittää liittyvien numerosarjojen asetuksiksi **Manuaaliset nrot**.

## <a name="to-create-a-new-number-series"></a>Uuden numerosarjan luominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nrosarja** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat uuden rivin kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-where-a-number-series-is-used"></a>Numerosarjan käyttökohteen määrittäminen
Seuraavaksi selitetään, miten myyntialueen numerosarja määritetään. Myös muut alueet määritetään vastaavasti.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myynti ja myyntisaamiset** ja valitse sitten liittyvä linkki.
2. Valitse **Myynnit ja myyntisaamiset** -sivun **Numerosarja**-pikavälilehdessä sopiva numerosarja kullekin myyntikortille tai -asiakirjalle.

Valitulla numerolla täytetään kyseisen kortin tai asiakirjan **Nro**-kenttä numerosarjarivillä tehtyjen asetusten mukaisesti.

## <a name="to-create-relationships-between-number-series"></a>Numerosarjojen suhteiden luonti
Jos tietylle perustiedolle tai tapahtumalle on luotu useampia numerosarjoja, näiden koodien välille voidaan luoda suhteita. Tämä toiminto auttaa koodien valinnassa kun käytetään numeroa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nrosarja** ja valitse sitten liittyvä linkki.
2. Valitse numerosarjoja sisältävä rivi, jolle haluat luoda suhteita. Valitse sitten **Suhteet**.
3. Kirjoita **Sarjakoodi**-kenttään sen numerosarjan koodi, johon haluat luoda suhteen vaiheessa 2 valitusta sarjasta.
4. Lisää rivi kullekin valittuun numerosarjaan liitettävälle koodille.
5. Sulje sivu.

Kun tarvitset numeron voit käyttää niitä suhteita, joita on luotu numerosarjojen valitsemiseksi.

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

