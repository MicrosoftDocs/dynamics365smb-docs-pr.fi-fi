---
title: Yhdistyneen kuningaskunnan ALV-ryhmän hallinnan laajennus
description: Voit olla yhteydessä muihin yrityksiin muodostaaksesi ALV-ryhmän, jonka kaikki jäsenet ilmoittavat ALV:n yhdessä palautuksessa.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, value added tax, report
ms.search.forms: ''
ms.date: 05/24/2022
ms.author: bholtorf
ms.openlocfilehash: c5757a78a44e3cdc2f6100c42b5105734928837b
ms.sourcegitcommit: 7a6efcbae293c024ca4f6622c82886decf86c176
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/02/2022
ms.locfileid: "8841918"
---
# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>Yhdistyneen kuningaskunnan ALV-ryhmän hallinnan laajennus

Voit yhdistää yhden tai useamman maasi yrityksen yhdistääksesi ALV-raportoinnin yhdelle rekisteröintinumerolle. Tämäntyyppistä järjestelyä kutsutaan *ALV-ryhmäksi*. Voit sitoutua ryhmään jäsenenä tai ryhmän edustajana.

## <a name="forming-a-vat-group"></a>ALV-ryhmän muodostaminen
ALV-ryhmän jäsenet ja ryhmän edustaja voivat käyttää **ALV-ryhmän hallinnan asetukset** -asetusopasta määrittääkseen niiden sitoutumisen ryhmään ja luomalla yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajien välille. Ryhmän jäsenet käyttävät yhteyttä lähettäessään ALV-palautuksia ryhmän edustajalle. Edustaja käyttää yhtä ALV-palautusta toimittaakseen arvonlisäveron veroviranomaisille ryhmän puolesta. 

## <a name="license-requirements"></a>Lisenssivaatimukset
Ryhmän jäsenillä on oltava [!INCLUDE[prod_short](includes/prod_short.md)]-käyttöoikeus. Et voi käyttää vierastilejä ALV-ryhmissä. 

* Laskeakseen ja toimittaakseen ALV-palautuksia käyttäjän on oltava Business Centralin täysi käyttäjä.
* Kirjautumiseen ja perustason tehtävien suorittamiseen, kuten tilien luomiseen, tarvitaan Dynamics 365 Business Centralin ryhmän jäsenen käyttöoikeus.

## <a name="vat-group-constellations"></a>ALV-ryhmän joukko
Yhteydenpito tapahtuu ryhmän jäseniltä edustajalle. Ryhmän edustaja paljastaa API URL -osoitteen, jonka avulla jäsenet voivat lähettää ALV-palautuksia ALV-ryhmän edustajalle. 
[!INCLUDE[prod_short](includes/prod_short.md)] tukee ryhmien välisiä ALV-palautuslähetyksiä yrityksissä, joissa käytetään [!INCLUDE[prod_short](includes/prod_short.md)]:n paikallista tai online-tilaa, ja missä tahansa yhdistelmässä. Tiedonsiirron asetukset määräytyvät konstellaation mukaan. Tässä artikkelissa kuvataan eri ryhmäkokoonpanoja.

Seuraavassa luettelossa on esitetty alv-ryhmän määritysvaiheiden suositeltava järjestys:

1. Luo asetukset Azure Active Directoryssä. Lisätietoja on kohdassa [Todennusvaatimukset](ui-extensions-vat-group.md#requirements-for-authentication).
2. Jaa tekniset tiedot, jotka alv-ryhmän jäsenet ja edustaja tarvitsevat yhteyden muodostamiseen [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajille. Yleensä alv-ryhmän edustajalla on nämä tiedot, esimerkiksi sen alv-ryhmän edustavan ympäristön nimi, johon alv-ryhmän jäsenet lähettävät ALV:n.
3. Luo käyttäjät, joita ALV-ryhmän jäsenet voivat käyttää tunnistautumiseen, kun he luovat yhteyden ALV-ryhmän edustajan [!INCLUDE[prod_short](includes/prod_short.md)]en. Käyttäjillä on oltava täydet käyttöoikeudet [!INCLUDE[prod_short](includes/prod_short.md)]en.
4. Yhdistä ALV-ryhmän jäsenet suorittamalla **Määritä ALV-ryhmän hallinnan** avustettu asetusopas.

  Opas vaatii joitakin tietoja alv-ryhmän edustajalta. Lisätietoja on kohdassa [Määritä ALV-ryhmän jäsenet](#set-up-vat-group-members). Merkitse muistiin kunkin alv-ryhmän jäsenen **ryhmäjäsentunnus**. Edustaja tarvitsee näitä tunnuksia lisätäksesi yritykset alv-ryhmään.
5. Määritä ALV-ryhmän hallinnan laajennus ALV-ryhmän edustajan [!INCLUDE[prod_short](includes/prod_short.md)] -kohdassa **Määritä ALV-ryhmän hallinnan** avusteinen asetusopas -toiminnon avulla. 

> [!NOTE]
> Muodostaakseen yhteyden ALV-ryhmän edustajaan, ryhmän jäsenillä on oltava käyttäjätili, jolla on ALV-ryhmän edustajan käyttöoikeus [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. ALV-ryhmän edustajan on kuitenkin luotava vähintään yksi käyttäjä suojaussyistä, mutta suosittelemme, että luot käyttäjän kullekin alv-ryhmän jäsenelle. Varmista, että jaat näiden käyttäjien tunnistetiedot alv-ryhmän jäsenille turvallisella tavalla. Tämä on järjestelmän käyttäjätili, joka ei liity todelliseen henkilöön.

## <a name="about-the-vat-group-management-setup"></a>Tietoja ALV-ryhmän hallinnan asetuksista

ALV-ryhmän edustaja näyttää ryhmän jäsenille ohjelmointirajapinnan. Jäsenet käyttävät ohjelmointirajapintaa yhteyden muodostamiseen edustajan [!INCLUDE[prod_short](includes/prod_short.md)]-vuokraajalle ja lähettävät ALV-palautukset. ALV-ryhmän jäsenet käyttävät usein [!INCLUDE[prod_short](includes/prod_short.md)]:sta erillisissä Azure Active Directory -vuokraajissa. Tämän vuoksi asetuksia tarvitaan ALV-ryhmän jäsenen ja edustajan [!INCLUDE[prod_short](includes/prod_short.md)]n välisen yhteyden luomiseen. 
  
ALV-ryhmän jäsenet muodostavat yhteyden edustajaan kutsumalla verkkopalvelua alv-ryhmän edustajan vuokraajalla. Kutsuja täytyy todentaa käyttämällä OAuth2-määritystä. Kun alv-ryhmän hallinnan laajennus on määritetty, ohjelma pyytää todentamaan sen ALV-ryhmän edustajalle, jotta hän voi hakea ja tallentaa käyttötunnussanoman. Tätä käyttötunnussanomaa käytetään alv-palautusten lähettämisen yhteydessä alv-ryhmän edustajalle. 

## <a name="construct-the-api-url"></a>API URL:n kokoaminen
1. Valitse edustajan vuokraajan Business Central -hallintakeskuksessa **Ympäristöt**-välilehti.
2. Kopioi **URL**-osoite **Tiedot**-osasta.
3. Avaa Muistio ja liitä URL-osoite. Korvaa osoite **https://businesscentral.dynamics.com** osoitteella **https://api.businesscentral.dynamics.com/v2.0**.

## <a name="requirements-for-authentication"></a>Todennusta koskevat vaatimukset 
> [!NOTE]
> Tämä edellyttää sellaisen järjestelmänvalvojatilin tunnistetietoja, jolla on täydet [!INCLUDE[prod_short](includes/prod_short.md)]n käyttöoikeudet.

Kun ALV-ryhmän edustaja käyttää [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaa onlinessa tai paikallisesti, ALV-ryhmän jäsenten on käytettävä Azure Active Directorya käyttäjien todentamiseen, kun he lähettävät ALV-palautuksia ALV-ryhmän edustajalle. Paikallisen [!INCLUDE[prod_short](includes/prod_short.md)]n osalta jäsenten on määritettävä kertakirjautuminen. Lisätietoja on kohdassa [Azure Active Directory -todennuksen määritys WS-Federation-tunnisteilla](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool). Jos myös alv-ryhmän jäsenet käyttävät [!INCLUDE[prod_short](includes/prod_short.md)]:n online-ominaisuutta, alv-ryhmän jäsen voi todentaa käyttämällä nimettyjä käyttäjätietoja ja päätepisteen tietoja. Lisätietoja on kohdassa [Määritä ALV-ryhmän jäsenet](ui-extensions-vat-group.md#set-up-vat-group-members).

alv-ryhmien jäsenten, jotka käyttävät [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaa paikallisesti, täytyy määrittää sovellusrekisteröinti Azure Active Directoryssä ALV-ryhmän edustajan [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajalle. Sovelluksen rekisteröinnin avulla alv-ryhmän edustajan [!INCLUDE[prod_short](includes/prod_short.md)] online-käyttäjä voi todentaa ryhmän jäsenen. Lisätietoja on kohdassa [Pika-aloitus: sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristössä](/azure/active-directory/develop/quickstart-register-app).

Kun luot sovelluksen rekisteröinnin Azure Active Directory -ohjelmassa, sinun täytyy määrittää seuraavat tiedot.

* Lisää **Todennus**-osassa **Verkkosivusto** alustaksi ja käytä seuraavaa **Uudelleenohjauksen URL-osoitetta**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* Valitse **Tuetut tili tyypit** -kohdassa **Todennus**-osassa **tilit mistä tahansa organisaatiohakemistosta** (mikä tahansa Azure AD -hakemisto - palveluna tarjottava sovellus).
* **Luo sertifikaatit & salaisuudet** -osassa uusi asiakassalaisuus ja merkitse arvo muistiin. Alv-ryhmän jäsenet tarvitsevat salaisuuden, kun he muodostavat yhteyden ryhmän edustajaan.
* Lisää käyttöoikeudet **API-oikeudet**-osiossa [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. Ota käyttöön delegoitu käyttöoikeus kohteisiin **Financials.ReadWrite.All** ja **user_impersonation**.
* Huomioi **Sovelluksen (asiakkaan) tunnus** **Yhteenveto**-osassa. Alv-ryhmän jäsenet tarvitsevat tunnuksen, kun he muodostavat yhteyden ryhmän edustajaan. 

## <a name="set-up-vat-group-members"></a>Määritä ALV-ryhmän jäsenet
> [!IMPORTANT]
> ALV-ryhmän jäsenyritysten ei tarvitse muodostaa yhteyttä HMRC:hen, koska ne tekevät ilmoitukset ryhmän edustajan välityksellä.

Ennen kuin aloitat, ota yhteyttä alv-ryhmän edustajaan seuraavien [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajan tietojen osalta:

* Ohjelmointirajapinnan URL-osoite
* Yrityksen nimi 
* Asiakasohjelman tunnus
* Asiakasohjelman salaisuus
* Kirjaa käyttäjän tunnistetiedot 

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Määritä ALV-ryhmän hallinta** ja valitse sitten vastaava linkki.
2. Määritä **ALV-ryhmän rooli** -kentässä, oletko ryhmän jäsen vai ryhmän edustaja. Valitse **Jäsen**, jos haluat toimia ryhmän jäsenenä ja lähettää ALV-palautuksesi veroviranomaisen sijasta ryhmän edustajalle, ja valitse sitten **Seuraava**.
3. Kopioi **ryhmän jäsentunnus** -kentän arvo ja jaa se sitten alv-ryhmän edustajan kanssa, jotta he voivat lisätä yrityksesi ryhmän hyväksytyksi jäseneksi.
4. Määritä **Ryhmän edustajan tuoteversio** -kentässä edustajan käyttämä [!INCLUDE[prod_short](includes/prod_short.md)]n versio.
5. Syötä ALV-ryhmän edustajan yrityksen nimi **Ryhmän edustajan yritys** -kenttään. Esimerkiksi **CRONUS UK Ltd**.
6. Valitse **Todennustyyppi**-kentässä **OAuth2**-vaihtoehto. Jos ALV-ryhmän edustaja käyttää [!INCLUDE[prod_short](includes/prod_short.md)] onlinea, määritä, että **Ryhmän edustaja käyttää Business Central Onlinea** ja valitse sitten **Seuraava**. Riippuen siitä, käyttääkö edustaja [!INCLUDE[prod_short](includes/prod_short.md)], verkko- vai paikallista versiota, noudata joko osan [ALV-ryhmän edustaja käyttää Business Central Onlinea](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) tai [ALV-ryhmän edustaja käyttää Business Central On-Premesisiä](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premesis) ohjeita.

### <a name="vat-group-representative-uses-business-central-online"></a>ALV-ryhmän edustaja käyttää Business Central Onlinea
1. Syötä ALV-ryhmän edustajan antamat tunnistetiedot ja lisää tarvittavat käyttöoikeudet.
2. Valitse ALV-raportin määritys, jota tällä hetkellä käytetään ALV-palautusten toimittamisen veroviranomaisille. Kun olet tehnyt määritykset, [!INCLUDE[prod_short](includes/prod_short.md)] luo uuden määrityksen tämän valinnan perusteella ja käyttää määritystä ALV-palautusten lähettämiseen ALV-ryhmän edustajalle.  
3. Lisää **API-URL-osoite** ALV-ryhmän edustajalle. Yleensä URL-osoite muotoillaan seuraavasti: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Esimerkiksi, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.

### <a name="vat-group-representative-uses-business-central-on-premesis"></a>ALV-ryhmän edustaja käyttää Business Central On-Premisisiä
1. Syötä **Asiakastunnus**-kenttään Azure Active Directoryssa suoritetun sovellusrekisteröinnin asiakastunnus.
2. Syötä **Asiakassalasana**-kenttään Azure Active Directoryssa suoritetun sovellusrekisteröinnin asiakassalasana.
3. Syötä **OAuth 2.0 Authority -päätepiste** -kenttään `https://login.microsoftonline.com/common/oauth2`.
4. Syötä **Syötä OAuth 2.0 Resource -URL-osoite** -kenttään `https://api.businesscentral.dynamics.com/`.
5. Syötä **OAuth 2.0 Redirect -URL-osoite** -kenttään `https://businesscentral.dynamics.com/OAuthLanding.htm`.
6. Kun olet määrittänyt eri kentät, valitse **Seuraava** ja syötä sitten käyttäjätiedot, jotka alv-ryhmän edustaja on toimittanut.
7. Valitse alv-raporttikonfiguraatio, jonka avulla ALV raportoidaan maasi viranomaisille.

## <a name="set-up-the-vat-group-representative"></a>ALV-ryhmän edustajan määrittäminen
> [!NOTE]
> Paikallisessa käytössä tuemme vain yhden vuokraajan esiintymää ryhmän edustajasta.

> [!IMPORTANT]
> Edustavan yrityksen on otettava käyttöön **HMRC VAT määritys** -palveluyhteys käyttöön **Palveluyhteydet**-sivulla. Edustajien on myös ladattava ALV-palautusjaksot HMRC:ltä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Määritä ALV-ryhmän hallinta** ja valitse sitten vastaava linkki.
2. Määritä **ALV-ryhmän rooli** -kentässä, oletko ryhmän jäsen vai ryhmän edustaja. Valitse **Edustaja**, jos haluat toimia ALV-ryhmän edustajana ja lähettää ALV-palautukset ryhmän puolesta ja valitse sitten **Seuraava**.
3. Määritä **ALV-maksutili**-kentässä tili, jota käytät ALV-maksuihin.
4. Määritä **Erääntyvä ALV -ruudun numero** -kentässä ruutu, joka kuvaa ALV-ryhmän toimituksen erääntyvää ALV-kokonaissummaa.
5. Määritä **Ryhmämaksun yleisen päiväkirjan malli** -kentässä yleisen päiväkirjan malli, jota on käytetty siinä asiakirjassa, jolla ryhmän ALV on siirretty maksutilille.
6. **Hyväksytyt jäsenet** -kentässä näkyy niiden ryhmän jäsenten määrä, jotka on määritetty toimittamaan ALV-palautuksia edustajalle. Voit lisätä uusia jäseniä valitsemalla heidän määränsä, jolloin **Hyväksytyt jäsenet** -sivu avautuu.
7. Lisää uusia jäseniä lisäämällä seuraavat tiedot **ALV-ryhmän hyväksytyt jäsenet** -sivulle:
    1. Määritä **Ryhmän jäsenen tunnus** -kentässä ryhmän jäsenen tunnus.
    2. Määritä **Ryhmän jäsenen nimi** -kentässä ryhmän jäsenen nimi. 
    3. Määritä **Yritys**-kentässä se yritys, jolta ryhmän jäsen lähettää ALV-palautuksia [!INCLUDE[prod_short](includes/prod_short.md)]ssa. Esimerkiksi **CRONUS UK Ltd**.
    4. Määritä yrityksen yhteystiedot.

## <a name="use-the-vat-group-management-features"></a>ALV-ryhmän hallintaominaisuuksien käyttäminen
ALV-ryhmän jäsenet käyttävät vakioprosesseja alv-palautusten valmisteluun. Ainoa ero on, että valitaan **VATGROUP**-raporttiversio, joka lähettää ALV-palautuksen alv-ryhmän edustajalle eikä viranomaisille. Lisätietoja on kohdassa [Tietoja ALV-palautusraportista](finance-how-report-vat.md#vatreturn).

Seuraavissa osissa kuvataan tehtävät, jotka alv-ryhmän edustajien on suoritettava.

### <a name="vat-group-submissions"></a>ALV-ryhmän lähetykset

**ALV-ryhmän lähetykset** -sivulla näkyvät jäsenten lähettämät alv-palautukset. Sivu toimii toimituksille luonnossijaintina, kunnes alv-ryhmän edustaja sisällyttää ne ryhmän ALV-palautukseen. Voit avata lähetykset ja tarkistaa ALV-ilmoituksen niiden yksittäisten ruutujen osalta, jotka alv-ryhmän jäsen on ilmoittanut. 

> [!TIP]
> **ALV-palautusjaksot**-sivun **Ryhmän jäsenten lähetykset** -kentässä näkyy, kuinka monta palautusta jäsenet ovat lähettäneet. Varmista tämän luvun ajantasaisuus valitsemalla **Hae ALV-palautukset**-toiminto.

### <a name="creating-a-group-vat-return"></a>Ryhmän ALV-ilmoituksen luominen

Jos haluat raportoida ALV:n ryhmän puolesta, luo ALV-ilmoitus vain yrityksellesi **ALV-palautus**-sivulla. Sisällytä sen jälkeen viimeisimmät ALV-lähetykset alv-ryhmän jäseniltä valitsemalla **Sisällytä ryhmä-ALV** -toimenpiteeseen.  

Kun ALV-ryhmän edustajan ALV-ilmoitus on lähetetty viranomaisille koko ryhmän puolesta, **Laske ja kirjaa ALV-laskelma** -toiminto suoritetaan tavallisesti. Tämä toiminto sulkee avoinna olevat ALV-tapahtumat ja siirtää summat ALV-maksutilille. Tällä hetkellä tämä toiminto ei ota huomioon ryhmälähetyksiä. <!--Has this changed?--> Vain ALV-ryhmää edustavan yrityksen ALV-tapahtumat kirjataan. ALV-ryhmän jäsenten lähetyssummat tulee kirjata ALV-laskelman summaan manuaalisesti, jolloin alv-ryhmän edustajan ALV-maksutili vastaa viranomaisilta raportoitujen vastuiden määrää. Tämä toiminta muuttuu [!INCLUDE[prod_short](includes/prod_short.md)]:n tulevassa päivityksessä, joten koko konsernin ALV (ALV-ilmoituksen raporttirivien kokonaissumma) selvitetään. <!--Has this behavior changed?-->

> [!NOTE]
> ALV-ryhmän jäsenet voivat korjata lähetetyt alv-palautukset niin kauan kuin ryhmän edustaja ei ole vapauttanut konsernin ALV-tuottoa. Korjauksen tekemistä varten alv-ryhmän jäsenen täytyy luoda uusi ALV-palautus ALV-palautus jaksolle ja lähettää se alv-ryhmän edustajalle. Alv-ryhmän edustajan puolelta Viimeisin ALV-palautus lisätään **ALV-palautus**-sivulle. 

> [!IMPORTANT]
> ALV-ryhmien toimintoa tuetaan vain niillä markkina-alueilla, joissa [!INCLUDE[prod_short](includes/prod_short.md)] käyttää ALV-palautuksista ja ALV-palautusjaksoista koostuvaa ALV-kehystä. Et voi käyttää ALV-ryhmiä muilla markkina-alueilla, joilla on muita paikallisia ALV-raportoinnin toteutuksia, kuten Itävalta, Saksa, Italia, Espanja ja Sveitsi. 

## <a name="see-also"></a>Katso myös
[Yhdistyneen kuningaskunnan paikallinen toiminnallisuus brittiversiossa](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Veron määrittäminen digitaaliseksi Yhdistyneessä Kuningaskunnassa](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  
[Määritä arvolisävero](finance-setup-vat.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
