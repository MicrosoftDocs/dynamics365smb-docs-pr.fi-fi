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
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765919"
---
# <a name="customizing-business-central-using-extensions"></a>Business Central -sovelluksen mukauttaminen laajennusten avulla

Voit muuttaa [!INCLUDE[d365fin](includes/d365fin_md.md)]ia asentamalla laajennuksia, jotka sisältävät lisätoimintoja, muuttavat toimintaa tai mahdollistavat esimerkiksi uusien verkkopalveluiden käyttämisen.

> [!NOTE]
> Jos haluat asentaa AppSourcen laajennuksia tai lisätä vuokraajakohtaisia laajennuksia, sinulla on oltava vaaditut käyttöoikeudet. Sinun on oltava D365 EXTENSION MGMT -käyttäjäryhmän jäsen tai sinulla on oltava D365 EXTENSION MGMT -käyttöoikeuksien joukko. Jos olet järjestelmänvalvoja, voit määrittää käyttäjäryhmiä ja käyttöoikeuksia yrityksesi muille käyttäjille.<br /><br />
Jos haluat käyttää laajennuksen mahdollistamaa toimintoa, kuten avata sivuja, suorittaa raportteja tai valita toimintoja, sinulla on oltava käyttöoikeuksien joukko, joka on asennettu laajennuksen osana.

> [!IMPORTANT]  
> Palveltavien laajennusten lataamista ja AppSource -laajennusten asentamista ei tueta yrityksen omissa tiloissa olevien asennusten **laajennuksen hallinta** -sivulla.

Kun käynnistät [!INCLUDE[d365fin](includes/d365fin_md.md)]in ensimmäisen kerran, joitakin laajennuksia on asennettu valmiiksi. Ajan kuluessa käytettävissä on yhä enemmän laajennuksia. Voit ottaa niitä käyttöön tarpeen mukaan.

Microsoft tarjoaa esimerkiksi laajennuksen, joka mahdollistaa integroinnin PayPal Payments Standard -ohjelman kanssa. Tämä laajennus asennetaan oletusarvoisesti.
Mutta jos käytettävissä on toinen laajennus, joka avulla voi suorittaa integroinnin toiseen maksujärjestelmään, voit asentaa uuden laajennuksen ja valita sen jälkeen käytettävän palvelun näistä kahdesta.  

Laajennuksia hallitaan **Laajennusten hallinta** -sivulla. Tämä sivu löytyy kotisivulta. Vaihtoehtoisesti voit valita **Etsi sivua tai raporttia** -kuvakkeen ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") oikeassa yläkulmassa. Syötä **Laajennus** ja valitse sitten liittyvä linkki. Lisätietoja on kohdassa [Laajennusten asentaminen ja asennusten poistaminen](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Jos sinulla on mielestäsi laajennuksen käyttöoikeus muttet löydä sen toimintoja, tarkista **Laajennusten hallinta** -sivu. Jos laajennusta ei mainita sivulla, voit asentaa sen seuraavassa osassa kerrotulla tavalla.  

> [!NOTE]  
> Uudet laajennukset eivät ole saatavana AppSourcessa heti, kun ilmoitamme päivityksestä. Voit tarkkailla laajennuksia osoitteessa [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

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
