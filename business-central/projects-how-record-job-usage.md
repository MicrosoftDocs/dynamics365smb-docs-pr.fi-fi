---
title: Projektiresurssien ja -nimikkeiden kulutuksen tai käytön tallentaminen
description: Tässä artikkelissa käsitellään projektien nimikkeiden tai resurssien kulutus tai käyttö kirjataan projektinhallinnassa.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
---
# Projektien kulutuksen tai käytön kirjaaminen

**Työkortti**-sivulla voidaan avata **Projektin suunnittelurivit** -sivu, jossa voidaan tarkastella projektin eri osia ja kirjata niiden käyttö. Nämä tiedot päivitetään automaattisesti, kun tietoja muokataan ja siirretään projektien ja projektipäiväkirjojen tai projektilaskujen välillä. Tämä edellyttää, että **Käytä käyttölinkkiä oletusarvoisesti** on otettu käyttöön vaihtopainikkeella **Projektiasetukset**-sivulla. Lisätietoja kohdassa [Projektien määrittäminen](projects-how-setup-jobs.md).  

<!-- Not really sure what this paragraph is saying, or why we start with it. Why do you transfer information between jobs and job journals or job invoices? I get the use of resources and items, but what about G/L account and Text?

On the Jobs Setup page there's an Apply Usage Link by Default toggle. Guessing that's what we're referring to -->

Esimerkiksi **Budjetti**-tyyppisille suunnitteluriveille voidaan syöttää resurssin määrä ja määrittää sitten projektipäiväkirjaan siirrettävä määrä. Jos suunnittelurivin tyyppi on **Laskutettava**, resurssin määrä voidaan syöttää ja sen jälkeen määrittää laskuun siirrettävä määrä. Lisätietoja asiakkaan laskuttamisesta on kohdassa [Projektien laskuttaminen](projects-how-invoice-jobs.md). Vertaamalla alkuperäistä, jäljellä olevaa tai kirjattua määrää voidaan tarkastella nopeasti käyttötietoja. Lisätietoja budjetoitujen arvojen arvioinnista suunnittelun aikana on kohdassa [Projektibudjettien hallinta](projects-how-manage-budgets.md).  

Seuraavaksi käsitellään projektipäiväkirjan todellisten (budjetoitujen) määrien ja kustannusten kirjaamista. Vaihtoehtoisesti voidaan käyttää ostoasiakirjoja projektin ostojen kirjaamiseen. Lisätietoja on kohdassa [Projektin tarvikkeiden hallinta](projects-how-manage-project-supplies.md).

## Käytön kirjaaminen Budjetti-tyypin projektin suunnitteluriville

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2. Valitse projekti ja valitse sitten **Projektin suunnittelurivit** -toiminto. 
3. Valitse projektin suunnittelurivin tyyppi, joka on **Budjetti** tai **Sekä budjetti että laskutettava** ja jolle haluat kirjata käytön.   

    > [!NOTE]
    > Voit myös tallentaa käytön **Laskutettava**-tyypin projektin suunnitteluriville. Yleensä näitä rivejä käytetään laskujen luomiseen, mutta tiedot voidaan siirtää myös päiväkirjaan. Lisätietoja on kohdassa [Projektin laskuttaminen](projects-how-invoice-jobs.md) <!--However, when you do that, a job planning line of type **Budget** is created to match the billable line. For more information, see [Manage Job Budgets](projects-how-manage-budgets.md).-->

4. Syötä **Päiväkirjaan siirrettävä määrä** -kenttään siirrettävä määrä. Oletusmäärä on **Määrä**-kenttään syöttämäsi arvo.

    **Jäljellä oleva määrä** -kentässä näyttää määrän, jota on vielä suorittamatta projektissa ja siirrettävä päiväkirjaan. <!--Should we mention that this field is not shown by default, and that if they want to use it they must add it?--> 
5. Valitse **Luo projektipäiväkirjan rivit** -toiminto.

    > [!TIP]
    > Jos tähän projektiin on tarkoitus lisätä enemmän projektiin suunnittelurivejä, tee tämä määritys vasta, kun olet lisännyt kaikki projektin suunnittelurivit.
6. Täytä **Projektin siirron projektisuunnittelurivi** -sivulla kenttiä tarpeen mukaan ja valitse sitten **OK**-painike. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Valitse **Avaa projektipäiväkirja** -toiminto.  
8. Valitse **Projektipäiväkirja**-sivulla asianmukainen rivi ja valitse sitten **Kirjaa**-toiminto.
9. Tarkista **Projektin suunnittelurivit** -sivulla kirjattu käyttö **Määrä**-, **Jäljellä oleva määrä**- ja **Päiväkirjaan siirrettävä määrä** -kentän avulla.  
10. Kirjaa lisäkäyttö toistamalla vaiheet 3–8.  

## Luo projektipäiväkirjan rivit manuaalisesti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Valitse **Erän nimi** -kentässä asianmukaisen projektipäiväkirjan erä.  
3. Kirjoita uudelle riville asiakirjan numero, projektinumero, projektin tehtävän numero, tyyppi ja kulutettavan tyypin määrä.  
4. Kun projektipäiväkirjan rivit ovat valmiit, valitse **Kirjaa**-toiminto.  

## Projektin käytön arvioiden tarkasteleminen ja päivitysten kirjaaminen

Voit katsella projektin käyttöä projektin valmistumiseen asti yhden vaiheen avulla. Tämä tapahtuu käyttämällä **Laske projektin jäljellä oleva käyttö** -eräajoa kaikissa tehtävissä projektin alusta loppuun.  

Näin voit seurata ja vertailla alkuperäisiä arvioita todellisiin tuloksiin. Voit myös tehdä tarvittaessa muutoksia tai uusia tapahtumia. Olet esimerkiksi saattanut arvioida projektin kestoksi 10 tuntia, mutta aikaa on kulunut jo 15 tuntia. Voit lisätä viisi tuntia aiemmin luotuun päiväkirjariviin tai luoda uuden rivin, jolla nämä viisi tuntia raportoidaan ylityönä, joka on toinen työtyyppi. Sitten lasketaan oikeat kustannukset ja hinta, jotka voidaan kirjata päiväkirjaan.  

> [!NOTE]  
> Nimiketapahtumat luovat nimiketapahtumia ja vähentävät varastomäärää. **Kirjaa varaston kustannus KP:oon** -eräajo siirtää kustannuksen varastosta pääkirjanpitoon. Resurssitapahtumat luovat resurssitapahtumia.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Valitse asianmukaisen projektin päiväkirja ja valitse sitten **Laske jäljellä oleva käyttö** -toiminto.  
3. Anna **Laske projektin jäljellä oleva käyttö** -sivulla päiväkirjaan lisättävä asiakirjan numero ja kirjauspäivämäärä. Valitse sitten **OK**-painike.  
4. Päivitä tarvittavat muutokset päiväkirjaan.  
5. Valitse **Kirjaa**.

## Luo varaston ja fyysisen varaston poiminta-asiakirjat projektille

Jos haluat luoda varaston ja fyysisen varaston poiminta-asiakirjat projekteille, järjestelmänvalvojan on määritettävä **Ominaisuuspäivitys: Ota käyttöön varaston ja fyysisen varaston poiminnat projekteista** -kohta käyttöön **Ominaisuuksien hallinta** -sivulla.

Toiminto lisää **Luo varastopoiminta**- ja **Luo fyysisen varaston poiminta** -toiminnot **projektikorttiin**. Jos haluat luoda tai rekisteröidä poiminta-asiakirjan, käytä **Hyllytys-/poiminta-/siirtorivit**- tai **Rekisteröidyt poimintarivit** -toimintoa. Lisätietoja on kohdassa [Tuotanto-, kokoonpano- ja projektityönkulut](design-details-internal-warehouse-flows.md).

Voit käyttää toimintoja seuraavien ehtojen perusteella:

* Projektin **tila** on **Avoin**.
* Projektin suunnittelurivin **rivityyppi** on **Budjetti** tai **Sekä budjetti että laskutettava**.
* Projektin suunnittelurivin **tyyppi** on **Nimike**.
* **Vaadi poiminta** -kohta on otettu käyttöön liittyvässä sijainnissa.
* **Ohjattu hyllytys ja poiminta** on poistettu käytöstä.

> [!NOTE] 
> Vaikka asetuksen nimi on **Vaadi poiminta**, voit silti kirjata kulutuksen suoraan projektin päiväkirjariviltä sijainnissa. Jos sijainti on asetettu vaatimaan poimintaprosessia mutta ei toimitusprosessia, sinun tulee käyttää **Varastopoiminta**-sivua poiminnan tietojen järjestämisessä ja tulostamisessa. Voit käyttää sivua myös poiminnan tuloksen syöttämisessä ja kirjaamisessa. Tämä kirjaa nimikkeiden kulutuksen. 
> 
> Jos sijainti on määritetty edellyttämään sekä poiminta- että toimituskäsittelyä eli olet valinnut sekä **Vaadi poiminta**- ja **Vaadi toimitus** -kohdan **Sijaintikortti**-sivulla, voit käsitellä poiminnan **F. varaston poiminta** -sivulla. Fyysisen varaston poiminnat ovat samanlaisia kuin varaston poiminnat. Erona on, että poiminnan tietojen kirjaamisen sijaan poiminta rekisteröidään. Tämä rekisteröinti ei kirjaa kulutusta, vaan se vain määrittää nimikkeet saataville kirjaamista varten. Varastopäällikkönä voit järjestää poimintatiedot poimintatyökirjan avulla ennen yksittäisten fyysisen varastoinnin poimintaohjeiden luontia

## Projektitapahtuman suunnittelurivien tarkasteleminen

Kun olet kirjannut projektipäiväkirjan rivit, näkyvissä ovat suunnittelurivit, jotka liittyvät kirjattuihin projektitapahtumiin.

> [!NOTE]  
> Tämä edellyttää sitä, että projektin **Käytä käyttölinkkiä** -valintaruutu on valittuna. Lisätietoja on kohdassa [Projektien määrittäminen](projects-how-setup-jobs.md).  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Valitse asianmukaisen projektin päiväkirja ja valitse sitten **Tapahtumakirjaukset**-toiminto.  
3. Valitse **Projektitapahtumat**-sivulla **Näytä linkitetyt projektin suunnittelurivit** -toiminto.

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/post-job-usage-sales/)

## Katso myös

[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
