---
title: Ei-realisoituneen arvonlisäveron määrittäminen | Microsoft Docs
description: Jos käytät kassaperusteista kirjanpitoa, voit määrittää, miten myynnin ja ostojen ei-realisoitunut ALV käsitellään.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 69e4d4f4e924edd7eea45da73a3b0b5f71dd8cc0
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "928791"
---
# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a>Ei-realisoituneen arvonlisäveron määrittäminen kassaperusteista kirjanpitoa varten
Jos käytät kassaperusteista kirjanpitoa, voit määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in käsittelemään ei-realisoidun arvonlisäveron.

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a>Pääkirjanpidon tilien käyttäminen ei-realisoitunutta arvonlisäveroa varten
ALV-summat voidaan laskea ja kirjata väliaikaiselle kirjanpitotilille laskun kirjaamisen yhteydessä. Sen jälkeen ne voidaan kirjata oikealle kirjanpitotilille ja sisällyttää ALV-ilmoituksiin laskun maksun kirjaamisen yhteydessä. Ennen sitä sinun täytyy määrittää ALV-kirjausasetukset.

Käytä ei-realisoituneen arvonlisäveron tilejä seuraavasti:
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake ja syötä **Pääkirjanpidon asetukset**.
2. Valitse **Pääkirjanpidon asetukset**-sivulla **Ei-realisoitunut ALV** -valintaruutu.
3. valitse **Etsi sivua tai raporttia** -kuvake ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") ja anna **ALV-kirjausten asetukset**.
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
[Arvolisäveron määrittäminen](finance-setup-vat.md)
