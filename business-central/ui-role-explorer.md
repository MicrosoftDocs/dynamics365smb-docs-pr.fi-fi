---
title: Roolin mukainen sivuihin tutustuminen ja niissä siirtyminen
description: Roolien hallinnan avulla saat yleiskuvan kaikista roolin käytössä olevista liiketoimintaominaisuuksista ja muiden roolien toiminnoista.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: role explorer, find features, navigate
ms.search.form: RoleExplorer, 9020, 9022, 9027, 9018
ms.date: 08/01/2021
ms.author: jswymer
ms.openlocfilehash: 00831e4109f765f9ae0d275acc3f0c9902e1dae2
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512072"
---
# <a name="finding-pages-with-the-role-explorer"></a>Sivujen etsiminen roolienhallinnan avulla

Saat yleiskuvan kaikista roolin käytössä olevista liiketoimintaominaisuuksista ja muiden roolien toiminnoista, jos siirryt yhden vaiheen eteenpäin. Seuraavassa dokumentaatiossa tätä ominaisuutta kutsutaan *Roolienhallinnaksi*.

Jokainen roolienhallinnan elementti on sivun avaava toiminto. Niinpä voitkin siirtyä [!INCLUDE[prod_short](includes/prod_short.md)]issa roolienhallinnan avulla.

## <a name="open-the-role-explorer"></a>Avaa roolien hallinta

Voit avata roolienhallinnan roolikeskuksesta ja kaikilta luettelosivuilta sekä **Kerro, mitä haluat tehdä** -ikkunasta.

- Valitse Roolikeskuksessa tai millä tahansa luettelosivulla ![Valikko-painike.](media/ui_menu_button.png "Valikko-painike") -painike siirtymispalkin oikealla puolella tai paina näppäinyhdistelmä Vaihto+F12.
- Valitse **Kerro, mitä haluat tehdä** -ikkunassa alareunassa oleva **tutustumistoiminto**.

Kun avaat roolikeskuksen ensimmäisen kerran, siinä näkyvät useimpien roolisi käytettävissä olevien toimintojen linkit.

## <a name="navigate-features"></a>Navigoi ominaisuuksia

Sivujen avoimet toiminnot on järjestetty ominaisuuksien tai sovellusalueiden mukaan nimetyille solmuille. Jokainen solmu voidaan tiivistää tai laajentaa yksittäin, ja voit tiivistää/laajentaa kaikki solmut yhteen.

- Jos haluat laajentaa tai supistaa yksittäisen solmun, valitse solmu. Tämä koskee ylimmän tason solmuja ja alisolmuja.
- Jos haluat laajentaa tai kutistaa kaikki sivun ylätason solmut, mutta jättää alisolmut sellaisiksi kuin ne ovat, valitse ylhäällä **...** ja valitse sitten **Laajenna** tai **Tiivistä**.
- Jos haluat laajentaa tai kutistaa kaikki sivun ylätason solmut ja alisolmut, valitse ylhäällä **...** ja valitse sitten **Laajenna kaikki** tai **Tiivistä kaikki**.

## <a name="search-for-features"></a>Etsi ominaisuuksia

Voit etsiä ominaisuuksia nopeasti valitsemalla **Etsi** ja kirjoittamalla sanan tai lauseen etsimääsi ominaisuutta varten. Roolikeskus tuo esiin mahdollisen vastaavan tekstin. Jos ominaisuus on piilossa tiivistetyn solmun näkymästä, tiivistetty solmu merkitään pisteellä. 

## <a name="explore-other-roles"></a>Tutki muita rooleja

Jos haluat tutkia muita rooleja kuin omia rooleja, valitse **Tutki lisää rooleja**. Roolikeskus näyttää jokaisen roolin oman otsikon alla, ja siinä on linkit sen ominaisuuksiin. Voit sitten navigoida ja etsiä ominaisuuksia aivan kuten omassa roolissasi.

> [!NOTE]
> Näet vain roolit, jotka on määritetty näkymään roolinhallinnassa. Jos et näe roolia, jonka oletit näkeväsi, sitä ei todennäköisesti ole määritetty. Lisätietoja on kohdassa [Profiilien hallinta](admin-users-profiles-roles.md). 

Kun tutustut muihin rooleihin, voit rajata etsintää myös roolikeskuksen yläosassa olevien **Raportti ja analyysi**- ja **Hallinta**-toimintojen avulla.

- **Raportti ja analyysi** näyttää vain ne ominaisuudet, jotka on luokiteltu raportti- ja analyysiominaisuuksina.
- **Hallinta**-ikkunassa näkyvät vain ne ominaisuudet, jotka on luokiteltu hallintaominaisuuksiksi.

> [!TIP]
> Sovelluskehittäjille voit luokitella sivuja ja raportteja määrittämällä objektin AL-koodissa [UsageCategory-ominaisuuden](/dynamics365/business-central/dev-itpro/developer/properties/devenv-usagecategory-property).
<!--
 
## Role explorer actions

There a several actions along the top of the role explorer to help you locate features of your role and other roles.

|Action|Description|
|------|------|
|**All**|Shows all features that are related to the role.|
|**Find**|Lets you enter a word or phrase to quickly locate feature names that match.|
|**Explore more roles**|All business features that are available for all roles including your own. When exploring all roles, the other actions work the same way, except for all roles shown. **NOTE:** You will only see roles that are set up to show in role explorer. For more information, see [Manage Profiles](admin-users-profiles-roles.md).  |
|**Report & Analysis**|This action Shows only those features that are categorized as reports and analysis features.|
|**Administration**|Shows only those features that are categorized as administration features.|



<!--
Choose the **Find** action at the top of the role explorer to quickly locate feature names that contain a certain term.

Choose the **Explore more roles** action at the top of the role explorer to get an overview of all business features that are available for all roles including your own.

> [!NOTE]
> Only Role Center actions for profiles where the **Show in Role Explorer** check box is selected will appear on the extended version of the role explorer (shown with the **Explore more roles** action). For more information, see [Manage Profiles](admin-users-profiles-roles.md).
-->

## <a name="expand-and-collapse-nodes-on-the-role-explorer"></a>Solmujen laajentaminen ja tiivistäminen roolienhallinnassa

Sivujen avoimet toiminnot on järjestetty ominaisuuksien tai sovellusalueiden mukaan nimetyille solmuille. Jokainen solmu voidaan tiivistää tai laajentaa yksittäin, ja voit tiivistää/laajentaa kaikki solmut yhteen.

- Jos haluat laajentaa tai supistaa solmun, valitse solmu. Tämä koskee ylimmän tason solmuja ja alisolmuja.
- Voit laajentaa tai kutistaa kaikki sivun ylätason solmut valitsemalla **Laajenna**- tai **Tiivistä** -toiminnon oikeasta yläkulmasta.
- Voit laajentaa/tiivistää kaikki ylimmän tason solmut ja niiden alla olevat alisolmut tekemällä jommankumman seuraavista toimista:
  - Paina Ctrl+Vaihto-näppäimiä samalla kun valitset **Laajenna** tai **Tiivistä**-toiminnon oikeassa yläkulmassa.
  - Valitse oikeassa yläkulmassa **...** ja valitse sitten **Laajenna kaikki**- tai **Tiivistä kaikki** -toiminto.

## <a name="see-also"></a>Katso myös
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Profiilien hallinta](admin-users-profiles-roles.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]