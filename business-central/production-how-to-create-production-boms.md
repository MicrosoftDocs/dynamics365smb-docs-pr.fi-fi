---
title: Tuotannon tuoterakenteiden luominen
description: 'Lue, miten voit luoda tuotannon tuoterakenteen, tuotannon tuoterakenteen uudet versiot ja käyttää määrälaskentakaavaa.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'production bom, bills of material,'
ms.search.form: '911, 912, 917, 9287, 99000786, 99000787, 99000788, 99000789, 99000795, 99000797, 99000800, 99000809, 99000811, 99000812, 99000818'
ms.date: 06/22/2021
ms.author: bholtorf
---
# <a name="create-production-boms" />Tuotannon tuoterakenteiden luominen

Tuotannon tuoterakenne sisältää perustiedot päänimikkeen tuotannossa käytettävistä komponenteista ja osakokoonpanoista. Kun päänimikkeelle luodaan tuotantotilaus, tuotannon tuoterakenne ohjaa materiaalitarpeiden laskentaa **Tuot.til. komponentit** -sivulla näkyvällä tavalla.

[!INCLUDE[prod_short](includes/prod_short.md)] tukee myös kokoonpanon tuoterakenteita. Voit käyttää kokoonpanotilauksia, kun teet komponenteista loppunimikkeitä yksinkertaisella prosessilla. Tämä prosessi voidaan toteutetaan vähintään yhdellä perusresurssilla, joka ei ole kuormituskeskus eikä tuotantosolu, tai ilman resursseja. Kokoonpanoprosessi voi olla esimerkiksi kahden viinipullon ja yhden kahvipaketin valinta ja niiden pakkaaminen lahjaksi. Lisätietoja on kohdassa [Kokoonpanon tuoterakenteet tai tuotannon tuoterakenteet](inventory-how-work-boms.md#assembly-boms-or-production-boms).  

> [!TIP]
> **Contoso Coffee -esittelytiedot** -sovellus sisältää esittelytuotteita useille tuotannon tuoterakenteen skenaarioille, joita voidaan käyttää testiympäristössä myös kokeilujakson aikana. Lisätietoja Contoso Coffee -tiedoista ja vaihekuvauksien etsimisestä eri skenaarioissa on kohdassa [Contoso Coffee -esittelytietojen esittely](contoso-coffee/contoso-coffee-intro.md).

Seuraavat toimet on oltava tehtynä ennen reitityksen määrittämistä:  

- Tuotannossa mukana olevien päänimikkeiden nimikekortit on luotu. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).
- Tuotantoresurssit on määritetty. Lisätietoja on kohdassa [Tuotantosolujen ja kuormituskeskusten määrittäminen](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-production-bom" />Tuotannon tuoterakenteen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotannon tuoterakenteet** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Jos haluat muokata tuoterakennetta, aseta **Tila**-kentän arvoksi **Uusi** tai **Kehityksen alla**. Jos haluat aktivoida tuoterakenteen, aseta **Tila**-kentän arvoksi **Hyväksytty**.  

    Siirry tuotannon tuoterakennerivien täyttämiseen.
5. Valitse **Tyyppi**-kentästä, onko tällä tuoterakennerivillä tavallinen nimike vai tuotannon tuoterakenne. Jos rivillä on tuotannon tuoterakenne, tämän on oltava jokin järjestelmään jo määritetyistä hyväksytyistä tuotannon tuoterakenteista.  
6. Valitse **Nro**-kenttään haluttu nimike tai tuotannon tuoterakenne (tai kirjoita numero kenttään).  
7. Määritä **Määrä per** -kenttään, monta yksikköä nimikettä tarvitaan päänimikkeeseen (esimerkiksi 4 rengasta yhteen autoon).  
8. **Hukka-%**-kenttään voit antaa komponenteista hukkatavaraksi tuotannon aikana joutuvan prosenttiosuuden. Kun vapautetun tuotantotilauksen komponentit ovat valmiita kulutettaviksi, lisätään tämä prosenttiosuus oletettuun määrään (**Kulutusmäärä**-kenttään) tuotantopäiväkirjassa. Lisätietoja on kohdassa [Kulutuksen ja tuotoksen rekisteröiminen](production-how-to-register-consumption-and-output.md).  

    > [!NOTE]  
    >  Tämä hukkaprosentti viittaa komponentteihin, jotka joutuvat hukkatavaraksi tuotannon aikana (varastosta poimittaessa), kun taas reititysrivien hukkaprosentti viittaa hukkatavaraksi ennen varastointia joutuvaan tuotokseen.  

9. Määritä **Reitityslinkin koodi** -kenttään koodi, joka liittää komponentin tiettyyn toimintoon. Lisätietoja on kohdassa [Reitityslinkkien luominen](production-how-to-create-routings.md#to-create-routing-links).
10. Voit kopioida rivit tuotannon tuoterakenteesta valitse aiemmin luodut rivit **Kopioi tuoterakenne** -toiminnolla.  
11. Hyväksy tuotannon tuoterakenne.  
12. Voit nyt liittää uuden tuotannon tuoterakenteen kyseisen päänimikkeen korttiin. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).  

> [!NOTE]  
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)] Voit laskea nimikkeen vakiokustannukset nimikkeen kortista valitsemalla ensin **Tuotanto**-toiminnon ja sitten **Laske vakiokustannus** -toiminnon.  

## <a name="to-create-a-new-version-of-a-production-bom" />Tuotannon tuoterakenteiden uusien versioiden luominen

Tuotannon tuoterakenteen uusia versioita käytetään esimerkiksi silloin, kun nimike vaihdetaan toiseen nimikkeeseen tai silloin, kun asiakas pyytää tuotteesta erikoisversiota. Versioperiaate mahdollistaa tuotannon tuoterakenteen useiden versioiden hallinnan. Tuotannon tuoterakenteen version rakenne vastaa tuotannon tuoterakenteen rakennetta. Perusero on versioiden ajallinen voimassaolo. Voimassaolon määrittää aloituspäivämäärä.  

Aloituspäivämäärä osoittaa alun jaksolle, jolloin kyseinen versio on voimassa. Aloituspäivämäärä on myös suodatuskriteeri laskennoille ja arvioinneille. Tuoterakenteen versio on voimassa niin kauan kuin seuraava versio tulee voimaan sen aloituspäivämäärän perusteella.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotannon tuoterakenteet** ja valitse sitten vastaava linkki.  
2. Valitse ensin kopioitava tuotannon tuoterakenne ja sitten **Versiot**-toiminto.  
3. Valitse **Uusi**-toiminto.  
4. Täytä tarvittavat kentät.
5. Anna **Versiokoodi**-kentässä version yksilöivä tunniste. Kaikenlaisten numero- ja kirjainyhdistelmien käyttö on sallittua.  

    Vasta luodulle versiolle määritellään automaattisesti tilaksi **Uusi.**
6. Kun tuoterakenteen versio on valmis, **Tila**-kentän asetuksena on **Hyväksytty**.  

Version voimassaoloajan määrittää **Aloituspvm**-kenttä.  

> [!NOTE]  
> Käytä nimikkeen päätietojen osaa tuotannon tuoterakenteessa valitsemalla **Nimike** **Tyyppi**-kentässä. Jos nimikkeellä on myös tuotannon tuoterakenne (jolloin nimikekortin **Tuotannon tuoterakenteen nro** -kenttä on täytetty), myös tämä tuotannon tuoterakenne otetaan huomioon.  
>
> Valitse **Tuotannon tuoterakenne** -vaihtoehto, jos haluat käyttää rivillä tuotannon haamutuoterakennetta.  
>
> Tuotannon haamutuoterakenteet auttavat tuotteiden rakenteistamisessa. Tämä tuotannon tuoterakenteen tyyppi ei johda koskaan valmiiseen tuotteeseen, vaan sitä käytetään ainoastaan riippuvaisen tarpeen määrittämisessä. Tuotannon haamutuoterakenteilla ei ole omia nimikkeen päätietoja.

## <a name="quantity-calculation-formula-on-production-boms" />Tuotannon tuoterakenteiden määrän laskentakaava

Määrän laskennassa otetaan huomioon eri dimensiot, jotka myös annetaan tuotannon tuoterakenteen riveille. Dimensiot viittaavat vastaavan nimikkeen tilausyksikköön. Dimensioiksi voidaan syöttää pituus, leveys, syvyys ja paino.  

Laskentakaava-, Pituus-, Leveys-, Syvyys- ja Paino- sarakkeet eivät näy, koska vain jotkin käyttäjät käyttävät niitä. Jos haluat käyttää määrän laskentaa, nämä sarakkeet tulee ensin tuoda näkyviin.  

Laskentakaava määrittää yksittäisten komponenttien suhteen. Laskentakaavaksi ovat saatavilla seuraavat mahdollisuudet:  

- **Tyhjä** – dimensioita ei oteta huomioon. (Määrä = Määrä per.)  
- **Pituus** - Määrä = Määrä per * Pituus  
- **Pituus x Leveys**- Määrä = Määrä per * Pituus x Leveys  
- **Pituus x Leveys x Syvyys**- Määrä = Määrä per x Pituus x Leveys x Syvyys  
- **Paino** – Määrä = Määrä per x Paino  
- **Kiinteä määrä** - Määrä = Määrä per

> [!NOTE]
> **Kiinteä määrä** -laskentakaava varmistaa, että komponentin kulutus on sama riippumatta hukkatavaran tai tuotoksen määristä. Kun tuotantotilauksen komponenteille määritetään **Laskentakaava**-kentän arvoksi **Kiinteä määrä**, **Oletettu määrä** -kentän arvo on aina sama kuin **Määrä per** -kentässä. Samalla rivillä määritetty hukkatavaran prosentti ohitetaan. **Saatavuus tuoterakennetason mukaan** -raportti noudattaa kiinteää määrää. Raportissa näkyy nimike pullonkaulana, jos saatavilla oleva määrä on pienempi kuin **Määrä pääkohdetta kohti** -kentässä. **Kykenee valmistamaan päänimikettä**- ja **Kykenee valmistamaan tärkeintä nimikettä** -kentät ovat aina tyhjiä riippumatta käytettävissä olevasta määrästä. Vakiokustannusten laskentaan sisällytetään myös kiinteämääräinen määrä. Tuotetun nimikkeen eräkoko vaikuttaa yhdelle nimikkeelle kohdistettuun kustannukseen.

### <a name="example" />Esimerkki

Tuotannon tuoterakenne vaatii 70 metalliosaa, joiden dimensioiden pituus = 0,20 m ja leveys = 0,15 m. Arvot annetaan seuraavalla tavalla: Laskentakaava = Pituus x Leveys, Pituus = 20, Leveys = 15, Määrä per = 70. Määräksi annetaan Määrä per x Pituus * Leveys eli Määrä = 70 x 0,20 m x 0,15 m = 2,1 m2.  

## <a name="see-also" />Katso myös

[Uusien reititysten luominen](production-how-to-create-routings.md)  
[Tuotevarianttien hallinta](inventory-item-variants.md)  
[Vaihekuvaus: Variantit](contoso-coffee/manufacturing/variants.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)  
[Suunnittelu](production-planning.md)  
[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)  
[Kokoonpanon tuoterakenteiden käyttäminen](assembly-how-work-assembly-boms.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
