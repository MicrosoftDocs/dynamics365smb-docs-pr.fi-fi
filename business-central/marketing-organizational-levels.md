---
title: Kontaktihenkilöiden organisaatiotasojen määrittäminen| Microsoft Docs
description: Voit määrittää organisaatiotason, ja kun se on määritetty kontaktille, voit ilmaista sen avulla, mikä on kontaktin asema yrityksessä (esimerkiksi ylin johto).
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 68f20af84652f684eaa0d69c98e0dc3cb722ee91
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242926"
---
# <a name="set-up-organizational-levels-for-contact-persons"></a><span data-ttu-id="849dd-103">Kontaktihenkilöiden organisaatiotasojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="849dd-103">Set Up Organizational Levels for Contact Persons</span></span>
<span data-ttu-id="849dd-104">Voit käyttää kontakteissa organisaatiotasoja (esimerkiksi ylin johto) kun haluat määrittää, missä asemassa he ovat yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="849dd-104">You can use organizational levels on your contacts to specify which position they have in the company, for example, top management.</span></span> <span data-ttu-id="849dd-105">Voit käyttää näitä tietoja kontaktien tietojen syöttämisessä.</span><span class="sxs-lookup"><span data-stu-id="849dd-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="849dd-106">Kontaktien organisaatiotasojen käyttäminen on kaksivaiheinen prosessi.</span><span class="sxs-lookup"><span data-stu-id="849dd-106">Using organizational levels on contacts is a two-step process.</span></span> <span data-ttu-id="849dd-107">Ensin määritetään organisaatiotason koodi.</span><span class="sxs-lookup"><span data-stu-id="849dd-107">First, you define the organizational level code.</span></span> <span data-ttu-id="849dd-108">Tämä vaihe suoritetaan vain kerran jokaiselle organisaatiotasolle.</span><span class="sxs-lookup"><span data-stu-id="849dd-108">You only have to perform this step one time for each organizational level.</span></span> <span data-ttu-id="849dd-109">Kun organisaation koodi on määritetty, voit aloittaa koodin liittämisen kontaktihenkilöille.</span><span class="sxs-lookup"><span data-stu-id="849dd-109">Once you have an organizational level code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-an-organizational-level-code"></a><span data-ttu-id="849dd-110">Organisaatiotason koodin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="849dd-110">To define an organizational level code</span></span>
<span data-ttu-id="849dd-111">Organisaatontason koodi määrittää organisaatiotason tyypin tai luokan. Se voi olla esimerkiksi TOIMITUSJOHTAJA tai TALOUSJOHTAJA.</span><span class="sxs-lookup"><span data-stu-id="849dd-111">The organizational level code defines the type or category of the organizational level, such a CEO  or CFO.</span></span> <span data-ttu-id="849dd-112">Organisaatiotason koodeja voi olla useita.</span><span class="sxs-lookup"><span data-stu-id="849dd-112">You can have several organizational level codes.</span></span> <span data-ttu-id="849dd-113">Voit määrittää organisaatiotason **Organisaatiotasot**-sivun avulla.</span><span class="sxs-lookup"><span data-stu-id="849dd-113">To define the organizational level, you use the **Organizational Levels** page.</span></span>

1. <span data-ttu-id="849dd-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Organisaation tasot** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="849dd-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Organizational Levels**, and then choose the related link.</span></span>
2. <span data-ttu-id="849dd-115">Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="849dd-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="849dd-116">Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.</span><span class="sxs-lookup"><span data-stu-id="849dd-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-organizational-levels-to-a-contact-person"></a><span data-ttu-id="849dd-117">Organisaatiotasojen määrittäminen kontaktihenkilölle</span><span class="sxs-lookup"><span data-stu-id="849dd-117">To assign organizational levels to a contact person</span></span>
<span data-ttu-id="849dd-118">Organisaatiotasoja voi liittää vain kontaktihenkilöihin, ei kontaktiyrityksiin.</span><span class="sxs-lookup"><span data-stu-id="849dd-118">You can assign organizational levels to contact persons only, not contact companies.</span></span> <span data-ttu-id="849dd-119">Jokaiseen kontaktiin voi liittää vain yhden organisatorisen tason.</span><span class="sxs-lookup"><span data-stu-id="849dd-119">You can only assign one organizational level to each contact.</span></span>

1. <span data-ttu-id="849dd-120">Avaa kontakti.</span><span class="sxs-lookup"><span data-stu-id="849dd-120">Open the contact.</span></span>
2. <span data-ttu-id="849dd-121">Valitse **Organisaatiotasot**-kentässä koodi, jonka haluat liittää.</span><span class="sxs-lookup"><span data-stu-id="849dd-121">In the **Organizational Levels** field, select the code you want to assign.</span></span>

<span data-ttu-id="849dd-122">Kun olet liittänyt kontakteihisi organisaatiotasoja, voit käyttää näitä tietoja luodessasi segmenttejä.</span><span class="sxs-lookup"><span data-stu-id="849dd-122">After you have assigned organizational levels to your contacts, you can use this information to create segments.</span></span>

<span data-ttu-id="849dd-123">Kun olet liittänyt vastuualueita kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi.</span><span class="sxs-lookup"><span data-stu-id="849dd-123">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="849dd-124">Lisätietoja on kohdassa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="849dd-124">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="849dd-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="849dd-125">See Also</span></span>
[<span data-ttu-id="849dd-126">Kontaktien luominen</span><span class="sxs-lookup"><span data-stu-id="849dd-126">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="849dd-127">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="849dd-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
