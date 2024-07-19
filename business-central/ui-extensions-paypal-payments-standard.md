---
title: PayPal Payments Standard -laajennuksen käyttäminen
description: 'Tässä artikkelissa kerrotaan, miten vakiolaajennusten avulla asiakkaille voidaan antaa mahdollisuus suorittaa PayPal-maksuja.'
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '1070, 1071, 1073, 1074'
ms.date: 07/09/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# PayPal Payments Standard -laajennus

PayPal Payments Standard -laajennus voi auttaa kasvattamaan asiakaspalvelutasojasi, sillä se helpottaa asiakkaiden laskujen maksamista.

Vaihtoehto maksujen keräämiselle pankkisiirron tai Kortit kautta, asiakkaat voivat maksaa PayPal tilinsä kautta. Kun lähetät myyntilaskun sähköpostitse, sähköpostin perustekstissä ja liitetyssä PDF-tiedostossa on PayPal-linkki. Jos asiakas valitsee linkin, PayPal tilinsä huoltosivu avautuu ja siinä näkyvät maksutiedot. Tämän jälkeen asiakas voi maksaa laskun kuten minkä tahansa PayPal-maksun.

PayPal Payments Standard -palvelusta on apua seuraavissa asioissa:

* asiakkaan maksut saapuvat nopeammin pankkitilillesi
* asiakkailla on useita vaihtoehtoja maksaa laskut.
* PayPal on luotettava maksupalvelu. Asiakkaat käyttävät PayPalia mieluummin kuin syöttävät luottokorttitietonsa verkkosivulle.
* PayPalin avulla maksuja voi käsitellä useilla eri tavoilla. Niitä ovat luottokorttikäsittely, PayPal-tilit ja muut lähteet.
* PayPal-linkki voidaan lisätä automaattisesti myyntiasiakirjoihin. Myös käyttäjä voi lisätä linkin.
* PayPal Payments Standard -palvelu ei sisällä kuukausi- tai aloitusmaksuja.
* Koska palvelu on laajennus, voit ottaa PayPal Payment Standard -palvelun helposti käyttöön silloin, kun yritys tarvitsee sitä.  

Lisätietoja laajennuksen [määrittämisestä on asiakkaan maksun ottamisesta käyttöön PayPal](sales-how-enable-payment-service-extensions.md).

## Yritystilien maksujen rekisteröiminen automaattisesti

[!INCLUDE [prod_short](includes/prod_short.md)] voit rekisteröidä maksut automaattisesti, jos sinulla on yrityskauppiastili PayPal Commerce Platformia varten. Kun asiakkaasi käyttävät PayPal-linkkiä laskun maksamiseen, [!INCLUDE [prod_short](includes/prod_short.md)]  kirjaa tapahtumat ja sulkee asiakirjan.

Kun haluat käyttää tätä ominaisuutta, **ota** Maksurekisteröinnin asetukset - [!INCLUDE [prod_short](includes/prod_short.md)] sivulla **rekisterimaksut käyttöön automaattisesti**, kun vaihdat ja vahvistat tilit, joita käytät maksuissa. Jos päätät, ettet halua rekisteröidä maksuja automaattisesti, voit poistaa ne käytöstä uudelleen.

> [!TIP]
> Kehittäjät voivat käyttää eristysruututilejä asetusten testaamiseen. Voit tehdä tämän muuttamalla PayPal URL-osoitteen numeroksi **sandbox.paypal.com**. [!INCLUDE [prod_short](includes/prod_short.md)] käyttää IPN (PayPals Instant Payment Notification) -ilmoitusta notify_url.

## Katso myös

[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
