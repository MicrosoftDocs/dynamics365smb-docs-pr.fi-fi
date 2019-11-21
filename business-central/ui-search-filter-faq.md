---
title: Tietoja hakemisesta ja suodattamisesta Business Central -sovelluksessa
description: Vastaa hakemiseen ja suodattamiseen liittyviin usein kysyttyihin kysymyksiin.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont04
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 10/01/2019
ms.author: mikebc
ms.openlocfilehash: a0b5d48f5decbed87337e27145486a2884a6612d
ms.sourcegitcommit: 49309bdff9b680a35032b355fe97c565845dba15
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2695189"
---
# <a name="searching-and-filtering-faq"></a>Usein kysyttyjen kysymysten haku ja suodatus
Tässä artikkelissa on vastauksia hakemiseen ja suodattamiseen liittyviin yleisiin kysymyksiin.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Onko hakemisella ja suodattamisella eroa?
Kyllä.
- Hakeminen on yksinkertainen ja laaja toiminto. Se hakee tietueet, jotka sisältävät hakutekstin sivulla näkyvissä kentissä. Kirjainkoolla ei ole merkitystä.
- Suodattaminen on erittäin mukautuvaa ja sitä voidaan hyödyntää erityisissä kentissä, myös sellaisissa joita ei näy sivulla: se esittää tietuut tarkkoina, kirjainkoon huomioon ottavina osumina, mutta sitä voidaan myös säätää voimakkailla hakusymboleilla, -tunnuksilla ja -kaavoilla. Lisätietoja näiden tietojen käyttämisestä on kohdassa [Lajitteleminen, hakeminen ja suodattaminen](ui-enter-criteria-filters.md)

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Voiko hakemista ja suodattamista käyttää näppäimistön avulla?
Hakemista ja suodattamista voi käyttää tehokkaasti myös ilman hiirtä. Käytettävissä on useita pikanäppäimiä, joiden avulla toimintoja voi käyttää nopeasti. Lisätietoja on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Onko suodatinruutu käytettävissä kaikissa luetteloissa?
Suodatinruutu on käytettävissä sivuilla, joissa luettelo on sivun ensisijainen sisältö. Tällaisia ovat esimerkiksi työkirjat ja luettelosivut, kuten siirtymispalkin avulla käytettävät luettelot. Suodatusruutu ei ole vielä tarjolla listoille jotka esitetään osina, kuten Tietoruudulle tai Roolikeskukselle. Kun listä on sisällytetty sivuun, kuten myyntirivi myyntitilauksessa, suodatusruutu on käytettävissä kun tämä rivi kohdistetaan kohdistustila painikkeella. Lisätietoja on kohdassa [Kohdistaminen rivinimikkeisiin](ui-enter-data.md#Focus).

## <a name="how-can-i-save-my-filters"></a>Miten voin tallentaa suodattimeni?
Suodattimet ja esimääritettyjen suodatinten muutokset jäävät muistiin istunnon ajaksi (kun olet kirjautuneena), vaikka siirtyisit pois sivulta. Voit tallentaa suodattimet pysyvästi nimettynä luettelonäkymänä valitsemalla suodatinruudussa ![Tallenna näkymä](media/save_view_icon.png "Tallenna näkymä") -kuvake. Lisätietoja on kohdassa [Luettelonäkymien usein kysytyt kysymykset](ui-views-faq.md). Huomaa, että suodattimista poiketen hakutekstiä ei muisteta, kun poistut sivulta, eikä sitä tallenneta, kun tallennat näkymän.

Voit lisäksi tallentaa suodattimia tai käyttää valmiiksi määritettyjä suodattimia raportin pyyntösivulla. Lisätietoja on kohdassa [Tallennettujen asetusten käyttäminen](ui-work-report.md#SavedSettings).

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Onko tämä samanlainen kuin Microsoft Dynamics NAV:n lisäsuodattimien ja kokonaisarvojen rajoituksen toiminto?
[!INCLUDE[d365fin](includes/d365fin_md.md)] muodostuu näistä suosituista toiminnoista. Sen avulla voi etsiä ja analysoida tietoja nykyaikaisella ja helposti käytettävällä tavalla. [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa on enemmän pikanäppäimiä kuin Dynamics NAV -sovelluksessa sekä haun esittely. Tämän vuoksi sen toiminnot ovat entistäkin parempia.  

## <a name="can-i-search-and-filter-using-the-companion-apps-and-outlook-addin"></a>Voinko hakea ja suodattaa kumppanin sovellusten ja Outlook-apuohjelman avulla?
Erilaisissa näyttökohteissa, kuten mobiililaitteissa tai Outlookissa, voit tehdä hakuja luetteloista mutta useimmiten yksittäisiä kenttiä ei voi suodattaa.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Laajentaako Microsoft suodatinruudun ominaisuuksia?
Microsoft saa jatkuvasti palautetta monipuoliselta käyttäjäyhteisöltä ja ottaa parhaat ehdotukset huomioon. Jos haluat laajentaa suodatinruudun useammille laitemuodoille ja luettelotyypeille tai jos sinulla on parannusehdotuksia, voit lisätä ne osoitteessa [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas). Siellä voit myös äänestää aiemmin tehtyjä ehdotuksia.

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Voinko tehdä jotain, jos näyttöön tulee Rivien hakeminen kestää liian kauan -sanoma?

Hakutoiminnon kestolle on määritetty aikaraja. Muuta ensin hakuehtoja ja tee haku uudelleen. Jos käytössä on paikallinen [!INCLUDE[prodshort](includes/prodshort.md)], ota yhteyttä järjestelmänvalvojaan. Hän voi muuttaa hakujen aikarajaa suuremmaksi.

Paikallinen järjestelmänvalvoja voi muuttaa hakujen aikarajaa suuremmaksi muuttamalla [!INCLUDE[prodshort](includes/prodshort.md)] -palvelimen **Haun aikakatkaisu** -asetusta. Lisätietoja on Business Central -sovelluksen kehittäjät ja IT-ammattilaiset -kohdan [Business Central Server -ratkaisun määrittäminen](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) -kohdassa.

## <a name="see-also"></a>Katso myös .
[Lajitteleminen, hakeminen ja suodattaminen](ui-enter-criteria-filters.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Sivujen etsiminen roolienhallinnan avulla](ui-role-explorer.md)  
[Käytön aloittaminen](product-get-started.md)  
