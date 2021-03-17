---
title: Hyllytysten suunnitteleminen työkirjoissa | Microsoft Docs
description: Jos sijainnissa on määritetty sekä hyllytyksen että vastaanoton käsittely pakolliseksi ja haluat suunnitella hyllytysohjeita useille vastaanotoille, voit käyttää hyllytystyökirjaa sen sijaan, että työntekijät noudattaisivat sovelluksen luomia ohjeita erillisille kirjatuille vastaanotoille.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1cf1a782a0c36e3f87935c8b2b965deb4ad04e9a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383648"
---
# <a name="plan-put-aways-in-worksheets"></a>Hyllytysten suunnitteleminen työkirjoissa
Jos sijainnissa on määritetty sekä hyllytyksen että vastaanoton käsittely pakolliseksi ja haluat suunnitella hyllytysohjeita useille vastaanotoille, voit käyttää hyllytystyökirjaa sen sijaan, että työntekijät noudattaisivat sovelluksen luomia ohjeita erillisille kirjatuille vastaanotoille.  

Jos haluat määrittää fyysisen varastoinnin niin, että vastaanottorivit ovat saatavilla hyllytystyökirjassa heti kirjaamisen jälkeen, lisää valintamerkki  **Käytä hyllytystyökirjaa** -kenttään sijaintikortin **F. varastointi** -pikavälilehdessä. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

Jos et valitse tätä kenttää, sovellus luo automaattisesti hyllytysohjeita vastaanotoille, kun ne kirjataan.  

> [!NOTE]  
>  Riippumatta sijaintikortin **Käytä hyllytystyökirjaa** -kentän tilasta, voit saada hyllytysohjerivejä (kirjattuja vastaanottorivejä) hyllytystyökirjaan tekemällä seuraavaa:  
>   
>  1.  Paina **F. varastoinnin hyllytys** -sivulla näppäinyhdistelmää Ctrl+D. Nyt voit poistaa koko hyllytysohjeen tai valita rivit käsiteltäviksi työkirjassa ja poistaa ne.  
> 2.  Jatka prosessia niin monessa hyllytyksessä kuin haluat siihen asti, kun olet poistanut kaikki rivit, joiden parissa haluat työskennellä työkirjassa. Napsauta nyt **Hyllytystyökirjat** ja jatka suunnittelua.  

## <a name="to-plan-instructions-in-the-put-away-worksheet"></a>Ohjeiden suunnittelu hyllytystyökirjassa  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Hyllytystyökirja** ja valitse sitten liittyvä linkki.  
2.  Valitse **Hae f. varastoinnin asiakirjat** -toiminto. Näyttöön tulee **Hyllytyksen valinta** -sivu.  

    Näet kaikki kirjatut vastaanotot ja rekisteröidyt sisäiset hyllytykset, jotka on lähetetty eteenpäin hyllytys-funktioon, mukaan lukien ne, joille hyllytysohjeita on jo luotu. Asiakirjat, joissa on hyllytysrivejä, joita ei ole täysin hyllytetty ja rekisteröity, ei näytetä tässä luettelossa.  

3. Valitse asiakirjat, joita haluat käsitellä työkirjassa. Voit käsitellä samaan aikaan useista asiakirjoista peräisin olevia rivejä.  

    > [!NOTE]  
    >  Jos yrität valita asiakirjan (vastaanoton tai hyllytysasiakirjan), jolle olet jo luonut ohjeita kaikkien rivien osalta, sovellus ilmoittaa, että mitään käsiteltävää ei ole.  

4. Järjestä rivit haluamallasi tavalla täyttämällä **Järjestämistapa**-kenttä.  

    > [!NOTE]  
    >  Rivien järjestelytapa työkirjassa ei siirry automaattisesti hyllytysohjeeseen, mutta samat järjestelymahdollisuudet – sekä yksi lisää, varastopaikan luokittelu – on saatavilla hyllytysohjeissa. Työkirjassa suunnittelemasi rivijärjestys voidaan siten luoda helposti uudelleen silloin, kun luodaan hyllytysohjeita, tai järjestelemällä hyllytysohjeissa.  

5.  Täytä **Käsiteltävä määrä** -kenttä. Valitse **Täytä autom. käsitelt. määrä** -toiminto tai täytä kentät manuaalisesti.  
6.  Muokkaa rivejä tarvittaessa manuaalisesti. Voit poistaa rivejä esimerkiksi, jos jotkin nimikkeet tulee hyllyttää varastopaikkaan, joka on kaukana muiden nimikkeiden varastopaikoista.  

    > [!NOTE]  
    >  Poistettavat rivit poistetaan vain kyseisestä työkirjasta, ei hyllytyksen valintaluettelosta.  

7.  Valitse **Luo hyllytys** -toiminto. Näyttöön tulevalla **Luo asiakirja** -sivulla voi lisätä lisätietoja luotavaan hyllytykseen:  

    -   Hyllytyksen voi määritellä tietylle työntekijälle.  
    -   Hyllytysohjerivit voidaan lajitella samoin kuin työkirjassa tai varastopaikan luokittelun mukaan. Kun järjestelet varastopaikan luokittelun mukaisesti, Ota-rivit tulevat ensimmäisiksi, koska useimmilla vastaanoton varastopaikoille on varastopaikan luokittelu 0, ja Aseta-rivit tulevat viimeisiksi alkaen varastopaikoista, joilla on alin varastopaikan luokittelu. Jos olet järjestänyt fyysisen varaston niin, että samanlaisen varastopaikan luokittelun varastopaikat ovat vierekkäin, rivien järjesteleminen tällä tavalla säästää lopulta työvaiheita varaston työntekijöiltä.  
    -   Voit valita, että näkyvissä ei ole välissä olevia rivejä, jotka luotiin sovelluksen erotellessa suuremman mittayksikön pienemmiksi mittayksiköiksi valitsemalla **Aseta erottelusuodatin** -kenttä. Lisätietoja on kohdassa [Irtotavaran ohjatulla hyllytyksellä ja poiminnalla tapahtuvan automaattisen erottelun ottaminen käyttöön](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md)  
    -   Voit valita, että ohjelma ei täytä automaattisesti hyllytysohjeiden **Käsiteltävä määrä** -kenttää.  
    -   Voit tulostaa asiakirjan heti.  

8.  Valitse **OK**, niin sovellus luo hyllytyksen vaatimustesi mukaisesti.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]