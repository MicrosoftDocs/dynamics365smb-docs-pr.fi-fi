---
title: Käytä Power Automate -työnkulun hälytyksiä entiteetin muutoksille
description: Opi luomaan Power Automatessa työnkulku, joka hälyttää, kun entiteetti muuttuu Dataverse-ympäristössä.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power Automate, Flow, Dataverse
ms.search.form: ''
ms.date: 09/05/2022
ms.author: bholtorf
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: fb5b2fa88289ff3d9d491f9b8ee7d73706740020
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2022
ms.locfileid: "9461256"
---
# <a name="use-a-power-automate-flow-for-alerts-to-dataverse-entity-changes"></a>Käytä Power Automate -työnkulun hälytyksiä Dataverse-entiteetin muutoksille

> [!IMPORTANT]
> Tässä artikkelissa kuvataan toiminnallisuus, joka tulee saataville vuoden 2022 julkaisuaalto 2:ssa. Ennen kuin kyseinen julkaisu on saatavilla, et voi käyttää Power Automate -työnkulkua varoittamiseen, kun entiteettiä muutetaan Dataversessä.

Järjestelmänvalvojat voivat luoda Power Automatessa automatisoidun työnkulun, joka ilmoittaa [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukselle muutoksista [!INCLUDE [cds_long_md](includes/cds_long_md.md)] -organisaation tietueisiin.

> [!NOTE]
> Tässä artikkelissa oletetaan, että olet kytkenyt [!INCLUDE[prod_short](includes/prod_short.md)]-Online-version [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-sovellukseen ja ajoittanut niiden synkronoinnin niiden välillä.

## <a name="define-the-flow-trigger"></a>Määritä työnkulun käynnistin

1. Kirjaudu sisään [Power Automateen](https://flow.microsoft.com).
2. Luo automatisoitu pilvityönkulku, joka alkaa, kun [!INCLUDE [cds_long_md](includes/cds_long_md.md)] -entiteetin rivi lisätään, muokataan tai poistetaan. Lisätietoja on kohdassa [Käynnistäminen työnkulkujen lisääminen rivin lisäämisen, muokkaamisen tai poistamisen yhteydessä](/power-automate/dataverse/create-update-delete-trigger). Tässä esimerkissä käytetään **asiakkuudet**-entiteettiä. Seuraavassa kuvassa on työnkulun käynnistimen määrittämisen ensimmäisen vaiheen asetukset.

:::image type="content" source="media/power-automate-flow-dataverse-trigger.png" alt-text="Työnkulun käynnistimen asetukset":::

3. Lisää yhteys [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-ympäristöön käyttämällä **AssistEdit (...)** -painiketta oikeassa yläkulmassa.
4. Valitse **Näytä lisäasetukset** ja kirjoita **Suodattimen rivit** -kenttään **customertypecode eq 3** tai **customertypecode eq 11** ja **statecode EQ 0**. Nämä arvot tarkoittavat, että käynnistin reagoi vain silloin, kun **asiakas**- tai **toimittaja**-tyypin aktiivisiin tileihin tehdään muutoksia.

## <a name="define-the-flow-condition"></a>Määritä työnkulun ehto

Tiedot synkronoidaan integrointikäyttäjätilin avulla [!INCLUDE[prod_short](includes/prod_short.md)]-sovelluksen ja [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-sovelluksen välillä. Voit ohittaa synkronoinnin tekemät muutokset luomalla työnkulkuun ehtovaiheen, joka ei sisällä integrointikäyttäjätilin tekemiä muutoksia.  

1. Lisää **Hae rivi tunnuksen mukaan Dataversestä**-vaihe työnkulun käynnistimen jälkeen seuraavilla asetuksilla. Lisätietoja on kohdassa [Hae rivi tunnuksen mukaan Dataversesta](/power-automate/dataverse/get-row-id).
    1. Valitse **Taulukon nimi** -kentässä **Käyttäjät**
    2. Valitse **rivin tunnus** -kentässä työnkulun käynnistimen **muokkaaja (arvo)**.  
2. Voit määrittää integrointikäyttäjätilin lisäämällä ehtovaiheen, jossa on seuraavat **tai**-asetukset.
    1. Käyttäjän **ensisijainen sähköpostiosoite** sisältää **contoso.com** 
    2. Käyttäjän **koko nimi** sisältää **[!INCLUDE[prod_short](includes/prod_short.md)]**. 
3. Lisää Lopeta ohjausobjekti, jos haluat pysäyttää työnkulun ehdon täyttyessä. Tämä tarkoittaa sitä, että jos ehto täyttyy ja integrointikäyttäjätili muutti entiteetin.

Seuraavassa kuvassa on lisätietoja, jotka lisätään työnkulun käynnistimen ja työnkulun kunnon määrittämiseksi.

:::image type="content" source="media/power-automate-flow-dataverse.png" alt-text="Yleiskuva työnkulun käynnistimen ja kunnon asetuksista":::

## <a name="notify-business-central-about-a-change"></a>Muutoksen ilmoittaminen Business Centralin avulla

Jos työnkulkua ei ole pysäytetty ehdon mukaan, sinun täytyy ilmoittaa kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)] muutoksen tapahtuneen. Käytä [!INCLUDE[prod_short](includes/prod_short.md)] -yhdistintä tehdäksesi sen.

1. Lisää toiminto **Ei**-haaraan ehtovaiheessa ja hae **Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]**. Valitse yhdistinkuvake luettelosta. 
2. Valitse **Luo tietue (V3)** -toiminto.

:::image type="content" source="media/power-automate-flow-dataverse-connector.png" alt-text="[!INCLUDE[prod_short](includes/prod_short.md)]-yhdistimen asetukset":::

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
2. Lisää [!INCLUDE[prod_short](includes/prod_short.md)]-API-liittymän avulla tietue, jonka **entiteetin nimi** on asetettu **tilille** **Dataverse-tapahtuman muutos** -taulukossa. 3. [!INCLUDE[prod_short](includes/prod_short.md)] aloittaa työjonotapahtuman, joka synkronoi asiakkaiden tilit.

## <a name="see-also"></a>Katso myös

[Business Centralin käyttö Power Automate -työnkuluissa](across-how-use-financials-data-source-flow.md)  
[Automaattisten työnkulkujen määrittäminen](/business-central/dev-itpro/powerplatform/automate-workflows)  
[Integrointi Microsoft Dataversein kanssa](admin-common-data-service.md)  
[Tietojen synkronointi Business Centralissa Microsoft Dataversen avulla](admin-synchronizing-business-central-and-sales.md)  