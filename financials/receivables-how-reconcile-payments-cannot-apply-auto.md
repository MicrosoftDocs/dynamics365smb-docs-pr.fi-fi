---
title: "Maksujen täsmäyttäminen eron tilille siirron toiminnolla | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten käsitellään maksut, joita ei voi kohdistaa asiakirjaan esimerkiksi silloin, kun summat eivät ole samat vaihtokurssin vuoksi."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 37d2d8af5086a9f633cb90abb380578b4ca73136
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-reconcile-payments-that-cannot-be-applied-automatically"></a>Toimintaohje: Niiden maksujen täsmäyttäminen, joita ei voi kohdistaa automaattisesti
Joskus pankkitilillä käsitellään maksuja, joita ei voi kohdistaa liittyvään avoimeen asiakas-, toimittaja- tai pankkitapahtumaan. Syy voi olla se, että [!INCLUDE[d365fin](includes/d365fin_md.md)]issa ei ole asiakirjaa, johon maksu voitaisiin kohdistaa, tai [!INCLUDE[d365fin](includes/d365fin_md.md)]in liittyvä asiakirja sisältää eri summan kuin tapahtuman summa esimerkiksi valuuttamuutoksen vuoksi. Kaikki niiden maksujen tapahtumien summat, joita ei ole vielä kohdistettu, näkyvät **Maksujen täsmäytyskirjauskansio** -ikkunan **Ero**-kentässä. Siellä näkyvät esimerkiksi summat, joita ei voi kohdistaa edellä mainittujen syiden vuoksi.

Maksut, joita ei voi kohdistaa, voivat näkyä maksujen täsmäytyskirjauskansion riveillä seuraavilla tavoilla:

* **Ero**-kentän arvo on sama kuin **Tapahtuman summa** -kentän arvo. Tämä tarkoittaa sitä, että mitään maksun osaa ei voi kohdistaa liittyvään avoimeen asiakas-, toimittaja- tai pankkitapahtumaan.
* **Ero**-kentän arvo on pienempi kuin **Tapahtuman summa** -kentän arvo. Tämä tarkoittaa sitä, että osa maksusta voidaan kohdistaa liittyvään avoimeen asiakas-, toimittaja- tai pankkitapahtumaan. Maksun jäljellä olevaa osaa ei voi kohdistaa. Se on täsmäytettävä manuaalisesti tai kirjaamalla se suoraan tilille.

Voit täsmäyttää tällaiset maksut valitsemalla Siirrä erotus tilille -painike ja määrittämällä, mille tilille Ero-kentän summa kirjataan, kun teet kirjauksen maksujen täsmäytyskirjauskansioon.

> [!NOTE]  
>   Vastaavan toiminnon avulla voit määrittää automaattisen täsmäytyksen toistuville maksuille, joita ei voi kohdistaa liittyviin avoimiin asiakas-, toimittaja- tai pankkitapahtumiin. Lisätietoja on kohdassa [Toimintaohje: Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

## <a name="to-reconcile-payments-that-cannot-be-applied"></a>Niiden maksujen täsmäyttäminen, joita ei voi kohdistaa
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksujen täsmäytyskirjauskansio** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa maksun täsmäytyksen päiväkirja. Lisätietoja on kohdassa [Toimintaohje: Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).
3. Valitse **Siirrä erotus tilille**. **Siirrä erotus tilille** -ikkuna avautuu.
4. Määritä **Tilityyppi**-kenttään sen tilin tyyppi, johon maksun summa kirjataan.
5. Valitse **Tilinumero**-kenttään tili, jolle maksun summa kirjataan.
6. Määritä **Kuvaus**-kenttään teksti, joka kuvaa tätä suoran maksun kirjausta. Oletusarvoisesti lisätään maksujen täsmäytyskirjauskansion rivin **Tapahtuman teksti** -kentän teksti.
7. Valitse **OK**-painike.

Jos **Ero**-kentän arvo on sama kuin **Tapahtuman summa** -kentän arvo, kun kirjaat maksujen täsmäytyskirjauskansion, koko päiväkirjan rivin maksu kirjataan suoraan määritetylle vastatilille.

Jos **Ero**-kentän arvo on pienempi kuin **Tapahtuman summa** -kentän arvon, samalla tekstillä ja päivämäärällä luodaan päiväkirjan lisärivi ja ero lisätään **Tapahtuman summa** -kenttään. Alkuperäisen päiväkirjan rivin ero vähennetään **Tapahtuman summa** -kentän arvosta ja maksun kohdistus siihen liittyvään asiakas-, toimittaja- tai pankkitilitapahtumaan säilyy. Kun kirjaat maksun täsmäytyskirjauskansion, yksi maksun osa kirjataan kohdistettuna maksuna. Maksun toinen osa kirjataan suoraan määritetylle tilille.

## <a name="see-also"></a>Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

