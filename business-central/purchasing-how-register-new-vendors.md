---
title: Uuden toimittajan rekisteröinti toimittajan kortin luonnin avulla | Microsoft Docs
description: Lisätietoja uuden toimittajan rekisteröinnistä toimittajan kortin luonnin avulla.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 04/27/2020
ms.author: sgroespe
ms.openlocfilehash: ce41715830545c89651bac7d117b6c356650b7c3
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324172"
---
# <a name="register-new-vendors"></a>Uusien toimittajien rekisteröiminen
Toimittajat tarjoavat tuotteita, jotka myydään. Jokainen toimittaja, jolta ostat, täytyy rekisteröidä toimittajakorttina.

Ennen kuin voit rekisteröidä uusia toimittajia, sinun on määritettävä ostokoodeja, joita valitaan toimittajien korttien täyttämisen yhteydessä. Kun kaikki tarvittavat päätiedot on luotu, voit tehdä muita toimittajaa koskevia määrityksiä, kuten priorisoida toimittajan maksutilanteita varten sekä eritellä nimikkeitä, joita toimittaja ja muut toimittajat voivat toimittaa. Kokonaan erillinen toimittajia koskevien määritystehtävien joukko on alennuksia, hintoja ja maksutapoja koskevien sopimusten tallentaminen. Lisätietoja on kohdassa [Ostojen määrittäminen](purchasing-setup-purchasing.md).

Toimittajan kortti sisältää tiedot, joita tarvitaan tuotteiden ostamiseksi toimittajalta. Lisätietoja on kohdissa [Ostojen kirjaaminen](purchasing-how-record-purchases.md) ja [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

> [!NOTE]  
>   Jos eri toimittajan tyypeille on olemassa toimittajamalleja, sivu avautuu, kun luot uuden toimittajan kortin, jossa voit valita haluamasi mallin. Jos vain yksi toimittajamalli on olemassa, uudet toimittajan kortit käyttävät aina kyseistä mallia.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="to-create-a-new-vendor-card"></a>Uuden toimittajan kortin luominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Toimittajat** ja valitse sitten liittyvä linkki.  
2. Valitse **Toimittajat**-sivulla **Uusi**.

    Jos on olemassa useita toimittajamalleja, näyttöön avautuu automaattisesti sivu, jossa voit valita toimittajamallin. Noudata tällaisessa tapauksessa kahta seuraavaa vaihetta.
3. Valitse **Valitse malli uudelle toimittajalle** -sivulla malli, jota haluat käyttää uudessa toimittajan kortissa.
4. Valitse **OK**-painike. Uuden toimittajan kortti avautuu. Jotkin sen kentät on täytetty mallin tiedoilla.
5. Voit täyttää toimittajan kortin kenttiä tai muuttaa niitä tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Jos et tiedä laskutusosoitetta, jota käytetään kaikissa toimittajan laskuissa, älä täytä **Tavaran laskuttaja** -kenttää. Valitse sen sijaan tavaran laskuttajan numeron sen jälkeen, kun olet määrittänyt ostotarjouksen, -tilauksen, -laskun otsikon.

Toimittaja on nyt rekisteröity, ja toimittajan kortti on valmis käytettäväksi ostoasiakirjoissa.

Jos haluat käyttää tätä toimittajan korttia mallina, kun luot uusia toimittajan kortteja, tallenna se toimittajamallina. Lisätietoja on seuraavassa osassa.

### <a name="deleting-vendor-cards"></a>Toimittajakorttien poistaminen
Jos olet kirjannut toimittajalle tapahtuman, et voi poistaa korttia, koska nimiketapahtumia voi tarvita valvontaan. Voit poistaa toimittajakortteja, joissa on tapahtumakirjauksia ottamalla yhteyttä Microsoft-kumppaniin koodin avulla.

## <a name="to-save-the-vendor-card-as-a-template"></a>Toimittajan kortin tallentaminen mallina
1. Valitse **Toimittajakortti**-sivulla **Tallenna mallina** -toiminto. **Toimittajamalli**-sivu avautuu ja näyttää toimittajan kortin mallina.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon. **Dimensiomallit**-sivu avautuu. Se sisältää kaikki toimittajalle määritetyt dimensiokoodit.
4. Muokkaa tai syötä dimensiokoodeja, joita käytetään mallin avulla luotuihin uusiin toimittajan kortteihin.
5. Kun olet määrittänyt uuden toimittajamallin, valitse **OK**-painike.  
   Toimittajamalli lisätään toimittajamallien luetteloon niin, että sen avulla voit luoda uusia toimittajan kortteja.

## <a name="see-also"></a>Katso myös
[Tietueiden kaksoiskappaleiden yhdistäminen](sales-how-merge-duplicate-records.md)  
[Numerosarjojen luominen](ui-create-number-series.md)  
[Osto](purchasing-manage-purchasing.md)  
[Ostojen kirjaus](purchasing-how-record-purchases.md)   
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
