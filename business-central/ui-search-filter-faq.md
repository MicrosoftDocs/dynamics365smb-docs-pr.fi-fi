---
title: Tietoja hakemisesta ja suodattamisesta Business Central -sovelluksessa
description: Vastaa hakemiseen ja suodattamiseen liittyviin usein kysyttyihin kysymyksiin.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 10/01/2018
ms.author: mikebc
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b34acf29e142ef1a892f6c3c5a0ce2b6b8f7cb29
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---

# <a name="about-searching-and-filtering-in-included365finincludesd365finmdmd"></a>Tietoja hakemisesta ja suodattamisesta [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa
Tässä artikkelissa on vastauksia hakemiseen ja suodattamiseen liittyviin yleisiin kysymyksiin.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Onko hakemisella ja suodattamisella eroa?
Kyllä.
- Hakeminen on yksinkertainen ja laaja toiminto. Se hakee tietueet, jotka sisältävät hakutekstin sivulla näkyvissä kentissä. Kirjainkoolla ei ole merkitystä.
- Suodattaminen on erittäin joustava toiminto. Se voidaan kohdistaa tiettyihin kenttiin, myös kenttiin, jotka eivät näy sivulla. Se näyttää tietueet, joissa on täsmälleen haettu teksti (kirjainkoko otetaan huomioon). Suodattamista voi muokata tehokkailla hakusymboleilla, tunnuksilla ja kaavoilla. Lisätietoja näiden toimintojen käyttämisestä on kohdassa [Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen](ui-enter-criteria-filters.md)

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Voiko hakemista ja suodattamista käyttää näppäimistön avulla?
Hakemista ja suodattamista voi käyttää tehokkaasti myös ilman hiirtä. Käytettävissä on useita pikanäppäimiä, joiden avulla toimintoja voi käyttää nopeasti. Lisätietoja on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Onko suodatinruutu käytettävissä kaikissa luetteloissa?
Suodatinruutu on käytettävissä näytöissä, joissa luettelo on sivun ensisijainen sisältä. Tällaisia ovat esimerkiksi työkirjat ja luettelosivut, kuten siirtymispalkin avulla käytettävät luettelot. Suodatinruutu ei ole vielä käytettävissä upotetuissa luetteloissa, kuten myyntitilausten myyntiriveillä tai dynaamisten sarakkeiden luetteloissa (joita kutsutaan usein matriisisivuiksi). 

## <a name="how-can-i-save-my-filters"></a>Miten voin tallentaa suodattimeni?
Suodattimet ja esimääritettyjen suodatinten muutokset jäävät muistiin istunnon ajaksi (jolloin olet kirjautuneena), vaikka siirtyisit pois sivulta. Tällä hetkellä suodattimien tallentaminen pysyvästi ei ole mahdollista.
Toisin kuin suodattimet, hakutekstiä ei jää muistiin, kun siirryt pois sivulta.

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Onko tämä samanlainen kuin Microsoft Dynamics NAV:n lisäsuodattimien ja kokonaisarvojen rajoituksen toiminto?
[!INCLUDE[d365fin](includes/d365fin_md.md)] muodostuu näistä suosituista toiminnoista. Sen avulla voi etsiä ja analysoida tietoja nykyaikaisella ja helposti käytettävällä tavalla. [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa on enemmän pikanäppäimiä kuin Dynamics NAV -sovelluksessa sekä haun esittely. Tämän vuoksi sen toiminnot ovat entistäkin parempia.

## <a name="can-i-search-and-filter-using-the-companion-apps-and-outlook-addin"></a>Voinko hakea ja suodattaa kumppanin sovellusten ja Outlook-apuohjelman avulla?
Erilaisissa laitemuodoissa, kuten mobiililaitteissa, tai Outlookissa, voit tehdä hakuja luetteloista, mutta et useimmiten et suodattaa yksittäisiä kenttiä.

## <a name="is-the-filter-pane-available-for-filtering-reports"></a>Onko suodatinruutu käytettävissä raporttien suodattamista varten?
Ei. Raportin suodatuksen valintaikkuna, jota yleensä sanotaan pyyntösivuksi, on tällä hetkellä toiminnoiltaan erilainen. Se sisältää kuitenkin joitakin suodatinruudun ominaisuuksia.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Laajentaako Microsoft suodatinruudun ominaisuuksia?
Microsoft saa jatkuvasti palautetta monipuoliselta käyttäjäyhteisöltä ja ottaa parhaat ehdotukset huomioon. Jos haluat laajentaa suodatinruudun useammille laitemuodoille tai luettelo- ja raporttityypeille tai jos sinulla on parannusehdotuksia, voit lisätä ne osoitteessa [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas). Siellä voit myös antaa äänesi aiemmille ehdotuksille.

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Voinko tehdä jotain, jos näyttöön tulee Rivien hakeminen kestää liian kauan -sanoma?

Hakutoiminnon kestolle on määritetty aikaraja. Muuta ensin hakuehtoja ja tee haku uudelleen. Jos käytössä on paikallinen [!INCLUDE[prodshort](includes/prodshort.md)], ota yhteyttä järjestelmänvalvojaan. Hän voi muuttaa hakujen aikarajaa suuremmaksi.

Paikallinen järjestelmänvalvoja voi muuttaa hakujen aikarajaa suuremmaksi muuttamalla [!INCLUDE[prodshort](includes/prodshort.md)] -palvelimen **Haun aikakatkaisu** -asetusta. Lisätietoja on Business Central -sovelluksen kehittäjät ja IT-ammattilaiset -kohdan [Business Central Server -ratkaisun määrittäminen](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) -kohdassa.

## <a name="see-also"></a>Katso myös .
[Käytön aloittaminen](product-get-started.md)  
[Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen](ui-enter-criteria-filters.md)
