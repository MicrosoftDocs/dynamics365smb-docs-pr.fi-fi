---
title: Shopify-tilin luominen ja määrittäminen
description: 'Katso, miten voit hankkia Shopify-tilin, jotta voit esitellä Shopifyn ja Business Centralin integroinnin työnkulkua.'
ms.date: 03/04/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102'
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
---

# <a name="create-and-set-up-a-shopify-account"></a>Shopify-tilin luominen ja määrittäminen



Jos harkitset Shopifyn käyttämistä verkkokaupparatkaisunasi ja tarvitset Shopify-tilin integroidun työnkulun vahvistamiseen, saatavillasi on seuraavat vaihtoehdot:

- Hanki kokeiluversio. Tämä on tavallinen aloituspiste loppukäyttäjille.  
- Luo testikauppoja. Tämä lähestymistapa on tarkoitettu kumppaneille, jotka tarjoavat toistuvia esittelyitä, koulutusta ja tukea.

## <a name="trial-end-user"></a>Kokeiluversio (loppukäyttäjä)

Siirry [Shopify-sivustolle](https://www.shopify.com) ja rekisteröi maksuton kokeiluversio käyttämällä järjestelmänvalvojatilin sähköpostitiliä. Lisätietoja verkkokaupan luomisesta ja mukauttamisesta on [Shopifyn ohjekeskuksessa](https://help.shopify.com/).

Ota seuraavat **asetukset** käyttöön luodun kaupan **Shopify Admin** -sivulta:

- Valitse [**suunnitelmien**](https://www.shopify.com/admin/settings/plan) asetuksista suunnitelma testataksesi kassaprosessia.

- Harkitse *Näytä kirjautumislinkki verkkokaupan otsikossa ja kassalla* -valinnan ottamista käyttöön **Shopify-järjestelmänvalvojan** [**Asiakastilit**](https://www.shopify.com/admin/settings/customer_accounts)-asetusten **Tilit verkkokaupassa ja kassalla** -osiossa.
- Harkitse *Uuden asiakastilin* valitsemista Asiakastilien asetusten **Tilit verkkokaupassa ja kassalla** -osassa.
- Harkitse *omatoimisten palautusten* käyttöönottoa Asiakastilien asetusten **Uudet asiakastilit** -osassa.

- Aktivoi testimaksut. Sinulla on kaksi vaihtoehtoa. Aloita avaamalla [**maksujen**](https://www.shopify.com/admin/settings/payments) asetukset:  
  1. *(for testing) Bogus Gateway*. Lisätietoja on kohdassa [Activate Bogus Gateway for testing](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* testitilassa. Lisätietoja on kohdassa [Shopify Paymentsin testaaminen](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Poista **Arkistoi tilaus automaattisesti** -vaihtoehto käytöstä [**Kassa**](https://www.shopify.com/admin/settings/checkout)-asetusten **Tilausten käsittely** -osiossa **Shopify Adminissa**.
- Harkitse *Yrityksen nimi - valinnainen* -vaihtoehdon ottamista käyttöön kassa-asetusten **Asiakastiedot**-osiosta.
- Ota **Näytä tippausvaihtoehdot kassalla** -vaihtoehto käyttöön kassa-asetusten **Tippaus**-osiosta, jos aiot esitellä tipin jättämistä.

> [!Important]  
> Muista peruuttaa Shopify-kokeiluversio välttyäksesi maksuilta.

## <a name="development-store"></a>Testikauppa

Aloita liittymällä [Shopify-kumppaniohjelmaan](https://help.shopify.com/partners/about). Käytä sen jälkeen **Partner Dashboard** -koontinäyttöä luodaksesi testikaupan. Lisätietoja on kohdassa [Testikauppojen luonti](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Kun olet luonut kaupan, ota seuraavat **asetukset** käyttöön luodun kaupan **Shopify Admin** -sivulta:

- Harkitse *Näytä kirjautumislinkki verkkokaupan otsikossa ja kassalla* -valinnan ottamista käyttöön **Shopify-järjestelmänvalvojan** [**Asiakastilit**](https://www.shopify.com/admin/settings/customer_accounts)-asetusten **Tilit verkkokaupassa ja kassalla** -osiossa.
- Harkitse *Uuden asiakastilin* valitsemista Asiakastilien asetusten **Tilit verkkokaupassa ja kassalla** -osassa.
- Harkitse *omatoimisten palautusten* käyttöönottoa Asiakastilien asetusten **Uudet asiakastilit** -osassa.
  
- Aktivoi testimaksut. Sinulla on kaksi vaihtoehtoa. Aloita siirtymällä [**maksujen**](https://www.shopify.com/admin/settings/payments) asetuksiin:  
  1. *(for testing) Bogus Gateway*. Lisätietoja on kohdassa [Activate Bogus Gateway for testing](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* testitilassa. Lisätietoja on kohdassa [Shopify Paymentsin testaaminen](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).
     
- Poista **Arkistoi tilaus automaattisesti** -vaihtoehto käytöstä [**Kassa**](https://www.shopify.com/admin/settings/checkout)-asetusten **Tilausten käsittely** -osiossa **Shopify-järjestelmänvalvojassa**.
- Harkitse *Yrityksen nimi - valinnainen* -vaihtoehdon ottamista käyttöön kassa-asetusten **Asiakastiedot**-osiosta.
- Jos aiot esitellä tipin jättämistä, ota **Näytä tippausvaihtoehdot kassalla** -vaihtoehto käyttöön kassa-asetusten **Tippaus**-osiosta.


> [!Note]  
> Kehittämisvarastot on yleensä suojattu salasanalla. Kun yrität avata tietyn verkkokauppasi sivun [!INCLUDE [prod_short](../includes/prod_short.md)]-ohjelmassa, esimerkiksi siirtyä tiettyyn tuotteeseen tai tilaukseen, sinun on kirjoitettava salasanasi. Kun testaat, sinun ei tarvitse syöttää salasanaasi, kun kirjaudut sisään Shopify-järjestelmänvalvojaasi ja avaat liikkeen sieltä. Sinun ei tarvitse syöttää liikkeen salasanaa, ennen kuin suljet selaimen tai istuntosi vanhenee.  

## <a name="see-also"></a>Katso myös

[Shopify-yhdistimen käytön aloittaminen](get-started.md)  
[Vaihekuvaus: Shopify-yhdistimen määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-shopify.md)
