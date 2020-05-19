---
title: Synkronoitavien taulujen ja kenttien yhdistäminen | Microsoft Docs
description: Tietoja taulujen ja kenttien yhdistämistietojen synkronoinnista Business Centralin ja Common Data Servicen välillä.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 04/20/2020
ms.author: bholtorf
ms.openlocfilehash: 0a6d6e08db723979fa938488bb0df6fb08a5c4d1
ms.sourcegitcommit: 99915b493a7e49d12c530f2f9fda1fcedb518b6e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2020
ms.locfileid: "3271988"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Synkronoitavien taulujen ja kenttien yhdistäminen
Tietojen synkronointi [!INCLUDE[d365fin](includes/d365fin_md.md)]ssa  [!INCLUDE[d365fin](includes/cds_long_md.md)]ssa olevien tietojen kanssa perustuu taulujen ja tietoja sisältävien kenttien yhdistämiseen toisiinsa. Yhdistäminen tapahtuu integrointitaulujen avulla. 

## <a name="mapping-integration-tables"></a>Integrointitaulujen yhdistämismääritys
Integrointitaulu on [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietokannassa, joka edustaa entiteettiä, kuten tiliä, [!INCLUDE[cds_long_md](includes/cds_long_md.md)]ssa. integrointitaulut sisältävät kenttiä, jotka vastaavat taulun kenttiä [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-entiteetissä. Esimerkiksi Tilin integrointi -taulu muodostaa yhteyden Tilit-entiteettiin kohteessa [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. Jokaista  [!INCLUDE [cds_short_md](includes/cds_short_md.md)]in entiteettiä kohden, jonka haluat synkronoida [!INCLUDE[prodshort](includes/prodshort.md)]ssa olevien tietojen kanssa, on oltava integraatiotaulun yhdistämismääritys.

Kun luot yhteyden sovellusten välille, [!INCLUDE[d365fin](includes/d365fin_md.md)] määrittää joitakin oletusarvoisia taulujen ja kenttien yhdistämismäärityksiä. Halutessasi voit myös muuttaa taulujen yhdistämismäärityksiä. Lisätietoja on kohdassa [Synkronoinnin vakioentiteettien yhdistämismääritys](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization). Jos olet muuttanut oletusmäärityksiä ja haluat peruuttaa tekemäsi muutokset, valitse **[!INCLUDE[d365fin](includes/cds_long_md.md)] -yhteyden asetukset** -sivulla **Käytä oletussynkronointiasetuksia**.

> [!Note]
> Jos käytössä on paikallinen versio [!INCLUDE[d365fin](includes/d365fin_md.md)]sta, integrointitaulun yhdistämismääritykset tallennetaan taulun 5335 integrointitaulukon yhdistämismäärityksiin, ja niitä voidaan tarkastella ja muokata sivun 5335 Integrointitaulumäärityksistä. Monimutkaiset yhdistämismääritykset ja synkronoinnin säännöt on määritetty codeunitissa 5341. 

### <a name="synchronization-rules"></a>Synkronointisäännöt
Integrointitaulun yhdistämismääritys sisältää myös sääntöjä, jotka ohjaavat sitä, miten integroinnin synkronointityöt synkronoivat taulun [!INCLUDE[d365fin](includes/d365fin_md.md)] tietueet ja entiteetin [!INCLUDE[d365fin](includes/cds_long_md.md)]-kohteessa. <!--For examples of rules for an integration with Sales, see [Synchronization Rules](admin-synchronizing-business-central-and-sales.md#synchronization-rules). need to verify link -->

## <a name="mapping-integration-fields"></a>Integraatiokenttien yhdistäminen
Yhdistämistaulut ovat vasta ensimmäinen vaihe. Sinun täytyy myös yhdistää taulujen kentät. Integrointikenttien yhdistämismääritykset linkittävät [!INCLUDE[d365fin](includes/d365fin_md.md)]taulujen kentät vastaaviin kenttiin [!INCLUDE[d365fin](includes/cds_long_md.md)]ssä ja määrittävät, synkronoidaanko kunkin taulun tiedot. Vakiomuotoinen taulunyhdistämismääritys, jonka [!INCLUDE[d365fin](includes/d365fin_md.md)] tarjoaa, sisältää kenttien yhdistämismääritykset, mutta voit halutessasi muuttaa niitä. Lisätietoja on kohdassa [Entiteettien yhdistämismääritysten tarkasteleminen](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings).

> [!Note]
> Jos käytössä on paikallinen versio [!INCLUDE[d365fin](includes/d365fin_md.md)]sta, integrointikenttien yhdistämismääritykset on määritelty taulun 5336 integrointikenttien yhdistämismäärityksessä.

### <a name="handling-differences-in-field-values"></a>Kenttien arvojen erojen käsitteleminen
Joskus kenttien arvot, jotka haluat yhdistää, ovat erilaisia. Esimerkiksi [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa Yhdysvaltojen kielikoodi on U.S., mutta [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä se on US. Tämä tarkoittaa, että arvo on muunnettava, kun tietoja synkronoidaan. Tämä tapahtuu muutossäännöillä, jotka määrität kentille. Muunnossäännöt määritetään **Integrointitaulukon yhdistämismääritykset** -sivulla valitsemalla **Yhdistämismääritys** ja sitten **Kentät**. Ennalta määritetyt säännöt ovat käytettävissä, mutta voit myös luoda omia sääntöjä. Lisätietoja on kohdassa [Muunnossäännöt](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### <a name="handling-missing-option-values-in-mapping"></a>Puuttuvien asetusarvojen käsitteleminen yhdistämismäärityksessä
[!INCLUDE[d365fin](includes/cds_long_md.md)] sisältää asetusjoukkokentät, joissa on **Asetus**-tyyppiä oleviin [!INCLUDE[d365fin](includes/d365fin_md.md)] -kenttiin yhdistettävät arvot automaattista synkronointia varten. Synkronoinnin aikana muut kuin yhdistetyt asetukset ohitetaan ja puuttuvat asetukset liitetään liittyvään [!INCLUDE[d365fin](includes/d365fin_md.md)] -tauluun ja lisätään **CDS-asetuksen yhdistäminen** -järjestelmätauluun myöhemmin tapahtuvaa manuaalista käsittelemistä varten. Voit esimerkiksi lisätä puuttuvat asetukset tuotteeseen ja päivittää sitten yhdistämismäärityksen. Lisätietoja on kohdassa [Puuttuvien asetusarvojen käsitteleminen](admin-cds-missing-option-values.md).

## <a name="coupling-records"></a>Tietueiden yhdistäminen
Kytkentä linkittää tietueet kohteessa [!INCLUDE[d365fin](includes/cds_long_md.md)] tietueisiin kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)]. Esimerkiksi tilit kohteessa [!INCLUDE[d365fin](includes/cds_long_md.md)] yhdistetään tyypillisesti asiakkaisiin kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kytkentätietueet tarjoavat seuraavat edut:

* Se tekee synkronoinnin mahdolliseksi.
* Käyttäjät voivat avata tietueita yhdessä yrityssovelluksessa toisesta. Tämän edellytyksenä on, että sovellukset on jo integroitu.

Kytkennät voidaan määrittää automaattisesti synkronoinnin töiden avulla tai manuaalisesti muokkaamalla tietuetta kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)]. Lisätietoja on kohdassa [Tietojen synkronoiminen kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)] ja [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) ja [Tietueiden kytkeminen ja synkronointi manuaalisesti](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)i.

## <a name="filtering-records"></a>Tietueiden suodattaminen  
Jos et halua synkronoida kaikkia tietyssä [!INCLUDE[d365fin](includes/cds_long_md.md)] -objektin tai [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukon tietueita, voit määrittää suodattimia rajoittamaan synkronoitavia tietueita. Suodattimet määritetään **Integrointitaulukon yhdistämismääritykset** -sivulla.  

#### <a name="to-filter-records-for-synchronization"></a>Synkronoitavien tietueiden suodattaminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Integrointitaulukon yhdistämismääritykset** ja valitse sitten liittyvä linkki.

2.  Voit suodattaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueita määrittämällä **Taulukkosuodatus**-kentän.  

3.  Voit suodattaa [!INCLUDE[d365fin](includes/cds_long_md.md)]in tietueita määrittämällä **Integrointitaulukon suodatus** -kentän.  

## <a name="creating-new-records"></a>Uusien tietueiden luominen  
Oletusarvoisesti vain yhdistetyt [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[d365fin](includes/cds_long_md.md)]in tietueet synkronoidaan integroinnin synkronointitöissä. Voit määrittää taulukon yhdistämismäärityksiä siten, että uudet tietueet luodaan kohteeseen (kuten [!INCLUDE[d365fin](includes/d365fin_md.md)]iin) kullekin lähteen tietueelle (kuten [!INCLUDE[d365fin](includes/cds_long_md.md)]), jota ei ole yhdistetty.  

Esimerkiksi MYYJÄT - Dynamics 365 Sales -synkronointityö käyttää taulukon yhdistämismääritystä MYYJÄT. Synkronointityö kopioi tiedot [!INCLUDE[d365fin](includes/cds_long_md.md)]in käyttäjätietueista [!INCLUDE[d365fin](includes/d365fin_md.md)]in myyjätietueisiin. Jos määrität yhdistämismääritykset luomaan uusia tietueita, jokaiselle [!INCLUDE[d365fin](includes/cds_long_md.md)]in käyttäjälle, jota ei vielä ole yhdistetty [!INCLUDE[d365fin](includes/d365fin_md.md)]in myyjään, luodaan uusi myyjätietue [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.  

#### <a name="to-create-new-records-during-synchronization"></a>Uusien tietueiden luominen synkronoinnin aikana  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Integrointitaulukon yhdistämismääritykset** ja valitse sitten liittyvä linkki.

2.  Poista luettelossa taulukon yhdistämismäärityksessä **Synkronoi vain yhdistetyt tietueet** -kentän arvo.  

## <a name="using-configuration-templates-on-table-mappings"></a>Määritysmallien käyttäminen taulukon yhdistämismäärityksissä
Määritysmallit voidaan määrittää taulumäärityksiin käyttämään uusia tietueita, jotka on luotu [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tai [!INCLUDE[d365fin](includes/cds_long_md.md)]issa. Voit määrittää kuhunkin taulukon yhdistämismääritykseen määritysmallin käytettäväksi uusissa [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueissa ja toisen mallin käytettäväksi uusissa [!INCLUDE[d365fin](includes/cds_long_md.md)]in tietueissa.  

Jos asennat oletussynkronointimäärityksen, kaksi määritysmallia luodaan useimmiten automaattisesti ja käytetään [!INCLUDE[d365fin](includes/d365fin_md.md)] -asiakkaiden ja [!INCLUDE[crm_md](includes/crm_md.md)] -tilien taulukon yhdistämismäärityksiin: **CDSCUST** ja **CDSACCOUNT**.  

-   **CDSCUST** luo ja synkronoi uudet asiakkaat [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen tilin perusteella.  

     Tämä malli on luotu kopioimalla sovelluksessa asiakkaille aiemmin luotu määritysmalli. **CDSCUST** luodaan vain, jos aiemmin luotu määritysmalli on olemassa ja mallin **Valuuttakoodi**-kenttä on tyhjä. Jos määritysmallin jossain kentässä on arvo, kyseistä arvoa käytetään [!INCLUDE[d365fin](includes/cds_long_md.md)]in tilin kentässä määritetyn arvon sijasta. Jos esimerkiksi [!INCLUDE[d365fin](includes/cds_long_md.md)] -tilin **Maa/alue**-kentässä on *Yhdysvallat* ja määritysmallin **Maa/alue**-kentässä on *Iso-Britannia*, sitten *Iso-Britannia* on myös [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakkaan **Maa/alue**-arvo.  

-   **CDSACCOUNT** luo ja synkronoi uusia käyttäjätilejä [!INCLUDE[d365fin](includes/cds_long_md.md)]ssa [!INCLUDE[d365fin](includes/d365fin_md.md)] tilin perusteella.  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Määritysmallien määrittäminen taulukon yhdistämismäärityksessä  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Integrointitaulukon yhdistämismääritykset** ja valitse sitten liittyvä linkki.

2.  Valitse luettelossa taulukon yhdistämismääritystapahtuman **Taulukon määritysmallin koodi** -kentässä [!INCLUDE[d365fin](includes/d365fin_md.md)]in uusissa tietueissa käytettävä määritysmalli.  

3.  Määritä määritysmallille **Integrointitaulukon määritysmallin koodi** -kenttä, jota käytetään [!INCLUDE[d365fin](includes/cds_long_md.md)]in uusissa tietueissa.

## <a name="see-also"></a>Katso myös  
[Tietoja Dynamics 365 Business Centralin ja [!INCLUDE[d365fin](includes/cds_long_md.md)]in integroinnista](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Business Centralin ja [!INCLUDE[d365fin](includes/cds_long_md.md)]in synkronointi](admin-synchronizing-business-central-and-sales.md)   
[Ajoitettu synkronointi](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
