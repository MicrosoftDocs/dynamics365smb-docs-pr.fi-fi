---
title: Yhdistyneen kuningaskunnan ALV-ryhmän hallinnan laajennus
description: 'Voit olla yhteydessä muihin yrityksiin muodostaaksesi ALV-ryhmän, jonka kaikki jäsenet ilmoittavat ALV:n yhdessä palautuksessa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, value added tax, report'
ms.search.form: '4700, 4701, 4703, 4704, 4705, 4706, 4707, 4708, 4709,'
ms.date: 07/08/2022
ms.author: bholtorf
---

# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>Yhdistyneen kuningaskunnan ALV-ryhmän hallinnan laajennus

Voit yhdistää yhden tai useamman Yhdistyneessä kuningaskunnassa sijaitsevan yrityksen yhdistääksesi arvonlisäveron (ALV) raportoinnin yhdelle rekisteröintinumerolle. Tämäntyyppistä järjestelyä kutsutaan *ALV-ryhmäksi*. Voit pitää ryhmään yhteyttä jäsenenä tai ryhmän edustajana.

## <a name="forming-a-vat-group"></a>ALV-ryhmän muodostaminen

ALV-ryhmän jäsenet ja ryhmän edustaja voivat käyttää **Määritä ALV-ryhmän hallinta** -asetusten ohjattua määritysopasta määrittääkseen sitoutumisensa ryhmän kanssa ja luodakseen yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajiensa välille. Ryhmän jäsenet käyttävät tätä yhteyttä lähettääkseen ALV-palautuksensa ryhmän edustajalle. Tämän jälkeen ryhmän edustaja käyttää yhtä ALV-palautusta toimittaakseen ryhmän arvonlisäveron veroviranomaisille.

[!INCLUDE[prod_short](includes/prod_short.md)] tukee ryhmien välisiä ALV-palautuslähetyksiä yrityksissä, joissa käytetään [!INCLUDE[prod_short](includes/prod_short.md)]in paikallista versiota tai verkkoversiota missä tahansa yritysten väliseen viestintäkokoonpanoon vaikuttamassa yhdistelmässä. Tässä artikkelissa kuvataan eri ryhmäkokoonpanoja.

### <a name="license-requirements"></a>Lisenssivaatimukset

Ryhmän jäsenillä on oltava [!INCLUDE[prod_short](includes/prod_short.md)]-käyttöoikeus. Et voi käyttää vierastilejä ALV-ryhmissä.

* Käyttäjän täytyy olla täysi [!INCLUDE[prod_short](includes/prod_short.md)] -käyttäjä ALV-palautuksen laskemista ja lähettämistä varten.
* Tarvitset [!INCLUDE[prod_long](includes/prod_long.md)] -ryhmän jäsenen käyttöoikeuden sisäänkirjautumiseen ja perustehtävien suorittamiseen, kuten tilien luomiseen.

## <a name="set-up-a-vat-group"></a>Määritä ALV-ryhmä

Alla on suositeltu järjestys vaiheille, joita järjestelmänvalvoja käyttää ALV-ryhmän määrittämiseen:

1. Luo kokoonpano [ryhmän jäsenille Azure Active Directoryssa](#azure-active-directory-setup-for-group-members).
2. Jaa tekniset tiedot, jotka ALV-ryhmän jäsenet ja ryhmän edustaja tarvitsevat yhdistääkseen [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajansa. Tavallisesti ryhmän edustajalla on nämä tiedot, kuten [ohjelmointirajapinnan URL-osoite](#group-api-setup) ja sen ALV-ryhmän edustajan ympäristön nimi, johon ALV-ryhmän jäsenet lähettävät ALV-tietonsa.
3. Luo käyttäjät, joita ALV-ryhmän jäsenet käyttävät tunnistautumiseen, kun he muodostavat yhteyden ALV-ryhmän edustajan [!INCLUDE[prod_short](includes/prod_short.md)]iin. Käyttäjillä on oltava täydet käyttöoikeudet [!INCLUDE[prod_short](includes/prod_short.md)]en.
4. Yhdistä ALV-ryhmän jäsenet suorittamalla **Määritä ALV-ryhmän hallinnan** avustettu asetusopas.

   ALV-ryhmän edustajan täytyy luovuttaa tietyt tiedot ryhmän jäsenille, jotta he voivat viimeistellä asetukset. (Lisätietoja on [Määritä ALV-ryhmän jäsenet](#set-up-vat-group-members) -osiossa alla). Merkitse jokaisen ALV-ryhmän jäsenen **Ryhmän jäsenen tunnus** muistiin. Ryhmän edustaja tarvitsee nämä tunnukset lisätäkseen yritykset ALV-ryhmään.
5. Määritä ALV-ryhmän hallinnan laajennus ALV-ryhmän edustajan [!INCLUDE[prod_short](includes/prod_short.md)]issa käyttämällä **Määritä ALV-ryhmän hallinta** -asetusten ohjattua määritysopasta.

> [!NOTE]
> Muodostaakseen yhteyden ALV-ryhmän edustajaan, ryhmän jäsenillä on oltava käyttäjätili, jolla on ALV-ryhmän edustajan käyttöoikeus [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. ALV-ryhmän edustajan täytyy luoda vähintään yksi käyttäjä tätä tarkoitusta varten. Tietoturvasyistä suosittelemme kuitenkin, että he luovat käyttäjän jokaiselle ALV-ryhmän jäsenelle. Tämä käyttäjä voi olla järjestelmäkäyttäjä, jota ei ole liitetty kehenkään todelliseen henkilöön. Muista jakaa käyttäjien tunnistetiedot ALV-ryhmän jäsenille turvallisella tavalla.

### <a name="azure-active-directory-setup-for-group-members"></a>Azure Active Directory -asetukset ryhmän jäsenille

Kun ALV-ryhmän edustaja käyttää [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaa onlinessa tai paikallisesti, ALV-ryhmän jäsenten on käytettävä Azure Active Directorya käyttäjien todentamiseen, kun he lähettävät ALV-palautuksia ALV-ryhmän edustajalle. Paikallisen [!INCLUDE[prod_short](includes/prod_short.md)]n osalta jäsenten on määritettävä kertakirjautuminen. Lisätietoja on kohdassa [Azure Active Directory -todennuksen määrittäminen WS-Federation-tunnisteilla](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool).

Jos ALV-ryhmän jäsenet käyttävät myös [!INCLUDE[prod_short](includes/prod_short.md)]in verkkoversiota,, he voi tunnistautua käyttämällä heille kohdistettuja käyttäjätietoja ja ryhmän edustajan heille toimittamia kirjautumistietoja. Lisätietoja on [Määritä ALV-ryhmän jäsenet ](#set-up-vat-group-members) -osiossa alla.

alv-ryhmien jäsenten, jotka käyttävät [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaa paikallisesti, täytyy määrittää sovellusrekisteröinti Azure Active Directoryssä ALV-ryhmän edustajan [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajalle. Sovelluksen rekisteröinnin avulla alv-ryhmän edustajan [!INCLUDE[prod_short](includes/prod_short.md)] online-käyttäjä voi todentaa ryhmän jäsenen. Lisätietoja on kohdassa [Pika-aloitus: sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristössä](/azure/active-directory/develop/quickstart-register-app).

Kun ALV-ryhmän jäsenen järjestelmänvalvoja luo sovelluksen rekisteröinnin Azure Active Directoryssa, hänen täytyy määrittää seuraavat tiedot.

* Lisää **Todennus**-osiossa **Verkkosivusto** alustaksi ja käytä seuraavaa **Uudelleenohjauksen URL-osoite** -arvoa: `https://businesscentral.dynamics.com/OAuthLanding.htm`.
* Valitse **Tuetut tili tyypit** -kohdassa **Todennus**-osassa **tilit mistä tahansa organisaatiohakemistosta** (mikä tahansa Azure AD -hakemisto - palveluna tarjottava sovellus).
* **Luo sertifikaatit & salaisuudet** -osassa uusi asiakassalaisuus ja merkitse arvo muistiin. Alv-ryhmän jäsenet tarvitsevat salaisuuden, kun he muodostavat yhteyden ryhmän edustajaan.
* Lisää käyttöoikeudet **API-oikeudet**-osiossa [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. Ota käyttöön delegoitu käyttöoikeus kohteisiin **Financials.ReadWrite.All** ja **user_impersonation**.
* Huomioi **Sovelluksen (asiakkaan) tunnus** **Yhteenveto**-osassa. Alv-ryhmän jäsenet tarvitsevat tunnuksen, kun he muodostavat yhteyden ryhmän edustajaan.

### <a name="group-api-setup"></a>Ryhmän ohjelmointirajapinnan asetukset

ALV-ryhmän edustaja luo ja toimittaa ohjelmointirajapinnan ryhmän jäsenille. Jäsenet käyttävät tätä ohjelmointirajapintaa muodostaakseen yhteyden edustajan [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajaan ja ALV-palautusten lähettämiseen. ALV-ryhmän jäsenet käyttävät usein [!INCLUDE[prod_short](includes/prod_short.md)]:sta erillisissä Azure Active Directory -vuokraajissa. Tästä syystä ALV-ryhmän jäsenen ja edustajan [!INCLUDE[prod_short](includes/prod_short.md)]in yhdistäminen toisiinsa edellyttää määritystoimia.

> [!NOTE]
> Tämä edellyttää sellaisen järjestelmänvalvojatilin tunnistetietoja, jolla on [!INCLUDE[prod_short](includes/prod_short.md)]in täydet käyttöoikeudet.

1. Valitse edustajan vuokraajan Business Central -hallintakeskuksessa **Ympäristöt**-välilehti.
1. Valitse edustajan ympäristö.
1. Kopioi **URL**-osoite **Tiedot**-osasta.
1. Avaa Muistio ja liitä URL-osoite. Korvaa osoite `https://businesscentral.dynamics.com` osoitteella `https://api.businesscentral.dynamics.com/v2.0`.

## <a name="set-up-vat-group-members"></a>Määritä ALV-ryhmän jäsenet

ALV-ryhmän jäsenet muodostavat yhteyden edustajaan kutsumalla verkkopalvelua alv-ryhmän edustajan vuokraajalla. Kutsuja täytyy todentaa käyttämällä OAuth2-määritystä. Kun ALV-ryhmän hallinnan laajennus on määritetty, jäseniä pyydetään tunnistautumaan ALV-ryhmän edustajalle, jolloin käyttötunnussanoma luodaan ja tallennetaan. Tätä käyttötunnussanomaa käytetään alv-palautusten lähettämisen yhteydessä alv-ryhmän edustajalle.

> [!IMPORTANT]
> ALV-ryhmän jäsenyritysten ei tarvitse muodostaa yhteyttä HMRC:hen, koska ne tekevät ilmoitukset ryhmän edustajan välityksellä.

Ennen kuin ALV-ryhmän jäsenet aloittavat kokoonpanonsa määrittämisen (luetteloitu alla), heidän täytyy ottaa yhteyttä ALV-ryhmän edustajaan saadakseen seuraavat [!INCLUDE[prod_short](includes/prod_short.md)] -vuokralaistaan koskevat tiedot:

* Ohjelmointirajapinnan URL-osoite
* Yrityksen nimi
* Kirjaa käyttäjän tunnistetiedot

1. Valitse oikeasta yläkulmasta **Asetukset** ![Asetukset.](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") -kuvake ja valitse sitten **Asetusten ohjattu määritys** -toiminto.
2. Valitse **Määritä ALV-ryhmän hallinta** -toiminto.
3. Valitse **ALV-ryhmän rooli** -kentästä **Jäsen** ja valitse sitten **Seuraava**.
4. Kopioi **ryhmän jäsentunnus** -kentän arvo ja jaa se sitten alv-ryhmän edustajan kanssa, jotta he voivat lisätä yrityksesi ryhmän hyväksytyksi jäseneksi.
5. Määritä **Ryhmän edustajan tuoteversio** -kenttään edustajan käyttämä [!INCLUDE[prod_short](includes/prod_short.md)] -versio.
6. Syötä **Ohjelmointirajapinnan URL-osoite** -kenttään ALV-ryhmän edustajan antama ohjelmointirajapinnan URL-osoite. Yleensä URL-osoite muotoillaan seuraavasti: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Esimerkiksi, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.
7. Syötä **Ryhmän edustajan yritys** -kenttään ALV-ryhmän edustajan yrityksen nimi, esimerkiksi **CRONUS UK Ltd**.
8. Valitse **Todennustyyppi**-kentässä **OAuth2**-vaihtoehto. Jos ALV-ryhmän edustaja käyttää [!INCLUDE[prod_short](includes/prod_short.md)] Onlinea, ota **Ryhmän edustaja käyttää Business Central Onlinea** -valitsin käyttöön ja valitse sitten **Seuraava**.

   Noudata sitten [ALV-ryhmän edustaja käyttää Business Central Online -versiota](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online)- tai [ALV-ryhmän edustaja käyttää Business Central On-Premises -versiota](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premises) -osion ohjeita alta.

### <a name="vat-group-representative-uses-business-central-online"></a>ALV-ryhmän edustaja käyttää Business Central Online -versiota

1. Syötä ALV-ryhmän edustajan antamat tunnistetiedot ja lisää tarvittavat käyttöoikeudet luodaksesi käyttötunnussanoman.
2. Valitse ALV-raporttikokoonpano, jota käytät ALV-palautusten toimittamiseen Yhdistyneen kuningaskunnan veroviranomaisille. 

Kun olet suorittanut määritykset loppuun, [!INCLUDE[prod_short](includes/prod_short.md)] luo tämän valinnan perusteella uuden kokoonpanon, jolla voit lähettää ALV-palautuksia ALV-ryhmän edustajalle.

### <a name="vat-group-representative-uses-business-central-on-premises"></a>ALV-ryhmän edustaja käyttää Business Central On-Premises -versiota

1. Syötä ALV-ryhmän edustajan antamat tunnistetiedot ja valitse **Seuraava**.
2. Syötä **Asiakastunnus**-kenttään [Azure Active Directoryssa](#azure-active-directory-setup-for-group-members) suoritetun sovellusrekisteröinnin asiakastunnus.
3. Syötä **Asiakassalasana**-kenttään Azure Active Directoryssa suoritetun sovellusrekisteröinnin asiakassalasana.
4. Syötä **OAuth 2.0 Authority -päätepiste** -kenttään `https://login.microsoftonline.com/common/oauth2`.
5. Syötä **Syötä OAuth 2.0 Resource -URL-osoite** -kenttään `https://api.businesscentral.dynamics.com/`.
6. Syötä **OAuth 2.0 Redirect -URL-osoite** -kenttään `https://businesscentral.dynamics.com/OAuthLanding.htm`.
7. Kun olet määrittänyt eri kentät, valitse **Seuraava** ja vahvista todennusyhteys luodaksesi käyttötunnussanoman.
8. Valitse ALV-raporttikokoonpano, jota käytät ALV-palautusten toimittamiseen Yhdistyneen kuningaskunnan veroviranomaisille.

## <a name="set-up-the-vat-group-representative"></a>Määritä ALV-ryhmän edustaja

> [!NOTE]
> Paikallinen [!INCLUDE[prod_short](includes/prod_short.md)] tukee vain yhden vuokraajan esiintymää ryhmän edustajasta.

> [!IMPORTANT]
> Edustavan yrityksen on otettava käyttöön **HMRC VAT määritys** -palveluyhteys käyttöön **Palveluyhteydet**-sivulla. Edustajien on myös ladattava ALV-palautusjaksot HMRC:ltä.

1. Valitse oikeasta yläkulmasta **Asetukset**-kuvake ![Asetukset.](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") ja valitse sitten **Asetusten ohjattu määritys** -toiminto.
2. Valitse **Määritä ALV-ryhmän hallinta** -toiminto.
3. Valitse **ALV-ryhmän rooli** -kentästä **Edustaja**, joka toimii ALV-ryhmän edustajana, ja valitse sitten **Seuraava**.
4. Valitse **Ryhmän maksutili** -kentästä maksutili, jota käytetään ryhmän jäsenten ALV-summille. Tällä tilillä tulee olla **käyttöomaisuus** **tililuokkana**.
5. Määritä **ALV-maksutili**-kentässä tili, jota käytät ALV-maksuihin. Tällä tilillä tulee olla **Velat** **tililuokkana**.
6. Määritä **Erääntyvä ALV -ruudun numero** -kentässä ruutu, joka kuvaa ALV-ryhmän toimituksen erääntyvää ALV-kokonaissummaa.
7. Valitse **Ryhmän laskelman yleisen päiväkirjan malli** -kentästä yleisen päiväkirjan malli. Sitä käytetään luomaan asiakirja, jolla ryhmän edustaja kirjaa ryhmän arvonlisäveron maksutilille.
8. **Hyväksytyt jäsenet** -kentässä näkyy niiden ryhmän jäsenten määrä, jotka on määritetty toimittamaan ALV-palautuksia ryhmän edustajalle. Jos haluat lisätä uusia jäseniä, valitse numero avataksesi **ALV-ryhmän hyväksytyt jäsenet** -sivun ja lisää seuraavat tiedot:
    1. Syöt' **Ryhmän jäsenen tunnus** -kenttään ryhmän jäsenen tunnus, joka näytetään ryhmän jäsenen määritysten aikana (lisätietoja on [ALV-ryhmän jäsenasetukset](#set-up-vat-group-members) -osiossa yllä).
    2. Määritä **Ryhmän jäsenen nimi** -kentässä ryhmän jäsenen nimi.
    3. Määritä **Yritys**-kenttään yritys, josta ryhmän jäsen lähettää ALV-palautuksia [!INCLUDE[prod_short](includes/prod_short.md)]issa, kuten, **CRONUS UK Ltd**.
    4. Määritä yrityksen yhteystiedot.

## <a name="use-the-vat-group-management-features"></a>ALV-ryhmän hallintaominaisuuksien käyttäminen

ALV-ryhmän jäsenet käyttävät vakioprosesseja alv-palautusten valmisteluun. Ainoa ero on se, että jäsenten täytyy valita **ALV-palautus**-sivulta **VATGROUP**-raporttiversio lähettääkseen ALV-palautuksen ALV-ryhmän edustajalle viranomaisten sijaan. Lisätietoja on kohdassa [Tietoja ALV-palautusraportista](finance-how-report-vat.md#vatreturn).

> [!NOTE]
> ALV-ryhmän jäsenet voivat korjata lähetetyt alv-palautukset niin kauan kuin ryhmän edustaja ei ole vapauttanut konsernin ALV-tuottoa. Korjauksen tekemistä varten alv-ryhmän jäsenen täytyy luoda uusi ALV-palautus ALV-palautus jaksolle ja lähettää se alv-ryhmän edustajalle. ALV-ryhmän edustajan puolella jäsenen viimeisin ALV-palautus korvaa edellisen ja lisätään **ALV-palautus**-sivulle.

Seuraavissa osioissa kuvataan tehtävät, jotka ALV-ryhmän edustajien täytyy suorittaa kirjatakseen ryhmän ALV-palautuksen.

### <a name="review-vat-member-submissions"></a>Tarkasta ALV-ryhmän jäsenten lähetykset

**ALV-ryhmän lähetykset** -sivulla näkyvät jäsenten lähettämät alv-palautukset. Sivu toimii toimituksille luonnossijaintina, kunnes alv-ryhmän edustaja sisällyttää ne ryhmän ALV-palautukseen. Edustaja voi avata lähetykset tarkastaakseen yksittäiset ruudut, jotka sisältävät VAT-ryhmän kunkin jäsenen ilmoittaman summan.

> [!TIP]
> **ALV-palautusjaksot**-sivun **Ryhmän jäsenten lähetykset** -kenttä näyttää, kuinka monta palautusta jäsenet ovat lähettäneet. Varmista tämän luvun ajantasaisuus valitsemalla **Hae ALV-palautukset**-toiminto.

### <a name="create-a-group-vat-return"></a>Luo ryhmän ALV-palautus

Jos haluat raportoida ALV:n ryhmän puolesta, luo ALV-ilmoitus vain yrityksellesi **ALV-palautus**-sivulla. Sisällytä sen jälkeen viimeisimmät ALV-lähetykset alv-ryhmän jäseniltä valitsemalla **Sisällytä ryhmä-ALV** -toimenpiteeseen.  

Kun ryhmän edustaja on lähettänyt ryhmän ALV-ilmoituksen viranomaisille, hän suorittaa tavallisesti **Laske ja kirjaa ALV-laskelma** -toiminnon. Tämä toiminto sulkee avoimet ALV-tapahtumat ja siirtää summat ALV-maksutilille. Tällä hetkellä tämä toiminto ei ota huomioon ryhmälähetyksiä. Vain ALV-ryhmää edustavan yrityksen ALV-tapahtumat kirjataan. ALV-ryhmän jäsenten lähetyssummat tulee kirjata ALV-laskelman summaan manuaalisesti, jolloin ALV-ryhmän edustajan ALV-maksutili vastaa viranomaisilta raportoitujen vastuiden määrää. Tämä toimintatapa muuttuu [!INCLUDE[prod_short](includes/prod_short.md)]in tulevassa päivityksessä siten, että koko ryhmän ALV (ALV-palautuksen raporttirivien kokonaissumma) selvitetään.

> [!IMPORTANT]
> ALV-ryhmien toimintoa tuetaan vain niillä markkina-alueilla, joissa [!INCLUDE[prod_short](includes/prod_short.md)] käyttää ALV-palautuksista ja ALV-palautusjaksoista koostuvaa ALV-kehystä. Et voi käyttää ALV-ryhmiä markkina-alueilla, joilla on muita paikallisen ALV-raportoinnin toteutuksia, kuten Espanja, Italia, Itävalta, Saksa ja Sveitsi.

## <a name="see-also"></a>Katso myös

[Yhdistyneen kuningaskunnan paikallinen toiminnallisuus brittiversiossa](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Veron määrittäminen digitaaliseksi Yhdistyneessä Kuningaskunnassa](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  
[Määritä arvolisävero](finance-setup-vat.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  
[Usean yrityksen kirjanpitotietojen konsolidoiminen](finance-consolidated-company-reporting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
