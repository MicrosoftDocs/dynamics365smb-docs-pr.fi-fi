---
title: Business Central -sovelluksen mukauttaminen asentamalla laajennuksia
description: Lisätietoja toimintojen lisäämisestä ja Business Central -sovelluksen mukauttamisesta laajennusten asentamisen avulla.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 805350a7b1213ec0e0d0550e5c5b63c557ee470a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771337"
---
# <a name="customizing-business-central-online-using-extensions"></a>Business Central Onlinen mukauttaminen laajennusten avulla

Voit muuttaa [!INCLUDE[prod_short](includes/prod_short.md)] onlinea asentamalla laajennuksia, jotka sisältävät lisätoimintoja, muuttavat toimintaa tai mahdollistavat esimerkiksi uusien verkkopalveluiden käyttämisen.

> [!NOTE]
> Jos haluat asentaa AppSourcen laajennuksia tai lisätä vuokraajakohtaisia laajennuksia, sinulla on oltava vaaditut käyttöoikeudet. Sinun on oltava D365 EXTENSION MGT -käyttäjäryhmän jäsen tai sinulla on oltava D365 EXTENSION MGT -käyttöoikeuksien joukko. Jos olet järjestelmänvalvoja, voit määrittää käyttäjäryhmiä ja käyttöoikeuksia yrityksesi muille käyttäjille.

Jos haluat käyttää laajennuksen mahdollistamaa toimintoa, kuten avata sivuja, suorittaa raportteja tai valita toimintoja, sinulla on oltava käyttöoikeuksien joukko, joka on asennettu laajennuksen osana.

> [!IMPORTANT]  
> Palveltavien laajennusten lataamista ja AppSource -laajennusten asentamista ei tueta yrityksen omissa tiloissa olevien asennusten **laajennuksen hallinta** -sivulla. AppSource-laajennuksia ei voi asentaa paikallisesti, esimerkiksi Docker-pohjaisissa käyttöönotoissa.

Kun käynnistät [!INCLUDE[prod_short](includes/prod_short.md)]in ensimmäisen kerran, joitakin laajennuksia on asennettu valmiiksi. Ajan kuluessa käytettävissä on yhä enemmän laajennuksia. Voit ottaa niitä käyttöön tarpeen mukaan.

Microsoft tarjoaa esimerkiksi laajennuksen, joka mahdollistaa integroinnin PayPal Payments Standard -ohjelman kanssa. Tämä laajennus asennetaan oletusarvoisesti.
Mutta jos käytettävissä on toinen laajennus, joka avulla voi suorittaa integroinnin toiseen maksujärjestelmään, voit asentaa uuden laajennuksen ja valita sen jälkeen käytettävän palvelun näistä kahdesta.  

Laajennuksia hallitaan **Laajennusten hallinta** -sivulla. Tämä sivu löytyy kotisivulta. Vaihtoehtoisesti voit valita **Etsi sivua tai raporttia** -kuvakkeen ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") oikeassa yläkulmassa. Syötä **Laajennus** ja valitse sitten liittyvä linkki. Lisätietoja on kohdassa [Laajennusten asentaminen ja asennusten poistaminen](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Jos sinulla on mielestäsi laajennuksen käyttöoikeus muttet löydä sen toimintoja, tarkista **Laajennusten hallinta** -sivu. Jos laajennusta ei mainita sivulla, voit asentaa sen seuraavassa osassa kerrotulla tavalla.  

> [!NOTE]  
> Kirjaudu sivustoon [AppSource.microsoft.com](https://appsource.microsoft.com/) [!INCLUDE[prod_short](includes/prod_short.md)] onlinessa käyttämäsi sähköpostitilin tiedoilla. Saman sähköpostitilin käyttäminen myös muissa palveluissa ja tuotteissa takaa sujuvan käyttökokemuksen.  

Kauppaan pääsee myös suoraan [!INCLUDE[prod_short](includes/prod_short.md)]ista. Tällä hetkellä asennettuna olevat laajennukset näkyvät **Laajennusten hallinta** -sivulla. Voit avata **Laajennuskauppa**-sivun, jossa näkyvät AppSourcessa tällä hetkellä käytettävissä olevat [!INCLUDE[prod_short](includes/prod_short.md)]in laajennukset. Jos valitset *Lisää sovelluksia* -linkin, sinut siirretään sivustoon [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Kun valitset laajennuksen, voit lukea tietoja laajennuksesta ja hakea lisätietoja käyttämällä laajennuksen Ohje-toimintoa. Kun haluat noutaa laajennuksen, sinun on hyväksyttävä käyttöehdot. Jos noudat laajennuksen AppSource-sivustosta, sinut kirjataan sisään [!INCLUDE[prod_short](includes/prod_short.md)]iin asennuksen viimeistelemiseksi.  

Laajennus on ehkä määritettävä asennuksen yhteydessä. Se tarkoittaa esimerkiksi **[!INCLUDE[prod_short](includes/prod_short.md)]in PayPal Payments Standard** -laajennuksen käyttämisessä tarvittavan tilin määrittämistä.
Muissa laajennuksissa esimerkiksi yksinkertaisesti lisätään kenttiä olemassa olevalle sivulle tai lisätään uusi sivu.   

Jos poistat laajennuksen asennuksen ja haluat ottaa sen takaisin käyttöön, voit asentaa laajennuksen uudelleen. Kun poistat käytössäsi olleen laajennuksen asennuksen, tiedot säilytetään. Jos siis asennat laajennuksen uudelleen, tiedot ovat yhä käytettävissäsi. Jotkin laajennukset ovat pakollisia. Niiden asennuksen poistaminen **Laajennusten hallinta** -sivulla on estetty. Jos yrität tehdä niin, näyttöön avautuu virhesanoma.  

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

> [!NOTE]  
> Voit pitää silmällä Microsoftin ja muiden toimittajien uusia laajennuksia osoitteessa [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).


## <a name="extensions-and-data-transfer"></a>Laajennukset ja tietojen siirto

Koska seuraavia laajennuksia käytetään viestintään muiden palvelujen kanssa, ne saattavat siirtää tietoja [!INCLUDE[prod_short](includes/prod_short.md)] -ympäristön maantieteellisen alueen ulkopuolelle:

* AMC Banking 365 Fundamentals -laajennus
* Image Analyzer
* Myöhästyneen maksun ennuste
* PayPal Payments Standard
* Myynti- ja varastoennuste
* WorldPay Payments Standard

Tämä koskee myös joitakin perussovelluksen toimintoja, kuten seuraavia ominaisuuksia:

* Kassavirtaennuste
* Document Exchange -palvelu
* Dataverse-yhteys
* OCR-palvelu
* Online Map
* EU:n ALV-nron tarkistuksen Palvelu

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
