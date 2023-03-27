---
title: Shopifyn yhdistimen käytön aloittaminen
description: Ensimmäiset vaiheet määritettäessä Business Centralin ja Shopifyn välistä yhteyttä
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: AndreiPanko
ms.author: andreipa
---

# Shopifyn yhdistimen käytön aloittaminen

Yhdistä Shopify-kauppasi [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelmaan ja maksimoi yrityksesi tuottavuus. Hallitse ja tarkastele yrityksesi ja Shopify-kauppasi merkityksellisiä tietoja yhtenä yksikkönä.

Jos haluat käyttää Shopifyta yhdessä [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelman kanssa, sinun on ensin tehtävä joitakin asioita. Tämä artikkeli toimii oppaana, jonka avulla voit integroida Shopify-kaupan [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelman kanssa.

## Vaatimukset Shopifylle

Tarvitaan:

- Shopify-tili
- Shopify-verkkokauppa

Lisätietoja Shopify-kokeiluversioiden luomisesta ja suositelluista asetuksista on kohdassa [Shopify-tilin luominen ja määrittäminen](shopify-account.md).

## Business Centralin edellytykset

- Varmista **[Shopify-yhdistin](https://go.microsoft.com/fwlink/?linkid=2196238)**-sovellus on asennettuna.

  Sovellus on asennettu valmiiksi kaikille uusille kirjautumisyrityksille ja kokeiluversioihin. Tutustu tarkemmin sovellusten asentamiseen AppSourcesta: [Laajennusten asentaminen ja poistaminen](../ui-extensions-install-uninstall.md#install). Noudata alla mainittuja ohjeita, jos sinulla ei ole [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaa.

- Varmista, että käyttäjällä on riittävät käyttöoikeudet. Shopify-yhdistin sisältyy *Shopify – Admin (SHPFY – ADMIN)* -käyttöoikeuksien joukkoon. Lisätietoja on kohdissa [Luo käyttäjät käyttöoikeuksien mukaan](../ui-how-users-permissions.md) ja [Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](../ui-define-granular-permissions.md)


## Asenna Dynamics 365 Business Central -sovellus Shopify-verkkokauppaasi

Olemassa olevan [!INCLUDE[prod_short](../includes/prod_short.md)]n osalta tämä vaihe on valinnainen, ja se voidaan ohittaa.

1. Etsi [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) -sovellus [Shopify AppStoresta](https://apps.shopify.com/)
2. Valitse **Lisää sovellus**-painike. Kirjaudu Shopify-tilillesi, jos ohjelma pyytää. Valitse tarvittava verkkokauppa, jos sinulla on niitä useampia.
3. Kun olet tarkastanut tietosuojan ja käyttöoikeudet, valitse **Asenna sovellus** -painike.

   Voit etsiä ja avata asennetun **Dynamics 365 Business Central** -sovelluksen **Shopifyn hallinta** -sivupalkin osassa **Sovellukset**-sivulla.
4. Valitse **Rekisteröidy nyt** aloittaaksesi [!INCLUDE[prod_short](../includes/prod_short.md)]-kokeilun tai **Kirjaudu**, jos sinulla on jo [!INCLUDE[prod_short](../includes/prod_short.md)]. Sinut ohjataan uudelleen [Business Central](https://businesscentral.dynamics.com) -sivullesi.
5. Seuraavat vaiheet tulisi suorittaa [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa.

## Business Centralin yhdistäminen Shopify-verkkokauppaan

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.  
3. Syötä **Koodi**-kenttään koodi, jonka avulla etsiminen on helppoa [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa. Nimi voi esimerkiksi kuvastaa sitä, mitä kauppa myy, kuten "huonekalut" tai "kahvi", tai maata tai aluetta, jossa se palvelee.
4. Syötä **Shopify-URL**-kenttään verkkokaupan URL-osoite, joka on yhdistettävä. Käytä seuraavaa muotoa: `https://{shop}.myshopify.com/`.
5. Aktivoi **käytössä**-vaihto, tarkista ja hyväksy ehdot ja edellytykset.
6. Kirjaudu pyydettäessä sisään Shopify-tiliisi, tarkista tietosuojaehdot ja käyttöoikeudet ja valitse sitten **Asenna sovellus** -painike.

Toista vaiheet 2-6 kaikille verkkokaupoille, jotka haluat yhdistää.

### Tunnetut ongelmat

- Selain estää ponnahdusikkunan. Kun otat käyttöön **Käytössä**-vaihtoehdon, järjestelmä avaa **Odotetaan vastausta - Älä sulje tätä sivu sivua** -sivun, joka odottaa käyttöoikeustunnusta Shopifysta, jos sivu on suljettu tai estetty – et voi muodostaa yhteyttä Shopifyhin. Lisätietoja on kohdassa [pyydä käyttöoikeustunnusta](troubleshoot.md#request-the-access-token)
- [Oauth-virhe invalid_request: Shopify-sovellusrajapintasovellusta ei löytynyt api_key-arvolla](troubleshoot.md#oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Yhteyttä ei voi muodostaa eritysympäristöstä](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment)


## Seuraavat vaiheet

Nyt verkkokauppa on yhteydessä [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan. Seuraavissa vaiheissa määritetään, miten ja mitä synkronoidaan.

- [Kohteiden synkronointi](synchronize-items.md)
- [Asiakkaiden synkronointi](synchronize-customers.md)
- [Tilausten synkronointi](synchronize-orders.md)

## Katso myös

[Vaihekuvaus: Shopify-yhdistimen määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-shopify.md)  

