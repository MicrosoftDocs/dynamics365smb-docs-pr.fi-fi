---
title: 'Toimintaohje: Erikoisostohintojen ja -alennusten kirjaaminen| Microsoft Docs'
description: 'Toimintaohje: Ostohintojen ja -alennusten tallentaminen'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 67625231d62a72bb0a62ab362bce92aa16b8956e
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-special-purchase-prices-and-discounts"></a>Toimintaohje: Erikoisostohintojen ja -alennusten kirjaaminen
Eri hinta- ja alennussopimukset, joita käytetään ostettaessa eri toimittajilta, täytyy määrittää, jotta sovittuja sääntöjä ja arvoja sovelletaan toimittajille luotaviin ostoasiakirjoihin.

Kun olet kirjannut myynnin ja ostojen erikoishinnat ja rivialennukset, [!INCLUDE[d365fin](includes/d365fin_md.md)] varmistaa, että nimikekaupan tuotto on aina optimaalinen laskemalla automaattisesti parhaan hinnan myynti- ja ostoasiakirjoille sekä työ- ja nimikepäiväkirjan riville. Lisätietoja on kohdassa [Lisäasetukset: Parhaan hinnan laskenta](advanced-best-price-calculation.md).

Ostoriveille lisätään erikoisostohinta, jos tietty toimittajan, nimikkeen, vähimmäismäärän, mittayksikön sekä aloitus- ja lopetuspäivämäärän yhdistelmä on olemassa.

Voit määrittää seuraavat kaksi ostoalennustyyppiä:

| Alennustyyppi | Kuvaus |
| --- | --- |
| **Ostorivin alennus** |Ostoriveille lisättävä summa-alennus, jos tietty toimittajan, nimikkeen, vähimmäismäärän, mittayksikön sekä aloitus- ja lopetuspäivämäärän yhdistelmä on olemassa. Tätä käytetään samoin kuin ostohinnoissa. |
| **Laskualennus** |Prosenttialennus, joka vähennetään kokonaissummasta, kun ostoasiakirjan kaikkien rivien summa ylittää määritetyn vähimmäisarvon. |

Koska ostorivin alennukset ja ostohinnat perustuvat nimikkeen ja toimittajan yhdistelmään, voit lisätä tämän määrityksen myös nimikkeen kortista, jossa säännöt ja arvot on määritetty. Lisätietoja on kohdassa [Toimintaohje: Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Tietyn ostohinnan määrittäminen toimittajalle
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Toimittajat** ja valitse sitten liittyvä linkki.
2. Avaa asianmukainen toimittajan kortti ja valitse **Hinnat**-toiminto.

    **Ostotyyppi**-kenttään täytetään **toimittajan** tiedot ja **Ostokoodi**-kenttään täytetään toimittajan numero.
3. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Täytä jokaisen sellaisen yhdistelmän rivi, jonka toimittaja myöntää sinulle ostorivialennuksen.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Rivialennuksen määrittäminen toimittajalle
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Toimittajat** ja valitse sitten liittyvä linkki.
2. Avaa asianmukainen toimittajan kortti ja valitse **Rivialennukset**-toiminto.

    **Ostotyyppi**-kenttään täytetään **toimittajan** tiedot ja **Ostokoodi**-kenttään täytetään toimittajan numero.
3. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Täytä jokaisen sellaisen yhdistelmän rivi, jonka toimittaja myöntää sinulle ostorivialennuksen.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Laskualennuksen määrittäminen toimittajalle
Kun toimittajat ovat kertoneet sinulle myöntämänsä laskualennukset, syötä laskun alennuskoodi toimittajien kortteihin ja määritä kunkin koodin ehdot.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Toimittajat** ja valitse sitten liittyvä linkki.
2. Avaa sen toimittajan kortti, jolle myönnetään laskun alennuksia.
3. Valitse **Laskualennuksen koodi** -kentässä asianmukaisille laskualennuksen ehdoille koodi, jonka avulla toimittajan laskualennukset lasketaan.

    **Huomautus**: Laskualennuksen koodit löytyvät olemassa olevien toimittajien korteista. Näin voit nopeasti liittää laskualennusten ehtoja toimittajiin poimimalla sellaisten toimittajien nimet, joilla on samat ehdot.

    Jatka uuden ostolaskun alennusehtojen määrittämiseen.
4. Valitse **Toimittajan kortti** -ikkunassa **Laskualennukset**-toiminto. **Toimittajien laskualennukset** -ikkuna aukeaa.
5. Syötä **Valuutan koodi** -kenttään sen valuutan koodi, johon rivin laskualennuksen ehdot kohdistetaan. Jätä kenttä tyhjäksi, jos laskualennuksen ehdot määritetään Yhdysvaltojen dollareina.
6. Syötä **Vähimmäissumma**-kenttään laskun vähimmäissumma, joka oikeuttaa alennukseen.
7. Syötä **Alennus-%**-kohtaan laskun alennus prosentteina laskun summasta.
8. Toista vaiheet 5–7 jokaiselle valuutalle, jossa toimittaja saa eri laskualennuksen.

Laskualennus on nyt määritetty ja liitetty kyseiselle toimittajalle. Kun valitset toimittajakoodin muiden toimittajien korttien **Laskun alennuskoodi** -kentässä, sama laskualennus liitetään myös näille toimittajille.

## <a name="see-also"></a>Katso myös
[Lisäasetukset: Parhaan hinnan laskenta](advanced-best-price-calculation.md)  
[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

