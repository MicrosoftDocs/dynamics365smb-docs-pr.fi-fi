---
title: Business Centralin ja Dataversen synkronointi
description: Lisätietoja tietojen synkronoinnissa Business Centralin ja Dataversein välillä.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
---

# <a name="scheduling-a-synchronization-between-business-central-and-dataverse"></a><a name="scheduling-a-synchronization-between-business-central-and-dataverse"></a>Business Centralin ja Dataversein synkronoinnin ajoittaminen

Voit synkronoida [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in tietyin väliajoin määrittämällä työt työjonoon. Synkronointityöt synkronoivat [!INCLUDE[prod_short](includes/prod_short.md)]in tietueiden tiedot ja [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in tietueet, jotka on yhdistetty. Vielä yhdistämättömistä tietueista synkronointityöt voivat luoda ja yhdistää uusia tietueita kohdejärjestelmässä synkronointisuunnan ja -sääntöjen mukaisesti.

Käytettävissä on heti useita synkronointitöitä. Työt suoritetaan seuraavassa järjestyksessä, jotta taulukoiden välille ei muodostu yhdistämisen riippuvuussuhteita. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).

1. VALUUTTA - Common Data Service -synkronointityö.
2. TOIMITTAJA - Common Data Service -synkronointityö.
3. YHTEYSHENKILÖ - Common Data Service -synkronointityö.
4. ASIAKAS - Common Data Service -synkronointityö.
5. MYYJÄT - Common Data Service -synkronointityö.

Voit tarkastella töitä **Työjonon tapahtumat** -sivulla. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).

## <a name="default-synchronization-job-queue-entries"></a><a name="default-synchronization-job-queue-entries"></a>Oletusarvoiset synkronoinnin työjonotapahtumat

Seuraavassa taulukossa kuvaillaan [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:n synkronoinnin oletustyöt.  

| Työjonotapahtuma | Kuvaus | Suunta | Integrointitaulukon yhdistämismääritys | Synkronoinnin oletustiheys (min) | Passivisuuden oletusaika (min) |
|--|--|--|--|--|--|--|
| KONTAKTI - Common Data Service -synkronointityö | Synkronoi [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in kontaktit [!INCLUDE[prod_short](includes/prod_short.md)]in kontakteilla. | Kaksisuuntainen | KONTAKTI | 30 | 720 <br>(12 tuntia) |
| VALUUTTA - Common Data Service -synkronointityö | Synkronoi [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in tapahtumien valuutat [!INCLUDE[prod_short](includes/prod_short.md)]in valuuttojen kanssa. | [!INCLUDE[prod_short](includes/prod_short.md)]ista [!INCLUDE[cds_long_md](includes/cds_long_md.md)]iin | VALUUTTA | 30 | 720 <br> (12 tuntia) |
| ASIAKAS - Common Data Service -synkronointityö | Synkronoi [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in tilit ja [!INCLUDE[prod_short](includes/prod_short.md)]in asiakkaat. | Kaksisuuntainen | ASIAKAS | 30 | 720<br> (12 tuntia) |
| TOIMITTAJA - Common Data Service -synkronointityö | Synkronoi [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in tilit ja [!INCLUDE[prod_short](includes/prod_short.md)]in asiakkaat. | Kaksisuuntainen | TOIMITTAJA | 30 | 720<br> (12 tuntia) |
| MYYJÄT - Common Data Service -synkronointityö | Synkronoi [!INCLUDE[prod_short](includes/prod_short.md)]in myyjät ja [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in käyttäjät. | [!INCLUDE[cds_long_md](includes/cds_long_md.md)]ista [!INCLUDE[prod_short](includes/prod_short.md)]iin | MYYJÄT | 30 | 1440<br> (24 tuntia) |

## <a name="synchronization-process"></a><a name="synchronization-process"></a>Synkronointiprosessi

Kunkin synkronoinnin työjonotapahtuma käyttää tiettyä integrointitaulukon yhdistämismääritystä, joka määrittää, mikä [!INCLUDE[prod_short](includes/prod_short.md)]in taulukko ja mikä [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in taulukko synkronoidaan. Taulukon yhdistämismääritykset sisältävät myös joitakin asetuksia, jotka määrittävät, mitkä [!INCLUDE[prod_short](includes/prod_short.md)]in taulukon ja [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in taulukon tietueet synkronoidaan.  

Tietojen synkronointi edellyttää, että [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -taulukon tietueet on yhdistettävä [!INCLUDE[prod_short](includes/prod_short.md)]in tietueisiin. Esimerkiksi [!INCLUDE[prod_short](includes/prod_short.md)]in asiakas on yhdistettävä [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in tiliin. Yhdistämiset voidaan määrittää manuaalisesti, ennen kuin suoritat synkronointitöitä tai voit antaa synkronointitöiden määrittää yhdistämiset automaattisesti. Seuraavassa luettelossa käsitellään tietojen synkronointia [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in ja [!INCLUDE[prod_short](includes/prod_short.md)]in välillä, kun käytät synkronoinnin työjonon tapahtumia. Lisätietoja on kohdassa [Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md).

- **Synkronoi vain yhdistetyt tietueet** -valintaruutu määrittää, luodaanko uusia tietueita synkronoinnin yhteydessä. Oletusarvon mukaan valintaruutu on valittuna, joten vain kytkettyjä tietueita synkronoidaan. Integraatiotaulukon yhdistämismäärityksissä voit muuttaa taulukon yhdistämismäärityksiä [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in taulukon ja [!INCLUDE[prod_short](includes/prod_short.md)]in taulukon välillä siten, että integroinnin synkronointityöt luovat uudet tietueet kohdetietokantaan kullekin lähdetietokannan riville, jota ei ole yhdistetty. Lisätietoja on kohdassa [Uusien tietueiden luominen](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

    **Esimerkki**: Jos tyhjennät **Synkronoi vain yhdistetyt tietueet** -valintaruudun, kun synkronoit [!INCLUDE[prod_short](includes/prod_short.md)] -asiakkaat [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -tilien kanssa, ohjelma luo uuden tilin kullekin asiakkaalle [!INCLUDE[prod_short](includes/prod_short.md)]ssa ja yhdistää sen automaattisesti. Lisäksi koska tässä tapauksessa synkronointi on kaksisuuntainen, uusi asiakas luodaan ja yhdistetään kuhunkin vielä yhdistämättömään [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in tiliin.  

    > [!NOTE]  
    > Synkronoitavat tiedot määrittyvät sääntöjen ja suodattimien perusteella. Lisätietoja on kohdassa [Synkronointisäännöt](admin-synchronizing-business-central-and-sales.md).

- Kun [!INCLUDE[prod_short](includes/prod_short.md)]issa luodaan uusia tietueita, tietueet käyttävät joko integrointitaulukon yhdistämismääritykselle määritettyä mallia tai oletusmallia, jollainen on jokaisella rivityypillä. Kentät täytetään [!INCLUDE[prod_short](includes/prod_short.md)]in tai [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in tiedoilla synkronoinnin suunnan perusteella. Lisätietoja on kohdassa [Taulukon yhdistämismääritysten muokkaaminen synkronointia varten](admin-how-to-modify-table-mappings-for-synchronization.md).  

- Seuraavissa synkronoinneissa päivitetään vain tietueet, joita on muokattu tai lisätty taulukon edellisen onnistuneen synkronointityön jälkeen.  

     [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in uudet tietueet lisätään [!INCLUDE[prod_short](includes/prod_short.md)]issa. Jos [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in tietueiden kenttien tiedot ovat muuttuneet, tiedot kopioidaan vastaavan kenttään [!INCLUDE[prod_short](includes/prod_short.md)]issa.  

- Kaksisuuntaisessa synkronoinnissa työ synkronoituu [!INCLUDE[prod_short](includes/prod_short.md)]ista [!INCLUDE[cds_long_md](includes/cds_long_md.md)]iin ja sitten [!INCLUDE[cds_long_md](includes/cds_long_md.md)]sta [!INCLUDE[prod_short](includes/prod_short.md)]iin.

## <a name="about-inactivity-timeouts"></a><a name="about-inactivity-timeouts"></a>Tietoja käyttämättömyyden aikakatkaisusta

Jotkin työjonotapahtumat, esimerkiksi ne, jotka ajoittavat [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman ja [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:n välisen synkronoinnin, käyttävät Työjonotapahtuma-sivulla **Käyttämättömyyden aikakatkaisu** -kenttää estämään työjonotapahtuman tarpeettoman suorittamisen.  

:::image type="content" source="media/on-hold-with-inactivity-timeout.png" alt-text="Vuokaavio siitä, kun työjonon tapahtumat ovat pidossa käyttämättömyyden vuoksi.":::

Jos tämän kentän arvo ei ole nolla eikä työjono löytänyt muutoksia viimeisen suorituksen aikana, [!INCLUDE[prod_short](includes/prod_short.md)] siirtää työjonotapahtuman pitoon. Kun näin tapahtuu, **Työjonon tila** -kentässä näkyy **Estossa toimettomuuden vuoksi**, ja [!INCLUDE[prod_short](includes/prod_short.md)] odottaa **Käyttämättömyyden aikakatkaisu** -kentässä määritetyn ajan, ennen kuin se suorittaa työjonotapahtuman uudelleen.  

Oletusarvon mukaan esimerkiksi CURRENCY-työjonotapahtuma, joka synkronoi valuutat [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -ohjelmassa [!INCLUDE[prod_short](includes/prod_short.md)]n valuuttakurssien mukaan, etsii vaihtokurssien muutoksia 30 minuutin välein. Jos muutoksia ei löydy, [!INCLUDE[prod_short](includes/prod_short.md)] asettaa CURRENCY-työjonotapahtuman pitoon 720 minuutin (kahdentoista tunnin) ajaksi. Jos vaihtokurssia muutetaan, [!INCLUDE[prod_short](includes/prod_short.md)]ssa, kun työjonotapahtuma on Estossa, [!INCLUDE[prod_short](includes/prod_short.md)] aktivoi automaattisesti uudelleen työjonontapahtuman ja työjono käynnistetään uudelleen. 

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] aktivoi pidossa olevat työjonotapahtumat automaattisesti vain, kun [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa tehdään muutoksia. Muutokset [!INCLUDE[cds_long_md](includes/cds_long_md.md)]ssa eivät aktivoi työjonotapahtumia.

## <a name="to-view-the-synchronization-job-log"></a><a name="to-view-the-synchronization-job-log"></a>Synkronointityön lokin tarkasteleminen

1. Valitse :::image type="icon" source="media/ui-search/search_small.png" border="false"::: -kuvake, kirjoita **Integroinnin synkronointiloki** ja valitse sitten aiheeseen liittyvä linkki.
2. Jos synkronointityössä tapahtui ainakin yksi virhe, virheiden määrä näkyy **Epäonnistui**-sarakkeessa. Näytä työn virheet valitsemalla numero.  

    > [!TIP]  
    > Voit tarkastella kaikkia synkronointitöiden virheitä avaamalla synkronointityölokin suoraan.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a><a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Synkronointityölokin tarkasteleminen taulukon yhdistämismäärityksistä

1. Valitse :::image type="icon" source="media/ui-search/search_small.png" border="false"::: -kuvake, kirjoita **Integroinnin yhdistämistaulukot** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Integrointitaulukon yhdistämismääritykset** -sivulla tapahtuma ja valitse sitten **Integroinnin synkronointityöloki**.  

## <a name="to-view-the-synchronization-error-log"></a><a name="to-view-the-synchronization-error-log"></a>Synkronoinnin virhelokin tarkasteleminen

- Valitse :::image type="icon" source="media/ui-search/search_small.png" border="false"::: -kuvake, kirjoita **Integroinnin synkronointivirheet** ja valitse sitten aiheeseen liittyvä linkki.

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Tietojen synkronointi Business Centralissa ja [!INCLUDE[cds_long_md](includes/cds_long_md.md)]issa](admin-synchronizing-business-central-and-sales.md)  
[Taulukon yhdistämismääritysten manuaalinen synkronointi](admin-manual-synchronization-of-table-mappings.md)  
[Business Centralin ja [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in synkronoinnin ajoittaminen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Tietoja Dynamics 365 Business Centralin ja [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in integroinnista](admin-prepare-dynamics-365-for-sales-for-integration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
