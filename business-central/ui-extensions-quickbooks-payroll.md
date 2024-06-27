---
title: QuickBooks Payroll -tiedoston tuontilaajennuksen käyttäminen | Microsoft Docs
description: 'Tässä artikkelissa kerrotaan, miten laajennuksella voi tuoda palkkatapahtumat QuickBooksista.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms. search.keywords: 'app, add-in, manifest, customize, salary, wage'
ms.date: 12/07/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="the-quickbooks-payroll-file-import-extension"></a>QuickBooks Payroll -tiedoston tuontilaajennus
QuickBooks Payroll -tiedoston tuontilaajennuksella voi tuoda palkanlaskentatapahtumia QuickBooksista pääkirjanpidon tileille [!INCLUDE[prod_short](includes/prod_short.md)]issa. Tämä on kätevää esimerkiksi siirryttäessä QuickBooksista [!INCLUDE[prod_short](includes/prod_short.md)]iin tai silloin, kun palkanlaskenta ulkoistetaan mutta haluat kuitenkin seurata sitä [!INCLUDE[prod_short](includes/prod_short.md)]issa.

## <a name="steps-to-import-payroll-data"></a>Palkanlaskentatietojen tuonnin ohjeet
Ensiksi sinun tai kirjanpitäjäsi on vietävä palkanlaskentatiedot .IIF-tiedostoon QuickBooksin vientitoiminnoilla. Avaa seuraavaksi **Yleiset päiväkirjat** -sivu [!INCLUDE[prod_short](includes/prod_short.md)]issa tuo tiedosto **Tuo palkkatapahtumat** -toiminnolla. Tuontiprosessin aikana QuickBooksin kirjanpitotilit yhdistetään vastaaviin [!INCLUDE[prod_short](includes/prod_short.md)]in tileihin. Lopuksi palkkatapahtumat kirjataan [!INCLUDE[prod_short](includes/prod_short.md)]issa tilin yhdistämisen mukaisesti. 

Lisätietoja on kohdassa [Palkkatapahtumien tuominen](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Katso myös
[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)    
[Rahoitus](finance.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
