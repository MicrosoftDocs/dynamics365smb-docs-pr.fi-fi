---
title: Business Centralin ja OneDrive for Businessin integrointi
description: OneDrive for Businessin avulla voit tallentaa, hallita ja jakaa tiedostoja, kuten raportteja tai tiedostoliitteitä.
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 371c090e321992ec2fdc0ee7cb218feaa6b16d9a
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8521226"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Centralin ja OneDrive for Businessin integrointi

OneDrive for Business on pilvitallennuspalvelu, joka sisältyy Microsoft 365:een. [!INCLUDE[prod_short](includes/prod_short.md)]in avulla on helppo tallentaa, hallita ja jakaa tiedostoja muiden ihmisten kanssa OneDriven kautta. Kun tiedosto on OneDrivessa, voit nauttia Microsoft-tuotteiden, kuten Wordin, Excelin ja PowerPointin, online-versioiden monipuolisista yhteiskäyttökokemuksista. Voit esimerkiksi jakaa Word-asiakirjan, jolloin sinä ja työtoverisi voitte muokata sitä yhdessä reaaliaikaisesti. OneDriven avulla voit myös avata muuntyyppisiä tiedostoja, kuten PDF-tiedostoja. 

## <a name="getting-started"></a>Aloitusopas

Olemme luoneet yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] onlinen ja OneDriven välille, joten on helppo päästä alkuun. Ainoa edellytys on, että käyttäjät ovat avanneet OneDriven ainakin yhden kerran. 

Useimmilla sivuilla, joilla on saatavilla tiedostoja, kuten raportin Saapuneet-kansio tai tiedostot, jotka on liitetty tietueisiin, löydät **Avaa OneDrivessa**- ja **Jaa**-toiminnot.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Raporttien Avaa OneDrivessa- ja Jaa-toiminnot":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Liitteiden Avaa OneDrivessa- ja Jaa-toiminnot":::

|Valitse…|Vastaanottaja...|Katso lisätietoja...|
|---------|-----|----------------|
|Avaa OneDrivessa|Kopioi tiedosto OneDriven Business Central -kansioon ja avaa tiedosto.|[Avaa OneDrivessa](across-share-onedrive.md#open-in-onedrive) |
|Osuus|Kopioi tiedosto OneDriveen ja jaa se muiden käyttäjien kanssa.|[Jaa OneDrivessa](across-share-onedrive.md#share) |

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).
-->

> [!NOTE]
> Voit myös yhdistää [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -version OneDriveen. On kuitenkin olemassa muutamia asioita, jotta se toimisi. Lisätietoja on kohdassa [Business Central on-premises -version määritys](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Katso myös
[OneDriven ja Business Centralin integroinnin hallinta](admin-onedrive-integration.md)  
[Business Central-tiedostojen avaaminen OneDrivessa](across-share-onedrive.md)  
[OneDrive – usein kysytyt kysymykset](admin-onedrive-faq.md)