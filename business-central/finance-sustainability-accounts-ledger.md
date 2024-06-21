---
title: Vastuullisuustilien ja -kirjanpidon tilikartta
description: 'Tutustu kestävyystilikartan, -luokat- ja alaluokkien hallintaan sekä kestävyystapahtumien yksityiskohtiin.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Kestävyystilien tilikartta ja kirjanpito

## Kestävyystilien tilikartta

Kestävyystilikartta (CoSA) muodostaa perustavan rakenteen luettelon, jota käytetään kaikkien päästötietojen tallentamiseen. Se toimii kehyksenä, joka luokittelee ja järjestää kestävyystilit niiden määritteiden, kuten laajuuden tai muiden ryhmittymien, perusteella. Jokaiseen tiliin on yleensä liitetty yksilöivä koodi tai numero, jotta siihen on helppo viitata ja seurata sitä. Sillä on sama rakenne kuin perinteisellä tilikartalla, mutta se on räätälöity erityisesti kestävyyteen liittyvien tietojen ja mittareiden seurantaa varten organisaatiossa.

Käyttäjät voivat lisätä kestävyystilien luokkia ja kestävyystilien aliluokkia määrittääkseen, miten järjestelmä käyttäytyy. Tällä tavalla he voivat valita seurattavia päästöjä, päästökertoimia, kaavoja ja vastaavia määrityksiä.

> [!NOTE]
> Kasvihuonekaasu (GHG) -standardeihin perustuen on olemassa kolme päästöaluetta:
>
> - **Vaikutusalueen 1 päästöihin** kuuluvat kiinteistä ja liikkuvista polttolähteistä sekä tahattomista hajapäästöistä johtuvat päästöt.
> - **Vaikutusalueen 2 päästöihin** kuuluvat epäsuorat päästöt, jotka aiheutuvat palveluntarjoajilta ostetun energian muodostamisesta.
> - **Vaikutusalueen 3 päästöihin** kuuluu laaja kirjo päästöjä ostetuista tavaroista ja palveluista sekä pääomahyödykkeistä, polttoaineeseen ja energiaan liittyvistä toiminnoista, alku- ja loppupään kuljetuksista, syntyvästä jätteestä, liikematkoista ja työntekijöiden työmatkoista jne.

CoSA:sta voit tehdä esimerkiksi:

- Voit tarkastella kestävyyskirjanpitotapahtumat- ja saldot näyttäviä raportteja.
- Voita avata kestävyystilikortin asetusten lisäämistä tai muuttamista varten.
- Tarkastella tilin luokkaa ja alaryhmää. 
- Yksittäisen tilin kunkin päästön erillisten saldojen tarkastelu.
- Lisää yksi tai useampi dimensio kuhunkin tiliin ja aseta dimensiosuodatukset.

Voit lisätä, muuttaa tai poistaa kestävyystilejä. Erojen estämiseksi et voi poistaa Kestävyystiliä, jos siihen liittyy yksi tai useampia tapahtumia.

### Lisää tai muuta tilejä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kestävyystilikartta** ja valitse sitten vastaava linkki.
2. **Kestävyystilikartta**-sivulla voit avata jokaisen kestävyystilin ja lisätä tai muuttaa asetuksia. Lue lyhyt kuvaus siirtämällä kohdistin kentän päälle.

**Summa**-tyyppisten tilien osalta sinun täytyy määrittää **Summausväli**-kenttä.

**Loppusumma**-tyyppisille tileille sisennys-toiminto asettaa automaattisesti **Summaus**-kentän. Kun olet määrittänyt kaikki tilit, suorita Sisennys-toiminto valitsemalla **Sisennä kestävyystilikartta** -toiminto ja aseta **Summausväli**-kenttä.

> [!IMPORTANT]
> Sisennys-funktio korvaa **Loppusumma**-tilien kaikkien kenttien arvon. Tästä syystä, jos olet antanut määritelmiä **Loppusumma**-tilien **Summausväli**-kenttiin ennen sisennyksen suorittamista, määritelmät on annettava uudelleen.

### Poista tilejä

Voit poistaa kestävyystilin. Varmista kuitenkin ensin, ettei siihen liity kirjanpitotapahtumia. Business Central estää sinua poistamasta kestävyystiliä, jos siihen on liitetty yksi tai useampi kirjanpitotapahtuma.

## Tililuokat

Käyttäjät voivat lisätä kestävyystilien luokkia ja kestävyystilien aliluokkia määrittääkseen, miten järjestelmä käyttäytyy. He voivat valita päästöalueita, seurattavia päästöjä, kaavoja ja vastaavia määrityksiä.

Voit tarkistaa kestävyystililuokat noudattamalla seuraavia vaiheita:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kestävyystililuokat** ja valitse sitten vastaava linkki.
2. **Kestävyystilin luokat** -sivulla voit muokata aiemmin luotua luetteloa tai luoda uuden luokan. Luo uusi luokka valitsemalla **Uusi**-toiminto.
3. Määritä **Koodi**- ja **Kuvaus**-kentät.
4. Valitse yksi vaikutusalueen vaihtoehdoista **Päästöalue**-kentässä.
5. Valitse seurattavat kaasupäästöt. Tällä hetkellä seuraavat vaihtoehdot ovat saatavilla: **CO2**, **CH4** ja **N2O**. Voit valita minkä tahansa seurattavan yhdistelmän, mutta valittuna tulee olla vähintään yksi päästö.
6. **Laskentaperuste**-kentässä voidaan valita päästöjen laskennassa käytettävä laskentaperuste (kaava), jos et tiedä tarkkaa päästösummaa. Voit valita jonkin seuraavista vaihtoehdoista: **Polttoaine/sähkö**, **Etäisyys**, **Asennus** tai **Mukautettu**.

    > [!NOTE]
    > Jos tämä saatavilla olevien kaavojen sarja **Laskentaperuste**-kentässä ei riitä, voit laajentaa kenttää ja lisätä laskelmia järjestelmään, jota käytetään kestävyyspäiväkirjoissa.

7. Jos valitsit **Laskentaperuste**-kentässä **Mukautettu**, mukautettu kuvaus voidaan määrittää **Mukautettu arvo** -kentässä.

Jos **Laskentaperuste**-kenttä määritetään, seuraavassa taulukossa selitetään, miten järjestelmä laskee päästöt valitsemasi vaihtoehdon perusteella. (Tässä taulukossa *EF* kuvaa **Päästökerroin**-arvoa, jonka voit määrittää **Kestävyystilin alaryhmä** -sivulla.)

| Päästön tyyppi | Laskentaperuste | Kaava | Kommentti |
|---------------|------------------------|---------|---------|
| **Laajuus 1** | | | |
| Kiinteät polttolähteet | Polttoaine/sähkö | *Päästöt* = *Polttoaine* &times; *EF* | *Polttoaine* = Kattiloiden, lämmittimien ja lämpöhapettimien jne. polttoaineen määrä |
| Liikkuvat polttolähteet | Polttoaine/sähkö | *Päästöt* = *Polttoaine* &times; *EF* | *Polttoaine* = Maantie- tai ei-maantieajoneuvoihin, rautatieajoneuvoihin käytetyn jne. polttoaineen määrä |
| | | *Päästö* = *Etäisyys* &times; *EF* | *Etäisyys* = Maantie- tai ei-maantieajoneuvojen, rautateiden jne. mittarilukema |
| Hajapäästöt | Asennus | *Päästöt* = *Asennuskerroin* &times; *Mukautettu määrä* &divide; 100 &times; *Aikakerroin* | *Mukautettu määrä* = Kokoonpanotappiot, Vuosittainen vuotamisprosentti jne. |
| **Laajuus 2** | | | |
| Yleishyödylliset palvelut | Polttoaine/sähkö | *Päästöt* = *Sähkö* &times; *EF* | *Polttoaine/Sähkö* = Sähkömäärä, Höyrymäärä, Lämmitysyksikkö jne. |
| | Mukautettu | *Päästöt* = *Mukautettu määrä* &times; *EF* | *Mukautettu määrä* = Lämpöyksikkö, Tonnitunti jne. |
| **Laajuus 3** | | | |
| Ostetut tavarat ja palvelut sekä tuotantohyödykkeet | Mukautettu | *Päästöt* = *Mukautettu määrä* &times; *EF* | *Mukautettu määrä* = Kustannus (KP) jne. |
| Alkupään kuljetus ja jakelu | Etäisyys | *Päästö* = *Etäisyys* &times; *EF* | |
| | Etäisyys | *Päästö* = *Etäisyys* &times; *Kerroin* &times; *EF* | *Kerroin* = Lastin tonnit |
| Loppupään kuljetus ja jakelu | Etäisyys | *Päästö* = *Etäisyys* &times; *EF* | |
| | Etäisyys | *Päästö* = *Etäisyys* &times; *Kerroin* &times; *EF* | *Kerroin* = Lastin tonnit |
| Myytävien tuotteiden toiminnassa ja loppukäsittelyssä syntyvät jätteet | Mukautettu | *Päästöt* = *Mukautettu määrä* &times; *EF* | *Mukautettu määrä* = Jäte |
| Liikematkustus ja työntekijöiden työmatkustus | Etäisyys | *Päästö* = *Etäisyys* &times; *EF* | *Etäisyys* = Käytetyn työsuhdeauton mittarilukema, vuokra-auto, juna, lento jne. |
| | Mukautettu | *Päästöt* = *Mukautettu määrä* &times; *EF* | *Mukautettu määrä* = Hotellimajoitus jne. |
| | Polttoaine/sähkö | *Päästöt* = *Polttoaine* &times; *EF* | *Polttoaine* = Yrityksen autoon, vuokra-autoon käytetyn polttoaineen määrä jne. |

## Tilin aliluokat

Käyttäjien on lisättävä kestävyystilin alaluokka jokaiseen kestävyystiliin. Tämä alaryhmä määrittää kaavoissa käytettävät päästötekijät kestävyystilikategorian päästöjen seurannan valinnan perusteella.

Voit tarkistaa kestävyystilin alaluokat noudattamalla seuraavia vaiheita:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kestävyystilin alaluokat** ja valitse sitten vastaava linkki. 
2. **Kestävyystilin alaluokat** -sivulla voit muokata aiemmin luotua luetteloa tai luoda uuden luokan. Luo uusi luokka valitsemalla **Uusi**-toiminto.
3. Määritä **Koodi**- ja **Kuvaus**-kentät.
4. Kestävyystililuokassa seurattavien kaasupäästöjen perusteella ja tämän alakategorian liittämiseksi voit määrittää myös yhden tai useamman päästötekijän: 

    - **Päästökerroin CO2** – Hiilidioksidipäästöjen päästökerroin (CO<sub>2</sub>).
    - **Päästökerroin CH4** – Metaanin päästökerroin (CH<sub>4</sub>).
    - **Päästökerroin N2O** – Typpioksiduulipäästöjen päästökerroin (N<sub>2</sub>).

5. Jos alaryhmä liittyy uusiutuvaan energiaan, valitse **Uusiutuva energia** -kenttä.

> [!NOTE]
> **Tuo tiedot**- ja **Tuo kohteesta** -kentät on tarkoitettu mahdolliseen integrointiin ulkoisten järjestelmien kanssa, joita käytetään päästöjen kertymiseen. **Vuoden 2024 julkaisuaallossa 1** näitä kenttiä ei kuitenkaan voi käyttää oletusarvoisesti ominaisuutena.

## Vastuullisuustapahtumat

Kestävyyskirjaukset tallentavat kaikkien kirjattujen kestävyystransaktioiden historian ja organisoivat kaikki päästötiedot kestävyystilikartan (CoSA) mukaan. Kun käyttäjä kirjaa kestävyyspäiväkirjan, kaikki ratkaisevat tiedot tallennetaan sinne. Kaikki aktiiviset raportit on luotu kestävyyskirjaustapahtumien perusteella.

Kun haluat avata tämän kirjanpidon tietylle tilille, käytä **Kestävyystilin kaavio** -sivulla olevaa **Tapahtumakirjaukset**-toimintoa. Avataksesi kaikki kirjanpitotapahtumat valitse ![Lamppu, joka avaa toisena Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kestävyyskirjaustapahtumat** ja valitse sitten vastaava linkki. Lue lyhyt kuvaus siirtämällä kohdistin kentän päälle.

> [!IMPORTANT]
> Kun olet kirjannut tiedot kestävyystapahtumiin, et voi poistaa sitä. Jos teit virheen, voit kirjata vastakirjauksen käyttäen samoja yksityiskohtia, mutta käyttämällä summalle negatiivista merkkiä.

## Katso myös

[Taloushallinto](finance.md)  
[Vastuullisuuden hallinnan yleiskatsaus](finance-manage-sustainability.md)  
[Vastuullisuusmääritys](finance-sustainability-setup.md)  
[Toimintaohje: päästöjen kirjaus](finance-sustainability-journal.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
