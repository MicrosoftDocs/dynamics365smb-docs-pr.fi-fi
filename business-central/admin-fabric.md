---
title: Johdatus Microsoft Fabriciin ja Business Centraliin
description: 'Microsoft Fabric:n yleiskatsaus merkityksellisten tietojen, liiketoimintatietojen ja tunnuslukujen hakemiseen Business Central -tiedoista.'
author: kennienp
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: bholtorf
ms.date: 04/24/2024
ms.author: kepontop
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="introduction-to-microsoft-fabric-and-business-central"></a>Johdatus Microsoft Fabriciin ja Business Centraliin

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] on kokonaisvaltainen analytiikkaratkaisu, joka sisältää täyden palvelun ominaisuudet, kuten tietojen siirron, Data Lake -tallennustilat, tietojen suunnittelun ja integroinnin, datatieteen, reaaliaikaisen analytiikan ja liiketoimintatiedot. Niitä tukee jaettu ympäristö, joka sisältää vankan tietoturvan, hallinnon ja vaatimustenmukaisuuden. Organisaatiossa ei enää tarvitse kerätä yksittäisiä analytiikkapalveluita useilta toimittajilta. Sen sijaan käytetään tehostettua ratkaisua, jonka yhdistäminen, käyttöönotto ja käyttö on helppoa.

> [!NOTE]
> Lisätietoja Microsoft Fabricin julkaisusuunnitelmasta on kohdassa [aka.ms/FabricRoadmap](https://aka.ms/FabricRoadmap)
> 
> Tämän toteutussuunnitelman säännöllinen julkaiseminen kertoo, miten [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] auttaa yrityksen tarpeiden täyttämisessä.

## <a name="where-does--fit-into-includeprod_short-analytics"></a>Miten [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] ja [!INCLUDE[prod_short](includes/prod_short.md)]in analytiikka toimivat yhdessä

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää useita valmiita raportteja ja tietoanalytiikkaominaisuuksia, kuten taloushallinnon raportointi, Excelissä avaaminen ja analytiikkatila luetteloissa ja kyselyissä. Tämän lisäksi on helppo määrittää Power BI -raportteja, jotka lukevat tietoja vakio-ohjelmointirajapinnoista ja mukautetuista ohjelmointirajapinnoista, määrittävät Power BI:n mittareiden tuloskortteja ja upottavat nämä kaikki suoraan [!INCLUDE[prod_short](includes/prod_short.md)] -asiakasohjelmaan. [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] voi olla hyvä vaihtoehto asiakkaille, jotka käyttävät edistyneitä datatiede- tai liiketoimintatietoskenaarioita, joissa vaaditaan monipuolista tietojen suunnittelua tai tietojen integrointia. 

## <a name="onelake"></a>OneLake

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] -valikoiman keskeinen osa on OneLake. OneLake on yksi yhtenäinen, looginen Data Lake -tallennustila koko organisaatiolle. OneLake on kuin OneDrive tiedoille. Se tarjoaa Data Lake -tallennustilan palveluna, joten sitä ei tarvitse muodostaa itse. OneLake sisältyy automaattisesti jokaiseen [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] -vuokraajaan, eikä hallittavaa infrastruktuuria ole. Kaikki OneLake -tallennustilaan siirrettävät tiedot ovat automaattisesti osa valmista tietojen hallintoa, kuten tietojen siirtymää, tietojen suojausta, sertifiointia ja luettelon integrointia. Se jaottelee tietosiilot ottamalla käyttöön organisaation eri osat itsenäiseen työskentelyyn niin, että ne yhä käyttävät samaa Data Lake -tallennustilaa.

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] -kohteet tallentavat tiedot OneLake-tallennustilaan avoimessa tiedostomuodossa. Rakenteellisilla taulukkomuotoisilla tiedoilla tämä muoto on *delta parquet*. Delta parquet -muodon avulla [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]in jokainen analyysimoduuli voi käyttää muiden analyysimoduulien tietoja. Näin tietojen käsittelijät voivat käyttää haluttuja työkaluja.


## <a name="see-also"></a>Katso myös
[Power BI:n käyttäminen Business Centralin kanssa](admin-powerbi.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
