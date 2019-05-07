---
title: Kontaktiyritysten verkkopalvelujen määrittäminen| Microsoft Docs
description: Voit määrittää internet- tai verkkolähteet ja määrittää ne kontaktiyritykseen. Tämä auttaa ilmaisemaan, miten haluat etsiä kontakteja koskevia tietoja.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: aa5998b989d8a3d37f3d7bfcdb348a2c09381168
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "934394"
---
# <a name="set-up-web-sources-for-contact-companies"></a><span data-ttu-id="8822c-103">Kontaktiyritysten verkkolähteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8822c-103">Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="8822c-104">Voit käyttää verkkolähteitä (esimerkiksi hakukoneita ja verkkosivustoja) kontaktiyrityksissä silloin, kun haluat ilmaista, mistä aiot hakea tietoa kontakteistasi Internetissä.</span><span class="sxs-lookup"><span data-stu-id="8822c-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="8822c-105">Kun liität verkkolähteitä, määritä, mitä hakukonetta ja hakusanaa sovellus käyttää hakiessaan pyydettyjä tietoja.</span><span class="sxs-lookup"><span data-stu-id="8822c-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="8822c-106">Kontaktien verkkolähteiden käyttäminen on kaksivaiheinen prosessi.</span><span class="sxs-lookup"><span data-stu-id="8822c-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="8822c-107">Ensin määritetään verkkolähteen koodi.</span><span class="sxs-lookup"><span data-stu-id="8822c-107">First, you define the web source code.</span></span> <span data-ttu-id="8822c-108">Tämä vaihe suoritetaan vain kerran jokaiselle verkkolähteelle.</span><span class="sxs-lookup"><span data-stu-id="8822c-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="8822c-109">Kun verkkolähteen koodi on määritetty, voit aloittaa koodin liittämisen kontaktihenkilöille.</span><span class="sxs-lookup"><span data-stu-id="8822c-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="8822c-110">Verkkolähteen koodin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8822c-110">To define a web source code</span></span>
1. <span data-ttu-id="8822c-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **WWW-lähteet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8822c-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="8822c-112">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="8822c-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="8822c-113">Täytä **Koodi**-, **Kuvaus**- ja **URL**-kentät.</span><span class="sxs-lookup"><span data-stu-id="8822c-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="8822c-114">Kirjoita %1 **URL-osoite**-kenttään lisätäksesi hakusanan paikkamerkin URL-osoitekenttään.</span><span class="sxs-lookup"><span data-stu-id="8822c-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="8822c-115">Kun avaat verkkolähteen kontaktista, %1 korvataan hakusanalla (esimerkiksi yrityksen nimellä), jonka annoit **Kontaktin verkkolähteet** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="8822c-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered on the **Contact Web Sources** page.</span></span>

<span data-ttu-id="8822c-116">Toista nämä vaiheet ja luo niin monta verkkolähdettä kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="8822c-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="8822c-117">Verkkolähteiden määrittäminen kontaktiyritykselle</span><span class="sxs-lookup"><span data-stu-id="8822c-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="8822c-118">Kun liität verkkolähteitä, määritä, mitä hakukonetta ja hakusanaa sovellus käyttää hakiessaan pyydettyjä tietoja.</span><span class="sxs-lookup"><span data-stu-id="8822c-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="8822c-119">Avaa kontakti.</span><span class="sxs-lookup"><span data-stu-id="8822c-119">Open the contact.</span></span>
2. <span data-ttu-id="8822c-120">Valitse **Yritys**-toiminto ja valitse sitten **Verkkolähteet**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="8822c-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="8822c-121">Näyttöön tulee **Kontaktin verkkolähteet** -sivu.</span><span class="sxs-lookup"><span data-stu-id="8822c-121">The **Contact Web Sources** page opens.</span></span>
3. <span data-ttu-id="8822c-122">Valitse **Verkkolähteen koodi** -kentässä verkkolähde, jonka haluat liittää.</span><span class="sxs-lookup"><span data-stu-id="8822c-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="8822c-123">Syötä **Hakusana**-kenttään se sana, jolla haluat ohjelman hakevan tietoa.</span><span class="sxs-lookup"><span data-stu-id="8822c-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="8822c-124">Toista nämä vaiheet ja luo niin monta verkkolähdettä kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="8822c-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="8822c-125">Voit liittää verkkolähteitä myös **Kontaktiluettelo**-sivulla noudattaen samaa menettelytapaa.</span><span class="sxs-lookup"><span data-stu-id="8822c-125">You can also assign web sources from the **Contact List** page by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="8822c-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8822c-126">See Also</span></span>
[<span data-ttu-id="8822c-127">Kontaktien luominen</span><span class="sxs-lookup"><span data-stu-id="8822c-127">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="8822c-128">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8822c-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
