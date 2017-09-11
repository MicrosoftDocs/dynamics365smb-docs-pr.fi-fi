---
title: "Arvonlisävero Kanadassa| Microsoft Docs"
description: "Lue kanadalaisesta tavaroita ja palveluita koskevasta arvonlisäverokäytännöstä."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 571b11f4f18ffd194bdfe1d1d412bca87df4b868
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="reporting-sales-tax-and-goodsservices-tax-in-canada"></a><span data-ttu-id="8f333-103">Kanadan arvonlisäveron raportointi</span><span class="sxs-lookup"><span data-stu-id="8f333-103">Reporting Sales Tax and Goods/Services Tax in Canada</span></span>
<span data-ttu-id="8f333-104">Jos Kanadassa toimittajalla ei ole liiketilaa provinssissa, jossa ostoja tehdään, toimittaja veloittaa vain arvonlisäveroa (GST) tai harmonisoitua arvonlisäveroa (HST).</span><span class="sxs-lookup"><span data-stu-id="8f333-104">In Canada, when a vendor does not have a business presence in the province in which purchases are made, the vendor will charge the Goods and Services Tax (GST) or Harmonized Sales Tax (HST) only.</span></span> <span data-ttu-id="8f333-105">Jos provinssissa on käytössä provinssin arvonlisävero (PST), ostajan on laskettava myös PST ja maksettava se suoraan provinssiin.</span><span class="sxs-lookup"><span data-stu-id="8f333-105">However, if the province has a Provincial Sales Tax (PST), then the purchaser must still calculate the PST and pay it directly to the province.</span></span> <span data-ttu-id="8f333-106">Kun provinssin veroaluekoodi on valittuna, [!INCLUDE[d365fin](includes/d365fin_md.md)] käyttää sitä PST:n laskemisessa ja kirjaa sen. Tällöin verovelkaa on sekä pääkirjanpidossa että arvonlisäverotietueissa.</span><span class="sxs-lookup"><span data-stu-id="8f333-106">When a Provincial Tax Area Code is selected, [!INCLUDE[d365fin](includes/d365fin_md.md)] uses it to calculate the PST and post it so that there is a tax liability in both the general ledger and the tax entry records.</span></span> <span data-ttu-id="8f333-107">Tämän vuoksi valitun veroaluekoodin tulee olla se, jossa on valittuna PST, ei GST.</span><span class="sxs-lookup"><span data-stu-id="8f333-107">Therefore, the tax area code selected here should be one where only the PST is included, not the GST.</span></span>  

<span data-ttu-id="8f333-108">Lisätietoja on kohdassa [Kanadan arvonlisävero ja veroryhmät](us-finance-sales-tax.md).</span><span class="sxs-lookup"><span data-stu-id="8f333-108">For more information about sales tax, see [Sales Tax and Tax Groups in the US and Canada](us-finance-sales-tax.md).</span></span>  

## <a name="submitting-the-gsthst-file"></a><span data-ttu-id="8f333-109">GST-/HST-tiedoston lähettäminen</span><span class="sxs-lookup"><span data-stu-id="8f333-109">Submitting the GST/HST File</span></span>
<span data-ttu-id="8f333-110">Ostoasiakirjojen verotietoja käytetään veroviranomaisille annettavan GST-/HST-verkkotiedoston siirron luomisessa.</span><span class="sxs-lookup"><span data-stu-id="8f333-110">The tax information in purchase documents is used to generate a GST/HST online file transfer that you must provide to the tax authorities.</span></span> <span data-ttu-id="8f333-111">Tämä tiedosto sisältää arvonlisäveron (GST) ja harmonisoidun arvonlisäveron (HST).</span><span class="sxs-lookup"><span data-stu-id="8f333-111">This file includes goods and services tax (GST) and harmonized sales tax (HST).</span></span> <span data-ttu-id="8f333-112">Tiedosto on luotu .tax-muodossa, joka voidaan siirtää verkossa.</span><span class="sxs-lookup"><span data-stu-id="8f333-112">The file is created in a .tax file format, which can be transferred online.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8f333-113">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8f333-113">See Also</span></span>
[<span data-ttu-id="8f333-114">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="8f333-114">Finance</span></span>](finance.md)  
[<span data-ttu-id="8f333-115">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8f333-115">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="8f333-116">Yhdysvaltojen ja Kanadan arvonlisävero ja veroryhmät</span><span class="sxs-lookup"><span data-stu-id="8f333-116">Sales Tax and Tax Groups in the US and Canada</span></span>](us-finance-sales-tax.md)  
<span data-ttu-id="8f333-117">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f333-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

