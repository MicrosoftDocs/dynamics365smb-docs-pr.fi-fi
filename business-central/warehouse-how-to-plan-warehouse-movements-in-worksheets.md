---
title: Fyysisen varaston siirtojen suunnitteleminen työkirjassa | Microsoft Docs
description: Varastosiirrot suunnitellaan työkirjassa käyttämällä varastopaikan täydennystoimintoa tai suunnittelemalla manuaalisesti rivit, jotka haluat luoda siirto-ohjeiksi.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1ec80435211b139868bf62ddf0ce269a802d2abc
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534046"
---
# <a name="plan-warehouse-movements-in-worksheets"></a>Fyysisen varaston siirtojen suunnitteleminen työkirjoissa

Varastosiirrot suunnitellaan työkirjassa käyttämällä varastopaikan täydennystoimintoa tai suunnittelemalla manuaalisesti rivit, jotka haluat luoda siirto-ohjeiksi.  

## <a name="to-calculate-a-replenishment-movement"></a>Täydennyssiirtojen laskeminen

Kun fyysinen varasto toimittaa nimikkeitä asiakkaille, varastopaikoista, joilla on korkein varastopaikan luokittelu, nimikkeiden määrä vähenee jatkuvasti. Voit täyttää näitä korkean luokittelun poimintavarastopaikkoja muiden varastopaikkojen nimikkeillä, suorittamalla **Laske var.paikan täydennys** -toiminto **Siirtotyökirja**-sivulla.

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston siirron työkirja** ja valitse sitten liittyvä linkki.  
2.  Valitse **Laske var.paikan täydennys**-toiminto.  

    [!INCLUDE[prod_short](includes/prod_short.md)] luo rivejä, joissa ohjataan tarkasti, miten nimikkeet on siirrettävä matalan luokittelun varastopaikoista korkean luokittelun varastopaikkoihin.  

    > [!NOTE]  
    >  Varaston siirtoa ehdotetaan FEFO:n mukaan, kun aktivoit  **Luo siirto** -toiminnon, jos seuraavat edellytykset täyttyvät kohteelle:  
    >   
    >  -   Nimikkeellä on vanhenemispäivämäärä.  
    > -   Sijaintikortin **FEFO-poiminta**-valintaruutu on valittuna.  
    > -   Sijaintikortin **Var.paikka pakollinen** -valintaruutu on valittuna.  
    > -   **Alue koodista**- ja **Var.paikasta**-kentät ovat tyhjiä.  

    Lisätietoja on kohdassa [FEFO-poiminta](warehouse-picking-by-fefo.md).  

3.  Tarkasta rivit ja muuta niitä tarvittaessa tai poista joitain niistä, jos kaikkien niiden suorittamiseen ei ole aikaa.  
4.  Valitse **Luo siirto** -toiminto, jos haluat tehdä fyysisen varastoinnin ohjeen työntekijöiden toiminnoksi.  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a>Voit siirtää yhden varastopaikan tai useiden varastopaikkojen koko sisällön Hae var.paikan sisältö -toiminnon avulla seuraavasti:

Voit myös käyttää muiden siirtojen suunnitteluun fyysisessä varastossa varastosiirtotyökirjaa. Kun haluat esimerkiksi sijoittaa nimikkeitä varastopaikkaan laaduntarkastusta varten, voit käyttää tämän toiminnon suunnittelemiseen varastosiirtotyökirjaa. Muodosta sitten ohjeet työntekijälle luomalla varastosiirto.  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston siirron työkirja** ja valitse sitten liittyvä linkki.  
2.  Valitse **Hae var.paikan sisältö** -toiminto. Pyyntösivun avulla voit suodattaa varastopaikat ja nimikkeet, jotka näkyvät varastosiirtotyökirjan riveillä.  
3.  Kirjoita eräajon pyyntösivulla asianmukaisten kenttien arvot. Jos haluat esimerkiksi nähdä sijainnin tietyn alueen kaikkien varastopaikkojen sisällön, kirjoita arvo **Alueen koodi** -kenttään. Jos haluat hakea tietyn nimikkeen sisältävien varastopaikkojen rivit, kirjoita arvo **Nimikkeen nro** -kenttään.  

    > [!NOTE]  
    >  Nimikkeitä ei voi siirtää manuaalisesti Vastaanotto-tyyppiseen varastopaikkaan eikä myöskään pois tällaisesta varastopaikasta. Tämä johtuu siitä, että Vastaanotto-tyyppisen varastopaikan nimikkeet on rekisteröitävä hyllytettäviksi, ennen kuin ne voivat olla osa saatavilla olevaa varastoa.  

4.  Jos haet useita rivejä, valitse **Lajittele**, valitse haluamasi työkirjan rivien lajittelutapa ja valitse sitten **OK**.  

    > [!NOTE]  
    >  Siirtorivit noudetaan FEFO:n mukaan, kun aktivoit **Hae var.paikan sisältö** -toiminnon, jos seuraavat edellytykset täyttyvät kohteelle:  
    >   
    >  -   Nimikkeellä on vanhenemispäivämäärä.  
    > -   Sijaintikortin **FEFO-poiminta**-valintaruutu on valittuna.  
    > -   Sijaintikortin **Var.paikka pakollinen** -valintaruutu on valittuna.  
    > -   **Alue koodista**- ja **Var.paikasta**-kentät ovat tyhjiä.  

5.  Tee haluamasi muutokset täydentämällä haettuja rivejä. Kullakin siirrettävällä nimikkeellä on oltava arvo **Nimikkeen nro**-, **Var.paikasta**-, **Varastopaikkakoodiin**- ja  **Määrä**-kentissä.  
6.  Poista epätäydelliset rivit, joita olet käyttänyt viitetietoina.  
7.  Kun varastosiirtotyökirjan rivit vastaavat tapaa, jolla haluat varastotyöntekijän tekevän siirron, luo ohjeet työntekijälle valitsemalla **Luo siirto** -toiminto.  

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/move-items/)

## <a name="see-also"></a>Katso myös

[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
