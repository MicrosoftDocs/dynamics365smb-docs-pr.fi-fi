---
title: ALV-ryhmän hallinnan laajennus | Microsoft Docs
description: Voit olla yhteydessä muihin yrityksiin, jos haluat muodostaa alv-ryhmän, ja toimia ryhmän jäsenenä tai edustajana ALV-raportoinnin yhteydessä.
author: bholtorf
manager: annbe
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: VAT, value added tax, report
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: ebe3c8748da04a2552f8f3d10967303459ba23c4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757040"
---
# <a name="the-vat-group-management-extension"></a>ALV-ryhmän hallinnan laajennus

Voit liittää yhden tai useamman maasi yrityksen yhdistääksesi alv-raportoinnin yhdelle rekisteröintinumerolle. Tämäntyyppistä järjestelyä kutsutaan *ALV-ryhmäksi*. Voit sitoutua ryhmään jäsenenä tai ryhmän edustajana.

## <a name="forming-a-vat-group"></a>ALV-ryhmän muodostaminen
ALV-ryhmän jäsenet ja ryhmän edustaja voivat käyttää **ALV-ryhmän hallinnan asetukset** -asetusopasta määrittääkseen niiden sitoutumisen ryhmään ja luomalla yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajien välille. Ryhmän jäsenet käyttävät yhteyttä lähettäessään ALV-palautuksia ryhmän edustajalle. Edustaja antaa arvonlisäveron veroviranomaisille konsernin puolesta käyttäen yhtä ALV-palautusta. 

## <a name="vat-group-constellations"></a>ALV-ryhmän joukko
Yhteydenpito tapahtuu ryhmän jäseniltä edustajalle. Ryhmän edustaja paljastaa API-liittymän, jonka avulla jäsenet voivat lähettää ALV-palautuksia alv-ryhmän edustajalle. 
[!INCLUDE[prod_short](includes/prod_short.md)] tukee ryhmien välisiä ALV-palautuslähetyksiä yrityksissä, joissa käytetään [!INCLUDE[prod_short](includes/prod_short.md)]:n paikallista tai online-tilaa, ja missä tahansa yhdistelmässä. Tiedonsiirron asetukset määräytyvät konstellaation mukaan. Seuraavissa osissa kuvataan, miten ryhmän eri lähettämiä ryhmiä määritetään.

Seuraavassa luettelossa on esitetty alv-ryhmän määritysvaiheiden suositeltava järjestys:

1. Luo asetukset Azure Active Directoryssä. Lisätietoja on kohdassa [Todennusvaatimukset](ui-extensions-vat-group.md#requirements-for-authentication).
2. Jaa tekniset tiedot, jotka alv-ryhmän jäsenet ja edustaja tarvitsevat yhteyden muodostamiseen [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajille. Yleensä alv-ryhmän edustajalla on nämä tiedot, esimerkiksi sen alv-ryhmän edustavan ympäristön nimi, johon alv-ryhmän jäsenet lähettävät ALV:n.
3. Luo käyttäjät alv-ryhmän edustajan [!INCLUDE[prod_short](includes/prod_short.md)]:lle, jota alv-ryhmän jäsenet voivat käyttää todennukseen ja yhteyden muodostamiseen.
4. Yhdistä alv-ryhmän jäsenet suorittamalla **Määritä alv-ryhmän hallinnan** avustettu asetusopas.

  Opas vaatii joitakin tietoja alv-ryhmän edustajalta. Lisätietoja on [ALV-ryhmän jäsenasetukset](#vat-group-member-setup) -osassa. Merkitse muistiin kunkin alv-ryhmän jäsenen **ryhmäjäsentunnus**. Edustaja tarvitsee näitä tunnuksia lisätäksesi yritykset alv-ryhmään.
5. Määritä alv-ryhmän hallinnan laajennus alv-ryhmän edustajan [!INCLUDE[prod_short](includes/prod_short.md)] -kohdassa **Määritä alv-ryhmän hallinnan** avusteinen asetusopas -toiminnon avulla. 

> [!NOTE]
> Kun haluat muodostaa yhteyden alv-ryhmän edustajaan, ryhmän jäsenet tarvitsevat käyttäjän, jolla on alv-ryhmän edustajan käyttöoikeus [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. ALV-ryhmän edustajan on kuitenkin luotava vähintään yksi käyttäjä suojaussyistä, mutta suosittelemme, että luot käyttäjän kullekin alv-ryhmän jäsenelle. Varmista, että jaat näiden käyttäjien tunnistetiedot alv-ryhmän jäsenille turvallisella tavalla.

## <a name="understanding-the-vat-group-management-setup"></a>ALV-ryhmän hallinnan asetusten ymmärtäminen

ALV-ryhmän edustaja paljastaa API-liittymän, jonka avulla alv-ryhmän jäsenet voivat muodostaa yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajaan ja lähettää ALV-palautuksen. ALV-ryhmän jäsenet käyttävät usein [!INCLUDE[prod_short](includes/prod_short.md)]:sta erillisissä Azure Active Directory -vuokraajissa. Tämän vuoksi lisäasetuksia tarvitaan, jotta alv-ryhmän jäsenen ja edustajan välille voidaan muodostaa yhteys [!INCLUDE[prod_short](includes/prod_short.md)]. 
  
ALV-ryhmän jäsenet muodostavat yhteyden edustajaan kutsumalla verkkopalvelua alv-ryhmän edustajan vuokraajalla. Kutsuja täytyy todentaa käyttämällä OAuth-määritystä. Kun alv-ryhmän hallinnan laajennus on määritetty, ohjelma pyytää todentamaan sen alv-ryhmän edustajalle, jotta hän voi hakea ja tallentaa käyttötunnussanoman. Tätä käyttötunnussanomaa käytetään alv-palautusten lähettämisen yhteydessä alv-ryhmän edustajalle. 

Todennusta käsitellään Azure Active Directoryssä siten, että asetukset on tehtävä alv-ryhmän edustajan Azure Active Directoryssä, että yhteydet sallitaan. Azure Active Directory -sovelluksen rekisteröinti on määritettävä siten, että käyttöoikeus on alv-ryhmän edustajan käytettävissä [!INCLUDE[prod_short](includes/prod_short.md)]. Tämä pätee myös, jos alv-ryhmän edustaja käyttää [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaa paikallisesti. Lisäksi kertakirjautuminen täytyy määrittää, jos alv-ryhmän edustaja käyttää [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaa paikallisesti.

> [!NOTE]
> Verkkopalvelun käyttöavaimen käyttöoikeuksien todennusta tuetaan myös rajoitetun ajan. Lisätietoja on kohdassa [Vanhentuneet ominaisuudet in 2021 julkaisuaalto 1:ssä](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#deprecated-features-in-2021-release-wave-1).

## <a name="requirements-for-authentication"></a>Todennusta koskevat vaatimukset 
Kun alv-ryhmän edustaja käyttää [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaa onlinessa tai paikallisesti, alv-ryhmän jäsenet käyttävät Azure Active Directorya todentamiseen, kun he lähettävät ALV-palautuksia alv-ryhmän edustajalle. Jos myös alv-ryhmän jäsenet käyttävät [!INCLUDE[prod_short](includes/prod_short.md)]:n online-ominaisuutta, alv-ryhmän jäsen voi todentaa käyttämällä nimettyjä käyttäjätietoja ja päätepisteen tietoja. Lisätietoja on kohdassa [ALV-ryhmän jäsenasetukset](ui-extensions-vat-group.md#vat-group-member-setup).

alv-ryhmien jäsenten, jotka käyttävät [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaa paikallisesti, täytyy määrittää sovellusrekisteröinti Azure Active Directoryssä ALV-ryhmän edustajan [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajalle. Sovelluksen rekisteröinnin avulla alv-ryhmän edustajan [!INCLUDE[prod_short](includes/prod_short.md)] online-käyttäjä voi todentaa ryhmän jäsenen. Lisätietoja on kohdassa [Pika-aloitus: sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristössä](/azure/active-directory/develop/quickstart-register-app).

Kun luot sovelluksen rekisteröinnin Azure Active Directory -ohjelmassa, sinun täytyy määrittää seuraava.

* Lisää **Todennus**-osassa **Verkkosivusto** alustaksi ja käytä seuraavaa **Uudelleenohjauksen URL-osoitetta**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* Valitse **Tuetut tili tyypit** -kohdassa **Todennus**-osassa **tilit mistä tahansa organisaatiohakemistosta** (mikä tahansa Azure AD -hakemisto - palveluna tarjottava sovellus).
* **Luo sertifikaatit & salaisuudet** -osassa uusi asiakassalaisuus ja merkitse arvo muistiin. Alv-ryhmän jäsenet tarvitsevat salaisuuden, kun he muodostavat yhteyden ryhmän edustajaan.
* Lisää käyttöoikeudet **API-oikeudet**-osiossa [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. Ota käyttöön delegoitu käyttöoikeus kohteisiin **Financials.ReadWrite.All** ja **user_impersonation**.
* Huomioi **Sovelluksen (asiakkaan) tunnus** **Yhteenveto**-osassa . Alv-ryhmän jäsenet tarvitsevat tunnuksen, kun he muodostavat yhteyden ryhmän edustajaan. 

## <a name="vat-group-member-setup"></a>ALV-ryhmän jäsenasetukset
Määritä alv-ryhmän jäsen suorittamalla **Määritä alv-ryhmän hallinnan** avustettu asetusopas. 

> [!NOTE]
> Ennen kuin aloitat, ota yhteyttä alv-ryhmän edustajaan seuraavien [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajan tietojen osalta:
>
> * Ohjelmointirajapinnan URL-osoite
> * Yrityksen nimi 
> * Asiakasohjelman tunnus
> * Asiakasohjelman salaisuus
> * Kirjaa käyttäjän tunnistetiedot 

1. Määritä yrityksen alv-ryhmän rooli valitsemalla **Jäsen** ja valitsemalla sitten **Seuraava**.
2. Kopioi **ryhmän jäsentunnus** -kentän arvo ja jaa se sitten alv-ryhmän edustajan kanssa, jotta he voivat lisätä yrityksesi ryhmän hyväksytyksi jäseneksi.
3. Lisää **API-URL-osoite** ALV-ryhmän edustajalle. Yleensä URL-osoite muotoillaan seuraavasti: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Esimerkiksi, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`. 
4. Lisää ALV-ryhmän edustajan [!INCLUDE[prod_short](includes/prod_short.md)] yrityksen nimi, kuten esimerkiksi *CRONUS UK Ltd.*.
5. Valitse **todennustyyppi**, valitse **OAuth2** ja valitse sitten **Seuraava**.
6. **Syötä asiakastunnus** -kenttään alv-ryhmän edustajan antama tunnus.
7. Syötä **ALV-ryhmän edustajan toimittama asiakassalaisuus** -kentässä oleva salaisuus.
8. **Syötä OAuth 2.0 Authority -päätepiste** -kenttään *https://login.microsoftonline.com/common/oauth2*.
9. **Syötä OAuth 2.0 Resource -URL-osoite** -kenttään *https://api.businesscentral.dynamics.com/*.
10. **Syötä OAuth 2.0 Redirect -URL-osoite** -kenttään *https://businesscentral.dynamics.com/OAuthLanding.htm*. 
11. Kun olet määrittänyt eri kentät, valitse **Seuraava** ja syötä sitten käyttäjätiedot, jotka alv-ryhmän edustaja on toimittanut.
12. Valitse alv-raporttikonfiguraatio, jonka avulla ALV raportoidaan maasi viranomaisille.

  Esimerkiksi Yhdistyneessä kuningas kunnassa alv-raportin konfiguraatio määritetään ilmoittamaan ALV:stä HMRC:lle. ALV-ryhmän hallinnan laajennus kopioi tämän asetuksen, mutta korvaa lähetyscodeunitin sellaisella, joka tukee toimittamista alv-ryhmän edustajalle veroviranomaisten sijaan. Microsoft tarjoaa codeunitin. Valitse **Seuraava**, kun olet valmis.

## <a name="using-the-vat-group-management-features"></a>ALV-ryhmän hallintaominaisuuksien käyttäminen

ALV-ryhmän jäsenet käyttävät vakioprosesseja alv-palautusten valmisteluun. Ainoa ero on, että valitaan **VATGROUP**-raporttiversio, joka lähettää ALV-palautuksen alv-ryhmän edustajalle eikä viranomaisille. Lisätietoja on kohdassa [Tietoja ALV-palautusraportista](finance-how-report-vat.md#about-the-vat-return-report).

Seuraavissa osissa kuvataan tehtävät, jotka alv-ryhmän edustajien täytyy suorittaa.

### <a name="vat-group-submissions"></a>ALV-ryhmän lähetykset

**ALV-ryhmän lähetykset** -sivulla näkyvät jäsenten lähettämät alv-palautukset. Sivu toimii toimituksille luonnossijaintina, kunnes alv-ryhmän edustaja sisällyttää ne ryhmän ALV-palautukseen. Voit avata lähetykset ja tarkistaa ALV-ilmoituksen niiden yksittäisten ruutujen osalta, jotka alv-ryhmän jäsen on ilmoittanut.

### <a name="creating-a-group-vat-return"></a>Ryhmän ALV-ilmoituksen luominen

Jos haluat raportoida ALV:n ryhmän puolesta, luo ALV-ilmoitus vain yrityksellesi **ALV-palautus**-sivulla. Sisällytä sen jälkeen viimeisimmät ALV-lähetykset alv-ryhmän jäseniltä valitsemalla **Sisällytä ryhmä-ALV** -toimenpiteeseen.  

Kun alv-ryhmän edustajan ALV-ilmoitus on lähetetty viranomaisille koko ryhmän puolesta, **Laske ja kirjaa ALV-laskelma** -toiminto suoritetaan tavallisesti. Tämä toiminto sulkee avoinna olevat ALV-tapahtumat ja siirtää summat ALV-maksutilille. Tällä hetkellä tämä toiminto ei ota huomioon ryhmälähetyksiä. Tämä tarkoittaa sitä, että vain alv-ryhmää edustavan yrityksen ALV-tapahtumat kirjataan. ALV-ryhmän jäsenten lähetyssummat tulee kirjata ALV-laskelman summaan manuaalisesti, jolloin alv-ryhmän edustajan ALV-laskelmatili vastaa viranomaisilta raportoitujen vastuiden määrää. Tämä toiminta muuttuu [!INCLUDE[prod_short](includes/prod_short.md)]:n tulevassa päivityksessä, joten koko konsernin ALV (ALV-ilmoituksen raporttirivien kokonaissumma) selvitetään. 

> [!NOTE]
> ALV-ryhmän jäsenet voivat korjata lähetetyt alv-palautukset niin kauan kuin ryhmän edustaja ei ole vapauttanut konsernin ALV-tuottoa. Korjauksen tekemistä varten alv-ryhmän jäsenen täytyy luoda uusi ALV-palautus ALV-palautus jaksolle ja lähettää se alv-ryhmän edustajalle. Alv-ryhmän edustajan puolelta Viimeisin ALV-palautus lisätään **ALV-palautus**-sivulle. 

## <a name="see-also"></a>Katso myös
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  
[Määritä arvolisävero](finance-setup-vat.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]