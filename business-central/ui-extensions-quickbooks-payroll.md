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
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="3d73d-103">QuickBooks Payroll -tiedoston tuontilaajennus</span><span class="sxs-lookup"><span data-stu-id="3d73d-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="3d73d-104">QuickBooks Payroll -tiedoston tuontilaajennuksella voi tuoda palkanlaskentatapahtumia QuickBooksista pääkirjanpidon tileille [!INCLUDE[prod_short](includes/prod_short.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="3d73d-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="3d73d-105">Tämä on kätevää esimerkiksi siirryttäessä QuickBooksista [!INCLUDE[prod_short](includes/prod_short.md)]iin tai silloin, kun palkanlaskenta ulkoistetaan mutta haluat kuitenkin seurata sitä [!INCLUDE[prod_short](includes/prod_short.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="3d73d-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="3d73d-106">Palkanlaskentatietojen tuonnin ohjeet</span><span class="sxs-lookup"><span data-stu-id="3d73d-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="3d73d-107">Ensiksi sinun tai kirjanpitäjäsi on vietävä palkanlaskentatiedot .IIF-tiedostoon QuickBooksin vientitoiminnoilla.</span><span class="sxs-lookup"><span data-stu-id="3d73d-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="3d73d-108">Avaa seuraavaksi **Yleiset päiväkirjat** -sivu [!INCLUDE[prod_short](includes/prod_short.md)]issa tuo tiedosto **Tuo palkkatapahtumat** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="3d73d-108">The second step is to open the **General Journals** page in [!INCLUDE[prod_short](includes/prod_short.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="3d73d-109">Tuontiprosessin aikana QuickBooksin kirjanpitotilit yhdistetään vastaaviin [!INCLUDE[prod_short](includes/prod_short.md)]in tileihin.</span><span class="sxs-lookup"><span data-stu-id="3d73d-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="3d73d-110">Lopuksi palkkatapahtumat kirjataan [!INCLUDE[prod_short](includes/prod_short.md)]issa tilin yhdistämisen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="3d73d-110">The final step is to post the payroll transactions in [!INCLUDE[prod_short](includes/prod_short.md)] according to the account mapping.</span></span> 

<span data-ttu-id="3d73d-111">Lisätietoja on kohdassa [Palkkatapahtumien tuominen](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="3d73d-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3d73d-112">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3d73d-112">See Also</span></span>
<span data-ttu-id="3d73d-113">[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="3d73d-113">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="3d73d-114">[Rahoitus](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="3d73d-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="3d73d-115">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3d73d-115">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]