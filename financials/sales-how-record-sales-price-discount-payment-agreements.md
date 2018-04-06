---
title: Asiakkaiden erikoismyyntihintojen ja -alennusten kirjaaminen | Microsoft Docs
description: "Tässä ohjeaiheessa kerrotaan, miten määritetään vaihtoehtoisten hintojen ja alennusten sopimukset, joita käytetään myyntiasiakirjoissa myytäessä eri asiakkaille."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e6e662ee13db1f9002e1c3e74a0d15e2aa2e2a98
ms.openlocfilehash: a130d946a7efa1d49584d4756fe6cd622c409827
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="record-special-sales-prices-and-discounts"></a>Erikoismyyntihintojen ja -alennusten kirjaaminen
Eri asiakkaiden hinta- ja alennussopimukset on määritettävä, jotta asiakkaille luotavissa myyntiasiakirjoissa käytetään sovittuja sääntöjä ja arvoja.

Kun olet kirjannut myynnin ja ostojen erikoishinnat ja rivialennukset, [!INCLUDE[d365fin](includes/d365fin_md.md)] varmistaa, että nimikekaupan tuotto on aina optimaalinen laskemalla automaattisesti parhaan hinnan myynti- ja ostoasiakirjoille sekä projekti- ja nimikepäiväkirjan riville. Lisätietoja on osiossa Parhaan hinnan laskenta.

Myyntiriveille lisätään erikoismyyntihinta, jos tietty asiakkaan, nimikkeen, vähimmäismäärän, mittayksikön sekä aloitus- ja lopetuspäivämäärän yhdistelmä on olemassa.

Voit määrittää seuraavat kaksi myyntialennustyyppiä:

| Alennustyyppi | Kuvaus |
| --- | --- |
| **Myyntirivin alennus** |Myyntiriveille lisättävä summa-alennus, jos tietty asiakkaan, nimikkeen, vähimmäismäärän, mittayksikön sekä aloitus- ja lopetuspäivämäärän yhdistelmä on olemassa. Tätä käytetään samoin kuin myyntihinnoissa. |
| **Laskualennus** |Prosenttialennus, joka vähennetään kokonaissummasta, kun myyntiasiakirjan kaikkien rivien summa ylittää määritetyn vähimmäisarvon. |

Koska myyntihinnat ja myyntirivialennukset perustuvat nimikkeen ja asiakkaan yhdistelmään, voit tehdä tämän määrityksen myös sen nimikkeen kortissa, jota säännöt ja arvot koskevat.

> [!NOTE]  
> Jos haluat, että nimikettä ei koskaan myydä alennetulla hinnalla, jätä nimikekortin alennuskentät tyhjiksi äläkä sisällytä nimikettä yhteenkään rivialennuksen määritykseen.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Myyntihinnan määrittäminen asiakkaalle
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakkaat** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa kyseessä olevan asiakkaan kortti ja valitse **Hinnat**-toiminto.

    **Myynnin tyyppi** -kentän arvoksi esitäytetään **Asiakas**. **Myyntikoodi** -kentän arvoksi esitäytetään asiakasnumero.
3. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Täytä rivi jokaiselle yhdistelmälle, jossa asiakkaalle myönnetään erikoismyyntihinta.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Myyntirivialennuksien määrittäminen asiakkaalle
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakkaat** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa kyseessä olevan asiakkaan kortti ja valitse **Rivialennukset**-toiminto.

    **Myynnin tyyppi** -kentän arvoksi esitäytetään **Asiakas**. **Myyntikoodi** -kentän arvoksi esitäytetään asiakasnumero.
3. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Täytä rivi jokaiselle yhdistelmälle, jossa asiakkaalle myönnetään myyntirivialennus.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Laskualennuksen määrittäminen asiakkaalle
Kun olet määrittänyt asiakkaat, joille myönnetään laskun alennuksia, määritä laskun alennuskoodi asiakkaiden kortteihin ja määritä kunkin koodin ehdot.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakkaat** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa sen asiakkaan kortti, jolle myönnetään laskun alennuksia.
3. Valitse **Laskualennuksen koodi** -kentässä asianmukaisille laskualennuksen ehdoille koodi, jonka avulla asiakkaan laskualennukset lasketaan.

> [!NOTE]  
>   Laskualennuksen koodit löytyvät olemassa olevien asiakkaiden korteista. Näin voit nopeasti liittää laskualennusten ehtoja asiakkaisiin poimimalla sellaisen asiakkaan nimen, jolla on samat ehdot.

    Proceed to set up new the sales invoice discount terms.
4. Valitse **Asiakkaan kortti** -ikkunassa **Laskualennukset**-toiminto. **Asiakkaan laskualennukset** -ikkuna aukeaa.
5. Syötä **Valuutan koodi** -kenttään sen valuutan koodi, johon rivin laskualennuksen ehdot kohdistetaan. Jätä kenttä tyhjäksi, jos laskualennuksen ehdot määritetään Yhdysvaltojen dollareina.
6. Syötä **Vähimmäissumma**-kenttään laskun vähimmäissumma, joka oikeuttaa alennukseen.
7. Syötä **Alennus-%**-kohtaan laskun alennus prosentteina laskun summasta.
8. Toista vaiheet 5–7 jokaiselle valuutalle, jossa asiakas saa eri laskualennuksen.

Laskualennus on nyt määritetty ja liitetty kyseiselle asiakkaalle. Kun valitset asiakaskoodin muiden asiakkaiden korttien **Laskun alennuskoodi** -kentässä, sama laskualennus liitetään myös näille asiakkaille.

## <a name="to-work-with-sales-invoice-discounts-and-service-charges"></a>Myyntilaskualennukset ja palvelumaksujen käyttäminen
Kun käytät laskualennuksia, laskusumman suuruus määrää annettavan alennuksen suuruuden.  

Voit myös lisätä **Asiakkaan laskualennukset** -ikkunassa tietyn summan ylittäville laskuille palvelumaksuja.  

Ennen kuin myynneissä voi käyttää laskualennuksia, ohjelmaan täytyy syöttää tiettyjä tietoja. Täytyy päättää:  

- ketkä asiakkaat saavat tämän tyyppisen alennuksen.  
- mitä alennusprosentteja käytetään.  

Jos haluat, että laskualennukset lasketaan automaattisesti, voit määrittää sen **Myyntien ja myyntisaamisten asetukset** -ikkunassa.  

Voit määrittää jokaiselle asiakkaalle erikseen, annetaanko tälle laskualennuksia, jos tarve on tyydytetty (eli jos laskusumma on tarpeeksi suuri). Laskualennusehdot voi määrittää paikallisena valuuttana kotimaisille asiakkaille ja ulkomaan valuuttana ulkomaisille asiakkaille.  

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
    - Täytyykö hinta- tai alennussopimuksen valuuttavaatimus? Jos täyttyy, kyseisen valuutan alhaisin hinta ja suurin rivialennus lisätään, vaikka paikallinen valuutta antaisi paremman hinnan. Jos määritellyllä valuuttakoodilla ei ole hinta- tai alennusopimusta, [!INCLUDE[d365fin](includes/d365fin_md.md)] lisää alhaisimman hinnan ja suurimman rivialennuksen paikallisena valuuttana.

Jos erikoishintaa ei voi laskea rivin nimikkeelle, joko viimeinen välitön kustannus tai nimikekortin yksikköhinta lisätään.

## <a name="to-copy-sales-prices"></a>Myyntihintojen kopioiminen  
Jos haluat kopioida myyntihintoja, kuten jonkin yksittäisen asiakkaan hintoja koko asiakashintaryhmälle, sinun tulee ajaa **Ehdota myyntihinta työkirja**  eräajo. Eräajon löytää **Myyntihintatyökirja**-ikkunasta.    

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntihinnan työkirja** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Ehdota myyntihintaa työkirjalle**. -toiminto.  
3.  Täytä **Myyntihinnat**-pikavälilehden kenttiin kopioitavien, alkuperäisten myyntihintojen **Myynnin tyyppi** ja **Myyntikoodi**.  
4.  Täytä pyyntöikkunan yläosassa **Myynnin tyyppi** ja **Myyntikoodi** tyypillä ja nimellä, joihin haluat kopioida myyntihinnat.  
5.  Jos haluat eräajon luovan uusia hintoja, lisää rasti **Luo uudet hinnat** -kenttään.  
6.  Napsauta **OK** täyttääksesi rivit **Myyntihintatyökirja**-ikkunassa ehdotetuilla uusilla hinnoilla ja ilmaistaksesi, että hinnat ovat voimassa valitulle **Myynnin tyypille**.  

> [!NOTE]  
>  Tämä eräajo luo ainoastaan ehdotuksia eikä se ota ehdotettuja muutoksia käyttöön. Jos olet tyytyväinen ehdotuksiin ja haluat ottaa ne käyttöön eli syöttää ne **Myyntihinnat**-taulukkoon, voit käyttää **Ota käyttöön hinnan muutos** -eräajoa, joka löytyy valitsemalla **Myyntihinnan työkirja** -ikkunan **Toiminnot**-välilehden Toiminnot **ryhmän**-ryhmästä.

## <a name="see-also"></a>Katso myös
[Myynnin määrittäminen](sales-setup-sales.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

