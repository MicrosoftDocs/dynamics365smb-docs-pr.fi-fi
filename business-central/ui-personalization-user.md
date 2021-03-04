---
title: Sivujen mukauttaminen | Microsoft Docs
description: Lisätietoja käyttöliittymän mukauttamisesta omaan Business Centralin käyttötapaan sopivaksi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4b112bf05c1bbc6110ce3b5a439c81a96759d1bf
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756765"
---
# <a name="personalize-your-workspace"></a>Työtilan mukauttaminen
Voit mukauttaa työtilan työskentelyysi ja valintoihisi sopivaksi muuttamalla sivujen ulkoasua siten, että vain tarvitsemasi tiedot näkyvät siellä, missä niitä tarvitset. Mukauttamalla tehdyt muutokset koskevat vain omaa näkymääsi; muut käyttäjät eivät siis näe mukautuksiasi.

Voit mukauttaa kaikenlaisia sivuja, myös Roolikeskus-sivua. Lisätietoja roolikeskuksesta on kohdassa [Roolikeskus](ui-change-basic-settings.md#role-center).

Sivun tyypin ja sen sisällön mukaan voit tehdä erilaisia muutoksia, kuten siirtää tai piilottaa kenttiä, sarakkeita, toimintoja ja kokonaisia osia sekä lisätä uusia kenttiä. Vaikka useimmat mukautukset on tehtävä aktivoimalla ensin **Mukauttaminen**-palkki, yksinkertaiset muutokset, kuten sarakkeen leveyden muuttaminen, voidaan tehdä suoraan luettelossa.

> [!NOTE]
> Järjestelmänvalvojat voivat tehdä samat asettelun muutokset kuin käyttäjät mukauttamalla sellaisen profiilin työtilaa, johon on määritetty useita käyttäjiä. Lisätietoja on kohdassa [Roolien sivujen mukauttaminen](ui-personalization-manage.md).<br /><br />
Järjestelmänvalvojat voivat myös ohittaa käyttäjien mukauttamiset tai poistaa ne käytöstä sekä määrittää, mitkä ominaisuudet käyttäjät näkevät kaikissa tai tietyissä yrityksissä. Lisätietoja on kohdassa [Business Centralin mukauttaminen](ui-customizing-overview.md).

## <a name="video-overview"></a>Videon yleiskuvaus
Seuraava video näyttää joitakin tapoja, joilla voit mukauttaa roolikeskuksesi.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## <a name="to-change-the-width-of-a-column"></a>Sarakkeen leveyden muuttaminen
Luettelon sarakkeiden kokoa on helppo muuttaa vetämällä kahden sarakkeen rajaa vasemmalle tai oikealle.
1. Valitse ja vedä sarakkeiden välissä olevaa rajaa luettelon otsikossa.
2. Voit vaihtoehtoisesti kaksoisnapsauttaa kahden sarakkeen rajaa, jolloin sarakkeen leveys sovitetaan automaattisesti. Leveys määritetään tällä tavoin luettavuuden kannalta optimaaliseksi.

Muiden mukautusten tavoin sarakkeen leveyteen tehdyt muutokset tallennetaan tiliin, ja ne ovat käytettävissä riippumatta siitä, millä laitetta käytetään kirjautumiseen.

## <a name="to-start-personalizing-a-page-through-the-personalizing-banner"></a>Sivun mukauttamisen aloittaminen **Mukauttaminen**-palkin avulla
1. Avaa mukautettava sivu.
2. Valitse oikeassa yläkulmassa ![Asetukset](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake")-kuvake, ja valitse sen jälkeen **Mukauta**-toiminto.

    **Mukautetaan**-palkki tulee yläreunaan osoittamaan, että voit aloittaa muutosten tekemisen.

    > [!NOTE]
    > Voit siirtyä mukauttamisen aikana käyttämällä toiminnossa CTRL+napsautus-yhdistelmää, jos nuolenpää osoittaa toiminnon olevan valittuna.

    Jos näet palkissa ![Mukautuksen lukitus](media/personalization-lock-icon.png "Mukautuksen lukitus") - tai ![Mukautus estetty](media/personalization-blocked-icon.png "Mukauttaminen estetty") -ilmoituksen, et voi mukauttaa sivua. Lisätietoja on kohdassa [Sivun mukauttamisen estäminen lukitsemalla](ui-personalization-locked.md).

3. Lisää kenttä valitsemalla **+ Kenttä** -toiminto.
4. Vedä ja pudota kenttä **Lisää kenttä sivulle** -ruudusta sopivaan paikkaan sivulla.
5. Voit muuttaa käyttöliittymän elementtiä osoittamalla elementtiä, kuten toimintoa, kenttää tai osaa. Elementti valitaan, minkä osoituksena on nuolenpää tai raja.
6. Valitse ensin elementti ja sitten joko **Siirrä**, **Poista**, **Piilota**, **Näytä**, **Näytä kohdassa ”Näytä lisää”**, **Näytä, kun tiivistetty**, **Näytä aina**, **Määritä tai tyhjennä kiinnitysruutu** tai **Sisällytä pikatapahtumaan tai Sulje pois pikatapahtumasta** käyttöliittymäelementin tyypin ja tilan mukaan. Lisätietoja on kohdassa [Mukautettavat toimet](#What).
7. Kun olet muuttanut yhden tai usean sivun asettelua, valitse **Mukauttaminen**-palkissa **Valmis**-painike.

## <a name="what-you-can-personalize"></a><a name="What"></a>Mukautettavat toimet

|Tehtävä toimi|Ohjeet|Huomautukset|
|----|------------|-------|
|Esimerkiksi kentän, luettelon sarakkeen, ruudun, toiminnon tai osan siirtäminen|Osoita siirron kohdetta ja vedä se uuteen paikkaan. Paikka osoitetaan paksulla vaaka- tai pystyviivalla.<br /><br />![Et voi siirtää tänne -kuvake](media/personalization-cannot-move-here.png "Personalisointitila - Ei voi siirtää tähän -kuvake") osoittaa, että et voi siirtää elementtiä valittuun sijaintiin.|Osat ovat osia tai alueita sivulla ja niissä on esimerkiksi useita kenttiä, toinen sivu, kaavio tai ruutuja.<br /><br />Lisätietoja toiminnon mukauttamisesta on kohdassa [Toimintojen mukauttaminen](ui-personalization-user.md#Actions). |
|Esimerkiksi kentän, luettelon sarakkeen, ruudun, toiminnon tai osan piilottaminen|Valitse ensin nuolenpää ja sitten <b>Piilota</b>.|Elementti näkyy harmaana, kun olet mukautustilassa. Jos piilottamasi kenttä näkyy myös tiivistetyn pikavälilehden otsikossa, kenttä ei enää näy tässä kohdassa.|
|Piilotettujen toimintojen ja osien näyttäminen.|Valitse ensin harmaan (piilotetun) elementin nuolenpää ja sitten <b>Näytä</b>.|Piilotettu elementti on taas näkyvissä.|
|Kentän tai sarakkeen lisääminen|Valitse <b>Mukauttaminen</b>-palkissa <b>+ Kenttä</b>-toiminto.<br /></br><b>Lisää kenttä sivulle</b> -ruutu avautuu näytössä oikealla. Siinä on luettelo sivulle lisättävistä kentistä.<br /><br />Lisää kenttä vetämällä se ruudusta haluamaasi paikkaa. Paikka osoitetaan paksulla vaaka- tai pystyviivalla.|Kullakin sivulla on valmiiksi määritetty joukko näytettäviä kenttiä. Voit lisätä tällä tavalla kenttiä tai sarakkeita, joita ei ole aiemmin näytetty, tai näyttää piilotettuja kenttiä.|
|Kentän näyttäminen kutistetun pikavälilehden otsikossa|Valitse ensin nuolenpää ja sitten <b>Näytä, kun tiivistetty</b>. <br /> <br />Jos tämä vaihtoehto ei näy, se on jo määritetty. Valitse tässä tapauksessa <b>Näytä aina</b>, jos haluat, että kenttä ei enää näy pikavälilehden otsikossa.|*Pikavälilehdellä* tarkoitetaan kenttiä, jotka on ryhmitetty yhteisen otsikon alle. Tärkeimmät kentät näkyvät, kun valitset <b>Näytä, kun tiivistetty</b>. Jos valitset otsikossa olevan kentän, pikavälilehti avautuu ja kohdistus on valitussa kentässä.<br /><br />Tämä vaihtoehto on käytettävissä vain, jos sivulla on useita pikavälilehtiä. Jos pikavälilehtiä on vain yksi, sitä ei voi tiivistää, joten <b>Näytä, kun tiivistetty</b> -vaihtoehto ei ole käytettävissä.|
|Kentän näyttäminen vain, kun **Näytä enemmän** on valittu|Valitse ensin nuolenpää ja sitten <b>Näytä kohdassa Näytä lisää</b>. <br /> <br />Jos <b>Näytä kohdassa Näytä lisää</b> -vaihtoehto ei ole näkyvissä, se on jo määritetty. Tällöin saat näkyviin aina, eikä vain, kun valitset-kentän **Näytä useita**, valitse <b>Näytä aina</b>.||
|Kiinnitysruudun muuttaminen toiseen sarakkeeseen luettelossa |Valitse sen sarakkeen nuolenpää, jonka haluat olevan kiinnitysruudun viimeinen sarake, ja valitse sitten <b>Määritä kiinnitysruutu</b>.<br /><br/>Jos haluat määrittää kiinnitysruudun takaiseen alkuperäiseen paikkaan, valitse ensin nykyisen kiinnitysruutusarakkeen nuolenpää ja sitten <b>Tyhjennä kiinnitysruutu</b>. Huomautus: Et voi poistaa tätä kiinnitysruutua.|Kiinnitysruutu määrittää aina vasemmalla puolella näkyvät sarakkeet; nämä sarakkeet näkyvät myös vaakasuoraan vieritettäessä.|  
|Kentän ohittaminen Enter-näppäintä painettaessa|Valitse ensin kentän vieressä oleva nuolenpää tai sarakkeen otsikko luettelossa ja valitse sitten **Sulje pois pikatapahtumasta**. <br /><br /> Jos tämä vaihtoehto ei ole näkyvissä, kenttä on jo määritetty ohitettavaksi. Voit siinä tapauksessa lopettaa kentän ohittamisen valitsemalla **Sisällytä pikatapahtumaan**. |Lisätietoja on kohdassa [Tietojen syöttämisen helpottaminen pikatapahtuman avulla](ui-enter-data.md#QuickEntry)|
|Suodatettuja luetteloita vastaavien näkymien järjestäminen uudelleen ja poistaminen|Valitse ensin näkymän vieressä oleva nuolenpää ja sitten **Siirrä**, **Poista** tai **Piilota**.|Katso [Luettelonäkymien tallentaminen ja mukauttaminen](ui-views.md)|  
|Lisää uusi toiminto roolikeskuksen sivuun tai raporttiin.|Valitse kohdesivu-, raportin pyyntösivu- tai Ilmoita-ikkunassa kirjanmerkkikuvake.|Katso [Sivun tai raportin kirjanmerkin luominen roolikeskuksessa](ui-bookmarks.md)|
|Aloita luettelo aina laajennettuna tai tiivistettynä|Valitse luettelon vasemmassa yläkulmassa oleva Laajenna kaikki- tai Tiivistä kaikki -painike tai valitse Laajenna kaikki- tai Tiivistä kaikki -toiminto ensimmäisen sarakkeen valikosta. |Koskee tiivistettäviä hierarkialuetteloita|

## <a name="personalizing-actions"></a><a name="Actions"></a>Toimintojen mukauttaminen

Mukauttamisen avulla voit päättää, mitkä toiminnot näkyvät siirtymispalkissa, toimintoriveillä ja roolikeskuksissa sekä muissa kohdissa, joissa niiden halutaan näkyvän. Voit näyttää, piilottaa tai siirtää yksittäisiä toimintoja tai toimintoryhmiä. Siirtymispalkkia ja toimintorivejä mukautetaan käytännössä samalla tavoin kuin muita käyttöliittymän elementtejä. Se, mitä kullekin toiminnolle tai ryhmälle voi tehdä, määräytyy sen mukaan, missä toiminto tai ryhmä on. Kätevimmin asian voi selvittää siirtymällä mukautustilaan ja toimimalla sitten ohjenuolien mukaan.

Toiminnon mukauttamista helpottaa, kun tiedät, mitä muutama termi tarkoittaa. Nämä termit ovat *toimintoryhmä* ja *ylätasolle siirretty luokka*.  

*Toimintoryhmä* on elementti, joka voidaan laajentaa näyttämään muita toimintoja tai ryhmiä. Esimerkiksi **Myyntitilaukset**-sivulla **Toiminnot**-toiminto tulee näkyviin, kun valitset **Toiminnot**-toiminnon toimintoryhmissä.

*Ylätasolle siirretty luokka* on toimintoryhmä, joka näkyy ennen pystyviivaa `|` toimintorivillä. Luokat sisältävät yleensä eniten käytetyt toiminnot, jotta ne löytyvät nopeasti. Esimerkiksi **Myyntitilaukset**-sivun **Tilaus**-, **Vapautus**- ja **Kirjaus**-toiminnot ovat ylätasolle siirrettyjä luokkia.

> [!NOTE]
> Et voi mukauttaa toimintopalkkia, joka näkyy sivun osissa (esimerkiksi **Myyntitilaus**-sivun myyntirivit-osassa).

### <a name="to-remove-hide-and-show-actions-and-action-groups"></a>Toimintojen ja toimintoryhmien poistaminen, piilottaminen ja näyttäminen
Jos haluat näyttää tai piilottaa toiminnot, nuolenpään vaihtoehdot määrittävät mahdolliset toimet toiminnon tilan mukaan.
1. Valitse toiminnon tai toimintoryhmän nuolenpää.
2. Valitse jokin seuraavista vaihtoehdoista:

|Asetus|Kuvaus|
|------|------------
|**Poista**|Tämä vaihtoehto näkyy, jos valittu toiminto näkyy myös jossain muualla siirtymispalkissa tai toimintorivillä. Tämän vaihtoehdon valitseminen poistaa toiminnon valitusta sijainnista siten, ettei se enää näy. Toiminto tai toimintoryhmä näkyy edelleen toisissa sijainneissa. |
|**Piilota**|Tämä vaihtoehto näkyy, jos toiminto tai toimintoryhmä ei sijaitse muualla siirtymispalkissa tai toimintorivillä. **Poista**-vaihtoehdon tavoin myös tämä vaihtoehto poistaa toiminnon tai toimintoryhmän näkyvistä siirtymispalkissa tai toimintorivillä. Toiminto tai toimintoryhmä näkyy kuitenkin mukauttamistilassa nykyisessä paikassa – himmennettynä.|
|**Näytä**|Tämä vaihtoehto näkyy, jos toiminto tai toimintoryhmä on piilotettu aiemmin (näkyy himmennettynä). Kun tämä vaihtoehto valitaan, toiminto tai toimintoryhmä tulee näkyviin siirtymispalkissa tai toimintorivillä.|

### <a name="to-move-actions-and-action-groups"></a>Toimintojen tai toimintoryhmien siirtäminen
Kahden toiminnon välinen vaakaviiva tai toimintoryhmää ympäröivä reunus ilmaisee, mihin voit pudottaa toimintoja ja toimintoryhmiä. Voimassa ovat seuraavat rajoitukset:

- Vaikka voit siirtää yksittäisiä toimintoja ylätasolle siirrettyihin luokkiin, et voi muuttaa toimintojen järjestystä luokan sisällä.
- Et voi siirtää toimintoryhmää ylätasolle siirrettyyn luokkaan.

1. Voit siirtää toiminnon tai toimintoryhmä vetämällä ja pudottamalla sen toivottuun paikkaan samalla tavoin kuin kentät ja sarakkeet.
2. Voit siirtää toiminnon tai toimintoryhmän toiseen, tyhjään toimintoryhmään vetämällä toiminnon tai toimintoryhmän uuteen ryhmään ja pudottamalla sen **Pudota toiminto tähän** -ruutuun.


## <a name="personalizing-parts"></a><a name="Parts"></a>Osien mukauttaminen

Osat ovat sivun alueita, jotka koostuvat yleensä useista kentistä, kaavioista tai muusta sisällöstä. Kun osat valitaan, ne tunnistetaan värillisestä reunasta. Esimerkiksi Roolikeskuksen aloitusnäytössä on useita osia. Voit mukauttaa koko osan sekä sen sisällön, koska raja on määritetty selvästi.

- Voit siirtää osaa vetämällä ja pudottamalla sen haluamaasi kohtaan. Värillinen rivi osoittaa sallitut sijainnit näytössä. Esimerkiksi tietoruutuja voi siirtää vain tietoruudun alueella muiden tietoruutujen viereen.
- Voit piilottaa osan valitsemalla **Piilota**-vaihtoehdon nuolenpään kohdalla.
- Kun aloitat mukauttamisen tai siirryt uudelle sivulle, kaikki piilotetut osat näkyvät sivulla niin, että käyttäjä tietää niiden olevan piilotettuja. Voit poistaa osan piilotuksen valitsemalla **Näytä**-vaihtoehdon nuolenpään kohdalla.

Voit poistaa kaikki yksittäisen osan sisällä tekemäsi mukautusmuutokset valitsemalla **Poista mukauttaminen** -asetuksen osan nuolenpään kohdalla. Osan mukauttamisen poistaminen vaikuttaa vain osan sisältöön, ei sivulla olevan osan sijoitteluun tai näkyvyyteen.  


## <a name="to-clear-personalization"></a>Mukautuksen tyhjentäminen
Haluat ehkä joissain vaiheessa kumota osan sivulle aiemmin tehdyistä mukautusmuutoksista tai kaikki muutokset.

1. Valitse **Mukauttaminen**-palkissa **Tyhjennä mukautus** -toiminto.
2. Valitse yksi seuraavista vaihtoehdoista. Muista, että mukautuksen tyhjentämistä ei voi kumota.

|Asetus|Kuvaus|
|------|------------
|**Vain siirtymisvalikko**|Poistaa kaikki mukautusmuutokset, jotka olet koskaan tehnyt siirtymisvalikkoon, joka on jaettu roolikeskuksen ja muiden sivujen kesken. Tämä sisältää kaikki uudet toiminnot, jotka lisättiin kirjanmerkeiksi, sekä kaikki muutokset linkkeihin ja ryhmiin valikossa.|  
|**Vain toiminnot**|Tyhjentää kaikki sivun siirtymispalkkien tai toimintorivien toimintoihin aiemmin tehdyt mukautusmuutokset.|
|**Vain kentät, sarakkeet ja osat**|Tyhjentää kaikki muut sivun toimintoihin aiemmin tehdyt mukautusmuutokset paitsi siirtymispalkin tai toimintorivin muutokset. Tämä sisältää kaikki kenttiin, sarakkeisiin, osiin ja ruutuihin tehdyt muutokset. |
|**Kaikki**|Tyhjentää kaikki sivulle tehdyt mukautusmuutokset, joten sivu palautetaan alkuperäiseen ulkoasuunsa. Tämä sisältää kaikki siirtymispalkkeihin, toimintoriveihin, kenttiin, sarakkeisiin, osiin ja ruutuihin tehdyt muutokset.|

## <a name="additional-points-of-interest"></a>Muita kiinnostavia seikkoja
Seuraavat seikat auttavat ymmärtämään mukauttamista entistä paremmin.

- Kun teet muutoksia luettelosta avautuvalle korttisivulle, muutokset koskevat kaikki kyseisestä luettelosta avattavia tietueita. Oletetaan esimerkiksi, että avaat tietyn asiakkaan Asiakasluettelo-sivulta ja mukautat sivua lisäämällä siihen kentän. Kun avaat luettelossa muita asiakkaita, myös lisäämäsi kenttä on näkyvissä.
- Tekemäsi muutokset koskevat kaikkia roolikeskuksia. Jos esimerkiksi teet muutoksen asiakasluetteloon, kun roolikeskuksen asetuksena on Liiketoimintajohtaja, asiakasluettelon muutos näkyy myös **Asiakkaat**-sivulla, kun roolikeskuksen asetuksena on Myyntitilausten käsittelijä.
- Ruudun sivulla tehdyt muutokset koskevat sivua kaikissa tilanteissa, joissa se näytetään.  
- Voit lisätä kenttiä ja sarakkeita vain kyseiseen sivuun perustuvasta ennaltamääritetystä luettelosta. Uusia kenttiä tai sarakkeita ei voi luoda.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös
[Profiilien sivujen mukauttaminen](ui-personalization-manage.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]