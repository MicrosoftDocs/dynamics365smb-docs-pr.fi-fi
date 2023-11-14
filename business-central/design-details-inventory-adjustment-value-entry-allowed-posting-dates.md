---
title: 'Virhesanoma: "Kirjauspäivämäärä ei kuulu sallittujen kirjauspäivämäärien alueeseen"'
description: 'Korjaa sanoman "Kirjauspäivämäärä ei ole sallittujen kirjaus päivämäärien rajoissa" virheen, kun suoritat Muuta kust. - nimike tapahtumat -eräajoa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: bholtorf
---

# Virhesanoma: "Kirjauspäivämäärä ei kuulu sallittujen kirjauspäivämäärien alueeseen..."

Kun käytät **Muuta kust.- nimiketapahtumat** -eräajoa, saatat törmätä seuraavaan virhesanomaan:

**Kirjauspäivämäärä ei kuulu sallittujen kirjauspäivämäärien alueelle**

Tämä virhesanoma ilmaisee, että käyttäjällä ei ole oikeutta kirjata kyseistä päivämäärää koskevia tapahtumia, ja tämä voidaan korjata muuttamalla käyttäjäasetuksia.

## Käyttäjäasetusten muuttaminen  

|Käyttäjätunnus  |Ensimm. sallittu kirjauspvm  | Viimeinen sallittu kirjauspvm  |
|---------|---------|--------|
|EUROOPPA  |  2020-09-11      |2020-09-30      |

Tässä tapauksessa käyttäjälle määritetty sallittu kirjauspäivämääräalue on 11.9. - 30.9. Muutoksen arvotapahtuman kirjauspäivämäärä ei siis voi olla 10.9.  

### Asiaankuuluvan kirjauspäivämäärän asetuksen yleiskuvaus

#### Varastokaudet

|Lopetuspvm  |Name  |Suljettu  |
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

Jos määritetään laajempi sallittu kirjauspäivämääräalue kuin varastokaudella tai kirjanpidon asetuksissa, virhesanomassa mainittu ristiriita vältetään. Oikaisun arvotapahtuma, jonka kirjauspvm on 10. syyskuuta, kirjataan onnistuneesti näillä asetuksilla.
  
## Katso myös  

[Rakennetiedot: Muutoksen arvotapahtuman kirjauspäivämäärä](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)  
[Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
