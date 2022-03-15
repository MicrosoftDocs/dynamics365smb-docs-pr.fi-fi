---
title: Business Centralin ja OneDrive for Businessin integrointi
description: OneDrive for Businessin avulla voit tallentaa, hallita ja jakaa tiedostoja, kuten raportteja tai tiedostoliitteitä.
author: brentholtorf
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: bholtorf
ms.openlocfilehash: 522bf01d08e77e52b4fbcf32f2652c53208cf8ec
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381827"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Centralin ja OneDrive for Businessin integrointi
OneDrive for Business on pilvitallennuspalvelu, joka sisältyy Microsoft 365:een. [!INCLUDE[prod_short](includes/prod_short.md)]in avulla on helppo tallentaa, hallita ja jakaa tiedostoja muiden ihmisten kanssa OneDriven kautta. Kun tiedosto on OneDrivessa, voit nauttia Microsoft-tuotteiden, kuten Wordin, Excelin ja PowerPointin, online-versioiden monipuolisista yhteiskäyttökokemuksista. Voit esimerkiksi jakaa Word-asiakirjan, jolloin sinä ja työtoverisi voitte muokata sitä yhdessä reaaliaikaisesti. OneDriven avulla voit myös avata muuntyyppisiä tiedostoja, kuten PDF-tiedostoja. 

## <a name="getting-started"></a>Aloitusopas
Olemme luoneet yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] onlinen ja OneDriven välille, joten on helppo päästä alkuun. Ainoa edellytys on, että käyttäjät ovat avanneet OneDriven ainakin yhden kerran. 

Useimmilla sivuilla, joilla on saatavilla tiedostoja, kuten raportin Saapuneet-kansio tai tiedostot, jotka on liitetty tietueisiin, löydät **Avaa OneDrivessa** -toiminnon.

:::image type="content" source="media/Open in OneDrive.PNG" alt-text="Avaa OneDrivessa -toiminto":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Tiedostoliitteiden jakaminen OneDrivessa":::

Kun käytät **Avaa OneDrivessa** -toimintoa ensimmäistä kertaa, [!INCLUDE[prod_short](includes/prod_short.md)] tekee seuraavat toimet OneDrivessa:

1. Luo kansion nimeltä [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. [!INCLUDE[prod_short](includes/prod_short.md)] -kansiossa se luo toisen kansion, jolla on sama nimi kuin käsiteltävällä yrityksellä. Jos työskentelet useammassa kuin yhdessä yrityksessä, ohjelma luo sen yrityksen kansion, jota käsittelet, kun käytät **Avaa OneDrivessa** -toimintoa. 
3. Tuo kansioon kopion valitusta tiedostosta ja avaa tiedoston. Kun seuraavan kerran käytät toimintoa, se vain kopioi ja avaa tiedoston. 

Kansio ja sen sisältö ovat yksityisiä, kunnes päätät jakaa ne muiden kanssa. Voit esimerkiksi päättää jakaa sisältöä yhden tai useamman työtoverisi tai jopa organisaatiosi ulkopuolisen henkilön kanssa. Lisätietoja on artikkelissa [OneDrive-tiedostojen ja -kansioiden jakaminen](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Voit myös yhdistää [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -version OneDriveen. On kuitenkin olemassa muutamia asioita, jotta se toimisi. Lisätietoja on kohdassa [Business Central on-premises -version määritys](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Katso myös
[OneDriven ja Business Centralin integroinnin hallinta](admin-onedrive-integration.md)  
[Business Central-tiedostojen avaaminen OneDrivessa](across-share-onedrive.md)  
[OneDrive – usein kysytyt kysymykset](admin-onedrive-faq.md)