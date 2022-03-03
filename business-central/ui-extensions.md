---
title: Business Central -sovelluksen mukauttaminen asentamalla laajennuksia
description: Lisätietoja toimintojen lisäämisestä ja Business Central -sovelluksen mukauttamisesta laajennusten asentamisen avulla.
author: edupont04
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/25/2021
ms.author: edupont
ms.openlocfilehash: 7839c4364f299619707b0a346b9b5d0db07e627b
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8132418"
---
# <a name="customizing-business-central-online-using-extensions"></a>Business Central Onlinen mukauttaminen laajennusten avulla

Voit muuttaa [!INCLUDE[prod_short](includes/prod_short.md)] onlinea asentamalla laajennuksia, jotka sisältävät lisätoimintoja, muuttavat toimintaa tai mahdollistavat esimerkiksi uusien verkkopalveluiden käyttämisen.

> [!NOTE]
> Jos haluat asentaa AppSourcen laajennuksia tai poistaa niitä tai lisätä vuokraajakohtaisia laajennuksia, sinulla on oltava vaaditut käyttöoikeudet. Sinun täytyy olla jäsen joko EXTEND. MGT. - ADMIN -käyttäjäryhmässä tai sinulla on oltava EXTEND. MGT. - ADMIN -käyttöoikeudet. Jos olet järjestelmänvalvoja, voit määrittää käyttäjäryhmiä ja käyttöoikeuksia yrityksesi muille käyttäjille.
>
> Jos haluat käyttää laajennuksen mahdollistamaa toimintoa, kuten avata sivuja, suorittaa raportteja tai valita toimintoja, sinulla on oltava käyttöoikeuksien joukko, joka on asennettu laajennuksen osana.

> [!NOTE]  
> **EXTEND. MGT. - ADMIN** -käyttöoikeudet otettiin käyttöön Business Central 2021:n julkaisuaallossa 1, ja ne korvasivat aiemmissa versioissa olleet **D365 EXTENSION MGT** -käyttöoikeudet.

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

## <a name="recommended-apps"></a>Suositellut sovellukset
Microsoft-kumppanit ja -jälleenmyyjät voivat luoda laajennuksia, joita he voivat käyttää sovellusluetteloiden laatimiseen, joita he usein suosittelevat asiakkailleen. Jos he tekevät näin ja ovat ottaneet laajennuksen käyttöön vuokraajassasi, sovellukset ovat käytettävissä **Suositellut sovellukset** -sivulla. Siellä voit lukea kustakin sovelluksesta ja päättää, asennetaanko se.

> [!NOTE]
> Jos olet Microsoft-kumppani tai -jälleenmyyjä ja olet kiinnostunut tarjoamaan luettelon suositelluista sovelluksista, katso [Suositellut sovellukset AppSourcesta](/dynamics365/business-central/dev-itpro/administration/recommend-apps).

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
