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
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7402899cb7fe369503eee1b451dc652180e96264
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-mailing-groups-for-contacts"></a><span data-ttu-id="6aeaa-103">Kontaktien postitusryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6aeaa-103">Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="6aeaa-104">Postitusryhmien avulla voi määrittää niiden kontaktien ryhmät, joiden haluat vastaanottavan samat tiedot.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="6aeaa-105">Voit määrittää esimerkiksi kontaktien postitusryhmän, jolle haluat lähettää ilmoituksen toimiston siirtämisestä, tai toisen ryhmän, jolle haluat lähettää lomalahjoja.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="6aeaa-106">Kontaktien postitusryhmien käyttäminen on kaksivaiheinen prosessi.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="6aeaa-107">Ensin määritetään postitusryhmän koodi.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-107">First, you define the mailing group code.</span></span> <span data-ttu-id="6aeaa-108">Tämä vaihe suoritetaan vain kerran jokaiselle postitusryhmälle.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="6aeaa-109">Kun postitusryhmän koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="6aeaa-110">Postitusryhmän koodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6aeaa-110">To define mailing group codes</span></span>
<span data-ttu-id="6aeaa-111">Postitusryhmän koodi määrittää ryhmän tyypin tai luokan. Se voi olla SIIRTO toimiston siirrolle tai LAHJA lomalahjalle.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="6aeaa-112">Toimialaryhmän koodeja voi olla useita.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-112">You can have several industry group codes.</span></span> <span data-ttu-id="6aeaa-113">Voit määrittää toimialaryhmät **Postitusryhmät**-ikkunan avulla.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-113">To define the industry groups, you use the **Mailing Groups** window.</span></span>

1. <span data-ttu-id="6aeaa-114">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Postitusryhmät** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="6aeaa-115">Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="6aeaa-116">Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignMailGroupContact"></a> <span data-ttu-id="6aeaa-117">Postitusryhmien määrittäminen kontaktiin</span><span class="sxs-lookup"><span data-stu-id="6aeaa-117">To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="6aeaa-118">Avaa kontakti.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-118">Open the contact.</span></span>
2. <span data-ttu-id="6aeaa-119">Valitse **Postitusryhmät**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="6aeaa-120">Näyttöön tulee **Kontaktin postitusryhmät** -ikkuna.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-120">The **Contact Mailing Groups** window opens.</span></span>
3. <span data-ttu-id="6aeaa-121">Valitse **Postitusryhmien koodi** -kentässä postitusryhmä, jonka haluat liittää.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="6aeaa-122">Toista nämä vaiheet ja liitä niin monta postitusryhmää kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="6aeaa-123">Voit liittää samaan tapaan postitusryhmiä myös kontaktiluetteloista.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="6aeaa-124">Kontaktiin liitettyjen postitusryhmien lukumäärä näytetään **Kontakti**-ikkunan **Segmentointi**-osan **Postitusryhmien lkm** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="6aeaa-125">Kun olet liittänyt postitusryhmät kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi.</span><span class="sxs-lookup"><span data-stu-id="6aeaa-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="6aeaa-126">Lisätietoja on ohjeaiheessa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="6aeaa-126">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6aeaa-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6aeaa-127">See Also</span></span>
[<span data-ttu-id="6aeaa-128">Kontaktiyrityksen luominen</span><span class="sxs-lookup"><span data-stu-id="6aeaa-128">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="6aeaa-129">Kontaktihenkilöiden luominen</span><span class="sxs-lookup"><span data-stu-id="6aeaa-129">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="6aeaa-130">Financialsin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="6aeaa-130">Working with Financials</span></span>](ui-work-product.md)

