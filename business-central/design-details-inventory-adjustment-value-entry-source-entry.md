---
title: Oikaisun arvon tapahtuman kirjauspäivämäärä verrattuna lähdetapahtumaan
description: 'Lisätietoja skenaariosta Kirjauspvm. muutosarvotapahtumassa vs. kirjauspvm. tapahtumassa, joka aiheuttaa muutoksen, kuten uudelleenarvostus tai nimikekulu", kun suoritetaan Muuta kustannuksia – Nimiketapahtumat -eräajoa.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: edupont
---

# <a name="posting-date-on-adjustment-value-entry-compared-to-the-source-entry"></a>Oikaisun arvon tapahtuman kirjauspäivämäärä verrattuna lähdetapahtumaan

Tässä artikkelissa verrataan muutosarvotapahtuman kirjauspäivämäärää sen tapahtuman kirjauspäivämäärään, joka aiheuttaa Muuta kustannuksia – Nimiketapahtumat -eräajon suorituksen, erityisesti uudelleenarvostusskenaario ja nimikekuluskenaario.

**Muuta kustannuksia – Nimiketapahtumat** -eräajo käsittelee tiedot riippuen skenaariosta ja [!INCLUDE[prod_short](includes/prod_short.md)]in kokoonpanosta. Tässä osassa kuvataan kaksi erillistä prosessia, ja jokaisesta näytämme, millaisia vaikutuksia Muuta kustannuksia – Nimiketapahtumat -eräajolla on tietoihin.

## <a name="revaluation-scenario"></a>Uudelleenarvostusskenaario

### <a name="prerequisites"></a>Vaatimukset

Määritä seuraavat arvot:

**Varastonhallinnan asetukset**:  

- Automaattinen kustannusten kirjaus = Kyllä  

- Automaattinen kustannusten muuttaminen = Aina  

- Keskim. kust. laskentatyyppi = Nimike  

- Keskimääräisen kustannuksen jakso = Päivä  

**Pääkirjanpidon asetukset**:  

- Ensimm. sallittu kirjauspvm = 1.1.2021  

- Viimeinen sallittu kirjauspvm = Tyhjä  

**Käyttäjäasetukset**:  

- Ensimm. sallittu kirjauspvm = 1.12.2020  

- Viimeinen sallittu kirjauspvm = Tyhjä  

### <a name="to-test-the-scenario"></a>Skenaarion testaaminen

Testaa tämä skenaario suorittamalla seuraavat vaiheet.

1. Luo **Nimike** nimeltä TEST käyttäen seuraavia arvoja:  

     - Perusmittayksikkö = Kpl  

     - Arvostusmenetelmä = Keskiarvo  

     - Valitse vaihtoehtoiset kirjausryhmät.  

2. Avaa **nimikepäiväkirja** ja luo uusi tapahtuma ja kirjaa rivi seuraavasti:  

     - Kirjauspäivämäärä = 15.12.2020  

     - Nimike = TESTI  

     - Tapahtuman tyyppi = Osto  

     - Määrä = 100  

     - Yksikkösumma = 10  

3. Avaa **nimikepäiväkirja** ja luo uusi tapahtuma ja kirjaa rivi seuraavasti:  

     - Päivämäärä = 20.12.2020  

     - Nimike = TESTI  

     - Tapahtuman tyyppi = Negatiivinen muutos  

     - Määrä = 2  

4. Avaa **nimikepäiväkirja** ja luo uusi tapahtuma ja kirjaa rivi seuraavasti:  

     - Päivämäärä = 15.1.2021  

     - Nimike = TESTI  

     - Tapahtuman tyyppi = Negatiivinen muutos  

     - Määrä = 3  

5. Avaa **Nimikkeen uudelleenarvostuspäiväkirja** ja luo uusi tapahtuma ja kirjaa rivi seuraavasti:  

     - Nimike = TESTI  

     - Kohdistetaan tapahtumaan = valitse vaiheessa 2 kirjattu ostotapahtuma. Uudelleenarvostuksen kirjauspäivämäärä on sama kuin tapahtuman, jota se muuttaa.  

     - Yksikkökustannus (uudelleenarvostettu) = 40  

Seuraavat **nimikekirjaukset** ja **arvotapahtumat** on kirjattu:  

**Nimiketapahtuma – osto**:  

|Tapahtumanumero  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  |Asiakirjanumero  |määrä  |Kustannussumma (Tod.)  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |TESTI         |2020-12-15         |Osto         |T00001         |100         |4000         |95        |

**Arvotapahtumat**  

|Tapahtumanumero  |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman nro  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  |Nimikenumerotapahtumien määrä  |Kustannussumma (Tod.)  |KP:oon kirjattu kustannus  |Muutos  |Kohdistetaan tapahtumaan  |Lähdekoodi  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |TESTI|   2020-12-15    |317         |Osto         |Välitön kustannus         |T00001         |100         |1 000,00          |1 000,00    |Ei         |0         |NIMIKENL         |
|379     |TESTI   |**2020-12-15**    |317         |Osto         |Uudelleenarvostus         |T04002         |0         |3 000,00         |3 000,00         |Ei         |0         |UUDARVINL         |

**Nimiketapahtuma - negatiivinen oikaisu, vaihe 3**  

|Tapahtumanro  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  |Asiakirjanumero  |määrä  |Kustannussumma (Tod.)  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |TESTI      |2020-12-20   |Negatiivinen muutos  |T00002         |-2         |-80         | 0        |

**Arvotapahtumat**  

|Tapahtumanumero  |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman nro  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  |Nimikenumerotapahtumien määrä  |Kustannussumma (Tod.)  |KP:oon kirjattu kustannus  |Muutos  |Kohdistetaan tapahtumaan  |Lähdekoodi  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |TESTI|   2020-12-20    |318         |Negatiivinen muutos         |Välitön kustannus         |T00002         |-2         |-20          |-20    |Ei         |0         |NIMIKENL         |
|380     |TESTI   |**2021-01-01**    |318         |Negatiivinen muutos         |Välitön kustannus         |T04002         |0         |-60         |-60         |Kyllä         |377         |VAROIK         |

**Nimiketapahtuma - negatiivinen oikaisu, vaihe 4**  

|Tapahtumanro  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  |Asiakirjanumero  |määrä  |Kustannussumma (Tod.)  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |TESTI      |2021-01-15   |Negatiivinen muutos  |T00003         |-3         |-120         | 0        |

**Arvotapahtumat**  

|Tapahtumanumero  |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman nro  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  |Nimikenumerotapahtumien määrä  |Kustannussumma (Tod.)  |KP:oon kirjattu kustannus  |Muutos  |Kohdistetaan tapahtumaan  |Lähdekoodi  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |TESTI|   2021-01-15    |319         |Negatiivinen muutos         |Välitön kustannus         |T00003         |-3         |-30          |-30    |Ei         |0         |NIMIKENL         |
|381     |TESTI   |**2021-01-15**    |319         |Negatiivinen muutos         |Välitön kustannus         |T04003         |0         |-90         |-90         |Kyllä         |378         |VAROIK         |

**Muuta kustannuksia - Nimiketapahtumat** -eräajo on tunnistanut muutokset kustannuksissa ja muuttanut negatiivisia muutoksia.  

**Luotujen muutoksen arvotapahtumien kirjauspäivämäärien tarkistaminen:** Muuta kustannuksia - Nimiketapahtumat -eräajon aikaisin sallittu kirjauspäivämäärä on 1.1.2021 pääkirjanpidon asetusten mukaan.  

**Negatiivinen muutos vaiheessa 3:** määritetty kirjauspäivämäärä on 1.1. pääkirjanpidon asetusten mukaan. Muutoksen arvotapahtuman kirjauspäivämäärä on 20.12.2020. Pääkirjanpidon asetusten mukaan päivämäärä ei kuulu sallittuun kirjauspäivämääräalueeseen. Tämän vuoksi muutoksen arvotapahtumalle on määritetty pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän kirjauspäivämäärä.  

**Negatiivinen muutos vaiheessa 4:** määritetty kirjauspäivämäärä on 15.1. Muutoksen arvotapahtuman kirjauspäivämäärä on 15.1., joka kuuluu sallittuun kirjauspäivämääräalueeseen pääkirjanpidon asetusten mukaan.  

Negatiiviseen muutokseen vaiheessa 3 tehty muutos aiheuttaa keskustelua. Muutoksen arvotapahtuman suositeltu kirjauspäivämäärä olisi ollut 20.12. tai jokin muu joulukuun päivämäärä, koska myytyjen tuotteiden kustannusten muutoksen aiheuttanut uudelleenarvostus kirjattiin joulukuussa.  

Jotta negatiiviseen muutokseen voidaan tehdä muutos joulukuussa vaiheessa 3, pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän päivämäärän on oltava joulukuussa.  

### <a name="conclusion"></a>Yhteenveto

Kun otetaan huomioon tässä skenaariossa saatu kokemus ja kun otetaan huomioon sopivimmat asetukset yrityksen sallimalle Kirjauspvm-alueelle, kannattaa ehkä harkita seuraavaa. Niin kauan kuin sallit varastoarvon muutosten kirjaamisen kaudessa, esimerkiksi joulukuussa tässä tapauksessa, asetukset, joita yritys käyttää sallituille kirjauspäivämääräväleille, tulisi yhtenäistää tämän päätöksen kanssa. Pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kenttä, johon on määritetty 1.12., sallii joulukuussa tehdyn uudelleenarvostuksen ohjauksen edelleen saman kauden muuttuneisiin lähteviin tapahtumiin.  

Tässä skenaariossa ollut asetus, jonka mukaan käyttäjäryhmät, jotka eivät voi tehdä kirjauksia joulukuussa, voivat tehdä niitä tammikuussa, kannattaa määrittää käyttäjäasetuksissa pääkirjanpidon asetusten sijaan.  

## <a name="item-charge-scenario"></a>Nimikekulujen skenaario

### <a name="prerequisites-1"></a>Vaatimukset

Määritä seuraavat arvot:

**Varastonhallinnan asetukset**:  

- Automaattinen kustannusten kirjaus = Kyllä  

- Automaattinen kustannusten muuttaminen = Aina  

- Keskim. kust. laskentatyyppi = Nimike  

- Keskimääräisen kustannuksen jakso = Päivä  

**Pääkirjanpidon asetukset**:  

- Ensimm. sallittu kirjauspvm = 1.12.2020.  

- Viimeinen sallittu kirjauspvm = Tyhjä  

**Käyttäjäasetukset**:  

- Ensimm. sallittu kirjauspvm = 1.12.2020.  

- Viimeinen sallittu kirjauspvm = Tyhjä  

### <a name="to-test-the-scenario-1"></a>Skenaarion testaaminen

Testaa tämä skenaario suorittamalla seuraavat vaiheet:

1.  Luo **Nimikekulu** käyttäen seuraavia arvoja:  

     - Perusmittayksikkö = Kpl  

     - Arvostusmenetelmä = Keskiarvo  

     - Valitse vaihtoehtoiset kirjausryhmät.  

2.  Luo uusi **Ostotilaus**, jossa on seuraavat arvot:  

     - Tavarantoimittajan nro: 10000  

     - Kirjauspäivämäärä = 15.12.2020

     - Toimittajan laskunro: 1 234  

     Valitse ostotilausrivillä seuraavat arvot:  

     - Nimike = KULU  

     - Määrä = 1  

     - Välitön yksikkökustannus = 100  

     Viimeistele vaihe kirjaamalla asiakirja vastaanotetuksi ja laskutetuksi.  

3.  Luo uusi **Myyntitilaus**, jossa on seuraavat arvot:  

     - Tilausasiakkaan nro: 10000  

     - Kirjauspäivämäärä = 16.12.2020  

     Myyntitilausrivillä:  

     - Nimike = KULU  

     - Määrä = 1  

     - Yksikköhinta = 135  

     Viimeistele vaihe kirjaamalla asiakirja vastaanotetuksi ja laskutetuksi.  

4.  Määritä **Pääkirjanpidon asetukset**-sivun arvot:  

     - Ensimm. sallittu kirjauspvm = 1.1.2021  

    -  Viimeinen sallittu kirjauspvm = tyhjä  

5.  Luo uusi **Ostotilaus**, jossa on seuraavat arvot:  

     - Tavarantoimittajan nro: 10000  

     - Kirjauspäivämäärä = 2.1.2021  

     - Toimittajan laskunro: 2 345  

     Ostotilausrivillä:  

     - Nimikekulu = JB-RAHTI  

     - Määrä = 1  

     - Välitön yksikkökustannus = 3  

     - Määritä nimikekuluksi ostovastaanotto vaiheesta 2.  

     Viimeistele vaihe kirjaamalla asiakirja vastaanotetuksi ja laskutetuksi.  


**Ostovaiheen 2 tilanimiketapahtuma**:  
  
|Tapahtumanumero  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  |Asiakirjanumero  |määrä  |Kustannussumma (Tod.)  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |VELOITUS         |2020-12-15         |Osto         |107030         |1         |105         |0        |

**Arvotapahtumat**  

|Tapahtumanumero |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman nro  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  | Nimikekulunro    |  Nimiketapahtumien määrä   |Kustannussumma (Tod.)     |KP:oon kirjattu kustannus |Muutos |Kohdistetaan tapahtumaan |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |VELOITUS|   2020-12-15    |324         |Osto         |Välitön kustannus         |108029         |         |1          |100    |100         |NRO         |0         |
|399      |VELOITUS   |2021-01-02    |324         |Osto         |Välitön kustannus         |108009         |JB-RAHTI         |0         |3         |3         |NRO         |0         |

**Tilanimiketapahtuma – myynti**:  
  
|Tapahtumanro  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  |Asiakirjanumero  |määrä  |Kustannussumma (Tod.)  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |VELOITUS         |2020-12-16         |Myynti         |102035         |-1         |-105         |0        |

**Arvotapahtumat**  

|Tapahtumanumero |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman nro  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  | Nimikekulunro    |  Nimiketapahtumien määrä   |Kustannussumma (Tod.)     |KP:oon kirjattu kustannus |Muutos |Kohdistetaan tapahtumaan |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |VELOITUS|   2020-12-16    |325         |Myynti         |Välitön kustannus         |109024         |         |-1          |-100    |-100         |NRO         |0         |
|400      |VELOITUS   |2021-01-01    |325         |Myynti         |Välitön kustannus         |109024         |         |0         |-3         |-3         |Kyllä         |398         |

6.  Ostolasku saapuu käsittelypäivänä 3.1. Ostolasku sisältää vaiheessa 2 ostoon tehdyn lisäkulun. Tämän laskun asiakirjan päivämäärä on 30.12. Tämän vuoksi sen kirjauspäivämääräksi tulee 30.12.2020.  

     Luo uusi **Ostotilaus**, jossa on seuraavat arvot:  

     - Tavarantoimittajan nro: 10000  

     - Kirjauspäivämäärä = 30.12.2020  

     - Toimittajan laskunro: 3 456  

     Valitse ostotilausrivillä seuraavat arvot:  

     - Nimikekulu = JB-RAHTI  

     - Määrä = 1  

     - Välitön yksikkökustannus = 2  

     Määritä nimikekuluksi ostovastaanotto vaiheesta 2  

     Viimeistele vaihe kirjaamalla asiakirja vastaanotetuksi ja laskutetuksi.  


**Oston tilanimiketapahtuma**:  

|Tapahtumanumero  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  |Asiakirjanumero  |määrä  |Kustannussumma (Tod.)  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |VELOITUS         |2020-12-15         |Osto         |107030         |1         |105         |0        |

**Arvotapahtumat**  

|Tapahtumanro |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman nro  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  | Nimikekulunro    |  Nimiketapahtumien määrä   |Kustannussumma (Tod.)     |KP:oon kirjattu kustannus |Muutos |Kohdistetaan tapahtumaan |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |VELOITUS   |2020-12-15    |324         |Osto         |Välitön kustannus         |108029         |            |1         |100    |100         |Ei         |0         |
|399      |VELOITUS   |2021-01-02    |324         |Osto         |Välitön kustannus         |108030         |JB-RAHTI   |0         |3         |3         |Ei         |0         |
|401      |VELOITUS   |**2020-12-30**    |324         |Osto         |Välitön kustannus         |108031         |JB-RAHTI   |0         |2         |2         |Ei         |0         |

**Tilanimiketapahtuma – myynti**:  
  
|Tapahtumanumero  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  |Asiakirjanumero  |määrä  |Kustannussumma (Tod.)  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |VELOITUS         |2020-12-16         |Myynti         |102035         |-1         |-105         |0        |

**Arvotapahtumat**  

|Tapahtumanro |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman nro  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  | Nimikekulunro    |  Nimiketapahtumien määrä   |Kustannussumma (Tod.)     |KP:oon kirjattu kustannus |Muutos |Kohdistetaan tapahtumaan |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |VELOITUS   |2020-12-16        |325         |Myynti         |Välitön kustannus         |103024         |            |-1         |-100       |-100         |Ei         |0         |
|400      |VELOITUS   |2021-01-01        |325         |Myynti         |Välitön kustannus         |103024         |            |0          |-3         |-3         |Kyllä         |398         |
|402      |VELOITUS   |**2021-01-01**    |325         |Myynti         |Välitön kustannus         |103024         |            |0          |-2         |-2         |Kyllä         |398         |

Varaston arvostus -raportti tulostetaan 31.12.2020

![Varaston arvostusraportin sisältö.](media/helene/TechArticleAdjustcost13.png "Varaston arvostusraportin sisältö")

**Skenaarion yhteenveto:**  

Kuvattu skenaario loppuu Varaston arvostus -raporttiin, jossa määrä = 0 ja arvo = 2. Vaiheessa 6 kirjattu nimikekulu on osa varaston arvon nousua joulukuussa. Saman kauden varaston arvon lasku ei ole muuttunut.  

Pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän arvo 1.1. on sopiva ensimmäiselle nimikekululle. Varaston arvon nousun ja laskun kustannukset tallennettiin samaan kauteen. Pääkirjanpidon asetusten vuoksi toinen nimikekulu aiheuttaa kuitenkin muutoksen myytyjen tuotteiden kustannuksessa. Muutos otetaan huomioon seuraavan kauden aikana.  

**Yhteenveto.**  

On haastavaa, kun Varaston arvostus -raportissa määritetään, että määrä = 0 samalla, kun arvo <> 0. Tässä tapauksessa on vaikeaa kertoa optimaaliset asetukset, koska ostolaskut saapuvat samana päivänä mutta ne koskevat eri kausia tai jopa eri tilivuosia. Uuteen tilivuoteen siirtäminen vaatii yleensä suunnittelua. Muuta kustannuksia - Nimiketapahtumat -prosessin on myös otettava huomioon myytyjen tuotteiden kustannukset.  

Tässä skenaariossa eräs vaihtoehto olisi ollut määrittää pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän arvoksi muutamaa päivää aikaisempi joulukuun päivämäärä ja kirjata ensimmäinen nimikekulu viiveellä, jolloin edellisen kauden/tilivuoden kaikki kustannukset tuloutettaisiin kaudelle, jolle ne alussa kuuluivat. Tämän jälkeen suoritettaisiin Muuta kustannuksia - Nimiketapahtumat -eräajo ja siirrettäisiin sallittu kirjauspäivämäärä seuraavaan kauteen\/tilivuoteen. Kirjatuksi olisi tullut ensimmäinen nimikekulu, jonka kirjauspäivämäärä on 2.1.  

## <a name="see-also"></a>Katso myös

[Rakennetiedot: Muutoksen arvotapahtuman kirjauspäivämäärä](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)  
[Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
