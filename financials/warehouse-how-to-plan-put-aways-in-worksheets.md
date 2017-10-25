---
title: "Hyllytysten suunnitteleminen työkirjoissa | Microsoft Docs"
description: "Jos sijainnissa on määritetty sekä hyllytyksen että vastaanoton käsittely pakolliseksi ja haluat suunnitella hyllytysohjeita useille vastaanotoille – sen asemesta, että työntekijät noudattaisivat ohjelman luomia ohjeita erillisille kirjatuille vastaanotoille – voit käyttää hyllytystyökirjaa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 99c3ac10460a62ee23294cfd0d8c25709c37901b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-plan-put-aways-in-worksheets"></a>Hyllytysten suunnitteleminen työkirjoissa
Jos sijainnissa on määritetty sekä hyllytyksen että vastaanoton käsittely pakolliseksi ja haluat suunnitella hyllytysohjeita useille vastaanotoille sen sijaan, että työntekijät noudattaisivat ohjelman luomia ohjeita erillisille kirjatuille vastaanotoille, voit käyttää hyllytystyökirjaa.  

Jos haluat määrittää fyysisen varastoinnin niin, että vastaanottorivit ovat saatavilla hyllytystyökirjassa heti kirjaamisen jälkeen, lisää valintamerkki  **Käytä hyllytystyökirjaa** -kenttään sijaintikortin **F. varastointi** -pikavälilehdessä. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

Jos et valitse tätä kenttää, ohjelma luo automaattisesti hyllytysohjeita vastaanotoille, kun ne kirjataan.  

> [!NOTE]  
>  Riippumatta sijaintikortin **Käytä hyllytystyökirjaa** -kentän tilasta, voit saada hyllytysohjerivejä (kirjattuja vastaanottorivejä) hyllytystyökirjaan tekemällä seuraavaa:  
>   
>  1.  Paina **F. varastoinnin hyllytys** -ikkunassa Ctrl+D. Nyt voit poistaa koko hyllytysohjeen tai valita rivit käsiteltäviksi työkirjassa ja poistaa ne.  
> 2.  Jatka prosessia niin monessa hyllytyksessä kuin haluat siihen asti, kun olet poistanut kaikki rivit, joiden parissa haluat työskennellä työkirjassa. Napsauta nyt **Hyllytystyökirjat** ja jatka suunnittelua.  

## <a name="to-plan-instructions-in-the-put-away-worksheet"></a>Ohjeiden suunnittelu hyllytystyökirjassa  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Hyllytystyökirja** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Hae f. varastoinnin asiakirjat** -toiminto. Näyttöön tulee **Hyllytyksen valinta** -ikkuna.  

    Näet kaikki kirjatut vastaanotot ja rekisteröidyt sisäiset hyllytykset, jotka on lähetetty eteenpäin hyllytys-funktioon, mukaan lukien ne, joille hyllytysohjeita on jo luotu. Asiakirjat, joissa on hyllytysrivejä, joita ei ole täysin hyllytetty ja rekisteröity, ei näytetä tässä luettelossa.  

3. Valitse asiakirjat, joita haluat käsitellä työkirjassa. Voit käsitellä samaan aikaan useista asiakirjoista peräisin olevia rivejä.  

    > [!NOTE]  
    >  Jos yrität valita asiakirjan (vastaanoton tai hyllytysasiakirjan), jolle olet jo luonut ohjeita kaikkien rivien osalta, ohjelma ilmoittaa, että mitään käsiteltävää ei ole.  

4. Järjestä rivit haluamallasi tavalla täyttämällä **Järjestämistapa**-kenttä.  

    > [!NOTE]  
    >  ( Rivien järjestelytapa työkirjassa ei siirry automaattisesti hyllytysohjeeseen, mutta samat järjestelymahdollisuudet – sekä yksi lisää, varastopaikan luokittelu – on saatavilla hyllytysohjeissa. Työkirjassa suunnittelemasi rivijärjestys voidaan siten luoda helposti uudelleen silloin, kun luodaan hyllytysohjeita, tai järjestelemällä hyllytysohjeissa.)  

5.  Täytä **Käsiteltävä määrä** -kenttä. Valitse **Täytä autom. käsitelt. määrä** -toiminto tai täytä kentät manuaalisesti.  
6.  Muokkaa rivejä tarvittaessa manuaalisesti. Voit poistaa rivejä esimerkiksi, jos jotkin nimikkeet tulee hyllyttää varastopaikkaan, joka on kaukana muiden nimikkeiden varastopaikoista.  

    > [!NOTE]  
    >  Poistettavat rivit poistetaan vain kyseisestä työkirjasta, ei hyllytyksen valintaluettelosta.  

7.  Valitse **Luo hyllytys** -toiminto. Näyttöön tulevassa **Luo asiakirja** -ikkunassa voit lisätä lisätietoja luotavaan hyllytykseen:  

    -   Hyllytyksen voi määritellä tietylle työntekijälle.  
    -   Hyllytysohjerivit voidaan lajitella samoin kuin työkirjassa tai varastopaikan luokittelun mukaan. Kun järjestelet varastopaikan luokittelun mukaisesti, Ota-rivit tulevat ensimmäisiksi, koska useimmilla vastaanoton varastopaikoille on varastopaikan luokittelu 0, ja Aseta-rivit tulevat viimeisiksi alkaen varastopaikoista, joilla on alin varastopaikan luokittelu. Jos olet järjestänyt fyysisen varaston niin, että samanlaisen varastopaikan luokittelun varastopaikat ovat vierekkäin, rivien järjesteleminen tällä tavalla säästää lopulta työvaiheita varaston työntekijöiltä.  
    -   Voit valita, että ohjeessa eivät näy välissä olevia rivejä, jotka luotiin ohjelman erotellessa suuremman mittayksikön pienemmiksi mittayksiköiksi (lisää rasti **Aseta erottelusuodatin** -kenttään). Lisätietoja on kohdassa [Toimintaohje: Irtotavaran ohjatulla hyllytyksellä ja poiminnalla tapahtuvan automaattisen erottelun ottaminen käyttöön] (warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    -   Voit valita, että ohjelma ei täytä automaattisesti hyllytysohjeiden **Käsiteltävä määrä** -kenttää.  
    -   Voit tulostaa asiakirjan heti.  

8.  Valitse **OK**, niin ohjelma luo hyllytyksen vaatimustesi mukaisesti.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

