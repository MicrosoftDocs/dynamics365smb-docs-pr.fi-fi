---
title: Palvelumääritys-laajennuksen määrittäminen ja käyttäminen
description: Opi määrittämään Palvelumääritys (Intrastat palveluille) -ominaisuudet ja raportoimaan muiden EU-maissa toimivien yritysten kanssa käyty palvelukauppa.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/21/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, service, declaration,'
ms.search.form: '30, 76, 5010, 5022, 5023, 5024, 5800'
---
# Palvelumääritys-laajennus

Joidenkin EU-maiden viranomaiset vaativat, että yritykset raportoivat muihin maihin viedyistä palveluista. **Palvelumääritys**-laajennuksen avulla voit kerätä tietoja palvelukaupasta EU:ssa ja raportoida siitä viranomaisille. Vaikka sen nimi **Palvelumääritys**, voit käyttää sitä myös **Intrastat palveluille** -ratkaisuna. Tämä laajennus on saatavilla kaikissa EU-maissa W1-versiona, ja sitä voidaan käyttää sellaisenaan Belgiassa. Muissa maissa tarvitaan maakohtainen laajennus. Jos maa tarvitsee vain eri formaatin, voit muuttaa formaattia **tiedonsiirtokehyksen** raporttikokoonpanon avulla.

## Palvelumääritys-laajennuksen ottaminen käyttöön

Kun olet asentanut laajennuksen ympäristöösi, sinun täytyy ottaa se käyttöön.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, avaa **Ominaisuuksien hallinta** ja valitse sitten vastaava linkki.
2. Etsi **Ominaisuus: Ota käyttöön palvelumäärityksen käyttö (Intrastat palveluille)** -vaihtoehto ja valitse **Käytössä:**-kentästä **Kaikki käyttäjät**. Lisätietoja ominaisuuksien hallinnasta on kohdassa [Tulevien ominaisuuksien käyttöönotto etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management) hallinann sisällössä.
3. Kun otat ominaisuuden käyttöön, sinun tulisi noudattaa ohjatun asennustoiminnon määritysprosessin vaiheita. Useimmat kentät on määritetty oletusarvoisesti.
4. Lisää vain **Palvelutapahtumatyypit**-kenttä toisessa vaiheessa valitsemalla **Avaa Palvelutapahtumatyypit-sivu ja määritä koodiluettelo** -vaihtoehto.
5. Tarkista **koodien kokonaismäärä** ennen aloittamista nähdäksesi, montako palvelutapahtumatyyppiä on jo määritetty.
6. Viimeistele määritys valitsemalla viimeisessä vaiheessa **Valmis**.

## Palvelumääritys-laajennuksen määrittäminen

Voit määrittää laajennuksen manuaalisesti tai käyttämällä tiedonsiirtomäärityksissä olevaa raportointitiedostoa.

### Palvelumäärityksen määrittäminen manuaalisesti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Palvelumäärityksen määritys** ja valitse sitten vastaava linkki.
2. Määritä **Yleiset**-pikavälilehdessä seuraavassa taulukossa kuvatut kentät:

    |Kenttä  |Kuvaus  |
    |---------|---------|
    |**Määrityksen nrosarja**     | Määrittää numerosarjan, jota käytetään tunnusten kohdistamiseen uusille tietueille.        |
    |**Raporttinimikekulut**  | Määrittää, täytyykö nimikekulut raportoida. Jos tämä vaihtoehto on käytössä, [!INCLUDE [prod_short](includes/prod_short.md)] tarkistaa nimikekulujen palvelutapahtuman koodin ja sisällyttää ne palvelumäärityksiin.        |
    |**Tilausasiakkaan/laskutusasiakkaan nro**     | Määrittää asiakkaan, jonka maakoodia verrataan **Yrityksen tiedot** -sivulla olevaan yrityksen koodiin. Palvelumääritykseen sisällytetään vain asiakirjat, joissa nämä kaksi koodia eivät ole samoja.<br><br>* **Laskutusasiakas**: Käytä **Laskutusasiakas**-kentästä saatua maakoodia <br<br>* **Tilausasiakas**: Käytä **Tilausasiakas**-kentästä saatua maakoodia.        |
    |**Tavarantoimittajan / tavaran laskuttajan nro**  | Määrittää tavarantoimittajan, jonka maakoodia verrataan **Yrityksen tiedot** -sivulla olevaan yrityksen koodiin. Palvelumääritykseen sisällytetään vain asiakirjat, joissa nämä kaksi koodia eivät ole samoja.<br><br> * **Tavarantoimittaja**: Käytä **Tavarantoimittaja**-kentästä saatua maakoodia. <br><br> * **Tavaran laskuttaja**: Käytä **Tavaran laskuttaja** -kentästä saatua maakoodia.         |
    |**Tiedonsiirtomäärityksen koodi**  | Määrittää tiedonsiirtomäärityksen koodin, jota käytetään palvelumäärityksen viedyn tiedoston luonnissa.        |
    |**Ota käyttöön verorekisterinumero**     |  Määrittää, onko **Verorekisterinumero** käytössä palvelumäärityksessä.       |

3. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Palvelutapahtumatyypit** ja valitse sitten vastaava linkki.
4. Määritä riveille **Koodit** ja **Kuvaukset** käyttämillesi maksutapahtumatyypeille.

### Määritä raportointitiedosto

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Tiedonsiirtomääritykset** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Kuvaa tiedonsiirronmääritelmää **Yleiset**-pikavälilehdessä määrittämällä datatiedoston tyyppi, sarakkeiden erotin, liittyvät koodiyksiköt ja XMLport sekä täyttämällä muut kentät.
4. Kuvaile **Rivimääritykset**-pikavälilehdessä datatiedoston rivien muotoilua täyttämällä kentät **rivityyppi**-kenttään ja missä sinun täytyy määrittää tämän rivin sarakkeiden määrä.
5. Täytä **Sarakemääritykset**-pikavälilehden kunkin suunniteltujen sarakkeiden rivi.
6. Valitse **kenttien vastaavuus** -toiminto **rivimääritykset**-pikavälilehdessä, kun haluat avata **kenttien vastaavuus** -sivun.
7. Luo uusi tapahtuma ja valitse **Yleiset**-pikavälilehdestä **Taulukon tunnus** (valitse **Palvelumäärityksen rivi** -kentälle **5024**) ja täytä sitten kentät seuraavalla tavalla:
   1. Määritä **Avainindeksi**-kenttään avainindeksi, jota käytetään lähdetietueiden lajittelemiseen ennen vientiä.
   2. Valitse **Vastaava Codeunit**.
8. Lisää **Kenttien vastaavuus** -pikavälilehdessä sarakkeet, jotka määritit aiemmin **Sarakemääritykset**-pikavälilehdessä, ja lisää sitten seuraavat:
   1. Määrittää kunkin sarakkeen **kenttätunnuksen**.
   2. Määritä **muunnossääntö** jokaiselle sarakkeelle tarvittaessa. Sääntö muuntaa tuodun tekstin tuetuksi arvoksi ennen kuin se voidaan yhdistää määritettyyn kenttään [!INCLUDE[prod_short](includes/prod_short.md)]-ratkaisussa. Kun valitset arvon tässä kentässä, täsmälleen sama arvo syötetään **Muunnossääntö**-kenttään **tiedonvaihto-kentän kartoituspuskuri** -taulukkoon ja päinvastoin.
9. Jos haluat ryhmitellä tapahtumat sarakkeiden perusteella, valitse **Kenttäryhmittely**-pikavälilehdestä kentät, joita haluat käyttää ryhmittelemiseen.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] sisältää esimääritetyn tiedonsiirtomäärityksen **palvelumääritystä** varten kaikille lokalisoiduille maille. Lisätietoja uuden tiedonsiirtomäärityksen luomisesta tai muuttamisesta on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).

## Muut asiaan liittyvät määritykset

Ennen kuin käytät Palvelumääritys-laajennusta, määritä nimikkeiden, resurssien ja nimikekulujen kentät.

### Nimikkeet

Määritä palvelumääritykseen liittyvät tiedot nimikkeiden korttien sivuilla:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet**, valitse sitten vastaava linkki.
2. Valitse kohde, jonka haluat määrittää.
3. Laajenna **Nimike**-pikavälilehti ja määritä seuraavat kentät:
   1. Valitse **Tyyppi**-kentästä **Palvelu**.
   2. Määritä **Palvelutapahtumatyypin koodi** -kenttään **palvelutapahtumatyypin** koodi.
   3. Jos et halua sisällyttää tätä palvelunimikettä palvelumäärityksiin, valitse **Sulje pois palvelumäärityksestä** -kenttä.

### Resurssit

Määritä palvelumääritykseen liittyvät tiedot resurssien korttien sivuilla:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Resurssit** ja valitse sitten vastaava linkki.
2. Valitse resurssi, jonka haluat määrittää.
3. Laajenna **Yleiset**-pikavälilehti ja määritä seuraavat kentät:
   1. Määritä **Palvelutapahtumatyypin koodi** -kenttään **palvelutapahtumatyypin** koodi.
   2. Jos et halua sisällyttää tätä resurssia palvelumäärityksiin, valitse **Sulje pois palvelumäärityksestä** -kenttä.

### Nimikekulut

Määritä palvelumääritykseen liittyvät tiedot nimikekuluille:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Nimikekulut** ja valitse sitten vastaava linkki.
2. Valitse nimikekulu, jonka haluat määrittää.
3. Määritä **Palvelutapahtumatyypin koodi** -kenttään **palvelutapahtumatyypin** koodi.
4. Jos et halua sisällyttää tätä nimikekulua palvelumäärityksiin, valitse **Sulje pois palvelumäärityksestä** -kenttä.

## Uuden palvelumäärityksen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Palvelumääritykset** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Yleiset**-pikavälilehdessä seuraavat kentät:
    1. Määritä **Määrityskoodi**-kenttään määrityskoodi, jota käytetään ehdottamaan rivejä ja luomaan tiedostoja. Sinun täytyy valita yksi **palvelumääritykseksi**.
    2. Määritä **Aloituspvm**- ja **Lopetuspvm**-kenttiin palvelumääritykseen sisällytettävän ajanjakson alkamis- ja päättymispäivät.
4. Valitse **Ehdota rivejä** -toiminto käynnistääksesi erätyön, joka kerää rivejä asiakirjasta ja täyttää palvelumäärityksen rivit.

Erätyö noutaa kaikki tapahtumat asiaankuuluvista osto- ja myyntiasiakirjoista vaaditulta ajanjaksolta ja lisää ne palvelumäärityksen riveille. Lue lyhyt kuvaus siirtämällä kohdistin riveillä olevien kenttien päälle.

## Palvelumäärityksen muokkaaminen

Voit tarvittaessa muokata rivejä tai lisätä uusia.

1. Valitse **Palvelumääritys**-sivulta **Uusi rivi** -toiminto **Rivit**-pikavälilehdestä.
2. Valitse **Asiakirjatyyppi**-kentästä haluamaasi asiakirjaan liittyvä vaihtoehto.
3. Täytä **Asiakirjanumero**-kenttä **Asiakirjatyyppi**-kentän perusteella.
4. Täytä jäljellä olevat kentät.

## Palvelumäärityksen rivien yleiskatsaus

Kun olet luonut palvelumäärityksen, käytä **Yleiskatsaus**-toimintoa nähdäksesi palvelumäärityksen rivien yleiskatsauksen. Voit ryhmitellä rivit ja tehdä niistä yhteenvedon samalla tavalla kuin viedyllä tiedostolla. Voit avata rivit myös Excelissä.

## Palvelumäärityksen raportointi tiedostossa

Voit lähettää palvelumäärityksen tiedostona, joka perustuu eri paikallisviranomaisten vaatimuksiin. Tiedoston luominen:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Palvelumäärityksen** ja valitse sitten vastaava linkki.
2. Valitse palvelumääritys, jonka haluat raportoida tiedostona.
3. Jos et ole jo tehnyt niin, täytä palvelumääritys manuaalisesti tai valitse **Ehdota rivejä** -toiminto.
4. Valitse **Luo tiedosto** -toiminto.
5. Palvelumäärityksen tiedosto tallennetaan vaaditussa muodossa.

## Muita huomioitavia seikkoja

Kun käytät **Palvelumääritys**-laajennusta, sinun tulisi huomioida muutama muu lisäseikka. On esimerkiksi tärkeää, että ryhmäsi vastaavat viranomaisten vaatimuksia. On myös tärkeää, että palvelut sisällytetään myynti- ja ostoasiakirjoihin oikein.

### Ryhmittelyrivit

Palvelumäärityksen riveillä ei ole ryhmittelyä minkään kentän mukaan. Kaikki tapahtumat kopioidaan käyttämällä alkuperäistä asiakirjaa lähteenä.

Viranomaisten edellyttämä ryhmittely annetaan viedyssä tiedostossa. Sinun täytyy määrittää ryhmät **tiedonsiirtomäärityksessä**, joka on täysin määritettävissä. Lisätietoja kohdassa [Tiedonsiirtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).

### Palveluiden käyttäminen asiakirjariveillä

Kun luot osto-, myynti- tai palvelulaskun, näkyvissä on kaksi kenttää, jotka liittyvät niiden riveillä oleviin palvelumäärityksiin. Molemmat kentät täytetään nimikkeiden, resurssien tai nimikekulujen määritysten oletusarvoilla.

- **Palvelutapahtumatyypin koodi** – Määrittää palvelutapahtumatyypin koodin.
- **Koskee palvelumääritystä** – Määrittää, koskeeko nimike tai resurssi palvelumääritystä.

Voit muuttaa näiden kenttien arvoja, mutta jos valitset **Koskee palvelumääritystä** -kentän, sinun täytyy määrittää arvo **Palvelutapahtumatyypin koodi** -kenttään. Jos et tee niin, et voi kirjata asiakirjaa.

Jos määrität arvon **Palvelutapahtumatyypin koodi** -kenttään, mutta et valitse **Koskee palvelumääritystä** -kenttää, voit kirjata asiakirjan, mutta riviä ei lasketa, kun teet niin.

## Lisätietoja aiheeseen liittyvästä koulutuksesta on [Microsoft Learnissa](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## Katso myös

[Intrastat-raportoinnin määrittäminen](finance-how-setup-report-intrastat.md)
[Intrastat-raportointi Business Centralissa](finance-how-report-intrastat.md)  
[Taloushallinto](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
