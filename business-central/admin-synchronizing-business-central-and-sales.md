---
title: Synkronointi ja tietojen integrointi | Microsoft Docs
description: Synkronointi kopioi tiedot Dynamics 365 for Salesin objektien ja Business Centralin tietueiden välillä ja pitää kummankin järjestelmän tiedot ajan tasalla.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: b5a3b83d21390711ff0517df67bf9912ece57f6b
ms.sourcegitcommit: f2e3b571eab6e01d9f5aa8ef47056b6bd313dcbd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/13/2019
ms.locfileid: "1629617"
---
# <a name="synchronizing-data-in-business-central-and-dynamics-365-for-sales"></a>Tietojen synkronointi Business Centralissa ja Dynamics 365 for Salesissa
Kun [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[d365fin](includes/d365fin_md.md)] integroidaan, voit päättää, synkronoidaanko [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietueiden (kuten asiakkaiden, kontaktien ja myyjien) valittujen kenttien tiedot vastaavien [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueiden (kuten tilien, yhteyshenkilöiden ja käyttäjien) kanssa. Tietueen tyypin mukaan voit synkronoida tietoja [!INCLUDE[crm_md](includes/crm_md.md)]ista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin ja päin vastoin. Lisätietoja on kohdassa [Dynamics 365 for Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synkronointi käyttää seuraavia elementtejä:

* Integrointitaulukon yhdistämismääritykset
* Integrointikentän yhdistämismääritykset
* Synkronointisäännöt
* Yhdistetyt tietueet

Synkronointia määritettäessä voit yhdistää [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueet [!INCLUDE[crm_md](includes/crm_md.md)]in tietueisiin niissä olevien tietojen synkronointia varten. Voit käynnistää synkronoinnin manuaalisesti tai aikataulun mukaan. Seuraavassa taulukossa on yleiskatsaus tietueiden synkronointitavoista.  

|  Tyyppi  |  Tapa  |  Katso  |  
|--------|----------|-------|  
|Manuaalinen synkronointi|Tietueet synkronoidaan tietuekohtaisesti.<br /><br /> Voit synkronoida yksittäisiä [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueita, kuten asiakkaita, vastaavan [!INCLUDE[crm_md](includes/crm_md.md)]in tietueen, kuten tiliin, kanssa. Tämä on tapa, jolla käyttäjät yleensä käyttävät [!INCLUDE[crm_md](includes/crm_md.md)]in tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.|[Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synkronointi taulukon yhdistämismäärityksen perusteella.<br /><br /> Voit synkronoida kaikki [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukon tietueet [!INCLUDE[crm_md](includes/crm_md.md)] -objektin kanssa.|[Yksittäisen taulukon yhdistämismääritysten synkronointi](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Kaikkien taulukon yhdistämismääritysten kaikkien muokattujen tietueiden synkronointi.<br /><br /> Voit synkronoida kaikki [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukoiden tietueet, joita on muutettu edellisen synkronoinnin jälkeen.|[Kaikkien muokattujen tietueiden synkronointi](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Kaikkien taulukon yhdistämismääritysten kaikkien tietojen synkronointi.<br /><br /> Voit synkronoida yhdistettyjen [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukoiden ja [!INCLUDE[crm_md](includes/crm_md.md)]in objektien kaikki tiedot ja luoda uusia tietueita kohderatkaisussa lähderatkaisun yhdistämättömille tietueille.<br /><br /> Täysi synkronointi synkronoi kaikki tiedot ja ohittaa yhdistämisen. Täysi synkronointi tehdään yleensä integrointia määritettäessä, kun vain yksi ratkaisu sisältää tietoja. Täysi synkronointi voi olla kätevä myös esittely-ympäristössä.|[Täyden synkronoinnin suorittaminen](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Ajoitettu synkronointi|Kaikkien taulukon yhdistämismääritysten kaikkien tietojen muutosten synkronointi.<br /><br /> Voit synkronoida [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in tietyin väliajoin määrittämällä työt työjonoon.|[Ajoitettu synkronointi](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Synkronoinnin Myynti-entiteetin yhdistämismääritys
Kohteet, kuten tilit [!INCLUDE[crm_md](includes/crm_md.md)]ssä yhdistetään samantyyppisiin tietoihin [!INCLUDE[d365fin](includes/d365fin_md.md)]ssa, kuten asiakkaisiin. [!INCLUDE[crm_md](includes/crm_md.md)]in tietoja käytetään määrittämällä linkkejä [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in välille. Tätä sanotaan yhdistämiseksi.

Seuraavassa taulukossa on luettelo tavallisista [!INCLUDE[d365fin](includes/d365fin_md.md)]in yhdistämismäärityksistä [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)] välillä.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[crm_md](includes/crm_md.md)]|Synkronoinnin suunta|Oletussuodatin|
|-------------------------------------------|-----|-------------------------|--------------|
|Myyjä/Ostaja|Käyttäjä|[!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-sovelluksen kontaktin suodatin: **Tila** on **Ei**, **Lisensoitu käyttäjä** on **Kyllä**, Integroinnin käyttäjä -tila on **Ei**|
|Asiakas|Tili|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-sovelluksen tilin suodatin: **Suhteen tyyppi** on **Asiakas** ja **Tila** on **Aktiivinen**.|
|Kontakti|Kontakti|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] kontaktisuodatus: **Tyyppi** on **Henkilö** ja kontakti on määritetty yritykselle. Sales-sovelluksen kontaktin suodatin: Kontakti on liitetty yritykseen ja pääyrityksen tyyppi on **Tili**|
|Valuutta|Tapahtumavaluutta|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Mittayksikkö|Yksikköryhmä|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Nimike|Tuote|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-sovelluksen kontaktin suodatin: **Tuotteen tyyppi** on **Myyntivarasto**|
|Resurssi|Tuote|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-sovelluksen kontaktin suodatin: **Tuotteen tyyppi** on **Palvelut**|
|Asiakkaan hintaryhmä|Hinnasto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Myyntihinta|Tuotehinnasto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] kontaktisuodatin: **Myyntikoodi** ei ole tyhjä, **Myyntityyppi** on **Asiakkaan hintaluokka**|
|Mahdollisuus|Mahdollisuus|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |
|Myyntilaskun otsikko|Lasku|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Myyntilaskurivi|Laskutustuote|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Myyntitilauksen otsikko|Myyntitilaus|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] Myynnin Ylätunnuksen suodatin: **Dokumenttityyppi** on Järjestys, **Tila** on Vapautettu.|
|Myyntitilauksen huomautukset|Myyntitilauksen huomautukset|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |

### <a name="tip-for-admins-viewing-entity-mappings"></a>Järjestelmänvalvojan vihje: objektin yhdistämismääritysten näyttäminen
Voit tarkastella [!INCLUDE[crm_md](includes/crm_md.md)]in objektien ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukoiden välistä yhdistämismääritystä **Integrointitaulukon yhdistämismääritykset** -sivulla, jossa voit käyttää myös suodattimia. [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukoiden kenttien ja [!INCLUDE[crm_md](includes/crm_md.md)]in objektien kenttien välinen yhdistämismääritys määritetään **Integrointitaulukon yhdistämismääritykset** -sivulla, jossa voit lisätä myös lisämäärityksen logiikan. Tässä voi hyötyä esimerkiksi synkronoinnin vianmäärityksessä.

### <a name="tip-for-developers-mapping-fields-in-business-central-to-the-option-sets-in-sales"></a>Kehittäjien vihje: Business Centralin kenttien yhdistäminen Salesin asetusjoukkoihin
Jos olet kehittäjä ja haluat lisätä asetuksia [!INCLUDE[crm_md](includes/crm_md.md)]in asetusjoukkoihin, nämä tiedot ovat välttämättömiä. [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on kolme taulukkoa, jotka yhdistetään [!INCLUDE[crm_md](includes/crm_md.md)]in **Tili**-objektin asetuskenttiin. Taulukkojen tietueita, joita ei ole linkitetty [!INCLUDE[crm_md](includes/crm_md.md)]in asetuksiin, ei synkronoida. Tämän vuoksi **Asetus**-kenttä on tyhjä [!INCLUDE[crm_md](includes/crm_md.md)]issa.

Seuraavassa taulukossa on [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukoiden [!INCLUDE[crm_md](includes/crm_md.md)]in **Tili**-objektiin **Asetus**-kentän yhdistämismääritykset.

|Sivupöytä|Tili-objektin Asetus-kenttä|
|----------------------|-------------------------------------------|
|Maksuehdot|Maksuehdot|
|Toimitusehto|Osoite 1: Kuljetusehdot|
|Kuljetusliike|Osoite 1: Toimitustapa|

### <a name="synchronization-rules"></a>Synkronointisäännöt
Seuraavassa taulukossa käsitellään sovellusten väliset synkronointisäännöt.

> [!NOTE]  
> [!INCLUDE[crm_md](includes/crm_md.md)]in muutoksia, jotka [!INCLUDE[crm_md](includes/crm_md.md)] -yhteyden käyttäjätili teki, ei synkronoida. Tämän vuoksi on suositeltavaa, että tietoja ei muuteta kyseistä tiliä käytettäessä. Lisätietoja on kohdassa [Dynamics 365 for Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md).

|Sivupöytä|Sääntö|
|-----|----|
|Asiakkaat|Ennen kuin asiakas voidaan synkronoida, asiakkaalle määritetyn myyjän on oltava yhdistettynä [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjään. Varmista tämän vuoksi CUSTOMERS - Dynamics 365 for Sales -synkronointityötä suoritettaessa ja määritettäessä uusien tietueiden luontia, että synkronoit myyjät ja [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjät, ennen kuin synkronoit asiakkaat [!INCLUDE[crm_md](includes/crm_md.md)]in tilien kanssa. <br /> <br />ASIAKKAAT – Dynamics 365 for Sales -synkronointityö synkronoi vain Sales-tilit, joiden suhdetyyppi on Asiakas.|
|Kontaktit|Vain tiliin liitetyt [!INCLUDE[crm_md](includes/crm_md.md)]in yhteystiedot luodaan [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Myyjän koodin arvo määrittää yhdistetyn entiteetin omistajan [!INCLUDE[crm_md](includes/crm_md.md)]issa.|
|Valuutat|Valuutat yhdistetään kytketään tapahtumavaluuttoihin [!INCLUDE[crm_md](includes/crm_md.md)]issa ISO-koodien perusteella. Vain valuuttoja, joilla on standardi ISO-koodi, kytketään ja synkronoidaan tapahtumanvaluuttojen kanssa.|
|Mittayksiköt|Mittayksiköt synkronoidaan yksikköryhmien kanssa [!INCLUDE[crm_md](includes/crm_md.md)]issa. Yksikköryhmälle voi määrittää vain yhden mittayksikön.|
|Nimikkeet|Kun nimikkeitä synkronisoidaan [!INCLUDE[crm_md](includes/crm_md.md)] tuotteiden kanssa [!INCLUDE[d365fin](includes/d365fin_md.md)] luo automaattisesti hintalistan [!INCLUDE[crm_md](includes/crm_md.md)]ssä. Synkronointivirheitä välttämiseksi Älä muokkaa tämän hinnaston manuaalisesti.|
|Myyjät|Myyjät yhdistetään järjestelmäkäyttäjiin [!INCLUDE[crm_md](includes/crm_md.md)]issa. Käyttäjä on otettava käyttöön ja hänellä on oltava käyttöoikeus. Käyttäjä ei voi olla integroinnin käyttäjä. Huomaa, että tämä taulukko tulee synkronoida ensimmäiseksi, koska sitä käytetään asiakkaiden, kontaktien, mahdollisuuksien ja myyntilaskujen kanssa.|
|Resurssit|Resurssit synkronoidaan niiden [!INCLUDE[crm_md](includes/crm_md.md)]in tuotteiden kanssa, joiden tyyppi on Palvelu.|
|Asiakashintaryhmät|Asiakkaan hintaryhmät synkronoidaan myyntihinnastojen kanssa.|
|Myyntihinnat|Myyntihintojen myyntityyppi on Asiakkaan hintaryhmä. Niiden määritetty myyntikoodi synkronoidaan [!INCLUDE[crm_md](includes/crm_md.md)]in hinnaston rivien kanssa.|
|Mahdollisuudet|Mahdollisuudet synkronoidaan [!INCLUDE[crm_md](includes/crm_md.md)]in mahdollisuuksien kanssa. Myyjän koodin arvo määrittää yhdistetyn entiteetin omistajan [!INCLUDE[crm_md](includes/crm_md.md)]issa.|
|Kirjatut myyntilaskut|Kirjatut myyntilaskut synkronoidaan myyntilaskujen kanssa. Ennen laskun synkronointia kannattaa synkronoida kaikki muut entiteetit, jotka voivat vaikuttaa laskuun. Niitä voivat olla esimerkiksi myyjät ja hinnastot. Laskun otsikossa oleva myyjän koodin arvo määrittää yhdistetyn entiteetin omistajan Sales-sovelluksessa.|
|Myyntitilaukset|Vapautettu myyntitilaus (otsikot) synkronoidaan myyntitilauksen kanssa. Ennen tilauksen synkronointia kannattaa synkronoida kaikki muut objektit, jotka voivat vaikuttaa tilaukseen. Niitä voivat olla esimerkiksi myyjät ja hinnastot. Tilauksen otsikossa oleva myyjän koodin arvo määrittää yhdistetyn entiteetin omistajan Salesissa.|  

## <a name="see-also"></a>Katso myös  
[Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md)   
[Ajoitettu synkronointi](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integrointi Dynamics 365 for Salesin kanssa](admin-prepare-dynamics-365-for-sales-for-integration.md)
