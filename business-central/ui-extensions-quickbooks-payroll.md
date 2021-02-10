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
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: eae93ea8cf81a2fad6af2c3810f94d5292eef93f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757090"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="2c9e7-103">QuickBooks Payroll -tiedoston tuontilaajennus</span><span class="sxs-lookup"><span data-stu-id="2c9e7-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="2c9e7-104">QuickBooks Payroll -tiedoston tuontilaajennuksella voi tuoda palkanlaskentatapahtumia QuickBooksista pääkirjanpidon tileille [!INCLUDE[prod_short](includes/prod_short.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="2c9e7-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="2c9e7-105">Tämä on kätevää esimerkiksi siirryttäessä QuickBooksista [!INCLUDE[prod_short](includes/prod_short.md)]iin tai silloin, kun palkanlaskenta ulkoistetaan mutta haluat kuitenkin seurata sitä [!INCLUDE[prod_short](includes/prod_short.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="2c9e7-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="2c9e7-106">Palkanlaskentatietojen tuonnin ohjeet</span><span class="sxs-lookup"><span data-stu-id="2c9e7-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="2c9e7-107">Ensiksi sinun tai kirjanpitäjäsi on vietävä palkanlaskentatiedot .IIF-tiedostoon QuickBooksin vientitoiminnoilla.</span><span class="sxs-lookup"><span data-stu-id="2c9e7-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="2c9e7-108">Avaa seuraavaksi **Yleiset päiväkirjat** -sivu [!INCLUDE[prod_short](includes/prod_short.md)]issa tuo tiedosto **Tuo palkkatapahtumat** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="2c9e7-108">The second step is to open the **General Journals** page in [!INCLUDE[prod_short](includes/prod_short.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="2c9e7-109">Tuontiprosessin aikana QuickBooksin kirjanpitotilit yhdistetään vastaaviin [!INCLUDE[prod_short](includes/prod_short.md)]in tileihin.</span><span class="sxs-lookup"><span data-stu-id="2c9e7-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="2c9e7-110">Lopuksi palkkatapahtumat kirjataan [!INCLUDE[prod_short](includes/prod_short.md)]issa tilin yhdistämisen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="2c9e7-110">The final step is to post the payroll transactions in [!INCLUDE[prod_short](includes/prod_short.md)] according to the account mapping.</span></span> 

<span data-ttu-id="2c9e7-111">Lisätietoja on kohdassa [Palkkatapahtumien tuominen](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="2c9e7-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2c9e7-112">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2c9e7-112">See Also</span></span>
<span data-ttu-id="2c9e7-113">[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="2c9e7-113">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="2c9e7-114">[Rahoitus](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="2c9e7-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="2c9e7-115">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2c9e7-115">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
