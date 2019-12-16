---
title: Business Central -sovelluksen mukauttaminen asentamalla laajennuksia | Microsoft Docs
description: Lisätietoja toimintojen lisäämisestä ja Business Central -sovelluksen mukauttamisesta laajennusten asentamisen avulla.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 10/14/2019
ms.author: edupont
ms.openlocfilehash: 595e52118cc4fa6aea1959e2ddea323b048a9d27
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882084"
---
# <a name="customizing-business-central-using-extensions"></a>Business Central -sovelluksen mukauttaminen laajennusten avulla
Voit muuttaa [!INCLUDE[d365fin](includes/d365fin_md.md)]ia asentamalla laajennuksia, jotka sisältävät lisätoimintoja, muuttavat toimintaa tai mahdollistavat esimerkiksi uusien verkkopalveluiden käyttämisen.

> [!NOTE]
> Jos haluat asentaa AppSourcen laajennuksia tai lisätä vuokraajakohtaisia laajennuksia, sinulla on oltava vaaditut käyttöoikeudet. Sinun on oltava D365 EXTENSION MGMT -käyttäjäryhmän jäsen tai sinulla on oltava D365 EXTENSION MGMT -käyttöoikeuksien joukko. Jos olet järjestelmänvalvoja, voit määrittää käyttäjäryhmiä ja käyttöoikeuksia yrityksesi muille käyttäjille.<br /><br />
Jos haluat käyttää laajennuksen mahdollistamaa toimintoa, kuten avata sivuja, suorittaa raportteja tai valita toimintoja, sinulla on oltava käyttöoikeuksien joukko, joka on asennettu laajennuksen osana.

Kun käynnistät [!INCLUDE[d365fin](includes/d365fin_md.md)]in ensimmäisen kerran, joitakin laajennuksia on asennettu valmiiksi. Ajan kuluessa käytettävissä on yhä enemmän laajennuksia. Voit ottaa niitä käyttöön tarpeen mukaan.

Microsoft tarjoaa esimerkiksi laajennuksen, joka mahdollistaa integroinnin PayPal Payments Standard -ohjelman kanssa. Tämä laajennus asennetaan oletusarvoisesti.
Mutta jos käytettävissä on toinen laajennus, joka avulla voi suorittaa integroinnin toiseen maksujärjestelmään, voit asentaa uuden laajennuksen ja valita sen jälkeen käytettävän palvelun näistä kahdesta.  

Laajennuksia hallitaan **Laajennusten hallinta** -sivulla. Tämä sivu löytyy kotisivulta. Vaihtoehtoisesti voit valita **Etsi sivua tai raporttia** -kuvakkeen ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") oikeassa yläkulmassa. Syötä **Laajennus** ja valitse sitten liittyvä linkki.  

> [!NOTE]  
>   Jos sinulla on mielestäsi laajennuksen käyttöoikeus muttet löydä sen toimintoja, tarkista **Laajennusten hallinta** -sivu. Jos laajennusta ei mainita sivulla, voit asentaa sen seuraavassa osassa kerrotulla tavalla.  

## <a name="installing-an-extension"></a>Laajennuksen asentaminen
Uusia laajennuksia on saatavana kaupasta osoitteessa [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1). Kaupassa on nähtävänä kaikki [!INCLUDE[d365fin](includes/d365fin_md.md)]in saatavilla olevat laajennukset, ja voit hankkia sieltä muiden Microsoftin tuotteiden sovelluksia, laajennuksia ja sisältöpaketteja. Määritä soveltuvat suodattimet, tutustu kunkin laajennuksen tietoihin ja hae laajennus [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.  
> [!NOTE]  
>   Kirjaudu sivustoon [AppSource.microsoft.com](https://appsource.microsoft.com/) [!INCLUDE[d365fin](includes/d365fin_md.md)]issa käyttämäsi sähköpostitilin tiedoilla. Saman sähköpostitilin käyttäminen myös muissa palveluissa ja tuotteissa takaa sujuvan käyttökokemuksen.  

Kauppaan pääsee myös suoraan [!INCLUDE[d365fin](includes/d365fin_md.md)]ista. Tällä hetkellä asennettuna olevat laajennukset näkyvät **Laajennusten hallinta** -sivulla. Voit avata **Laajennuskauppa**-sivun, jossa näkyvät AppSourcessa tällä hetkellä käytettävissä olevat [!INCLUDE[d365fin](includes/d365fin_md.md)]in laajennukset. Jos valitset *Lisää sovelluksia* -linkin, sinut siirretään sivustoon [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Kun valitset laajennuksen, voit lukea tietoja laajennuksesta ja hakea lisätietoja käyttämällä laajennuksen Ohje-toimintoa. Kun haluat noutaa laajennuksen, sinun on hyväksyttävä käyttöehdot. Jos noudat laajennuksen AppSource-sivustosta, sinut kirjataan sisään [!INCLUDE[d365fin](includes/d365fin_md.md)]iin asennuksen viimeistelemiseksi.  

Laajennus on ehkä määritettävä asennuksen yhteydessä. Se tarkoittaa esimerkiksi **[!INCLUDE[d365fin](includes/d365fin_md.md)]in PayPal Payments Standard** -laajennuksen käyttämisessä tarvittavan tilin määrittämistä.
Muissa laajennuksissa esimerkiksi yksinkertaisesti lisätään kenttiä olemassa olevalle sivulle tai lisätään uusi sivu.   

Jos poistat laajennuksen asennuksen ja haluat ottaa sen takaisin käyttöön, voit asentaa laajennuksen uudelleen. Kun poistat käytössäsi olleen laajennuksen asennuksen, tiedot säilytetään. Jos siis asennat laajennuksen uudelleen, tiedot ovat yhä käytettävissäsi. Jotkin laajennukset ovat pakollisia. Niiden asennuksen poistaminen **Laajennusten hallinta** -sivulla on estetty. Jos yrität tehdä niin, näyttöön avautuu virhesanoma.  

Jotkin ovat Microsoftin laajennuksia, jotkin [muiden yritysten](ui-extensions-other.md). Kaikki laajennukset testataan, ennen kuin ne ovat käyttäjien käytettävissä. Suosittelemme kuitenkin lisätietoihin tutustumista laajennuksen mukana saatavien linkkien avulla ennen laajennuksen asentamista.  

Microsoft tarjoaa seuraavat laajennukset:  

* [Business Centralin kirjanpitäjän portaali](ui-extensions-accountant-portal.md)
* [Ceridian Payroll](ui-extensions-ceridian-payroll.md)
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
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [AMC Banking 365 -perusteiden laajennus](ui-extensions-amc-banking.md)
* [DK – C5-tietojen siirto](ui-extensions-c5-data-migration.md)
* [DK - Maksut ja täsmäytykset](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK – Verotiedostomuodot](ui-extensions-tax-file-formats-dk.md)
* [UK – Ison-Britannian postinumeroiden GetAddress.io](ui-extensions-getaddressio.md)
* [US/CA/UK/AU/NZ/ZA - Maksusuositusehdotuksen lähettäminen](ui-extensions-send-remittance-advice.md)
* [Muiden toimittajien Business Central -laajennukset](ui-extensions-other.md)

> [!NOTE]  
>  Uudet laajennukset eivät ole saatavana AppSourcessa heti, kun ilmoitamme päivityksestä. Voit tarkkailla laajennuksia osoitteessa [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## <a name="see-also"></a>Katso myös
[Dynamics 365 Business Centralin laajentaminen](about-develop-extensions.md)  
[Muiden toimittajien Business Central -laajennukset](ui-extensions-other.md)  
[Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md)  
[Asiakkaan maksujen ottaminen käyttöön PayPalin kautta](sales-how-enable-payment-service-extensions.md)  
[Liiketoiminnan tietojen siirtäminen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[Muiden palveluntarjoajien [!INCLUDE[d365fin](includes/d365fin_md.md)]in laajennukset](ui-extensions-other.md)  
[Käytön aloittaminen](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
