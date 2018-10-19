---
title: Business Central -sovelluksen mukauttaminen | Microsoft Docs
description: "Lisätietoja toimintojen lisäämisestä ja Business Central. -sovelluksen mukauttamisesta."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, add-in, extend, customize
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 63ba198a761b0c79c51ac94d36314310e330fc58
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="customizing-business-central"></a><span data-ttu-id="5765f-103">Business Central -sovelluksen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="5765f-103">Customizing Business Central</span></span>
<span data-ttu-id="5765f-104">Sovelluksen voi mukauttaa useilla eri tavoilla, jotta sinä ja työtoverisi voitte käyttää eniten tarvitsemianne ominaisuuksia, toimintoja ja tietoja tavalla, joka sopii parhaiten päivittäiseen työhönne.</span><span class="sxs-lookup"><span data-stu-id="5765f-104">There are different ways to customize the application to give you and your colleagues access to the features, functionality, and data that you need most, in a manner that bests suits your daily work.</span></span> <span data-ttu-id="5765f-105">Seuraavassa taulukossa kerrotaan ketkä näkevät muutokset sen mukaan, mitä teet.</span><span class="sxs-lookup"><span data-stu-id="5765f-105">Those who see the changes will depend on what you do, as described in this table.</span></span>

| <span data-ttu-id="5765f-106">Sallitut toimet</span><span class="sxs-lookup"><span data-stu-id="5765f-106">What you can do</span></span>    |  <span data-ttu-id="5765f-107">Description</span><span class="sxs-lookup"><span data-stu-id="5765f-107">Description</span></span>  |  <span data-ttu-id="5765f-108">Muutosten näkijät</span><span class="sxs-lookup"><span data-stu-id="5765f-108">Who sees the changes</span></span>  |  <span data-ttu-id="5765f-109">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="5765f-109">More information</span></span>  |
|-----|---------------|---------|-------|
|<span data-ttu-id="5765f-110">Laajennuksen asentaminen</span><span class="sxs-lookup"><span data-stu-id="5765f-110">Install an extension</span></span>|<span data-ttu-id="5765f-111">Laajennukset ovat kuin pieniä sovelluksia, jotka esimerkiksi sisältävät lisätoimintoja, muuttavat toimintaa tai mahdollistavat uuden online-palvelun käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="5765f-111">Extensions are like small applications that add functionality, change behavior, provide access to new online services, and more.</span></span> <span data-ttu-id="5765f-112">Microsoft tarjoaa esimerkiksi laajennuksen, joka mahdollistaa integroinnin PayPal Payments Standard -ohjelman kanssa.</span><span class="sxs-lookup"><span data-stu-id="5765f-112">For example, Microsoft provides an extension that provides integration with PayPal Payments Standard.</span></span>|<span data-ttu-id="5765f-113">Kaikki yrityksen käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="5765f-113">All users in all companies.</span></span>|[<span data-ttu-id="5765f-114">Laajennusten käyttämisen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="5765f-114">Customizing Using Extensions</span></span>](ui-extensions.md)|
|<span data-ttu-id="5765f-115">Vaihda käyttöliittymäelementit, jotka ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="5765f-115">Change which UI elements are visible.</span></span>|<span data-ttu-id="5765f-116">**Käyttökokemus**-asetus määrittää, miten suuri osa toimintoja näytetään käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="5765f-116">The **Experience** setting determines how much of the functionality is displayed in the user interface.</span></span> <span data-ttu-id="5765f-117">Valitse Essential tai Premium.</span><span class="sxs-lookup"><span data-stu-id="5765f-117">Choose between Essential and Premium.</span></span>|<span data-ttu-id="5765f-118">Kaikki tietyn yrityksen käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="5765f-118">All users in a specific company.</span></span>|[<span data-ttu-id="5765f-119">Näytettävien ominaisuuksien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="5765f-119">Changing Which Features are Displayed</span></span>](ui-experiences.md)|
|<span data-ttu-id="5765f-120">Mukauta työtilaa</span><span class="sxs-lookup"><span data-stu-id="5765f-120">Personalize your workspace</span></span>|<span data-ttu-id="5765f-121">Muuta sivujen asettelua ja sisältöä.</span><span class="sxs-lookup"><span data-stu-id="5765f-121">Change the layout and content of your pages.</span></span>|<span data-ttu-id="5765f-122">Vain sinä.</span><span class="sxs-lookup"><span data-stu-id="5765f-122">Only you.</span></span>|[<span data-ttu-id="5765f-123">Työtilan mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="5765f-123">Personalizing Your Workspace</span></span>](ui-personalization-user.md)|

> [!NOTE]
> <span data-ttu-id="5765f-124">[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen käyttäjän dokumentaation kaikkien toimintojen kuvauksissa käsitellään **Premium**-käyttökokemusta. Tämä tarkoittaa sitä, että kuvaukset sisältävät käyttöliittymän kaikki elementit.</span><span class="sxs-lookup"><span data-stu-id="5765f-124">All feature descriptions in user documentation for [!INCLUDE[d365fin](includes/d365fin_md.md)] assumes the **Premium** experience, meaning the descriptions cover the full scope of UI elements.</span></span> <span data-ttu-id="5765f-125">Tämän vuoksi **Essential**-käyttökokemuksen käyttäjien ohjeaiheissa saatetaan käsitellä toimintoja ja käyttöliittymän elementtejä, jotka eivät ole käytettävissä käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="5765f-125">Therefore, users with the **Essential** experience may in some topics read about functionality and UI elements that are not visible in their user interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="5765f-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5765f-126">See Also</span></span>
<span data-ttu-id="5765f-127">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5765f-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

