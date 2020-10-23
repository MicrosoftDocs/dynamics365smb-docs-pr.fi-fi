---
title: Määrityspaketin valmisteleminen | Microsoft Docs
description: Tietoja RapidStart-määrityspaketista, joka helpottaa uusien yritysten määrittämistä aiemmin luotujen tietojen perusteella.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: cfb7c0186f7ed81687ad3f4d667b3f71d77af424
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922515"
---
# <a name="prepare-a-configuration-package"></a>Määrityspaketin valmisteleminen

Kun määrität uuden yrityksen määrityspaketin perusteella, taulukon suhteet tunnistetaan ja käsitellään. Tiedot tuodaan ja otetaan käyttöön oikeassa järjestyksessä. Dimensiotaulukot tuodaan myös, jos ne on sisällytetty määrityspakettiin. Lisätietoja on kohdassa [Asiakastietojen tuominen](admin-migrate-customer-data.md#to-import-customer-data).  

Auttaaksesi asiakastasi käyttämään kokoonpano-pakettia haluat ehkä lisätä pakettiin kyselylomakkeen tai useita kyselylomakkeita. Kyselylomake voi auttaa asiakkaita ymmärtämään eri asetusvaihtoehtoja. Yleensä suurille asetustaulukoille luodaan kyselylomakkeet, jolloin asiakas voi vaatia lisää ohjeita siitä, miten voi valita haluamansa asetuksen. Lisätietoja on kohdassa [Asiakkaan asetusarvojen kerääminen](admin-gather-customer-setup-values.md).

## <a name="before-you-create-a-configuration-package"></a>Ennen määrityspaketin luomista

Ennen määrityspaketin luomista on otettava huomioon joitakin asioita, koska ne vaikuttavat sinuun tai asiakkaasi mahdollisuuteen tuoda se.  

### <a name="tables-that-contain-posted-entries"></a>Kirjattuja tapahtumia sisältävät taulut

Tietoja ei voi tuoda tauluihin, jotka sisältävät kirjattuja tapahtumia, kuten asiakas-, toimittaja- ja nimiketapahtumien tauluihin, joten näitä tietoja ei pitäisi sisällyttää määrityspakettiin. Voit lisätä näihin tauluihin tapahtumia, kun olet tuonut määrityspaketin käyttämällä kirjauskansioita tapahtumien kirjaamiseen. Lisätietoja on kohdassa [Asiakirjojen ja kirjauskansioiden](ui-post-documents-journals.md) kirjaaminen.

### <a name="table-names-that-contain-special-characters"></a>Erikoismerkkejä sisältävät taulukoiden nimet

Käytä harkintaa, jos sinulla on taulukkoja tai kenttiä, joilla on sama ajallinen nimi mutta jotka eroavat erikoismerkkien osalta, kuten %, &, <, >, (ja). Esimerkiksi taulukossa "XYZ" voi olla "kenttä 1" ja "kenttä 1 %" -kentät.

XML-suoritin hyväksyy vain tietyt erikoismerkit ja poistaa ne, joita se ei hyväksy. Jos poistat erikoismerkin, esimerkiksi %-merkin "Kenttä 1 %" -esimerkissä, tuloksena on kaksi tai useampia samannimistä taulukkoja tai kenttiä. Virhe ilmenee, kun viet tai tuot kokoonpanopaketin. 

### <a name="licensing"></a>Käyttöoikeudet

Käyttöoikeuden on sisällettävä päivitettävät taulut. Jos et ole varma, **Konfiguroi työkirja** -sivu voi auttaa. Jos käyttöoikeus sisältää taulun, **Käyttöoikeudet sisältävä taulu** -valintaruutu on valittu.  

### <a name="permissions"></a>Käyttöoikeudet

Määrityspaketin luonti- ja tuontiprosessiin liittyvät seuraavat voimassa olevat käyttöoikeudet kaikkiin paketin tauluihin:  

- Määrityspaketin tietoja vievällä käyttäjällä on oltava voimassa oleva **Luku**oikeus.
- Määrityspaketin tietoja tuovalla käyttäjällä on oltava voimassa olevat **Lisää**- ja **Muokkaa**-oikeudet.

### <a name="database-schema"></a>Tietokannan rakenne

Kun yrityksen tietokantojen välillä tuodaan tai viedään määrityspaketteja, tietokantojen tulisi noudattaa samaa rakennetta, jotta kaikki tiedot siirtyvät onnistuneesti. Tämä tarkoittaa, että tietokannoilla tulisi olla sama taulukko- ja kenttärakenne, jossa taulukoilla on samat ensisijaiset avaimet ja kentillä on samat tunnukset ja tietotyypit.  

Tietokannasta, jolla on eri rakenne kuin kohdetietokanta, voi tuoda määrityspaketin. Mitään määrityspaketissa olevia taulukoita tai kenttiä, joita ei löydy kohdetietokannasta, ei kuitenkaan tuoda. Taulukoita, joilla on poikkeavat ensisijaiset avaimet tai kenttiä, joilla on poikkeavat tietotyypit ei myöskään voi tuoda. Tietoja ei voi tuoda, jos esimerkiksi määrityspaketissa on taulukko **50 000, asiakas**, jonka ensisijainen avain on **Code20**, ja kohdetietokannassa on taulukko **50 000, asiakkaan pankkitili**,jonka ensisijainen avain on **Code20 + Code 20**.  

## <a name="to-create-a-configuration-package"></a>Luo määrityspaketti

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määrityspaketit** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3. Täytä loput **Yleinen**-pikavälilehden kentät asianmukaisella tavalla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Sulje määrityskyselyt, kokoonpanomallit ja määritystyökirjojen taulukot valitsemalla **Jätä määritystaulukot pois** -valintaruutu. Muutoin nämä taulukot lisätään pakettitaulukoiden luetteloon automaattisesti, kun viet paketin.  
5. Valitse **Hae taulukot** -toiminto. **Hae pakettitaulukot** -eräajon sivu avautuu.  
6. Valitse **Valitse taulukot** -kenttä. **Määrityksen valinta** -sivu avautuu.  
7. Valitse **Valitse kaikki** -toiminto, jos haluat lisätä kaikki taulukot pakettiin, tai valitse luettelosta kaikkien lisättävien taulukoiden **Valittu**-valintaruutu.
8. Valitse **OK**-painike. Valitsemiesi taulukoiden määrä ilmaistaan **Valitse taulukot** -kentässä. Määritä lisäasetukset ja paina **OK** -painiketta. [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukoiden rivejä lisätään **Määrityspaketti**-sivulle.  

    > [!NOTE]  
    >  Voi tehdä tämän myös määritystyökirjassa. Valitse pakettiin sisällytettävät taulukot ja valitse sitten **Määritä paketti** -toiminto.

9. Valitse taulukosta kentät, jotka haluat sisällyttää, ja valitse **Rivit**-välilehdessä **Kentät**-toiminto.
Määritä kentät, jotka sisältyvät pakkaukseen. Kaikki kentät ovat oletusarvoisesti mukana.

    - Jos haluat valita vain sisällytettävät kentät, valitse **Tyhjennä sisällytetty** -toiminto. Jos haluat lisätä kaikki kentät, valitse **Aseta sisällytetty** -toiminto.  
    - Määrittääksesi, että kentän tietoja ei tule vahvistaa, poista **Tarkista kenttä** -valintaruutu.  

10. Määritä, oletko toteuttanut mahdollisia virheitä, valitsemalla **Hyväksy paketti** -toiminto. Näin voi tapahtua, kun ei ole otettu mukaan taulukkoja, joihin määritykset perustuvat.  
11. Valitse **OK**-painike.  

Kun olet hienosäätänyt sisällytettävät kentät taulukosta, voit tarkistaa tulokset Excelissä.  

### <a name="to-filter-and-review-your-dataset"></a>Suodata ja esikatsele tietojoukko

1. Voit suodattaa tietyn joukon tietueita pakettiin kuuluvaksi valitsemalla **Rivit**-välilehdessä **Suodattimet**-toiminnon ja määrittämällä soveltuvat suodatinarvot.  
2. Valitse pakettikortin **Rivit**-välilehden **Vie Exceliin** -toiminto.  
3. Vahvista viestit, joiden avulla voit viedä tiedot Exceliin. Nimetty .xlsx-tiedosto avataan. Tarkastele tietueet, jotka on viety.  
4. Sulje Excel.  

### <a name="to-include-a-template-for-application-to-a-table"></a>Sisällytä malli taulukon sovellukseen

Voit määrittää tietyille päätietoja sisältäville taulukoille mallin, johon tiedot kohdistetaan. Malli voi sisältää pakolliset kentät, jotka halutaan ottaa käyttöön kaikissa perustiedoissa ja joiden ei koskaan haluta vaihtelevan. Voit esimerkiksi luoda mallin, jota voi käyttää asiakkaiden tietojen käsittelyssä. Malli voi sisältää kaikki pakolliset kentät, mikä puolestaan mahdollistaa standardoidun tiedon johdonmukaisen tuonnin. Tiedot, joita ei voida standardoida (kuten asiakkaan nimi), käsitellään asiakastietojen tuonnin yhteydessä. Lisätietoja on ohjeaiheessa [Asiakastietojen siirtämisen valmisteleminen mallien avulla](admin-use-templates-to-prepare-customer-data-for-migration.md).  

1. Valitse **Määritä pakettikortti** -sivulla taulukko ja valitse sitten **Tietomalli**-kenttä. Näyttöön tulee taulukkoon perustuva malliluettelo.
2. Valitse malli ja sitten **OK**-painike.  

Kun paketti on valmis, noudata seuraavaa menettelyä, jonka mukaan paketti tallennetaan tiedostoon. voit sitten antaa paketin asiakkaalle tai kumppanille käytettäväksi.

### <a name="to-save-and-export-a-configuration-package"></a>Tallenna ja vie kokoonpanopaketti

- Valitse **Määritä pakettikortti** -sivulla **Vie paketti** -toiminto.  

Paketti luodaan .rapidstart-tiedostosssa, joka toimittaa paketin sisällön pakatussa muodossa. Määrityskyselyt, määritysmallit ja määritystyökirja lisätään pakettiin automaattisesti, ellet ole jättänyt niitä erityisesti ulkopuolelle.  

Voit tallentaa tiedoston nimellä, joka on sinulle merkityksellinen, mutta et voi vaihtaa tiedoston tunnistetta. Sen on oltava .rapidstart.  

### <a name="to-copy-a-configuration-package"></a>Kopioi paketin kokoonpano

Kun olet luonut paketin, joka täyttää suurimman osan tarpeistasi, voit käyttää sitä perustana luodaksesi vastaavia paketteja. Tämä voi nopeuttaa täytäntöönpanoaikaa ja parantaa RapidStart Servicesin toistettavuutta.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määrityspaketit** ja valitse sitten liittyvä linkki.  
2. Valitse paketti luettelosta ja valitse sitten **Kopioi paketti** -toiminto.  
3. Anna **Uusi pakettikoodi** -kentässän uuden paketin koodi.  
4. Valitse **Kopioi tiedot** -valintaruutu, jos haluat myös kopioida tietokannan tiedot olemassa olevasta paketista.  
5. Valitse **OK**-painike.

## <a name="to-customize-a-configuration-package"></a>Määrityspaketin mukauttaminen

Käytä määritystyökirjaa kerätäksesi ja luokitellaksesi tietoja, joita haluat käyttää, jotta voit määrittää uuden yrityksen ja järjestää taulukot loogisesti. Työkirjan muotoilu perustuu yksinkertaiseen hierarkiaan: alueet sisältävät ryhmiä, jotka sisältävät taulukoita. Alueet ja ryhmät ovat valinnaisia, mutta ne ovat tarpeen, jos haluat ottaa käyttöön yleiskuvan määritysprosessista RapidStart Servicesin roolikeskuksessa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määritystyökirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Rivityyppi**-kentässä **Alue**. Anna **Nimi**-kentässä kuvaava nimi.  
3. Valitse **Rivityyppi**-kentässä **Ryhmä**. Anna **Nimi**-kentässä kuvaava nimi.  
4. Valitse **Rivityyppi**-kentässä **Taulukko**. Valitse **Taulukon tunnus** -kentässä taulukko, jonka haluat sisällyttää työkirjaan.  

Voit nyt liittää taulukot tiettyihin määrityspaketteihin, jotka olet luonut tai aiot luoda. Lisätietoja on kohdassa [Taulukon määrittäminen määrityspakettiin](admin-how-to-prepare-a-configuration-package.md#to-assign-a-table-to-a-configuration-package).

## <a name="to-work-with-promoted-tables"></a>Toimi ylemmän tason taulukoiden kanssa

1. Valitse **Ylätasolle siirretty taulukko** -valintaruutu. Se osoittaa taulukon, esimerkiksi **KP-tili** -taulukon, jota tyypillinen asiakas käyttää usein määritysprosessin aikana. Kun taulukossa on tämä määritys, asiakas voi helposti suodattaa työkirjansa nähdäkseen luettelon vain ylemmän tason taulukoista, joita on käsiteltävä.  
2. Valitse **Vain ylätaso** -toiminto, kun haluat nähdä suodatetun näkymän. Taulukoiden luettelo sisältää vain ne taulukot, joiden valintaruudussa on rasti.  

## <a name="to-assign-a-table-to-a-configuration-package"></a>Määritä taulukko määrityspakettiin

Kun olet määrittänyt taulukot, jotka haluat käsitellä osana kokoonpanoa, voit helposti määrittää taulukot kokoonpanopaketteihin. Voit määritellä taulukon vain yhdelle paketille. Seuraavassa toimenpiteessä määritetään paketti määritystyökirjasta.  

> [!NOTE]  
> Voit myös luoda paketin suoraan ja lisätä taulukot siihen. Lisätietoja on kohdassa [Määrityspaketin luominen](admin-how-to-prepare-a-configuration-package.md#to-create-a-configuration-package).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määritystyökirja** ja valitse sitten liittyvä linkki.
2. Valitse määritystyökirjassa rivi tai rivit määrityspakettiin määrittämistä varten. Vailtse sitten **Määritä paketti** -toiminto.  
3. Valitse paketti luettelosta tai valitse **Uusi**-toiminto, jos haluat luoda uuden paketin. Valitse sitten **OK**-painike.  

    Jos taulukko ei vielä sisälly pakettiin, se lisätään nyt. Pakettikoodi-kenttä työkirjarivillä täytetään sen paketin koodilla, jolle taulukko on määritetty.  
4. Jos valitset olemassa olevan paketin, voit tarkistaa paketin sisältämien taulukoiden määrän **Taulukoiden määrä** -kentästä.

## <a name="to-review-or-customize-existing-database-data"></a>Olemassa olevien tietokantatietojen tarkistaminen tai mukauttaminen

Kun luot kokoonpanonpaketin ratkaisua varten, voit tarkastella ja mukauttaa käytettävissä olevia tietokannan tietoja vastaamaan asiakkaan tarpeita. Tietokannan taulukolla on oltava siihen liittyvä sivu.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määritystyökirja** ja valitse sitten liittyvä linkki.
2. Etsi määritystyökirjasta taulukot, joiden tietoja haluat tarkastella tai muokata.  

    > [!NOTE]  
    >  Varmista, että jokaiseen taulukkoon on määritetty sivun tunnus. Tämä arvo on täytetty automaattisesti vakiomuotoisissa [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukoissa. Mukautetuille taulukoille on annettava tunnus.

3. Valitse **Tietokantatiedot**-toiminto. Liittyvän sivun sivu avautuu.
4. Tarkastele käytettävissä olevia tietoja Muokkaa sitä tarpeen mukaan poistamalla epäolennaiset tietueet tai lisäämällä uusia.  

## <a name="to-copy-data-from-a-test-environment-to-a-production-environment"></a>Tietojen kopioiminen testiympäristöstä tuotantoympäristöön

Kun olet tarkistanut ja testannut kaikki asetustiedot, voit jatkaa tietojen kopioimiseen tuotantoympäristöön. Luo uusi yritys samaan tietokantaan.

1. Avaa ja alusta uusi yritys.  
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määritystyökirja** ja valitse sitten liittyvä linkki.  
3. Valitse **Kopioi tiedot yrityksestä** -toiminto.  
4. Valitse **Kopioi yrityksen tiedot** -sivulla **Kopiointilähde**-kenttä. **Yritykset**-sivu avautuu.  
5. Valitse yritys, josta tiedot kopioidaan, ja valitse sitten **OK**-painike. Määritystyökirjassa valittujen taulukoiden luettelo tulee esiin. Tähän luetteloon sisältyvät vain ne taulukot, jotka sisältävät tietueita.
6. Valitse taulukot, joista haluat kopioida tietoja, ja valitse sitten **Kopioi tiedot** -toiminto. Valitse **Kopioi yrityksen tiedot** -sivulla **OK**.  

## <a name="see-also"></a>Katso myös

[Asiakastietojen siirtämisen valmisteleminen mallien avulla](admin-use-templates-to-prepare-customer-data-for-migration.md)  
[Asiakkaan asetusarvojen kerääminen](admin-gather-customer-setup-values.md)  
[Yrityksen konfiguroinnin määrittäminen](admin-set-up-company-configuration.md)  
[Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)  
