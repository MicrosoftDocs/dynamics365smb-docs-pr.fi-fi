---
title: Käytä tilastotilejä muiden kuin tapahtumatietojen analysoimiseen
description: 'Tietoja siitä, miten tilastollisia tilitietoja voidaan käyttää analyysien toisena tietolähteenä.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/07/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, financial report'
ms.search.form: '2632, 2631, 2633, 2623, 2634'
ms.service: dynamics-365-business-central
---
# Analysoi tietoja tilastotilien avulla

Kirjanpitoraporttien avulla voit täydentää tilastotietoja. Tilastolliset tilit mahdollistavat muihin kuin tapahtumatietoihin perustuvien tietojen lisäämisen. Lisää muut kuin tapahtumapohjaiset tiedot numeropohjaisiin yksiköihin, kuten:

* Työntekijöiden määrä
* Neliömetrit
* Erääntyneiden asiakkaiden määrä

Voit esimerkiksi mitata tuottoa tai kustannuksia osaston henkilöstön lukumäärän perusteella. Osaston henkilöstömäärä on tilastotilin yksikkö. Seuraavassa kuvassa on esimerkki raportista, jossa on työntekijän tuottoon käytetty tilastotili.

:::image type="content" source="media/statistical account report example.png" alt-text="Esimerkki raportista, jossa on tilastotilin tietoja":::

Toimintatavoiltaan tilastotilit ovat samankaltaisia kuin kirjaustilit. Ne tallentavat tapahtumat, jotka kirjataan tilastotilin päiväkirjojen avulla, joten voit käyttää tapahtumia talousraporttien tietojen pohjana. Lisätietoja talousraporteista on kohdassa [Financial Reportingin valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md). 

Tilastollisissa tileissä ja kirjaustileissä on muutama erottava avaintekijä. Tilastotilit ovat erillisiä entiteettejä, eivätkä ne sisälly päätilin saldoraportteihin. Sinun ei myöskään tarvitse tasapainottaa debet- ja kredit-summaa, kun käytät tilastotilin päiväkirjoja kirjataksesi tapahtumia tilastotilille. Sinä vain kirjaat summan.

## Tilastollisen tilin määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilastolliset tilit**, valitse sitten vastaava linkki.
1. Täytä  **Yleinen**-pikavälilehden kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Kirjaa määrät tilastolliseen tiliin

1. Kun haluat kirjata seurattavat määrät, valitse **Tilastolliset tilit** -sivulla **Tilastotilin päiväkirja** -toiminto.
1. Syötä **Kirjauspvm**-kenttään viimeinen päivämäärä, jolla haluat kirjauskaudella kirjata summia.
1. Valinnainen: Jos haluat seurata tietyn asiakirjan summaa, syötä **asiakirjannro**-kenttään asiakirjan tunnus.
1. Valitse **Tilastollisen tilin nro** -kentässä tilastotili, johon haluat kirjata määrät.
1. Syötä **Kuvaus**-kenttään lyhyt kuvaus siitä, mitä mittaat.  
1. Syötä kirjattava summa **Summa**-kenttään. 
1. Valinnainen: Jos haluat sisällyttää tilastotilin myös kehittyneemmille analyyseille, määrittele dimensiot **Osastokoodi**- ja **Asiakasryhmäkoodi**-kenttiin. Saat lisätietoja dimensioista siirtymällä kohtaan [Tietojen analysoiminen dimensioittain](bi-how-analyze-data-dimension.md).

## Tarkista tilastollisen tilin summat

Käytä **Tilastotilit**-sivulla **Tilastotilien saldo** -toimintoa varmistaaksesi, että rekisteröidyt summat ovat oikein kullekin ajanjaksolle.  

## Sisällytä tilastotili talousraporttiin

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
1. Luo uusi rahoitusraportti jollakin seuraavista tavoista:
    1. Voit aloittaa alusta valitsemalla **Uusi**. Saat lisätietoja talousraporttien luomisesta valitsemalla [Luo uusi rahoitusraportti](bi-how-work-account-schedule.md#create-a-new-financial-report).
    1. Jos haluat käyttää jo olemassa olevan samankaltaisen raportin asetuksia, valitse kopioitava raportti ja valitse sitten **Kopioi taloudellinen raportti** -toiminto. Voit muokata uuteen raporttiin kopioitavia asetuksia.
1. Lisää tilastotili:
    1. Jos aloitat tyhjästä, valitse **Muokkaa rivimääritystä** -toiminto.
    1. Jos haluat käyttää olemassa olevan raportin rivimääritystä, valitse kopioitava raportti ja valitse sitten **Kopioi rivimääritys** -toiminto.
1. Valitse **Rivimääritys**-sivu **Rivinro**-kohdasta -kentässä voit määrittää, missä rivi näkyy raporttirivien järjestyksessä.
1. Syötä **Kuvaus**-kenttään teksti, joka kuvaa siitä, mitä mittaat.
1. Valitse **Summaustyyppi**-kentässä **Tilastotilit**.
1. Valitse **Summaus**-kentässä tilastotili.
1. Valitse **Rivityyppi**-kentässä, haluatko tarkastella saldoa kirjauspäivämääränä vai kirjausjakson alussa, tai näyttää muutoksen summaan jakson aikana.
1. Täytä jäljellä olevat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Katso myös

[Taloudelliset liiketoimintatiedot](bi.md)  
[Talousraportit ja analytiikka Business Centralissa](finance-reports.md)