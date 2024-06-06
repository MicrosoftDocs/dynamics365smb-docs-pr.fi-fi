---
title: Roolin mukainen sivuihin tutustuminen ja niissä siirtyminen
description: Roolien hallinnan avulla saat yleiskuvan kaikista roolin käytössä olevista liiketoimintaominaisuuksista ja muiden roolien toiminnoista.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'role explorer, find features, navigate'
ms.search.form: 'RoleExplorer, 9020, 9022, 9027, 9024'
ms.date: 08/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# <a name="finding-pages-and-reports-with-the-role-explorer"></a>Sivujen ja raporttien etsiminen roolienhallinnan avulla

Saat yleiskuvan kaikista roolin käytössä olevista liiketoimintaominaisuuksista ja muiden roolien toiminnoista, jos siirryt yhden vaiheen eteenpäin. Tässä artikkelissa ominaisuutta kutsutaan *roolienhallinnaksi*.

Jokainen roolienhallinnan elementti on sivun tai raportin avaava toiminto. Niinpä voitkin siirtyä [!INCLUDE[prod_short](includes/prod_short.md)]issa roolienhallinnan avulla.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="open-the-role-explorer"></a>Avaa roolien hallinta

Voit avata roolienhallinnan roolikeskuksesta ja kaikilta luettelosivuilta sekä **Kerro, mitä haluat tehdä** -ikkunasta.

- Valitse roolikeskuksessa tai millä tahansa luettelosivulla ![Valikko-painike.](media/ui_menu_button.png "Valikko-painike") -painike siirtymispalkin oikealla puolella tai paina näppäinyhdistelmä <kbd>Vaihto</kbd>+<kbd>F12</kbd>.
- Valitse **Kerro, mitä haluat tehdä** -ikkunassa alareunassa oleva **tutustumistoiminto**.

Kun avaat roolikeskuksen ensimmäisen kerran, siinä näkyvät useimpien roolisi käytettävissä olevien toimintojen linkit.

## <a name="open-the-role-explorer-filtered-to-show-reports"></a>Raporttien näyttämiseen suodatetun roolienhallinnan avaaminen

Voit avata roolienhallinnan näkymässä, joka on suodatettu näyttämään roolikeskuksen ja kaikkien luettelosivujen sekä **Kerro, mitä haluat tehdä** -ikkunan raportit.

- Valitse roolikeskuksessa tai luettelosivulla **Kaikki raportit** -linkin siirtymispalkin oikealla puolella.
- Valitse **Kerro, mitä haluat tehdä** -ikkunan alareunassa **raporttien tutustumistoiminto**.

## <a name="navigate-features"></a>Navigoi ominaisuuksia

Sivujen tai raporttien avoimet toiminnot on järjestetty ominaisuuksien tai sovellusalueiden mukaan nimetyille solmuille. Kukin solmu voidaan tiivistää tai laajentaa yksittäin taikka kaikki solmut yhdessä.

- Jos haluat laajentaa tai supistaa yksittäisen solmun, valitse solmu. Tämä koskee ylimmän tason solmuja ja alisolmuja.
- Jos haluat laajentaa tai kutistaa kaikki sivun ylätason solmut, mutta jättää alisolmut sellaisiksi kuin ne ovat, valitse ylhäällä **...** ja valitse sitten **Laajenna** tai **Tiivistä**.
- Jos haluat laajentaa tai kutistaa kaikki sivun ylätason solmut ja alisolmut, valitse ylhäällä **...** ja valitse sitten **Laajenna kaikki** tai **Tiivistä kaikki**.

## <a name="search-for-features"></a>Etsi ominaisuuksia

Voit etsiä ominaisuuksia nopeasti valitsemalla **Etsi** ja kirjoittamalla sanan tai lauseen etsimääsi ominaisuutta varten. Roolikeskus tuo esiin mahdollisen vastaavan tekstin. Jos ominaisuus on piilossa tiivistetyssä solmussa, tiivistetty solmu merkitään pisteellä. 

## <a name="explore-other-roles"></a>Tutki muita rooleja

Jos haluat tutkia muita rooleja kuin omia rooleja, valitse **Tutki lisää rooleja**. Roolikeskus näyttää jokaisen roolin oman otsikon alla, ja siinä on linkit sen ominaisuuksiin. Voit sitten etsiä ominaisuuksia ja siirtyä niihin oman roolin tavoin.

> [!NOTE]
> Vain niitä rooleja voidaan käyttää, jotka on määritetty näkymään roolinhallinnassa. Jos rooli ei ole käytettävissä, sitä ei todennäköisesti ole määritetty nähtäväksi. Lisätietoja on kohdassa [Profiilien hallinta](admin-users-profiles-roles.md). 

Kun tutustut muihin rooleihin, voit rajata etsintää myös roolikeskuksen yläosassa olevien **Raportti ja analyysi**- ja **Hallinta**-toimintojen avulla.

- **Raportti ja analyysi** näyttää vain ne ominaisuudet, jotka on luokiteltu raportti- ja analyysiominaisuuksina.
- **Hallinta**-ikkunassa näkyvät vain ne ominaisuudet, jotka on luokiteltu hallintaominaisuuksiksi.

> [!TIP]
> Sovelluskehittäjille voit luokitella sivuja ja raportteja määrittämällä objektin AL-koodissa [UsageCategory-ominaisuuden](/dynamics365/business-central/dev-itpro/developer/properties/devenv-usagecategory-property).
<!--
 
## <a name="role-explorer-actions"></a>Role explorer actions

There a several actions along the top of the role explorer to help you locate features of your role and other roles.

|Action|Description|
|------|------|
|**All**|Shows all features that are related to the role.|
|**Find**|Lets you enter a word or phrase to quickly locate feature names that match.|
|**Explore more roles**|All business features that are available for all roles including your own. When exploring all roles, the other actions work the same way, except for all roles shown. **NOTE:** You can only access roles that are set up to show in role explorer. For more information, see [Manage Profiles](admin-users-profiles-roles.md).  |
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
  - Paina <kbd>Ctrl</kbd>+<kbd>Vaihto</kbd>-näppäimiä samalla kun valitset **Laajenna** tai **Tiivistä**-toiminnon oikeassa yläkulmassa.
  - Valitse oikeassa yläkulmassa **...** ja valitse sitten **Laajenna kaikki**- tai **Tiivistä kaikki** -toiminto.

## <a name="see-also"></a>Katso myös

[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Profiilien hallinta](admin-users-profiles-roles.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
