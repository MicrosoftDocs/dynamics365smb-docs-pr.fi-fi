---
title: Nimikkeiden myynnin tai oston estäminen
description: Voit estää nimikkeen käytön esimerkiksi myynti- tai ostoasiakirjoissa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4bc130d6982d969084f7fcbf3618893978317f36
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786046"
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


[!INCLUDE[footer-include](includes/footer-banner.md)]