---
title: Projektin edistymisen laskemisen ja kirjaamisen KET-menetelmät
description: 'Tässä artikkelissa käsitellään KET-menetelmiä, joilla kirjataan, seurataan ja lasketaan keskeneräisten projektien rahoitustietoja.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'work in process, work in progress, calculate project WIP'
ms.search.form: '1010,'
ms.date: 08/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="understanding-wip-methods-in-project-management"></a>Projektinhallinnan KET-menetelmien ymmärtäminen

Projektin edetessä kulutetaan materiaaleja, resursseja ja muita kuluja, ja nämä on kirjattava projektiin. Keskeneräinen työ (KET) on ominaisuus, jonka avulla voidaan arvioida kirjanpidossa olevien projektien taloudellisen arvon projektin ollessa kesken. Monissa tapauksissa saatat kirjata projektille kuluja ennen projektin laskuttamista. Kun vain kuluja kirjataan, rahoituslaskelma on epätarkka.

Voit seurata arvoa kirjanpidossa laskemalla KET:n ja kirjaamalla arvon kirjanpitoon. Lisätietoja on kohdassa [Projektin edistymisen ja suorituskyvynvalvominen](projects-how-monitor-progress-performance.md).

Tukee seuraavia keskeneräisen [!INCLUDE[prod_short](includes/prod_short.md)]  työn arvon laskenta- ja tallennusmenetelmiä.

| KET-menetelmä | Kuvaus | Tuloutetut kustannukset | Tuloutettu myynti |
| --- | ------- |--- | --- |
| Kustannusarvo |Tunnistaa kustannuksen, kun asiakasta laskutetaan. Tunnistaa laskutettuun myyntiin perustuvan myynnin. |Kustannusarvo|Sopimus (laskuhinta)|
| Myynnin kulut |Tunnistaa kustannuksen, kun asiakasta laskutetaan. Tunnistaa laskutettuun myyntiin perustuvan myynnin.|Myynnin kulut|Sopimus (laskutettu hinta)|
| Myyntiarvo |Tunnistaa kustannukset raportoitaessa. Tuloutetaan myynti suhteessa raportoituihin kustannuksiin.|Käyttö (kokonaiskustannus)|Myyntiarvo|
| Valmistumisen prosenttiosuus |Tunnistaa kustannukset raportoitaessa. Tuloutetaan myynti suhteessa raportoituihin kustannuksiin.|Käyttö (kokonaiskustannus)|Valmistumisen prosenttiosuus|
| Valmis sopimus |Mikään myynti tai kustannus ei ole osa KET-laskentaa. Valmis sopimus ei tulouta tuottoa ja kustannuksia ennen projektin valmistumista. Tämä vaihtoehto on hyödyllinen esimerkiksi silloin, kun projektin kustannus- ja tuottoarvioiden ympärillä on suurta epävarmuutta.|Valmistuessa|Valmistuessa|

Tarkat kaavat ja pääkirjanpidon tapahtumat määritetään Tuloutettu [**kustannus- ja**](#recognized-cost) Tuloutettu myynti [**-kenttien valinnalla**](#recognized-sales) .

## <a name="create-a-project-wip-method"></a>Projektin KET-menetelmän luominen

Projektiin luodaan organisaation tarpeita vastaava KET-menetelmä, joka määritetään oletukseksi.  

> [!NOTE]
> Kun olet luonut KET-tapahtumat menetelmän avulla, et voi muuttaa tai poistaa tapaa.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, kirjoita **Projektin KET-menetelmät** ja valitse linkit.  
2. Valitse Uusi-toiminto **·**, valitse tuloutetut kustannukset **- ja** Tuloutettu myynti **-kentille asianmukaiset arvot** ja täytä sitten muut kentät tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Sulje sivu.
4. Jos haluat tehdä tästä menetelmästä oletusarvon, valitse ![Valolamppu, joka avaa Kerro minulle -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, määritä **projektin asetukset** ja valitse linkit.  
5. Valitse **Oletus KET-menetelmä** -kentässä menetelmä luettelosta.

### <a name="recognized-cost"></a>Tuloutettu kustannus

| Tuloutettu kustannus | Tuloutetun kustannuksen laskentakaava | Pääkirjanpidon tapahtumat |
| --- | --- | ---------- |
|Valmistuessa|0 (Nolla)| **Tuloutettujen kustannusten tilin** hyvitysten **KET-kustannusten tili** </br>Summa: Tuloutettu kustannus </br></br>KeT-kustannusten **tilin**  **kohdistetut projektin kustannukset -tili** </br>Summa: MAKSIMI[tuloutettu kustannus; Todellinen (kokonaiskustannus)]|
|Myynnin kulut|Todellinen (kokonaiskustannus) - Budjetti (kokonaiskustannukset) * Laskutettu%, jossa:</br></br> Laskutettu% = Laskutettu (kokonaishinta) / Laskutettava (kokonaishinta)</br></br>**Huomaa:**  Tämä laskenta edellyttää, että laskutettava (kokonaishinta) ja Budjetti (kokonaiskustannukset) on syötetty oikein koko projektille.| **Tuloutettujen kustannusten tilin** hyvitysten **KET-kustannusten tili** </br>Summa: Tuloutettu kustannus </br></br>KeT-kustannusten **tilin**  **kohdistetut projektin kustannukset -tili** </br>Summa: MAKSIMI[tuloutettu kustannus; Todellinen (kokonaiskustannus)] </br></br> **Projektin kustannusten muutostilin**  **kertyneiden KET-kustannusten tili** </br>Summa: Tuloutettu kustannus - todellinen (kokonaiskustannus), jos tuloutettu kustannus > todellinen (kokonaiskustannus)|
|Kustannusarvo|Todellinen (kokonaiskustannus) - [valmistumis-% - Laskutettu%] * Laskutettava (kokonaishinta) * BudgetCostPriceRatio, jossa: </br></br> BudgetCostPriceRatio = Budjetti (kokonaiskustannus) / Budjetti (kokonaishinta)</br>Laskutettu% = Laskutettu (kokonaishinta) / Laskutettava (kokonaishinta)</br>Valmistumis-% = Todellinen (kokonaiskustannus)/budjetti (kokonaiskustannus)</br></br>**Huomaa:**  Tämä laskenta edellyttää, että laskutettava (kokonaishinta), Budjetti ( kokonaishinta) ja budjetti (kokonaiskustannukset) syötetään oikein koko projektia varten.| **Tuloutettujen kustannusten tilin** hyvitysten **KET-kustannusten tili** </br>Summa: Tuloutettu kustannus</br></br>KeT-kustannusten **tilin**  **kohdistetut projektin kustannukset -tili** </br>Summa: MAKSIMI[tuloutettu kustannus; Todellinen (kokonaiskustannus)] </br></br> **Projektin kustannusten muutostilin**  **kertyneiden KET-kustannusten tili** </br>Summa: Tuloutettu kustannus - todellinen (kokonaiskustannus), jos tuloutettu kustannus > todellinen (kokonaiskustannus)|
|Sopimus (laskutettu kustannus)|Laskutettu (kokonaiskustannus) | **Tuloutettujen kustannusten tilin** hyvitysten **KET-kustannusten tili** </br>Summa: Tuloutettu kustannus </br></br> KeT-kustannusten **tilin**  **kohdistetut projektin kustannukset -tili** </br>Summa: MAKSIMI[tuloutettu kustannus; Todellinen (kokonaiskustannus)] </br></br> **Projektin kustannusten muutostilin**  **kertyneiden KET-kustannusten tili** </br>Summa: Tuloutettu kustannus - todellinen (kokonaiskustannus), jos tuloutettu kustannus > todellinen (kokonaiskustannus)|
|Käyttö (kokonaiskustannus)|Toteuma (kokonaiskustannus) | **Tuloutettujen kustannusten tilin** hyvitysten **KET-kustannusten tili** </br>Summa: Tuloutettu kustannus </br></br>KeT-kustannusten **tilin**  **kohdistetut projektin kustannukset -tili** </br>Summa: MAKSIMI[tuloutettu kustannus; Todellinen (kokonaiskustannus)]|

Kun projektin tilaksi muutetaan Valmis, **Laske KET** -tehtävä peruuttaa KET-tapahtuman ja kirjaa sen sijaan.

Tuloutetun kustannuksen **tilin** hyvitysprojektin **kohdistetun kustannuksen tili**, Summa: **Todellinen (kokonaiskustannus)**

> [!NOTE]
> Käytetty **KET-kirjaustapa -kentän** valinnan **mukaan Projektin kust. kohdistettu tili** -tiliä, **Resurssin kust. kohdistettu tili**- tai **KP-kust. kohdistetun kirjanpidon tiliä** voidaan käyttää projektin kohdistetun kustannuksen **tilin** sijaan. Lisätietoja [on projektin kirjausryhmissä](projects-how-setup-jobs.md#to-set-general-information-for-projects).

### <a name="recognized-sales"></a>Tuloutettu myynti

| Tuloutettu myynti | Tuloutetun myynnin laskentakaava | Pääkirjanpidon tapahtumat |
| --- | --- | ---------- |
|Valmistuessa|0 (Nolla)|Laskutetun KET-myynnin **tilin**  **tuloutetun myynnin tili** </br>Summa: Tuloutetut summat</br></br>Projektin myyntikoht **. kohdistettu tili** Hyvitys **keT laskutettu myyntitili** </br>Summa: Laskutettu (kokonaishinta)|
|Sopimus (laskutettu hinta)|Laskutettu (kokonaishinta)|Laskutetun KET-myynnin **tilin**  **tuloutetun myynnin tili** </br>Summa: Tuloutetut summat</br></br>Projektin myyntikoht **. kohdistettu tili** Hyvitys **keT laskutettu myyntitili** </br>Summa: Laskutettu (kokonaishinta)|
|Käyttö (kokonaiskustannus)|Toteuma (kokonaiskustannus)|Laskutetun KET-myynnin **tilin**  **tuloutetun myynnin tili** </br>Summa: Tuloutetut summat</br></br>Projektin myyntikoht **. kohdistettu tili** Hyvitys **keT laskutettu myyntitili** </br>Summa: Laskutettu (kokonaishinta)
|Valmistumisen prosenttiosuus|MIN[Laskutettava (kokonaishinta) * Valmistumis-%; Laskutus (kokonaishinta)], jossa:</br></br>Valmistumis-% = Todellinen (kokonaiskustannus)/budjetti (kokonaiskustannus)</br></br>**Huomaa:**  Tämä laskenta edellyttää, että laskutettava (kokonaishinta) ja Budjetti (kokonaiskustannukset) on syötetty oikein koko projektille.|Kertyneen KET-myynnin **tilin**  **tuloutetun myynnin tili** </br>Summa: Tuloutetut summat</br></br>Projektin myyntikoht **. kohdistettu tili** Hyvitys **keT laskutettu myyntitili** </br>Summa: Laskutettu (kokonaishinta)|
|Käyttö (kokonaishinta)|Toteuma (kokonaishinta)|Laskutetun KET-myynnin **tilin**  **tuloutetun myynnin tili** </br>Summa: Tuloutetut summat </br></br>Projektin myyntikoht **. kohdistettu tili** Hyvitys **keT laskutettu myyntitili** </br>Summa: MAKS[tuloutetut tuloutetut myyntisaaminen; Laskutettu (kokonaishinta)]</br></br>Kertyneen KET-myyntitilin **·**  **projektin myynnin muutoksen tili** </br>Summa: MAKS[tuloutetut tuloutetut myyntisaaminen; Laskutettu (kokonaishinta)] - Laskutettu (kokonaishinta)|
|Myyntiarvo| Todellinen (kokonaishinta) * laskutettava (kokonaishinta)/budjetti (kokonaishinta)</br></br>**Huomaa:**  Tämä laskenta edellyttää, että laskutettava (kokonaishinta) ja Budjetti (kokonaishinta) on syötetty oikein koko projektille.|Laskutetun KET-myynnin **tilin**  **tuloutetun myynnin tili** </br>Summa: Tuloutetut summat</br></br>Projektin myyntikoht **. kohdistettu tili** Hyvitys **keT laskutettu myyntitili** </br>Summa: MAKS[tuloutetut tuloutetut myyntisaaminen; Laskutettu (kokonaishinta)]</br></br>Kertyneen KET-myyntitilin **·**  **projektin myynnin muutoksen tili** </br>Summa: MAKS[tuloutetut tuloutetut myyntisaaminen; Laskutettu (kokonaishinta)] - Laskutettu (kokonaishinta)|

Kun projektin tilaksi muutetaan Valmis, **Laske KET** -tehtävä peruuttaa KET-tapahtuman ja kirjaa sen sijaan.

 **Projektin myynnin kohdistustilin**  **tuloutetun myynnin tili**, Summa: **Laskutettu (kokonaishinta)**

## <a name="see-also"></a>Katso myös

[Projektien hallinta](projects-manage-projects.md)  
[Taloushallinto](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
