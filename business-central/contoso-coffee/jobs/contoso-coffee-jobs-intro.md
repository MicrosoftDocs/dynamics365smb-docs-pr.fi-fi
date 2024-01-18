---
title: Johdatus Contoso Coffeeen projektinhallintaan
description: Tässä artikkelissa esitellään Consoso Coffee -esimerkkitietoja töiden ja projektinhallinnan osalta.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# Johdatus Contoso Coffeeen töihin ja projektinhallintaan

Contoso Coffee on kuvitteellinen yritys, joka tuottaa kuluttajille ja yrityksille kahvinkeittimiä. **Contoso Coffee** -sovellukset Business Centralille lisäävät demotietoja, joiden avulla voit opetella käyttämään työ- ja projektinhallintaominaisuuksia Business Centralissa.

Tässä sovelluksessa on useita elementtejä, joita käytetään pääkuvauksissa:

- Resurssit määritetyillä osaamisalueilla ja vyöhykkeillä
- Nimikkeet, jotka on määritetty huoltonimikkeiden luomista varten

> [!IMPORTANT]
> Ennen kuin suoritat mitään Contoso Coffeen skenaarioista, kirjaa kaikki nimikepäiväkirja rivit, joilla on alkusaldot. Lisätietoja vaatimuksista on [Contoso Coffee -tietojen määrittäminen](#set-up-contoso-coffee-jobs-and-project-management-data) -osiossa.
>
> 
## Määritä Contoso Coffeeen töiden ja projektinhallinnan tiedot

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Kun asianmukaiset sovellukset on asennettu, siirry [Contoso Coffeen töiden esittelytiedot](https://businesscentral.dynamics.com/?page=4767) -sivulle [!INCLUDE [prod_short](../../includes/prod_short.md)] ja muuta oletusasetuksia tarpeidesi mukaan. Asetukset kuvaillaan seuraavissa taulukoissa:  

|Kenttä  |Kuvaus  |
|---------|---------|
|**Aloitusvuosi** |Määrittää ensimmäisen vuoden, jota haluat käyttää Contoso Coffee -demotiedoissa. Yrityksen asetuksista riippuen vuosi on joko kalenterivuosi tai tilikausi.|
|**Asiakasnro**  |Asiakas, jota käytetään myyntitoimintojen skenaarioissa.|
|**Nimikkeen 1 nro**  |Sopimusskenaarioissa käytettävä nimike.|
|**Nimikkeen 2 nro**  |Laitteistoviat kattavien sopimusten skenaarioissa käytettävä nimike.|
|**Paikallisen resurssin 1 nro**  |Sopimusskenaarioissa käytettävä resurssi.|
|**Etäresurssin 1 nro**  |Laitteistoviat kattavien sopimusten skenaarioissa käytettävä resurssi.|
|**Asiakkaan kirjausryhmä**|Määrittää liiketoimintakoodin kotimaan asiakkaille. Liiketoimintakoodeja käytetään, kun tapahtumia kirjataan. |
|**Asiakkaan yleinen liiketoiminnan kirjausryhmä**|Määrittää liiketoimintakoodin kotimaan asiakkaille. Liiketoimintakoodeja käytetään, kun tapahtumia kirjataan. |
|**Kotimaa – Yleinen liiketoiminnan kirjausryhmä**|Määrittää liiketoimintakoodin kotimaan asiakkaille ja toimittajille. Liiketoimintakoodeja käytetään, kun tapahtumia kirjataan. |
|**Jälleenmyynti – Varaston kirjausryhmä**    |Määrittää koodin nimikkeille, joita tulee käyttää kirjattaessa uudelleenmyyntiä.|
|**Vähittäismyynti – Tuotteen yleinen kirjausryhmä**    |Määrittää koodin nimikkeille, joita tulee käyttää kirjattaessa vähittäismyyntiä.|
|**Tuotteen ALV-kirjausryhmä**    |Määrittää tuotteen ALV-koodin nimikkeille ALV:n kirjaamista varten, jos ALV on käytössä.|
|**Hintakerroin**     |Määrittää kertoimen, jolla hinta muunnetaan USD/EUR-valuutasta paikalliseksi valuutaksi. *1* tarkoittaa, että hinta on sama summa kaikissa valuutoissa. Korkeampaa numeroa käytetään, kun hinta saadaan paikallisena valuuttana. |
|**Pyöristystarkkuus**  |Määrittää, miten lasketun kulutuksen määrät pyöristetään, kun ne syötetään kulutuspäiväkirjan riveille. Määrät, jotka ovat pienempiä kuin 0,5, pyöristetään alaspäin. Määriä, jotka ovat yhtä suuria tai suurempia kuin 0,5, pyöristetään ylöspäin.|

Kun olet valmis, valitse **Luo demotiedot** -toiminto. Tietojen lisääminen pohjana olevaan tietokantaan kestää muutaman minuutin, mutta sitten olet valmis suorittamaan erilaisia skenaarioita.  

## Katso myös
