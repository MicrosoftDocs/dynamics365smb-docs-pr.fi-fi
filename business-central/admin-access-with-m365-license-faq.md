---
title: Usein kysyttyjä kysymyksiä käytöstä Microsoft 365 -käyttöoikeuksien avulla
description: 'Hanki vastauksia yleisimpiin kysymyksiin, jotka koskevat Business Centralin käyttöä Microsoft 365 -käyttöoikeuksilla.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: faq
ms.date: 11/22/2022
ms.custom: bap-template
---
# <a name="access-with-microsoft--licenses-faq" />Usein kysyttyjä kysymyksiä käytöstä Microsoft 365 -käyttöoikeuksien avulla

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Käyttäjät voivat käyttää Business Central -tietoja Microsoft Teamsissa käyttämällä Microsoft 365 -käyttöoikeuksiaan . Tämä artikkeli vastaa usein kysyttyihin kysymyksiin, joita järjestelmänvalvojat, konsultit ja muut ovat esittäneet. Kehittäjien tulisi katsoa kehittäjien usein kysytyt kysymykset. Jos sinulla on kysyttävää Business Centralin integroinnista Microsoft Teamsiin, katso [Teams – usein kysytyt kysymykset](teams-faq.md).

## [Käyttöoikeudet](#tab/permissions) 

### <a name="can-i-proactively-configure-different-starting-permissions-for-different-groups-of-users" />Voinko määrittää ennakoivasti erilaisia alustavia käyttöoikeuksia eri käyttäjäryhmille?

Et tällä hetkellä. Business Central sallii sinun määrittää vain yhden ryhmän käyttöoikeuksia, jotka kohdistetaan kaikille Microsoft 365 -käyttäjille, kun he kirjautuvat Business Centraliin ensimmäistä kertaa.

### <a name="can-i-proactively-configure-permissions-profiles-and-settings-for-individual-users-before-they-sign-in" />Voinko määrittää käyttöoikeuksia, profiileja ja asetuksia ennakoivasti yksittäisille käyttäjille ennen kuin he kirjautuvat sisään?

Kyllä. Tämä voidaan saavuttaa suojausryhmien avulla. Käyttämällä suojausryhmää ympäristölle voit määrittää joukon käyttäjiä, joilla on kyseisen ympäristön käyttöoikeus. Tämä suojausryhmä voi sisältää käyttäjiä, joilla on Business Central -käyttöoikeus, ja käyttäjiä, joilla on Microsoft 365 -käyttöoikeus. Kun päivität käyttäjät seuraavan kerran Microsoft 365:n **Käyttäjät**-luettelosta, järjestelmä luo Microsoft 365 -käyttäjätietueet. Sen jälkeen voit määrittää käyttäjäryhmiä, käyttöoikeuksia, profiileja ja muita asetuksia ennen kuin he kirjautuvat sisään.

### <a name="after-a-user-signs-in-can-i-change-which-objects-they-have-access-to" />Kun käyttäjä on kirjautunut sisään, voinko muuttaa objekteja, joiden käyttöoikeus hänellä on?

Kyllä. Kun käyttäjät ovat kirjautuneet sisään ensimmäisen kerran ja heidän käyttäjätietueensa on valmisteltu, järjestelmänvalvojat hallitsevat näitä käyttäjiä samalla tavalla kuin muita Business Central -käyttäjiä. He voivat esimerkiksi lisätä tai poistaa eri objektien käyttöoikeuksia. Jos muutat Microsoft 365 -käyttöoikeuteen lisättyjä käyttöoikeuksien joukkoa Käyttöoikeuden konfiguraatio -sivulta, muutos vaikuttaa vain seuraaviin käyttäjiin, jotka kirjautuvat sisään ensimmäisen kerran.

### <a name="how-do-i-prevent-access-to-sensitive-tables" />Miten estän pääsyn luottamuksellisiin taulukoihin?

Business Central tarjoaa tehokkaan ja joustavan käyttöoikeusmallin. Sen avulla järjestelmänvalvojat voivat määrittää käyttöoikeuksien joukkoja, jotka myöntävät pääsyn tiettyihin objekteihin, liiketoimintaprosesseihin tai kokonaisiin rooleihin. Voit estää luottamuksellisten taulukoiden käytön luomalla mukautettuja käyttöoikeuksien joukkoja, jotka eivät sisällä luottamuksellisten objektien käyttöoikeuksia. Lisätietoja käyttöoikeuksien sulkemisesta pois on kohdassa [Käyttöoikeuksien joukon luominen](ui-define-granular-permissions.md).  

### <a name="instead-of-customizing-the-license-configuration-can-i-customize-a-user-group" />Voinko mukauttaa käyttäjäryhmää käyttöoikeuden määrityksen mukauttamisen sijaan?

Kyllä. Käyttöoikeuksien joukkojen lisääminen Microsoft Teamsin sisäiset käyttäjät -käyttäjäryhmään Business Centralissa on sama nettovaikutus kuin käyttöoikeuksien joukkojen lisäämisellä Microsoft 365 -käyttöoikeuteen, kunhan Microsoft 365 -käyttöoikeus on edelleen määritetty tälle käyttäjäryhmälle. Tällä lähestymistavalla on se lisäetu, että käyttöoikeuksien joukot synkronoidaan ryhmän jäsenten välillä aina, kun muokkaat käyttäjäryhmää.

### <a name="when-a-business-central-user-shares-a-record-in-teams-do-they-grant-new-permissions" />Kun Business Central -käyttäjä jakaa tietueiden Teamsissa, myöntääkö hän uusia käyttöoikeuksia?

Nro Tämä toiminto ei ole sama asia kuin linkin jakaminen SharePoint -asiakirjaan, jolloin asiakirjan jakava henkilö voi halutessaan myöntää käyttöoikeuden muille käyttäjille. Vain järjestelmänvalvojat voivat määrittää ja kohdistaa käyttöoikeuksia Business Centralissa. Verrattaessa SharePoint-asiakirjojen jakamiseen, se vastaa ”Jaa henkilöille, joilla on olemassa oleva käyttöoikeus” -vaihtoehdon valitsemista.

### <a name="does-this-feature-support-row-level-security" />Tukeeko tämä ominaisuus rivitason suojausta?

Kyllä. Vaikka henkilöllä, joka käyttää tietuetta Teamsissa Microsoft 365 -käyttöoikeudella, voi olla oikeat taulukko- ja sivuobjektien käyttöoikeudet, rivitason käyttöoikeudet ovat voimassa, jos ne on otettu käyttöön kyseiselle taulukolle.  

### <a name="if-i-configure-permissions-that-include-write-access-will-users-be-able-to-write-in-teams" />Jos määritän kirjoitusoikeuksia sisältäviä käyttöoikeuksia, voivatko käyttäjät kirjoittaa Teamsissa?

Jos määrität Business Centralin kohdistamaan käyttöoikeuksien joukon, joka sisältää yhden tai useamman objektin lisäys-, muokkaus- tai poisto-oikeuden, käyttäjät, joilla on kyseinen käyttöoikeuksien joukko, eivät vieläkään voi kirjoittaa Teamsissa, jos heillä on vain Microsoft 365 -käyttöoikeus. Business Central -palvelu noudattaa Vain luku -oikeuksia riippumatta määrittämistäsi lisäys-, muokkaus- tai poisto-oikeuksista.  

Vaikka Business Central tarjoaa tämän suojaustason, suosittelemme silti, että vältät käyttämästä kirjoitusoikeuksia sisältäviä käyttöoikeuksien joukkoja. Näin vältyt ongelmilta myöhemmin, kun käyttäjät muuttavat roolia tai saavat uusia käyttöoikeuksia.  

## [Määritys ja konfigurointi](#tab/setup)

### <a name="why-is-the-setting-to-enable-access-not-available-for-my-environment" />Miksi asetus, joka ottaa käyttöoikeuden käyttöön, ei ole käytettävissä ympäristössäni?

Käytön salliminen Microsoft 365 -käyttöoikeuksilla on saatavilla vain Business Central -ympäristöille, joiden sovellusalustan versio on 21.1 tai sitä uudempi. Kun ympäristösi päivitetään tähän vähimmäisversioon, asetus tulee automaattisesti saataville. Voit tarkistaa ympäristösi version sen lisätietosivulta Business Central -hallintakeskuksesta. Voit myös kirjautua ympäristöön ja siirtyä **Ohje ja tuki** -sivulle **Ohje**-valikosta.

### <a name="can-i-access-business-central-on-premises-with-microsoft--licenses" />Voinko käyttää Business Central on-premises -versiota Microsoft 365 -käyttöoikeuksilla?

Ei, sitä ei tueta. Business Central näyttää virheen, kun käyttäjät yrittävät käyttää Business Central on-premises -tietueita Teamsissa.

### <a name="what-is-the-employee-profile" />Mikä on Työntekijä-profiili?

**Profiilit (roolit)** -luettelosivulla näytetty **Työntekijä**-profiili otettiin käyttöön päivityksessä 21.1. Se on oletusarvoinen profiili, joka kohdistetaan käyttäjille, jotka käyttävät Business Centralia Microsoft 365 -käyttöoikeudellaan. Tämä profiili on tarkoitettu organisaation henkilöille, joilla ei ole erityistä roolia Business Centralissa ja joiden tarvitsee nähdä vain heille jaetut tiedot.

### <a name="what-is-the-teams-users-user-group" />Mikä on Teams-käyttäjät-käyttäjäryhmä?

**Käyttäjäryhmät** -sivulla näytetty **Microsoft Teamsin sisäiset käyttäjät** -käyttäjäryhmä otettiin käyttöön päivityksessä 21.1. Tämä ryhmä on oletusarvoinen käyttäjäryhmä, joka kohdistetaan käyttäjille, jotka käyttävät Business Centralia Microsoft 365 -käyttöoikeudellaan. Käyttäjäryhmä on tarkoitettu henkilöille, jotka kuuluvat Business Centralin isäntäorganisaatioon ja jotka tekevät yhteistyötä Microsoft Teamsissa.  

### <a name="do-users-that-only-have-a-microsoft--license-show-up-in-the-users-list-in-business-central" />Näytetäänkö Business Centralin Käyttäjät-luettelossa käyttäjät, joilla on vain Microsoft 365 -käyttöoikeus?

Kyllä. Jos käytät ympäristöille suojausryhmiä, kyseiset käyttäjät näytetään Käyttäjät-luettelossa, kun suoritat Päivitä käyttäjät Microsoft 365:stä -toiminnon **Käyttäjät**-luettelosta. Jos et käytä suojausryhmiä, käyttäjätietueet näytetään Käyttäjät-luettelossa, kun käyttäjät käyttävät Business Central -tietuetta ensimmäisen kerran.

### <a name="does-this-feature-work-for-embed-isv-solutions" />Toimiiko tämä ominaisuus upotettujen ISV-ratkaisujen kanssa?

Kyllä. Käyttäjät, joilla on vain Microsoft 365 -käyttöoikeus, voivat käyttää tietueita myös *.bc.dynamics.com-toimialueessa toimivissa ympäristöissä.

## [Käyttöoikeudet](#tab/license)

### <a name="can-a-customer-use-this-feature-if-they-dont-have-business-central" />Voiko asiakas käyttää tätä ominaisuutta ilman Business Centralia?

Business Centralin käyttäminen Microsoft 365 -käyttöoikeudella on tarkoitettu organisaatioille, joilla on jo Business Central -tilaus ja jotka käyttävät yhtä tai useampaa Business Central -ympäristöä, joissa on lisensoituja Business Central -käyttäjiä. Se ei tarjoa uusia ominaisuuksia tai käyttöoikeuksia Microsoft 365 -asiakkaille, joilla ei ole Business Central -suunnitelmaa.

### <a name="how-does-this-help-me-manage-subscription-costs-in-my-organization" />Miten tämä auttaa minua hallitsemaan organisaationi tilausten kustannuksia?

PK-yritykset ostavat Dynamics 365 Business Centralin usein yhdessä Microsoft 365:n kanssa tuottavuuden maksimoimiseksi ja toiminnan virtaviivaistamiseksi. Tämä tarkoittaa, että useimmat ihmiset saavat Microsoft 365 -käyttöoikeuden, mutta vain tietyt roolit tai henkilöt saavat Business Central -käyttöoikeuden. Business Central tarjoaa joustavan lisensointitavan, jotta asiakkaat maksavat vain siitä, mitä he tarvitsevat:

- Käyttäjille, jotka tarvitsevat Business Centralin täydet käyttöoikeudet, kohdistetaan usein Business Central Essentials- tai Business Central Premium -käyttöoikeus. 
- Käyttäjille, jotka tarvitsevat rajoitetut kirjoitusoikeudet, kohdistetaan tavallisesti Business Central Team Member -käyttöoikeus.
- Kaikki muut organisaation työntekijät, joiden tarvitsee lukea vain satunnaisesti heille jaettuja liiketoimintatietoja, tarvitsevat vain Microsoft 365 -käyttöoikeuden. Heille ei tarvitse kohdistaa Team Member -käyttöoikeutta. Muita lisensointivaihtoehtoja on saatavilla. Lataa ja lue [Dynamics 365 -käyttöoikeusopas](https://go.microsoft.com/fwlink/?LinkId=866544) saadaksesi lisätietoja.

### <a name="is-this--free-of-charge" />Onko se täysin ilmainen?
 
Nro Business Central -tietojen käyttäminen Microsoft Teamsissa edellyttää, että jokaisella käyttäjällä on joko Business Central -käyttöoikeus tai tuettujen suunnitelmien luettelossa mainittu Microsoft 365 -käyttöoikeus.

### <a name="does-this-work-with-microsoft--trials-and-business-central-trials" />Toimiiko tämä Microsoft 365- ja Business Central -kokeiluversioissa?

Kyllä. Jos käyttäjälle on kohdistettu tuetun suunnitelman kokeiluversion Microsoft 365 -käyttöoikeus, hän voi käyttää myös Business Central -tietueita Teamsissa. Näin asiakkaat voivat kokeilla Microsoftin tuottavuus- ja yrityssovelluksia yhdessä ja kumppanien myyjät ja konsultit voivat helposti esitellä tätä ominaisuutta helposti. Kumppanit voivat esimerkiksi tarjota osoitteesta [https://aka.ms/CDX](https://aka.ms/CDX) omia Azure AD -vuokralaisiaan, jotka sisältävät Microsoft 365- ja Business Central -kokeiluversioita, esitelläkseen Business Centralia.

### <a name="the-list-of-licenses-in-business-central-shows-a-microsoft--license-whats-that" />Business Centralin käyttöoikeuksien luettelossa näkyy Microsoft 365 -käyttöoikeus. Mikä se on?

Business Centralin **Käyttöoikeuden konfiguraatio** -sivulla näytetään erityyppisiä käyttöoikeuksia, jotka voivat tarjota pääsyn Business Central -palveluun. Microsoft lisäsi Microsoft 365:n tähän luetteloon versiossa 21 tarjotakseen uuden tavan käyttää Business Centralia. Tämä käyttöoikeuksien luettelo ei tarkoita sitä, että organisaatiosi olisi ostanut tilauksia mihinkään näistä käyttöoikeuksista tai että organisaatiosi olisi sallinut käytön kyseisten käyttöoikeuksien kautta.

### <a name="do-i-need-to-acquire-a-new-type-of-microsoft--license-for-this-feature-to-work" />Täytyykö minun hankkia uudentyyppinen Microsoft 365 -käyttöoikeus, jotta tämä ominaisuus toimisi?

Microsoft ei ole luonut tälle ominaisuudelle uusia käyttöoikeuksia tai uusia suunnitelmia. Tämä ominaisuus perustuu täysin olemassa oleviin Microsoft 365 -suunnitelmiin ja -käyttöoikeuksiin. Jos olet jo tilannut jonkin tuetuista Microsoft 365 -suunnitelmista, sinulla on jo tämä uusi käyttöoikeus. Muussa tapauksessa, jos et tilaa Microsoft 365:ää tänään, voit rekisteröidä Microsoft 365 Business Premium -suunnitelman tai sitä vastaavia suunnitelmia täältä. 

### <a name="how-do-i-find-out-which-users-have-only-a-microsoft--license" />Miten saan selville, kenellä käyttäjistä on vain Microsoft 365 -käyttöoikeus?

Tähän on monia tapoja. Siirry Microsoft 365 -hallintakeskuksen **Aktiiviset käyttäjät** -luetteloon ja tarkasta **Käyttöoikeudet**-sarake. Siirry Business Centralin **Käyttäjät**-luetteloon, valitse käyttäjä ja tarkasta **Käyttöoikeudet**-tietoruutu.  

### <a name="how-do-i-filter-the-users-list-in-business-central-to-see-users-that-only-have-a-microsoft--license" />Miten suodatan Business Centralin Käyttäjät-luetteloa nähdäkseni käyttäjät, joilla on vain Microsoft 365 -käyttöoikeus?

Tämä ei ole tällä hetkellä mahdollista käyttämällä suodatinta tai luettelonäkymää. Voit kuitenkin valita luettelosta käyttäjän ja tarkastaa tietoruudun, joka sisältää vain Microsoft 365:n, jos käyttäjällä on vain Microsoft 365 -käyttöoikeus.

### <a name="what-about-users-that-have-both-a-microsoft--license-and-a-business-central-license" />Entä käyttäjät, joilla on sekä Microsoft 365- että Business Central -käyttöoikeus?

Kun käyttäjälle on kohdistettu useita käyttöoikeuksia, laajemmat käyttöoikeudet ovat etusijalla rajoitetumpiin käyttöoikeuksiin nähden Business Centralia käytettäessä. Tällöin Business Central -käyttöoikeus myöntää käyttäjälle enemmän käyttöoikeuksia. Käyttäjät voivat siis lukea ja kirjoittaa Business Central -tietueita Teamsissa ja käyttää Business Central -verkkosovellusta selaimessa muiden Business Central -käyttöoikeuden haltijoiden tavoin. Jos Microsoft 365 -käyttöoikeudelle on määritetty erityisiä käyttöoikeuksien joukkoja, käyttäjä saa määritetyt käyttöoikeuksien joukot yhdistettynä käyttöoikeuksien joukkoihin, jotka on saatu Business Central -käyttöoikeudesta tai jotka on jo kohdistettu käyttäjälle.

### <a name="is-this-licensing-related-to-the-business-central-team-member-license" />Liittyykö tämän käyttöoikeus Business Central Team Member -käyttöoikeuteen?

Business Central Team Member -käyttöoikeudet eivät liity millään tavalla Business Centralin käyttämiseen Microsoft Teamsissa Microsoft 365 -käyttöoikeuksilla. Vaikka Microsoft Teamsissa ja sen dokumentaatiossa tiimiin kuuluvia ihmisiä kutsutaan *tiimin jäseniksi*, se on kollektiivinen nimitys Microsoft Teams -käyttäjien ryhmälle. Se ei viittaa Business Central -käyttöoikeuksiin.

### <a name="does-business-central-enforce-any-of-the-constraints" />Onko Business Centralissa voimassa rajoituksia?

Kyllä, Business Central -alusta noudattaa kaikki alustan rajoituksia ja vähimmäisvaatimuksia, mukaan lukien käyttöoikeusvaatimukset. Tämä opastaa virheviestejä näkeviä käyttäjiä suorittamaan vianmäärityksen kokoonpanolleen ja estää väärinkäyttöä. Jos esimerkiksi käyttäjä, jolla on vain Microsoft 365 -käyttöoikeus, yrittää käyttää Business Central -verkkosovellusta selaimessa, hänen pääsynsä estetään ja hänelle näytetään virheviesti. 

## [Käyttö](#tab/usage)
 
### <a name="can-i-access-records-on-teams-for-ios-and-teams-for-android" />Voinko käyttää tietueita Teamsin iOS- ja Android-sovelluksissa?

Tällä hetkellä Business Central -tietoja ei voi käyttää Teams-mobiilisovelluksessa pelkällä Microsoft 365 -käyttöoikeudella. Microsoft pyrkii mahdollistamaan tämän lähiaikoina. 

### <a name="how-do-users-change-their-personal-settings-in-my-settings" />Miten käyttäjät muuttavat henkilökohtaisia asetuksiaan Omat asetukset -sivulta?

Kun käyttäjä käyttää Business Centralia ensimmäistä kertaa pelkällä Microsoft 365 -käyttöoikeudella, hänen käyttäjäasetuksensa, kuten kieli, aikavyöhyke ja aluekohtaiset asetukset, määritetään automaattisesti hänen käyttöjärjestelmänsä tai selaimensa asetusten perusteella. Järjestelmänvalvojat voivat muokata näitä asetuksia jokaisen käyttäjän osalta Business Centralista. 

### <a name="what-determines-the-choice-of-language-when-you-sign-in-for-the-first-time" />Miten valittu kieli määritetään, kun kirjaudut sisään ensimmäisen kerran?

Business Centralissa näkemäsi kieli riippuu useista eri tekijöistä, mukaan lukien Teams-sovellus, jolla käytit Business Centralia ensimmäistä kertaa. Teams-työpöytäsovelluksessa ja Teamsin iOS- ja Android-sovelluksissa käytetään käyttöjärjestelmän kieltä. Teams-verkkosovelluksessa käytetään selaimen kieltä. Teams-kieltä ei oteta huomioon missään tilanteessa. 

### <a name="why-cant-i-activate-some-of-the-colored-links-in-tabs-and-card-details" />Miksi en voi aktivoida joitakin väritettyjä linkkejä välilehdissä ja kortin tiedoissa?

Business Central -sivujen toimintolinkit näytetään usein lihavoituina hyperlinkkeinä, joiden aktivointi siirtää käyttäjän muualle tai suorittaa jonkin toiminnon. Teknisellä tasolla nämä linkit on toteutettu tavallisesti ilman otsikkoa kenttäarvoina, jotka käynnistävät jonkin koodin ja jossa valittu tyyli kuvastaa usein tilaa. Kun käyttäjät käyttävät Business Central -sivuja Microsoft 365 -käyttöoikeudellaan, linkit on muotoiltu ikään kuin ne olisivat interaktiivisia. Niitä ei voi kuitenkaan aktivoida, koska tämä käyttöoikeus ei tarjoa oikeutta suorittaa toimintoja.  

### <a name="why-cant-i-activate-page-notification-actions" />Miksi en voi aktivoida sivun ilmoitustoimintoja?

Sivuilla näytetyissä tilannekohtaisissa ilmoituksissa on usein toimintolinkkejä. Kun käyttäjät käyttävät Business Central -sivuja Microsoft 365 -käyttöoikeudellaan, nämä linkit näytetään, mutta niitä ei voi aktivoida, koska tämä käyttöoikeus ei tarjoa oikeutta suorittaa toimintoja. Teknisellä tasolla nämä linkit on toteutettu toimintoina.

### <a name="can-microsoft--users-remove-tabs" />Voivatko Microsoft 365 -käyttäjät poistaa välilehtiä?

Kyllä. Kuka tahansa keskustelussa tai kanavassa voi poistaa toisten luomia välilehtiä. Välilehden poistaminen ei poista Business Central -tietoja tai vaikuta niihin, mutta välilehti poistetaan kaikilta keskustelun tai kanavan käyttäjiltä.

### <a name="if-i-cant-filter-will-i-still-see-a-filtered-list-that-was-created-by-others" />Jos en voi suodattaa, näenkö silti muiden luoman suodatetun luettelon?

Business Centralia Microsoft 365 -käyttöoikeudella käyttävillä käyttäjillä ei ole oikeutta suodattaa käyttämällä suodatinruutua tai käyttää luettelonäkymiä. Jos toinen käyttäjä on kuitenkin luonut suodatetun luettelosivun sisältävän välilehden, myös Microsoft 365 -käyttäjät näkevät välilehdelle lisätyt suodattimet.

---

## <a name="see-also" />Katso myös

[Yleiskatsaus Business Centralin käyttämisestä Microsoft 365 -käyttöoikeuksilla](admin-access-with-m365-license.md#minimum-requirements)  
[Käytön määrittäminen Microsoft 365 -käyttöoikeuksien avulla](admin-access-with-m365-license-setup.md)  
