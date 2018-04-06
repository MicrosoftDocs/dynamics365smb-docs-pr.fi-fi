---
title: "Ei-realisoituneen arvonlisäveron määrittäminen | Microsoft Docs"
description: "Jos käytät kassaperusteista kirjanpitoa, voit määrittää, miten myynnin ja ostojen ei-realisoitunut ALV käsitellään."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.date: 09/08/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 09759cc8538e0870c0801df73e9c869a0cab4b34
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a>Ei-realisoituneen arvonlisäveron määrittäminen kassaperusteista kirjanpitoa varten
Jos käytät kassaperusteista kirjanpitoa, voit määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in käsittelemään ei-realisoidun arvonlisäveron.

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a>Pääkirjanpidon tilien käyttäminen ei-realisoitunutta arvonlisäveroa varten
ALV-summat voidaan laskea ja kirjata väliaikaiselle kirjanpitotilille laskun kirjaamisen yhteydessä. Sen jälkeen ne voidaan kirjata oikealle kirjanpitotilille ja sisällyttää ALV-ilmoituksiin laskun maksun kirjaamisen yhteydessä. Ennen sitä sinun täytyy määrittää ALV-kirjausasetukset.

Käytä ei-realisoituneen arvonlisäveron tilejä seuraavasti:
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake ja anna **Pääkirjanpidon asetukset**.
2. Valitse **Pääkirjanpidon asetukset** -sivun **Yleiset**-pikavälilehdessä **Näytä lisää** ja valitse sitten **Ei-realisoitunut ALV** -valintaruutu.
3. Sulje sivu.
4. Valitse **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") ja kirjoita **ALV-kirjausten asetukset**.
5. Valitse ensin **ALV-kirjausten asetukset** -sivulla ALV-kirjausryhmä ja sitten **Muokkaa**.
6. Valitse **Ei-realisoituneen ALV:n tyyppi** -kentässä vaihtoehto määrittämään maksujen kohdistus laskun summalle (ilman ALV:tä) ja itse ALV-summalle, ja miten ALV-summat siirretään ei-realisoituneen ALV:n tililtä realisoituneelle tilille. Asetukset kuvaillaan seuraavassa taulukossa.

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
>   ALV-summa kirjataan tälle tilille, jossa se on asiakkaan maksun kirjaamisen saakka. Summa siirretään sitten myynnin ALV-tilille.
7. Määritä ostojen ei-realisoituneen ALV:n KP-tili **Ostojen ei-realis. ALV:n tili** -kentässä.

    > [!NOTE]  
    >   ALV-summa kirjataan tälle tilille, jossa se on asiakkaan maksun kirjaamisen saakka. Summa siirretään sitten oston ALV-tilille.

## <a name="see-also"></a>Katso myös
[Arvolisäveron määrittäminen](finance-setup-vat.md)

