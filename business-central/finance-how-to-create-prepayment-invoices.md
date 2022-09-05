---
title: Ennakkomaksulaskujen luominen
description: Toiminta tilanteissa, joissa edellytät itse ennakkomaksua tai toimittajasi edellyttää sitä. Käytä kullekin myynti- tai ostoriville oletusprosenttiosuuksia tai muuta laskun summia tarpeen mukaan.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 50, 9305, 9307
ms.date: 12/02/2021
ms.author: edupont
ms.openlocfilehash: 620a1af0deff6f9615b38706dd3f53f3db285008
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/29/2022
ms.locfileid: "9362065"
---
# <a name="create-prepayment-invoices"></a>Ennakkomaksulaskujen luominen

Jos asiakkaiden on lähetettävä maksu, ennen kuin lähetät tilauksen heille, voit käyttää ennakkomaksuominaisuuksia. Näin voi toimia myös silloin, jos toimittaja edellyttää, että maksat ennen tilauksen toimittamista.  

Voit aloittaa ennakkomaksuprosessin, kun olet luonut ostotilauksen. Jos sinulla on oletusarvoinen ennakkomaksuprosentti tilauksen kohteelle tai asiakkaalle tai myyjälle, prosenttiosuus sisällytetään ennakkomaksun laskuun. Voit määrittää ennakkomaksuprosentin myös koko asiakirjalle.

Kun olet luonut myynti- tai ostotilauksen, voit luoda sille ennakkomaksun laskun. Käytä joko kullekin myynti- tai ostoriville oletusprosenttiosuuksia tai muuta laskun summia. Voit määrittää esimerkiksi koko tilauksen yhteissumman.  

Seuraavaksi käsitellään myyntitilauksen ennakkomaksun laskuttamista. Ostotilausten vaiheet ovat vastaavanlaiset.  

## <a name="to-create-a-prepayment-invoice"></a>Ennakkomaksulaskun luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Luo uusi myyntitilaus asianomaiselle asiakkaalle. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).  

    **Ennakkomaksu**-pikavälilehden **Ennakkomaksuprosentti**-kenttä määrittää prosentin, jolla ennakkomaksun summa lasketaan. Jos asiakaskortissa on oletusarvoinen ennakkomaksuprosentti, kenttä täytetään automaattisesti. Prosenttia voi muuttaa. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Valitse **Tiivistä ennakkomaksu** -kenttä, jos haluat luoda ennakkomaksulaskuun rivejä, jotka yhdistää myyntitilauksen rivejä seuraavissa tilanteissa:  

    - Riveillä on sama KP-tili ennakkomaksuja varten (yleisten kirjausasetusten mukaisesti).  
    - Riveillä on samat dimensiot.  

    Jos haluat määrittää ennakkomaksulaskun, jossa on yksi rivi kutakin ennakkomaksuprosentin sisältävää myyntitilausriviä varten. älä valitse **Tiivistä ennakkomaksu** -kenttää.  

    Ennakkomaksun eräpäivä lasketaan automaattisesti **Ennakkomaksun maksuehtojen koodi** -arvon perusteella.

3. Täytä myyntirivit.  

    Jos olet määrittänyt oletusarvoisen ennakkomaksuprosentin joko asiakkaalle tai tämän asiakirjan **Ennakkomaksu**-pikavälilehdessä, tämä arvo kopioidaan kullekin riville. Voit muuttaa rivin **Ennakkomaksuprosentti**-kentän sisällön.  

    > [!TIP]
    > Jos et näe **Ennakkomaksuprosentti**-kenttää, voit lisätä sen mukauttamisen avulla.  Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

4. Valitse **Tilastot**-toiminto, jos haluat tarkastella ennakkomaksun kokonaissummaa.

    Jos haluat muuttaa ennakkomaksun kokonaissummaa, voit muuttaa **Myyntitilaustilastot**-sivun **Ennakkomaksun summa** -kentän sisältöä.  

    Jos **Hinnat sisältävät ALV:n** -kenttä on valittuna, **Ennakkomaksun summa sis. ALV:a** -kenttää voi muokata.  

    Jos muutat **Ennakkomaksun summa** -kentän sisältöä, summa jaetaan suhteellisesti muiden rivien kesken, paitsi rivien, joiden **Ennakkomaksuprosentti**-kentän arvo on **0**.  

5. Voit tulostaa testiraportin ennen ennakkomaksulaskun kirjaamista valitsemalla ensin **Ennakkomaksu**- ja sitten **Ennakkomaksun testiraportti** -toiminnon.  
6. Voit kirjata ennakkomaksulaskun valitsemalla ensin **Ennakkomaksu**- ja sitten **Kirjaa ennakkomaksulasku** -toiminnon.  

    Voit kirjata ja tulostaa ennakkomaksulaskun valitsemalla **Kirjaa ja tulosta ennakkomaksulasku** -toiminnon.  

Voit antaa muita tilauksen ennakkomaksulaskuja. Luo uusi lasku nostamalla yhden tai useamman rivin ennakkomaksua ja muuttamalla tarvittaessa asiakirjan päivämäärää ja kirjaamalla ennakkomaksulasku. Uusi lasku luodaan ennakkomaksun toistaiseksi laskutettujen summien ja uuden ennakkomaksun summan välisen eron vuoksi.  

> [!NOTE]  
> Jos sijaintisi on Pohjois-Amerikassa, et voi muuttaa ennakkomaksun osuutta sen jälkeen, kun ennakkomaksulasku on kirjattu. Tämä on estetty pohjoisamerikkalaisessa [!INCLUDE[prod_short](includes/prod_short.md)] -versiossa, koska arvonlisäveron laskutoimitus tuottaa muutoin väärän tuloksen.  

 Kun olet valmis kirjaamaan loput laskusta, kirjaa se kuten mikä tahansa lasku. Ennakkomaksusumma vähennetään automaattisesti erääntyvästä summasta.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Ennakkoon maksettujen tilausten ja laskujen tilan päivittäminen automaattisesti

Voit nopeuttaa tilausten ja laskujen käsittelemistä määrittämällä työjonotapahtumat, jotka päivittävät kyseisten asiakirjojen tilan automaattisesti. Kun ennakkomaksulasku on maksettu, työjonotapahtumat voivat automaattisesti muuttaa asiakirjan tilan **odottavasta ennakkomaksusta** **lähetetyksi**. Kun määrität työjonon tapahtumia, koodiyksiköt, joita tarvitset, ovat **383 Upd. Pending Prepmt. Sales** ja **383 Upd. Pending Prepmt. Purchase**. On suositeltavaa ajoittaa tapahtumat suoritettavaksi usein, esimerkiksi joka minuutti. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/prepayment-invoices-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Ennakkomaksujen laskuttaminen](finance-invoice-prepayments.md)  
[Vaihekuvaus: Myynnin ennakkomaksujen määrittäminen ja laskuttaminen](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Rahoitus](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Työtilan mukauttaminen](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]