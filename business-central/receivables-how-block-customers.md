---
title: Myynnin estäminen asiakkaille
description: Voit tarvittaessa estää asiakasta sisältymästä myyntiasiakirjoihin ja muihin myyntitapahtumiin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a5ac7b1cd9d58c91584c2777442094bace0673fd
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436021"
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
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Valitse asiakas ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Estetty**-kentässä, mitä haluat estää, kuten yllä olevassa taulukossa on kuvattu.

## <a name="see-also"></a>Katso myös  
[Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md)  
[Avointen saldojen perintä](receivables-collect-outstanding-balances.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]