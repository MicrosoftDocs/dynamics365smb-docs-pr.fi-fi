---
title: Tietoja valmiin tuotantotilauksen kustannuksista | Microsoft Docs
description: Tuotantotilauksen valmistuminen on erittäin tärkeää tuotettavan nimikkeen kustannuselinkaaren päättämisen kannalta. Lopulliset kustannukset (tavallisen kustannusympäristön vaihtelut, FIFO-menetelmän lopputuotteet, keskiarvo tai LIFO-kustannusympäristö) lasketaan Muuta kustannuksia - Nimiketapahtumat -eräajolla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 96cf025bbac137f61f41a65cbd2f9520f2c5e787
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242788"
---
# <a name="about-finished-production-order-costs"></a>Tietoja valmiin tuotantotilauksen kustannuksista
Tuotantotilauksen valmistuminen on erittäin tärkeää tuotettavan nimikkeen kustannuselinkaaren päättämisen kannalta. Lopulliset kustannukset (tavallisen kustannusympäristön vaihtelut; FIFO-menetelmän lopputuotteet, keskiarvo tai LIFO-kustannusympäristö) lasketaan **Muuta kustannuksia - Nimiketapahtumat** -eräajolla, joka mahdollistaa nimikkeen tuotantokustannusten täsmäyttämisen. Vain sellaisten nimikkeiden kustannuksia voi muuttaa, joiden tila on **Valmis**. Sen vuoksi on ehdottoman tärkeää, että valmistuneen tuotantotilauksen tilaksi vaihdetaan **Valmis**.  

## <a name="example"></a>Esimerkki  
 Kun materiaalia kulutetaan tavallisessa kustannusympäristössä nimikkeen tuottamiseksi, nimikkeen kustannukset sekä työn kustannukset ja yleiskustannukset kirjataan KET-tilille. Kun nimike on tuotettu, standardikustannusten summa vähennetään KET:istä. Yleensä näiden kustannusten tulos ei ole nolla. Jotta näiden kustannusten tulokseksi saadaan nolla, **Muuta kustannuksia - Nimiketapahtumat** -eräajo on suoritettava ja huomioitava, että vain **Valmis**-tilassa olevat tuotantotilaukset otetaan huomioon muutoksessa.  

## <a name="see-also"></a>Katso myös  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Tuotanto](production-manage-manufacturing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
