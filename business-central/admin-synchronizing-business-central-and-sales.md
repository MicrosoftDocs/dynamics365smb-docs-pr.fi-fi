---
title: Synkronointi ja tietojen integrointi | Microsoft Docs
description: Synkronointi kopioi tiedot Microsoft Dataverse -taulukoiden ja Business Centralin tietueiden välillä ja pitää kummankin järjestelmän tiedot ajan tasalla.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'Dataverse, integration, sync, synchronize, mapping'
ms.service: dynamics-365-business-central
---

# Tietojen synkronointi Business Centralissa Microsoft Dataversen avulla

Kun [!INCLUDE[prod_short](includes/cds_long_md.md)] ja [!INCLUDE[prod_short](includes/prod_short.md)] integroidaan, voit päättää, synkronoidaanko [!INCLUDE[prod_short](includes/prod_short.md)] -rivien (kuten asiakkaiden, kontaktien ja myyjien) valittujen kenttien tiedot vastaavien [!INCLUDE[prod_short](includes/cds_long_md.md)] -rivien (kuten tilien, yhteyshenkilöiden ja käyttäjien) kanssa. Rivin tyypin mukaan voit synkronoida tietoja [!INCLUDE[prod_short](includes/cds_long_md.md)]ista [!INCLUDE[prod_short](includes/prod_short.md)]iin ja päinvastoin. Lisätietoja on kohdassa [Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synkronointi käyttää seuraavia elementtejä:

* Integrointitaulukon yhdistämismääritykset
* Integrointikentän yhdistämismääritykset
* Synkronointisäännöt
* Yhdistetyt tietueet

Synkronointia määritettäessä voit yhdistää [!INCLUDE[prod_short](includes/prod_short.md)]in rivit [!INCLUDE[prod_short](includes/cds_long_md.md)]in riveihin niissä olevien tietojen synkronointia varten. Voit käynnistää synkronoinnin manuaalisesti tai aikataulun mukaan. Seuraavassa taulukossa on yleiskatsaus rivien synkronointitavoista.  

|  Tyyppi  |  Tapa  |  Katso  |  
|--------|----------|-------|  
|Manuaalinen synkronointi|Tietueet synkronoidaan rivikohtaisesti.<br /><br /> Voit synkronoida yksittäisiä [!INCLUDE[prod_short](includes/prod_short.md)]in rivejä, kuten asiakkaita, vastaavan [!INCLUDE[prod_short](includes/cds_long_md.md)]in rivin, kuten tilin, kanssa. Tämä on tapa, jolla käyttäjät yleensä käyttävät [!INCLUDE[prod_short](includes/cds_long_md.md)]in tietoja [!INCLUDE[prod_short](includes/prod_short.md)]issa.|[Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synkronointi taulukon yhdistämismäärityksen perusteella.<br /><br /> Voit synkronoida kaikki [!INCLUDE[prod_short](includes/prod_short.md)] -taulukon tietueet [!INCLUDE[prod_short](includes/cds_long_md.md)] -taulukon kanssa.|[Yksittäisen taulukon yhdistämismääritysten synkronointi](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Kaikkien taulukon yhdistämismääritysten kaikkien muokattujen tietueiden synkronointi.<br /><br /> Voit synkronoida kaikki [!INCLUDE[prod_short](includes/prod_short.md)]in taulukoiden tietueet, joita on muutettu edellisen synkronoinnin jälkeen.|[Kaikkien muokattujen tietueiden synkronointi](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Kaikkien taulukon yhdistämismääritysten kaikkien tietojen synkronointi.<br /><br /> Voit synkronoida yhdistettyjen [!INCLUDE[prod_short](includes/prod_short.md)]in taulukoiden ja [!INCLUDE[prod_short](includes/cds_long_md.md)]in taulukoiden kaikki tiedot ja luoda uusia tietueita tai rivejä kohderatkaisussa lähderatkaisun yhdistämättömille tietueille.<br /><br /> Täysi synkronointi synkronoi kaikki tiedot ja ohittaa yhdistämisen. Täysi synkronointi tehdään yleensä integrointia määritettäessä, kun vain yksi ratkaisu sisältää tietoja. Täysi synkronointi voi olla kätevä myös esittely-ympäristössä.|[Täyden synkronoinnin suorittaminen](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Ajoitettu synkronointi|Kaikkien taulukon yhdistämismääritysten kaikkien tietojen muutosten synkronointi.<br /><br /> Voit synkronoida [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[prod_short](includes/cds_long_md.md)]in tietyin väliajoin määrittämällä työt työjonoon.|[Ajoitettu synkronointi](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

> [!NOTE]
> [!INCLUDE[prod_short](includes/cds_long_md.md)] -ohjelman ja [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman välinen synkronointi työjono tapahtumien aikataulutetun suorituksen perusteella ei takaa kahden palvelun reaaliaikaisen tietojen yhdenmukaisuutta. Reaaliaikaisten tietojen johdonmukaisuuden varmistamiseksi voit tutkia [Business Centralin virtuaalitauluja](/dynamics365/business-central/dev-itpro/powerplatform/powerplat-overview) tai Business Centralin ohjelmointirajapintaa.   

## Synkronoinnin vakiotaulukon yhdistämismääritys

Taulukot, kuten tilit [!INCLUDE[prod_short](includes/cds_long_md.md)]ssä yhdistetään samantyyppisiin tietoihin [!INCLUDE[prod_short](includes/prod_short.md)]ssa, kuten asiakkaisiin. [!INCLUDE[prod_short](includes/cds_long_md.md)]in tietoja käytetään määrittämällä linkkejä [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[prod_short](includes/cds_long_md.md)]in taulukoiden välille. Tätä sanotaan yhdistämiseksi.

Seuraavassa taulukossa on luettelo tavallisista yhdistämismäärityksistä [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[prod_short](includes/cds_long_md.md)]en taulukoiden välillä.

> [!TIP]
> Voit palauttaa integrointitaulukon ja kenttien yhdistämismääritysten muutokset oletusasetuksiin valitsemalla yhdistämismääritykset ja valitsemalla sitten **Käytä oletussynkronointiasetuksia**.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] | Synkronoinnin suunta | Oletussuodatin |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Myyjä/Ostaja | Käyttäjä | [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] -kontaktisuodatin: **Tila** on **Ei**, **Käyttäjällä käyttöoikeus** on **Kyllä**, Integrointikäyttäjän tila on **Ei** |
| Asiakas | Tili | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] ja [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] -tilisuodatin: **Suhdetyyppi** on **Asiakas** ja **Tila** on **Aktiivinen**. [!INCLUDE[prod_short](includes/prod_short.md)] -suodatin: **Estetty**on tyhjä (asiakasta ei ole estetty). |
| Toimittaja | Tili | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] ja [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] -tilisuodatin: **Suhdetyyppi** on **Toimittaja** ja **Tila** on **Aktiivinen**. [!INCLUDE[prod_short](includes/prod_short.md)] -suodatin: **Estetty**on tyhjä (toimittaja ei ole estetty). |
| Kontakti | Kontakti | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] ja [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] kontaktisuodatus: **Tyyppi** on **Henkilö** ja kontakti on määritetty yritykselle. [!INCLUDE[prod_short](includes/cds_long_md.md)] -kontaktisuodatin: kontakti on liitetty yritykseen ja pääasiakkaan tyyppi on **Asiakas**. |
| Valuutta | Tapahtumavaluutta | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] |  |

> [!NOTE]
> **Dataverse**-toiminnot eivät ole käytettävissä sivuilla, esimerkiksi Asiakaskortti-sivulla, jos tietueessa ei ole käytössä integroinnin taulukon yhdistämismäärityksen taulukkosuodatusta.

### Järjestelmänvalvojan vihje: taulukon yhdistämismääritysten näyttäminen

Voit tarkastella [!INCLUDE[prod_short](includes/cds_long_md.md)]in taulukoiden ja [!INCLUDE[prod_short](includes/prod_short.md)]in taulukoiden välistä yhdistämismääritystä **Integrointitaulukon yhdistämismääritykset** -sivulla, jossa voit käyttää myös suodattimia. [!INCLUDE[prod_short](includes/prod_short.md)]in taulukoiden kenttien ja [!INCLUDE[prod_short](includes/cds_long_md.md)]in taulukoiden sarakkeiden välinen yhdistämismääritys määritetään **Integrointitaulukon yhdistämismääritykset** -sivulla, jossa voit lisätä myös lisämäärityksen logiikan. Tässä voi hyötyä esimerkiksi synkronoinnin vianmäärityksessä.

## Virtuaalitaulukoiden käyttäminen tietojen hakemiseksi

Kun olet määrittämässä integrointia, voit käyttää virtuaalitaulukoita, jotta saat enemmän tietoa saataville kohteessa [!INCLUDE[prod_short](includes/cds_long_md.md)] ilman kehittäjän apua.

Virtuaalinen taulukko on mukautettu taulukko, jonka sarakkeissa ja riveillä on tietoja ulkoisesta tietolähteestä, kuten [!INCLUDE [prod_short](includes/prod_short.md)]. Virtuaalitaulukon sarakkeet ja rivit näyttävät tavalliselta taulukolta, mutta tietoja ei tallenneta [!INCLUDE[prod_short](includes/cds_long_md.md)] -tietokannan fyysiseen taulukkoon. Sen sijaan tiedot haetaan ajon aikana.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] sisältää objekteja, joita kutsutaan myös virtuaalitaulukoiksi. Nämä taulukon objektit eivät liity virtuaalitaulukoihin, joita käytetään kohteen [!INCLUDE[prod_short](includes/cds_long_md.md)] kanssa.

Lisätietoja virtuaalitaulukoista on seuraavissa artikkeleissa:

* [Ulkoisen tietolähteen tietoja sisältävien virtuaalitaulukoiden luominen ja muokkaaminen](/power-apps/maker/data-platform/create-edit-virtual-entities) (Power Apps -dokumentaatio)
* [Business Centralin virtuaalitaulukko Microsoft Dataverse -järjestelmänvalvojan viittauksia varten](/business-central/dev-itpro/powerplatform/powerplat-admin-reference) ([!INCLUDE [prod_short](includes/prod_short.md)] -dokumentaatio)

Virtuaalitaulukoiden käyttäminen edellyttää, että asennat **Business Central -virtuaaliobjekti** -sovelluksen [AppSourcesta](https://appsource.microsoft.com/en-US/product/dynamics-365/microsoftdynsmb.businesscentral_virtualentity). 

Kun olet asentanut sovelluksen, voit ottaa virtuaalitaulukot käyttöön jollakin seuraavista seuraavista sivuista kohteessa [!INCLUDE [prod_short](includes/prod_short.md)]:

* Kun suoritat **Määritä Dataverse-yhteys** -asetusten ohjatun määrityksen oppaan, voit valita useita virtuaalitaulukoita **Dataversen käytettävissä olevat virtuaalitaulukot** -sivulla. Sen jälkeen taulukot ovat käytettävissä kohteessa [!INCLUDE[prod_short](includes/cds_long_md.md)] ja PowerApps Maker Portalissa. 
* **Dataverse-yhteyden asetukset**-, **Virtuaalitaulukot**- ja **Käytettävissä olevat virtuaalitaulukot** -sivuilta.  
* Power App Maker Portalista.

## Useiden yritysten tai ympäristöjen tietojen synkronoiminen

Voit synkronoida usean [!INCLUDE [prod_short](includes/prod_short.md)] -yrityksen tai -ympäristön tietoja [!INCLUDE[prod_short](includes/cds_long_md.md)] -ympäristön kanssa. Usean yrityksen synkronointiskenaarioissa on harkittavana useita asioita.

### Yrityksen tunnusten määrittäminen

Kun synkronoit tietueita, määritämme [!INCLUDE[prod_short](includes/cds_long_md.md)] -entiteetille yritystunnuksen, joka selkeyttää [!INCLUDE [prod_short](includes/prod_short.md)] -yritystä, josta tietueet ovat peräisin. Integrointitaulukon yhdistämismäärityksissä on integrointitaulukon suodatuskentät, joissa yritystunnus otetaan huomioon. Jos haluat sisällyttää taulukon yhdistämismäärityksen usean yrityksen asetuksiin, valitse **Integrointitaulukon yhdistämismääritys** -sivulta **Usean yrityksen synkronointi käytössä** -valintaruutu. Asetus optimoi sen, miten integrointitaulukon suodatuskentät suodattavat yrityksen tunnukset usean yrityksen asetuksissa.

Integrointitaulukon määritysten kohdalla, jotka synkronoivat asiakirjoja, kuten tilauksia, tarjouksia ja mahdollisuuksia, valitsemalla **Usean yrityksen synkronointi käytössä** -valintaruudun, integrointi ottaa huomioon vain ne objektit, joilla on nykyisen [!INCLUDE [prod_short](includes/prod_short.md)] -yrityksen yritystunnus. Kun haluat synkronoida asiakirjoja esimerkiksi Business Centralin ja Salesin välillä, Salesin käyttäjien on määritettävä yrityksen tunnus asiakirjoissa. Muussa tapauksessa asiakirjat eivät synkronoidu.  

Muissa integrointitaulukon yhdistämismäärityksessä, kun valitset **Usean yrityksen synkronointi käytössä** -valintaruudun, poistat suodattimen yrityksen tunnuksesta. Synkronoinnissa otetaan huomioon asiaan liittyvät objektit yrityksen tunnuksista riippumatta.

### Määritä synkronointisuunta

Jos otat usean yrityksen tuen käyttöön integrointitaulukon yhdistämismäärityksessä, on suositeltavaa määrittää määrityksen suunnaksi **FromIntegration**. Jos asetat suunnaksi **ToIntegration** tai **Bidirectional**, on hyvä käyttää **Taulukkosuodatusta** ja **Integrointitaulukkosuodatusta**, kun halutaan hallita, mitkä objektit synkronoidaan minkäkin yrityksen kanssa. On myös hyvä käyttää vastaavuuteen perustuvaa yhdistämistä, jotta vältetään tietueiden kopioiden luominen. Lisätietoja vastaavuuteen perustuvasta yhdistämisestä on kohdassa [Vastaavuuteen perustuvan yhdistämisen mukauttaminen](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#customize-the-match-based-coupling).

### Käytä yksilöllisiä numeroita

Jos numerosarjasi eivät takaa, että perusavainarvot ovat yksilöllisiä jokaisessa yrityksessä, on suositeltavaa käyttää etuliitteitä. Kun haluat aloittaa etuliitteiden käytön, luo muuntosääntö integrointikenttien yhdistämismääritykseen. Lisätietoja muutossäännöistä on [Kenttien arvojen erojen käsitteleminen](admin-how-to-modify-table-mappings-for-synchronization.md#handle-differences-in-field-values) -kohdassa.

## Katso myös  

[Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md)   
[Ajoitettu synkronointi](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
