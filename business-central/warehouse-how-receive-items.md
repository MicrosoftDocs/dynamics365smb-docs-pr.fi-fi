---
title: Nimikkeiden vastaanottaminen | Microsoft Docs
description: "Kun nimikkeet saapuvat varastolle, jossa on käytössä fyysisen varastoinnin vastaanoton käsittely, niiden vastaanoton käynnistäneestä vapautetusta lähdeasiakirjasta tulee hakea rivit."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 52290609eca12eb09f9d1065b1013baeee5b8a5b
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="receive-items"></a>Nimikkeiden vastaanottaminen
Kun nimikkeet saapuvat fyysiseen varastoon, johon ei ole määritetty fyysisen varaston vastaanottokäsittelyä, vastaanotto vain kirjataan liittyvään asiakirjaan, kuten ostotilaukseen, myyntipalautustilaukseen tai saapuvaan siirtotilaukseen.

Kun nimikkeet saapuvat varastoon, jossa on käytössä fyysisen varastoinnin vastaanoton käsittely, rivit on noudettava niiden vastaanoton käynnistäneestä vapautetusta lähdeasiakirjasta. Jos käytössä on varastopaikkoja, voit hyväksyä kentässä olevan oletusvarastopaikan. Jos nimikettä ei ole käytetty aiemmin varastossa, kirjoita varastopaikka, johon nimike tulisi hyllyttää.  

## <a name="to-receive-items-with-a-purchase-order"></a>Nimikkeiden vastaanottaminen ostotilauksella
Seuraavaksi käsitellään, miten nimikkeitä vastaanotetaan ostotilauksella. Vaiheet ovat samankaltaiset myyntipalautustilauksille ja siirtotilauksille.  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostotilaukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa aiemmin luotu ostotilaus tai luo uusi myyntitilaus. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).
3. Anna **Vastaanotettava määrä** -kenttään vastaanotettu määrä.

    **Määrä vast.otettu** -kentän arvo päivitetään. Jos kyse on osavastaanotosta, arvo on pienempi kuin **Määrä**-kentän arvo.
4. Valitse **Kirjaa**-toiminto.

## <a name="to-receive-items-with-a-warehouse-receipt"></a>Nimikkeiden vastaanottaminen fyysisen varasto vastaanottona
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **F.var. vast.otot** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  

    Täytä **Yleinen**-pikavälilehden kentät. Kun haet lähdeasiakirjan rivit, ohjelma kopioi otsikon tiedot kullekin riville.  

    Jos fyysisen varaston määrityksissä on käytössä ohjattu hyllytys ja poiminta ja jos sijainnilla on oletusalue ja oletusvarastopaikka vastaanotoille, **Alueen koodi**- ja **Varastopaikkakoodi**-kentät täytetään automaattisesti, mutta voit muuttaa niiden arvoja tarpeen mukaan.  

    > [!NOTE]  
    >  Jos haluat vastaanottaa nimikkeitä, joiden fyysisen varastoinnin luokkakoodi ei ole sama kuin asiakirjan otsikon **Varastopaikkakoodi**-kentässä olevan varastopaikan luokkakoodi, poista otsikon **Varastopaikkakoodi**-kentän sisältö ennen lähdeasiakirjan rivien hakemista nimikkeitä varten.  
3.  Valitse **Hae lähdeasiakirjat** -toiminto. Näyttöön tulee **Lähdeasiakirjat**-ikkuna.

    Voit käyttää uuden tai avoimen fyysisen varastoinnin vastaanoton **Suod. lähdeasiakirj. saamisek.** -ikkunaa hakiessasi vastaanotettava tai toimitettavat nimikkeet määrittävän vapautetun lähdeasiakirjan rivit.

    1. Valitse **Käytä suodat. kun haet lähd.d** -toiminto.  
    2. Määritä uusi suodatin antamalla kuvaileva koodi **Koodi**-kenttään ja valitse **Muokkaa**-toiminto.  
    3. Määritä ne lähdeasiakirjan rivien tyypit, jotka haluat hakea, täyttämällä soveltuvat suodatinkentät.  
    4. Valitse **Aja**-toiminto.  

    Kaikki julkaistut lähdeasiakirjan rivit, jotka täyttävät suodatusehdot, on nyt lisätty **F. varastoinnin vastaanotto** -ikkunassa, josta aktivoit suodatustoiminnon.  

    Määrittämäsi suodatinyhdistelmät tallennetaan **Suod. lähdeasiakirj. saamisek.** -ikkunaan tulevaa käyttöä varten. Voit tehdä niin monta suodatinyhdistelmää kuin haluat. Voit muuttaa ehtoja milloin tahansa valitsemalla **Muokkaa**-toiminnon.

4.  Valitse lähdeasiakirjat, joille haluat vastaanottaa nimikkeitä, ja valitse sitten **OK**.  

    Lähdeasiakirjojen rivit näkyvät **F. varastoinnin vastaanotto** -ikkunassa. Ohjelma on jo täyttänyt **Vastaanotettava määrä** -kenttään jokaisen rivin avoimen määrän, mutta määrää voi muuttaa tarpeen mukaan. Jos olet poistanut **Yleinen**-pikavälilehden **Varastopaikkakoodi**-kentän sisällön ennen rivien hakemista, kirjoita kullekin vastaanottoriville asianmukainen varastopaikkakoodi.  

    > [!NOTE]  
    >  Jos haluat, että **Vastaanotettava määrä** -kentän kaikki rivit täytetään arvolla nolla, valitse **Poista vastaanotettava määrä** -toiminto. Voit täyttää sen uudelleen avoimella määrällä valitsemalla **Täytä autom. vast.ot. määrä** -toiminto.  

    > [!NOTE]  
    >  Et voi vastaanottaa enempää nimikkeitä kuin määrä **Avoin määrä** -kentässä lähdeasiakirjan rivillä ilmaisee. Vastaanota enemmän nimikkeitä hakemalla toinen lähdeasiakirja, jossa on rivi nimikkeelle, käyttämällä suodatintoimintoa hakeaksesi lähdeasiakirjat ja nimike.  

5.  Kirjaa fyysisen varastoinnin vastaanotto. Ohjelma päivittää lähdeasiakirjojen määräkentät ja kirjaa nimikkeet osaksi yrityksen varastoa.  

Jos käytössä on fyysisen varastoinnin hyllytys, ohjelma lähettää vastaanottorivit fyysisen varastoinnin hyllytystoimintoon. Vastaanotettuja nimikkeitä ei voi poimia ennen kuin ne on hyllytetty. Ohjelma tunnistaa vastaanotetut nimikkeet saatavilla olevaksi varastoksi vasta sitten, kun hyllytys on rekisteröity.  

Jos fyysisen varastoinnin hyllytys ei ole käytössä mutta käytät varastopaikkoja, ohjelma kirjaa nimikkeiden hyllytyksen lähdeasiakirjan rivillä määritettyyn varastopaikkaan.  

> [!NOTE]  
>  Jos käytät **Kirjaa ja tulosta** -toimintoa, vastaanoton kirjauksen yhteydessä tulostetaan hyllytysohje, joka kertoo, mihin nimikkeet sijoitetaan varastossa.  
>   
>  Jos sijainnissa on käytössä ohjattu hyllytys ja poiminta, hyllytysmalleja käytetään parhaan nimikkeiden hyllytyspaikan laskemisessa. Tämä tulostetaan sitten hyllytysohjeeseen.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

