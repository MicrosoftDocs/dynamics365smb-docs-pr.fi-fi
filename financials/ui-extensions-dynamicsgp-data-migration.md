---
title: "Tietojen siirtäminen Dynamics GP:stä tietojen siirron laajennuksella | Microsoft Docs"
description: "Voit siirtää asiakkaita, toimittajia, varastonimikkeitä ja tilejä Dynamics GP:stä Finance and Operations, Business editioniin Dynamics GP:n tietojen siirron laajennuksella."
documentationcenter: 
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: bfd3ca3e28b6eb3efa2a16cc131b508db6bd1590
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-finance-and-operations-business-edition"></a><span data-ttu-id="f40fb-103">Finance and Operations, Business editionin Dynamics GP -tiedonsiirtolaajennus</span><span class="sxs-lookup"><span data-stu-id="f40fb-103">The Dynamics GP Data Migration Extension for Finance and Operations, Business edition</span></span> 
<span data-ttu-id="f40fb-104">Tämän laajennuksen avulla asiakkaat, toimittajat, varastonimikkeet ja tilit on helppo siirtää Dynamics GP:stä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="f40fb-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f40fb-105">Jos yrityksessä on käytössä Dynamics GP, voit viedä soveltuvat päätietueet ja lisätä tiedot [!INCLUDE[d365fin](includes/d365fin_md.md)]iin avaamalla avustetun asennusoppaan.</span><span class="sxs-lookup"><span data-stu-id="f40fb-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f40fb-106">Lisätietoja on kohdassa [Tietojen siirtäminen muista rahoitusjärjestelmistä](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="f40fb-106">For more information, see [Migrate Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="f40fb-107">Tietojen vieminen Dynamics GP:stä</span><span class="sxs-lookup"><span data-stu-id="f40fb-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="f40fb-108">Sinun on vietävä tiedostoon osa tai kaikki aiemmin luodut asiakkaat, toimittajat, varastonimikkeet ja tilit Dynamics GP:n tietojen vientitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="f40fb-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="f40fb-109">Voit viedä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin seuraavan tyyppisiä tietoja:</span><span class="sxs-lookup"><span data-stu-id="f40fb-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="f40fb-110">Tili</span><span class="sxs-lookup"><span data-stu-id="f40fb-110">Account</span></span>  
* <span data-ttu-id="f40fb-111">Asiakas</span><span class="sxs-lookup"><span data-stu-id="f40fb-111">Customer</span></span>  
* <span data-ttu-id="f40fb-112">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="f40fb-112">Item</span></span>  
* <span data-ttu-id="f40fb-113">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="f40fb-113">Vendor</span></span>  

<span data-ttu-id="f40fb-114">Dynamics GP:n tietojen siirtolaajennus yhdistää viedyt tiedot automaattisesti, joten tiedot ovat nopeasti käytettävissä uudessa [!INCLUDE[d365fin](includes/d365fin_md.md)]-yritykseen.</span><span class="sxs-lookup"><span data-stu-id="f40fb-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="f40fb-115">Prosessin aikana luodaan tukevia määritystietoja, kuten kirjausryhmiä.</span><span class="sxs-lookup"><span data-stu-id="f40fb-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="f40fb-116">Varastonimikkeet tuodaan järjestelmään käyttämällä FIFO-menetelmää kustannusten arvostukseen.</span><span class="sxs-lookup"><span data-stu-id="f40fb-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="f40fb-117">Tilit määritetään Dynamics GP:n dimensioita sisältävänä päätilisegmenttinä, koska [!INCLUDE[d365fin](includes/d365fin_long_md.md)]issa ei ole tilisegmenttejä.</span><span class="sxs-lookup"><span data-stu-id="f40fb-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="f40fb-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f40fb-118">See Also</span></span>
[<span data-ttu-id="f40fb-119">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="f40fb-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="f40fb-120">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="f40fb-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

