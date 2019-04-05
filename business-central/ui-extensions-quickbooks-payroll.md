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
ms.date: 01/09/2019
ms.author: bholtorf
ms.openlocfilehash: ac68f8a4d67224ad55b1c34ff9b2e4ffa2c372aa
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795412"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="da005-103">QuickBooks Payroll -tiedoston tuontilaajennus</span><span class="sxs-lookup"><span data-stu-id="da005-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="da005-104">QuickBooks Payroll -tiedoston tuontilaajennuksella voi tuoda palkanlaskentatapahtumia QuickBooksista pääkirjanpidon tileille [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="da005-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="da005-105">Tämä on kätevää esimerkiksi siirryttäessä QuickBooksista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin tai silloin, kun palkanlaskenta ulkoistetaan mutta haluat kuitenkin seurata sitä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="da005-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="da005-106">Palkanlaskentatietojen tuonnin ohjeet</span><span class="sxs-lookup"><span data-stu-id="da005-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="da005-107">Ensiksi sinun tai kirjanpitäjäsi on vietävä palkanlaskentatiedot .IIF-tiedostoon QuickBooksin vientitoiminnoilla.</span><span class="sxs-lookup"><span data-stu-id="da005-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="da005-108">Avaa seuraavaksi **Yleiset päiväkirjat** -sivu [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tuo tiedosto **Tuo palkkatapahtumat** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="da005-108">The second step is to open the **General Journals** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="da005-109">Tuontiprosessin aikana QuickBooksin kirjanpitotilit yhdistetään vastaaviin [!INCLUDE[d365fin](includes/d365fin_md.md)]in tileihin.</span><span class="sxs-lookup"><span data-stu-id="da005-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="da005-110">Lopuksi palkkatapahtumat kirjataan [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tilin yhdistämisen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="da005-110">The final step is to post the payroll transactions in [!INCLUDE[d365fin](includes/d365fin_md.md)] according to the account mapping.</span></span> 

<span data-ttu-id="da005-111">Lisätietoja on kohdassa [Palkkatapahtumien tuominen](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="da005-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="da005-112">Katso myös</span><span class="sxs-lookup"><span data-stu-id="da005-112">See Also</span></span>
<span data-ttu-id="da005-113">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="da005-113">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="da005-114">[Rahoitus](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="da005-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="da005-115">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="da005-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
