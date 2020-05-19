---
title: Uusien asiakkaiden rekisteröinti asiakkaan kortin luonnin avulla | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten asiakkaan kortti luodaan rekisteröimään tietoja kustakin uudesta asiakkaasta, jolle myyt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/27/2020
ms.author: sgroespe
ms.openlocfilehash: 3b56b4009e08085bb232b050790aa03acf2aa4cf
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324268"
---
# <a name="register-new-customers"></a>Uusien asiakkaiden rekisteröinti
Asiakkaat ovat tulonlähteesi. Jokainen asiakas, jolle myyt, on rekisteröitävä asiakaskorttina. Asiakkaan kortit sisältävät tietoja, jotka tarvitaan tuotteiden asiakkaalle myymistä varten. Lisätietoja on kohdissa [Myynnin laskutus](sales-how-invoice-sales.md) ja [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).  

Ennen kuin voit rekisteröidä uusia asiakkaita, sinun on määritettävä myyntikoodit, jotka voidaan valita asiakkaiden korttien täyttämisen yhteydessä. Lisätietoja on kohdassa [Myynnin määrittäminen](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

> [!NOTE]  
> Jos eri asiakastyypeille on olemassa asiakasmalleja, sivu avautuu, kun luot uuden asiakkaan kortin, jossa voit valita haluamasi mallin. Jos vain yksi asiakasmalli on olemassa, uudet asiakaskortit käyttävät aina kyseistä mallia.  

## <a name="to-create-a-new-customer-card"></a>Uuden asiakkaan kortin luominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.  
2. Valitse **Asiakkaat** -sivulla **Uusi**-toiminto.

    Jos vain yksi asiakasmalli on olemassa, uusi asiakkaan kortin avautuu. Osa kortin kentistä täytetty mallin tiedoilla.

    Jos on olemassa useita asiakasmalleja, näyttöön avautuu automaattisesti sivu, jossa voit valita asiakasmallin. Noudata tällaisessa tapauksessa kahta seuraavaa vaihetta.
3. Valitse **Valitse malli uudelle asiakkaalle** -sivulla malli, jota haluat käyttää uudessa asiakkaan kortissa.
4. Valitse **OK**-painike. Uuden asiakkaan kortti avautuu. Osa kortin kentistä on täytetty mallin tiedoilla.  
5. Voit täyttää asiakkaan kortin kenttiä tai muuttaa niitä tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Myyntihinnat**-pikavälilehti sisältää erityiset hinnat tai alennukset, jotka haluat myöntää asiakkaalle, jos tietyt ehdot, kuten nimike, vähimmäistilausmäärä tai päättymispäivämäärä, täyttyvät. Kukin rivi edustaa erityistä hinnan alennusta tai rivialennusta. Kukin sarake vastaa ehtoa, joka takaa **Yksikköhinta**-kenttään kirjoitetun erikoishinnan tai **Rivialennus-%**-kenttään kirjoitetun rivialennuksen. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).

Asiakas on nyt rekisteröity, ja asiakkaan kortti on valmis käytettäväksi myyntiasiakirjoissa.

### <a name="deleting-customer-cards"></a>Asiakaskorttien poistaminen
Jos olet kirjannut asiakkaalle tapahtuman, et voi poistaa korttia, koska nimiketapahtumia voi tarvita valvontaan. Voit poistaa asiakaskortin, jossa on tapahtumakirjauksia ottamalla yhteyttä Microsoft-kumppaniin koodin avulla.

Jos haluat käyttää tätä asiakkaan korttia mallina, kun luot uusia asiakkaan kortteja, tallenna se mallina. Lisätietoja on seuraavassa osassa.

## <a name="to-save-the-customer-card-as-a-template"></a>Asiakkaan kortin tallentaminen mallina
1. Valitse **Asiakkaan kortti** -sivulla **Tallenna mallina** -toiminto. **Asiakasmalli**-sivu avautuu ja näyttää asiakaskortin mallina.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon. **Dimensiomallit**-sivu avautuu. Se sisältää kaikki asiakkaalle määritetyt dimensiokoodit.
4. Muokkaa tai syötä dimensiokoodit, joita käytetään mallin avulla luotuihin uusiin asiakkaan kortteihin.  
5. Kun olet määrittänyt uuden asiakasmallin, valitse **OK**-painike.

Asiakasmalli lisätään asiakasmallien luetteloon niin, että sen avulla voit luoda uusia asiakkaiden kortteja.

## <a name="see-also"></a>Katso myös
[Maksutapojen määrittäminen](finance-payment-methods.md)  
[Tietueiden kaksoiskappaleiden yhdistäminen](sales-how-merge-duplicate-records.md)  
[Numerosarjojen luominen](ui-create-number-series.md)  
[Myynti](sales-manage-sales.md)    
[Myynnin määrittäminen](sales-setup-sales.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
