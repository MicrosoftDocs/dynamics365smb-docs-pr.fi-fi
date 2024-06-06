---
title: Perusraportit ja asiakirjat tuotos nopeasti käynnistyy
description: Business Central tarjoaa sisäänrakennettuja malleja raporteille ja asiakirjoille sekä monia mukautusvaihtoehtoja niiden mukauttamiseksi yrityksesi tarpeisiin.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: quickstart
ms.search.form: null
ms.date: 05/17/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="basic-reports-and-documents-output-quick-start"></a>Perusraportit ja asiakirjat tuotos nopeasti käynnistyy

Jos haluat sopeuttaa [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen yrityksesi tarpeisiin, aseta ja käytä raportteja ja räätälöityjä asiakirjoja, jotka sopivat yrityksesi prosesseihin ja visuaaliseen identiteettiin.

## <a name="add-your-company-logo-to-documents"></a>Lisää yrityksesi logo asiakirjoihin

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää malleja, jotka on asetettu käyttämään yrityksesi logoa, mikä säästää aikaa asiakirjojen, kuten laskujen, tilausten ja tiliotteiden, mukauttamiseen.

1. Valitse ![Hammaspyörä-kuvake, joka avaa Asetukset-valikon.](media/ui-experience/settings_icon_small.png) -valikko, valitse sitten **Yrityksen tiedot** -toiminto.
2. Valitse ensin **Kuva**-toiminto ja sitten **Valitse**.
3. Valitse laitteessa oleva kuvatiedosto.

Kun kuva näkyy Kuva-kentässä **·**, voit sulkea **Oman yrityksen tiedot** -sivun.

## <a name="run-reports"></a>Raporttien suorittaminen

Raportit järjestävät tietoja eri lähteistä [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa ja esittävät ne luettavassa muodossa, joka voidaan helposti tulostaa tai jakaa digitaalisesti. Raportit ovat sivuilla, joihin ne on liitetty asiasisällön yhteydessä. Esimerkiksi **Nimikkeet**-sivulla on luettelo raporteista, jotka liittyvät varastotasoihin, ostoihin ja myynteihin.

1. Avaa pyydettyyn raporttiin liittyvä sivu, esimerkiksi **Nimikkeet**-sivu.
2. Valitse **Raportit**-valikosta **Varasto - Top 10** -luetteloraportti.
3. Määritä raportin pyyntösivulla suodattimet kaventaaksesi ajanjaksoa tai muuttaaksesi raportissa käytettyä mittayksikköä.
4. Valitse **Tulostus**-toiminto ja noudata laitteen tulostusvaiheita.
    1. Vaihtoehtoisesti voit valita **esikatselu**-toiminnon, joka näyttää raportin näytössä.

Saat lisätietoja tietojen suodattamisesta, raporttien ajoittamisesta ja lisätietoja kohdasta [Suorita ja tulosta raportteja](ui-work-report.md).

## <a name="save-reports-as-pdf-excel-or-word-documents"></a>Tallentaminen PDF-, Excel- tai Word-tiedostoina

Voit jakaa raportteja nopeasti tallentamalla [!INCLUDE[prod_short](includes/prod_short.md)] -raportit suoraan PDF-, Microsoft Excel- tai Microsoft Word -asiakirjoihin.

1. Toista vaiheet 1-3 edellä olevassa [Suorita raportit](#run-reports) -osassa.
2. Valitse **Lähetä kohteeseen** -toiminto.
3. Valitse tiedostotyyppi ja valitse sitten **OK**.
Luotu raporttitiedosto tallentuu automaattisesti selaimen latauskansioon.

### <a name="change-report-and-document-layouts"></a>Muutosraportti ja asiakirjojen asettelu

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää useita valmiita asetteluita raportteihisi ja muihin luomiisi asiakirjoihin, kuten myyntilaskuihin. Voit käyttää esimerkiksi Microsoft Word- tai Excel-sovelluksia asiakirjojen ja raporttien asettelumallien muokkaamiseen seuraavassa esimerkissä kuvatulla tavalla:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttiasettelut**, valitse sitten vastaava linkki.
2. Valitse **Raportin asettelut** - sivulla **Etsi** -toiminnon avulla *StandardSalesInvoice.docx*-asettelu ja lataa sitten asettelumallitiedosto valitsemalla **Vie asettelu** -toiminto.

    Laitteeseesi tallennetaan Word-asiakirja, jossa on sama nimi kuin **Raportin asettelut** -sivulla.
3. Avaa asettelutiedosto Microsoft Wordissa ja muokkaa asiakirjaa esimerkiksi siirtämällä pvm-kenttää (*DocumentDate*) tai logoa tai muuttamalla fonttikokoja ja tallentamalla sitten tiedosto.
4. Taas **Raporttiasettelut**-sivulla valitse **Uusi asettelu** -toiminto.
5. Kirjoita nimi ja kuvaus **Lisää uusi asettelu raporttiin** -sivulle **Asettelun nimi**- ja **Kuvaus**-kenttiin, jotta asettelu olisi helppo löytää.
6. Valitse **Muotoiluasetukset**-kentässä **Word**-vaihtoehto ja valitse sitten **OK**.
7. Avaa muokattu asettelutiedosto laitteessa valitsemalla **Valitse Word-asettelu** -sivulla **Valitse**.
8. Testaa uusi asettelu valitsemalla **Suorita raportti** -toiminto.

Lisätietoja raporttien ja asiakirjojen mukauttamisesta liiketoimintatarpeisiin kohdassa [Raportti- ja asiakirja-asettelut](ui-manage-report-layouts.md).

## <a name="see-also"></a>Katso myös

[Raporttien käyttäminen päivittäisessä työssä](reports-use-reports.md)  
[Käytettävissä olevat raportit kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Asiakirjaraporttien valinta](across-report-selections.md)  
[Business Centralin pika-aloitus](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
