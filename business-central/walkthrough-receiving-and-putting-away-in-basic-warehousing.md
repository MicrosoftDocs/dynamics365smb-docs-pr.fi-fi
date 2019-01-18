---
title: "Vaihekuvaus – Vastaanotto ja hyllytys fyysisen varastoinnin perusmäärityksissä | Microsoft Docs"
description: "Business Central -sovelluksessa vastaanoton ja hyllytyksen saapuvat prosessit voidaan suorittaa neljällä tavalla eri toimintojen avulla varastotason monimutkaisuuden mukaan."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 0ba61572a237e177b763b7b8a2e13ca7ec93eea4
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Vaihekuvaus: Vastaanotto ja hyllytys fyysisen varastoinnin perusmäärityksissä
[!INCLUDE[d365fin](includes/d365fin_md.md)]issa vastaanoton ja hyllytyksen saapuvat prosessit voidaan suorittaa neljällä tavalla eri toimintojen avulla varastotason monimutkaisuuden mukaan.  

|Tapa|Saapuva prosessi|Varastopaikat|Vastaanotot|Hyllytykset|Monimutkaisuustaso (katso [Rakennetiedot: Fyysisen varaston asetukset](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|L|Vastaanoton ja hyllytyksen kirjaaminen tilausriviltä|X|||2|  
|B|Vastaanoton ja hyllytyksen kirjaaminen varaston hyllytysasiakirjasta|||X|3|  
|N|Kirjaa vastaanotto ja hyllytys fyysisen varastoinnin vastaanottoasiakirjasta||X||4/5/6|  
|P|Kirjaa vastaanotto fyysisen varastoinnin vastaanottoasiakirjasta ja kirjaa hyllytys varaston hyllytysasiakirjasta||X|X|4/5/6|  

Lisätietoja on kohdassa [Rakennetiedot: Saapuvan fyysisen varastoinnin virta](design-details-inbound-warehouse-flow.md).  

Seuraavassa vaihekuvauksessa kuvataan edellisen taulukon menetelmää B.  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta  
Jos fyysisen varastoinnin perusmääritykset määrittävät sijainnin edellyttämään hyllytyksen muttei vastaanoton käsittelyä, saapuvien lähdeasiakirjojen hyllytys- ja vastaanottotiedot tallennetaan ja kirjataan **Varastohyllytys**-sivulla. Saapuva lähdeasiakirja voi olla ostotilaus, myyntipalautustilaus, saapuva siirtotilaus tai tuotantotilaus jonka tuotos odottaa hyllytystä.

> [!NOTE]
> Vaikka asetusten nimenä on **Vaadi poiminta** ja **Vaadi hyllytys**, voit silti kirjata vastaanottoja ja toimituksia suoraan lähdeasiakirjoista sijainneissa, joissa olet valinnut nämä valintaruudut.  

Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä.  

-   HOPEA-sijainnin määrittäminen varastopaikan hyllytykseen.  
-   HOPEA-sijainnin määrittäminen varastopaikan käsittelyyn.  
-   Oletusvarastopaikan määrittäminen nimikkeelle LS-81. (LS-75 on jo määritetty CRONUSISSA.)  
-   Luo ostotilaus toimittajalle 10000 40 kaiuttimesta.  
-   Tarkistetaan, että hyllytyksen varastopaikat määritetään ennalta asetusten avulla.  
-   Ostotilauksen vapauttaminen varaston käsittelyyn.  
-   Varastohyllytyksen julkaistusta lähdeasiakirjasta luominen  
-   Tarkistetaan, että hyllytyksen varastopaikat peritään ostotilauksesta.  
-   Rekisteröidään fyysisen varastoinnin siirtoa varastoon ja kirjataan samanaikaisesti lähdeostotilauksen ostokuittia.  

## <a name="roles"></a>Roolit  
Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:  

-   Varastopäällikkö  
-   Ostaja  
-   Varastotyöntekijä  

## <a name="prerequisites"></a>Vaatimukset  
Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:  

-   CRONUS Finland Oy on asennettu.  
-   Tee itsestäsi fyysisen varaston työntekijä HOPEISESSA sijainnissa tekemällä seuraavat toimet:  

    1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Varaston työntekijät** ja valitse sitten liittyvä linkki.  
    2.  Valitse ensin **Käyttäjätunnus**-kenttä ja valitse oma käyttäjätilisi **Käyttäjät**-sivulla.  
    3.  Kirjoita **Sijaintikoodi**-kenttään HOPEA.  
    4.  Valitse **Oletus**-kenttä.  

## <a name="story"></a>Taustatietoja  
Ellen on CRONUS Finland Oy:n varastopäällikkö ja hän luo ostotilauksen, jossa on 10 yksikköä LS-75-nimikettä ja 30 yksikköä LS-81-nimikettä, toimittajalta 10000 toimitettavaksi HOPEISEEN varastoon. Kun toimitus saapuu varastoon, varastotyöntekijä Joakim hyllyttää nimikkeitä niille määritettyihin oletusvarastopaikkoihin. Kun Joakim kirjaa hyllytyksen, nimikkeet kirjataan vastaanotetuksi varastoon, ja ne ovat käytettävissä myyntiä tai muita kysyntää varten.  

## <a name="setting-up-the-location"></a>Sijainnin määrittäminen  
 **Sijaintikortti**-sivun asetuksissa määritellään yrityksen varaston työnkulut.  

### <a name="to-set-up-the-location"></a>Sijainnin määrittäminen  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten liittyvä linkki.  
2.  Avaa asianmukaisen HOPEA sijainnin kortti.  
3.  Valitse **Vaadi hyllytys** -valintaruutu.  

    Siirry määrittämään oletusvarastopaikka kahdelle nimikenumerolla, jotka valvovat, missä ne on hyllytetty.  

4.  Valitse **Varastopaikat**-toiminto.  
5.  Valitse varastopaikan S-01-0001 ensimmäinen rivi ja valitse sitten **Sisältö**-toiminto.  

    Huomaa **Varastopaikan sisältö** -sivulla, että nimike LS-75 on jo määritetty sisällöksi varastopaikassa S-01-0001.  

6.  Valitse **Uusi**-toiminto.  
7.  Valitse **Kiinteä**- ja **Oletus**-kentät.  
8.  Anna **Nimikenro**-kentässä LS-81.  

## <a name="creating-the-purchase-order"></a>Ostotilauksen luominen  
Ostotilaukset ovat yleisin saapuvien lähdeasiakirjojen tyyppi.  

### <a name="to-create-the-purchase-order"></a>Ostotilausten luominen  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Luo ostotilaus toimittajalle 10000 (23.1.) käsittelypäivämääränä seuraavien ostontilausrivien kanssa.  

    |Nimike|Sijaintikoodi|Varastopaikan koodi|määrä.|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|HOPEINEN|S-01-0001|10|  
    |LS_81|HOPEINEN|S-01-0001|30|  

    > [!NOTE]  
    >  Varastopaikkakoodi lisätään automaattisesti "Sijainnin määrittäminen" -osassa suorittamiesi määritysten mukaisesti.  

    Siirry ja ilmoita varastolle, että ostotilaus on valmis varaston käsittelyyn, kun toimitus saapuu.  

4.  Valitse **Vapauta**-toiminto.  

    Kaiuttimien toimitus toimittajalta 10000 on saapunut HOPEISEEN varastoon, ja John ryhtyy hyllyttämään niitä.  

## <a name="receiving-and-putting-the-items-away"></a>Nimikkeiden vastaanottaminen ja hyllyttäminen  
Voit hallita **Varastohyllytys**-sivulla kaikkia tietyn lähdeasiakirjan saapuvia varastotoimintoja, kuten ostotilausta.  

### <a name="to-receive-and-put-the-items-away"></a>Nimikkeiden vastaanottaminen ja hyllyttäminen  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston hyllytykset** ja valitse sitten liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Valitse ensin **Lähdeasiakirja**-kenttä ja sitten **Ostotilaus**.  
4.  Valitse **Lähteen nro** -kentässä toimittajalta 10000 tehdyn oston rivi ja valitse sitten **OK**.  

    Valitse vaihtoehtoisesti **Toiminnot**-välilehden **Funktiot**-ryhmässä **Hae lähdeasiakirja**, ja valitse ostotilaus.  

5.  Valitse **Täytä autom. käsitelt. määrä** -toiminto.  

    Vaihtoehtoisesti voit antaa **Käsiteltävä määrä** -kentässä 10 ja 30 kahdelle varastohyllytysriville.  

6.  Valitse ensin **Kirjaa**-toiminto, sitten **Vastaanotto**-toiminto ja lopuksi **OK**.  

    40 kaiutinta on nyt rekisteröity hyllytetyiksi varastopaikasta S-01-0001, ja luodaan positiivinen nimiketapahtuma, joka heijastaa kirjattua ostotoimitusta.  

## <a name="see-also"></a>Katso myös  
 [Nimikkeiden hyllyttäminen varastohyllytyksen avulla](warehouse-how-to-put-items-away-with-inventory-put-aways.md)   
 [Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)   
 [Komponenttien siirtäminen toiminta-alueelle fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)   
 [Poiminta tuotantoon tai kokoonpanoon](warehouse-how-to-pick-for-production.md)   
 [Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)   
 [Rakennetiedot: saapuvan fyysisen varastoinnin virta](design-details-inbound-warehouse-flow.md)   
 [Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

