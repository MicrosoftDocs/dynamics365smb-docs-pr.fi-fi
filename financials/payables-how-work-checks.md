---
title: "Toimintaohje: Sekkien käsitteleminen| Microsoft Docs"
description: "Toimintaohje: Sekkien käsitteleminen"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6debfe7d1f5e9726ba1f70d023076d73f123ef24
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-work-with-checks"></a>Toimintaohje: Sekkien käsitteleminen
Voit myöntää sähköisiä ja manuaalisia sekkejä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Molemmissa menetelmissä sekit myönnetään toimittajille maksupäiväkirjaa käyttäen. Ohjelman avulla voit myös mitätöidä sekkejä ja tarkastella sekkitapahtumia.

Sekkien myöntämiskäsittelyyn kuuluvat maksujen ehdottaminen, tapahtumien luominen ja tietokonesekkien tulostaminen.

**Huomautus**: Voit varmistaa lähettämällä toimittaja-, sekki- ja maksutiedot sisältävän tiedoston, että pankki vahvistaa vain tarkistetut sekit ja summat. Lisätietoja on kohdassa [Toimintaohje: Positive Pay -tiedostojen vieminen](finance-how-positive-pay.md).

Tulostin on määritettävä oikein sekkimuotoja varten. Myös käytettävä sekkien asettelu on määritettävä. Lisätietoja on kohdassa [Toimintaohje: Sekkien asetteluiden määrittäminen](finance-how-define-check-layouts.md)

## <a name="to-issue-checks"></a>Sekkien myöntäminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Maksupäiväkirjat** ja valitse sitten liittyvä linkki.
2. Täytä asianmukaisten maksujen tiedot päiväkirjaan esimerkiksi Ehdota toimittajamaksuja -toiminnon avulla. Lisätietoja on kohdassa [Toimintaohje: Toimittajamaksujen ehdottaminen](payables-how-suggest-vendor-payments.md).
3. Valitse sekkien avulla tehtävän maksun päiväkirjan rivillä **Pankkimaksun tyyppi** -kentässä jokin seuraavista vaihtoehdoista:

   * **Tietokonesekki**: Valitse tämä vaihtoehto, jos haluat tulostaa sekin maksupäiväkirjan tällä rivillä olevalle summalle. Tulosta sekit, ennen kuin kirjaat päiväkirjan rivit. Voit valita **Tietokonesekki**-kohdan vain, jos **Vastatilin tyyppi** tai **Tilin tyyppi** on **Pankkitili**.
   * **Manuaalinen sekki**: Valitse tämä vaihtoehto, jos olet luonut sekin manuaalisesti ja haluat luoda vastaavan sekkitapahtuman tälle summalle. Tämän vaihtoehdon avulla et voi tulostaa sekkejä [!INCLUDE[d365fin](includes/d365fin_md.md)]ista. Voit valita **Manuaalinen sekki** -kohdan vain, jos **Vastatilin tyyppi** tai **Tilin tyyppi** on **Pankkitili**.

     **Huomautus**: Tulosta tietokonesekit, ennen kuin kirjaat liittyvät päiväkirjan rivit.
4. Jos kyseessä on tietokonesekki, valitse **Tulosta sekki**.
5. Täytä **Sekki**-ikkunassa tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Valitse **Tulosta**-painike.

**Huomautus**: Jos haluat tulostaa sekkejä monessa valuutassa eri pankkitileiltä, sinun täytyy suorittaa **Tulosta sekki** -eräajo erikseen kullekin valuutalle ja määrittää sopivat pankkitilit.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Kirjaamattomien ja tulostettujen sekkien peruuttaminen
Voit peruuttaa kirjaamattomat sekit niiden tulostamisen jälkeen **Maksupäiväkirja**-ikkunan **Mitätöi sekki** -toiminnon avulla.

1. Valitse **Maksupäiväkirja**-ikkunassa **Mitätöi sekki** ja valitse peruutettavat sekit.

## <a name="to-void-checks"></a>Sekkien mitätöiminen
Kun sekkimaksu on kirjattu, voit peruuttaa (mitätöidä) sekit vain tuloksena syntyvistä pankkitapahtumista.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Valitse oikea pankkitili, valitse **Muokkaa**-toiminto ja valitse sitten **Sekkitapahtumat**-toiminto.
3. Valitse **Sekkitapahtumat**-ikkunassa **Mitätöi sekki** -toiminto.
4. Valitse **Mitätöi vain sekki** -valintaruutu.
5. Valitse **OK**-painike.

## <a name="see-also"></a>Katso myös
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Toimintaohje: Positive Pay -tiedoston vieminen](finance-how-positive-pay.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  
