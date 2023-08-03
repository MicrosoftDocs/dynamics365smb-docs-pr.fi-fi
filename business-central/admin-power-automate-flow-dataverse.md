---
title: Käytä Power Automate -työnkulun hälytyksiä entiteetin muutoksille
description: 'Opi luomaan Power Automatessa työnkulku, joka hälyttää, kun entiteetti muuttuu Dataverse-ympäristössä.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Power Automate, Flow, Dataverse'
ms.search.form: null
ms.date: 09/05/2022
ms.author: bholtorf
---
# Käytä Power Automate -työnkulun hälytyksiä Dataverse-entiteetin muutoksille

Järjestelmänvalvojat voivat luoda Power Automatessa automatisoidun työnkulun, joka ilmoittaa [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukselle muutoksista [!INCLUDE [cds_long_md](includes/cds_long_md.md)] -organisaation tietueisiin.

> [!NOTE]
> Tässä artikkelissa oletetaan, että olet kytkenyt [!INCLUDE[prod_short](includes/prod_short.md)]-Online-version [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-sovellukseen ja ajoittanut niiden synkronoinnin niiden välillä.

## Tuo työnkulun malli

> [!TIP]
> Työnkulun määrittämisen helpottamiseksi olemme luoneet mallin, joka määrittää työnkulun käynnistimen ja työnkulun kunnon. Voit käyttää mallia noudattamalla tämän osion ohjeita. Jos haluat luoda työnkulun itse, ohita tämä osa ja aloita kohdassa [työnkulun käynnistimen määrittäminen](#define-the-flow-trigger).

1. Kirjaudu sisään [Power Automateen](https://powerautomate.microsoft.com).
2. Valitse **Mallit** ja etsi sitten **Ilmoita Business Centralille**.

:::image type="content" source="media/power-automate-import-template.png" alt-text="Avainsanat, joilla löydät työnkulun mallin.":::
3. Valitse **Ilmoita Business Centralille, kun tili muuttuu** -malli.
4. Jatka seuraamalla ohjeita [Ilmoita Business Centralille muutoksista](#notify-business-central-about-a-change) -osiosta.

## Määritä työnkulun käynnistin

1. Kirjaudu sisään [Power Automateen](https://flow.microsoft.com).
2. Luo automatisoitu pilvityönkulku, joka alkaa, kun [!INCLUDE [cds_long_md](includes/cds_long_md.md)] -entiteetin rivi lisätään, muokataan tai poistetaan. Lisätietoja on kohdassa [Käynnistäminen työnkulkujen lisääminen rivin lisäämisen, muokkaamisen tai poistamisen yhteydessä](/power-automate/dataverse/create-update-delete-trigger). Tässä esimerkissä käytetään **asiakkuudet**-entiteettiä. Seuraavassa kuvassa on työnkulun käynnistimen määrittämisen ensimmäisen vaiheen asetukset.

:::image type="content" source="media/power-automate-flow-dataverse-trigger.png" alt-text="Työnkulun käynnistimen asetukset":::
3. Lisää yhteys [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-ympäristöön käyttämällä **AssistEdit (...)** -painiketta oikeassa yläkulmassa.
4. Valitse **Näytä lisäasetukset** ja kirjoita **Suodattimen rivit** -kenttään **customertypecode eq 3** tai **customertypecode eq 11** ja **statecode EQ 0**. Nämä arvot tarkoittavat, että käynnistin reagoi vain silloin, kun **asiakas**- tai **toimittaja**-tyypin aktiivisiin tileihin tehdään muutoksia.

## Määritä työnkulun ehto

Tiedot synkronoidaan integrointikäyttäjätilin avulla [!INCLUDE[prod_short](includes/prod_short.md)]-sovelluksen ja [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-sovelluksen välillä. Voit ohittaa synkronoinnin tekemät muutokset luomalla työnkulkuun ehtovaiheen, joka ei sisällä integrointikäyttäjätilin tekemiä muutoksia.  

1. Lisää **Hae rivi tunnuksen mukaan Dataversestä**-vaihe työnkulun käynnistimen jälkeen seuraavilla asetuksilla. Lisätietoja on kohdassa [Hae rivi tunnuksen mukaan Dataversesta](/power-automate/dataverse/get-row-id).

    1. Valitse **Taulukon nimi** -kentässä **Käyttäjät**
    2. Valitse **rivin tunnus** -kentässä työnkulun käynnistimen **muokkaaja (arvo)**.  

2. Voit määrittää integrointikäyttäjätilin lisäämällä ehtovaiheen, jossa on seuraavat **tai**-asetukset.
    1. Käyttäjän **ensisijainen sähköpostiosoite** sisältää **contoso.com**
    2. Käyttäjän **koko nimi** sisältää **[!INCLUDE[prod_short](includes/prod_short.md)]**.

3. Lisää Lopeta ohjausobjekti, jos haluat pysäyttää työnkulun, jos integrointikäyttäjätili on muuttanut entiteetin.

Seuraavassa kuvassa nähdään miten työnkulun käynnistin ja työnkulun kunto määritetään.

:::image type="content" source="media/power-automate-flow-dataverse.png" alt-text="Yleiskuva työnkulun käynnistimen ja kunnon asetuksista":::

## Muutoksen ilmoittaminen Business Centralin avulla

Jos työnkulkua ei ole pysäytetty ehdon mukaan, sinun täytyy ilmoittaa kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)] muutoksen tapahtuneen. Käytä [!INCLUDE[prod_short](includes/prod_short.md)] -yhdistintä tehdäksesi sen.

1. Lisää toiminto **Ei**-haaraan ehtovaiheessa ja hae **Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]**. Valitse yhdistinkuvake luettelosta.
2. Valitse **Luo tietue (V3)** -toiminto.

:::image type="content" source="media/power-automate-flow-dataverse-connector.png" alt-text="[!INCLUDE[prod_short](includes/prod_short.md)] liittimen asetukset":::

3. Lisää yhteys [!INCLUDE[prod_short](includes/prod_short.md)]-ympäristöön käyttämällä **Muokkausapu (...)** -painiketta oikeassa yläkulmassa.
4. Kun yhteys on muodostettu, täytä **ympäristön nimi**- ja **yrityksen nimi** -kentät.
5. Kirjoita **API-luokka**-kenttään **microsoft/dataverse/v 1.0**.
6. Syötä **Taulukon nimi** -kenttään **dataverseEntityChanges**.
7. Syötä **Tili** **entityName**-kenttään.
8. Tallenna työnkulku.

Seuraavasta kuvasta näet miltä työnkulun pitäisi näyttää.

:::image type="content" source="media/power-automate-flow-dataverse-summary.png" alt-text="Kaikkien työnkulun asetusten yleiskuvaus":::

Kun lisäät, poistat tai muokkaat tiliä omassa [!INCLUDE [cds_long_md](includes/cds_long_md.md)] -ympäristössäsi, tämä työnkulku tekee seuraavat toimet:

1. Soita [!INCLUDE[prod_short](includes/prod_short.md)]-ympäristöön, jonka olet määrittänyt [!INCLUDE[prod_short](includes/prod_short.md)]-yhdistimessä.
2. Lisää [!INCLUDE[prod_short](includes/prod_short.md)]-API-liittymän avulla tietue, jonka **entityName** on asetettu **tilille** **Dataverse-tapahtuman muutos** -taulukossa. Tämä parametri on sen Dataverse-entiteetin tarkka nimi, jolle olet luomassa työnkulun.
3. [!INCLUDE[prod_short](includes/prod_short.md)] aloittaa työjonotapahtuman, joka synkronoi asiakkaiden tilit.

## Katso myös

[Business Centralin käyttö Power Automate -työnkuluissa](across-how-use-financials-data-source-flow.md)  
[Automaattisten työnkulkujen määrittäminen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Integrointi Microsoft Dataversein kanssa](admin-common-data-service.md)  
[Tietojen synkronointi Business Centralissa Microsoft Dataversen avulla](admin-synchronizing-business-central-and-sales.md)  
