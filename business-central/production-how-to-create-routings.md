---
title: Uusien reititysten luominen
description: Tässä aiheessa on yleiskuvaus eri tavoista luoda reitityksiä, mukaan lukien vaaditut edellytykset ja reitityslinkkien luominen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000764, 99000765, 99000766, 99000767, 99000794, 99000796, 99000798, 99000806, 99000808, 99000810, 99000817, 99000834, 99000835, 99000836, 99000837, 99000840, 99000841, 99000844, 99000845
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 9aca8b6308fc5a45e008bc5aba529f51e764c79d
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516872"
---
# <a name="create-routings"></a>Uusien reititysten luominen

Tuotantoyritykset käyttävät reitityksiä tuotantoprosessin näyttämiseen ja ohjaamiseen.

Reititys on prosessiaikataulutuksen, kapasiteettiaikataulutuksen sekä materiaalitarpeitten ja tuotantoasiakirjojen aikataulutetun määrittelyn perusta.  

Reititykset määritetään tuotannon tuoterakenteissa tuotannon loppunimikkeeseen. Reititys sisältää perustiedot tuotettavan nimikkeen prosessivaatimuksista. Kun nimikkeelle luodaan tuotantotilaus, reititys ohjaa toimintojen aikatauluja tuotantotilauksen **Tuotantotilaus reititys** -sivulla näkyvällä tavalla.  

Seuraavat toimet on oltava tehtynä ennen reitityksen määrittämistä:  

- Tuotannossa mukana olevien päänimikkeiden nimikekortit on luotu. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).
- Tuotantoresurssit on määritetty. Lisätietoja on kohdassa [Tuotantosolujen ja kuormituskeskusten määrittäminen](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-routing"></a>Reitityksen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Reititykset** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **Tyyppi**-kentässä **Sarja**, jos haluat laskea tuotantoreitityksen kentän **Operaation nro** arvon mukaan. -kentässä.  
    Valitse **Rinnakkainen** laskeaksesi operaatiot **Seuraavan operaation nro**-kentän mukaan. -kentässä.  
5. Jos haluat muokata reititystä, aseta **Tila**-kentän arvoksi **Uusi** tai **Kehityksen alla**. Jos haluat aktivoida sen, määritä **Tila**-kentän arvoksi **Hyväksytty**.  

    Siirry reititysrivien täyttämiseen.
6. Täytä **Operaation nro** -kenttään ensimmäisen operaation numero (esimerkiksi **10**).  
7. Määritä **Tyyppi**-kentässä käytettävän resurssin tyyppi (esimerkiksi **Tuotantosolu**).  
8. Valitse **Nro**-kenttään käytettävä resurssi (tai kirjoita numero kenttään).  
9. Määritä **Reitityslinkin koodi** -kenttään koodi, joka liittää komponentin tiettyyn toimintoon. Lisätietoja on kohdassa [Reitityslinkkien luominen](production-how-to-create-routings.md#to-create-routing-links).
10. Anna **Ajoaika**- ja **Asetusaika**-kenttiin toiminnon suorittamiseen tarvittavat prosessiajat.

     > [!NOTE]
     > Asetusaika lasketaan tuotantotilausta kohden, ajoaika tuotettavaa nimikettä kohden.  

11. Määritä **Samanaikaiset kapasiteetit** -kentässä, kuinka monta valitun resurssin yksikköä toiminnon suorittamiseen käytetään. Jos esimerkiksi yhteen pakkaustoimintoon on kohdistettu kaksi työntekijää, ajoaika puolitetaan.  
12. Jatka rivien täyttämistä, kunnes kaikki nimikkeen tuottamiseen tarvittavat toiminnot on määritetty.  
13. Voit kopioida rivit reitityksestä valitsemalla aiemmin luodut rivit ja valitsemalla sitten **Kopioi reititys**.  
14. Hyväksy reititys.  
15. Voit nyt liittää uuden reitityksen kyseisen tuotantonimikkeen korttiin täyttämällä **Reititysnro**-kentän. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).  

> [!NOTE]  
> Muista myös laskea nimikkeen vakiokustannukset uudelleen **Nimike**-kortista: valitse ensin **Tuotanto**-toiminto, sitten **Laske vakiokustannus** -toiminto ja lopuksi **Kaikille tasoille** -toiminto.  

## <a name="to-create-routing-links"></a>Reitityslinkkien luominen

Reitityslinkkejä luomalla komponentteja voidaan liittää tiettyihin toimintoihin niin, että suhde säilyy, vaikka tuotannon tuoterakennetta ja/tai reititystä muokattaisiin. Reitityslinkit mahdollistavat myös komponenttien materiaalinoton juuri oikeaan aikaan eli linkitetyn toiminnon alkaessa - eikä silloin, kun koko tilaus vapautetaan. Lisätietoja on kohdassa [Komponenttien materiaalinotto toiminnan tuotoksen mukaan](production-how-to-flush-components-according-to-operation-output.md).  

Toinen tästä seuraava tärkeä etu on se, että linkitetyt komponentit ja toiminnot voidaan näyttää loogisena prosessirakenteena kirjattaessa tuotosta ja kulutusta **Tuotantopäiväkirja**-sivulla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Reititykset** ja valitse sitten vastaava linkki.  
2. Avaa reititys, joka sisältää linkitettävät operaatiot.  

    Varmista, että reitityksen tila on **Kehityksen alla**.  

3. Valitse koodi asianmukaisen reititysrivin **Reitityslinkin koodi** -kentässä.  
4. Lisää tarvittaessa eri reitityslinkin koodeja muihin reitityksen toimintoihin.  

    > [!NOTE]  
    > Älä käytä samaa reitityslinkin koodia reitityksen eri toiminnoissa, sillä saatat virheellisesti linkittää komponentin kahteen eri toimintoon ja käyttää sen näin kahteen kertaan.  
    >
    > Reitityslinkin koodi kannattaa nimetä toiminnon mukaan reitityslinkkien säilyttämiseksi toimintokohtaisina.

5. Aseta reitityksen tilaksi **Hyväksytty**.  

    Reitityslinkkien koodit on nyt määritetty operaatioille. Seuraavaksi on luotava todellinen linkki määrittämällä samat koodit tiettyihin komponetteihin asianmukaisessa tuoterakenteessa.  

6. Avaa **Tuotannon tuoterakenne**, joka sisältää edellä mainittuihin toimintoihin linkitettävät komponentit. Lisätietoja on kohdassa [Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md).
7. Varmista, että tuoterakenteen tila on **Kehityksen alla**.  
8. Valitse asianmukaisen tuotannon tuoterakenteen rivin **Reitityslinkin koodi** -kentässä koodi, jonka juuri määritit asianmukaiselle toiminnolle.  
9. Jatka reitityslinkkien koodien lisäämistä muille komponenteille sen mukaan, missä toiminnossa kutakin komponenttia käytetään.  
10. Aseta tuotannon tuoterakenteen tilaksi **Hyväksytty**.  

    > [!NOTE]  
    > Voit ottaa aiemmin luodun tuotantotilauksen reitityslinkit käyttöön päivittämällä tuotantotilauksen. Lisätietoja on kohdassa [Tuotantotilausten luominen](production-how-to-create-production-orders.md).  

Kun nyt luodaan ja/tai päivitetään tuotantotilaus, joka käyttää yllä käsiteltyjä tuotannon tuoterakennetta ja reititystä, komponentit linkitetään valittuihin toimintoihin. Tämä on näkyvissä **Tuot. til.komponentit**-sivulla tuotantotilauksen kohdalla. Määritettyjä reitityslinkkien koodeja voidaan myös lisätä ja poistaa tällä sivulla koska tahansa.

## <a name="to-assign-personnel-tools-and-quality-measures-to-routing-operations"></a>Henkilöstön, työkalujen ja laatutoimien määrittäminen reititystoimintoihin

Jos operaatiolle vaaditaan henkilöstöä, jolla on pätevyyttä, erikoistietämystä tai erityisvaltuutus, kyseisen henkilöstön voi määritellä operaatiolle. Voit määrittää toimintoon myös työkaluja ja laatuvaatimuksia. Tässä toimintaohjeessa käsitellään henkilöstön määrittämistä. Muiden toimintotyyppien tietoja koskevat vastaavanlaiset ohjeet.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Reititykset** ja valitse sitten vastaava linkki.  
2. Avaa käsiteltävä reititys.  
3. Valitse **Rivit**-pikavälilehdessä ensin käsiteltävä rivi, sitten **Toiminnot**-toiminto ja lopuksi **Henkilöstö**-toiminto.  
4. Täytä **Reititys henkilöstö** -sivun kentät.  
5. Poistu sivulta valitsemalla **OK**-painike. Syötetyt arvot kopioidaan ja määritellään operaatiolle.  

## <a name="to-create-a-new-versions-of-a-routing"></a>Reititysten uusien versioiden luominen

Versioperiaate mahdollistaa useiden reititysversioiden hallitsemisen. Reititysversion rakenne vastaa reititysversion otsikosta ja reititysversion riveistä koostuvan reitityksen rakennetta. Peruseron määrittää aloituspäivämäärä.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Reititykset** ja valitse sitten vastaava linkki.  
2. Valitse ensin kopioitava reititys ja sitten **Versiot**-toiminto.  
3. Valitse **Reititysversiot**-sivulla **Uusi**-toiminto.
4. Täytä tarvittavat kentät.
5. Anna **Versiokoodi**-kentässä version yksilöivä tunniste. Kaikenlaisten numero- ja kirjainyhdistelmien käyttö on sallittua.  

    Vasta luodulle versiolle määritetään automaattisesti tilaksi **Uusi.**  
6. Voit luoda toimintorivejä valitsemalla ensin tyhjän rivin ja täyttämällä sitten **Operaation nro** -kentän operaatioiden järjestyksen mukaisesti.

    Operaatiorivit on lajiteltu operaationumeroiden nousevassa järjestyksessä. Jotta myöhemmin olisi mahdollista tehdä muutoksia, on suositeltavaa valita riittävän suuria työvaiheiden välejä. **Seuraavan operaation nro** -kenttä viittaa seuraavaan operaatioon. Operaation numero voidaan syöttää suoraan.

7. Kun reititysversio on valmis, **Tila**-kentän asetuksena on **Hyväksytty**.

Version voimassaoloajan määrittää **Aloituspvm**-kenttä.  

## <a name="see-also"></a>Katso myös

[Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)  
[Suunnittelu](production-planning.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]