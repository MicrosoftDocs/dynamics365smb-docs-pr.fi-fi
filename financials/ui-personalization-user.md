---
title: Sivujen mukauttaminen Financialsissa | Microsoft Docs
description: "Lisätietoja käyttöliittymän mukauttamisesta omaan työskentelytapaan sopivaksi."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: daf2a1349cc3e12e634324082d4e6507c5b312be
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="personalizing-your-workspace"></a>Työtilan mukauttaminen
<!--NAV in the Web client-->
Voit *mukauttaa* työtilan työskentelyysi ja valintoihisi sopivaksi muuttamalla sivujen ulkoasua siten, että vain tarvitsemasi tiedot näkyvät siellä, missä niitä tarvitset. Mukauttamalla tehdyt muutokset koskevat vain omaa näkymääsi; muut käyttäjät eivät siis näe mukautuksiasi.

Sivun tyypin ja sen sisällön perusteella voit

-   lisätä, siirtää ja poistaa kenttiä
-   lisätä, siirtää ja poistaa luettelon sarakkeita
-   muuttaa luettelon sarakkeiden kiinnitysruutua. Kiinnitysruutu lukitsee vähintään yhden sarakkeen luettelon vasemmalle puolelle siten, että se näkyy myös silloin, kun näkymää vieritetään vaakasuunnassa.
-   siirtää ja poistaa jonoja (ruutuja)
-   siirtää ja poistaa osia. Osat ovat osia tai alueita sivulla ja niissä on esimerkiksi useita kenttiä, toinen sivu, kaavio tai ruutuja.  

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
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttökokemuksen mukauttaminen](ui-experiences.md)  

