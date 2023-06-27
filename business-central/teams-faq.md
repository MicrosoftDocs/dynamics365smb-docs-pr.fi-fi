---
title: Teams – usein kysytyt kysymykset
description: 'Hanki vastauksia joihinkin tyypillisiin kysymyksiin, jotka liittyvät Teamsin ja Business Centralin käyttöön.'
author: jswymer
ms.author: jswymer
ms.topic: faq
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors'
ms.date: 09/28/2022
ms.custom: bap-template
---
# <a name="teams-faq" />Teams – usein kysytyt kysymykset

[!INCLUDE [online_only](includes/online_only.md)]

Tässä artikkelissa vastataan joihinkin kysymyksiin, joita sinulla voi olla Microsoft Teamsin ja sovelluksen [!INCLUDE [prod_short](includes/prod_short.md)] käyttämiseen liittyen.

## [Yleiset](#tab/general)

### <a name="how-do-i-sign-in-to-the--app-in-teams" />Miten kirjaudun [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellukseen Teamsissa?

Sovelluksen asennuksen jälkeen sinua pyydetään kirjautumaan sisään, kun käytät sovellusta ensimmäisen kerran, kun liität [!INCLUDE [prod_short.md](includes/prod_short.md)] -linkin Teams-keskusteluun tai kun valitset Teamsin kortissa **Tiedot**-toiminnon. Teams-asiakkaan mukaan sinun on ehkä annettava tunnistetiedot, joita käytät kirjautuessasi sovellukseen [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="how-do-i-sign-out-of-the--app-in-teams" />Miten kirjaudun ulos [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovelluksesta Teamsissa?

Voit kirjautua ulos Teamsista, jota käytettiin muodostettaessa yhteys sovellukseen [!INCLUDE [prod_short.md](includes/prod_short.md)], siirtymällä johonkin keskusteluruutuun, napsauttamalla hiiren kakkospainikkeella alla olevaa [!INCLUDE [prod_short.md](includes/prod_short.md)] -kuvaketta ja valitsemalla sitten **Asetukset**. Kun ikkuna avautuu, valitse käyttäjätiedot, joilla olet kirjautuneena, ja valitse lopuksi **Kirjaudu ulos**.

### <a name="does-the-app-for-teams-connect-to--on-premises" />Muodostetaanko Teamsin sovelluksesta yhteys [!INCLUDE [prod_short.md](includes/prod_short.md)] on-premises -sovellukseen?

Nro [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus Teamsille toimii vain [!INCLUDE [prod_short.md](includes/prod_short.md)] online -version kanssa. [!INCLUDE [prod_short.md](includes/prod_short.md)] -käyttöönottotyyppejä, joita Microsoft ei isännöi tai hallitse – kuten paikallista, hybridipilveä tai yksityistä pilveä – ei tueta.

### <a name="does-the-app-work-with-multiple-companies-and-environments" />Toimiiko sovellus useissa yrityksissä ja ympäristöissä?

Kyllä. Toisessa yrityksessä olevia yhteyshenkilöitä voi hakea valitsemalla [Asetukset](across-teams-settings.md). Kun sovellus [!INCLUDE [prod_short.md](includes/prod_short.md)] laajentaa linkin korttiin, linkin tulee sisältää sovelluksen ympäristön ja yrityksen nimet, jotka vastaavat oikean yrityksen tietueita. Voit liittää linkkejä kaikkiin yrityksiin ja ympäristöihin, joihin sinulla on käyttöoikeus organisaatiossasi, ja [!INCLUDE [prod_short.md](includes/prod_short.md)] -tililtä, jota käytit sisäänkirjautuessa. Chatin osanottajat näkevät kortin. He eivät kuitenkaan voi tarkastella kortin tietoja, ellei heillä ole oikeuksia yritykseen tai ympäristöön, jossa kyseinen tietue on tallennettuna.

### <a name="in-which-countries-or-regions-is-the--app-available" />Missä maissa tai millä alueilla [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus on saatavilla?

[!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus Teamsille ei ole rajoitettu maan tai alueen mukaan. Sovellus on saatavilla kaikilla markkinoilla, joissa Teams on tällä hetkellä saatavilla. 

### <a name="does-the--app-work-with-any-localization-of-include-prod_shortmd" />Toimiiko [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus [!INCLUDE [prod_short.md](includes/prod_short.md)] -lokalisointien kanssa?

Kyllä. Sovelluksen on tarkoitus toimia minkä tahansa [!INCLUDE [prod_short.md](includes/prod_short.md)] -lokalisoinnin kanssa riippumatta siitä, tarjotaanko lokalisointia suoraan Microsoftilta vai kumppanilta. Lisätietoja on kohdassa [Maa- ja aluekohtainen saatavuus ja tuetut kielet](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="which-languages-does-the--app-support" /><a name="language"></a>Mitä kieliä [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus tukee?

Kaksi asiaa määrittää kielen, jota käytetään korteissa ja korttien tiedoissa Teamsissa:

1. Teamsiin määrittämäsi kieli, jonka näet Teamsin tiliasetuksista. 
2. [!INCLUDE [prod_short.md](includes/prod_short.md)] -ohjelman kieli, jonka näet [!INCLUDE [prod_short.md](includes/prod_short.md)] -verkkoasiakkaassa (katso [Perusasetusten muuttaminen – kieli](ui-change-basic-settings.md#language)).

Seuraavassa taulukossa kuvataan, miten viestin tekijöiden ja vastaanottajien kokemus poikkeea toisistaan eri kieliasetusten ja kielten saatavuuden mukaan.

|Kuka|Kortti|Kortin tiedot |
|-|----|--------------| 
|Viestin tekijä |Näkyy Teamsissa määritetyllä kielellä. Jos [!INCLUDE [prod_short.md](includes/prod_short.md)] ei tarjoa samaa kieltä, kortti näkyy englanniksi. |Näytetään kielellä, joka sovelluksessa [!INCLUDE [prod_short.md](includes/prod_short.md)] on määritetty. Kielet voivat olla kumppaneiden tarjoamien kielisovellusten kieliä. |
|Viesti vastaanottaja |Näkyy viestin tekijän kielellä. |Näkyy [!INCLUDE [prod_short.md](includes/prod_short.md)]issa määritetyllä kielellä. |

Luettelo [!INCLUDE [prod_short.md](includes/prod_short.md)]in tuetuista kielistä on kohdassa [Tuetut kielet](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### <a name="does-the--app-work-with-industry-solutions" />Voiko [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellusta käyttää toimialaratkaisujen kanssa?

Kyllä. Kuitenkin vain joitakin sovelluksen ominaisuuksia voi käyttää [upotettujen sovellusten](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) kanssa:

- Sovellus toimii linkeissä, jotka perustuvat upotettujen sovellusten kanssa tyypillisesti käytetyssä **\*.bc.dynamics.com**-mallissa.
- Yhteyshenkilöhaku ei ole käytettävissä upotetuissa sovelluksissa, jotka korvaavat Microsoftin perussovelluksen.

### <a name="does--work-with-the-teams-mobile-app" />Toimiiko [!INCLUDE [prod_short.md](includes/prod_short.md)] Teamsin mobiilisovelluksen kanssa?

Kyllä. [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus voidaan asentaa tiimien Teams-työpöytäsovelluksesta tai selaimesta tai järjestelmänvalvoja kaikille käyttäjille. Asennettu [!INCLUDE [prod_short.md](includes/prod_short.md)]-sovellus on automaattisesti saatavana Teamsin iOS- ja Android-sovelluksissa. Mobiililaitteissa voi vain katsella muiden lähettämiä kortteja, käyttää tietoja tai avata kortti koko käyttökokemuksessa [!INCLUDE [prod_short.md](includes/prod_short.md)] -mobiilisovelluksessa. Et voi kuitenkaan liittää linkkejä, jotka laajentuvat korteiksi viestejä kirjoittaessa, etkä hakea yhteyshenkilöitä. Lisätietoja mobiilisovelluksen vähimmäisvaatimuksista ovat kohdassa [Business Centralin käyttämisen vähimmäisvaatimukset](product-requirements.md).

### <a name="is-the--app-for-teams-the-same-as-the-include-prod_shortmd-app-for-ios-and-android" />Onko Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus sama kuin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovelluksen iOS- ja Android-versio?

Ei. Sovellus Teamsille on Microsoft Teamsin apuohjelma, joka on suunniteltu erityisesti yhteistyöhön Teamsin kanssa. Vaihtoehtoisesti [!INCLUDE [prod_short.md](includes/prod_short.md)] -mobiilisovelluksessa on monipuoliset käyttökokemukset [!INCLUDE [prod_short.md](includes/prod_short.md)] -tietojen työstöön mobiililaitteissa.

Mobiilikäyttäjiä kehotetaan asentamaan sekä mobiilisovellus että Teams-sovellus, jottaa [!INCLUDE [prod_short.md](includes/prod_short.md)]ista saadaan irti mahdollisimman paljon. Kun molemmat on asennettu, voit valita **Ponnahdusruutu**-toiminnon Teamsin kortissa avataksesi kortin tiedot [!INCLUDE [prod_short.md](includes/prod_short.md)] -mobiilisovelluksessa. Lisätietoja [!INCLUDE [prod_short.md](includes/prod_short.md)]- ja Teams-mobiilisovellusten asentamisesta on kohdassa:

- [Business Central -sovelluksen hakeminen mobiililaitteeseen](install-mobile-app.md)
- [Hanki Teams-mobiilisovellus](https://support.microsoft.com/office/download-the-mobile-app-for-teams-5940ebdc-0082-4fb1-83c4-751edc23dcb5) Microsoft-tuesta

### <a name="does-the--app-work-in-all-teams-clients" />Toimiiko [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus kaikkien Teams-asiakkaiden kanssa?

Nro Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellusta ei tueta asennettaessa macOS-tai Linux-pakettina. Näissä ympäristöissä voit käyttää Teamsia sen sijaan tuetulla selaimella.

[!INCLUDE [prod_short.md](includes/prod_short.md)]in vähimmäisvaatimukset ovat kohdassa [Business Centralin käyttämisen vähimmäisvaatimukset](product-requirements.md#teams).

Lisätietoja Teams-asiakkaiden valinnasta ja niiden asentamisesta on Teamsin dokumentaation ohjeaiheessa [Microsoft Teams -asiakkaiden hankkiminen](/microsoftteams/get-clients).

### <a name="which-teams-client-is-best-for-" />Mitkä Teams-asiakas on paras [!INCLUDE [prod_short.md](includes/prod_short.md)]ille?

Teams-asiakkaiden välillä on vain vähäisiä eroja ja rajoituksia, jotka voivat vaikuttaa Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovelluksen käyttökokemukseen. Kun valitset Teams-asiakasta, harkitse seuraavia asioita:

- Kameraa ja sijaintia ei voi käyttää Teams-työpöytäsovelluksen Tiedot-ikkunasta.
- Puhelinnumeroita ei voi aktivoida Teamsin tietoikkunassa iOS- tai Android-sovelluksessa tai selaimessa.
- Käyttämällä Microsoft Edgeä Teamsin kanssa selaimessa voit helposti työskennellä eri tunnistetiedoilla ja tileillä kirjautumalla Teamsiin eri profiileista. Jos haluat lisätietoja profiilien käyttämisestä Microsoft Edge -ohjelmassa, katso ohjeaihe [Kirjautuminen ja usean profiilin luominen Microsoft Edgessä](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435).

### <a name="what-is-the-best-way-for-me-to-demonstrate--and-microsoft-teams-to-prospective-customers" />Mikä on paras tapa esitellä [!INCLUDE [prod_short.md](includes/prod_short.md)]ia ja Microsoft Teamsia mahdollisille asiakkaille?

Jos olet jälleenmyyjäkumppani, haluat ehkä saada ympäristön, jonka voit näyttää prospekteille osana myyntiä edeltäviä esittelyjä. Jotta et vaikuttaisi organisaatiosi Microsoft Teamsiin, voit hankkia Microsoft 365 -esittelytilin osoitteesta [https://aka.ms/CDX](https://aka.ms/CDX). Tämän tilin avulla voit hallita täysin itsenäistä Azure-organisaatiota, joka sisältää Microsoft Teamsin ja [!INCLUDE [prod_short.md](includes/prod_short.md)]in. Lisätietoja on kohdassa [Dynamics 365 Business Central -esittely-ympäristöjen valmistelu](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### <a name="does-the--app-for-teams-cater-to-my-customization-and-personalization" />Ottaako Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus huomioon mukautukseni ja personointini?

Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus voi näyttää kortteja, joissa on linkkejä asiakkaan sivuihin ja taulukoihin [!INCLUDE [prod_short.md](includes/prod_short.md)]issa, kuten sivuihin ja taulukoihin, jotka ovat peräisin omista mukautetuista laajennuksistasi tai AppSourcesta.

Teamsissa kortilla näkyviin kenttiin voivat vaikuttaa myös organisaatioosi asennetut [!INCLUDE [prod_short.md](includes/prod_short.md)] -mukautukset. Kortit eivät ota huomioon roolikohtaisia mukautuksia tai käyttäjän mukauttamista. Kortin tiedot -ikkunassa näkyvät kuitenkin tietueiden yksityiskohdat siinä muodossa kuin näkisit ne [!INCLUDE [prod_short.md](includes/prod_short.md)]issa, mukaan lukien laajennukset, roolien mukautukset ja käyttäjän personoinnit.

Yhteyshenkilöitä haettaessa mukautuksella tai mukauttamisella ei ole vaikutusta kenttiin, jotka vastaavat hakutuloksissa näytettyä **Yhteyshenkilöt**-taulukkoa tai -kenttiä.

### <a name="how-do-the-permissions-required-by-the-app-affect-my-privacy" />Miten sovelluksen vaatimat käyttöoikeudet vaikuttavat tietosuojaan?

Ennen kuin asennat Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovelluksen, voit tarkastella sovelluksen toiminnan edellyttämiä vähimmäisoikeuksia. Asentamalla sovelluksen hyväksyt sen, että sovelluksella on oikeus vastaanottaa sille tarjotut viestit ja tiedot, ja Teamsilla on oikeus säilyttää ja käsitellä näitä viestejä.

Myös jotkin [!INCLUDE [prod_short.md](includes/prod_short.md)] -ominaisuudet edellyttävät ulkoisten linkkien avaamista tai kameran tai maantieteellisen sijainnin käyttöä. Oletetaan, että haluat siepata kuvan ostolaskusta käsittelyä varten. [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus ei käytä näitä ominaisuuksia ilman suostumustasi, ja ne ovat vain tiettyjen ominaisuuksien käytössä **Tiedot**-ikkunassa. Kun käytät jotakin näistä ominaisuuksista ensimmäistä kertaa, Teams näyttää valintaikkunan, jossa sinua pyydetään myöntämään käyttöoikeus tarvittaviin laiteominaisuuksiin.

- Teams-työpöydällä voit tarkastella ja muuttaa sovelluksen käyttö oikeuksia **Asetukset**-ikkunassa. Valitse profiilikuvasi sovelluksen yläosasta, valitse **Asetukset** > **Käyttöoikeudet** ja valitse sitten [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus.

- Jos käytät Teamsia selaimella tai iOS- tai Android-laitteessa, voit tarkistaa tai muuttaa käyttöoikeuksia selaimen tai laitteen asetuksissa.

> [!NOTE]
> Se, mitkä [!INCLUDE [prod_short.md](includes/prod_short.md)] -ominaisuudet kehottavat sinua antamaan käyttöoikeuksia, riippuu niistä lisäsovelluksista ja mukautuksista, jotka on otettu käyttöön [!INCLUDE [prod_short.md](includes/prod_short.md)] -ympäristössä, johon muodostat yhteyden.

### <a name="where-can-i-learn-about-my-privacy" />Mistä saan tietoja tietosuojasta?

[Microsoftin tietosuojatiedoissa](https://go.microsoft.com/fwlink/?linkid=2030602) on tietoja siitä, miten Microsoft käsittelee tietojasi. 

Järjestelmänvalvojaltasi saat tietoja siitä, miten organisaatiosi käsittelee tietojesi yksityisyyttä.

### <a name="how-do-i-uninstall-the--app-for-teams" />Miten poistan Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovelluksen asennuksen?

Jos haluat poistaa itsellesi asennetun sovelluksen, siirry johonkin keskusteluruutuun, etsi alla oleva [!INCLUDE [prod_short.md](includes/prod_short.md)] -kuvake, napsauta kuvaketta hiiren kakkospainikkeella ja valitse **Poista asennus**.  

### <a name="will-microsoft-continue-to-improve-the--app-for-teams" />Jatkaako Microsoft Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)]-sovelluksen parantamista?

Microsoft saa jatkuvasti palautetta monipuoliselta käyttäjäyhteisöltä ja ottaa parhaat ehdotukset huomioon. Jos haluat tietää, mitä on seuraavaksi tulossa Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellukselle, tutustu [Dynamics 365:n julkaisusuunnitelmaan](/dynamics365-release-plan/2021wave1/).

Jos haluat osallistua Teamsin sovelluksen parantamiseen tai sinulla on idea, joka auttaisi yksinkertaistamaan työtä tai yhteistyökokemuksia Teamsissa, lisää idea tai äänestä olemassa olevia ideoita osoitteessa [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

### <a name="where-can-i-find-teams-integration-inside-the-business-central-web-client" />Mistä löydän Teams-integroinnin Business Central -verkkoasiakkaan sisällä?

Lisätietoja Teamsiin linkitetyn verkkoasiakkaan toiminnoista on kohdassa [Tietueiden ja sivulinkkien jakaminen Microsoft Teamsissa](across-working-with-teams.md#share-link).

## [Business Central -välilehdet](#tab/tabs)

### <a name="who-can-see-the-content-of-a-tab" /><a name="who-can-view"></a>Kuka näkee välilehden sisällön?

Kaikki keskusteluun tai kanavaan liittyvät henkilöt, joilla on:

1. Business Central-sovellus Teamsille asennettuna.
2. Joko Business Central -käyttöoikeus tai sille on myönnetty käyttöoikeus Business Centraliin Microsoft 365 -käyttöoikeuden avulla.
3. Käyttöoikeudet sivun tietojen tarkasteluun.

### <a name="where-does-the-recommended-content-come-from" /><a name=#recommended-content></a>Mistä suositeltu sisältö on peräisin?

**Välilehden sisältö** -asetuksen avulla voit valita suositellun sisällön roolikeskuksesi perusteella. Suositeltu sisältö sisältää vain luettelosivut, kuten asiakkaat, myyntitilaukset ja toimittajat - ei yksittäisiä korttisivuja, kuten tietty asiakas tai toimittaja.

Erityisesti suositeltu sisältö sisältää:

- Roolikeskuksen yläreunan siirtymisvalikon toiminnot
- Kaikki merkitsemäsi luettelosivut.
- Jos luettelosivulla on erilaisia näkymiä, kuten luomasi näkymät, saat myös valita näistä näkymistä

Voit lisätä suositellun sisällön luettelosivuja lisäämällä kirjanmerkkejä. Voit myös poistaa suositellun sisällön poistamalla kirjanmerkkejä. Lisätietoja kirjanmerkkien lisäämisestä ja poistamisesta on ohjeaiheessa [Sivun tai raportin kirjanmerkin luominen roolikeskuksessa](ui-bookmarks.md).

Jos vaihdat ympäristön tai yrityksen asetukset-välilehdessä, suositeltu sisältö muuttuu sen ympäristön ja yrityksen roolikeskuksen ja kirjanmerkkien perusteella, johon siirryt.

### <a name="when-i-create-a-tab-does-it-grant-permissions-to-the-people-in-the-channel-or-chat" />Kun luon välilehden, myöntääkö se oikeudet kanavan tai keskustelun käyttäjille?

Nro Välilehtien luominen ei vaikuta käyttöoikeuksiin, ja käyttäjillä on jo oltava näiden tietojen käyttöoikeus, kun he käyttävät välilehteä.

### <a name="can-i-chat-alongside-a-tab" />Voinko keskustella välilehden rinnalla?

Kyllä. Aloita keskustelu keskustelu-kuvakkeen avulla. Tämä keskusteluketju liitetään sitten välilehteen. 

### <a name="if-i-remove-a-tab-from-a-chat-or-channel-is-any-business-central-data-deleted" />Jos poistan välilehden keskustelusta tai kanavasta, onko mitään Business Central -tietoa poistettu?

Nro

### <a name="can-i-safely-rename-a-tab" />Voinko nimetä välilehden turvallisesti uudelleen?

Kyllä. Välilehden sisältö ei liity välilehden todelliseen nimeen. Nimeä uudelleen kuinka haluat! 

### <a name="i-need-to-work-across-tasks-in-different-windows-can-i-do-this" />Minun täytyy työskennellä eri tehtävien parissa eri ikkunoissa. Voinko tehdä näin?

Kyllä. Voit avata välilehden omalle selainikkunalle ja näyttää Business Central -verkkoasiakkaan. 

### <a name="can-i-add-or-pin-tab-in-team-meetings" />Voinko lisätä tai kiinnittää välilehden Teams-kokouksiin?

Nro Teamsin Business Central -sovellus ei tue välilehtiä kokouksissa.

### <a name="cant-add-a-tab-if-using-isv-urls-like-bcdynamicscom-but-can-pin" />Välilehteä ei voi lisätä, jos käytetään ISV-URL-osoitteita, kuten *. bc.dynamics.com (mutta ne voi kiinnittää)

Ei tueta.

### <a name="when-i-do-things-in-the-tab-like-navigate-resort-apply-a-filter-or-search-do-others-see-my-changes" />Kun teen asioita välilehdellä, kuten navigoin, järjestelen uudelleen tai haen, näkevätkö muut muutokseni?

Nro Vain kenttien muutokset tai käynnissä olevat toiminnot vaikuttavat siihen, miten muut näkevät välilehden sisällön.

### <a name="does-the-tab-content-refresh-automatically-if-not-how-do-i-refresh-it" />Päivitetäänkö välilehden sisältö automaattisesti? Jos ei, miten voin päivittää sen?

Sisältö ei päivity automaattisesti, ja tällä hetkellä päivitä-painiketta ei ole. Paras tapa päivittää sisältöä ja varmistaa, että tiedot ovat ajan tasalla, on poistua välilehdeltä ja palata takaisin. 

### <a name="does-this-show-lists-and-records-from-my-customizations-and-add-ons" />Näytetäänkö luettelot ja tietueet omista mukautuksista ja lisäosista?

Kyllä. 

### <a name="when-i-add-a-tab-will-people-see-it-in-my-language" />Kun lisään välilehden, näkevätkö ihmiset sen omalla kielelläni?

Nro Kukin käyttäjä tarkastelee välilehden sisältöä Business Centralin kieli-, alue- ja aikavyöhyke-asetuksissa. 

### <a name="can-i-have-multiple-tabs-pointing-to-different-content" />Voiko eri sisältöön osoittaa useita välilehtiä?

Kyllä.

### <a name="can-i-also-add-tabs-to-chat-with-a-single-person" />Voinko lisätä välilehtiä myös keskusteluun yksittäisen henkilön kanssa?

Kyllä, niin kauan kuin keskustelu ei ole luonnos (eli viestiä ei ole lähetetty käynnistämään kyseistä keskustelua) ja toisen henkilön on asennettava Business Central -sovellus.

### <a name="can-i-switch-companies-within-a-tab" />Voinko vaihtaa yrityksiä välilehdessä?

Nro 

### <a name="is-this-different-than-using-teams-generic-ability-to-create-a-tab-that-hosts-a-website" />Onko tämä eri asia kuin käyttää Teamsin yleistä kykyä luoda välilehti, joka isännöi verkkosivustoa?

Kyllä. Emme suosittele, että käytät tätä lähestymistapaa. Monissa tapauksissa se ei toimi Business Centralin yhteydessä.

## [Hae yhteyshenkilöitä](#tab/contacts)

### <a name="which-tables-does-the-app-search-in" />Missä taulukoissa sovellus tekee hakuja?

Kun yhteyshenkilöitä haetaan Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovelluksesta, hakusanoja verrataan [!INCLUDE [prod_short.md](includes/prod_short.md)]in **Yhteyshenkilöt**-taulukon tietueisiin. 

### <a name="which-fields-in-the-contacts-table-can-i-search" />Missä yhteyshenkilötaulukon kentissä voi tehdä hakuja?

Kun hakusanoja kirjoitetaan hakuruutuun, niitä verrataan useimpiin **Yhteyshenkilöt**-taulukon kenttiin. Näitä kenttiä ovat esimerkiksi **Nro**, **Nimi**, **Osoite**, **Puhelinnro** tai **Matkapuhelinnro** ja **Sähköposti**. 

Hakutermejä ei yhdistetä mukautettuihin kenttiin, joita sovellukset ja laajennukset ovat lisänneet **Yhteystiedot**-taulukkoon.

### <a name="do-search-results-include-companies-and-persons" />Sisältävätkö hakutulokset yritykset ja henkilöt?

Kyllä. Yhteyshenkilöiden tyyppi [!INCLUDE [prod_short.md](includes/prod_short.md)]issa voi olla **Yritys** tai **Henkilö**, kun vähintään yksi henkilö voi olla liitetty yritykseen. Yrityksillä ja henkilöillä on hakutuloksissa erilainen kuvake.

### <a name="do-contacts-of-any-business-relationship-appear-in-the-results" />Sisältyvätkö liikesuhteiden yhteyshenkilöt tuloksiin?

Kyllä. Jotkin yhteyshenkilöt voivat ilmaista asiakkaita tai toimittajia tai molempia. Muut yhteyshenkilöt, joilla ei ole määritetty liikesuhdetta, ilmaisevat yleensä mahdollisen asiakkaan. Yhteyshenkilöt, joissa on muita liikesuhteita, kuten [!INCLUDE [prod_short.md](includes/prod_short.md)]issa mahdollisesti määritettyjä mukautettuja suhteita, näkyvät myös hakutuloksissa.

### <a name="can-i-look-up-contact-details-during-meetings" />Voinko hakea yhteyshenkilön tietoja kokousten aikana?

Kyllä. Voit hakea asiakkaan tai toimittajan yhteystiedot, vuorovaikutushistorian ja liittyvät asiakirjat Teams-kokouksen tai puhelun aikana Teamsista poistumatta.

Voit itse asiassa hakea yhteyshenkilön tietoja mistä tahansa Teamsissa komentoruudun avulla. Voit esimerkiksi hakea yhteyshenkilön tiedot Teams-kalenterista, mikä auttaa sopimaan tapaamisen.

### <a name="how-do-i-view-my-last-interactions-with-a-contact" />Miten viimeisimpiä vuorovaikutuksia yhteyshenkilön kanssa tarkastellaan?

Yhteyshenkilön tietoikkunassa on näkyvissä vuorovaikutuslokin tapahtumat. Vuorovaikutuslokin tapahtumat ilmaisevat organisaation ja tietyn yhteyshenkilön vuorovaikutushistorian. Vuorovaikutuksia ovat esimerkiksi sähköpostikirjeenvaihto, vastaanotetut puhelut ja lähetetyt asiakirjat.

Vuorovaikutusten näyttäminen edellyttää, että [!INCLUDE [prod_short.md](includes/prod_short.md)] on määritetty seuraamaan vuorovaikutuksia. Lisätietoja vuorovaikutusten kirjaamisesta lokiin on kohdassa [Yhteyshenkilöiden kanssa tapahtuvien vuorovaikutusten kirjaaminen](marketing-interactions.md).

### <a name="how-do-i-register-a-teams-call-or-meeting-as-an-interaction" />Miten Teams-puhelu tai -kokous rekisteröidään vuorovaikutuksena?

Etsi yhteyshenkilön tietoikkunassa **Luo vuorovaikutus** -toiminto ja valitse saapuvat tai lähtevät puhelut vuorovaikutusmalleina. Voit luoda myös omia mukautettuja vuorovaikutusmalleja nimenomaan Teams-keskusteluissa käytettäviksi.

### <a name="can-i-call-a-contact-from-the--app-for-teams" />Voinko soittaa yhteyshenkilölle Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovelluksesta?

[!INCLUDE [prod_short.md](includes/prod_short.md)] on integroitu jossain määrin Teamsin puheluominaisuuksiin. VOIP-puhelua ei aloittaa välittömästi yhteyshenkilökortista tai yhteyshenkilön tietoikkunasta. Kun yhteyshenkilötietoja kuitenkin tarkastellaan Teams-työpöytäsovelluksesta, puhelinnumerokentän valitsemalla voidaan soittaa kyseiseen numeroon, jos Teams on määritetty laitteessa soitonvalintasovellukseksi. Jos Teamsissa soitetaan lankapuhelimeen tai matkapuhelinnumeroihin perinteisellä PSTN-puhelinjärjestelmä, käytössä on oltava Microsoft 365 Business Voice -sovellus. Lisätietoja on kohdassa [Mikä on Microsoft 365 Business Voice?](/MicrosoftTeams/business-voice/whats-business-voice).

### <a name="how-do-i-view-recent-documents-for-a-customer-or-vendor" />Miten voin tarkastella asiakkaan tai toimittajan viimeaikaisia asiakirjoja?

[!INCLUDE [prod_short.md](includes/prod_short.md)] liittää yhteyshenkilön yleensä asiakas- tai toimittajatietueeseen, joka puolestaan liittyy liiketapahtumatietueisiin, kuten myyntitarjouksiin tai ostolaskuihin. Voit tarkastella yhteyshenkilön liittyviä asiakirjoja siirtymällä yhteyshenkilön tietoikkunaan, valitsemalla **Liikesuhde**-kentän arvon tai siirtymällä liitettyyn asiakkaaseen tai toimittajaan toimintojen avulla. Laajenna asiakas- tai toimittajasivulla tietoruutu. Näkyviin tulee erilaisten asiakirjojen tilastoja, joihin voi porautua. Kokemus voi olla erilainen omien mukautusten tai mukauttamisten vuoksi.

### <a name="how-do-i-search-for-contacts-using-special-characters" />Miten erikoismerkkejä käyttäviä yhteyshenkilöjä haetaan?

Hakuehdoissa voidaan käyttää lähes kaikki unicode-merkkejä. [!INCLUDE [prod_short.md](includes/prod_short.md)] varaa kuitenkin seuraavat symbolit muuta käyttöä varten: **=**, **.**, **\*** ja **@**. Näiden symbolien käyttö hakusanoissa ei ehkä palauta odotuksenmukaisia tuloksia. Jos tulokset eivät ole odotuksenmukaiset, käytä heittomerkkejä hakusanojen ympärillä, kuten seuraavassa: **Contoso'='2**.

### <a name="how-can-i-search-contacts-stored-in-a-different-company" />Miten haetaan toiseen yritykseen tallennettuja yhteyshenkilöitä?

Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus voi hakea asiakkaita, toimittajia ja muita yhteyshenkilöitä samanaikaisesti yhdestä yrityksestä.  
Toiseen [!INCLUDE [prod_short.md](includes/prod_short.md)] -yritykseen tallennettuja yhteyshenkilöitä voi hakea avaamalla [Asetukset](across-teams-settings.md) sekä vaihtamalla ympäristön ja yrityksen siellä.

### <a name="are--contacts-different-than-the-ones-in-the-teams-contacts-screen" />Ovatko [!INCLUDE [prod_short.md](includes/prod_short.md)]in yhteyshenkilöt erilaisia kuin Teamsin yhteyshenkilönäytön yhteyshenkilöt?

Kyllä. [!INCLUDE [prod_short.md](includes/prod_short.md)]iin tallennetut yhteyshenkilöt ilmaisevat organisaatiossa käytettävissä olevia liiketoiminnan yhteyshenkilöitä. Ne ovat yhteyshenkilöitä, jotka on muodostettu ja joilla on hyvin määritetty liikesuhde, tai yhteyshenkilöitä, jotka ilmaisevat mahdollisia asiakkaita. Nämä yhteyshenkilöt ovat tyypillisesti ulkoisia yhteyshenkilöitä. Teamsin puhelujen yhteyshenkilöluettelossa näkyvät yhteyshenkilöt ovat sen sijaan omia yhteyshenkilöitä. Näitä yhteyshenkilöitä ei välttämättä jaeta muiden kanssa organisaatiossa, ja ne ilmaisevat tyypillisesti organisaation sisäisiä yhteyshenkilöitä.

### <a name="does--synchronize-contacts-with-teams" />Synkronoiko [!INCLUDE [prod_short.md](includes/prod_short.md)] yhteyshenkilöt Teamsin kanssa?

Ei. [!INCLUDE [prod_short.md](includes/prod_short.md)]iin tallennetut yhteyshenkilöt jäävät erilleen Teamsiin tallennetuista yhteyshenkilöistä.
Tällä hetkellä kahden luettelon synkronointia ei suunnitella.

### <a name="what-is-the-minimum-version-of--for-contact-search" />Mikä on yhteyshenkilöhaussa käytettävä [!INCLUDE [prod_short.md](includes/prod_short.md)]in vähimmäisversio?

Yhteyshenkilöhakua varten on asennettava Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovelluksen versio 1.0.4 tai sitä uudempi versio ja muodostettava yhteys [!INCLUDE [prod_short.md](includes/prod_short.md)] -ympäristön versioon 18 tai sitä uudempaan versioon.

### <a name="can-i-search-from-my-mobile-device" />Voiko haun tehdä mobiililaitteesta?

Yhteyshenkilöhaku ei ole käytettävissä iOS- ja Android-laitteiden Teamsissa tällä hetkellä.

### <a name="which-permissions-do-i-need-for-contact-search" />Mitä oikeuksia tarvitaan yhteyshenkilöhakuun?

Yhteyshenkilöhakua varten tarvitaan **Yhteyshenkilöt**-taulukon objektitason oikeus haettavassa [!INCLUDE [prod_short.md](includes/prod_short.md)] -yrityksessä. Yhteyshenkilön tietoikkunan näyttämiseen tarvitaan ainakin **Yhteyshenkilö**-sivun ja muiden liittyvien objektien lukuoikeudet [!INCLUDE [prod_short.md](includes/prod_short.md)] -yrityksessä.

### <a name="can-i-use-contact-search-if-im-a-delegated-admin" />Voiko delegoitu järjestelmänvalvoja käyttää yhteyshenkilöhakua?

Kyllä. Yhteyshenkilöitä ja yhteyshenkilön tietoja voi hakea, jos käyttäjällä on delegoidun järjestelmänvalvojan rooli organisaatiossa.

### <a name="is-contact-search-affected-by-api-limits" />Vaikuttavatko ohjelmointirajapinnan rajoitukset yhteyshenkilöhakuun?

Kyllä. Yhteyshenkilöiden haku Teamsista perustuu [!INCLUDE [prod_short.md](includes/prod_short.md)] v2.0 -ohjelmointirajapintoihin ja kaikki käytön hallinnassa käytetyt ohjelmointirajapintojen rajoitukset koskevat sitä. Lisätietoja rajoituksista on kohdassa [Tämän hetkiset ohjelmointirajapintojen rajoitukset](/dynamics-nav/api-reference/v2.0/dynamics-current-limits).

### <a name="why-does-it-sometimes-ask-me-to-set-up-the-app" />Miksi sovelluksen määrittämistä pyydetään joskus?

Kun kirjaudut Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellukseen ensimmäisen kerran, sovellus yrittää määrittää [!INCLUDE [prod_short.md](includes/prod_short.md)]in ensisijaisen yrityksen. Jos sovellus ei pysty määrittämään yritystä, on ehkä siirryttävä **asetuksiin** valitsemaan yritys, jossa haku halutaan tehdä. Näin voi tapahtua esimerkiksi silloin, jos käytettävissä on useita yrityksiä organisaation eri ympäristöissä. Siinä tapauksessa yritys on valittava ennen haun aloittamista.  

Sovellus voi myös pyytää siirtymään **asetuksiin**, jos sinulla ei ole tuotteen [!INCLUDE [prod_short.md](includes/prod_short.md)] tilausta, jos tuotteen [!INCLUDE [prod_short.md](includes/prod_short.md)] ympäristöjä ei ole tai tilillä ei ole tuotteen [!INCLUDE [prod_short.md](includes/prod_short.md)] käyttöoikeutta.

### <a name="id-like-to-search-for-items-or-records-from-other-tables-can-i-do-this-from-teams" />Haluan hakea nimikkeitä tai tietueita muista taulukoista. Onko tämä mahdollista myös Teamsissa?

Haku muista taulukoista ei ole mahdollista tällä hetkellä. Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus tekee hakuja vain [!INCLUDE [prod_short.md](includes/prod_short.md)] -yhteyshenkilöluettelossa, joka voi sisältää toimittajia, asiakkaita ja muita yhteyshenkilöitä.

Jos haluat, että hakuominaisuudet kehittyvät sisältämään muita taulukoita, yhteisöä kannustetaan lisäämään idea tai äänestämään aiemmin luotuja ideoita osoitteessa https://aka.ms/BusinessCentralIdeas.

## [Korttien käsitteleminen](#tab/cards)

### <a name="which-types-of-links-does-the-app-support" />Minkä tyyppisiä linkkejä sovellus tukee?

Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus reagoi useimpiin [!INCLUDE [prod_short.md](includes/prod_short.md)] -verkkoasiakkaan linkkeihin. Kun linkki viittaa yhteen sivun tietueeseen, kortissa näkyvät kyseisen tietueen kentät. Tuetut sivutyypit ovat seuraavat: 

- Korttisivut, kuten nimikekortti
- Asiakirjasivut, kuten myyntitilausasiakirja
- ListPlus-sivut, jotka edustavat yhtä tietuetta, joka koostuu muista tietueista, kuten pankkitilin täsmäytyslaskelma
- Yksinkertaiset luettelosivut, joilla tietueessa ei ole mahdollisuutta poratua erilliseen tietosivuun; esimerkiksi postinumeroluettelo

Kun liität linkin verkkoasiakkaan URL-pääosoitteeseen, esimerkiksi https://businesscentral.dynamics.com, kortissa näkyy tietoja, joiden avulla uudet käyttäjät voivat aloittaa [!INCLUDE [prod_short.md](includes/prod_short.md)]in käytön.

### <a name="how-do-i-delete-a-card-i-sent-to-a-chat" />Miten poistan keskusteluun lähettämääni kortin?

Et voi poistaa korttia, jonka olet jo lähettänyt keskusteluun. Voit kuitenkin poistaa koko viestin, johon kortti kuuluu.

Viestin tekijänä voit poistaa kaikki viestit, jotka lähetit keskusteluihin henkilön, ryhmän tai kanavan kanssa – ellei järjestelmänvalvoja ole määrittänyt käytäntöjä, jotka estävät viestien poistamisen. Jos moderoit kanavaa kanavan omistajana, järjestelmänvalvojasi on saattanut myös myöntää sinulle oikeuden poistaa kaikki kanavan viestit, myös muiden käyttäjien lähettämät viestit.

Kortin sisältävän viestin poistaminen ei poista tai vaikuta [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovelluksen tietoihin.

### <a name="do-cards-always-show-up-to-date-information" />Näyttävätkö kortit aina ajan tasalla olevat tiedot?

Ei. Teamsissa korttien kenttien arvot, myös kuvat, perustuvat tietoihin, jotka olivat käytettävissä, kun kyseinen kortti lähetettiin chattiin. [!INCLUDE [prod_short.md](includes/prod_short.md)] -kortit eivät päivity automaattisesti Teamsissa. 

### <a name="why-dont-cards-show-more-information-instead-of-just-the-page-name-and-details-button" />Miksei korteissa ole lisätietoja vain sivun nimi- ja tiedot -painikkeiden sijaan?

Järjestelmänvalvoja on saattanut määrittää Teams-integroinnin niin, että kortit eivät näytä tietueita koskevia tietoja. Lisätietoja on ohjeaiheessa [Korttien tietuetietojen näyttäminen tai piilottaminen](admin-teams-integration.md#show-or-hide-record-data-on-cards).

### <a name="will-others-see-my-card-if-they-dont-have-the--app-for-teams" />Näkevätkö muut korttini, jos heillä ei ole Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellusta?

Kun kirjoitat ja lähetät viestin keskusteluun, jossa on kortti, kaikki käyttäjät näkevät kortin, vaikka he eivät olisikaan asentaneet Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellusta.

### <a name="how-do-i-find-out-which-company-a-card-in-teams-belongs-to" />Miten saan selville, mihin yritykseen Teams-kortti kuuluu?

Jos työskentelet eri [!INCLUDE [prod_short.md](includes/prod_short.md)] -yrityksissä, kysy järjestelmänvalvojalta yritystunnuksen käyttöönottoa jokaiselle yritykselle. Kun toiminto on käytössä, tämä selkeä vihje näkyy Teamsissa kaikissa tietoikkunoissa ja siinä näkyy yritys ja ympäristö, johon tietue kuuluu. Lisätietoja yrityksen merkin määrittämisestä on kohdassa [Yrityksen merkkien näyttäminen](admin-company-information.md#badge).

## [Korttitietojen käsitteleminen](#tab/carddetails)

### <a name="where-is-the-save-button-in-the-details-window-in-teams" />Missä on tietoikkunan Tallenna-painike Teamsissa?

[!INCLUDE [prod_short.md](includes/prod_short.md)] tallentaa mihin tahansa kenttään tekemäsi muutokset automaattisesti heti, kun poistut kentästä. Jos haluat poistua kentästä, napsauta/napauta mitä tahansa kohtaa kentän ulkopuolella tai siirry seuraavaan kenttään sarkaimen avulla. Kun tiedot tulevat näkyviin tietoikkunan valintaikkunaan, sinun on ehkä valittava **OK**-painike jotta [!INCLUDE [prod_short.md](includes/prod_short.md)] tallentaisi muutokset.

### <a name="if-i-choose-to-view-details-for-a-card-will-other-users-see-my-details-window" />Jos valitsen katsoa kortin tiedot, näkevätkö muut käyttäjät tietoikkunani?

Ei. Siinä missä kaikki keskustelussa tai kokouksessa olevat voivat tarkastella itse korttia, tietoikkuna avautuu vain omassa laitteessa, kun valitset **Tiedot**. Muiden käyttäjien täytyy valita **Tiedot**, jos he haluaisivat tarkastella tietoikkunaa laitteissaan.

### <a name="can-i-start-a-teams-call-from-the-details-window-in-teams" />Voinko aloittaa Teams-puhelun Tiedot-ikkunasta Teamsissa?

Kyllä. Jos käytät Teams-työpöytäsovellusta, voit aloittaa puhelun valitsemalla linkitetyn numeron puhelinnumerokentässä. Tällainen kenttä on esimerkiksi **Matkapuhelimen numero**. kentästä **Yhteyshenkilö**-kortissa. Teamsin täytyy olla määritetty soittovalintasovelluksesi.

Jos haluat soittaa paikallisiin tai kansainvälisiin lankapuhelimiin ja matkapuhelimiin, Teams edellyttää, että sinulla on Business Voice -käyttöoikeus yrityspuheluita varten. Sinun täytyy myös määrittää Teams puheluratkaisuksesi. Lisätietoja on Teams-dokumentaation ohjeaiheessa [Teams-ääniratkaisun suunnitteleminen](/microsoftteams/cloud-voice-landing-page).

### <a name="can-i-print-documents-from-the-details-window-in-teams" />Voinko tulostaa asiakirjoja Teamsin tietoikkunasta?

Kyllä. Tulostat raportteja ja muita asiakirjoja käyttämällä [!INCLUDE [prod_short.md](includes/prod_short.md)] -vakiotulostustoimintoa ja mitä tahansa pilvipohjaista tulostinta, joka on määritetty **Tulostimen hallinta** -sivulla [!INCLUDE [prod_short.md](includes/prod_short.md)]issa. Et voi tulostaa Teamsista asiakaslaitteesi tunnistamiin paikallisiin tulostimiin, kuten tulostimiin, joilla tavallisesti tulostetaan selaimesta. Tästä syystä et voi tulostaa raportin esikatseluikkunasta, vaan vain pääraportin pyyntösivulta suoraan pilvitulostimiin.

Lisätietoja pilvitulostimien määrittämisestä on kohdassa [Tulostimien määrittäminen](ui-specify-printer-selection-reports.md).

### <a name="can-i-access-the-camera-from-the-details-window-in-teams" />Voinko käyttää kameraa Teamsin tietoikkunasta?

Kyllä. Kaikki tietoikkunan [!INCLUDE [prod_short.md](includes/prod_short.md)] -ominaisuudet, jotka käyttävät kameraa, ovat saatavilla kaikissa Teams-asiakkaissa.

### <a name="can-i-access-my-location-from-the-details-window-in-teams" /><a name="location"></a>Voinko käyttää sijaintiani Teamsin tietoikkunasta?

Jos käytät [!INCLUDE [prod_short.md](includes/prod_short.md)] -ohjelman nykyisiä sijaintisi koordinaatteja käyttäviä toimintoja, kuten karttoja, sinun on käytettävä Teamsia selaimessa tai Teams-mobiilisovelluksessa. Sijainti ei ole käytettävissä, kun käytetään Teams-työpöytäsovellusta.

### <a name="how-do-i-open-the-details-in-a-new-window" />Miten tiedot avataan uudessa ikkunassa?

Tietoikkunan avaamisesta eri ikkunassa on hyötyä moniajoon tai liiketoimintatietojen työstämiseen, ja Teamsin keskustelu- ja muiden toimintojen käyttäminen on silti mahdollista. Jos haluat avata tiedot omassa ikkunassaan, valitse **Avaa selaimessa** ikkunan oikeassa yläkulmassa olevasta ellipsivalikosta (**...**).

## [Yhteistyö vieraiden kanssa](#tab/collaborating)

### <a name="can-i-share-cards-with-users-outside-my-organization" />Voinko jakaa kortteja organisaation ulkopuolisten käyttäjien kanssa?

Kyllä. Kun kirjoitat ja lähetät viestin, jossa on kortti, kaikki chatin vastaanottajat näkevät kortin – vaikka he olisivat vieraita tai organisaation ulkopuolisia. Asiakkaat voivat myös avata tiedot-ikkunan, jos heille on myönnetty käyttöoikeus [!INCLUDE [prod_short.md](includes/prod_short.md)] -tietoihin.

### <a name="is-the-experience-any-different-for-users-that-are-guests" />Onko kokemus erilainen käyttäjille, jotka ovat vieraita?

Kyllä. Organisaation ulkopuolisten vieraskäyttäjien kutsuminen osallistumaan keskusteluun tai kanavaan antaa heille samankaltaisen mutta ei identtisen kokemuksen kuin organisaation käyttäjille. Kun vieras vastaanottaa viestin, jossa on kortti, hän voi tarkastella sitä. Asiakkaat voivat myös avata tietosivun, jos heillä on kyseisten tietojen käyttöoikeus [!INCLUDE [prod_short.md](includes/prod_short.md)]issa ja jos heille on määritetty [!INCLUDE [prod_short.md](includes/prod_short.md)] -käyttöoikeus organisaatiossa.

Tietolinkin valitseminen missä tahansa Business Central -kortissa kirjaa käyttäjän siihen ympäristöön, josta kortti jaettiin, mikäli käyttäjällä on ympäristön käyttöoikeus.

Vieraskäyttäjät eivät saa käyttää yhteishenkilöhakua, koska se on sidottu alkuperäiseen vuokraajaan eikä tällaista delegoitua skenaariota tueta tällä hetkellä.

Kun vieras kirjoittaa viestin, linkit kummankaan [!INCLUDE [prod_short.md](includes/prod_short.md)]iin eivät laajene korteiksi.

Lisätietoja vieraiden ja tiimin jäsenten kokemusten samankaltaisuuksista ja eroista on Teams-ohjeiden kohdassa [Teamsin vieraskokemus](/MicrosoftTeams/guest-experience).

### <a name="how-does-a-guest-user-install-the--app" />Miten vieraskäyttäjä asentaa [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovelluksen?

Vierailla ei ole pääsyä sovelluskauppaan, jotta he voisivat asentaa itse sovelluksia. Sovellus voidaan kuitenkin asentaa heille automaattisesti organisaatiosi käytäntöjen mukaan. Toinen tapa, jolla vieraskäyttäjä voi asentaa [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovelluksen, on vastaanottaa chat-viesti, joka sisältää [!INCLUDE [prod_short.md](includes/prod_short.md)] -kortin. Tässä tapauksessa käyttäjä valitsee kortin **Tiedot**-painikkeen tai -valikon ja asentaa sitten [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovelluksen käytettäväksi organisaatiosi kanssa. Sovelluksen asentamisen jälkeen käyttäjä ei automaattisesti saa mitään oikeuksia käyttää [!INCLUDE [prod_short.md](includes/prod_short.md)] -tietojasi.

## [Jaa Teamsiin](#tab/share)

### <a name="does-share-to-teams-send-a-compact-card" />Lähettääkö Jaa Teamsiin -toiminto kompaktin kortin?

Kyllä. Linkki laajenee automaattisesti korttiin, jos Teamsille on asennettu Business Central-sovellus. 

### <a name="will-recipients-receive-the-message-from-me-or-from-a-business-central-service-account" />Saavatko vastaanottajat viestin minulta vai Business Central -palvelutililtä?

Kun käytät Jaa Teamsiin -toimintoa, viesti lähetetään henkilölle, ryhmälle tai kanavalle, samalla lailla kuin jos olisit lähettänyt viestin itse Microsoft Teamsissa. Vastaanottajat näkevät viestisi käyttämässään Teams-asiakasohjelmassa ja voivat reagoida ja vastata tavalliseen tapaan. 

### <a name="is-share-to-teams-available-in-business-central-on-premises" />Onko Jaa Teamsiin -toiminto saatavilla Business Central on-premises -versiolle?

Ei. Tämä toiminto on saatavilla vain verkkoasiakasohjelmalle [!INCLUDE [prod_short.md](includes/prod_short.md)] onlinessa samoin kuin Teamsin [!INCLUDE [prod_short.md](includes/prod_short.md)] -sovellus. [!INCLUDE [prod_short.md](includes/prod_short.md)]&mdash; -käyttöönottotyyppejä, joita Microsoft ei isännöi tai hallitse – kuten paikallista, hybridipilveä tai yksityistä pilveä – ei tueta.

### <a name="does-share-to-teams-grant-permissions-to-recipients" />Myöntääkö Jaa Teamsiin -toiminto käyttöoikeuksia vastaanottajille?

Ei. Kun jaat henkilön, ryhmän tai kanavan kanssa, käyttöoikeudet säilyvät ennallaan. Käyttäjät, joilla on jo oikeus tarkastella linkin osoittamia sivuja ja tietoja, voivat tehdä niin. Jos käyttäjällä ei ole oikeutta tarkastella kyseistä sivua tai tietoja tai hänellä ei ole [!INCLUDE [prod_short.md](includes/prod_short.md)] -käyttöoikeutta, näyttöön tulee virhe sanoma. 
 
### <a name="must-i-have-the-teams-desktop-app-installed-to-use-share-to-teams" />Pitääkö Teams-työpöytäsovellus olla asennettuna, jotta voin käyttää Jaa Teamsiin -toimintoa?

Ei. Kaikki tarvitsemasi on kelvollinen tili, jolla on Microsoft Teams -käyttöoikeus. 

### <a name="is-share-to-teams-available-in-all-business-central-clients" />Onko Jaa Teamsiin -toiminto saatavilla kaikille Business Central -asiakasohjelmille?

Tällä hetkellä Jaa Teamsiin -toiminto on saatavilla työpöydän verkkoasiakkaalle, tietoikkunassa Teamsissa ja avattaessa sivua uudessa ikkunassa Outlook-apuohjelmasta.

### <a name="where-do-i-find-share-to-teams-in-business-central" />Mistä löydän Jaa Teamsiin -toiminnon Business Centralissa?

**Jaa Teamsiin -toiminto** löytyy kaikkien sivujen **Jaa**-valikosta, kuten kortti- ja asiakirjasivuista, luettelo- tai laskentataulukko-sivuista, mukaan lukien mukautetut sivut. Toiminto ei ole käytettävissä valintaikkunoissa tai sivuissa, jotka näkyvät valintaikkunoina, kuten hakusivuissa tai ohjatuissa toiminnoissa.

---
## <a name="see-also" />Katso myös

[[!INCLUDE [prod_short](includes/prod_short.md)]in ja Microsoft Teamsin integroinnin yleiskatsaus](across-teams-overview.md)  
[Microsoft Teamsin [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen asentaminen](across-install-app-for-teams.md)  
[Asiakkaiden, toimittajien ja muiden yhteyshenkilöiden hakeminen Microsoft Teamsista](across-search-contacts-teams.md)  
[Tietueiden jakaminen Microsoft Teams -keskusteluissa](across-working-with-teams.md)  
[Vianetsintä – Teams](admin-teams-troubleshooting.md)  
[Yrityksen ja muiden asetusten muuttaminen Teamsissa](across-teams-settings.md)  
[Teamsin integroinnin kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
