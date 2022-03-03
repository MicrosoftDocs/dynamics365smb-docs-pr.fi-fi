---
title: 'Vian etsintä: kameran ja sijainnin käyttäminen'
description: Tässä artikkelissa kuvataan, miten voidaan tehdä vianmääritys kameran ja sijaintitietojen käyttämiseen Business Centralin avulla.
author: blrobl
ms.author: t-blrobl
ms.date: 04/01/2021
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
ms.openlocfilehash: c484be64a252ae8f565bf04215b9a2191e572875
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8138204"
---
# <a name="troubleshooting-accessing-camera-and-location"></a>Vian etsintä: kameran ja sijainnin käyttäminen

Saatat törmätä joihinkin ongelmiin, kun yrität käyttää laitteen kameraa ja sijaintitietoja kohteesta [!INCLUDE[prod_short](includes/prod_short.md)]. Löydät mahdolliset syyt näiden ongelmien takana ja voit kiertää ne alla olevien ohjeiden avulla.

## <a name="device-must-have-camera-and-location-capabilities"></a>Laitteessa on oltava kamera- ja sijaintiominaisuudet

Jotta voisit käyttää kameraa tai käyttäjän sijaintia laitteesta, laitteessa on oltava fyysinen kamera tai mahdollisuus hakea sijaintitietoja.

Jos laitteessa on kamera ja sijaintiominaisuudet, mutta ongelmia ilmenee edelleen, jotkin ohjaimet on ehkä päivitettävä tai asennettava uudelleen. Vaikka et olisikaan varma, suosittelemme aina, että päivität laitteesi käyttöjärjestelmän, ohjaimet ja selaimen uusimpaan versioon saadaksesi parhaan käyttökokemuksen.

## <a name="access-permissions-not-enabled"></a>Käyttöoikeuksia ei ole otettu käyttöön

Sinun on otettava käyttöön kameran ja sijainnin yleinen käyttöoikeus laitteesi tietosuoja-asetuksista ja annettava niille eksplisiittisesti käyttöoikeus kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)]. Jos haluat esimerkiksi tarkastella tai muuttaa Windowsissa suoritettavan laitteen käyttöoikeuksia, valitse **Asetukset**, valitse **Yksityisyys** ja valitse sitten **Sovelluksen käyttöoikeudet**. 

Mobiililaitteissa on annettava kameran ja sijainnin käyttöoikeudet [!INCLUDE[prod_short](includes/prod_short.md)] -mobiilisovellukselle. Voit tehdä tämän iOS-laitteessa siirtymällä kohtaan **Asetukset**, valitsemalla **Yksityisyys** ja sitten **Kamera** tai **Sijainti**. Jos kyseessä on Android-laite, siirry kohtaan **Asetukset**, valitse **Sovellukset & ilmoitukset**, **Lisäasetukset**, **Käyttöoikeuksien hallinta** ja sitten **Kamera** tai **Sijainti**.

Lisäksi jos käytät [!INCLUDE[prod_short](includes/prod_short.md)] -sivustoa selaimessa, sinun täytyy myös myöntää [!INCLUDE[prod_short](includes/prod_short.md)] -sivustolle oikeus käyttää kameraa tai sijaintitietojasi. Jos haluat tarkastella tai muuttaa sivustojen käyttö oikeuksia Microsoft Edge -selaimessa, mene kohtaan **Asetukset**, valitse **Sivustojen käyttöoikeudet** ja valitse sitten **Kamera** tai **Sijainti**. Huomaa, että tämä voi olla erilainen muissa selaimissa.

Oletusarvon mukaan laite tai selain näyttää pyynnön käyttää näitä ominaisuuksia, kun käyttäjä aktivoi ne ensimmäisen kerran.

> [!NOTE]  
> Jotkin vanhat selaimet eivät salli kameran ja sijainnin käyttöä. Kamera ei ole käytettävissä esimerkiksi Internet Explorerissa tai vanhassa Edge-selaimessa.

## <a name="web-client-connection-not-secure"></a>WWW-asiakasohjelman yhteys ei ole suojattu

Kamera- ja sijaintiominaisuudet ovat käytettävissä vain, kun WWW-asiakasohjelmaa käytetään SSL-suojattujen HTTP-yhteyksien avulla `https://`-URI-mallin avulla. 

Ainoa poikkeus on yhteyden muodostus kohteeseen `http://localhost`, jota käytetään kehitys- ja testitarkoituksiin.


## <a name="working-with-virtualization-technologies"></a>Virtualisointitekniikoiden käyttäminen

Kun muodostat yhteyden kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)] etätyöpöydän tai muun virtualisoinnin kautta, kameran tai sijainnin käyttö ei välttämättä ole käytettävissä. Käytä tässä tapauksessa fyysistä järjestelmää sen sijaan.

## <a name="antivirus-software"></a>Virustentorjuntaohjelmisto
Jotkin virustentorjuntaohjelmat estävät oletusarvoisesti kameran ja sijainnin käytön. Muista tarkistaa virustentorjuntaohjelman asetukset.

## <a name="see-also"></a>Katso myös
[Kameran käyttöönotto AL:ssä](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[Sijainnin käyttöönotto AL:ssä](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)


[!INCLUDE[footer-include](includes/footer-banner.md)]