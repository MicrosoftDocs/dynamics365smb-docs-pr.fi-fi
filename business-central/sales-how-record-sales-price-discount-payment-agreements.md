---
title: Asiakkaiden myyntihintojen ja -alennusten määrittäminen | Microsoft Docs
description: Tietoja myyntiasiakirjojen hinnoittelu- ja alennussopimusten määrittämisestä ja käyttämisestä.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 1345, 7002, 7007, 7015, 7016, 7023
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 8b7943caba8482e39217307be904f368f0ec31c0
ms.sourcegitcommit: a9e2aaee735870af566db68532cfa697347d68e0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752428"
---
# <a name="record-sales-prices-and-discounts"></a>Myyntihintojen ja -alennusten kirjaaminen
> [!NOTE]
> Vuoden 2020 julkaisuaallossa 2 julkaisimme virtaviivaiset prosessit hintojen ja alennusten määritykseen ja hallintaan. Jos olet uusi asiakas, joka käyttää kyseistä versiota, käytät uutta käyttökokemusta. Jos olet jo asiakas, uuden käyttöokemuksen käyttö riippuu siitä, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuden päivityksen **ominaisuuksien hallinnassa**. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management).

[!INCLUDE[prod_short](includes/prod_short.md)] tukee erilaisia hinnoittelustrategioita olipa kyse yhtä hintaa käyttävistä malleista, joissa nimikkeen myyntihinta on aina sama, tai myyntikampanjan tiettyjä asiakkaita, asiakasryhmissä tai erikoistarjouksia koskevista erikoishintasopimuksista. Erikoishinta voidaan tarjota myyntitilauksessa esimerkiksi seuraavien ehtojen perusteella:

* Kyse on vähimmäismäärästä.
* Kyse on tietystä nimikkeestä.  
* Kyse tiettynä ajankohtana luodusta tilauksesta.

Perushintamallin käyttöä varten on määritettävä vain nimikkeen tai resurssin yksikköhinta. Kyseistä hintaa käytetään aina myyntiasiakirjoissa. Edistyneissä malleissa, kuten myyntikampanjan erikoishinnoissa, erikoishintojen ehdot voidaan määrittää **Myyntihinnat**-sivulla. Erikoishintoja voidaan tarjota seuraavien yhdistelmien perusteella: 

* Asiakas
* Nimike
* Mittayksikkö
* Vähimmäismäärä
* Hintojen voimassaolon määrittävät päivämäärävälit

Sen jälkeen kun erikoishinnat on määritetty, [!INCLUDE[prod_short](includes/prod_short.md)] voi lisäksi laskea automaattisesti parhaan hinnan osto- ja myyntiasiakirjoissa sekä työ- ja nimikepäiväkirjan riveillä. Lisätietoja on kohdassa [Parhaan hinnan laskenta](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).  

Myyntialennuksia varten voidaan määrittää ja niissä voidaan käyttää seuraavia tyyppejä:

| Alennustyyppi | Kuvaus |
| --- | --- |
| **Myyntirivin alennus** |Myyntiriveillä käytettävä summa, jos tietty asiakkaan, nimikkeen, vähimmäismäärän, mittayksikön sekä aloitus- ja lopetuspäivämäärän yhdistelmä on olemassa. Nämä yhdistelmä toimivat samalla tavoin kuin myyntihinnoissa. |
| **Laskualennus** |Prosenttialennus, joka vähennetään kokonaissummasta, kun myyntiasiakirjan kaikkien rivien summa ylittää määritetyn vähimmäisarvon. |

> [!TIP]  
> Jos nimikettä ei koskaan myydä alennetulla hinnalla, jätä nimikesivun alennuskentät tyhjiksi äläkä sisällytä nimikettä yhteenkään rivialennuksen määritykseen.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Myyntihinnan määrittäminen asiakkaalle

Nämä vaiheet vaihtelevat sen mukaan, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuspäivityksen. Jos ominaisuuspäivitystä ei ole otettu käyttöön, noudata Nykyinen kokemus -välilehdessä olevia ohjeita. 

#### <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience/)

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Valitse asiakas ja valitse sitten **Hinnat**-toiminto.
3. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Täytä rivi jokaiselle yhdistelmälle, jossa asiakkaalle myönnetään erikoismyyntihinta.

---

#### <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience/)  
Uusien hinnastojen tila on oletusarvoisesti Luonnos. Luonnoshinnastoja ei sisällytetä hintalaskelmiin. Kun rivejä ei enää lisätä ja haluat aloittaa hintojen käyttämisen, muuta tilaksi Aktiivinen.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Valitse asiakas ja valitse sitten **Myyntihinnastot**-toiminto. 
3. Luo uusi myyntihinnasto valitsemalla **Uusi**.
4. Täytä **Yleiset**- ja **Vero**-pikavälilehdissä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Nimikkeitä voi lisätä luetteloon seuraavasti:
   * Voit lisätä useita nimikkeitä valitsemalla **Ehdota rivejä** ja määrittämällä lisättävät nimiketyypit syöttämällä suodatusehdot. Nimikkeille voi valinnaisesti antaa muita asetuksia. Nämä asetukset ovat hinnastokohtaisia. Niitä voidaan muuttaa tarvittaessa myöhemmin.
   * Voit kopioida nimikkeitä toisesta hinnastoista valitsemalla **Kopioi rivit** ja valitsemalla kopioitavan hinnaston.
   * Voit lisätä nimikkeitä manuaalisesti valitsemalla rivin **Tuotetyyppi**-kentässä tuotteen tyypin, jossa hinnastoa käytetään. Täytä tarvittaessa jäljellä olevat kentät valintojen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Voit aloittaa hinnaston käyttämisen valitsemalla **Tila**-kentässä **Aktiivinen**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Myynti- ja ostohinnastojen käyttäminen
> [!NOTE]
> Hinnastojen käyttäminen edellyttää, että järjestelmänvalvoja on ottanut **Uusi myyntihinnoittelukokemus** -ominaisuuspäivityksen käyttöön **ominaisuuksien hallinnassa**. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management).

**Koskee tyyppiä**- ja **Koskee nroa** -kenttien avulla voidaan valita, missä hinnastoa käytetään, oli onko kysymys esimerkiksi asiakkaasta tai asiakashintaryhmästä. **Näytä sarakkeet kohteelle** -kentän avulla voidaan näyttää vain hintoja, alennuksia tai hintoja ja alennuksia koskevat sarakkeet.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Aiemmin luotujen hintojen muuntaminen, kun hinnoittelun ominaisuuspäivitys otetaan käyttöön
Kun **Uusi myyntihinnoittelukokemus** -ominaisuuspäivitys otetaan käyttöön **Ominaisuuksien hallinta** -sivulla, **Ominaisuustietojen päivitys** -opas avautuu. Käytä **Käytä oletushintoja** -vaihtopainiketta seuraavasti:

* Jos haluat käyttää kaikkia hintoja yhdellä sivulla, ota se käyttöön. Aiemmin luodut hinnat muunnetaan yhdeksi oletushinnastoksi kullekin seuraavista:

    * Myynti
    * Ostot
    * Projektimyynti
    * Projektiostot 

    Tämän jälkeen kaikkien näiden alueiden hintoja voidaan muokata **Hintojen työkirja** -sivulla. Oletushinnastot määritetään **Myyntien ja myyntisaamisten asetukset**-, **Ostojen ja ostovelkojen asetukset**- ja **Projektienhallinnan asetukset** -sivuilla. 

    > [!NOTE]
    > Jos hinnat määritetään vain nimike- tai resurssikorteissa, kyseisiä hintoja ei täytetä oletushinnastoihin tietojen päivityksen aikana. Minkä tahansa oletushinnaston voi kuitenkin avata Hintatyökirja-sivulla ja nimike- tai resurssikorteissa määritetyt hinnat voidaan lisätä **Ehdota rivejä** -toiminnolla. 

* Myyntihinnastoja voidaan käyttää, poistamalla hinnasto käytöstä. Aiemmin luodut hinnat muunnetaan kunkin asiakas-, asiakasryhmä- tai kampanjayhdistelmän uudeksi hinnastoksi, jotka sisältävät alkamis- ja päättymispäivämäärät sekä valuutat. Jos yhdistelmiä on useita, myös hinnastoja on useita.

Jos uusi hinnoittelukokemus on jo otettu käyttöön, oletushinnastot voidaan luoda manuaalisesti tai aiemmin luotu hinnasto voidaan määrittää oletukseksi. Aiemmin luotu hinnasto määritetään oletukseksi siirtämällä **Salli oletusten päivittäminen** -vaihtopainike hinnastossa käyttöönottoasentoon. Määritä hinnasto sitten oletukseksi **Myyntien ja myyntisaamisten asetukset**-, **Ostojen ja ostovelkojen asetukset**- tai **Projektienhallinnan asetukset** -sivuilla.

### <a name="editing-active-price-lists"></a>Aktiivisen hinnastojen muokkaaminen
Jos hintojen muokkaaminen halutaan sallia nimikkeiden, resurssien, asiakkaiden, toimittajien tai muiden hinnoittelua käyttävien entiteettien aktiivisissa hinnastoissa, **Sallii aktiivisen hinnan muokkaaminen** -vaihtopainike siirretään käyttöönottoasentoon **Myyntien ja myyntisaamisten asetukset**- ja **Ostojen ja ostovelkojen asetukset** -sivuilla. 

Kun **Salli aktiivisen hinnan muokkaus** -vaihtopainike on siirretty käytöstäpoistoasentoon, hinnaston päivittäminen edellyttää, että hinnaston tilaksi muutetaan **Luonnos**. Muutos tehdään tämän jälkeen ja hinnasto aktivoidaan uudelleen.

**Hintojen yleiskuvaus** -sivulla on hinnastojen kaikkien hintojen yleiskuvaus. Luetteloa voi tarkentaa suodattimia määrittämällä. Hintojen muuttamisen jälkeen hinnat on tarkistettava muiden hinnastojen rivien perusteella käyttämällä **Tarkista rivit**. Hintojen tarkistaminen auttaa esimerkiksi välttää hintojen kaksoiskappaleet ja ristiriitaiset hinnat. 

> [!NOTE]
> Kun aktiivisen hinnaston riviä muokataan, rivin tilaksi tulee Luonnos eikä rivi sisällytetä hintalaskelmiin ennen **Tarkista rivit** -toiminnon käyttämistä. Kun hinta on tarkistettu, rivin tilaksi tulee Aktiivinen, ja sitä käytetään hintalaskelmissa.

Uusia hintoja lisätään **Hintojen yleiskuvaus** -sivun **Lisää uusia rivejä** -toiminnolla. Hintarivejä lisätään avautuvalla **Hintojen työkirja** -sivulla seuraavasti:

* Ehtoihin perustuvat ehdotukset
* Kopiointi muista hinnastoista
* Manuaalinen syöttäminen 

Uusia hintoja voi sitten verrata muihin hinnastoihin **Ota käyttöön hinnan muutos** -toiminnolla. Tällä tavoin voidaan välttää kaksoiskappaleet.

## <a name="to-copy-sales-prices"></a>Myyntihintojen kopioiminen
Nämä vaiheet vaihtelevat sen mukaan, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuspäivityksen. Jos ominaisuuspäivitystä ei ole otettu käyttöön, noudata Nykyinen kokemus -välilehdessä olevia ohjeita.

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

---

#### <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience/)  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntihinnastot** ja valitse sitten liittyvä linkki. 
2. Valitse kopioitava hinnasto ja valitse sitten **Kopioi rivit**.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Kahdella eri rivillä ei voi olla samoja asetuksia mutta eri hintoja. Jos näin tapahtuu, näyttöön tulee sanoma, kun aktivoit hinnaston. Voit valita käytettävän hinnan avaamalla hinnaston ja poistamalla virheellisen hinnan.  
  
---

## <a name="to-bulk-update-item-prices"></a>Nimikehintojen joukkopäivitys
Nämä vaiheet vaihtelevat sen mukaan, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuspäivityksen. Jos ominaisuuspäivitystä ei ole otettu käyttöön, noudata Nykyinen kokemus -välilehdessä olevia ohjeita.

#### <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience/)

Jos nimikehinnoille halutaan tehdä joukkopäivitys, kuten nostaa kaikkien nimikkeiden hintoja tietyllä prosenttiosuudella, **Myyntihinnan työkirja** voidaan täyttää seuraavilla erätöillä:

* **Ehdota nimikehintaa työkirjaan** ehdottaa muutoksia käyttämällä muutoskerrointa aiemmin luoduissa myyntihinnoissa tai kopioimalla aiemmin luodut myyntihintasopimukset toisiin asiakkaisiin, asiakashintaryhmiin tai myyntikampanjoihin.
* **Ehdota nimikehintaa työkirjaan** ehdottaa muutoksia käyttämällä muuntokerrointa nimikekorttien aiemmin luoduissa yksikköhinnoissa tai ehdottamalla hintoja esimerkiksi uusille valuutta- ja mittayksikköyhdistelmille. Nimikkeiden yksikköhintoja ei muuteta.    

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntihintatyökirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Ehdota nimikehintaa työkirjaan** -toiminto.  
3. Täytä **Nimike**-pikavälilehdessä **Nro**- tai **Varaston kirjausryhmä** -kenttään tai muihin kenttiin päivitettävät alkuperäiset hinnat.  
4. Täytä pyyntösivun yläosassa **Myynnin tyyppi** ja **Myyntikoodi** tyypillä ja nimellä, joihin haluat kopioida myyntihinnat.
5. Jos eräajon halutaan muuttavan ehdotettuja hintoja automaattisesti, anna muutos **Muutoskerroin**-kentässä. Esimerkki: jos annat **Muutoskerroin**-kentässä annetaan **1,15**, nimikehinta nousee **15 %**.  
6. Jos eräajon halutaan luovan uusia hintoja, siirrä **Luo uudet hinnat** -vaihtopainike käyttöönottoasentoon.  
7. Täytä **Myyntihinnan työkirja** -sivun rivit ehdotetuilla uusilla hinnoilla valitsemalla **OK**.
8. Ehdotukset toteutetaan **Toteuta hinnan muutokset** -toiminnolla. Eräajo luo ehdotuksia muttei toteuta niitä.

---

#### <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience/)

Jos haluat päivittää monien nimikkeiden hinnat, sinun täytyy luoda uusi hinnasto ja kopioida rivit olemassa olevasta hinnastosta. Kun kopioit rivit, voit määrittää suodattimien avulla, mitä haluat kopioida, ja voit määrittää kokonaisluvun tai desimaaliluvun **Muutoskerroin**-kenttään hintojen korottamiseksi tai vähentämiseksi. Hinnaston tilan on oltava **Luonnos**. Voit poistaa vanhan hinnaston käytöstä tarpeen mukaan.

> [!NOTE]
> Kahdella eri rivillä ei voi olla samoja asetuksia mutta eri hintoja. Jos näin tapahtuu, näyttöön tulee sanoma, kun aktivoit hinnaston. Voit valita käytettävän hinnan avaamalla hinnaston ja poistamalla virheellisen hinnan.  

## <a name="sales-invoice-discounts-and-service-charges"></a>Myyntilaskualennukset ja palvelumaksut
Laskualennuksia käytettäessä laskun loppusumma määrittää annettavan alennuksen suuruuden. Voit lisätä **Asiakkaan laskualennukset** -sivulla tietyn summaisille laskuille myös palvelumaksuja.  

Jos laskualennukset halutaan laskettavan automaattisesti, **Lask. laskun alennus** -vaihtopainike on siirrettävä käyttöönottoasentoon **Myyntien ja myyntisaamisten asetukset** -sivulla.  

Kullekin asiakkaalle voidaan määrittää, tarjotaanko laskualennuksia, jos ehdot täyttyvät. Näin voidaan tehdä esimerkiksi silloin, kun laskun summa on riittävän suuri. Laskualennusehdot voi määrittää paikallisena valuuttana kotimaisille asiakkaille ja ulkomaan valuuttana ulkomaisille asiakkaille.  

Voit linkittää alennusprosentit tiettyihin laskusummiin kunkin asiakkaan **Asiakkaan laskualennukset** -sivulla. Voit syöttää mitä tahansa prosenttilukuja. Jokainen asiakas voi olla erillisellä sivulla, tai samalle sivulle voi linkittää useita asiakkaita.  

Alennusprosentin lisäksi tai sen sijaan tiettyyn laskusummaan voidaan linkittää palvelumaksusumma.  

Koulutusta myynnin alennuksista on Microsoft Learnin kohteessa [Alennusten määrittäminen asiakkaillesi](/learn/modules/customer-discounts-dynamics-365-business-central/index).  

---

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

---

#### <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience/)  

1. Valitse ![Lamppu, joka avaa Kerro -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä")-kuvake, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
2. Valitse asiakas ja valitse sitten **Myyntihinnastot**-toiminto.
3. Avaa hinnasto, jolle rivialennus määritetään.
4. Luo uusi rivi tai valitse aiemmin luotu rivi ja täytä kentät tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Valitse **Määrittää**-kentässä joko **Hinta ja alennus** tai vain **Alennus**. 
6. Määritä alennusprosentti **Rivialennus-%**-kentässä.

    > [!TIP]
    > Rivejä voidaan suodattaa valitsemalla sopiva vaihtoehto **Näytä sarakkeet kohteelle** -kentässä.
    > [!NOTE]  
    > Laskualennuksen koodit ilmaistaan aiemmin luoduissa asiakaskorteissa. Kun asiakkaiden nimiä käytetään koodeina, laskualennusten ehdot voidaan määrittää nopeasti asiakkaille valitsemalla sellaisen asiakkaan nimi, jolla on samat ehdot. Voit määrittää asiakaskohtaisia laskualennusehtoja määrittämällä **Laskun alennuskoodi** -kentän asiakkaan asiakaskoodille ja jatkamalla sitten seuraavaan vaiheeseen.
---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Laskualennuksen määrittäminen asiakkaalle
Kun olet määrittänyt asiakkaat, joille myönnetään laskun alennuksia, määritä laskun alennuskoodi asiakkaiden kortteihin ja määritä kunkin koodin ehdot.

1. Valitse ![Lamppu, joka avaa Kerro -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä")-kuvake, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
2. Avaa sen asiakkaan sivu, jolle myönnetään laskun alennuksia.
3. Valitse **Laskualennuksen koodi** -kentässä asianmukaisille laskualennuksen ehdoille koodi, jonka avulla asiakkaan laskualennukset lasketaan. 

> [!NOTE]  
> Laskualennuksen koodit ilmaistaan aiemmin luoduissa asiakaskorteissa. Kun asiakkaiden nimiä käytetään koodeina, laskualennusten ehdot voidaan määrittää nopeasti asiakkaille valitsemalla sellaisen asiakkaan nimi, jolla on samat ehdot.

Seuraavaksi määritetään uuden myyntilaskun alennusehdot.

1. Valitse **Asiakkaat** -sivulla **Laskualennukset**-toiminto. **Asiakkaan laskualennukset** -sivu avautuu.
2. Anna **Valuutan koodi** -kenttään sen valuutan koodi, johon rivin laskualennuksen ehdot kohdistetaan. Jätä kenttä tyhjäksi, jos laskualennuksen ehtojen määritys tapahtuu valuutassa EUR.
3. Syötä **Vähimmäissumma**-kenttään laskun vähimmäissumma, joka oikeuttaa alennukseen.
4. Syötä **Alennus-%**-kohtaan laskun alennus prosentteina laskun summasta.
5. Toista vaiheet 5–7 jokaiselle valuutalle, jossa asiakas saa eri laskualennuksen.

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