---
title: Asiakkaiden erikoismyyntihintojen ja -alennusten kirjaaminen | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten määritetään vaihtoehtoisten hintojen ja alennusten sopimukset, joita käytetään myyntiasiakirjoissa myytäessä eri asiakkaille.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 6d358afec4689a3543245295427d5fae992dd680
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436774"
---
# <a name="record-special-sales-prices-and-discounts"></a>Erikoismyyntihintojen ja -alennusten kirjaaminen
> [!NOTE]
> Vuoden 2020 julkaisuaallossa 2 julkaisimme virtaviivaiset prosessit hintojen ja alennusten määritykseen ja hallintaan. Jos olet uusi asiakas, joka käyttää kyseistä versiota, käytät uutta käyttökokemusta. Jos olet jo asiakas, uuden käyttöokemuksen käyttö riippuu siitä, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuden päivityksen **ominaisuuksien hallinnassa**. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management).

Asiakkaiden hinta- ja alennussopimukset on määritettävä, jotta myyntiasiakirjoissa käytetään sovittuja sääntöjä ja arvoja.

Kun olet kirjannut myynnin ja ostojen erikoishinnat ja rivialennukset, [!INCLUDE[prod_short](includes/prod_short.md)] varmistaa, että nimikekaupan tuotto on aina optimaalinen laskemalla automaattisesti parhaan hinnan myynti- ja ostoasiakirjoille sekä projekti- ja nimikepäiväkirjan riville. Lisätietoja on kohdassa [Parhaan hinnan laskenta](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Myyntiriveille lisätään erikoismyyntihinta, jos tietty asiakkaan, nimikkeen, vähimmäismäärän, mittayksikön sekä aloitus- ja lopetuspäivämäärän yhdistelmä on olemassa. Lisätietoja on [Myyntihinnan määrittäminen asiakkaalle](#to-set-up-a-sales-price-for-a-customer) ja [Parhaan hinnan laskenta](#best-price-calculation) -osioissa.  

Voit määrittää seuraavat kaksi myyntialennustyyppiä:

| Alennustyyppi | Kuvaus |
| --- | --- |
| **Myyntirivin alennus** |Myyntiriveille lisättävä summa-alennus, jos tietty asiakkaan, nimikkeen, vähimmäismäärän, mittayksikön sekä aloitus- ja lopetuspäivämäärän yhdistelmä on olemassa. Tätä käytetään samoin kuin myyntihinnoissa. |
| **Laskualennus** |Prosenttialennus, joka vähennetään kokonaissummasta, kun myyntiasiakirjan kaikkien rivien summa ylittää määritetyn vähimmäisarvon. |

Koska myyntihinnat ja myyntirivialennukset perustuvat nimikkeen ja asiakkaan yhdistelmään, voit tehdä tämän määrityksen myös sen nimikkeen sivulla, jota säännöt ja arvot koskevat.

> [!TIP]  
> Jos nimikettä ei koskaan myydä alennetulla hinnalla, jätä nimikesivun alennuskentät tyhjiksi äläkä sisällytä nimikettä yhteenkään rivialennuksen määritykseen.

**Koskee tyyppiä**- ja **Koskee nroa** -kenttien avulla voit valita, mihin tämä hinnasto kohdistetaan, esimerkiksi asiakkaaseen tai asiakashintaryhmään. **Näytä sarakkeet kohteelle** -asetuksen avulla voit näyttää tai piilottaa hintojen ja alennusten määrittämisessä tarvittavat kentät.

Voit määrittää hinnaston rivejä manuaalisesti tai voit käyttää esimerkiksi **Ehdota rivejä** -toimintoa luodessasi uusia hintoja valituille nimikkeille, nimikealennusryhmille, resursseille ja muille tuotetyypeille. Jos valitset Ehdota rivejä, voit Hintarivit – Luo uusi -sivulla asettaa suodattimia valitsemaan tuotteita, joille haluat luoda uusia hinnastorivejä. Voit myös määrittää, otetaanko vähimmäismäärä huomioon laskettaessa hintoja, uusien hinnastorivien muutoksen kerrointa ja hintojen osalta pyöristystapaa. **Kopioi rivit** -toiminnon avulla voit kopioida olemassa olevat hinnaston rivit hinnastojen välillä.

Uusien hinnastojen tila on oletusarvoisesti Luonnos. Kun olet lopettanut rivien lisäämisen ja haluat hinnanlaskentamoduulin sisällyttävän sen, voit muuttaa tilaksi Aktiivinen.

Voit tarkastella tiettyjen asiakkaiden tai toimittajien hinnastoja ja hintoja valitsemalla **Asiakas**-sivulla **Myyntihinnastot** tai valitsemalla **Toimittaja**-sivulla **Ostohinnastot**. Voit tarkastella hinnaston rivejä eri hinnastoissa valitsemalla **Nimike**- ja **Resurssi**-sivuilta **Myyntihinnat** tai **Ostohinnat**.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Myyntihinnan määrittäminen asiakkaalle

Nämä vaiheet vaihtelevat sen mukaan, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuden päivityksen.  

#### <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience/)

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Valitse asiakas ja valitse sitten **Hinnat**-toiminto.
3. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Täytä rivi jokaiselle yhdistelmälle, jossa asiakkaalle myönnetään erikoismyyntihinta.

#### <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience/)  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Valitse asiakas ja valitse sitten **Myyntihinnastot**-toiminto. 
3. Luo uusi myyntihinnasto valitsemalla **Uusi**.
4. Täytä **Yleiset**- ja **Vero**-pikavälilehdissä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Voit lisätä luetteloon kohteita tekemällä jommankumman seuraavista:
   * Voit lisätä useita nimikkeitä valitsemalla **Ehdota rivejä** ja määrittämällä lisättävät nimiketyypit syöttämällä suodatusehdot. Vaihtoehtoisesti voit myös syöttää joitain lisäasetuksia nimikkeille, jotka liittyvät hinnastoon. Voit muuttaa niitä tarvittaessa myöhemmin.
   * Voit kopioida nimikkeitä toisesta hinnastoista valitsemalla **Kopioi rivit** ja valitsemalla kopioitavan hinnaston.
   * Voit lisätä nimikkeitä manuaalisesti valitsemalla ruudukossa **Tuotetyyppi**-kentässä tuotteen tyypin, jolle hinnasto on tarkoitettu. Täytä tarvittaessa jäljellä olevat kentät valintojen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Voit aloittaa hinnaston käyttämisen valitsemalla **Tila**-kentässä **Aktiivinen**.  

---

## <a name="sales-invoice-discounts-and-service-charges"></a>Myyntilaskualennukset ja palvelumaksut
Kun käytät laskualennuksia, laskun loppusumma määrää annettavan alennuksen suuruuden. Voit lisätä **Asiakkaan laskualennukset** -sivulla tietyn summaisille laskuille myös palvelumaksuja.  

Ennen kuin myynneissä voi käyttää laskualennuksia, on määritettävä tiettyjä tietoja. Sinun täytyy päättää seuraavista asioista:  

- Ketkä asiakkaat saavat tämän tyyppisen alennuksen  
- Mitä alennusprosentteja käytetään  

Jos haluat, että laskualennukset lasketaan automaattisesti, voit määrittää sen **Myyntien ja myyntisaamisten asetukset** -sivulla.  

Voit määrittää jokaiselle asiakkaalle erikseen, annetaanko tälle laskualennuksia, jos tarve on tyydytetty (eli jos laskusumma on tarpeeksi suuri). Laskualennusehdot voi määrittää paikallisena valuuttana kotimaisille asiakkaille ja ulkomaan valuuttana ulkomaisille asiakkaille.  

Voit linkittää alennusprosentit tiettyihin laskusummiin kunkin asiakkaan **Asiakkaan laskualennukset** -sivulla. Voit syöttää mitä tahansa prosenttilukuja. Jokainen asiakas voi olla erillisellä sivulla, tai samalle sivulle voi linkittää useita asiakkaita.  

Spesifiseen laskusummaan voi linkittää alennusprosentin lisäksi (tai sen sijaan) palvelumaksusumman.  

> [!TIP]  
> Ennen kuin näiden tietojen syöttäminen aloitetaan, käytettävästä alennusrakenteesta kannattaa tehdä luonnos. Tällä tavalla on helpompi nähdä, ketkä asiakkaat voi linkittää samaan laskualennussivulle. Mitä vähemmän sivuja on määritettävä, sitä nopeampaa perustietojen antaminen on.

Koulutusta myynnin alennuksista on Microsoft Learnin kohteessa [Alennusten määrittäminen asiakkaillesi](/learn/modules/customer-discounts-dynamics-365-business-central/index).  

### <a name="calculating-invoice-discounts-on-sales"></a>Myynnin laskualennusten laskenta

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Myyntirivialennuksien määrittäminen asiakkaalle
Nämä vaiheet vaihtelevat sen mukaan, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuden päivityksen. 

#### <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience/)  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Avaa kyseessä olevan asiakkaan kortti ja valitse **Rivialennukset**-toiminto.
3. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Täytä rivi jokaiselle yhdistelmälle, jossa asiakkaalle myönnetään myyntirivialennus.

> [!Note]
> Kun avaat tietyn asiakkaan **Myyntihinnat**- ja **Myyntirivialennukset**-sivut, **Myyntityypin suodatus**-ja **Myyntikoodin suodatus** -kentät on määritetty asiakkaalle, eikä niitä voi muuttaa tai poistaa.
>
> Kun haluat määrittää hinnat tai rivialennukset kaikille asiakkaille, asiakkaan hintaryhmälle tai kampanjalle, sinun täytyy avata sivut nimikekortista. Vaihtoehtoisesti voit käyttää myyntihinnoille **Myyntihinnan työkirja** -sivua. Lisätietoja on kohdassa [Nimikehintojen joukkopäivitys](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience/)  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Valitse asiakas ja valitse sitten **Myyntihinnastot**-toiminto.
3. Avaa hinnasto, jolle rivialennus määritetään.
4. Ota käyttöön **Salli rivialennus** -valinta.
5. Luo uusi rivi tai valitse aiemmin luotu rivi ja täytä kentät tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Valitse **Määrittää**-kentässä joko **Hinta ja alennus** tai vain **Alennus**. 
7. Määritä alennusprosentti **Rivialennus-%**-kentässä.

    > [!TIP]
    > Jos muokkaat aiemmin luotua riviä, voit suodattaa rivit valitsemalla haluamasi asetuksen **Näytä sarakkeet kohteelle** -kentästä.

    > [!NOTE]  
    > Laskualennuksen koodit löytyvät olemassa olevien asiakkaiden korteista. Näin voit nopeasti liittää laskualennusten ehtoja asiakkaisiin poimimalla sellaisen asiakkaan nimen, jolla on samat ehdot. Voit määrittää asiakaskohtaisia laskualennusehtoja määrittämällä **Laskun alennuskoodi** -kentän asiakkaan asiakaskoodille ja jatkamalla sitten seuraavaan vaiheeseen.

8. Valitse **Asiakkaan kortti** -sivulla **Laskualennukset**-toiminto. **Asiakkaan laskualennukset** -sivu avautuu.
9. Anna **Valuutan koodi** -kenttään sen valuutan koodi, johon rivin laskualennuksen ehdot kohdistetaan. Jätä kenttä tyhjäksi, jos laskualennuksen ehtojen määritys tapahtuu paikallisessa valuutassasi.
10. Valinnainen: Syötä **Vähimmäissumma**-kenttään laskun vähimmäissumma, joka oikeuttaa alennukseen.
11. Syötä **Alennus-%**-kohtaan laskun alennus prosentteina laskun summasta.
12. Toista vaiheet 5–7 jokaiselle valuutalle, jossa asiakas saa eri laskualennuksen.

Laskualennus on nyt määritetty ja liitetty asiakkaalle. Kun valitset asiakaskoodin muiden asiakkaiden korttien **Laskun alennuskoodi** -kentässä, sama laskualennus liitetään myös näille asiakkaille.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Laskualennuksen määrittäminen asiakkaalle
Kun olet määrittänyt asiakkaat, joille myönnetään laskun alennuksia, määritä laskun alennuskoodi asiakkaiden kortteihin ja määritä kunkin koodin ehdot.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Avaa sen asiakkaan sivu, jolle myönnetään laskun alennuksia.
3. Valitse **Laskualennuksen koodi** -kentässä asianmukaisille laskualennuksen ehdoille koodi, jonka avulla asiakkaan laskualennukset lasketaan. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Laskualennuksen koodit löytyvät olemassa olevien asiakkaiden korteista. Näin voit nopeasti liittää laskualennusten ehtoja asiakkaisiin poimimalla sellaisen asiakkaan nimen, jolla on samat ehdot.

Jatka uuden myyntilaskun alennusehtojen määrittämiseen.

1. Valitse **Asiakkaat** -sivulla **Laskualennukset**-toiminto. **Asiakkaan laskualennukset** -sivu avautuu.
2. Anna **Valuutan koodi** -kenttään sen valuutan koodi, johon rivin laskualennuksen ehdot kohdistetaan. Jätä kenttä tyhjäksi, jos laskualennuksen ehtojen määritys tapahtuu paikallisessa valuutassasi.
3. Syötä **Vähimmäissumma**-kenttään laskun vähimmäissumma, joka oikeuttaa alennukseen.
4. Syötä **Alennus-%**-kohtaan laskun alennus prosentteina laskun summasta.
5. Toista vaiheet 5–7 jokaiselle valuutalle, jossa asiakas saa eri laskualennuksen.

## <a name="to-copy-sales-prices"></a>Myyntihintojen kopioiminen
Nämä vaiheet vaihtelevat sen mukaan, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuden päivityksen. 

#### <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience/)  

Jos haluat kopioida myyntihintoja, kuten jonkin yksittäisen asiakkaan hintoja koko asiakashintaryhmälle, sinun tulee ajaa **Ehdota myyntihinta työkirja** -erätyö **Myyntihintatyökirja**-sivulla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntihintatyökirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Ehdota myyntihintaa työkirjalle**. -toiminto.  
3. Täytä **Myyntihinnat**-pikavälilehden kenttiin kopioitavien, alkuperäisten myyntihintojen **Myynnin tyyppi** ja **Myyntikoodi**.  
4. Täytä pyyntösivun yläosassa **Myynnin tyyppi**- ja **Myyntikoodi**-kenttiin tyyppi ja nimi, joihin haluat kopioida myyntihinnat.  
5. Jos haluat eräajon luovan uusia hintoja, valitse **Luo uudet hinnat** -valintaruutu.  
6. Täytä **Myyntihintatyökirja**-sivun rivit ehdotetuilla uusilla hinnoilla valitsemalla **OK**. Tämä ilmaisee, että hinnat ovat voimassa valitulle myyntityypille.  

   > [!NOTE]  
   > Tämä eräajo luo ainoastaan ehdotuksia eikä se ota ehdotettuja muutoksia käyttöön. Jos olet tyytyväinen ehdotuksiin ja haluat ottaa ne käyttöön eli lisätä ne **Myyntihinnat**-sivulle, valitse **Ota käyttöön hinnan muutos** -toiminto **Myyntihinnan työkirja** -sivulla.

#### <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience/)  

Hinnaston rivin tilan on oltava **Luonnos**. 

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntihinnastot** ja valitse sitten liittyvä linkki. 
2. Valitse kopioitava hinnasto ja valitse sitten **Kopioi rivit**.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Kahdella eri rivillä ei voi olla samoja asetuksia mutta eri hintoja. Jos näin tapahtuu, näyttöön tulee sanoma, kun aktivoit hinnaston. Voit valita käytettävän hinnan avaamalla hinnaston ja poistamalla virheellisen hinnan.  
  
---

## <a name="to-bulk-update-item-prices"></a>Nimikehintojen joukkopäivitys
Nämä vaiheet vaihtelevat sen mukaan, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuden päivityksen. 

#### <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience/)

Jos haluat tehdä nimikehintojen joukkopäivityksen, kuten nostaa kaikkien nimikkeiden hintoja tietyllä prosenttiosuudella, sinun on suoritettava **Ehdota nimikehintaa työkirjaan**  eräajo. Eräajon linkki sijaitsee **Myyntihinnan työkirja** -sivulla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntihintatyökirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Ehdota nimikehintaa työkirjaan** -toiminto.  
3. Täytä **Nimike**-pikavälilehdessä **Nro**- tai **Varaston kirjausryhmä** -kenttään tai muihin kenttiin päivitettävät alkuperäiset hinnat.  
4. Täytä pyyntösivun yläosassa **Myynnin tyyppi** ja **Myyntikoodi** tyypillä ja nimellä, joihin haluat kopioida myyntihinnat.
5. Jos haluat, että eräajo muuttaa ehdotettuja hintoja automaattisesti, anna muutos **Muutoskerroin**-kentässä. Esimerkki: jos annat 1,15 **Muutoskerroin**-kentässä, nimikehinta nousee 15 %.  
6. Jos haluat eräajon luovan uusia hintoja, lisää rasti **Luo uudet hinnat** -kenttään.  
7. Täytä **Myyntihinnan työkirja** -sivun rivit ehdotetuilla uusilla hinnoilla valitsemalla **OK**. Tämä ilmaisee, että hinnat ovat voimassa valitulle **nimikkeelle**.  

> [!NOTE]
> Tämä eräajo luo ainoastaan ehdotuksia eikä se ota ehdotettuja muutoksia käyttöön. Jos olet tyytyväinen ehdotuksiin ja haluat ottaa ne käyttöön eli antaa ne **Myyntihinnat**-taulukkoon, voit käyttää **Ota käyttöön hinnan muutos** -eräajoa, joka löytyy valitsemalla **Myyntihinnan työkirja** -sivun **Toiminnot**-välilehden **Toiminnot**-ryhmästä.

#### <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience/)

Jos haluat päivittää monien nimikkeiden hinnat, sinun täytyy luoda uusi hinnasto ja kopioida rivit olemassa olevasta hinnastosta. Kun kopioit rivit, voit määrittää suodattimien avulla, mitä haluat kopioida, ja voit määrittää kokonaisluvun tai desimaaliluvun **Muutoskerroin**-kenttään hintojen korottamiseksi tai vähentämiseksi. Hinnaston tilan on oltava **Luonnos**. Voit poistaa vanhan hinnaston käytöstä tarpeen mukaan.

> [!NOTE]
> Kahdella eri rivillä ei voi olla samoja asetuksia mutta eri hintoja. Jos näin tapahtuu, näyttöön tulee sanoma, kun aktivoit hinnaston. Voit valita käytettävän hinnan avaamalla hinnaston ja poistamalla virheellisen hinnan.  

---

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

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Myynnin määrittäminen](sales-setup-sales.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]