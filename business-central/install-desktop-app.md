---
title: Business Centralin asentaminen työpöydälle
description: Tässä artikkelissa kuvataan, miten Business Central -sovellus saadaan Windows-tai MACiOS-työpöydälle.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: phone, tablet
ms.date: 10/01/2021
ms.author: jswymer
ms.openlocfilehash: babf20be3c22a3d4b7dd710e2486c59bc11351fe
ms.sourcegitcommit: 795f0298e32b4c0174aeeb9a7da64f1e5c8457d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/04/2021
ms.locfileid: "7596645"
---
# <a name="get-business-central-desktop-app"></a>Business Central -työpöytäsovelluksen hankkiminen

Jos sinulla on Windows (PC)- tai macOS-tietokone, voit asentaa Business Central -sovelluksen työpöydälle. 
> [!NOTE]
> Jos käytät Business Centralin vuoden 2021 1. julkaisuaallon versiota tai sitä vanhempaa versiota, hanki sovellus [Windows-kaupasta](https://go.microsoft.com/fwlink/?LinkId=734848).

## <a name="why-use-the-app"></a>Miksi käyttää sovellusta?

Business Central -sovellus muistuttaa verkkoasiakasta, mutta siinä on muutamia etuja, kuten:

- Sovellus on helposti saatavilla **Käynnistä**-valikosta, voit helposti kiinnittää sen tehtäväpalkkiin, tai se käynnistetään oletusarvoisesti, kun käynnistät tietokoneen.
- Yleensä sovellus on myös nopeampi ja sujuvampi hahmontaa ruudulla, ilman suorituskykyeroja, verrattuna [!INCLUDE[prod_short](includes/prod_short.md)]in käyttämiseen selaimessa.
- Sovellus avautuu omassa ikkunassaan kaikista selainikkunoista riippumatta. Tämän ominaisuuden ansiosta se on helpompi löytää, jos käytössä on monia sovelluksia tai selaimen välilehtiä.
- Jos käytössäsi on enemmän kuin yksi Business Central -ympäristö (vain online), voit asentaa sovelluksen erikseen kutakin ympäristöä varten.

     Kun avaat sovelluksen tiettyä ympäristöä varten, ympäristön nimi sisältyy ikkunan otsikkoon. Kun työskentelet useissa [!INCLUDE[prod_short](includes/prod_short.md)] -ympäristöissä, jokainen sovellusikkuna näytetään erikseen. Nimi helpottaa sinua näkemään, mikä ikkuna kuhunkin ympäristöön liittyy.

## <a name="install-the-app"></a>Asenna sovellus

1. Avaa [!INCLUDE[prod_short](includes/prod_short.md)] -verkkoasiakas joko Microsoft Edgessä tai Google Chromessa.

2. Jos näyttöön tulee ympäristön valintasivu, voit tehdä jommankumman seuraavista:

   - Valitse ympäristö ja siirry seuraavaan vaiheeseen, jossa sovellus asennetaan. Tässä tapauksessa asennettu sovellus avaa valitsemasi ympäristön.
   - Älä valitse ympäristöä ja siirry suoraan seuraavaan vaiheeseen, jossa sovellus asennetaan. Tässä tapauksessa asennettu sovellus avaa ympäristön valintasivun tietyn ympäristön sijaan.

3. Jos haluat asentaa sovelluksen, valitse selaimesta riippuen ![kuvake, jonka avulla voit asentaa sovelluksen Edgeen.](media/ui-edge-install-app-icon.png) **Sovellus saatavilla. Asenna Business Central** tai ![Kuvake sovelluksen asentamiseen Chromessa.](media/ui-chrome-install-app-icon.png) **Asenna Business Central**, sitten **Asenna**.

   | Microsoft Edge | Google Chrome |
   |--|--|
   | :::image type="content" source="media/ui-edge-install-app-v2.png" alt-text="kuva painikkeesta, jolla sovellus asennetaan Edgessä."::: | :::image type="content" source="media/ui-chrome-install-app-v2.png" alt-text="kuva painikkeesta, jolla sovellus asennetaan Chromessa."::: |

  > [!TIP]
  > Edgen avulla voit myös asentaa sovelluksen menemällä **selaimen asetusvalikkoon** ja valitsemalla sitten **Sovellukset** > **Asenna tämä sivusto sovelluksena** > **Asenna**.

Kun sovellus on asennettu, se näkyy **Käynnistä**-valikossa. Jos olet valinnut sovellukselle tietyn ympäristön, ympäristön nimi lisätään sovelluksen nimeen **Käynnistä**-valikossa.

### <a name="for-business-central-on-premises"></a>Business Central on-premises -versiolle

Sovelluksen asentaminen käytettäessä Business Centralin on-premises -versiota on periaatteessa sama kuin yllä kuvatulla tavalla. Jos sinulla on vain yksi vuokraaja, avaa vain Business Central selaimessasi ja valitse sitten joko ![kuvake sovelluksen asentamiseen Edgessä.](media/ui-edge-install-app-icon.png) **Sovellus saatavilla. Asenna Business Central** tai ![Kuvake sovelluksen asentamiseen Chromessa.](media/ui-chrome-install-app-icon.png) **Asenna Business Central** yllä kuvatulla tavalla. 

Eroa on silloin, kun sinulla on useampia vuokraajia. Toisin kuin [!INCLUDE[prod_short](includes/prod_short.md)] onlinessa, jossa voit asentaa sovelluksen erikseen eri ympäristöjä varten, on-premises-versiossa voit asentaa sovelluksen vain yhdelle vuokralaiselle. Joten ennen kuin asennat sovelluksen, kun sinulla on useampia vuokraajia, muista vaihtaa oikea vuokraaja. Kun sovellus on asennettu ja se avataan, se avaa vuokraajan suoraan.

<!-- for FAQ or troubleshooting
> [!NOTE]
> To install the app, [!INCLUDE[prod_short](includes/prod_short.md)] must be configured for HTTPS. If it isn't, you won't see ![Icon for installing an app in Edge.](media/ui-edge-install-app-icon.png) **App available. Install Business Central** or ![Icon for installing an app in Chrome.](media/ui-chrome-install-app-icon.png) **Install Business Central** in the browser. If you're having problems, contact your administrator or see [Configuring SSL to Secure the Business Central Web Client Connection](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection) about how to configure HTTPS.
-->

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on [Microsoft Learnissa](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Mobiilisovellukset – usein kysytyt kysymykset](ui-mobile-faq.yml)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]