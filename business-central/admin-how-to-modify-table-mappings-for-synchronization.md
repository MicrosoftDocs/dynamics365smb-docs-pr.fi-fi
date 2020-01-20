---
title: Synkronoitavien taulujen ja kenttien yhdistäminen | Microsoft Docs
description: Tietoja taulujen ja kenttien yhdistämistietojen synkronoinnista Business Centralin ja Dynamics 365 Salesin välillä.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 12/18/2019
ms.author: bholtorf
ms.openlocfilehash: 371bd80c04917495ea1b35f214d10d716ed5f9ad
ms.sourcegitcommit: b570997f93d1f7141bc9539c93a67a91226660a8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943111"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Synkronoitavien taulujen ja kenttien yhdistäminen
Tietojen synkronointi [!INCLUDE[d365fin](includes/d365fin_md.md)]ssa  [!INCLUDE[crm_md](includes/crm_md.md)]ssa olevien tietojen kanssa perustuu taulujen ja tietoja sisältävien kenttien yhdistämiseen toisiinsa. Yhdistäminen tapahtuu integrointitaulujen avulla. 

## <a name="mapping-integration-tables"></a>Integrointitaulujen yhdistämismääritys
Integrointitaulu on [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietokannassa, joka edustaa entiteettiä, kuten tiliä, [!INCLUDE[crm_md](includes/crm_md.md)]ssa. integrointitaulut sisältävät kenttiä, jotka vastaavat taulun kenttiä [!INCLUDE[crm_md](includes/crm_md.md)]-entiteetissä. Esimerkiksi Tilin integrointi -taulu muodostaa yhteyden Tilit-entiteettiin kohteessa [!INCLUDE[crm_md](includes/crm_md.md)]. Jokaista  [!INCLUDE[crm_md](includes/crm_md.md)]in entiteettiä kohden, jonka haluat synkronoida [!INCLUDE[d365fin](includes/d365fin_md.md)]]ssa olevien tietojen kanssa, on oltava integraatiotaulun yhdistämismääritys.

Kun luot yhteyden sovellusten välille, [!INCLUDE[d365fin](includes/d365fin_md.md)] määrittää joitakin oletusarvoisia taulujen ja kenttien yhdistämismäärityksiä. Halutessasi voit myös muuttaa taulujen yhdistämismäärityksiä. Lisätietoja on kohdassa [Synkronoinnin vakiomyyntiobjektin yhdistämismääritys](admin-synchronizing-business-central-and-sales.md#standard-sales-entity-mapping-for-synchronization). Jos olet muuttanut oletusmäärityksiä ja haluat peruuttaa tekemäsi muutokset, valitse**Dynamics 365-yhteyden asetukset** -sivulla **Käytä oletussynkronointiasetuksia**.

> [!Note]
> Jos käytössä on paikallinen versio [!INCLUDE[d365fin](includes/d365fin_md.md)]sta, integrointitaulun yhdistämismääritykset tallennetaan taulun 5335 integrointitaulukon yhdistämismäärityksiin, ja niitä voidaan tarkastella ja muokata sivun 5335 Integrointitaulumäärityksistä. Monimutkaiset yhdistämismääritykset ja synkronoinnin säännöt on määritetty codeunitissa 5341. 

### <a name="synchronization-rules"></a>Synkronointisäännöt
Integrointitaulun yhdistämismääritys sisältää myös sääntöjä, jotka ohjaavat sitä, miten integroinnin synkronointityöt synkronoivat taulun [!INCLUDE[d365fin](includes/d365fin_md.md)] tietueet ja entiteetin [!INCLUDE[crm_md](includes/crm_md.md)]-kohteessa. Lisätietoja on kohdassa [Synkronointisäännöt](admin-synchronizing-business-central-and-sales.md#synchronization-rules). 

## <a name="mapping-integration-fields"></a>Integraatiokenttien yhdistäminen
Yhdistämistaulut ovat vasta ensimmäinen vaihe. Sinun täytyy myös yhdistää taulujen kentät. Integrointikenttien yhdistämismääritykset linkittävät [!INCLUDE[d365fin](includes/d365fin_md.md)]taulujen kentät vastaaviin kenttiin [!INCLUDE[crm_md](includes/crm_md.md)]ssä ja määrittävät, synkronoidaanko kunkin taulun tiedot. Vakiomuotoinen taulunyhdistämismääritys, jonka [!INCLUDE[d365fin](includes/d365fin_md.md)] tarjoaa, sisältää kenttien yhdistämismääritykset, mutta voit halutessasi muuttaa niitä. Lisätietoja on kohdassa [Entiteettien yhdistämismääritysten tarkasteleminen](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings).

> [!Note]
> Jos käytössä on paikallinen versio [!INCLUDE[d365fin](includes/d365fin_md.md)]sta, integrointikenttien yhdistämismääritykset on määritelty taulun 5336 integrointikenttien yhdistämismäärityksessä.

## <a name="coupling-records"></a>Tietueiden yhdistäminen
Kytkentä linkittää tietueet kohteessa [!INCLUDE[crm_md](includes/crm_md.md)] tietueisiin kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)]. Esimerkiksi tilit kohteessa [!INCLUDE[crm_md](includes/crm_md.md)] yhdistetään tyypillisesti asiakkaisiin kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kytkentätietueet tarjoavat seuraavat edut:

* Se tekee synkronoinnin mahdolliseksi.
* Käyttäjät voivat avata tietueita yhdessä yrityssovelluksessa toisesta. Tämä edellyttää, että [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrointiratkaisu on asennettu kohteeseen [!INCLUDE[crm_md](includes/crm_md.md)].

Kytkennät voidaan määrittää automaattisesti synkronoinnin töiden avulla tai manuaalisesti muokkaamalla tietuetta kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)]. Lisätietoja on kohdassa [Tietojen synkronoiminen kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md) ja [Tietueiden kytkeminen ja synkronointi manuaalisesti](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)i.

## <a name="filtering-records"></a>Tietueiden suodattaminen  
Jos et halua synkronoida kaikkia tietyssä [!INCLUDE[crm_md](includes/crm_md.md)] -objektin tai [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukon tietueita, voit määrittää suodattimia rajoittamaan synkronoitavia tietueita. Suodattimet määritetään **Integrointitaulukon yhdistämismääritykset** -sivulla.  

#### <a name="to-filter-records-for-synchronization"></a>Synkronoitavien tietueiden suodattaminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Integrointitaulukon yhdistämismääritykset** ja valitse sitten liittyvä linkki.

2.  Voit suodattaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueita määrittämällä **Taulukkosuodatus**-kentän.  

3.  Voit suodattaa [!INCLUDE[crm_md](includes/crm_md.md)]in tietueita määrittämällä **Integrointitaulukon suodatus** -kentän.  

## <a name="creating-new-records"></a>Uusien tietueiden luominen  
 Oletusarvoisesti vain yhdistetyt [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in tietueet synkronoidaan integroinnin synkronointitöissä. Voit määrittää taulukon yhdistämismäärityksiä siten, että uudet tietueet luodaan kohteeseen (kuten [!INCLUDE[d365fin](includes/d365fin_md.md)]iin) kullekin lähteen tietueelle (kuten [!INCLUDE[crm_md](includes/crm_md.md)]), jota ei ole yhdistetty.  

 Esimerkiksi MYYJÄT - Dynamics 365 Sales -synkronointityö käyttää taulukon yhdistämismääritystä MYYJÄT. Synkronointityö kopioi tiedot [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjätietueista [!INCLUDE[d365fin](includes/d365fin_md.md)]in myyjätietueisiin. Jos määrität yhdistämismääritykset luomaan uusia tietueita, jokaiselle [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjälle, jota ei vielä ole yhdistetty [!INCLUDE[d365fin](includes/d365fin_md.md)]in myyjään, luodaan uusi myyjätietue [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.  

#### <a name="to-create-new-records-during-synchronization"></a>Uusien tietueiden luominen synkronoinnin aikana  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Integrointitaulukon yhdistämismääritykset** ja valitse sitten liittyvä linkki.

2.  Poista luettelossa taulukon yhdistämismäärityksessä **Synkronoi vain yhdistetyt tietueet** -kentän arvo.  

## <a name="using-configuration-templates-on-table-mappings"></a>Määritysmallien käyttäminen taulukon yhdistämismäärityksissä
Määritysmallit voidaan määrittää taulumäärityksiin käyttämään uusia tietueita, jotka on luotu [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tai [!INCLUDE[crm_md](includes/crm_md.md)]issa. Voit määrittää kuhunkin taulukon yhdistämismääritykseen määritysmallin käytettäväksi uusissa [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueissa ja toisen mallin käytettäväksi uusissa [!INCLUDE[crm_md](includes/crm_md.md)]in tietueissa.  

Jos asennat oletussynkronointimäärityksen, kaksi määritysmallia luodaan useimmiten automaattisesti ja käytetään [!INCLUDE[d365fin](includes/d365fin_md.md)] -asiakkaiden ja [!INCLUDE[crm_md](includes/crm_md.md)] -tilien taulukkomääritysksiin: **CRMCUST** ja **CRMACCOUNT**.  

-   **CRMCUST** luo ja synkronoi uudet asiakkaat [!INCLUDE[d365fin](includes/d365fin_md.md)]issa [!INCLUDE[crm_md](includes/crm_md.md)]in tilin perusteella.  

     Tämä malli on luotu kopioimalla sovelluksessa asiakkaille aiemmin luotu määritysmalli. **CRMCUST** luodaan vain, jos aiemmin luotu määritysmalli on olemassa ja mallin **Valuuttakoodi**-kenttä on tyhjä. Jos määritysmallin jossain kentässä on arvo, kyseistä arvoa käytetään [!INCLUDE[crm_md](includes/crm_md.md)]in tilin kentässä määritetyn arvon sijasta. Jos esimerkiksi [!INCLUDE[crm_md](includes/crm_md.md)] -tilin **Maa/alue**-kentässä on *Yhdysvallat* ja määritysmallin **Maa/alue**-kentässä on *Iso-Britannia*, sitten *Iso-Britannia* on myös [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakkaan **Maa/alue**-arvo.  

-   **CRMACCOUNT** luo ja synkronoi uusia käyttäjätilejä [!INCLUDE[crm_md](includes/crm_md.md)]ssa [!INCLUDE[d365fin](includes/d365fin_md.md)] tilin perusteella.  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Määritysmallien määrittäminen taulukon yhdistämismäärityksessä  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Integrointitaulukon yhdistämismääritykset** ja valitse sitten liittyvä linkki.

2.  Valitse luettelossa taulukon yhdistämismääritystapahtuman **Taulukon määritysmallin koodi** -kentässä [!INCLUDE[d365fin](includes/d365fin_md.md)]in uusissa tietueissa käytettävä määritysmalli.  

3.  Määritä määritysmallille **Integrointitaulukon määritysmallin koodi** -kenttä, jota käytetään [!INCLUDE[crm_md](includes/crm_md.md)]in uusissa tietueissa.

## <a name="see-also"></a>Katso myös  
[Tietoja Dynamics 365 Business Centralin ja Dynamics 365 Salesin integroinnista](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Business Centralin ja Dynamics 365 Salesin synkronointi](admin-synchronizing-business-central-and-sales.md)   
[Ajoitettu synkronointi](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
