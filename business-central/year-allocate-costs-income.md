---
title: Kustannusten ja tulojen kohdistustehtävien yleiskatsaus
description: 'Tässä ohjeaiheessa kerrotaan tehtävistä, joilla voi kohdistaa toistuvan yleisen päiväkirjan tapahtuman useille eri tileille päiväkirjan kirjaamisen yhteydessä.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.devlang: al
ms.search.form: '283, 5629'
ms.date: 08/08/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="allocate-recurring-costs-and-income"></a>Toistuvien kustannusten ja tulojen kohdistaminen

Voit kohdistaa toistuvan yleisen päiväkirjan tapahtuman useille tileille päiväkirjan kirjaamisen yhteydessä. Jos haluat lisätietoja toistuvista yleisistä päiväkirjoista, siirry kohtaan [Toistuvien tapahtumien päiväkirjojen käyttäminen](ui-work-general-journals.md#work-with-recurring-journals). 

Kohdistamisen voi tehdä kolmella eri tavalla:

* Määrä
* prosenttiosuus (%)
* Summa

Kohdistustoimintoja voi käyttää toistuvien yleisten päiväkirjojen ja käyttöomaisuuspäiväkirjojen kanssa.
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

Seuraavaksi kerrotaan, miten kustannusten kohdistus valmistellaan toistuvissa yleisessä päiväkirjassa määrittämällä kohdistusavaimet. Kun kohdistusavaimet on määritetty, voit suorittaa ja kirjata päiväkirjan muiden toistuvien yleisten päiväkirjojen tavoin. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

## <a name="to-set-up-allocation-keys"></a>Kohdistusavaimien määrittäminen

Voit kohdistaa toistuvan yleisen päiväkirjan tapahtuman useille eri tileille päiväkirjan kirjaamisen yhteydessä. Kohdistus voidaan tehdä määrän, prosentin tai summan mukaan.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, syötä **Toistuvat yleiset päiväkirjat** ja valitse linkit.
2. Valitse **Erän nimi** -kenttä, kun haluat avata **Yleisen päiväkirjan erät** -sivun.
3. Voit muokata luettelon olemassa olevan erän kohdistuksia tai luoda uuden erän ja kohdistukset.
   * Luo uusi erä valitsemalla **Uusi**-toiminto ja siirtymällä seuraavaan vaiheeseen.
   * Voit muuttaa olemassa olevan päiväkirjan kohdistuksia valitsemalla päiväkirjan ja siirtymällä vaiheeseen 7.    
4. Syötä **Nimi**-kenttään erän nimi, esimerkiksi SIIVOUS. Syötä **Kuvaus**-kenttään kuvaus, esimerkiksi Siivouskulujen päiväkirja.
5. Kun olet valmis, sulje sivu. Esiin tulee uusi tyhjä toistuva kirjaus.
6. Täytä rivin kentät.
7. Valitse **Kohdistukset**-toiminto.
8. Lisää rivi jokaista kohdistusta varten. Sinun täytyy täyttää jokin seuraavista kentistä: **Kohdistus- %**, **Kohdistettava määrä** tai **Summa**. Sinun täytyy myös täyttää Tilinro.- **kenttä.** ja jos kohdistat tapahtuman globaaleille dimensioille, yleinen dimensio kenttiä.
9. Jos syötät riville prosentin, ohjelma laskee **Summa**-kentän arvon automaattisesti. Näillä summilla on vastakkainen merkki kuin kokonaissummalla toistuvan kirjauksen **Summa**-kentässä.
10. Kun olet syöttänyt kohdistusrivit, valitse **OK** palataksesi takaisin **Toistuva yleinen päiväkirja** -sivulle. **Kohdistettu summa (USD)** -kenttä on täytetty ja vastaa **Summa** -kenttää.
11. Kirjaa päiväkirja.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Aiemmin määritetyn kohdistusavaimen muuttaminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, syötä **Toistuvat yleiset päiväkirjat** ja valitse linkit.
2. Valitse Toistuvien yleisten **päiväkirjojen sivulta päiväkirja, jossa kohdistus** on.
3. Valitse ensin kohdistuksen rivi ja sitten **Kohdistukset**-toiminto.
4. Vaihda soveltuvat kentät ja valitse sitten **OK**.

## <a name="see-also"></a>Katso myös

[Tilikauden päättämisvuodet ja -jaksot](year-close-years-periods.md)    
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)    
[Asiakirjojen ja päiväkirjojen kirjaaminen](ui-post-documents-journals.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
