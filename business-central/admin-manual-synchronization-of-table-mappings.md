---
title: Taulukon yhdistämismääritysten manuaalinen synkronointi | Microsoft Docs
description: 'Synkronointi kopioi tiedot Microsoft Dataversein taulukoiden ja Business Centralin välillä, jotta kumpikin järjestelmä pysyy ajan tasalla.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="manually-synchronize-table-mappings"></a>Taulukon yhdistämismääritysten manuaalinen synkronointi


Integrointitaulukon yhdistämismääritys liittää [!INCLUDE[prod_short](includes/prod_short.md)] -taulukon (tietuetyypin), kuten asiakkaan, [!INCLUDE[prod_short](includes/cds_long_md.md)] -taulukkoon, kuten tiliin. Integrointitaulukon yhdistämismäärityksen synkronoinnin ansiosta voit synkronoida yhdistetyn [!INCLUDE[prod_short](includes/prod_short.md)] -taulukon ja [!INCLUDE[prod_short](includes/cds_long_md.md)] -taulukon kaikkien tietueiden tiedot. Lisäksi taulukon yhdistämismäärityksen mukaan synkronointi voi luoda ja yhdistää uusia tietueita lähteen yhdistämättömien tietueiden kohderatkaisussa.  

Integrointitaulukon yhdistämismääritysten manuaalisesta synkronoinnista voi olla hyötyä, kun integraatio määritetään ensimmäisen ja kun synkronointivirheitä diagnosoidaan.  

Tässä artikkelissa käsitellään kolme tapaa, jolla integrointitaulukon yhdistämismääritykset voidaan synkronoida manuaalisesti. Kunkin tavan synkronointitaso on erilainen.

## <a name="run-a-full-synchronization"></a>Täyden synkronoinnin suorittaminen
Täysi synkronointi suorittaa kaikki [!INCLUDE[prod_short](includes/prod_short.md)] -tietueiden ja [!INCLUDE[prod_short](includes/cds_long_md.md)] -taulukoiden synkronoinnin oletusintegroinnin synkronointityöt **Integrointitaulukon yhdistämismääritykset** -sivun määritysten mukaisesti. 

Täysi synkronointi suorittaa seuraavat [!INCLUDE[prod_short](includes/prod_short.md)]- tai [!INCLUDE[prod_short](includes/cds_long_md.md)] -tietueiden toiminnot:

* Luodaan uusi, yhdistämätön vastaava rivi, joka yhdistetään vastakkaiseen ratkaisuun.
Rivin luonti ja luontiajankohta määräytyy synkronointisuunnan mukaan. Esimerkiksi silloin, kun tietoja synkronoidaan [!INCLUDE[prod_short](includes/prod_short.md)] -asiakkaista [!INCLUDE[prod_short](includes/cds_long_md.md)] -tileille mutta asiakasta ei ole yhdistetty tiliin, uusi tili lisätään automaattisesti [!INCLUDE[prod_short](includes/cds_long_md.md)]iin ja yhdistetään [!INCLUDE[prod_short](includes/prod_short.md)] -asiakkaaseen. Tilanne on päinvastainen, kun synkronointisuunta on [!INCLUDE[prod_short](includes/cds_long_md.md)] &gt; [!INCLUDE[prod_short](includes/prod_short.md)]. Jokaiselle tilille, jota ei ole vielä yhdistetty asiakkaaseen, luodaan vastaava asiakas [!INCLUDE[prod_short](includes/prod_short.md)]:ssa, joka sitten yhdistetään [!INCLUDE[prod_short](includes/cds_long_md.md)]in tiliin.  

     > [!NOTE]  
     >  Tätä varten täysi synkronointi poistaa tilapäisesti **Synkronoi vain yhdistetyt tietueet** -asetuksen valinnan siinä integrointitaulukon yhdistämismäärityksessä, jota synkronointityö käyttää. Kun täysi synkronointi päättyy, sinulta kysytään, haluatko, että tämä asetus on valitsematta kaikissa töissä.  

* Yhdistettynä integrointitaulukon yhdistämismääritykset ovat määrittäneet synkronointisuunnan (kuten [!INCLUDE[prod_short](includes/prod_short.md)] &gt; [!INCLUDE[prod_short](includes/cds_long_md.md)] tai [!INCLUDE[prod_short](includes/cds_long_md.md)] &gt; [!INCLUDE[prod_short](includes/prod_short.md)]) ennalta. Lisätietoja on kohdassa [Synkronoinnin vakiotaulukoiden yhdistämismääritys](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).  

> [!IMPORTANT]  
>  Yleensä täyttä synkronointia käytetään, kun [!INCLUDE[prod_short](includes/prod_short.md)]- ja [!INCLUDE[prod_short](includes/cds_long_md.md)] -integrointi määritetään ja vain toisessa ratkaisussa on tietoja, jotka halutaan kopioida toiseen ratkaisuun. Täysi synkronointi voi olla kätevä esittely-ympäristössä. Koska täysi synkronointi luo ja yhdistää tietueita ratkaisujen välillä, se nopeuttaa tietueiden välillä synkronoitavien tietojen käytön aloittamista. Täysi synkronointi pitäisi toisaalta suorittaa vain, jos haluat lisätä tietyn taulukon yhdistämismääritysten [!INCLUDE[prod_short](includes/prod_short.md)] -rivin jokaiseen [!INCLUDE[prod_short](includes/cds_long_md.md)] -riviin. Muussa tapauksessa syntyy ei-toivottuja tietueita tai tietueiden kaksoiskappaleita joko [!INCLUDE[prod_short](includes/prod_short.md)]- tai [!INCLUDE[prod_short](includes/cds_long_md.md)] -ratkaisuun.  

### <a name="to-run-a-full-synchronization"></a>Täyden synkronoinnin suorittaminen
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Dataverse-yhteyden määritys** ja valitse sitten vastaava linkki.

    > [!NOTE]
    > Jos haluat suorittaa täydellisen synkronoinnin taulukoille Dynamics 365 Salesin avulla, käytä sen sijaan **Microsoft Dynamics 365 Sales -yhteyden määritys** -sivua.

2.  Valitse ensin **Suorita täysi synkronointi**-toiminto ja sitten **Kyllä**-painike.  
3.  Kun täysi synkronointi on valmis, voit määrittää, saavatko ajoitetut synkronointityöt luoda uusia tietueita.  

    Jos haluat, että kaikki synkronointityöt luovat uusia tietueita lähteen yhdistämättömien tietueiden kohteessa, valitse **Kyllä**. Näin määritetään synkronointitöiden käyttämien taulukon yhdistämismääritysten **Synkronoi vain yhdistetyt tietueet** -kenttä.  

    Jos haluat, että synkronointityöt suoritetaan uusien tietueiden luonnin osalta samalla tavoin kuin ennen täyttä synkronointia, valitse **Ei**. **Synkronoi vain yhdistetyt tietueen** -kentän asetukseksi määritetään nyt asetus, joka siinä oli ennen täyttä synkronointia.  

Voit tarkastella täyden synkronoinnin tuloksia **Integroinnin synkronointityöt** -sivulla. Lisätietoja on kohdassa [Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records"></a>Kaikkien muokattujen tietueiden synkronointi
Voit synkronoida kaikkien integrointitaulukon yhdistämismääritysten tietojen muutokset **Common Data Service -yhteyden määritys** -sivulla. Tämä muistuttaa täyttä synkronointia. Kaikki taulukon yhdistämismäärityksissä määritetyt [!INCLUDE[prod_short](includes/prod_short.md)] -taulukoiden ja [!INCLUDE[prod_short](includes/cds_long_md.md)] -taulukoiden yhdistettyjen tietueiden tiedot synkronoidaan. Oletusarvoisesti vain tiedot, joita on muokattu edellisen synkronointikerran jälkeen, synkronoidaan. Synkronointityöt synkronoivat taulukon yhdistämismääritykset seuraavassa järjestyksessä, jotta taulukoiden välille ei muodostu yhdistämisen riippuvuussuhteita:  

1.  VALUUTTA  
2.  MYYJÄT  
3.  TOIMITTAJA  
4.  ASIAKAS  
5.  YHTEYSHENKILÖT  

Voit tarkastella synkronoinnin tuloksia **Integroinnin synkronointityöt** -sivulla. Lisätietoja on kohdassa [Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Jos muokkaat integrointitaulukon yhdistämismääritystä etukäteen, voit luoda suodattimet valitsemaan synkronoitavat tiedot. Vaihtoehtoisesti voit määrittää yhdistämismääritykset luomaan uudet tiedot kohderatkaisussa lähteen yhdistämättömille tietueille tai riveille. Lisätietoja on kohdassa [Taulukon yhdistämismääritysten muokkaaminen synkronointia varten](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-data-for-all-tables"></a>Kaikki taulukoiden tietojen synkronointi
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Microsoft Dynamics 365 Sales -yhteyden määritys** ja valitse sitten vastaava linkki.
2.  Valitse ensin **Synkronoi muokatut tietueet** -toiminto ja sitten **Kyllä**.  

## <a name="synchronize-individual-table-mappings"></a>Yksittäisen taulukon yhdistämismääritysten synkronointi
Voit suorittaa taulukon yhdistämismääritysten synkronointityön **Integrointitaulukon yhdistämismääritykset** -sivulla. Kaikki taulukon yhdistämismäärityksessä määritetyt [!INCLUDE[prod_short](includes/prod_short.md)] -taulukon ja [!INCLUDE[prod_short](includes/cds_long_md.md)] -taulukon yhdistettyjen tietueiden ja rivien tiedot synkronoidaan. Oletusarvoisesti vain tiedot, joita on muokattu edellisen synkronointikerran jälkeen, synkronoidaan.  

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>Integrointitaulukon yhdistämismäärityksen tietueiden synkronointi
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Integroinnin yhdistämistaulukot** ja valitse sitten liittyvä linkki.
2.  Valitse ensin **Synkronoi muokatut tietueet** -toiminto ja sitten **Kyllä**.  

## <a name="see-also"></a>Katso myös
[Business Centralin ja Dynamics 365 Salesin synkronointi](admin-synchronizing-business-central-and-sales.md)   
[Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
