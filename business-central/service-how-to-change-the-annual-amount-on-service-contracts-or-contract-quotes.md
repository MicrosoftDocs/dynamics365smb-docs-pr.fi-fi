---
title: Huoltosopimuksen tai sopimustarjouksen vuosittaisen summan muuttaminen
description: Voit muuttaa huoltosopimuksen tai huoltosopimustarjouksen vuosittain laskutettavaa summaa.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="change-the-annual-amount-on-service-contracts-or-contract-quotes"></a>Huoltosopimuksen tai sopimustarjouksen vuosittaisen summan muuttaminen
Huoltosopimuksen tai sopimustarjouksen vuosittaista summaa voidaan muuttaa, jos vuosittain laskutettavaa summaa tarvitsee korjata.  

## <a name="to-change-the-annual-amount-of-the-service-contract-or-contract-quote"></a>Huoltosopimuksen tai sopimustarjouksen vuosittaisen summan muuttaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimukset** tai **Huoltosopimustarjoukset** ja valitse sitten vastaava linkki.  
2. Valitse sopimus tai sopimustarjous.  
3. Avaa muokattava sopimus tai sopimustarjous valitsemalla **Avaa sopimus** -toiminto.  
4. Valitse **Salli epätäsmäävät summat** -valintaruutu, jos haluat muuttaa vuosittaista summaa ja jakaa vuosittaisen summan eron manuaalisesti sopimusriveille. Poista muussa tapauksessa valintaruudun valinta, jotta vuosittainen summa neron jaetaan automaattisesti sopimusriveille, kun vuosittaista summaa on muutettu.  
5. Muuta **Vuosittainen summa** -kentän sisältöä. Et voi allekirjoittaa huoltosopimusta eli tarjousta ei voi muuntaa huoltosopimukseksi, jos käsittelet sopimustarjousta, etkä lukita sitä, jos sen vuosittainen summa on negatiivinen. Jos vuosittaiseksi summaksi annetaan nolla, **Laskutuskausi**-kentässä on oltava **Ei mitään**, kun huoltosopimus allekirjoitetaan tai lukitaan.  
6. Jaa vuosittaisen summan ero manuaalisesti tai automaattisesti sen mukaan, onko **Salli epätäsmäävät summat** -valintaruutu valittu. Sopimusrivit päivitetään niin, että **Laskettu vuosittainen summa** -kentän arvoksi tulee sama kuin uusi vuosittainen summa.  

## <a name="distributing-differences-between-new-and-calculated-annual-amounts"></a>Uuden ja lasketun vuosittaisen summan eron jakaminen
Jos huoltotarjouksen tai -sopimuksen vuosittaista summaa muutetaan, voidaan uuden ja lasketun vuosittaisen summan välinen ero joutua jakamaan sopimusriveille. Voit jakaa summat kolmella tavalla:

* Tasainen jako  
* Jako rivisummien perusteella  
* Tuottoon perustuva jako

### <a name="even-distribution"></a>Tasainen jako
Jos huoltotarjouksen tai huoltosopimuksen vuosittaista summaa muutetaan, voidaan uuden ja lasketun vuosittaisen summan välinen ero joutua jakamaan sopimusriveille. Tasainen jako on yksi automaattisista jakomenetelmistä, jotka auttavat jakamaan uuden ja lasketun vuosittaisen summan eron tasaisesti sopimuksen rivisummien kesken. Seuraavassa toimenpiteiden luettelossa kuvataan tämän menetelmän perusajatus:  

1. **Vuosittainen summa** -kentän uuden arvon ja **Laskettu vuosittainen summa** -kentän arvon ero jaetaan huoltosopimuksen tai sopimustarjouksen sopimusrivien lukumäärällä.  
2. **Rivisumma**-kentän arvo päivitetään lisäämällä siihen edellisen laskennan tulos.  
3. **Rivin alennussumma**-, **Rivialennus-%**- ja **Tuotto**-kenttien sisältö päivitetään **Rivisumma**-kentän uuden arvon mukaisesti:   
    * Rivin alennussumma = Rivin arvo - Rivisumma.  
    * Rivialennus-% = Rivin alennussumma / Rivin arvo * 100.  
    * Tuotto = Rivisumma - Rivikustannus.  

 Vaiheet toistetaan kullekin sopimusriville.  

#### <a name="example"></a>Esimerkki
Huoltosopimuksen **Salli epätäsmäävät summat**-kentässä ei ole valintamerkkiä, ja sopimus sisältää kolme sopimusriviä, joilla on seuraavat tiedot:  

|Nimike|Rivikustannus|Rivin arvo|Rivialennus-%|Rivin alennussumma|Rivisumma|Tuotto|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Nimike 1|30,00|40,00|0,00|0,00|40,00|10,00|  
|Nimike 2|40,00|50,00|10,00|5,00|45,00|5,00|  
|Nimike 3|50,00|70,00|10,00|7,00|63,00|13,00|  

**Vuosittainen summa** -kentän arvo on sama kuin **Laskettu vuosittainen summa**-kentän arvo, joka on aina rivisummien yhteissumma. Tässä tapauksessa se on yhtä suuri kuin seuraava: 40 + 45 + 63 = 148.  

Jos muutat **Vuotuinen summa** -kohdan arvoksi 139, lasketaan määrä, joka tulee lisätä jokaiseen **Rivisumma**-kentän arvoon. Tämä määrä lasketaan vähentämällä **Laskettu vuosittainen summa** -kentän arvo **Vuosittainen summa** -kentän uudesta arvosta ja jakamalla saatu tulos huoltosopimuksessa olevien sopimusrivien lukumäärällä. Tässä tapauksessa se on yhtä suuri kuin seuraava: (139 - 148) / 3 = -3. Sitten viimeinen laskettu luku lisätään jokaiseen **Rivisumma**-kentän arvoon, ja **Rivialennus-%**-, **Rivin alennussumma**- ja **Voitto**-kenttien arvot päivitetään käyttämällä kaavoja, joita on kuvattu edellä mainituissa toimenpiteissä.  

Sopimusriveillä on lopuksi seuraavat tiedot:  

|Nimike|Rivikustannus|Rivin arvo|Rivialennus-%|Rivin alennussumma|Rivisumma|Tuotto|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Nimike 1|30,00|40,00|7,50|3,00|37,00|7,00|  
|Nimike 2|40,00|50,00|16.00|8.00|42.00|2.00|  
|Nimike 3|50.00|70.00|14.29|10.00|60.00|10.00|  

### <a name="distribution-based-on-line-amount"></a>Jako rivisumman perusteella
Jos huoltosopimuksen tai sopimustarjouksen vuosittaista summaa muutetaan, voidaan uuden ja lasketun vuosittaisen summan välinen ero joutua jakamaan sopimusriveille. Rivisummaan perustuva jako on automaattinen menetelmä, joka auttaa jakamaan uuden ja lasketun vuosittaisen summan eron sopimusrivien rivisummien kesken. Jako tehdään suhteessa kunkin rivisumman osuuteen lasketusta vuosittaisesta summasta. Seuraavassa kullakin rivillä tehtävien toimenpiteiden luettelossa kuvataan tämän menetelmän perusajatus:  

1. Rivisumman osuus lasketaan seuraavasti: **Rivisumma**-kentän sisältö jaetaan **Laskettu vuosittainen summa** -kentän arvolla kaikilla sopimusriveillä.  
2. **Rivisumma**-kentän arvo päivitetään lisäämällä siihen uuden ja lasketun vuosittaisen summan ero kerrottuna rivisumman osuudella.  
3. **Rivin alennussumma**-, **Rivialennus-%**- ja **Tuotto**-kenttien sisältö päivitetään **Rivin alennussumma** -kentän uuden arvon mukaisesti:  

    * Rivin alennussumma = Rivin arvo - Rivisumma.  
    * Rivialennus-% = Rivin alennussumma / Rivin arvo * 100.  
    * Tuotto = Rivisumma - Rivikustannus.  

Vaiheet toistetaan kullekin sopimusriville.  

#### <a name="example-1"></a>Esimerkki
Huoltosopimuksen **Salli epätäsmäävät summat**-kentässä ei ole valintamerkkiä, ja sopimus sisältää kolme sopimusriviä, joilla on seuraavat tiedot:  

|Nimike|Rivikustannus|Rivin arvo|Rivialennus-%|Rivin alennussumma|Rivisumma|Tuotto|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Nimike 1|15,00|17,00|3,00|0,51|25,00|1,49|  
|Nimike 2|20,00|23,00|Ei mitään|0,00|55,10|3,00|  
|Nimike 3|24,00|27,00|3,00|0,81|112,70|2,19|  

**Vuosittainen summa** -kentän arvo on sama kuin **Laskettu vuosittainen summa**-kentän arvo, joka on aina rivisummien yhteissumma. Tässä tapauksessa se on yhtä suuri kuin seuraava: 16,49 + 23,00 + 26,19 = 65,68.  

Jos muutat **Vuotuinen summa** -kohdan arvoksi 60, jokaiselle sopimusriville lasketaan tuottoprosenttiosuudet:  

* Nimike 1 – 5 / (5 + 5,1 +12,7) = 0,2193 %  
* Nimike 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Nimike 3 – 12,7 / (5 + 5,1 +12,7) = 0,557 %  

Kunkin sopimusrivin **Rivisumma**-kentän arvo päivitetään sitten käyttämällä seuraavaa kaavaa Rivisumma = Rivin arvo + uuden ja lasketun vuosittaisen summan ero * prosenttiosuus. Tämän jälkeen **Rivin alennussumma-**, **Rivialennus-% %**, - ja  **Tuotto**-kenttien arvot päivitetään edellä olevan toimenpideluettelon kaavoja käyttäen.  

Sopimusriveillä on lopuksi seuraavat tiedot:  

|Nimike|Rivikustannus|Rivin arvo|Rivialennus-%|Rivin alennussumma|Rivisumma|Tuotto|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Nimike 1|15,00|17,00|11,41|1,94|15,06|0,06|  
|Nimike 2|20,00|23,00|8.65|1.99|21.01|1.01|  
|Nimike 3|24.00|27.00|11.37|3.07|23.93|-0,07|  

### <a name="distribution-based-on-profit"></a>Tuottoon perustuva jako
Jos huoltosopimuksen tai sopimustarjouksen vuosittaista summaa muutetaan, voidaan uuden ja lasketun vuosittaisen summan välinen ero joutua jakamaan sopimusriveille. Tuottoon perustuva jako on yksi automaattisista menetelmistä, jotka auttavat jakamaan uuden ja lasketun vuosittaisen summan eron sopimusrivien rivisummien kesken. Jako tehdään suhteessa rivien osuuteen sopimuksen tai sopimustarjouksen yhteistuotosta. Seuraavassa kullakin rivillä tehtävien toimenpiteiden luettelossa kuvataan tämän menetelmän perusajatus:  

1. Tuottoprosenttiosuus lasketaan seuraavasti: **Tuotto**-kentän sisältö jaetaan kaikkien sopimusrivien **Tuotto**-kenttien yhteissummalla.  
2. **Rivisumma**-kentän arvo päivitetään lisäämällä siihen uuden ja lasketun vuosittaisen summan ero kerrottuna tuottoprosenttiosuudella.  
3. Rivin alennussumma-, Rivialennus-%- ja Tuotto-kenttien sisältö päivitetään **Rivisumma**-kentän uuden arvon mukaisesti:  

    * Rivin alennussumma = Rivin arvo - Rivisumma.  
    * Rivialennus-% = Rivin alennussumma / Rivin arvo * 100.  
    * Tuotto = Rivisumma - Rivikustannus.  

#### <a name="example-2"></a>Esimerkki
Huoltosopimuksen **Salli epätäsmäävät summat**-valintaruutua ei ole valittu, ja sopimus sisältää kolme sopimusriviä, joilla on seuraavat tiedot:  

|Nimike|Rivikustannus|Rivin arvo|Rivialennus-%|Rivin alennussumma|Rivisumma|Tuotto|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Nimike 1|20,00|25,00|0,00|0,00|25,00|5,00|  
|Nimike 2|50,00|58,00|5,00|2,90|55,10|5,10|  
|Nimike 3|100,00|115,00|2,00|2,30|112,70|12,70|  

**Vuosittainen summa** -kentän arvo on sama kuin **Laskettu vuosittainen summa**-kentän arvo, joka on aina rivisummien yhteissumma. Tässä tapauksessa se on yhtä suuri kuin seuraava: 25,00 + 55,10 + 112.70 = 192,80.  

 Jos muutat **Vuotuinen summa** -kohdan arvoksi 180, jokaiselle sopimusriville lasketaan tuottoprosenttiosuudet:  

* Nimike 1 – 5 / (5 + 5,1 +1 2,7) = 0,2193 %  
* Nimike 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Nimike 3 – 12,7 / (5 + 5,1 +12,7) = 0,557 %  

Kunkin sopimusrivin **Rivisumma**-kentän arvo päivitetään sitten käyttämällä seuraavaa kaavaa Rivisumma = Rivin arvo + uuden ja lasketun vuosittaisen summan ero * prosenttiosuus. Tämän jälkeen **Rivin alennussumma**-, **Rivialennus-%**- ja **Tuotto**-kenttien arvot päivitetään edellä olevan toimenpideluettelon kohdan 3 kaavoja käyttäen.  

Sopimusriveillä on lopuksi seuraavat tiedot:  

|Nimike|Rivikustannus|Rivin arvo|Rivialennus-%|Rivin alennussumma|Rivisumma|Tuotto|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Nimike 1|20,00|25,00|11,24|2,81|22,19|2,19|  
|Nimike 2|50,00|58,00|9.93|5.76|52.24|2.24|  
|Nimike 3|100.00|115.00|8.20|9.43|105.57|5.57|  

## <a name="see-also"></a>Katso myös
[Huoltosopimusten ja huoltosopimustarjousten luominen](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Huoltohallinnon määrittäminen](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
