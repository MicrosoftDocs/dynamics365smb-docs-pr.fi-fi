---
title: Ennakkolaskumaksujen luominen | Microsoft Docs
description: Lisätietoja tilanteiden käsittelyssä, jossa edellytät itse ennakkomaksua toimittajasi edellyttää sitä.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2020
ms.author: edupont
ms.openlocfilehash: 85a5bbd3c1920aaac3e0560737f921c7518d1d32
ms.sourcegitcommit: 63102669366eb26f9c32729848170bc2e5c4d6ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503592"
---
# <a name="create-prepayment-invoices"></a>Ennakkomaksulaskujen luominen

Jos asiakkaiden on lähetettävä maksu, ennen kuin lähetät tilauksen heille, voit käyttää ennakkomaksutoimintoja. Näin voi toimia myös silloin, jos toimittaja edellyttää, että lähetät maksun ennen tilauksen toimittamista.  

Voit aloittaa ennakkomaksuprosessin, kun olet luonut ostotilauksen. Jos kyseisellä asiakkaalla tai toimittajalla on oletusarvoinen ennakkomaksuprosentti, se sisällytetään automaattisesti tuloksena olevaan ennakkomaksulaskuun. Voit määrittää ennakkomaksuprosentin myös koko asiakirjalle.

Kun olet luonut myynti- tai ostotilauksen, voit luoda ennakkomaksun laskun. Voit käyttää kullekin myynti- tai ostoriville oletusprosenttiosuuksia tai voit muuttaa laskun summia tarpeen mukaan. Voit määrittää esimerkiksi koko tilauksen yhteissumman.  

Seuraavaksi käsitellään myyntitilauksen ennakkomaksun laskuttamista. Ostotilausten vaiheet ovat vastaavanlaiset.  

## <a name="to-create-a-prepayment-invoice"></a>Ennakkomaksulaskun luominen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.  
2. Luo uusi myyntitilaus asianomaiselle asiakkaalle. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).  

    **Ennakkomaksu**-pikavälilehden **Ennakkomaksuprosentti**-kenttä määrittää prosentin, jolla ennakkomaksun summa lasketaan. Jos asiakaskortissa on oletusarvoinen ennakkomaksuprosentti, kenttä täytetään automaattisesti. Prosenttia voi muuttaa. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Valitse **Tiivistä ennakkomaksu** -kenttä, jos haluat luoda ennakkomaksulaskuun rivejä, jotka yhdistää myyntitilauksen rivejä seuraavissa tilanteissa:  

    - Riveillä on sama KP-tili ennakkomaksuja varten (yleisten kirjausasetusten mukaisesti).  
    - Riveillä on samat dimensiot.  

    Jos haluat määrittää ennakkomaksulaskun, jossa on yksi rivi kutakin ennakkomaksuprosentin sisältävää myyntitilausriviä varten. älä valitse **Tiivistä ennakkomaksu** -kenttää.  

    Ennakkomaksun eräpäivä lasketaan automaattisesti **Ennakkomaksun maksuehtojen koodi** -arvon perusteella.

3. Täytä myyntirivit.  

    Jos olet määrittänyt oletusarvoisen ennakkomaksuprosentin joko asiakkaalle tai tämän asiakirjan **Ennakkomaksu**-pikavälilehdessä, tämä arvo kopioidaan kullekin riville. Voit muuttaa rivin **Ennakkomaksuprosentti**-kentän sisällön.  

4. Valitse **Tilastot**-toiminto, jos haluat tarkastella ennakkomaksun kokonaissummaa.

    Jos haluat muuttaa ennakkomaksun kokonaissummaa, voit muuttaa **Myyntitilaustilastot**-sivun **Ennakkomaksun summa** -kentän sisältöä.  

    Jos **Hinnat sisältävät ALV:n** -kenttä on valittuna, **Ennakkomaksun summa sis. ALV:a** -kenttää voi muokata.  

    Jos muutat **Ennakkomaksun summa** -kentän sisältöä, summa jaetaan suhteellisesti muiden rivien kesken, paitsi niiden, joiden **Ennakkomaksuprosentti**-kentän arvo on **0**.  

5. Voit tulostaa testiraportin ennen ennakkomaksulaskun kirjaamista valitsemalla ensin **Ennakkomaksu**- ja sitten **Ennakkomaksun testiraportti** -toiminnon.  
6. Voit kirjata ennakkomaksulaskun valitsemalla ensin **Ennakkomaksu**- ja sitten **Kirjaa ennakkomaksulasku** -toiminnon.  

    Voit kirjata ja tulostaa ennakkomaksulaskun valitsemalla **Kirjaa ja tulosta ennakkomaksulasku** -toiminnon.  

Voit antaa lisää tilauksen ennakkomaksulaskuja. Tee tämä nostamalla yhden tai useamman rivin ennakkomaksua ja muuttamalla tarvittaessa asiakirjan päivämäärää ja kirjaamalla ennakkomaksulasku. Uusi lasku luodaan ennakkomaksun toistaiseksi laskutettujen summien ja uuden ennakkomaksun summan välisen eron vuoksi.  

> [!NOTE]  
> Jos sijaintisi on Pohjois-Amerikassa, et voi muuttaa ennakkomaksun osuutta sen jälkeen, kun ennakkomaksulasku on kirjattu. Tämä on estetty pohjoisamerikkalaisessa [!INCLUDE[d365fin](includes/d365fin_md.md)] -versiossa, koska arvonlisäveron laskutoimitus tuottaa muutoin väärän tuloksen.  

 Kun olet valmis kirjaamaan loput laskusta, kirjaa se kuten mikä tahansa lasku. Ennakkomaksusumma vähennetään automaattisesti erääntyvästä summasta.  

## <a name="see-also"></a>Katso myös

[Ennakkomaksujen laskuttaminen](finance-invoice-prepayments.md)  
[Vaihekuvaus: Myynnin ennakkomaksujen määrittäminen ja laskuttaminen](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
