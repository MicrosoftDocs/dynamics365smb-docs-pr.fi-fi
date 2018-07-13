---
title: Dynamics 365 Business Central -sovelluksen mukauttaminen | Microsoft Docs
description: Business Centralin sovellusten ja laajennusten luominen, esitteleminen ja markkinoiminen.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 04/12/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 69f660f8a19bd1fd9cb39a79d5be7977e68d3a47
ms.contentlocale: fi-fi
ms.lasthandoff: 06/28/2018

---
# <a name="extending-included365finlongincludesd365finlongmdmd"></a>[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] -järjestelmän laajentaminen
Microsoft [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]on liiketoiminnan hallintaratkaisu, joka auttaa yrityksiä yhdistämään taloushallinnon, myynnin, palvelun ja toiminnot, jotta voitaisiin virtaviivaistaa liiketoimintaprosesseja, parantaa asiakasviestinnän toimintoja ja tehdä parempia päätöksiä. [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]on käytettävissä pilvessä ja käyttäjille useilla erilaisilla laitteilla, ja on aina ajan tasalla. Tämän nykyaikaisen liiketoiminta-alustan avulla voit nopeasti ja helposti mukauttaa, laajentaa ja luoda sovelluksia, jotta ne sopisivat tarpeisiisi – vähäisellä koodilla tai jopa ilman koodia.  

[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]in käytöstä alustana on monia etuja sovellusten muodostajille:

* Aloita ongelmitta saumattoman perehdytyskokemuksen ansiosta 
* Käytä Microsoftin Markkinoille-palvelua
* Sovelluksen luettelointisivun mukauttaminen 
* Ota suoraan yhteyttä päätöksentekijöihin ja tavoita enemmän asiakkaita
* Tehosta liiketoiminnan arvoa ja kasvata kauppojen kokoa vanhojen ja uusien asiakkaiden kanssa
* Modernien käyttökokemuksen tarjoava skaalautuva alusta parantaa tuloksia.  
* Hanki toimintaa ohjaavia näkemyksiä luetteloidesi tehokkuudesta Cloud Partner Portalin tai Office-sovellusten julkaisuprosessin kautta
* Yhdistäminen älykkäisiin liiketoimintasovelluksiin, kuten PowerApps, Flow, Power BI ja Cortana Intelligence, on mahdollista.  

Tuo omat [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] -palvelut to Microsoft AppSourceen: 

**Yksittäisinä sovelluksina** – joilla tuot toimialaosaamisesi markkinoille.  
**Paketoituina konsultointipalveluina** – joilla tuot markkinoille valmiita aktivointipaketteja markkinoille.

Uusien kehitystyökalujen avulla voit rakentaa laajennuksia [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] -käyttäjille. Voit halutessasi tutustua uusiin työkaluihin tai katsoa lisätietoja laajennusversiosta 2.0 osoitteessa [aka.ms/GetStartedWithApps](http://aka.ms/GetStartedWithApps).  

Tietoja sovelluksista ja konsulttipalveluista, jotka ovat tällä hetkellä käytettävissä [Microsoft AppSourcessa](https://appsource.microsoft.com/en-us/marketplace/consulting-services?country=US&page=1).

Jotta yrityskäyttäjät voivat aloittaa nopeasti, Microsoft on lisännyt luettelon AppSourcen konsulttipalveluista ratkaisuille jotka perustuvat seuraaviin: [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], Power BI ja PowerApps. Lisätietoja [konsultointipalveluista ](/dynamics-nav/developer/readiness/readiness-consulting).

## <a name="choosing-which-services-to-offer-with-included365finlongincludesd365finlongmdmd"></a>Valitse, mitä palveluita tarjoat seuraavan kanssa: [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] 

### <a name="integrate-a-3rd-party-solution"></a>Integroi 3. osapuolten ratkaisu
[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] sisältää useita valmiita avulla ohjelmointirajapintoja [Connect-sovelluksille](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-connect-apps), jotta voit toteuttaa saumattoman integroinnin palvelusi ja [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]:n välille. Voit niputtaa palvelusi [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]:n kanssa ja tarjota asiakkaillesi integroidun kokemuksen. Lisätietoja [3. osapuolen ratkaisun integroinnista](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-thirdparty-solution).

### <a name="development-of-a-vertical-solution"></a>Vertikaalisen ratkaisun kehittäminen
Luo sovellus, joka on suunniteltu tietylle toimialalle. [Embed-sovelluksen](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-embed-apps) avulla voit laajentaa ja mukauttaa olemassa olevaa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] -sovellusta ja rikastaa loppukäyttäjän kokemusta toimialakohtaisilla ominaisuuksilla käyttämällä uusia ja moderneja kehitystyölkaluja Extensions-versiota 2.0. Lisätietoja [vertikaalisen ratkaisun kehittämisestä ](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-vertical).

### <a name="development-of-a-horizontal-solution"></a>Horisontaalisen ratkaisun kehittäminen
Laajenna [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]:n käyttökokemusta ja ominaisuuksia luomalla [lisäosasovellus](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-add-on-apps), joka integroituu [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] -käyttäjäkokemukseen. Muodosta käyttöliittymä, joka perustuu siihen, miten haluat tietojen siirtyvän [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]:n ja palveluidesi välillä. Lisätietoja [horisontaalisen ratkaisun kehittämisestä ](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-horizontal). 

### <a name="development-of-a-localization-solution"></a>Lokalisointiratkaisun kehittäminen
Noudata paikallista säännöstenmukaisuutta kehittämällä [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] -sovellusta, joka mukautuu paikallisten markkinoiden vaatimiin toimintoihinyhdessä [Dynamics 365 -käännöspalvelun](/dynamics365/unified-operations/dev-itpro/lifecycle-services/translation-service-overview) kanssa. Kohdista paikalliset lakisääteiset vaatimukset ja laajenna ominaisuuksia, jotta voi onnistuneesti kilpailla paikallisilla markkinoilla. Lisätietoja [lokalisointiratkaisun kehittämisestä ](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-localization).

### <a name="reseller-solution"></a>Jälleenmyyjäratkaisu
Koska kaikki yritykset ovat ainutlaatuisia, [mukauttaminen vuokraajia](/dynamics-nav/developer/readiness/readiness-customizing-tenants) voit määrittää, miten käsittelet yksinkertaistettuja prosessejasi, omaa terminologiaa ja sitä, miten työntekijäsi tai osastosi ovat yhetydessä ja tekevät yhteistyötä. Lisäksi voit valita jälleenmyydä ja mukauttaa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]:n asiakkaiden yksilöllisiin tarpeisiin tarjoamalla [konsultointipalveluita](/dynamics-nav/developer/readiness/readiness-consulting). Tai käytä Microsoft Flow-, Power Apps- ja Power BI -palveluita, jotta voit luoda [mukautettuja työnkulkuja](/dynamics-nav/developer/readiness/readiness-no-code), sovelluksia ja liiketoimintaraportteja tarvitsematta kirjoittaa riviäkään koodia. Lisätietoja: [Dynamics 365 Reseller (VARs)](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-reseller). 

## <a name="where-do-i-learn-more"></a>Mistä löydän lisätietoja?
Lisätietoja Microsoft AppSourcen konsultointipalveluiden tarjoomasta löydät seuraavista linkeistä: 

[AppSourcen konsultointitarjooma](https://appsource.microsoft.com/en-us/marketplace/consulting-services?country=US&page=1)  
[Kumppanien kelpoisuus](https://smp-cdn-prod.azureedge.net/documents/Microsoft%20AppSource%20Partner%20Listing%20Guidelines.pdf)  
[Kumppanin nimityslomake](https://appsource.microsoft.com/en-us/partners/list-consulting-service)  

## <a name="the-ready-to-go-program"></a>Ready to Go -ohjelma
Ready to Go -on suunniteltu tukemaan sinua, kun tuot Microsoft [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] -tarjouksia Microsoft Appsourceen. Ohjelman sisältö: 

- [Verkkokursseja](http://aka.ms/ReadyToGoOnlineLearning)
- [Koulutusta ja työpajoja](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-ready-to-go#the-ready-to-go-coaching)
- [Microsoft Collaborate -ympäristön](http://aka.ms/Collaborate)

Lisätietoja siitä, miten voit rakentaa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] -tarjooman [Ready to Go -ohjelmassa](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-ready-to-go). Jos sinulla on kysymyksiä tai palautetta **Ready to Go** -ohjelmasta, voit [ottaa meihin hteyttä ](mailto:dyn365bep@microsoft.com). 

## <a name="see-also"></a>Katso myös
[Käytön aloittaminen](product-get-started.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[https://appsource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365-for-financials&page=1)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

