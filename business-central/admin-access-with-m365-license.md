---
title: Business Centralin käyttäminen Microsoft 365 -käyttöoikeuksilla
description: Tutustu siihen, miten käyttäjät voivat käyttää Business Central -tietoja, esimerkiksi Microsoft Teams -keskusteluissa ja -kanavissa, vain Microsoft 365 -käyttöoikeudella, mutta ilman Business Central -käyttöoikeutta.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.date: 11/22/2022
ms.custom: bap-template
ms.search.keywords: License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams
ms.openlocfilehash: 8fcef5dca8698d0241e5fc6d37574b3c80b833da
ms.sourcegitcommit: 61f22aeede684f0ae772353ede6530ff03ff2f90
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/24/2022
ms.locfileid: "9804443"
---
# <a name="business-central-access-with-microsoft-365-licenses"></a>Business Centralin käyttäminen Microsoft 365 -käyttöoikeuksilla

Business Central -käyttäjille annetaan Dynamics 365 Business Central -käyttöoikeus, jonka avulla he voivat tarkastella, muokata ja käsitellä liiketoimintatietojaan mistä tahansa käyttöliittymästä. Kaikille muille organisaation työntekijöille, joiden tarvitsee tarkastella tietoja vain ajoittain, Business Central tarjoaa käyttöoikeuden Microsoft 365:n kautta.  

Kun organisaatiossa on sekä Dynamics 365 Business Central- että Microsoft 365 -tilaus, järjestelmänvalvojat voivat määrittää ympäristöt, jotka mahdollistavat Microsoft 365 -käyttöoikeuksien käyttämisen, ja valita, mitä taulukoita ja muita objekteja tämä käyttäjäryhmä voi käyttää. Konfiguroitaessa työntekijät, joilla on Microsoft 365 -käyttöoikeus mutta ei Business Central -käyttöoikeutta, voivat tarkastella heille jaettuja Business Central -tietueita Microsoft Teams -keskustelussa ja -kanavissa.

## <a name="why-enable-access-with-microsoft-365-licenses"></a>Miksi Microsoft 365 -käyttöoikeuksien käyttäminen tulisi ottaa käyttöön  

- Salli kaikille organisaatioon kuuluville työntekijöille käyttöoikeus päätietoihin.

- Valtuuta osastot, jotka eivät suorita Business Centralin toimintoja omatoimisesti, avaamalla heidän tehtäviensä suorittamiseen tarvittavia avaintietoja, poistamalla tarpeen jatkuvasti pyytää tietoja muilta. 

- Tehosta yhteistyön tehoa niin, että osastojen väliset tehtävät ja projektit ovat valmiita ajallaan, poistamalla käyttöoikeuksien vuoksi käyttö estetty -virheistä johtuvan kitkan. 

- Paranna tiimin suorituskykyä niin, että käyttäjät voivat tehdä tietoon perustuvia päätöksiä, jotka ovat kaikkien ryhmän jäsenten tekemiä, vaikka he eivät työskentelisi Business Centralissa. 

- Saavuta lisensointibudjettitavoitteet myöntämällä lisenssit, jotka vastaavat asteittain työntekijöiden tarpeita, Microsoft 365 -lisenssillä vain luku -käyttöoikeuksia varten, Dynamics 365 Business Central Team Member -lisenssillä rajoitettua kirjoitusoikeutta varten ja Dynamics 365 Business Central Essentialsilla tai Premiumilla täydet kirjoitusoikeudet.

- Paranna tietoturvaa vähentämällä tarvetta liittää yritystietojen näyttökatkelmia tietohallinnon rajojen ulkopuolelle.

## <a name="use-rights"></a>Käyttöoikeudet

Kun henkilö käyttää Business Centralia Microsoft 365 -käyttöoikeudella, tämä käyttöoikeus oikeuttaa käyttäjän lukemaan (mutta ei kirjoittamaan) Business Central -tietoja yksinkertaistetun Microsoft Teams -käyttöliittymän kautta. Tässä osassa selitetään nämä käyttöoikeudet ja rajoitukset, joiden avulla voit suunnitella tämän ominaisuuden määrittämisen ja käytön. Lisätietoja tästä käyttöoikeustyypistä muihin Business Central -käyttöoikeuksiin verrattuna on [Dynamics 365 -käyttöoikeusoppaassa](https://go.microsoft.com/fwlink/?LinkId=866544).
 
### <a name="client-access"></a>Asiakasohjelman käyttöoikeus

Käyttäjillä on oikeus käyttää Business Central -tietoja Microsoft Teamsissa. Seuraavassa taulukossa on yhteenveto siitä, mitkä Business Central -palvelun käyttämisen eri tavoista sallitaan tämän käyttöoikeuden yhteydessä. 

|Business Central -palvelua käyttävät asiakasohjelmat |Käyttöoikeus|
|-|-|
|Business Central -sovellus Microsoft Teamsille|![Kyllä](media/check.png)|
|Business Central -verkkoasiakas |![Ei](media/x-icon.png ) |
|Business Central -mobiilisovellukset|![Ei](media/x-icon.png )|
|Business Central -ohjelmointirajapinnat|![Ei](media/x-icon.png )|
|Business Centralin integrointi muihin Office-sovelluksiin|![Ei](media/x-icon.png )|
|Business Central upotettu muihin sovelluksiin |![Ei](media/x-icon.png )|

### <a name="data-access"></a>Pääsy tietoihin 

Käyttäjillä on oikeus lukea taulukon tietoja, mutta he eivät voi muokata, luoda tai poistaa tietueita. Business Central -ympäristö estää automaattisesti kirjoittamisen mihinkään tietotaulukoihin.  

### <a name="use-of-objects"></a>Objektien käyttö 

Microsoft 365 -käyttöoikeuksien käyttäminen ei rajoita sitä, mitä Business Centralin objekteja tai objektialueita voi käyttää. Käyttäjillä on oikeus käyttää Microsoftin perussovellusta ja kaikkia laajennuksia, kuten mukautuksia ja lisäsovelluksia. 

## <a name="simplified-ui"></a>Simplified UI 

Käyttäjillä on oikeus vähennettyyn määrään Business Centralin Microsoft Teams -käyttöön tarkoitettuja ominaisuuksia ja toimintoja. Alla olevissa taulukoissa on huomionarvoisia piirteitä. Luettelo ei ole tyhjentävä, ja se voi muuttua.

Business Central-sovellus Teamsille ominaisuudet:

|Ominaisuus  |Saatavilla|
|-|-|
|Tarkastele Business Central -kortteja|![Kyllä](media/check.png)|
|Näytä kortin tiedot |![Kyllä](media/check.png) |
|Kortin tietojen kiinnittäminen välilehteen |![Kyllä](media/check.png)|
|Tarkastele Business Central -välilehtiä|![Kyllä](media/check.png)|
|Business Central -välilehden lisääminen|![Nro_](media/x-icon.png )|
|Hae työyhteyshenkilöitä |![Ei](media/x-icon.png )|
|Liitä ja jaa linkin esiversio korttina|![Ei](media/x-icon.png )|

Business Central -asiakkaan tehtävät, jotka on upotettu Teamsiin:

|Toiminto |Saatavilla|Esimerkkifunktiot|
|-|-|-|
|Tietojenkäsittelyjärjestelmän toiminnot |![Ei](media/x-icon.png )|Muokkaus, Luonti, Poisto|
|Luetteloiden perusfunktiot|![Kyllä](media/check.png)|Etsi, lajittele, muuta asettelua|
|Luetteloiden lisäfunktiot|![Ei](media/x-icon.png )|Suodatinruutu, näkymät|
|Poraudu alaspäin luettelosta korttiin |![Kyllä](media/check.png)||
|Liittyvien taulukoiden tietojen käyttäminen|![Ei](media/x-icon.png )|Tietoruutu, kenttien siirtyminen, kurkistus, haku |
|Tapahtumat|![Ei](media/x-icon.png )|Toimintopalkki, toimintovalikot, sivun ilmoitustoiminnot|
|Järjestelmänlaajuiset pikakuvakkeet|![Ei](media/x-icon.png )|Omat asetukset, roolinhallinta, kerro-haku  |
|Kopioi|![Kyllä](media/check.png)|Kopioi rivit, kopioi kentän arvo, kopioi linkki sivuun|
|UI:n mukauttaminen|![Ei](media/x-icon.png )|Mukauta| 
|Sisäänrakennettu räätälöinti|![Kyllä](media/check.png)|Muuta sarakkeen kokoa, Laajenna tai kutista, Näytä lisää |
|Tietojen jakaminen |![Ei](media/x-icon.png )|Avaaminen tai muokkaaminen Excelissä, Jaa Teamsiin|
|Sisäinen käyttäjäapu|![Kyllä](media/check.png) |Työkaluvihjeet, linkit asiakirjoihin|
|Käyttäjäavun parannus |![Ei](media/x-icon.png )|Sivu- ja kenttäopetuksen vihjeet, ohje-ruutu|

## <a name="minimum-requirements"></a>Vähimmäisvaatimukset

Tässä osassa kuvataan vähimmäisvaatimukset, jotka organisaation on täytettävä, jotta Microsoft 365 -käyttöoikeudet voidaan sallia ja yksittäisten Microsoft Teams -käyttäjät voivat käyttää Business Central -tietoja ilman Business Central -lisenssiä.

### <a name="requirements-to-enable-access"></a>Käyttöoikeuden käytön vaatimukset

- Business Central online (SaaS).

- Ympäristöjen on oltava alustaversiolla 21.1 tai uudempi.

### <a name="requirements-for-individual-users-to-access-data-in-teams"></a>Teamsin tietojen käyttöä koskevat vaatimukset yksittäisille käyttäjille

- Tietoja on käytettävä Teamsin Business Central -sovelluksen avulla. Käyttäjillä on oltava Business Central -sovellus Teamsille asennettuna, ja niiden on käytettävä jotakin tuetuista Teams-asiakkaista. Luettelo Business Centralin tuetuista Teams-asiakkaista on kohdassa [Business Centralin käyttämisen vähimmäisvaatimukset](product-requirements.md#teams).

- Käyttäjien on oltava organisaation sisäisiä, mikä tarkoittaa sitä, että käyttäjätunnus on peräisin samasta kotivuokraajasta, jossa on käytössä Business Central. Ulkoisia henkilöllisyyksiä ei tueta. Business Central estää automaattisesti vieraiden pääsyn.

- Käyttäjille on määritettävä Microsoft 365 -käyttöoikeus jostakin seuraavista suunnitelmista.
  
  |Tuettu suunnitelma|Tuotteen tunnus |
  |-|-|
  |Microsoft 365 Business Basic|3b555118-da6a-4418-894f-7df1e2096870|
  |Microsoft 365 Business Standard|f245ecc8-75af-4f8e-b61f-27d8114de5f3|
  |Microsoft 365 Business Premium |cbdc14ab-d96c-4c30-b9f4-6ada7cdc1d46|
  |Microsoft 365 E3 |05e9a617-0261-4cee-bb44-138d3ef5d965 |
  |Microsoft 365 E5|06ebc4ee-1bb5-47dd-8120-11324bc54e06|
  |Microsoft 365 F1|50f60901-3181-4b75-8a2c-4c8e4c1d5a72|
  |Microsoft 365 F3|66b55226-6b4f-492c-910c-a3b7a3c9d993|
  |Office 365 E1|18181a46-0d4e-45cd-891e-60aabd171b4e|
  |Office 365 E2 |6634e0ce-1a9f-428c-a498-f84ec7b8aa2e|
  |Office 365 E3|6fd2c87f-b296-42f0-b197-1e91e994b900|
  |Office 365 E5|c7df2760-2c81-4ef7-b578-5b5392b571df|
  |Office 365 F2|131fd665-5752-4995-a628-bcba5c889745|
  |Office 365 F3|4b585984-651b-448a-9e53-3b10f069cf7f|
  |Microsoft Teams Essentials ( Azure AD -identiteetti) |3ab6abff-666f-4424-bfb7-f0bc274ec7bc|
  
  Myös useimpia näihin suunnitelmiin perustuvia tarjouksia tuetaan. Jos tilaat esimerkiksi Microsoft 365 Business Premium (Nonprofit Staff Pricing) -suunnitelman, se on ainoastaan hyväntekeväisyysjärjestöjä koskeva tarjous Microsoft 365 Business Premium -suunnitelman perusteella, eli sitä tuetaan.

  > [!NOTE]
  > Etkö löydä suunnitelmaasi luettelosta? Microsoft hakee jatkuvasti palautetta siitä, miten voimme parantaa palvelujamme ja laajentaa tarjontaamme, jotta yhä useammat asiakkaat voivat hyödyntää tätä ominaisuutta. Jaa ideasi siitä, mitä suunnitelmia meidän pitäisi tukea seuraavaksi kohdassa [https://aka.ms/bcIdeas](https://aka.ms/bcIdeas).

- Käyttäjille on määritettävä Microsoft 365 -käyttöoikeus, jonka Microsoft Teams -sovellus on ottanut käyttöön kyseisen lisenssin sovellusluettelossa. 

  |Tuetut sovellukset|Palvelusuunnitelman tunnus|
  |-|-|
  |Microsoft Teams|57ff2da0-773e-42df-b2af-ffb7a2317929 |

- Organisaatiossa on oltava vähintään toinen käyttäjä, jolle on määritetty Dynamics 365 Business Central -käyttöoikeus.

## <a name="next-steps"></a>Seuraavat vaiheet

- Saat käsityksen käyttäjän käyttötyönkulusta, jotta voit suunnitella Business Centralin lähestymistavan ja konfiguroinnin vastaamaan yrityksen tarpeita. Katso [Käyttöoikeustyönkulku](admin-access-with-m365-license-flow.md).
- Määritä Microsoft 365 -käyttöoikeutesi ympäristöön ja käyttäjiin. Katso [Käytön määrittäminen Microsoft 365 -käyttöoikeuksien avulla ](admin-access-with-m365-license-setup.md).

## <a name="see-also"></a>Katso myös

[Business Centralin ja Microsoft Teamsin integraatio](across-teams-overview.md)  
