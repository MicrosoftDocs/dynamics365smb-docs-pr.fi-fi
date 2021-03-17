---
title: QuickBooks Payroll -tiedoston tuontilaajennuksen käyttäminen | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten laajennuksella voi tuoda palkkatapahtumat QuickBooksista.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: fc8767f1e6a33f957b33f9076a8cee485b2f1412
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386372"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a>QuickBooks Payroll -tiedoston tuontilaajennus
QuickBooks Payroll -tiedoston tuontilaajennuksella voi tuoda palkanlaskentatapahtumia QuickBooksista pääkirjanpidon tileille [!INCLUDE[prod_short](includes/prod_short.md)]issa. Tämä on kätevää esimerkiksi siirryttäessä QuickBooksista [!INCLUDE[prod_short](includes/prod_short.md)]iin tai silloin, kun palkanlaskenta ulkoistetaan mutta haluat kuitenkin seurata sitä [!INCLUDE[prod_short](includes/prod_short.md)]issa.

## <a name="steps-to-import-payroll-data"></a>Palkanlaskentatietojen tuonnin ohjeet
Ensiksi sinun tai kirjanpitäjäsi on vietävä palkanlaskentatiedot .IIF-tiedostoon QuickBooksin vientitoiminnoilla. Avaa seuraavaksi **Yleiset päiväkirjat** -sivu [!INCLUDE[prod_short](includes/prod_short.md)]issa tuo tiedosto **Tuo palkkatapahtumat** -toiminnolla. Tuontiprosessin aikana QuickBooksin kirjanpitotilit yhdistetään vastaaviin [!INCLUDE[prod_short](includes/prod_short.md)]in tileihin. Lopuksi palkkatapahtumat kirjataan [!INCLUDE[prod_short](includes/prod_short.md)]issa tilin yhdistämisen mukaisesti. 

Lisätietoja on kohdassa [Palkkatapahtumien tuominen](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Katso myös
[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)    
[Rahoitus](finance.md)    
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]