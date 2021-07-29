---
title: Yhteyden vianmääritys
description: Tässä artikkelissa kuvataan, miten Business Central online -yhteyden muodostamiseen liittyviä ongelmia tunnistetaan ja korjataan Yhteyden vianmääritys -sivulla.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: connectivity, troubleshooting, connection problems
ms.date: 06/17/2021
ms.author: jswymer
ROBOTS: NOINDEX
ms.openlocfilehash: db7b9e602817d7dddcf6bce1b35ede078bd70aa0
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443179"
---
# <a name="troubleshoot-connectivity-for-business-central"></a>Business Central -yhteyden vianmääritys

> **KOHDE:** [!INCLUDE[prod_short](includes/prod_short.md)] Online
>
> Tämä ominaisuus on käytettävissä esiversiona. Toiminnot ja dokumentaatio voivat muuttua uusissa versioissa. Jos haluat osallistua dokumentaatioon omien havaintojesi perusteella, valitse ![Muokkaa artikkelia GitHubissa.](media/github-edit-pencil.png) **Muokkaa** ja ehdota muutoksia. Tutustumme sitten ehdotuksiisi!

[!INCLUDE[prod_short](includes/prod_short.md)] Online sisältää **Yhteyden vianmääritys** -sivun, jonka avulla voit tunnistaa online-palvelun yhteyteen liittyvät ongelmat. Business Central -yhteyksiin vaikuttavat useat asiat, kuten verkon palomuuriasetukset tai toimialueen nimipalvelun määritykset. Sivun avulla voit suorittaa tarkistussarjan, joka diagnosoi yleiset Business Central -yhteysongelmat. Tietojen avulla voit yrittää korjata ongelmat itse tai välittää ongelmat tukihenkilöllesi.

> [!NOTE]
> **Yhteyden vianmääritys** -sivulla ei testata verkon suorituskykyä tai luotettavuutta, kuten yhteyden nopeutta. Se tarkistaa vain yhteyden eri resursseihin.

## <a name="start-the-connectivity-check"></a>Aloita yhteyden tarkistus 

1. Valitse [tämä linkki](https://businesscentral.dynamics.com/connectivity) tai avaa Internet-selain ja kirjoita osoitteeseen seuraava URL-osoite:

    ```http
    https://businesscentral.dynamics.com/connectivity
    ```

2. Valitse **Yhteyden vianmääritys** -sivulla **Aloita tarkistus**.

    Suoritetaan sarja tarkistuksia, ja kunkin tarkistuksen tulos näytetään:

    - ![Yhteyden tarkistus onnistui.](media/connectivity-check.png) ilmaisee, että tarkistus onnistui.
    - ![Yhteyden tarkistus epäonnistui.](media/connectivity-failed.png) ilmaisee, että tarkistus epäonnistui. Katso lisätietoja tarkistuksen alla olevasta viestistä.
    - ![Yhteyden tarkistusta ei suoritettu.](media/connectivity-blocked.png) ilmaisee, että tarkistusta ei suoritettu, mikä johtuu yleensä edellisen tarkistuksen epäonnistumisesta. Katso lisätietoja tarkistuksen alla olevasta viestistä.

3. Jos haluat suorittaa tarkistuksen uudelleen, valitse **Käynnistä tarkistus uudelleen**.

Seuraavissa osissa selitetään suoritettavat tarkistukset ja annetaan vihjeitä ongelmien korjaamiseen.

## <a name="basic-internet-connectivity"></a>Perusyhteys internetiin

Tarkistaa, että internet-yhteys on muodostunut, varmistamalla, että voit käyttää tunnettua julkista toimialuetta kuten www.bing.com.

|Ongelma|Kokeile seuraavaa:|
|-------|-------------|
|Selaimesi ei tue tätä tarkistusta|Avaa sivu tuetussa selaimessa ja yritä uudelleen. Luettelo tuetuista selaimista on kohdassa [Business Centralin käyttämisen vähimmäisvaatimukset – selaimet](product-requirements.md#browsers)|
|Palvelimen ping-komento ei onnistunut seuraavassa URL-osoitteessa: {url}|Tarkista palomuuriasetukset.|

## <a name="cdn-content-delivery-network-resources-loading"></a>CDN (content delivery network) -resurssien lataaminen

[!INCLUDE[prod_short](includes/prod_short.md)] käyttää Azure Content Delivery Network (CDN) -verkkoa, joka tarjoaa Business Central -verkkosovelluksen käyttämiseen vaadittavat resurssit. Lähettämällä ping-kutsun Business Central -ilmentymälle CDN:ssä tämä tarkistus varmistaa, että tarvittavat resurssit ovat käytettävissä.

|Ongelma|Kokeile seuraavaa:|
|-------|-------------|
|Selaimesi ei tue tätä tarkistusta|Katso **Perusyhteys internetiin** -tarkistus.|
|Palvelimen ping-komento ei onnistunut seuraavassa URL-osoitteessa: {url}|Tarkista palomuuriasetukset.|

## <a name="user-authentication"></a>Käyttäjän todennus

Tarkistaa, että nykyinen käyttäjä on kirjautunut sisään kelvollisella Business Central -tilillä.

|Ongelma|Kokeile seuraavaa:|
|-------|-------------|
|Yhtään käyttäjää ei ole todennettu|Kirjaudu Business Centraliin kelvollisen käyttäjänimen ja salasanan avulla.|

## <a name="business-central-environments-discovery"></a>Business Central -ympäristöjen etsiminen

Tarkistaa todennetun käyttäjän käytettävissä olevat Business Central -ympäristöt ja tarkistaa sitten, voidaanko käyttäjä todentaa ympäristössä.
<!-- example: Your user name or password is incorrect, or you do not have a valid account.. Request duration: 332 milliseconds)-->

|Ongelma|Kokeile seuraavaa:|
|-------|-------------|
|Ei todennettua käyttäjää, jolle suorittaa tämä tarkistus|Katso **Käyttäjän todennus** -tarkistus.|
|Tilin käytettävissä olevien ympäristöjen noutaminen epäonnistui.|Tarkista luettelo käytettävissä olevista ympäristöistä Business Centralin hallintakeskuksessa.|
|Käyttäjänimi tai salasana ei ole oikea tai sinulla ei ole voimassa olevaa tiliä.| Varmista, että olet kirjautunut sisään oikealla käyttäjänimellä ja salasanalla.|

## <a name="application-service-connectivity"></a>Sovelluspalvelun yhteys

Tarkistaa, että todennettu käyttäjä voi muodostaa yhteyden löydettyyn ympäristöön, aloittaen yleensä tuotantoympäristöstä.

|Ongelma|Kokeile seuraavaa:|
|-------|-------------|
|Ei todennettua käyttäjää, jolle suorittaa tämä tarkistus|Katso **Käyttäjän todennus -tarkistus**.|
|Tilin käytettävissä olevien ympäristöjen noutaminen epäonnistui.|Katso **Business Central -ympäristöjen etsiminen**.|
|Ei klusteriosoitetta, jolle suorittaa tämä tarkistus|Tarkista luettelo käytettävissä olevista ympäristöistä Business Centralin hallintakeskuksessa.|
|Version päätepistettä ei ole|Tarkista luettelo käytettävissä olevista ympäristöistä Business Centralin hallintakeskuksessa.|

## <a name="see-also"></a>Katso myös

[Ohje- ja tukiresurssit](product-help-and-support.md)  
[Business Centralin määritystehtävien yleiskatsaus](setup.md)  
[Usein kysyttyjä kysymyksiä Business Centralin käyttämisestä](across-faq.yml)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Business Centralin hallintakeskus](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)

[!INCLUDE[footer-include](includes/footer-banner.md)]
