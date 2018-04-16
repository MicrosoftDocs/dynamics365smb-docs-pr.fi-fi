---
title: Varastopaikkojen luominen | Microsoft Docs
description: "Tehokkain tapa luoda fyysisen varaston varastopaikkoja on luoda samankaltaisten varastopaikkojen ryhmiä varastopaikan luontityökirjassa, mutta varastopaikkoja voi luoda myös yksittäin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f8cd19f97c530397dd6b499157e13340331aa3ba
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="create-bins"></a>Varastopaikkojen luominen
Tehokkain tapa luoda fyysisen varaston varastopaikkoja on luoda samankaltaisten varastopaikkojen ryhmiä varastopaikan luontityökirjassa, mutta varastopaikkoja voi luoda myös yksittäin sijainnin kortista. Voit luoda varastopaikkoja myös automaattisesti **Var.paikan luontityökirja** -ikkunassa.  

## <a name="to-create-a-bin-from-the-location-card"></a>Varastopaikan luonti sijaintikortista  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sijainnit** ja valitse aiheeseen liittyvä linkki.  
2. Valitse ensin sijainti, josta haluat luoda varastopaikan, ja sitten **Varastopaikat**-toiminto.  
3. Valitse **Uusi**-toiminto.
4. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Varastopaikkojen luominen yksittäin varastopaikan luontityökirjassa  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Var.paikan luontityökirja** ja valitse aiheeseen liittyvä linkki.  
2.  Täytä jokaisella rivillä kentät, jotka tarvitaan luotavien varastopaikkojen nimeämiseen ja kuvailemiseen.  
3.  Valitse **Luo varastopaikat** -toiminto.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Varastopaikkojen muodostaminen automaattisesti varastopaikkojen luontityökirjassa  
Ennen kuin aloitat varastopaikkojen automaattisen luonnin, sinun on päätettävä toimintojesi kannalta olennainen varastopaikkojen tyyppi ja nimikkeiden kätevin kulku fyysisen varaston rakenteiden läpi.  

> [!NOTE]  
>  Kun varastopaikkaa on käytetty, sitä ei voi poistaa kuin tyhjänä. Mutta jos haluat joskus käyttää muuta varastopaikan nimeämisjärjestelmää, voit käyttää uudelleenluokittelupäiväkirjaa "siirtääksesi" nimikkeet uuteen varastopaikkajärjestelmään. Tämä prosessi on kuitenkin manuaalinen ja se vie aikaa, joten parasta on määrittää varastopaikat oikein alusta lähtien.  

Voit käyttää **Var.paikan luontityökirja** -ikkunaa, jos sinut on määritetty varastotyöntekijäksi varastopaikkojen sijaintipaikkaan. Lisätietoja on kohdassa [Varastotyöntekijöiden määrittäminen](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Var.paikan luontityökirja** ja valitse aiheeseen liittyvä linkki.  
2.  Valitse **Laske varastopaikat** -toiminto.
3. Valitse **Laske varastopaikat** -ikkunan **Varastopaikkamallin koodi** -kentässä varastopaikkamalli, jota haluat käyttää luotavien varastopaikkojen mallina.
4.  Täytä kuvaus varastopaikoille, joita olet luomassa.  
5.  Luo varastopaikkakoodit täyttämällä **Numerosta**- ja **Numeroon**-kentät ikkunassa näkyvissä kolmessa luokassa: **Hylly**, **Osio** ja **Taso**. Varastopaikkakoodi voi sisältää enintään 20 merkkiä.  

    > [!NOTE]  
    >  Merkkien lukumäärä, jonka olet syöttänyt kolmeen luokkaan kummankin kentän osalta (esimerkiksi kolmeen **Numerosta**-kenttiin syöttämäsi merkit), sekä kenttien mahdolliset erottimet voivat olla yhteensä korkeintaan 20 merkkiä.  

     Voit käyttää koodissa kirjaimia yksilöivänä yhdistelmänä, mutta kirjaimen täytyy olla sama **Numerosta**- ja **Numeroon**-kentät -kentät. Voit esimerkiksi määritellä hyllyä koskevan koodin osaksi **Numerosta A01** ja **Numeroon A10**. Ohjelmaa ei ole määritetty luomaan koodeja, joissa on kirjainjonoja, esim. A01 - F05.  

6.  Jos haluat jonkin merkin, esimerkiksi yhdysmerkin, erottavan luokkakenttiä, jotka on määritelty osaksi varastopaikkakoodia, täytä **Kenttäerotin**-kenttään tämä merkki.  
7.  Jos et halua ohjelman luovan riviä varastopaikalle, jos se on jo olemassa, lisää rasti **Tarkasta olemassa olevat var.paikat** -kenttään.  
8. Sen jälkeen kun olet täyttänyt kaikki kentät, paina **OK**-painiketta .

    Ohjelma luo työkirjaan rivin kullekin varastopaikalle. Voit nyt poistaa joitain varastopaikoista, jos sinulla on esimerkiksi hylly, jossa on käytävä parin osion kahden ensimmäisen tason välillä.  

9. Kun olet poistanut kaikki tarpeettomat varastopaikat, valitse **Luo varastopaikat** -toiminto, ohjelma luo työkirjan kullekin riville varastopaikkoja.  

Prosessi toistetaan toisen varastopaikkasarjan osalta, siihen asti kun fyysiseen varastoon on luotu kaikki varastopaikat.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

