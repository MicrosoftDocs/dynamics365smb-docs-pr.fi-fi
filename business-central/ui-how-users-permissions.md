---
title: Käyttöoikeuksien määrittäminen tai muokkaaminen | Microsoft Docs
description: Lisätietoja Office 365 -käyttäjien lisäämisestä Business Central -sovellukseen sekä käyttöoikeuksien ja suojausasetusten määrittämisestä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: e60b7d875ebd0a598908f37a59a49953c61479f1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795874"
---
# <a name="managing-users-and-permissions"></a>Käyttäjien ja käyttöoikeuksien hallinta
Käyttäjiä voi lisätä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin sen jälkeen, kun yrityksen Office 365:n järjestelmänvalvoja on ensin luonut käyttäjät Office 365:n hallintaportaalissa. Lisätietoja on kohdassa [Käyttäjien lisääminen Office 365 for Businessiin](https://aka.ms/CreateOffice365Users).

Kun käyttäjät on luotu Office 365:ssä, käyttäjätiedot voidaan tuoda [!INCLUDE[d365fin](includes/d365fin_md.md)]:n **Käyttäjät**-sivulle. Käyttäjille määritetään käyttöoikeusjoukot sen mukaan, mitä palvelupaketti on määritetty käyttäjälle Office 365:ssä. Lisätietoja käyttöoikeuksista on kohdassa [Microsoft Dynamics 365 Business Centralin käyttöoikeusopas](https://aka.ms/BusinessCentralLicensing).

Voit sitten määrittää käyttäjille käyttöoikeusjoukkoja, jotka määrittävät, mitä tietokantaobjekteja siten myös mitä käyttöliittymäelementtejä käyttäjät saavat käyttää ja missä yrityksissä niitä saa käyttää. Voit lisätä käyttäjiä käyttäjäryhmiin. Tämä helpottaa samojen käyttöoikeusjoukkojen määrittämistä useille käyttäjille.

Oikeussarja on joukko tietyn tietokannan objektien käyttöoikeuksia. Kaikille käyttäjille on määritettävä vähintään yksi käyttöoikeusjoukko, ennen kuin he voivat käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]ia.

Voit avata **Käyttäjän kortti** -sivulla **Voimassa olevat käyttöoikeudet** -sivun, jos haluat katsoa käyttäjän käyttöoikeudet ja käyttöoikeuksien joukot, joiden kautta ne on myönnetty. Tässä kohdassa voit myös muuttaa niiden käyttöoikeuksien joukkojen käyttöoikeuksien tietoja, joiden tyyppi on **Käyttäjän määrittämä**. Lisätietoja on kohdassa [Käyttäjän käyttöoikeuksien yleiskatsauksen hankkiminen](ui-how-users-permissions.md#to-get-an-overview-of-a-users-permissions).

Järjestelmänvalvojat voivat määrittää **Käyttäjäasetukset**-sivulla ajanjaksoja, joiden aikana määritetyt käyttäjät voivat tehdä kirjauksia. He voivat myös määrittää, kirjaako järjestelmä ajan, jonka käyttäjät olivat kirjautuneena.

Toinen järjestelmä, joka määrittää, mitä käyttäjät voivat käyttää Kokemus-asetuksissa. Lisätietoja on kohdassa [Näytettävien ominaisuuksien muuttaminen](ui-experiences.md).

## <a name="to-add-a-user-in-business-central"></a>Käyttäjän lisääminen Business Central -sovellukseen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Valitse **Hae käyttäjät Office 365:stä** -toiminto.

Kaikki uudet Office 365 -tilaukseen luodut käyttäjät lisätään **Käyttäjät**-sivulla.

## <a name="to-group-users-in-user-groups"></a>Käyttäjien ryhmittäminen käyttäjäryhmiin
Voit määrittää käyttäjäryhmiä auttamaan hallitsemaan oikeusryhmät käyttäjäryhmille yrityksessä.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjäryhmät** ja valitse sitten liittyvä linkki.
2. Vaihtoehtoisesti voit valita **Käyttäjät**-sivulla **Käyttäjäryhmät**-toiminnon.
3. Valitse **Käyttäjäryhmä**-sivulla **Käyttäjäryhmän jäsenet** -toiminto.
4. Valitse **Käyttäjäryhmän jäsenet** -sivulla **Lisää käyttäjät** -toiminto.

Kun käyttäjiä tai käyttäjäryhmiä, niihin on liitettävä käyttöoikeuksien joukot. Näin määritetään, mitä objekteja käyttäjä voi käyttää. Ensin on järjestettävä käyttöoikeuksien joukkojen asianmukaiset käyttöoikeudet. Lisätietoja on kohdassa [Käyttäjän käyttöoikeuksien yleiskatsauksen hankkiminen](ui-how-users-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Käyttäjäryhmän ja sen kaikkien käyttöoikeuksien joukkojen kopioiminen
Voit määrittää uuden käyttäjäryhmän nopeasti kopioimalla kaikki käyttöoikeusjoukot aiemmin luodusta käyttäjäryhmästä uuteen käyttäjäryhmään.

Käyttäjäryhmän jäseniä ei kopioida uuteen käyttäjäryhmään. Heidät on lisättävä myöhemmin manuaalisesti.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjäryhmät** ja valitse sitten liittyvä linkki.
2. Valitse ensin kopioitava käyttäjäryhmä ja sitten **Kopioi käyttäjäryhmä** -toiminto.
3. Anna **Uuden käyttäjäryhmän koodi** -kentässä ryhmälle nimi ja valitse sitten **OK**-painike.

Uusi käyttäjäryhmä lisätään **Käyttäjäryhmät**-sivulle. Aloita käyttäjien lisääminen. Lisätietoja on kohdassa [Käyttäjien ryhmittäminen käyttäjäryhmiin](ui-how-users-permissions.md#to-group-users-in-a-user-group).  

## <a name="to-set-up-user-time-constraints"></a>Määritä käyttäjän aikarajoitukset
Järjestelmänvalvojat voivat määrittää ajanjaksoja, joiden aikana määritetyt käyttäjät voivat tehdä kirjauksia. He voivat myös määrittää, kirjaako järjestelmä ajan, jonka käyttäjät olivat kirjautuneena. Järjestelmänvalvojat voivat myös määrittää käyttäjille vastuupaikkoja. Lisätietoja on kohdassa [Vastuupaikkojen käyttäminen](inventory-responsibility-centers.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Käyttäjäasetukset** ja valitse sitten liittyvä linkki.
2. Valitse avautuvalla **Käyttäjäasetukset**-sivulla **Uusi**-toiminto.
3. Anna **Käyttäjätunnus**-kentässä käyttäjän tunnus tai valitse kenttä, jos haluat nähdä kaikki järjestelmässä tällä hetkellä olevat Windows-käyttäjät.
4. Täytä tarvittavat kentät.

## <a name="to-create-or-modify-a-permission-set"></a>Käyttöoikeusjoukon luominen tai muokkaaminen
Käyttöoikeuksien joukot toimivat käyttöoikeuksien säilöinä. Niiden avulla voit helposti hallinnoida yhden tietueen useita käyttöoikeuksia. Kun käyttöoikeuksien joukko on luotu, sille on lisättävä todelliset käyttöoikeudet. Lisätietoja on kohdassa [Käyttöoikeuksien luominen tai muokkaaminen manuaalisesti](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).

> [!NOTE]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] -ratkaisu sisältää yleensä useita esimääritettyjä käyttöoikeuksien joukkoja, jotka Microsoft tai oma ohjelmistotoimittajasi on lisännyt. Näiden käyttöoikeuksien joukkojen tyyppi on **Järjestelmä** tai **Laajennus**. Käyttöoikeuksien joukkoja ja niihin kuuluvia käyttöoikeuksia, joiden tyyppi on jompikumpi edellä mainituista, ei voi luoda tai muokata. Voit kuitenkin kopioida ne ja määrittää omia käyttöoikeuksien joukkoja ja käyttöoikeuksia. <br /><br />
Käyttäjien luomien uusien tai kopioina luotujen käyttöoikeuksien joukkojen tyyppi on **Käyttäjän määrittämä**. Niitä voi muokata.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöoikeuksien joukot** ja valitse sitten liittyvä linkki.
2. Voit luoda uuden käyttöoikeuksien joukon valitsemalla **Uusi**-toiminnon.
3. Täytä tarvittavat uuden rivin kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-copy-a-permission-set"></a>Käyttöoikeuksien joukon kopioiminen
Kun luotu uusia käyttöoikeuksien joukkoja, voit siirtää kopiointitoiminnolla kaikki toisen käyttöoikeuksien joukon käyttöoikeudet nopeasti uuteen käyttöoikeuksien joukkoon.

> [!NOTE]  
> Jos kopioimaasi järjestelmän käyttöoikeuksien joukkoa muutetaan, saat siitä ilmoituksen (valinnastasi riippuen). Tämän jälkeen voit määrittää, tuleeko muutokset kopioida tai kirjoittaa käyttäjän määrittämään käyttöoikeuksien joukkoon.

1. Valitse **Käyttöoikeuksien joukot** -sivulla kopioitavan käyttöoikeuksien joukon rivi. Valitse sitten **Kopioi käyttöoikeuksien joukko** -toiminto.
2. Määritä **Kopioi käyttöoikeuksien joukko** -sivulla uuden käyttöoikeuksien joukon nimi ja valitse sitten **OK**-painike.
3. Valitse **Ilmoita muutetusta käyttöoikeuksien joukosta** -valintaruutu, jos haluat ylläpitää alkuperäisen ja kopioidun käyttöoikeuksien joukon välistä linkkiä. Tämän linkin avulla sinulle ilmoitetaan, jos alkuperäisen käyttöoikeuksien joukon nimeä tai sisältöä muutetaan tulevissa versioissa, joissa ratkaisu päivitetään.

Uusi käyttöoikeuksien joukko, joka sisältää kaikki kopioidun käyttöoikeuksien joukon käyttöoikeudet, lisätään uutena rivinä **Käyttöoikeuksien joukot** -sivulla. Huomaa, että kunkin tyypin rivit on lajiteltu aakkosjärjestykseen.

## <a name="to-create-or-modify-permissions-manually"></a>Käyttöoikeuksien luominen tai muokkaaminen manuaalisesti
Työvaiheessa kerrotaan, miten käyttöoikeudet lisätään tai miten niitä muokataan manuaalisesti. Voit myös luoda käyttöoikeuksien joukon automaattisesti käyttöliittymän toiminnoista. Lisätietoja on kohdassa [Käyttöoikeusjoukkojen luominen tai muokkaaminen toimia tallentamalla](ui-how-users-permissions.md#to-create-or-modify-permission-sets-by-recording-your-actions).

1. Valitse **Käyttöoikeuksien joukot** -sivulla käyttöoikeuksien joukon rivi. Valitse sitten **Käyttöoikeudet**-toiminto.
2. Luo **Käyttöoikeudet**-sivulla uusi rivi tai muokkaa olemassa olevan rivin kenttiä.

Voit valita kaikissa viidessä käyttöoikeustyyppien kentässä (**luku-**, **lisäys-**, **muokkaus-**, **poisto**- ja **suoritusoikeus**) yhden seuraavista kolmesta käyttöoikeusasetuksesta:

|Asetus|Description|Luokittelu|
|------|-----------|
|**Kyllä**|Käyttäjä voi suorittaa kyseiselle objektille toiminnon.|Suurin|
|**Epäsuora**|Käyttäjä voi suorittaa kyseiselle objektille toiminnon, mutta vain toisen sellaisen liittyvän objektin kautta, jonka täydet käyttöoikeudet käyttäjällä on.|Toiseksi korkein|
|**Tyhjä**|Käyttäjä ei voi suorittaa kyseiselle objektille toimintoa.|Pienin|

### <a name="example---indirect-permission"></a>Esimerkki - epäsuora käyttöoikeus
Voit määrittää epäsuoria käyttöoikeuksia, jos haluat käyttää objektia vain toisen objektin kautta.
Käyttäjällä voi olla esimerkiksi oikeus ajaa koodiyksikkö 80, myynti kirjattu. Codeunit Myynti kirjattu suorittaa useita tehtäviä, myös muokkaa taulukkoa 37, Ostorivi. Kun käyttäjä kirjaa myyntiasiakirjan, codeunitin Myynti kirjattu, [!INCLUDE[d365fin](includes/d365fin_md.md)] tarkistaa, onko käyttäjällä oikeus muokata Myyntirivi-taulukkoa. Jos ei, codeunit ei voi suorittaa tehtäviä ja käyttäjä saa virhesanoman. Tällöin koodiyksikön suorittaminen onnistuu.

Käyttäjällä ei kuitenkaan tarvitse olla Ostorivi-taulukon täysiä käyttöoikeuksia codeunitin suorittamiseksi. Jos käyttäjällä on Myyntirivi-taulukon epäsuorat käyttöoikeudet, codeunitin Myynti kirjattu suorittaminen onnistuu. Kun käyttäjällä on epäsuorat oikeudet, kyseinen käyttäjä voi muokata vain Ostorivi-taulukkoa suorittamalla codeunitin Myynti kirjattu tai toisen objektin, jolla on Ostorivi-taulukon muokkausoikeudet. Käyttäjä voi muokata Ostorivi-taulukkoa vain silloin, kun se tapahtuu tuetulla sovellusalueella. Käyttäjä ei voi suorittaa toimintoa vahingossa tai tahallaan muita menetelmiä käyttäen.

### <a name="to-limit-a-users-access-to-specific-records-in-a-table"></a>Käyttäjän käyttöoikeuden rajoittaminen tiettyihin taulukon tietueisiin
[!INCLUDE[d365fin](includes/d365fin_md.md)]in tietuetason suojauksessa käyttäjän käyttöoikeus rajoitetaan taulukon tietoihin suojaussuodattimien avulla. Suojaussuodattimet luodaan taulukon tietojen perusteella. Suojaussuodatin kuvaa sitä taulukon tietuejoukkoa, jonka käyttöoikeus käyttäjällä on. Voit määrittää esimerkiksi, että käyttäjä saa lukea vain tietueita, joissa on tietoja tietystä asiakkaasta. Tämä tarkoittaa, että käyttäjällä ei ole muiden asiakkaiden tietoja sisältävien tietueiden käyttöoikeutta. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeen kohdassa [Suojaussuodattimien käyttäminen](/dynamics365/business-central/dev-itpro/security/security-filters).


## <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Käyttöoikeusjoukkojen luominen tai muokkaaminen toimia tallentamalla
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöoikeuksien joukot** ja valitse sitten liittyvä linkki.
2.  Vaihtoehtoisesti voit valita **Käyttäjät**-sivulla **Käyttöoikeuksien joukko** -toiminnon.
3.  Valitse **Käyttöoikeuksien joukko** -sivulla **Uusi**-toiminto.
4.  Täytä tarvittaessa uuden rivin kentät.
5.  Valitse **Käyttöoikeudet**-toiminto.
6.  Valitse **Käyttöoikeudet**-sivulla ensin **Kirjausoikeudet**-toiminto ja sitten **Aloita**-toiminto.

    Käynnistyvä tallennusprosessi tallentaa kaikki käyttöliittymässä tekemäsi toimet.
7.  Siirry niille [!INCLUDE[d365fin](includes/d365fin_md.md)]in sivulle ja niihin toimintoihin, joita haluat tämän käyttöoikeusjoukon käyttäjien käyttävän. Sinun on tehtävä ne tehtävät, joille haluat tallentaa käyttöoikeudet.
8.  Kun tallennus on valmis, palaa **Käyttöoikeudet**-sivulle ja valitse sitten **Lopeta**-toiminto.
9.  Lisää tallennetut käyttöoikeudet uuteen käyttöoikeusjoukkoon valitsemalla **Kyllä**.
10. Määritä jokaiselle tallennetun luettelon objektille, saavatko käyttäjät lisätä, muokata tai poistaa tietueita tallennetuissa taulukoissa.

> [!NOTE]  
> Kun muokkaat käyttöoikeutta ja samalla liittyvää käyttöoikeuksien joukkoa, muutokset kohdistuvat myös niihin käyttäjiin, joille on määritetty käyttöoikeuksien joukko.

## <a name="to-assign-permission-sets-to-users-or-user-groups"></a>Käyttöoikeuksien joukkojen määrittäminen käyttäjille tai käyttäjäryhmille
Voit määrittää käyttöoikeuksia käyttäjille kahdella seuraavalla tavalla:
- Määritä käyttöoikeuksien joukot käyttäjän kortissa.
- Valitse **Käyttöoikeuksien joukko käyttäjän mukaan** -sivulla käyttäjän valintaruutu sarakkeessa ja liittyvän käyttöoikeuksien joukon valintaruutu rivillä.
    Näin voit määrittää myös käyttöoikeuksien joukkoja käyttäjäryhmille.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Käyttäjäoikeuksien joukon määrittäminen käyttäjän kortissa
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Valitse käyttäjä, jolle haluat määrittää käyttöoikeuden.
Kaikki käyttäjälle jo määritetyt käyttöoikeusjoukot **Käyttöoikeuksien joukot** -tietoruudussa.
3. Avaa **Käyttäjän kortti** -sivu valitsemalla **Muokkaa** -toiminto.
4. Täytä **Käyttöoikeuksien joukot** -tietoruudun uudella rivillä tarvittavat kentät. Lisätietoja on kohdassa [Käyttöoikeuksien joukon luominen tai muokkaaminen](ui-how-users-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Käyttöoikeuksien joukon määrittäminen **Käyttöoikeuksien joukko käyttäjän mukaan** -sivulla  
Seuraavassa kerrotaan, miten käyttöoikeuksien joukot määritetään käyttäjälle **Käyttöoikeuksien joukko käyttäjän mukaan** -sivulla. Vaiheet ovat samanlaisia kuin **Käyttöoikeuksien joukko käyttäjäryhmän mukaan** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Valitse **Käyttäjät**-sivulla sopiva käyttäjä ja valitse sitten **Käyttöoikeuksien joukko käyttäjän mukaan** -toiminto.
3. Valitse **Käyttöoikeuksien joukko käyttäjän mukaan** -sivulla sen käyttöoikeuksien joukon rivin **[käyttäjätunnus]**-valintaruutu, joka määritetään käyttäjälle.
4. Valitse **Kaikki käyttäjät** -valintaruutu, jos haluat määrittää käyttöoikeuksien joukon kaikille käyttäjille.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Yleiskuvan saaminen käyttöoikeuksista
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Avaa asianmukaisen käyttäjän kortti.
3. Valitse **Voimassa olevat käyttöoikeudet** -toiminto.

    **Käyttöoikeudet**-osassa ovat kaikki tietokantaobjektit, joiden käyttöoikeus käyttäjällä on. Et voi muokata tätä osaa.

    **Käyttöoikeuksien joukon mukaan** -osassa ovat ne määritetyt käyttöoikeuksien joukot, joiden kautta käyttäjälle myönnetään käyttöoikeudet, käyttöoikeuksien joukon lähde ja tyyppi sekä erilaisten käyttöoikeustyyppien hyväksytty laajuus.

    Jokaisella **Käyttöoikeudet**-osan valitun rivin **Käyttöoikeuksien joukon mukaan** -osassa näytetään käyttöoikeuksien joukko tai joukot, joiden kautta käyttöoikeus myönnetään. Tässä osassa voit muokata arvoa kaikissa viidessä käyttöoikeustyyppien kentässä: **luku-**, **lisäys-**, **muokkaus-**, **poisto**- ja **suoritusoikeus**.   

    > [!NOTE]  
    > Vain **Käyttäjän määrittämä** -tyyppisiä käyttöoikeuksien joukkoja voi muokata.<br /><br />
    > Rivit, joiden lähde on oikeutus, ovat peräisin tilaussuunnitelmasta. Oikeutuksen käyttöoikeusarvot korvaavat muiden käyttöoikeuksien joukkojen arvot, jos niillä on korkeampi luokitus. Muun kuin oikeuden käyttöoikeuksien joukon arvo, jonka luokitus on korkeampi kuin oikeutuksen liittyvän arvon luokitus, on suluissa. Tämä osoittaa, että se ei ole voimassa, koska oikeutus korvaa sen. Lisätietoja luokituksesta on kohdassa [Käyttöoikeuksien luominen tai muokkaaminen manuaalisesti](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).  

4. Voit muokata käyttöoikeuksien joukkoa valitsemalla **Käyttöoikeuksien joukon mukaan** -osan asianmukaisen käyttöoikeuksien joukon **Käyttäjän määrittämä** -tyyppisellä rivillä yksi viidestä käyttöoikeustyypin kentästä ja valitse siihen toinen arvo.

5. Voit muokata käyttöoikeuksien joukon yksittäisiä käyttöoikeuksia valitsemalla arvon **Käyttöoikeuksien joukko** -kentässä. **Käyttöoikeudet**-sivu avautuu. Seuraa kohdassa [Käyttöoikeuksien luominen tai muokkaaminen](ui-how-users-permissions.md#to-create-or-modify-permissions-manually) olevia ohjeita.  

> [!NOTE]  
> Kun muokkaat käyttöoikeuksien joukkoa, muutokset kohdistuvat myös niihin käyttäjiin, joille on määritetty käyttöoikeuksien joukko.

## <a name="see-also"></a>Katso myös
[Business Centralin tietoturva ja suojaus](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Tietoja käyttäjistä, profiileista ja roolikeskuksista](admin-users-profiles-roles.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Hallinta](admin-setup-and-administration.md)  
[Käyttäjien lisääminen Office 365 for Businessiin](https://aka.ms/CreateOffice365Users)  
[Microsoft Dynamics 365 Business Centralin käyttöoikeusopas](https://aka.ms/BusinessCentralLicensing)
