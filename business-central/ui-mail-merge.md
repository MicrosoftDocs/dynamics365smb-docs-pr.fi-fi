---
title: Word-mallien käyttö joukkoviestinnässä
description: Word-mallit helpottavat tietyille entiteeteille mukautettujen asiakirjojen joukkoluontia.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/01/2023
ms.custom: bap-template
ms.search.forms: '9989, 13,'
---

# <a name="use-word-templates-for-bulk-communication" />Word-mallien käyttö joukkoviestinnässä

Microsoft Word -mallit helpottavat entiteettien, kuten kontaktien, asiakkaiden ja toimittajien, kanssa tapahtuvaa joukkoviestintää postitse tai sähköpostitse. Voit esimerkiksi luoda

* esitteitä, joissa kerrotaan asiakkaille myyntikampanjoista
* kirjeitä, joissa toimittajille kerrotaan uudesta ostokäytännöstä
* kutsuja, joilla houkutellaan yhteyshenkilöitä tulevaan tapahtumaan

> [!NOTE]
> Kun määrität Word-malleja, sinun täytyy käyttää laitetta, jossa on Microsoft Word 2019 tai uudempi ja Windows-käyttöjärjestelmä asennettuna.

## <a name="set-up-the-source-of-data" />Valitse tietolähde

[!INCLUDE[prod_short](includes/prod_short.md)]in entiteettejä voi käyttää mallin tietolähteinä, ja asiakirjat voidaan mukauttaa kullekin entiteetille lisäämällä yhdistämiskenttiä. Yhdistämiskentät saadaan [!INCLUDE[prod_short](includes/prod_short.md)]in entiteetistä. Kun Word-mallia käytetään entiteetissä, yhdistämiskenttien tiedot lisätään asiakirjaan.

Kun luot uuden mallin **Word-mallit** -sivulla, asetusten ohjattu määritys auttaa seuraavien vaiheiden läpi:

1. Valitse vähintään yksi tiedon lähteenä käytettävä yksikkö. Jos esimerkiksi haluat luoda esitteen myyntikampanjaa varten, voit todennäköisesti valita lähteeksi Asiakas-objektin.
2. Valitse muut objektit lisätietolähteiksi. Lisätietoja on kohdassa [Lähdeobjektiin liittyvien tai liittymättömien tapahtumien lisääminen](#add-entries-that-are-related-or-unrelated-to-the-source-entity).
3. Lataa tyhjä malli. Voit määrittää mallin Wordissa heti tai voit ladata tyhjän mallin ja viimeistellä oppaan. Kun malli on valmis, korvaa tyhjä malli valmiin mallin avulla käyttämällä **Lataa** -toimintoa **Word-mallit** -sivulla. Lisätietoja on kohdassa [Mallin määrittäminen Wordissa](#set-up-the-template-in-word).
4. Lataa valmisteltu malli.
5. Syötä koodi ja nimi, joka yksilöi mallin.

Kun lataat mallin, saat. zip-tiedoston, joka sisältää kaksi tiedostoa.

|Tiedosto  |Kuvaus  |
|---------|---------|
|DataSource.xlsx     | Tieto lähdetiedosto sisältää kentät, joita voidaan käyttää mallissa. Älä muokkaa tietolähdetiedostoa. Voit käyttää vain ladattuja Word-malli- ja tietolähdetiedostoja, ja nämä tiedostot on tallennettava samaan sijaintiin.     |
|Word-malli     | Mallina käytettävä .docx-tiedosto.        |

Saat lisätietoja mallin määrittämisestä Wordissa valitsemalla [Mallin määrittäminen Wordissa](#set-up-the-template-in-word).

## <a name="add-entries-that-are-related-or-unrelated-to-the-source-entity" />Lähdeobjektiin liittyvien tai liittymättömien tapahtumien lisääminen

Voit myös yhdistää muiden entiteettien tietoja. Jos haluat lisätä muita objekteja tietolähteiksi, käytä jotakin seuraavista toiminnoista **Word-mallit** -sivulla tai käyttäessäsi asetusten ohjattua määritystä:

|Toiminto  |Kuvaus  |
|---------|---------|
|**Lisää liittyvä objekti**  | Käytä lähdeobjekteihin liittyen objektien tietoja. Esimerkiksi Asiakas-objektille voi myös yhdistää tietoja Yhteyshenkilö-objektista. Objektit liittyvät toisiinsa, kun yhden objektin kenttä viittaa toiseen. Asiakas-objektin kenttä viittaa Yhteyshenkilö-objektin kenttään, joten ne liittyvät toisiinsa. Jaettu kenttä on usein tunniste, kuten nimi, koodi tai tunnus.        |
|**Lisää liittymätön objekti**| Käytä lähdeobjekteihin liittymättömien objektien tietoja. Olet esimerkiksi luomassa Asiakas-objektille mallia. Voit lisätä Yritystiedot-objektin, jotta voit sisällyttää yhteystietosi. Avainetuna on, että jos muutat yhteystietojasi, se päivitetään automaattisesti malliin. Kun olet lisännyt liittymättömän objektin, voit lisätä siihen liittyviä objekteja.         |

Liittymättömien objektien osalta valitset tietyn tietueen. Koska voit lisätä objektin vain kerran, voit käyttää eri tietueita poistamalla objektin ja lisäämällä sen uudelleen uuteen tietueeseen.

Voit luoda objektihierarkian, sekä toisiinsa liittyvät että liittymättömät. Suhde näkyy puurakenteena. **Objektin suhde** -kentässä näkyy tietoja myös suhteesta. Liittymättömille objekteille kentässä näkyy tietue, joka luo suhteen.

Kun lisäät objekteja, voit määrittää kenttien nimien etuliitteen käyttämällä **Kentän etuliite** -kenttää. Kun myöhemmin lisäät kenttiä malliin, etuliite helpottaa lähteen ja muiden objektien kenttien erottamista toisistaan.

### <a name="select-the-fields-to-include" />Valitse sisällytettävät kentät

Voit määrittää kunkin objektin osalta, mitä kenttiä haluat käyttää mallissa. Valitse numero **Valittujen kenttien määrä** -sarakkeesta, niin voit avata käytettävissä olevien kenttien luettelon. **Kentän valinta** -sivulla voit määrittää kentät **Sisällytä**-valintaruudun avulla. Joissakin objekteissa yritysten yleisesti käyttämät kentät on sisällytetty oletusarvoisesti. Voit esimerkiksi muokata luetteloa ja poistaa oletuskentät. Tekemäsi muutokset koskevat vain mallia, jota käsittelet.

> [!NOTE]
> Kaikista objekteista lisättävien kenttien kokonaismäärä on 250.

> [!NOTE]
> Sinä tai Microsoft-kumppani voi lisätä objekteihin mukautettuja kenttiä. Kun teet näin, kenttien nimen etuliitteenä on **CALC** ja niiden kenttätyyppinä on **Laskettu**. Kenttätyyppiä kutsutaan lasketuksi ilmaisemaan, että kenttä voi näyttää erityyppisiä arvoja, kuten tekstiä, numeroita, päivämääriä ja niin edelleen.

## <a name="to-create-a-word-template-in-business-central" />Word-mallin luominen Business Centralissa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Word-mallit** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**, sitten **Luo malli** ja noudata sitten avustetun asennusoppaan ohjeita. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Voit myös luoda mallin suoraan entiteetin sivulta valitsemalla **Käytä Word-mallia** -toiminnon avataksesi avustetun asetusoppaan ja sitten **Uusi malli**. Kun teet näin, tietolähde valitaan entiteetin tyypin mukaan.

## <a name="set-up-the-template-in-word" />Mallin määrittäminen Wordissa

Kun mallia määritetään Wordissa, yhdistämiskentät voidaan lisätä **Postitukset**-välilehdessä valitsemalla **Lisää yhdistämiskenttä**. Yhdistämiskentät ovat peräisin tietolähdetiedostosta, jonka latasit entiteetille. Ne toimivat paikkamerkkeinä, jotka kertovat Wordille, mihin asiakirjassa on tarkoitus sijoittaa entiteetin tiedot.

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Yhdistämiskenttien lisääminen Microsoft Wordiin":::

## <a name="apply-a-template" />Käytä mallia

Kun Word-malli on valmis, asiakirjat voidaan luoda valitsemalla **Word-mallit**-sivulla **Käytä**. Kun Word-mallia käytetään entiteetissä, yhdistämiskenttien tiedot lisätään asiakirjaan. Voit luoda joko yhden asiakirjan, jossa on osa kullekin entiteetille, tai valita **Jaa**-toiminnon luomaan uuden asiakirjan kullekin entiteetille.

Voit käyttää **Käytä Word-malleja** -toimintoa, kun haluat käyttää malleja yhdessä tai useassa samantyyppisessä objektissa, kuten asiakas, suoraan objektin sivun kontekstissa. Esimerkiksi **Asiakas**- tai **Toimittaja**-sivut.

## <a name="use-word-templates-with-email" />Word-mallien käyttäminen sähköpostissa

Voit lisätä sisältöä sähköpostiviesteihin Word-mallien avulla. Kun kirjoitat sähköpostiviestiä, voit ottaa mallin sisällön käyttöön viestissä käyttämällä **Käytä Word-mallia** -toimintoa. Objektille on luotava malleja. Voit käyttää yhtä mallia kerrallaan ja siirryttäessä mallien välillä viesti muuttuu valitun mallin sisällön mukaiseksi.

Lisäksi voit liittää mallin sisällön sähköpostiin tiedostona käyttämällä **Lisää tiedosto Word-mallista** -toimintoa. Tiedosto käyttää mallin tulostuksessa määritettyä muotoa.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Wordin-mallin sisällön käyttövaihtoehdot sähköpostissa":::

## <a name="edit-a-word-template" />Word-mallin luominen

Voit tehdä seuraavat muutokset Word-malleihin:

* Jos haluat muokata mallin leipätekstiä tai yhdistämiskenttiä, käytä **Lataa**-toimintoa, tee muutokset ja käytä **Lataa**-toimintoa
* Voit muuttaa tietolähteitä käyttämällä **Muokkaa liittyviä objekteja** -toimintoa
* Voit korvata Word-mallin uudella mallilla käyttämällä **Lataa**-toimintoa
* Poista malli

## <a name="see-also" />Katso myös

[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
[Määritä sähköposti](admin-how-setup-email.md)  
