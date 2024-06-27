---
title: Käyttöomaisuuden hallinta
description: Saat tietoja käyttöomaisuustoiminnoista sekä yleiskuvan käyttöomaisuuserien käsittelystä ja hallinnasta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="manage-fixed-assets"></a>Käyttöomaisuuden hallinta

[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman Käyttöomaisuus-sovellusalueesta saat yleiskuvan käyttöomaisuudestasi, ja voit varmistaa, että poistot ovat oikein. Se auttaa myös kunnossapitokulujen seuraamista, vakuutussopimusten hallinnoimista, käyttöomaisuustransaktioiden kirjaamista sekä monenlaisten raporttien ja tilastojen luomista.

## <a name="what-is-a-fixed-asset"></a>Mikä on käyttöomaisuus?

Käyttöomaisuuserät eroavat fyysisen varaston muista nimikkeistä. Käyttöomaisuus, joka tunnetaan myös pääomaomaisuuseränä, on aineellinen omaisuuserä, laitos tai väline (PP&E), jonka omistat tai jota hallinnoit odottaen, että se jatkaa tulojen tuottamista. Resurssi on käyttöomaisuus silloin, kun se on nimike, jota yrityksesi ei kuluta, myy tai muunna käteisenä seuraavan kalenterivuoden aikana. Käyttöomaisuuserät eroavat resursseista, jotka ovat käteisenä tai jotka muunnetaan käteiseksi seuraavien 12 kuukauden aikana. Käyttöomaisuuserät eroavat myös varastosta, koska varastoa kulutetaan yleensä lyhyessä ajassa.

## <a name="types-of-fixed-assets"></a>Käyttöomaisuuden tyypit

Yritykset investoivat yleensä muutamiin käyttöomaisuuseriin. Esimerkkejä:

- Rakennukset ja tilat
- Tietokonelaitteet ja ohjelmistot
- Huonekalut ja kalusteet
- Koneet
- Ajoneuvot

## <a name="understanding-fixed-asset-accounting"></a>Käyttöomaisuuden kirjanpidon ymmärtäminen

Käyttöomaisuuden laskenta tarkoittaa, että pääomaomaisuudesta on pidettävä tarkkoja kirjanpitotietoja. Nämä tietueet sisältävät yksityiskohtaisia tietoja resurssin elinkaaren viidestä vaiheesta. Alkuperäisen oston jälkeen kunkin käyttöomaisuuserän elinkaaressa on vähintään kolme seuraavaa vaihetta:

- Hankinta: Kirjoihin lisätään uusi käyttöomaisuus.
- Poisto: resurssin jaksottainen arvon lasku kirjataan, ja poistomenetelmää käytetään laskennassa. Saat lisätietoja siirtymällä [KO:n poistolaskelmat](LocalFunctionality/India/FA_Depreciation.md) -kohtaan.
- Uudelleenarvostus: Omaisuuserän käypää markkina-arvoa arvioidaan. Lisätietoja on kohdassa [Käyttöomaisuuden arvon uudelleenmäärittäminen](fa-how-revalue.md).
- Arvonalentuminen: Tapahtumista tai olosuhteista johtuva arvon lasku kirjataan.
- Luovutus: Käyttöomaisuuserä myydään, hävitetään tai käytetään muuta tapaa, jolla omaisuuserästä luovutaan sen käyttöiän lopussa.

Tilintarkastukset sisältyvät myös yrityksen kirjanpitotietueiden yksityiskohtaisiin tarkastuksiin tilikauden kirjojen sulkemisen jälkeen. Olipa kyse sisäisistä tai ulkoisista tarkastuksista, saatat huomata epäjohdonmukaisuuksia tai eroja muistioiden ja käyttöomaisuuserien todellisen tilan välillä. Tilintarkastukset lisäävät käyttöomaisuuden ja kirjanpidon avoimuutta, jos menetät ennakoitua enemmän rahaa.

## <a name="video-overview"></a>Videon yleiskatsaus

Seuraavassa videossa käsitellään käyttöomaisuuden perusteet:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## <a name="initial-setup-of-fixed-assets"></a>Käyttöomaisuuden alustavat asetukset

Ennen käyttöomaisuuden hallintaa on tehtävä seuraavat määritykset:

- Oletusarvot
- Käyttöomaisuuden kirjanpito
- Kirjausryhmät ja -tyypit
- Kohdistusavaimet
- Käyttöomaisuuspäiväkirjat

Lisätietoja on kohdassa [Käyttöomaisuuden määrittäminen](fa-setup.md).

## <a name="fixed-assets-analytics"></a>Käyttöomaisuuden analyysi

Tässä osassa kuvataan analyysityökaluja, joita voit käyttää, kun haluat saada tietoja käyttöomaisuudesta.

| Vastaanottaja... | Katso |
| --- | --- |
| Tutustu käyttöomaisuuserien tietojen analysointimahdollisuuksiin. | [Käyttöomaisuuden analyysin yleiskatsaus](fa-analytics-overview.md) |
| Tee käyttöomaisuustietojen ad-hoc-analyysi suoraan luettelosivuilla ja kyselyissä. | [Käyttöomaisuuden tapauskohtainen analyysi](ad-hoc-analysis-fa.md) |
| Tutustu käyttöomaisuuden valmiisiin raportteihin. | [Valmiit käyttöomaisuusraportit](fa-reports.md) |
| Valvo kunnossapitokustannuksia. | [Kunnossapitokustannusten valvonta](fa-how-maintain.md#monitor-maintenance-costs)|
| Tarkkaile vakuutuksen kattavuutta. | [Vakuutuksen kattavuuden tarkkailu](fa-how-insure.md#to-monitor-insurance-coverage) |
| Katso luovutustapahtumia. | [Luovutustapahtumien tarkasteleminen](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Katso suunniteltuja luovutusarvoja. | [Suunniteltujen luovutusarvojen tarkasteleminen](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="register-fixed-assets"></a>Rekisteröi käyttöomaisuutta

Kunkin käyttöomaisuuserän osalta tulee määrittää kortti, joka sisältää tietoja niistä. Voit esimerkiksi määrittää rakennukset tai tuotantolaitteet voidaan pääkäyttöomaisuuseräksi, jolla on komponenttiluettelo. Resursseja voi ryhmitellä monella tavalla, esimerkiksi luokan, osaston tai sijainnin mukaan. Tämän jälkeen voit hankkia, kunnossapitää ja myydä käyttöomaisuutta. Voit myös määrittää budjetoitua käyttöomaisuutta. Budjetointi mahdollistaa minkä tahansa ennakoidun hankinnan ja myynnin sisällyttämisen raportteihin.

| Vastaanottaja  | Katso |
| --- | --- |
| Hallitse käyttöominaisuuserien budjetteja, budjetin hankintamenoja, käyttöomaisuuden luovutusten budjetointia ja poistojen budjetointia. |[Käyttöomaisuuden budjettien hallinta](fa-how-manage-budgets.md) |
| Luo käyttöomaisuus, liitä poistomenetelmät, kirjaa hankinnat ja jäännösarvot ja tulosta käyttöomaisuusluettelot. |[Käyttöomaisuuden hankkiminen](fa-how-acquire.md) |

## <a name="set-up-depreciations-for-your-fixed-assets"></a>Määritä käyttöomaisuuden poistot

Käyttöomaisuuden poistoja sekä muita käyttöomaisuuden rahoitustapahtumia voidaan seurata määrittämällä niistä jokaiselle vähintään yksi poistokirja. Resurssien poistaminen edellyttää muutamien vaiheiden suorittamista:

1. Aja raportti, joka laskee jaksottaiset poistot.
1. Täytä päiväkirja tuloksena olevilla merkinnöillä.
1. Kirjaa päiväkirja.

[!INCLUDE[prod_short](includes/prod_short.md)] tukee useita poistotapoja. Saat lisätietoja siirtymällä [Poistomenetelmät](fa-depreciation-methods.md) -kohtaan. Voit määrittää useita poistokirjoja käyttöomaisuutta kohti eri tarkoituksia varten. Poistokirjat voivat käsitellä esimerkiksi veroraportointia tai sisäistä raportointia.

| Vastaanottaja  | Katso |
| --- | --- |
| Lisätietoja käyttöomaisuuden erilaisista poistotavoista. |[Poistotavat](fa-depreciation-methods.md) |
| Laske ja kirjaa poisto sekä analysoi poisto käyttöomaisuusraporteissa. |[Käyttöomaisuuden poistaminen tai kuolettaminen](fa-how-depreciate-amortize.md) |
| Muuttuneiden poistokirja-arvojen tarkastelu. | [Muuttuneiden poistokirja-arvojen tarkasteleminen](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification) |
| Tallenna manuaalisesti käyttöomaisuustapahtumat **Käyttöomaisuuden KP-päiväkirja**- tai **Käyttöomaisuuspäiväkirja**-sivulle sen mukaan, koskevatko tapahtumat talousraportointia vai sisäistä hallintaa. | [Käyttöomaisuuden poiston määrittäminen](fa-how-setup-depreciation.md) |

## <a name="fixed-assets-maintenance-and-insurance"></a>Käyttöomaisuuden kunnossapito ja vakuutus

Voit tallentaa kunnossapitokulut ja seuraavan huoltopäivämäärän kullekin käyttöomaisuuserälle. Kunnossapitokulujen seuraaminen voi olla tärkeää budjetointia varten ja käyttöomaisuuden vaihtamisesta päätettäessä. Kukin käyttöoikeus voidaan liittää vähintään yhteen vakuutussopimukseen ja varmistaa, että sopimusmaksut vastaavat resurssien arvoa.

| Vastaanottaja  | Katso |
| --- | --- |
| Tallenna huoltokäynnit ja kirjaa kunnossapitokustannukset sekä seuraa niitä. |[Käyttöomaisuuden ylläpitäminen](fa-how-maintain.md) |
| Valvo kunnossapitokustannuksia. | [Kunnossapitokustannusten valvonta](fa-how-maintain.md#monitor-maintenance-costs)|
| Päivitä vakuutustiedot, kirjaa hankintakustannukset vakuutussopimuksiin, muokkaa vakuutuksen kattavuutta, katsele vakuutustilastoja ja luetteloi vakuutussopimukset. |[Käyttöomaisuuden vakuuttaminen](fa-how-insure.md) |
| Tarkkaile vakuutuksen kattavuutta. | [Vakuutuksen kattavuuden tarkkailu](fa-how-insure.md#to-monitor-insurance-coverage) |

## <a name="reclassify-transfer-split-upcombine-adjust-value-write-down-and-dispose-fixed-assets"></a>Uudelleenluokittelu, siirto, jakaminen/yhdistäminen, arvon muuttaminen, arvonalennus ja käyttöomaisuuden luovuttaminen

| Vastaanottaja  | Katso |
| --- | --- |
| Luokittele käyttöomaisuus uudelleen, siirrä käyttöomaisuus eri sijainteihin, jaa käyttöomaisuuseriä tai yhdistä niitä. |[Käyttöomaisuuserien siirtäminen, jakaminen tai yhdistäminen](fa-how-trans-split-combine.md) |
| Muuta käyttöomaisuuserien arvoja ja kirjaa arvonkorotus- sekä arvonalennustransaktiot. |[Käyttöomaisuuden uudelleenarvostus](fa-how-revalue.md) |
| Kirjaa luovutustransaktiot, tarkastele luovutustapahtumia ja kirjaa osittaisia luovutuksia. |[Käyttöomaisuuden luovuttaminen tai poistaminen käytöstä](fa-how-dispose-retire.md) |
| Katso luovutustapahtumia. | [Luovutustapahtumien tarkasteleminen](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Katso suunniteltuja luovutusarvoja. | [Suunniteltujen luovutusarvojen tarkasteleminen](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="tips-for-improving-your-fixed-asset-accounting"></a>Vinkkejä käyttöomaisuuslaskennan kehittämiseen

Käyttöomaisuuden kirjanpitostrategiassa voidaan toteuttaa muutamia asioita, jotka voivat auttaa varmistamaan, että tulot maksimoidaan.

- Määritä pääomasijoitukselle kynnysarvo. Kun ostat nimikkeen, määritä kiinteä summa pääomasijoitukselle. Summa auttaa varmistamaan kirjanpitokirjojen johdonmukaisuuden ja helpottaa kirjanpitovirheiden havaitsemista.
- Arvioi laitteiden elinkaari uudelleen. On tärkeää arvioida oikein aika, jonka käyttöomaisuutta voi käyttää alkuperäisiin tarkoituksiin. Koska kirjanpito ja poistot perustuvat oikeisiin elinkaariarvioihin, uudelleenarvosta tarvittaessa, koska ne voivat muuttua ajan mittaan.
- Merkitse resurssit. On tärkeää seurata ja merkitä resursseja koko niiden elinkaaren ajan, koska monet tekijät voivat vaikuttaa niiden arvoon. Merkitseminen auttaa seuraamaan nimikkeitä niiden elinkaaren eri vaiheissa, auttaa ehkäisemään varkauksia, poistamaan käyttövirheet ja tukemaan taloudellisia tilastoja.
- Automatisoi oivalluksia käyttöomaisuuden kirjanpito-ohjelmiston avulla. Manuaalisen aktiviteetin automatisointi tietojen seuraamiseksi käyttöomaisuuslaskentaohjelmiston avulla helpottaa prosessien valmistumista. Salasanasuojaus voi auttaa tarjoamaan pääsyn vain ihmisille, jotka tarvitsevat sitä ja jotka on koulutettu siihen.

## <a name="see-also"></a>Katso myös

[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuuden analyysin yleiskatsaus](fa-analytics-overview.md)  
[Talouden yleiskatsaus](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
