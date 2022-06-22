---
title: Laajennusten asentaminen ja poistaminen
description: Tietoja laajennusten asentamisesta ja asennusten poistamisesta Business Centralissa.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.search.form: 2500
ms.date: 05/24/2022
ms.author: solsen
ms.openlocfilehash: a70ea442ffb9d6e5f131e4d720da57f033474e16
ms.sourcegitcommit: 6eeac924d8e211080316ce5068e3d4fb5a2d5ed9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804654"
---
# <a name="install-and-uninstall-extensions-in-business-central"></a>Laajennusten asentaminen ja asennusten poistaminen Business Centralissa

Voit muuttaa [!INCLUDE[prod_short](includes/prod_short.md)]ia asentamalla laajennuksia, jotka esimerkiksi sisältävät lisätoimintoja, muuttavat toimintaa tai mahdollistavat uusien verkkopalveluiden käyttämisen. Lisätietoja on kohdassa [Business Centralin mukauttaminen laajennusten avulla](ui-extensions.md).

> [!NOTE]
> Jos haluat asentaa AppSourcen laajennuksia tai poistaa niitä tai lisätä vuokraajakohtaisia laajennuksia, sinulla on oltava vaaditut käyttöoikeudet. Sinun täytyy olla jäsen joko EXTEND. MGT. - ADMIN -käyttäjäryhmässä tai sinulla on oltava EXTEND. MGT. - ADMIN -käyttöoikeudet. Jos olet järjestelmänvalvoja, voit määrittää käyttäjäryhmiä ja käyttöoikeuksia yrityksesi muille käyttäjille.
>
> Jos haluat käyttää laajennuksen mahdollistamaa toimintoa, kuten avata sivuja, suorittaa raportteja tai valita toimintoja, sinulla on oltava käyttöoikeuksien joukko, joka on asennettu laajennuksen osana.

> [!NOTE]  
> **EXTEND. MGT. - ADMIN** -käyttöoikeudet otettiin käyttöön Business Central 2021:n julkaisuaallossa 1, ja ne korvasivat aiemmissa versioissa olleet **D365 EXTENSION MGT** -käyttöoikeudet.

## <a name="install-an-extension"></a><a name="install"></a>Laajennuksen asentaminen

Laajennuksia hallitaan **Laajennusten hallinta** -sivulla. Tämä sivu löytyy kotisivulta. Vaihtoehtoisesti valitse **Hae sivua tai raporttia** -kuvake ![Lamppu, joka avaa Kerro-toiminnon.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") oikeassa yläkulmassa, syötä **Laajennus** ja valitse sitten liittyvä linkki.  

Uusia laajennuksia on saatavana kaupasta osoitteessa [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Kaupassa on nähtävänä kaikki [!INCLUDE[prod_short](includes/prod_short.md)]in saatavilla olevat laajennukset, ja voit hankkia sieltä muiden Microsoftin tuotteiden sovelluksia, laajennuksia ja sisältöpaketteja. Määritä soveltuvat suodattimet, tutustu kunkin laajennuksen tietoihin ja hae laajennus [!INCLUDE[prod_short](includes/prod_short.md)]iin.  

> [!NOTE]  
> Kirjaudu sivustoon [AppSource.microsoft.com](https://appsource.microsoft.com/) [!INCLUDE[prod_short](includes/prod_short.md)]issa käyttämäsi sähköpostitilin tiedoilla. Saman sähköpostitilin käyttäminen myös muissa palveluissa ja tuotteissa takaa sujuvan käyttökokemuksen.  

Kauppaan pääsee myös suoraan [!INCLUDE[prod_short](includes/prod_short.md)]ista. Tällä hetkellä asennettuna olevat laajennukset näkyvät **Laajennusten hallinta** -sivulla. Voit avata **Laajennuskauppa**-sivun, jossa näkyvät AppSourcessa tällä hetkellä käytettävissä olevat [!INCLUDE[prod_short](includes/prod_short.md)]in laajennukset. Jos valitset *Lisää sovelluksia* -linkin, sinut siirretään sivustolle [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Kun valitset laajennuksen, voit lukea tietoja laajennuksesta ja hakea lisätietoja käyttämällä laajennuksen Ohje-toimintoa. Kun haluat noutaa laajennuksen, sinun on hyväksyttävä käyttöehdot. Jos noudat laajennuksen AppSource-sivustosta, sinut kirjataan sisään [!INCLUDE[prod_short](includes/prod_short.md)]iin asennuksen viimeistelemiseksi.  

Laajennus on ehkä määritettävä asennuksen yhteydessä. Se tarkoittaa esimerkiksi **[!INCLUDE[prod_short](includes/prod_short.md)]in PayPal Payments Standard** -laajennuksen käyttämisessä tarvittavan tilin määrittämistä.
Muissa laajennuksissa esimerkiksi yksinkertaisesti lisätään kenttiä olemassa olevalle sivulle tai lisätään uusi sivu.

Jos poistat laajennuksen asennuksen ja haluat ottaa sen takaisin käyttöön, voit asentaa laajennuksen uudelleen. Kun poistat käytössäsi olleen laajennuksen asennuksen, tiedot säilytetään. Jos siis asennat laajennuksen uudelleen, tiedot ovat yhä käytettävissäsi. Jotkin laajennukset ovat pakollisia. Näiden laajennusten asennuksen poistaminen **Laajennusten hallinta** -sivulla on estetty. Jos yrität tehdä niin, näyttöön avautuu virhesanoma.

Jotkin ovat Microsoftin laajennuksia, jotkin [muiden yritysten](ui-extensions-other.md). Kaikki laajennukset testataan, ennen kuin ne ovat käyttäjien käytettävissä. Suosittelemme kuitenkin lisätietoihin tutustumista laajennuksen mukana saatavien linkkien avulla ennen laajennuksen asentamista.

Microsoft tarjoaa seuraavat laajennukset:

* [AMC Banking 365 Fundamentals -laajennus](ui-extensions-amc-banking.md)
* [Ceridian Payroll](ui-extensions-ceridian-payroll.md)
* [Yritystoiminto](ui-extensions-company-hub.md)  
* [Dynamics GP -tietojen siirto](ui-extensions-dynamicsgp-data-migration.md)
* [Envestnet Yodlee Bank Feeds](ui-extensions-yodlee-bank-feeds.md)
* [Olennaiset liiketoimintanäkemykset](ui-extensions-essential-business-insights.md)
* [Kuvan analysointitoiminto](ui-extensions-image-analyzer.md)
* [Älykäs pilvi](ui-extensions-data-replication.md)
* [Älykäs Pilvipohja](ui-extensions-intelligent-cloud.md)  
* [Myöhästyneen maksun ennusteet](ui-extensions-late-payment-prediction.md)
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)
* [QuickBooks-tietojen siirto](ui-extensions-quickbooks-data-migration.md)
* [QuickBooks Online -tietojen siirto](ui-extensions-quickbooks-online-data-migration.md)
* [Quickbooks Payroll -tiedostojen tuonti](ui-extensions-quickbooks-payroll.md)
* [Myynti- ja varastoennuste](ui-extensions-sales-forecast.md)
* [Arvonlisäveroryhmä](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [DK – C5-tietojen siirto](ui-extensions-c5-data-migration.md)
* [DK - Maksut ja täsmäytykset](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK – Verotiedostomuodot](ui-extensions-tax-file-formats-dk.md)
* [Ison-Britannian postinumeroiden GetAddress.io-laajennus](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [US/CA/UK/AU/NZ/ZA - Maksusuositusehdotuksen lähettäminen](ui-extensions-send-remittance-advice.md)

## <a name="upload-a-per-tenant-extension-pte"></a>Vuokraajakotaisen laajennuksen (PTE) lataaminen palvelimeen

Lataat PTE:n käyttämällä **Laajennuksen hallinta** -sivua. Valitse **Laajennuksen hallinta** -sivulla **Hallinta** ja valitse sitten **Lataa laajennus palvelimeen**. Valitse **Lataa ja ota käyttöön laajennus** -sivulla ladattava .app-tiedosto. Jatka valitsemalla **Hyväksy**-painike ja sitten **Ota käyttöön**-painike, jolloin PTE-käyttöönottoprosessi aloitetaan.

Jos PTE sisältää rikkovia mallin muutoksia, on mahdollista *pakottaa* sen lataaminen. Voit tehdä sen valitsemalla **Mallin synkronointi tila** -kohdassa **Pakota**-asetuksen. Näyttöön tulee vahvistusikkuna, jonka voi hyväksyä ennen jatkamista.  

## <a name="uninstall-an-extension"></a>Laajennuksen asennuksen poistaminen

Laajennuksen asennus poistetaan **Laajennuksen hallinta** -sivulla. Jos haluat poistaa laajennuksen, valitse se sivulla ja valitse sitten **Poista asennus** -toiminto. Jos poistat laajennuksen asennuksen ja haluat ottaa sen takaisin käyttöön, voit asentaa laajennuksen uudelleen.

Kun poistat käytössäsi olleen laajennuksen asennuksen, tiedot säilytetään oletusarvoisesti mahdollista laajennuksen uudelleenasennusta varten. Voit myös valita tietojen poistamisen laajennuksen kanssa. Tätä toimintoa ohjataan **Poista laajennuksen tiedot** -kytkimellä. Tämä kytkin on oletusarvoisesti **pois päältä**. Kun yrität kytkeä laajennuksen **Poista laajennuksen tiedot** -kytkentä, avautuu vahvistusvalintaikkuna, jossa päälle kytkeminen edellyttää valintaa **Kyllä**. Kun **Poista laajennuksen tiedot** -kytkin on kytketty päälle, voit poistaa laajennuksen asennuksen, jonka yhteydessä sinua pyydetään vahvistamaan uudelleen, että haluat poistaa laajennuksen asennuksen ja poistaa tiedot.

> [!IMPORTANT]  
> - Saattaa olla muita laajennuksia, joiden toimiminen vaatii poistettavan laajennuksen tai on riippuvainen siitä. Näitä muita laajennuksia kutsutaan *riippuvaisiksi*. Et voi poistaa laajennuksen asennusta, ellei myös sen riippuvaisia poisteta.
> - Kun päätät poistaa sellaisen laajennuksen, jolla on vähintään yksi riippuvainen, avautuu vahvistusvalintaruutu, jossa riippuvaiset näkyvät ja sinulta kysytään, haluatko poistaa laajennuksen ja kaikki sen riippuvaiset. Jatkaaksesi sinun on valittava **Kyllä**.
> - Jos kytket **Poista laajennuksen tiedot** -kytkimen päälle, laajennuksen asennuksen poistaminen poistaa kaikki laajennuksen tiedot **sekä** kaikki riippuvaisten laajennusten tiedot. Toimintoa ei voi kumota.
> - Osa laajennuksista on pakollisia. Niiden asennuksen poistaminen **Laajennusten hallinta** -sivulla on estetty. Jos yrität tehdä niin, näyttöön avautuu virhesanoma.  

## <a name="see-also"></a>Katso myös

[Business Centralin mukauttaminen](ui-customizing-overview.md)  
[Muiden toimittajien Business Central -laajennukset](ui-extensions-other.md)  
[Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md)  
[Asiakkaan maksujen ottaminen käyttöön PayPalin kautta](sales-how-enable-payment-service-extensions.md)  
[Liiketoiminnan tietojen siirtäminen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[Muiden palveluntarjoajien [!INCLUDE[prod_short](includes/prod_short.md)]in laajennukset](ui-extensions-other.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]