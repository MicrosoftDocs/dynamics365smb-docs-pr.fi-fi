---
title: Business Centralin ja Common Data Servicein synkronointi | Microsoft Docs
description: Lisätietoja tietojen synkronoinnissa Business Centralin ja Common Data Servicein välillä.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: cce95930cde316c5e233382effb0bb241b3b79fd
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196589"
---
# <a name="scheduling-a-synchronization-between-business-central-and-common-data-service"></a>Business Centralin ja Common Data Servicein synkronoinnin ajoittaminen
Voit synkronoida [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[d365fin](includes/cds_long_md.md)]in tietyin väliajoin määrittämällä työt työjonoon. Synkronointityöt synkronoivat [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueiden tiedot ja [!INCLUDE[d365fin](includes/cds_long_md.md)]in tietueet, jotka on aiemmin yhdistetty. Jos kyse on vielä yhdistämättömistä tietueista synkronointityöt voivat luoda ja yhdistää uusia tietueita kohdejärjestelmässä synkronointisuunnan ja -sääntöjen mukaisesti. 

Käytettävissä on heti useita synkronointitöitä. Työt suoritetaan seuraavassa järjestyksessä, jotta objektien välille ei muodostu yhdistämisen riippuvuussuhteita. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](/dynamics365/business-central/admin-job-queues-schedule-tasks.md).

1. VALUUTTA - [!INCLUDE[d365fin](includes/cds_long_md.md)] -synkronointityö.
2. TOIMITTAJA - [!INCLUDE[d365fin](includes/cds_long_md.md)] -synkronointityö. 
3. YHTEYSHENKILÖ - [!INCLUDE[d365fin](includes/cds_long_md.md)] -synkronointityö.
4. ASIAKAS - [!INCLUDE[d365fin](includes/cds_long_md.md)] -synkronointityö.
5. MYYJÄT - [!INCLUDE[d365fin](includes/cds_long_md.md)] -synkronointityö.

Voit tarkastella töitä **Työjonon tapahtumat** -sivulla. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).

### <a name="default-synchronization-job-queue-entries"></a>Oletusarvoiset synkronoinnin työjonotapahtumat  
Seuraavassa taulukossa kuvaillaan [!INCLUDE[d365fin](includes/cds_long_md.md)]:n synkronoinnin oletustyöt.  

|Työjonotapahtuma|Kuvaus|Suunta|Integrointitaulukon yhdistämismääritys|Synkronoinnin oletustiheys (min)|Passivisuuden oletusaika (min)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|KONTAKTI - [!INCLUDE[d365fin](includes/cds_long_md.md)] -synkronointityö|Synkronoi [!INCLUDE[d365fin](includes/cds_long_md.md)]in kontaktit [!INCLUDE[d365fin](includes/d365fin_md.md)]in kontakteilla.|Kaksisuuntainen|KONTAKTI|30|720 <br>(12 tuntia)| 
|VALUUTTA - [!INCLUDE[d365fin](includes/cds_long_md.md)] -synkronointityö|Synkronoi [!INCLUDE[d365fin](includes/cds_long_md.md)]in tapahtumien valuutat [!INCLUDE[d365fin](includes/d365fin_md.md)]in valuuttojen kanssa.|[!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[d365fin](includes/cds_long_md.md)]iin|VALUUTTA|30|720 <br> (12 tuntia)| 
|ASIAKAS - [!INCLUDE[d365fin](includes/cds_long_md.md)] -synkronointityö|Synkronoi [!INCLUDE[d365fin](includes/cds_long_md.md)]in tilit ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakkaat.|Kaksisuuntainen|ASIAKAS|30|720<br> (12 tuntia)|
|TOIMITTAJA - [!INCLUDE[d365fin](includes/cds_long_md.md)] -synkronointityö|Synkronoi [!INCLUDE[d365fin](includes/cds_long_md.md)]in tilit ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakkaat.|Kaksisuuntainen|TOIMITTAJA|30|720<br> (12 tuntia)|
|MYYJÄT - [!INCLUDE[d365fin](includes/cds_long_md.md)] -synkronointityö|Synkronoi [!INCLUDE[d365fin](includes/d365fin_md.md)]in myyjät ja [!INCLUDE[d365fin](includes/cds_long_md.md)]in käyttäjät.|[!INCLUDE[d365fin](includes/cds_long_md.md)]ista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin|MYYJÄT|30|1440<br> (24 tuntia)|

## <a name="synchronization-process"></a>Synkronointiprosessi  
Kunkin synkronoinnin työjonotapahtuma käyttää tiettyä integrointitaulukon yhdistämismääritystä, joka määrittää, mikä [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukko ja mikä [!INCLUDE[d365fin](includes/cds_long_md.md)]in objekti synkronoidaan. Taulukon yhdistämismääritykset sisältävät myös joitakin asetuksia, jotka määrittävät, mitkä [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukon ja [!INCLUDE[d365fin](includes/cds_long_md.md)]in objektin tietueet synkronoidaan.  

Tietojen synkronointi edellyttää, että [!INCLUDE[d365fin](includes/cds_long_md.md)] -objektin tietueet on yhdistettävä [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueisiin. Esimerkiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakas on yhdistettävä [!INCLUDE[d365fin](includes/cds_long_md.md)]in tiliin. Yhdistämiset voidaan määrittää manuaalisesti, ennen kuin suoritat synkronointitöitä tai voit antaa synkronointitöiden määrittää yhdistämiset automaattisesti. Seuraavassa luettelossa käsitellään tietojen synkronointia Common Data Servicein ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in välillä, kun käytät synkronoinnin työjonon tapahtumia. Lisätietoja on kohdassa [Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md).

-   **Synkronoi vain yhdistetyt tietueet** -valintaruutu määrittää, luodaanko uusia tietueita synkronoinnin yhteydessä. Oletusarvon mukaan valintaruutu on valittuna, joten vain kytkettyjä tietueita synkronoidaan. Integraatiotaulukon yhdistämismäärityksissä voit muuttaa taulukon yhdistämismäärityksiä [!INCLUDE[d365fin](includes/cds_long_md.md)]in objektin ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in taulukon välillä siten, että integroinnin synkronointityöt luovat uudet tietueet kohdetietokantaan kullekin lähdetietokannan tietueelle, jota ei ole yhdistetty. Lisätietoja on kohdassa [Uusien tietueiden luominen](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records). 
    
    **Esimerkki**: Jos tyhjennät **Synkronoi vain yhdistetyt tietueet** -valintaruudun, kun synkronoit [!INCLUDE[d365fin](includes/d365fin_md.md)] -asiakkaat [!INCLUDE[d365fin](includes/cds_long_md.md)] -tilien kanssa, ohjelma luo uuden tilin kullekin asiakkaalle [!INCLUDE[d365fin](includes/d365fin_md.md)]ssa ja yhdistää sen automaattisesti. Lisäksi koska tässä tapauksessa synkronointi on kaksisuuntainen, uusi asiakas luodaan ja yhdistetään kuhunkin vielä yhdistämättömään [!INCLUDE[d365fin](includes/cds_long_md.md)]in tiliin.  

    > [!NOTE]  
    > Synkronoitavat tiedot määrittyvät sääntöjen ja suodattimien perusteella. Lisätietoja on kohdassa [Synkronointisäännöt](admin-synchronizing-business-central-and-sales.md).

-   Kun [!INCLUDE[d365fin](includes/d365fin_md.md)]issa luodaan uusia tietueita, tietueet käyttävät joko integrointitaulukon yhdistämismääritykselle määritettyä mallia tai oletusmallia, jollainen on jokaisella tietuetyypillä. Kentät täytetään [!INCLUDE[d365fin](includes/d365fin_md.md)]in tai [!INCLUDE[d365fin](includes/cds_long_md.md)]in tiedoilla synkronoinnin suunnan perusteella. Lisätietoja on kohdassa [Taulukon yhdistämismääritysten muokkaaminen synkronointia varten](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Seuraavissa synkronoinneissa päivitetään vain tietueet, joita on muokattu tai lisätty edellisen onnistuneen synkronointityön jälkeen.  

     [!INCLUDE[d365fin](includes/cds_long_md.md)]in uudet tietueet lisätään [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Jos [!INCLUDE[d365fin](includes/cds_long_md.md)]in tietueiden kenttien tiedot ovat muuttuneet, tiedot kopioidaan vastaavan kenttään [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.  

-   Kaksisuuntaisessa synkronoinnissa työ synkronoituu [!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[d365fin](includes/cds_long_md.md)]iin ja sitten [!INCLUDE[d365fin](includes/cds_long_md.md)]sta [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.

## <a name="about-inactivity-timeouts"></a>Tietoja käyttämättömyyden aikakatkaisusta
Jotkin työjonotapahtumat, esimerkiksi ne, jotka ajoittavat [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman ja [!INCLUDE[d365fin](includes/cds_long_md.md)]:n välisen synkronoinnin, käyttävät Työjonotapahtuma-kortissa **Käyttämättömyyden aikakatkaisu** -kenttää estämään työjonotapahtuman tarpeettoman suorittamisen.  
<br><br>

> ![Vuokaavio siitä, kun työjonon tapahtumat ovat pidossa käyttämättömyyden vuoksi.](media/on-hold-with-inactivity-timeout.png)

Jos tämän kentän arvo ei ole nolla eikä työjono löytänyt muutoksia viimeisen suorituksen aikana, [!INCLUDE[d365fin](includes/d365fin_md.md)] siirtää työjonotapahtuman pitoon. Kun näin tapahtuu, **Työjonon tila** -kentässä näkyy **Estossa toimettomuuden vuoksi**, ja [!INCLUDE[d365fin](includes/d365fin_md.md)] odottaa **Käyttämättömyyden aikakatkaisu** -kentässä määritetyn ajan, ennen kuin se suorittaa työjonotapahtuman uudelleen. 

Oletusarvon mukaan esimerkiksi CURRENCY-työjonotapahtuma, joka synkronoi valuutat [!INCLUDE[d365fin](includes/cds_long_md.md)] -ohjelmassa [!INCLUDE[d365fin](includes/d365fin_md.md)]n valuuttakurssien mukaan, etsii vaihtokurssien muutoksia 30 minuutin välein. Jos muutoksia ei löydy, [!INCLUDE[d365fin](includes/d365fin_md.md)] asettaa CURRENCY-työjonotapahtuman Estossa olevaksi 720 minuutin (kuuden tunnin) ajaksi. Jos vaihtokurssia muutetaan, [!INCLUDE[d365fin](includes/d365fin_md.md)]ssa, kun työjonotapahtuma on Estossa, [!INCLUDE[d365fin](includes/d365fin_md.md)] aktivoi automaattisesti uudelleen työjonontapahtuman ja työjono käynnistetään uudelleen. 

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] aktivoi pidossa olevat työjonotapahtumat automaattisesti vain, kun [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa tehdään muutoksia. Muutokset [!INCLUDE[d365fin](includes/cds_long_md.md)]ssa eivät aktivoi työjonotapahtumia.

## <a name="to-view-the-synchronization-job-log"></a>Synkronointityön lokin tarkasteleminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Integroinnin synkronointiloki** ja valitse sitten liittyvä linkki.
2.  Jos synkronointityössä tapahtui ainakin yksi virhe, virheiden määrä näkyy **Epäonnistui**-sarakkeessa. Näytä työn virheet valitsemalla numero.  

    > [!TIP]  
    > Voit tarkastella kaikkia synkronointitöiden virheitä avaamalla synkronointityölokin suoraan.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Synkronointityölokin tarkasteleminen taulukon yhdistämismäärityksistä  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Integrointitaulukon yhdistämismääritykset** ja valitse sitten liittyvä linkki.
2.  Valitse **Integrointitaulukon yhdistämismääritykset** -sivulla tapahtuma ja valitse sitten **Integroinnin synkronointityöloki**.  

## <a name="to-view-the-synchronization-error-log"></a>Synkronoinnin virhelokin tarkasteleminen  
* Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Integroinnin synkronointivirheet** ja valitse sitten liittyvä linkki.

## <a name="see-also"></a>Katso myös  
[Tietojen synkronointi Business Centralissa ja [!INCLUDE[d365fin](includes/cds_long_md.md)]issa](admin-synchronizing-business-central-and-sales.md)  
[Taulukon yhdistämismääritysten manuaalinen synkronointi](admin-manual-synchronization-of-table-mappings.md)  
[Business Centralin ja [!INCLUDE[d365fin](includes/cds_long_md.md)]in synkronoinnin ajoittaminen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Tietoja Dynamics 365 Business Centralin ja [!INCLUDE[d365fin](includes/cds_long_md.md)]in integroinnista](admin-prepare-dynamics-365-for-sales-for-integration.md)  
