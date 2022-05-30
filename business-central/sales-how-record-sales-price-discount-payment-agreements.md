---
title: Asiakkaiden myyntihintojen ja -alennusten määrittäminen | Microsoft Docs
description: Tietoja myyntiasiakirjojen hinnoittelu- ja alennussopimusten määrittämisestä.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 5ff042e1dec609b568c36967f56a8cd3673b9558
ms.sourcegitcommit: 2fa712d0aabe4287ebd4454c28d142d6baf045a0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/09/2022
ms.locfileid: "8729839"
---
# <a name="record-special-sales-prices-and-discounts"></a>Erikoismyyntihintojen ja -alennusten kirjaaminen
> [!NOTE]
> Vuoden 2020 julkaisuaallossa 2 julkaisimme virtaviivaiset prosessit hintojen ja alennusten määritykseen ja hallintaan. Jos olet uusi asiakas, joka käyttää kyseistä versiota, käytät uutta käyttökokemusta. Jos olet jo asiakas, uuden käyttöokemuksen käyttö riippuu siitä, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuden päivityksen **ominaisuuksien hallinnassa**. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management).

[!INCLUDE[prod_short](includes/prod_short.md)] tukee erilaisia hinnoittelustrategioita, kuten:
* Yhtä hintaa käyttävät mallit, joissa nimikettä myydään aina samaan hintaan.
* Erikoishintasopimukset tiettyjen asiakkaiden tai asiakasryhmien kanssa.
* Kampanjat, kun myynti täyttää erikoistarjouksen kriteerit. Kriteerinä voi olla esimerkiksi se, että tilaus täyttää minimimäärän, on ennen tiettyä päivämäärää tai sisältää tietyntyyppisen nimikkeen.  

Perushintamallin käyttöä varten on määritettävä vain nimikkeen tai resurssin yksikköhinta. Kyseistä hintaa käytetään aina myyntiasiakirjoissa. Edistyneissä malleissa, kuten myyntikampanjan erikoishinnoissa, erikoishintojen ehdot voidaan määrittää **Myyntihinnat**-sivulla. Erikoishintoja voidaan tarjota seuraavien tietojen yhdistelmien perusteella: 

* Asiakas
* Nimike
* Mittayksikkö
* Vähimmäismäärä
* Päivämäärät, jotka määrittävät ajanjakson, jolla hinnat ovat voimassa.

Sen jälkeen kun erikoishinnat on määritetty, [!INCLUDE[prod_short](includes/prod_short.md)] voi laskea parhaat hinnat osto- ja myyntiasiakirjoissa sekä työ- ja nimikepäiväkirjan riveillä. Lisätietoja on kohdassa [Parhaan hinnan laskenta](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Voit määrittää seuraavat kaksi myyntialennustyyppiä:

| Alennustyyppi | Kuvaus |
| --- | --- |
| **Myyntirivin alennus** |Myyntiriveillä käytettävä summa, jos niissä on tietty asiakkaan, nimikkeen, vähimmäismäärän, mittayksikön sekä aloitus- ja lopetuspäivämäärän yhdistelmä. Tätä tyyppiä käytetään samoin kuin myyntihinnoissa. |
| **Laskualennus** |Prosenttialennus, joka vähennetään kokonaissummasta, kun myyntiasiakirjan kaikkien rivien summa ylittää määritetyn vähimmäisarvon. |

> [!TIP]  
> Jos nimikettä ei koskaan myydä alennetulla hinnalla, jätä nimikesivun alennuskentät tyhjiksi äläkä sisällytä nimikettä yhteenkään rivialennuksen määritykseen.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Myyntihinnan määrittäminen asiakkaalle

Nämä vaiheet vaihtelevat sen mukaan, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuspäivityksen. Jos ominaisuuspäivitystä ei ole otettu käyttöön, noudata Nykyinen kokemus -välilehdessä olevia ohjeita. 

#### <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience/)

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
2. Valitse asiakas ja valitse sitten **Hinnat**-toiminto.
3. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Täytä rivi jokaiselle yhdistelmälle, jossa asiakkaalle myönnetään erikoismyyntihinta.

#### <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience/)  

Uusien hinnastojen tila on oletusarvoisesti Luonnos. Luonnoshinnastoja ei sisällytetä hintalaskelmiin. Kun rivejä ei enää lisätä ja haluat aloittaa hintojen käyttämisen, muuta tilaksi Aktiivinen.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
2. Valitse asiakas ja valitse sitten **Myyntihinnastot**-toiminto. 
3. Luo uusi myyntihinnasto valitsemalla **Uusi**.
4. Täytä **Yleiset**- ja **Vero**-pikavälilehdissä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Voit lisätä luetteloon kohteita tekemällä jommankumman seuraavista:
   * Voit lisätä useita nimikkeitä valitsemalla **Ehdota rivejä** ja määrittämällä lisättävät nimiketyypit syöttämällä suodatusehdot. Vaihtoehtoisesti voit syöttää joitain muita asetuksia nimikkeille, jotka liittyvät hinnastoon. Voit muuttaa näitä asetuksia tarvittaessa myöhemmin.
   * Voit kopioida nimikkeitä toisesta hinnastoista valitsemalla **Kopioi rivit** ja valitsemalla kopioitavan hinnaston.
   * Voit lisätä nimikkeitä manuaalisesti valitsemalla ruudukossa **Tuotetyyppi**-kentässä tuotteen tyypin, jolle hinnasto on tarkoitettu. Täytä tarvittaessa jäljellä olevat kentät valintojen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Voit aloittaa hinnaston käyttämisen valitsemalla **Tila**-kentässä **Aktiivinen**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Myynti- ja ostohinnastojen käyttäminen
> [!NOTE]
> Hinnastojen käyttäminen edellyttää, että järjestelmänvalvoja on ottanut **Uusi myyntihinnoittelukokemus** -ominaisuuspäivityksen käyttöön **ominaisuuksien hallinnassa**. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management).

Suurin osa uudesta myyntihinnoittelukokemuksesta muistuttaa nykyistä kokemusta, mutta joitain eroja on. Nämä erot kuvataan seuraavissa osissa.

**Koskee tyyppiä**- ja **Koskee nroa** -kenttien avulla voidaan valita, missä hinnastoa käytetään, oli onko kysymys esimerkiksi asiakkaasta tai asiakashintaryhmästä. **Näytä sarakkeet kohteelle** -asetuksen avulla voit näyttää tai piilottaa hintojen ja alennusten määrittämisessä tarvittavat kentät.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Aiemmin luotujen hintojen muuntaminen, kun hinnoittelun ominaisuuspäivitys otetaan käyttöön
Kun **Uusi myyntihinnoittelukokemus** -ominaisuuspäivitys otetaan käyttöön **Ominaisuuksien hallinta** -sivulla, **Ominaisuustietojen päivitys** -opas avautuu. Käytä **Käytä oletushintoja** -vaihtopainiketta seuraavasti:

* Jos haluat käyttää kaikkia hintoja yhdellä sivulla, ota se käyttöön. Aiemmin luodut hinnat muunnetaan yhdeksi oletushinnastoksi kullekin seuraavista asiakirjoista:

    * Myynti
    * Ostot
    * Projektimyynti
    * Projektiostot 

    Kaikkien näiden alueiden hintoja voidaan muokata **Hintojen työkirja** -sivulla. Oletushinnastot määritetään **Myyntien ja myyntisaamisten asetukset**-, **Ostojen ja ostovelkojen asetukset**- ja **Projektienhallinnan asetukset** -sivuilla. 

> [!NOTE]
> Jos hinnat määritetään vain nimike- tai resurssikorteissa, kyseisiä hintoja ei täytetä oletushinnastoihin ominaisuustietojen päivityksen aikana. Minkä tahansa oletushinnaston voi kuitenkin avata Hintatyökirja-sivulla ja nimike- tai resurssikorteissa määritetyt hinnat voidaan lisätä **Ehdota rivejä** -toiminnolla. 

* Myyntihinnastoja voidaan käyttää, poistamalla hinnasto käytöstä. Nykyiset hinnat muunnetaan uudeksi hinnastoksi jokaiselle seuraavien asioiden yhdistelmälle: 

* Asiakas
* Asiakasryhmä tai kampanja
* Aloitus- ja lopetuspäivämäärät
* Valuutat 

Jos yhdistelmiä on useita, myös hinnastoja on useita.

Jos uusi hinnoittelukokemus on jo otettu käyttöön, oletushinnastot voidaan luoda manuaalisesti tai aiemmin luotu hinnasto voidaan määrittää oletukseksi. Aiemmin luotu hinnasto määritetään oletukseksi siirtämällä **Salli oletusten päivittäminen** -vaihtopainike hinnastossa käyttöönottoasentoon. Määritä hinnasto sitten oletukseksi **Myyntien ja myyntisaamisten asetukset**-, **Ostojen ja ostovelkojen asetukset**- tai **Projektienhallinnan asetukset** -sivuilla.

### <a name="editing-active-price-lists"></a>Aktiivisen hinnastojen muokkaaminen
Jos hintojen muokkaaminen halutaan sallia nimikkeiden, resurssien, asiakkaiden, toimittajien tai muiden hinnoittelua käyttävien entiteettien aktiivisissa hinnastoissa, **Sallii aktiivisen hinnan muokkaaminen** -vaihtopainike siirretään käyttöönottoasentoon **Myyntien ja myyntisaamisten asetukset**- ja **Ostojen ja ostovelkojen asetukset** -sivuilla.   

Kun **Salli aktiivisen hinnan muokkaus** -vaihtopainike on siirretty käytöstäpoistoasentoon, hinnaston päivittäminen edellyttää, että hinnaston tilaksi muutetaan **Luonnos**. Muutos tehdään tämän jälkeen ja hinnasto aktivoidaan uudelleen.

**Hintojen yleiskuvaus** -sivulla on hinnastojen kaikkien hintojen yleiskuvaus. Voit asettaa suodattimia, kun haluat rajata niiden hintojen luetteloa, joita haluat muokata tai lisätä. Hintojen muuttamisen jälkeen hinnat on tarkistettava muiden hinnastojen rivien perusteella käyttämällä **Tarkista rivit**. Hintojen vahvistaminen auttaa välttämään kopioita ja epäselvyyksiä hinnan laskennassa. 

> [!NOTE]
> Kun aktiivisen hinnaston riviä muokataan, rivin tilaksi tulee Luonnos eikä riviä sisällytetä hintalaskelmiin ennen **Tarkista rivit** -toiminnon käyttämistä. Kun hinta on tarkistettu, rivin tilaksi tulee Aktiivinen, ja sitä käytetään hintalaskelmissa.

Uusia hintoja lisätään **Hintojen yleiskuvaus** -sivun **Lisää uusia rivejä** -toiminnolla. **Hintojen työkirja** -sivu avautuu, ja voit lisätä hintarivejä joko ehdottamalla niitä ehtojen perusteella, kopioimalla ne muista hinnastoista tai syöttämällä ne manuaalisesti. Uusia hintoja voi sitten verrata muihin hinnastoihin **Ota käyttöön hinnan muutos** -toiminnolla. Tällä tavoin voidaan välttää kaksoiskappaleet ja epäselvyydet hinnan laskennassa.

## <a name="to-copy-sales-prices"></a>Myyntihintojen kopioiminen
Nämä vaiheet vaihtelevat sen mukaan, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuspäivityksen. Jos ominaisuuspäivitystä ei ole otettu käyttöön, noudata Nykyinen kokemus -välilehdessä olevia ohjeita.

#### <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience/)  

Jos haluat kopioida myyntihintoja, kuten jonkin yksittäisen asiakkaan hintoja koko asiakashintaryhmälle, sinun tulee ajaa **Ehdota myyntihinta työkirja** -erätyö **Myyntihintatyökirja**-sivulla.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntihintatyökirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Ehdota myyntihintaa työkirjalle**. -toiminto.  
3. Täytä **Myyntihinnat**-pikavälilehden kenttiin kopioitavien, alkuperäisten myyntihintojen **Myynnin tyyppi** ja **Myyntikoodi**.  
4. Täytä pyyntösivun yläosassa **Myynnin tyyppi**- ja **Myyntikoodi**-kenttiin tyyppi ja nimi, joihin haluat kopioida myyntihinnat.  
5. Jos haluat eräajon luovan uusia hintoja, valitse **Luo uudet hinnat** -valintaruutu.  
6. Täytä **Myyntihintatyökirja**-sivun rivit ehdotetuilla uusilla hinnoilla valitsemalla **OK**. Tämä ilmaisee, että hinnat ovat voimassa valitulle myyntityypille.  

   > [!NOTE]  
   > Tämä eräajo luo ainoastaan ehdotuksia eikä se ota ehdotettuja muutoksia käyttöön. Jos olet tyytyväinen ehdotuksiin ja haluat ottaa ne käyttöön eli lisätä ne **Myyntihinnat**-sivulle, valitse **Ota käyttöön hinnan muutos** -toiminto **Myyntihinnan työkirja** -sivulla.

#### <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience/)  
Voit määrittää, käyttävätkö uudet hinnastot kopioimasi luettelon otsikon asetuksia vai kopioitavan uuden luettelon asetuksia. Jos haluat käyttää sen hinnaston asetuksia, johon kopioit hinnat, ota käyttöön **Käytä oletusarvoja lähteestä** -vaihto.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntihinnastot** ja valitse sitten liittyvä linkki. 
2. Valitse kopioitava hinnasto ja valitse sitten **Kopioi rivit**.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Kahdella eri nimikkeillä ei voi olla samoja asetuksia mutta eri hintoja. Jos näin tapahtuu, näyttöön tulee sanoma, kun aktivoit hinnaston. Voit valita käytettävän hinnan avaamalla hinnaston ja poistamalla virheellisen hinnan.  
  
---

## <a name="to-bulk-update-item-prices"></a>Nimikehintojen joukkopäivitys
Nämä vaiheet vaihtelevat sen mukaan, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuspäivityksen. Jos ominaisuuspäivitystä ei ole otettu käyttöön, noudata Nykyinen kokemus -välilehdessä olevia ohjeita.

#### <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience/)

Jos nimikehinnoille halutaan tehdä joukkopäivitys, kuten nostaa kaikkien nimikkeiden hintoja tietyllä prosenttiosuudella, Myyntihinnan työkirja -sivu voidaan täyttää seuraavilla erätöillä:

* **Ehdota myyntihintaa työkirj.** Ehdottaa muutoksia kahdella tavalla. Joko käyttämällä muutoskerrointa aiemmin luoduissa myyntihinnoissa tai kopioimalla aiemmin luodut myyntihintasopimukset toisiin asiakkaisiin, asiakashintaryhmiin tai myyntikampanjoihin.
* **Ehdota nimikehintaa työkirjaan** Ehdottaa muutoksia kahdella tavalla. Joko käyttämällä muuntokerrointa nimikekorttien aiemmin luoduissa yksikköhinnoissa tai ehdottamalla hintoja esimerkiksi uusille valuutta- ja mittayksikköyhdistelmille. Erätyö ei muuta nimikkeiden yksikkökohtaisia hintoja.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntihintatyökirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Ehdota nimikehintaa työkirjaan** -toiminto.  
3. Täytä **Nimike**-pikavälilehdessä **Nro**- tai **Varaston kirjausryhmä** -kenttään tai muihin kenttiin päivitettävät alkuperäiset hinnat.  
4. Täytä pyyntösivun yläosassa **Myynnin tyyppi** ja **Myyntikoodi** tyypillä ja nimellä, joihin haluat kopioida myyntihinnat.
5. Jos eräajon halutaan muuttavan ehdotettuja hintoja automaattisesti, anna muutos **Muutoskerroin**-kentässä. Esimerkki: jos annat 1,15 **Muutoskerroin**-kentässä, nimikehinta nousee 15 %.  
6. Jos eräajon halutaan luovan uusia hintoja, siirrä **Luo uudet hinnat** -vaihtopainike käyttöönottoasentoon.  
7. Täytä **Myyntihinnan työkirja** -sivun rivit ehdotetuilla uusilla hinnoilla valitsemalla **OK**-painike.
8. Ehdotukset toteutetaan **Toteuta hinnan muutokset** -toiminnolla. Eräajo luo ehdotuksia muttei toteuta niitä. 

#### <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience/)

Jos haluat päivittää monien nimikkeiden hinnat, sinun täytyy luoda uusi hinnasto ja kopioida rivit olemassa olevasta hinnastosta. Kun kopioit rivit, voit määrittää suodattimien avulla, mitä haluat kopioida, ja voit määrittää kokonaisluvun tai desimaaliluvun **Muutoskerroin**-kenttään hintojen korottamiseksi tai vähentämiseksi. Hinnaston tilan on oltava **Luonnos**. Voit poistaa vanhan hinnaston käytöstä tarpeen mukaan.

> [!NOTE]
> Kahdella eri rivillä ei voi olla samoja asetuksia mutta eri hintoja. Jos näin tapahtuu, näyttöön tulee sanoma, kun aktivoit hinnaston. Voit valita käytettävän hinnan avaamalla hinnaston ja poistamalla virheellisen hinnan.  

---

## <a name="best-price-calculation"></a>Parhaan hinnan laskenta
Kun olet tallentanut erikoishinnat ja rivialennukset myynneille ja ostoille, [!INCLUDE[d365fin](includes/d365fin_md.md)] laskee parhaan hinnan myynti- ja ostotositteisiin sekä työ- ja nimikepäiväkirjariveihin.

Paras hinta on alin hinta, jolla on suurin sallittu rivialennus tiettynä päivänä. [!INCLUDE[d365fin](includes/d365fin_md.md)] laskee parhaat hinnat, kun se lisää yksikköhinnat ja rivialennusprosentit asiakirjan ja päiväkirjan riveille.

> [!NOTE]  
> Seuraavaksi kerrotaan, miten myynnin paras hinta lasketaan. Samaa laskentaa käytetään ostoissa.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] tarkistaa laskutusasiakas- ja nimikeyhdistelmän ja laskee sitten käytettävän yksikköhinnan ja rivialennusprosentin seuraavien ehtojen mukaisesti:

    - Onko asiakkaalla hinta- tai alennussopimus tai kuuluuko asiakas ryhmään, jolla on tällainen sopimus on?
    - Kuuluuko rivillä oleva nimike tai nimikealennusryhmä johonkin näistä hinta- tai alennussopimuksista?
    - Onko tilauspäivämäärä (tai laskun ja hyvityslaskun osalta kirjauspäivämäärä) hinta- tai alennussopimuksen aloitus- ja lopetuspäivämäärän välissä?
    - Onko mittayksikön koodia määritelty? Jos on, [!INCLUDE[d365fin](includes/d365fin_md.md)] tarkastaa hinnat tai alennukset, joilla on sama mittayksikön koodi, ja hinnat tai alennukset, joilla ei ole mittayksikön koodia.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] tarkistaa, sovelletaanko mitään hinta-/alennussopimuksia asiakirjan tai päiväkirjan rivin tietoihin. Sen jälkeen se lisää sovellettavan yksikköhinnan ja rivialennusprosentin käyttämällä seuraavia kriteereitä:

    - Täytyykö hinta- tai alennussopimuksen vähimmäismäärävaatimus?
    - Täytyykö hinta- tai alennussopimuksen valuuttavaatimus? Jos täyttyy, kyseisen valuutan alhaisin hinta ja suurin rivialennus lisätään, vaikka paikallinen valuutta antaisi paremman hinnan. Jos määritellyllä valuuttakoodilla ei ole hinta- tai alennusopimusta, [!INCLUDE[d365fin](includes/d365fin_md.md)] lisää alhaisimman hinnan ja suurimman rivialennuksen paikallisena valuuttana.

Jos erikoishintaa ei voi laskea rivin nimikkeelle, joko viimeinen välitön kustannus tai nimikekortin yksikköhinta lisätään.

## <a name="sales-invoice-discounts-and-service-charges"></a>Myyntilaskualennukset ja palvelumaksut
Laskualennuksia käytettäessä laskun loppusumma määrittää annettavan alennuksen suuruuden. Voit lisätä **Asiakkaan laskualennukset** -sivulla tietyn summaisille laskuille myös palvelumaksuja.  

Ennen kuin myynneissä voi käyttää laskualennuksia, on määritettävä tiettyjä tietoja. Sinun täytyy päättää seuraavista asioista:  

- Ketkä asiakkaat saavat tämän tyyppisen alennuksen?  
- Mitä alennusprosentteja käytetään?  

Jos laskualennukset halutaan laskettavan automaattisesti, **Lask. laskun alennus** -vaihtopainike on siirrettävä käyttöönottoasentoon **Myyntien ja myyntisaamisten asetukset** -sivulla.  

Voit määrittää, myönnetäänkö laskuista alennuksia, kun lasku täyttää tietyt kriteerit kullekin asiakkaalle. Näin voidaan tehdä esimerkiksi silloin, kun laskun summa on riittävän suuri. Laskualennuksen voi määrittää paikallisena valuuttana kotimaisille asiakkaille tai ulkomaan valuuttana ulkomaisille asiakkaille.  

Voit linkittää alennusprosentit tiettyihin laskusummiin kunkin asiakkaan **Asiakkaan laskualennukset** -sivulla. Voit syöttää mitä tahansa prosenttilukuja. Jokainen asiakas voi olla erillisellä sivulla, tai samalle sivulle voi linkittää useita asiakkaita.  

Alennusprosentin lisäksi tai sen sijaan tiettyyn laskusummaan voidaan linkittää palvelumaksusumma.  

> [!TIP]  
> Ennen kuin näitä tietoja aletaan syöttää ohjelmaan, olisi hyvä tehdä luonnos alennusrakenteesta, jota haluat käyttää. Tällä tavalla on helpompi nähdä, ketkä asiakkaat voi linkittää samaan laskualennussivulle. Mitä vähemmän sivuja on määritettävä, sitä nopeampaa perustietojen antaminen on.

Koulutusta myynnin alennuksista on Microsoft Learnin kohteessa [Alennusten määrittäminen asiakkaillesi](/learn/modules/customer-discounts-dynamics-365-business-central/index).  

### <a name="calculating-invoice-discounts-on-sales"></a>Myynnin laskualennusten laskenta

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Myyntirivialennuksien määrittäminen asiakkaalle
Nämä vaiheet vaihtelevat sen mukaan, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuspäivityksen. Jos ominaisuuspäivitystä ei ole otettu käyttöön, noudata Nykyinen kokemus -välilehdessä olevia ohjeita.

#### <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience/)  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
2. Avaa kyseessä olevan asiakkaan kortti ja valitse **Rivialennukset**-toiminto.
3. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Täytä rivi jokaiselle yhdistelmälle, jossa asiakkaalle myönnetään myyntirivialennus.

> [!Note]
> Kun avaat tietyn asiakkaan **Myyntihinnat**- ja **Myyntirivialennukset**-sivut, **Myyntityypin suodatus**-ja **Myyntikoodin suodatus** -kentät on määritetty asiakkaalle, eikä niitä voi muuttaa tai poistaa.
>
> Kun haluat määrittää hinnat tai rivialennukset kaikille asiakkaille, asiakkaan hintaryhmälle tai kampanjalle, sinun täytyy avata sivut nimikekortista. Vaihtoehtoisesti voit käyttää myyntihinnoille **Myyntihinnan työkirja** -sivua. Lisätietoja on kohdassa [Nimikehintojen joukkopäivitys](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience/)  

1. Valitse ![Lamppu, joka avaa Kerro -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä")-kuvake, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
2. Valitse asiakas ja valitse sitten **Myyntihinnastot**-toiminto.
3. Avaa hinnasto, jolle rivialennus määritetään.
4. Luo uusi rivi tai valitse aiemmin luotu rivi ja täytä kentät tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Valitse **Määrittää**-kentässä joko **Hinta ja alennus** tai vain **Alennus**. 
6. Määritä alennusprosentti **Rivialennus-%**-kentässä.

    > [!TIP]
    > Jos muokkaat aiemmin luotua riviä, voit suodattaa rivit valitsemalla haluamasi asetuksen **Näytä sarakkeet kohteelle** -kentästä.

    > [!NOTE]  
    > Laskualennuksen koodit löytyvät olemassa olevien asiakkaiden korteista. Näin voit nopeasti liittää laskualennusten ehtoja asiakkaisiin poimimalla sellaisen asiakkaan nimen, jolla on samat ehdot. Voit määrittää asiakaskohtaisia laskualennusehtoja määrittämällä **Laskun alennuskoodi** -kentän asiakkaan asiakaskoodille ja jatkamalla sitten seuraavaan vaiheeseen.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Laskualennuksen määrittäminen asiakkaalle
Kun olet määrittänyt asiakkaat, joille myönnetään laskun alennuksia, määritä laskun alennuskoodi asiakaskorttisivuille. Määritä sitten ehdot kullekin koodille.

1. Valitse ![Lamppu, joka avaa Kerro -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä")-kuvake, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
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

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Myynnin määrittäminen](sales-setup-sales.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]