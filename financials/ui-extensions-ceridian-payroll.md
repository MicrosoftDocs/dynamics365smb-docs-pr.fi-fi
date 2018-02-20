---
title: Palkanlaskennan tai palkkatietojen tuonti Ceridian Payroll -laajennuksella | Microsoft Docs
description: "Voit tuoda tällä laajennuksella palkkatapahtumia Ceridian HR/Payroll (USA)- ja Ceridian PowerPay (Kanada) -palveluista."
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
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 442459e82ebeb6b5b767b443e49c62ff0d4364d1
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="the-ceridian-payroll-extension-to-finance-and-operations-business-edition"></a><span data-ttu-id="a67fd-103">Finance and Operations, Business editionin Ceridian Payroll -laajennus</span><span class="sxs-lookup"><span data-stu-id="a67fd-103">The Ceridian Payroll Extension to Finance and Operations, Business edition</span></span> 
<span data-ttu-id="a67fd-104">Jotta palkanmaksut ja liittyvät tapahtumat voidaan käsitellä, palkanlaskennan tarjoajan tekemät rahoitustapahtumat on tuotava ja kirjattava pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="a67fd-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="a67fd-105">Voit tehdä tämän tuomalla ensin palkanlaskennan tarjoajalta saadun csv-tiedoston **Yleinen päiväkirja** -ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="a67fd-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="a67fd-106">Linkitä sitten ulkoiset tilit palkanlaskentatiedostoon soveltuvissa KP-tileissä.</span><span class="sxs-lookup"><span data-stu-id="a67fd-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="a67fd-107">Kirjaa lopuksi palkkatapahtumat tilin yhdistämisen perusteella.</span><span class="sxs-lookup"><span data-stu-id="a67fd-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="a67fd-108">Lisätietoja on kohdassa [Palkkatapahtumien tuominen](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="a67fd-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="a67fd-109">Voit tuoda Ceridian Payroll -laajennuksella palkkatapahtumia Ceridian HR/Payroll (USA)- ja Ceridian PowerPay (Kanada) -palveluista.</span><span class="sxs-lookup"><span data-stu-id="a67fd-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="a67fd-110">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a67fd-110">See Also</span></span>
<span data-ttu-id="a67fd-111">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="a67fd-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="a67fd-112">[Rahoitus](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="a67fd-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="a67fd-113">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a67fd-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

