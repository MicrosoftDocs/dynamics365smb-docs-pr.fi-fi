---
title: Nimikkeiden myynnin tai oston estäminen
description: Voit estää nimikkeen käytön esimerkiksi myynti- tai ostoasiakirjoissa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 467b43b14f1905018c2a26a06c15abc5a0a17e99
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410642"
---
# <a name="block-items-from-sales-or-purchasing"></a>Nimikkeiden myynnin tai oston estäminen
Voit estää tuotteen syöttämisen myynti- tai ostoasiakirjojen riveille ja estää sen kirjaamiseen kaikissa tapahtumissa. Tämä on hyödyllistä esimerkiksi silloin, kun nimikkeellä on tunnettu vika. Jos joku valitsee myynti- tai ostoasiakirjassa estetyn nimikkeen, viesti ilmoittaa heille, että nimike on suljettu.

Seuraava taulukko kuvaa, mitä tapahtuu, kun nimikkeet on estetty.  

|Asetus|Kuvaus|  
|--------------------|------------|  
|**Myynti estetty**|Nimikettä ei voi viedä myyntiasiakirjaan tai myynnin nimikepäiväkirjaan.|  
|**Osto estetty**|Et voi viedä nimikettä ostoasiakirjaan, ostonimikepäiväkirjaan tai ostojen suunnitteluprosesseihin.|  
|**Estetty**|Et voi käyttää nimikettä missä nimiketapahtumassa.|  

> [!NOTE]
> Estetyt nimikkeet voidaan palauttaa. Tämä tarkoittaa sitä, etteivät mitkään yllämainitut asetukset päden, kun nimikettä käytetään palautustilauksissa ja hyvitysmaksuissa.

Kun luot uusia asiakirjoja aiemmin luotujen asiakirjojen perusteella **Kopioi asiakirjasta** -toiminnolla, saat ilmoituksen, jos lähdeasiakirjan riveillä olevia nimikkeitä on estetty. Estetyt asiakirjarivit jätetään pois uudesta asiakirjasta, ja ilmoitus sisältää yhteenvedon kaikista lähdeasiakirjassa estetyistä asiakirjariveistä.

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Nimikkeen myyntiriveille viennin estäminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.  
2.  Valitse estettävä nimike ja valitse sitten **Myynti estetty** -valintaruutu.  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Nimikkeen ostoriveille viennin estäminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.  
2.  Valitse estettävä nimike ja valitse sitten **Osto estetty** -valintaruutu.  

## <a name="to-block-an-item-from-being-posted"></a>Nimikkeen kirjaamisen estäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Valitse estettävä nimike ja valitse sitten **Estetty**-valintaruutu.

## <a name="see-also"></a>Katso myös  
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varasto](inventory-manage-inventory.md)  
