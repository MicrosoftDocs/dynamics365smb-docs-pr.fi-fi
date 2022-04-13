---
title: Tietojen jakaminen
description: Tutustu eri tapoihin jakaa yritystietoja Business Centralista.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2022
ms.author: jswymer
ms.openlocfilehash: 8fd3d76ed8affd506ad4cd1838a182e595ecb0bf
ms.sourcegitcommit: d6af3155bb818430f22d5caca78df322a8d9b178
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2022
ms.locfileid: "8528503"
---
# <a name="sharing-business-data-from-business-central"></a>Yritystietojen jakaminen Business Centralista

Organisaation sisä- ja ulkopuolisten henkilöiden välinen yhteistyö on osa useimpia yrityksiä. [!INCLUDE[prod_short](includes/prod_short.md)] sisältää useita toimintoja, joiden avulla voit jakaa yritystietoja, kuten tietueluettelon, tietyt tietueet tai asiakirjat. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Kaikkien näiden ominaisuuksien avulla tietojen käyttö on suojattu Business Centralin lisenssillä ja käyttöoikeuksilla.

## <a name="copying-a-link"></a>Linkin kopioiminen

![Tuettu](media/check.png) Business Central Online ![Tuettu](media/check.png) Business Central On-premises

Millä tahansa sivulla voit kopioida sivun URL-osoitteen, liittää sen ja jakaa sen muihin mediamuotoihin, kuten sähköposteihin, Teams-keskusteluihin tai tekstiviesteihin. Helpoin tapa kopioida linkki on valita **Jaa** > **Kopioi linkki** sivun yläreunasta. Toinen tapa on kopioida URL-osoite suoraan selaimen osoiteruudusta.

### <a name="modify-the-page-link"></a>Muokkaa sivun linkkiä

Kun olet kopioinut linkin, ennen sen lähettämistä voit muokata URL-osoitetta niin, että se vaikuttaa siihen, mitä näytetään, kun sivu avataan. Voit esimerkiksi lisätä suodattimia tai määrittää eri yrityksen.

Lisätietoja on kohdassa [Verkkoasiakkaan URL-osoite](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

### <a name="about-filtered-lists"></a>Tietoja suodatetuista luetteloista

Luettelosivujen suodatinruudun avulla voit tarkentaa luettelossa olevia tietueita käyttämällä suodattimia. Jos käytät **Kopioi linkki** -toimintoa tai kopioit URL-osoitteen selaimesta, sivun linkki ei sisällä suodattimen muutoksia. Linkin avaavat käyttäjät näkevät koko kokoelman. Tapa säilyttää suodatus kokoelmasivulla on tallentaa suodatettu sivu **näkymäksi** ensin. Avaa sitten näkymä ja kopioi linkki sieltä.

Lisätietoja on kohdassa [Lajitteleminen, hakeminen ja suodattaminen](ui-enter-criteria-filters.md).

## <a name="sharing-to-teams"></a>Jakaminen Teamsiin

![Tuettu](media/check.png) Business Central Online ![Ei tueta](media/x-icon.png) Business Central On-premises

Suoraan useimmista kokoelmasivuista ja tietosivuista voit lähettää linkin sivulle henkilöille, ryhmäkeskusteluille tai kanaville. Voit esimerkiksi jakaa linkin tietueiden suodatettuun näkymään. Vastaanottajat voivat sitten napsauttamalla linkkiä avata sivun Business Centralissa.

Lisätietoja on kohdassa [Jaa tietueiden ja sivujen linkkejä Teamsissa](across-working-with-teams.md).

## <a name="sharing-through-onedrive"></a>Jakaminen OneDriven kautta

![Tuettu](media/check.png) Business Central Online ![Tuettu](media/check.png) Business Central On-premises

Business Centralin avulla on helppo tallentaa, hallita ja jakaa tiedostoja muiden ihmisten kanssa OneDrive for Businessin kautta. Useimmilla sivuilla, joilla on saatavilla tiedostoja, kuten raportin Saapuneet-kansio tai tiedostot, jotka on liitetty tietueisiin, löydät **Avaa OneDrivessa**- ja **Jaa**-toiminnon. Kumpikin toiminto tallentaa tiedoston kopion OneDriveen. Kun olet OneDrivessa, voit käyttää tiedoston jakamis- ja osallistumistoimintoja. Toimintojen erona on se, että **Avaa OneDrivessa** avaa tiedoston OneDrivessa. **Jaa** avaa sivun, jossa valitset, kenen kanssa haluat jakaa tiedoston. Vastaanottajat saavat sähköposti-ilmoituksen, jossa he voivat käyttää tiedostoa sinun OneDrivestasi.

Lisätietoja on kohdassa [Jaa tietueita OneDrivessa](across-share-onedrive.md).

## <a name="opening-in-excel"></a>Avaaminen Excelissä

![Tuettu](media/check.png) Business Central Online ![Tuettu](media/check.png) Business Central On-premises

Voit käyttää **Avaa Excelissä** -toimintoa luettelosivuissa ja luetteloissa, jotka on upotettu sivulle. Tämä toiminto vie tietueluettelon Excel-työkirjaan (.xlsx-tiedostoon), jonka voit jakaa muiden kanssa. Työkirjassa voit käyttää myös Excelin osana olevaa Jaa-toimintoa.

Lisätietoja on kohdassa [Katsele ja muokkaa Excelissä](across-work-with-excel.md).

## <a name="sharing-rows-or-tables"></a>Rivien tai taulukoiden jakaminen

![Tuettu](media/check.png) Business Central Online ![Tuettu](media/check.png) Business Central On-premises

Voit jakaa yhden tai useamman tietueen luettelossa. Paina vain CTRL + C-pikanäppäintä kopioidaksesi leikepöydälle. Liitä sitten kopioitu kohde toiseen sovellukseen painamalla CTRL + V. Jos esimerkiksi kopioit kolme myyntitilausta ja liität ne sähköpostiin, tilaukset näytetään kauniisti muotoiltuna taulukkona.

Lisätietoja on kohdassa [Kopioinnin ja liittämisen usein kysytyt kysymykset](faq-copy-paste.yml).

## <a name="see-also"></a>Katso myös

[Business Centralin ja OneDriven integraatio](across-onedrive-overview.md)  
[OneDriven ja Business Centralin integroinnin hallinta](admin-onedrive-integration.md)  
[OneDrive – usein kysytyt kysymykset](admin-onedrive-faq.md)