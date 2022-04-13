---
title: ADCS (Automated Data Capture System) -järjestelmä
description: Automaattisen tiedonkeruujärjestelmän (ADCS) avulla voit rekisteröidä nimikkeiden varaston siirron fyysisessä varastossa ja rekisteröidä joitakin päiväkirjan aktiviteetteja.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: barcode
ms.search.form: 7700, 7703, 7704, 7706, 7707, 7710, 9813, 9814
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: cf0ac9f90efe234b73d4509e50502ca37dcf458e
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514697"
---
# <a name="use-automated-data-capture-systems-adcs"></a>Käytä ADCS (Automated Data Capture System) -järjestelmää

> [!NOTE]
> Automaattinen tiedonkeruujärjestelmän (ADCS) ratkaisu tarjoaa [!INCLUDE[prod_short](includes/prod_short.md)]:lle keinon kommunikoida kannettavien laitteiden kanssa verkkopalveluiden avulla. Sinun on toimittava sellaisen Microsoft-palveluntarjoajan kanssa, joka pystyy tarjoamaan linkin Web-palvelun ja tietyn kannettavan laitteen välille. 

Automaattista tiedonkeruujärjestelmää (ADCS) voidaan käyttää rekisteröimään kaikki nimikkeiden siirrot fyysisessä varastossa ja rekisteröimään kaikki päiväkirjatoiminnot, joihin sisältyvät määrän muutokset fyysisen varastoinnin nimikepäiväkirjassa, inventoinneissa ja uudelleenluokitteluissa. ADCS sisältää yleensä viivakoodin skannauksen.

ADCS:n käyttöön on annettava kullekin nimikkeelle, joka on tallennettu varastoon, nimikkeen tunnus. Sinun täytyy myös määrittää pienoislomakkeet, kannettavat toiminnot, tiedon siirrot, ja määrittää eritysasetukset kentille, jotka määrittävät ADCS-asetuksia. Voit määrittää käytetäänkö ADCS:ää varaston sijaintikortissa.

Fyysisen varastoinnin tarpeiden pohjalta pienoislomakkeen asetuksissa määritetään tietojen määrä, joka näytetään tietyssä kannettavassa laitteessa. Seuraavat ovat esimerkkejä tiedoista, joita voit näyttää:  

- Tiedot [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman taulukoista, kuten lista poiminta-asiakirjoista, joista käyttäjä voi valita.  
- Tekstitiedot.  
- Vahvistuksia tai virhesanomia suoritetuista toiminnoista, jotka käyttäjä on tehnyt ja rekisteröinyt kannettavalla laitteella.

## <a name="to-enable-web-services-for-adcs"></a>Voit ottaa ADCS-verkkopalvelut käyttöön
Jotta voisit käyttää automaattista tiedonkeruujärjestelmää, sinun on otettava ADCS-verkkopalvelu käyttöön.  

## <a name="to-enable-and-publish-the-adcs-web-service"></a>ADCS-verkkopalvelun käyttöönotto ja julkaiseminen  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Verkkopalvelut** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.  
3. Lisää seuraavat tiedot **verkkopalvelut**-sivun uudelle riville:  

    |Kenttä|Arvo|  
    |---------------------------------|-----------|  
    |**Objektityyppi**|Codeunit|  
    |**Objektin tunnus**|7714|  
    |**Palvelun nimi**|ADCS **Tärkeää:** Sinun on annettava palvelulle nimeksi **ADCS**.|  

5. Valitse **Julkaistu**-valintaruutu.  
6. Valitse **OK**-painike.  

## <a name="to-set-up-a-warehouse-to-use-adcs"></a>Fyysisen varaston määrittäminen ADCS-järjestelmän käyttämistä varten  
ADCS:n käytössä on määritettävä, mitkä fyysisen varaston sijainnit käyttävät tekniikkaa.  

> [!NOTE]  
>  Suosittelemme, että et määritä varastoa käyttämään automaattista tiedonkeruujärjestelmää, jos varastossa on myös varastopaikan kapasiteettitapa.

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.
2.  Valitse luettelosta fyysinen varasto, jossa haluat ottaa käyttöön ADCS-järjestelmä, ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Sijainnin kortti** -sivulla **Käytä ADCS** -valintaruutu.  

## <a name="to-specify-an-item-to-use-adcs"></a>Nimikkeen määrittäminen käyttämään ADCS-järjestelmää  
Kullekin varastonimikkeelle, jota haluat käyttää ADCS:n kanssa, on määritettävä tunnuskoodia, joka yhdistää sen nimikkeen numeroon. Esimerkiksi nimikkeen viivakoodia voi käyttää tunnuskoodina. Nimikkeellä voi olla myös useita tunnuskoodeja. Saatat pitää tätä hyödyllisenä siinä tapauksessa, että nimike on käytettävissä eri mittayksiköissä, kuten kappaleissa ja kuormalavoissa. Määritä tässä tapauksessa jokaiselle tunnuskoodi.    

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2.  Valitse luettelosta nimike, joka on osa ADCS-ratkaisua, ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Nimikkeen kortti** -sivulla **Tunnisteet**-toiminto.
4. Valitse **Nimiketunnisteet**-sivulla **Uusi**-toiminto.
5. Määritä **Koodi**-kentässä nimikkeen tunnus. Tunnus voi olla esimerkiksi nimikkeen viivakoodinumero.  

    Voit myös kirjoittaa **Varianttikoodi** ja **Mittayksikkö** -koodi.  

6. Syötä tarvittaessa jokaiselle nimikkeelle useita koodeja.
7. Valitse **OK**-painike.  
8.  Voit tarkastella tietoja avaamalla **Nimiketunnisteet**-sivu valitsemalla **Tunnistimen koodi** -kenttä.

## <a name="to-add-an-adcs-user"></a>ADCS-käyttäjän lisääminen  
Voit lisätä minkä tahansa käyttäjän Automated Data Capture System (ADCS) -järjestelmän käyttäjäksi. Kun teet tämän, käyttäjän on myös annettava salasana. Voit myös antaa yhteyden, joka määrittää ADCS-käyttäjän fyysisen varastoinnin työntekijäksi. ADCS-käyttäjän salasana voi olla eri kuin käyttäjän Windows-kirjautumissalasana. Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md).

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ADCS-käyttäjät** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3.  Kirjoita **Nimi**-kenttään käyttäjän nimi. Nimi voi olla enintään 20 merkkiä pitkä, välilyönnit mukaan lukien.  
4.  Anna **Salasana**-kenttään salasana. Salasana on peitetty.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user"></a>Varastotyöntekijän määrittäminen ADCS-käyttäjäksi  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston työntekijät** ja valitse sitten vastaava linkki.  
2.  Lisää tarvittaessa uusi varastotyöntekijä. Lisätietoja on kohdassa [Varastotyöntekijöiden määrittäminen](warehouse-how-to-set-up-warehouse-employees.md).  
3.  Valitse **Muokkaa luetteloa** -toiminto.  
4.  Valitse varastotyöntekijä luettelosta. Valitse **ADCS-käyttäjä** -kentässä avattavan nuolipainike ja valitse luettelosta ADCS-käyttäjän nimi.  

> [!NOTE]  
>  Työntekijän oletusvaraston on oltava sellainen, jossa käytetään ADCS-järjestelmää.

## <a name="to-create-and-customize-miniforms"></a>Pienoislomakkeiden luominen ja mukauttaminen
Pienoislomakkeiden avulla voit kuvailla tietoja, jotka haluat esittää käsilaitteesta. Voit luoda pienoislomakkeita, jotka tukevat nimikkeiden poiminnan fyysisen varastoinnin toimintoja. Pienoislomakkeen luotuasi voit lisätä siihen toimintoja yleisiä toimenpiteitä varten, jotka käyttäjä tekee kannettavissa laitteissa, esimerkiksi siirtyminen ylös- tai alaspäin rivillä.  

> [!NOTE] 
> Ota käyttöön tai muuta pienoislomakkeen toiminto luomalla uusi codeunit **Käsittelevä codeunit** -kenttään suorittamaan vaadittu toiminto tai vastaus. Saat lisätietoja ADCS-toiminnosta tarkastelemalla codeuniteja, joita ovat esimerkiksi 7705, 7706, 7712 ja 7713.  

### <a name="to-create-a-miniform-for-adcs"></a>Luo ADCS-pienoislomake  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pienoislomakkeet** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3.  Anna **Koodi**-kenttään pienoislomakkeen koodi. Voit antaa arvot myös muihin kenttiin.  

    Valitsemalla **Käynnistä Miniform** -valintaruudun määritetään, että pienoislomake on ensimmäinen lomake, jonka käyttäjä näkee kirjautumisen yhteydessä.  

4.  Määritä **Rivit**-pikavälilehdessä pienoislomakkeessa näkyvät kentät. Järjestys, jossa syötät rivit on sama, jossa rivit näkyvät kannettavalla päätteellä.  

Pienoislomakkeen luonnin jälkeen luodaan seuraavaksi toiminnot ja liitetään toiminnot näppäimistön syötteille.  

### <a name="to-customize-miniform-functions"></a>Mukauta pienoislomakkeen toiminnot  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pienoislomakkeet** ja valitse sitten vastaava linkki.  
2.  Valitse pienoislomake luettelosta ja valitse sitten **Muokkaa**-toiminto.  
3.  Valitse **Toiminnot**-toiminto.  
4.  Valitse avattavasta **Toimintokoodi**-luettelosta sitä toimintoa vastaava koodi, jonka haluat liittää pienoislomakkeeseen. Voit valita esimerkiksi ESC-vaihtoehdon, joka liittää toiminnon ESC-näppäimen painallukseen.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]