---
title: "Poiminta sisäisissä toiminnoissa laajennetuissa varastomäärityksissä | Microsoft-asiakirjat"
description: "Jos sijainti on määritetty laajennetuissa varastomäärityksissä käyttämään sekä poimintaa että toimitusta, tuotannon ja kokoonpanon toimintojen komponentteja voi poimia **F.varastoinnin poiminta** -ikkunassa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 94f45dd0b9d3a384fa0aafcc8f0555c52de25816
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-pick-for-assembly-or-production-in-advanced-warehouse-configurations"></a>Toimintaohje: Kokoonpano- tai tuotantopoiminta laajennetuissa varastointimäärityksissä
Jos sijainti on määritetty laajennetuissa varastomäärityksissä käyttämään sekä poimintaa että toimitusta, tuotannon ja kokoonpanon toimintojen komponentteja voi poimia **F.varastoinnin poiminta** -ikkunassa.  

Vaihtoehtoisesti voit käyttää **Siirtotyökirja**-ikkunaa siirtääksesi kohteita varastopaikasta toiseen ad hoc, eli ilman viitettä lähdeasiakirjaan. Lisätietoja on kohdassa [Toimintaohje: Nimikkeiden siirtäminen laajennetuissa varastomäärityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Lisätietoja nimikkeiden poiminnasta sisäisiä toimintoja varten niissä fyysisen varaston perussijainneissa, jotka on määritetty vain poimintaa varten, on kohdassa [Toimintaohje: Komponenttien siirtäminen toiminta-alueelle fyysisen varastoinnin määrityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

Fyysisen varastoinnin poiminta-asiakirjaa voi luoda alusta alkaen, koska poiminta-aktiviteetti on aina osa työnkulkua sekä veto- että työntötilanteessa.  

Voit luoda fyysisen varastoinnin poiminta-asiakirjan valitsemalla push-muodissa **Luo F.var. poiminta** lähdeasiakirjassa, kuten julkaistu kokoonpanotilaus tai fyysisen varaston toimitus. Lisätietoja on kohdassa [Toimintaohje: Nimikkeiden poiminen ja fyysisen varastoinnin poiminnat](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Vaihtoehtoisesti voit luoda varastopoiminta-asiakirjan käyttämällä **Poimi työkirja**  -ikkunaa poimintapyyntöjen tunnistamiseksi sekä toimitusta että sisäisiä toimintoja varten, ja luomalla sitten tarvittavat varastopoiminta-asiakirjat.  

Seuraavassa ohjeissa selitetään vetotilanne, jossa **Valitse työkirja** -ikkunassa poimitaan komponentteja vapautetulle tuotantotilaukselle. Menettely koskee myös kokoonpanotilauksia.  

Luodaksesi poimintapyynnöt sekä veto- että työntötilanteille, kyseiset lähdeasiakirjat on vapautettava. Vapauta sisäisten toimintojen lähdeasiakirjat seuraavilla tavoilla.  

|Lähdeasiakirja|Vapautustapa|  
|---------------------|--------------------|  
|Tuotantotilaus|Muuta tilauksen tyypiksi vapautettu tuotantotilaus.|  
|Kokoonpanotilaus|Muuta tilaksi Vapautettu.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Komponenttien poiminta poimintatyökirjoista  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Poimintatyökirja** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse ensin **Hae f. varastoinnin asiakirjat** -toiminto ja sitten komponenttirivit vapautetusta tuotantotilauksesta.  
3.  Käy rivit läpi, järjestele ne tehokkaan poimintakierroksen tekemiseksi ja yhdistele niitä tarpeen mukaan muiden työkirjarivien kanssa hyödyntääksesi parhaiten työntekijän ajan.  
4.  Valitse **Luo poiminta** -toiminto.  
5.  Määritä, miten voit luoda fyysisen varastoinnin poiminta-asiakirjat ja lajitella poimintarivit täyttämällä kentät **Luo poiminta** -ikkunassa.  
6.  Valitse **OK**-painike. Varastopoiminta-asiakirjat on luotu poimintarivien kanssa jokaiselle osalle, jota tarvitaan sisäisessäl toiminnassa.  

Jos sisäiselle toimintoalueelle, kuten tuotantokerrokselle, määritetään oletusvarastopaikka toiminnossa käytettävien komponenttien sijoitusta varten, tämä varastopaikkakoodi lisätään fyysisen varaston poiminta-asiakirjan Aseta-riveille. Se ohjaa varastotyöntekijöitä nimikkeiden sijoittamisessa paikoilleen. Lisätietoja on **Tuotannon valmisteluvarastopaikkakoodi** tai **Kokoonpanoon-varastop.koodi** -kentässä.

## <a name="filling-the-consumption-bin"></a>Kulutuksen varastopaikan täyttäminen
Tämä työnkulkukaavio näyttää, miten tuotantotilauksen osarivien**Varastopaikkakoodi**-kenttä täytetään sijaintiasetusten mukaisesti.

![Varastopaikkojen vuokaavio](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Katso myös
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

