---
title: Maksualennusten ohittaminen
description: 'Käytä maksualennusten ohittamistoimintoa kokonaissumman yhteydessä, kun haluat hyväksyä maksut seuraavien ehtojen täyttyessä:'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8a21b9ed5eac0aa504a6fd95f45044f1aadb4b98
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "915936"
---
# <a name="disregard-payment-discounts"></a>Maksualennusten ohittaminen
Käytä maksualennusten ohittamistoimintoa kokonaissumman yhteydessä, kun haluat hyväksyä maksut seuraavien ehtojen täyttyessä:  

- Maksualennuksen päivämäärä < maksupäivämäärä <= maksutoleranssin päivämäärä  
- Kokonaissumma >= maksun summa >= kokonaissumma - maksualennus  

## <a name="to-disregard-a-payment-discount"></a>Maksualennuksen ohittaminen  

1.  Valitse ![Etsi sivu tai raportti](../../media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksuehdot** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse rivi, jonka maksuehdolle haluat ottaa käyttöön maksualennuksia tai jolta haluat poistaa ne.  
3.  Ota tämä toiminto käyttöön valitsemalla **Ohita maks.alen. kok.sum. yht.** -valintaruutu. Poista toiminto käytöstä tyhjentämällä valintaruutu.  

> [!NOTE]  
>  Kun yksi maksu kohdistetaan useisiin laskuihin, maksualennuksen ohitustoimintoa ei tueta kokonaissumman yhteydessä.  

## <a name="see-also"></a>Katso myös  
[Verkkopankkitoiminta Suomessa](electronic-banking-in-finland.md)   
[Maksutiedostojen luominen](how-to-generate-payment-files.md)   
[Maksutapojen määrittäminen](../../finance-payment-methods.md)  
[Maksutoleranssien ja maksualennustoleranssien käsitteleminen](../../finance-payment-tolerance-and-payment-discount-tolerance.md)     
[Pankin viitetiedostojen määrittäminen](how-to-set-up-bank-reference-files.md)
