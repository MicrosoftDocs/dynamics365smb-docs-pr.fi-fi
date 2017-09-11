---
title: "Kontaktien postitusryhmien määrittäminen| Microsoft Docs"
description: "Voit ilmaista postitusryhmien avulla ryhmät, joiden avulla määritetään samat tiedot saavat kontaktiryhmät esimerkiksi markkinointi- tai mainoskampanjaa varten."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bc1c89b87426b72ce4f9522cb7f0dc31c77acad1
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-mailing-groups-for-contacts"></a><span data-ttu-id="43828-103">Toimintaohje: Kontaktien postitusryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="43828-103">How to: Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="43828-104">Postitusryhmien avulla voi määrittää niiden kontaktien ryhmät, joiden haluat vastaanottavan samat tiedot.</span><span class="sxs-lookup"><span data-stu-id="43828-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="43828-105">Voit määrittää esimerkiksi kontaktien postitusryhmän, jolle haluat lähettää ilmoituksen toimiston siirtämisestä, tai toisen ryhmän, jolle haluat lähettää lomalahjoja.</span><span class="sxs-lookup"><span data-stu-id="43828-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="43828-106">Kontaktien postitusryhmien käyttäminen on kaksivaiheinen prosessi.</span><span class="sxs-lookup"><span data-stu-id="43828-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="43828-107">Ensin määritetään postitusryhmän koodi.</span><span class="sxs-lookup"><span data-stu-id="43828-107">First, you define the mailing group code.</span></span> <span data-ttu-id="43828-108">Tämä vaihe suoritetaan vain kerran jokaiselle postitusryhmälle.</span><span class="sxs-lookup"><span data-stu-id="43828-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="43828-109">Kun postitusryhmän koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.</span><span class="sxs-lookup"><span data-stu-id="43828-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="43828-110">Postitusryhmän koodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="43828-110">To define mailing group codes</span></span>
<span data-ttu-id="43828-111">Postitusryhmän koodi määrittää ryhmän tyypin tai luokan. Se voi olla SIIRTO toimiston siirrolle tai LAHJA lomalahjalle.</span><span class="sxs-lookup"><span data-stu-id="43828-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="43828-112">Toimialaryhmän koodeja voi olla useita.</span><span class="sxs-lookup"><span data-stu-id="43828-112">You can have several industry group codes.</span></span> <span data-ttu-id="43828-113">Voit määrittää toimialaryhmät **Postitusryhmät**-ikkunan avulla.</span><span class="sxs-lookup"><span data-stu-id="43828-113">To define the industry groups, you use the **Mailing Groups** window.</span></span>

1. <span data-ttu-id="43828-114">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Postitusryhmät** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="43828-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="43828-115">Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="43828-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="43828-116">Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.</span><span class="sxs-lookup"><span data-stu-id="43828-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="43828-117"><a name="AssignMailGroupContact"></a> Postitusryhmien määrittäminen kontaktiin</span><span class="sxs-lookup"><span data-stu-id="43828-117"><a name="AssignMailGroupContact"></a> To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="43828-118">Avaa kontakti.</span><span class="sxs-lookup"><span data-stu-id="43828-118">Open the contact.</span></span>
2. <span data-ttu-id="43828-119">Valitse **Postitusryhmät**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="43828-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="43828-120">Näyttöön tulee **Kontaktin postitusryhmät** -ikkuna.</span><span class="sxs-lookup"><span data-stu-id="43828-120">The **Contact Mailing Groups** window opens.</span></span>
3. <span data-ttu-id="43828-121">Valitse **Postitusryhmien koodi** -kentässä postitusryhmä, jonka haluat liittää.</span><span class="sxs-lookup"><span data-stu-id="43828-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="43828-122">Toista nämä vaiheet ja liitä niin monta postitusryhmää kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="43828-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="43828-123">Voit liittää samaan tapaan postitusryhmiä myös kontaktiluetteloista.</span><span class="sxs-lookup"><span data-stu-id="43828-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="43828-124">Kontaktiin liitettyjen postitusryhmien lukumäärä näytetään **Kontakti**-ikkunan **Segmentointi**-osan **Postitusryhmien lkm** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="43828-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="43828-125">Kun olet liittänyt postitusryhmät kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi.</span><span class="sxs-lookup"><span data-stu-id="43828-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="43828-126">Lisätietoja on kohdassa [Toimintaohje: Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="43828-126">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="43828-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="43828-127">See Also</span></span>
[<span data-ttu-id="43828-128">Kontaktiyrityksen luominen</span><span class="sxs-lookup"><span data-stu-id="43828-128">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="43828-129">Kontaktihenkilöiden luominen</span><span class="sxs-lookup"><span data-stu-id="43828-129">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="43828-130">Financialsin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="43828-130">Working with Financials</span></span>](ui-work-product.md)

