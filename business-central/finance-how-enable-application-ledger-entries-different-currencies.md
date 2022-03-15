---
title: Eri valuutoissa olevien tapahtumien kohdistaminen
description: Jos asiakkaan maksu vastaanotetaan eri valuuttana kuin myytäessä käytetty valuutta, voidaan kirjanpitotapahtumat kohdistaa useana valuuttana.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.search.form: 148, 460, 25
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 24a0465b787afb6f78a82869f1025ffe60bd02ee
ms.sourcegitcommit: 6d48c1f601ed22b6b0358311baf63c073ab75e64
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/01/2022
ms.locfileid: "8366826"
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a>Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa

Jos ostat toimittajalta yhdessä valuutassa ja maksat maksun toisessa valuutassa, maksu voidaan kohdistaa ostoon.

Ja jos asiakkaalle myydään yhdessä valuutassa ja maksu vastaanotetaan toisessa valuutassa, maksu voidaan kohdistaa myyntilaskuun.

Seuraavassa kuvataan, miten tämä määritetään toimittajatapahtumille **Ostojen ja ostovelkojen asetukset** -sivulla. Asetukset tehdään samoin kuin asiakastapahtumille **Myyntien ja myyntisaamisten asetukset** -sivulla.

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Toimittajatapahtumien kohdistamisen ottaminen käyttöön eri valuutoissa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostojen ja maksettavien määritys** ja valitse sitten vastaava linkki.
2. Valitse **Valuuttojen välinen kohdistus** -kentässä jokin seuraavista vaihtoehdoista.

| Asetus | Kuvaus |
| --- | --- |
| Ei yhtään |Valuuttojen välistä kohdistusta ei sallita. |
| EMU |EMU-valuuttojen välinen kohdistus sallitaan. |
| Kaikki |Kaikkien valuuttojen välinen kohdistus sallitaan. |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a>KP-tilien määrittäminen valuutan kohdistuksen pyöristyseroille

Jos eri valuutoissa olevia tapahtumia kohdistetaan, täytyy määrittää KP-tilit, jolle haluat kirjata pyöristyserot.  

> [!NOTE]  
> Sinun on määritettävä pääkirjanpidon tilit, ennen kuin viimeistelet tehtävän. Lisätietoja on kohdassa [Tietoja pääkirjanpidosta ja tilikartasta](finance-general-ledger.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaan kirjausryhmät** ja valitse sitten vastaava linkki.  
2. Anna **Debet val. kohd. pyör. tili**- ja **Kredit val. kohd. pyör. tili** -kenttiin asianmukaiset pääkirjanpitotilit, joihin pyöristyserot kirjataan.  
3. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajan kirjausryhmät** ja valitse sitten vastaava linkki.  
4. Anna **Debet val. kohd. pyör. tili**- ja **Kredit val. kohd. pyör. tili** -kentissä pääkirjanpitotilit, joihin pyöristyserot kirjataan.  

## <a name="see-also"></a>Katso myös

[Ostovelkojen hallinta](payables-manage-payables.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]