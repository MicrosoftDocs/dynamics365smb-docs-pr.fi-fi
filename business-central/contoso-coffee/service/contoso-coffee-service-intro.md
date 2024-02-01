---
title: Johdatus Contoso Coffee -palvelun hallintaan
description: Tässä artikkelissa esitellään Consoso Coffee -esimerkkitietoja huoltohallinnon osalta.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/27/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Johdatus Contoso Coffee -palvelun hallintaan

Contoso Coffee on kuvitteellinen yritys, joka tuottaa kuluttajille ja yrityksille kahvinkeittimiä. **Contoso Coffee** -sovellukset Business Centralille lisäävät demotietoja, joiden avulla voit opetella käyttämään huoltohallinnon ominaisuuksia Business Centralissa.

Tässä sovelluksessa on useita elementtejä, joita käytetään pääkuvauksissa:

- Resurssit määritetyillä osaamisalueilla
- Nimikkeet, jotka on määritetty huoltonimikkeiden luomista varten
- Lainatavaran nimikkeet

> [!IMPORTANT]
> Ennen kuin suoritat mitään Contoso Coffeen skenaarioista, kirjaa kaikki nimikepäiväkirja rivit, joilla on alkusaldot. Lisätietoja vaatimuksista on [Contoso Coffee -tietojen määrittäminen](#set-up-contoso-coffee-service-management-data) -osiossa.
>
> 
## Contoso Coffee -palvelun hallinnan tietojen määrittäminen

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Kun asianmukaiset sovellukset on asennettu, siirry [Contoson demotyökalu](https://businesscentral.dynamics.com/?page=5194) -sivulle kohteessa [!INCLUDE [prod_short](../../includes/prod_short.md)], valitse *Huoltomoduuli*-rivi ja valmistele moduulit käyttämällä **Määritä**-toimintoa. Asetukset kuvaillaan seuraavassa taulukossa:  

|Kenttä  |Kuvaus  |
|---------|---------|
|**Asiakasnro**  |Asiakas, jota käytetään myyntitoimintojen skenaarioissa.|
|**Toimittajanro**  |Toimittaja, jota käytetään kaikissa ostotoimintojen skenaarioissa.|
|**Nimikkeen 1 nro**  |Nimike, jota käytetään korjaus- ja kunnossapitoskenaarioissa.|
|**Huoltonimikkeen 1 nro**  |Huolto-tyyppinen nimike, jota käytetään korjausskenaariossa.|
|**Huoltonimikkeen 2 nro**  |Huolto-tyyppinen nimike, jota käytetään korjausskenaariossa.|
|**Paikallisen resurssin 1 nro**  |Sopimusskenaarioissa käytettävä resurssi.|
|**Paikallisen resurssin 2 nro**  |Laitteistovika-/korjausskenaarioissa käytettävä resurssi.|
|**Palvelun sijainti** |Määrittää varaston, jota haluat käyttää huoltotoiminnoissa. Oletus arvo on *MAIN*, mutta sitä voi muuttaa tarpeidesi mukaan.|

Kun olet valmis, valitse **Luo demotiedot** -toiminto. Tietojen lisääminen pohjana olevaan tietokantaan kestää muutaman minuutin, mutta sitten olet valmis suorittamaan erilaisia skenaarioita.  

## Esimerkkitilanteet

Contoso Coffeen esittelytiedot tukevat tällä hetkellä seuraavia testin ja harjoittelun huoltoskenaarioita:

1. Luo huoltotilaus tapauskohtaista korjauspyyntöä varten, sijoita ja vastaanota lainatavarat, rekisteröi aika ja laskuta asiakkaita [huoltonimikkeiden huoltotilausten vaihekuvauksen avulla](service-basic-flow-order.md)
2. Luo huoltosopimuksia, luo huoltotilauksia, laskuta sopimusmaksuja ja kohdista resursseja [huoltonimikkeiden huoltosopimusten vaihekuvauksen avulla](service-contract-flow.md)

Lue kunkin skenaarion vaiheet asianomaisessa artikkelissa.  

> [!IMPORTANT]
> Huollon vaihekuvaukset edellyttävät, että käyttäjäkokemukseksi on asetettu **Premium** **Yritystiedot**-sivulla.


## Katso myös

[Palvelu](../../service-service.md)
