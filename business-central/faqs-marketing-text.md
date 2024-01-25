---
title: Markkinointitekstiehdotusten usein kysytyt kysymykset
description: 'Usein kysytyt kysymykset sisältävät tietoja Business Centralin käyttämästä tekoälyteknologiasta sekä tärkeitä huomioita tekoälyn käyttämisestä, sen testaamisesta ja arvioimisesta sekä mahdollisista erityisistä rajoituksista.'
ms.date: 10/07/2023
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.collection:
  - bap-ai-copilot
---

# Copilotin avulla luotujen markkinointitekstiehdotusten UKK

Nämä usein kysytyt kysymykset (UKK) kuvaavat tekoälyn vaikutusta [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] -ominaisuuteen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa.

## Mitä ovat kohteen markkinointitekstiehdotukset?

Copilotin tarjoaa kirjoitusapua käyttäjille, jotka vastaavat markkinointitekstin (eli copyn) kirjoittamisesta nimikkeissä [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa. Tätä ominaisuutta kutsutaan nimellä [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]. [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] -ominaisuus tarjoaa kirjoitusapua käyttäjille, jotka vastaavat markkinointitekstin (eli *copyn*) kirjoittamisesta nimikkeissä [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa.

Ominaisuus on käytettävissä missä tahansa nimikkeen kortissa [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa. Voit käyttää sitä avaamalla nimikkeen ja valitsemalla sitten **Markkinointiteksti** > **Tee luonnos Copilotin** avulla. Tämä toiminto luo automaattisesti tekstiehdotuksen, joka on mukaansatempaava, luova ja spesifi näytettävälle nimikkeelle. Ehdotukset perustuvat erilaisiin syötteisiin, esimerkiksi:

- Nimikkeen määritteet, luokka ja nimi.
- Henkilökohtaiset kirjoitustyyliasetukset, kuten äänen sävy, korostettu laatu, muoto ja pituus.

Voit muuttaa näiden syötevaihtoehtojen arvoa vaikuttaaksesi tekoälyn luoman tekstin lopputulokseen. Ennen ehdotuksen tallentamista voit tarkastaa ja muokata ehdotusta helposti tai kokeilla muuta ehdotusta.

Tämän ominaisuuden keskeisiä etuja ovat seuraavat:

- Vähentää tekstin kirjoittamiseen käytettyä aikaa, mikä voi nopeuttaa verkkokaupoissa myytävien tuotteiden markkinoille tuloa.
- Avaa luovuuden ja tarjoaa kiinnostavamman tuotekuvauksen.
- Parantaa tuoteryhmien markkinointimateriaalin yhdenmukaisuutta.

## Mitkä ovat järjestelmän toiminnot?

[!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] -ominaisuus käyttää [Microsoft Azure OpenAI Serviceä](/azure/cognitive-services/openai/overview) käyttääkseen tehokkaita kielimalleja, jotka analysoivat ja luovat luonnollista kieltä. Nämä mallit on koulutettu laajoilla tekstikokonaisuuksilla. Tämän seurauksena Copilot voi luoda ehdotettuja, henkilökohtaisia vastauksia englanniksi. Ne perustuvat vähimmäismäärään syötettyä tietoa, kuten kohteen määritteitä, luokkaa tai kuvausta. 

## Mitä järjestelmän on tarkoitus käyttää?

Tämän ominaisuuden tarkoituksena on auttaa käyttäjiä luomaan markkinointitekstiä nimikkeille [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa. Kirjoittajat käyttävät ominaisuutta saadakseen nopeasti pakottavia ja kiinnostavia tekstiehdotuksia, joita sitten tarkistetaan ja muokataan oikeellisuuden varmistamiseksi. 

## Miten nimikkeen markkinointiteksti on arvioitu? Mitä mittareita suorituskyvyn mittaamiseen käytetään?

- Ominaisuus kävi läpi laajan testauksen, jossa kieliasiantuntijat arvioivat lukuisia eri kielillä käytettäviä tekstejä eri kriteerien perusteella. Testaus perustui [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman esimerkkitietoihin ja muihin kuvitteellisiin tuotekatalogeihin.
- Tämä ominaisuus on rakennettu Microsoftin Vastuullinen tekoäly -standardin mukaisesti. [Lisätietoja Microsoftin vastuullisesta tekoälystä](https://aka.ms/RAI).

## Miten Microsoft seuraa luodun sisällön laatua?

Microsoftilla on käytössään useita järjestelmiä, joiden avulla varmistetaan, että Copilot-ominaisuudet pysyvät toiminnassa ja ne luovat mahdollisimman laadukasta sisältöä.

- Käyttäjillä on mahdollisuus antaa palautetta, kun he voivat raportoida epäasiallisesta sisällöstä ja parantaa toimintoja.

  - Jos kohtaat sopimatonta sisältöä, ilmoita siitä Microsoftille käyttämällä tätä palautelomaketta: [Ilmoita väärinkäytöstä](https://go.microsoft.com/fwlink/?linkid=2249810). 

    Microsoft voi poistaa Copilotiin liittyvät toiminnot käytöstä valittujen asiakkaiden osalta, jos toimintojen väärinkäyttö havaitaan. 

  - Seuraamme [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] -ohjelman käyttäjäpalautetta, jonka avulla voimme parantaa ehdotuksia. 

    Käyttäjä antaa palautetta käyttämällä [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman **Copilot**-sivulla vastaavaa (peukalo ylös) tai ei pidä (peukalot alaspäin) -kuvaketta. Keräämme näiden eleiden telemetrian jokaiselle tekoälytuotokselle, josta lähetät palautetta.

    ![Näyttää nimikkeen kortin, jossa on markkinointitekstiruutu](media/create-with-copilot-window-feedback.svg)

- Azure OpenAI -palvelu tallentaa kehotteet ja täydennykset palvelusta valvomaan väärinkäyttöä sekä kehittämään ja parantamaan Azure OpenAI:n sisällön hallintajärjestelmien laatua. [Lisätietoja sisällönhallinnasta ja suodattamisesta.](/azure/cognitive-services/openai/concepts/content-filter). Yrityksen tietoja ei käytetä tekoälymallien kouluttamiseen Azure OpenAI Servicessä.

   Valtuutetut Microsoft-työntekijät voivat käyttää kehote- ja valmistumistietojasi, jotka ovat käynnistäneet automatisoidut järjestelmämme mahdollisten väärinkäytösten tutkintaa ja todentamista varten. Asiakkaille, jotka käyttävät [!INCLUDE[prod_short](includes/prod_short.md)] -palvelua Euroopan unionissa, valtuutetut Microsoft-työntekijät sijaitsevat Euroopan unionissa. Näitä tietoja voidaan käyttää sisällönhallintajärjestelmien parantamiseen. Jos kyseessä on vahvistettu käytäntörikkomus, saatamme pyytää sinua ryhtymään välittömiin toimiin ongelman kunnostamisen ja väärinkäytösten estämiseksi. Ongelman laiminlyönti voi johtaa Azure OpenAI -resurssin käyttöoikeuden keskeyttämiseen tai lopettamiseen.

   Lisätietoja on kohdassa [Azure OpenAI -palvelun tiedot, tietosuoja ja tietoturva](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

## Onko olemassa lokiinkirjaus- ja ihmistarkistusprosessi osana Azure OpenAI Serviceä, ja jos on, voinko kieltäytyä?  

Osana Azure OpenAI Servicen tarjoamista Microsoft käsittelee ja varastoi palveluun lähetettyjä asiakastietoja sekä tulostussisältöä tarkkaillakseen ja estääkseen palvelun väärinkäyttöä tai haitallisia käyttötarkoituksia tai tuotoksia; ja kehittääkseen, testatakseen ja parantaakseen valmiuksia, joiden avulla estetään palvelun väärinkäyttö ja/tai haitalliset tuotokset. 

Valtuutettu Microsoft-henkilöstö voi tarkastella tietoja, jotka ovat käynnistäneet automatisoidut järjestelmämme mahdollisten väärinkäytösten tutkimiseksi ja tarkistamiseksi, ja se voi käyttää rajoitettua satunnaisotantaa käsitteistä, joita automaattiset järjestelmämme eivät ole merkittyjä varmistaakseen, että järjestelmät toimivat oikein. Valtuutettu Microsoft-henkilöstö voi myös käyttää näitä tietoja parantaakseen järjestelmiämme, jotka valvovat palvelun väärinkäyttöä tai haitallisia käyttötarkoituksia tai tuotoksia. Lue lisää kohdasta [esiversion ehdot](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

Jotta Microsoft suojasi huollon ja sen asiakkaat, lokiin kirjaamista ja tarkastelemista koskevia prosesseja ei voi kieltää.

## Mitä tietoja ominaisuus kerää? Miten tietoja käytetään?

Markkinointitekstiehdotusten ominaisuus kerää Business Centralin minimitiedot palvelun tarjoamiseksi. Lisätietoja on kohdassa [Dynamics 365:n käyttöehdot Azure OpenAI -pohjaisille ominaisuuksille](https://go.microsoft.com/fwlink/?linkid=2236010).

Ominaisuus kerää tietoja myös palautekäyttäjiltä, jotka voivat käyttää **Copilot**-sivun yläosassa olevia tykkään (peukalo ylös)- tai en tykkää (peukalo alas) -kuvakkeita. Tiedot ovat anonyymejä ja sisältävät valinnan tykkää tai ei tykkää, ei-tykkäämisen syyn, jos se on annettu, ja Copilot-ominaisuuden, jota palaute koskee. Käytämme näitä tietoja ominaisuuden laadun arviointiin ja parantamiseen.

## Mitkä ovat [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] -ohjelman rajoitukset? Miten käyttäjät voivat minimoida [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] -ohjelman rajoitukset, kun he käyttävät järjestelmää?

- Koska ominaisuuden taustalla oleva teknologia käyttää tekoälyä, joka on koulutettu monenlaisilla lähteillä, tuotettu sisältö ei aina ole tosiasiallista tai sopivaa. Joihinkin ehdotuksiin voi sisältyä jopa kyseenalaista tai sopimatonta sisältöä. On sinun vastuullasi tarkistaa ja muokata luotuja ehdotuksia varmistaaksesi, että se on oikea ja sopiva.
- [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

  Epätarkkoja vastauksia saatetaan palauttaa, kun käyttäjät ovat vuorovaikutuksessa järjestelmän kanssa muilla kuin tuetuilla kielillä. Myös virheellinen teksti voi syntyä, kun käyttäjän kieli ja tietokannan perustietokieli [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa eivät ole samoja.


## Mitkä operatiiviset tekijät ja asetukset mahdollistavat järjestelmän tehokkaan ja vastuullisen käytön?

On olemassa muutamia asioita, joita voit tehdä, jotta saat kaiken irti ominaisuudesta:

- Lisää määritteitä nimikkeeseen, jos haluat mainostaa tiettyjä toimintoja ja ominaisuuksia, joita olet kiinnostunut.
- Muuta vaihtoehtoja äänensävyn ja painopisteen laadun osalta vastaamaan henkilökohtaisia mieltymyksiä.
- Paranna nimikkeen kuvausta.
- Varmista, että nimikkeelle on määritetty sopivin luokka.

Lisätietoja on ohjeaiheessa [Tekstiehdotusten parantaminen ja mukauttaminen](item-marketing-text.md#improve-and-tailor-text-suggestions).

> [!TIP]
> Tarkista aina tarkkuusehdotukset, ennen kuin tallennat ne ja julkaiset ne yleiseen käyttöön.


## Katso myös

- [Markkinointitekstiehdotukset](ai-overview.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]