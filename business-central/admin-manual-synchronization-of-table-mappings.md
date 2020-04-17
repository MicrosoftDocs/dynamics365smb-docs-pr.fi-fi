---
title: Taulukon yhdistämismääritysten manuaalinen synkronointi | Microsoft Docs
description: Synkronointi kopioi tiedot Common Data Service -entiteettien tapahtumien ja Business Centralin välillä, jotta kumpikin järjestelmä pysyy ajan tasalla.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 015084b999f7488339c98605018bff2bc9a4ded2
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196709"
---
# <a name="manually-synchronize-table-mappings"></a>Taulukon yhdistämismääritysten manuaalinen synkronointi
Integrointitaulukon yhdistämismääritys liittää [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukon (tietuetyypin), kuten asiakkaan, [!INCLUDE[d365fin](includes/cds_long_md.md)] -objektiin, kuten tiliin. Integrointitaulukon yhdistämismäärityksen synkronoinnin ansiosta voit synkronoida yhdistetyn [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukon ja [!INCLUDE[d365fin](includes/cds_long_md.md)] -objektin kaikkien tietueiden tiedot. Lisäksi taulukon yhdistämismäärityksen mukaan synkronointi voi luoda ja yhdistää uusia tietueita lähteen yhdistämättömien tietueiden kohderatkaisussa.  

Integrointitaulukon yhdistämismääritysten manuaalisesta synkronoinnista voi olla hyötyä, kun integraatio määritetään ensimmäisen ja kun synkronointivirheitä diagnosoidaan.  

Tässä artikkelissa käsitellään kolme tapaa, jolla integrointitaulukon yhdistämismääritykset voidaan synkronoida manuaalisesti. Kunkin tavan synkronointitaso on erilainen.

## <a name="run-a-full-synchronization"></a>Täyden synkronoinnin suorittaminen
Täysi synkronointi suorittaa kaikki [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietueiden ja [!INCLUDE[d365fin](includes/cds_long_md.md)] -objektien synkronoinnin oletusintegroinnin synkronointityöt **Integrointitaulukon yhdistämismääritykset** -sivun määritysten mukaisesti. 

Täysi synkronointi suorittaa seuraavat [!INCLUDE[d365fin](includes/d365fin_md.md)]- tai [!INCLUDE[d365fin](includes/cds_long_md.md)] -tietueiden toiminnot:

* Luodaan uusi, yhdistämätön tietue, joka yhdistetään vastakkaiseen ratkaisuun.
Tietueen luonti ja luontiajankohta määräytyy synkronointisuunnan mukaan. Esimerkiksi silloin, kun tietoja synkronoidaan [!INCLUDE[d365fin](includes/d365fin_md.md)] -asiakkaista [!INCLUDE[d365fin](includes/cds_long_md.md)] -tileille mutta asiakasta ei ole yhdistetty tiliin, uusi tili lisätään automaattisesti [!INCLUDE[d365fin](includes/cds_long_md.md)]iin ja yhdistetään [!INCLUDE[d365fin](includes/d365fin_md.md)] -asiakkaaseen. Tilanne on päinvastainen, kun synkronointisuunta on [!INCLUDE[d365fin](includes/cds_long_md.md)] > [!INCLUDE[d365fin](includes/d365fin_md.md)]. Jokaiselle tilille, jota ei ole vielä yhdistetty asiakkaaseen, luodaan vastaava asiakas [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa, joka sitten yhdistetään [!INCLUDE[d365fin](includes/cds_long_md.md)]in tiliin.  

     > [!NOTE]  
     >  Tätä varten täysi synkronointi poistaa tilapäisesti **Synkronoi vain yhdistetyt tietueet** -asetuksen valinnan siinä integrointitaulukon yhdistämismäärityksessä, jota synkronointityö käyttää. Kun täysi synkronointi päättyy, sinulta kysytään, haluatko, että tämä asetus on valitsematta kaikissa töissä.  

* Yhdistettynä integrointitaulukon yhdistämismääritykset ovat määrittäneet synkronointisuunnan (kuten [!INCLUDE[d365fin](includes/d365fin_md.md)] > [!INCLUDE[d365fin](includes/cds_long_md.md)] tai [!INCLUDE[d365fin](includes/cds_long_md.md)] > [!INCLUDE[d365fin](includes/d365fin_md.md)]) ennalta. Lisätietoja on kohdassa [Synkronoinnin vakioentiteettien yhdistämismääritys](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).  

> [!IMPORTANT]  
>  Yleensä täyttä synkronointia käytetään, kun [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja [!INCLUDE[d365fin](includes/cds_long_md.md)] -integrointi määritetään ja vain toisessa ratkaisussa on tietoja, jotka halutaan kopioida toiseen ratkaisuun. Täysi synkronointi voi olla kätevä esittely-ympäristössä. Koska täysi synkronointi luo ja yhdistää tietueita ratkaisujen välillä, se nopeuttaa tietueiden välillä synkronoitavien tietojen käytön aloittamista. Täysi synkronointi pitäisi toisaalta suorittaa vain, jos haluat lisätä tietyn taulukon yhdistämismääritysten [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietueen jokaiseen [!INCLUDE[d365fin](includes/cds_long_md.md)] -tietueeseen. Muussa tapauksessa syntyy ei-toivottuja tietueita tai tietueiden kaksoiskappaleita joko [!INCLUDE[d365fin](includes/d365fin_md.md)]- tai [!INCLUDE[d365fin](includes/cds_long_md.md)] -ratkaisuun.  

### <a name="to-run-a-full-synchronization"></a>Täyden synkronoinnin suorittaminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Common Data Service -yhteyden määritys** ja valitse sitten liittyvä linkki.

    > [!NOTE]
    > Jos haluat suorittaa täydellisen synkronoinnin entiteeteille Dynamics 365 Salesin avulla, käytä sen sijaan **Microsoft Dynamics 365 Sales -yhteyden määritys** -sivua.

2.  Valitse ensin **Suorita täysi synkronointi**-toiminto ja sitten **Kyllä**-painike.  
3.  Kun täysi synkronointi on valmis, voit määrittää, saavatko ajoitetut synkronointityöt luoda uusia tietueita.  

    Jos haluat, että kaikki synkronointityöt luovat uusia tietueita lähteen yhdistämättömien tietueiden kohteessa, valitse **Kyllä**. Näin määritetään synkronointitöiden käyttämien taulukon yhdistämismääritysten **Synkronoi vain yhdistetyt tietueet** -kenttä.  

    Jos haluat, että synkronointityöt suoritetaan uusien tietueiden luonnin osalta samalla tavoin kuin ennen täyttä synkronointia, valitse **Ei**. **Synkronoi vain yhdistetyt tietueen** -kentän asetukseksi määritetään nyt asetus, joka siinä oli ennen täyttä synkronointia.  

Voit tarkastella täyden synkronoinnin tuloksia **Integroinnin synkronointityöt** -sivulla. Lisätietoja on kohdassa [Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records"></a>Kaikkien muokattujen tietueiden synkronointi
Voit synkronoida kaikkien integrointitaulukon yhdistämismääritysten tietojen muutokset **CDS-yhteyden määritys** -sivulla. Tämä muistuttaa täyttä synkronointia. Kaikki taulukon yhdistämismäärityksissä määritetyt [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukoiden ja [!INCLUDE[d365fin](includes/cds_long_md.md)] -objektien yhdistettyjen tietueiden tiedot synkronoidaan. Oletusarvoisesti vain tietueet, joita on muokattu edellisen synkronointikerran jälkeen, synkronoidaan. Synkronointityöt synkronoivat taulukon yhdistämismääritykset seuraavassa järjestyksessä, jotta objektien välille ei muodostu yhdistämisen riippuvuussuhteita:  

1.  VALUUTTA  
2.  MYYJÄT  
3.  TOIMITTAJA  
4.  ASIAKAS  
5.  YHTEYSHENKILÖT  

Voit tarkastella synkronoinnin tuloksia **Integroinnin synkronointityöt** -sivulla. Lisätietoja on kohdassa [Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Jos muokkaat integrointitaulukon yhdistämismääritystä etukäteen, voit määrittää synkronointiin suodattimet valitsemaan synkronoitavat tietueet. Vaihtoehtoisesti voit määrittää sen luomaan uudet tietueet kohderatkaisussa lähteen yhdistämättömille tietueille. Lisätietoja on kohdassa [Taulukon yhdistämismääritysten muokkaaminen synkronointia varten](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-records-for-all-tables"></a>Kaikki taulukoiden tietueiden synkronointi  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Microsoft Dynamics 365 Sales -yhteyden määritys** ja valitse sitten liittyvä linkki.
2.  Valitse ensin **Synkronoi muokatut tietueet** -toiminto ja sitten **Kyllä**.  

## <a name="synchronize-individual-table-mappings"></a>Yksittäisen taulukon yhdistämismääritysten synkronointi
Voit suorittaa tietyn taulukon yhdistämismääritysten synkronointityön **Integrointitaulukon yhdistämismääritykset** -sivulla. Kaikki taulukon yhdistämismäärityksessä määritetyt [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukon ja [!INCLUDE[d365fin](includes/cds_long_md.md)] -objektin yhdistettyjen tietueiden tiedot synkronoidaan. Oletusarvoisesti vain tietueet, joita on muokattu edellisen synkronointikerran jälkeen, synkronoidaan.  

Muokkaamalla integrointitaulukon yhdistämismääritystä etukäteen voit määrittää synkronointityön luomaan uusia tietueita kohderatkaisussa lähteen yhdistämättömille tietueille.

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>Integrointitaulukon yhdistämismäärityksen tietueiden synkronointi  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Integrointitaulukon yhdistämismääritykset** ja valitse sitten liittyvä linkki.
2.  Valitse ensin **Synkronoi muokatut tietueet** -toiminto ja sitten **Kyllä**.  

## <a name="see-also"></a>Katso myös  
[Business Centralin ja Dynamics 365 Salesin synkronointi](admin-synchronizing-business-central-and-sales.md)   
[Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)   
