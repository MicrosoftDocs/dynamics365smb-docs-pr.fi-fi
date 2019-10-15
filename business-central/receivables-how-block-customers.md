---
title: Asiakkaiden nimikkeiden myynnin estäminen myynnissä tai ostossa
description: Nimike voidaan merkitä Business Centralissa estetyksi myynnin tai oston osalta tai kaikkia tarkoituksia varten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c2b0d5b15571b7e8af1ed1dbee22859f4c131aa3
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316618"
---
# <a name="block-customers"></a>Asiakkaiden estäminen
Voit estää asiakkaan esimerkiksi maksukyvyttömyyden vuoksi niin, että asiakasta ei voi lisätä myyntiasiakirjaan tai asiakkaalle ei voi kirjata tapahtumia.

Asiakkaan estämisen lisäksi voit määrittää estoon asiakkaan myyntisaatavat yhdessä muistutusten kanssa. Lisätietoja on kohdassa [Avointen saldojen perintä](receivables-collect-outstanding-balances.md).   

Seuraavassa taulukossa kuvaillaan eri estoasetukset.  

|Asetus|Description|  
|--------------------|------------|  
|**Tyhjä**|Tapahtumat ovat sallittuja tälle asiakkaalle.|
|**Toimitus**|Tälle asiakkaalle ei voi luoda uusia tilauksia ja toimituksia. Aiemmin luodut toimitukset, joita ei ole vielä laskutettu, saa laskuttaa.|  
|**Lasku**|Tälle asiakkaalle ei voi luoda uusia tilauksia, toimituksia ja laskuja. Aiemmin luotuja toimituksia, joita ei ole vielä laskutettu, ei voi laskuttaa.|  
|**Kaikki**|Yksikään tapahtuma ei ole sallittu tälle asiakkaalle, eivät myöskään maksut.|  

## <a name="to-block-a-customer"></a>Asiakkaan estäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
2. Valitse asiakas ja valitse sitten **Muokkaa**-toiminto.
3. Täytä **Estetty**-kenttään jonkin yläpuolella kuvatuista vaihtoehtoista.

## <a name="see-also"></a>Katso myös  
[Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md)  
[Avointen saldojen perintä](receivables-collect-outstanding-balances.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
