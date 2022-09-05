---
title: Shopifyn yhdistimen käytön aloittaminen
description: Ensimmäiset vaiheet määritettäessä Business Centralin ja Shopifyn välistä yhteyttä
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: 30100, 30101, 30102, 30103, 30104, 30135,
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: e59dd0dcf757fbcf76d4068756adfe7bc9475f54
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361553"
---
# <a name="get-started-with-the-shopify-connector"></a>Shopifyn yhdistimen käytön aloittaminen

Yhdistä Shopify-kauppasi [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelmaan ja maksimoi yrityksesi tuottavuus. Hallitse ja tarkastele yrityksesi ja Shopify-kauppasi merkityksellisiä tietoja yhtenä yksikkönä. 

Shopify-yhdistin sisältää seuraavat ominaisuudet:

- Tuki useammalle kuin yhdelle Shopify-kaupalle  

  - Jokaisella myymälällä on omat määrityksensä, kuten tuotekokoelma, varaston laskemiseen käytetyt sijainnit ja hinnastot.  
- Nimikkeiden tai tuotteiden kaksisuuntainen synkronointi  

  - Yhdistin synkronoi kuvia, nimikemuunnoksia, viivakoodeja, toimittajan nimikenumeroita, laajennettuja tekstejä ja tunnisteita.  
  -    Nimikemääritteiden vienti Shopifyhin.  
  -    Käytä valittuja asiakashintaryhmiä ja alennuksia määrittääksesi Shopifyhin vietyjä hintoja.  
  -    Päätä, voidaanko nimikkeitä luoda automaattisesti vai sallitaanko vain päivitykset aiemmin luotuihin tuotteisiin.  
- Varastotasojen synkronointi  

  -    Valitse joitakin [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelmassa käytettävissä olevista sijainneista tai ne kaikki.  
  -    Päivitä usean sijainnin varastotasot Shopifyssa.  
- Asiakkaiden kaksisuuntainen synkronointi  

  -    Kohdista asiakkaat älykkäästi puhelinnumeron ja sähköpostiosoitteen perusteella.  
  -    Käytä maakohtaisia malleja asiakkaiden luomisessa, mikä auttaa varmistamaan, että veroasetukset ovat oikein.  
- Tilausten tuonti Shopifysta  

  -    Tuonnin aikana voit luoda automaattisesti asiakkaita [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelmassa tai päättää hallita asiakkaita Shopifyssa.  
  -    Sisällytä muissa kanavissa, kuten Shopifyssa tai Amazonissa, luotuja tilauksia.  
  -    Toimituskulut, lahjakortit, vinkit, toimitus- ja maksutavat, tapahtumat ja petosriski.  
  - Vastaanota maksusuoritustietoja Shopify Paymentsista.  
- Täyttämistietojen helppo seuranta  

  -    Voit halutessa valita nimikeseurantatietojen kirjoittamisen [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelmasta Shopifyhin.  

Jos haluat käyttää Shopifyta yhdessä [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelman kanssa, sinun on ensin tehtävä joitakin asioita. Tämä artikkeli toimii oppaana, jonka avulla voit viimeistellä Shopify-kaupan integroinnin [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelman kanssa.

## <a name="prerequisites-for-shopify"></a>Vaatimukset Shopifylle

Tarvitaan:

- Shopify-tili
- Shopify-verkkokauppa

Voit luoda uuden Shopify-tilin tai rekisteröityä maksutta 14 päivän kokeiluversioon siirtymällä kohteeseen [Shopify](https://www.shopify.com/). Lisätietoja verkkokaupan luomisesta ja mukauttamisesta on [Shopifyn ohjekeskuksessa](https://help.shopify.com/).
  
Muita myyntikanavia tuetaan, esimerkiksi Shopify POS.

### <a name="recommended-settings"></a>Suositellut asetukset

- Poista käytöstä **Arkistoi tilaus automaattisesti** [**Kassa**](https://www.shopify.com/admin/settings/checkout)-asetusten **Tilauksen käsittely** -osiossa **Shopify-järjestelmänvalvojassasi**.

Lisätietoja Shopifydemo- ja kokeiluskenaarioiden asetuksista on kohdassa [testi- ja harjoitteluskenaariot](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Business Centralin edellytykset

- Varmista **[Shopify-yhdistin](https://go.microsoft.com/fwlink/?linkid=2196238)**-sovellus on asennettuna.

Sovellus on asennettu valmiiksi kaikille uusille kirjautumisyrityksille ja kokeiluversioihin. Tutustu tarkemmin sovellusten asentamiseen Marketplacesta: [Laajennusten asentaminen ja poistaminen](../ui-extensions-install-uninstall.md#install). Noudata alla mainittuja ohjeita, jos sinulla ei ole [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaa.

## <a name="installing-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>**Dynamics 365 Business Central**-sovelluksen asentaminen Shopify-verkkokauppaan

Olemassa olevan [!INCLUDE[prod_short](../includes/prod_short.md)]n osalta tämä vaihe on valinnainen, ja se voidaan ohittaa.

1. Etsi [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) -sovellus [Shopify AppStoresta](https://apps.shopify.com/)
2. Valitse **Lisää sovellus**-painike. Kirjaudu pyydettäessä Shopify-tilillesi. Valitse tarvittava verkkokauppa, jos sinulla on niitä useampia.
3. Kun olet tarkastanut tietosuojan ja käyttöoikeudet, valitse **Asenna sovellus** -painike.
  Voit etsiä ja avata asennetun **Dynamics 365 Business Central** -sovelluksen **Shopifyn hallinta** -sivupalkin **Sovellukset**-osassa.
4. Valitse **Rekisteröidy nyt** aloittaaksesi [!INCLUDE[prod_short](../includes/prod_short.md)]-kokeilun tai **Kirjaudu**, jos sinulla on jo [!INCLUDE[prod_short](../includes/prod_short.md)]. Sinut ohjataan uudelleen [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaasi [Business Centralissa](https://businesscentral.dynamics.com).
5. Seuraavat vaiheet tulisi suorittaa [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa.

## <a name="connecting-business-central-to-the-shopify-online-store"></a>Business Centralin yhdistäminen Shopify-verkkokauppaan

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.  
3. Syötä haluttu koodi **Koodi**-kenttään.  
4. Kirjoita **Shopify-URL**-kenttään verkkokaupan URL-osoite, joka on yhdistettävä. Käytä seuraavaa muotoa: `https://{shop}.myshopify.com/`.
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

