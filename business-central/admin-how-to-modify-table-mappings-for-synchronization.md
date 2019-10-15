---
title: Taulukon yhdistämismääritysten muokkaaminen synkronointia varten | Microsoft Docs
description: Tietoja Business Centralin ja Dynamics 365 Salesin väliseen tietojen synkronointiin käytettävien taulukon yhdistämismääritysten muuttamisesta.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 505c1427c63a0a6f9e68980ea0ff05c93918ea60
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308069"
---
# <a name="modify-table-mappings-for-synchronization"></a>Taulukon yhdistämismääritysten muokkaaminen synkronointia varten
Integrointitaulukon yhdistämismääritys liittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukon [!INCLUDE[crm_md](includes/crm_md.md)] -objektin integrointitaulukkoon. Kullakin [!INCLUDE[crm_md](includes/crm_md.md)] -objektilla, jonka kanssa haluat synkronoida vastaavat [!INCLUDE[d365fin](includes/d365fin_md.md)]in tiedot, on oltava vastaava integrointitaulukon yhdistämismääritys. Integrointitaulukon yhdistämismääritys sisältää useita asetuksia, joiden avulla voit määrittää miten [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukon tietueet ja [!INCLUDE[crm_md](includes/crm_md.md)] -objekti synkronoidaan vastaavissa integroinnin synkronointitöissä.  

## <a name="filtering-records"></a>Tietueiden suodattaminen  
 Jos et halua synkronoida kaikkia tietyssä [!INCLUDE[crm_md](includes/crm_md.md)] -objektin tai [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukon tietueita, voit määrittää suodattimia rajoittamaan synkronoitavia tietueita. Suodattimet määritetään **Integrointitaulukon yhdistämismääritykset** -sivulla.  

#### <a name="to-filter-records-for-synchronization"></a>Synkronoitavien tietueiden suodattaminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Integrointitaulukon yhdistämismääritykset** ja valitse sitten liittyvä linkki.

2.  Voit suodattaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueita määrittämällä **Taulukkosuodatus**-kentän.  

3.  Voit suodattaa [!INCLUDE[crm_md](includes/crm_md.md)]in tietueita määrittämällä **Integrointitaulukon suodatus** -kentän.  

## <a name="creating-new-records"></a>Uusien tietueiden luominen  
 Oletusarvoisesti vain yhdistetyt [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in tietueet synkronoidaan integroinnin synkronointitöissä. Voit määrittää taulukon yhdistämismäärityksiä siten, että uudet tietueet luodaan kohteeseen (kuten [!INCLUDE[d365fin](includes/d365fin_md.md)]iin) kullekin lähteen tietueelle (kuten [!INCLUDE[crm_md](includes/crm_md.md)]), jota ei ole yhdistetty.  

 Esimerkiksi MYYJÄT - Dynamics 365 Sales -synkronointityö käyttää taulukon yhdistämismääritystä MYYJÄT. Synkronointityö kopioi tiedot [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjätietueista [!INCLUDE[d365fin](includes/d365fin_md.md)]in myyjätietueisiin. Jos määrität yhdistämismääritykset luomaan uusia tietueita, jokaiselle [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjälle, jota ei vielä ole yhdistetty [!INCLUDE[d365fin](includes/d365fin_md.md)]in myyjään, luodaan uusi myyjätietue [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.  

#### <a name="to-create-new-records-during-synchronization"></a>Uusien tietueiden luominen synkronoinnin aikana  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Integrointitaulukon yhdistämismääritykset** ja valitse sitten liittyvä linkki.

2.  Poista luettelossa taulukon yhdistämismäärityksessä **Synkronoi vain yhdistetyt tietueet** -kentän arvo.  

## <a name="using-configuration-templates-on-table-mappings"></a>Määritysmallien käyttäminen taulukon yhdistämismäärityksissä
Määritysmallit voidaan määrittää taulumäärityksiin käyttämään uusia tietueita, jotka on luotu [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tai [!INCLUDE[crm_md](includes/crm_md.md)]issa. Voit määrittää kuhunkin taulukon yhdistämismääritykseen määritysmallin käytettäväksi uusissa [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueissa ja toisen mallin käytettäväksi uusissa [!INCLUDE[crm_md](includes/crm_md.md)]in tietueissa.  

Jos asennat oletussynkronointimäärityksen, kaksi määritysmallia luodaan useimmiten automaattisesti ja käytetään [!INCLUDE[d365fin](includes/d365fin_md.md)] -asiakkaiden ja [!INCLUDE[crm_md](includes/crm_md.md)] -tilien taulukkomääritysksiin: **CRMCUST** ja **CRMACCOUNT**.  

-   **CRMCUST** luo ja synkronoi uudet asiakkaat [!INCLUDE[d365fin](includes/d365fin_md.md)]issa [!INCLUDE[crm_md](includes/crm_md.md)]in tilin perusteella.  

     Tämä malli on luotu kopioimalla sovelluksessa asiakkaille aiemmin luotu määritysmalli. **CRMCUST** luodaan vain, jos aiemmin luotu määritysmalli on olemassa ja mallin **Valuuttakoodi**-kenttä on tyhjä. Jos määritysmallin jossain kentässä on arvo, kyseistä arvoa käytetään [!INCLUDE[crm_md](includes/crm_md.md)]in tilin kentässä määritetyn arvon sijasta. Jos esimerkiksi [!INCLUDE[crm_md](includes/crm_md.md)] -tilin **Maa/alue**-kentässä on *Yhdysvallat* ja määritysmallin **Maa/alue**-kentässä on *Iso-Britannia*, sitten *Iso-Britannia* on myös [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakkaan **Maa/alue**-arvo.  

-   **CRMACCOUNT** luo ja synkronoi uusia käyttäjätilejä [!INCLUDE[crm_md](includes/crm_md.md)]ssa [!INCLUDE[d365fin](includes/d365fin_md.md)] tilin perusteella.  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Määritysmallien määrittäminen taulukon yhdistämismäärityksessä  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Integrointitaulukon yhdistämismääritykset** ja valitse sitten liittyvä linkki.

2.  Valitse luettelossa taulukon yhdistämismääritystapahtuman **Taulukon määritysmallin koodi** -kentässä [!INCLUDE[d365fin](includes/d365fin_md.md)]in uusissa tietueissa käytettävä määritysmalli.  

3.  Määritä määritysmallille **Integrointitaulukon määritysmallin koodi** -kenttä, jota käytetään [!INCLUDE[crm_md](includes/crm_md.md)]in uusissa tietueissa.

## <a name="see-also"></a>Katso myös  
[Tietoja Dynamics 365 Business Centralin ja Dynamics 365 Salesin integroinnista](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Business Centralin ja Dynamics 365 Salesin synkronointi](admin-synchronizing-business-central-and-sales.md)   
[Ajoitettu synkronointi](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
