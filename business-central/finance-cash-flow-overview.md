---
title: Kassavirran yleiskatsaus
description: Yleiskuvaus kassaviroista sisään ja kassavirroista ulos. Yleiskuvaus auttaa ennustamaan saatavaa ja maksettavaa rahaa.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'cash flow, money flow, expense and income, liquidity, cash receipts minus cash payments'
ms.search.form: '841, 849, 1818'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---

# Kassavirran yleiskatsaus

Tietoja siitä, että saapuvat ja lähtevät kassavirrat ovat avain onnistuneeseen liiketoimintaan. Kassavirran avulla voit helposti luoda lyhyen aikavälin ennusteen, joka ennustaa miten ja milloin voit odottaa vastaanottavasi ja maksavasi rahaa. On tärkeää tietää, että yritykselläsi on tarpeeksi rahaa velkojen ja kulujen maksuun niden erääntyessä.

## Kassavirran määritelmä

Termi *kassavirta* tarkoittaa tietyn ajanjakson aikana määritettyjä kassaanmaksuja, joista on vähennetty kassastamaksut. Se on arvio rahasummasta, jonka odotetaan siirtyvän yritykseen ja yrityksestä, ja se sisältää kaikki ennustetut tulot ja menot.

## Kassavirtojen käsittely

Seuraavassa kuvassa on yhteenveto siitä, miten voit käsitellä kassavirtaa.

![Kassavirta – yleistä.](media/finance_cash_flow_overview.png "Kassavirta – yleistä")

- Määritä kassavirtaennuste.  

- Saat kassavirtaennusteen lähteet seuraavilta alueilta:  

  - Pääkirjanpito – yrityksen käyttövarojen ja budjetoitujen tuottojen ja kulujen tiedot.  
  - Osto – Nykyisten ostovelkojen ja avointen ostotilausten ennustettujen varausten tiedot.  
  - Myynti – Nykyisten myyntien ja saamisten ja kaikkien myyntitilausten ennustettujen vastaanottojen tiedot.  
  - Palvelu – avoimien huoltotilausten tietoja.  
  - Käyttöomaisuus – tietoja käyttöomaisuuden suunnitellusta luovutuksesta ja budjetoiduista ostoista.  
  - Manuaaliset tuotot ja kulut – Hallitse manuaalisia tuottoja ja kuluja ja sisällytä se kassavirtaennusteeseen.  
- Siirrä seuraavien alueiden tietoja työkirjaan eräajon avulla: pääkirjanpito, ostaminen, myynti, huolto, käyttöomaisuus. Tee sitten kassavirtaennuste rekisteröimällä työkirjan rivit.  
- Käytä eri sivuja, raportteja ja kaavioita analysoidaksesi ja tulostaaksesi kassavirtaennusteen, joka liittyy saatavuuteen ja aikajanan yhteenvetoihin.  

## Kassavirtaennusteen tekeminen

Rekisteröityjen työkirjan riveihin perustuen voit tehdä säännöllisesti kassavirran ennusteen. Seuraavaa asettelua käytetään usein kassavirtaennusteessa. Asettelussa on kolme osaa:

- Kassaanmaksu  
- Kassasuoritukset  
- Nettokassavirta tai käteisvarat  

Kassaanmaksut tarjoavat tiedot yrityksen saamista tuloista.

*kassaanmaksut yhteensä* = *saatavat* + *avoimet myyntitilaukset* + *avoimet huoltotilaukset* + *käyttöomaisuuden luovutukset* + *manuaaliset tulot* + *budjetoidut tulot*

> [!NOTE]
> Manuaalisia tuottoja voivat olla vuokratuotto, rahoitussaatavien korko tai uusi yksityinen pääoma. Voit suunnitella manuaaliset tuotot ajanjaksolle ja käyttää niitä kassavirtaennusteen laskennassa.

Kassasuoritukset sisältävät tiedot yrityksen tekemistä maksuista.

*kassasuoritukset yhteensä* = *ostovelat* + *avoimet ostotilaukset* + *käyttöomaisuuden investoinnit* + *manuaaliset kulut* + *budjetoidut kulut*

> [!NOTE]
> Manuaalisia kuluja voivat olla esimerkiksi palkat, luoton korko ja yksityiset kulutukset. Voit suunnitella manuaaliset kulut ajanjaksolle ja käyttää niitä kassavirtaennusteen laskennassa.

Kassavirta tai käteisvarat lasketaan kunkin jakson lopussa vähentämällä maksujen yhteissumma kassasuoritusten yhteissummasta.

*nettokassavirta* = *kassaanmaksut yhteensä* – *kassasuoritukset yhteensä* + *käyttövarat*

Voit käyttää ennustetta sisäisen päätöksenteon työkaluna, jonka avulla voit suunnitella etukäteen ja tehdä yrityksen toiminnalle tärkeitä strategisia päätöksiä.

## Katso myös

[Kassavirta-analyysin määrittäminen](finance-setup-cash-flow-analyses.md)  
[Kassavirran analysoiminen](finance-analyze-cash-flow.md)  
[Kassavirran ennustaminen Dynamics 365 Business Centralissa](/training/modules/forecast-cash-flow-dynamics-365-business-central/index)  
[Määritä kassavirtaennusteet käyttämällä Azure AI:n määritystä Dynamics 365 Business Centralissa](/training/modules/setup-cash-flow-forecasts/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
