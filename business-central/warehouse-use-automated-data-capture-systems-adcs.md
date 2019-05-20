---
title: ACDS (Automated Data Capture Systems) -järjestelmän käyttäminen | Microsoft Docs
description: Automaattista tiedonkeruujärjestelmää (ADCS) voidaan käyttää rekisteröimään kaikki nimikkeiden siirrot fyysisessä varastossa ja rekisteröimään kaikki päiväkirjatoiminnot, joihin sisältyvät määrän muutokset fyysisen varastoinnin nimikepäiväkirjassa, inventoinneissa ja uudelleenluokitteluissa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 20ef2d88bb5f96326962efb53fd724b8fc706dc5
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248483"
---
# <a name="use-automated-data-capture-systems-adcs"></a>ADCS (Automated Data Capture System) -järjestelmä

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] -vakioversiossa ADCS toimii vain paikallisissa käyttöönotoissa. Microsoft-kumppani voi kuitenkin mahdollistaa verkkokäyttöönotot esimerkiksi PowerAppsin avulla.

Automaattista tiedonkeruujärjestelmää (ADCS) voidaan käyttää rekisteröimään kaikki nimikkeiden siirrot fyysisessä varastossa ja rekisteröimään kaikki päiväkirjatoiminnot, joihin sisältyvät määrän muutokset fyysisen varastoinnin nimikepäiväkirjassa, inventoinneissa ja uudelleenluokitteluissa.  

ADCS:n käyttöön on annettava kullekin nimikkeelle, joka on tallennettu varastoon, nimikkeen tunnus. Sinun täytyy myös määrittää pienoislomakkeet, kannettavat toiminnot, tiedon siirrot, ja määrittää eritysasetukset kentille, jotka määrittävät ADCS-asetuksia. Voit määrittää käytetäänkö ADCS:ää varaston sijaintikortissa.

Fyysisen varastoinnin tarpeiden pohjalta pienoislomakkeen asetuksissa määritetään tietojen määrä, joka näytetään tietyssä kannettavassa laitteessa. Seuraavat ovat esimerkkejä tiedoista, joita voit näyttää:  

- Tiedot [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman taulukoista, kuten lista poiminta-asiakirjoista, joista käyttäjä voi valita.  
- Tekstitiedot.  
- Vahvistuksia tai virhesanomia suoritetuista toiminnoista, jotka käyttäjä on tehnyt ja rekisteröinyt kannettavalla laitteella.

Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeaiheessa [ADCS (Automated Data Capture System) -järjestelmän määrittäminen](/dynamics-nav/Configuring-Automated-Data-Capture-System).

## <a name="to-set-up-a-warehouse-to-use-adcs"></a>Fyysisen varaston määrittäminen ADCS-järjestelmän käyttämistä varten  
ADCS:n käytössä on määritettävä, mitkä fyysisen varaston sijainnit käyttävät tekniikkaa.  

> [!NOTE]  
>  Suosittelemme, että et määritä varastoa käyttämään automaattista tiedonkeruujärjestelmää, jos varastossa on myös varastopaikan kapasiteettitapa.

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse liittyvä linkki.
2.  Valitse luettelosta fyysinen varasto, jossa haluat ottaa käyttöön ADCS-järjestelmä, ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Sijainnin kortti** -sivulla **Käytä ADCS** -valintaruutu.  

## <a name="to-specify-an-item-to-use-adcs"></a>Nimikkeen määrittäminen käyttämään ADCS-järjestelmää  
Kullekin varastonimikkeelle, jota haluat käyttää ADCS:n kanssa, on määritettävä tunnuskoodia, joka yhdistää sen nimikkeen numeroon. Esimerkiksi nimikkeen viivakoodia voi käyttää tunnuskoodina. Nimikkeellä voi olla myös useita tunnuskoodeja. Saatat pitää tätä hyödyllisenä siinä tapauksessa, että nimike on käytettävissä eri mittayksiköissä, kuten kappaleissa ja kuormalavoissa. Määritä tässä tapauksessa jokaiselle tunnuskoodi.    

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.  
2.  Valitse luettelosta nimike, joka on osa ADCS-ratkaisua, ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Nimikkeen kortti** -sivulla **Tunnisteet**-toiminto.
4. Valitse **Nimiketunnisteet**-sivulla **Uusi**-toiminto.
5. Määritä **Koodi**-kentässä nimikkeen tunnus. Tunnus voi olla esimerkiksi nimikkeen viivakoodinumero.  

    Voit myös kirjoittaa **Varianttikoodi** ja **Mittayksikkö** -koodi.  

6. Syötä tarvittaessa jokaiselle nimikkeelle useita koodeja.
7. Valitse **OK**-painike.  
8.  Voit tarkastella tietoja avaamalla **Nimiketunnisteet**-sivu valitsemalla **Tunnistimen koodi** -kenttä.

## <a name="to-add-an-adcs-user"></a>ADCS-käyttäjän lisääminen  
Voit lisätä minkä tahansa käyttäjän Automated Data Capture System (ADCS) -järjestelmän käyttäjäksi. Kun teet tämän, käyttäjän on myös annettava salasana. Voit myös antaa yhteyden, joka määrittää ADCS-käyttäjän fyysisen varastoinnin työntekijäksi. ADCS-käyttäjän salasana voi olla eri kuin käyttäjän Windows-kirjautumissalasana. Lisätietoja on kohdassa [Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ADCS-käyttäjät** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3.  Kirjoita **Nimi**-kenttään käyttäjän nimi. Nimi voi olla enintään 20 merkkiä pitkä, välilyönnit mukaan lukien.  
4.  Anna **Salasana**-kenttään salasana. Salasana on peitetty.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user"></a>Varastotyöntekijän määrittäminen ADCS-käyttäjäksi  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston työntekijät** ja valitse sitten liittyvä linkki.  
2.  Lisää tarvittaessa uusi varastotyöntekijä. Lisätietoja on kohdassa [Varastotyöntekijöiden määrittäminen](warehouse-how-to-set-up-warehouse-employees.md).  
3.  Valitse **Muokkaa luetteloa** -toiminto.  
4.  Valitse varastotyöntekijä luettelosta. Valitse **ADCS-käyttäjä** -kentässä avattavan nuolipainike ja valitse luettelosta ADCS-käyttäjän nimi.  

> [!NOTE]  
>  Työntekijän oletusvaraston on oltava sellainen, jossa käytetään ADCS-järjestelmää.

## <a name="to-create-and-customize-miniforms"></a>Pienoislomakkeiden luominen ja mukauttaminen
Pienoislomakkeiden avulla voit kuvailla tietoja, jotka haluat esittää käsilaitteesta. Voit luoda pienoislomakkeita, jotka tukevat nimikkeiden poiminnan fyysisen varastoinnin toimintoja. Pienoislomakkeen luotuasi voit lisätä siihen toimintoja yleisiä toimenpiteitä varten, jotka käyttäjä tekee kannettavissa laitteissa, esimerkiksi siirtyminen ylös- tai alaspäin rivillä.  

Ota käyttöön tai muuta pienoislomakkeen toiminto luomalla uusi koodiyksikkö tai muokkaamalla aiemmin luotua suorittamaan vaadittu toiminto tai vastaus. Lue lisätietoja ADCS-toiminnoista tutkimalla koodiyksikköjä, kuten 7705, joka on sisäänkirjautumistoiminnon käsittelyn koodiyksikkö. Koodiyksikkö 7705 näyttää, kuinka korttityyppinen pienoislomake toimii.  

### <a name="to-create-a-miniform-for-adcs"></a>Luo ADCS-pienoislomake  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pienoislomakkeet** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3.  Anna **Koodi**-kenttään pienoislomakkeen koodi. Voit antaa arvot myös muihin kenttiin.  

    Valitsemalla **Käynnistä Miniform** -valintaruudun määritetään, että pienoislomake on ensimmäinen lomake, jonka käyttäjä näkee kirjautumisen yhteydessä.  

4.  Määritä **Rivit**-pikavälilehdessä pienoislomakkeessa näkyvät kentät. Järjestys, jossa syötät rivit on sama, jossa rivit näkyvät kannettavalla päätteellä.  

Pienoislomakkeen luonnin jälkeen luodaan seuraavaksi toiminnot ja liitetään toiminnot näppäimistön syötteille.  

### <a name="to-add-support-for-a-function-key"></a>Tuen lisääminen toimintonäppäimeen  
1.  Lisää seuraavan esimerkin mukainen koodi .xsl-tiedostoon laajennusta varten. Tämä luo toiminnon **F6**-näppäimelle. Näppäinyhdistelmätiedot voi saada laitteen valmistajalta.  
    ```xml  
    <xsl:template match="Function[.='F6']">  
      <Function Key1="27" Key2="91" Key3="49" Key4="55" Key5="126" Key6="0"><xsl:value-of select="."/></Function>  
    </xsl:template>  
    ```  
2.  Avaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in kehitysympäristössä taulukko 7702 ja lisää uutta näppäintä vastaava koodi. Luo tässä esimerkissä avain, jonka nimi on **F6**.  
3.  Lisää C/AL-koodi asianmukaiseen funktioon pienoislomakekohtaisessa koodiyksikössä toimintonäppäimen käsittelemiseksi.  

### <a name="to-customize-miniform-functions"></a>Mukauta pienoislomakkeen toiminnot  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pienoislomakkeet** ja valitse sitten liittyvä linkki.  
2.  Valitse pienoislomake luettelosta ja valitse sitten **Muokkaa**-toiminto.  
3.  Valitse **Toiminnot**-toiminto.  
4.  Valitse avattavasta **Toimintokoodi**-luettelosta sitä toimintoa vastaava koodi, jonka haluat liittää pienoislomakkeeseen. Voit valita esimerkiksi ESC-vaihtoehdon, joka liittää toiminnon ESC-näppäimen painallukseen.  

Muokkaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in kehitysympäristössä **Käsittelevä koodiyksikkö** -kentän koodia, jos haluat luoda koodin tarvittavan toiminnon tai vastauksen suorittamiseen tai muokata koodia.

Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeaiheessa [ADCS (Automated Data Capture System) -järjestelmän määrittäminen](/dynamics-nav/Configuring-Automated-Data-Capture-System).

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
