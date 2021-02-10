---
title: Tietoja hakemisesta ja suodattamisesta Business Central -sovelluksessa
description: Vastaa hakemiseen ja suodattamiseen liittyviin usein kysyttyihin kysymyksiin.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont04
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 11/16/2020
ms.author: mikebc
ms.openlocfilehash: b993fd047db09b1dc412d9927168aa0233c057a6
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756715"
---
# <a name="searching-and-filtering-faq"></a>Usein kysyttyjen kysymysten haku ja suodatus
Tässä artikkelissa on vastauksia hakemiseen ja suodattamiseen liittyviin yleisiin kysymyksiin.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Onko hakemisella ja suodattamisella eroa?
Kyllä.
- Hakeminen on yksinkertainen ja laaja toiminto. Se hakee tietueet, jotka sisältävät hakutekstin sivulla näkyvissä kentissä. Kirjainkoolla ei ole merkitystä.
- Suodattaminen on erittäin mukautuvaa ja sitä voidaan hyödyntää erityisissä kentissä, myös sellaisissa joita ei näy sivulla: se esittää tietuut tarkkoina, kirjainkoon huomioon ottavina osumina, mutta sitä voidaan myös säätää voimakkailla hakusymboleilla, -tunnuksilla ja -kaavoilla. Lisätietoja näiden tietojen käyttämisestä on kohdassa [Lajitteleminen, hakeminen ja suodattaminen](ui-enter-criteria-filters.md)

## <a name="exactly-which-fields-are-matched-when-searching"></a>Mitkä kentät tarkalleen yhdistetään haun yhteydessä?
[!INCLUDE[prod_short](includes/prod_short.md)] käyttää hakuehtoja kaikissa sivulla näkyvissä kentissä. Jos kenttä on piilotettu, esimerkiksi käyttämällä mukautustoimintoa, haku ei ota tätä kenttää huomioon. Hakuehdot kohdistetaan kenttiin vain, jos niiden tietotyyppi vastaa hakuehtojen tietotyyppiä. Esimerkiksi hakutermillä *tänään* etsitään kaikkia teksti- ja koodikenttiä literaaliarvolle "tänään" ja myös sellaisia päivämääräkenttiä, joissa *tänään* on laskettu kuluvan päivän lausekkeena, mutta ei etsitä numeerisia kenttiä. Lisätietoja suodausehdoista on kohdassa [Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen](ui-enter-criteria-filters.md#-filter-criteria-and-operators).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Voiko hakemista ja suodattamista käyttää näppäimistön avulla?
Hakemista ja suodattamista voi käyttää tehokkaasti myös ilman hiirtä. Käytettävissä on useita pikanäppäimiä, joiden avulla toimintoja voi käyttää nopeasti. Lisätietoja on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Onko suodatinruutu käytettävissä kaikissa luetteloissa?
Suodatinruutu on käytettävissä sivuilla, joissa luettelo on sivun ensisijainen sisältö. Tällaisia ovat esimerkiksi työkirjat ja luettelosivut, kuten siirtymispalkin avulla käytettävät luettelot. Suodatinruutu ei ole vielä käytettävissä luetteloille, jotka näkyvät osina, kuten tietoruuduille tai roolikeskuksen osille, tai valintaikkunoina näytettäville luetteloille, kuten valinnoille. Kun listä on sisällytetty sivuun, kuten myyntirivi myyntitilauksessa, suodatusruutu on käytettävissä kun tämä rivi kohdistetaan kohdistustila painikkeella. Lisätietoja on kohdassa [Kohdistaminen rivinimikkeisiin](ui-enter-data.md#Focus).

## <a name="how-can-i-save-my-filters"></a>Miten voin tallentaa suodattimeni?
Suodattimet ja esimääritettyjen suodatinten muutokset jäävät muistiin istunnon ajaksi (kun olet kirjautuneena), vaikka siirtyisit pois sivulta. Voit tallentaa suodattimet pysyvästi nimettynä luettelonäkymänä valitsemalla suodatinruudussa ![Tallenna näkymä](media/save_view_icon.png "Tallenna näkymä") -kuvake. Lisätietoja on kohdassa [Luettelonäkymien usein kysytyt kysymykset](ui-views-faq.md). Huomaa, että suodattimista poiketen hakutekstiä ei muisteta, kun poistut sivulta, eikä sitä tallenneta, kun tallennat näkymän.

Voit lisäksi tallentaa suodattimia tai käyttää valmiiksi määritettyjä suodattimia raportin pyyntösivulla. Lisätietoja on kohdassa [Tallennettujen asetusten käyttäminen](ui-work-report.md#SavedSettings).

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Onko tämä samanlainen kuin Microsoft Dynamics NAV:n lisäsuodattimien ja kokonaisarvojen rajoituksen toiminto?
[!INCLUDE[prod_short](includes/prod_short.md)] muodostuu näistä suosituista toiminnoista. Sen avulla voi etsiä ja analysoida tietoja nykyaikaisella ja helposti käytettävällä tavalla. [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa on enemmän pikanäppäimiä kuin Dynamics NAV -sovelluksessa sekä haun esittely. Tämän vuoksi sen toiminnot ovat entistäkin parempia.  

## <a name="can-i-search-and-filter-using-the-companion-apps-and-add-ins-for-microsoft-365"></a>Voinko hakea ja suodattaa kumppanien sovellusten ja Microsoft 365 -laajennusten avulla?
Erilaisissa näyttökohteissa, kuten mobiililaitteissa tai Outlookissa, voit tehdä hakuja luetteloista mutta useimmiten yksittäisiä kenttiä ei voi suodattaa. Microsoft Teamsin  [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa sekä haku että suodatin ovat käytettävissä luetteloille.

## <a name="how-do-i-view-how-my-search-terms-have-been-applied-to-fields-in-the-list"></a>Miten voin tarkastella, miten hakutermejäni on käytetty luettelon kentissä?
Kun olet syöttänyt hakuehdot hakuuutuun, voit tarkastella tarkkoja hakuehtoja ja kenttiä, joihin ne on kohdistettu, avaamalla sivun tarkastusruudun ( **Ctrl + Alt + F1**) ja valitsemalla **Sivun suodattimet** -välilehden.

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Voinko tehdä jotain, jos näyttöön tulee Rivien hakeminen kestää liian kauan -sanoma?

Hakutoiminnon kestolle on määritetty aikaraja. Muuta ensin hakuehtoja ja tee haku uudelleen. Jos käytössä on paikallinen [!INCLUDE[prod_short](includes/prod_short.md)], ota yhteyttä järjestelmänvalvojaan. Hän voi muuttaa hakujen aikarajaa suuremmaksi.

Paikallinen järjestelmänvalvoja voi muuttaa hakujen aikarajaa suuremmaksi muuttamalla [!INCLUDE[prod_short](includes/prod_short.md)] -palvelimen **Haun aikakatkaisu** -asetusta. Lisätietoja on Business Central -sovelluksen kehittäjät ja IT-ammattilaiset -kohdan [Business Central Server -ratkaisun määrittäminen](/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) -kohdassa.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Laajentaako Microsoft suodatinruudun ominaisuuksia?
Microsoft saa jatkuvasti palautetta monipuoliselta käyttäjäyhteisöltä ja ottaa parhaat ehdotukset huomioon. Jos haluat laajentaa suodatinruudun useammille laitemuodoille ja luettelotyypeille tai jos sinulla on parannusehdotuksia, voit lisätä ne osoitteessa [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas). Siellä voit myös äänestää aiemmin tehtyjä ehdotuksia.

## <a name="see-also"></a>Katso myös .
[Lajitteleminen, hakeminen ja suodattaminen](ui-enter-criteria-filters.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Sivujen etsiminen roolienhallinnan avulla](ui-role-explorer.md)  
[Käytön aloittaminen](product-get-started.md)  
