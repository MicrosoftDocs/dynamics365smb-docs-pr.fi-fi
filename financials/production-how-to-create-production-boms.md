---
title: Tuotannon tuoterakenteiden luominen | Microsoft Docs
description: "Tuotannon tuoterakenne sisältää perustiedot päänimikkeen tuotannossa käytettävistä komponenteista ja osakokoonpanoista. Kun päänimikkeelle luodaan tuotantotilaus, tuotannon tuoterakenne ohjaa materiaalitarpeiden laskentaa **Tuot.til. komponentit** -ikkunassa näkyvällä tavalla."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/05/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a193d1ac19a0474b4a541165ef9f06d21ac7fb7d
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="create-production-boms"></a>Tuotannon tuoterakenteiden luominen
Tuotannon tuoterakenne sisältää perustiedot päänimikkeen tuotannossa käytettävistä komponenteista ja osakokoonpanoista. Kun päänimikkeelle luodaan tuotantotilaus, tuotannon tuoterakenne ohjaa materiaalitarpeiden laskentaa **Tuot.til. komponentit** -ikkunassa näkyvällä tavalla.

[!INCLUDE[d365fin](includes/d365fin_md.md)] tukee myös kokoonpanon tuoterakenteita. Voit käyttää kokoonpanotilauksia, kun teet komponenteista loppunimikkeitä yksinkertaisella prosessilla. Tämä prosessi voidaan toteutetaan vähintään yhdellä perusresurssilla, joka ei ole kuormituskeskus eikä tuotantosolu, tai ilman resursseja. Kokoonpanoprosessi voi olla esimerkiksi kahden viinipullon ja yhden kahvipaketin valinta ja niiden pakkaaminen lahjaksi. Lisätietoja on ohjeaiheen [Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md) kohdassa Kokoonpanon tuoterakenteet tai tuotannon tuoterakenteet.  

Seuraavat toimet on oltava tehtynä ennen reitityksen määrittämistä:  

- Tuotannossa mukana olevien päänimikkeiden nimikekortit on luotu. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).
- Tuotantoresurssit on määritetty. Lisätietoja on kohdassa [Tuotantosolujen ja kuormituskeskusten määrittäminen](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-production-bom"></a>Tuotannon tuoterakenteen luominen  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tuotannon tuoterakenne** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Jos haluat muokata tuoterakennetta, aseta **Tila**-kentän arvoksi **Uusi** tai **Kehityksen alla**. Jos haluat aktivoida tuoterakenteen, aseta **Tila**-kentän arvoksi **Hyväksytty**.  

    Siirry tuotannon tuoterakennerivien täyttämiseen.
5. Valitse **Tyyppi**-kentästä, onko tällä tuoterakennerivillä tavallinen nimike vai tuotannon tuoterakenne. Jos rivillä on tuotannon tuoterakenne, tämän on oltava jokin järjestelmään jo määritetyistä hyväksytyistä tuotannon tuoterakenteista.  
6.  Valitse **Nro**-kenttään haluttu nimike tai tuotannon tuoterakenne (tai kirjoita numero kenttään).  
7.  Määritä **Määrä per** -kenttään, monta yksikköä nimikettä tarvitaan päänimikkeeseen (esimerkiksi 4 rengasta yhteen autoon).  
8.  **Hukka-%**-kenttään voit antaa komponenteista hukkatavaraksi tuotannon aikana joutuvan prosenttiosuuden. Kun vapautetun tuotantotilauksen komponentit ovat valmiita kulutettaviksi, lisätään tämä prosenttiosuus oletettuun määrään (**Kulutusmäärä**-kenttään) tuotantopäiväkirjassa. Lisätietoja on kohdassa [Kulutuksen ja tuotoksen rekisteröiminen](production-how-to-register-consumption-and-output.md).  

    > [!NOTE]  
    >  Tämä hukkaprosentti viittaa komponentteihin, jotka joutuvat hukkatavaraksi tuotannon aikana (varastosta poimittaessa), kun taas reititysrivien hukkaprosentti viittaa hukkatavaraksi ennen varastointia joutuvaan tuotokseen.  

9.  Määritä **Reitityslinkin koodi** -kenttään koodi, joka liittää komponentin tiettyyn toimintoon. Lisätietoja on ohjeaiheen [Uusien reititysten luominen](production-how-to-create-routings.md) kohdassa Reitityslinkkien luominen.
10. Voit kopioida rivit tuotannon tuoterakenteesta valitse aiemmin luodut rivit **Kopioi tuoterakenne** -toiminnolla.  
11.  Hyväksy tuotannon tuoterakenne.  
12.  Voit nyt liittää uuden tuotannon tuoterakenteen kyseisen päänimikkeen korttiin. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).  

> [!NOTE]  
>  Voit laskea nimikkeen vakiokustannukset nimikkeen kortista valitsemalla ensin **Tuotanto**-toiminnon ja sitten **Laske Vakiokustannus** -toiminnon.  

## <a name="to-create-a-new-versions-of-a-production-bom"></a>Tuotannon tuoterakenteiden uusien versioiden luominen
Tuotannon tuoterakenteen uusia versioita käytetään esimerkiksi silloin, kun nimike vaihdetaan toiseen nimikkeeseen tai silloin, kun asiakas pyytää tuotteesta erikoisversiota. Versioperiaate mahdollistaa tuotannon tuoterakenteen useiden versioiden hallinnan. Tuotannon tuoterakenteen version rakenne vastaa tuotannon tuoterakenteen rakennetta. Perusero on versioiden ajallinen voimassaolo. Voimassaolon määrittää aloituspäivämäärä.  

Aloituspäivämäärä osoittaa alun jaksolle, jolloin kyseinen versio on voimassa. Aloituspäivämäärä on myös suodatuskriteeri laskennoille ja arvioinneille. Tuoterakenteen versio on voimassa niin kauan kuin seuraava versio tulee voimaan sen aloituspäivämäärän perusteella.  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tuotannon tuoterakenne** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse ensin kopioitava tuotannon tuoterakenne ja sitten **Versiot**-toiminto.  
3.  Valitse **Kotisivu**-välilehden **Uusi**-ryhmässä **Uusi**.  
4. Täytä tarvittavat kentät.
5. Anna **Versiokoodi**-kentässä version yksilöivä tunniste. Kaikenlaisten numero- ja kirjainyhdistelmien käyttö on sallittua.  

    Vasta luodulle versiolle määritellään automaattisesti tilaksi **Uusi.**
6. Kun tuoterakenteen versio on valmis, **Tila**-kentän asetuksena on **Hyväksytty**.  

Version voimassaoloajan määrittää **Aloituspvm**-kenttä.  

> [!NOTE]  
>  Käytä nimikkeen päätietojen osaa tuotannon tuoterakenteessa valitsemalla **Nimike** **Tyyppi**-kentässä. Jos nimikkeellä on myös tuotannon tuoterakenne (jolloin nimikekortin **Tuotannon tuoterakenteen nro** -kenttä on täytetty), myös tämä tuotannon tuoterakenne otetaan huomioon.  
>   
>  Valitse **Tuotannon tuoterakenne** -vaihtoehto, jos haluat käyttää rivillä tuotannon haamutuoterakennetta.  
>   
>  Tuotannon haamutuoterakenteet auttavat tuotteiden rakenteistamisessa. Tämä tuotannon tuoterakenteen tyyppi ei johda koskaan valmiiseen tuotteeseen, vaan sitä käytetään ainoastaan riippuvaisen tarpeen määrittämisessä. Tuotannon haamutuoterakenteilla ei ole omia nimikkeen päätietoja.

## <a name="quantity-calculation-formula-on-production-boms"></a>Tuotannon tuoterakenteiden määrän laskentakaava  
Määrän laskennassa otetaan huomioon eri dimensiot, jotka myös annetaan tuotannon tuoterakenteen riveille. Dimensiot viittaavat vastaavan nimikkeen tilausyksikköön. Dimensioiksi voidaan syöttää pituus, leveys, syvyys ja paino.  

Laskentakaava-, Pituus-, Leveys-, Syvyys- ja Paino- sarakkeet eivät näy, koska vain jotkin käyttäjät käyttävät niitä. Jos haluat käyttää määrän laskentaa, nämä sarakkeet tulee ensin tuoda näkyviin.  

Laskentakaava määrittää yksittäisten komponenttien suhteen. Laskentakaavaksi ovat saatavilla seuraavat mahdollisuudet:  

-  **Tyhjä** – dimensioita ei oteta huomioon. (Määrä = Määrä per.)  
-  **Pituus** - Määrä = Määrä per * Pituus  
-  **Pituus x Leveys**- Määrä = Määrä per * Pituus x Leveys  
-  **Pituus x Leveys x Syvyys**- Määrä = Määrä per x Pituus x Leveys x Syvyys  
-  **Paino** – Määrä = Määrä per x Paino  

### <a name="example"></a>Esimerkki  
Tuotannon tuoterakenteelle tarvitaan seitsemänkymmentä metalliosaa, joiden dimensioiden pituus = 0,20 m ja leveys = 0,15 m. Arvot annetaan seuraavalla tavalla: Laskentakaava = Pituus x Leveys, Pituus = 20, Leveys = 15, Määrä per = 70. Määräksi annetaan Määrä per x Pituus x Leveys eli Määrä = 70 x 0,20 m x 0,15 m = 2,1 m2.  

## <a name="see-also"></a>Katso myös  
[Uusien reititysten luominen](production-how-to-create-routings.md)   
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Suunnittelu](production-planning.md)   
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

