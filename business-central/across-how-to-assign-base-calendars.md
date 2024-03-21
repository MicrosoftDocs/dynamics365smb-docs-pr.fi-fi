---
title: Peruskalenterien määrittäminen
description: Voit määrittää yrityksellesi ja sen liikekumppaneille peruskalenterin toimitus- ja vastaanottopäivämäärien laskemista varten määritettyjen työpäivien mukaan.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '7600, 7601, 7602, 5703'
ms.date: 06/11/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-base-calendars"></a>Peruskalenterien määrittäminen

Peruskalenterin voi määritellä yrityksellesi ja sen liiketoimintakumppaneille, esimerkiksi asiakkaille, toimittajille tai sijainneille. Toimituksen ja vastaanoton päivämäärät lasketaan tuleville myyntitilaus-, ostotilaus-, siirtotilaus- ja tuotantotilausriveille kalenteriin määritettyjen työpäivien mukaisesti. Päätehtävä uuden peruskalenterin määrittämisessä on käytettävien, muiden kuin työpäivien eritteleminen ja määritteleminen.  

## <a name="to-set-up-a-base-calendar"></a>Peruskalenterin määrittäminen

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Peruskalenteri** ja valitse sitten vastaava linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Täytä **Koodi**-kenttä.  
4. Valitse **Ylläpidä peruskalenterin muutokset** -toiminto.
5. Voit merkitä **Peruskalenterin muutokset** -sivun **Toistamisjärjestelmä**-kentässä tietyn päivämäärän tai päivän toistuvaksi ei-työskentelypäiväksi. Valittavat vaihtoehdot ovat **Vuosittain toistuva** ja **Viikoittain toistuva**.  

    Jos valitset **Vuosittain toistuva** -vaihtoehdon, asianmukainen päivämäärä on syötettävä myös **Pvm**-kenttään.  

    Jos valitset **Viikoittain toistuva** -vaihtoehdon, **Päivä**-kenttään on valittava asianmukainen viikonpäivä. Jos kenttä jätetään tyhjäksi, **Pvm**-kenttä tulee täyttää. Ohjelma täyttää **Päivämäärä**-kentän automaattisesti.  

Kun teet tapahtuman, **Ei työskentely** -kenttä on valittuna. Voit valita valintaruudun poiston tehdäksesi valinnasta työpäivän.  
 Kun palaat peruskalenterin korttiin, huomaat, että ohjelma on päivittänyt automaattisesti tekemäsi vapaapäivätapahtumat. Nämä tapahtumat näkyvät nyt punaisina ja **Ei työskentely** -kenttä on valittuna.  

> [!NOTE]  
>  Uutta peruskalenteria määritettäessä kalenterista voi valita ja kopioida rivejä. Tämä tehdään asianmukaisessa **Peruskalenterin muutokset** -sivulla.  

> [!IMPORTANT]  
>  Toimittajalle tai sijainnille määritetyt peruskalenterit vaikuttavat siihen, kuinka päivämäärät lasketaan ja pyöristetään työpäiviin.
Määrittää päivämääräkaavan ajalle, joka kuluu nimikkeen täydentämiseen. Sen avulla lasketaan **Suun. vast.otto pvm** -kentän arvo eteenpäin laskettaessa ja **Tilauspvm**-kentän arvo taaksepäin laskettaessa. Katso [Toimitusajan laskenta](across-how-to-assign-base-calendars.md#lead-time-calculation).

## <a name="lead-time-calculation"></a>Toimitusajan laskenta

Toimittajalle tai sijainnille määritetyt peruskalenterit vaikuttavat siihen, kuinka päivämäärät lasketaan ja pyöristetään työpäiviin. Näin ollen ostotilauksen rivien kaksi päivämääräkenttää lasketaan seuraavasti eri olosuhteissa.

|Laskennan suunta|Toimittajan kalenteri määritetty|Toimittajan kalenteria ei ole määritetty|
|---------------------|-----------------------|---------------------------|
|Eteenpäin|suunniteltu vastaanottopäivämäärä = tilauspäivämäärä + toimittajan toimitusaika (toimittajan kalenterin mukaan ja pyöristettynä edelliseen työpäivään enisn toimittajan kalenterissa ja sitten sijainnin kalenterissa)|suunniteltu vastaanottopäivämäärä = tilauspäivämäärä + toimittajan toimitusaika (sijainnin kalenterin mukaan)|
|Taaksepäin|tilauspäivämäärä = suunniteltu vastaanottopäivämäärä - toimittajan toimitusaika (toimittajan kalenterin mukaan ja pyöristettynä edelliseen työpäivään enisn toimittajan kalenterissa ja sitten sijainnin kalenterissa)|tilauspäivämäärä = suunniteltu vastaanottopäivämäärä - toimittajan toimitusaika (sijainnin kalenterin mukaan)|

> [!NOTE]
> Suunniteltuun vastaanotto- ja tilauspäivämäärään vaikuttavan toimitusajan laskennan lisäksi (edellä olevan taulukon mukaisesti) fyysisen varaston käsittelyaika ja toimitusajan varmistus voidaan lisätä seuraavasti laskentakaavoihin, jotka muodostavat **Oletettu vastaanottopvm** -kentän arvon: suunniteltu vastaanottopäivä + toimitusajan varmistus + saapuvan fyysisen varastoinnin käsittelyaika = oletettu vastaanottopäivä.

> [!Important]
> Jos sijainnissa käytettävä kalenteri on hyvin erilainen kuin toimittajien käyttämät kalenterit, on tärkeää määrittää näille toimittajille erityiset kalenterit, joiden avulla toimittajille voidaan laskea parhaat mahdolliset toimitusajat. Lisätietoja toimittajan kalenterien määrittämisestä on kohdassa [Peruskalenterin määrittäminen](across-how-to-assign-base-calendars.md#to-assign-a-base-calendar).

**Toimitusajan laskenta** -kentän sisältö kopioidaan nimikkeen kortista tai varastointiyksikön kortista, jos nimikkeelle on määritelty toimitusaika, tai **Nimikkeen toimittajaluettelo** -sivulla, jos toimitusaika on määritetty toimittajalle.

## <a name="to-customize-a-calendar"></a>Kalenterin räätälöiminen
Päätehtävä peruskalenterin räätälöimisessä yrityksellesi tai yhdelle sen liiketoimintakumppaneista on syöttää kaikki työskentely- ja ei-työskentelypäivätilan muutokset.

Kun esimerkiksi peruskalenterissa on tavallisesti luetteloitu kaikki lauantait ei-työskentelypäiviksi, tietyn sijainnin räätälöidyssä kalenterissa kaikki marras- ja joulukuun lauantait voidaan luetteloida työskentelypäiviksi.

Seuraavassa menettelyssä käytetään esimerkkinä sijainnin tapausta. Huomaa, että tässä vaiheessa sijainnille on jo määritelty peruskalenteri.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.
2. Avaa päivitettävä sijainti ja valitse sitten **Muokattu kalenteri** -kenttä. Huomaa, että kalenteri on valittava **Peruskalenterin koodi** -kentässä.
3. Valitse avautuvassa **Räätälöidyt kalenteritapahtumat** -sivulla **Ylläpidä räätälöityjä kalenterimuutoksia** -toimintoja.
4. Lisää räätälöityjen kalenteritapahtumien rivit **Räätälöity kalenterimuutos** -ikkunassa.

    Kun annat rivin, **Ei työskentely** -valintaruutu on valittuna. Voit poistaa valintaruudun valinnan, jos haluat muuttaa tilan työpäiväksi.

    Voit käyttää **Toistamisjärjestelmä**-kenttää, jos haluat merkitä tietyn päivämäärän tai päivän toistuvaksi vapaapäiväksi. Valittavat vaihtoehdot ovat **Vuosittain toistuva** ja **Viikoittain toistuva**.

    Jos valitset **Vuosittain toistuva** -vaihtoehdon, asianmukainen päivämäärä on syötettävä myös **Pvm**-kenttään. Jos valitset **Viikoittain toistuva** -vaihtoehdon, **Päivä**-kenttään on valittava asianmukainen viikonpäivä. Jos kenttä jätetään tyhjäksi, **Pvm**-kenttä tulee täyttää. **Päivä**-kenttä täytetään automaattisesti. Tämä voi olla hyödyllistä, jos haluat merkitä yksittäisen päivämäärän ei-työskentelypäiväksi tai työskentelypäiväksi.

5. Valitse **OK**-painike.

**Räätälöidyt kalenteritapahtumat** -sivulla päivämäärätapahtumat näkyvät päivitettyinä tekemiesi muutosten mukaisesti.

Huomaat sijaintikortissa, että **Muokattu kalenteri** -kenttään on **Kyllä**, joka ilmaisee, että mukautettu kalenteri on määritetty.

> [!Important]
> Jos tilausrivin **Sijaintikoodi**-kenttää ei täytetä, ohjelma käyttää yrityksesi kalenteria.


Jos tilausrivin **Kuljetusliikkeen koodi** -kenttää ei täytetä, ohjelma käyttää yrityksesi kalenteria.

> [!NOTE]  
> Jos teet muutoksia peruskalenteriin, jossa on räätälöityjä kalenteritapahtumia, ohjelma päivittää automaattisesti kaikki olemassa olevat räätälöidyt kalenterit.

## <a name="to-assign-a-base-calendar"></a>Peruskalenterin määritteleminen:
Seuraavassa menettelyssä käytetään esimerkkinä asiakkaan tapausta (ja toimituspäivämäärien aikatauluttamista myyntitilausriveille).

Peruskalenterit määritetään omalle yritykselle, asiakkaille, toimittajille, sijainneille ja kuljetusliikkeille seuraavasti:  

-   **Yritystiedot**- ja **Asiakas**-korteissa peruskalenteri määritetään  **Toimitus**-pikavälilehdessä.  
-   **Toimittaja**-kortissa peruskalenteri määritetään **Vastaanotto**-pikavälilehdessä.  
-   **Sijainti**-kortissa peruskalenteri määritetään **Fyysinen varasto** -pikavälilehdessä.  
-   **Kuljetusliikkeet**-sivulla oleva peruskalenteri määritetään **Kuljetusliikkeen palvelut** -sivulla.  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.  
2.  Avaa **Asiakkaan** kortti, jolle haluat määrittää peruskalenterin.  
3.  Valitse **Toimitus**-pikavälilehden **Peruskalenterin koodi** -kentässä peruskalenteri, jonka haluat määrittää.  

> [!IMPORTANT]  
>  -   Jos yritykselle ei määritellä peruskalenteria, ohjelma laskee kaikki päivämäärät työskentelypäiviksi.  
> -   Jos tilausriville syötetään tyhjä sijainti, ohjelma laskee kaikki päivämäärät työskentelypäiviksi.  
> -   Toimittajalle tai sijainnille määritetyt peruskalenterit vaikuttavat siihen, kuinka päivämäärät lasketaan ja pyöristetään työpäiviin.

> [!NOTE]  
>  Ennen kuin räätälöityjä kalenteritapahtumia voidaan tehdä, yritykselle tulee ensin määritellä peruskalenteri.  

## <a name="see-also"></a>Katso myös
[Osto](purchasing-manage-purchasing.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Varasto](inventory-manage-inventory.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
