---
title: Synkronointi ja tietojen integrointi | Microsoft Docs
description: Synkronointi kopioi tiedot Common Data Service -entiteettien ja Business Centralin tietueiden välillä ja pitää kummankin järjestelmän tiedot ajan tasalla.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 01629cb7e881de1c679d8c6925eaacc3a5639597
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196469"
---
# <a name="synchronizing-data-in-business-central-with-common-data-service"></a>Tietojen synkronointi Business Centralissa Common Data Servicen avulla
Kun [!INCLUDE[d365fin](includes/cds_long_md.md)] ja [!INCLUDE[d365fin](includes/d365fin_md.md)] integroidaan, voit päättää, synkronoidaanko [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietueiden (kuten asiakkaiden, kontaktien ja myyjien) valittujen kenttien tiedot vastaavien [!INCLUDE[d365fin](includes/cds_long_md.md)]in tietueiden (kuten tilien, yhteyshenkilöiden ja käyttäjien) kanssa. Tietueen tyypin mukaan voit synkronoida tietoja [!INCLUDE[d365fin](includes/cds_long_md.md)]ista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin ja päin vastoin. Lisätietoja on kohdassa [Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synkronointi käyttää seuraavia elementtejä:

* Integrointitaulukon yhdistämismääritykset
* Integrointikentän yhdistämismääritykset
* Synkronointisäännöt
* Yhdistetyt tietueet

Synkronointia määritettäessä voit yhdistää [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueet [!INCLUDE[d365fin](includes/cds_long_md.md)]in tietueisiin niissä olevien tietojen synkronointia varten. Voit käynnistää synkronoinnin manuaalisesti tai aikataulun mukaan. Seuraavassa taulukossa on yleiskatsaus tietueiden synkronointitavoista.  

|  Tyyppi  |  Tapa  |  Katso  |  
|--------|----------|-------|  
|Manuaalinen synkronointi|Tietueet synkronoidaan tietuekohtaisesti.<br /><br /> Voit synkronoida yksittäisiä [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueita, kuten asiakkaita, vastaavan [!INCLUDE[d365fin](includes/cds_long_md.md)]in tietueen, kuten tiliin, kanssa. Tämä on tapa, jolla käyttäjät yleensä käyttävät [!INCLUDE[d365fin](includes/cds_long_md.md)]in tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.|[Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synkronointi taulukon yhdistämismäärityksen perusteella.<br /><br /> Voit synkronoida kaikki [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukon tietueet [!INCLUDE[d365fin](includes/cds_long_md.md)] -objektin kanssa.|[Yksittäisen taulukon yhdistämismääritysten synkronointi](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Kaikkien taulukon yhdistämismääritysten kaikkien muokattujen tietueiden synkronointi.<br /><br /> Voit synkronoida kaikki [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukoiden tietueet, joita on muutettu edellisen synkronoinnin jälkeen.|[Kaikkien muokattujen tietueiden synkronointi](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Kaikkien taulukon yhdistämismääritysten kaikkien tietojen synkronointi.<br /><br /> Voit synkronoida yhdistettyjen [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukoiden ja [!INCLUDE[d365fin](includes/cds_long_md.md)]in objektien kaikki tiedot ja luoda uusia tietueita kohderatkaisussa lähderatkaisun yhdistämättömille tietueille.<br /><br /> Täysi synkronointi synkronoi kaikki tiedot ja ohittaa yhdistämisen. Täysi synkronointi tehdään yleensä integrointia määritettäessä, kun vain yksi ratkaisu sisältää tietoja. Täysi synkronointi voi olla kätevä myös esittely-ympäristössä.|[Täyden synkronoinnin suorittaminen](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Ajoitettu synkronointi|Kaikkien taulukon yhdistämismääritysten kaikkien tietojen muutosten synkronointi.<br /><br /> Voit synkronoida [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[d365fin](includes/cds_long_md.md)]in tietyin väliajoin määrittämällä työt työjonoon.|[Ajoitettu synkronointi](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-entity-mapping-for-synchronization"></a>Synkronoinnin vakioentiteetin yhdistämismääritys
Kohteet, kuten tilit [!INCLUDE[d365fin](includes/cds_long_md.md)]ssä yhdistetään samantyyppisiin tietoihin [!INCLUDE[d365fin](includes/d365fin_md.md)]ssa, kuten asiakkaisiin. [!INCLUDE[d365fin](includes/cds_long_md.md)]in tietoja käytetään määrittämällä linkkejä [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[d365fin](includes/cds_long_md.md)]in välille. Tätä sanotaan yhdistämiseksi.

Seuraavassa taulukossa on luettelo tavallisista [!INCLUDE[d365fin](includes/d365fin_md.md)]in yhdistämismäärityksistä [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[d365fin](includes/cds_long_md.md)] välillä.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/cds_long_md.md)]|Synkronoinnin suunta|Oletussuodatin|
|-------------------------------------------|-----|-------------------------|--------------|
|Myyjä/Ostaja|Käyttäjä|[!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-sovelluksen kontaktin suodatin: **Tila** on **Ei**, **Lisensoitu käyttäjä** on **Kyllä**, Integroinnin käyttäjä -tila on **Ei**|
|Asiakas|Tili|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-sovelluksen tilin suodatin: **Suhteen tyyppi** on **Asiakas** ja **Tila** on **Aktiivinen**.|
|Toimittaja|Tili|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-sovelluksen tilin suodatin: **Suhteen tyyppi** on **Toimittaja** ja **Tila** on **Aktiivinen**.|
|Kontakti|Kontakti|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] kontaktisuodatus: **Tyyppi** on **Henkilö** ja kontakti on määritetty yritykselle. Sales-sovelluksen kontaktin suodatin: Kontakti on liitetty yritykseen ja pääyrityksen tyyppi on **Tili**|
|Valuutta|Tapahtumavaluutta|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |


### <a name="tip-for-admins-viewing-entity-mappings"></a>Järjestelmänvalvojan vihje: objektin yhdistämismääritysten näyttäminen
Voit tarkastella [!INCLUDE[d365fin](includes/cds_long_md.md)]in objektien ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukoiden välistä yhdistämismääritystä **Integrointitaulukon yhdistämismääritykset** -sivulla, jossa voit käyttää myös suodattimia. [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukoiden kenttien ja [!INCLUDE[d365fin](includes/cds_long_md.md)]in objektien kenttien välinen yhdistämismääritys määritetään **Integrointitaulukon yhdistämismääritykset** -sivulla, jossa voit lisätä myös lisämäärityksen logiikan. Tässä voi hyötyä esimerkiksi synkronoinnin vianmäärityksessä.

## <a name="see-also"></a>Katso myös  
[Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md)   
[Ajoitettu synkronointi](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md)
