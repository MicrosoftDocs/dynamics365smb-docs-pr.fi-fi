---
title: Shopify-tilin luominen ja määrittäminen
description: Katso, miten voit hankkia Shopify-tilin, jotta voit esitellä Shopifyn ja Business Centralin integroinnin työnkulkua.
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: b4449b573307582595ee9949dcb53d5d553ce0f2
ms.sourcegitcommit: bb6ecb20cbd82fdb5235e3cb426fc73c29c0a7ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803035"
---
# <a name="create-and-set-up-a-shopify-account"></a>Shopify-tilin luominen ja määrittäminen

Jos harkitset Shopifyn käyttämistä verkkokaupparatkaisunasi ja tarvitset Shopify-tilin integroidun työnkulun vahvistamiseen, saatavillasi on seuraavat vaihtoehdot:

- Hanki kokeiluversio. Tämä on tavallinen aloituspiste loppukäyttäjille.  
- Luo testikauppoja. Tämä lähestymistapa on tarkoitettu kumppaneille, jotka tarjoavat toistuvia esittelyitä, koulutusta ja tukea.

## <a name="trial-end-user"></a>Kokeiluversio (loppukäyttäjä)

Siirry [Shopify-sivustolle](https://www.shopify.com) ja rekisteröi maksuton kokeiluversio käyttämällä järjestelmänvalvojatilin sähköpostitiliä. Lisätietoja verkkokaupan luomisesta ja mukauttamisesta on [Shopifyn ohjekeskuksessa](https://help.shopify.com/).

Ota seuraavat **asetukset** käyttöön luodun kaupan **Shopify Admin** -sivulta:

- Poista käytöstä **Arkistoi tilaus automaattisesti** [**Kassa**](https://www.shopify.com/admin/settings/checkout)-asetusten **Tilauksen käsittely** -osiossa **Shopify-järjestelmänvalvojassasi**.
- Harkitse *Näytä kirjautumislinkki verkkokaupassa ja kassalla* -vaihtoehdon ottamista käyttöön kassa-asetusten **Asiakastilin asetukset** -osiosta.
- Harkitse *Yrityksen nimi - valinnainen* -vaihtoehdon ottamista käyttöön kassa-asetusten **Asiakastiedot**-osiosta.
- Ota **Näytä tippausvaihtoehdot kassalla** -vaihtoehto käyttöön kassa-asetusten **Tippaus**-osiosta, jos aiot esitellä tipin jättämistä.
- Aktivoi testimaksut. Sinulla on kaksi vaihtoehtoa. Aloita avaamalla [**maksujen**](https://www.shopify.com/admin/settings/payments) asetukset:  
  1. *(for testing) Bogus Gateway*. Lisätietoja on kohdassa [Activate Bogus Gateway for testing](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* testitilassa. Lisätietoja on kohdassa [Shopify Paymentsin testaaminen](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Valitse [**suunnitelmien**](https://www.shopify.com/admin/settings/plan) asetuksista suunnitelma testataksesi kassaprosessia.

> [!Important]  
> Muista peruuttaa Shopify-kokeiluversio välttyäksesi maksuilta.

## <a name="development-store"></a>Testikauppa

Aloita liittymällä [Shopify-kumppaniohjelmaan](https://help.shopify.com/partners/about). Käytä sen jälkeen **Partner Dashboard** -koontinäyttöä luodaksesi testikaupan. Lisätietoja on kohdassa [Testikauppojen luonti](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Kun olet luonut kaupan, ota seuraavat **asetukset** käyttöön luodun kaupan **Shopify Admin** -sivulta:

- Poista **Arkistoi tilaus automaattisesti** -vaihtoehto käytöstä [**Kassa**](https://www.shopify.com/admin/settings/checkout)-asetusten **Tilausten käsittely** -osiossa **Shopify Adminissa**.
- Harkitse *Näytä kirjautumislinkki verkkokaupassa ja kassalla* -vaihtoehdon ottamista käyttöön kassa-asetusten **Asiakastilin asetukset** -osiosta.
- Harkitse *Yrityksen nimi - valinnainen* -vaihtoehdon ottamista käyttöön kassa-asetusten **Asiakastiedot**-osiosta.
- Jos aiot esitellä tipin jättämistä, ota **Näytä tippausvaihtoehdot kassalla** -vaihtoehto käyttöön kassa-asetusten **Tippaus**-osiosta.
- Aktivoi testimaksut. Sinulla on kaksi vaihtoehtoa. Aloita siirtymällä [**maksujen**](https://www.shopify.com/admin/settings/payments) asetuksiin:  
  1. *(for testing) Bogus Gateway*. Lisätietoja on kohdassa [Activate Bogus Gateway for testing](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* testitilassa. Lisätietoja on kohdassa [Shopify Paymentsin testaaminen](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

## <a name="see-also"></a>Katso myös

[Shopify-yhdistimen käytön aloittaminen](get-started.md)  
[Vaihekuvaus: Shopify-yhdistimen määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-shopify.md)
