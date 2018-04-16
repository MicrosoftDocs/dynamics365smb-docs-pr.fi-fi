---
title: "Nimikekulujen määrittäminen myyntiin ja ostoihin| Microsoft Docs"
description: "Jos haluat, että varastonimikkeisiin liittyy lisäkustannuksia, kuten nimikkeiden ostamisessa ja myynnissä syntyvät rahti-, käsittely-, vakuutus- ja kuljetuskulut, voit käyttää nimikekuluominaisuutta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: transportation, added cost
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5a40482673c8b8110a6036046174a58f5d7be18f
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="use-item-charges-to-account-for-additional-trade-costs"></a>Kaupan lisäkustannusten huomiointi nimikekulujen avulla
Voit varmistaa oikean arvostuksen liittämällä varastonimikkeisiin lisäkustannukset, kuten nimikkeiden ostamisessa ja myynnissä syntyvät rahti-, käsittely-, vakuutus- ja kuljetuskulut. Ostoissa ostetun nimikkeen kokonaiskustannukset koostuvat toimittajan ostohinnasta ja kaikista suorista lisänimikekuluista, jotka voidaan määritellä yksittäisiin vastaanottoihin tai palautustoimituksiin. Myynnissä Myytyjen nimikkeiden lähetyskulujen tietäminen voi olla yritykselle yhtä tärkeää kuin ostettujen nimikkeiden kokonaiskustannusten tietäminen.

Lisäkustannuksen varastoarvoon kirjaamisen lisäksi voit käyttää nimikekuluominaisuutta seuraavissa tilanteissa:

- Saapuneen nimikkeen kulun määrittäminen, jotta voidaan tehdä täsmällisiä päätöksiä jakeluverkon optimoimiseksi.
- Nimikkeen yksikkökulun tai yksikköhinnan erittely analyysia varten.
- Ostohyvitysten sisällyttäminen yksikkökuluun ja myyntihyvitysten yksikköhintaan.

Ennen nimikekulujen määrittämistä on määritettävä erityyppisten nimikekulujen nimikekulunumerot, mukaan lukin KP-tilit, joille myyntiin, ostoihin ja varaston muutoksiin liittyvät kustannukset kirjataan. Nimikekulunumero sisältää yleisen tuotteen kirjausryhmän, veroryhmäkoodin, tuotteen ALV-kirjausryhmän ja nimikekulun yhdistelmä. Kun nimikekulunumero annetaan osto- tai myyntiasiakirjassa, liittyvä KP-tili haetaan nimikkeen kulunumeroasetusten ja yksittäisen asiakirjan tietojen perusteella.

Nimikekulun voi määrittää sekä osto- että myyntiasiakirjoissa kahdella tavalla:
- Asiakirjassa, jossa on luettelo nimikkeistä, joihin nimikekulu liittyy. Tämä tehdään yleensä asiakirjoissa, joita ei ole vielä kokonaan kirjattu.
- Erillisessä laskussa linkittämällä nimikekulu linkitetään kirjattuun vastaanottoon tai lähetykseen, jossa on luettelo nimikkeistä, joihin nimikekulu liittyy.

> [!NOTE]  
>   Voit määrittää nimikekulut myynneissä ja ostoissa tilauksiin, laskuihin ja hyvityslaskuihin. Seuraavat toimenpiteet kuvaavat, miten ostolaskujen nimikekuluja käsitellään. Vaiheet ovat samanlaiset kaikissa osto- ja myyntiasiakirjoissa.

## <a name="to-set-up-item-charge-numbers"></a>Nimikekulunumeroiden määrittäminen
Nimikekulunumeroita käytetään erottelemaan eri tyyppisiä nimikekuluja, joita yrityksessäsi käytetään ostoasiakirjoille.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Nimikekulut** ja valitse sitten aiheeseen liittyvä linkki.
2. Luo uusi rivi valitsemalla **Nimikekulut**-ikkunassa **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item"></a>Nimikekulun määrittäminen suoraan nimikkeen ostolaskuun
Jos tiedät nimikekulun nimikkeen ostolaskua kirjatessa, toimi seuraavasti.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostolaskut** ja valitse sitten aiheeseen liittyvä linkki.
2. Luo uusi ostolasku. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).
3. Varmista, että ostolasku on vähintään yksi rivi Nimike-tyyppinen rivi.
4. Valitse uuden rivin **Tyyppi**-kentässä **Kulu (nimike)**.
5. Anna **Määrä**-kenttään laskutetun nimikekulun yksiköt.
6. Anna **Välitön yksikkökustannus** -kentässä nimikekulun summa.
7. Täytä tarvittavat jäljellä olevat kentät. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Varsinainen määritys tehdään seuraavissa vaiheissa. **Määriteltävä määrä** -kentän arvo näkyy punaisella fontilla, kunnes nimikekulu on määritetty kokonaan.
8. Valitse **Rivit**-välilehdessä **Nimikekulujen määritys** toiminto.

    Avautuvassa **Nimikekulujen määritys** -ikkunassa näkyy yksi rivi kutakin ostolaskun Nimike-tyypin riviä. Voit määrittää nimikekululle vähintään yhdelle laskuriville käyttämällä toimintoa, joka määrittää ja jakaa sen puolestasi. Vaihtoehtoisesti voit täyttää **Määritettävä määrä** -kentän manuaalisesti. Seuraavissa vaiheissa kerrotaan, miten kuvataan, miten nimikekulujen määrityksen ehdotustoimintoa käytetään.

9. Valitse **Nimikekulun määritys** -ikkunassa **Ehdota nimikk. kulumääritystä** -toiminto.
10. Jos Nimike-tyyppisiä laskurivejä on useita, valitse yksi neljästä jakeluvaihtoehdosta.  

Jos nimikekulu on määritetty kokonaan, ostolaskun **Määriteltävä määrä** -kentän arvo on nolla.

Nimikekulu on nyt määritetty ostolaskuun. Kun kirjaat ostolaskun vastaanoton, nimikkeiden varastoarvot päivitetään nimikekulun kustannusten arvolla.  

## <a name="to-assign-an-item-charge-from-a-separate-invoice-to-the-purchase-invoice-for-the-item"></a>Nimikekulun määrittäminen erillisestä laskusta nimikkeen ostolaskuun
Jos vastaanotit nimikekulun laskun alkuperäisen laskun vastaanoton kirjaamisen jälkeen, toimi seuraavasti.
1. Toista Nimikekulun määrittäminen suoraan nimikkeen ostolaskuun -kohdan vaiheet 1–8.
2. Valitse **Nimikekulujen määritys** -ikkunassa **Hae vastaanoton rivit** -toiminto.
3. Valitse **Oston vast.otto rivit** -ikkunassa sen nimikkeen kirjattu oston vastaanotto, johon haluat määrittää nimikekulun, ja valitse sitten **OK**-painike.
4. Valitse **Ehdota nimikk. kulumääritystä** -toiminto.

Erillisen ostolaskun nimikekulu on nyt määritetty kirjatun oston vastaanoton nimikkeelle, joten nimikkeen varastoarvo päivitetään nimikekulun kustannuksella.

## <a name="see-also"></a>Katso myös
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Ostojen kirjaus](purchasing-how-record-purchases.md)  
[Myynnin laskutus](sales-how-invoice-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

