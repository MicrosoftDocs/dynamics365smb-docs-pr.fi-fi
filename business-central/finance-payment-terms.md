---
title: Maksuehtojen määrittäminen
description: Käytä maksuehtoja hallitaksesi eräpäiviä ja maksualennuksia.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '4,'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-payment-terms"></a>Maksuehtojen määrittäminen

Maksuehdot määrittävät, miten eräpäiviä ja maksualennuksia hallitaan. Päivämääräkaavoja voi käyttää maksuehtojen määrittämiseen. Kun ensin rekisteröit [!INCLUDE [prod_short](includes/prod_short.md)]in, esittely-yritys tarjoaa muutamia maksutapoja, joita yritykset usein käyttävät. Voit kuitenkin lisätä niitä tarvittavan määrän.  

Jos maksuehdot määritetään asiakkaille ja toimittajille, heille luotavissa myynti- ja ostoasiakirjoissa käytetään aina samoja maksuehtoja. Myynti- ja ostoasiakirjojen asiakirjapäivämääriä, ei niiden kirjauspäivämääriä, käytetään laskettaessa maksujen eräpäiviä. Voit tarvittaessa muuttaa ehtoja myynti- tai ostoasiakirjassa. Jos esimerkiksi haluat tietyn asiakkaan maksavan sinulle seitsemän päivän kuluessa oletusarvoisen 14 päivän sijaan. Asiakirjan ehtojen muuttaminen ei muuta asiakkaalle määritettyä oletusmaksuehtoa. Samat maksuehdot ovat käytettävissä myynti- ja ostoasiakirjoissa.

Kun kirjaat laskun, [!INCLUDE [prod_short](includes/prod_short.md)] laskee maksualennukset maksuehtojen perusteella. Maksualennuksen päivämäärä on viimeinen päivä, jolloin asiakas voi saada maksualennuksen. Päivämäärä lasketaan myös silloin, kun kirjaat laskun.  

Vastaavasti kun kirjaat hyvityslaskun, [!INCLUDE [prod_short](includes/prod_short.md)] laskee maksualennukset maksuehtojen perusteella. Se laskee hyvityslaskujen alennuksen samalla tavalla kuin laskujen maksualennukset. Kun hyvityslasku kohdistetaan laskuun, [!INCLUDE [prod_short](includes/prod_short.md)] alentaa alennussummaa hyvityslaskun alennussummalla.  

Jos haluat lähettää asiakkaille muistutuksia erääntyneistä maksuista, sinun täytyy määrittää muistutustasot ja -ehdot. Saat lisätietoja muistutuksista kohdasta [Muistutusehtojen ja -tasojen määrittäminen](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>Maksuehtojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksuehdot** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Kun olet määrittänyt maksuehdot, voit määrittää ne asiakkaille ja toimittajille. Vaihtoehtoisesti voit liittää maksuehdot maksutapoihisi.  

> [!TIP]
> [!INCLUDE [prod_short](includes/prod_short.md)]in perusversiossa maksuehdot eivät tue osittaisia maksuja. Sen sijaan sinun täytyy käyttää ennakkomaksutoimintoa. Saat lisätietoja ennakkomaksuista valitsemalla [Ennakkomaksujen määrittäminen](finance-set-up-prepayments.md).
>
> Joissakin maissa ja tietyillä alueilla *voit* määrittää maksuehdot osittaisilla maksuilla. Jos haluat tietää, tuetaanko maassasi tai alueellasi tätä ominaisuutta, siirry [Microsoft Learn](about-localization.md) -artikkelin sisällysluettelon **Paikalliset toiminnot** -osioon.

## <a name="see-also"></a>Katso myös

[Maksutapojen määrittäminen](finance-payment-methods.md)  
[Ennakkomaksujen määrittäminen](finance-set-up-prepayments.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md)  
[Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
