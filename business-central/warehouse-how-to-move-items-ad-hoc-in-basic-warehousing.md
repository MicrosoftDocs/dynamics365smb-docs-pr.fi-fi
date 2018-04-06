---
title: "Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä | Microsoft Docs"
description: "Voit joskus joutua siirtämään nimikkeitä sisäisissä varastopaikoissa, ilman, että vastaanotat tai toimitat varastopaikkoja, ilman erityispyyntöä lähdeasiakirjasta. Voi suorittaa nämä suunnittelemattomat siirrot esimerkiksi silloin, jos haluat järjestellä fyysistä varastoa tuomalla nimikkeitä tarkastusalueelle tai siirtää lisänimikkeitä tuotantoalueelle ja sieltä pois ilman järjestelmäsuhdetta tuotantotilauksen lähdeasiakirjaan."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 198bd85853ac0cfb4501c412237e9192c55dbc30
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="move-items-ad-hoc-in-basic-warehouse-configurations"></a>Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä
Voit joskus joutua siirtämään nimikkeitä sisäisissä varastopaikoissa ilman, että vastaanotat tai toimitat varastopaikkoja tai ilman erityispyyntöä lähdeasiakirjasta. Voi suorittaa nämä suunnittelemattomat siirrot esimerkiksi silloin, jos haluat järjestellä fyysistä varastoa tuomalla nimikkeitä tarkastusalueelle tai siirtää lisänimikkeitä tuotantoalueelle ja sieltä pois ilman järjestelmäsuhdetta tuotantotilauksen lähdeasiakirjaan.  

Fyysisen varaston perusmäärityksissä eli sijainneissa, joissa käytetään **Var.paikka pakollinen** -asetuskenttiä ja mahdollisesti **Vaadi poiminta**- ja **Vaadi hyllytys** -asetuskenttiä, voi rekisteröidä ad hoc -varastosiirrot ilman lähdeasiakirjoja seuraavilla tavoilla:  

- **Sisäinen liikkuvuus** -ikkunan avulla.  
- **Nimikkeen uudellenluokituspvk** -ikkunan avulla  

> [!NOTE]  
>  Fyysisen varaston laajennetuissa määrityksissä eli sijainneissa, joissa **Ohjattu hyllytys ja poiminta** -asetuskenttä on käytössä, nimikkeet siirretään varastopaikasta toiseen ad hoc **Var.siirtotyökirja**-, **Sisäinen f. var. poiminta**- tai **Sisäinen f.var. hyllytys** -ikkunan avulla.  

## <a name="to-move-items-as-an-internal-movement"></a>Siirrä kohteita sisäisenä siirtona  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sisäinen siirto** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Täytä **Yleinen**-pikavälilehden **Nro** Voit jättää sen tyhjäksi tai valita **MuokkausApu**-painikkeen ja valita sitten numerosarjan.  
3.  Anna **Sijaintikoodi**-kentässä sijainti, jossa varaston siirto tapahtuu.  

    Jos sijainti on määritetty oletussijainniksi fyysisen varaston työntekijälle, sijaintikoodi lisätään automaattisesti.  
4.  Anna **Varastopaikkakoodiin**-kentässä sen varastopaikan koodi, johon haluat siirtää nimikkeen. Tämä voi olla esimerkiksi tuotantotarkoituksissa sijainnin kortissa tai tuotantosolussa määritetty avoin tuotannon varastopaikka.  
5.  Anna **Eräpäivä**-kentässä päivämäärä, jona varaston siirron on oltava valmis.  
6.  Valitse **Rivit**-pikavälilehdessä **Nimikenro**, jolloin **Var.paikkojen sisältöluettelo** -ikkuna avautuu, ja valitse sitten siirrettävä nimike sen saatavuuden perusteella varastopaikoissa. Voit myös valita **Hae var.paikan sisältö** -toiminnon, jos haluat täyttää sisäiset siirtorivit suodattimien perusteella. Lisätietoja on **Hae var.paikan sisältö** toiminnon työkaluvihjeessä.   

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

    Suorita muut ad hoc -siirrot **Varastosiirto** -ikkunassa samalla tavalla kuin mitä tekisit liikkeelle, joka perustuu lähdeasiakirjoihin. Lisätietoja on esimerkiksi kohdassa [Komponenttien siirtäminen toiminta-alueelle fyysisen varaston perusmäärityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Siirrä nimikkeet nimikkeiden uudelleenluokituspäiväkirjan kanssa
Fyysisen varastoinnin siirtoasiakirjojen käytön sijaan voit kirjata nimikkeiden siirron luokittelemalla niiden varastopaikkakoodit uudelleen. Lisätietoja on kohdassa [Varaston laskeminen, muuttaminen ja uudelleenluokitus](inventory-how-count-adjust-reclassify.md).   
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Nimikkeen uudell.luokit. pvk** ja valitse sitten aiheeseen liittyvä linkki.  
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
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

