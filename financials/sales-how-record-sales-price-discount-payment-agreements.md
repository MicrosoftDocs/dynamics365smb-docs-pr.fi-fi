---
title: Asiakkaiden erikoismyyntihintojen ja -alennusten kirjaaminen | Microsoft Docs
description: "Tässä ohjeaiheessa kerrotaan, miten määritetään vaihtoehtoisten hintojen ja alennusten sopimukset, joita käytetään myyntiasiakirjoissa myytäessä eri asiakkaille."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 07/03/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: 41558d6eec29a277db3cf8f156ae476faf315238
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-record-special-sales-prices-and-discounts"></a>Toimintaohje: Erikoismyyntihintojen ja -alennusten kirjaaminen
Eri asiakkaiden hinta- ja alennussopimukset on määritettävä, jotta asiakkaille luotavissa myyntiasiakirjoissa käytetään sovittuja sääntöjä ja arvoja.

Kun olet kirjannut myynnin ja ostojen erikoishinnat ja rivialennukset, [!INCLUDE[d365fin](includes/d365fin_md.md)] varmistaa, että nimikekaupan tuotto on aina optimaalinen laskemalla automaattisesti parhaan hinnan myynti- ja ostoasiakirjoille sekä projekti- ja nimikepäiväkirjan riville. Lisätietoja on osiossa Parhaan hinnan laskenta.

Myyntiriveille lisätään erikoismyyntihinta, jos tietty asiakkaan, nimikkeen, vähimmäismäärän, mittayksikön sekä aloitus- ja lopetuspäivämäärän yhdistelmä on olemassa.

Voit määrittää seuraavat kaksi myyntialennustyyppiä:

| Alennustyyppi | Kuvaus |
| --- | --- |
| **Myyntirivin alennus** |Myyntiriveille lisättävä summa-alennus, jos tietty asiakkaan, nimikkeen, vähimmäismäärän, mittayksikön sekä aloitus- ja lopetuspäivämäärän yhdistelmä on olemassa. Tätä käytetään samoin kuin myyntihinnoissa. |
| **Laskualennus** |Prosenttialennus, joka vähennetään kokonaissummasta, kun myyntiasiakirjan kaikkien rivien summa ylittää määritetyn vähimmäisarvon. |

Koska myyntihinnat ja myyntirivialennukset perustuvat nimikkeen ja asiakkaan yhdistelmään, voit tehdä tämän määrityksen myös sen nimikkeen kortissa, jota säännöt ja arvot koskevat.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Myyntihinnan määrittäminen asiakkaalle
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakkaan tiliote** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa kyseessä olevan asiakkaan kortti ja valitse **Hinnat**-toiminto.

    **Myynnin tyyppi** -kentän arvoksi esitäytetään **Asiakas**. **Myyntikoodi** -kentän arvoksi esitäytetään asiakasnumero.
3. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Täytä rivi jokaiselle yhdistelmälle, jossa asiakkaalle myönnetään erikoismyyntihinta.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Myyntirivialennuksien määrittäminen asiakkaalle
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakkaan tiliote** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa kyseessä olevan asiakkaan kortti ja valitse **Rivialennukset**-toiminto.

    **Myynnin tyyppi** -kentän arvoksi esitäytetään **Asiakas**. **Myyntikoodi** -kentän arvoksi esitäytetään asiakasnumero.
3. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Täytä rivi jokaiselle yhdistelmälle, jossa asiakkaalle myönnetään myyntirivialennus.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Laskualennuksen määrittäminen asiakkaalle
Kun olet määrittänyt asiakkaat, joille myönnetään laskun alennuksia, määritä laskun alennuskoodi asiakkaiden kortteihin ja määritä kunkin koodin ehdot.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakkaan tiliote** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa sen asiakkaan kortti, jolle myönnetään laskun alennuksia.
3. Valitse **Laskualennuksen koodi** -kentässä asianmukaisille laskualennuksen ehdoille koodi, jonka avulla asiakkaan laskualennukset lasketaan.

    > [!NOTE]  
>   Laskualennuksen koodit löytyvät olemassa olevien asiakkaiden korteista. Näin voit nopeasti liittää laskualennusten ehtoja asiakkaisiin poimimalla sellaisen asiakkaan nimen, jolla on samat ehdot.

    Jatka uuden myyntilaskun alennusehtojen määrittämiseen.
4. Valitse **Asiakkaan kortti** -ikkunassa **Laskualennukset**-toiminto. **Asiakkaan laskualennukset** -ikkuna aukeaa.
5. Syötä **Valuutan koodi** -kenttään sen valuutan koodi, johon rivin laskualennuksen ehdot kohdistetaan. Jätä kenttä tyhjäksi, jos laskualennuksen ehdot määritetään Yhdysvaltojen dollareina.
6. Syötä **Vähimmäissumma**-kenttään laskun vähimmäissumma, joka oikeuttaa alennukseen.
7. Syötä **Alennus-%**-kohtaan laskun alennus prosentteina laskun summasta.
8. Toista vaiheet 5–7 jokaiselle valuutalle, jossa asiakas saa eri laskualennuksen.

Laskualennus on nyt määritetty ja liitetty kyseiselle asiakkaalle. Kun valitset asiakaskoodin muiden asiakkaiden korttien **Laskun alennuskoodi** -kentässä, sama laskualennus liitetään myös näille asiakkaille.

## <a name="sales-invoice-discounts-and-service-charges"></a>Myyntilaskualennukset ja palvelumaksut
Kun käytät laskualennuksia, laskusumman suuruus määrää annettavan alennuksen suuruuden.  

Voit myös lisätä **Asiakkaan laskualennukset** -ikkunassa tietyn summan ylittäville laskuille palvelumaksuja.  

Ennen kuin myynneissä voi käyttää laskualennuksia, ohjelmaan täytyy syöttää tiettyjä tietoja. Täytyy päättää:  

- ketkä asiakkaat saavat tämän tyyppisen alennuksen.  
- mitä alennusprosentteja käytetään.  

Jos haluat ohjelman laskevan automaattisesti laskualennukset, tämän voi määrittää Myyntien ja myyntisaamisten asetukset -ikkunassa.  

Voit määrittää jokaiselle asiakkaalle erikseen, annetaanko tälle laskualennuksia, jos tarve on tyydytetty (eli jos laskusumma on tarpeeksi suuri). Laskualennusehdot voi määrittää PVA:ssa kotimaisille asiakkaille ja ulkomaan valuutassa ulkomaisille asiakkaille.  

Voit linkittää alennusprosentit tiettyihin laskusummiin **Asiakkaan laskualennukset** -ikkunoissa. Voit syöttää mitä tahansa prosenttilukuja kussakin ikkunassa. Jokainen asiakas voi olla erillisessä ikkunassa, tai samaan ikkunaan voi linkittää useita asiakkaita.  

Spesifiseen laskusummaan voi linkittää alennusprosentin lisäksi (tai sen sijaan) palvelumaksusumman.  

> [!TIP]  
>  Ennen kuin näitä tietoja aletaan syöttää ohjelmaan, olisi hyvä tehdä luonnos alennusrakenteesta, jota haluat käyttää. Tällä tavalla on helpompi nähdä, ketkä asiakkaat voi linkittää samaan laskualennusikkunaan. Mitä vähemmän ikkunoita täytyy määrittää, sitä nopeampaa perustietojen syöttäminen on.  

## <a name="best-price-calculation"></a>Parhaan hinnan laskenta
Kun olet kirjannut myynnin ja ostojen erikoishinnat ja rivialennukset, [!INCLUDE[d365fin](includes/d365fin_md.md)] varmistaa, että nimikekaupan tuotto on aina optimaalinen laskemalla automaattisesti parhaan hinnan myynti- ja ostoasiakirjoille sekä projekti- ja nimikepäiväkirjan riville.

Paras hinta on tietyn päivän alhaisin sallittu hinta, jolla on suurin sallittu rivialennus. [!INCLUDE[d365fin](includes/d365fin_md.md)] laskee tämän automaattisesti, kun se lisää nimikkeiden yksikköhinnan ja rivialennusprosentin uuteen asiakirjaan ja päiväkirjariville.

> [!NOTE]  
>   Seuraavaksi kerrotaan, miten myynnin paras hinta lasketaan. Samaa laskentaa käytetään ostoissa.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] tarkistaa laskutusasiakas- ja nimikeyhdistelmän ja laskee sitten käytettävän yksikköhinnan ja rivialennusprosentin seuraavien ehtojen mukaisesti:

    - Onko asiakkaalla hinta- tai alennussopimus tai kuuluuko asiakas ryhmään, jolla on tällainen sopimus on?
    - Kuuluuko rivillä oleva nimike tai nimikealennusryhmä johonkin näistä hinta- tai alennussopimuksista?
    - Onko tilauspäivämäärä (tai laskun ja hyvityslaskun osalta kirjauspäivämäärä) hinta- tai alennussopimuksen aloitus- ja lopetuspäivämäärän välissä?
    - Onko mittayksikön koodia määritelty? Jos on, [!INCLUDE[d365fin](includes/d365fin_md.md)] tarkastaa hinnat tai alennukset, joilla on sama mittayksikön koodi, ja hinnat tai alennukset, joilla ei ole mittayksikön koodia.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] tarkistaa, koskeeko jokin hinta- tai alennussopimus asiakirjan tai päiväkirjarivin tietoja, ja lisää sitten käytettävän yksikköhinnan ja rivialennusprosentin seuraavien ehtojen mukaisesti:

    - Täytyykö hinta- tai alennussopimuksen vähimmäismäärävaatimus?
    - Täytyykö hinta- tai alennussopimuksen valuuttavaatimus? Jos täyttyy, kyseisen valuutan alhaisin hinta ja suurin rivialennus lisätään, vaikka paikallinen valuutta antaisi paremman hinnan. Jos määritellyllä valuuttakoodilla ei ole hinta- tai alennusopimusta, [!INCLUDE[d365fin](includes/d365fin_md.md)] lisää alhaisimman hinnan ja suurimman rivialennuksen paikallisessa valuutassa.

Jos erikoishintaa ei voi laskea rivin nimikkeelle, joko viimeinen välitön kustannus tai nimikekortin yksikköhinta lisätään.

## <a name="see-also"></a>Katso myös
[Myynnin määrittäminen](sales-setup-sales.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

