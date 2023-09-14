---
title: 'Maksuehtojen määrittäminen:'
description: Käytä Business Centralin perusversiossa maksuehtoja eräpäivien ja maksualennusten hallintaan.
author: brentholtorf
ms.topic: conceptual
ms.search.form: 4
ms.date: 04/01/2021
ms.author: bholtorf
---
# Maksuehtojen määrittäminen

Maksuehdot määrittävät, miten eräpäiviä ja maksualennuksia hallitaan. Maksuehtoja voi määrittää kuinka monta tahansa, ja niiden määrittämiseen voi käyttää päivämääräkaavoja. Kun ensin rekisteröit [!INCLUDE [prod_short](includes/prod_short.md)]in, esittely-yritys tarjoaa muutamia maksutapoja, joita yritykset usein käyttävät. Voit kuitenkin lisätä niitä tarvittavan määrän.  

Kun maksuehdot määritetään asiakkaille ja toimittajille, heille luotavissa myynti- ja ostoasiakirjoissa käytetään aina samoja maksuehtoja. Tarvittaessa voit muuttaa myynti- tai ostoasiakirjan ehtoja, esimerkiksi jos haluat tietyn asiakkaan maksavan sinulle 7 päivän kuluessa 14 päivän oletusarvon sijasta. Tämä muutos ei vaikuta asiakkaalle määritettyyn oletusmaksuehtoon. Samat maksuehdot ovat käytettävissä myynti- ja ostoasiakirjoissa.

Kun sitten kirjaat laskun, [!INCLUDE [prod_short](includes/prod_short.md)] laskee maksualennukset maksuehtojen perusteella. Samalla lasketaan myös maksualennuksen päivämäärä (esimerkiksi viimeinen maksualennukseen oikeuttava maksupäivämäärä).  

Vastaavasti kun kirjaat hyvityslaskun, [!INCLUDE [prod_short](includes/prod_short.md)] laskee mahdolliset maksualennukset maksuehtojen perusteella. Järjestelmä laskee ja käsittelee hyvityslaskujen maksualennuksen samojen periaatteiden mukaan kuin laskujen maksualennukset. Kun hyvityslasku kohdistetaan laskuun, laskun mahdollisesta maksualennussummasta vähennetään hyvityslaskun maksualennussumma.  

Jos haluat lähettää asiakkaille muistutuksia erääntyneistä maksuista, sinun täytyy määrittää muistutustasot ja -ehdot. Lisätietoja on ohjeaiheessa [Muistutusehtojen ja -tasojen määrittäminen](finance-setup-reminders.md).  

## Maksuehtojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksuehdot** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Kun olet määrittänyt maksuehdot, voit määrittää ne asiakkaille ja toimittajille. Vaihtoehtoisesti voit liittää maksuehdot maksutapoihisi.  

> [!TIP]
> [!INCLUDE [prod_short](includes/prod_short.md)]in perusversiossa ei tueta maksuehtoja, joissa on osittaisia maksuja. Sen sijaan sinun täytyy käyttää ennakkomaksutoimintoa. Lisätietoja on ohjeaiheessa [Ennakkomaksujen määrittäminen](finance-set-up-prepayments.md).
>
> Tietyissä maissa ja tietyillä alueilla *voit* määrittää maksuehdot osittaisilla maksuilla. Jos haluat tietää, tuetaanko kyseistä toimintoa maassasi tai alueellasi, tutustu [Microsoft Learn](about-localization.md) -artikkelin **Paikalliset toiminnot** -osaan.

## Katso myös

[Maksutapojen määrittäminen](finance-payment-methods.md)  
[Ennakkomaksujen määrittäminen](finance-set-up-prepayments.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md)  
[Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]