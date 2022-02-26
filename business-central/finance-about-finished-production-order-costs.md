---
title: Tietoja valmiin tuotantotilauksen kustannuksista
description: Tuotantotilauksen viimeisteleminen on avainasemassa tuotantonimikkeen kustannuselinkaaren päättämisen kannalta. Lopulliset kustannukset lasketaan eräajossa Muuta kustannuksia - Nimiketapahtumat.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.form: 99000867
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: f8e4c6b4a0db47c56650ea91410670d81bae4cef
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2022
ms.locfileid: "7973646"
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