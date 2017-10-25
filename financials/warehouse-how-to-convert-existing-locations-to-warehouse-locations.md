---
title: Olemassa olevien sijaintien muuntaminen fyysisen varaston sijainneiksi | Microsoft Docs
description: "Ottamalla alueet ja varastopaikat käyttöön aiemmin luodussa varastosijainnissa voit tehdä siitä fyysisen varastoinnin sijainnin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 01081b166df81a76bba984bcb679069e59c660c9
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-convert-existing-locations-to-warehouse-locations"></a>Olemassa olevien sijaintien muuntaminen fyysisen varaston sijainneiksi
Ottamalla alueet ja varastopaikat käyttöön aiemmin luodussa varastosijainnissa voit tehdä siitä fyysisen varastoinnin sijainnin.  

Eräajo, joka mahdollistaa fyysisen varastoinnin käytön sijainnissa, luo alustavat fyysisen varastoinnin tapahtumat fyysisen varastoinnin muutosvarastopaikkaa varten kaikille nimikkeille, joilla on varastoa sijainnissa. Nämä alustavat tapahtumat täsmätään, kun fyysisen varastoinnin inventointitapahtumat syötetään eräajon suorittamisen jälkeen.  

Voit luoda alueet ja varastopaikat ennen muunnosta tai sen jälkeen. Ainoa varastopaikka, joka on luotava ennen muunnosta, on jatkossa muutosvarastopaikkana käytettävä varastopaikka.  

> [!IMPORTANT]  
>  Tyhjennä kaikki negatiiviset varastot ja mahdolliset avoimet fyysisen varastoinnin asiakirjat ennen kuin konvertoit fyysisen varaston käsittelyn sijainnin ja aja raportti määrittääksesi negatiivisen varaston nimikkeet ja avoimen fyysisen varaston asiakirjat tässä sijainnissa. Lisätietoa on kohdassa Negatiivisen varaston tarkistus.  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a>Aiemmin luodun sijainnin valmisteleminen fyysisen varastoinnin sijainniksi  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Luo fyys. var. sijainti** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Määritä **Sijaintikoodi**-kentässä sijainti, jossa haluat ottaa käyttöön fyysisen varaston käsittelyn.  
3.  Määritä **Muutosvarastopaikan koodi** -kentässä varastopaikka sijainnissa, johon synkronoimattomat fyysisen varastoinnin tapahtumat tallennetaan. Lisätietoja on ohjeaiheen [Toimintaohje: Varaston laskeminen, muuttaminen ja uudelleenluokitus](inventory-how-count-adjust-reclassify.md) kohdassa Muutettujen fyysisen varastoinnin tapahtumien ja liittyvien nimiketapahtumien synkronointi.  

    Käyttämällä määritetylle sijainnille avoimia nimiketapahtumia ohjelma luo fyysisen varastoinnin päiväkirjarivit, joilla on kaikki mahdolliset nimiketapahtumissa olevat Nimikkeen nro-, Varianttikoodi-, Mittayksikön koodi- ja tarvittaessa Eränro- ja Sarjanro-kenttien yhdistelmät. Ohjelma kirjaa sen jälkeen fyysisen varastoinnin päiväkirjarivit. Tämä kirjaus luo fyysisen varastoinnin tapahtumat, jotka sijoittavat varaston fyysisen varastoinnin muutosvarastopaikkaan. Ohjelma määrittää myös sijaintikortin **Muutosvarastopaikan koodi**-kentän arvon.  

4.  Voit tarkastella muutosvarastopaikkaan eräajon aikana lisättyjä nimikkeitä suorittamalla **F. var. muutosvar.paikka** -raportin.  
5.  Kun **Luo fyys. var. sijainti** -eräajo on valmis, suorita ja kirjaa fyysisen varastoinnin inventointi. Lisätietoja on kohdassa [Toimintaohje: Varaston laskeminen, muuttaminen ja uudelleenluokitus](inventory-how-count-adjust-reclassify.md).  

> [!NOTE]  
>  On suositeltavaa suorittaa **Luo fyys. var. sijainti** -eräajo sellaiseen aikaan, ettei se häiritse järjestelmän tavallista käyttöä. Tämä eräajo käsittelee jokaisen **Nimiketapahtuma**-taulukon tapahtuman, ja jos nimiketapahtumia on paljon, eräajo voi kestää useita tunteja.  

 Sijainneissa, joissa ei ole käytetty varastoinninhallinnan asiakirjoja ennen muunnosta, kaikki ennen muunnosta vastaanotetut tai osittain toimitetut lähdeasiakirjat on avattava uudelleen ja vapautettava.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

