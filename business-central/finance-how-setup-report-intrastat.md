---
title: "Intrastat-ilmoituksen määrittäminen ja raportoiminen| Microsoft Docs"
description: "Opi määrittämään Intrastat-raportointiominaisuudet ja raportoimaan muiden EU-maissa toimivien yritysten kanssa käyty kauppa."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: b75d709933cd9d147a9b5e0862a88a44a300f3c1
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="how-to-set-up-and-report-intrastat"></a>Toimintaohje: Intrastat-ilmoituksen määrittäminen ja raportoiminen
Kaikkien Euroopan unionin alueen yritysten täytyy raportoida kaupastaan muiden EU-maiden/alueiden kanssa. Tavaran liikkuminen on raportoitava kotimaan/-alueen tilastoviranomaisille kuukausittain ja raportti on toimitettava veroviranomaisille. Ohjelmassa tätä kutsutaan Intrastat-raportoinniksi. **Intrastat-ilmoitus**-sivulla voi täyttää jaksottaiset Intrastat-ilmoitukset.  

## <a name="required-and-optional-setups"></a>Pakolliset ja valinnaiset määritykset
Sinun on määritettävä useita asetuksia, ennen kuin voit raportoida Intrastat-tiedot Intrastat-ilmoituksella.  

* **Intrastat-ilmoitusmallit**: Käytettävät Intrastat-ilmoitusmallit ja -erät on määritettävä. Koska Intrastat-tiedot raportoidaan kuukausittain, sinun on luotava 12 samaan malliin perustuvaa Intrastat-ilmoituserää.  
* **Kauppatavarakoodit**: Tulli- ja veroviranomaiset ovat luoneet nimikkeiden ja palvelujen luokittelua varten numeeriset koodit. Nämä koodit määritetään nimikkeissä.
* **Kauppatapahtuman luonteen koodit**: Mailla ja alueilla on eri koodit Intrastat-tapahtumatyypeille, kuten tavallisille ostoille ja myynneille, palautettujen tavaroiden vaihdolle ja palauttamattomien tavaroiden vaihdolle. Määritä omaa maata tai aluetta koskevat koodit. Voit käyttää niitä myynti- ja ostoasiakirjoissa ja palautusten käsittelyssä.  
* **Kuljetusmuodot**: Intrastat-kuljetusmuodoilla on seitsemän yksimerkkistä koodia. **1** tarkoittaa merikuljetusta, **2** rautatiekuljetusta, **3** tiekuljetusta, **4** ilmakuljetusta, **5** postitusta, **7** kiinteää asennusta ja **9** omaa käyttövoimaa (kuten auton kuljettaminen sitä ajamalla). [!INCLUDE[d365fin](includes/d365fin_md.md)] ei edellytä näitä koodeja, mutta suosituksena on käyttää merkitykseltään vastaavia kuvauksia.  

Myös seuraavat voi määrittää:

* **Tapahtumamääritykset**: Voit täydentää näiden määritysten avulla tapahtumatyyppien kuvauksia.  
* **Alueet**: Voit täydentää tämän vaihtoehdon avulla maita ja alueita koskevia tietoja.  
* **Tulo-/ lähtöpaikat**: Voit määrittää tämän vaihtoehdon avulla sijainnit, joissa lähetät nimikkeitä muihin maihin tai vastaanotat nimikkeitä muista maista. Heathrow'n lentoasema on esimerkki tulo- tai lähtöpaikasta. Tulo- tai lähtöpaikat annetaan myynti- ja ostoasiakirjoihin **Ulkomaankauppa**-pikavälilehdessä. Nämä tiedot kopioidaan myös nimiketapahtumista Intrastat-ilmoituksen luomisen yhteydessä.  

### <a name="to-set-up-intrastat-templates-and-batches"></a>Intrastat-ilmoituksen mallien ja erien määrittäminen
Intrastat-erätyöt sisältävät vain nimiketapahtumat mutta ei kirjanpitotapahtumia. Jos yrityksellä on Intrastat-raportointiin soveltuvia kirjanpitotapahtumia, ne on lisättävä manuaalisesti. Jos esimerkiksi ostat tietokoneen toisesta EU-maasta tai toiselta EU-alueelta, tietokonetta ei sijoiteta varastoon, mutta se kirjataan pääkirjanpitoon. Tällaiset tapahtumat on lisättävä manuaalisesti Intrastat-ilmoitukseen.  

Voit viedä tapahtumat tiedostoon, jonka voit lähettää Intrastat-viranomaisille. Voit myös tulostaa raportin, lisätä viranomaisten tiedot manuaalisesti lomakkeisiin ja lähettää sitten tiedot.

>  [!Note]
> Jokaiselle kuukaudelle kannattaa määrittää Intrastat-ilmoituksen erä.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-ilmoituksen mallit** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Luo malli jokaiselle käyttämällesi Intrastat-lomakkeelle.  
3. Luo eriä valitsemalla **Navigoi**-välilehdessä **Erät**.  
4. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Luo malli jokaiselle käyttämällesi Intrastat-lomakkeelle.  

> [!Note]
> Anna tilastokausi **Tilastokausi**-kenttään nelinumeroisena lukuna, jossa kaksi ensimmäistä lukua merkitsevät vuotta ja kaksi seuraavaa kuukautta. Anna esimerkiksi kesäkuulle 2017 luku 1706.

### <a name="to-set-up-commodity-codes"></a>Kauppatavarakoodien määrittäminen
Kaikilla ostettavilla ja myytävillä nimikkeillä on oltava kauppatavarakoodi.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kauppatavarakoodit** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Määritä kauppatavarakoodi laajentamalla **Nimikkeen kortti** -sivulla **Kustannukset ja kirjaus** -pikavälilehti ja antamalla koodi **Kauppatavarakoodi**-kenttään.   

### <a name="to-set-up-transaction-nature-codes"></a>Kauppatapahtuman luonteen koodien määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kauppatapahtuman luonteen koodit** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Jos käytät tiettyä kauppatapahtuman luonteen koodia usein, voit määrittää sen oletusasetukseksi. Se onnistuu valitsemalla koodi **Valtiokohtaiset asetukset** -sivulla.

### <a name="to-set-up-transport-methods"></a>Kuljetusmuotojen määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kuljetusmuodot** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-which-intrastat-report-fields-are-mandatory"></a>Joidenkin Intrastat-raportin kenttien määrittäminen pakolliseksi
Joissakin maissa, kuten Espanjassa ja Isossa-Britanniassa, viranomaiset vaativat Intrastat-raportteihin esimerkiksi ostojen toimitustavan tai joitakin arvoja myynnin ylittäessä tietyn raja-arvon. Voit valita **Intrastat-asetukset**-sivulla voi osoittaa, että **Intrastat-tarkistusluettelon asetukset** määrittää pakolliset kentät **Intrastat-ilmoitus**-sivulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-asetukset** ja valitse sitten liittyvä linkki.
2. Valitse **Intrastat-tarkistusluettelon asetukset** -toiminto.
3. Valitse **Intrastat-tarkistusluettelon asetukset** -sivulla **Kentän nimi** ja valitse se Intrastat-raportin kenttä, josta tehdään pakollinen. 

## <a name="to-report-intrastat"></a>Intrastat-raportointi
Kun olet täyttänyt Intrastat-ilmoituksen, voit suorittaa **Tarkistusluettelo-raportti**-toiminnon ja varmistaa, että kaikki ilmoituksen tiedot ovat oikein. **Intrastat-tarkistusluettelon asetukset** -sivulla määritetyt pakolliset kentät, joissa ei ole arvoja, näytetään Virheet ja varoitukset -tietoruudussa **Intrastat-kirjaus**-sivulla. Voit sitten tulostaa Intrastat-raportin lomakkeena tai luoda tiedoston, jonka voit lähettää oman maasi tai alueesi veroviranomaisille.  

### <a name="to-fill-in-intrastat-journals"></a>Intrastat-ilmoitusten täyttäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-kirjaus** ja valitse sitten liittyvä linkki.  
2. Valitse **Intrastat-ilmoitus**-sivulla **Erän nimi** -kentässä käsiteltävä kirjauskansion erä ja valitse sitten **OK**.  
3. Valitse **Ehdota rivejä** -toiminto. **Aloituspvm**- ja **Lopetuspvm**-kentissä on valmiina päivämäärät, jotka määriteltiin tilastokaudelle päiväkirjan erässä.  
4. Voit syöttää **Epäsuorien kustann. pros.osuus** -kenttään prosentin (kattamaan kuljetus- ja vakuutuskustannuksia). Jos syötät prosentin, päiväkirjan **Tilastoarvo**-kentän sisältö on suhteellisesti korkeampi.  
5. Käynnistä eräajo valitsemalla **OK**.  

Eräajo hakee kaikki tämän tilastokauden nimiketapahtumat ja lisää ne riveiksi Intrastat-ilmoitukseen. Voit muokata rivejä tarvittaessa.  

> [!IMPORTANT]  
>  Eräajo hakee vain ne tapahtumat, joilla on sellainen maa- tai aluekoodi, joille Intrastat-koodi annettiin **Maat/alueet**-sivulla. Siksi on tärkeää, että syötät Intrastat-koodit sellaisille maa-/aluekoodeille, joilla tulet tekemään eräajoja.  

### <a name="report-intrastat-on-a-form-or-a-file"></a>Intrastat-raportointi lomakkeella tai tiedostona
Saat Intrastat-lomakkeeseen tarvittavat tiedot tilastoja ylläpitäviltä viranomaisilta tulostamalla **Intrastat – lomake** -raportin. Ennen sitä sinun täytyy laatia Intrastat-ilmoitus ja täyttää se. Jos sinulla on sekä myyntiin että ostoihin liittyviä kauppatahtumia, sinun täytyy tehdä erillinen lomake molemmille tyypeille, ja sinun täytyy siten tulostaa raportti kahdesti.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-kirjaukset** ja valitse sitten liittyvä linkki.  
2. Valitse käsiteltävä päiväkirjan erä **Intrastat-ilmoitus**-sivun **Erän nimi** -kentässä.  
3. Jos et vielä ole täyttänyt ilmoitusta manuaalisesti tai valitsemalla **Ehdota rivejä**, tee se nyt.  
4. Valitse **Tulostaa Intrastat-ilmoituksen** -toiminnon.  
5. Lisää **Intrastat-ilmoituksen rivi** -pikavälilehdessä **Tyyppi**-suodatin ja määritä, onko kyseessä **Vastaanotto** vai **Toimitus**.  
6. Tulosta raportti valitsemalla **Lähetä kohteeseen**.  

### <a name="report-intrastat-in-a-file"></a>Intrastat-raportointi tiedostona
Voit nyt lähettää Intrastat-raportin tiedostona. Ennen tiedoston luomista voit tulostaa tarkastusluettelon, jossa on samat tiedo kuin mitä tiedostossa tulee olemaan.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-kirjaus** ja valitse sitten liittyvä linkki.  
2. Valitse käsiteltävä päiväkirjan erä **Intrastat-ilmoitus**-sivun **Erän nimi** -kentässä.  
3. Jos et ole vielä täyttänyt ilmoitusta manuaalisesti tai valitsemalla **Ehdota rivejä**, tee se nyt.  
4. Valitse **Luo tiedosto** -toiminto.  
5. Valitse eräajosivulla **OK**.  
6. Valitse **Tallenna**.  
7. Selaa sijaintiin, jonne haluat tallentaa tiedoston. Anna tiedoston nimi ja valitse sitten **Tallenna**.

## <a name="reorganize-intrastat-journals"></a>Intrastat-ilmoitusten uudelleenjärjestely
Koska Intrastat-raportti on lähetettävä joka kuukausi ja luot uuden päiväkirjan erä kullekin raportille, sinulla tulee olemaan ajan mittaan useita päiväkirjan eriä. Kirjauskansiorivejä ei poisteta automaattisesti. Haluat ehkä järjestää päiväkirjan erien nimet uudelleen jaksoittain. Voit tehdä sen poistamalla ne päiväkirjan erät, joita et enää tarvitse. Näissä erissä olevat päiväkirjan rivit poistuvat myös.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-kirjaukset** ja valitse sitten liittyvä linkki.  
2. Voit tarkastella asetuksia valitsemalla **Erän nimi** -kentän.  
3. Valitse ensin poistettavat päiväkirjan erät ja sitten **Poista**.  

## <a name="see-also"></a>Katso myös
[Taloushallinto](finance.md)

