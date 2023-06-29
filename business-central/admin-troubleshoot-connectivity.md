---
title: Yhteyden vianmääritys
description: 'Tässä artikkelissa kuvataan, miten Business Central online -yhteyden muodostamiseen liittyviä ongelmia tunnistetaan ja korjataan Yhteyden vianmääritys -sivulla.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'connectivity, troubleshooting, connection problems'
ms.date: 06/17/2021
ms.author: jswymer
ROBOTS: NOINDEX
---
# <a name="troubleshoot-connectivity-for-business-central"></a><a name="troubleshoot-connectivity-for-business-central"></a>Business Central -yhteyden vianmääritys

> **KOHDE:** [!INCLUDE[prod_short](includes/prod_short.md)] Online
>
> Tämä ominaisuus on käytettävissä esiversiona. Toiminnot ja dokumentaatio voivat muuttua uusissa versioissa. Jos haluat osallistua dokumentaatioon omien havaintojesi perusteella, valitse ![Muokkaa artikkelia GitHubissa.](media/github-edit-pencil.png) **Muokkaa** ja ehdota muutoksia. Tutustumme sitten ehdotuksiisi!

[!INCLUDE[prod_short](includes/prod_short.md)] Online sisältää **Yhteyden vianmääritys** -sivun, jonka avulla voit tunnistaa online-palvelun yhteyteen liittyvät ongelmat. Business Central -yhteyksiin vaikuttavat useat asiat, kuten verkon palomuuriasetukset tai toimialueen nimipalvelun määritykset. Sivun avulla voit suorittaa tarkistussarjan, joka diagnosoi yleiset Business Central -yhteysongelmat. Tietojen avulla voit yrittää korjata ongelmat itse tai välittää ongelmat tukihenkilöllesi.

> [!NOTE]
> **Yhteyden vianmääritys** -sivulla ei testata verkon suorituskykyä tai luotettavuutta, kuten yhteyden nopeutta. Se tarkistaa vain yhteyden eri resursseihin.

## <a name="start-the-connectivity-check"></a><a name="start-the-connectivity-check"></a>Aloita yhteyden tarkistus

1. Avaa selain.
2. Kirjoita osoitteeksi URL-osoite, jolla Business Central avataan, ja kirjoita loppuun `/connectivity`. 

    Jos käytössä on esimerkiksi `https://businesscentral.dynamics.com`, kirjoita

    ```http
    https://businesscentral.dynamics.com/connectivity
    ```

    Tai jos URL-osoite sisältää vuokraajan tunnuksen, kuten `https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB`, kirjoita sitten

    ```http
    https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB/connectivity
    ```
 
3. Valitse **Yhteyden vianmääritys** -sivulla **Aloita tarkistus**.

    Suoritetaan sarja tarkistuksia, ja kunkin tarkistuksen tulos näytetään:

    - ![Yhteyden tarkistus onnistui.](media/connectivity-check.png) ilmaisee, että tarkistus onnistui.
    - ![Yhteyden tarkistus epäonnistui.](media/connectivity-failed.png) ilmaisee, että tarkistus epäonnistui. Katso lisätietoja tarkistuksen alla olevasta viestistä.
    - ![Yhteyden tarkistusta ei suoritettu.](media/connectivity-blocked.png) ilmaisee, että tarkistusta ei suoritettu, mikä johtuu yleensä edellisen tarkistuksen epäonnistumisesta. Katso lisätietoja tarkistuksen alla olevasta viestistä.

4. Jos haluat suorittaa tarkistuksen uudelleen, valitse **Käynnistä tarkistus uudelleen**.

Seuraavissa osissa selitetään suoritettavat tarkistukset ja annetaan vihjeitä ongelmien korjaamiseen.

## <a name="basic-internet-connectivity"></a><a name="basic-internet-connectivity"></a>Perusyhteys internetiin

Tarkistaa, että internet-yhteys on muodostunut, varmistamalla, että voit käyttää tunnettua julkista toimialuetta kuten www.bing.com.

|Ongelma|Kokeile seuraavaa:|
|-------|-------------|
|Selaimesi ei tue tätä tarkistusta|Avaa sivu tuetussa selaimessa ja yritä uudelleen. Luettelo tuetuista selaimista on kohdassa [Business Centralin käyttämisen vähimmäisvaatimukset – selaimet](product-requirements.md#browsers)|
|Palvelimen ping-komento ei onnistunut seuraavassa URL-osoitteessa: {url}|Tarkista palomuuriasetukset.|

## <a name="cdn-content-delivery-network-resources-loading"></a><a name="cdn-content-delivery-network-resources-loading"></a>CDN (content delivery network) -resurssien lataaminen

[!INCLUDE[prod_short](includes/prod_short.md)] käyttää Azure Content Delivery Network (CDN) -verkkoa, joka tarjoaa Business Central -verkkosovelluksen käyttämiseen vaadittavat resurssit. Lähettämällä ping-kutsun Business Central -ilmentymälle CDN:ssä tämä tarkistus varmistaa, että tarvittavat resurssit ovat käytettävissä.

|Ongelma|Kokeile seuraavaa:|
|-------|-------------|
|Selaimesi ei tue tätä tarkistusta|Katso **Perusyhteys internetiin** -tarkistus.|
|Palvelimen ping-komento ei onnistunut seuraavassa URL-osoitteessa: {url}|Tarkista palomuuriasetukset.|

## <a name="user-authentication"></a><a name="user-authentication"></a>Käyttäjän todennus

Tarkistaa, että nykyinen käyttäjä on kirjautunut sisään kelvollisella Business Central -tilillä.

|Ongelma|Kokeile seuraavaa:|
|-------|-------------|
|Yhtään käyttäjää ei ole todennettu|Kirjaudu Business Centraliin kelvollisen käyttäjänimen ja salasanan avulla.|

## <a name="business-central-environments-discovery"></a><a name="business-central-environments-discovery"></a>Business Central -ympäristöjen etsiminen

Tarkistaa todennetun käyttäjän käytettävissä olevat Business Central -ympäristöt ja tarkistaa sitten, voidaanko käyttäjä todentaa ympäristössä.
<!-- example: Your user name or password is incorrect, or you do not have a valid account.. Request duration: 332 milliseconds)-->

|Ongelma|Kokeile seuraavaa:|
|-------|-------------|
|Ei todennettua käyttäjää, jolle suorittaa tämä tarkistus|Katso **Käyttäjän todennus** -tarkistus.|
|Tilin käytettävissä olevien ympäristöjen noutaminen epäonnistui.|Tarkista luettelo käytettävissä olevista ympäristöistä Business Centralin hallintakeskuksessa.|
|Käyttäjänimi tai salasana ei ole oikea tai sinulla ei ole voimassa olevaa tiliä.| Varmista, että olet kirjautunut sisään oikealla käyttäjänimellä ja salasanalla.|

## <a name="application-service-connectivity"></a><a name="application-service-connectivity"></a>Sovelluspalvelun yhteys

Tarkistaa, että todennettu käyttäjä voi muodostaa yhteyden löydettyyn ympäristöön, aloittaen yleensä tuotantoympäristöstä.

|Ongelma|Kokeile seuraavaa:|
|-------|-------------|
|Ei todennettua käyttäjää, jolle suorittaa tämä tarkistus|Katso **Käyttäjän todennus -tarkistus**.|
|Tilin käytettävissä olevien ympäristöjen noutaminen epäonnistui.|Katso **Business Central -ympäristöjen etsiminen**.|
|Ei klusteriosoitetta, jolle suorittaa tämä tarkistus|Tarkista luettelo käytettävissä olevista ympäristöistä Business Centralin hallintakeskuksessa.|
|Version päätepistettä ei ole|Tarkista luettelo käytettävissä olevista ympäristöistä Business Centralin hallintakeskuksessa.|

## <a name="web-server-connectivity"></a><a name="web-server-connectivity"></a>Verkkopalvelimen yhteys

Tarkistaa, että todennettu käyttäjä pystyy muodostamaan yhteyden Web-palvelimeen onnistuneesti.

|Ongelma|Kokeile seuraavaa:|
|-------|-------------|
|Todennettua käyttäjää tämän tarkistuksen suorittamiseksi ei ole|Katso **Käyttäjän todennus -tarkistus**.|
|Tilin käytettävissä olevien ympäristöjen noutaminen epäonnistui.|Katso **Business Central -ympäristöjen etsiminen**.|
|Ei klusteriosoitetta, jolle suorittaa tämä tarkistus|Tarkista luettelo käytettävissä olevista ympäristöistä Business Centralin hallintakeskuksessa.|
|Yhteyttä verkkopalvelimeen ei voitu muodostaa|Tyhjennä välimuisti ja lataa sivu uudelleen.|

## <a name="service-health-status"></a><a name="service-health-status"></a>Palvelun kunnon tila

Raportoi Business Centralin huollon kunnon tilan tarkistamalla ilmoitetut katkokset.

|Ongelma|Kokeile seuraavaa:|
|-------|-------------|
|Todennettua käyttäjää tämän tarkistuksen suorittamiseksi ei ole|Katso **Käyttäjän todennus -tarkistus**.|
|Valitettavasti Business Central on tilapäisesti pois käytöstä. Ole hyvä ja yritä uudelleen myöhemmin.|Yritä myöhemmin uudelleen.|

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Ohje- ja tukiresurssit](product-help-and-support.md)  
[Business Centralin määritystehtävien yleiskatsaus](setup.md)  
[Usein kysyttyjä kysymyksiä Business Centralin käyttämisestä](across-faq.yml)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Business Centralin hallintakeskus](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)

[!INCLUDE[footer-include](includes/footer-banner.md)]
