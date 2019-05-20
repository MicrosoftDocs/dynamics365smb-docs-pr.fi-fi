---
title: Sivujen mukauttaminen | Microsoft Docs
description: Lisätietoja käyttöliittymän mukauttamisesta omaan Business Centralin käyttötapaan sopivaksi.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 16f334548d9831507970a1b74ba5fa1716611380
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253721"
---
# <a name="personalizing-your-workspace"></a>Työtilan mukauttaminen

Voit *mukauttaa* työtilan työskentelyysi ja valintoihisi sopivaksi muuttamalla sivujen ulkoasua siten, että vain tarvitsemasi tiedot näkyvät siellä, missä niitä tarvitset. Mukauttamalla tehdyt muutokset koskevat vain omaa näkymääsi; muut käyttäjät eivät siis näe mukautuksiasi.

Sivun tyypin ja sen sisällön mukaan voit tehdä erilaisia asioita, kuten siirtää tai piilottaa kenttiä, sarakkeita ja toimintoja sekä siirtää ja piilottaa kokonaisia osia.
<!--
-   Add, move, and remove fields.
-   Add, move, and remove columns in a list.
-   Change the freeze pane of columns in a list. The freeze pane locks one or more columns to the left side of a list so that are always present, even when you scroll horizontally.
-   Adjust the width of columns in a list.
-   Move and remove Cues (tiles).
-   Move and remove parts. Parts are subdivisions or areas on a page that contain things like multiple fields, another page, a chart, or tiles.

-->
> [!NOTE]
> Sen lisäksi mitä käyttäjät voivat mukauttaa, järjestelmänvalvojat ja superkäyttäjät voivat ohittaa käyttäjien mukauttamiset ja määrittää, mitä ominaisuuksia kaikki tai tietyt yritykset voivat käyttää. Lisätietoja on kohdassa [Business Centralin mukauttaminen](ui-customizing-overview.md).

## <a name="to-personalize-a-page"></a>Sivun mukauttaminen

1. Valitse oikeassa yläkulmassa ensin ![Asetukset](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") -kuvake ja sitten **Mukauta**.

    **Mukautetaan**-palkki tulee yläreunaan osoittamaan, että voit aloittaa muutosten tekemisen.

    ![Mukautustila](media/ui_personalize_mode_small.png "Mukautustila")

2. Siirry mukautettavalle sivulle.

    Jos palkissa näkyy ![Mukautuksen lukitus](media/personalization-lock-icon.png "Mukautuksen lukitus") tai ![Mukautuksen esto](media/personalization-blocked-icon.png "Mukautuksen esto"), et voi mukauttaa sivua. Lisätietoja on kohdassa [Syitä, miksi sivun mukauttaminen ei onnistu](ui-personalization-locked.md).

3. Osoita mukautettavaa aluetta, kuten kenttää tai sarakkeen otsikkoa luettelossa. Mukautettavat kohdat osoitetaan joko nuolella tai reunuksilla. [Seuraavassa osassa](#What) on tietoja siitä, mitä voit tehdä.

4. Voit jatkaa muutosten tekemistä samalla sivulla tai avata toisen sivun. Muutokset tallennetaan automaattisesti samalla, kun niitä tehdään. Kun olet valmis, valitse **Mukautetaan**-palkissa **Valmis**.

## <a name="What"></a>Mukautettavat toimet

|Tehtävä toimi|Ohjeet|Huomautukset|
|----|------------|-------|
|Esimerkiksi kentän, luettelon sarakkeen, ruudun, toiminnon tai osan siirtäminen|Osoita siirron kohdetta ja vedä se uuteen sijaintiin. Sijainti osoitetaan paksulla vaaka- tai pystyviivalla.<br /><br />![Siirto ei ole sallittu -kuvake](media/personalization-cannot-move-here.png "Mukautustila – Siirto ei ole sallittu -kuvake") ilmaisee, että elementtiä ei voi siirtää valittuun sijaintiin.|Osat ovat osia tai alueita sivulla ja niissä on esimerkiksi useita kenttiä, toinen sivu, kaavio tai ruutuja.<br /><br />Lisätietoja toimen mukauttamisesta on [seuraavassa osassa](ui-personalization-user.md#Actions). |
|Esimerkiksi kentän, luettelon sarakkeen, ruudun tai osan piilottaminen|Valitse ensin nuolenpää ja sitten <b>Piilota</b>.|Jos piilottamasi kenttä näkyy myös kutistetun pikavälilehden otsikossa, kenttä ei enää näy tässä kohdassa.|
|Kentän tai sarakkeen lisääminen|Valitse <b>Mukautetaan</b>-palkissa ensin <b>Lisää</b> ja sitten <b>Kenttä</b>.<br /></br><b>Lisää kenttä sivulle</b> -ruutu avautuu näytössä oikealla. Siinä on luettelo sivulle lisättävistä kentistä.<br /><br />Lisää kenttä vetämällä se ruudusta haluamaasi sijaintiin. Sijainti osoitetaan paksulla vaaka- tai pystyviivalla.|Kullakin sivulla on valmiiksi määritetty joukko näytettäviä kenttiä. Voit lisätä tällä tavalla kenttiä tai sarakkeita, joita ei ole aiemmin näytetty, tai näyttää piilotettuja kenttiä.|
|Kentän näyttäminen kutistetun pikavälilehden otsikossa|Valitse ensin nuolenpää ja sitten <b>Näytä, kun tiivistetty</b>. <br /> <br />Jos tämä vaihtoehto ei näy, se on jo määritetty. Valitse tässä tapauksessa <b>Näytä aina</b>, jos haluat, että kenttä ei enää näy pikavälilehden otsikossa.|*Pikavälilehdellä* tarkoitetaan kenttiä, jotka on ryhmitetty yhteisen otsikon alle. Tärkeimmät kentät näkyvät, kun valitset <b>Näytä, kun tiivistetty</b>. Jos valitset otsikossa olevan kentän, pikavälilehti avautuu ja kohdistus on valitussa kentässä.<br /><br />Tämä vaihtoehto on käytettävissä vain, jos sivulla on useita pikavälilehtiä. Jos pikavälilehtiä on vain yksi, sitä ei voi tiivistää, joten <b>Näytä, kun tiivistetty</b> -vaihtoehto ei ole käytettävissä.|
|Kentän näyttäminen vain, kun **Näytä enemmän** on valittu|Valitse ensin nuolenpää ja sitten <b>Näytä kohdassa Näytä lisää</b>. <br /> <br />Jos <b>Näytä kohdassa Näytä lisää</b> -vaihtoehto ei ole näkyvissä, se on jo määritetty. Tällöin saat näkyviin aina, eikä vain, kun valitset-kentän **Näytä useita**, valitse <b>Näytä aina</b>.||
|Kiinnitysruudun muuttaminen toiseen sarakkeeseen luettelossa |Valitse sen sarakkeen nuolenpää, jonka haluat olevan kiinnitysruudun viimeinen sarake, ja valitse sitten <b>Määritä kiinnitysruutu</b>.<br /><br/>Jos haluat määrittää kiinnitysruudun takaiseen alkuperäiseen sijaintiin, valitse ensin nykyisen kiinnitysruutusarakkeen nuolenpää ja sitten <b>Tyhjennä kiinnitysruutu</b>. Huomautus: Et voi poistaa tätä kiinnitysruutua.|Kiinnitysruutu määrittää aina vasemmalla puolella näkyvät sarakkeet; nämä sarakkeet näkyvät myös vaakasuoraan vieritettäessä.|  
|Sarakkeen leveyden muuttaminen|Vedä sarakkeen oikeaa reunaa taulukon otsikkorivillä. <br /><br />Voit suurentaa sarakkeen leveyttä niin, että se on sarakkeen pisimmän rivin pituinen, kun kaksoisnapsautat oikeaa reunaa.||
|Kentän ohittaminen Enter-näppäintä painettaessa|Valitse ensin kentän vieressä oleva nuolenpää tai sarakkeen otsikko luettelossa ja valitse sitten **Sulje pois pikatapahtumasta**. <br /><br /> Jos tämä vaihtoehto ei ole näkyvissä, kenttä on jo määritetty ohitettavaksi. Voit siinä tapauksessa lopettaa kentän ohittamisen valitsemalla **Sisällytä pikatapahtumaan**. |Lisätietoja on kohdassa [Tietojen syöttämisen helpottaminen pikatapahtuman avulla](ui-enter-data.md#QuickEntry)|

## <a name="Actions"></a>Toimintojen mukauttaminen

Voit mukauttaa sivun yläreunan toimintoriviä, joka näkyy korostettuna seuraavassa kuvassa.

![Toimintorivin mukautus](media/personalize-action-bar.png "Toimintorivin mukautus")

Mukauttamisen avulla voit päättää, mitkä toiminnot näkyvät toimintorivillä ja missä ne näytetään. Voit näyttää, piilottaa tai siirtää yksittäisiä toimintoja tai toimintoryhmiä. Toimintoriviä mukautetaan käytännössä samalla tavoin kuin muita työtilan elementtejä. Se, mitä kullekin toiminnolle tai ryhmälle voi tehdä, määräytyy sen mukaan, missä toiminto tai ryhmä on toimintorivillä. Kätevimmin asian voi selvittää kokeilemalla ja noudattamalla näytön ohjeita. Seuraavissa osissa käsitellä muutamia toimintorivin mukauttamiseen liittyviä seikkoja.

### <a name="action-bar-overview"></a>Toimintorivin yleiskuvaus

Toiminnon mukauttamista helpottaa, kun tiedät, mitä muutama termi tarkoittaa. Nämä termit ovat *toimintoryhmä* ja *ylätasolle siirretty luokka*.  

*Toimintoryhmä* voidaan laajentaa näyttämään muita toimintoja tai ryhmiä. Esimerkiksi seuraavassa kuvassa **Kirjaus** on toimintoryhmä.

*Ylätasolle siirretty luokka* on toimintoryhmä, joka näkyy kahden pystyviivan (`|`) välissä toimintorivillä. Luokat sisältävät yleensä eniten käytetyt toiminnot, jotta ne löytyvät nopeasti. Esimerkiksi seuraavassa kuvassa **Vapauta**, **Kirjaus**, **Lasku** ja **Navigoi** ovat ylätasolle siirrettyjä luokkia.

![Toimintorivin ryhmän mukautus](media/personalize-action-bar-group-clip.png "Toimintorivin ryhmän mukautus")

### <a name="to-remove-hide-and-show-actions-and-groups"></a>Toimintojen ja ryhmien poistaminen, piilottaminen ja näyttäminen

Valitse ensin näytettävä tai piilotettava toiminto tai toimintoryhmä ja sitten jokin seuraavista vaihtoehdoista:

|Asetus|Kuvaus|
|------|------------
|**Poista**|Tämä vaihtoehto näkyy, jos valittu toiminto näkyy myös jossain muualla toimintorivillä. Tämän vaihtoehdon valitseminen poistaa toiminnon valitusta sijainnista siten, ettei se enää näy. Toiminto tai toimintoryhmä näkyy edelleen toisissa sijainneissa. |
|**Piilota**|Tämä vaihtoehto näkyy, jos toiminto tai toimintoryhmä ei sijaitse muualla toimintorivillä. **Poista**-vaihtoehdon tavoin myös tämä vaihtoehto poistaa toiminnon tai toimintoryhmän näkyvistä toimintorivillä. Toiminto tai toimintoryhmä näkyy kuitenkin mukauttamistilassa nykyisessä sijainnissa – himmennettynä.|
|**Näytä**|Tämä vaihtoehto näkyy, jos toiminto tai toimintoryhmä on piilotettu aiemmin (näkyy himmennettynä). Kun tämä vaihtoehto valitaan, toiminto tai toimintoryhmä tulee näkyviin toimintorivillä.|

### <a name="to-move-actions-and-action-groups"></a>Toimintojen tai toimintoryhmien siirtäminen

Voit siirtää toiminnon tai toimintoryhmä vetämällä ja pudottamalla sen toivottuun sijaintiin samalla tavoin kuin kentät ja sarakkeet.

Toimintojen välinen vaakaviiva tai toimintoryhmää ympäröivä reunus ilmaisee, mihin voit pudottaa toimintoja ja toimintoryhmiä.

- Vaikka voit siirtää yksittäisiä toimintoja ylätasolle siirrettyihin luokkiin, et voi muuttaa toimintojen järjestystä luokan sisällä.
- Et voi siirtää toimintoryhmää ylätasolle siirrettyyn luokkaan.
- Voit siirtää toiminnon tai toimintoryhmän toiseen, tyhjään toimintoryhmään vetämällä toiminnon tai toimintoryhmän uuteen ryhmään ja pudottamalla sen **Pudota toiminto tähän** -ruutuun.

## <a name="additional-points-of-interest"></a>Muita kiinnostavia seikkoja

Seuraavat seikat auttavat ymmärtämään mukauttamista entistä paremmin.

- Kun teet muutoksia luettelosta avautuvalle korttisivulle, muutokset koskevat kaikki kyseisestä luettelosta avattavia tietueita. Oletetaan esimerkiksi, että avaat tietyn asiakkaan Asiakasluettelo-sivulta ja mukautat sivua lisäämällä siihen kentän. Kun avaat luettelossa muita asiakkaita, myös lisäämäsi kenttä on näkyvissä.
- Tekemäsi muutokset koskevat kaikkia roolikeskuksia. Jos esimerkiksi teet muutoksen asiakasluetteloon, kun roolikeskuksen asetuksena on Liiketoimintajohtaja, asiakasluettelon muutos näkyy myös roolikeskuksessa, jonka asetuksena on Myyntitilausten käsittelijä.
- Ruudun sivulla tehdyt muutokset koskevat sivua kaikissa tilanteissa, joissa se näytetään.  
- Voit lisätä kenttiä ja sarakkeita vain kyseiseen sivuun perustuvasta ennaltamääritetystä luettelosta. Uusia kenttiä tai sarakkeita ei voi luoda.

## <a name="to-clear-personalization"></a>Mukautuksen tyhjentäminen

Haluat ehkä joissain vaiheessa kumota osan sivulle aiemmin tehdyistä mukautusmuutoksista tai kaikki muutokset. Voit tehdä sen valitsemalla **Mukautetaan**-palkissa ensin **Lisää**, sitten **Tyhjennä mukautus** ja valitsemalla lopuksi jonkin seuraavista vaihtoehdoista. Muista, että mukautuksen tyhjentämistä ei voi kumota.

|Asetus|Kuvaus|
|------|------------
|Vain toiminnot|Tyhjentää kaikki sivun toimintorivin toimintoihin aiemmin tehdyt mukautusmuutokset.|
|Kaikki paitsi toiminnot|Tyhjentää kaikki muut sivun toimintoihin aiemmin tehdyt mukautusmuutokset paitsi toimintorivin muutokset. Tämä sisältää kaikki kenttiin, sarakkeisiin, osiin ja ruutuihin tehdyt muutokset. |
|Kaikki|Tyhjentää kaikki sivulle tehdyt mukautusmuutokset, joten palautetaan alkuperäiseen ulkoasuunsa. Tämä sisältää kaikki toimintoriviin kenttiin, sarakkeisiin, osiin ja ruutuihin tehdyt muutokset.|

## <a name="see-also"></a>Katso myös

[Mukautuksen hallinta](ui-personalization-manage.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
