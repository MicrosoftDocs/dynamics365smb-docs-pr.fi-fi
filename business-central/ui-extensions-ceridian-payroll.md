---
title: Palkanlaskennan tai palkkatietojen tuominen Ceridian Payroll -laajennuksella
description: Voit tuoda tällä laajennuksella palkkatapahtumia Ceridian HR/Payroll (USA)- ja Ceridian PowerPay (Kanada) -palveluista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e85defd6570795fb5e0573af44d43c6a41f02c1d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377396"
---
# <a name="the-ceridian-payroll-extension"></a><span data-ttu-id="039eb-103">Ceridian Payroll -laajennus</span><span class="sxs-lookup"><span data-stu-id="039eb-103">The Ceridian Payroll Extension</span></span>

<span data-ttu-id="039eb-104">Jotta palkanmaksut ja liittyvät tapahtumat voidaan käsitellä, palkanlaskennan tarjoajan tekemät rahoitustapahtumat on tuotava ja kirjattava pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="039eb-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="039eb-105">Voit tehdä tämän tuomalla ensin palkanlaskennan tarjoajalta saadun csv-tiedoston **Yleinen päiväkirja** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="039eb-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="039eb-106">Linkitä sitten ulkoiset tilit palkanlaskentatiedostoon soveltuvissa KP-tileissä.</span><span class="sxs-lookup"><span data-stu-id="039eb-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="039eb-107">Kirjaa lopuksi palkkatapahtumat tilin yhdistämisen perusteella.</span><span class="sxs-lookup"><span data-stu-id="039eb-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="039eb-108">Lisätietoja on kohdassa [Palkkatapahtumien tuominen](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="039eb-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="039eb-109">Voit tuoda Ceridian Payroll -laajennuksella palkkatapahtumia Ceridian HR/Payroll (USA)- ja Ceridian PowerPay (Kanada) -palveluista.</span><span class="sxs-lookup"><span data-stu-id="039eb-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="039eb-110">Katso myös</span><span class="sxs-lookup"><span data-stu-id="039eb-110">See Also</span></span>

<span data-ttu-id="039eb-111">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="039eb-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="039eb-112">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="039eb-112">Finance</span></span>](finance.md)  
<span data-ttu-id="039eb-113">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="039eb-113">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]