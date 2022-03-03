---
title: Sähköisen tiedonvaihdon määrittäminen | Microsoft Docs
description: Voit käyttää ulkoista OCR-palvelua PDF- tai kuvatiedostojen muuntamiseen sähköisiksi asiakirjoiksi.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ba59e1164dbbe4cdd95cca31687b63db2af8018c
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8129231"
---
# <a name="set-up-data-exchange-definitions"></a>Tietojenvaihtomääritysten määrittäminen
Voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in vaihtamaan tiettyjen taulukoiden tietoja ulkoisten tiedostojen kanssa. Tällöin voit esimerkiksi lähettää ja vastaanottaa sähköisiä asiakirjoja sekä tuoda ja viedä pankkitietoja tai muita tietoja, kuten palkanlaskennan tietoja, vaihtokursseja ja tuoteluetteloita. Lisätietoja on kohdassa [Sähköinen tiedonsiirto](across-data-exchange.md).  

Datatiedoston tai tietovirran tietojenvaihtomäärityksen luonnin valmisteluun voit käyttää liittyvää XML-rakennetta. Sen avulla voit määrittää **Sarakkeen määritykset** -pikalomakkeeseen sisällytettävät tietoelementit. Katso vaihe 6 kohdassa [Tiedoston rivien ja sarakkeiden muotoilun kuvaileminen](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Lisätietoja on kohdassa [XML-rakenteiden käyttäminen tiedonsiirtomääritysten valmistelussa](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Tiedonsiirtomääritykset määritetään yleensä **Tiedonsiirtomääritys**-sivulla. Vaihtokurssien päivityspalvelun tiedonsiirtomääritysten määrittäminen aloitetaan kuitenkin yksinkertaistetussa **Vaihtokurssin päivitysasetusten kortti** -sivulla.  

> [!NOTE]  
>  Jos muunnettava tiedosto on XML-muodossa, tämän ohjeaiheen termi *sarake* on tulkittava *tietoa sisältäväksi XML-elementiksi*.  

Tämä ohjeaihe sisältää seuraavat menettelyt:  

* Tietojenvaihtomääritysten määrittäminen  
* Tietojenvaihtomäärityksen vieminen XML-tiedostona muiden käyttöä varten  
* XML-tiedoston tuominen olemassa olevaa tietojenvaihtomääritystä varten  

## <a name="to-create-a-data-exchange-definition"></a>Tietojenvaihtomääritysten määrittäminen  
Tietojenvaihtomäärityksen luominen muodostuu kahdesta tehtävästä:  

1. Kuvaa tiedoston rivien ja sarakkeiden muotoilu **Tiedonsiirtomääritys**-sivulla.  
2. Kohdista **Tiedonsiirron vastaavuus** -sivulla datatiedoston sarakkeet [!INCLUDE[prod_short](includes/prod_short.md)]in kenttiin.  

Tämä kuvataan seuraavissa menettelytavoissa.  

> [!TIP]
> Jos haluat nähdä, mitä codeuniteja Microsoft käyttää vakiotuotteen nykyisissä määritelmissä, voit tarkistaa ne kunkin määritelmän **Kentän vastaavuus** -sivun ylätunnisteessa olevasta kolmesta **Codeunit**-kentästä.

#### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a>Tiedoston rivien ja sarakkeiden muotoilun kuvaaminen  
1. Kirjoita **Haku**-ruutuun **Tietojenvaihtomääritykset** ja valitse aiheeseen liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3. Kuvaile tietojenvaihtomääritys ja datatiedoston tyyppi **Yleiset**-pikalomakkeessa täyttämällä kentät seuraavan taulukon mukaisesti.  

    |Kenttä|Määritys|  
    |---------------------------------|---------------------------------------|  
    |**Koodi**|Anna koodi, jonka avulla tietojenvaihtomääritys tunnistetaan.|  
    |**Nimi**|Anna tietojenvaihtomäärityksen nimi.|  
    |**Tiedostotyyppi**|Määritä, minkälaiselle tiedostolle tietojenvaihtomääritystä käytetään. Valittavana on neljä tiedostotyyppiä:<br /><br /> -   **XML**: sisällön kerroksittaiset merkkijonot ja merkinnät, joita ympäröivät toimintoa osoittavat tunnisteet.<br />-   **Muuttuva teksti**: Tietueiden pituus on muuttuva, ja ne erotetaan merkillä, kuten pilkulla tai puoli\-pisteellä. Tunnetaan myös nimellä *eroteltu tiedosto*.<br />-   **Kiinteä teksti**: tietueilla on sama pituus pad-merkkejä käytettäessä ja jokainen tietue on erillisellä rivillä. Tunnetaan myös nimellä *kiinteäleveyksinen tiedosto*.<br />- **Json**: JavaScriptin kerrostettu komentosarjasisältö.|  
    |**Tyyppi**|Määritä, minkälaiselle aktiviteetille tietojenvaihtomääritystä käytetään (esimerkiksi **Maksun vienti**).|  
    |**Tietoja käsittelevä Codeunit**|Määritä codeunit, joka siirtää tietoa [!INCLUDE[prod_short](includes/prod_short.md)]in taulukoihin ja taulukoista pois.|  
    |**Tarkistuksen Codeunit**|Määritä codeunit, jonka avulla tiedot tarkistetaan ennalta määritettyjen liiketoimintasääntöjen mukaan.|  
    |**Codeunit luetaan/kirjoitetaan**|Määritä codeunit, joka työstää tuodut tiedot ennen kartoitusta ja viedyt tiedot kartoituksen jälkeen.|  
    |**XMLportia luetaan/kirjoitetaan**|Määritä XMLportin, jonka kautta tuotava tiedosto tai palvelu vastaanotetaan ennen yhdistämistä ja jonka kautta viedyt tiedot lähetetään, kun ne kirjoitetaan tiedostoon tai palveluun yhdistämisen jälkeen.|  
    |**Ulk. tietoja käsittelevä Codeunit**|Määritä codeunit, joka siirtää ulkoiset tiedot tiedonsiirtokehykseen ja siitä pois.|  
    |**Käyttäjäpalautteen Codeunit**|Määritä codeunit, joka tekee erilaisia puhdistustoimia (esimerkiksi merkitsee rivit viedyiksi ja poistaa tilapäiset tietueet) yhdistämisen jälkeen|  
    |**Tiedoston koodaus**|Määritä tiedoston koodaus. **Huomautus:** Tätä kenttää käytetään vain tuonnissa.|  
    |**Sarake-erotin**|Määritä se, kuinka tiedoston sarakkeet erotetaan toisistaan, jos tiedosto on tyyppiä **Muuttuva teksti**.|  
    |**Otsikkorivit**|Määritä, kuinka monta otsikkoriviä on tiedostossa.<br /><br /> Näin varmistat, että ylätunnisteen tietoja ei tuoda. **Huomautus:** Tätä kenttää käytetään vain tuonnissa.|  
    |**Otsikon tunniste**|Jos otsikkorivi on tiedostossa useissa eri kohdissa, kirjoita ensimmäisen sarakkeen teksti otsikkoriville.<br /><br /> Näin varmistat, että ylätunnisteen tietoja ei tuoda. **Huomautus:** Tätä kenttää käytetään vain tuonnissa.|  
    |**Alatunnisteen tunniste**|Jos alatunnisterivi on tiedostossa useissa eri kohdissa, kirjoita ensimmäisen sarakkeen teksti alatunnisteriville.<br /><br /> Näin varmistat, että alatunnisteen tietoja ei tuoda. **Huomautus:** Tätä kenttää käytetään vain tuonnissa.|  

4. Kuvaile datatiedoston rivien muotoilu **Rivin määritykset**-pikalomakkeessa täyttämällä kentät seuraavan taulukon mukaisesti.  

    > [!NOTE]  
    >  Tiliotteiden tuontia varten luodaan vain yksi rivi kutakin tuotavaa tiliotteen yksittäistä muotoa kohden.  
    >   
    >  Maksujen vientiä varten voit luoda rivin jokaista vietävää maksutyyppiä kohden. Tällöin **Sarakkeen määritykset** -pikalomakkeessa näkyy erilliset sarakkeet kullekin maksutyypille.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Koodi**|Lisää koodi, jonka avulla tiedoston rivi tunnistetaan.|  
    |**Nimi**|Kirjoita nimi, joka kuvaa tiedoston riviä.|  
    |**Sarakemäärä**|Määritä datatiedoston rivin sarakkeiden määrä. **Huomautus:** Tätä kenttää käytetään vain tuonnissa.|  
    |**Tietorivin tunniste**|Määritä elementtiin liittyvän XML-kaavan sijainti, joka edustaa tiedoston pääkirjausta. **Huomautus:** Tätä kenttää käytetään vain tuonnissa.|  
    |**Nimitila**|Määritä nimitila, jota tiedostolta odotetaan, mikä mahdollistaa nimitilan validoinnin. Voit jättää tämän kenttä tyhjäksi, jos et halua ottaa nimitilan tarkistusta käyttöön.|  

5. Luo rivi jokaista vietävää datatiedoston tyyppiä kohden toistamalla vaihe 4.  

     Jatka kuvailemalla datatiedoston sarakkeiden muotoilu **Sarakkeen määritykset**-pikalomakkeessa täyttämällä kentät alla olevan taulukon mukaisesti. Voit käyttää apuna rakennetiedostoa (esimerkiksi .XSD-tiedostoa), jolloin datatiedosto esitäyttää pikalomakkeeseen tarvittavat elementit. Lisätietoja on kohdassa [XML-rakenteiden käyttäminen tiedonsiirtomääritysten valmistelussa](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

6. Valitse **Sarakkeen määritykset** -pikalomakkeessa **Hae tiedostorakenne**.  
7. Valitse liittyvä rakennetiedosto **Hae tiedostorakenne** -sivulla ja valitse sitten **OK**. **Sarakkeen määritykset** -pikalomakkeen rivit täytetään datatiedoston rakenteen mukaisesti.  
8. Muokkaa **Sarakkeen**-pikalomakkeen kenttiä tai täytä ne seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Sarakkeen nro**|Määritä määrä, joka kuvaa sarakkeen sijaintia tiedostorivillä.<br /><br /> Määritä XML-tiedostojen osalta luku, joka ilmaisee tiedostossa olevien tietojen elementin tyyppiä.|  
    |**Nimi**|Määritä sarakkeen nimi.<br /><br /> Määritä XML-tiedostojen osalta merkintä, joka merkitsee siirrettävät tiedot.|  
    |**Tietotyyppi**|Määritä, onko vaihdettavat tiedot tyyppiä **Teksti**, **Päivämäärä** vai **Desimaali**.|  
    |**Tietojen muoto**|Määritä tietomuoto, jos sellainen on. Esimerkiksi **-kk-pp-vvvv**, jos tietotyyppi on **Päivämäärä**. **Huomautus:** Määritä tietojen muoto vientiä varten [!INCLUDE[prod_short](includes/prod_short.md)]in mukaan. Määritä tietojen muoto vientiä varten .NET Frameworkin mukaan. Lisätietoja on kohdassa [Vakiomuotoiset päivämäärä- ja aikamerkkijonot](/dotnet/standard/base-types/standard-date-and-time-format-strings).|  
    |**Tietojen muotoilun maa-asetus**|Määritä tiedontallennusmuototapa, jos sellainen on. Esimerkiksi **fi-fi**, jos tietotyyppi on **Desimaali**, jotta varmistetaan, että pilkkua käytetään erottimena suomalaisen muodon mukaisesti. Lisätietoja on kohdassa [Vakiomuotoiset päivämäärä- ja aikamerkkijonot](/dotnet/standard/base-types/standard-date-and-time-format-strings). **Huomautus:** Tätä kenttää käytetään vain tuonnissa.|  
    |**Pituus**|Määritä kiinteäleveyksisten rivien pituudet, jotka käsittävät sarakkeen, jos tiedosto on tyyppiä **Kiinteä teksti**.|  
    |**Kuvaus**|Kirjoita sarakkeen kuvaus tiedoksi.|  
    |**Polku**|Määritä elementin sijainti liittyvässä XML-kaavassa.|  
    |**Negatiivisen etumerkin tunniste**|Kirjoita arvo, jota tiedostossa käytetään negatiivisten tietojen tunnistamiseen niissä tiedostoissa, joissa ei voi olla negatiivisia etumerkkejä. Tätä tunnusta käytetään tunnistettujen summien negatiivisten etumerkkien palauttamisessa tuonnin aikana. **Huomautus:** Tätä kenttää käytetään vain tuonnissa.|  
    |**Vakio**|Määritä mitkä tahansa tiedot, jotka haluat viedä tästä sarakkeesta, kuten ylimääräiset tiedot maksutyypistä. **Huomautus:** Tätä kenttää käytetään vain viennissä.|  

9. Toista vaihe 8 jokaiselle sellaisen datatiedoston sarakkeelle tai XML-elementille, jonka tietoja halutaan vaihtaa [!INCLUDE[prod_short](includes/prod_short.md)]in kanssa.  

 Seuraavaksi on päätettävä, mitkä datatiedoston sarakkeet tai XML-elementit ja [!INCLUDE[prod_short](includes/prod_short.md)]in kentät yhdistetään.  

> [!NOTE]  
>  Erityinen kartoitus riippuu vaihdettavan tiedoston liiketoimintatarkoituksesta ja paikallisista variaatioista. Jopa SEPA-pankkistandardissa on paikallisia vaihteluita. [!INCLUDE[prod_short](includes/prod_short.md)] tukee SEPA CAMT -tiliotetiedostojen tuontia \-ilman\- lisä\-toimia. Siitä on osoituksena **SEPA CAMT** -tiedonsiirtomäärityksen tietuekoodi **Tiedonsiirtomääritykset**-sivulla. Lisätietoja SEPA CAMT -tuelle ominaisista kenttien yhdistämismäärityksistä on kohdassa [Kenttien yhdistämismääritykset SEPA CAMT -tiedostoja tuotaessa](across-field-mapping-when-importing-sepa-camt-files.md).  

#### <a name="to-map-columns-in-the-data-file-to-fields-in-prod_short"></a>Datatiedoston sarakkeiden yhdistäminen [!INCLUDE[prod_short](includes/prod_short.md)]in kenttiin  
> [!TIP]
> Joskus kenttien arvot, jotka haluat yhdistää, ovat erilaisia. Esimerkiksi yhdessä yrityssovelluksessa Yhdysvaltojen kielikoodi on "U.S.", mutta toisessa se on "US". Tämä tarkoittaa, että arvo on muunnettava, kun tietoja vaihdetaan. Tämä tapahtuu muutossäännöillä, jotka määrität kentille. Lisätietoja on kohdassa [Muunnossäännöt](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

1. Valitse **Rivin määritykset** -pikalomakkeessa rivi, jonka kenttiin haluat yhdistää sarakkeita, ja valitse sitten **Kenttien yhdistämismääritys**. **Tiedonsiirron vastaavuus** -sivu avautuu.  
2. Määritä kohdistus **Yleinen**-pikavälilehdellä täyttämällä seuraavassa taulukossa kuvatut kentät.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Taulukon tunnus**|Määritä taulukko, joka käsittää kentät, joista tai joihin tiedot vaihdetaan kartoituksen mukaan.|  
    |**Käytä väliaikaisena taulukkona**|Määritä, onko **Taulukon tunnus** -kentässä valittu taulukko väliaikainen taulukko, johon tuodut tiedot tallennetaan ennen niiden siirtämistä kohdetaulukkoon.<br /><br /> Väliaikaista taulukkoa käytetään yleensä silloin, kun tiedonsiirtomääritystä käytetään sähköisten asiakirjojen tuomiseen ja muuntamiseen, kuten toimittajalaskujen tuomiseen ja muuntamiseen ostolaskuiksi [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja on kohdassa [Sähköinen tiedonsiirto](across-data-exchange.md).|  
    |**Nimi**|Kirjoita kohdistusasetuksen nimi.|  
    |**Yhdistämistä edeltävä Codeunit**|Määritä codeunit, joka valmistelee [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman kenttien ja ulkoisten tietojen yhdistämisen.|  
    |**Vastaava Codeunit**|Määritä codeunit, jota käytetään yhdistämään määritetyt sarakkeet tai XML-elementit [!INCLUDE[prod_short](includes/prod_short.md)]in kenttiin.|  
    |**Yhdistämisen jälkeinen Codeunit**|Määritä codeunit, joka täydentää [!INCLUDE[prod_short](includes/prod_short.md)]in kenttien ja ulkoisten tietojen väliset yhdistämismääritykset. **Huomautus:** Kun AMC Banking 365 Fundamentals 365 -laajennustoiminto on käytössä, codeunit muuntaa [!INCLUDE[prod_short](includes/prod_short.md)]ista viedyt tiedot yleiseen vientiin soveltuvaksi muodoksi. Codeunit muuntaa ulkoiset tiedot vientiä varten sellaiseen muotoon, jonka voi tuoda [!INCLUDE[prod_short](includes/prod_short.md)]iin.|  

3.  Määritä **Kentän vastaavuus** -pikavälilehdessä, mitkä sarakkeet yhdistetään mihin [!INCLUDE[prod_short](includes/prod_short.md)]in kenttiin täyttämällä kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Sarakkeen nro**|Määritä se tiedoston sarake, jonka haluat määrittää kartoitusta varten.<br /><br /> Voit valita vain sarakkeita, joilla on rivi **Tiedonsiirtomääritykset**-sivun **Sarakkeen määritykset** -pikavälilehdessä.|  
    |**Kentän tunnus**|Määritä, mihin kenttään **Sarakkeen nro** -kentän sarake yhdistetään.<br /><br /> Voit valita vain **Yleinen**-pikavälilehden **Taulukko**-kenttään määrittämäsi taulukon kenttiä.|  
    |**Valinnainen**|Määritä, että kartta ohitetaan, jos kenttä on tyhjä. **Huomautus:** Jos et valitse tätä valintaruutua, järjestelmä ilmoittaa vientivirheestä, jos kenttä on tyhjä. **Huomautus:** Tätä kenttää käytetään vain viennissä.|  
    |**Kohdetaulukon tunnus**|Näkyvissä vain, kun **Käytä väliaikaisena taulukkona** -valintaruutu on valittu.<br /><br /> Määritä taulukko, johon **Sarakeotsikko**-kentän arvo yhdistetään, kun tietojen tuonnissa käytetään väliaikaista taulukkoa.|  
    |**Kohdetaulukon seloste**|Näkyvissä vain, kun **Käytä väliaikaisena taulukkona** -valintaruutu on valittu.<br /><br /> Määritä **Kohdetaulukon tunnus** -kentän taulukon nimi. **Sarakeotsikko**-kentän arvo yhdistetään tähän taulukkoon, kun tietojen tuonnissa käytetään väliaikaista taulukkoa.|  
    |**Kohdekentän tunnus**|Näkyvissä vain, kun **Käytä väliaikaisena taulukkona** -valintaruutu on valittu.<br /><br /> Määritä kenttä kohdetaulukossa, johon **Sarakeotsikko**-kentän arvo yhdistetään, kun tietojen tuonnissa käytetään väliaikaista taulukkoa.|  
    |**Kohdekentän seloste**|Näkyvissä vain, kun **Käytä väliaikaisena taulukkona** -valintaruutu on valittu.<br /><br /> Määritä kentän nii kohdetaulukossa, johon **Sarakeotsikko**-kentän arvo yhdistetään, kun tietojen tuonnissa käytetään väliaikaista taulukkoa.|  
    |**Valinnainen**|Näkyvissä vain, kun **Käytä väliaikaisena taulukkona** -valintaruutu on valittu.<br /><br /> Määritä, pitääkö yhdistäminen ohittaa, jos kenttä on tyhjä. Jos et valitse tätä valintaruutua, tällöin järjestelmä ilmoittaa vientivirheestä, jos kenttä on tyhjä.|  

Tietojenvaihtomääritys voidaan nyt ottaa käyttöön käyttäjille. Lisätietoja on kohdissa [Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md), [SEPA-tilisiirron määrittäminen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer), [Maksujen kerääminen SEPA-suoraveloituksella](finance-collect-payments-with-sepa-direct-debit.md) ja [Maksujen suorittaminen AMC Banking 365 Fundamentals -laajennuksella tai SEPA-tilisiirrolla](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).  

### <a name="transformation-rules"></a>Muunnossäännöt
Jos kenttien arvot ovat erilaisia, sinun on käytettävä muunnossääntöjä tietojen vaihdon määrityksissä, jotta ne olisivat samat. Voit määrittää muunnossäännöt tiedonvaihtomäärittelyjä varten avaamalla aiemmin luodun määrityksen tai luomalla uuden määrityksen ja valitsemalla sitten **Rivimääritykset** -pikavälilehdessä **Hallitse** ja sitten **Kenttien yhdistämismääritykset**. Ennalta määritetyt säännöt ovat käytettävissä, mutta voit myös luoda omia sääntöjä. Seuraavassa taulukossa kuvataan, millaisia muunnoksia voit suorittaa.

|Asetus|Kuvaus|
|---------|---------|
|**Isot kirjaimet**|Muunna kaikki kirjaimet isoiksi.|
|**Pienet kirjaimet**|Muunna kaikki kirjaimet pieniksi.|
|**Otsikon kirjainkoko**|Muunna kunkin sanan ensimmäinen kirjain isoksi.|
|**Rajaus**|Poista tyhjät tilat ennen arvoa ja sen jälkeen.|
|**Alimerkkijono**|Muuttaa tietyn osan arvosta. Jos haluat määrittää, mistä muunnos aloitetaan, valitse joko **Aloituskohta** tai **Aloitusteksti**. Aloituskohta on luku, joka edustaa ensimmäistä muunnettavaa merkkiä. Alkuteksti on kirjain, joka on välittömästi ennen korvattavaa kirjainta. Jos haluat aloittaa arvon ensimmäisestä kirjaimesta, käytä sen sijaan aloitussijaintia. Voit määrittää, mihin muunnos lopetetaan, valitsemalla joko **Pituuden**, joka on korvattavienmerkkien määrä, tai **Lopetustekstin**, joka on heti viimeisen muunnettavan merkin jälkeinen merkki.|
|**Korvaa**|Etsi arvo ja korvaa se toisella. Tästä on hyötyä yksinkertaisten arvojen, kuten tietyn sanan, korvaamiseen.|
|**Säännöllinen lauseke -korvaa**|Käytä säännöllistä lauseketta osana etsi ja korvaa -toimintoa. Tämä on kätevä korvaamaan useita tai ehkä monimutkaisempia arvoja.|
|**Ei-aakkosnumeeristen merkkien poistaminen**|Poista merkit, jotka eivät ole kirjaimia tai numeroita, kuten symbolit tai erikoismerkit.|
|**Päivämäärän muotoilu**|Määritä päivämäärien näyttäminen. Voit esimerkiksi muuntaa PP-KK-VVVV muotoon VVVV-KK-PP.|
|**Desimaalien muotoilu**|Määritä desimaalien erottelun ja pyöristystarkkuuden säännöt.|
|**Säännöllinen lauseke -vastaavuus**|Etsi yksi tai useampi arvo säännöllisen lausekkeen avulla. Tämä on samanlainen kuin **Alimerkkijono** ja **Säännöllinen lauseke -korvaa** -vaihtoehdot.|
|**Mukautettu**|Tämä on kehittynyt vaihtoehto, joka edellyttää apua kehittäjältä. Se mahdollistaa integrointitapahtuman, jonka voit tilata, jos haluat käyttää omaa muunnoskoodia. Jos olet sovelluskehittäjä ja haluat käyttää tätä vaihtoehtoa, katso alla olevaa kohtaa Kehittäjien vinkki: Esimerkki mukautetusta vaihtoehdosta.|
|**Päivämäärän ja ajan muotoilu**|Määritä, miten nykyinen päivämäärä ja kellonaika näytetään.|

#### <a name="tip-for-developers-example-of-the-custom-option"></a>Vinkki kehittäjille: Esimerkki mukautetusta vaihtoehdosta
Seuraavassa esimerkissä kuvataan, miten oma muunnoskoodi toteutetaan.

```
codeunit 60100 "Hello World"
{
    [EventSubscriber(ObjectType::Table, Database::"Transformation Rule", 'OnTransformation', '', false, false)]
    procedure OnTransformation(TransformationCode: Code[20]; InputText: Text; var OutputText: Text)
    begin
        if TransformationCode = 'CUST' then
            OutputText := InputText + ' testing';
    end;
}
```
Kun olet määritellyt säännöt, voit testata niitä. Kirjoita **Testi**-osaan esimerkki arvosta, jonka haluat muuttaa, ja tarkista sitten tulokset.

### <a name="to-export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Tietojenvaihtomäärityksen vieminen XML-tiedostona muiden käyttöä varten
Kun olet luonut tietojenvaihtomäärityksen tietylle datatiedostolle, voit viedä tietojenvaihtomäärityksen XML-tiedostona, joka voidaan tuoda. Tämä kuvataan seuraavassa menettelytavassa.  

1. Kirjoita **Haku**-ruutuun **Tietojenvaihtomääritykset** ja valitse aiheeseen liittyvä linkki.  
2. Valitse tietojenvaihtomääritys, jonka haluat viedä.  
3. Valitse **Vie tiedonsiirtomääritys** -toiminto.  
4. Tallenna XML-tiedosto, joka edustaa tietojenvaihtomääritystä tarvittavassa paikassa.  

    Jos tietojenvaihtomääritys on jo luotu, riittää, että tuot XML-tiedoston tietojen vaihtamiskehykseen. Tämä kuvataan seuraavassa menettelytavassa.  

### <a name="to-import-an-existing-data-exchange-definition"></a>Olemassa olevan tietojenvaihtomäärityksen tuominen  
1. Tallenna XML-tiedosto, joka edustaa tietojenvaihtomääritystä tarvittavassa paikassa.  
2. Kirjoita **Haku**-ruutuun **Tietojenvaihtomääritykset** ja valitse aiheeseen liittyvä linkki.  
3. Valitse **Uusi**-toiminto. **Tiedonsiirtomääritys**-sivu avautuu.  
4. Valitse **Tuo tiedonsiirtomääritys** -toiminto.  
5. Valitse vaiheessa 1 tallennettu tiedosto.  

## <a name="see-also"></a>Katso myös  
[Tiedonsiirron määrittäminen](across-set-up-data-exchange.md)  
[Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Maksujen kerääminen SEPA-suoraveloitusperintänä.](finance-collect-payments-with-sepa-direct-debit.md)  
[Maksujen suorittaminen AMC Banking 365 Fundamentals -laajennuksen tai SEPA-tilisiirron avulla](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]