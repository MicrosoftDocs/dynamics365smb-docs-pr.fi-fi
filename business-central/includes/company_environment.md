---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: fa7e5a51696c149e66da0d76cf1042c5e8f7e7e3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776394"
---
Käyttäjät tukevat joskus useita yrityksiä, ja heidän on voitava voi siirtyä nopeasti yrityksestä toiseen [!INCLUDE [prod_short](prod_short.md)]issa. Yrityksellä voi esimerkiksi olla myyntitoimistoja kaupungeissa ja useissa maissa, joten se on luonut erillisen liiketoimintayksikön kullekin toimistolle. Samassa maassa olevat toimistot määritetään erillisinä yrityksinä jaetussa ympäristössä. Muut toimistot luodaan yrityksinä erillisissä ympäristöissä, koska ne sijaitsevat maantieteellisesti muissa maissa.<br><br>  

Mikä on ympäristö? [!INCLUDE[prod_short](prod_short.md)]in yritykset sijaitsevat *ympäristöissä*. Ympäristötyyppejä on kaksi: **tuotanto** ja **eristys**. Lyhyesti sanottuna tuotantoympäristöt sisältävät live-liiketoimintatietoja, kun taas eristysympäristöt ovat turvallinen tapa kokeilla esimerkiksi uusia liiketoimintaprosesseja tai ominaisuuksia. Lisätietoja on kohdassa [Ympäristötyypit](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments). Jos sinulla on yrityksen käyttöoikeus, sinulla on myös sen ympäristön käyttöoikeus, jossa yritys sijaitsee. Jos sinulla on usean yrityksen käyttöoikeus ja kyseiset yritykset ovat eri ympäristöissä, sinun on määritettävä ympäristö, jota haluat käyttää, kun kirjaudut [!INCLUDE[prod_short](prod_short.md)]iin. Ympäristöt ovat maakohtaisia, joten jos organisaatio toimii useissa maissa, kullakin maalla on oltava erillinen ympäristö.<br><br>  

Mikä on yritys? *Yritys* on räänlainen säilö, joka säilyttää yritystä koskevia tietoja. Edellistä esimerkkiä mukaillen yrityksellä on yksi myyntitoimisto Seattlessa ja toinen New Yorkissa, joten se luo [!INCLUDE[prod_short](prod_short.md)]issa yrityksen kummallekin toimistolle, jotta se voi hallita kummankin toimiston toimintoja erillään.  
