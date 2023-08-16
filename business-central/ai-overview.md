---
title: Tekoälypohjainen tuotteen markkinointiteksti (esiversio) Copilotin avulla -yleiskatsaus
description: Hanki yleiskuva Business Centralin tekoälypohjaisista sisällönluontiominaisuuksista.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: overview
ms.date: 03/16/2023
ms.custom: bap-template
---
# Tekoälypohjainen tuotteen markkinointiteksti (esiversio) Copilotin avulla -yleiskatsaus

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Tässä artikkelissa esitellään Business Centralin Copilot-palvelun tarjoamasta tekoälypohjaisesta ominaisuudesta.

## Mikä on nimikkeen tekoälypohjainen markkinointiteksti ja Copilot

Copilot tarjoaa tekoälypohjaista kirjoitusapua Business Centralin käyttäjille, jotka vastaavat markkinointitekstien (tuotekuvausten) luomisesta verkkokaupoissa, kuten Shopifyssa myytäviin tuotteisiin. Copilot luo napin painalluksella tekstiä, joka on houkuttelevaa ja luovaa, ja korostaa tietyn nimikkeen keskeisiä määritteitä. Kevyen tarkistuksen ja muokkauksen jälkeen se on valmis julkaistavaksi.

Copilot käyttää [Microsoft Azure OpenAI -palvelua](/azure/cognitive-services/openai/overview) kielimalleihin, jotka tunnistavat, ennustavat ja luovat koulutettuja tietojoukkoja koskevaa tekstiä.

<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RWZdAr]

*Video ei vastaa täysin sitä, miten ominaisuus tällä hetkellä toimii tai miltä se näyttää tuotteessa. Ominaisuus on muuttunut hieman videon tuottamisen jälkeen. Mutta se antaa sinulle yleisen käsityksen ominaisuudesta ja siitä, mihin voit käyttää sitä*.
  
## Käyttökohde

Copilot on saatavilla nimikekortteihin Business Centralissa. Business Centralin nimikkeet ovat kuin tuotteita muissa sovelluksissa ja kaupoissa. Kutakin nimikettä voi hallita kortilta, johon syötetään tietoja nimikkeestä, esimerkiksi sen dimensiot, kustannukset tai kuva. Tämä kortti sisältää myös ruudun markkinointitekstin syöttämistä varten. Tämä markkinointiteksti voidaan julkaista verkkokaupassamme kohteen mainostamiseksi. Tässä Copilot tulee mukaan. Jos valitset nimikekortissa **Luo Copilotilla** -toiminnon, Copilot luo sinulle älykkään tekstiluonnoksen. Kun saat ensimmäisen luonnoksen, voit suorittaa Copilotin uudelleen ja uudelleen, kunnes saat sellaisen luonnoksen kuin haluat. Kun pidät ehdotuksesta, voit tarkistaa ja muokata sen tietoja ja tallentaa sen.

Jos Business Central on määritetty muodostamaan yhteys Shopifyn online-myymälään, voit viedä tätä tekstiä vielä pidemmälle julkaisemalla sen nimikkeen kanssa suoraan myymälääsi valitsemalla **Lisää Shopifyhin**.

## Miksi sitä käytetään ja miten

Tekoälypohjaisen tekstin avulla voit nopeuttaa online-kaupoissa olevien tuotteiden markkinoille pääsyä rajoittamalla tekstin luomiseen käytettyä työaikaa. Tärkeimpiin etuihin kuuluu:

- Auttaa käyttäjiä voittamaan tyhjän sivun kammon saamalla heidät alkuun älykkään luonnoksen avulla.
- Avaa luovuuden ja tarjoaa kiinnostavamman tuotekuvauksen.
- Parantaa tuoteryhmien markkinointisisällön yhdenmukaisuutta.

Tekoälypohjainen teksti kannattaa ottaa huomioon **vain ehdotuksena**. Ehdotukset voivat joissakin tapauksissa sisältää virheitä ja jopa sopimatonta tekstiä, joten ihmisten valvontaa ja tarkistamista tarvitaan. Ennen kuin julkaiset tekstin, sinun täytyy tarkistaa, että sen tiedot virheettömiä, ja tehdä tarvittavat muutokset.

## Nykyiset rajoitukset

Tässä osassa selitetään Copilotin tarjoamien tekoälypohjaisten tekstiominaisuuksien rajoitukset.

- Tekoälypohjaiset tekstiehdotukset ovat vain englanninkielisiä.
- Huonot ehdotukset voivat johtaa siihen, että käytetään epämääräisiä tai geneerisiä tuotenimiä ja että nimikkeestä puuttuu tietoja, kuten päämääritteet tai luokka.
- Copilot tukee vain Business Central Onlinea; ei yksityisiä pilviympäristöjä tai paikallisia Business Central -ympäristöjä.
- Copilot-palvelua ei tueta Azure-tilauksessasi oman Azure OpenAI -palveluresurssin yhteyksien kautta.
- Tekoälyvalmiuksien kumppanilaajennettavuuden Al-koodia ei tueta.

## Seuraavat vaiheet

Päästäksesi alkuun tarvitset Business Central -version 22 ympäristön, joka on otettu käyttöön Copilot-toiminnon avulla.

- Jos olet aiemmin luotu Business Central -asiakas, Business Central -järjestelmänvalvojan on määritettävä version 22 ympäristö sinulle.
- Jos et ole Business Central -asiakas, mutta haluat kokeilla sitä, voit rekisteröityä maksuttoman kokeiluversion käyttäjäksi.

Lisätietoja on osoitteessa [Hanki Business Central -esiversio](ai-preview-getstarted.md).  

## Katso myös

[Nimikkeen tekoälypohjaisen markkinointitekstin määrittäminen järjestelmänvalvojana](enable-ai.md)  
[Luo markkinointiteksti Copilotin avulla](item-marketing-text.md)  
[Nimikkeen tekoälypohjainen markkinointiteksti Copilotin avulla - UKK](ai-faq.md)  
[Shopify-yhdistimen käytön aloittaminen](shopify/get-started.md)  
