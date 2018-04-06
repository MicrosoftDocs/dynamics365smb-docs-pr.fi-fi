---
title: "Tietojen siirtäminen Dynamics GP:stä tietojen siirron laajennuksella | Microsoft Docs"
description: "Voit siirtää asiakkaita, toimittajia, varastonimikkeitä ja tilejä Dynamics GP:stä Business Central -sovellukseen Dynamics GP:n tietojen siirron laajennuksella."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5d689a43e3debe51cfbb9306252d0c9f75e7bb70
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-business-central"></a><span data-ttu-id="4c22f-103">Dynamics GP -tietojen siirron laajennus Business Central -sovellusta varten</span><span class="sxs-lookup"><span data-stu-id="4c22f-103">The Dynamics GP Data Migration Extension for Business Central</span></span> 
<span data-ttu-id="4c22f-104">Tämän laajennuksen avulla asiakkaat, toimittajat, varastonimikkeet ja tilit on helppo siirtää Dynamics GP:stä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="4c22f-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4c22f-105">Jos yrityksessä on käytössä Dynamics GP, voit viedä soveltuvat päätietueet ja lisätä tiedot [!INCLUDE[d365fin](includes/d365fin_md.md)]iin avaamalla avustetun asennusoppaan.</span><span class="sxs-lookup"><span data-stu-id="4c22f-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4c22f-106">Lisätietoja on kohdassa [Tietojen siirtäminen muista rahoitusjärjestelmistä](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="4c22f-106">For more information, see [Migrate Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="4c22f-107">Tietojen vieminen Dynamics GP:stä</span><span class="sxs-lookup"><span data-stu-id="4c22f-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="4c22f-108">Sinun on vietävä tiedostoon osa tai kaikki aiemmin luodut asiakkaat, toimittajat, varastonimikkeet ja tilit Dynamics GP:n tietojen vientitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="4c22f-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="4c22f-109">Voit viedä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin seuraavan tyyppisiä tietoja:</span><span class="sxs-lookup"><span data-stu-id="4c22f-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="4c22f-110">Tili</span><span class="sxs-lookup"><span data-stu-id="4c22f-110">Account</span></span>  
* <span data-ttu-id="4c22f-111">Asiakas</span><span class="sxs-lookup"><span data-stu-id="4c22f-111">Customer</span></span>  
* <span data-ttu-id="4c22f-112">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="4c22f-112">Item</span></span>  
* <span data-ttu-id="4c22f-113">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="4c22f-113">Vendor</span></span>  

<span data-ttu-id="4c22f-114">Dynamics GP:n tietojen siirtolaajennus yhdistää viedyt tiedot automaattisesti, joten tiedot ovat nopeasti käytettävissä uudessa [!INCLUDE[d365fin](includes/d365fin_md.md)]-yritykseen.</span><span class="sxs-lookup"><span data-stu-id="4c22f-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="4c22f-115">Prosessin aikana luodaan tukevia määritystietoja, kuten kirjausryhmiä.</span><span class="sxs-lookup"><span data-stu-id="4c22f-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="4c22f-116">Varastonimikkeet tuodaan järjestelmään käyttämällä FIFO-menetelmää kustannusten arvostukseen.</span><span class="sxs-lookup"><span data-stu-id="4c22f-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="4c22f-117">Tilit määritetään Dynamics GP:n dimensioita sisältävänä päätilisegmenttinä, koska [!INCLUDE[d365fin](includes/d365fin_long_md.md)]issa ei ole tilisegmenttejä.</span><span class="sxs-lookup"><span data-stu-id="4c22f-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c22f-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4c22f-118">See Also</span></span>
[<span data-ttu-id="4c22f-119">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="4c22f-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="4c22f-120">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="4c22f-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

