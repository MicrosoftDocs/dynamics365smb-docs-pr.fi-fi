---
title: Reititysten luominen | Microsoft Docs
description: "Reititys sisältää perustiedot tuotettavan nimikkeen prosessivaatimuksista. Kun nimikkeelle luodaan tuotantotilaus, reititys ohjaa toimintojen aikatauluja tuotantotilauksen **Tuotantotilaus reititys** -ikkunassa näkyvällä tavalla."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: daa014eaa78caa7a317b05ca92ff27c1d1530c06
ms.openlocfilehash: 85cd332e4b62ba73f511989983e1eb9f5147c5fb
ms.contentlocale: fi-fi
ms.lasthandoff: 10/17/2017

---
# <a name="how-to-create-routings"></a>Uusien reititysten luominen
Tuotantoyritykset käyttävät reitityksiä tuotantoprosessin näyttämiseen ja ohjaamiseen.

Reititys on prosessiaikataulutuksen, kapasiteettiaikataulutuksen sekä materiaalitarpeitten ja tuotantoasiakirjojen aikataulutetun määrittelyn perusta.  

Reititykset määritetään tuotannon tuoterakenteissa tuotannon loppunimikkeeseen. Reititys sisältää perustiedot tuotettavan nimikkeen prosessivaatimuksista. Kun nimikkeelle luodaan tuotantotilaus, reititys ohjaa toimintojen aikatauluja tuotantotilauksen **Tuotantotilaus reititys** -ikkunassa näkyvällä tavalla.  

Seuraavat toimet on oltava tehtynä ennen reitityksen määrittämistä:  

- Tuotannossa mukana olevien päänimikkeiden nimikekortit on luotu. Lisätietoja on ohjeaiheessa [Toimintaohje: Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).
- Tuotantoresurssit on määritetty. Lisätietoja on kohdassa [Toimintaohje: Tuotantosolujen ja kuormituskeskusten määrittäminen](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-routing"></a>Reitityksen luominen  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Reititykset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Valitse **Tyyppi**-kentässä **Sarja**, jos haluat laskea tuotantoreitityksen kentän **Operaation nro** arvon mukaan. -kentässä.   
    Valitse **Rinnakkainen** laskeaksesi operaatiot **Seuraavan operaation nro**-kentän mukaan. -kentässä.  
5.  Jos haluat muokata reititystä, aseta **Tila**-kentän arvoksi **Uusi** tai **Kehityksen alla**. Jos haluat aktivoida sen, määritä **Tila**-kentän arvoksi **Hyväksytty**.  

    Siirry reititysrivien täyttämiseen.
6.  Täytä **Operaation nro** -kenttään ensimmäisen operaation numero (esimerkiksi **10**).  
7.  Määritä **Tyyppi**-kentässä käytettävän resurssin tyyppi (esimerkiksi **Tuotantosolu**).  
8.  Valitse **Nro**-kenttään käytettävä resurssi (tai kirjoita numero kenttään).  
9.  Määritä **Reitityslinkin koodi** -kenttään koodi, joka liittää komponentin tiettyyn toimintoon. Lisätietoja on kohdassa Reitityslinkkien luominen.
10.  Anna **Ajoaika**- ja **Asetusaika**-kenttiin toiminnon suorittamiseen tarvittavat prosessiajat.  

    > [!NOTE]  
    >  Asetusaika lasketaan tuotantotilausta kohden, ajoaika tuotettavaa nimikettä kohden.  

11.  Määritä **Samanaikaiset kapasiteetit** -kentässä, kuinka monta valitun resurssin yksikköä toiminnon suorittamiseen käytetään. Jos esimerkiksi yhteen pakkaustoimintoon on kohdistettu kaksi työntekijää, ajoaika puolitetaan.  
12.  Jatka rivien täyttämistä, kunnes kaikki nimikkeen tuottamiseen tarvittavat toiminnot on määritetty.  
13.  Voit kopioida rivit reitityksestä valitsemalla aiemmin luodut rivit ja valitsemalla sitten **Kopioi reititys**.  
14. Hyväksy reititys.  
15. Voit nyt liittää uuden reitityksen kyseisen tuotantonimikkeen korttiin täyttämällä **Reititysnro**-kentän. Lisätietoja on ohjeaiheessa [Toimintaohje: Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).  

> [!NOTE]  
>  Muista myös laskea nimikkeen vakiokustannukset uudelleen **Nimike**-kortista: valitse ensin **Tuotanto**-toiminto, sitten **Laske vakiokustannus** -toiminto ja lopuksi **Kaikille tasoille** -toiminto.  

## <a name="to-create-routing-links"></a>Reitityslinkkien luominen
Reitityslinkkejä luomalla komponentteja voidaan liittää tiettyihin toimintoihin niin, että suhde säilyy, vaikka tuotannon tuoterakennetta ja/tai reititystä muokattaisiin. Reitityslinkit mahdollistavat myös komponenttien materiaalinoton juuri oikeaan aikaan eli linkitetyn toiminnon alkaessa - eikä silloin, kun koko tilaus vapautetaan. Lisätietoja on kohdassa [Komponenttien materiaalinotto toiminnan tuotoksen mukaan](production-how-to-flush-components-according-to-operation-output.md).  

Toinen tästä seuraava tärkeä etu on se, että linkitetyt komponentit ja toiminnot voidaan näyttää loogisena prosessirakenteena kirjattaessa tuotosta ja kulutusta **Tuotantopäiväkirja**-ikkunassa.  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Reititykset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Avaa reititys, joka sisältää linkitettävät operaatiot.  

    Varmista, että reitityksen tila on **Kehityksen alla**.  

3.  Valitse koodi asianmukaisen reititysrivin **Reitityslinkin koodi** -kentässä.  
4.  Lisää tarvittaessa eri reitityslinkin koodeja muihin reitityksen toimintoihin.  

    > [!NOTE]  
    >  Älä käytä samaa reitityslinkin koodia reitityksen eri toiminnoissa, sillä saatat virheellisesti linkittää komponentin kahteen eri toimintoon ja käyttää sen näin kahteen kertaan.  
    >   
    >  Reitityslinkin koodi kannattaa nimetä toiminnon mukaan reitityslinkkien säilyttämiseksi toimintokohtaisina.

5.  Aseta reitityksen tilaksi **Hyväksytty**.  

    Reitityslinkkien koodit on nyt määritetty operaatioille. Seuraavaksi on luotava todellinen linkki määrittämällä samat koodit tiettyihin komponetteihin asianmukaisessa tuoterakenteessa.  

6.  Avaa **Tuotannon tuoterakenne**, joka sisältää edellä mainittuihin toimintoihin linkitettävät komponentit. Lisätietoja on kohdassa [Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md).
7.  Varmista, että tuoterakenteen tila on **Kehityksen alla**.  
8.  Valitse asianmukaisen tuotannon tuoterakenteen rivin **Reitityslinkin koodi** -kentässä koodi, jonka juuri määritit asianmukaiselle toiminnolle.  
9. Jatka reitityslinkkien koodien lisäämistä muille komponenteille sen mukaan, missä toiminnossa kutakin komponenttia käytetään.  
10. Aseta tuotannon tuoterakenteen tilaksi **Hyväksytty**.  

    > [!NOTE]  
    >  Voit ottaa aiemmin luodun tuotantotilauksen reitityslinkit käyttöön päivittämällä tuotantotilauksen. Lisätietoja on kohdassa [Toimintaohje: Tuotantotilausten luominen](production-how-to-create-production-orders.md).  

Kun nyt luodaan ja/tai päivitetään tuotantotilaus, joka käyttää yllä käsiteltyjä tuotannon tuoterakennetta ja reititystä, komponentit linkitetään valittuihin toimintoihin. Tämä on näkyvissä **Tuot. til.komponentit**-ikkunassa tuotantotilauksen kohdalla. Määritettyjä reitityslinkkien koodeja voidaan myös lisätä ja poistaa tässä ikkunassa koska tahansa.

## <a name="to-assign-personnel-tools-and-quality-measures-to-routing-operations"></a>Henkilöstön, työkalujen ja laatutoimien määrittäminen reititystoimintoihin
Jos operaatiolle vaaditaan henkilöstöä, jolla on pätevyyttä, erikoistietämystä tai erityisvaltuutus, kyseisen henkilöstön voi määritellä operaatiolle. Voit määrittää toimintoon myös työkaluja ja laatuvaatimuksia. Tässä toimintaohjeessa käsitellään henkilöstön määrittämistä. Muiden toimintotyyppien tietoja koskevat vastaavanlaiset ohjeet.

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Reititykset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Avaa käsiteltävä reititys.  
3.  Valitse **Rivit** -pikavälilehdessä ensin käsiteltävä rivi ja sitten **Henkilöstö**-toiminto.  
4.  Täytä **Reititys henkilöstö** -ikkunan kentät.  
5.  Valitse **OK**-painike ikkunan sulkemiseksi. Syötetyt arvot kopioidaan ja määritellään operaatiolle.    

## <a name="to-create-a-new-versions-of-a-routing"></a>Reititysten uusien versioiden luominen  
Versioperiaate mahdollistaa useiden reititysversioiden hallitsemisen. Reititysversion rakenne vastaa reititysversion otsikosta ja reititysversion riveistä koostuvan reitityksen rakennetta. Peruseron määrittää aloituspäivämäärä.  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Reititykset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse ensin kopioitava reititys ja sitten **Versiot**-toiminto.  
3. Valitse **Reititysversiot**-ikkunassa **Uusi**-toiminto.
4. Täytä tarvittavat kentät.
5.  Anna **Versiokoodi**-kentässä version yksilöivä tunniste. Kaikenlaisten numero- ja kirjainyhdistelmien käyttö on sallittua.  

    Vasta luodulle versiolle määritetään automaattisesti tilaksi **Uusi.**  
6.  Voit luoda toimintorivejä valitsemalla ensin tyhjän rivin ja täyttämällä sitten **Operaation nro** -kentän operaatioiden järjestyksen mukaisesti.

    Operaatiorivit on lajiteltu operaationumeroiden nousevassa järjestyksessä. Jotta myöhemmin olisi mahdollista tehdä muutoksia, on suositeltavaa valita riittävän suuria työvaiheiden välejä. **Seuraavan operaation nro** -kenttä viittaa seuraavaan operaatioon. Operaation numero voidaan syöttää suoraan.

7. Kun reititysversio on valmis, **Tila**-kentän asetuksena on **Hyväksytty**.

Version voimassaoloaika määritetään **Aloituspvm**-kentässä.  

## <a name="see-also"></a>Katso myös  
[Toimintaohje: Uusien tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Suunnittelu](production-planning.md)   
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

