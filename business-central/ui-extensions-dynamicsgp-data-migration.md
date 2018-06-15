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
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 3761bdb0d6b9a51ed309ac4189ff263de76f4679
ms.contentlocale: fi-fi
ms.lasthandoff: 05/17/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-business-central"></a><span data-ttu-id="4dfc2-103">Dynamics GP -tietojen siirron laajennus Business Central -sovellusta varten</span><span class="sxs-lookup"><span data-stu-id="4dfc2-103">The Dynamics GP Data Migration Extension for Business Central</span></span> 
<span data-ttu-id="4dfc2-104">Tämän laajennuksen avulla asiakkaat, toimittajat, varastonimikkeet ja tilit on helppo siirtää Dynamics GP:stä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="4dfc2-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4dfc2-105">Jos yrityksessä on käytössä Dynamics GP, voit viedä soveltuvat päätietueet ja lisätä tiedot [!INCLUDE[d365fin](includes/d365fin_md.md)]iin avaamalla avustetun asennusoppaan.</span><span class="sxs-lookup"><span data-stu-id="4dfc2-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4dfc2-106">Lisätietoja on kohdassa [Tietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="4dfc2-106">For more information, see [Importing Business Data from Other Finance Systems](across-import-data-configuration-packages.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="4dfc2-107">Tietojen vieminen Dynamics GP:stä</span><span class="sxs-lookup"><span data-stu-id="4dfc2-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="4dfc2-108">Sinun on vietävä tiedostoon osa tai kaikki aiemmin luodut asiakkaat, toimittajat, varastonimikkeet ja tilit Dynamics GP:n tietojen vientitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="4dfc2-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="4dfc2-109">Voit viedä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin seuraavan tyyppisiä tietoja:</span><span class="sxs-lookup"><span data-stu-id="4dfc2-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="4dfc2-110">Tili</span><span class="sxs-lookup"><span data-stu-id="4dfc2-110">Account</span></span>  
* <span data-ttu-id="4dfc2-111">Asiakas</span><span class="sxs-lookup"><span data-stu-id="4dfc2-111">Customer</span></span>  
* <span data-ttu-id="4dfc2-112">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="4dfc2-112">Item</span></span>  
* <span data-ttu-id="4dfc2-113">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="4dfc2-113">Vendor</span></span>  

<span data-ttu-id="4dfc2-114">Dynamics GP:n tietojen siirtolaajennus yhdistää viedyt tiedot automaattisesti, joten tiedot ovat nopeasti käytettävissä uudessa [!INCLUDE[d365fin](includes/d365fin_md.md)]-yritykseen.</span><span class="sxs-lookup"><span data-stu-id="4dfc2-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="4dfc2-115">Prosessin aikana luodaan tukevia määritystietoja, kuten kirjausryhmiä.</span><span class="sxs-lookup"><span data-stu-id="4dfc2-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="4dfc2-116">Varastonimikkeet tuodaan järjestelmään käyttämällä FIFO-menetelmää kustannusten arvostukseen.</span><span class="sxs-lookup"><span data-stu-id="4dfc2-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="4dfc2-117">Tilit määritetään Dynamics GP:n dimensioita sisältävänä päätilisegmenttinä, koska [!INCLUDE[d365fin](includes/d365fin_long_md.md)]issa ei ole tilisegmenttejä.</span><span class="sxs-lookup"><span data-stu-id="4dfc2-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="4dfc2-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4dfc2-118">See Also</span></span>
[<span data-ttu-id="4dfc2-119">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="4dfc2-119">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="4dfc2-120">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="4dfc2-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

