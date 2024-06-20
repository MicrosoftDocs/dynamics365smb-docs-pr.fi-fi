---
title: Tietojen jakaminen
description: Tutustu eri tapoihin jakaa yritystietoja Business Centralista.
author: jswymer
ms.topic: conceptual
ms.search.keywords: null
ms.date: 09/21/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Yritystietojen jakaminen Business Centralista

Organisaation sisä- ja ulkopuolisten henkilöiden välinen yhteistyö on osa useimpia yrityksiä. [!INCLUDE[prod_short](includes/prod_short.md)] sisältää useita toimintoja, joiden avulla voit jakaa yritystietoja, kuten tietueluettelon, tietyt tietueet tai asiakirjat. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Kaikkien näiden ominaisuuksien avulla tietojen käyttö on suojattu Business Centralin lisenssillä ja käyttöoikeuksilla.

## Linkin kopioiminen

![Tuettu](media/check.png) Business Central Online ![Tuettu](media/check.png) Business Central On-premises

Millä tahansa sivulla voit kopioida sivun URL-osoitteen, liittää sen ja jakaa sen muihin mediamuotoihin, kuten sähköposteihin, Teams-keskusteluihin tai tekstiviesteihin. Helpoin tapa kopioida linkki on valita **Jaa** > **Kopioi linkki** sivun yläreunasta. Toinen tapa on kopioida URL-osoite suoraan selaimen osoiteruudusta.

Kun liität URL-osoitteen rtf-editoriin, kuten Wordiin, Outlookiin tai Teamsiin, sen sijaan että näyttäisit koko URL-osoitteen, linkille annetaan luettavampi nimi, joka ilmaisee selvästi kohteen kontekstin. Nimi ja kuvio vaihtelevat sen mukaan, mihin sivuun linkität. Esimerkkejä:

|Malli|Sivun esimerkki|Linkin nimi|
|-|-|-|
|Luettelosivut|**Nimikkeet**-luettelosivu | **Nimikkeet**|
|Luettelonäkymä| **Avaa** suodatettu näkymä **Myyntitilaukset**-luettelossa|**Myyntitilaukset - Avoimet**|
| Yksittäinen tietue|Nimikekortti, jossa näkyy yksittäinen tietue|"Nimikekortti - 1896 - ATHENS Desk"|
|Luonnostietueet| Uusi asiakaskortti|**Uusi - asiakaskortti**|
|Merkkiä käyttävä yritys|Merkit sisältävän yrityksen **Nimikkeet**-luettelosivu **CRONUS**| **Nimikkeet (CRONUS)**|

> [!TIP]
> Samanlaista nimeämistapaa käytetään selainvälilehdissä.

### Jaa data-analyysi
Jos tarkastelet sivua tai kyselyä tietojen analysointitilassa, voit jakaa tietyn analyysivälilehden valitsemalla välilehdessä alanuolipään ja valitsemalla sitten **Kopioi linkki**. [Lisätietoja tietojen analysointitilasta](analysis-mode.md). 

### Muokkaa sivun linkkiä

Kun olet kopioinut linkin, ennen sen lähettämistä voit muokata URL-osoitetta niin, että se vaikuttaa siihen, mitä näytetään, kun sivu avataan. Voit esimerkiksi lisätä suodattimia tai määrittää eri yrityksen.

[Lisätietoja verkkoasiakasohjelman URL-osoitteesta](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

### Tietoja suodatetuista luetteloista

Luettelosivujen suodatinruudun avulla voit tarkentaa luettelossa olevia tietueita käyttämällä suodattimia. Jos käytät **Kopioi linkki** -toimintoa tai kopioit URL-osoitteen selaimesta, sivun linkki ei sisällä suodattimen muutoksia. Linkin avaavat käyttäjät näkevät koko kokoelman. Tapa säilyttää suodatus kokoelmasivulla on tallentaa suodatettu sivu **näkymäksi** ensin. Avaa sitten näkymä ja kopioi linkki sieltä.

[Lisätietoja lajittelusta, hausta ja suodattamisesta](ui-enter-criteria-filters.md).

## Jakaminen Teamsiin

![Tuettu](media/check.png) Business Central Online ![Ei tueta](media/x-icon.png) Business Central On-premises

Suoraan useimmista kokoelmasivuista ja tietosivuista voit lähettää linkin sivulle henkilöille, ryhmäkeskusteluille tai kanaville. Voit esimerkiksi jakaa linkin tietueiden suodatettuun näkymään. Jos olet asentanut [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen Teamsiin, linkki laajenee automaattisesti pieneen korttiin, jonka voit sisällyttää viestiin. Vastaanottajat voivat sitten linkkiä tai korttia napsauttamalla avata sivun Business Centralissa.

[Lisätietoja tietueiden ja sivulinkkien jakamisesta Teamsissa](across-working-with-teams.md).

## Jakaminen OneDriven kautta

![Tuettu](media/check.png) Business Central Online ![Tuettu](media/check.png) Business Central On-premises

Business Centralin avulla on helppo tallentaa, hallita ja jakaa tiedostoja muiden ihmisten kanssa OneDrive for Businessin kautta. Useimmilla sivuilla, joilla on saatavilla tiedostoja, kuten raportin Saapuneet-kansio tai tiedostot, jotka on liitetty tietueisiin, löydät **Avaa OneDrivessa**- ja **Jaa**-toiminnon. Kumpikin toiminto tallentaa tiedoston kopion OneDriveen. Kun olet OneDrivessa, voit käyttää tiedoston jakamis- ja osallistumistoimintoja. Toimintojen erona on se, että **Avaa OneDrivessa** avaa tiedoston OneDrivessa. **Jaa** avaa sivun, jossa valitset, kenen kanssa haluat jakaa tiedoston. Vastaanottajat saavat sähköposti-ilmoituksen, jossa he voivat käyttää tiedostoa sinun OneDrivestasi.

[Lisätietoja tiedostojen jakamisesta OneDrivessa](across-share-onedrive.md)

## Avaaminen Excelissä

![Tuettu](media/check.png) Business Central Online ![Tuettu](media/check.png) Business Central On-premises

Voit käyttää **Avaa Excelissä** -toimintoa luettelosivuissa ja luetteloissa, jotka on upotettu sivulle. Tämä toiminto vie tietueluettelon Excel-työkirjaan (.xlsx-tiedostoon), jonka voit jakaa muiden kanssa. Työkirjassa voit käyttää myös Excelin osana olevaa Jaa-toimintoa.

[Lisätietoja tarkastelusta ja muokkaamisesta Excelissä](across-work-with-excel.md).

## Rivien tai taulukoiden jakaminen

![Tuettu](media/check.png) Business Central Online ![Tuettu](media/check.png) Business Central On-premises

Voit jakaa yhden tai useamman tietueen luettelossa. Kopioi leikepöydälle näppäinyhdistelmällä <kbd>Ctrl</kbd>+<kbd>C</kbd>. Liitä sitten kopioitu kohde toiseen sovellukseen näppäinyhdistelmällä <kbd>Ctrl</kbd>+<kbd>V</kbd>. Jos esimerkiksi kopioit kolme myyntitilausta ja liität ne sähköpostiin, tilaukset näytetään kauniisti muotoiltuna taulukkona.

[Lisätietoja kopioimisesta ja liittämisestä usein kysytyissä kysymyksissä](faq-copy-paste.yml).

## Katso myös

[Business Centralin ja OneDriven integraatio](across-onedrive-overview.md)  
[OneDriven ja Business Centralin integroinnin hallinta](admin-onedrive-integration.md)  
[OneDrive – usein kysytyt kysymykset](admin-onedrive-faq.md)
