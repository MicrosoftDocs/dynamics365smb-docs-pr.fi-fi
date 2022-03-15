---
title: Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä
description: Tässä aiheessa käsitellään suunnittelemattomia siirtoja, joita tehdään silloin, kun nimikkeitä täytyy siirtää sisäisten varastopaikkojen välillä, ilman että niillä on tiettyä kysyntää lähdeasiakirjasta.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 393, 7382
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 965a87d731a2e1d9cb2ae390add4536c77c6824c
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381034"
---
# <a name="move-items-ad-hoc-in-basic-warehouse-configurations"></a>Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä
Voit joskus joutua siirtämään nimikkeitä sisäisissä varastopaikoissa ilman, että vastaanotat tai toimitat varastopaikkoja tai ilman erityispyyntöä lähdeasiakirjasta. Voi suorittaa nämä suunnittelemattomat siirrot esimerkiksi silloin, jos haluat järjestellä fyysistä varastoa tuomalla nimikkeitä tarkastusalueelle tai siirtää lisänimikkeitä tuotantoalueelle ja sieltä pois ilman järjestelmäsuhdetta tuotantotilauksen lähdeasiakirjaan.  

Fyysisen varaston perusmäärityksissä eli sijainneissa, joissa käytetään **Var.paikka pakollinen** -asetuskenttiä ja mahdollisesti **Vaadi poiminta**- ja **Vaadi hyllytys** -asetuskenttiä, voi rekisteröidä ad hoc -varastosiirrot ilman lähdeasiakirjoja seuraavilla tavoilla:  

- **Sisäinen siirto** -sivulla.  
- **Nimikkeen uudellenluokituspvk** -sivulla.  

> [!NOTE]  
>  Fyysisen varaston laajennetuissa määrityksissä eli sijainneissa, joissa **Ohjattu hyllytys ja poiminta** -asetuskenttä on käytössä, nimikkeet siirretään varastopaikasta toiseen ad hoc **Var.siirtotyökirja**-, **Sisäinen f. var. poiminta**- tai **Sisäinen f.var. hyllytys** -sivujen avulla.  

## <a name="to-move-items-as-an-internal-movement"></a>Siirrä kohteita sisäisenä siirtona  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sisäinen siirto** ja valitse sitten vastaava linkki.  
2.  Täytä **Yleinen**-pikavälilehden **Nro** Voit jättää sen tyhjäksi tai valita **MuokkausApu**-painikkeen ja valita sitten numerosarjan.  
3.  Anna **Sijaintikoodi**-kentässä sijainti, jossa varaston siirto tapahtuu.  

    Jos sijainti on määritetty oletussijainniksi fyysisen varaston työntekijälle, sijaintikoodi lisätään automaattisesti.  
4.  Anna **Varastopaikkakoodiin**-kentässä sen varastopaikan koodi, johon haluat siirtää nimikkeen. Tämä voi olla esimerkiksi tuotantotarkoituksissa sijainnin kortissa tai tuotantosolussa määritetty avoin tuotannon varastopaikka.  
5.  Anna **Eräpäivä**-kentässä päivämäärä, jona varaston siirron on oltava valmis.  
6.  Valitse **Rivit**-pikavälilehdessä **Nimikenro**, jolloin **Var.paikkojen sisältöluettelo** -sivu avautuu, ja valitse sitten siirrettävä nimike sen saatavuuden perusteella varastopaikoissa. Voit myös valita **Hae var.paikan sisältö** -toiminnon, jos haluat täyttää sisäiset siirtorivit suodattimien perusteella. Lisätietoja on **Hae var.paikan sisältö** toiminnon työkaluvihjeessä.   

    Kun olet valinnut kohteen, **Varastopaikkakoodista** -kenttä täytetään automaattisesti valitun varastopaikan sisällön perusteella, mutta voit muuttaa sen toiseen varastopaikkaan, jossa nimike on saatavilla.  

    > [!NOTE]  
    >  Koska **Nimikkeen nro** -kenttä ja **Var.paikasta**-kenttä ovat yhdistetty, niiden arvot voi muuttua keskenään riippuvaisesti, kun muokkaat kenttiä.  

    **Varastopaikkakoodi** -kenttään täytetään otsikkoon kirjoitettu arvo, mutta sitä voidaan muuttaa minkä tahansa muun varastopaikkakoodin rivillä, jota ei ole estetty tai varattu erityistarkoituksiin. Lisätietoja varastopaikkojen määrittämisestä tiettyä tarkoitusta varten on ohjeaiheessa Erityinen.  
7.  Kun olet määrittänyt mihin varastopaikkoihin ja mistä haluat nimikkeitä siirtää, kirjoita määrä siirtääksesi **Määrä** -kentässä.  

    > [!NOTE]  
    >  Määrän on oltava saatavissa Var.paikasta.  

8.  Kun olet valmis käsittelemään sisäistä siirtoa, valitse **Luo varastosiirto** -toiminto.  

    > [!NOTE]  
    >  Kun olet luonut varastosiirron, sisiäisen siirron rivit poistetaano.  

    Suorita muut ad hoc -siirrot **Varastosiirto**-sivulla samalla tavalla kuin mitä tekisit liikkeelle, joka perustuu lähdeasiakirjoihin. Lisätietoja on esimerkiksi kohdassa [Komponenttien siirtäminen toiminta-alueelle fyysisen varaston perusmäärityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Siirrä nimikkeet nimikkeiden uudelleenluokituspäiväkirjan kanssa
Fyysisen varastoinnin siirtoasiakirjojen käytön sijaan voit kirjata nimikkeiden siirron luokittelemalla niiden varastopaikkakoodit uudelleen. Lisätietoja on kohdassa [Varaston laskeminen, muuttaminen ja uudelleenluokitus päiväkirjojen avulla](inventory-how-count-adjust-reclassify.md).   
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimik. uud.luok.pvk** ja valitse sitten vastaava linkki.  
2.  Määritä jokaiselle päiväkirjariville varastopaikat, josta ja johon haluat siirtää nimikkeitä täyttämällä kentät **Varastopaikkakoodi** ja **Uusi varastopaikkakoodi**.  

    1.  Jos haluat siirtää koko sisällön toiseen varastopaikkaan, valitse **Hae var.paikan sisältö** -toiminto.  
    2.  Etsi suodattimien avulla varastopaikka, jonka sisällön haluat siirtää, ja valitse **OK**. Kirjauskansioriveille on täytetty varastopaikan sisältö.  
3.  Täytä kunkin päiväkirjan rivin muut kentät.   
4.  Kirjaa uudelleenluokituspäiväkirja.  

    > [!NOTE]  
    >  Toisin kuin varaston siirtoasiakirjoissa, siirto, joka on kirjattu uudelleenluokittelupäiväkirjaan ei luo fyysisen varaston pyyntöä fyysisten tehtävien suorittamiseen.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]