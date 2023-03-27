---
title: Aloita asettelujen luominen
description: 'Voit tutustua asettelujen luomiseen ja raportin ulkoasun muokkaamiseen, kun sitä tarkastellaan, tulostetaan tai tallennetaan.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/23/2022
ms.author: jswymer
---
# Aloita raporttiasettelujen luominen

Business Centralin mukana tulee monia valmiita asetteluita, joita voit käyttää raporteissa. Muita asetteluita on saatettu lisätä osana muita laajennuksia. On myös mahdollista luoda omia raportteja joko tyhjästä tai olemassa olevan asettelun perusteella.

> [!IMPORTANT]
> Voit myös käyttää raporttiasetteluja lisätäksesi sisältöä sähköpostiviesteihin. Raporttiasettelut voivat esimerkiksi säästää aikaa ja auttaa yhdenmukaisuuden varmistamisessa siten, että samaa sisältöä käytetään uudelleen, kun viestit asiakkaidesi kanssa. Jotta voit käyttää mukautettuja raporttiasetteluja sähköpostissa, niiden tiedostotyyppinä on oltava Word. Et voi käyttää RDLC-tiedostotyyppiä. Lisätietoja: [Uudelleenkäytettävien sähköpostitekstien ja -asettelujen määrittäminen](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## Yleiskuvaus

Kun käsittelet raportin asetteluja, voit ajatella asettelua tiedostona, joka on tuotu ja liitetty raporttiin. Asettelun tyypistä riippumatta asettelujen hallinta on periaatteessa samanlaista kuin Business Centralin asettelut. Tavallisesti käsittely tehdään **Raporttiasettelut**-sivulla. Pääasiallinen ero on asettelun suunnittelussa, joka tehdään käyttämällä asettelusovellusta, jolle asettelu on luotu, kuten Wordia, Exceliä tai SQL Server Report Builderia.

Tätä käsitettä silmällä pitäen. Raportin asettelun määrittämiseen liittyy periaatteessa kolme tai neljä tehtävää:

1. Määritä asettelun tyyppi.
2. Vie aiemmin luodun asettelun kopio käytettäväksi lähtökohtana.
3. Tee muutokset asettelutiedostoon sopivassa sovelluksessa.
4. Lisää uusi asettelutiedosto raporttiin.

> [!IMPORTANT]
> Et voi muokata tai korvata laajennuksen asettelua, joka on peräisin laajennuksesta. Vain käyttäjän määrittämiä asetteluja voidaan muokata tai korvata. **Raporttiasettelut**-sivulla voit määrittää, onko asettelu laajennusasettelu vai käyttäjän määrittämä asettelu, tarkastelemalla **Laajennus**-saraketta. Laajennuksen asettelussa näkyy tietoja sarakkeen lähdelaajennuksesta. **Laajennus**-sarake on tyhjä käyttäjän määrittämän asettelun osalta.
>
> Lisätietoja laajennusasettelujen ja käyttäjän määrittämien asettelujen välisistä eroista on kohdassa [Asettelun lähde](ui-manage-report-layouts.md#layout-sources).

## Aloitus

Riippuen siitä, mikä tilanne on, todelliset tehtävät vaihtelevat. Seuraavan taulukon avulla pääset alkuun.

|Mitä haluat tehdä?|Katso...|
|-----------------------|------|
|Selvitä, mikä on paras asettelutyyppi käytettäväksi omassa tilanteessani|[Haluamasi asettelun tyypin valitseminen](#decide)|
|Luo uusi asettelu raporttia varten, joka perustuu aiemmin luotuun asetteluun, säilyttäen nykyisen asettelun sellaisena kuin se on.|[Uuden asettelun luominen](#create)|
|Muutosten tekeminen raportissa käytettyyn aiemmin luotuun asetteluun|[Asettelun muokkaaminen](#modify)|
|Asettelutiedostosta on uusi versio raporttia varten. Haluan korvata aiemmin luodun asettelutiedoston.|[Korvaa asettelu](#replace)|
|Raportin käytössä olevan asettelun vaihtaminen toiseen asetteluun|[Raportin käyttämän asettelun määrittäminen](ui-set-report-layout.md)|
|Asettelun nimen ja kuvauksen muuttaminen|[Asettelun nimeäminen uudelleen](#rename)|

## <a name="decide"></a>Haluamasi asettelun tyypin valitseminen

Ensimmäinen asia, kun luodaan asettelua, on päättää, minkä [asettelun tyypin](ui-manage-report-layouts.md#layout-types) haluat. Voit valita joko Word, Excel tai RDLC. Asettelun tyyppi määräytyy sen mukaan, miltä haluat luodun raportin näyttävän. Lisäksi se riippuu siitä, miten hyvin tunnet sovellusohjelmiston asettelujen luomiseen, kuten Wordin, Excelin ja SQL Server Report Builderin.

<!--
* The process for setting up Word, Excel, and RDLC layouts on reports is the same. The main difference is in the way you modify the layouts. Excel and Word layouts are typically easier to create and modify than RDLC layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.-->

* Excel-asettelujen luominen ja muokkaaminen on yleensä helpointa, koska tietojen yhteenveto-, grafiikka- ja muotoiluominaisuudet ovat tavallisia Excelin ominaisuuksia.

* Kaikilla raporteilla ja asiakirjoilla ei ole tietojoukkoa, joka on optimoitu Excel-asettelun käyttämistä varten. Esimerkiksi koosteet ja monimutkaiset laskennat toimivat parhaiten RDLC- tai Word-asetteluilla. Sama pätee asiakirjoihin.

* Jos olet tekemässä vain tyylin muutoksia, kuten fontin tyypin, koon ja värin muutoksia, myös Wordin asettelu on hyvä valinta.

* Tietokenttien lisääminen Wordissa tai RDLC:ssä tai tietokenttien järjestäminen uudelleen on kehittyneempää kuin Excelissä.

* Word- ja RDLC-asettelujen käyttäminen on hyvää raporteissa, jotka tulostetaan lopulta.  

* Word- ja RDLC-asetteluiden yleiset rakenteet ovat samanlaisia. Silti, jokaisella tyypillä on tiettyjä suunnittelu ominaisuuksia, jotka vaikuttavat siihen miltä luodut raportit näyttävät [!INCLUDE[prod_short](includes/prod_short.md)]ssa. Sama raportti saattaa näyttää erilaiselta RDLC-asetteluun verrattuna Word-asettelua käytettäessä.

## <a name="create"></a>Uuden asettelun luominen

Uuden asettelun voi luoda olemassa olevasta asettelusta kahdella tavalla. Yksi tapa on tallentaa olemassa oleva asettelu kopioon. Toinen tapa on viedä olemassa oleva asettelu.

## [Kopiointi](#tab/copy)

Kopioiminen on nopea tapa luoda uusi asettelu, joka on sama kuin aiemmin luotu asettelu. Kun olet tehnyt kopion, voit tehdä muutokset viemällä asettelun. 

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Valitse asettelu, josta haluat kopion, uutta asettelua varten, ja valitse sitten **Muokkaa tietoja** -toiminto.

    Jos valitsit laajennuksen asettelun, ohjelma kysyy, haluatko muokata kopiota. Jatka valitsemalla **Kyllä**.

    > [!TIP]
    > Voit etsiä asettelua käyttämällä **Haku**-ruutua, **Suodatin**-ruutua ja sarakkeiden lajittelua.
3. **Asettelun nimen** muuttaminen.
4. Vaihda **Tallenna muutokset kopioon** -asetus asentoon **Käytössä** ja valitse sitten **OK**

   Uusi asettelu näkyy **Raporttiasettelut**-sivulla.
5. Jos haluat tehdä muutoksia uuteen asetteluun, lisätietoja on kohdassa [Olemassa olevan asettelun muokkaaminen](#modify).

### [Vieminen/tuominen](#tab/export)

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Valitse asettelu, josta haluat kopion, uutta asettelua varten, ja valitse sitten **Vie asettelu** -toiminto.

   Asettelutiedosto ladataan laitteellesi. 

    > [!TIP]
    > Voit etsiä asettelua käyttämällä **Haku**-ruutua, **Suodatin**-ruutua ja sarakkeiden lajittelua.

3. Avaa asettelutiedosto haluamassasi sovelluksessa, kuten Wordissa (.docx-tiedosto) tai Excelissä (.xlsx-tiedosto).

   Lisätietoja on kohdassa

   * [Wordin asettelujen käyttö](ui-how-add-fields-word-report-layout.md)
   * [Excel-asettelujen käyttö](ui-excel-report-layouts.md)
   * [RDLC-asettelujen käyttö](ui-rdlc-report-layouts.md)

   Tee muutokset tiedostoon ja tallenna se.

4. Taas **Raporttiasettelut**-kohdassa valitse **Uusi asettelu** -toiminto.
5. Täytä kentät seuraavasti:

   |Kenttä|Kuvaus|Pakollinen|
   |-----|-----------|---------|
   |Raportin tunnus|Määritetty raportille määritettyyn tunnukseen|kyllä|
   |Asettelun nimi| Kirjoita asettelulle lyhyt kuvausnimi, jotta tunnistat sen helposti.|kyllä|
   |Kuvaus| Kirjoita tarkempia tietoja asettelusta. |ei|
   |Muotoiluasetukset|Määritä tämä kenttä vastaamaan asettelun tyyppiä, kuten Word, Excel tai RDLC.|kyllä|

6. Valitse **OK** > **Valitse**, jos haluat avata Resurssienhallinnan laitteessasi.
7. Etsi ja valitse Excel-tiedosto ja valitse sitten **Avaa**.

   Valitsemasi tiedosto ladataan asetteluun, ja palaat **Raporttiasettelut**-sivulle.

Jos haluat nähdä, miltä raportti näyttää uudessa asettelussa, valitse asettelu luettelosta ja valitse sitten **Suorita raportti**.

---

## <a name="modify"></a>Asettelun muokkaaminen

Muokkaa aiemmin luotua käyttäjän määrittämää asettelua noudattamalla seuraavia ohjeita.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Valitse muokattava asettelu ja valitse sitten **Vie asettelu** -toiminto.

   Asettelutiedosto ladataan laitteellesi. 

   > [!TIP]
   > Voit etsiä asettelua käyttämällä **Haku**-ruutua, **Suodatin**-ruutua ja sarakkeiden lajittelua.

3. Avaa asettelutiedosto haluamassasi sovelluksessa, kuten Wordissa (.docx-tiedosto) tai Excelissä (.xlsx-tiedosto).

   Lisätietoja on kohdassa

   * [Wordin asettelujen käyttö](ui-how-add-fields-word-report-layout.md)
   * [Excel-asettelujen käyttö](ui-excel-report-layouts.md)
   * [RDLC-asettelujen käyttö](ui-rdlc-report-layouts.md)

   Tee muutokset tiedostoon ja tallenna se.

4. **Raportin asettelut** -sivulla valitse aiemmin luotu asettelu ja valitse sitten **Korvaa asettelu** -toiminto.
5. Valitse **OK** > **Valitse**, jos haluat avata Resurssienhallinnan laitteessasi.
6. Etsi ja valitse Excel-tiedosto ja valitse sitten **Avaa**.

   Valitsemasi tiedosto ladataan asetteluun, ja palaat **Raporttiasettelut**-sivulle.
7. Jos haluat nähdä, miltä raportti näyttää uudessa asettelussa, valitse asettelu luettelosta ja valitse sitten **Suorita raportti**.

## <a name="replace"></a>Korvaa asettelu

Voit korvata aiemmin luodun käyttäjän määrittämän asettelutiedoston uudella tiedostolla noudattamalla seuraavia ohjeita.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Valitse olemassa oleva asettelu ja valitse sitten **Korvaa asettelu** -toiminto.
3. Valitse **OK** > **Valitse**, jos haluat avata Resurssienhallinnan laitteessasi.
4. Etsi ja valitse Excel-tiedosto ja valitse sitten **Avaa**.

   Valitsemasi tiedosto ladataan asetteluun, ja palaat **Raporttiasettelut**-sivulle.
5. Jos haluat nähdä, miltä raportti näyttää uudessa asettelussa, valitse asettelu luettelosta ja valitse sitten **Suorita raportti**.

## <a name="rename"></a>Asettelun nimeäminen uudelleen

Noudata seuraavia ohjeita, jos haluat muuttaa käyttäjän määrittämän asettelun nimeä ja kuvausta.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Valitse uudelleen nimettävä asettelu ja valitse sitten **Muokkaa tietoja** -toiminto.

    > [!TIP]
    > Voit etsiä asettelua käyttämällä **Haku**-ruutua, **Suodatin**-ruutua ja sarakkeiden lajittelua.
3. Muuta **asettelun nimi** ja valitse sitten **OK**.

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/change-documents-dynamics-365-business-central/index)

## Katso myös

[Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
[Wordin asettelujen käyttö](ui-how-add-fields-word-report-layout.md)  
[Excel-asettelujen käyttö](ui-excel-report-layouts.md)  
[Raporttien, eräajojen ja XMLportien käsitteleminen](ui-work-report.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
