---
title: 'Virhesanoma: "Kirjauspäivämäärä ei kuulu sallittujen kirjauspäivämäärien alueeseen"'
description: 'Korjaa sanoman "Kirjauspäivämäärä ei ole sallittujen kirjaus päivämäärien rajoissa" virheen, kun suoritat Muuta kust. - nimike tapahtumat -eräajoa.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
---

# Virhesanoma: "Kirjauspäivämäärä ei kuulu sallittujen kirjauspäivämäärien alueeseen..."

Kun käytät **Muuta kust.- nimiketapahtumat** -eräajoa, saatat törmätä seuraavaan virhesanomaan:

**Kirjauspäivämäärä ei kuulu sallittujen kirjauspäivämäärien alueelle**

Tämä viesti tarkoittaa, että et voi kirjata tapahtumia syöttämääsi päivämäärää varten. Voit kiertää tämän ongelman muuttamalla käyttäjäasetuksia.

## Käyttäjäasetusten muuttaminen  

|Käyttäjätunnus  |Ensimm. sallittu kirjauspvm  | Viimeinen sallittu kirjauspvm  |
|---------|---------|--------|
|EUROOPPA  |  2020-09-11      |2020-09-30      |

Tässä tapauksessa voit kirjata päivämääräväliksi 11.9.–30.9. Et kuitenkaan voi kirjata muutosarvotapahtumaa, jonka kirjauspäivämäärä on 10. syyskuuta.  

### Kirjauspäivämäärän asetuksen yleiskuvaus

#### Varastokaudet

|Päättymispäivämäärä  |Nimi  |Sulj.  |
|---------|---------|---------|
|2020-01-31     |Tammikuu 2020      |  Kyllä    |
|2020-02-28     |Helmikuu 2020     |  Kyllä    |
|2020-03-31     |Maaliskuu 2020        |  Kyllä    |
|2020-04-30     |Huhtikuu 2020        |  Kyllä    |
|2020-05-31     |Toukokuu 2020        |  Kyllä    |
|2020-06-30     |Heinäkuu 2020       |  Kyllä    |
|2020-07-31     |Heinäkuu 2020        |   Kyllä   |
|2020-08-31     |Elokuu 2020     |   Kyllä   |
|2020-09-30     |Syyskuu 2020  |         |
|2020-10-31     |Lokakuu 2020    |         |
|2020-11-30     |Marraskuu 2020   |         |
|2020-12-31     |Joulukuu 2020   |         |  

#### Pääkirjanpidon asetukset

|Kenttä|Arvo|
|---------|---------|
|Ensimm. sallittu kirjauspvm:  |  2020-09-10      |
|Viimeinen sallittu kirjauspvm:    |  2020-09-30      |
|Rekisteröi aika:       |         |
|Paikallinen osoitemuoto:|   Postinro      |  

#### Käyttäjäasetukset

|Käyttäjätunnus  |Ensimm. sallittu kirjauspvm  | Viimeinen sallittu kirjauspvm  |
|---------|---------|--------|
|KÄYTTÄJÄTUNNUS |  2020-09-10      |2020-09-30      |

Jos määritetään laajempi sallittu kirjauspäivämääräalue kuin **varastokaudella** tai **kirjanpidon asetukset** -sivuilla, virhesanomassa mainittu ristiriita vältetään. Esimerkiksi laajemman vaihteluvälin ansiosta muutosarvotapahtuman päivämääräksi voidaan kirjata 10.9.
  
## Katso myös  

[Rakennetiedot: Muutosarvotapahtuman kirjauspäivä](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)  
[Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
