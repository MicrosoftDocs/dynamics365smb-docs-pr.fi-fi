---
title: Arvotapahtumien kirjauspäivämäärä
description: 'Lisätietoja siitä, miten Muuta kustannuksia - Nimiketapahtumat -eräajo tunnistaa ja määrittää niiden arvotapahtumien kirjauspäivämäärän, joita eräajo on luomassa.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: edupont
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Rakennetiedot: Muutoksen arvotapahtuman kirjauspäivämäärä

Tässä artikkelissa on ohjeita varaston arvostustoimintojen käyttäjille [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa ja erityisesti siitä, miten **Muuta kust. - nimiketapahtumat** -eräajo tunnistaa ja liittää kirjauspäivämäärän arvotapahtumiin, jotka eräajo on aikeissa luoda.

## <a name="how-posting-dates-are-assigned"></a>Miten kirjauspäivämäärät määritellään

**Muuta kustannuksia - Nimiketapahtumat** -eräajo määrittää kirjauspäivämäärän arvotapahtumalle, jonka se luo seuraavien vaiheiden avulla:  

1. Alussa luotavan tapahtuman kirjauspäivämäärä on sama kuin päivämäärän, jota se muuttaa.  

2. Kirjauspäivämäärä vahvistetaan varastokausien ja/tai pääkirjanpidon asetusten avulla.  

3. Kirjauspäivämäärän määritys: jos alkuperäinen kirjauspäivämäärä ei kuulu sallittuun kirjauspäivämääräalueeseen, eräajo määrittää sallitu kirjauspäivämäärän pääkirjanpidon asetuksista tai varastokausista. Jos pääkirjanpidon asetuksissa on määritetty sekä varastokaudet että sallitut kirjauspäivämäärät, muutoksen arvotapahtumalle määritetään myöhempi näistä kahdesta päivämäärästä.  

Tarkastellaan tätä prosessia lähemmin. Oletetaan, että käsittelyssä on myynnin nimiketapahtuma. Nimike on toimitettu 5.9.2020 ja laskutettu päivää myöhemmin.  

#### <a name="item-ledger-entry"></a>Nimiketapahtuma

|Tapahtumanro  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  | Asiakirjanumero |Sijaintikoodi   |määrä  |Kustannussumma (Tod.)  |Laskutettu määrä  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Myynti       |102033     |  Sininen       | -1    |    -11     |-1     |    0     |

Alla ovat liittyvät arvotapahtumat:

- **Tapahtuma 379** edustaa toimitusta. Sen kirjauspäivämäärä on sama kuin päänimiketapahtuman päivämäärä.  
- **Tapahtuma 381** vastaa laskua.  
- **Tapahtuma 391** on laskutuksen arvotapahtuman (tapahtuma 381 edellä) muutos.  

|Tapahtumanro  |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  |Nimiketapahtuman nro  |Sijaintikoodi   |Nimiketapahtumien määrä  |Laskutettu määrä  |Kustannussumma (Tod.)  |Kustannussumma (oletettu)  |Muutos  |Kohdistetaan tapahtumaan  |Lähdekoodi  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Myynti     | Välitön kustannus   | 102033        |319     | Sininen        | -1       |0         |  0       |     -10   |Ei   |0    |Myynti          |
|381     |  A       |    2020-09-06     |    Myynti     | Välitön kustannus   | 103022        |319     | Sininen        |  0       |-1        |-10       |    10     | Ei  |0      |       Myynti   |
|391     |  A       |    2020-09-10     |    Myynti     | Välitön kustannus   | 103022        |319     | Sininen        |  0       |0         |-1        |    0     |Kyllä   |    181   | VARMUUTOS   |

Määrittääksesi **Tapahtuman 391** kirjauspäivämäärän seuraavat vaiheet otettiin käyttöön:

1. Luotava **muutoksen arvotapahtuma** (**Tapahtuma 391**) on määritetty samaan **kirjauspäivämäärään** kuin tapahtuma, jota se muuttaa.

2. **Muuta kustannuksia - Nimiketapahtumat** -eräajo määrittää, kuuluuko muutoksen arvotapahtuman alkuperäinen kirjauspäivämäärä sallittuun kirjauspäivämääräalueeseen varastokausien ja/tai pääkirjanpidon asetusten perusteella.  

Tarkistetaan yllämainittu myynti lisäämällä sallittujen kirjauspäivämääräalueiden asetukset.  
  
#### <a name="inventory-periods"></a>Varastokaudet

|Lopetuspvm  |Name  |Suljettu  |
|---------|---------|---------|
|2020-01-31     |Tammikuu 2020      |  Kyllä    |
|2020-02-28     |Helmikuu 2020     |  Kyllä    |
|2020-03-31     |Maaliskuu 2020        |  Kyllä    |
|2020-04-30     |Huhtikuu 2020        |  Kyllä    |
|2020-05-31     |Toukokuu 2020        |  Kyllä    |
|2020-06-30     |Heinäkuu 2020       |  Kyllä    |
|2020-07-31     |Heinäkuu 2020        |  Kyllä    |
|2020-08-31     |Elokuu 2020     |  Kyllä    |
|2020-09-30     |Syyskuu 2020  |         |
|2020-10-31     |Lokakuu 2020    |         |
|2020-11-30     |Marraskuu 2020   |         |
|2020-12-31     |Joulukuu 2020   |         |

Ensimmäinen sallittu kirjauspäivämäärä on ensimmäisen avoimen kauden ensimmäinen päivä eli 1.9.2020.  

#### <a name="general-ledger-setup"></a>Pääkirjanpidon asetukset

|Kenttä|Arvo  |
|---------|---------|
|Ensimm. sallittu kirjauspvm:  |  2020-09-10      |
|Viimeinen sallittu kirjauspvm:    |  2020-09-30      |
|Rekisteröi aika:       |         |
|Paikallinen osoitemuoto:|   Postinro      |  

Ensimmäinen sallittu kirjauspäivämäärä on **Ensimm. sallittu kirjauspvm** -kentässä mainittu päivämäärä: 10.9.2020. Jos **pääkirjanpidon asetuksissa** on määritetty sekä varastokaudet että sallitut kirjauspäivämäärät, jälkimmäinen päivämäärä määrittää sallitun kirjauspäivämäärän.  

**Sallitun kirjauspäivämäärän määrittäminen**  

Alkuperäinen määritetty kirjauspäivämäärä oli 6.9., kuten vaiheessa 1 kerrottiin. Toisessa vaiheessa kuitenkin Muuta kustannuksia - Nimiketapahtumat -eräajo määrittää, että aikaisin sallittu kirjauspäivämäärä on 10.9. ja tämän vuoksi määrittää alla muutoksen arvotapahtumalle (**Tapahtuma 391**) päivämäärän 10.9.  


|Tapahtumanro  |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  |Nimiketapahtuman nro  |Sijaintikoodi   |Nimiketapahtumien määrä  |Laskutettu määrä  |Kustannussumma (Tod.)  |Kustannussumma (oletettu)  |Muutos  |Kohdistetaan tapahtumaan  |Lähdekoodi  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Myynti     | Välitön kustannus   | 102033        |319     | Sininen        | -1       |0         |  0       |     -10   |Ei   |0    |Myynti          |
|381     |  A       |    2020-09-06     |    Myynti     | Välitön kustannus   | 103022        |319     | Sininen        |  0       |-1        |-10       |    10     | Ei  |0      |       Myynti   |
|391     |  A       |    **2020-09-10**     |    Myynti     | Välitön kustannus   | 103022        |319     | Sininen        |  0       |0         |-1        |    0     |Kyllä   |    181   | VARMUUTOS   |

## <a name="common-problems-with-the-adjust-cost---item-entries-batch-job"></a>Yleisiä ongelmia Muuta kustannuksia - Nimiketapahtumat -eräajossa

On olemassa kaksi skenaariota, joita tuki tiimi kohtaa niin usein, että niillä on omat ongelmanratkaisuartikkelinsa.

### <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Virhesanoma: "Kirjauspäivämäärä ei kuulu sallittujen kirjauspäivämäärien alueeseen..."

Jos kohtaat tämän virheen, sinun täytyy muuttaa päivämääriä, jolloin käyttäjällä on oikeus kirjata tapahtumia. Lisätietoja: [Virhesanoma: "Kirjauspäivämäärä ei kuulu sallittujen kirjauspäivämäärien alueeseen"](design-details-inventory-adjustment-value-entry-allowed-posting-dates.md)

### <a name="posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Kirjauspäivämäärään verratun muutoksen arvotapahtuman kirjauspäivämäärän vuoksi muutos voi olla uudelleenarvostus tai nimikekulu.

Lisätietoja: [Oikaisun arvon tapahtuman kirjauspäivämäärä verrattuna lähdetapahtumaan](design-details-inventory-adjustment-value-entry-source-entry.md)

## <a name="see-also"></a>Katso myös

[Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)  
[Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
