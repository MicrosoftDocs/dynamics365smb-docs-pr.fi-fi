---
title: "Quickbooks Payroll -tiedoston tuontilaajennuksen käyttäminen | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten laajennuksella voi tuoda palkkatapahtumat Quickbooks Payroll -palvelusta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 03/29/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: c826ab2f82b2fb0d53339690a2da4978d79ab643
ms.contentlocale: fi-fi
ms.lasthandoff: 11/10/2017

---
# <a name="the-quickbooks-payroll-file-import-extension-to-dynamics-365-business-edition"></a><span data-ttu-id="411eb-103">Dynamics 365 Business editionin Quickbooks Payroll -tiedoston tuontilaajennus</span><span class="sxs-lookup"><span data-stu-id="411eb-103">The Quickbooks Payroll File Import Extension to Dynamics 365 Business edition</span></span> 
<span data-ttu-id="411eb-104">Jotta palkanmaksut ja liittyvät tapahtumat voidaan käsitellä, palkanlaskennan tarjoajan tekemät rahoitustapahtumat on tuotava ja kirjattava pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="411eb-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="411eb-105">Voit tehdä tämän tuomalla ensin palkanlaskennan tarjoajalta saadun csv-tiedoston **Yleinen päiväkirja** -ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="411eb-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="411eb-106">Linkitä sitten ulkoiset tilit palkanlaskentatiedostoon soveltuvissa KP-tileissä.</span><span class="sxs-lookup"><span data-stu-id="411eb-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="411eb-107">Kirjaa lopuksi palkkatapahtumat tilin yhdistämisen perusteella.</span><span class="sxs-lookup"><span data-stu-id="411eb-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="411eb-108">Lisätietoja on kohdassa [Toimintaohje: Palkkatapahtumien tuominen](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="411eb-108">For more information, see [How to: Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="411eb-109">Quickbooks-palkanlaskentatiedostojen tuontilaajennuksen avulla voit tuoda palkkatapahtumat Quickbooks-palvelusta.</span><span class="sxs-lookup"><span data-stu-id="411eb-109">The Quickbooks Payroll File Import extension allows you to import payroll transaction from the Quickbooks Payroll service.</span></span>

## <a name="see-also"></a><span data-ttu-id="411eb-110">Katso myös</span><span class="sxs-lookup"><span data-stu-id="411eb-110">See Also</span></span>
<span data-ttu-id="411eb-111">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="411eb-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="411eb-112">[Rahoitus](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="411eb-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="411eb-113">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="411eb-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

