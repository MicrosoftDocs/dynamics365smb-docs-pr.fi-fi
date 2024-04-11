---
title: Analyysiraporttien luominen
description: 'Kuvaa, miten uusien analyysiraporttien luominen myyntejä, ostoja ja varastoa varten sekä analyysimallien määrittäminen tapahtuu.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 04/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Analyysiraporttien luominen

Myyntipäälliköiden on analysoitava liikevaihtoa, bruttokatetta ja muita myynnin tunnuslukuja säännöllisesti. Ostajat ovat kiinnostuneempia ostovolyymien dynamiikasta, toimittajien suorituskyvystä ja ostohinnoista. Logistiikka-/varastopäälliköt puolestaan tarvitsevat tietoja varaston kierrosta, varaston siirtoanalyysin ja tilastotietoja varaston arvosta. Yhden koon analyysiraporttia ei siis ole.

Voit mukauttaa analyysiraportteja kirjattujen tapahtumien, esimerkiksi myynnin, ostojen, siirtojen ja varastonmuutosten, tietueiden perusteella. Räätälöitävän raportin lähdetietoja, jotka johdetaan nimiketapahtumista (niihin liittyvien arvotapahtumien kera), voidaan yhdistää, vertailla ja esittää mielekkäillä käyttäjän määrittämillä tavoilla. Niinpä analyysiraportti muistuttaa paljon Microsoft Excelin pivot-taulukkoraporttia.  

Voit esimerkiksi luoda henkilökohtaisen raportin, jossa keskitytään avaintiliisi tuotteen kokonaisvaihtuvuuden ja myytyjen määrien, bruttotuoton ja bruttotuoton prosenttiosuuden osalta kuluvana kuukautena. Sitten voit verrata näitä lukuja edellisen kuukauden tai saman kuukauden viime vuoden tuloksiin ja laskea poikkeamat. Kaikki tämä voidaan tehdä yhdessä ja samassa näkymässä, jolloin voit navigoida tunnistettujen ongelma-alueiden syihin ja jopa valita pudotusvalikosta nollataksesi yksityiskohdat aina yksittäisten tapahtumien tasolle asti.  

Analyysiraportit koostuvat analysoitavista objekteista (kuten asiakkaista, asiakasryhmistä ja myyjistä, jotka esitetään riveinä) ja analyysin parametreista eli objektin analysointitavasta (kuten katelaskelmista, myyntisummien ja -määrien jaksoittaisista vertailuista tai todellisten ja budjetoitujen lukujen jaksoittaisista vertailuista, jotka esitetään sarakkeina). 

Analyysiraporttien lisäksi voit luoda ja tarkastella samanlaisia tietoja analyysinäkymissä, (jotka perustuvat dimensioihin). Lue lisätietoja kohdasta [Analysoi tietoja dimensioiden mukaan](bi-how-analyze-data-dimension.md).

## Esimerkki

Voit määrittää nämä rivit (analysoitavat objektit):  

- Tietokoneet  
- Näytöt  
- Varaosat  

Tämän jälkeen voit määrittää sarakkeet (miten haluat objektit analysoida):  

- Kuluvan kuukauden myynti  
- Edellisen kuukauden myynti  
- Edellisen kuukauden myynti prosentteina.  

## Rivi- ja sarakeasettelujen määrittäminen

**Analyysiraportti**-sivun avulla voit katsella eri rivi- ja sarakeasetteluja, joita olet määrittänyt:

* **Analyysirivimallit**-sivulla, jossa määrität raportin nimen ja objektit, jotka haluat näyttää raportin riveillä, ja
* **Analyysisarkemallit**-sivu, jolla voit määrittää tällä sivulla sarakkeen mallin nimen ja raportissa sarakkeina esitettävät analyysin parametrit. Jokainen rivi tällä sivulla vastaa raportin saraketta. 

Huomaa, että analyysin rivit ja sarakkeet ovat riippumattomia toisistaan.  

[!INCLUDE[prod_short](includes/prod_short.md)] yhdistää raportin tuloksen **Analyysiraportti**-sivulla määritettyjen rivien ja sarakkeiden perusteella seuraavassa taulukossa näytetyllä tavalla.  

|- |Kuluvan kuukauden myynti|Edellisen kuukauden myynti|Edellisen kuukauden myynti (%)|  
|-|-|-|-|  
|Tietokoneet| | | |  
|Näytöt| | | |  
|Varaosat| | | |  
|Yhteensä| | | |  

Voit esimerkiksi esittää kuukausiraportin määrittämällä yhden ryhmän riviasetteluja ja vuosiraportin määrittämällä useita ryhmiä sarakeasetteluja.

## Analyysisarakkeen mallien määrittäminen

Seuraava toimenpide perustuu myynnin analyysinäkymiin. Vaiheet ovat samanlaiset ostojen ja varaston analyysinäkymille.

Analyysisarakemalli sisältää joukon rivejä, joista jokainen edustaa analyysiraporttiin haluamaasi analyysisaraketta. Kun määrität sarakkeen, riville on määritettävä analyysin tyyppikoodi. Analyysin tyyppikoodi määrittää lähdetietojen tyypin nimiketapahtumissa, joihin analyysi perustuu. Lähdetiedot voivat sisältää kustannukset, myyntisumman tai määrän ja niihin liittyvät arvotapahtumat. Voit määrittää haluamasi määrän sarakkeen malleja ja luoda sen jälkeen niiden avulla uusia analyysiraportteja.    

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntisarakemallit**, valitse sitten liittyvä linkki.  
2. Valitse ensimmäinen tyhjä rivi ja täytä tarvittavat kentät.
3. Valitse **Sarakkeet**-toiminto.  
4. Määritä analyysiraporttiin sisällytettävät sarakkeet täyttämällä **Analysointisarakkeet**-sivun kentät.  

    > [!NOTE]  
    > Kun määrität sarakkeen, täytä **Analyysin tyyppikoodi** -kenttä (kaikkien saraketyyppien osalta lukuun ottamatta tyyppiä **Kaava**). Määritä analyysin tyyppikoodi **Analyysityypit**-sivulla.  
    
    Jos lisäksi valitset **Tapahtumakirjauksen tyyppi** -kentässä **Nimiketapahtumat**, ohjelma kopioi todelliset luvut nimiketapahtumasta. Jos valitset **Nimikkeiden budjettitapahtumat**, ohjelma kopioi budjetoidut luvut budjetista.  
5. Tallenna muutokset valitsemalla  **OK**.  

## Analyysirivimallien määrittäminen

Seuraava toimenpide perustuu myynnin analyysiraportteihin. Vaiheet ovat samanlaiset ostojen ja varaston analyysiraporteille.

Analyysirivimalli sisältää joukon rivejä, joista jokainen edustaa analyysiraporttiin haluamaasi analyysiriviä. Rivi voi tarkoittaa yhtä nimikettä tai nimikkeiden aluetta, yhtä asiakasta tai asiakkaiden aluetta, yhtä toimittajaa tai toimittajien aluetta tai yhtä ryhmää tai ryhmien aluetta. Voit myös luoda riville kaavan, joka laskee muut rivit yhteen. Voit määrittää haluamasi määrän rivimalleja ja luoda niiden avulla sen jälkeen uusia analyysiraportteja.   

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntirivimallit**, valitse sitten liittyvä linkki.  
2. Valitse ensimmäinen tyhjä rivi ja täytä tarvittavat kentät.
3. Valitse **Rivit**-toiminto.  
4. Luo **Analyysin rivit** -sivulla rivejä niitä nimikkeitä, asiakkaita, toimittajia tai myyjiä varten, joiden luvut haluat näyttää analyysiraportissa. Täytä **Tyyppi**-, **Alue**- ja **Kuvaus**-kenttä.  

> [!NOTE]  
> Voit myös luoda useita yksittäisiä rivejä jokaista nimikettä, asiakasta ja niin edelleen kohti. Valitse Toiminnot ja sitten haluamasi lisäysvaihtoehto, jolloin ohjelma täyttää rivin kaikki asiaankuuluvat kentät. Sen jälkeen voit tarvittaessa muokata rivejä manuaalisesti. Voit halutessasi muokata rivejä manuaalisesti. Voit lisätä rivejä valitsemalla **Lisää nimikkeet** tai **Lisää nimikeryhmät** -toiminnon.  

## Uusien myynnin analyysiraporttien luominen

Seuraava toimenpide perustuu myynnin analyysiraportteihin. Vaiheet ovat samanlaiset ostojen ja varaston analyysiraporteille.

Analyysiraporttien avulla voit analysoida myynnin dynamiikkaa tunnuslukujen mukaan, jotka valitset, esimerkiksi liikevaihto, sekä summat että määrät, katetuotto tai todellisen myynnin edistyminen budjettiin verraten. Analyysiraportin avulla voit myös analysoida keskimääräisiä myyntihintojasi ja arvioida myyntihenkilöstösi myyntituloksia.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myynnin analyysiraportit**, valitse sitten liittyvä linkki.  
2. Valitse **Analyysiraportti - Myynti** -sivulla **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **Muokkaa analyysiraporttia** -toiminto.
5. Valitse **Myynnin analyysiraportti** -sivulla **Näytä matriisi** -toiminto.  

> [!NOTE]  
> Rivi- ja sarakemallien yhdistelmien muodostaminen raporttien luontia varten sekä yksilöivien nimien määrittäminen niille on vapaavalintaista. Jos teet näin, sinun ei tarvitse valita rivi- ja sarakemalleja **Myynnin analyysiraportti** -sivulla jos valitset raportin nimen. Kun raportin nimi on valittu, voidaan rivi- ja sarakemalleja muuttaa itsenäisesti. Alkuperäinen yhdistelmä voidaan sitten myöhemmin palauttaa valitsemalla raportin nimi uudelleen.

## Katso myös

[Taloudelliset liiketoimintatiedot](bi.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
