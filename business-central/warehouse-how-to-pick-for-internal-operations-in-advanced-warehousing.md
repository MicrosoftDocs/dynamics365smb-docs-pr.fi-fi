---
title: Poiminta sisäisissä toiminnoissa laajennetuissa varastomäärityksissä
description: Jos sijainnit käyttävät poimintaa sekä toimituksia, poimi komponentteja tuotannon ja kokoonpanon toimintoja varten F.varastoinnin poiminta -sivulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ea056bf4255cf557c711113854821f9dece17cad
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771033"
---
# <a name="pick-for-production-or-assembly-in-advanced-warehouse-configurations"></a>Tuotanto- tai kokoonpanopoiminta laajennetuissa varastointimäärityksissä
Jos sijainti on määritetty laajennetuissa varastomäärityksissä käyttämään sekä poimintaa että toimitusta, tuotannon ja kokoonpanon toimintojen komponentteja voi poimia **F.varastoinnin poiminta** -sivulla.  

Vaihtoehtoisesti voit siirtää kohteita varastopaikasta toiseen **Siirtotyökirja**-sivulla ilman viittausta lähdeasiakirjaan. Lisätietoja on kohdassa [Nimikkeiden siirtäminen laajennetussa varastointimäärityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Lisätietoja nimikkeiden poiminnasta sisäisiä toimintoja varten niissä fyysisen varaston perussijainneissa, jotka on määritetty vain poimintaa varten, on kohdassa [Komponenttien siirtäminen toiminta-alueelle fyysisen varastoinnin määrityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

Fyysisen varastoinnin poiminta-asiakirjaa voi luoda alusta alkaen, koska poiminta-aktiviteetti on aina osa työnkulkua sekä veto- että työntötilanteessa.  

Voit luoda fyysisen varastoinnin poiminta-asiakirjan valitsemalla push-muodissa **Luo F.var. poiminta** lähdeasiakirjassa, kuten julkaistu kokoonpanotilaus tai fyysisen varaston toimitus. Lisätietoja on kohdassa [Nimikkeiden poiminta fyysisen varaston poiminnassa](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Vaihtoehtoisesti voit luoda varastopoiminta-asiakirjan tunnistamalla sekä toimitusten että sisäisten toimintojen poimintapyynnöt **Poimi työkirja** -sivulla ja luomalla sitten tarvittavat varastopoiminta-asiakirjat.  

Seuraavassa ohjeissa selitetään vetotilanne, jossa **Valitse työkirja** -sivulla poimitaan komponentteja vapautetulle tuotantotilaukselle. Menettely koskee myös kokoonpanotilauksia.  

Luodaksesi poimintapyynnöt sekä veto- että työntötilanteille, kyseiset lähdeasiakirjat on vapautettava. Vapauta sisäisten toimintojen lähdeasiakirjat seuraavilla tavoilla.  

|Lähdeasiakirja|Vapautustapa|  
|---------------------|--------------------|  
|Tuotantotilaus|Muuta tilauksen tyypiksi vapautettu tuotantotilaus.|  
|Kokoonpanotilaus|Muuta tilaksi Vapautettu.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Komponenttien poiminta poimintatyökirjoista  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poimintatyökirja** ja valitse sitten liittyvä linkki.  
2.  Valitse ensin **Hae f. varastoinnin asiakirjat** -toiminto ja sitten komponenttirivit vapautetusta tuotantotilauksesta.  
3.  Käy rivit läpi, järjestele ne tehokkaaksi poimintakierrokseksi ja yhdistele niitä tarpeen mukaan muiden työkirjarivien kanssa siten, että työntekijän aika käytetään mahdollisimman tehokkaasti.  
4.  Valitse **Luo poiminta** -toiminto.  
5.  Määritä, miten voit luoda fyysisen varastoinnin poiminta-asiakirjat ja lajitella poimintarivit täyttämällä kentät **Luo poiminta** -sivulla.  
6.  Valitse **OK**-painike. Varastopoiminta-asiakirjat on luotu poimintarivien kanssa jokaiselle osalle, jota tarvitaan sisäisessäl toiminnassa.  

Jos sisäiselle toimintoalueelle, kuten tuotantokerrokselle, määritetään oletusvarastopaikka toiminnossa käytettävien komponenttien sijoitusta varten, tämä varastopaikkakoodi lisätään fyysisen varaston poiminta-asiakirjan Aseta-riveille. Se ohjaa varastotyöntekijöitä nimikkeiden sijoittamisessa paikoilleen. Lisätietoja on **Tuotannon valmisteluvarastopaikkakoodi** tai **Kokoonpanoon-varastop.koodi** -kentässä.

## <a name="filling-the-consumption-bin"></a>Kulutuksen varastopaikan täyttäminen
Tämä työnkulkukaavio näyttää, miten tuotantotilauksen osarivien **Varastopaikkakoodi**-kenttä täytetään sijaintiasetusten mukaisesti.

![Varastopaikkojen työnkulkukaavio](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Katso myös
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]