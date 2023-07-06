---
title: Rakennetiedot –Täsmäytys pääkirjanpidon kanssa | Microsoft Docs
description: 'Tässä ohjeaiheessa käsitellään täsmäytys pääkirjanpidon kanssa varastotapahtumia kirjattaessa. Näitä tapahtumia ovat esimerkiksi tapahtumat, tuotannon tuotos ja negatiiviset muutokset.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, reconciliation, general ledger, inventory'
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-reconciliation-with-the-general-ledger"></a><a name="design-details-reconciliation-with-the-general-ledger"></a><a name="design-details-reconciliation-with-the-general-ledger"></a>Rakennetiedot: täsmäytys pääkirjanpidon kanssa
Kun kirjaat varastotapahtumia, kuten myyntitoimituksia, tuotannon tuloksia tai negatiivisia muutoksia, ohjelma kirjaa varaston määrien muutokset nimiketapahtumiin ja varaston arvojen muutokset arvotapahtumiin. Prosessin seuraava vaihe on kirjata varastoarvot pääkirjanpidon varastotileille.  

Inventointipäiväkirjan ja pääkirjanpidon voi täsmäyttää kahdella eri tavalla:  

* Manuaalisesti suorittamalla **Kirjaa varaston kustannus KP:oon** -eräajo.  
* Automaattisesti aina, kun kirjaat varastotapahtuman.  

## <a name="post-inventory-cost-to-gl-batch-job"></a><a name="post-inventory-cost-to-gl-batch-job"></a><a name="post-inventory-cost-to-gl-batch-job"></a>Kirjaa varaston kust. KP:oon -eräajo
Kun suoritat **Kirjaa varaston kustannus KP:oon** -eräajon, KP-tapahtumat luodaan arvotapahtumien perusteella. Voit tehdä yhteenvedon pääkirjanpidon tapahtumista jokaisen arvotapahtuman osalta tai luoda pääkirjanpidon tapahtumat jokaiselle kirjauspäivämääräyhdistelmälle, sijaintikoodille, varaston kirjausryhmälle, yleisen liiketoiminnan kirjausryhmälle ja yleisen tuotteen kirjausryhmälle.  

Pääkirjan kirjausten tiliöintipäivät on määritetty vastaavan arvokirjauksen tiliöintipäiväksi lukuun ottamatta sitä, kun arvokirjaus osuu suljetulle kirjanpitokaudelle. Tässä tapauksessa arvotapahtuma ohitetaan ja sinun on muutettava joko pääkirjanpidon asetusta tai käyttäjäasetusta kirjaamisen asettamiseksi käyttöön päivämääräalueella.  

Tämän **Kirjaa varaston kustannus KP:oon** -eräajon suoritus saattaa aiheuttaa virheitä, koska dimension asetukset puuttuvat tai ne eivät ole yhteensopivia. Jos dimension asetuksissa havaitaan virheitä eräajon aikana, eräajo ohittaa nämä virheet ja käyttää arvotapahtuman dimensioita. Muiden virheiden kohdalla eräajo jättää arvotapahtumat kirjaamatta ja listaa ne raportin lopussa osassa **Ohitetut tapahtumat**. Voit kirjata nämä tapahtumat korjattuasi ensin virheet. Saat virheluettelon näkyviin ennen eräajoa, kun suoritat **Kirjaa varaston kustannukset kirjanpitoon - Testaa** -raportin. Tämä raportti luetteloi kaikki testikirjauksen aikana havaitut virheet. Voit korjata virheet ja suorittaa sitten varaston kustannusten kirjauksen eräajon niin, että tapahtumia ei ohiteta.  

## <a name="automatic-cost-posting"></a><a name="automatic-cost-posting"></a><a name="automatic-cost-posting"></a>Automaattinen kustann. kirjaus
Voit määrittää pääkirjanpidon kustannusten kirjaamisen automaattiseksi varastotapahtuman kirjaamisen yhteydessä valitsemalla **Varastonhallinnan asetukset** -sivun **Automaattinen kustann. kirjaus** -valintaruudun. Pääkirjan kirjauksen tiliöintipäivä on sama kuin nimikkeen pääkirjan kirjauksen tiliöintipäivä.  

## <a name="account-types"></a><a name="account-types"></a><a name="account-types"></a>Tilityypit
Täsmäytyksessä varastoarvot kirjataan taseen varastotilille. Sama summa, mutta kumousmerkillä, tiliöidään asianmukaiseen tasapainotustiliin. Yleensä vastatili on tuloslaskelmatili. Kun kirjaat kulutukseen tai tuotokseen liittyvän välittömän kustannuksen, vastatili on tasetili. Nimiketapahtuman ja arvotapahtuman tyyppi määrittää sen, mille kirjanpitotilille kirjaus tehdään.  

Kirjaustyyppi määrittää sen, mihin pääkirjan tiliin tiliöinti tehdään. Tämä määritetään joko nimiketapahtuman määrän etumerkillä tai arvotapahtuman arvostetulla määrällä, koska määrillä on aina sama etumerkki. Esimerkiksi myyntitapahtuma positiivisella määrällä kuvaa myynnin aiheuttamaa varaston arvon laskua ja myyntitapahtuma negatiivisella määrällä kuvaa myyntipalautuksen aiheuttamaa varaston arvon lisäystä.  

### <a name="example"></a><a name="example"></a><a name="example"></a>Esimerkki
Seuraavassa esimerkissä kuvataan polkupyörän ketju, joka on valmistettu ostetuista lenkeistä. Tämä esimerkki osoittaa, miten eri pääkirjanpidon tilityyppejä käytetään tavallisessa skenaariossa.  

**Varastonhallinnan asetukset** -sivulla on valittu **Oletettu kust. kirjaus KP:oon** -valintaruutu ja seuraavat asetukset on määritetty.  

Seuraavassa taulukossa esitetään, kuinka lenkki on määritetty nimikekortissa.  

|Kentän asetukset|Arvo|  
|-----------------|-----------|  
|**Arvostusmenetelmä**|Vakio|  
|**Vakiokustannus**|1.00 PVA|  
|**Yleiskustannus (arvo)**|0.02 PVA|  

Seuraavassa taulukossa esitetään, kuinka ketju on määritetty nimikekortissa.  

|Kentän asetukset|Arvo|  
|-----------------|-----------|  
|**Arvostusmenetelmä**|Vakio|  
|**Vakiokustannus**|150.00 PVA|  
|**Yleiskustannus (arvo)**|25.00 PVA|  

Seuraavassa taulukossa esitetään, kuinka työkeskus on määritetty työkeskuskortissa.  

|Kentän asetukset|Arvo|  
|-----------------|-----------|  
|**Välitön yksikkökustannus**|2.00 PVA|  
|**Välillinen kustannusprosentti**|10|  

##### <a name="scenario"></a><a name="scenario"></a><a name="scenario"></a>Esimerkkitilanne
1. Käyttäjä ostaa 150 lenkkiä ja kirjaa ostotilauksen vastaanotetuksi. (Osto)  
2. Käyttäjä kirjaa ostotilauksen laskutetuksi. Tämä luo kohdistettavan yleiskustannussumman 3,00 (PVA) ja erosumman 18,00 (PVA). (Osto)  

    1. Tilapäistilit on selvitetty. (Osto)  
    2. Välittömät kustannukset tiliöidään. (Osto)  
    3. Välilliset kustannukset lasketaan ja tiliöidään. (Osto)  
    4. Ostovarianssi on laskettu ja tiliöity (vain peruskustannusnimikkeille). (Osto)  
3. Käyttäjä myy yhden ketjun ja kirjaa myyntitilauksen toimitetuksi. (Myynti)  
4. Käyttäjä kirjaa myyntitilauksen laskutetuksi. (Myynti)  

    1. Tilapäistilit on selvitetty. (Myynti)  
    2. Myytyjen tuotteiden kustannus (MTK) kirjataan. (Myynti)  

        ![Myynnin KP-tilikirjausten tulokset.](media/design_details_inventory_costing_3_gl_posting_sales.png "Myynnin KP-tilikirjausten tulokset")  
5. Käyttäjä kirjaa kulutukseksi 150 lenkkiä, joka on yhden ketjun tuottamisessa käytettyjen lenkkien määrä. (Materiaalin kulutus)  

    ![Materiaalin KP-tilikirjausten tulokset.](media/design_details_inventory_costing_3_gl_posting_material.png "Materiaalin KP-tilikirjausten tulokset")  
6. Tuotantosolulta meni 60 minuuttia ketjun tekemiseen. Käyttäjä kirjaa muunnoksen kustannukset. (Kulutus, kapasiteetti)  

    1. Välittömät kustannukset tiliöidään. (Kulutus, kapasiteetti)  
    2. Välilliset kustannukset lasketaan ja tiliöidään. (Kulutus, kapasiteetti)  

        ![Kapasiteetin KP-tilikirjausten tulokset.](media/design_details_inventory_costing_3_gl_posting_capacity.png "Kapasiteetin KP-tilikirjausten tulokset")  
7. Käyttäjä kirjaa yhden ketjun oletetut kustannukset. (Tuotto)  
8. Käyttäjä tekee tuotantotilauksen valmiiksi ja suorittaa **Muuta kustannuksia - Nimiketapahtumat** -eräajon. (Tuotto)  

    1. Tilapäistilit on selvitetty. (Tuotto)  
    2. Välittömät kustannukset siirretään WIP-tililtä varastotilille. (Tuotto)  
    3. Välilliset kustannukset (yleiskustannukset) siirretään välillisten kustannusten tililtä varastotilille. (Tuotto)  
    4. Tuloksena on erosumma 157,00 (PVA). Varianssit lasketaan vain vakiokustannuksen omaaville nimikkeille. (Tuotto)  

        ![Tuotosten KP-tilikirjausten tulokset.](media/design_details_inventory_costing_3_gl_posting_output.png "Tuotosten KP-tilikirjausten tulokset")  

        > [!NOTE]  
        >  Yksinkertaisuuden vuoksi näytetään vain yksi vaihtelutili. Todellisuudessa on olemassa viisi erilaista tiliä:  
        >   
        >  * Materiaalin vaihtelu  
        >  * Kapasit. vaihtelu  
        >  * Kapasit. yleiskust. vaihtelu  
        >  * Alihankintavaihtelu  
        >  * Tuotannon yleiskustannusten vaihtelu  

9. Käyttäjä määrittää ketjun hinnaksi 140,00 (PVA) aiemman 150,00 (PVA):n sijaan. (Muutos/uudelleenarvostus/pyöristys/siirto)  

    ![Muutosten KP-tilikirjausten tulokset.](media/design_details_inventory_costing_3_gl_posting_adjustment.png "Muutosten KP-tilikirjausten tulokset")  

Saat lisätietoja tilityyppien välisestä suhteesta ja erityyppisistä arvotapahtumista kohdasta [Rakennetiedot: pääkirjanpidon tilit](design-details-accounts-in-the-general-ledger.md).  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös
[Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)   
[Rakennetiedot: oletetun kustannuksen kirjaus](design-details-expected-cost-posting.md)   
[Rakennetiedot: Kustannusten muuttaminen](design-details-cost-adjustment.md)
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Rahoitus](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
