---
title: "Kontaktiyritysten verkkopalvelujen määrittäminen| Microsoft Docs"
description: "Voit määrittää internet- tai verkkolähteet ja määrittää ne kontaktiyritykseen. Tämä auttaa ilmaisemaan, miten haluat etsiä kontakteja koskevia tietoja."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b80edfbbad575cfcaa15b2c1b79a4feacb077371
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-web-sources-for-contact-companies"></a><span data-ttu-id="86779-103">Kontaktiyritysten verkkolähteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86779-103">Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="86779-104">Voit käyttää verkkolähteitä (esimerkiksi hakukoneita ja verkkosivustoja) kontaktiyrityksissä silloin, kun haluat ilmaista, mistä aiot hakea tietoa kontakteistasi Internetissä.</span><span class="sxs-lookup"><span data-stu-id="86779-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="86779-105">Kun liität verkkolähteitä, määritä, mitä hakukonetta ja hakusanaa sovellus käyttää hakiessaan pyydettyjä tietoja.</span><span class="sxs-lookup"><span data-stu-id="86779-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="86779-106">Kontaktien verkkolähteiden käyttäminen on kaksivaiheinen prosessi.</span><span class="sxs-lookup"><span data-stu-id="86779-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="86779-107">Ensin määritetään verkkolähteen koodi.</span><span class="sxs-lookup"><span data-stu-id="86779-107">First, you define the web source code.</span></span> <span data-ttu-id="86779-108">Tämä vaihe suoritetaan vain kerran jokaiselle verkkolähteelle.</span><span class="sxs-lookup"><span data-stu-id="86779-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="86779-109">Kun verkkolähteen koodi on määritetty, voit aloittaa koodin liittämisen kontaktihenkilöille.</span><span class="sxs-lookup"><span data-stu-id="86779-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="86779-110">Verkkolähteen koodin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86779-110">To define a web source code</span></span>
1. <span data-ttu-id="86779-111">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Verkkolähteet** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="86779-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="86779-112">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="86779-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="86779-113">Täytä **Koodi**-, **Kuvaus**- ja **URL**-kentät.</span><span class="sxs-lookup"><span data-stu-id="86779-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="86779-114">Kirjoita %1 **URL-osoite**-kenttään lisätäksesi hakusanan paikkamerkin URL-osoitekenttään.</span><span class="sxs-lookup"><span data-stu-id="86779-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="86779-115">Kun avaat verkkolähteen kontaktista, %1 korvataan hakusanalla (esimerkiksi yrityksen nimellä), jonka syötit **Kontaktin verkkolähteet** -ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="86779-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered in the **Contact Web Sources** window.</span></span>

<span data-ttu-id="86779-116">Toista nämä vaiheet ja luo niin monta verkkolähdettä kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="86779-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="86779-117">Verkkolähteiden määrittäminen kontaktiyritykselle</span><span class="sxs-lookup"><span data-stu-id="86779-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="86779-118">Kun liität verkkolähteitä, määritä, mitä hakukonetta ja hakusanaa sovellus käyttää hakiessaan pyydettyjä tietoja.</span><span class="sxs-lookup"><span data-stu-id="86779-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="86779-119">Avaa kontakti.</span><span class="sxs-lookup"><span data-stu-id="86779-119">Open the contact.</span></span>
2. <span data-ttu-id="86779-120">Valitse **Yritys**-toiminto ja valitse sitten **Verkkolähteet**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="86779-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="86779-121">Näyttöön tulee **Kontaktin verkkolähteet** -ikkuna.</span><span class="sxs-lookup"><span data-stu-id="86779-121">The **Contact Web Sources** window opens.</span></span>
3. <span data-ttu-id="86779-122">Valitse **Verkkolähteen koodi** -kentässä verkkolähde, jonka haluat liittää.</span><span class="sxs-lookup"><span data-stu-id="86779-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="86779-123">Syötä **Hakusana**-kenttään se sana, jolla haluat ohjelman hakevan tietoa.</span><span class="sxs-lookup"><span data-stu-id="86779-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="86779-124">Toista nämä vaiheet ja luo niin monta verkkolähdettä kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="86779-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="86779-125">Voit liittää samaan tapaan verkkolähteitä myös **Kontaktiluettelo**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="86779-125">You can also assign web sources from the **Contact List** window by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="86779-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="86779-126">See Also</span></span>
[<span data-ttu-id="86779-127">Kontaktiyrityksen luominen</span><span class="sxs-lookup"><span data-stu-id="86779-127">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="86779-128">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="86779-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

