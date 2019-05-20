---
title: Kontaktien postitusryhmien määrittäminen| Microsoft Docs
description: Voit ilmaista postitusryhmien avulla ryhmät, joiden avulla määritetään samat tiedot saavat kontaktiryhmät esimerkiksi markkinointi- tai mainoskampanjaa varten.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: fb9c540819279d042685ad69c790e36e71dcfbed
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238277"
---
# <a name="set-up-mailing-groups-for-contacts"></a><span data-ttu-id="760a2-103">Kontaktien postitusryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="760a2-103">Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="760a2-104">Postitusryhmien avulla voi määrittää niiden kontaktien ryhmät, joiden haluat vastaanottavan samat tiedot.</span><span class="sxs-lookup"><span data-stu-id="760a2-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="760a2-105">Voit määrittää esimerkiksi kontaktien postitusryhmän, jolle haluat lähettää ilmoituksen toimiston siirtämisestä, tai toisen ryhmän, jolle haluat lähettää lomalahjoja.</span><span class="sxs-lookup"><span data-stu-id="760a2-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="760a2-106">Kontaktien postitusryhmien käyttäminen on kaksivaiheinen prosessi.</span><span class="sxs-lookup"><span data-stu-id="760a2-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="760a2-107">Ensin määritetään postitusryhmän koodi.</span><span class="sxs-lookup"><span data-stu-id="760a2-107">First, you define the mailing group code.</span></span> <span data-ttu-id="760a2-108">Tämä vaihe suoritetaan vain kerran jokaiselle postitusryhmälle.</span><span class="sxs-lookup"><span data-stu-id="760a2-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="760a2-109">Kun postitusryhmän koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.</span><span class="sxs-lookup"><span data-stu-id="760a2-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="760a2-110">Postitusryhmän koodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="760a2-110">To define mailing group codes</span></span>
<span data-ttu-id="760a2-111">Postitusryhmän koodi määrittää ryhmän tyypin tai luokan. Se voi olla SIIRTO toimiston siirrolle tai LAHJA lomalahjalle.</span><span class="sxs-lookup"><span data-stu-id="760a2-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="760a2-112">Toimialaryhmän koodeja voi olla useita.</span><span class="sxs-lookup"><span data-stu-id="760a2-112">You can have several industry group codes.</span></span> <span data-ttu-id="760a2-113">Voit määrittää toimialaryhmät **Postitusryhmät**-sivun avulla.</span><span class="sxs-lookup"><span data-stu-id="760a2-113">To define the industry groups, you use the **Mailing Groups** page.</span></span>

1. <span data-ttu-id="760a2-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Postitusryhmät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="760a2-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="760a2-115">Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="760a2-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="760a2-116">Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.</span><span class="sxs-lookup"><span data-stu-id="760a2-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignMailGroupContact"></a> <span data-ttu-id="760a2-117">Postitusryhmien määrittäminen kontaktiin</span><span class="sxs-lookup"><span data-stu-id="760a2-117">To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="760a2-118">Avaa kontakti.</span><span class="sxs-lookup"><span data-stu-id="760a2-118">Open the contact.</span></span>
2. <span data-ttu-id="760a2-119">Valitse **Postitusryhmät**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="760a2-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="760a2-120">Näyttöön tulee **Kontaktin postitusryhmät** -sivu.</span><span class="sxs-lookup"><span data-stu-id="760a2-120">The **Contact Mailing Groups** page opens.</span></span>
3. <span data-ttu-id="760a2-121">Valitse **Postitusryhmien koodi** -kentässä postitusryhmä, jonka haluat liittää.</span><span class="sxs-lookup"><span data-stu-id="760a2-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="760a2-122">Toista nämä vaiheet ja liitä niin monta postitusryhmää kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="760a2-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="760a2-123">Voit liittää samaan tapaan postitusryhmiä myös kontaktiluetteloista.</span><span class="sxs-lookup"><span data-stu-id="760a2-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="760a2-124">Kontaktiin liitettyjen postitusryhmien lukumäärä näytetään **Kontakti**-sivun **Segmentointi**-osan **Postitusryhmien lkm** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="760a2-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="760a2-125">Kun olet liittänyt postitusryhmät kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi.</span><span class="sxs-lookup"><span data-stu-id="760a2-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="760a2-126">Lisätietoja on kohdassa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="760a2-126">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="760a2-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="760a2-127">See Also</span></span>
[<span data-ttu-id="760a2-128">Kontaktien luominen</span><span class="sxs-lookup"><span data-stu-id="760a2-128">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="760a2-129">Business Centralin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="760a2-129">Working with Business Central</span></span>](ui-work-product.md)
