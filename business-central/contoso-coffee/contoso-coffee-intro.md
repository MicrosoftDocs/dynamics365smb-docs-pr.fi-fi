---
title: Johdatus Contoso Coffee -demotietoihin
description: 'Yleiskuvaus tilanteista, joissa Contoso Coffee -demotietojen avulla opit käyttämään Business Centralin ominaisuuksia.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.date: 09/20/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '5194,'
ms.custom: bap-template
---

# Johdatus Contoso Coffee -demotietoihin

Contoso Coffee on kuvitteellinen yritys, joka tuottaa kuluttajille ja yrityksille kahvinkeittimiä. **Contoso Coffee** -sovellukset kohteelle [!INCLUDE [prod_short](../includes/prod_short.md)] lisäävät demotietoja, joiden avulla voit opetella käyttämään ominaisuuksia kohteessa [!INCLUDE [prod_short](../includes/prod_short.md)].  

## Contoso Coffee -tietojen määrittäminen

[!INCLUDE [contoso-coffee-app-install](contoso-coffee-app-install.md)].

Kun sovellukset on asennettu, valmistele seuraavat moduulit **Contoson demotyökalu** -sivulla käyttämällä **Määritä**-toimintoa. Voit valita, että asennat kaikki käytettävissä olevat tiedot, kuten asetus- ja tuotantotiedot, tai ainoastaan asetustiedot.

 - **Yleinen-moduuli**, joka valmistelee yleiset asetukset, jotka [!INCLUDE [prod_short](../includes/prod_short.md)] tarvitsee. Tällaisia voivat olla esimerkiksi numerosarjat. 

Asetukset kuvaillaan seuraavassa taulukossa:  

|Kenttä  |Kuvaus  |
|---------|---------|
|**Aloitusvuosi** |Määrittää ensimmäisen vuoden, jota haluat käyttää Contoso Coffee -demotiedoissa. Yrityksen asetuksista riippuen vuosi on joko kalenterivuosi tai tilikausi.|
|**Maa- tai aluekoodi**|Määrittää maa- tai aluekoodin kotimaan asiakkaille ja toimittajille.|
|**Yritystyyppi**    |Määrittää, onko valitun yrityksen ilmoitettava ALV vai myyntivero. |
|**Hintakerroin**     |Määrittää kertoimen, jolla hinta muunnetaan USD/EUR-valuutasta paikalliseksi valuutaksi. *1* tarkoittaa, että hinta on sama summa kaikissa valuutoissa. Korkeampaa numeroa käytetään, kun hinta saadaan paikallisena valuuttana. |
|**Pyöristystarkkuus**  |Määrittää pyöristystarkkuuden, jolla esittelytiedot luodaan.|

 - [Tuotantomoduuli](manufacturing/contoso-coffee-manufacturing-intro.md) valmistautumiseen [tuotantoskenaarioita](manufacturing/contoso-coffee-manufacturing-intro.md#scenarios) varten
 - [Varastointimoduuli](warehousing/contoso-coffee-warehousing-intro.md) valmistautumiseen [varastoinnin skenaarioita](warehousing/contoso-coffee-warehousing-intro.md#scenarios) varten.
 - [Huoltomoduuli](service/contoso-coffee-service-intro.md) valmistautumiseen [huollon skenaarioita](service/contoso-coffee-service-intro.md#scenarios) varten.

Kun olet määrittänyt moduulit, joita haluat kokeilla, luo niille esimerkkitiedot valitsemalla **Luo**-toiminto.

## Katso myös

[Tuotanto](../production-manage-manufacturing.md)  
[Varastointi](../warehouse-manage-warehouse.md)  
[Palvelu](../service-service.md)
<!-- [Projects and Jobs](../projects-manage-projects.md) -->

