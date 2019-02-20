---
title: Business Central -sovelluksen mukauttaminen asentamalla laajennuksia | Microsoft Docs
description: "Lisätietoja toimintojen lisäämisestä ja Business Central -sovelluksen mukauttamisesta laajennusten asentamisen avulla."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 11/27/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: add32e82465610830b68a979e238103bfa10d438
ms.openlocfilehash: 8b68012cc6032d14071ec0eb30c0efaf947344a0
ms.contentlocale: fi-fi
ms.lasthandoff: 11/29/2018

---
# <a name="customizing-business-central-using-extensions"></a>Business Central -sovelluksen mukauttaminen laajennusten avulla
Voit muuttaa [!INCLUDE[d365fin](includes/d365fin_md.md)]ia asentamalla laajennuksia, jotka sisältävät lisätoimintoja, muuttavat toimintaa tai mahdollistavat esimerkiksi uusien verkkopalveluiden käyttämisen.
Kun käynnistät [!INCLUDE[d365fin](includes/d365fin_md.md)]in ensimmäisen kerran, joitakin laajennuksia on asennettu valmiiksi. Ajan kuluessa käytettävissä on yhä enemmän laajennuksia. Voit ottaa niitä käyttöön tarpeen mukaan.

Microsoft tarjoaa esimerkiksi laajennuksen, joka mahdollistaa integroinnin PayPal Payments Standard -ohjelman kanssa. Tämä laajennus asennetaan oletusarvoisesti.
Mutta jos käytettävissä on toinen laajennus, joka avulla voi suorittaa integroinnin toiseen maksujärjestelmään, voit asentaa uuden laajennuksen ja valita sen jälkeen käytettävän palvelun näistä kahdesta.  

Laajennuksia hallitaan **Laajennusten hallinta** -sivulla. Tämä sivu löytyy kotisivulta. Vaihtoehtoisesti voit valita **Etsi sivua tai raporttia** -kuvakkeen ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") oikeassa yläkulmassa. Syötä **Laajennus** ja valitse sitten liittyvä linkki.  

> [!NOTE]  
>   Jos sinulla on mielestäsi laajennuksen käyttöoikeus muttet löydä sen toimintoja, tarkista **Laajennusten hallinta** -sivu. Jos laajennusta ei mainita sivulla, voit asentaa sen seuraavassa osassa kerrotulla tavalla.  

## <a name="installing-an-extension"></a>Laajennuksen asentaminen
Uusia laajennuksia on saatavana kauppapaikasta osoitteessa [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?src=dynamics365website&product=dynamics-365-business-central). Kaupassa on nähtävänä kaikki [!INCLUDE[d365fin](includes/d365fin_md.md)]in saatavilla olevat laajennukset, ja voit hankkia sieltä muiden Microsoftin tuotteiden sovelluksia, laajennuksia ja sisältöpaketteja. Määritä soveltuvat suodattimet, tutustu kunkin laajennuksen tietoihin ja hae laajennus [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.  
> [!NOTE]  
>   Kirjaudu sivustoon [AppSource.microsoft.com](https://appsource.microsoft.com/) [!INCLUDE[d365fin](includes/d365fin_md.md)]issa käyttämäsi sähköpostitilin tiedoilla. Saman sähköpostitilin käyttäminen myös muissa palveluissa ja tuotteissa takaa sujuvan käyttökokemuksen.  

Kauppaan pääsee myös suoraan [!INCLUDE[d365fin](includes/d365fin_md.md)]ista. Tällä hetkellä asennettuna olevat laajennukset näkyvät **Laajennusten hallinta** -sivulla. Voit avata **Laajennuskauppa**-sivun, jolla näkyvät AppSource-sivustossa tällä hetkellä käytettävissä olevat [!INCLUDE[d365fin](includes/d365fin_md.md)]in laajennukset. Jos valitset *Lisää sovelluksia* -linkin, sinut siirretään osoitteeseen [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).  

Kun valitset laajennuksen, voit lukea tietoja laajennuksesta ja hakea lisätietoja käyttämällä laajennuksen Ohje-toimintoa. Kun haluat noutaa laajennuksen, sinun on hyväksyttävä käyttöehdot. Jos noudat laajennuksen AppSource-sivustosta, sinut kirjataan sisään [!INCLUDE[d365fin](includes/d365fin_md.md)]iin asennuksen viimeistelemiseksi.  

Laajennus on ehkä määritettävä asennuksen yhteydessä. Se tarkoittaa esimerkiksi **[!INCLUDE[d365fin](includes/d365fin_md.md)]in PayPal Payments Standard** -laajennuksen käyttämisessä tarvittavan tilin määrittämistä.
Muissa laajennuksissa esimerkiksi yksinkertaisesti lisätään kenttiä olemassa olevalle sivulle tai lisätään uusi sivu.   

Jos poistat laajennuksen asennuksen ja haluat ottaa sen takaisin käyttöön, voit asentaa laajennuksen uudelleen. Kun poistat käytössäsi olleen laajennuksen asennuksen, tiedot säilytetään. Jos siis asennat laajennuksen uudelleen, tiedot ovat yhä käytettävissäsi.  

Jotkin ovat Microsoftin laajennuksia, jotkin [muiden yritysten](ui-extensions-other.md). Kaikki laajennukset testataan, ennen kuin ne ovat käyttäjien käytettävissä. Suosittelemme kuitenkin lisätietoihin tutustumista laajennuksen mukana saatavien linkkien avulla ennen laajennuksen asentamista.  

Microsoft tarjoaa seuraavat laajennukset:  

* [Dynamics GP -tietojen siirto](ui-extensions-dynamicsgp-data-migration.md)  
* [Envestnet Yodlee -pankkisyötteet](ui-extensions-yodlee-bank-feeds.md)  
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)  
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)  
* [QuickBooks-tietojen siirto](ui-extensions-quickbooks-data-migration.md)  
* [Myynti- ja varastoennuste](ui-extensions-sales-forecast.md)  
* [Ceridian Payroll](ui-extensions-ceridian-payroll.md)  
* [Quickbooks Payroll -tiedostojen tuonti](ui-extensions-quickbooks-payroll.md)  
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)  
* [Ison-Britannian postinumeroiden GetAddress.io](ui-extensions-getaddressio.md)  
* [QuickBooks Online -tietojen siirto](ui-extensions-quickbooks-online-data-migration.md)  
* [Kirjanpitäjän portaali](ui-extensions-accountant-portal.md)  
* [Kuvan analysointitoiminto](ui-extensions-image-analyzer.md)  
* [Maksut ja täsmäytykset](ui-extensions-payments-reconciliation-formats-dk.md)  
* [C5-tietojen siirto](ui-extensions-c5-data-migration.md)  
* [Olennaiset liiketoimintanäkemykset](ui-extensions-essential-business-insights.md)  
* [Myöhästyneen maksun ennusteet](ui-extensions-late-payment-prediction.md  )

> [!NOTE]  
>  Uudet laajennukset eivät ole saatavana AppSourcessa heti, kun ilmoitamme päivityksestä. Voit tarkkailla laajennuksia osoitteessa [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).

## <a name="see-also"></a>Katso myös
[Dynamics 365 Business Centralin laajentaminen](about-develop-extensions.md)  
[Envestnet Yodlee -pankkisyötepalvelun määrittäminen](bank-how-setup-bank-statement-service.md)  
[Asiakkaan maksujen ottaminen käyttöön PayPalin kautta](sales-how-enable-payment-service-extensions.md)  
[Liiketoiminnan tietojen siirtäminen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[Muiden palveluntarjoajien [!INCLUDE[d365fin](includes/d365fin_md.md)]in laajennukset](ui-extensions-other.md)  
[Käytön aloittaminen](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

