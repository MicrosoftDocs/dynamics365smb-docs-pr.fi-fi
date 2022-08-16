---
title: Määritä hajautetut käyttöoikeudet
description: Tässä artikkelissa kuvataan, kuinka määritellään yksityiskohtaiset käyttöoikeudet ja määritetään kullekin käyttäjälle käyttöoikeusjoukot, joita he tarvitsevat työnsä suorittamiseen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 1, 119, 8930, 9800, 9807, 9808, 9830, 9831
ms.date: 07/27/2022
ms.author: edupont
ms.openlocfilehash: 2b5bba12afb2fbb05dbfd3240088c2726f5d8337
ms.sourcegitcommit: bb9b2b4e693fa326a13d94e5e83f60e6c7ac5b68
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227497"
---
# <a name="assign-permissions-to-users-and-groups"></a>Määritä käyttöoikeudet käyttäjille ja ryhmille

[!INCLUDE[prod_short](includes/prod_short.md)]-suojausjärjestelmä ohjaa, mitä objekteja käyttäjä voi käyttää kussakin tietokannassa tai ympäristössä yhdessä käyttäjän käyttöoikeuden kanssa. Voit määrittää jokaiselle käyttäjälle, voivatko he lukea, muokata tai syöttää tietoja valituissa tietokantaobjekteissa. Lisätietoja on [Tietosuoja](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level)-kohdassa [!INCLUDE[prod_short](includes/prod_short.md)]:n kehitys- ja hallintosisällössä.

Ennen kuin määrität käyttöoikeuksia käyttäjille ja käyttäjäryhmille, sinun täytyy määrittää, ketkä voivat kirjautua sisään luomalla käyttäjiä heidän käyttöoikeutensa mukaisesti. Katso lisätietoja kohdasta [Luo käyttäjiä lisenssien mukaan](ui-how-users-permissions.md).

[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa tietokantaobjektien käyttöoikeustasoja on kaksi:

- Käyttöoikeuden mukaiset yleiset käyttöoikeudet, joita kutsutaan myös oikeutuksisi.

  Käyttöoikeuksiin kuuluvat käyttöoikeuksien oletusjoukot. Vuoden 2022 julkaisuaallosta 1 alkaen järjestelmänvalvojat voivat mukauttaa näitä oletusoikeuksia asianmukaisille käyttöoikeustyypeille. Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen käyttöoikeuksien perusteella](ui-how-users-permissions.md#licensespermissions).  

- Yksityiskohtaisemmat käyttöoikeudet, jotka on määritetty [!INCLUDE[prod_short](includes/prod_short.md)]:n sisältä.

  Tässä artikkelissa kuvataan, miten voit määrittää, käyttää ja hakea käyttöoikeuksia kohteessa [!INCLUDE [prod_short](includes/prod_short.md)] oletusmääritysten muuttamiseksi.  

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]  
Lisätietoja hallintasisällössä: [Valtuutettu järjestelmänvalvojan käyttöoikeus Business Central Onlineen](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

[!INCLUDE [prod_short](includes/prod_short.md)] online sisältää oletuskäyttäjäryhmät, jotka on määritetty käyttäjille automaattisesti käyttöoikeuden perusteella. Voit muuttaa oletusmäärityksiä muuttamalla tai lisäämällä käyttäjäryhmiä, käyttöoikeuksien joukkoja ja käyttöoikeuksia. Seuraavassa taulukossa on esitelty oletuskäyttöoikeuksien muokkaamiseen liittyvät keskeiset skenaariot.  

|Tehtävä  |Katso  |
|---------|---------|
|Voit helpottaa useiden käyttäjien käyttöoikeuksien hallintaa järjestämällä ne käyttäjäryhmiin ja määrittämällä sitten yhden toiminnon useille käyttäjille yhden käyttöoikeusjoukon tai muuttamaan sitä.| [Käyttöoikeuksien hallinta käyttäjäryhmien avulla](#to-manage-permissions-through-user-groups) |
|Käyttöoikeuksien joukkojen hallinta tiettyjen käyttäjien osalta | [Käyttöoikeusjoukkojen määrittäminen käyttäjälle](#to-assign-permission-sets-to-users) |
|Lisätietoja käyttöoikeuksien joukon määrittämisestä|[Käyttöoikeusjoukon luominen tai muokkaaminen](#to-create-or-modify-a-permission-set)|
|Tiettyjen käyttöoikeuksien hallinta|[Käyttöoikeuksien luominen tai muokkaaminen manuaalisesti](#to-create-or-modify-permissions-manually)|
|Käyttäjän käyttöoikeuksien tarkasteleminen tai vianmääritys|[Yleiskuvan saaminen käyttöoikeuksista](#to-get-an-overview-of-a-users-permissions)|
|Tietoja tietuetason suojauksesta|[Suojaussuodattimet rajoittavat käyttäjän käyttöoikeuden tiettyihin taulukon tietueisiin](#security-filters-limit-a-users-access-to-specific-records-in-a-table)|

> [!NOTE]
> Lisätapa määrittää, mitä ominaisuuksia käyttäjällä on oikeus käyttää, on määrittää se **Kokemus**-kentässä **Yritystiedot**-sivulla. Lisätietoja on kohdassa [Näytettävien ominaisuuksien muuttaminen](ui-experiences.md).
>
> Voit määrittää mitä käyttäjät näkevät käyttöliittymässä ja miten he käyttävät sallittuja toimintoja sivuilla. Se tehdään profiilien avulla ja nämä määritetään eri käyttäjätyypeille heidän työnsä tai osastonsa mukaisten roolien mukaan. Lisätietoja on kohdissa [Profiilien hallinta](admin-users-profiles-roles.md) ja [[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen](ui-customizing-overview.md).

## <a name="to-manage-permissions-through-user-groups"></a>Käyttöoikeuksien hallinta käyttäjäryhmien avulla

Käyttäjäryhmät auttavat hallitsemaan koko yrityksen käyttöoikeuksien joukkoja. [!INCLUDE [prod_short](includes/prod_short.md)] online sisältää oletuskäyttäjäryhmät, jotka on määritetty käyttäjille automaattisesti käyttöoikeuden perusteella. Voit lisätä käyttäjiä käyttäjäryhmään manuaalisesti, ja voit luoda uusia käyttäjäryhmiä aiemmin luotujen käyttäjäryhmien kopioiksi.  

Aloitat luomalla käyttäjäryhmän. Sen jälkeen voit määrittää ryhmälle käyttöoikeuksien ryhmiä, jotka määrittävät, mitä objektia ryhmän käyttäjät voivat käyttää. Kun lisäät käyttäjän ryhmään, ryhmälle määritetyt käyttöoikeusjoukot koskevat käyttäjää.

Käyttäjän käyttäjäryhmän kautta määritetyt käyttöoikeusjoukot pysyvät synkronoituina. Käyttäjäryhmän käyttöoikeuksiin lisätään muutos automaattisesti käyttäjille. Jos poistat käyttäjän käyttäjäryhmästä, asiaan liittyvät käyttöoikeudet peruutetaan automaattisesti.

### <a name="to-add-users-to-a-user-group"></a>Käyttäjien lisääminen käyttäjäryhmään

Seuraavissa ohjeissa selitetään, miten käyttäjäryhmiä luodaan manuaalisesti. Lisätietoja käyttäjäryhmien luomisesta automaattisesti on kohdassa [Käyttäjäryhmän ja kaikkien sen käyttöoikeusjoukkojen kopioiminen](#to-copy-a-user-group-and-all-its-permission-sets).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjäryhmät** ja valitse sitten vastaava linkki.

    1. Vaihtoehtoisesti voit valita **Käyttäjät**-sivulla **Käyttäjäryhmät**-toiminnon.
2. Valitse **Käyttäjäryhmä**-sivulla **Käyttäjäryhmän jäsenet** -toiminto.
3. Valitse **Käyttäjäryhmän jäsenet** -sivulla **Lisää käyttäjät** -toiminto.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Käyttäjäryhmän ja sen kaikkien käyttöoikeuksien joukkojen kopioiminen

Voit määrittää uuden käyttäjäryhmän nopeasti kopioimalla kaikki käyttöoikeusjoukot aiemmin luodusta käyttäjäryhmästä uuteen käyttäjäryhmään.

> [!NOTE]
> Käyttäjäryhmän jäseniä ei kopioida uuteen käyttäjäryhmään. Heidät on lisättävä myöhemmin manuaalisesti. Lisätietoja on osassa [Käyttäjien lisääminen käyttäjäryhmään](#to-add-users-to-a-user-group).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjäryhmät** ja valitse sitten vastaava linkki.
2. Valitse ensin kopioitava käyttäjäryhmä ja sitten **Kopioi käyttäjäryhmä** -toiminto.
3. Anna **Uuden käyttäjäryhmän koodi** -kentässä ryhmälle nimi ja valitse sitten **OK**-painike.

Uusi käyttäjäryhmä lisätään **Käyttäjäryhmät**-sivulle. Aloita käyttäjien lisääminen. Lisätietoja on osassa [Käyttäjien lisääminen käyttäjäryhmään](#to-add-users-to-a-user-group).  

> [!IMPORTANT]
> Saat vahvistusvirheen, jos yrität kohdistaa käyttäjälle käyttäjäryhmää, joka viittaa poistetussa laajennuksessa määritettyyn käyttöoikeuksien joukkoon. Tämä johtuu siitä, että laajennuksen sovellustunnus vahvistetaan joka kerta, kun siihen viitataan. Jos haluat kohdistaa tämän käyttäjäryhmän käyttäjälle, voit joko asentaa laajennuksen uudelleen, poistaa poistetun laajennutuksen viittaukset käyttöoikeuksien joukosta tai poistaa käyttöoikeuksien joukon käyttäjäryhmästä.


### <a name="to-assign-permission-sets-to-user-groups"></a>Käyttöoikeuksien joukkojen määrittäminen käyttäjäryhmille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjäryhmät** ja valitse sitten vastaava linkki.
2. Valitse käyttäjäryhmä, jolle haluat määrittää käyttöoikeuden.  

    Kaikki käyttäjälle jo määritetyt käyttöoikeusjoukot **Käyttöoikeuksien joukot** -tietoruudussa.
3. Avaa **Käyttöoikeuksien joukot**-toiminto, jos haluat avata **Käyttöoikeuksien joukot** -sivun.
4. Täytä **Käyttöoikeuksien joukot** -sivulla uudella rivillä tarvittavat kentät.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>Käyttöoikeuksien joukon määrittäminen **Käyttöoikeuksien joukko käyttäjäryhmän mukaan** -sivulla

Seuraavassa kerrotaan, miten käyttöoikeuksien joukot määritetään käyttäjäryhmälle **Käyttöoikeuksien joukko käyttäjäryhmän mukaan** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.
2. Valitse **Käyttäjät**-sivulla sopiva käyttäjä ja valitse sitten **Käyttöoikeuksien joukko käyttäjäryhmän mukaan** -toiminto.
3. Valitse **Käyttöoikeuksien joukko käyttäjäryhmän mukaan** -sivulla sen käyttöoikeuksien joukon rivin **[käyttäjäryhmän nimi]**-kenttä, joka määritetään käyttäjäryhmälle.
4. Valitse **Kaikki käyttäjäryhmät** -valintaruutu, jos haluat määrittää käyttöoikeuksien joukon kaikille käyttäjäryhmille.

Voit myös määrittää käyttöoikeusjoukkoja suoraan käyttäjälle.

## <a name="to-assign-permission-sets-to-users"></a>Käyttöoikeusjoukkojen määrittäminen käyttäjälle

Käyttöoikeusjoukko on joukko tiettyjen tietokantaobjektien käyttöoikeuksia. Kaikille käyttäjille on määritettävä vähintään yksi käyttöoikeusjoukko, ennen kuin he voivat käyttää [!INCLUDE[prod_short](includes/prod_short.md)]ia.  

[!INCLUDE[prod_short](includes/prod_short.md)] -ratkaisu sisältää esimääritettyjä käyttöoikeuksien joukkoja, jotka Microsoft tai oma ratkaisutoimittajasi on lisännyt. Voit myös lisätä uusia käyttöoikeusjoukkoja, jotka on räätälöity organisaatiosi tarpeiden mukaan. Lisätietoja on [Käyttöoikeuksien joukon luominen tai muokkaaminen](#to-create-or-modify-a-permission-set) -osassa.

> [!NOTE]
> Jos et halua rajoittaa käyttäjän oikeuksia enempää kuin käyttöoikeussopimuksessa on jo määritetty, voit määrittää käyttäjälle erityisen käyttöoikeusjoukon nimeltä SUPER. Tämä käyttöoikeusjoukko varmistaa, että käyttäjä voi käyttää kaikkia lisenssissä määritettyjä objekteja.
>
> Käyttäjällä, jolla on olennainen käyttöoikeus ja SUPER-käyttöoikeusjoukko, on käyttöoikeustoimintoja enemmän kuin käyttäjillä, joilla on tiiminjäsenlisenssi ja SUPER-käyttöoikeusjoukko.

Voit määrittää käyttöoikeusjoukkoja käyttäjille kahdella seuraavalla tavalla:

- **Käyttäjän kortti** -sivulta valitsemalla käyttöoikeusjoukot käyttäjän määrittämistä varten.
- **Käyttöoikeusjoukko**-sivulta valitsemalla käyttäjät, joille käyttöoikeusjoukko on määritetty.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Käyttäjäoikeuksien joukon määrittäminen käyttäjän kortissa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.
2. Valitse käyttäjä, jolle haluat määrittää käyttöoikeuden.
Kaikki käyttäjälle jo määritetyt käyttöoikeusjoukot **Käyttöoikeuksien joukot** -tietoruudussa.
3. Avaa **Käyttäjän kortti** -sivu valitsemalla **Muokkaa** -toiminto.
4. Täytä **Käyttöoikeuksien joukot** -tietoruudun uudella rivillä tarvittavat kentät. Lisätietoja on kohdassa [Käyttöoikeuksien joukon luominen tai muokkaaminen](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Käyttöoikeuksien joukon määrittäminen Käyttöoikeuksien joukko käyttäjän mukaan -sivulla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.
2. Valitse **Käyttäjät**-sivulla **Käyttöoikeuksien joukko käyttäjän mukaan** -toiminto.
3. Valitse **Käyttöoikeuksien joukko käyttäjän mukaan** -sivulla sen käyttöoikeuksien joukon rivin **[käyttäjätunnus]**-valintaruutu, joka määritetään käyttäjälle.

    Valitse **Kaikki käyttäjät** -valintaruutu, jos haluat määrittää käyttöoikeuksien joukon kaikille käyttäjille.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Yleiskuvan saaminen käyttöoikeuksista

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.
2. Avaa asianmukaisen käyttäjän kortti.
3. Valitse **Voimassa olevat käyttöoikeudet** -toiminto.

    **Käyttöoikeudet**-osassa ovat kaikki tietokantaobjektit, joiden käyttöoikeus käyttäjällä on. Et voi muokata tätä osaa.

    **Käyttöoikeuksien joukon mukaan** -osassa ovat ne määritetyt käyttöoikeuksien joukot, joiden kautta käyttäjälle myönnetään käyttöoikeudet, käyttöoikeuksien joukon lähde ja tyyppi sekä erilaisten käyttöoikeustyyppien hyväksytty laajuus.

    Jokaisella **Käyttöoikeudet**-osan valitun rivin **Käyttöoikeuksien joukon mukaan** -osassa näytetään käyttöoikeuksien joukko tai joukot, joiden kautta käyttöoikeus myönnetään. Tässä osassa voit muokata arvoa kaikissa viidessä käyttöoikeustyyppien kentässä: **luku-**, **lisäys-**, **muokkaus-**, **poisto**- ja **suoritusoikeus**.

    > [!NOTE]  
    > Vain **Käyttäjän määrittämä** -tyyppisiä käyttöoikeuksien joukkoja voi muokata.
    >
    > Rivit, joiden lähde on oikeutus, ovat peräisin tilauslisenssistä. Oikeutuksen käyttöoikeusarvot korvaavat muiden käyttöoikeuksien joukkojen arvot, jos niillä on korkeampi luokitus. Muun kuin oikeuden käyttöoikeuksien joukon arvo, jonka luokitus on korkeampi kuin oikeutuksen liittyvän arvon luokitus, on suluissa. Tämä osoittaa, että se ei ole voimassa, koska oikeutus korvaa sen.
    >
    > Lisätietoja luokituksesta on kohdassa [Käyttöoikeuksien luominen tai muokkaaminen manuaalisesti](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

4. Voit muokata käyttöoikeuksien joukkoa valitsemalla **Käyttöoikeuksien joukon mukaan** -osan asianmukaisen käyttöoikeuksien joukon **Käyttäjän määrittämä** -tyyppisellä rivillä yksi viidestä käyttöoikeustyypin kentästä ja valitse siihen toinen arvo.

5. Voit muokata käyttöoikeuksien joukon yksittäisiä käyttöoikeuksia valitsemalla arvon **Käyttöoikeuksien joukko** -kentässä. **Käyttöoikeudet**-sivu avautuu. Seuraa kohdassa [Käyttöoikeuksien luominen tai muokkaaminen](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually) olevia ohjeita.  

> [!NOTE]  
> Kun muokkaat käyttöoikeuksien joukkoa, muutokset kohdistuvat myös niihin käyttäjiin, joille on määritetty käyttöoikeuksien joukko.

### <a name="security-filters-limit-a-users-access-to-specific-records-in-a-table"></a>Suojaussuodattimet rajoittavat käyttäjän käyttöoikeutta tiettyihin taulukon tietueisiin

[!INCLUDE[prod_short](includes/prod_short.md)]in tietuetason suojauksessa käyttäjän käyttöoikeus rajoitetaan taulukon tietoihin suojaussuodattimien avulla. Suojaussuodattimet luodaan taulukon tietojen perusteella. Suojaussuodatin kuvaa sitä taulukon tietuejoukkoa, jonka käyttöoikeus käyttäjällä on. Voit määrittää esimerkiksi, että käyttäjä saa lukea vain tietueita, joissa on tietoja tietystä asiakkaasta. Tällä tavoin käyttäjällä ei ole muiden asiakkaiden tietoja sisältävien tietueiden käyttöoikeutta. Lisätietoja on hallintasisällön kohdassa [Suojaussuodattimien käyttäminen](/dynamics365/business-central/dev-itpro/security/security-filters).


## <a name="to-create-or-modify-a-permission-set"></a>Käyttöoikeusjoukon luominen tai muokkaaminen

Käyttöoikeuksien joukot toimivat käyttöoikeuksien säilöinä. Niiden avulla voit helposti hallinnoida yhden tietueen useita käyttöoikeuksia.

> [!NOTE]  
> [!INCLUDE[prod_short](includes/prod_short.md)] -ratkaisu sisältää yleensä useita esimääritettyjä käyttöoikeuksien joukkoja, jotka Microsoft tai oma ohjelmistotoimittajasi on lisännyt. Näiden käyttöoikeuksien joukkojen tyyppi on **Järjestelmä** tai **Laajennus**. Käyttöoikeuksien joukkoja ja niihin kuuluvia käyttöoikeuksia, joiden tyyppi on jompikumpi edellä mainituista, ei voi luoda tai muokata. Voit kuitenkin kopioida ne ja määrittää omia käyttöoikeuksien joukkoja ja käyttöoikeuksia.
>
> Käyttäjien luomien uusien tai kopioina luotujen käyttöoikeuksien joukkojen tyyppi on **Käyttäjän määrittämä**. Niitä voi muokata.

### <a name="to-create-new-permission-set-from-scratch"></a>Uuden käyttöoikeusjoukon luominen tyhjästä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöoikeuksien joukot** ja valitse sitten vastaava linkki.
2. Voit luoda uuden käyttöoikeuksien joukon valitsemalla **Uusi**-toiminnon.
3. Täytä tarvittavat uuden rivin kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Kun olet luonut käyttöoikeuksien joukon, sinun täytyy lisätä todelliset käyttöoikeudet. Lisätietoja on kohdassa [Käyttöoikeuksien luominen tai muuttaminen manuaalisesti](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-copy-a-permission-set"></a>Käyttöoikeuksien joukon kopioiminen

Voit myös siirtää kopiointitoiminnolla kaikki toisen käyttöoikeuksien joukon käyttöoikeudet nopeasti uuteen käyttöoikeuksien joukkoon.

> [!NOTE]  
> Jos kopioimaasi järjestelmän käyttöoikeuksien joukkoa muutetaan, saat siitä ilmoituksen (valinnastasi riippuen). Tämän jälkeen voit määrittää, tuleeko muutokset kopioida tai kirjoittaa käyttäjän määrittämään käyttöoikeuksien joukkoon.

1. Valitse **Käyttöoikeuksien joukot** -sivulla kopioitavan käyttöoikeuksien joukon rivi. Valitse sitten **Kopioi käyttöoikeuksien joukko** -toiminto.
2. Määritä **Kopioi käyttöoikeuksien joukko** -sivulla uuden käyttöoikeuksien joukon nimi ja valitse sitten **OK**-painike.
3. Valitse **Ilmoita muutetusta käyttöoikeuksien joukosta** -valintaruutu, jos haluat ylläpitää alkuperäisen ja kopioidun käyttöoikeuksien joukon välistä linkkiä. Näin saat ilmoituksen, jos alkuperäisen käyttöoikeusjoukon nimi tai sisältö muuttuu tulevassa versiossa.

Uusi käyttöoikeuksien joukko, joka sisältää kaikki kopioidun käyttöoikeuksien joukon käyttöoikeudet, lisätään uutena rivinä **Käyttöoikeuksien joukot** -sivulla. Nyt voit muokata uuden käyttöoikeuksien joukon käyttöoikeuksia. 

> [!TIP]
> Kunkin tyypin rivit on lajiteltu aakkosjärjestykseen.

### <a name="to-export-and-import-a-permission-set"></a>Käyttöoikeusjoukon vieminen ja tuominen

Jos haluat määrittää käyttöoikeudet nopeasti, voit tuoda toisesta [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajasta viedyt käyttöoikeusjoukot.

Multivuokraaja-ympäristöissä käyttöoikeusjoukko tuodaan tietylle vuokralaiselle. Toisin sanoen tuonnin laajuus on *vuokralainen*.

1. Valitse Vuokraaja 1:ssä **Käyttöoikeuksien joukot** -sivulla vietävien käyttöoikeuksien joukon rivi tai rivit. Valitse sitten **Vie käyttöoikeuksien joukot** -toiminto.

    Tietokoneen latauskansioon luodaan XML-tiedosto. Oletusarvon mukaan sen nimi on *Export Permission Sets.xml*.

2. Valitse vuokralainen 2:n **Käyttöoikeuksien joukot** -sivulla **Tuo käyttöoikeuksien joukot** -toiminto.
3. Harkitse **Tuo käyttöoikeuksien joukot** -valintaikkunassa, haluatko yhdistää aiemmin luodut käyttöoikeuksien joukot uusien käyttöoikeuksien joukkojen kanssa XML-tiedostoon.

    Jos valitset **Päivitä aiemmin luodut käyttöoikeudet** -valintaruudun, aiemmin luodut käyttöoikeuksien joukot, joilla on sama nimi kuin XML-tiedostossa, yhdistetään tuotuihin käyttöoikeuksien joukkoihin.

    Jos et valitse **Päivitä aiemmin luodut käyttöoikeudet** -valintaruudun, aiemmin luodut käyttöoikeuksien joukot, joilla on sama nimi kuin XML-tiedostossa, ohitetaan tuonnin aikana. Tässä tapauksessa sinulle ilmoitetaan ohitettujen käyttöoikeuksien joukoista.

4. Etsi ja valitse tuotava XML-tiedosto **Tuo**-valintaikkunasivulta ja valitse sitten **Avaa**-toiminto.

Käyttöoikeusien joukot tuodaan.

## <a name="to-create-or-modify-permissions-manually"></a>Käyttöoikeuksien luominen tai muokkaaminen manuaalisesti

Työvaiheessa kerrotaan, miten käyttöoikeudet lisätään tai miten niitä muokataan manuaalisesti. Voit myös luoda käyttöoikeuksia automaattisesti käyttöliittymän toiminnoista. Lisätietoja on kohdassa [Käyttöoikeuksien luominen tai muokkaaminen toimia tallentamalla](ui-define-granular-permissions.md#to-create-or-modify-permissions-by-recording-your-actions).

> [!NOTE]
> Kun muokkaat käyttöoikeutta ja samalla liittyvää käyttöoikeuksien joukkoa, muutokset kohdistuvat myös niihin käyttäjiin, joille on määritetty käyttöoikeuksien joukko.

1. Valitse **Käyttöoikeuksien joukot** -sivulla käyttöoikeuksien joukon rivi. Valitse sitten **Käyttöoikeudet**-toiminto.
2. Luo **Käyttöoikeudet**-sivulla uusi rivi tai muokkaa olemassa olevan rivin kenttiä.

Voit valita kaikissa viidessä käyttöoikeustyyppien kentässä (**luku-**, **lisäys-**, **muokkaus-**, **poisto**- ja **suoritusoikeus**) yhden seuraavista kolmesta käyttöoikeusasetuksesta:

|Asetus|Description|Luokittelu|
|------|-----------|-------|
|**Kyllä**|Käyttäjä voi suorittaa kyseiselle objektille toiminnon.|Suurin|
|**Epäsuora**|Käyttäjä voi suorittaa kyseiselle objektille toiminnon, mutta vain toisen sellaisen liittyvän objektin kautta, jonka täydet käyttöoikeudet käyttäjällä on. Lisätietoja epäsuorista käyttöoikeuksista on kehitys- ja IT-ammattilaisten ohjeessa [Käyttöoikeudet-ominaisuus](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property)|Toiseksi korkein|
|**Tyhjä**|Käyttäjä voi suorittaa kyseiselle objektille toiminnon.|Pienin|

> [!IMPORTANT]
> Käytä harkintaa, kun määrität **Lisäysoikeus**- tai **Muokkausoikeus**-oikeuksia **9001-käyttäjäryhmän jäsenelle** tai **9003-käyttäjäryhmän käyttöoikeusjoukolle**. Kaikki käyttöoikeus joukkoon liitetyt käyttäjät voivat mahdollisesti määrittää itsensä muihin käyttäjäryhmiin, mikä puolestaan voi antaa heille tahattomia käyttöoikeuksia.

### <a name="example---indirect-permission"></a>Esimerkki - epäsuora käyttöoikeus

Voit määrittää epäsuoria käyttöoikeuksia, jos haluat käyttää objektia vain toisen objektin kautta.
Käyttäjällä voi olla esimerkiksi oikeus ajaa codeunit 80, myynti kirjattu. Codeunit Myynti kirjattu suorittaa useita tehtäviä, myös muokkaa taulukkoa 37, Ostorivi. Kun käyttäjä kirjaa myyntiasiakirjan, codeunitin Myynti kirjattu, [!INCLUDE[prod_short](includes/prod_short.md)] tarkistaa, onko käyttäjällä oikeus muokata Myyntirivi-taulukkoa. Jos ei, codeunit ei voi suorittaa tehtäviä ja käyttäjä saa virhesanoman. Tällöin codeunitin suorittaminen onnistuu.

Käyttäjällä ei kuitenkaan tarvitse olla Ostorivi-taulukon täysiä käyttöoikeuksia codeunitin suorittamiseksi. Jos käyttäjällä on Myyntirivi-taulukon epäsuorat käyttöoikeudet, codeunitin Myynti kirjattu suorittaminen onnistuu. Kun käyttäjällä on epäsuorat oikeudet, kyseinen käyttäjä voi muokata vain Ostorivi-taulukkoa suorittamalla codeunitin Myynti kirjattu tai toisen objektin, jolla on Ostorivi-taulukon muokkausoikeudet. Käyttäjä voi muokata Ostorivi-taulukkoa vain silloin, kun se tapahtuu tuetulla sovellusalueella. Käyttäjä ei voi suorittaa toimintoa vahingossa tai tahallaan muita menetelmiä käyttäen.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Käyttöoikeuksien luominen tai muokkaaminen toimia tallentamalla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöoikeuksien joukot** ja valitse sitten vastaava linkki.

    Vaihtoehtoisesti voit valita **Käyttäjät**-sivulla **Käyttöoikeuksien joukko** -toiminnon.
2. Valitse **Käyttöoikeuksien joukko** -sivulla **Uusi**-toiminto.
3. Täytä tarvittaessa uuden rivin kentät.
4. Valitse **Käyttöoikeudet**-toiminto.
5. Valitse **Käyttöoikeudet**-sivulla ensin **Kirjausoikeudet**-toiminto ja sitten **Aloita**-toiminto.

    Käynnistyvä tallennusprosessi aloittaa ja tallentaa kaikki käyttöliittymässä tekemäsi toimet.
6. Siirry niille [!INCLUDE[prod_short](includes/prod_short.md)]in sivulle ja niihin toimintoihin, joita haluat tämän käyttöoikeusjoukon käyttäjien käyttävän. Sinun on tehtävä ne tehtävät, joille haluat tallentaa käyttöoikeudet.
7. Kun tallennus on valmis, palaa **Käyttöoikeudet**-sivulle ja valitse sitten **Lopeta**-toiminto.
8. Lisää tallennetut käyttöoikeudet uuteen käyttöoikeusjoukkoon valitsemalla **Kyllä**.
9. Määritä jokaiselle tallennetun luettelon objektille, saavatko käyttäjät lisätä, muokata tai poistaa tietueita tallennetuissa taulukoissa.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>Voit poistaa vanhentuneet käyttöoikeudet kaikista käyttöoikeuksien joukoista seuraavasti.

1. Valitse **Käyttöoikeuksien joukot** -sivulla **Poista vanhentuneet käyttöoikeudet** -toiminto.

## <a name="to-set-up-user-time-constraints"></a>Määritä käyttäjän aikarajoitukset

Järjestelmänvalvojat voivat määrittää ajanjaksot, joina määritetyt käyttäjät voivat kirjata. Järjestelmänvalvojat voivat myös määrittää, kirjataanko järjestelmä lokiin, kuinka kauan käyttäjät ovat kirjautuneena sisään. Vastaavasti järjestelmänvalvojat voivat määrittää käyttäjille vastuupaikkoja. Lisätietoja on kohdassa [Vastuupaikkojen käyttäminen](inventory-responsibility-centers.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän määritys** ja valitse sitten vastaava linkki.
2. Valitse avautuvalla **Käyttäjäasetukset**-sivulla **Uusi**-toiminto.
3. Anna **Käyttäjätunnus**-kentässä käyttäjän tunnus tai valitse kenttä, jos haluat nähdä kaikki järjestelmässä tällä hetkellä olevat Windows-käyttäjät.
4. Täytä tarvittavat kentät.

## <a name="viewing-permission-changes-telemetry"></a>Käyttöoikeuksien muutosten telemetrian tarkasteleminen

Voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in lähettämään käyttöoikeuksiin tehdyt muutokset Application Insights -resurssiin Microsoft Azuressa. Sitteen Azure Monitorin avulla luot raportteja ja määrität hälytyksiä kerätyille tiedoille. Lisätietoja on [!INCLUDE[prod_short](includes/prod_short.md)]in kehittäjien ja järjestelmänvalvojan ohjeen seuraavissa artikkeleissa:

- [Telemetrian seuranta ja analysointi – Application Insightsin käyttöönotto](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Kentän seurannan telemetrian analysointi](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## <a name="delegated-admin-users"></a>Delegoidut järjestelmänvalvojakäyttäjät

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

## <a name="see-also"></a>Katso myös

[Luo käyttäjät käyttöoikeuksien mukaan](ui-how-users-permissions.md)  
[Profiilien hallinta](admin-users-profiles-roles.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen mukauttaminen](ui-customizing-overview.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Hallinta](admin-setup-and-administration.md)  
[Käyttäjien lisääminen Microsoft 365 for Businessiin](/microsoft-365/admin/add-users/add-users)  
[Turvallisuus ja suojaus Business Centralissa](/dynamics365/business-central/dev-itpro/security/security-and-protection) kohdassa Kehittäjä- ja IT-Pro -ohje  
[Telemetriatunnuksen määrittäminen käyttäjille](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]