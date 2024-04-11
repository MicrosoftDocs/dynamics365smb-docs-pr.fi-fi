---
title: Analysoi tiedot dimensioiden mukaan
description: 'Tässä artikkelissa kuvataan, miten liiketoimintatietoja voidaan analysoida dimensioiden avulla saadaksesi paremman käsityksen yrityksestäsi.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: kepontop
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '545, 555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Tietojen analysoiminen dimensioiden mukaan

Talousanalyysissä dimensio on tieto, joka lisätään tapahtumaan eräänlaiseksi merkiksi ryhmitellä tapahtumia, joissa on samankaltaisia ominaisuuksia. Dimensiot esimerkiksi ryhmittelevät usein asiakkaiden, alueiden, tuotteiden ja myyjien tapahtumat. Ryhmien avulla on helppo noutaa niitä koskevia tietoja analysoitavaksi. Dimensioita voidaan käyttää päiväkirjojen tapahtumissa, asiakirjoissa ja budjeteissa.

Kukin dimensio kuvaa sitä, mihin analysointi keskittyy. Joten esimerkiksi kaksidimensioinen analyysi voisi olla myynti per alue. Useamman kuin kahden dimension käyttäminen tapahtumaa luotaessa mahdollistaa monisyisen analysoinnin. Esimerkki monimutkaisesta analyysista on perehtyä alue-, asiakasryhmä- ja myyntikampanjakohtaiseen myyntiin. Näin saadaan entistä enemmän merkityksellisiä tietoja liiketoiminnasta. Tällaisia tietoja ovat esimerkiksi se, miten hyvin yritys toimii, missä se menestyy ja missä ei sekä minne pitäisi kohdentaa enemmän resursseja. Nämä merkitykselliset tiedot auttavat tekemään tietopohjaisia liiketoimintapäätöksiä. Lisätietoja on kohdassa [Dimensioiden käsitteleminen](finance-dimensions.md).

> [!TIP]
> Tapahtumatietoja voi analysoida nopeasti dimensioiden mukaan suodattamalla tilikarttojen loppusummat ja kaikkien **Tapahtumat**-sivujen tapahtumat dimensioittain. Hae **Määritä dimension suodatus** -toiminto.

> [!NOTE]
> Jos havaitset, että kirjatuissa pääkirjanpidon tapahtumissa oli käytetty virheellistä dimensioarvoa, voit korjata sen ja päivittää analyysinäkymät. Lisätietoja on kohdassa [Vianmääritys ja dimensioiden korjaaminen](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## Analyysinäkymän luominen

Dimensioittainen analyysi käyttää valittua dimensioyhdistelmää. Kyseinen dimensiojoukko tallennetaan, noudetaan ja päivitetään luomalla **analyysinäkymä**-kortti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Analyysinäkymät**, valitse sitten vastaava linkki.  
2. Valitse **Analyysinäkymän luettelo** -sivulla **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Jos haluat lisätä muita dimensiokoodeja neljän **Dimensiot**-pikavälilehden koodin lisäksi, valitse **Suodatin**-toiminto, täytä kentät ja valitse **OK**.  
5. Voit päivittää näkymän valitsemalla **Päivitä**-toiminnon.

## Analyysi dimensioiden mukaan

Käytä analyysinäkymiä, jotka olet jo määrittänyt **analyysi dimension mukaan** -matriisilla, nähdäksesi pääkirjapidon summia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Analyysinäkymät**, valitse sitten vastaava linkki.  
2. Valitse haluamasi analyysinäkymä ja valitse sitten **Analyysi dimensioittain** -toiminto.
3. Täyttämällä **Analyysi dimensioittain** -sivun yläosan kentät määrität, mitkä tiedot näytetään ja miten ne näytetään.
4. Avaa analyysinäkymän matriisisivu valitsemalla **Näytä matriisi** -toiminto.
5. Matriisisivun summan tietoja voi käyttää valitsemalla summa.  

- Vasemmalla olevissa sarakkeissa oleva tieto perustuu otsikon **Näytä riveinä** -kentässä tehtyyn valintaan.  
- Oikealla olevissa sarakkeissa oleva tieto perustuu otsikon **Näytä sarakkeina** -kentässä tehtyyni valintaan.

> [!IMPORTANT]  
> **Analyysinäkymä**-kortin päivämäärätiivistyksessä määritettyä jaksoa lyhyempää jakson pituutta ei voi valita. **Seuraava joukko**- ja **Edellinen joukko** -toiminnot eivät ole käytettävissä, jos **Jakso**-vaihtoehto on valittu **Näytä riveinä**- tai **Näytä sarakkeina** -kentässä.  

> [!NOTE]  
> **Dimensiot - Yksityiskohdat** -raportti sisältää yksityiskohtaisen luokittelun, josta näkyy, miten dimensioita on käytetty valitun jakson tapahtumissa. **Dimensiot - Yhteensä** -raporttia voidaan käyttää yhteissummien tarkastelemiseen.  

> [!TIP]  
> Voit muuttaa näkymää myös muuttamalla **Näytä riveinä**- ja **Näytä sarakkeina** -kenttien sisältöä. Voit peruuttaa näkymäasetukset **Muuta rivit ja sar. käänt.** -toiminnolla.

## Analyysinäkymän päivittämien

**Analyysi dimensioittain** -sivun summat kuvaavat yrityksen tilaa viimeisimmän päivityksen aikaan. Tämän hetkisen tilan saa päivittämällä analyysinäkymään päivitystoiminnolla.

Seuraavan menettelyn avulla voit päivittää analyysinäkymän **Analyysi dimensioittain** -sivulla. Vaiheet ovat samanlaiset, kuin päivitys **Analyysinäkymän kortti** ja **Analyysinäkymän luettelo** -sivuilla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Analyysinäkymät**, valitse sitten vastaava linkki.
2. Valitse haluamasi analyysinäkymä ja valitse sitten **Analyysi dimensioittain** -toiminto.
3. Valitse **Analyysi dimensioittain** -sivulla **Analyysinäkymän koodi** -kenttä.  
4. Valitse asianomaisen analyysinäkymän rivi.  
5. Valitse **Analyysinäkymät**-sivulla ensin analyysinäkymä, sitten **Päivitä**-toiminto.  

> [!TIP]  
> Jos valitset **Päivitä kirjattaessa** -valintaruudun analyysinäkymäkortissa, näkymä päivittyy automaattisesti, kun joku kirjaa liitetyn tapahtuman.

> [!NOTE]  
> **Päivitä analyysinäkymät** -erätyön avulla voi päivittää osan analyysinäkymistä tai kaikki analyysinäkymät samanaikaisesti.  

## Katso myös

[Taloushallinnon liiketoimintatiedot](bi.md)  
[Taloushallinto](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
