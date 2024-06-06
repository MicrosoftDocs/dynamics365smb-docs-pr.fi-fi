---
title: Määritä yrityksen konsolidointi
description: 'Tietoja siitä, miten voit määrittää, miten eri yritysten tiedot Business Centralissa raportoidaan konsolidointiyritykseen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 03/14/2024
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# <a name="set-up-company-consolidation"></a>Yrityksen konsolidoinnin määrittäminen

Ennen kuin voit konsolidoida kahden tai useamman yrityksen (tytäryritysten) pääkirjanpidon tapahtumat konsolidoituun yritykseen, sinun täytyy valmistella tilikartat ja konsolidointiyritys.  

Yritysten monimutkaisuus määrittää, kumpaa tapaa käytetään konsolidoinnin määrittämiseen:

* Jos et tarvitse lisäasetuksia, kuten vain osittain omistamasi yrityksen sisällyttämistä, voit määrittää konsolidoinnin nopeasti käyttämällä **Yrityksen konsolidointi** -määritystä. Opas auttaa suorittamaan perusvaiheet.
* Jos tarvitset lisäasetuksia, voit määrittää konsolidoidun yrityksen ja liiketoimintayksiköt itse.
  * Määritä, mitkä kunkin liiketoimintayksikön pääkirjanpidon tilit sisällytetään konsolidointiin, sekä muuntomenetelmän määrittäminen kullekin tilille.
  * Liiketoimintayksikön kortin määrittäminen kullekin konsolidointiin sisällytettävälle yritykselle konsolidoidussa yrityksessä. Liiketoimintayksikön kortin tietoihin kuuluvat esimerkiksi liiketoimintayksikön tilikauden päivämäärät, kunkin konsolidointiin sisällytettävän tilin prosenttiosuus, joka tulee sisällyttää konsolidointiin.

## <a name="simple-consolidation-setup"></a>Yksinkertaiset konsolidoinnin asetukset

Jos kyse on suoraviivaisesta konsolidoinnista, koska esimerkiksi omistat kokonaan konsolidoitavat liiketoimintayksiköt, **Yrityksen konsolidointi** -määritys auttaa seuraavissa vaiheissa:

* Luo uusi konsolidoitu yritys tai konsolidoi aiemmin luomasi yritys. Yrityksessä ei saa olla tapahtumia.
* Esikatsele tulokset. [!INCLUDE[prod_short](includes/prod_short.md)] varmistaa, että päätiedot ja tapahtumat voidaan siirtää konsolidoituun yritykseen.

Käytä asetusten ohjattua määritystä seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asetusten ohjattu määritys** ja valitse sitten vastaava linkki.
2. Valitse **Käsittele konsolidoinnit** ja tee vaiheet yrityksen konsolidoinnin ohjatun määrityksen mukaisesti.

## <a name="advanced-consolidation-setup"></a>Konsolidoinnin lisäasetukset

Jos konsolidoinnissa on käytettävä lisäasetuksia, voit määrittää konsolidoinnin manuaalisesti. Sinulla voi esimerkiksi olla yrityksiä, jotka omistat osittain, tai et ehkä halua sisällyttää tiettyjä yrityksiä.  

### <a name="set-up-the-consolidated-company"></a>Määritä konsolidoitu yritys

Ensin tulee määrittää konsolidoitu yritys. Konsolidoitu yritys määritetään samalla tavalla kuin muutkin yritykset. Lisätietoja yrityksen perustamisesta on kohdassa [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).  

Seuraavassa luettelossa havainnollistetaan konsolidoidun yrityksen keskeiset piirteet.

1. Tilikartan määrittäminen.

    Lisätietoja tilikartan määrittämisestä on kohdassa [Tilikartan määrittäminen tai muuttaminen](finance-setup-chart-accounts.md).  

    Tilikartat voivat olla identtisiä liiketoimintayksikön ja konsolidoidun yrityksen välillä, tai konsolidoidulla yrityksellä voi olla eri tilikartta. Jos liiketoimintayksikön tilikartta poikkeaa konsolidoidun yrityksen tilikartasta, sinun täytyy määrittää tilit liiketoimintayksikön tileihin Lisätietoja on [Pääkirjanpitotilin valmisteleminen konsolidointia varten](#glacc) -osassa.

2. Lisää liiketoimintayksiköt.

    Kun haluat konsolidoida useamman yrityksen tietoja, sinun täytyy määrittää tytäryhtiöt liiketoimintayksiköiksi ja määrittää, kuinka paljon niiden saldoista sisällytetään. Lisätietoja liiketoimintayksiköistä on [Lisää liiketoimintayksiköitä](#busunit) -kohdassa.

3. Määritä tarvittaessa vaihtokurssit.

    Määritä vaihtokurssit, jos haluat konsolidoida tietoja eri valuuttoja käyttäville liiketoimintayksiköille. Ohjelman käyttämät kolme vaihtokurssia ovat **Keskikurssi (manuaalinen)**, **Loppukurssi** ja **Viimeinen loppukurssi**. Lisätietoja vaihtokursseista on [Määritä valuutan vaihtokurssit konsolidoiduissa yrityksissä](#exchrates) -osassa.

4. Voit konsolidoida dimensiotietoja samoin kuin KP-tilejäkin.

    Jos haluat lisätietoja, siirry [Dimensioiden sisällyttäminen tai jättäminen pois](#dim) -kohtaan.

### <a name="add-business-units"></a><a name="busunit"></a>Lisää liiketoimintayksiköt

Määritä konsolidoidussa yrityksessä jokainen yritys, jonka tietoja haluat konsolidoida liiketoimintayksikkönä. Ennen konsolidoinnin suorittamista ja konsolidointiraportin luontia on hyvä tarkistaa kunkin liiketoimintayksikön finanssitiedot.

Liiketoimintayksikön määrittämisessä on suuri osa sen määrittämistä, miten yksikkö jakaa taloustietonsa konsolidoidun yrityksen kanssa. Saatavana on manuaalisia ja automaattisia vaihtoehtoja:

* Manuaalisen prosessin käyttämiseksi [!INCLUDE [prod_short](includes/prod_short.md)] onlinelle ja paikalliselle versiolle voit viedä .xml-tiedoston, joka sisältää yksikön pääkirjanpidon tapahtumat. Tuo sitten tiedosto konsolidoidussa yrityksessä.
* Voit automatisoida tietojen vaihdon käyttämällä [!INCLUDE [prod_short](includes/prod_short.md)] onlinessa ohjelmointirajapintaan, jonka [!INCLUDE [prod_short](includes/prod_short.md)] tarjoaa tietojen jakamiseksi ympäristöissä. Jos yrityksesi ovat samassa ympäristössä, voit käyttää **Tietokanta**-vaihtoehtoa.

> [!NOTE]
> Ohjelmointirajapinnan vaihtoehdon avulla voit myös jakaa pääkirjanpidon tapahtumia muista [!INCLUDE [prod_short](includes/prod_short.md)] -ympäristöistä. Jotta ohjelmointirajapinnan vaihtoehtoa voi käyttää, konsolidoinnin määrittävällä käyttäjällä on oltava kp-tapahtumien käyttöoikeus. Voit käyttää esimerkiksi D365 Perus- ja D365-luku-käyttöoikeuksien joukkoa.

#### <a name="set-up-business-unit-currencies"></a>Liiketoimintayksikön valuuttojen määrittäminen

Kun ulkomaanvaluuttaa käyttävien liiketoimintayksiköiden konsolidointi suoritetaan, huomiota on kiinnitettävä etenkin prosessien eri osien käyttämiin vaihtokursseihin ja varsinkin silloin, kun konsolidointi suoritetaan uudelleen. Sitä varten voi käyttää **Liiketoimintayksikön valuuttojen määrittäminen** -sivua, sillä se helpottaa kurssien seuraamista.

**Liiketoimintayksikön valuuttojen määrittäminen** -sivulla viimeisimmät keskivaihtokurssit, loppukurssit ja viimeisimmät loppuvaihtokurssit. Vaihtokurssit voidaan hakea valuutan vaihtokurssitaulukossa, mikä helpottaa kurssien tarkistamista. Nykyisen ajon vaihtokurssit voidaan muuttaa syöttämällä arvot tai kopioimalla ne aiemmista ajoista. Kurssit kopioidaan valitsemalla **Liiketoimintayksikön valuuttojen määrittäminen**. Tämä sivu tärkeä etenkin silloin, kun halutaan suorittaa edellinen konsolisointi uudelleen, jolloin on käytettävä aiempaa loppukurssia. Se on välttämätöntä, jotta taseen nimikkeiden uudelleenarvostus tehdään oikein. **Valitse aiemmista konsolidoinneista** -sivu on kätevä myös silloin, jos halutaan vain tarkastella käytettyjä kursseja esimerkiksi vianmäärityksen aikana. Tämä sivu suodatettu näyttämään ajo, jotka sisältyvät valittuun liiketoimintayksikköön.

**Suorita konsolidointi** -eräajo suoritetaan **Liiketoimintayksiköt**-luettelosivulta. **Määritä liiketoimintayksikön valuutat** -sivu löydetään myös valitsemalla **Vaihtokurssit**-toiminto.

> [!NOTE]
> Keskikurssin, loppukurssin ja viimeisen loppukurssin vaihtokurssin määrityssivut, jotka ovat tällä hetkellä käytettävissä **Liiketoimintayksikkö**-kortissa, vanhentuvat tulevassa versiossa. Näitä kursseja voidaan kuitenkin edelleen ylläpitää, jos liiketoimintayksiköitä on tuotu tiedostojen kautta.

#### <a name="create-a-business-unit"></a>Liiketoimintayksikön luominen

1. Kirjaudu konsolidoituun yritykseen.
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liiketoimintayksiköt** ja valitse sitten vastaava linkki.  
3. Valitse **Uusi** ja täytä sitten pakolliset kentät **Yleiset**- ja **KP-tilit**-pikavälilehdissä. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Kun täytät **Aloituspvm**- ja **Lopetuspvm** -kentät, varmista, että noudata kenttiä, varmista, että noudatat liiketoimintayksikön eikä emoyrityksen tilikausien GAAP-sääntöjä.
4. Määritä **Tietojen tuominen** -pikavälilehden **Tietojen oletusarvoinen tuonti** -kentässä, miten jaat pääkirjanpidon tapahtumat konsolidoidun yrityksen kanssa:

   * Jos haluat jakaa tietoja samassa ympäristössä olevien yritysten välillä, valitse **Tietokanta**.
   * Voit jakaa tietoja yritysten välillä eri ympäristöissä valitsemalla **Ohjelmointirajapinta** ja täyttämällä sitten **APIn päätepiste** -kentän.
        
        Saat päätepisteen URL-osoitteen avaamalla liiketoimintayksikköyrityksen kohteessa [!INCLUDE [prod_short](includes/prod_short.md)] **Liiketoimintayksikön kortti** -sivun ja valitsemalla **Asetukset**-toiminnon. 
   * Voit viedä .xml-tiedoston ja jakaa sen manuaalisesti valitsemalla **Tiedostomuoto**.

### <a name="prepare-general-ledger-accounts-for-consolidation"></a><a name="glacc"></a>Valmistele kirjanpitotilit konsolidointia varten

Konsolidoitavan yrityksen tilikartan on määritettävä konsolidoinnissa käytettävät tilit. Kunkin yrityksen kullekin KP-tilille on määritettävä konsolidoidun yrityksen KP-tili, jolle saldo siirretään. Yhdistämismäärityksen avulla voit konsolidoida yrityksiä, joilla on eri tilikartat.

Jos liiketoimintayksikön tilikartta poikkeaa konsolidoidun yrityksen tilikartasta, kirjanpitotilit on valmisteltava konsolidointia varten. Voit määrittää tilit, joihin debet- ja kreditsummat kirjataan, ja menetelmän, jolla valuutat muunnetaan konsolidoidussa yrityksessä.

1. Valitse kunkin liiketoimintayksikön [!INCLUDE [prod_short](includes/prod_short.md)]issa ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten vastaava linkki.  
2. Avaa tilin kortti ja täytä **Konsolidointi**-pikavälilehden kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Jos et täytä **Konsol. debet-tili** ja **Konsol. kredit-tili** -kenttiä, [!INCLUDE [prod_short](includes/prod_short.md)] olettaa, että ne on linkitetty samoille tileille konsolidoidussa yrityksessä.

> [!TIP]
> Saattaa olla tilanteita, joissa et halua sisällyttää tiliä konsolidointiin. Jos esimerkiksi haluat, että konsolidointiyritys ottaa huomioon vain tytäryritysten taseet. Jos haluat jättää tilin konsolidoinnin ulkopuolelle, ota tilin **Sulje pois konsolidoinnista** -vaihtoehto käyttöön.

### <a name="specify-exchange-rates-for-consolidations"></a><a name="exchrates"></a>Määritä valuutan vaihtokurssit konsolidoiduissa yrityksissä

Jos liiketoimintayksikön käyttämä valuutta ei ole sama kuin konsolidoidun yrityksen käyttämä valuutta, kullekin tilille on määritettävä vaihtokurssimenetelmä ennen konsolidointia. Kunkin tilin **Konsolid. muuntomenetelmä** -kentän sisältö määrittää vaihtokurssin. Määritä konsolidoidussa yhtiössä kunkin liiketoimintayksikön **Valuutan vaihtok.taulu** -kentässä, käytetäänkö konsolidoinnissa liiketoimintayksikön vai konsolidoidun yrityksen vaihtokursseja. Jos käytät konsolidoidun yrityksen vaihtokursseja, voit muuttaa liiketoimintayksikön vaihtokursseja. Jos liiketoimintayksikön kortin **Valuutan vaihtok.taulu** -kentässä on arvo **Paikallinen**, voit muuttaa vaihtokurssia liiketoimintayksikön kortista. Vaihtokurssit kopioidaan **Valuutan vaihtokurssi** -taulukosta, mutta voit muuttaa niitä ennen konsolidointia.

Seuraavassa taulukossa käsitellään tileillä käytettäviä vaihtokurssimenetelmiä.

|Vaihtokurssi | Tyypillinen käyttö |
|---|---|
|Keskikurssi (manuaalinen) | Konsolidoitavan jakson keskikurssi lasketaan manuaalisesti. Laske keskikurssi joko aritmeettisena keskiarvona tai parhaana arvioina ja määritä kunkin liiketoimintayksikön tulos. Käytä tuloslaskelmatileillä.|
|Loppukurssi | Käytetään tasetileillä.|
|Viimeinen loppukurssi | Valuuttamarkkinoiden kurssi päivämääränä, jona tasetta tai tuloslaskelmaa valmistellaan. Käyttäjä antaa tämän kurssin kullekin liiketoimintayksikölle. Käytä tasetileillä.|
|Historiallinen kurssi | Vaihtokurssi tapahtuman suoritusajankohtana.|
|Yhdistelmäkurssi | Kuluvan jakson summat muunnetaan keskikurssin mukaan ja lisätään aiemmin kirjattuun saldoon konsolidoidussa yrityksessä. Tätä menetelmää käytetään tavallisesti jakamattoman voiton tileihin. Nämä tilit sisältävät summia eri jaksoilta, joten ne sisältävät eri vaihtokursseja sisältäviä summia.|
|Pääomakurssi | Tämä vaihtoehto muistuttaa **yhdistelmäkurssia**. Erot kirjataan erillisille kirjanpitotileille.|

Liiketoimintayksikön vaihtokurssit määritetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liiketoimintayksiköt** ja valitse sitten vastaava linkki.  
2. Valitse ensin **Liiketoimintayksiköiden luettelo** -sivulla liiketoimintayksikkö ja sitten **Vaihtokurssit**-toiminto.  
3. Täytä tarvittavat kentät **Määritä liiketoimintayksikön valuutat** -sivulla. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="include-or-exclude-dimensions"></a><a name="dim"></a>Dimensioiden sisällyttäminen tai jättäminen pois

Voit konsolidoida dimensiotietoja samoin kuin KP-tilejäkin.

* Määrittele dimensioissa **Konsolidointikoodi** -kenttä tai jätä se tyhjäksi.
  * Jos haluat sulkea dimension pois konsolidoinnista, jätä **Dimension konsolidointikoodi** -kenttä tyhjäksi äläkä valitse dimensioita konsolidointifunktioiden tai -raporttien **Kopioi dimensiot** -kentissä.
  * Jos haluat sisällyttää dimensiotiedot konsolidointiin, jätä **Konsolidointikoodi**-kenttä tyhjäksi. Konsolidointi kuitenkin onnistuu vain, jos liiketoimintayksikön dimensiotiedot ovat täsmälleen samat kuin konsolidoidulla yrityksellä.
  * Konsolidoi dimension arvokoodi liiketoimintayksikössä eri dimension arvokoodilla konsolidoidussa yrityksessä täyttämällä dimensioiden **Konsolidointikoodi**-kenttä.  
* Lisää dimensiot kirjanpitotileihin.

### <a name="exclude-a-company-from-consolidation"></a><a name="exclude"></a>Jätä yritys konsolidoinnin ulkopuolelle

Jos et halua sisällyttää liiketoimintayksikköä konsolidointiin, voit jättää sen pois. Se onnistuu siirtymällä liiketoimintayksikön korttiin ja poistamalla **Konsolidoi**-valintaruudun valinta.

### <a name="include-a-partially-owned-company-in-consolidation"></a><a name="include"></a>Sisällytä osittain omistettu yritys konsolidointiin

Jos omistat osan yrityksestä, voit sisällyttää kustakin tapahtumasta sen prosenttiosuuden, joka vastaa omistamaasi osuutta. Jos esimerkiksi omistat yrityksestä 70 prosenttia, konsolidointiin sisältyy lasku 70 dollaria 100 dollarin laskusta. Voit määrittää omistusosuuden yrityksestä siirtymällä liiketoimintayksikön korttiin ja antamalla prosenttiosuuden **Konsolidointi-%** -kentässä.  

## <a name="see-also"></a>Katso myös

[Usean yrityksen kirjanpitotietojen konsolidoiminen](finance-consolidated-company-reporting.md)  
[Konsernitapahtumien hallinta](intercompany-manage.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Liiketoimintatietojen vienti Exceliin](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
