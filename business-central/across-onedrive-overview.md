---
title: Business Centralin ja OneDrive for Businessin integrointi
description: OneDrive for Businessin avulla voit tallentaa, hallita ja jakaa tiedostoja, kuten raportteja tai tiedostoliitteitä. Voit myös kirjoittaa sen muodossa One Drive.
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 5968cd8d2348b0fac7c81c4b588dfd89388a27f5
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606465"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Centralin ja OneDrive for Businessin integrointi

OneDrive for Business on pilvitallennuspalvelu, joka sisältyy Microsoft 365:een. [!INCLUDE[prod_short](includes/prod_short.md)]in avulla on helppo tallentaa, hallita ja jakaa tiedostoja muiden ihmisten kanssa OneDriven kautta. Kun tiedosto on OneDrivessa, voit nauttia Microsoft-tuotteiden, kuten Wordin, Excelin ja PowerPointin, online-versioiden monipuolisista yhteiskäyttökokemuksista. Voit esimerkiksi jakaa Word-asiakirjan, jolloin sinä ja työtoverisi voitte muokata sitä yhdessä reaaliaikaisesti. OneDriven avulla voit myös avata muuntyyppisiä tiedostoja, kuten PDF-tiedostoja. 

## <a name="get-started-with-onedrive-features"></a>Aloita OneDrive-ominaisuuksien käyttö

Jos käytät [!INCLUDE[prod_short](includes/prod_short.md)] onlinea, olemme jo luoneet yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] onlinen ja OneDriven välille, joten on helppo päästä alkuun. Ainoa edellytys on, että käyttäjät ovat avanneet OneDriven ainakin yhden kerran. Paikallisessa [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa järjestelmänvalvojan on määritettävä yhteys, ennen kuin pääset alkuun. Lue lisätietoja kohdasta [OneDriven ja Business Centralin integroinnin hallinta](admin-onedrive-integration.md).

<!-- We've created the connection between [!INCLUDE[prod_short](includes/prod_short.md)] online and OneDrive, so it's easy to get started. The only requirement is that users have opened OneDrive at least one time. -->

### <a name="open-and-share-in-onedrive"></a>Avaa ja jaa OneDrivessä

Useimmilla sivuilla, joilla on saatavilla tiedostoja, kuten raportin Saapuneet-kansio tai tiedostot, jotka on liitetty tietueisiin, löydät **Avaa OneDrivessa**- ja **Jaa**-toiminnot.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Raporttien Avaa OneDrivessa- ja Jaa-toiminnot":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Liitteiden Avaa OneDrivessa- ja Jaa-toiminnot":::

|Valitse…|Vastaanottaja...|Katso lisätietoja...|
|---------|-----|----------------|
|Avaa OneDrivessa|Kopioi tiedosto OneDriven Business Central -kansioon ja avaa tiedosto.|[Avaa OneDrivessa](across-share-onedrive.md#open-in-onedrive) |
|Osuus|Kopioi tiedosto OneDriveen ja jaa se muiden käyttäjien kanssa.|[Jaa OneDrivessa](across-share-onedrive.md#share) |

### <a name="save-excel-workbooks-and-report-files-in-onedrive"></a>Tallenna Excel-työkirjat ja raporttitiedostot OneDriveen

Kun OneDrive-integrointi on määritetty, pari muuta tuttua ominaisuutta käyttää automaattisesti OneDrivea tiedostojen tallentamiseen sen sijaan, että tallentaisi tiedostoja laitteeseen:

- **Avaa Excelissä** ja **Muokkaa Excelissä** -toiminnot luettelosivuilla kopioivat Excel-tiedoston automaattisesti OneDriveen ja avaavat sen sitten Excel Onlinessa. Lisätietoja on kohdassa [Katsele ja muokkaa Excelissä](across-work-with-excel.md).
- Raportin lähettäminen Exceliin tai Wordiin kopioi tiedoston automaattisesti OneDriveen ja avaa sen sitten Excel- tai Word Onlinessa. Lisätietoja on kohdassa [Raportin tallentaminen tiedostoon](ui-work-report.md#saving-a-report-to-a-file).

Nämä toiminnot eivät ole oletusarvoisesti käytössä. Järjestelmänvalvojana voit kuitenkin helposti ottaa ne käyttöön käyttämällä **OneDrive-määrityksen** asetusten ohjattua määritysopasta.

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) in the content for OneDrive.
-->

> [!NOTE]
> Voit myös yhdistää [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -version OneDriveen. On kuitenkin olemassa muutamia asioita, jotta se toimisi. Lisätietoja on kohdassa [Business Central on-premises -version määritys](admin-onedrive-integration-onpremises.md).

## <a name="see-also"></a>Katso myös

[OneDriven ja Business Centralin integroinnin hallinta](admin-onedrive-integration.md)  
[Business Central-tiedostojen avaaminen OneDrivessa](across-share-onedrive.md)  
[OneDrive – usein kysytyt kysymykset](admin-onedrive-faq.md)  
