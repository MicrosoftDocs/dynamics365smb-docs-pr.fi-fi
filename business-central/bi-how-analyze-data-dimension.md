---
title: Analysoi tiedot dimensioiden mukaan
description: 'Tässä artikkelissa kuvataan, miten liiketoimintatietoja voidaan analysoida dimensioiden avulla saadaksesi paremman käsityksen yrityksestäsi.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '545, 555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="analyze-data-by-dimensions"></a>Analysoi tiedot dimensioiden mukaan

Talousanalyysissä dimensio on tieto, jonka lisäät tapahtumaan eräänlaiseksi merkiksi. Tämän tiedon avulla voi yhdistää ryhmiksi tapahtumia, joilla on samoja ominaisuuksia, kuten asiakkaita, alueita, tuotteita tai myyjiä, sekä noutaa nämä ryhmät helposti analysoitavaksi. Dimensioita voi käyttää päiväkirjojen tapahtumissa, asiakirjoissa ja budjeteissa. 

Kukin dimensio kuvaa analysoinnin fokusta. Joten esimerkiksi kaksidimensioinen analyysi voisi olla myynti per alue. Käyttämällä tapahtumaa luodessasi useita dimensiota voit luoda monimutkaisia analyysejä, kuten myynti per myyntikampanja per asiakasryhmä per alue. Saat liiketoiminnasta selkeän kuvan ja voit arvioida esimerkiksi, miten hyvin yritys toimii, missä se menestyy ja missä ei, sekä minne pitäisi kohdentaa enemmän resursseja, otta voit tehdä tietoisempia päätöksiä siirtyessäsi eteenpäin. Lisätietoja on kohdassa [Dimensioiden käsitteleminen](finance-dimensions.md).

> [!TIP]
> Tapahtumatietoja voi analysoida nopeasti dimensioiden mukaan suodattamalla tilikarttojen loppusummat ja kaikkien **Tapahtumat**-sivujen tapahtumat dimensioittain. Hae **Määritä dimension suodatus** -toiminto.

> [!NOTE]
> Jos havaitset, että kirjatuissa pääkirjanpidon tapahtumissa on käytetty virheellistä dimensioarvoa, voit korjata sen ja päivittää analyysinäkymät. Lisätietoja on [Vianmääritys ja dimensioiden korjaaminen](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting) -osassa.

## <a name="set-up-an-analysis-view"></a>Analyysinäkymän luominen

Dimensioittainen analyysi käyttää valittua dimensioyhdistelmää. Kyseinen dimensiojoukko tallennetaan, noudetaan ja päivitetään luomalla **analyysinäkymä**-kortti. 

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Analyysinäkymät**, valitse sitten vastaava linkki.  
2. Valitse **Analyysinäkymän luettelo** -sivulla **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Jos haluat lisätä muita dimensiokoodeja neljän **Dimensiot**-pikavälilehden koodin lisäksi, valitse **Suodatin**-toiminto, täytä kentät ja valitse **OK**.  
5. Voit päivittää näkymän valitsemalla **Päivitä**-toiminnon.

## <a name="analyze-by-dimensions"></a>Analyysi dimensioiden mukaan

Käytä analyysinäkymiä, jotka olet jo määrittänyt **analyysi dimension mukaan** -matriisilla, nähdäksesi pääkirjapidon summia.   

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Analyysinäkymät**, valitse sitten vastaava linkki.  
2. Valitse haluamasi analyysinäkymä ja valitse sitten **Analyysi dimensioittain** -toiminto.
3. Täyttämällä **Analyysi dimensioittain** -sivun yläosan kentät määrität, mitkä tiedot näytetään ja miten ne näytetään.
4. Avaa määritettyyn analyysinäkymään liittyvä matriisisivu valitsemalla **Näytä matriisi** -toiminto.
5. Voit näyttää matriisisivulla näkyvän summan määrityksen siirtymällä siihen valitsemalla summan.  

- Vasemmanpuoleisimmisssa sarakkeissa oleva tieto perustuu otsikon **Näytä riveinä** -kentässä tekemääsi valintaan.  
- Oikeanpuoleisissa sarakkeissa oleva tieto perustuu otsikon **Näytä sarakkeina** -kentässä tekemääsi valintaan.

> [!IMPORTANT]  
> **Analyysinäkymä**-kortin Pvmtiivistys-kentässä määritettyä jaksoa lyhyempää jakson pituutta ei voi valita. **Seuraava joukko**- ja **Edellinen joukko** -komennot eivät ole käytettävissä, jos olet valinnut **Jakso**-vaihtoehdon **Näytä riveinä**- tai **Näytä sarakkeina** -kentässä.  

> [!NOTE]  
> Voit käyttää **Dimensiot - Yksityiskohdat** -raporttia, kun haluat yksityiskohtaisen erittelyn siitä, miten dimensioita on käytetty tapahtumissa tietyn ajanjakson aikana. **Dimensiot - Yhteensä** -raporttia voidaan käyttää yhteissummien tarkastelemiseen.  

> [!TIP]  
> Voit muuttaa näkymää myös muuttamalla **Näytä riveinä**- ja **Näytä sarakkeina** -kenttien sisältöä. Voit peruuttaa näkymäasetukset **Muuta rivit ja sar. käänt.** -toiminnolla.

## <a name="update-an-analysis-view"></a>Analyysinäkymän päivittämien

Summat, jotka näkyvät **Analyysi dimensioittain** -sivulla, kuvaavat yrityksen tilaa viimeisimmän päivityksen aikaan. Jos haluat nähdä nykyisen tilanteen, sinun on päivitettävä analyysinäkymä suorittamalla päivitystoiminto.

Seuraavan menettelyn avulla voit päivittää analyysinäkymän **Analyysi dimensioittain** -sivulla. Vaiheet ovat samanlaiset, kuin päivitys **Analyysinäkymän kortti** ja **Analyysinäkymän luettelo** -sivuilla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Analyysinäkymät**, valitse sitten vastaava linkki.
2. Valitse haluamasi analyysinäkymä ja valitse sitten **Analyysi dimensioittain** -toiminto.
3. Valitse **Analyysi dimensioittain** -sivulla **Analyysinäkymän koodi** -kenttä.  
4. Valitse asianomaisen analyysinäkymän rivi.  
5. Valitse **Analyysinäkymät**-sivulla ensin analyysinäkymä, sitten **Päivitä**-toiminto.  

> [!TIP]  
> Jos valitset **Päivitä kirjattaessa** -valintaruudun analyysinäkymän kortilla, näkymä päivitetään automaattisesti liittyvää tapahtumaa kirjattaessa.

> [!NOTE]  
> Kun haluat päivittää joitakin tai kaikkia analyysinäkymiä samanaikaisesti, sinun täytyy käyttää **Päivitä analyysinäkymät** -eräajoa.  

## <a name="see-also"></a>Katso myös

[Taloushallinnon liiketoimintatiedot](bi.md)  
[Taloushallinto](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
