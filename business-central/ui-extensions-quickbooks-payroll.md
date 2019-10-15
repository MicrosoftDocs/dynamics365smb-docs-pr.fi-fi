---
title: QuickBooks Payroll -tiedoston tuontilaajennuksen käyttäminen | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten laajennuksella voi tuoda palkkatapahtumat QuickBooksista.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 42514576f7fb9542bbecfbbe8e9ff7996040da9b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311114"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a>QuickBooks Payroll -tiedoston tuontilaajennus
QuickBooks Payroll -tiedoston tuontilaajennuksella voi tuoda palkanlaskentatapahtumia QuickBooksista pääkirjanpidon tileille [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Tämä on kätevää esimerkiksi siirryttäessä QuickBooksista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin tai silloin, kun palkanlaskenta ulkoistetaan mutta haluat kuitenkin seurata sitä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.

## <a name="steps-to-import-payroll-data"></a>Palkanlaskentatietojen tuonnin ohjeet
Ensiksi sinun tai kirjanpitäjäsi on vietävä palkanlaskentatiedot .IIF-tiedostoon QuickBooksin vientitoiminnoilla. Avaa seuraavaksi **Yleiset päiväkirjat** -sivu [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tuo tiedosto **Tuo palkkatapahtumat** -toiminnolla. Tuontiprosessin aikana QuickBooksin kirjanpitotilit yhdistetään vastaaviin [!INCLUDE[d365fin](includes/d365fin_md.md)]in tileihin. Lopuksi palkkatapahtumat kirjataan [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tilin yhdistämisen mukaisesti. 

Lisätietoja on kohdassa [Palkkatapahtumien tuominen](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)    
[Rahoitus](finance.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
