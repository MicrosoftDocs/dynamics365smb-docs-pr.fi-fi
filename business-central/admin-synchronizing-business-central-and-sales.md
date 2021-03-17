---
title: Synkronointi ja tietojen integrointi | Microsoft Docs
description: Synkronointi kopioi tiedot Microsoft Dataverse -taulukoiden ja Business Centralin tietueiden välillä ja pitää kummankin järjestelmän tiedot ajan tasalla.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 129f60744df5cd471992642318dd42ae26ee8261
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385222"
---
# <a name="synchronizing-data-in-business-central-with-microsoft-dataverse"></a>Tietojen synkronointi Business Centralissa Microsoft Dataversen avulla
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

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

## <a name="standard-table-mapping-for-synchronization"></a>Synkronoinnin vakiotaulukon yhdistämismääritys
Taulukot, kuten tilit [!INCLUDE[prod_short](includes/cds_long_md.md)]ssä yhdistetään samantyyppisiin tietoihin [!INCLUDE[prod_short](includes/prod_short.md)]ssa, kuten asiakkaisiin. [!INCLUDE[prod_short](includes/cds_long_md.md)]in tietoja käytetään määrittämällä linkkejä [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[prod_short](includes/cds_long_md.md)]in taulukoiden välille. Tätä sanotaan yhdistämiseksi.

Seuraavassa taulukossa on luettelo tavallisista yhdistämismäärityksistä [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[prod_short](includes/cds_long_md.md)]en taulukoiden välillä.

> [!TIP]
> Voit palauttaa integrointitaulukon ja kenttien yhdistämismääritysten muutokset oletusasetuksiin valitsemalla yhdistämismääritykset ja valitsemalla sitten **Käytä oletussynkronointiasetuksia**.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] | Synkronoinnin suunta | Oletussuodatin |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Myyjä/Ostaja | Käyttäjä | [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] -kontaktisuodatin: **Tila** on **Ei**, **Käyttäjällä käyttöoikeus** on **Kyllä**, Integrointikäyttäjän tila on **Ei** |
| Asiakas | Tili | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] ja [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] -tilisuodatin: **Suhdetyyppi** on **Asiakas** ja **Tila** on **Aktiivinen**. [!INCLUDE[prod_short](includes/prod_short.md)] -suodatin: **Estetty** on tyhjä (asiakasta ei ole estetty). |
| Toimittaja | Tili | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] ja [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] -tilisuodatin: **Suhdetyyppi** on **Toimittaja** ja **Tila** on **Aktiivinen**. [!INCLUDE[prod_short](includes/prod_short.md)] -suodatin: **Estetty** on tyhjä (toimittaja ei ole estetty). |
| Kontakti | Kontakti | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] ja [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] kontaktisuodatus: **Tyyppi** on **Henkilö** ja kontakti on määritetty yritykselle. [!INCLUDE[prod_short](includes/cds_long_md.md)] -kontaktisuodatin: kontakti on liitetty yritykseen ja pääasiakkaan tyyppi on **Tili** |
| Valuutta | Tapahtumavaluutta | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] |  |


### <a name="tip-for-admins-viewing-table-mappings"></a>Järjestelmänvalvojan vihje: taulukon yhdistämismääritysten näyttäminen
Voit tarkastella [!INCLUDE[prod_short](includes/cds_long_md.md)]in taulukoiden ja [!INCLUDE[prod_short](includes/prod_short.md)]in taulukoiden välistä yhdistämismääritystä **Integrointitaulukon yhdistämismääritykset** -sivulla, jossa voit käyttää myös suodattimia. [!INCLUDE[prod_short](includes/prod_short.md)]in taulukoiden kenttien ja [!INCLUDE[prod_short](includes/cds_long_md.md)]in taulukoiden sarakkeiden välinen yhdistämismääritys määritetään **Integrointitaulukon yhdistämismääritykset** -sivulla, jossa voit lisätä myös lisämäärityksen logiikan. Tässä voi hyötyä esimerkiksi synkronoinnin vianmäärityksessä.

## <a name="see-also"></a>Katso myös  
[Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md)   
[Ajoitettu synkronointi](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]