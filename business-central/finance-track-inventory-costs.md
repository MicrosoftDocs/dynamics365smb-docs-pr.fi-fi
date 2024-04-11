---
title: Nimikekustannusten muutosten seuraaminen
description: Tietoja nimikekustannustietojen pitämisestä tarkkoina nimikekustannusten muutosten seurannan avulla.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: null
ms.search.form: null
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="track-item-cost-adjustments"></a>Nimikekustannusten muutosten seuraaminen

On tärkeää, että nimikekustannukset pysyvät tarkkoina ja että tapahtuman kirjaamisen ja sen kustannuksen kirjanpidossa näkymisen väli lyhenee. Yksittäisten muutosajojen ja nimikkeiden kustannusten muutoksia voidaan seurata. Virhetilanteessa ongelmalliset nimikkeet voidaan tunnistaa ja korjaukset voidaan tehdä. Nimikkeitä voidaan esimerkiksi jättää pois laskelmista, mikä varmistaa, ettei muiden nimikkeiden muutokset keskeydy. Yksittäisten nimikkeiden kustannuksia voidaan muuttaa. Vaihtoehtoisesti voidaan luoda nimike-eriä, jotka sitten muutetaan samanaikaisesti.

## <a name="start-tracking-cost-adjustments"></a>Kustannusten muutosten seurannan aloittaminen

Aloittaminen on helppoa. **Varastonhallinnan asetukset** -sivun **Kustannusmuutoksen lokiinkirjaus** -kentässä on muutamia vaihtoehtoja:

* **Pois käytöstä** tarkoittaa, ettei kustannusten muutosajo kirjata lokiin.
* **Vain virheet** tarkoittaa, että vain epäonnistuneet ajot kirjataan lokiin.
* **Kaikki** tarkoittaa, että kaikki ajot kirjataan lokiin.

> [!NOTE]
> Lokin koon minimoinnin vuoksi [!INCLUDE [prod_short](includes/prod_short.md)] ei kirjaa lokiin muutoksia, jotka tapahtuvat automaattisesti, kun joku kirjaa nimikkeen.

Myös **Kirjaa varaston kustannus KP:oon (1002)** -työjonotapahtuma on määritettävä. Tämä työjonotapahtuma muuttaa kustannukset automaattisesti aikataulun mukaisesti. Lisätietoja työjonotapahtumista on kohdassa [Työjonojen käyttäminen tehtävien ajoittamisessa](admin-job-queues-schedule-tasks.md).

## <a name="manage-cost-adjustments"></a>Kustannusten muutosten hallinta

**Varastokustannusmuutos**-sivulla voi hallita ja seurata kustannusten muutosprosessia. Tällä sivulla on näkyvissä nimikkeet sekä niiden kustannuslaskennan parametrit ja kustannusmuutoksen tila. Luettelo voidaan suodattaa keskittymään nimikkeet, joita on muutettava tai jotka jätetty pois kustannusten muutosprosessista.

### <a name="about-item-batches"></a>Tietoja nimike-eristä

Useiden nimikkeiden kustannusten muutos voidaan suorittaa ryhmittelemällä nimikkeet eriksi. Erien avulla on helppo muuttaa nimikkeitä erikseen esimerkiksi siksi, että niiden muuttaminen kestää pitkään. Erät voivat myös auttaa tunnistamaan ongelmalliset nimikkeet.

Erä luodaan **Varastokustannusmuutos**-sivulla jollakin seuraavista tavoista:

* Valitse ensin nimikkeet luettelossa, sitten **Suorita kustannusmuutos** ja lopuksi **Lisää erä**.
* Erä voidaan luoda ja kustannuksen muutos suorittaa heti valitsemalla ensin nimikkeet luettelossa, sitten **Suorita kustannusmuutos** ja lopuksi **Lisää erä ja suorita**.
* Valitse ensin **Suorita kustannusmuutos** ja sitten **Nimike-erät** sekä syötä suodatin **Nimikesuodatus**-kentässä.
  
> [!TIP]
> Kaikille nimikkeille, jotka eivät vielä sisälly erään, voidaan luoda nopeasti toinen erä valitsemalla **Kustannusten muutos – Nimike-erät** -sivulla **Lisää puuttuvat nimikkeet**.

Kun erä on suoritettu, erän tilana on **Nimike-erät**-sivulla jokin seuraavista:

* **Onnistui**: kustannusten muutos onnistui.
* **Epäonnistui**: Jos kustannusten muutos epäonnistuu, [!INCLUDE [prod_short](includes/prod_short.md)] tunnistaa virheen aiheuttaneen nimikkeen ja jakaa valitun erän kahtia. Toisessa erässä ongelmallinen nimike ja toisessa kaikki muut nimikkeet. Kustannusten muutos suoritetaan uudelleen kaikki muut nimikkeet sisältävässä erässä. Jos epäonnistuu uudelleen, prosessi toistetaan. Jakojen enimmäismäärä määritetään **Yritysten enimmäismäärä** -kentässä. Uudelleenyritysten oletusarvo on 10, mutta sen tilalle voidaan syöttää uusi raja-arvo.
* **Aikakatkaistu**: Jos erän kustannusten muutos ei valmistu **Aikakatkaisu (minuuttia)** -kentässä (arvo voi olla 1–720 minuuttia) määritetyssä ajassa, istunto päättyy ja muutokset peruutetaan. [!INCLUDE [prod_short](includes/prod_short.md)] jakaa sitten valitun erän kahtia ja suorittaa kustannusten muutosprosessin kummallekin puolelle. Tämä prosessi jatkuu, kunnes muutos onnistuu tai uudelleenyritysten enimmäismäärä täyttyy.

> [VIHJE!] Kukin erä suoritetaan erillisenä istuntona. Edistymistä voi seurata **Päivitys**-toiminnolla.

### <a name="run-cost-adjustment"></a>Suorita kustannusmuutos

Muutoksia tehdään **Varastokustannusmuutos**-sivulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastokustannusmuutos** ja valitse sitten soveltuva linkki.
1. Seuraavat vaihtoehdot ovat käytettävissä sen mukaan, mitä halutaan tehdä:

  * Jos muutos halutaan tehdä yhdessä tai useassa nimikkeessä heti, nimikkeet valitaan ensin luettelossa ja sitten valitaan **Suorita kustannusmuutos**.
  * Erissä on käytettä yhtä seuraavista vaihtoehdoista:

    * Erä voidaan luoda ja kustannuksia muuttaa heti valitsemalla ensin nimikkeet luettelossa, sitten **Suorita kustannusmuutos** ja lopuksi **Lisää erä ja suorita**.
    * Kaikki erät voidaan suorittaa valitsemalla **Suorita kustannusmuutos**, **Nimike-erät** ja valitsemalla sitten **Ajo**.
    
    Lisätietoja eristä on kohdassa [Tietoja nimike-eristä](#about-item-batches).

### <a name="explore-item-details"></a>Nimikkeen tietoihin perehtyminen

**Nimike**-valikon kautta saadaan tietoja valitun nimikkeen kustannusten muutoksista.

* **Nimiketapahtumat**: Luettelo kunkin nimikkeen nimiketapahtumista. **Merkitse muutettavaksi** -toiminto mahdollistaa sellaisten nimikkeiden kustannusten muutoksen pakotetun suorittamisen uudelleen, jotka on linkitetty suoraan tai epäsuorasti valittuihin saapuviin tapahtumiin. Pakotetusta uudelleensuorituksesta voi olla hyötyä, jos edellisten suoritusten tuloksena oli virheelliset kustannukset.
* **Arvotapahtumat**: luettelo nimikkeen arvotapahtumista.
* **Kustannusmuutostapahtumien pisteet**: Avaa se **Keskim. kust. muutoksen tulopaikka** -sivu, jota ensisijaisesti käytetään keskimääräisen kustannuksen laskemiseen. Tällä sivulla on niiden nimikkeiden, sijaintien, varianttien ja arvostuspäivien yhdistelmiä, joille kustannusten muutoksia suoritetaan tai joille ne on suoritettava.
* **Kustannusmuutostilaukset**: Avaa **Varastonmuutostapahtuma (Tilaus)** -sivun, jossa muutetaan tuotanto- ja kokoonpanotilauksia. Näkyvissä on, onko tilauksia muutettu vai onko niitä muutettava.

### <a name="view-the-outcome"></a>Tuloksen tarkasteleminen

**Kirjaa loki suoritusta kohti** -valikon avulla voi tarkastella kustannusten muutosten tulosta:

* **Suorita**: Näyttää kunkin suorituksen kustannusten muutoslokit. Lokissa on tietoja nimikkeen suodattimesta, tilasta (onnistui, epäonnistui tai aikakatkaistu), alkamis- ja päättymispäivästä ja -ajasta sekä suorituksen tuloksena olevista kustannusten eroista.
* **Nimike**: näyttää tarkkoja tietoja valitun nimikkeen muutosprosessista.

### <a name="include-or-exclude-items-from-adjustments"></a>Nimikkeiden sisällyttäminen muutoksiin tai jättäminen pois niistä

Jos yksi tai usea nimike epäonnistui, nimikkeet voidaan jättää pois muutossuorituksesta ja sisällyttää ne sitten myöhempiin suorituksiin. **Toiminnot**-valikossa valitaan jompikumpi seuraavista:

* **Sulje nimike pois muutoksesta** ja **Sisällytä nimike muutokseen**: Poistaa valitun nimikkeen kustannuksen muutoksen väliaikaisesti käytöstä ja ottaa sen sitten uudelleen käyttöön: Kustannusten muutos jatkaa muiden nimikkeiden kustannusten pitämistä ajan tasalla samalla, kun tiettyyn nimikkeeseen liittyvää ongelmaa selvitetään.

## <a name="post-adjusted-costs-to-the-general-ledger"></a>Muutettujen kustannusten kirjaaminen pääkirjanpitoon

Uudet arvotapahtumat kirjataan yleensä pääkirjanpitoon **Kirjaa varaston kustannus KP:oon (1002)** -työjonotapahtuman aikataulun mukaisesti. Muutokset voidaan kuitenkin kirjata heti pääkirjanpitoon **Varastokustannusmuutos**-sivulta valitsemalla **Toiminnot**-valikossa **Varastokustannusmuutos**.

## <a name="troubleshoot-cost-adjustments"></a>Kustannusten muutosten vianmääritys

Kustannusten muutossuoritusten vianmääritys voidaan tehdä seuraavilla **Diagnostiikka**-valikon vaihtoehdoilla.

* **Vie nimiketiedot**: Nimikkeeseen liittyvät tiedot viedään tekstitiedostoon. Tiedostoa voidaan analysoida lisää eristysympäristössä tai se voidaan liittää tukipyyntöön kustannuslaskennan ongelmia selvitettäessä.
* **Tuo nimiketiedot**: Aiemmin viety tekstitiedosto tuodaan takaisin tietokantaan. Tämä toiminto on otettu käyttöön vain eristysympäristöissä tai arviointiyrityksissä.
* **Palauta Kustannus on muutettu**: Palauttaa nimikkeiden, tuotantotilausten ja kokoonpanotilausten **Kustannusta on muutettu** -vaihtopainikkeen. Tämä asetus mahdollistaa kustannusten muutoksen suorittamisen uudelleen niiden osalta.
* **Arvostusongelmien tunnistus -raportti**: Kustannuslaskennassa tyypillisesti laskentavirheitä aiheuttavien tieto-ongelmien diagnosointi. Se tarkistaa, ovatko nimiketapahtumat, arvotapahtumat, nimikkeen kohdistustapahtumat ja kapasiteettitapahtumat oikein.
* **Poista nimiketiedot**: Tyhjentää kaikki nimikkeeseen liittyvät taulukot tietokannassa. Tämä toiminto on saatavana vain eristysympäristöissä tai arviointiyrityksissä.

## <a name="see-also"></a>Katso myös

[Nimikekustannusten muuttaminen](inventory-how-adjust-item-costs.md)  
[Rakennetiedot: Kustannusten muutos](design-details-cost-adjustment.md)  
