---
title: Dynamics 365 Business Centralin mukauttaminen | Microsoft Docs
description: Business Centralin sovellusten ja laajennusten luominen, esitteleminen ja markkinoiminen.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 7e1ef15d8076aa0a17978de5418f39a2de8a1ac0
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188946"
---
# <a name="extending-d365fin"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] -järjestelmän laajentaminen
Microsoft [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]on liiketoiminnan hallintaratkaisu, joka auttaa yrityksiä yhdistämään taloushallinnon, myynnin, palvelun ja toiminnot, jotta voitaisiin virtaviivaistaa liiketoimintaprosesseja, parantaa asiakasviestinnän toimintoja ja tehdä parempia päätöksiä. [!INCLUDE[d365fin](includes/d365fin_md.md)]on käytettävissä pilvessä ja käyttäjille useilla erilaisilla laitteilla, ja on aina ajan tasalla. Tämän nykyaikaisen liiketoiminta-alustan avulla voit nopeasti ja helposti mukauttaa, laajentaa ja luoda sovelluksia, jotta ne sopisivat tarpeisiisi – vähäisellä koodilla tai jopa ilman koodia.  

[!INCLUDE[d365fin](includes/d365fin_md.md)]in käytöstä alustana on monia etuja sovellusten muodostajille:

* Aloita ongelmitta saumattoman perehdytyskokemuksen ansiosta
* Käytä Microsoftin Markkinoille-palvelua
* Sovelluksen luettelointisivun mukauttaminen
* Ota suoraan yhteyttä päätöksentekijöihin ja tavoita enemmän asiakkaita
* Tehosta liiketoiminnan arvoa ja kasvata kauppojen kokoa vanhojen ja uusien asiakkaiden kanssa
* Modernien käyttökokemuksen tarjoava skaalautuva alusta parantaa tuloksia.  
* Hanki toimintaa ohjaavia näkemyksiä luetteloidesi tehokkuudesta Cloud Partner Portalin tai Office-sovellusten julkaisuprosessin kautta
* Yhdistäminen älykkäisiin liiketoimintasovelluksiin, kuten Power Apps, Power Automate, Power BI ja Azure AI  

Tuo omat [!INCLUDE[d365fin](includes/d365fin_md.md)] -palvelut to Microsoft AppSourceen:

**Yksittäisinä sovelluksina** – joilla tuot toimialaosaamisesi markkinoille.  
**Paketoituina konsultointipalveluina** – joilla tuot markkinoille valmiita aktivointipaketteja markkinoille.

Uusien kehitystyökalujen avulla voit rakentaa laajennuksia [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjille. Voit halutessasi tutustua uusiin työkaluihin tai katsoa lisätietoja laajennusversiosta 2.0 osoitteessa [aka.ms/GetStartedWithApps](https://aka.ms/GetStartedWithApps).  

Tietoja sovelluksista ja konsulttipalveluista, jotka ovat tällä hetkellä käytettävissä [Microsoft AppSourcessa](https://appsource.microsoft.com/marketplace/consulting-services?country=US&page=1&product=dynamics-365%3Bdynamics-365-business-central).

Jotta yrityskäyttäjät voivat aloittaa nopeasti, Microsoft on lisännyt AppSourceen luettelon konsulttipalveluista ratkaisuille, jotka perustuvat seuraaviin: [!INCLUDE[prodshort](includes/prodshort.md)], Power BI ja Power Apps. Lisätietoja [konsultointipalveluista ](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-consulting).

## <a name="choosing-which-services-to-offer-with-d365fin"></a>Valitse, mitä palveluita tarjoat seuraavan kanssa: [!INCLUDE[d365fin](includes/d365fin_md.md)]

### <a name="integrate-a-3rd-party-solution"></a>Integroi 3. osapuolten ratkaisu
[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää useita valmiita avulla ohjelmointirajapintoja [Connect-sovelluksille](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-connect-apps), jotta voit toteuttaa saumattoman integroinnin palvelusi ja [!INCLUDE[d365fin](includes/d365fin_md.md)]:n välille. Voit niputtaa palvelusi [!INCLUDE[d365fin](includes/d365fin_md.md)]:n kanssa ja tarjota asiakkaillesi integroidun kokemuksen. Lisätietoja [3. osapuolen ratkaisun integroinnista](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-thirdparty-solution).

### <a name="development-of-a-vertical-solution"></a>Vertikaalisen ratkaisun kehittäminen
Luo sovellus, joka on suunniteltu tietylle toimialalle. [Embed-sovelluksen](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-embed-apps) avulla voit laajentaa ja mukauttaa olemassa olevaa [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellusta ja rikastaa loppukäyttäjän kokemusta toimialakohtaisilla ominaisuuksilla käyttämällä uusia ja moderneja kehitystyölkaluja Extensions-versiota 2.0. Lisätietoja [vertikaalisen ratkaisun kehittämisestä ](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-vertical).

### <a name="development-of-a-horizontal-solution"></a>Horisontaalisen ratkaisun kehittäminen
Laajenna [!INCLUDE[d365fin](includes/d365fin_md.md)]:n käyttökokemusta ja ominaisuuksia luomalla [lisäosasovellus](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-add-on-apps), joka integroituu [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjäkokemukseen. Muodosta käyttöliittymä, joka perustuu siihen, miten haluat tietojen siirtyvän [!INCLUDE[d365fin](includes/d365fin_md.md)]:n ja palveluidesi välillä. Lisätietoja [horisontaalisen ratkaisun kehittämisestä ](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-horizontal).

### <a name="development-of-a-localization-solution"></a>Lokalisointiratkaisun kehittäminen
Noudata paikallista säännöstenmukaisuutta kehittämällä [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellusta, joka mukautuu paikallisten markkinoiden vaatimiin toimintoihinyhdessä [Dynamics 365 -käännöspalvelun](/dynamics365/unified-operations/fin-ops-core/dev-itpro/lifecycle-services/translation-service-overview) kanssa. Kohdista paikalliset lakisääteiset vaatimukset ja laajenna ominaisuuksia, jotta voi onnistuneesti kilpailla paikallisilla markkinoilla. Lisätietoja [lokalisointiratkaisun kehittämisestä ](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-localization).

### <a name="reseller-solution"></a>Jälleenmyyjäratkaisu
Koska kaikki yritykset ovat ainutlaatuisia, [mukauttaminen vuokraajia](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-customizing-tenants) voit määrittää, miten käsittelet yksinkertaistettuja prosessejasi, omaa terminologiaa ja sitä, miten työntekijäsi tai osastosi ovat yhetydessä ja tekevät yhteistyötä. Lisäksi voit valita jälleenmyydä ja mukauttaa [!INCLUDE[d365fin](includes/d365fin_md.md)]:n asiakkaiden yksilöllisiin tarpeisiin tarjoamalla [konsultointipalveluita](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-consulting). Tai käytä Power Appsia, Power Automatea ja Power BI:tä, jotta voit luoda [mukautettuja työnkulkuja](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-no-code), sovelluksia ja liiketoimintaraportteja ilman koodin kirjoittamista. Lisätietoja: [Dynamics 365 Reseller (VARs)](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-reseller).

## <a name="where-do-i-learn-more"></a>Mistä löydän lisätietoja?
Katso lisätietoja Microsoft AppSourcen konsultointipalveluiden tarjoomasta seuraavissa linkeissä:

[AppSourcen konsultointitarjooma](https://appsource.microsoft.com/marketplace/consulting-services)  
[Kumppanien kelpoisuus](https://smp-cdn-prod.azureedge.net/documents/Microsoft%20AppSource%20Partner%20Listing%20Guidelines.pdf)  
[Kumppanin nimityslomake](https://appsource.microsoft.com/partners/list-consulting-service)  

## <a name="the-ready-to-go-program"></a>Valmis aloittamaan -ohjelma
Valmis aloittamaan -ohjelma on suunniteltu tukemaan sinua, kun tuot [!INCLUDE[d365fin](includes/d365fin_md.md)] -tarjoomia Microsoft AppSourceen. Ohjelman sisältö:

- [Verkkokursseja](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-learning-catalog)
- [Koulutusta ja työpajoja](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-ready-to-go)
- [Microsoft Collaborate -ympäristön](https://aka.ms/Collaborate)

Lisätietoja siitä, miten voit rakentaa [!INCLUDE[d365fin](includes/d365fin_md.md)] -tarjooman [Valmis aloittamaan -ohjelmassa](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-ready-to-go). Jos sinulla on kysymyksiä tai palautetta **Valmis aloittamaan** -ohjelmasta, voit [ottaa meihin hteyttä ](mailto:dyn365bep@microsoft.com).

## <a name="d365fin-extensions-provided-by-microsoft"></a>Microsoftin [!INCLUDE[d365fin](includes/d365fin_md.md)] -laajennukset
Tuotteen vakioversio sisältää entistä enemmän Microsoftin kehittämiä laajennuksia. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md).

## <a name="see-also"></a>Katso myös
[Käytön aloittaminen](product-get-started.md)  

[https://appsource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
