---
title: Ennakkolaskumaksujen luominen | Microsoft Docs
description: Lisätietoja tilanteiden käsittelyssä, jossa edellytät itse ennakkomaksua toimittajasi edellyttää sitä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 96433274efa8ea8f5ec93248f4a7c992e456aa26
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "912239"
---
# <a name="create-prepayment-invoices"></a>Ennakkomaksulaskujen luominen
Jos haluat, että asiakkaat lähettävät maksun ennen kuin toimitat heille tilauksen tai jos toimittaja haluaa maksun ennen kuin toimitus lähetetään sinulle, voit käyttää Ennakkomaksu-toimintoa.  

Kun olet luonut myynti- tai ostotilauksen, voit luoda ennakkomaksun laskun. Voit käyttää kullekin myynti- tai ostoriville oletusprosenttiosuuksia tai voit muuttaa laskun summia tarpeen mukaan. Voit määrittää esimerkiksi koko tilauksen yhteissumman.  

Seuraavaksi käsitellään myyntitilausten ennakkomaksun laskuttamista. Ostotilausten vaiheet ovat vastaavanlaiset.  

## <a name="to-create-a-prepayment-invoice"></a>Ennakkomaksulaskun luominen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.  
2. Luo uusi myyntitilaus. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).  

    **Ennakkomaksu**-pikavälilehden **Ennakkomaksuprosentti**-kenttä täytetään automaattisesti, jos asiakaskortissa on oletusennakkomaksuprosentti. Kentän sisältöä voidaan muuttaa. Ennakkomaksun osuus kopioidaan otsikosta vain niille riveille, jotka eivät kopioi ennakkomaksun vakio-osuutta nimikkeeltä.  

    Jos **Tiivistä ennakkomaksu** -kenttä on valittuna, rivit yhdistetään laskussa, jos:  
    - Riveillä on sama KP-tili ennakkomaksuja varten (yleisten kirjausasetusten mukaisesti).  
    - Riveillä on samat dimensiot.  

    Jätä kenttä tyhjäksi, jos haluat määrittää ennakkomaksulaskun, jossa on yksi rivi kutakin ennakkomaksuprosentin sisältävää myyntitilausriviä varten.  

3. Täytä myyntirivit.  

    Jos nimikkeille on määritetty oletusennakkomaksuprosentit, ohjelma kopioi oletusarvon automaattisesti rivin **Ennakkomaksuprosentti**-kenttään. Muussa tapauksessa ennakkomaksuprosentti kopioidaan tunnistetiedoista. Voit muuttaa rivin **Ennakkomaksuprosentti**-kentän sisällön.  
4. Jos haluat kohdistaa yhden etumaksuprosentin koko tilaukseen, muuta tunnistetietojen **Ennakkomaksuprosentti**-kentän arvo rivien täyttämisen jälkeen.  
5. Valitse **Tilastot**-toiminto, jos haluat tarkastella ennakkomaksun kokonaissummaa.

    Jos haluat muuttaa ennakkomaksun kokonaissummaa, voit muuttaa **Myyntitilaustilastot**-sivun **Ennakkomaksun summa** -kentän sisältöä.  

    Jos **Hinnat sisältävät ALV:n** -kenttä on valittuna, **Ennakkomaksun summa sis. ALV:a** -kenttää voi muokata.  

    Jos muutat **Ennakkomaksun summa** -kentän sisältöä, summa jaetaan suhteellisesti muiden rivien kesken, paitsi niiden, joiden **Ennakkomaksuprosentti**-kentän arvo on **0**.  
6. Voit tulostaa testiraportin ennen ennakkomaksulaskun kirjaamista valitsemalla ensin **Ennakkomaksu**- ja sitten **Ennakkomaksun testiraportti** -toiminnon.  
7. Voit kirjata ennakkomaksulaskun valitsemalla ensin **Ennakkomaksu**- ja sitten **Kirjaa ennakkomaksulasku** -toiminnon.  

    Voit kirjata ja tulostaa ennakkomaksulaskun valitsemalla **Kirjaa ja tulosta ennakkomaksulasku** -toiminnon.  

Voit antaa lisää tilauksen ennakkomaksulaskuja. Tee tämä nostamalla yhden tai useamman rivin ennakkomaksua ja muuttamalla tarvittaessa asiakirjan päivämäärää ja kirjaamalla ennakkomaksulasku. Uusi lasku luodaan ennakkomaksun toistaiseksi laskutettujen summien ja uuden ennakkomaksun summan välisen eron vuoksi.  

> [!NOTE]  
>  Jos sijaintisi on Pohjois-Amerikassa, et voi muuttaa ennakkomaksun osuutta sen jälkeen, kun ennakkomaksulasku on kirjattu. Tämä on estetty pohjoisamerikkalaisessa [!INCLUDE[d365fin](includes/d365fin_md.md)] -versiossa, koska arvonlisäveron laskutoimitus tuottaa muutoin väärän tuloksen.  

 Kun olet valmis kirjaamaan loput laskusta, kirjaa se kuten mikä tahansa lasku. Ennakkomaksusumma vähennetään automaattisesti erääntyvästä summasta.  

## <a name="see-also"></a>Katso myös  
[Ennakkomaksujen laskuttaminen](finance-invoice-prepayments.md)  
[Vaihekuvaus: Myynnin ennakkomaksujen määrittäminen ja laskuttaminen](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
