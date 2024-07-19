---
title: Microsoft Dynamics 365 Field Service ‑integrointi
description: Integroi Business Central Field Servicen kanssa.
ms.date: 02/21/2024
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---

# <a name="integrate-with-microsoft-dynamics-365-field-service"></a>Microsoft Dynamics 365 Field Service ‑integrointi

Huolto-organisaatiot tarvitsevat kokonaisvaltaisen sovelluksen, jossa taloustiedot, varasto ja hankinta on kytketty tiukasta huollon toimittamiseen. Jokainen tapahtuma muodostaa niissä taloustietoja. Jokainen työtilaus on sekä kustannus että tuotto; jokainen resurssi tuottaa voittoa ja tappiota. Asiakasvuorovaikutukset lisäävät tapahtumia pääkirjanpitoon. [!INCLUDE [prod_short](includes/prod_short.md)]in ja [!INCLUDE [field-service-short](includes/field-service-short.md)]in välinen integrointi sujuvoittaa huollon hallintatoimintojen kokonaisvaltaista hallintaa sekä varmistaa sujuvan tiedonkulun järjestelmien välillä.  

[!INCLUDE [field-service-short](includes/field-service-short.md)]ssa on helppo luoda ja hallita työtilauksia, seurata huoltotehtävien edistymistä, määrittää resursseja ja siepata kulutustiedot. Kun työtilaus valmistuu [!INCLUDE [field-service-short](includes/field-service-short.md)]ssa, integrointi mahdollistaa tietojen siirron sujuvasti [!INCLUDE [prod_short](includes/prod_short.md)]iin lisäkäsittelyä varten.  

Integrointi edistää myös työtilausten laskutusta ja täyttämistä [!INCLUDE [prod_short](includes/prod_short.md)]issa. [!INCLUDE [field-service-short](includes/field-service-short.md)]en kirjattujen huoltoaktiviteettien ja kulutuksen perusteella voidaan luoda tarkkoja laskuja.  

[!INCLUDE [prod_short](includes/prod_short.md)]in ja [!INCLUDE [field-service-short](includes/field-service-short.md)]en integroinnin ansiosta tietoja ei tarvitse syöttää manuaalisesti eikä samoja tehtäviä tarvitse tehdä kahdesti. Integrointi mahdollistaa myös kattavan näkymän huoltotoiminnoista ja taloustiedosta, mikä parantaa päätöksentekoa ja tehostaa toimintaa.

## <a name="prerequisites"></a>Vaatimukset

Koska [!INCLUDE [field-service-short](includes/field-service-short.md)] pohjautuu Dynamics 365 Salesiin, [Dataverse-yhteys on määritettävä](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#to-use-the-dataverse-connection-setup-assisted-setup-guide) ja [Dynamics 365 Sales -integrointi otettava käyttöön](/dynamics365/business-central/admin-prepare-dynamics-365-for-sales-for-integration#connection-settings-in-the-setup-guide).

Kenttäpalvelun integrointi -sovellus [AppSource](https://go.microsoft.com/fwlink/?linkid=2277917) on ladattava ja asennettava siihen [!INCLUDE [prod_short](includes/prod_short.md)].

### <a name="permissions-and-security-roles-for-user-accounts"></a>Käyttäjätilien käyttöoikeudet ja käyttöoikeusroolit

Kun integrointiratkaisua asennetaan, integroinnin käyttäjätilin käyttöoikeudet määritetään. Jos nämä käyttöoikeudet muuttuvat, ne on ehkä palautettava alkuperäisiksi. Se tehdään asentamalla integrointiratkaisu **Dynamics 365 -yhteyden määritys** -sivulla valitsemalla **Ota integrointiratkaisu uudelleen käyttöön**. Seuraavissa osissa käsitellään käyttöoikeuksia ja käyttöoikeusrooleja, jotka ratkaisu ottaa käyttöön kussakin sovelluksessa.

#### <a name="sales"></a>Myynti

* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]in integroinnin järjestelmänvalvoja
* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]in integraation käyttäjä
* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)] -tuotteen saatavuuden käyttäjä

#### <a name="business-central"></a>Business Central

Projektipäiväkirjoja kirjaavilla on oltava seuraava käyttöoikeuksien joukko:

* Dynamics 365 Sales -integrointi

#### <a name="field-service"></a>Field Service

Käyttäjät tarvitset seuraavan käyttöoikeusroolin integroitujen tietojen käyttämiseen:

* Business Central Field Service -integrointi

Käyttäjällä on oltava tämä rooli esimerkiksi työtilausten yhdistämiseen [!INCLUDE [prod_short](includes/prod_short.md)]iin käsittelyä varten.

> [!NOTE]
> On varmistettava, että käyttäjille on määritetty vakiokäyttöoikeusroolit ja -profiilit [!INCLUDE [field-service-short](includes/field-service-short.md)]ssa.  
>
> Lisätietoja sarakkeen suojausprofiileista [!INCLUDE [field-service-short](includes/field-service-short.md)]ssa on kohdassa [Field Servicen käyttöoikeusroolit](/dynamics365/field-service/users-licenses-permissions#field-service-security-roles).
>
> Järjestelmänvalvojien on lisättävä Power Platformissa käyttäjille yksi soveltuvista sarakkeen suojausprofiileista. Lisätietoja on kohdassa [Käytön hallinta lisäämällä ryhmiä tai käyttäjiä sarakkeen suojausprofiilin](/power-platform/admin/add-teams-users-field-security-profile).

> [!NOTE]
> Voidaksesi käyttää **Avaa Business Centralissa** -toimintoa Salesissa, sinulla on oltava seuraavat oikeudet seuraaville taulukoille:
>
> * **Dynamics 365 Business Central -yhteys** (nav_connection) -taulukkoon on oltava **lukuoikeudet**.
> * **Dynamics 365 Business Central -oletusyhteys** (nav_defaultconnection) -taulukkoon on oltava **luku**-, **kirjoitus**- ja **poisto**-oikeudet.

### <a name="other-settings-in-field-service"></a>Muut Field Servicen asetukset

**Field Service -asetukset** -sivun muutosten määritys:

* Tyhjennä **Osto**-välilehden **Varastosta loppuneiden tuotteiden käyttö** -kenttä. Muussa tapauksessa voidaan varoitus varastosta loppumisesta, kun valitaan tuote, joka on loppunut varastosta [!INCLUDE [field-service-short](includes/field-service-short.md)] mutta jota on varastossa [!INCLUDE [prod_short](includes/prod_short.md)]issa.
* Ota **Laske hinta** ja **Laske kustannus** käyttöön vaihtopainikkeella **Työtila tai varaus** -välilehdessä Valitse **Työtilauksen laskun luonti** -kentässä **Ei koskaan**.

> [!NOTE]
> Yhteyden muodostaminen [!INCLUDE [field-service-short](includes/field-service-short.md)]en poistaa resurssien ja tuotteiden välisen yhdistämisen. [!INCLUDE [prod_short](includes/prod_short.md)] -nimikkeet saadaan käyttöön [!INCLUDE [field-service-short](includes/field-service-short.md)]ssa päivittämällä **Field Servicen tuotteen tyyppi** vastaamaan nimikkeiden **Tyyppi**-kenttää [!INCLUDE [prod_short](includes/prod_short.md)]issa. Lisätietoja on kohdassa [Tuotteen tai palvelun luominen](/dynamics365/field-service/create-product-or-service#create-a-product-or-service).

## <a name="set-up-the-integration-in-business-central"></a>Integroinnin määrittäminen Business Centralissa

Kun yhteys Dataverseen ja Salesiin on muodostettu, [!INCLUDE [field-service-short](includes/field-service-short.md)] -integrointi voidaan määrittää.

* Lataa ja asenna Field Service Integration -sovellus kohteesta [AppSource](https://go.microsoft.com/fwlink/?linkid=2277917).  **Myöhemmin etsi Laajennustenhallinta-sivulta** Field Service Integration -sovellus ja suorita avustetun asetusoppaan suorittaminen valitsemalla **Määritä-toiminto** .
* Ohjatun asetusten määritysopas suoritetaan valitsemalla [!INCLUDE [prod_short](includes/prod_short.md)]in **Asetusten ohjattu määritys** -sivulla **Määritä Dynamics 365 Field Service -integrointi**.

Tässä osassa käsitellään oppaan tärkeitä asetuksia.

Henkilöt voivat kirjata [!INCLUDE [field-service-short](includes/field-service-short.md)] -työtilausten nimikkeiden ja palvelujen kulutuksen, kun **Projektipäiväkirjan malli** ja **Projektipäiväkirjan erä** määritetään käyttämään tuotteiden ja palvelujen kulutuksen kirjaamista.

Palvelut ilmaistaan [!INCLUDE [field-service-short](includes/field-service-short.md)]ssa kestona, **Tunnit mittayksikkö** on määritettävä käyttämään kestojen muuntamista määriksi [!INCLUDE [prod_short](includes/prod_short.md)]issa.

Lisäksi voidaan määrittää, milloin työtilauksen tuotteet ja huoltorivit synkronoidaan [!INCLUDE [prod_short](includes/prod_short.md)]iin. Synkronointi voidaan tehdä esimerkiksi silloin, kun työtilauksen rivejä käytetään tai kun työtilaus valmistuu. Sopiva vaihtoehto valitaan **Synkronoi työtilauksen tuotteet/palvelut** -kentässä.

Kun työtilauksen tuotteet ja palvelut on synkronoitu [!INCLUDE [prod_short](includes/prod_short.md)]in projektipäiväkirjoihin, voidaan valita, kirjataanko projektipäiväkirjat manuaalisesti. Sopiva vaihtoehto valitaan **Kirjaa projektipäiväkirjan rivit automaattisesti** -kentässä.

* Kun työtilaus on valmis.
* Kun työtilauksen tuotteita tai palveluja käytetään.

Määritysten valmistumisen jälkeen suoritetaan täydellinen synkronointi **Dynamics 365 Field Service -integroinnin asetukset** -sivulta. Tämä toiminto synkronoi esimerkiksi seuraavankaltaiset taulukon yhdistämismääritykset.

* Projektitehtävät projekteissa, joissa **Käytä käyttölinkkiä** on määritetty. Tämä synkronoinnin avulla [!INCLUDE [prod_short](includes/prod_short.md)]in projekteja voidaan valita [!INCLUDE [field-service-short](includes/field-service-short.md)]ssa.
* Resurssit, joita ei ole estetty, joissa **Käytä aikaraporttia** ei ole valittu ja joissa **Tunnit** on määritetty mittayksiköksi **Dynamics 365 Field Service -integroinnin asetukset** -sivulla.
* Huoltonimikkeet (edellyttää, että käytössä on [!INCLUDE [prod_short](includes/prod_short.md)]in Premium-käyttökokemus).

## <a name="standard-field-service-entity-mapping-for-synchronization"></a>Synkronoinnin Field Service -yksikön vakioyhdistämismääritys

Tietojen synkronointi [!INCLUDE [prod_short](includes/prod_short.md)]in taulukoiden ja kenttien yhdistämiseen Dataversen taulukoihin ja sarakkeisiin, jotta sovellukset voivat vaihtaa tietoja. Yhdistäminen tapahtuu integrointitaulujen avulla. Lisätietoja taulukon yhdistämismäärityksistä on kohdassa [Synkronoitavien taulujen ja kenttien yhdistäminen](/dynamics365/business-central/admin-how-to-modify-table-mappings-for-synchronization).

[!INCLUDE [field-service-short](includes/field-service-short.md)] -integrointi ottaa käyttöön seuraavat integrointitaulukon vakioyhdistämismääritykset:

* **PJLINE-WORDERPRODUCT** – yhdistää työtilauksen tuotteet [!INCLUDE [field-service-short](includes/field-service-short.md)]ssa ja projektipäiväkirjan riveille [!INCLUDE [prod_short](includes/prod_short.md)]issa.
* **PJLINE-WORDERSERVICE** – yhdistää työtilauksen palvelut [!INCLUDE [field-service-short](includes/field-service-short.md)]ssa ja projektipäiväkirjan riveille [!INCLUDE [prod_short](includes/prod_short.md)]issa.
* **PROJECTTASK** – yhdistää [!INCLUDE [prod_short](includes/prod_short.md)]in projektit ja projektitehtävät ulkoisten projektien tuotteisiin [!INCLUDE [field-service-short](includes/field-service-short.md)]ssa.
* **RESOURCE-BOOKABLERSC** – yhdistää [!INCLUDE [prod_short](includes/prod_short.md)]in resurssit varattavissa oleviin [!INCLUDE [field-service-short](includes/field-service-short.md)]n resursseihin.
* **SVCITEM-CUSTASSET** – (vain Premium-kokemus) yhdistää [!INCLUDE [prod_short](includes/prod_short.md)]in huoltonimikkeet asiakkaan resursseihin [!INCLUDE [field-service-short](includes/field-service-short.md)]ssa.

## <a name="use-data-in-both-applications"></a>Tietojen käyttäminen kummassakin sovelluksissa

Seuraavissa osissa käsitellään toimintoja, joissa voidaan käyttää [!INCLUDE [prod_short](includes/prod_short.md)]in ja [!INCLUDE [field-service-short](includes/field-service-short.md)] -ohjelmasta saatavia tietoja.

### <a name="field-service-1"></a>Kenttähuolto

Voit [luoda työtilauksia](/dynamics365/field-service/create-work-order) käyttämällä [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman **palvelutiliä** ja **laskutustiliä**. Työtilauksissa on valittava **Business Central -projektitehtävä** **Ulkoinen projekti** -kentässä. Projektin valinta mahdollistaa työtilauksen tuotteiden ja palvelujen synkronoinnin oikeaan projektitehtävään [!INCLUDE [prod_short](includes/prod_short.md)]issa.

Työtilauksiin voi lisätä varastonimikkeitä ja muita kuin varastonimikkeitä, kuten **Työtilauksen tuotteet**. Tällä tavoin saadaan varastosaldo sekä kustannukset ja hinnat [!INCLUDE [prod_short](includes/prod_short.md)]ista. Lisätietoja on kohdassa [Työtilauksen luominen työtilauslomakkeesta ja tietueluettelosta](/dynamics365/field-service/create-work-order#create-a-work-order-from-the-work-order-form-and-record-list).

Huoltotyyppisiä nimikkeitä voidaan lisätä **työtilauksen palveluina**, jonka jälkeen kustannukset ja hinnat saadaan [!INCLUDE [prod_short](includes/prod_short.md)]ista. Lisätietoja on kohdassa [Tuotteet ja palvelut -välilehti](/dynamics365/field-service/work-order-experience#products-and-services-tab).

> [!NOTE]
> Kun työtilauksen tuotteen tai palvelun tila **Arvioitu** muuttuu tilaksi **Käytetty** [!INCLUDE [field-service-short](includes/field-service-short.md)]ssa, ne synkronoidaan projektipäiväkirjan riveille [!INCLUDE [prod_short](includes/prod_short.md)]issa. in .

Resurssi voidaan varata ja liittää **varaukset** työtilauksen palveluihin käyttämällä **Varattavissa oleva resurssi** -vaihtoehtoa [!INCLUDE [prod_short](includes/prod_short.md)]issa.

### <a name="business-central-1"></a>Business Central

**Field Service -integroinnin asetukset** -sivun asetusten mukaan tuotteita ja palveluja sisältävien työtilausten kulutustiedot siirretään ja kirjataan [!INCLUDE [prod_short](includes/prod_short.md)]in **projektipäiväkirjan** avulla.

**Laskutettava määrä**- ja **Laskutuksen kesto** -arvot kopioidaan **Laskuun siirrettävä määrä** -kenttään. Näiden arvojen perusteella voidaan laskuttaa asiakasta luomalla ja kirjaamalla myyntilaskuja [!INCLUDE [prod_short](includes/prod_short.md)]issa. Kun lasku on kirjattu tai kulutus käsitelty [!INCLUDE [prod_short](includes/prod_short.md)]issa, laskutettu määrä ja kulutettu määrä näkyvät **Työtilauksen tuote**- ja **Työtilauksen palvelu** -sivujen [!INCLUDE [prod_short](includes/prod_short.md)] -välilehdessä.  

**Projektin suunnittelurivit** -sivulla voi seurata työtilauksen kulutuksen kirjaamista ja laskuttamista. **Projektin suunnittelurivit** -sivulla voidaan luoda ja kirjata myyntilaskuja [!INCLUDE [prod_short](includes/prod_short.md)]issa. Ne voidaan myöhemmin synkronoida [!INCLUDE [field-service-short](includes/field-service-short.md)]en, jossa voidaan seurata laskujen tilaa.

> [!NOTE]
> Työtilauspalvelut, joissa on varaus, jossa käytetään varattavissa olevaa resurssia ja joka on yhdistetty [!INCLUDE [prod_short](includes/prod_short.md)] -resurssiin, synkronoidaan kahteen projektipäiväkirjan riviin: yhteen liitettyyn resurssiin liittyvä **budjetti**-tyyppinen rivi ja huollettavan nimikkeen toinen **Laskutettava**-tyyppinen rivi.
>
> Työtilauksen palveluun valittu tuote on yhdistettävä nimikkeeseen, jonka tyyppi [!INCLUDE [prod_short](includes/prod_short.md)]issa on **Palvelu**. Lisäksi nimikkeen perusmittayksiköksi on määritettävä **Tunnit mittayksikkö**, joka on valittu **Dynamics 365 Field Service -integroinnin asetukset** -sivulla.
>
> **Palvelu**-tyyppisen nimikkeen lasku voidaan luoda laskutettavan projektin suunnitteluriviltä, kun taas budjetin projektin suunnitteluriviä käytetään rekisteröimään resurssin kustannus.

## <a name="see-also"></a>Katso myös

[Microsoft Dataverse-integrointi tietojen synkronoinnin avulla](admin-common-data-service.md)  
[Synkronoitavien taulujen ja kenttien yhdistäminen](admin-how-to-modify-table-mappings-for-synchronization.md)
