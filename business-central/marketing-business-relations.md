---
title: Kontaktien liikesuhteen koodien määrittäminen| Microsoft Docs
description: Voit käyttää Business Central -sovelluksen liikesuhteita markkinoinnissa. Niiden avulla voit ilmaista, minkälainen liikesuhde sinulla on prospektien ja asiakkaiden kanssa. Kyse voi olla esimerkiksi pankista tai palvelun toimittajasta.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: ffeb19820b29453750ca9c03258d455dddff287c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239335"
---
# <a name="setting-up-business-relations-on-contacts"></a><span data-ttu-id="17516-103">Liikesuhteiden määrittäminen kontaktissa</span><span class="sxs-lookup"><span data-stu-id="17516-103">Setting Up Business Relations on Contacts</span></span>
<span data-ttu-id="17516-104">Voit käyttää liikesuhteita, kun haluat osoittaa eri kontaktien, kuten prospektin, pankin, konsultin tai palvelun toimittajan, kanssa olevan liikesuhteen.</span><span class="sxs-lookup"><span data-stu-id="17516-104">You can use business relations to indicate the business relationship you have with your contacts, for example, a prospect, bank, consultant, service supplier, and so on.</span></span>

<span data-ttu-id="17516-105">Kontaktien liikesuhteiden käyttäminen on kaksivaiheinen prosessi.</span><span class="sxs-lookup"><span data-stu-id="17516-105">Using business relations on contacts is a two-step process.</span></span> <span data-ttu-id="17516-106">Ensin määritetään liikesuhteen koodi.</span><span class="sxs-lookup"><span data-stu-id="17516-106">First, you define the business relation code.</span></span> <span data-ttu-id="17516-107">Tämä vaihe suoritetaan vain kerran jokaiselle liikesuhteelle.</span><span class="sxs-lookup"><span data-stu-id="17516-107">You only have to perform this step one time for each business relation.</span></span> <span data-ttu-id="17516-108">Kun liikesuhteen koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.</span><span class="sxs-lookup"><span data-stu-id="17516-108">Once you have a business relation code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="17516-109">Jos aiot synkronisoida kontaktisi ohjelman muissa osissa olevien toimittajien, asiakkaiden tai pankkitilien kanssa, haluat ehkä määrittää niille liikesuhteen.</span><span class="sxs-lookup"><span data-stu-id="17516-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-a-business-relation-code"></a><span data-ttu-id="17516-110">Liikesuhteen koodin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="17516-110">To define a business relation code</span></span>
<span data-ttu-id="17516-111">Liikesuhteen koodi määrittää liikesuhteen luokan tai tyypin. Se voi olla esimerkiksi PANKKI tai LAKI.</span><span class="sxs-lookup"><span data-stu-id="17516-111">The business relation code defines a category or type of the business relationship, such as BANK or Law.</span></span> <span data-ttu-id="17516-112">Liikesuhteen koodeja voi olla useita.</span><span class="sxs-lookup"><span data-stu-id="17516-112">You can have several business relation codes.</span></span> <span data-ttu-id="17516-113">Määritä liikesuhde **Liikesuhteet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="17516-113">To define the business relation, you use the **Business Relations** page.</span></span>

1. <span data-ttu-id="17516-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liikesuhteet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="17516-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Business Relations**, and then choose the related link.</span></span>
2. <span data-ttu-id="17516-115">Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="17516-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="17516-116">Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.</span><span class="sxs-lookup"><span data-stu-id="17516-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignBusRelContact"></a> <span data-ttu-id="17516-117">Liikesuhteiden määrittäminen kontaktille</span><span class="sxs-lookup"><span data-stu-id="17516-117">To assign business relations to a contact</span></span>
<span data-ttu-id="17516-118">Liikesuhteita ei voi liittää kontaktihenkilöön, vaan ainoastaan yrityksiin.</span><span class="sxs-lookup"><span data-stu-id="17516-118">You cannot assign business relations to a contact person - only companies.</span></span>

1. <span data-ttu-id="17516-119">Avaa kontakti.</span><span class="sxs-lookup"><span data-stu-id="17516-119">Open the contact.</span></span>
2. <span data-ttu-id="17516-120">Valitse **Yritys**-toiminto ja sitten **Liikesuhteet**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="17516-120">Choose the **Company** action, and then the **Business Relations** action.</span></span>

    <span data-ttu-id="17516-121">**Kontaktin liikesuhteet** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="17516-121">The **Contact Business Relations** page opens.</span></span>
3. <span data-ttu-id="17516-122">Valitse **Liikesuhteen koodi** -kentässä liikesuhde, jonka haluat määrittää.</span><span class="sxs-lookup"><span data-stu-id="17516-122">In the **Business Relation Code** field, select the business relation you want to assign.</span></span>

<span data-ttu-id="17516-123">Toista nämä vaiheet ja luo niin monta liikesuhdetta kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="17516-123">Repeat these steps to assign as many business relations as you want.</span></span> <span data-ttu-id="17516-124">Voit myös liittää liikesuhteita kontaktiluettelosta saman menettelytavan avulla.</span><span class="sxs-lookup"><span data-stu-id="17516-124">You can also assign business relations from the contact list by following the same procedure.</span></span>

<span data-ttu-id="17516-125">Kontaktille liitettyjen liikesuhteiden lukumäärä näkyy **Kontakti**-sivun **Segmentointi**-osan **Liikesuhteiden lkm** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="17516-125">The number of business relations you have assigned to the contact is displayed in the **No. of Business Relations** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="17516-126">Kun olet liittänyt liikesuhteita kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi.</span><span class="sxs-lookup"><span data-stu-id="17516-126">After you have assigned business relations to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="17516-127">Lisätietoja on kohdassa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="17516-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="17516-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="17516-128">See Also</span></span>
<span data-ttu-id="17516-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="17516-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
