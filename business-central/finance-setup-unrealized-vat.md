---
title: Ei-realisoituneen arvonlisäveron määrittäminen
description: Jos käytät kassaperusteista kirjanpitoa, voit määrittää, miten myynnin ja ostojen ei-realisoitunut ALV käsitellään.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.search.form: 118, 472, 473
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 1ae48b042cf3df00a1d62a6871136e2526b3db0c
ms.sourcegitcommit: 3ca91139035b34cfe0b0303e4caff7c6d02d0d14
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/14/2022
ms.locfileid: "8417693"
---
# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a>Ei-realisoituneen arvonlisäveron määrittäminen kassaperusteista kirjanpitoa varten

Jos käytät kassaperusteista kirjanpitoa, voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in käsittelemään ei-realisoidun arvonlisäveron.

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a>Pääkirjanpidon tilien käyttäminen ei-realisoitunutta arvonlisäveroa varten

ALV-summat voidaan laskea ja kirjata väliaikaiselle kirjanpitotilille laskun kirjaamisen yhteydessä. Sen jälkeen ne voidaan kirjata oikealle kirjanpitotilille ja sisällyttää ALV-ilmoituksiin laskun maksun kirjaamisen yhteydessä. Ennen sitä sinun täytyy [määrittää ALV-kirjausasetukset](finance-setup-vat.md).

Käytä ei-realisoituneen arvonlisäveron tilejä seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake ja syötä **Kirjanpidon asetukset**.
2. Valitse **Pääkirjanpidon asetukset**-sivulla **Ei-realisoitunut ALV** -valintaruutu.
3. Valitse **Hae sivua tai raporttia** -kuvake ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") ja syötä **ALV-kirjausten asetukset**.
4. Valitse ensin **ALV-kirjausten asetukset** -sivulla ALV-kirjausryhmä ja sitten **Muokkaa**-toiminto.
5. Valitse **Ei-realisoituneen ALV:n tyyppi** -kentässä vaihtoehto määrittämään maksujen kohdistus laskun summalle (ilman ALV:tä) ja itse ALV-summalle, ja miten ALV-summat siirretään ei-realisoituneen ALV:n tililtä realisoituneelle tilille. Asetukset kuvaillaan seuraavassa taulukossa.

| Asetus | Kuvaus |
| --- | --- |
| Tyhjä | Valitse tämä vaihtoehto, jos et halua käyttää ei-realisoitunuttu ALV-toimintoa. |
| Prosentti | Maksut kattavat sekä ALV-summan että laskun summan siinä suhteessa, kuinka suuri osa kyseinen maksu on jäljellä olevasta laskun summasta. Maksettu ALV-summa siirretään ei-realisoituneen ALV:n tililtä realisoituneen ALV:n tilille. |
| Ensimmäinen | Maksut kattavat ensin ALV:n ja sitten laskun summat. Tässä tapauksessa ei-realisoituneen ALV:in tililtä siirretään ALV-tilille yhtä suuri summa kuin maksun summa kunnes ALV on kokonaisuudessaan maksettu. |
| Viimeinen | Maksut kattavat ensin laskun summan ja sitten ALV:n. Tässä tapauksessa mitään summaa ei siirretä ei-realisoituneen ALV:in tililtä ALV-tilille ennen kuin koko laskun summa, ilman ALV:tä, on maksettu. |
| Ensimmäinen (kokonaan maksettu) | Maksut kattavat ensin ALV:n (kuten _Ensimmäinen_-vaihtoehdossa), mutta mitään summaa ei siirretä ALV-tilille ennen kuin koko ALV-summa on maksettu. |
| Viimeinen (kokonaan maksettu) | Maksut kattavat ensin laskun summan (kuten _Viimeinen_-vaihtoehdossa), mutta mitään summaa ei siirretä ALV-tilille ennen kuin koko ALV-summa on maksettu. |

6. Valitse myynnin ei-realisoituneen ALV:n tili **Ei-real. myynti-ALV:n tili** -kentässä.

    > [!NOTE]  
    > ALV-summa kirjataan tälle tilille, jossa se on asiakkaan maksun kirjaamisen saakka. Summa siirretään sitten myynnin ALV-tilille.
7. Määritä ostojen ei-realisoituneen ALV:n KP-tili **Ostojen ei-realis. ALV:n tili** -kentässä.

> [!NOTE]  
> ALV-summa kirjataan tälle tilille, jossa se on asiakkaan maksun kirjaamisen saakka. Summa siirretään sitten oston ALV-tilille.

## <a name="see-also"></a>Katso myös
[Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen](finance-setup-vat.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
