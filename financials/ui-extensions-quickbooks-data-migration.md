---
title: "QuickBooksin siirtolaajennuksen käyttäminen | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten laajennuksella tuodaan asiakkaita, toimittajia, nimikkeitä ja tilejä QuickBooks Desktopista Dynamics 365 for Financialsiin."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: fdda803b7cc2f93ae4d7353be28282dc60d904d8
ms.contentlocale: fi-fi
ms.lasthandoff: 11/10/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-business-edition"></a><span data-ttu-id="2ee3a-103">Dynamics 365 Business editionin QuickBooks-tietojen siirtolaajennus</span><span class="sxs-lookup"><span data-stu-id="2ee3a-103">The QuickBooks Data Migration Extension for Dynamics 365 Business edition</span></span>
<span data-ttu-id="2ee3a-104">Tämän laajennuksen avulla asiakkaat, toimittajat, nimikkeet ja tilit on helppo siirtää QuickBooksista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="2ee3a-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2ee3a-105">Jos yrityksessä on käytössä QuickBooks, voit viedä tarpeelliset tiedot ja ladata ne sitten [!INCLUDE[d365fin](includes/d365fin_md.md)]iin avaamalla avustetun asennusoppaan.</span><span class="sxs-lookup"><span data-stu-id="2ee3a-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="2ee3a-106">Lisätietoja on kohdassa [Tietojen tuominen muista rahoitusjärjestelmistä](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="2ee3a-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks-desktop"></a><span data-ttu-id="2ee3a-107">Tietojen vieminen QuickBooks Desktopista</span><span class="sxs-lookup"><span data-stu-id="2ee3a-107">Exporting Data from QuickBooks Desktop</span></span>
<span data-ttu-id="2ee3a-108">Osa tai kaikki asiakkaat, toimittajat, varastonimikkeet ja tilit on oltava vietynä IIF (Intuit Interchange Format) -tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="2ee3a-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="2ee3a-109">QuickBooks-tietojen siirron laajennus sisältää QuickBooks-tietojen oletusmäärityksen. Voit siis käyttää olemassa olevia tietoja, kun testaat uutta [!INCLUDE[d365fin](includes/d365fin_md.md)]-yritystä.</span><span class="sxs-lookup"><span data-stu-id="2ee3a-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="2ee3a-110">Oletusmääritys on riittävä lähes kaikissa tapauksissa. Voit kuitenkin muuttaa määritystä avustetun asennusoppaan avulla.</span><span class="sxs-lookup"><span data-stu-id="2ee3a-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="2ee3a-111">QuickBooks-ohjelman Tiedosto-valikko sisältää apuohjelman luetteloiden viemistä varten.</span><span class="sxs-lookup"><span data-stu-id="2ee3a-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="2ee3a-112">Voit viedä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin seuraavat luettelot:</span><span class="sxs-lookup"><span data-stu-id="2ee3a-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="2ee3a-113">Asiakasluettelo</span><span class="sxs-lookup"><span data-stu-id="2ee3a-113">Customer List</span></span>  
* <span data-ttu-id="2ee3a-114">Toimittajaluettelo</span><span class="sxs-lookup"><span data-stu-id="2ee3a-114">Vendor List</span></span>  
* <span data-ttu-id="2ee3a-115">Nimikeluettelo</span><span class="sxs-lookup"><span data-stu-id="2ee3a-115">Item List</span></span>  
* <span data-ttu-id="2ee3a-116">Tililuettelo</span><span class="sxs-lookup"><span data-stu-id="2ee3a-116">Account List</span></span>  

<span data-ttu-id="2ee3a-117">Viedyt tiedot tallennetaan IIF-tiedostona, jonka voi sitten ladata [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="2ee3a-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="2ee3a-118">QuickBooks-tietojen siirtolaajennuksen etsiminen</span><span class="sxs-lookup"><span data-stu-id="2ee3a-118">Finding the QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="2ee3a-119">QuickBooks-tietojen siirtolaajennus on asennettu ja valmis käytettäväksi tietojen siirtoasetusten ohjatun määrityksen osana.</span><span class="sxs-lookup"><span data-stu-id="2ee3a-119">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="2ee3a-120">Jos olet valmis aloittamaan käytön nyt ja olet vienyt tiedot QuickBooksista, valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asetusten ohjattu määritys** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2ee3a-120">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="2ee3a-121">Valitse **Siirrä liiketoimintatiedot** ja noudata oppaan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="2ee3a-121">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2ee3a-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2ee3a-122">See Also</span></span>
[<span data-ttu-id="2ee3a-123">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="2ee3a-123">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="2ee3a-124">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2ee3a-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

