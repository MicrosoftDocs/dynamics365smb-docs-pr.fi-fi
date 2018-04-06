---
title: "Lisätoiminnot näyttävän tai piilottavan käyttäjäkokemuksen valitseminen | Microsoft Docs"
description: "Tutustu, miten Dynamics 365 for Financialsin Basic- ja Essential-käyttäjäkokemus tarkoittaa käyttöliittymässä, sovellusalueilla ja yrityksessä."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 03/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f1c5b49185621a960c84e599bbd267bd534a3730
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="customizing-your-included365finincludesd365finmdmd-experience"></a><span data-ttu-id="e159b-103">[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttökokemuksen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="e159b-103">Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="e159b-104"> on suunniteltu auttamaan liiketoiminnan käytännön asioissa toimialasta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="e159b-104"> is designed to help you run your business, regardless which line of business you are in.</span></span> <span data-ttu-id="e159b-105">[!INCLUDE[d365fin](includes/d365fin_md.md)]in ydintä ovat talousraportointi sekä myynti- ja ostoprosessit.</span><span class="sxs-lookup"><span data-stu-id="e159b-105">At the core of [!INCLUDE[d365fin](includes/d365fin_md.md)], you find financial reporting and sales and purchasing processes.</span></span> <span data-ttu-id="e159b-106">Voit lisätä siihen kokemuksia liiketoiminnan tarpeiden mukaan lisäämällä laajennuksia AppSourcesta tai muuttamalla yrityksen Kokemus-asetusta.</span><span class="sxs-lookup"><span data-stu-id="e159b-106">You add experiences to that according to your business needs by adding extensions from AppSource or by changing the Experience setting for your company.</span></span> <span data-ttu-id="e159b-107">Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md) tai alla olevassa Toimintojen näyttäminen tai piilottaminen käyttäjäkokemuksen valinnan avulla -osassa.</span><span class="sxs-lookup"><span data-stu-id="e159b-107">For more information, see [Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md), or the "Choosing a User Experience to Show or Hide Features" section below.</span></span>

## <a name="choosing-a-user-experience-to-show-or-hide-features"></a><span data-ttu-id="e159b-108">Ominaisuuksien näyttäminen tai piilottaminen valitsemalla käyttäjäkokemus</span><span class="sxs-lookup"><span data-stu-id="e159b-108">Choosing a User Experience to Show or Hide Features</span></span>
<span data-ttu-id="e159b-109">Käyttäjäkokemus määrittää, kuinka suurta osaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in perustoiminnoista voit työtovereittesi kanssa käyttää.</span><span class="sxs-lookup"><span data-stu-id="e159b-109">The user experience determines how much of the core functionality is available when you and your colleagues use [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e159b-110">Voit valita yrityksen käyttökokemuksen **Yrityksen tiedot** -ikkunan **Kokemus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e159b-110">You can choose the user experience for your company in the **Company Information** window, in the **Experience** field.</span></span>

> [!NOTE]  
> <span data-ttu-id="e159b-111">Tämä asetus koskee kaikki yrityksen käyttäjiä.</span><span class="sxs-lookup"><span data-stu-id="e159b-111">This setting applies to all users in your company.</span></span> <span data-ttu-id="e159b-112">Käyttäjät voivat lisäksi mukauttaa omaa kokemustaan muuttamalla sivun asettelua ja sisältöä.</span><span class="sxs-lookup"><span data-stu-id="e159b-112">Users can customize their own experience even further by changing page layouts and content.</span></span> <span data-ttu-id="e159b-113">Lisätietoja on kohdassa [Työtilan ja sivujen mukauttaminen](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="e159b-113">For more information, see [Personalizing Your Workspace and Pages](ui-personalization-user.md).</span></span>  

<span data-ttu-id="e159b-114">Seuraavassa taulukossa on luettelo nyt käytettävissä olevista kokemuksista.</span><span class="sxs-lookup"><span data-stu-id="e159b-114">The following table lists the experiences that are currently available.</span></span>

| <span data-ttu-id="e159b-115">Kokemus</span><span class="sxs-lookup"><span data-stu-id="e159b-115">Experience</span></span> | <span data-ttu-id="e159b-116">Vaikutus käyttöliittymään</span><span class="sxs-lookup"><span data-stu-id="e159b-116">Impact on User Interface</span></span> |
| --- | --- |
| <span data-ttu-id="e159b-117">**Perus**</span><span class="sxs-lookup"><span data-stu-id="e159b-117">**Basic**</span></span> |<span data-ttu-id="e159b-118">Näyttää vain yleisimpien liiketoimintatoimintojen, kuten myynnin, ostojen, varaston ja rahoituksen, perustoiminnot ja kentät.</span><span class="sxs-lookup"><span data-stu-id="e159b-118">Shows only core actions and fields within the most common business functionality, such as sales, purchasing, inventory, and finance.</span></span> |
| <span data-ttu-id="e159b-119">**Olennainen**</span><span class="sxs-lookup"><span data-stu-id="e159b-119">**Essential**</span></span> |<span data-ttu-id="e159b-120">Näyttää kaikkien yleisten liiketoimintatoimintojen kaikki toiminnot ja kentät.</span><span class="sxs-lookup"><span data-stu-id="e159b-120">Shows all actions and fields for all common business functionality.</span></span>|
| <span data-ttu-id="e159b-121">**Premium**</span><span class="sxs-lookup"><span data-stu-id="e159b-121">**Premium**</span></span> |<span data-ttu-id="e159b-122">Näyttää kaikkien liiketoimintojen toiminnot ja kentät myös valmistukselle ja huoltohallinnolle.</span><span class="sxs-lookup"><span data-stu-id="e159b-122">Shows all actions and fields for all business functionality, including Manufacturing and Service Management.</span></span>|

> [!NOTE]  
> <span data-ttu-id="e159b-123">[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa valitut käyttökokemukset riippuvat ratkaisun käyttöoikeudesta, jota kutsutaan palvelupaketiksi.</span><span class="sxs-lookup"><span data-stu-id="e159b-123">The experiences that you can select from in [!INCLUDE[d365fin](includes/d365fin_md.md)] depend on your solution license, called a plan.</span></span> <span data-ttu-id="e159b-124">Lisätietoja **Essential**- ja **Premium**-palvelupaketeista on Microsoft Dynamics 365:n markkinointisivuston kohdassa [Business Central](https://go.microsoft.com/fwlink/?linkid=870242).</span><span class="sxs-lookup"><span data-stu-id="e159b-124">For information about the **Essential** and **Premium** plans, see [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) on the Microsoft Dynamics 365 marketing site.</span></span> 

## <a name="see-also"></a><span data-ttu-id="e159b-125">Katso myös .</span><span class="sxs-lookup"><span data-stu-id="e159b-125">See also</span></span>
[<span data-ttu-id="e159b-126">Uusien yritysten luominen</span><span class="sxs-lookup"><span data-stu-id="e159b-126">Creating New Companies</span></span>](about-new-company.md)  
[<span data-ttu-id="e159b-127">Perusasetusten muuttaminen</span><span class="sxs-lookup"><span data-stu-id="e159b-127">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
<span data-ttu-id="e159b-128">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="e159b-128">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="e159b-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e159b-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

