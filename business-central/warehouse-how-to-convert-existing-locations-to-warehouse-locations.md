---
title: Olemassa olevien sijaintien muuntaminen fyysisen varaston sijainneiksi | Microsoft Docs
description: Ottamalla alueet ja varastopaikat käyttöön aiemmin luodussa varastosijainnissa voit tehdä siitä fyysisen varastoinnin sijainnin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 95198789cd0fa4f00999c57ae9b6431dae8c9243
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386772"
---
# <a name="convert-existing-locations-to-warehouse-locations"></a>Aiemmin luotujen sijaintien muuntaminen fyysisen varaston sijainneiksi
Ottamalla alueet ja varastopaikat käyttöön aiemmin luodussa varastosijainnissa voit tehdä siitä fyysisen varastoinnin sijainnin.  

Eräajo, joka mahdollistaa fyysisen varastoinnin käytön sijainnissa, luo alustavat fyysisen varastoinnin tapahtumat fyysisen varastoinnin muutosvarastopaikkaa varten kaikille nimikkeille, joilla on varastoa sijainnissa. Nämä alustavat tapahtumat täsmätään, kun fyysisen varastoinnin inventointitapahtumat syötetään eräajon suorittamisen jälkeen.  

Voit luoda alueet ja varastopaikat ennen muunnosta tai sen jälkeen. Ainoa varastopaikka, joka on luotava ennen muunnosta, on jatkossa muutosvarastopaikkana käytettävä varastopaikka.  

> [!IMPORTANT]  
>  Tyhjennä kaikki negatiiviset varastot ja mahdolliset avoimet fyysisen varastoinnin asiakirjat ennen kuin konvertoit fyysisen varaston käsittelyn sijainnin ja aja raportti määrittääksesi negatiivisen varaston nimikkeet ja avoimen fyysisen varaston asiakirjat tässä sijainnissa. Lisätietoa on kohdassa Negatiivisen varaston tarkistus.  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a>Aiemmin luodun sijainnin valmisteleminen fyysisen varastoinnin sijainniksi  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Luo fyys. var. sijainti** ja valitse sitten liittyvä linkki.  
2.  Määritä **Sijaintikoodi**-kentässä sijainti, jossa haluat ottaa käyttöön fyysisen varaston käsittelyn.  
3.  Määritä **Muutosvarastopaikan koodi** -kentässä varastopaikka sijainnissa, johon synkronoimattomat fyysisen varastoinnin tapahtumat tallennetaan. Lisätietoja on kohdassa [Muutettujen fyysisen varastoinnin tapahtumien ja liittyvien nimiketapahtumien synkronointi](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).  

    Käyttämällä määritetylle sijainnille avoimia nimiketapahtumia ohjelma luo fyysisen varastoinnin päiväkirjarivit, joilla on kaikki mahdolliset nimiketapahtumissa olevat Nimikkeen nro-, Varianttikoodi-, Mittayksikön koodi- ja tarvittaessa Eränro- ja Sarjanro-kenttien yhdistelmät. Ohjelma kirjaa sen jälkeen fyysisen varastoinnin päiväkirjarivit. Tämä kirjaus luo fyysisen varastoinnin tapahtumat, jotka sijoittavat varaston fyysisen varastoinnin muutosvarastopaikkaan. Ohjelma määrittää myös sijaintikortin **Muutosvarastopaikan koodi**-kentän arvon.  

4.  Voit tarkastella muutosvarastopaikkaan eräajon aikana lisättyjä nimikkeitä suorittamalla **F. var. muutosvar.paikka** -raportin.  
5.  Kun **Luo fyys. var. sijainti** -eräajo on valmis, suorita ja kirjaa fyysisen varastoinnin inventointi. Lisätietoja on kohdassa [Varaston laskeminen, muuttaminen ja uudelleenluokitus päiväkirjojen avulla](inventory-how-count-adjust-reclassify.md).  

> [!NOTE]  
>  On suositeltavaa suorittaa **Luo fyys. var. sijainti** -eräajo sellaiseen aikaan, ettei se häiritse järjestelmän tavallista käyttöä. Tämä eräajo käsittelee jokaisen **Nimiketapahtuma**-taulukon tapahtuman, ja jos nimiketapahtumia on paljon, eräajo voi kestää useita tunteja.  

 Sijainneissa, joissa ei ole käytetty varastoinninhallinnan asiakirjoja ennen muunnosta, kaikki ennen muunnosta vastaanotetut tai osittain toimitetut lähdeasiakirjat on avattava uudelleen ja vapautettava.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]