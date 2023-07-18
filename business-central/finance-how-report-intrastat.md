---
title: Intrastat-raportoinnin käyttäminen
description: Opi raportoimaan muiden EU-maissa ja -alueilla toimivien yritysten kanssa käyty kauppa Intrastat-järjestelmän avulla.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
ms.date: 09/02/2022
ms.author: altotovi
---
# <a name="work-with-intrastat-reporting"></a>Intrastat-raportoinnin käyttäminen

Kaikkien Euroopan unionin (EU) alueen yritysten täytyy raportoida kaupastaan muiden EU-maiden/alueiden kanssa. Tavaran liikkuminen on raportoitava kotimaan/-alueen tilastoviranomaisille kuukausittain ja raportti on toimitettava veroviranomaisille. Intrastat on järjestelmä, jolla kerätään kauppatilastoja tavaroista näissä maissa/alueilla. **Intrastat-raportin** avulla voit suorittaa jaksoittaisen Intrastat-raportoinnin (tyypillisesti kuukausittain), keräämisen, kirjaamisen ja raportoinnin kauppatavaran paikallishallinnon lainsäädännön mukaisesti.

Intrastat-raportointi perustuu kaikkiin maihin ja alueisiin sovellettaviin EU:n perussäädöksiin. Käytännössä on kuitenkin eroja yksittäisten maiden ja alueiden välillä. Jokaisella maalla ja alueella on omat sääntönsä siitä, mitä ja miten tarkalleen raportoidaan.

> [!IMPORTANT]
> Tässä artikkelissa kuvataan uusi Intrastat-kokemus, joka on saatavilla [!INCLUDE[prod_short](includes/prod_short.md)]ssa vuoden 2022 julkaisuaalto 2:sta alkaen, jossa on lisätoimintoja ja [joka on kytkettävä olemassa oleville yrityksille](finance-how-setup-report-intrastat.md#enable-the-new-intrastat-experience). Ota yhteys järjestelmänvalvojaan ja määritä uusi ominaisuus.
>
> Lue edellisen version Intrastat-asetukset- ja käyttö-artikkeli kohdassa [Määritä ja raportoi Intrastat](finance-how-setup-report-intrastat-v20.md).

> [!NOTE]
> Intrastat-tietoja ei sovelleta maiden tai alueiden välisten palvelujen siirtoon, vaan vain tavaroihin (nimikkeisiin ja käyttöomaisuuteen). Jos paikallishallinto vaatii rekisteröimään palvelujen liikkumisen maiden ja alueiden välillä, se voidaan tehdä käyttämällä **Palvelumääritys**-toimintoa.
>
> Tällä hetkellä odotamme, että tämä ominaisuus on saatavilla marraskuusta 2022 alkaen sovelluksena osoitteessa [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Jos haluat käyttää sitä, sinun on ensin asennettava se **Laajennuksen hallinta** -sivulle.

## <a name="fill-in-the-intrastat-report"></a>Täytä Intrastat-raportti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-luettelo** ja valitse sitten vastaava linkki.
2. Luo uusi **Intrastat-raportti** valitsemalla **Uusi**-toiminto.
3. Jos **Intrastat-raporttia** varten täytyy syöttää sisäisiä tietoja, täytä nämä tiedot **kuvaus**-kenttään.
4. Valitse **Tilastojakso**-kentässä kuukausi, josta tiedot raportoidaan. Syötä jakso nelinumeroisena lukuna ilman välilyöntejä tai symboleita. Määritä maan tai alueen mukaan joko ensin kuukausi ja sitten vuosi tai päinvastoin. Anna esimerkiksi kesäkuulle 2022 joko luku *2206* tai *0622*.
5. Valitse **Ehdota rivejä** -toiminto. **Aloituspvm**- ja **Lopetuspvm**-kentissä on valmiina päivämäärät, jotka määriteltiin tilastokaudelle Intrastat-raportin otsikossa.
6. Voit syöttää **Epäsuorien kustann. pros.osuus** -kenttään prosentin (kattamaan kuljetus- ja vakuutuskustannuksia). Jos syötät prosentin, päiväkirjan **Tilastoarvo**-kentän sisältö on suhteellisesti korkeampi. Mutta jos haluat käyttää tätä ominaisuutta, sinun täytyy vaihtaa **summa sis. nimikekulut** -kentän arvoksi **Kyllä**.
7. Lisä konfiguraatioita voi määrittää myöhemmin **lisä**-pikavälilehdessä:
   1. **Ohita uudelleenlaskenta nollasummille**, jos haluat määrittää, että rivejä, joilla ei ole summaa, ei lasketa uudelleen eräajon aikana.
   2. **Ohita nollasummat** määrittääksesi, että ilman summia olevia nimiketapahtumia ei sisällytetä erätyöhön.
   3. **Näytä tuoteveloitusmerkinnät** määrittääksesi, haluatko näyttää välittömät kustannukset, jotka yrityksesi on määrittänyt ja kirjannut nimikekuluina.
   4. **Ohita laskuttamattomat merkinnät** määrittääksesi, jätetäänkö prosessista pois ne nimiketapahtumat, jotka on toimitettu tai vastaanotettu mutta joita ei ole vielä laskutettu.
8. Käynnistä eräajo valitsemalla **OK**.

Eräajo hakee kaikki tämän tilastokauden nimiketapahtumat ja lisää ne riveiksi **Intrastat-raportti**-riveille. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="modify-the-intrastat-report"></a>Muokkaa Intrastat-raporttia

Voit tarvittaessa muokata rivejä, mutta aina kun muutat arvoa Intrastat-raportin rivillä, **korjaus**-kentän arvoksi merkitään automaattisesti **kyllä**. Lopulta voit lisätä uuden rivin manuaalisesti, jos siihen on syy. Uuden rivin lisääminen manuaalisesti:

1. Valitse **Intrastat-raportti**-sivulla **uusi rivi** -toiminto **rivit**-pikavälilehdessä.
2. Valitse **Tyyppi**-kentässä **Vastaanotto** tai **Toimitus**.
3. Valitse **lähdetyyppi**-kentässä jokin lähteistä: **Nimiketapahtuma**, **KO-tapahtuma** tai **Työtapahtuma**.
4. **Nimikkeen nro** -kentän **Lähdetyypin** perusteella voidaan valita **Nimike** (molemmissa tapauksissa, **Nimiketapahtuma** tai **Projektitapahtuma**) tai **käyttöomaisuus**.
5. Täytä muut Intrastat-raportointiin tarvittavat kentät.

> [!NOTE]
> Kun lisäät uuden rivin Intrastat-raporttiin manuaalisesti, rivin **pvm**-kentän tulee olla otsikossa lisäämäsi **tilastojakson** sisällä.

## <a name="validate-intrastat-lines"></a>Tarkista Intrastat-rivit

Kun olet täyttänyt **Intrastat-ilmoituksen**, voit suorittaa **Tarkistusluettelo-raportti**-toiminnon ja varmistaa, että kaikki **Intrastat-ilmoituksen** tiedot ovat oikein. **Intrastat-tarkistusluettelo**-sivulla määritetyt pakolliset kentät, joissa ei ole arvoja, näytetään **Virheet ja varoitukset** -tietoruudussa **Intrastat-kirjaus**-sivulla.

Suorittamalla **Intrastat-raportin tarkistusluettelo** -raportin voit tarkistaa Intrastat-rivit ennen niiden viemistä vaaditussa muodossa. Tarkistus suoritetaan **Intrastat-raportin** sisällä.

## <a name="recalculating-weight-or-supplementary-unit-of-measure"></a>Painon tai täydentävän mittayksikön uudelleenlaskenta

Jos sait virheilmoituksen *Kokonaispaino Intrastat-raportin rivillä ei saa olla tyhjä*, se johtuu todennäköisesti siitä, että et ole määrittänyt käytetylle lähteelle, nimikkeelle tai käyttöomaisuudelle **Nettopaino**-kenttää. Etsi tässä tapauksessa nimike tai käyttöomaisuuden kortti ja lisää tarvittava arvo. Sen jälkeen sinun tarvitsee vain avata **Intrastat-raportti** uudelleen ja noudattaa seuraavia vaiheita:

1. Valitse **Uudelleenlask. paino/lisä UOM** -toiminto, joka laskee **kokonaispainon** ja/tai **lisämäärän** uudelleen.
2. Valitse yksi vaihtoehdoista:

    1. **Paino** – lasketaan uudelleen vain **kokonaispaino** nimikkeen ja käyttöomaisuuden korttien **nettopainoa** koskevien tämänhetkisten tietojen perusteella.
    2. **Täydentävä UOM. määrä** – lasketaan uudelleen vain **Intrastat-raportti**-rivin **lisämäärä**, jos se on olemassa, perustuen nimikkeen ja käyttöomaisuuden korttien **täydennysosan** nykyisiin tietoihin.
    3. **MOlemmat** – lasketaan uudelleen sekä **kokonaispaino** ja **lisämäärä**, nimikkeiden ja käyttöomaisuuden tämänhetkisten tietojen perusteella.
3. Käynnistä eräajo valitsemalla **OK**.

## <a name="report-intrastat-in-a-file"></a>Intrastat-raportointi tiedostona

Voit lähettää Intrastat-raportin tiedostona, joka perustuu eri paikallisviranomaisten vaatimuksiin. Ennen kuin luot tiedoston, tarkista, että kaikki rivit sisältävät kaikki tarvittavat ja kelvolliset tiedot, suorittamalla **tarkistusluetteloraportin**. Tiedoston luominen:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-luettelo** ja valitse sitten vastaava linkki.
2. Valitse **Intrastat-raportti**, jonka haluat raportoida tiedostona.
3. Jos et vielä ole tehnyt tätä, täytä **Intrastat-raportti** manuaalisesti tai valitsemalla **Ehdota rivejä** -toiminto.
4. Valitse **Luo tiedosto** -toiminto.
5. Intrastat-tiedosto tallennetaan vaaditussa muodossa.

Kun olet luonut tiedoston, [!INCLUDE[prod_short](includes/prod_short.md)] täyttää automaattisesti seuraavat raportoinnin tiedot:

* **Vientipäivä** määrittää päivämäärän, jolloin raportti on viety.
* **Vientiaika** määrittää ajan, jolloin raportti on viety.

> [!NOTE]
> Kun seuraavan kerran luot tiedoston, **Vie päivämäärä**- ja **Vie aika** -kentissä säilytetään tietoja vain viimeisestä luodusta tiedostosta.

## <a name="intrastat-rules"></a>Intrastat-säännöt

### <a name="grouping-lines"></a>Ryhmittelyrivit

**Intrastat-raportti**-riveillä ei ole ryhmittelyä minkään kentän mukaan. Kaikki tapahtumat kopioidaan alkuperäisestä lähteestä, joten voit etsiä ne nopeasti **lähdetyypin** ja **lähdetapahtumanumeron** yhdistelmän perusteella.

Viranomaisten edellyttämä ryhmittely annetaan viedyssä tiedostossa. Tämä täytyy määrittää **Tiedonvaihtomäärityksessä**, joka on täysin määritettävissä. Lisätietoja kohdassa [Tiedonsiirtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).

### <a name="fixed-assets-reporting"></a>Käyttöomaisuuden raportit

Käyttöomaisuuserät näkyvät Intrastat-riveillä vain, jos:

* **KO:n kirjaustyyppi** **ALV-tapahtuma**-kentässä on **hankintameno** ja jos **asiakirjatyyppi** on **lasku** ostojen ollessa kyseessä ja
* **KO:n kirjaustyyppi** **ALV-tapahtuma**-kentässä on **Jatkuu luovutuksessa** ja jos **asiakirjatyyppi** on **lasku** myynnin ollessa kyseessä.

### <a name="intrastat-report-statuses"></a>Intrastat-raportin tilat

Kun käsittelet **Intrastat-raporttia**, asiakirjan otsikossa näkyy **tila**-kenttä. Voit löytää seuraavat tilat yhdessä asiaan liittyvien sääntöjen kanssa:

* *Avaa*: Tämä tila luodaan automaattisesti, kun luot uuden Intrastat-raportin, ja voit tehdä kaikki toiminnot tässä tilassa.
* *Vapautettu*: [!INCLUDE[prod_short](includes/prod_short.md)] muuttaa tilaksi automaattisesti *vapautettu*, kun luot tiedoston. Tästä hetkestä lähtien **Intrastat-raporttia** ei voi muuttaa. Jos sinun täytyy muuttaa jotain ja raportoida uudelleen, voit avata Intrastat-raportin uudelleen **avaa uudelleen** -toiminnon avulla. Kun asiakirja on avattu uudelleen, voit vapauttaa asiakirjan uudelleen **vapautus**-toiminnon avulla.
* **Raportoitu**: Määrittää, onko tapahtumasta jo raportoitu veroviranomaisille. Tämä ei ole tavallinen tila, mutta itsenäinen kenttä, ja vaikka olisit avannut uudelleen Intrastat-raportin, se silti näyttää, että tiedosto on jo luotu tälle raportille.

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvästä koulutuksesta on [Microsoft Learnissa](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a>Katso myös

[Intrastat-raportoinnin määrittäminen](finance-how-setup-report-intrastat.md)  
[Taloushallinto](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
