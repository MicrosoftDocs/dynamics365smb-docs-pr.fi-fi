---
title: Tietoja valmiin tuotantotilauksen kustannuksista | Microsoft Docs
description: Tuotantotilauksen valmistuminen on erittäin tärkeää tuotettavan nimikkeen kustannuselinkaaren päättämisen kannalta. Lopulliset kustannukset (tavallisen kustannusympäristön vaihtelut, FIFO-menetelmän lopputuotteet, keskiarvo tai LIFO-kustannusympäristö) lasketaan Muuta kustannuksia - Nimiketapahtumat -eräajolla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0c9cf50b7c3b46c67cacebf67b80b4ba911023c4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747214"
---
# <a name="about-finished-production-order-costs"></a>Tietoja valmiin tuotantotilauksen kustannuksista
Tuotantotilauksen valmistuminen on erittäin tärkeää tuotettavan nimikkeen kustannuselinkaaren päättämisen kannalta. Lopulliset kustannukset (tavallisen kustannusympäristön vaihtelut; FIFO-menetelmän lopputuotteet, keskiarvo tai LIFO-kustannusympäristö) lasketaan **Muuta kustannuksia - Nimiketapahtumat** -eräajolla, joka mahdollistaa nimikkeen tuotantokustannusten täsmäyttämisen. Vain sellaisten nimikkeiden kustannuksia voi muuttaa, joiden tila on **Valmis**. Sen vuoksi on ehdottoman tärkeää, että valmistuneen tuotantotilauksen tilaksi vaihdetaan **Valmis**.  

## <a name="example"></a>Esimerkki  
 Kun materiaalia kulutetaan tavallisessa kustannusympäristössä nimikkeen tuottamiseksi, nimikkeen kustannukset sekä työn kustannukset ja yleiskustannukset kirjataan KET-tilille. Kun nimike on tuotettu, standardikustannusten summa vähennetään KET:istä. Yleensä näiden kustannusten tulos ei ole nolla. Jotta näiden kustannusten tulokseksi saadaan nolla, **Muuta kustannuksia - Nimiketapahtumat** -eräajo on suoritettava ja huomioitava, että vain **Valmis**-tilassa olevat tuotantotilaukset otetaan huomioon muutoksessa.  

## <a name="see-also"></a>Katso myös  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Tuotanto](production-manage-manufacturing.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]