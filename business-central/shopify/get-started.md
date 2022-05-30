---
title: Shopifyn yhdistimen käytön aloittaminen
description: Ensimmäiset vaiheet määritettäessä Business Centralin ja Shopifyn välistä yhteyttä
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 2b88995cad8cfe0c3688ca062643f2d339fed9bf
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768128"
---
# <a name="get-started-with-the-shopify-connector"></a>Shopifyn yhdistimen käytön aloittaminen

[!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelman avulla voit liittää Shopify-myymäläsi siihen yrityksesi tuottavuuden maksimoimiseksi. Voit hallita ja tarkastella yrityksesi ja Shopify-verkkokaupan näkemyksiä yhtenä yksikkönä käyttämällä Shopify-yhdistintä. Käyttääksesi Shopify-toimintoa [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelmalla, sinun on seurattava joitakin vaiheita. Tämä sivu toimii oppaana, jonka avulla voit viimeistellä Shopify-myymälän integroinnin [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelman kanssa.

## <a name="prerequisites-for-shopify"></a>Vaatimukset Shopifylle

Tarvitaan:

- Shopify-tili
- Shopify-verkkokauppa

Voit luoda uuden Shopify-tilin tai rekisteröityä maksutta 14 päivän kokeiluversioon siirtymällä kohteeseen [Shopify](https://www.shopify.com/). Lisätietoja verkkokaupan luomisesta ja mukauttamisesta on [Shopifyn ohjekeskuksessa](https://help.shopify.com/).
  
- Muita myyntikanavia tuetaan, esimerkiksi Shopify POS.

### <a name="recommended-settings"></a>Suositellut asetukset

- Poista käytöstä **Arkistoi tilaus automaattisesti** [**Kassa**](https://www.shopify.com/admin/settings/checkout)-asetusten **Tilauksen käsittely** -osiossa **Shopify-järjestelmänvalvojassasi**.

Lisätietoja Shopifydemo- ja kokeiluskenaarioiden asetuksista on kohdassa [testi- ja harjoitteluskenaariot](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Business Centralin edellytykset

- Varmista, että **Yhdistä Shopify [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmalle**-laajennus on asennettu.

Laajennus on asennettu valmiiksi kaikille uusille kirjautumisyrityksille ja kokeiluversioihin. Jos laajennuksia täytyy asentaa Marketplacesta, käy kohteessa [laajennusten asentaminen ja poistaminen](../ui-extensions-install-uninstall.md#install). Noudata alla mainittuja ohjeita, jos sinulla ei ole [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaa.
<!--
## Installing the **Dynamics 365 Business Central** app to your Shopify online store

For existing [!INCLUDE[prod_short](../includes/prod_short.md)], this step is optional and can be skipped.

1. Locate the [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) app on the [Shopify AppStore](https://apps.shopify.com/)
2. Choose the **Add App** button. Sign-in into your Shopify account if prompted. Select the required online shop if you've more than one.
3. After reviewing privacy and permissions, choose the **Install App** button.
  You can find and open the installed **Dynamics 365 Business Central** app in the **Apps** section on the sidebar of **Shopify admin**.
4. Choose **Sign up now** to start [!INCLUDE[prod_short](../includes/prod_short.md)] trial or **Sign in** if you already have [!INCLUDE[prod_short](../includes/prod_short.md)]. You'll be redirected to your [!INCLUDE[prod_short](../includes/prod_short.md)] at [Business Central](https://businesscentral.dynamics.com).
5. The next steps should be done in [!INCLUDE[prod_short](../includes/prod_short.md)].
-->
## <a name="connecting-business-central-to-the-shopify-online-store"></a>Business Centralin yhdistäminen Shopify-verkkokauppaan

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.  
3. Syötä haluttu koodi **Koodi**-kenttään.  
4. Kirjoita **Shopify-URL**-kenttään verkkokaupan URL-osoite, joka on yhdistettävä.
5. Aktivoi **käytössä**-vaihto, tarkista ja hyväksy ehdot ja edellytykset.
6. Kirjaudu pyydettäessä sisään Shopify-tiliisi, tarkista tietosuoja ja käyttöoikeudet ja valitse sitten **Asenna sovellus** -painike.

Toista vaiheet 2-6 kaikille verkkokaupoille, jotka haluat yhdistää.

### <a name="next-steps"></a>Seuraavat vaiheet

Nyt verkkokauppa on yhteydessä [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan. Seuraavissa vaiheissa määritetään, miten ja mitä synkronoidaan.

- [Kohteiden synkronointi](synchronize-items.md)
- [Asiakkaiden synkronointi](synchronize-customers.md)
- [Tilausten synkronointi](synchronize-orders.md)

## <a name="see-also"></a>Katso myös

[Testi- ja koulutusskenaariot](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).

