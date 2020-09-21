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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 6e73913f9d03d0cbeab475268a339bd7d9430dd2
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778375"
---
# <a name="disregard-payment-discounts"></a>Maksualennusten ohittaminen
Käytä maksualennusten ohittamistoimintoa kokonaissumman yhteydessä, kun haluat hyväksyä maksut seuraavien ehtojen täyttyessä:  

- Maksualennuksen päivämäärä < maksupäivämäärä <= maksutoleranssin päivämäärä  
- Kokonaissumma >= maksun summa >= kokonaissumma - maksualennus  

## <a name="to-disregard-a-payment-discount"></a>Maksualennuksen ohittaminen  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksuehdot** ja valitse sitten liittyvä linkki.  
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
