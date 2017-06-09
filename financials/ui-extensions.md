---
title: Dynamics 365 for Financials mukauttaminen laajennuksilla | Microsoft Docs
description: Dynamics 365 for Financials mukauttaminen laajennuksilla
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 04/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1de01d9944489f862dfc6db145c1542c3d0dd2e3
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="customizing-dynamics-365-for-financials-using-extensions"></a>Dynamics 365 for Financials mukauttaminen laajennuksilla
Voit muuttaa [!INCLUDE[d365fin](includes/d365fin_md.md)]ia asentamalla laajennuksia, jotka sisältävät lisätoimintoja, muuttavat toimintaa tai mahdollistavat esimerkiksi uusien verkkopalveluiden käyttämisen.
Kun käynnistät [!INCLUDE[d365fin](includes/d365fin_md.md)]in ensimmäisen kerran, joitakin laajennuksia on asennettu valmiiksi. Ajan kuluessa käytettävissä on yhä enemmän laajennuksia. Voit ottaa niitä käyttöön tarpeen mukaan.

Microsoft tarjoaa esimerkiksi laajennuksen, joka mahdollistaa integroinnin PayPal Payments Standard -ohjelman kanssa. Tämä laajennus asennetaan oletusarvoisesti.
Mutta jos käytettävissä on toinen laajennus, joka avulla voi suorittaa integroinnin toiseen maksujärjestelmään, voit asentaa uuden laajennuksen ja valita sen jälkeen käytettävän palvelun näistä kahdesta.  

Laajennuksia hallitaan **Laajennusten hallinta** -ikkunassa. Tämä ikkuna löytyy kotisivulta. Voit myös valita oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvakkeen ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoittaa **Laajennus** ja valita sitten liittyvän linkin.  

**Huomautus**: Jos sinulla on mielestäsi laajennuksen käyttöoikeus muttet löydä sen toimintoja, tarkista **Laajennusten hallinta** -ikkuna. Jos laajennusta ei mainita ikkunassa, voit asentaa seuraavassa osassa kuvattavalla tavalla.  

## <a name="installing-an-extension"></a>Laajennuksen asentaminen
Uusia laajennuksia on saatavana kauppapaikasta osoitteessa [AppSource.microsoft.com](https://appsource.microsoft.com/). Kaupassa on nähtävänä kaikki [!INCLUDE[d365fin](includes/d365fin_md.md)]in saatavilla olevat laajennukset, ja voit hankkia sieltä muiden Microsoftin tuotteiden sovelluksia, laajennuksia ja sisältöpaketteja. Määritä soveltuvat suodattimet, tutustu kunkin laajennuksen tietoihin ja hae laajennus [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.  
**Huomautus**: Kirjaudu sivustoon [AppSource.microsoft.com](https://appsource.microsoft.com/) [!INCLUDE[d365fin](includes/d365fin_md.md)]issa käyttämäsi sähköpostitilin tiedoilla. Saman sähköpostitilin käyttäminen myös muissa palveluissa ja tuotteissa takaa sujuvan käyttökokemuksen.  

Kauppaan pääsee myös suoraan [!INCLUDE[d365fin](includes/d365fin_md.md)]ista. Tällä hetkellä asennettuna olevat laajennukset näkyvät **Laajennusten hallinta** -ikkunassa. Voit avata **Laajennuskauppa**-sivun, jolla näkyvät AppSource-sivustossa tällä hetkellä käytettävissä olevat [!INCLUDE[d365fin](includes/d365fin_md.md)]in laajennukset. Jos valitset *Lisää sovelluksia* -linkin, sinut siirretään osoitteeseen [AppSource.microsoft.com](https://appsource.microsoft.com/).  

Kun valitset laajennuksen, voit lukea tietoja laajennuksesta ja hakea lisätietoja käyttämällä laajennuksen Ohje-toimintoa. Kun haluat noutaa laajennuksen, sinun on hyväksyttävä käyttöehdot. Jos noudat laajennuksen AppSource-sivustosta, sinut kirjataan sisään [!INCLUDE[d365fin](includes/d365fin_md.md)]iin asennuksen viimeistelemiseksi.  

Laajennus on ehkä määritettävä asennuksen yhteydessä. Se tarkoittaa esimerkiksi **[!INCLUDE[d365fin](includes/d365fin_md.md)]in PayPal Payments Standard** -laajennuksen käyttämisessä tarvittavan tilin määrittämistä.
Muissa laajennuksissa esimerkiksi yksinkertaisesti lisätään kenttiä olemassa olevalle sivulle tai lisätään uusi sivu.   

Jos poistat laajennuksen asennuksen ja haluat ottaa sen takaisin käyttöön, voit asentaa laajennuksen uudelleen. Kun poistat käytössäsi olleen laajennuksen asennuksen, tiedot säilytetään. Jos siis asennat laajennuksen uudelleen, tiedot ovat yhä käytettävissäsi.  

Jotkin ovat Microsoftin laajennuksia, jotkin [muiden yritysten](ui-extensions-other.md). Kaikki laajennukset testataan, ennen kuin ne ovat käyttäjien käytettävissä. Suosittelemme kuitenkin lisätietoihin tutustumista laajennuksen mukana saatavien linkkien avulla ennen laajennuksen asentamista.  

Microsoft tarjoaa seuraavat laajennukset:  

* [Dynamics GP -tietojen siirto](ui-extensions-dynamicsgp-data-migration.md)  
* [Envestnet Yodlee -pankkisyötteet](ui-extensions-yodlee-bank-feeds.md)  
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)  
* [QuickBooks-tietojen siirto](ui-extensions-quickbooks-data-migration.md)  
* [Myynnin ja varaston ennuste](ui-extensions-sales-forecast.md)  
* [Ceridian Payroll](ui-extensions-ceridian-payroll.md)  
* [Quickbooks Payroll -tiedostojen tuonti](ui-extensions-quickbooks-payroll.md)  
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [Ison-Britannian postinumeroiden GetAddress.io](ui-extensions-getaddressio.md)

## <a name="see-also"></a>Katso myös
[Toimintaohje: Envestnet Yodlee -pankkisyötepalvelun määrittäminen](bank-how-setup-bank-statement-service.md)  
[Toimintaohje: Asiakkaan maksujen ottaminen käyttöön PayPalin kautta](sales-how-enable-payment-service-extensions.md)  
[Liiketoiminnan tietojen siirtäminen muista rahoitusjärjestelmistä](upload-data.md)  
[Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen](uk-setup-postal-code-service.md)  
[Muiden valmistajien [!INCLUDE[d365fin](includes/d365fin_md.md)]-laajennukset] (ui-extensions-other.md)  
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin](index.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
