---
title: Myynnin estäminen asiakkaille
description: Voit tarvittaessa estää asiakasta sisältymästä myyntiasiakirjoihin ja muihin myyntitapahtumiin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7cc82ab0aaf28b355117571d0d2cc5869141693f
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410714"
---
# <a name="block-customers"></a>Asiakkaiden estäminen
Voit estää asiakkaan esimerkiksi maksukyvyttömyyden vuoksi niin, että asiakasta ei voi lisätä myyntiasiakirjaan tai asiakkaalle ei voi kirjata tapahtumia.

Asiakkaan estämisen lisäksi voit määrittää estoon asiakkaan myyntisaatavat yhdessä muistutusten kanssa. Lisätietoja on kohdassa [Avointen saldojen perintä](receivables-collect-outstanding-balances.md).   

Seuraavassa taulukossa kuvaillaan eri asiakkaiden estoasetukset.  

|Asetus|Kuvaus|  
|--------------------|------------|  
|**Tyhjä**|Tapahtumat ovat sallittuja tälle asiakkaalle.|
|**Toimitus**|Tälle asiakkaalle ei voi luoda uusia tilauksia ja toimituksia. Aiemmin luodut toimitukset, joita ei ole vielä laskutettu, saa laskuttaa.|  
|**Lasku**|Tälle asiakkaalle ei voi luoda uusia tilauksia, toimituksia ja laskuja. Aiemmin luotuja toimituksia, joita ei ole vielä laskutettu, ei voi laskuttaa. Voit edelleen lähettää asiakkaalle muistutuksia ja viivästyskulujen laskuja.|  
|**Kaikki**|Yksikään tapahtuma ei ole sallittu tälle asiakkaalle, eivät myöskään maksut.|  

## <a name="to-block-a-customer"></a>Asiakkaan estäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
2. Valitse asiakas ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Estetty**-kentässä, mitä haluat estää, kuten yllä olevassa taulukossa on kuvattu.

## <a name="see-also"></a>Katso myös  
[Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md)  
[Avointen saldojen perintä](receivables-collect-outstanding-balances.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
