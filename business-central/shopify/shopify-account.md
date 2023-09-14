---
title: Shopify-tilin luominen ja määrittäminen
description: 'Katso, miten voit hankkia Shopify-tilin, jotta voit esitellä Shopifyn ja Business Centralin integroinnin työnkulkua.'
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102'
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# Shopify-tilin luominen ja määrittäminen

Jos harkitset Shopifyn käyttämistä verkkokaupparatkaisunasi ja tarvitset Shopify-tilin integroidun työnkulun vahvistamiseen, saatavillasi on seuraavat vaihtoehdot:

- Hanki kokeiluversio. Tämä on tavallinen aloituspiste loppukäyttäjille.  
- Luo testikauppoja. Tämä lähestymistapa on tarkoitettu kumppaneille, jotka tarjoavat toistuvia esittelyitä, koulutusta ja tukea.

## Kokeiluversio (loppukäyttäjä)

Siirry [Shopify-sivustolle](https://www.shopify.com) ja rekisteröi maksuton kokeiluversio käyttämällä järjestelmänvalvojatilin sähköpostitiliä. Lisätietoja verkkokaupan luomisesta ja mukauttamisesta on [Shopifyn ohjekeskuksessa](https://help.shopify.com/).

Ota seuraavat **asetukset** käyttöön luodun kaupan **Shopify Admin** -sivulta:

- Poista **Arkistoi tilaus automaattisesti** -vaihtoehto käytöstä [**Kassa**](https://www.shopify.com/admin/settings/checkout)-asetusten **Tilausten käsittely** -osiossa **Shopify Adminissa**.
- Harkitse *Näytä kirjautumislinkki verkkokaupassa ja kassalla* -vaihtoehdon ottamista käyttöön kassa-asetusten **Asiakastilin asetukset** -osiosta.
- Harkitse *Yrityksen nimi - valinnainen* -vaihtoehdon ottamista käyttöön kassa-asetusten **Asiakastiedot**-osiosta.
- Ota **Näytä tippausvaihtoehdot kassalla** -vaihtoehto käyttöön kassa-asetusten **Tippaus**-osiosta, jos aiot esitellä tipin jättämistä.
- Aktivoi testimaksut. Sinulla on kaksi vaihtoehtoa. Aloita avaamalla [**maksujen**](https://www.shopify.com/admin/settings/payments) asetukset:  
  1. *(for testing) Bogus Gateway*. Lisätietoja on kohdassa [Activate Bogus Gateway for testing](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* testitilassa. Lisätietoja on kohdassa [Shopify Paymentsin testaaminen](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Valitse [**suunnitelmien**](https://www.shopify.com/admin/settings/plan) asetuksista suunnitelma testataksesi kassaprosessia.

> [!Important]  
> Muista peruuttaa Shopify-kokeiluversio välttyäksesi maksuilta.

## Testikauppa

Aloita liittymällä [Shopify-kumppaniohjelmaan](https://help.shopify.com/partners/about). Käytä sen jälkeen **Partner Dashboard** -koontinäyttöä luodaksesi testikaupan. Lisätietoja on kohdassa [Testikauppojen luonti](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Kun olet luonut kaupan, ota seuraavat **asetukset** käyttöön luodun kaupan **Shopify Admin** -sivulta:

- Poista **Arkistoi tilaus automaattisesti** -vaihtoehto käytöstä [**Kassa**](https://www.shopify.com/admin/settings/checkout)-asetusten **Tilausten käsittely** -osiossa **Shopify Adminissa**.
- Harkitse *Näytä kirjautumislinkki verkkokaupassa ja kassalla* -vaihtoehdon ottamista käyttöön kassa-asetusten **Asiakastilin asetukset** -osiosta.
- Harkitse *Yrityksen nimi - valinnainen* -vaihtoehdon ottamista käyttöön kassa-asetusten **Asiakastiedot**-osiosta.
- Jos aiot esitellä tipin jättämistä, ota **Näytä tippausvaihtoehdot kassalla** -vaihtoehto käyttöön kassa-asetusten **Tippaus**-osiosta.
- Aktivoi testimaksut. Sinulla on kaksi vaihtoehtoa. Aloita siirtymällä [**maksujen**](https://www.shopify.com/admin/settings/payments) asetuksiin:  
  1. *(for testing) Bogus Gateway*. Lisätietoja on kohdassa [Activate Bogus Gateway for testing](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* testitilassa. Lisätietoja on kohdassa [Shopify Paymentsin testaaminen](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

> [!Note]  
> Kehittämisvarastot on yleensä suojattu salasanalla. Kun yrität avata tietyn verkkokauppasi sivun [!INCLUDE [prod_short](../includes/prod_short.md)]-ohjelmassa, esimerkiksi siirtyä tiettyyn tuotteeseen tai tilaukseen, sinun on kirjoitettava salasanasi. Kun testaat, sinun ei tarvitse syöttää salasanaasi, kun kirjaudut sisään Shopify-järjestelmänvalvojaasi ja avaat liikkeen sieltä. Sinun ei tarvitse syöttää liikkeen salasanaa, ennen kuin suljet selaimen tai istuntosi vanhenee.  

## Katso myös

[Shopify-yhdistimen käytön aloittaminen](get-started.md)  
[Vaihekuvaus: Shopify-yhdistimen määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-shopify.md)
