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
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: c7ac2a17ecc0c2a33ea166968f577ca46e8282ed
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "920533"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="a6b2a-103">QuickBooks Payroll -tiedoston tuontilaajennus</span><span class="sxs-lookup"><span data-stu-id="a6b2a-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="a6b2a-104">QuickBooks Payroll -tiedoston tuontilaajennuksella voi tuoda palkanlaskentatapahtumia QuickBooksista pääkirjanpidon tileille [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="a6b2a-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a6b2a-105">Tämä on kätevää esimerkiksi siirryttäessä QuickBooksista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin tai silloin, kun palkanlaskenta ulkoistetaan mutta haluat kuitenkin seurata sitä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="a6b2a-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="a6b2a-106">Palkanlaskentatietojen tuonnin ohjeet</span><span class="sxs-lookup"><span data-stu-id="a6b2a-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="a6b2a-107">Ensiksi sinun tai kirjanpitäjäsi on vietävä palkanlaskentatiedot .IIF-tiedostoon QuickBooksin vientitoiminnoilla.</span><span class="sxs-lookup"><span data-stu-id="a6b2a-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="a6b2a-108">Avaa seuraavaksi **Yleiset päiväkirjat** -sivu [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tuo tiedosto **Tuo palkkatapahtumat** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="a6b2a-108">The second step is to open the **General Journals** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="a6b2a-109">Tuontiprosessin aikana QuickBooksin kirjanpitotilit yhdistetään vastaaviin [!INCLUDE[d365fin](includes/d365fin_md.md)]in tileihin.</span><span class="sxs-lookup"><span data-stu-id="a6b2a-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a6b2a-110">Lopuksi palkkatapahtumat kirjataan [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tilin yhdistämisen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a6b2a-110">The final step is to post the payroll transactions in [!INCLUDE[d365fin](includes/d365fin_md.md)] according to the account mapping.</span></span> 

<span data-ttu-id="a6b2a-111">Lisätietoja on kohdassa [Palkkatapahtumien tuominen](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="a6b2a-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a6b2a-112">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a6b2a-112">See Also</span></span>
<span data-ttu-id="a6b2a-113">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="a6b2a-113">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="a6b2a-114">[Rahoitus](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="a6b2a-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="a6b2a-115">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a6b2a-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
