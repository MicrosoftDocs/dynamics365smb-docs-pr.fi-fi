---
title: Business Centralin asentaminen työpöydälle
description: 'Tässä artikkelissa kuvataan, miten Business Central -sovellus saadaan Windows-tai MACiOS-työpöydälle.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'phone, tablet'
ms.date: 01/11/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Business Central -työpöytäsovelluksen hankkiminen

Jos sinulla on Windows (PC)- tai macOS-tietokone, voit asentaa Business Central -sovelluksen työpöydälle. Sovellus toimii Business Central Onlinessa ja paikallisesti.

## Miksi käyttää sovellusta?

Business Central -sovellus muistuttaa verkkoasiakasta, mutta siinä on muutamia etuja, kuten:

- Sovellus on helposti saatavilla **Käynnistä**-valikosta, voit helposti kiinnittää sen tehtäväpalkkiin, tai se käynnistetään oletusarvoisesti, kun käynnistät tietokoneen.
- Yleensä sovellus on myös nopeampi ja sujuvampi hahmontaa ruudulla, ilman suorituskykyeroja, verrattuna [!INCLUDE[prod_short](includes/prod_short.md)]in käyttämiseen selaimessa.
- Sovellus avautuu omassa ikkunassaan kaikista selainikkunoista riippumatta. Tämän ominaisuuden ansiosta se on helpompi löytää, jos käytössä on monia sovelluksia tai selaimen välilehtiä.
- Jos käytössäsi on enemmän kuin yksi Business Central -ympäristö (vain online), voit asentaa sovelluksen erikseen kutakin ympäristöä varten.

     Kun avaat sovelluksen tiettyä ympäristöä varten, ympäristön nimi sisältyy ikkunan otsikkoon. Kun työskentelet useissa [!INCLUDE[prod_short](includes/prod_short.md)] -ympäristöissä, jokainen sovellusikkuna näytetään erikseen. Nimi helpottaa sinua näkemään, mikä ikkuna kuhunkin ympäristöön liittyy.

## Sovelluksen asentaminen Business Central Onlinea varten

Business Central Onlinen sovelluksen voi asentaa kahdella tavalla. Voit asentaa sen suoraan selaimesta tai Microsoft Storesta. Sovellus on kummassakin tapauksessa sama. Erona on se, että asentaminen selaimesta mahdollistaa sovelluksen asentamisen jokaiseen ympäristöön, kun ympäristöjä on enemmän kuin yksi.

### Microsoft Storesta

1. Siirry [Microsoft Storeen](https://go.microsoft.com/fwlink/?linkid=2182870).
2. Valitse **Hanki** > **Asenna**. 
3. Kun sovellus on asennettu, valitse **Avaa** ja kirjaudu Business Centraliin.

Kun seuraavan kerran haluat avata sovelluksen, etsi se **Käynnistä**-valikosta.

### Selaimesta

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

## Sovelluksen asentaminen paikallista Business Centralia varten

Käytettäessä Business Centralia paikallisesti työpöytäsovellus asennetaan suoraan selaimesta, kuten [edellä kuvataan](#from-the-browser). Jos sinulla on vain yksi vuokraaja, avaa vain Business Central selaimessasi ja valitse sitten joko ![kuvake sovelluksen asentamiseen Edgessä.](media/ui-edge-install-app-icon.png) **Sovellus saatavilla. Asenna Business Central** tai ![Kuvake sovelluksen asentamiseen Chromessa.](media/ui-chrome-install-app-icon.png) **Asenna Business Central** yllä kuvatulla tavalla.

Eroa on silloin, kun sinulla on useampia vuokraajia. Toisin kuin [!INCLUDE[prod_short](includes/prod_short.md)] onlinessa, jossa voit asentaa sovelluksen eri ympäristöjä varten, voit asentaa sovelluksen vain yhdelle vuokralaiselle. Joten ennen kuin asennat sovelluksen, kun sinulla on useampia vuokraajia, muista vaihtaa oikea vuokraaja. Kun sovellus on asennettu ja se avataan, se avaa vuokraajan suoraan.

> [!IMPORTANT]
> Jos käytät Business Centralin vuoden 2021 julkaisuaaltoa 1 (versio 18) tai sitä vanhempaa versiota, et voi asentaa sovellusta tässä artikkelissa kuvatulla tavalla. Asenna sen sijaan sovellus [Microsoft Storesta ](https://go.microsoft.com/fwlink/?LinkId=734848). Lisätietoja ja ohjeita tämän vanhan sovelluksen asentamisesta: [Business Central -sovelluksen valmistelu ja asennus](/dynamics365/business-central/dev-itpro/deployment/install-business-central-app).

## Katso myös

[Mobiilisovellusten usein kysytyt kysymykset](ui-mobile-faq.yml)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
