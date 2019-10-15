---
title: Business Centralin ja Dynamics 365 Salesin synkronointi | Microsoft Docs
description: Lisätietoja tietojen synkronoinnissa Business Centralin ja Dynamics 365 Salesin välillä.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 8b1fd4a676d1efe508e6fd2dcb37a67b3c24cdb1
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304346"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-sales"></a>Business Centralin ja Dynamics 365 Salesin synkronoinnin ajoittaminen
Voit synkronoida [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in tietyin väliajoin määrittämällä työt työjonoon. Synkronointityöt synkronoivat [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueiden tiedot ja [!INCLUDE[crm_md](includes/crm_md.md)]in tietueet, jotka on aiemmin yhdistetty. Jos kyse on vielä yhdistämättömistä tietueista synkronointityöt voivat luoda ja yhdistää uusia tietueita kohdejärjestelmässä synkronointisuunnan ja -sääntöjen mukaisesti. Käytettävissä on heti useita synkronointitöitä. Voit tarkastella niitä **Työjonon tapahtumat** -sivulla. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.--> 

## <a name="synchronization-process"></a>Synkronointiprosessi  
Kunkin synkronoinnin työjonotapahtuma käyttää tiettyä integrointitaulukon yhdistämismääritystä, joka määrittää, mikä [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukko ja mikä [!INCLUDE[crm_md](includes/crm_md.md)]in objekti synkronoidaan. Taulukon yhdistämismääritykset sisältävät myös joitakin asetuksia, jotka määrittävät, mitkä [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukon ja [!INCLUDE[crm_md](includes/crm_md.md)]in objektin tietueet synkronoidaan.  

Tietojen synkronointi edellyttää, että [!INCLUDE[crm_md](includes/crm_md.md)] -objektin tietueet on yhdistettävä [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueisiin. Esimerkiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakas on yhdistettävä [!INCLUDE[crm_md](includes/crm_md.md)]in tiliin. Yhdistämiset voidaan määrittää manuaalisesti, ennen kuin suoritat synkronointitöitä tai voit antaa synkronointitöiden määrittää yhdistämiset automaattisesti. Seuraavassa luettelossa käsitellään tietojen synkronointia [!INCLUDE[crm_md](includes/crm_md.md)]in ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in välillä, kun käytät synkronoinnin työjonon tapahtumia. Lisätietoja on kohdassa [Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md). 

-   Oletusarvoisesti vain ne [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueet, jotka on yhdistetty [!INCLUDE[crm_md](includes/crm_md.md)]in tietueisiin, synkronoidaan. Voit muuttaa taulukon yhdistämismäärityksiä [!INCLUDE[crm_md](includes/crm_md.md)]in objektin ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukon välillä siten, että integroinnin synkronointityöt luovat uudet tietueet kohdetietokantaan kullekin lähdetietokannan tietueelle, jota ei ole yhdistetty. Myös uudet tietueet yhdistetään lähteen vastaaviin tietueisiin. Kun esimerkiksi synkronoit asiakkaita [!INCLUDE[crm_md](includes/crm_md.md)]in tilien kanssa, kullekin [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakkaalle luodaan uusi tilitietue. Uudet tilit yhdistetään automaattisesti [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakkaisiin. Koska tässä tapauksessa synkronointi on kaksisuuntainen, uusi asiakas luodaan ja yhdistetään kuhunkin vielä yhdistämättömään [!INCLUDE[crm_md](includes/crm_md.md)]in tiliin.  

    > [!NOTE]  
    > Synkronoitavat tiedot määrittyvät sääntöjen ja suodattimien perusteella. Lisätietoja on kohdassa [Synkronointisäännöt](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   Kun [!INCLUDE[d365fin](includes/d365fin_md.md)]issa luodaan uusia tietueita, tietueet käyttävät joko integrointitaulukon yhdistämismääritykselle määritettyä mallia tai oletusmallia, jollainen on jokaisella tietuetyypillä. Kentät täytetään [!INCLUDE[d365fin](includes/d365fin_md.md)]in tai [!INCLUDE[crm_md](includes/crm_md.md)]in tiedoilla synkronoinnin suunnan perusteella. Lisätietoja on kohdassa [Toimintaohje: Taulukon yhdistämismääritysten muokkaaminen synkronointia varten](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Seuraavissa synkronoinneissa päivitetään vain tietueet, joita on muokattu tai lisätty edellisen onnistuneen synkronointityön jälkeen.  

     [!INCLUDE[crm_md](includes/crm_md.md)]in uudet tietueet lisätään [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Jos [!INCLUDE[crm_md](includes/crm_md.md)]in tietueiden kenttien tiedot ovat muuttuneet, tiedot kopioidaan vastaavan kenttään [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.  

-   Kaksisuuntaisessa synkronoinnissa työ synkronoituu [!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin ja sitten [!INCLUDE[crm_md](includes/crm_md.md)]sta [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.

## <a name="default-synchronization-job-queue-entries"></a>Oletusarvoiset synkronoinnin työjonotapahtumat  
Seuraavassa taulukossa kuvaillaan synkronoinnin oletustyöt.  

|Työjonotapahtuma|Kuvaus|Suunta|Integrointitaulukon yhdistämismääritys|  
|---------------------|---------------------------------------|---------------|-------------------------------|  
|KONTAKTI – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in kontaktit [!INCLUDE[d365fin](includes/d365fin_md.md)]in kontakteilla.|Kaksisuuntainen|KONTAKTI|  
|VALUUTTA – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in tapahtumien valuutat [!INCLUDE[d365fin](includes/d365fin_md.md)]in valuuttojen kanssa.|[!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|VALUUTTA|  
|ASIAKAS – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in tilit ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakkaat.|Kaksisuuntainen|ASIAKAS|  
|ASIAKHNTRHM-HINTA – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in myyntihinnaston ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakashintaryhmät.| |ASIAKASHINTARYHMÄT-MYYNTIHINNASTOT|
|NIMIKE-TUOTE – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in tuotteet ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in nimikkeet.|[!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|NIMIKE-TUOTE|
|KIRJMNTILASKU-LASK – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in laskut ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in kirjatut myyntilaskut.|[!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|LASKUT-KIRJATUT MYYNTILASKUT|
|RESURSSI-TUOTE – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in tuotteet ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in resurssit.|[!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|RESURSSI-TUOTE|  
|MYYJÄT – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[d365fin](includes/d365fin_md.md)]in myyjät ja [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjät.|[!INCLUDE[crm_md](includes/crm_md.md)]ista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin|MYYJÄT|
|MYYNTIHNT-TUOTEHINTA – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in tuotehinnat ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in myyntihinnat.||TUOTEHINTA-MYYNTIHINTA|
|MITTAYKSIKKÖ – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in yksikköryhmät ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in mittayksiköt.|[!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|MITTAYKSIKKÖ|  
|Asiakastilastot – Dynamics 365 Salesin synkronointityö|Päivittää [!INCLUDE[crm_md](includes/crm_md.md)]in tilit uusilla [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakastiedoilla. Nämä tiedot näkyvät [!INCLUDE[crm_md](includes/crm_md.md)]issa niiden tilien **Business Central -tilin tilastot** -pikanäkymälomakkeessa, jotka on yhdistetty [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakkaisiin.<br /><br /> Nämä tiedot voidaan päivittää myös manuaalisesti kustakin asiakastietueesta. Lisätietoja on kohdassa [Toimintaohje: Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Huomautus:** Tällä työjonotapahtumalla on merkitystä vain, jos [!INCLUDE[d365fin](includes/d365fin_md.md)] -integrointiratkaisu on asennettu [!INCLUDE[crm_md](includes/crm_md.md)]iin. Lisätietoja on kohdassa [Tietoja Business Central -integraatioratkaisusta](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Ei sovellu.|Ei sovellu.|   

## <a name="to-view-the-synchronization-job-log"></a>Synkronointityön lokin tarkasteleminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Integroinnin synkronointiloki** ja valitse sitten liittyvä linkki.
2.  Jos synkronointityössä tapahtui ainakin yksi virhe, virheiden määrä näkyy **Epäonnistui**-sarakkeessa. Näytä työn virheet valitsemalla numero.  

    > [!TIP]  
    > Voit tarkastella kaikkia synkronointitöiden virheitä avaamalla synkronointityölokin suoraan.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Synkronointityölokin tarkasteleminen taulukon yhdistämismäärityksistä  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Integrointitaulukon yhdistämismääritykset** ja valitse sitten liittyvä linkki.
2.  Valitse **Integrointitaulukon yhdistämismääritykset** -sivulla tapahtuma ja valitse sitten **Integroinnin synkronointityöloki**.  

## <a name="to-view-the-synchronization-error-log"></a>Synkronoinnin virhelokin tarkasteleminen  
* Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Integroinnin synkronointivirheet** ja valitse sitten liittyvä linkki.

## <a name="see-also"></a>Katso myös  
[Business Centralin ja Dynamics 365 Salesin tietojen synkronointi](admin-synchronizing-business-central-and-sales.md)  
[Taulukon yhdistämismääritysten manuaalinen synkronointi](admin-manual-synchronization-of-table-mappings.md)  
[Business Centralin ja Dynamics 365 Salesin synkronoinnin ajoittaminen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Tietoja Dynamics 365 Business Centralin ja Dynamics 365 Salesin integroinnista](admin-prepare-dynamics-365-for-sales-for-integration.md)  



