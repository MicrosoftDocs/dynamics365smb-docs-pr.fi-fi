---
title: Kirjausryhmän määrittäminen
description: 'Yleiskatsaus kirjausryhmistä, joiden avulla voit säästää aikaa ja välttää virheitä tapahtumia kirjattaessa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'posting setup, initialize'
ms.search.form: '312, 313'
ms.date: 08/26/2022
ms.author: bholtorf
---
# Määritä kirjanpidon kirjausryhmät

Kirjausryhmät yhdistävät entiteetit kirjanpitotileihin. Esimerkkejä entiteeteistä ovat asiakkaat, toimittajat, nimikkeet, resurssit sekä myynti- ja ostoasiakirjat. Kirjausryhmät säästävät aikaa ja auttavat välttämään virheitä tapahtumia kirjattaessa. Tapahtuman arvot viedään kyseisen objektin kirjausryhmässä määritetylle tilille. Kirjausryhmiä varten tarvitaan vain tilikartta. Lisätietoja on kohdassa [Tilikartan määrittäminen](finance-setup-chart-accounts.md).  

Kirjausryhmiä on kolmenlaisia:  

* Yleiset

  Määritä, kenelle myyt ja keneltä ostat sekä mitä myyt ja ostat. Voit myös yhdistää ryhmät määrittämään esimerkiksi tuloslaskelmatilit, joille kirjaukset tehdään, tai suodattaa raportteja ryhmien avulla.  
* Määrätty

  Käytä esimerkiksi myyntiasiakirjoa sen sijaan, että kirjaisit suoraan pääkirjanpitoon. Kun luot asiakastapahtumia, vastaavat tapahtumat tulevat myös pääkirjanpitoon.  
* Vero

  Määritä niitä henkilöitä koskevat veroprosentit ja laskentatyypit, joille myyt ja joilta ostat. Ne koskevat myös myymiäsi ja ostamiasi nimikkeitä.

Seuraavissa osioissa käsitellään kutakin kirjausryhmätyyppiä.  

## Yleiset kirjausryhmät

Seuraavassa taulukossa kuvaillaan yleisiä kirjausryhmätyyppiä.

| Tyyppi | Kuvaus |
| --- | --- |
| Yleiset liiketoiminnan kirjausryhmät |Liittämällä tämän ryhmän asiakkaisiin ja toimittajiin voi määrittää, kenelle myyt ja keneltä ostat. Määritä nämä kirjausryhmät **Yleiset liiketoim. kirj.ryhmät** -sivulla. Mieti määrityksiä tehdessäsi, kuinka monta ryhmää tarvitset myyntien ja ostojen erittelemiseen. Voit esimerkiksi ryhmitellä asiakkaat ja toimittajat maantieteellisen alueen tai liiketoiminnan tyypin mukaan. |
| Yleiset tuotteen kirjausryhmät |Liittämällä tämän ryhmän nimikkeisiin ja resursseihin voit määrittää, mitä myyt ja mitä ostat. Määritä nämä kirjausryhmät **Yleiset tuotteen kirj.ryhmät** -sivulla. Mieti määrityksiä tehdessäsi, kuinka monta ryhmää tarvitse erittelemään tuotteiden (nimikkeiden ja resurssien) mukaisen myynnin ja nimikkeiden mukaiset ostot. Jaa nämä ryhmät esimerkiksi raaka-aineiden, resurssien ja kapasiteetin mukaan. |
| Yleiset kirjausasetukset |Yhdistä liiketoiminnan ja tuotteen kirjausryhmiä ja valitse tilit, joille kirjaukset tehdään. Kullekin liiketoiminnan ja tuotteen kirjausryhmien yhdistelmälle voi määrittää eri joukon pääkirjanpidon tilejä. Saman nimikkeen myynnin voi siis esimerkiksi kirjata eri pääkirjanpitotileille, sillä asiakkaille on määritetty eri liiketoiminnan kirjausryhmät. Määritä nämä asetukset **Yleiset kirjausasetukset** -sivulla. |

## Erityiset kirjausryhmät

Seuraavassa taulukossa kuvaillaan tietotyyppikohtaisia nimiketyyppejä.

|Tyyppi | Kuvaus |
| --- | --- |
| Asiakkaan kirjausryhmät |Määritä tilit, joita käytetään, kun kirjaat myyntireskontran tapahtumia. Jos käytät varastoa, jossa on myyntisaatavia, asiakkaille määritetty yleinen liiketoiminnan kirjausryhmä ja varastonimikkeelle määritetty yleinen tuotteen kirjausryhmä määrittävät, mille tileille myyntitilausrivin tapahtumat kirjataan. Lisätietoja on [Yleiset kirjausryhmät](#general-posting-groups) -kohdan kohdissa *Yleiset liiketoiminnan kirjausryhmät* ja *Yleiset tuotteen kirjausryhmät*. Määritä nämä kirjausryhmät **Asiakkaan kirjausryhmät** -sivulla. |
| Toimittajan kirjausryhmät |Määritä, mihin ostovelkatilien, palveluveloitustilien ja maksualennustilien tapahtumat kirjataan. Tämä muistuttaa asiakkaan kirjausryhmiä. Määritä nämä kirjausryhmät **Toimittajan kirjausryhmät** -sivulla. |
| Varaston kirjausryhmät |Määritä varaston kirjausryhmät, jotka sitten määritetään soveltuville nimiketileille **Varastokirjauksien asetukset** -sivulla. Kun kirjaat nimikettä koskevia tapahtumia, järjestelmää tekee kirjaa KP-tilille, joka on määritetty nimikkeeseen linkitetylle varaston kirjausryhmän ja sijainnin yhdistelmälle. Varaston kirjausryhmät ovat myös kätevä tapa järjestää varasto, sillä voit erotella nimikkeet kirjausryhmien mukaan, kun luot raportteja. Määritä nämä kirjausryhmät **Varaston kirjausryhmät** -sivulla. |
| Pankkitilin kirjausryhmät |Määritä pääkirjanpitotilit, joihin pankkitilitapahtumat kirjataan. Tämä esimerkiksi yksinkertaistaa tapahtumien jäljittämistä ja pankkitilin täsmäyttämistä. Määritä nämä kirjausryhmät **Pankkitilin kirjausryhmät** -sivulla. Suosittelemme, että näiden KP-tilien **Suorakirjaus**-kentän arvoksi asetetaan *Ei*. |
| Käyttöomaisuuden kirjausryhmät |Määritä erilaisten kulujen ja kustannusten tilit. Näitä kuluja ja kustannuksia ovat esimerkiksi hankintamenot, kokonaispoistosummat, hankintamenot luovutettaessa, kokonaispoistot luovutettaessa, voitot luovutettaessa, tappiot luovutettaessa, ylläpitokulut ja poistokustannukset. Määritä nämä kirjausryhmät **KO:n kirjausryhmät** -sivulla. |

### Korvaavien asiakkaan tai toimittajan kirjausryhmien salliminen asiakirjoille

[!INCLUDE [preview](includes/preview.md)]

Voit antaa käyttäjien valita eri asiakkaan ja toimittajan kirjausryhmät kuin oletusarvot, kun he työskentelevät myynti- tai ostoasiakirjojen ja päiväkirjojen parissa.

Jos haluat sallia muutokset asiakkaan kirjausryhmiin, valitse **Salli useita kirjausryhmiä** **Myyntien ja myyntisaamisten asetukset**- ja **Huoltohallinnon asetukset** -sivuilla ja **Ostojen ja ostovelkojen asetukset** -sivulla toimittajan kirjausryhmien muutoksille.

**Asiakkaan kirjausryhmät**- tai **Toimittajan kirjausryhmät** -sivuilla voit määrittää kirjausryhmät, jotka sallitaan korvaaviksi valitsemalla **Korvaukset**. Korvaavat kirjausryhmät voivat korvata asiakkaalle tai toimittajalle määritetyt oletusasiakas- tai -toimittajakirjausryhmät.

Kun olet määrittänyt tämän, voit valita sallituista korvaavista kirjausryhmistä ja muuttaa asiakkaan tai toimittajan kirjausryhmää kirjattaessa myynti- tai ostoasiakirjoja ja päiväkirjoja. Korvaavat asiakkaan tai toimittajan kirjausryhmät kopioidaan kirjattuihin asiakirjoihin ja päiväkirjoihin, ja maksettavat tai saatavat KP-tapahtumat kirjataan korvaaville kirjausryhmille määritetyille KP-tileille.

Esimerkiksi silloin, kun kirjataan lasku ja maksu, jotka on kirjattu eri asiakkaan tai toimittajan kirjausryhmien kanssa (eri KP-tilit), [!INCLUDE[prod_short](includes/prod_short.md)] siirtää summat KP-tilien välillä, jotta ne tasapainotetaan.

## Verokirjausryhmä

Seuraavassa taulukossa kuvaillaan veroihin liittyviä kirjausryhmätyyppiä.

| Tyyppi | Kuvaus |
| --- | --- |
| Liiketoiminnan verokirjausryhmät |Määrittää, miten asiakkaiden ja toimittajien arvonlisävero lasketaan ja kirjataan. Määritä nämä kirjausryhmät **Veron liiketoim. kirj.ryhmät** -sivulla. Mieti määrityksiä tehdessäsi, kuinka monta ryhmää tarvitset. Siihen voi vaikuttaa esimerkiksi paikallinen lainsäädäntö ja se, käytkö sekä kotimaan- että ulkomaankauppaa. |
| Tuotteen verokirjausryhmät |Ilmoita, mitä verolaskelmia on tehtävä nimike- tai resurssityypeille, joita ostat tai myyt. |
| Verokirjausten asetukset |Yhdistä liiketoiminnan verokirjausryhmät ja tuotteen verokirjausryhmät. Kun täytät yleisen päiväkirjarivin, ostorivin tai myyntirivin, käytettävät tilit tunnistetaan yhdistelmän avulla. |

Jos maasi tai alueesi käyttää arvonlisäveroa (ALV), lisätietoja on kohdassa [Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen](finance-setup-vat.md).  

## Esimerkki kirjausryhmien linkittämisestä

Käytettävä skenaario.  

Asiakaskortista on valittu seuraavat kirjausryhmät:  

* Yleinen liiketoiminnan kirjausryhmä
* Asiakkaan kirjausryhmä  

Nimikekortista on valittu seuraavat kirjausryhmät:  

* Yleinen tuotteen kirjausryhmä  
* Varaston kirjausryhmä  

Kun luot myyntiasiakirjan, myyntiotsikko käyttää asiakaskortin tietoja ja myyntirivit käyttävät nimikekortin tietoja.  

* Tuottojen kirjaus (tuloslaskelma) määräytyy yleisen liiketoiminnan kirjausryhmän ja yleisen tuotteen kirjausryhmän yhdistelmän perusteella.  
* Myyntireskontran kirjaus (tase) määräytyy asiakkaan kirjausryhmän perusteella.  
* Varaston kirjaus (tase) määräytyy varaston kirjausryhmän perusteella.  
* Myytyjen tavaroiden kustannusten kirjaus (tuloslaskelma) määräytyy yleisen liiketoiminnan kirjausryhmän ja yleisen tuotteenkirjausryhmän yhdistelmän perusteella.  

Kirjausajankohta määräytyy asetusten mukaan. Esimerkiksi jaksoittaiset toiminnot, kuten varaston kustannusten kirjaus- tai kustannusnimikkeiden muutostapahtumat, vaikuttavat ajoitukseen.

## Kirjausasetusrivien kopioiminen

Mitä enemmän tuotteen ja liiketoiminnan kirjausryhmiä on luotu, sitä enemmän rivejä näkyy **Yleiset kirjausasetukset** -sivulla. Yrityksen yleisten kirjausasetusten määrittäminen voi vaatia paljon tietojen syöttämistä. Vaikka liiketoiminnan ja tuotteen kirjausryhmiä saattaa olla useita, eri yhdistelmillä voi kuitenkin kirjata samoille pääkirjanpidon tileille. Manuaalisia vientejä voi rajoittaa kopioimalla pääkirjanpidon tilit aiemmin luodulta riviltä **Yleiset kirjausasetukset** -sivulla.

## Kirjausryhmien määrittäminen liikkeellä ollessa

Jotta käyttäjät voisivat aloittaa nopeammin, [!INCLUDE[prod_short](includes/prod_short.md)] voi näyttää ilmoitukset puuttuvista pääkirjanpitotileistä asiakirjojen eri kirjausryhmien asetuksissa. Jos haluat saada nämä ilmoitukset, varmista, että **KP-tili puuttuu kirjausryhmästä tai asetuksesta** -ilmoitus on valittuna **Omat ilmoitukset** -sivulla, jonka voit avata **Omat asetukset**-sivun **Muuta vastaanotettaessa ilmoituksia** -kentän avulla.  

Tällöin saat ilmoituksen, kun työskentelet asiakirjan parissa, joka käyttää kirjausryhmää tai kokoonpanoa, josta puuttuu vaadittu pääkirjanpitotili. Valitse ilmoituksessa oleva linkki avataksesi sivun, jolla voit tehdä tarvittavat muutokset, jos sinulla on siihen oikeus.  

> [!NOTE]
> Jotta voisit siirtyä suoraan kirjausryhmään tai asetukseen, joista puuttuu pääkirjanpitotili, [!INCLUDE[prod_short](includes/prod_short.md)] luo paikkamerkkikirjausryhmän tai -asetukset. Kirjausryhmät ja -asetukset ovat tapa, jolla kirjanpitäjä voi hallita sitä, kuinka kirjaukset kirjataan pääkirjaan, joten tällainen kirjausryhmien ja -asetusten luominen oikeaan aikaan ei ehkä ole sallittua organisaatiossasi.  
>
> Poista siinä tapauksessa käytöstä *KP-tili puuttuu kirjausryhmästä tai asetuksesta* -ilmoitus, ja tee sitten tarvittavat muutokset kirjausryhmään, asetuksiin tai asiakirjaan yhdessä kirjanpitäjän kanssa. Tämä on tärkeä vaihe, koska asiakirjojen kirjaamisen jälkeen kaikkia virheellisesti käytettyjä kirjausryhmiä tai asetuksia ei voi poistaa, koska niille on luotu pääkirjanpidon tapahtumia.

Vuoden 2022 1. julkaisuaallossa voit käyttää **Yleiset kirjausasetukset** -sivun **Estetty**-kenttää, jos haluat estää käyttäjiä vahingossa käyttämästä asetuksia, jotka eivät enää ole merkityksellisiä uusissa kirjauksissa.  

## Kirjausryhmän virheiden vianetsintä

Kirjausryhmät ovat eräs kehittyneimmistä käsitteistä, jotka määritetään [!INCLUDE[prod_short](includes/prod_short.md)]issa. Jos niitä ei ole määritetty oikein, asiakirjojen tai päiväkirjarivien kirjauksessa voi ilmetä virheitä. Virheet johtuvat esimerkiksi siitä, miten kirjanpitotilit määritetään tai miten kirjausryhmät yhdistetään virheellisesti.

Kun jotain on vialla, [!INCLUDE[prod_short](includes/prod_short.md)] -näyttöön tulee **Virhesanomat**-sivu. **Virhesanomat**-sivu voi helpottaa ongelman tunnistamista ja ratkaisemista. Sivulla on kuvaus virheestä, joka korostaa kirjausryhmän asetukset, joihin on kiinnitettävä huomiota. Viesti voi esimerkiksi olla: "Myynnin ennakkomaksutililtä puuttuvat yleiset kirjausasetukset". On myös linkki avata sivu, joka on ongelman aiheuttaja, joten voit nopeasti ratkaista sen.  

> [!NOTE]
> Yllä kuvattu virheen käsittely ei ole käytettävissä nimike-, resurssi-, työntekijä- ja käyttöomaisuuspäiväkirjoissa tai KP-tileissä, jotka on lisätty kirjausryhmien paikallisiin versioihin.

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/posting-groups-dynamics-365-business-central/)

## Katso myös

[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
