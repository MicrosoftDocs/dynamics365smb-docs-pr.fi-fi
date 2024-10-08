---
author: brentholtorf
ms.topic: include
ms.date: 04/01/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
[!INCLUDE[prod_short](prod_short.md)] -käyttäjät voivat joskus tukea useampaa kuin yhtä osastoa tai aliorganisaatiota liiketoimintayksikön sisällä. Yrityksellä voi esimerkiksi olla myyntitoimistoja eri kaupungeissa useissa maissa ja useilla alueilla, joten se on luonut erillisen liiketoimintayksikön kullekin toimistolle. Samassa maassa tai samalla alueella olevat toimistot määritetään erillisinä *yrityksinä* jaetussa *ympäristössä*. Muut toimistot luodaan yrityksinä erillisissä ympäristöissä, koska ne sijaitsevat maantieteellisesti muissa maissa tai muilla alueilla.

- Mikä on yritys?

  *Yritys* on räänlainen säilö, joka säilyttää yritystä koskevia tietoja. Edellistä esimerkkiä mukaillen yrityksellä on yksi myyntitoimisto Seattlessa ja toinen New Yorkissa, joten se luo [!INCLUDE[prod_short](prod_short.md)]issa yrityksen kummallekin toimistolle, jotta se voi hallita kummankin toimiston toimintoja erillään.

- Mikä on ympäristö?

  [!INCLUDE[prod_short](prod_short.md)] Onlinen yritykset sijaitsevat *ympäristöissä*. Ympäristötyyppejä on kaksi: **tuotanto** ja **eristys**. Lyhyesti sanottuna tuotantoympäristöt sisältävät live-liiketoimintatietoja, kun taas eristysympäristöt ovat turvallinen tapa kokeilla esimerkiksi uusia liiketoimintaprosesseja tai ominaisuuksia. Lisätietoja on kohdassa [Ympäristötyypit](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments) (vain englanniksi). Jos sinulla on yrityksen käyttöoikeus, sinulla on myös sen ympäristön käyttöoikeus, jossa yritys sijaitsee. Jos sinulla on usean yrityksen käyttöoikeus ja kyseiset yritykset ovat eri ympäristöissä, sinun on määritettävä ympäristö, jota haluat käyttää, kun kirjaudut [!INCLUDE[prod_short](prod_short.md)]iin. Ympäristöt ovat maa- ja aluekohtaisia, joten jos organisaatio toimii useissa maissa tai useilla alueilla, kullakin maalla tai alueella on oltava erillinen ympäristö. Lisätietoja on kohdassa [Ympäristöt ja yritykset](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology#environments-and-companies) (vain englanniksi).
