---
title: 'Markkinointitekstiehdotukset, joissa on Copilot-yleiskatsaus'
description: Hanki yleiskuva Business Centralin tekoälypohjaisista sisällönluontiominaisuuksista.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: overview
ms.date: 10/29/2023
ms.custom: bap-template
---
# <a name="marketing-text-suggestions-with-copilot-overview"></a>Markkinointitekstiehdotukset, joissa on Copilot-yleiskatsaus

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

Tässä artikkelissa esitellään Business Centralin Copilot-palvelun tarjoamasta tekoälypohjaisesta ominaisuudesta.

## <a name="what-is-ai-powered-item-marketing-text-with-copilot"></a>Mikä on nimikkeen tekoälypohjainen markkinointiteksti ja Copilot

Copilot tarjoaa tekoälypohjaista kirjoitusapua Business Centralin käyttäjille, jotka vastaavat markkinointitekstien (tuotekuvausten) luomisesta verkkokaupoissa, kuten Shopifyssa myytäviin tuotteisiin. Copilot luo napin painalluksella tekstiä, joka on houkuttelevaa ja luovaa, ja korostaa tietyn nimikkeen keskeisiä määritteitä. Kevyen tarkistuksen ja muokkauksen jälkeen se on valmis julkaistavaksi.

Copilot käyttää [Microsoft Azure OpenAI -palvelua](/azure/cognitive-services/openai/overview) kielimalleihin, jotka tunnistavat, ennustavat ja luovat koulutettuja tietojoukkoja koskevaa tekstiä.

<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RWZdAr]

*Video ei vastaa täysin sitä, miten ominaisuus tällä hetkellä toimii tai miltä se näyttää tuotteessa. Ominaisuus on muuttunut videon tuottamisen jälkeen. Mutta se antaa sinulle yleisen käsityksen ominaisuudesta ja siitä, mihin voit käyttää sitä.*
  
## <a name="where-its-used"></a>Käyttökohde

Copilot on saatavilla nimikekortteihin Business Centralissa. Business Centralin nimikkeet ovat kuin tuotteita muissa sovelluksissa ja kaupoissa. Kutakin nimikettä voi hallita kortilta, johon syötetään tietoja nimikkeestä, esimerkiksi sen dimensiot, kustannukset tai kuva. Tämä kortti sisältää myös ruudun markkinointitekstin syöttämistä varten. Tämä markkinointiteksti voidaan julkaista verkkokaupassamme kohteen mainostamiseksi. Tässä Copilot tulee mukaan. Jos valitset nimikekortissa **Luonnostele Copilotilla** -toiminnon, Copilot luo sinulle älykkään tekstiluonnoksen. Kun saat ensimmäisen luonnoksen, voit suorittaa Copilotin uudelleen ja uudelleen, kunnes saat sellaisen luonnoksen kuin haluat. Kun pidät ehdotuksesta, voit tarkistaa ja muokata sen tietoja ja tallentaa sen.

Jos Business Central on määritetty muodostamaan yhteys Shopifyn online-myymälään, voit viedä tätä tekstiä vielä pidemmälle julkaisemalla sen nimikkeen kanssa suoraan myymälääsi valitsemalla **Lisää Shopifyhin**.

## <a name="why-and-how-to-use-it"></a>Miksi sitä käytetään ja miten

Tekoälypohjaisen tekstin avulla voit nopeuttaa online-kaupoissa olevien tuotteiden markkinoille pääsyä rajoittamalla tekstin luomiseen käytettyä työaikaa. Tärkeimpiin etuihin kuuluu:

- Auttaa käyttäjiä voittamaan tyhjän sivun kammon saamalla heidät alkuun älykkään luonnoksen avulla.
- Avaa luovuuden ja tarjoaa kiinnostavamman tuotekuvauksen.
- Parantaa tuoteryhmien markkinointisisällön yhdenmukaisuutta.

Tekoälypohjainen teksti kannattaa ottaa huomioon *vain ehdotuksena*. Ehdotukset voivat joissakin tapauksissa sisältää virheitä ja jopa sopimatonta tekstiä, joten ihmisten valvontaa ja tarkistamista tarvitaan. Ennen kuin julkaiset tekstin, sinun täytyy tarkistaa, että sen tiedot virheettömiä, ja tehdä tarvittavat muutokset.

## <a name="current-limitations"></a>Nykyiset rajoitukset

Tässä osassa selitetään Copilotin tarjoamien tekoälypohjaisten tekstiominaisuuksien rajoitukset.

- [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]
- Huonot ehdotukset voivat johtaa siihen, että käytetään epämääräisiä tai geneerisiä tuotenimiä ja että nimikkeestä puuttuu tietoja, kuten päämääritteet tai luokka.
- Copilot tukee vain Business Central Onlinea; ei yksityisiä pilviympäristöjä tai paikallisia Business Central -ympäristöjä.
- Copilot-palvelua ei tueta Azure-tilauksessasi oman Azure OpenAI -palveluresurssin yhteyksien kautta.

<!-- Partner extensibility of the AI capability by using AL code isn't supported.-->

## <a name="next-steps"></a>Seuraavat vaiheet

Päästäksesi alkuun tarvitset Business Central (v23.1 ja myöhempi) -ympäristön, joka on otettu käyttöön Copilot-toiminnon avulla.

- Jos olet aiemmin luotu Business Central -asiakas, Business Central -järjestelmänvalvojan on määritettävä ympäristö, jossa on otettu käyttöön markkinontitekstit. Lisätietoja on [Copilotinn ja tekoälyn ominaisuuksien määrittämisessä](enable-ai.md).

- Jos et ole Business Central -asiakas, mutta haluat kokeilla sitä, voit rekisteröityä maksuttoman kokeiluversion käyttäjäksi. Lisätietoja kohdassa [Rekisteröidy maksutonta Dynamics 365 Business Central -kokeilua varten](trial-signup.md).

Kun ympäristö tai jäljitys on valmis, siirry kohtaan [Markkinointitekstin lisääminen nimikkeisiin Copilotin avulla](item-marketing-text.md).  

## <a name="see-also"></a>Katso myös

[Copilot- ja tekoälyominaisuuksien määrittäminen](enable-ai.md)  
[Lisää markkinointiteksti nimikkeille Copilotin avulla](item-marketing-text.md)  
[Markkinointitekstiehdotusten usein kysytyt kysymykset](faqs-marketing-text.md)  
[Shopify-yhdistimen käytön aloittaminen](shopify/get-started.md)  
