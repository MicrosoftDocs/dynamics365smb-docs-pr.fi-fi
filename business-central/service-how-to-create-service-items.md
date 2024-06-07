---
title: Huoltonimikkeiden luominen
description: 'Lue, miten voit luoda huoltonimikkeitä Business Centralissa esimerkiksi huoltotilauksen sisäisesti tai toimitessasi nimikkeitä.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Huoltonimikkeiden luonti

[!INCLUDE[prod_short](includes/prod_short.md)]issä huoltonimikkeellä tarkoitetaan huoltoa edellyttävää laitetta tai nimikettä. Kun luot huoltotilauksen, määrität huoltoa tarvitsevat nimikkeet. Voit linkittää huoltonimikkeen tilauksessa varaston tai huoltonimikeryhmän nimikkeeseen.

Kun vastaanotat huoltoa tarvitsevan nimikkeen, voit rekisteröidä sen huoltonimikkeeksi. Sen voi tehdä usealla tavalla. Voit esimerkiksi luoda huoltonimikkeen **Huoltonimikkeet**-sivulla tai toisen prosessin osana esimerkiksi huoltotilausta käsiteltäessä.

## Huoltonimikkeiden luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltonimikkeet** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Huoltonimikkeiden luominen huoltotilauksissa

Kun vastaanotat huollettavaksi nimikkeitä, jotka haluat rekisteröidä huoltonimikkeiksi, ne voi luoda huoltonimikkeiksi **Huoltotilaus**- tai **Huoltotarjous**-sivulla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Valitse **Luo huoltonimike** -toiminto.  

    Numero annetaan huoltonimikkeelle ja huoltonimikekortti luodaan. Se täyttää **Huoltonimikkeen nro** -kentän uuden huoltonimikkeen numerolla.

## Huoltonimikkeiden luominen nimikkeitä toimitettaessa

Kun nimikkeitä toimitetaan kirjaamalla joko myyntitilauksia tai myyntilaskuja, ohjelma rekisteröi toimitetut nimikkeet automaattisesti huoltonimikkeiksi, jos seuraava ehto toteutuu. Nimikkeiden tulee kuulua huoltonimikeryhmään, jonka **Luo huoltonimike** -kentässä on valintamerkki. Jos nimikkeille on rekisteröity sarjanumero Nimikkeen seurantarivit -sivulla, ohjelma kopioi tämän tiedon automaattisesti huoltonimikekortin **Sarjanro**-kenttään huoltonimikkeiden luonnin yhteydessä.  

Seuraavassa kuvataan, miten huoltonimikkeitä luodaan myyntitilauksissa olevia nimikkeitä toimitettaessa.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Avaa käsiteltävä myyntitilaus.  
3. Valitse **Kirjaa**- tai **Kirjaa ja tulosta** -toiminto.  
4. Valitse **Toimitus**- tai **Toimitus ja lasku** -toiminto.  
5. Ohjelma luo automaattisesti huoltonimikkeet tilauksessa oleville nimikkeille, jos ne kuuluvat huoltonimikkeiden luomiseksi määritettyyn huoltonimikeryhmään. Jos **Nimikkeen seurantarivit** -sivulla on rekisteröity sarjanumeroita, nämä määritetään huoltonimikkeille.  

> [!NOTE]  
> Jos nimike on tuoterakenne ja olet purkanut tuoterakenteen, puretun tuoterakenteen nimikkeitä käsitellään tavallisen nimikkeen tavoin. Ohjelma luo huoltonimikkeet huoltonimikeryhmää koskevan ehdon ja mahdollisen sarjanumeroehdon mukaan. Jos lisäksi huoltonimike on luotu puretun tuoterakenteen nimikkeelle, joka muodostuu muista tuoterakenteen komponenteista, nämä nimikkeet luodaan puretun tuoterakenteen huoltonimikkeen huoltonimikkeen komponenteiksi.  
>
> Jos nimike on tuoterakenne etkä ole purkanut tuoterakennetta, ohjelma luo nimikkeelle huoltonimikkeen huoltonimikeryhmää koskevan ehdon ja mahdollisen sarjanumeroehdon mukaan.  

## Aloitusmaksujen syöttäminen huoltonimikkeille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotehtävät** ja valitse sitten vastaava linkki.
2. Valitse **Nimikkeen työkirja** -toiminto.
3. Valitse ensin huoltorivi ja sitten **Toiminnot**. Valitse sitten **Toiminnot** ja lopuksi **Syötä aloitusmaksu** -toiminto.  

    Ohjelma lisää **Kustannus**-tyypin huoltorivin, jolla on aloitusmaksu. Tämä aloitusmaksu koskee valittua huoltonimikettä.

## Nimikkeiden, nimikevarianttien tai tiettyjen huoltonimikkeiden estäminen

Nimikkeiden, nimikevarianttien tai huoltonimikkeiden käyttäminen huollonhallinnan tapahtumissa, kuten huoltosopimuksissa, huoltotilauksissa ja huoltolaskuissa, voidaan estää. Tämä voi olla kätevää, jos halutaan rajoittaa joidenkin nimikkeiden tai palvelunimikkeiden saatavuutta huollossa esimerkiksi päättyneen tuen, rajallisen varaston tai sopimuksen ehtojen vuoksi.

Nimikkeen tai nimikevariantin käytön estäminen huollonhallinnan tapahtumissa tehdään ottamalla **Huolto estetty** käyttöön vaihtopainikkeella **Nimikekortti**-, **Nimikevariantit**- ja **Nimikevariantti-kortti**-sivulla. Tämä kenttä voidaan määrittää myös **Nimikemalli**-sivulla, josta se kopioidaan kyseisestä mallista luotuihin nimikkeisiin.

Kun nimikkeen tai nimikevariantin käyttö huollossa on estetty, se ei ole valittavissa seuraavilla sivuilla:

- Huoltorivi (poikkeuksena huoltohyvityslaskut, joissa näkyy ilmoitus, että nimike tai variantti on estetty mutta sallitaan tämän tyyppisessä asiakirjassa)
- Huoltonimike
- Huoltosopimuksen rivi
- Vakiohuoltorivi

Jos estetty nimikenumero tai variantti syötetään manuaalisesti, tuloksena on virhesanoma: Kenttä sisältää arvon, jota ei löydy siihen liittyvästä taulukosta.

Lisäksi seuraavia toimintoja ei voi käyttää, jos huoltosopimukset, huoltosopimustarjoukset tai huoltotilaukset sisältävät estettyjä huoltonimikkeitä tai nimikevariantteja:

- **Lukitus** tai **Tee sopimus** **Huoltosopimustarjous**-sivulla.
- **Lukitse sopimus**, **Allekirj. sopimus**, **Luo sopimushuoltotilauksia** tai **Luo sopimuslaskut** **Huoltosopimus**-sivulla.
- **Tee tilaus** **Huoltotarjous**-sivulla.
- **Vapauta toimitettavaksi** tai **Kirjaa** **Huoltotilaus**-sivulla.
- **Kirjaa** **Huoltolasku**-sivulla.

### Huoltonimikkeen estäminen

Huoltonimikkeen käytön estäminen huollonhallinnan tapahtumissa tehdään valitsemalla **Huoltonimikekortti**-sivun **Estetty**-kentässä jokin seuraavista vaihtoehdoista:

- **Huoltosopimus**: huoltonimikkeen käytön estäminen huoltosopimuksissa ja huoltosopimustarjouksissa muttei huoltotilauksissa tai muissa huoltoasiakirjoissa.
- **Kaikki**: huoltonimikkeen käytön estäminen kaikissa huollonhallinnan tapahtumissa, mukaan lukien huoltosopimuksissa, huoltotilauksissa ja muissa huoltoasiakirjoissa.

Kun huoltonimike estetään, sitä ei voi valita seuraavilla sivuilla:

- Huoltosopimuksen rivi (jos estetty huoltosopimuksissa tai kaikki estetty)
- Huoltonimikerivi (ei kuitenkaan huoltohyvityslaskuissa, jos estetty kaikissa)

Jos estetyn huoltonimikkeen huoltonimikenumero syötetään manuaalisesti, tuloksena on virhesanoma: Kenttä sisältää arvon, jota ei löydy siihen liittyvästä taulukosta.

Lisäksi seuraavia toimintoja ei voi käyttää, jos huoltosopimukset, huoltosopimustarjoukset tai huoltotilaukset sisältävät estettyjä huoltonimikkeitä:

- **Lukitus** ja **Tee sopimus** **Huoltosopimustarjous**-sivulla (jos estetty huoltosopimuksissa tai kaikissa).
- **Lukitse sopimus**, **Allekirj. sopimus** tai **Vaihda asiakas** **Huoltosopimus**-sivulla (jos estetty huoltosopimuksissa tai kaikissa).
- **Tee tilaus** **Huoltotarjous**-sivulla (jos estetty kaikissa).
- **Vapauta toimitettavaksi** tai **Kirjaa** **Huoltotilaus**-sivulla (jos estetty kaikissa. Jos huoltotilausasiakirjoissa on useita huoltonimikkeitä, joista osa on estetty ja osa ei, ei-estetyt rivit voidaan vapauttaa ja kirjata. Kannattaa harkita, otetaanko **Yksi huoltonimikerivi/tilaus** käyttöön vaihtopainikkeella **Huoltohallinnon asetukset** -sivulla).
- **Kirjaa** **Huoltolasku**-sivulla (jos estetty kaikissa).

Estettyjä huoltonimikkeitävoi tarkastella myös käyttämällä suodatinta seuraavissa raporteissa:

- Huoltonimikkeet (raportti 5935)
- Huoltonimikkeet ilman takuuta (raportti 5937)
- Huollon tuotto (huoltonimikk.) (raportti 5938)

### Tietojen päivitys

Tämä ominaisuus ei edellytä lisäasetuksia. Seuraavat on kuitenkin huomattava, jos [!INCLUDE [prod_short](includes/prod_short.md)] päivitetään:

- Jos käytössä on nimikkeitä, nimikevariantteja tai nimikemalleja, joissa **Myynti estetty** on otettu käyttöön vaihtopainikkeella, myös **Huolto estetty** -kenttä on otettu käyttöön kyseisissä tietueissa päivityksen yhteydessä. Tämä varmistaa, että aiemmin luotua myynnin estologiikkaa käytetään huollonhallinnan tapahtumiin.
- Tiedot päivittyvät vain, jos yrityksessä on vähintään yksi huoltonimike, mikä tarkoittaa, että huollon hallintatoimintoja käytetään ja tiedot on päivitettävä. Jos huoltonimikkeitä ei ole, tietojen päivitys ohitetaan, ja **Huolto estetty** poistetaan oletusarvoisesti käytöstä vaihtopainikkeella kaikissa nimikkeissä, nimikevarianteissa ja nimikemalleissa.

## Katso myös

[Huoltonimikkeiden ja huoltonimikkeiden komponenttien määrittäminen](service-how-setup-service-items.md)  
[Huoltohallinnon määrittäminen](service-setup-service.md)  
[Huoltohallinto](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
