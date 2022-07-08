---
title: Vaihekuvaus – Sarja-/eränumeroiden jäljitys
description: Tässä aiheessa kuvataan toimet, joita tarvitaan viallisen nimikkeen myymisen estämiseksi, sekä se, miten nimikkeitä voidaan jäljittää ja peruuttaa tarpeen mukaan.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: bholtorf
ms.openlocfilehash: b7e2ae55e231cdadf02a0a8e91f6d3ad066a0cb5
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9075222"
---
# <a name="walkthrough-tracing-seriallot-numbers"></a>Vaihekuvaus: Sarja-/eränumeroiden jäljitys

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Kun virheellisiä tuotteita havaitaan, on tarpeen määrittää virheet ja estää virheellisiä nimikkeitä lähtemästä yrityksestä. Jos virheellisiä nimikkeitä on jo lähetetty, on selvitettävä, kuka vastaanotti kyseiset nimikkeet ja pitääkö ne kutsua takaisin.  

Vikojenhallinnan ensimmäinen tehtävä on tutkia mistä viallisten nimikkeiden olivat peräisin ja missä niitä käytettiin. Tämä tutkimus perustuu historiatietoihin ja se helpottaa hakua nimikeseurantatapahtumista **Nimikkeen jäljitys** -sivun avulla.  

Toisessa vaiheessa määritetäänkö, onko jäljitettyjä nimikkeitä käytetty suunnitteluun avoimissa asiakirjoissa, kuten kirjaamattomissa myyntitilauksissa tai kulutuspäiväkirjoissa. Tämä työ tehdään **Etsi tapahtumat**-sivulla. Etsi merkintöjä -toiminnon avulla voit etsiä kaikenlaisia tietokantatietueita.  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta

Tässä vaihekuvauksessa kuvataan, miten virheelliset nimikkeet määritetään. Lisäksi selvitetään, mikä toimittaja toimitti virheelliset nimikkeet ja missä niitä on käytetty, joten tilaukset voidaan pysäyttää tai kutsua takaisin.  

Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

- jäljittäminen käytöstä alkuperään  
- jäljittäminen alkuperästä käyttöön  
- jäljitetyn sarja-/eränumeron sisältävien tietueiden hakeminen.  

## <a name="roles"></a>Roolit

Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:  

- Laadunvalvontapäällikkö  
- Varastopäällikkö  
- Tilausten käsittelijä  
- Ostaja  

## <a name="prerequisites"></a>Vaatimukset

Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:  

- [!INCLUDE[prod_short](includes/prod_short.md)] -yritys.  
<!-- - To create new items and several business transactions by following the [Prepare Sample Data](walkthrough-tracing-serial-lot-numbers.md#prepare-sample-data).   -->

## <a name="story"></a>Taustatietoja

Laatupäällikkö Riku käsittelee nimikkeen 1002, Kilpapyörä, myyntipalautusta. Asiakas Tinayhtymä Oy lähetti valituksen, jonka mukaan kilpapyörän rungon hitsaussaumat ovat murtuneet. Laadunvalvontainsinöörit ovat vahvistaneet, että palautetun pyörän runko on vioittunut. Laatupäällikön on nyt määritettävä seuraavat seikat:  

- mikä runkoerä oli virheellinen  
- mikä ostotilaus tuotti virheellisen erän.  

Myyntiosastolta kerrotaan laatupäällikölle, että palautetun kilpapyörän (nimike 1002) sarjanumero on Snro1. Käyttämällä näitä perustietoja hänen selvitettävä, missä valmista kilpapyörää on viimeksi käytetty, ja sitten hänen on jäljitettävä taaksepäin aikaisimpaan alkuperään muodostaakseen eränumeron, josta viallinen osa (kilparunko) on tullut.  

Nimikkeen jäljityksen ensimmäisen tehtävän tulokset ilmaisevat, mitkä kilpapyörän rungot olivat viallisia ja miltä toimittajalta ne ovat peräisin. Myöhemmin saman jäljitysprosessin aikana laatupäällikön on etsittävät kaikki myydyt kilpapyörät, joihin käytettiin viallisesta erästä peräisin olevia kilpapyörän runkoja, jotta nämä tilaukset voidaan pysäyttää tai kutsua takaisin. Lopuksi laatupäällikön on etsittävä kaikki avoimet asiakirjat, joissa viallista erää käytetään, jotta niissä ei suoriteta enempää tapahtumia.  

Vianhallinnan kaksi ensimmäistä tehtävää tehdään **Nimikkeen jäljitys** -sivulla. Viimeinen tehtävä tehdään **Etsi tapahtumat**- ja **Nimikkeen jäljitys** -sivuilla.  

## <a name="prepare-sample-data"></a>Esimerkkitietojen valmisteleminen

Sinun on luotava seuraavat uudet kohteet:  

- 2000, Kilpapyörän runko: eräkohtainen jäljitys, nimikkeen 1002 komponentti  
- 1002, Kilpapyörä: sarjanumerokohtainen jäljitys.  

Seuraavaksi näille kahdelle nimikkeelle luodaan osto-, tuotanto- ja myyntitilauksia.  

### <a name="to-create-the-items"></a>Nimikkeiden luominen  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Valitse **Nro**-kenttään **2000** ja täytä sitten seuraavat kentät.  

    |Kuvaus|Perusmittayksikkö|Yl. Tuotteen kirjausryhmä|Tuotteen ALV-kirjausryhmä|Varaston kirjausryhmä|Nimikkeen seurantakoodi|  
    |-----------|--------------------|------------------------|-----------------------|--------------------|------------------|  
    |Kilpapyörän runko|KPL|RAAKA-AINE|ALV25|RAAKA-AINE|T.ERÄTKKKI|  

    > [!NOTE]  
    >  Syötä perusmittayksikkö valitsemalla **Uusi** -painike ja valitse sitten **PSC** **Nimikkeen mittayksiköt** -sivulla.  

4. Muiden kenttien oletusarvot voidaan hyväksyä, tai niitä ei tarvitse täyttää.  
5. Luo ensimmäisen uuden nimikkeen (2000) kortti valitsemalla **OK**.  
6. Valitse **Uusi**.  
7. Valitse **Nro**-kenttään **1002** ja täytä sitten seuraavat kentät.  

    |Kuvaus|Perusmittayksikkö|Yl. Tuotteen kirjausryhmä|Tuotteen ALV-kirjausryhmä|Varaston kirjausryhmä|Täydennysjärjestelmä|Nimikkeen seurantakoodi|  
    |-----------------|--------------------------|------------------------------|-----------------------------|-----------------------------|--------------------------|------------------------|  
    |Kilpapyörä|KPL|VÄH.MYYNTI|ALV25|VALMIS|Tuotantotilaus|SNROKAIKKI|  

    > [!NOTE]  
    >  Syötä perusmittayksikkö valitsemalla **Uusi** -painike ja valitse sitten **PSC** **Nimikkeen mittayksiköt** -sivulla.  

    Määritä seuraavaksi nimikkeen tuotannon asetukset.

8. Anna **Täydennys**-pikavälilehden **Reititysnro**-kenttään **1000**.  
9. Valitse ensin **Tuotannon tuoterakenteen nro**-kenttä ja sitten **Lisäasetukset**.  
10. Valitse **Tuotannon tuoterak. luettelo** -sivulla ensimmäinen rivi, **1000**, ja valitse sitten **Muokkaa**.  
11. Muuta **Tuotannon tuoterakenne** -sivun **Tila**-kentän arvoksi **Kehityksen alla**.  
12. Siirry tyhjälle riville, kirjoita **2000** **Nro**-kenttään ja **1** **Määrä per** -kenttään.  
13. Muuta **Tila**-kentän arvoksi jälleen **Hyväksytty**.  
14. Valitse **OK**-painike lisätäksesi tuoterakenteen nimikkeen korttiin, ja sulje **Tuotannon tuoterakenne** -sivu.  

    Osta seuraavaksi kilpapyörän runkoja Pyöräliike Oy:ltä.  

### <a name="to-purchase-components"></a>Osta osia

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Luo ostotilaus toimittajalle, Custom Metals Incorporated, täyttämällä seuraavat rivikentät.  

    |Vaihtoehto|Määrä|Eränro|  
    |----|--------|-------|  
    |2000|10|ERÄ1|  

4. Anna eränumero valitsemalla **Nimikkeen seurantarivit** -toiminto.  
5. Täytä **Nimikkeen seurantarivit** -sivulla **Eränro**- ja **Määrä (perus)** -kentät ja sulje sivu.  
6. Anna **Toimittajan laskunro** -kentässä arvo.  
7. Valitse ensin **Kirjaa**-toiminto, sitten **Vastaanota ja laskuta** -asetus ja lopuksi **OK**.  

    Osta seuraavaksi kilpapyörän runkoja Huippupuu-tekniikalta.  
8. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.  
9. Valitse **Uusi**-toiminto.
10. Luo ostotilaus toimittajalle, Coolwood Technologies, täyttämällä seuraavat rivikentät.  

    |Nimike|määrä.|Eränro|  
    |----------|--------------|-------------|  
    |2000|11|ERÄ2|  

11. Anna eränumero valitsemalla **Rivit** -pikavälilehden **Rivi**-ryhmässä **Nimikkeen seurantarivit** -toiminto.  
12. Täytä **Nimikkeen seurantarivit** -sivulla **Eränro**- ja **Määrä (perus)** -kentät ja sulje sivu.  
13. Anna **Toimittajan laskunro** -kentässä arvo.  
14. Valitse ensin **Kirjaa**-toiminto, sitten **Vastaanota ja laskuta** -asetus ja lopuksi **OK**.  

    Tuota seuraavaksi kaksi kilpapolkupyörää, Snro1 ja Snro2.  

### <a name="to-produce-end-items"></a>Tuota lopullisia nimikkeitä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vapautetut tuotantotilaukset** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-ryhmä.  
3. Luo uusi vapautettu tuotantotilaus täyttämällä seuraavat kentät.  

    |Lähteen nro|määrä|Sarjanumero|  
    |----------|--------|----------|  
    |1002|2|Snro1|  
    |1002|2|Snro2|  

4. Täytä rivi valitsemalla ensin **Päivitä tuotantotilaus** -toiminto ja sitten **OK**.  
5. Anna sarjanumerot valitsemalla **Nimikkeen seurantarivit** -toiminto.  
6. Täytä **Nimikkeen seurantarivit** -sivulla **Sarjanro**- ja **Määrä (perus)** -kentät ja sulje sivu.  

    Seuraavaksi on tarpeen kirjata ERÄ1:n kilpapyörän runkojen kulutus.  
7. Valitse **Vapautettu tuotantotilaus** -sivulla **Tuotantopäiväkirja** -toiminto.  
8. Valitse ensin **Tuotantopäiväkirja**-sivulla nimikkeen 2000 kulutusrivi ja sitten **Nimikkeen seurantarivit** -toiminto.
9. Valitse **Nimikkeen seurantarivit** -sivulla ensin **Eränro**-kenttä ja sitten **ERÄ1** ja lopuksi **OK**.  
10. Älä muuta muita **Tuotantopäiväkirja** sivun oletusasetuksia. Valitse sitten **Kirjaa**-toiminto.  

    Tuota seuraavaksi kaksi kilpapolkupyörää lisää, Snro3 ja Snro4.  

11. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vapautetut tuotantotilaukset** ja valitse sitten vastaava linkki.  
12. Valitse **Uusi**-toiminto.  
13. Luo uusi vapautettu tuotantotilaus täyttämällä seuraavat kentät otsikossa.  

    |Lähteen nro|Määrä|Sarjanumero|  
    |----------------|--------------|----------------|  
    |1002|2|Snro3|  
    |1002|2|Snro4|  

14. Täytä rivi valitsemalla **Päivitä tuotantotilaus**-toiminto.  
15. Anna sarjanumerot valitsemalla ensin **Nimikkeen seurantarivit**-toiminto ja sitten numerot kahdelta **Sarjanumero**-kentän riviltä **Nimikkeiden seurantarivit** -sivulla.  

    Seuraavaksi on tarpeen kirjata ERÄ1:n kilpapyörän runkojen kulutus.  
16. Valitse **Vapautettu tuotantotilaus** -sivulla **Tuotantopäiväkirja** -toiminto.  
17. Valitse ensin **Tuotantopäiväkirja**-sivulla nimikkeen 2000 kulutusrivi ja sitten **Nimikkeen seurantarivit** -toiminto.
18. Valitse **Nimikkeen seurantarivit** -sivulla ensin **Eränro**-kenttä ja sitten **ERÄ1** ja lopuksi **OK**.  
19. Älä muuta muita **Tuotantopäiväkirja** sivun oletusasetuksia. Valitse sitten **Kirjaa**-toiminto.  

    Olet nyt tuottanut neljä kilpapyörää Snro1 - Snro4 ja kuluttanut neljä kymmenestä kilpapyörän rungosta ERÄ1:stä. Kumpaankin tuotantotilaukseen kulutettiin kaksi runkoa.  

20. Sulje tuotantopäiväkirja ja tuotantotilaukset.  

    Myy seuraavaksi kilpapolkupyöriä. Myy ensin kilpapyörä (Snro1) Tinayhtymä Oy:lle.  

### <a name="to-sell-the-end-items"></a>Myy lopullisia nimikkeitä

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2.  Valitse **Uusi**-toiminto ja luo sitten myyntitilaus täyttämällä seuraavat kentät.  

    |Asiakas|Nimike|Määrä|Sarjanumero|  
    |--------------|----------|----------|----------------|  
    |Tinayhtymä Oy|1002|1|Snro1|  

3.  Anna sarjanumero valitsemalla ensin **Nimikkeen seurantarivit**-toiminto ja sitten numero **Sarjanumero**-kentän riviltä **Nimikkeiden seurantarivit** -sivulla.  
4.  Valitse ensin **Kirjaa**-toiminto, sitten **Toimitus ja lasku** -asetus ja lopuksi **OK**.  

    Myy seuraavaksi kilpa-pyörä SN2 ja Tuotantoyhtymä Oyj:lle.  

5.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
6.  Valitse **Uusi**-toiminto ja luo sitten myyntitilaus täyttämällä seuraavat kentät.  

    |Asiakas|Nimike|Määrä|Sarjanumero|  
    |--------------|----------|----------|----------------|  
    |Cannon Group PLC.|1002|1|Snro2|  

7.  Anna sarjanumero valitsemalla ensin **Nimikkeen seurantarivit**-toiminto ja sitten numero **Sarjanumero**-kentän riviltä **Nimikkeiden seurantarivit** -sivulla.  
8.  Valitse ensin **Kirjaa**-toiminto, sitten **Toimitus ja lasku** -asetus ja lopuksi **OK**.  

    Lopuksi on tarpeen myydä kilpapyörän runkoja erikseen. Tuotantoyhtymä Oyj tilaa lisäksi neljä erillistä kilpapyörän runkoa omaa tuotantolinjaansa varten.  

9. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
10. Valitse **Uusi**-toiminto ja luo sitten myyntitilaus täyttämällä seuraavat kentät.  

    |Asiakas|Nimike|Määrä|Sarjanro|  
    |--------------|----------|----------|----------------|  
    |Cannon Group PLC.|2000|5|ERÄ1|  

11. Anna sarjanumero valitsemalla ensin **Rivit**-pikavälilehden **Rivi**-ryhmässä **Nimikkeen seurantarivit** -toiminto ja sitten numero **Sarjanumero**-kentän riviltä **Nimikkeiden seurantarivit** -sivulla.  

    > [!NOTE]  
    >  Älä kirjaa viimeistä myyntitilausta (joka on viidelle kilpapyörän rungolle).  

    Näin olet valmistellut tiedot Nimikkeen jäljitys- ja Etsi merkintöjä -toimintojen esittelyä varten.  

## <a name="tracing-from-usage-to-origin"></a>Jäljittäminen käytöstä alkuperään

 Myyntiosastolta kerrotaan laatupäällikölle, että palautetun kilpapyörän (nimike 1002) eränumero on Snro1. Käyttämällä näitä perustietoja hän voi määrittää, missä valmista kilpapyörää on viimeksi käytetty, tässä tapauksessa Selangorian Ltd.:hen lähtevässä toimituksessa. Sitten laatupäällikön täytyy jäljittää taaksepäin ensimmäiseen alkuperään saadakseen tietää, mistä eränumerosta viallinen kilpakehys on peräisin, ja kuka oli sen toimittaja.  

### <a name="to-determine-which-lot-included-the-faulty-frame-and-who-supplied-it"></a>Virheellisen rungon erän ja toimittajan määrittäminen

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeen jäljitys** ja valitse sitten vastaava linkki.  
2.  Kirjoita **Nimikkeen jäljitys** -sivulla **Sarjanron suodatus** -kenttään **Snro1** ja lisää **Nimikesuodatus**-kenttään **1002**.  
3.  Säilytä **Näytä komponentit** -kentän oletusarvo **Vain nimikeseuranta**. Säilytä myös **Jäljitystapa**-kentän oletusjäljitystapa **Käytöstä alkuperään**.  
4.  Valitse **Jäljitys**-toiminto.  

    Huomaa, yksi lähtevän toimituksen otsikko vastaa hakuehtoja. Ennen kuin jatkat jäljitystä, varmista, että kyseessä on toimitus, joka sisälsi Tinayhtymä Oy:lle toimitetun virheellisen kilpapyörän.  

5.  Valitse ensin jäljitysrivi ja sitten **Näytä asiakirja** -toiminto.  

    Jatka sitten kilpapyörän (Snro1) myyntitoimituksen alkuperän jäljitystä.  
6.  Jäljitysrivien pluskuvaketta napsauttamalla voit laajentaa rivejä vähitellen ja näin siirtyä taaksepäin tapahtumaketjussa, josta myyntitoimitus on peräisin.  

    Seuraava tapahtumahistoria voidaan jäljittää:  

    - Siirryttäessä ketjussa taaksepäin ensimmäinen kirjattu asiakirja tapahtumaketjussa on Snro1:n ensimmäiseksi vapautetun tuotantotilauksen tuotoksen kirjaus.  
    - Siirryttäessä ketjussa vielä taaksepäin seuraava kirjattu asiakirja on ensimmäisen vapautetun tuotantotilauksen kulutuksen kirjaus. Tässä laatupäällikkö näkee, että ERÄ1:stä peräisin olevaa kilpapyörän runkoa käytettiin.  
    - Ketjun viimeinen kirjattu asiakirja on kirjattu ostovastaanotto, jolla ERÄ1:n kilpapyörän rungot kirjattiin varastoon.  

    Laatupäällikkö on nyt selvittänyt, mikä kilpapyörän runkojen erä oli virheellinen. Viimeisen jäljitysrivin avulla hän voi tarkistaa, että virheellinen erä on peräisin toimittajalta Pyöräliike Oy.  

    > [!NOTE]  
    >  Älä muokkaa jäljityksen tuloksia muutoin, sillä niitä käytetään seuraavassa osassa.  

     Nyt virheenhallinnan ensimmäinen **Nimikkeen jäljitys** -sivulla toteutettavista tehtävistä on valmis. Laatupäällikön on nyt määritettävä, onko ERÄ1:stä peräisin olevia kilpapyörän runkoja käytetty muissa kirjatuissa asiakirjoissa.  

## <a name="tracing-from-origin-to-usage"></a>Jäljittäminen alkuperästä käyttöön

 Laatupäällikkö on selvittänyt, että virheellinen kilpapyörän runkoerä on peräisin ERÄ1:stä. Hänen on nyt määritettävä, onko virheellisiä runkoja käytetty muualla, jotta nämä kilpapyörät voidaan pysäyttää tai kutsua takaisin.  

 Yksi tapa valmistella tämä jäljitystehtävä **Nimikkeen jäljitys** sivulla on, että anna manuaalisesti arvon ERÄ1 **Eränro suodatus** -kenttään ja arvon 2000 **Nimikesuodatus**-kenttään. Tässä vaihekuvauksessa käytetään kuitenkin **Jäljitä vastapuoli - riviltä** -funktiota.  

### <a name="to-find-all-usage-of-the-faulty-lot"></a>Virheellisen erän kaikkien käyttökohteiden etsiminen  

1.  Valitse **Nimikkeen jäljitys** -sivulla ostovastaanoton rivi, viimeinen jäljitysrivi ja lopuksi **Jäljitä vastapuoli - Riviltä**.  

    Jäljityksen tulos perustuu nyt ostovastaanoton, ERÄ1:n ja nimikkeen 2000 suodattimiin. Jäljitys toteutetaan **Alkuperästä käyttöön**-jäljitystavalla.  

    Voit tarkastella ERÄ1:n nimikkeen 2000 käytön yleiskatsausta laajentamalla kaikki jäljitysrivit.  

2.  Valitse **Laajenna kaikki** -toiminto.  

    Neljä ensimmäistä jäljitysriviä viittaavat Tinayhtymä Oy:n myyntitoimitukseen, joka on jo ratkaistu. Viimeinen rivi ilmaisee, että yksi kilpapyörä, Snro2, tuotettiin samassa tuotantotilauksessa sekä myytiin ja toimitettiin toisessa myyntitoimituksessa.  

    Laatupäällikkö ilmoittaa asian välittömästi myyntiosastolle, jotta asiakkaalle eli Tuotantoyhtymälle toimitettu virheellinen kilpapyörä voidaan kutsua takaisin.  

    Samalla laatupäällikkö havaitsee kolmelta viimeiseltä jäljitysriviltä, että kahden muun nimikkeen, Snro3 ja Snro4, tuotannossa on käytetty ERÄ1:n kilpapyörän runkoja. Hän estää näiden valmiiden tuotteiden toimituksen varastosta.  

    Nyt toinen virheenhallinnan **Nimikkeen jäljitys** -sivulla toteutettavista tehtävistä on valmis. Koska **Nimikkeen jäljitys** -sivu perustuu vain kirjattuihin tapahtumiin, laatupäällikön on **Etsi tapahtumat** -sivun avulla varmistettava, ettei ERÄ1:tä ole käytetty kirjaamattomissa asiakirjoissa.  

## <a name="finding-all-records-of-a-seriallot-number"></a>Sarja-/eränumeron kaikkien tietueiden etsiminen

 **Nimikkeen jäljitys** -sivun avulla laatu-ohjain havaitsi, että LOT1 sisälsi viallisia kilpakehyksiä, jotka toimittaja on toimittanut, ja kirjatun tapahtuman, jossa niitä on käytetty. Hänen on nyt selvitettävä, sisältyykö ERÄ1 mihinkään avoimeen asiakirjaan integroimalla jäljitystulos **Etsi tapahtumat** -sivulle, jossa hän voi suorittaa haun kaikista tietokantatietueista.  

### <a name="to-find-all-occurrences-of-lot1-in-non-posted-records-such-as-open-orders"></a>ERÄ1:n kaikkien esiintymien etsiminen avoimista tilauksista ja muista kirjaamattomista tietueista  

1.  Valitse **Nimikkeen jäljitys** -sivulla ensimmäisen jäljitysrivin eli ERÄ1:n ostovastaanoton osoitin.  
2.  Valitse **Etsi tapahtumat** -toiminto.  

    **Etsi tapahtumat** -sivu sisältää valmiiksi ERÄ1:n jäljitystuloksiin perustuvat hakusuodattimet. Laatupäällikkö havaitsee, että suurin osa tietueista kuuluu **Nimikkeen jäljitys** -sivulla määritettyihin asiakirjoihin. Esimerkiksi Tuotantotilaus-tyypin viimeinen Etsi merkintöjä -rivi viittaa kahteen vapautettuun tuotantotilaukseen, joissa käytettiin ERÄ1:stä peräisin olevia kilpapyörän runkoja.  

    Sen sijaan **Myyntirivi**-tyypin toinen Etsi merkintöjä -rivi on kirjaamaton asiakirjarivi. Laatupäällikkö tutustuu tämän rivin tietoihin.  

3.  Avaa myyntirivin tietue valitsemalla ensin toinen Etsi merkintöjä -rivi ja sitten **Näytä**-toiminto. Voit myös valita arvon **Tietueiden lukumäärä** -kentästä.  

    Tässä laatupäällikkö näkee yhden avoimen myyntirivin, joka sisältää virheellisiä kilpapyörän runkoja. Hän ehdottaa välittömästi myyntiosastolle, että tämä tilaus peruutetaan ja uusi, virheettömiin runkoihin perustuva tuotantotilaus luodaan.  

 **Etsi tapahtumat**- ja **Nimikkeen jäljitys** -sivujen käytön integrointia vikojen hallinnassa käsittelevä vaihekuvaus on nyt käyty läpi.  

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/paths/use-serial-lot-numbers/)

## <a name="see-also"></a>Katso myös

[Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md)  
[Nimikeseurannan nimikkeiden jäljittäminen](inventory-how-to-trace-item-tracked-items.md)  
[Etsi tapahtumat](ui-find-entries.md)  
[Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]