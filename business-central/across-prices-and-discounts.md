---
title: Hintojen ja alennusten määrittäminen
description: Tietoja siitä, miten vakio- ja erikoishintoja ja alennussopimuksia määritetään myyntejä ja ostoja varten.
author: bholtorf
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: price, pricing, discount, discounting, rebate, sale, purchase, invoice
ms.search.form: 459, 460, 7001, 7011, 7015, 7016, 7017, 7018
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 24768e03181599b2329d4ed532453a60516bd9f3
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134120"
---
# <a name="set-up-prices-and-discounts"></a>Hintojen ja alennusten määrittäminen
> [!NOTE]
> Vuoden 2020 julkaisuaallossa 2 julkaisimme virtaviivaiset prosessit hintojen ja alennusten määritykseen ja hallintaan. Jos olet uusi asiakas, joka käyttää kyseistä versiota, käytät uutta käyttökokemusta. Jos olet jo asiakas, uuden käyttöokemuksen käyttö riippuu siitä, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuden päivityksen **Ominaisuuksien hallinta** -sivulla. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management).

Nimikkeiden ja palveluiden osto- ja myyntistrategiat ovat perustyökaluja menestyville yrityksille. Kun yrityksesi ostaa ja myy nimikkeitä ja palveluja, voit määrittää, mitä maksat tai laskutat niistä, ja nämä summat lisätään automaattisesti myynti- ja ostoasiakirjoihin. 

## <a name="setting-up-prices-and-discounts"></a>Hintojen ja alennusten määrittäminen
Ennen kuin luot hinnastoja, sinun täytyy määrittää hinnoittelu- ja alennusstrategiat **Myyntien ja myyntisaamisten asetukset**- ja **Ostojen ja ostovelkojen asetukset** -sivuilla.

Voit määrittää seuraavat kaksi alennustyyppiä:

| Alennustyyppi | Kuvaus |
| --- | --- |
| **Rivialennus** |Alennussumma, joka annetaan myynti- ja ostoasiakirjojen riveille. Yleensä rivialennukset perustuvat asiakkaan, nimikkeen, vähimmäismäärän, mittayksikön tai ajanjakson yhdistelmään, jonka määrität myynneille ja ostoille **Myyntien ja myyntisaamisten asetukset**- ja **Ostojen ja ostovelkojen asetukset** -sivuilla.|
| **Laskualennus** |Prosenttialennus, joka vähennetään kokonaissummasta, kun myynti- ja ostoasiakirjan kaikkien rivien summa ylittää määritetyn vähimmäisarvon. |

Koska myyntihinnat ja myyntirivialennukset perustuvat nimikkeen ja asiakkaan yhdistelmään, voit tehdä tämän määrityksen myös sen nimikkeen sivulla, jota säännöt ja arvot koskevat.

> [!TIP]  
> Jos nimikettä ei koskaan myydä alennetulla hinnalla, jätä nimikesivun alennuskentät tyhjiksi äläkä sisällytä nimikettä yhteenkään rivialennuksen määritykseen.

## <a name="about-price-lists"></a>Tietoja hinnastoista
Hinnastot ovat joustavia, ja niiden avulla voit määrittää, mihin liiketoimintakumppaniin tai toimintoon ne kohdistetaan. Voit esimerkiksi määrittää yhden hinnaston, joka koskee kaikkia toimittajia ja asiakkaita, tai tarjota erikoishintoja tai -alennuksia kullekin liiketoimintapartnerille, perustuen esimerkiksi osto- tai myyntitilausten vähimmäismäärään tai tiettyyn asiakkaan, nimikkeen, vähimmäismäärän, mittayksikön tai ajanjakson yhdistelmään. Määrittämäsi hinnat ja alennukset kohdistetaan automaattisesti osto- ja myyntiasiakirjoihin. 

## <a name="set-up-prices"></a>Määritä hinnat

Nämä vaiheet vaihtelevat sen mukaan, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuden päivityksen. 

#### <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience)  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Valitse asiakas ja valitse sitten **Hinnat**-toiminto.
3. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Täytä rivi jokaiselle yhdistelmälle, jossa asiakkaalle myönnetään erikoismyyntihinta.

#### <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience)  
Voit lisätä nimikketitä ja palveluita manuaalisesti kullekin riville tai voit käyttää **Ehdota rivejä** -toimintoa luodessasi uusia hintoja valituille nimikkeille, nimikealennusryhmille, resursseille ja muille tuotetyypeille. Jos valitset **Hintarivit – Luo uusi** -sivulla **Ehdota rivejä**, voit suodattimien avulla valita hinnastoihin sisällytettävät nimikkeet tai palvelut. Voit myös määrittää, otetaanko vähimmäismäärä huomioon laskettaessa hintoja, uusien hinnastorivien muutoksen kerrointa ja hintojen osalta pyöristystapaa. 

Uusien hinnastojen tila on oletusarvoisesti **Luonnos**. Kun olet valmis aloittamaan luettelon käyttämisen, voit muuttaa tilaksi **Aktiivinen**.

Voit tarkastella tiettyjen asiakkaiden tai toimittajien hinnastoja ja hintoja valitsemalla **Asiakas**- tai **Toimittaja**-sivulla vastaavasti **Myyntihinnastot**- tai **Ostohinnastot**-toiminnon. Nimikkeille ja resursseille voit tarkastella hinnaston rivejä eri hinnastoissa valitsemalla **Nimike**- ja **Resurssi**-sivuilta **Myyntihinnat** tai **Ostohinnat**.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Valitse asiakas ja valitse sitten **Myyntihinnastot**-toiminto. 
3. Luo uusi myyntihinnasto valitsemalla **Uusi**.
4. Täytä **Yleiset**- ja **Vero**-pikavälilehdissä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Voit lisätä luetteloon kohteita tekemällä jommankumman seuraavista:
   * Voit lisätä useita nimikkeitä valitsemalla **Ehdota rivejä** ja määrittämällä lisättävät nimiketyypit syöttämällä suodatusehdot. Vaihtoehtoisesti voit myös syöttää joitain lisäasetuksia nimikkeille, jotka liittyvät hinnastoon. Voit muuttaa niitä tarvittaessa myöhemmin.
   * Voit kopioida nimikkeitä toisesta hinnastoista valitsemalla **Kopioi rivit** ja valitsemalla kopioitavan hinnaston.
   * Voit lisätä nimikkeitä manuaalisesti valitsemalla **Tuotetyyppi**-kentässä tuotteen tyypin, jolle hinnasto on tarkoitettu. Täytä tarvittaessa jäljellä olevat kentät valintojen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Voit aloittaa hinnaston käyttämisen valitsemalla **Tila**-kentässä **Aktiivinen**.  

---

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

---

## <a name="working-with-invoice-discounts-and-service-charges"></a>Laskualennusten ja palvelumaksujen käyttäminen
Kun käytät laskualennuksia, laskusumman suuruus määrää annettavan alennuksen suuruuden. Voit lisätä **Laskualennukset** -sivulla tietyn summaisille laskuille myös palvelumaksuja.  <!--The Invoice Discounts page is hard to find.-->

Ennen kuin myynneissä voi käyttää laskualennuksia, sovellukseen on annettava tiettyjä tietoja. Sinun täytyy päättää, mille asiakkaille myönnetään tämän tyyppinen alennus, ja mitä alennusprosentteja käytät.  

Jos haluat, että laskualennukset lasketaan automaattisesti, voit määrittää sen **Myyntien ja myyntisaamisten asetukset** -sivulla.  

Voit määrittää jokaiselle asiakkaalle erikseen, annetaanko tälle laskualennuksia, jos tarve on tyydytetty (eli jos laskusumma on tarpeeksi suuri). Laskualennusehdot voi määrittää paikallisena valuuttana kotimaisille asiakkaille ja ulkomaan valuuttana ulkomaisille asiakkaille.  

Voit linkittää alennusprosentit tiettyihin laskusummiin **Laskualennukset**-sivuilla. Voit lisätä niin monta prosenttia kuin on tarpeen. Jokainen asiakas voi olla erillisellä sivulla, tai samalle sivulle voi linkittää useita asiakkaita.  

Spesifiseen laskusummaan voi linkittää alennusprosentin lisäksi (tai sen sijaan) palvelumaksusumman.  

> [!TIP]  
> Ennen tietojen kirjoittamista on suositeltavaa valmistella alennusrakenne etukäteen, jolloin on helpompi nähdä, mitkä asiakkaat linkitetään samaan laskualennussivuun. Lisätietoja myynnin alennuksista on kohdassa [Alennusten määrittäminen asiakkaillesi](/learn/modules/customer-discounts-dynamics-365-business-central/index)Microsoft Learnissa.  

### <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Laskualennuksen määrittäminen asiakkaalle
Kun olet määrittänyt asiakkaat, joille myönnetään laskun alennuksia, määritä laskun alennuskoodi asiakkaiden kortteihin ja määritä kunkin koodin ehdot.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Avaa sen asiakkaan sivu, jolle myönnetään laskun alennuksia.
3. Valitse **Laskualennuksen koodi** -kentässä asianmukaisille laskualennuksen ehdoille koodi, jonka avulla asiakkaan laskualennukset lasketaan. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Laskualennuksen koodit löytyvät olemassa olevien asiakkaiden korteista. Näin voit nopeasti liittää laskualennusten ehtoja asiakkaisiin poimimalla sellaisen asiakkaan nimen, jolla on samat ehdot.

Jatka uuden myyntilaskun alennusehtojen määrittämiseen.

1. Valitse **Asiakkaat** -sivulla **Laskualennukset**-toiminto. **Asiakkaan laskualennukset** -sivu avautuu.
2. Anna **Valuutan koodi** -kenttään sen valuutan koodi, johon rivin laskualennuksen ehdot kohdistetaan. Jätä kenttä tyhjäksi, jos laskualennuksen ehtojen määritys tapahtuu valuutassa EUR.
3. Syötä **Vähimmäissumma**-kenttään laskun vähimmäissumma, joka oikeuttaa alennukseen.
4. Syötä **Alennus-%**-kohtaan laskun alennus prosentteina laskun summasta.
5. Toista vaiheet 5–7 jokaiselle valuutalle, jossa asiakas saa eri laskualennuksen.

Laskualennus on nyt määritetty ja liitetty kyseiselle asiakkaalle. Kun valitset asiakaskoodin muiden asiakkaiden korttien **Laskun alennuskoodi** -kentässä, sama laskualennus liitetään myös näille asiakkaille.

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

## <a name="calculating-the-best-price"></a>Parhaan hinnan laskenta
Kun olet kirjannut myynnin ja ostojen erikoishinnat ja rivialennukset, [!INCLUDE[d365fin](includes/d365fin_md.md)] varmistaa, että nimikekaupan tuotto on aina optimaalinen laskemalla automaattisesti parhaan hinnan myynti- ja ostoasiakirjoille sekä projekti- ja nimikepäiväkirjan riville. Lisätietoja on kohdassa [Parhaan hinnan laskenta](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

## <a name="see-also"></a>Katso myös
[Myynnin määrittäminen](sales-setup-sales.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
