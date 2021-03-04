---
title: Projektin laskuttaminen luomalla projektimyynnin lasku| Microsoft Docs
description: Ohjeaiheessa kerrotaan, miten projektin kustannukset laskutetaan asiakkailta projektin edetessä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 368b0b1edf1105045a365d8d5ac523c88955ad8a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758740"
---
# <a name="invoice-jobs"></a>Projektien laskuttaminen
Projektin aikana voi kertyä projektin kustannuksia resurssien käytöstä, materiaaleista ja projektiin liittyvistä ostoista. Projektin edetessä nämä tapahtumat kirjataan projektipäiväkirjaan. On tärkeää, että kaikki kustannukset kirjataan projektipäiväkirjaan ennen asiakkaan laskuttamista.

> [!NOTE]
> Voit ostaa myös ulkoisia resursseja, jotka eivät liity työhön, kuten esimerkiksi laskuttaa toimittajaa tehdystä työstä. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).

Voit laskuttaa koko projektin **Projektitehtävärivit**-sivulla tai laskuttaa vain valitut laskutettavat rivit **Suunnittelurivit**-sivulla. Laskutuksen voi tehdä joko projektin valmistumisen jälkeen tai tietyin laskutusaikataulun mukaisin väliajoin projektin aikana.

> [!NOTE]  
> Jos valitset projektiin liittyvien ostojen ostoasiakirjojen **Projektin rivityyppi** -kentässä **Laskutettava**, projektin suunnittelurivit, jotka ovat valmiita asiakkaalta laskutusta varten, luodaan. Lisätietoja on kohdassa [Projektin tarvikkeiden hallinta](projects-how-manage-project-supplies.md).

## <a name="to-create-multiple-job-sales-invoices"></a>Voit luoda monta projektin myyntilaskua
Voit luoda asiakkaalle laskun projektista tai vähintään yhdestä projektitehtävästä, kun laskutettava työ on valmis tai kun laskutusaikatauluun perustuva laskutuspäivämäärä on saavutettu.

Seuraavassa kerrotaan, miten eräajoa käytetään useiden projektien laskuttamisessa.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo projektin myyntilasku** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Määritä suodattimet, jos haluat rajata erätyön käsittelemien projektien määrää.
4. Luo laskut valitsemalla **OK**.  

Voit tarkastella ja kirjata luotuja laskuja **Myyntilaskut**-ikkunassa.

> [!NOTE]
> Vaihtoehtoisesti voit laskuttaa Projektit-sivulla asiakasta valitsemalla projektin ja valitsemalla sitten **Luo projektin myyntilasku** -toiminnon. 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a>Projektin myyntilaskun luominen ja kirjaaminen projektin suunnitteluriveistä
Voit luoda laskun projektin suunnitteluriveiltä ja määrittää samalla nimikkeen määrän, resurssin tai KP-tilin, jonka haluat laskuttaa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Työt** ja valitse sitten liittyvä linkki.
2. Avaa liittyvä projekti.
3. Valitse projektitehtävä, jonka **Projektitehtävätyyppi**-kentän arvo on **Kirjaus**. Valitse sitten **Projektin suunnittelurivit** -toiminto.  
4. Annan projektin suunnittelurivin **Laskuun siirrettävä määrä** -kentässä nimikkeen, resurssin tai pääkirjanpidon tilin tyyppi, jonka haluat laskuttaa.  
5. Valitse **Luo myyntilasku** -toiminto.
6. Anna **Luo projektin myyntilasku** -sivulla kirjauspäivämäärä. Määritä, haluatko luoda uuden laskun vai kohdistaa tämän laskun aiemmin luotuun laskuun.
7. Valitse **OK**-painike.  
8. Valitse **Projektin suunnittelurivit** -sivulla **Myyntilaskut/hyvityslaskut**-toiminto.

    Avautuvassa **Myyntilasku**-sivulla näkyy laskuun siirretty määrä.
9. Tee tarvittavat muutokset ja valitse **Kirjaa**-toiminto.

> [!NOTE]  
>   Projektiin liittyvän myyntihyvityslaskun luominen, tarkistaminen ja kirjaaminen tapahtuu vastaavalla tavalla.

## <a name="to-calculate-and-post-job-completion-entries"></a>Projektin valmistumistapahtumien laskeminen ja kirjaaminen
Kun olet saanut kaikki projektin toimenpiteet, kuten käytön kirjauksen ja laskutuksen, valmiiksi, projekti on päivitettävä **tilaan** **Valmis**. Tämän jälkeen mahdollinen kirjanpitoon kirjattu KET peruuntuu.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Työt** ja valitse sitten liittyvä linkki.  
2. Valitse avoin projekti ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Tila**-kentässä **Valmis**.
4. Laske ja kirjaa KET ohjattujen vaiheiden avulla. Vaihtoehtoisesti voit tehdä toiminnot manuaalisesti vaiheiden 5 ja 6 mukaisesti.  
5. Valitse **Laske KET** -toiminto.
6. Täytä **Laske projektin KET** -sivulla tarvittavat kentät.  

     Erätyön luomien projektin KET-tapahtumien vieressä on nyt valintamerkki **Projekti valmis** -kentässä. Valintamerkki osoittaa, että kyseessä ovat valmistumistapahtumat.  
7. Valitse **Kirjaa projektin KET kirjanpitoon** -toiminto.
8. Täytä **Kirjaa projektin KET kirjanpitoon** -sivulla tarvittavat kentät.  

     Erätyön luomien projektin pääkirjanpidon KET-tapahtumien vieressä on nyt valintamerkki **Projekti valmis** -kentässä. Valintamerkki osoittaa, että kyseessä ovat valmistumistapahtumat.

## <a name="see-also"></a>Katso myös
[Projektien hallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]