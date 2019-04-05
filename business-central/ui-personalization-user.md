---
title: Sivujen mukauttaminen | Microsoft Docs
description: Lisätietoja käyttöliittymän mukauttamisesta omaan työskentelytapaan sopivaksi.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: 65bd6d24395990d2b92b7eeea0c7b208f7311eef
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/19/2019
ms.locfileid: "852307"
---
# <a name="personalizing-your-workspace"></a>Työtilan mukauttaminen
<!--NAV in the Web client-->
Voit *mukauttaa* työtilan työskentelyysi ja valintoihisi sopivaksi muuttamalla sivujen ulkoasua siten, että vain tarvitsemasi tiedot näkyvät siellä, missä niitä tarvitset. Mukauttamalla tehdyt muutokset koskevat vain omaa näkymääsi; muut käyttäjät eivät siis näe mukautuksiasi.

Sivun tyypin ja sen sisällön perusteella voit

-   lisätä, siirtää ja poistaa kenttiä
-   lisätä, siirtää ja poistaa luettelon sarakkeita
-   muuttaa luettelon sarakkeiden kiinnitysruutua. Kiinnitysruutu lukitsee vähintään yhden sarakkeen luettelon vasemmalle puolelle siten, että se näkyy myös silloin, kun näkymää vieritetään vaakasuunnassa.
-   Muokkaa luettelon sarakkeiden leveyttä.
-   siirtää ja poistaa jonoja (ruutuja)
-   siirtää ja poistaa osia. Osat ovat osia tai alueita sivulla ja niissä on esimerkiksi useita kenttiä, toinen sivu, kaavio tai ruutuja.

> [!NOTE]
> Sen lisäksi mitä käyttäjät voivat mukauttaa, järjestelmänvalvojat ja superkäyttäjät voivat ohittaa käyttäjien mukautukset ja määrittää, mitä ominaisuuksia kaikki tai tietyt yritykset voivat käyttää. Lisätietoja on kohdassa [Business Centralin mukauttaminen](ui-customizing-overview.md). 

## <a name="to-personalize-a-page"></a>Sivun mukauttaminen

1. Valitse oikeassa yläkulmassa ensin ![Asetukset](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") -kuvake ja sitten **Mukauta**.

    **Mukautetaan**-palkki tulee yläreunaan osoittamaan, että voit aloittaa muutosten tekemisen.

    ![Mukautustila](media/ui_personalize_mode_small.png "Mukautustila")

2.  Siirry mukautettavalle sivulle.

    Jos palkissa on lukkokuvake, lisätietoja on kohdassa [Lukittu sivu](ui-personalization-locked.md).

3.  Osoita mukautettavaa aluetta, kuten kenttää tai sarakkeen otsikkoa luettelossa. Mukautettavat kohdat osoitetaan joko nuolella tai reunuksilla.
<!--
    -  If a component can be personalized, an arrow head (![Personalization indicator arrow left](media/ui_personalize_arrow_left.png "Personalization indicator arrow left") or ![Personalization indicator arrow down](media/ui_personalize_arrow_down.png "Personalization indicator arrow down")) appears.
    -   If the component is a part, the extent of the part is indicated by a border.
    -   The freeze pane in a list is indicated by a vertical line along the entire right-side of the last column of the freeze pane.
    -->

4.  Voit tehdä muutoksia tämän taulukon avulla:     <table>
        <tr><th>Tehtävä toimi</td><th>Ohjeet</th></tr>
        <tr><td>Esimerkiksi kentän, luettelon sarakkeen, ruudun tai osan siirtäminen</td><td> Osoita siirron kohdetta ja vedä se uuteen sijaintiin. Sijainti osoitetaan paksulla vaaka- tai pystyviivalla.</td></tr>
        <tr><td>Kohteen poistaminen</td><td>Valitse ensin nuolenpää ja sitten <b>Poista</b>. </td></tr>
        <tr><td>Kentän tai sarakkeen lisääminen</td><td>Valitse <b>Mukautetaan</b>-palkissa ensin <b>Lisää</b> ja sitten <b>Kenttä</b>.<br /></br><b>Lisää kenttä sivulle</b> -ruutu avautuu näytössä oikealla. Siinä on luettelo sivulle lisättävistä kentistä. Jos kentässä on merkintä <b>Sijoitettu</b>, kenttä on jo sivulla. Jos kentässä on merkintä <b>Valmis</b>, kenttä ei ole vielä sivulla.<br /></br>Lisää kenttä vetämällä se ruudusta haluamaasi sijaintiin. Sijainti osoitetaan paksulla vaaka- tai pystyviivalla.</td></tr>
        <tr><td>Kiinnitysruudun muuttaminen toiseen sarakkeeseen luettelossa</td><td>Valitse sen sarakkeen nuolenpää, jonka haluat olevan kiinnitysruudun viimeinen sarake, ja valitse sitten <b>Määritä kiinnitysruutu</b>.<br /><br/>Jos haluat määrittää kiinnitysruudun takaiseen alkuperäiseen sijaintiin, valitse ensin nykyisen kiinnitysruutusarakkeen nuolenpää ja sitten <b>Tyhjennä kiinnitysruutu</b>. Huomautus: Et voi poistaa tätä kiinnitysruutua.</td></tr>
        <tr><td>Sarakkeen leveyden muuttaminen</td><td>Vedä sarakkeen oikeaa reunaa taulukon otsikkorivillä. <br /><br />Voit suurentaa sarakkeen leveyttä niin, että se on sarakkeen pisimmän rivin pituinen, kun kaksoisnapsautat oikeaa reunaa.</td></tr>
      </table>

    > [!IMPORTANT]  
    >   Luetteloon ei voi tehdä muutoksia, jos luettelo näytetään ruutuina. Sivu on ensin vaihdettava luettelonäkymään valitsemalla ![Näytä luettelona](media/ui_show_as_list_icon.png "Vasen Näytä luettelona -nuoli") -kuvake.

5.  Voit jatkaa muutosten tekemistä samalla sivulla tai siirtyä toiselle sivulle. Muutokset tallennetaan automaattisesti samalla, kun niitä tehdään. Kun olet valmis, valitse **Mukautetaan**-palkissa **Valmis**.

## <a name="clear-personalization-to-change-a-page-back-to-its-original-layout"></a>Sivun palauttaminen alkuperäiseen asetteluun tyhjentämällä mukautukset
Haluat ehkä joissain vaiheessa kumota kaikki sivulle aiemmin tehdyt mukautusmuutokset ja palauttaa sivun alkuperäisen ulkoasun. Voit tehdä sen valitsemalla **Mukautetaan**-palkissa ensin **Lisää** ja sitten **Tyhjennä mukautus**.

## <a name="personalization-in-detail"></a>Lisätietoja mukauttamisesta
Seuraavat seikat auttavat ymmärtämään mukauttamista entistä paremmin.  
-   Kun teet muutoksia luettelosta avautuvalle korttisivulle, muutokset koskevat kaikki kyseisestä luettelosta avattavia tietueita. Oletetaan esimerkiksi, että avaat tietyn asiakkaan Asiakasluettelo-sivulta ja mukautat sivua lisäämällä siihen kentän. Kun avaat luettelossa muita asiakkaita, myös lisäämäsi kenttä on näkyvissä.
-   Tekemäsi muutokset koskevat kaikkia roolikeskuksia. Jos esimerkiksi teet muutoksen asiakasluetteloon, kun roolikeskuksen asetuksena on Liiketoimintajohtaja, asiakasluettelon muutos näkyy myös roolikeskuksessa, jonka asetuksena on Myyntitilausten käsittelijä.
-   Ruudun sivulla tehdyt muutokset koskevat sivua kaikissa tilanteissa, joissa se näytetään.  
-   Voit lisätä kenttiä ja sarakkeita vain kyseiseen sivuun perustuvasta ennaltamääritetystä luettelosta. Uusia kenttiä tai sarakkeita ei voi luoda.

## <a name="see-also"></a>Katso myös
[Mukautuksen hallinta](ui-personalization-manage.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
