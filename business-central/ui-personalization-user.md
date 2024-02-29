---
title: Sivujen mukauttaminen (sisältää videon)
description: Lisätietoja käyttöliittymän ja työtilan mukauttamisesta omaan Business Centralin käyttötapaan ja omiin preferensseihin sopivaksi.
author: jswymer
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.reviewer: jswymer
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 01/15/2024
ms.author: jswymer
---
# Mukauta työtilaa

Voit voivat mukauttaa työtilasi työsi ja mieltymystesi mukaiseksi. Muuta sivuja siten, että niissä näkyy vain tarvitsemasi tiedot, missä niitä tarvitaan. Mukauttaminen vaikuttaa vain työtilaan. Se ei muuta toisten työskentelyä. Voit mukauttaa kaikenlaisia sivuja, myös [roolikeskuksen](ui-change-basic-settings.md#role-center) sivua.

> [!NOTE]
> Verkkoasiakasohjelman suunnitteluominaisuuksien rajoitusten vuoksi ei ole tällä hetkellä mahdollista mukauttaa tai personoida ohjaimia `grid`- ja `fixed`-syntaksin sisällä.
Se koskee kaikkia suunnittelutiloja, ei vain personointia.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Voit tehdä erilaisia muutoksia, kuten siirtää tai piilottaa kenttiä, sarakkeita, toimintoja ja kokonaisia osia sekä lisätä uusia kenttiä. Useimmat mukautukset on tehtävä aktivoimalla ensin **mukautus**-palkki. Voit tehdä yksinkertaisia muutoksia, kuten sarakkeen leveyden, heti missä tahansa luettelossa.

> [!NOTE]
> Järjestelmänvalvojat voivat tehdä samat asettelun muutokset kuin käyttäjät mukauttamalla profiilia (roolia), jolle on määritetty useita käyttäjiä. Saat lisätietoja roolien sivuista valitsemalla [Roolien sivujen mukauttaminen](ui-personalization-manage.md)<br /><br />
Järjestelmänvalvojat voivat myös ohittaa käyttäjien mukauttamiset tai poistaa ne käytöstä sekä määrittää, mitkä ominaisuudet käyttäjät näkevät kaikissa tai tietyissä yrityksissä. Lisätietoja on kohdassa [Business Centralin mukauttaminen](ui-customizing-overview.md).

## Video

Seuraava video näyttää joitakin tapoja, joilla voit mukauttaa roolikeskuksesi.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## Sarakkeen leveyden muuttaminen

Voit helposti muuttaa sarakkeiden kokoa missä tahansa luettelossa. Vedä vain kahden sarakkeen välistä rajaa vasemmalle tai oikealle.  

1. Valitse ja vedä sarakkeiden välissä olevaa rajaa luettelon otsikossa.
2. Voit vaihtoehtoisesti kaksoisnapsauttaa kahden sarakkeen rajaa, jolloin sarakkeen leveys sovitetaan automaattisesti. Leveys säätyy luettavuuden kannalta optimaaliseksi.

Muiden mukautusten tavoin sarakkeen leveyteen tehdyt muutokset tallennetaan tiliin, ja ne ovat käytettävissä riippumatta siitä, millä laitetta käytetään kirjautumiseen.

## Mukauttamisen aloittaminen mukautustilan avulla

1. Avaa mukautettava sivu.
1. Valitse oikeasta yläkulmasta ![Asetukset.](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") -kuvake ja valitse sitten **Mukauta**-toiminto.

    **Mukautetaan**-palkki tulee yläreunaan osoittamaan, että voit aloittaa muutosten tekemisen.

    > [!NOTE]
    > Voit siirtyä mukauttamisen aikana käyttämällä toiminnossa <kbd>Ctrl</kbd>+<kbd>napsautus</kbd>-yhdistelmää, jos nuolenpää osoittaa toiminnon olevan valittuna.

    Jos näet palkissa ![Mukautuksen lukitus](media/personalization-lock-icon.png "Mukautuksen lukitus") - tai ![Mukautus estetty](media/personalization-blocked-icon.png "Mukauttaminen estetty") -ilmoituksen, et voi mukauttaa sivua. Lisätietoja on kohdassa [Sivun mukauttamisen estäminen lukitsemalla](ui-personalization-locked.md).

1. Voit muuttaa käyttöliittymän elementtiä osoittamalla elementtiä, kuten toimintoa, kenttää tai osaa. Elementti valitaan, minkä osoituksena on nuolenpää tai raja. Valitse ensin elementti ja sitten joko **Siirrä**, **Poista**, **Piilota**, **Näytä**, **Näytä kohdassa ”Näytä lisää”**, **Näytä, kun tiivistetty**, **Näytä aina**, **Määritä tai tyhjennä kiinnitysruutu** tai **Sisällytä pikatapahtumaan tai Sulje pois pikatapahtumasta** käyttöliittymäelementin tyypin ja tilan mukaan.
1. Lisää kenttä valitsemalla **+ Kenttä** -toiminto. Vedä ja pudota kenttä **Lisää kenttä sivulle** -ruudusta sopivaan paikkaan sivulla.
1. Kun olet muuttanut yhden tai usean sivun asettelua, valitse**Mukauttaminen**-palkissa **Valmis**-painike.

Lisätietoja on kohdassa [Mukautettavat toimet](#What).

## <a name="What"></a>Mukautettavat toimet

|Tehtävä toimi|Ohjeet|Huomautukset|
|----|------------|-------|
|Esimerkiksi kentän, luettelon sarakkeen, ruudun, toiminnon tai osan siirtäminen toiseen kohtaan sivulla|Osoita siirron kohdetta ja vedä se uuteen paikkaan. Paksu vaaka- tai pystyviiva osoittaa paikan.<br /><br />![Et voi siirtää tänne -kuvake](media/personalization-cannot-move-here.png "Personalisointitila - Ei voi siirtää tähän -kuvake") osoittaa, että et voi siirtää elementtiä valittuun sijaintiin.|Osat ovat osia tai alueita sivulla ja niissä on esimerkiksi useita kenttiä, toinen sivu, kaavio tai ruutuja.<br /><br />[Lisätietoja toimintojen mukauttamisesta](#Actions)<br>[Lisätietoja osien mukauttamisesta](#Parts)|
|Piilota näkyvissä parhaillaan oleva elementti, kuten kenttä, luettelon sarake, ruutu, toiminto tai osa.|Valitse elementti, piilota nuolenpää ja valitse sitten <b>Piilota</b>.|Mukautustilassa piilotetut toiminnot näkyvät harmaina, ja niiden teksti on kursivoitu. Piilotetut osat varjostetaan vinoviivoilla. Piilotettuja kenttiä ja sarakkeita ei ole ilmaistu suoraan sivulla, mutta voit paikallistaa ne <b>Lisää kenttää sivulle</b> -ruudun avulla (l[isätietoja työskentelykentistä](#fields)).<br><br>Kun poistut mukautustilasta, kaikki elementit katoavat näkymästä. Jos piilottamasi kenttä näkyy myös tiivistetyn pikavälilehden otsikossa, kenttä ei enää näy tässä kohdassa.|
|Näytä parhaillaan piilotettuna oleva toiminto tai osa|Valitse ensin harmaan (piilotetun) elementin nuolenpää ja sitten <b>Näytä</b>.|Piilotettu elementti on taas näkyvissä.|
|Lisää parhaillaan piilotettuna oleva kenttä|Valitse <b>Mukauttaminen</b>-palkissa <b>+ Kenttä</b>-toiminto.<br /></br><b>Lisää kenttä sivulle</b> -ruutu avautuu sivun oikealla puolelle. Jos valitset kentän ruudusta, sen piilotettu sijainti näkyy sivulla.<br /><br />Lisää kenttä vetämällä se ruudusta tai sen piilotetusta sijainnista haluttuun sijaintiin. Paikka osoitetaan paksulla vaaka- tai pystyviivalla.<br><br> Toinen tapa on valita nuolenpää kentän piilotetussa sijainnissa ja valita sitten **Näytä**. |Kullakin sivulla on valmiiksi määritetty joukko kenttiä, joita voi valita näytettäviksi.<br /><br />[Lisätietoja kenttien käyttämisestä](#fields) |
|Kentän näyttäminen kutistetun pikavälilehden otsikossa.|Valitse ensin nuolenpää ja sitten <b>Näytä, kun tiivistetty</b>. <br /> <br />Jos tämä vaihtoehto ei näy, se on jo määritetty. Valitse tässä tapauksessa <b>Näytä aina</b>, jos haluat, että kenttä ei enää näy pikavälilehden otsikossa.|*Pikavälilehdellä* tarkoitetaan kenttiä, jotka on ryhmitetty yhteisen otsikon alle. Tärkeimmät kentät näkyvät, kun valitset <b>Näytä, kun tiivistetty</b>. Jos valitset otsikossa olevan kentän, pikavälilehti avautuu ja kohdistus on valitussa kentässä.<br /><br />Tämä vaihtoehto on käytettävissä vain, jos sivulla on useita pikavälilehtiä. Jos pikavälilehtiä on vain yksi, sitä ei voi tiivistää, joten <b>Näytä, kun tiivistetty</b> -vaihtoehto ei ole käytettävissä.|
|Kentän näyttäminen vain, kun **Näytä enemmän** on valittu|Valitse ensin nuolenpää ja sitten <b>Näytä kohdassa Näytä lisää</b>.|Jos <b>Näytä kohdassa Näytä lisää</b> -vaihtoehto ei ole näkyvissä, kenttä on jo määritetty. Tällöin saat näkyviin aina, eikä vain, kun valitset-kentän **Näytä useita**, valitse <b>Näytä aina</b>.|
|Määritä, voiko kenttää muokata vai ei.|Valitse kenttä ja valitse sitten nuolenpää kentässä. Valitse <b>Lukitse muokkaus</b>, jos haluat estää kentän arvon muuttamisen. Valitse <b>Avaa muokkauksen lukitus</b>, jos haluat muuttaa kentän arvoa.|Voit poistaa vain niiden kenttien lukituksen, jotka olet aiemmin lukinnut itse. Jotkin kentät on suunniteltu oletusarvoisesti lukituiksi. Jotkut kentät [sivua muokannut](ui-personalization-manage.md) profiilin järjestelmänvalvoja on lukinnut. Näiden kenttien lukitusta ei voi poistaa.|
|Kiinnitysruudun muuttaminen toiseen sarakkeeseen luettelossa |Valitse sen sarakkeen nuolenpää, jonka haluat olevan kiinnitysruudun viimeinen sarake, ja valitse sitten <b>Määritä kiinnitysruutu</b>.<br /><br/>Jos haluat määrittää kiinnitysruudun takaiseen alkuperäiseen paikkaan, valitse ensin nykyisen kiinnitysruutusarakkeen nuolenpää ja sitten <b>Tyhjennä kiinnitysruutu</b>. Huomautus: Et voi poistaa tätä kiinnitysruutua.|Kiinnitysruutu määrittää aina luettelon vasemmalla puolella näkyvät sarakkeet. Nämä sarakkeet näkyvät myös vaakasuoraan vieritettäessä.|  
|Kentän ohittaminen Enter-näppäintä painettaessa|Valitse ensin kentän vieressä oleva nuolenpää tai sarakkeen otsikko luettelossa ja valitse sitten **Sulje pois pikatapahtumasta**.  | Jos **Jätä pois pikasyötöstä** -kohta ei ole näkyvissä, kenttä on jo ohitettu. Voit siinä tapauksessa lopettaa kentän ohittamisen valitsemalla **Sisällytä pikatapahtumaan**.<br><br>[Lisätietoja pikasyötöstä](ui-enter-data.md#QuickEntry)|
|Suodatettuja luetteloita vastaavien näkymien järjestäminen uudelleen ja poistaminen|Valitse ensin näkymän vieressä oleva nuolenpää ja sitten **Siirrä**, **Poista** tai **Piilota**.|[Lisätietoja luettelonäkymien tallentamisesta ja mukauttamisesta](ui-views.md)|  
|Lisää uusi toiminto roolikeskuksen sivuun tai raporttiin.|Valitse kohdesivu-, raportin pyyntösivu- tai Ilmoita-ikkunassa kirjanmerkkikuvake.|[Lisätietoja kirjanmerkkien lisäämisestä sivuihin ja raportteihin](ui-bookmarks.md)|
|Aloita luettelo aina laajennettuna tai tiivistettynä|Valitse **Laajenna kaikki**- tai **Tiivistä kaikki** -painike luettelon vasemmassa yläkulmassa. Voit myös valita **Laajenna kaikki**- tai **Tiivistä kaikki** -toiminnot ensimmäisen sarakkeen valikosta. |Koskee tiivistettäviä hierarkialuetteloita|

## <a name="Actions"></a>Toimintopalkin ja valikoiden mukauttaminen

Mukauttamisen avulla voit päättää, mitkä toiminnot näkyvät siirtymispalkissa, toimintoriveillä ja roolikeskuksissa sekä muissa kohdissa, joissa niiden halutaan näkyvän. Voit näyttää, piilottaa tai siirtää yksittäisiä toimintoja tai toimintoryhmiä.

Seuraavassa videossa näkyy, miten voit mukauttaa sivujen ja roolikeskusten toimintoja.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE594m2]

Siirtymispalkkia ja toimintorivejä mukautetaan käytännössä samalla tavoin kuin muita käyttöliittymän elementtejä. Se, mitä kullekin toiminnolle tai ryhmälle voi tehdä, määräytyy sen mukaan, missä toiminto tai ryhmä on. Kätevimmin asian voi selvittää siirtymällä mukautustilaan ja toimimalla sitten ohjenuolien mukaan.

Toiminnon mukauttamista helpottaa, kun tiedät, mitä muutama termi tarkoittaa. Nämä termit ovat *toimintoryhmä* ja *ylätasolle siirretty luokka*.  

*Toimintoryhmä* on elementti, joka voidaan laajentaa näyttämään muita toimintoja tai ryhmiä. Esimerkiksi **Myyntitilaukset**-sivulla yksi toimintoryhmä on **Toiminnot**-toiminto, joka tulee näkyviin, kun valitset **Toiminnot**-toiminnon toimintoryhmissä.

*Ylätasolle siirretty luokka* on toimintoryhmä, joka näkyy ennen pystyviivaa `|` toimintorivillä. Luokat sisältävät yleensä eniten käytetyt toiminnot, jotta ne löytyvät nopeasti. Esimerkiksi **Myyntitilaukset**-sivun **Tilaus**-, **Vapautus**- ja **Kirjaus**-toiminnot ovat ylätasolle siirrettyjä luokkia.

> [!NOTE]  
> Jos haluat poistaa mukauttamisen, valitse nuolenkärki osan suunnitteluvalikon ympärillä ja valitse sitten **Tyhjennä mukauttaminen**.

### Toimintojen ja toimintoryhmien poistaminen, piilottaminen ja näyttäminen

Jos haluat näyttää tai piilottaa toiminnot, nuolenpään vaihtoehdot määrittävät mahdolliset toimet toiminnon tilan mukaan. 

1. Valitse toiminnon tai toimintoryhmän nuolenpää.
2. Valitse jokin seuraavista vaihtoehdoista:

|Asetus|Kuvaus|
|------|------------|
|**Poista**|Tämä vaihtoehto näkyy, jos valittu toiminto näkyy myös jossain muualla siirtymispalkissa tai toimintorivillä. Tämän vaihtoehdon valitseminen poistaa toiminnon valitusta sijainnista siten, ettei se enää näy. Toiminto tai toimintoryhmä näkyy edelleen toisissa sijainneissa. |
|**Piilota**|Tämä vaihtoehto näkyy, jos toiminto tai toimintoryhmä ei sijaitse muualla siirtymispalkissa tai toimintorivillä. **Poista**-vaihtoehdon tavoin myös tämä vaihtoehto poistaa toiminnon tai toimintoryhmän näkyvistä siirtymispalkissa tai toimintorivillä. Toiminto tai toimintoryhmä näkyy kuitenkin mukauttamistilassa nykyisessä paikassa – himmennettynä.|
|**Näytä**|Tämä vaihtoehto näkyy, jos toiminto tai toimintoryhmä on piilotettu (näkyy himmennettynä). Kun tämä vaihtoehto valitaan, toiminto tai toimintoryhmä tulee näkyviin siirtymispalkissa tai toimintorivillä.|

### Toimintojen tai toimintoryhmien siirtäminen

Kahden toiminnon välinen vaakaviiva tai toimintoryhmää ympäröivä reunus ilmaisee, mihin voit pudottaa toimintoja ja toimintoryhmiä. Voimassa ovat seuraavat rajoitukset:

- Vaikka voit siirtää yksittäisiä toimintoja ylätasolle siirrettyihin luokkiin, et voi muuttaa toimintojen järjestystä luokan sisällä.
- Et voi siirtää toimintoryhmää ylätasolle siirrettyyn luokkaan.

1. Voit siirtää toiminnon tai toimintoryhmä vetämällä ja pudottamalla sen toivottuun paikkaan samalla tavoin kuin kentät ja sarakkeet.
2. Voit siirtää toiminnon tai toimintoryhmän toiseen, tyhjään toimintoryhmään vetämällä toiminnon tai toimintoryhmän uuteen ryhmään ja pudottamalla sen **Pudota toiminto tähän** -ruutuun.

### Tietoja Automatisointi-valikosta

- **Automatisointi**-valikkoa ja **Power Automate** -alivalikkoa ja sen toimintoja ei voi piilottaa eikä siirtää.
- Voit siirtää **automaattinen**-nimikkeeseen kuuluvia työnkulkuja, mutta et voi piilottaa niitä personoinnin avulla. Työnkulun siirtäminen kopioi työnkulun määräpäähän, se ei poista sitä **automaattisesta** nimikkeestä.

> [!TIP]
> Järjestelmänvalvojana voit piilottaa **Automaattisen** nimikkeen käyttäjiltä. Lisätietoja kohdassa [Power Automate -integraation määrittäminen](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

## <a name="Parts"></a>Osien mukauttaminen

Osoita kohtaa tai valitse <kbd>Alt</kbd>+<kbd>ylänuoli</kbd>. Osat ovat sivun alueita, jotka koostuvat tavallisesti useista kentistä, kaavioista tai muusta sisällöstä. Osassa näkyy värillinen reunus, kun keskityt osaan. Esimerkiksi Roolikeskuksen aloitusnäytössä on useita osia. Voit mukauttaa koko osan ja sen sisällön, koska raja on määritetty selvästi.

- Voit siirtää osaa vetämällä ja pudottamalla sen haluamaasi kohtaan. Värillinen rivi osoittaa sallitut sijainnit näytössä. Esimerkiksi tietoruutuja voi siirtää vain tietoruudun alueella muiden tietoruutujen viereen.
- Voit piilottaa osan valitsemalla **Piilota**-vaihtoehdon nuolenpään kohdalla.
- Kun aloitat mukauttamisen tai siirryt uudelle sivulle, kaikki piilotetut osat näkyvät sivulla niin, että käyttäjä tietää niiden olevan piilotettuja. Voit poistaa osan piilotuksen valitsemalla **Näytä**-vaihtoehdon nuolenpään kohdalla.

Voit poistaa kaikki yksittäisen osan sisällä tekemäsi mukautusmuutokset valitsemalla **Poista mukauttaminen** -asetuksen osan nuolenpään kohdalla. Osan mukauttamisen poistaminen vaikuttaa vain osan sisältöön, ei sivulla olevan osan sijoitteluun tai näkyvyyteen.  

## <a name="fields"></a> Kenttien ja sarakkeiden käsitteleminen

Käytä sivua mukautettaessa **Lisää kenttä sivulle** -ruutua, jos haluat sisällyttää näkymässä parhaillaan piilotettuna olevat kentät tai sarakkeet. Voit avata tämän ruudun valitsemalla lähellä sivun yläosaa olevan **+ Kenttä** -toiminnon. Piilotetut kentät eivät näy sivulla mukautustilassa, kuten muut piilotetut elementit. Voit kuitenkin tunnistaa piilotetut kentät **Lisää kenttä sivulle** -ruudun avulla.

Tässä muutamia yleisiä ohjeita, joita voit seurata, kun käytät **Lisää kenttä sivulle** -ruutua:

- Oletusarvon mukaan ruudussa näkyvät kaikki piilotetut kentät. Piilotetut kentät on merkitty ![Näyttää piilotetun kentän kuvakkeen](media/hidden-icon.png "Näyttää piilotetun kentän -kuvake") -kuvakkeella.
- Voit suodattaa luettelon niin, että se näyttää muut kentät, esimerkiksi sivulla parhaillaan näkyvissä olevat kentät. Valitse tällöin **Suositellut kentät** -painike luettelon alla ja valitse sitten suodatusvaihtoehto. Painikkeen nimi muuttuu valitsemasi suodatusvaihtoehdon perusteella.
  
   :::image type="content" source="media/personlaization-filter.svg" alt-text="Näyttää suodatuspainikkeen mukautustilassa Lisää kenttä -ruudussa.":::
- Kun kenttä valitaan luettelosta, sen sijainti sivulla korostetaan. Jos kenttä on tällä hetkellä piilotettu, sen suunniteltu sijainti näkyy varjostetussa tilassa. 
- Saat lisätietoja luettelossa olevasta kentästä osoittamalla sitä tai valitsemalla <kbd>Alt</kbd>+<kbd>ylänuoli</kbd>, jolloin näyttöön tulee työkaluvihje.
- **Lisää kenttä sivulle** -ruudun käytettävissä olevat kentät on määrittänyt sivun ja sen lähdetaulukon kehittäjä tai profiilin järjestelmänvalvoja, joka on [mukauttanut sivun](ui-personalization-manage.md). Uusia kenttiä tai sarakkeita ei voi luoda.
- Joillakin sivuilla on useita sivukenttiä, jotka on linkitetty samaan lähdetaulukkoon. Ruudussa näkyvät molemmat tai kaikki sivun kentät erikseen. Kenttien näyttäminen, piilottaminen ja siirtäminen on myös itsenäistä, eikä toiminto vaikuta muihin kenttiin.

### Kentän lisääminen siten, että se näkyy sivulla

**Lisää kenttä sivulle** -ruudussa on kaksi tapaa sisällyttää sivulle piilotettu kenttä.

- Vedä kenttä haluamaasi kohtaan. Kohdesijainti osoitetaan paksulla vaaka- tai pystyviivalla.
- Valitse kenttä luettelosta ja siirry sivun varjostettuun kenttään. Valitse lopuksi **Näytä**-vaihtoehto.

> [!NOTE]
> Kaikkia lisäämiäsi kenttiä ei voi muokata sivulla, kun olet tehnyt mukautukset. Nämä kentät on alun perin suunniteltu näin, tai järjestelmänvalvoja on [mukauttanut](ui-personalization-manage.md) sivua, jotta kenttiä ei voi muokata.

## Tyhjennä mukautus

Haluat ehkä joissain vaiheessa kumota osan sivulle aiemmin tehdyistä mukautusmuutoksista tai kaikki muutokset.

1. Valitse **Mukauttaminen**-palkissa **Tyhjennä mukautus** -toiminto.
2. Valitse yksi seuraavista vaihtoehdoista.  

> [!CAUTION]
> Mukautuksen tyhjentämistä ei voi kumota.

|Asetus|Kuvaus|
|------|------------
|**Vain siirtymisvalikko**|Poistaa kaikki mukautusmuutokset, jotka olet koskaan tehnyt siirtymisvalikkoon, joka on jaettu roolikeskuksen ja muiden sivujen kesken. Nämä muutokset sisältävät kaikki uudet toiminnot, jotka lisättiin kirjanmerkeiksi, sekä kaikki muutokset linkkeihin ja ryhmiin valikossa.|  
|**Vain toiminnot**|Tyhjentää kaikki sivun siirtymispalkkien tai toimintorivien toimintoihin aiemmin tehdyt mukautusmuutokset.|
|**Vain kenttä ja sarakkeet**|Tyhjentää kaikki muut sivun toimintoihin aiemmin tehdyt mukautusmuutokset paitsi siirtymispalkin tai toimintorivin muutokset. Nämä muutokset sisältävät kaikki kenttiin, sarakkeisiin, osiin ja ruutuihin tehdyt muutokset. |
|**Kaikki**|Tyhjentää kaikki sivulle tehdyt mukautusmuutokset, joten sivu palautetaan alkuperäiseen ulkoasuunsa. Nämä muutokset sisältävät kaikki siirtymispalkkeihin, toimintoriveihin, kenttiin, sarakkeisiin, osiin ja ruutuihin tehdyt muutokset.|

## Vinkkejä ja muita kiinnostavia seikkoja

Seuraavat seikat auttavat ymmärtämään mukauttamista entistä paremmin.

- Kun teet muutoksia luettelosta avautuvalle korttisivulle, muutokset koskevat kaikki kyseisestä luettelosta avattavia tietueita. Oletetaan esimerkiksi, että avaat tietyn asiakkaan Asiakasluettelo-sivulta ja mukautat sivua lisäämällä siihen kentän. Kun avaat luettelossa muita asiakkaita, myös lisäämäsi kenttä on näkyvissä.
- Tekemäsi muutokset koskevat kaikkia roolikeskuksia. Jos esimerkiksi teet muutoksen asiakasluetteloon, kun roolikeskuksen asetuksena on Liiketoimintajohtaja, asiakasluettelon muutos näkyy myös **Asiakkaat**-sivulla, kun roolikeskuksen asetuksena on Myyntitilausten käsittelijä.
- Ruudun sivulla tehdyt muutokset koskevat sivua kaikissa tilanteissa, joissa se näytetään.  
- Sivua, joka ei ole [analyysitilassa](analysis-mode.md), ei voi mukauttaa. **Analysoi**-vaihtopainikkeen aktivointi on poistettu. Jos siirryt mukautustilaan sivun ollessa analyysitilassa, analysointitila poistetaan automaattisesti käytöstä. 
- Joillakin sivuilla on useita sivukenttiä, jotka on linkitetty samaan lähdetaulukkoon. Ruudussa näkyvät molemmat tai kaikki sivun kentät erikseen. Kenttien näyttäminen, piilottaminen ja siirtäminen on myös itsenäistä, eikä toiminto vaikuta muihin kenttiin.
- Jos piilotettuna on osa tai ryhmä, kentät, joista on luotu esimerkki, näkyvät yhä sen sisällä, mutta et voi vetää ja pudottaa tai lisätä ja näyttää kenttää ennen kuin ryhmä tai osa on määritetty näkyväksi.

## Katso myös

[Profiilien sivujen mukauttaminen](ui-personalization-manage.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
