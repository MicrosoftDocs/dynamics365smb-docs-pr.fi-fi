---
title: "Toimintaohje: Uusien asiakkaiden rekisteröiminen| Microsoft Docs"
description: "Toimintaohje: Uusien asiakkaiden rekisteröiminen"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6789e6a4129789e950c7f71ff86e62263ae9c087
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-register-new-customers"></a>Toimintaohje: Uusien asiakkaiden rekisteröiminen
Asiakkaat ovat tulonlähteesi. Jokainen asiakas, jolle myyt, on rekisteröitävä asiakaskorttina. Asiakkaan kortit sisältävät tietoja, jotka tarvitaan tuotteiden asiakkaalle myymistä varten. Lisätietoja on kohdassa [Toimintaohje: Myynnin laskutus](sales-how-invoice-sales.md) ja [Toimintaohje: Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).  

Ennen kuin voit rekisteröidä uusia asiakkaita, sinun on määritettävä myyntikoodit, jotka voidaan valita asiakkaiden korttien täyttämisen yhteydessä. Lisätietoja on kohdassa [Myynnin määrittäminen](sales-setup-sales.md).

**Huomautus**: Jos eri asiakastyypeille on olemassa asiakasmalleja, ikkuna tulee näkyviin, kun luot uuden asiakkaan kortin, jossa voit valita haluamasi mallin. Jos vain yksi asiakasmalli on olemassa, uudet asiakaskortit käyttävät aina kyseistä mallia.

## <a name="to-create-a-new-customer-card"></a>Uuden asiakkaan kortin luominen
1. Valitse kotisivun **Asiakkaat**-toiminto, kun haluat avata olemassa olevien asiakkaiden luettelon.  
2. Valitse **Asiakkaat**-ikkunassa **Uusi**-toiminto.

    Jos vain yksi asiakasmalli on olemassa, uusi asiakkaan kortin avautuu. Osa kortin kentistä täytetty mallin tiedoilla.

    Jos on olemassa useita asiakasmalleja, näyttöön avautuu automaattisesti ikkuna, jossa voit valita asiakasmallin. Noudata tällaisessa tapauksessa kahta seuraavaa vaihetta.
3. Valitse **Valitse malli uudelle asiakkaalle** -ikkunassa malli, jota haluat käyttää uudessa asiakkaan kortissa.
4. Valitse **OK**-painike. Uuden asiakkaan kortti avautuu. Osa kortin kentistä on täytetty mallin tiedoilla.  
5. Voit täyttää asiakkaan kortin kenttiä tai muuttaa niitä tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Myyntihinnat**-pikavälilehti sisältää erityiset hinnat tai alennukset, jotka haluat myöntää asiakkaalle, jos tietyt ehdot, kuten nimike, vähimmäistilausmäärä tai päättymispäivämäärä, täyttyvät. Kukin rivi edustaa erityistä hinnan alennusta tai rivialennusta. Kukin sarake vastaa ehtoa, joka takaa **Yksikköhinta**-kenttään kirjoitetun erikoishinnan tai **Rivialennus-%**-kenttään kirjoitetun rivialennuksen. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).

Asiakas on nyt rekisteröity, ja asiakkaan kortti on valmis käytettäväksi myyntiasiakirjoissa.

Jos haluat käyttää tätä asiakkaan korttia mallina, kun luot uusia asiakkaan kortteja, tallenna se mallina. Lisätietoja on seuraavassa osassa.

## <a name="to-save-the-customer-card-as-a-template"></a>Asiakkaan kortin tallentaminen mallina
1. Valitse **Asiakkaan kortti** -ikkunassa **Tallenna mallina** -toiminto. **Asiakasmalli**-ikkuna avautuu ja näyttää asiakaskortin mallina.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon. **Dimensiomallit**-ikkuna avautuu. Se sisältää kaikki asiakkaalle määritetyt dimensiokoodit.
4. Muokkaa tai syötä dimensiokoodit, joita käytetään mallin avulla luotuihin uusiin asiakkaan kortteihin.  
5. Kun olet määrittänyt uuden asiakasmallin, valitse **OK**-painike.

Asiakasmalli lisätään asiakasmallien luetteloon niin, että sen avulla voit luoda uusia asiakkaiden kortteja.

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)    
[Myynnin määrittäminen](sales-setup-sales.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

