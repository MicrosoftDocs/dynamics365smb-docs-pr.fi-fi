---
title: Asiakkaiden erikoismyyntihintojen ja -alennusten kirjaaminen | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten määritetään vaihtoehtoisten hintojen ja alennusten sopimukset, joita käytetään myyntiasiakirjoissa myytäessä eri asiakkaille.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 07/07/2020
ms.author: sgroespe
ms.openlocfilehash: 16d88ee490b5e9115ed22a12297fcf35b5739984
ms.sourcegitcommit: 8b2f02dd5189c46ecff33c07223ed62b36842d34
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2020
ms.locfileid: "3542615"
---
# <a name="record-special-sales-prices-and-discounts"></a>Erikoismyyntihintojen ja -alennusten kirjaaminen

Eri asiakkaiden hinta- ja alennussopimukset on määritettävä, jotta asiakkaille luotavissa myyntiasiakirjoissa käytetään sovittuja sääntöjä ja arvoja.

Kun olet kirjannut myynnin ja ostojen erikoishinnat ja rivialennukset, [!INCLUDE[d365fin](includes/d365fin_md.md)] varmistaa, että nimikekaupan tuotto on aina optimaalinen laskemalla automaattisesti parhaan hinnan myynti- ja ostoasiakirjoille sekä projekti- ja nimikepäiväkirjan riville. Lisätietoja on kohdassa [Parhaan hinnan laskenta](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

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

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
2. Avaa kyseessä olevan asiakkaan kortti ja valitse **Hinnat**-toiminto.

    **Myyntihinnat**-sivulla **Myynnin tyyppi** -kentän arvoksi esitäytetään **Asiakas**. **Myyntikoodi**-kentän arvoksi esitäytetään asiakasnumero.
3. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Täytä rivi jokaiselle yhdistelmälle, jossa asiakkaalle myönnetään erikoismyyntihinta.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Myyntirivialennuksien määrittäminen asiakkaalle

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
2. Avaa kyseessä olevan asiakkaan kortti ja valitse **Rivialennukset**-toiminto.

    **Myyntirivien alennukset** -sivulla **Myynnin tyyppi** -kentän arvoksi esitäytetään **Asiakas**. **Myyntikoodi**-kentän arvoksi esitäytetään asiakasnumero.
3. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Täytä rivi jokaiselle yhdistelmälle, jossa asiakkaalle myönnetään myyntirivialennus.

> [!Note]
> Kun avaat tietyn asiakkaan **Myyntihinnat**- ja **Myyntirivialennukset**-ikkunat, **Myyntityypin suodatus**-ja **Myyntikoodin suodatus** -kentät on määritetty asiakkaalle, eikä niitä voi muuttaa tai poistaa, mikä on nähtävissä harmaaksi muutetusta arvosta **Myyntikoodin suodatus** -kentässä.
>
> Kun haluat määrittää hinnat tai rivialennukset kaikille asiakkaille, asiakkaan hintaryhmälle tai kampanjalle, sinun täytyy avata ikkunat nimikekortista. Vaihtoehtoisesti voit käyttää myyntihinnoille **Myyntihinnan työkirja** -sivua. Lisätietoja on kohdassa [Nimike hintojen ryhmäpäivitys](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Laskualennuksen määrittäminen asiakkaalle

Kun olet määrittänyt asiakkaat, joille myönnetään laskun alennuksia, määritä laskun alennuskoodi asiakkaiden kortteihin ja määritä kunkin koodin ehdot.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
2. Avaa sen asiakkaan kortti, jolle myönnetään laskun alennuksia.
3. Valitse **Laskualennuksen koodi** -kentässä asianmukaisille laskualennuksen ehdoille koodi, jonka avulla asiakkaan laskualennukset lasketaan.

> [!NOTE]  
> Laskualennuksen koodit löytyvät olemassa olevien asiakkaiden korteista. Näin voit nopeasti liittää laskualennusten ehtoja asiakkaisiin poimimalla sellaisen asiakkaan nimen, jolla on samat ehdot.

Jatka uuden myyntilaskun alennusehtojen määrittämiseen.

1. Valitse **Asiakkaan kortti** -sivulla **Laskualennukset**-toiminto. **Asiakkaan laskualennukset** -sivu avautuu.
2. Anna **Valuutan koodi** -kenttään sen valuutan koodi, johon rivin laskualennuksen ehdot kohdistetaan. Jätä kenttä tyhjäksi, jos laskualennuksen ehtojen määritys tapahtuu valuutassa EUR.
3. Syötä **Vähimmäissumma**-kenttään laskun vähimmäissumma, joka oikeuttaa alennukseen.
4. Syötä **Alennus-%**-kohtaan laskun alennus prosentteina laskun summasta.
5. Toista vaiheet 5–7 jokaiselle valuutalle, jossa asiakas saa eri laskualennuksen.

Laskualennus on nyt määritetty ja liitetty kyseiselle asiakkaalle. Kun valitset asiakaskoodin muiden asiakkaiden korttien **Laskun alennuskoodi** -kentässä, sama laskualennus liitetään myös näille asiakkaille.

## <a name="to-work-with-sales-invoice-discounts-and-service-charges"></a>Myyntilaskualennukset ja palvelumaksujen käyttäminen

Kun käytät laskualennuksia, laskusumman suuruus määrää annettavan alennuksen suuruuden.  

Voit lisätä **Asiakkaan laskualennukset** -sivulla tietyn summaisille laskuille myös palvelumaksuja.  

Ennen kuin myynneissä voi käyttää laskualennuksia, sovellukseen on annettava tiettyjä tietoja. Täytyy päättää:  

- ketkä asiakkaat saavat tämän tyyppisen alennuksen.  
- mitä alennusprosentteja käytetään.  

Jos haluat, että laskualennukset lasketaan automaattisesti, voit määrittää sen **Myyntien ja myyntisaamisten asetukset** -sivulla.  

Voit määrittää jokaiselle asiakkaalle erikseen, annetaanko tälle laskualennuksia, jos tarve on tyydytetty (eli jos laskusumma on tarpeeksi suuri). Laskualennusehdot voi määrittää paikallisena valuuttana kotimaisille asiakkaille ja ulkomaan valuuttana ulkomaisille asiakkaille.  

Voit linkittää alennusprosentit tiettyihin laskusummiin **Asiakkaan laskualennukset** -sivuilla. Voit syöttää mitä tahansa prosenttilukuja kullakin sivulla. Jokainen asiakas voi olla erillisellä sivulla, tai samalle sivulle voi linkittää useita asiakkaita.  

Spesifiseen laskusummaan voi linkittää alennusprosentin lisäksi (tai sen sijaan) palvelumaksusumman.  

> [!TIP]  
> Ennen kuin näiden tietojen syöttäminen aloitetaan, käytettävästä alennusrakenteesta kannattaa tehdä luonnos. Tällä tavalla on helpompi nähdä, ketkä asiakkaat voi linkittää samaan laskualennussivulle. Mitä vähemmän sivuja on määritettävä, sitä nopeampaa perustietojen antaminen on.

Lisätietoja myynnin alennuksista on kohdassa [Alennusten määrittäminen asiakkaillesi](/learn/modules/customer-discounts-dynamics-365-business-central/index)Microsoft Learnissa.  

## <a name="best-price-calculation"></a>Parhaan hinnan laskenta

Kun olet kirjannut myynnin ja ostojen erikoishinnat ja rivialennukset, [!INCLUDE[d365fin](includes/d365fin_md.md)] varmistaa, että nimikekaupan tuotto on aina optimaalinen laskemalla automaattisesti parhaan hinnan myynti- ja ostoasiakirjoille sekä projekti- ja nimikepäiväkirjan riville.

Paras hinta on tietyn päivän alhaisin sallittu hinta, jolla on suurin sallittu rivialennus. [!INCLUDE[d365fin](includes/d365fin_md.md)] laskee tämän automaattisesti, kun se lisää nimikkeiden yksikköhinnan ja rivialennusprosentin uuteen asiakirjaan ja päiväkirjariville.

> [!NOTE]  
> Seuraavaksi kerrotaan, miten myynnin paras hinta lasketaan. Samaa laskentaa käytetään ostoissa.

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

Jos haluat kopioida myyntihintoja, kuten jonkin yksittäisen asiakkaan hintoja koko asiakashintaryhmälle, sinun tulee ajaa **Ehdota myyntihinta työkirja** eräajo, joka voidaan käynnistää **Myyntihintatyökirja**-sivulla.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntihintatyökirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Ehdota myyntihintaa työkirjalle**. -toiminto.  
3. Täytä **Myyntihinnat**-pikavälilehden kenttiin kopioitavien, alkuperäisten myyntihintojen **Myynnin tyyppi** ja **Myyntikoodi**.  
4. Täytä pyyntösivun yläosassa **Myynnin tyyppi**- ja **Myyntikoodi**-kenttiin tyyppi ja nimi, joihin haluat kopioida myyntihinnat.  
5. Jos haluat eräajon luovan uusia hintoja, valitse **Luo uudet hinnat** -valintaruutu.  
6. Täytä **Myyntihintatyökirja**-sivun rivit ehdotetuilla uusilla hinnoilla valitsemalla **OK**. Tämä ilmaisee, että hinnat ovat voimassa valitulle myyntityypille.  

> [!NOTE]  
> Tämä eräajo luo ainoastaan ehdotuksia eikä se ota ehdotettuja muutoksia käyttöön. Jos olet tyytyväinen ehdotuksiin ja haluat ottaa ne käyttöön eli lisätä ne **Myyntihinnat**-sivulle, valitse **Ota käyttöön hinnan muutos** -toiminto **Myyntihinnan työkirja** -sivulla.

## <a name="to-bulk-update-item-prices"></a>Nimikehintojen joukkopäivitys

Jos haluat tehdä nimikehintojen joukkopäivityksen, kuten nostaa kaikkien nimikkeiden hintoja tietyllä prosenttiosuudella, sinun on suoritettava **Ehdota nimikehintaa työkirjaan**  eräajo. Eräajon linkki sijaitsee **Myyntihinnan työkirja** -sivulla.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntihintatyökirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Ehdota nimikehintaa työkirjaan** -toiminto.  
3. Täytä **Nimike**-pikavälilehdessä **Nro**- tai **Varaston kirjausryhmä** -kenttään tai muihin kenttiin päivitettävät alkuperäiset hinnat.  
4. Täytä pyyntösivun yläosassa **Myynnin tyyppi** ja **Myyntikoodi** tyypillä ja nimellä, joihin haluat kopioida myyntihinnat.
5. Jos haluat, että eräajo muuttaa ehdotettuja hintoja automaattisesti, anna muutos **Muutoskerroin**-kentässä. Esimerkki: jos annat 1,15 **Muutoskerroin**-kentässä, nimikehinta nousee 15 %.  
6. Jos haluat eräajon luovan uusia hintoja, lisää rasti **Luo uudet hinnat** -kenttään.  
7. Täytä **Myyntihinnan työkirja** -sivun rivit ehdotetuilla uusilla hinnoilla valitsemalla **OK**. Tämä ilmaisee, että hinnat ovat voimassa valitulle **nimikkeelle**.  

> [!NOTE]
> Tämä eräajo luo ainoastaan ehdotuksia eikä se ota ehdotettuja muutoksia käyttöön. Jos olet tyytyväinen ehdotuksiin ja haluat ottaa ne käyttöön eli antaa ne **Myyntihinnat**-taulukkoon, voit käyttää **Ota käyttöön hinnan muutos** -eräajoa, joka löytyy valitsemalla **Myyntihinnan työkirja** -sivun **Toiminnot**-välilehden **Toiminnot**-ryhmästä.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Myynnin määrittäminen](sales-setup-sales.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
