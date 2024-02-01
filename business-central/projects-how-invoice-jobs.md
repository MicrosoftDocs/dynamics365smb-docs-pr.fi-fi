---
title: Projektin laskuttaminen luomalla projektin myyntilasku
description: 'Ohjeaiheessa kerrotaan, miten projektin kustannukset laskutetaan asiakkailta projektin edetessä ja kustannusten kertyessä.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: project invoice
ms.search.form: '1002, 1007,'
ms.date: 06/22/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Projektien laskuttaminen

Projektin aikana voi kertyä projektin kustannuksia resurssien käytöstä, materiaaleista ja projektiin liittyvistä ostoista. Projektin edetessä nämä tapahtumat kirjataan projektipäiväkirjaan. On tärkeää, että kaikki kustannukset kirjataan projektipäiväkirjaan ennen asiakkaan laskuttamista.

> [!NOTE]
> Voit ostaa myös ulkoisia resursseja, jotka eivät liity työhön, kuten esimerkiksi laskuttaa toimittajaa tehdystä työstä. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).

Voit laskuttaa koko projektin **Projektitehtävärivit**-sivulla tai laskuttaa vain valitut laskutettavat rivit **Suunnittelurivit**-sivulla. Laskutuksen voi tehdä joko projektin valmistumisen jälkeen tai tietyin laskutusaikataulun mukaisin väliajoin projektin aikana.

> [!NOTE]  
> Jos valitset projektiin liittyvien ostojen ostoasiakirjojen **Projektin rivityyppi** -kentässä **Laskutettava**, projektin suunnittelurivit, jotka ovat valmiita asiakkaalta laskutusta varten, luodaan. Lisätietoja on kohdassa [Projektin tarvikkeiden hallinta](projects-how-manage-project-supplies.md).

Voit myös laskuttaa yritystä, joka ei ole loppuasiakas. Joskus osapuoli, jolle projekti on luotu, eroaa laskun maksavasta osapuolesta. **Projektit**-sivulla voit määrittää projektista hyötyvän asiakkaan **Tilausasiakas**-kentissä sekä laskutettavan osapuolen **Laskutusasiakas**-kentissä. 

## Voit luoda monta projektin myyntilaskua

Voit luoda asiakkaalle laskun projektista tai vähintään yhdestä projektitehtävästä, kun laskutettava työ on valmis tai kun laskutusaikatauluun perustuva laskutuspäivämäärä on saavutettu.

Seuraavassa kerrotaan, miten eräajoa käytetään useiden projektien laskuttamisessa.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo projektin myyntilasku** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Määritä suodattimet, jos haluat rajata erätyön käsittelemien projektien määrää.
4. Luo laskut valitsemalla **OK**.  

Voit tarkastella ja kirjata luotuja laskuja **Myyntilaskut**-ikkunassa.

> [!NOTE]
> Vaihtoehtoisesti voit laskuttaa Projektit-sivulla asiakasta valitsemalla projektin ja valitsemalla sitten **Luo projektin myyntilasku** -toiminnon. 

## Projektin myyntilaskun luominen ja kirjaaminen projektin suunnitteluriveistä

Voit luoda laskun projektin suunnitteluriveiltä ja määrittää samalla nimikkeen määrän, resurssin tai KP-tilin, jonka haluat laskuttaa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.
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

## Katso myös

[Projektien hallinta](projects-manage-projects.md)  
[Taloushallinto](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
