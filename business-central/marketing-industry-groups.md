---
title: "Toimialaryhmien määrittäminen kontaktiyrityksille| Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten toimialaryhmä määritetään ja miten sille sitten määritetään kontaktiryhmä, kuten vähittäistavarakauppa tai autoteollisuus."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 7e55ac991a946d32028d9527e56643d305ec4095
ms.contentlocale: fi-fi
ms.lasthandoff: 12/11/2018

---
# <a name="set-up-industry-groups-for-contact-companies"></a><span data-ttu-id="8fdfc-103">Kontaktiyritysten toimialaryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8fdfc-103">Set Up Industry Groups for Contact Companies</span></span>
<span data-ttu-id="8fdfc-104">Toimialaryhmien avulla osoitetaan, minkä tyyppiseen toimialaryhmään (esimerkiksi vähittäistavarakauppa ja autoteollisuus) kontaktit kuuluvat.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-104">You use industry groups to indicate the type of industry to which your contacts belong, for example, the retail industry or the automobile industry.</span></span>

<span data-ttu-id="8fdfc-105">Kontaktien toimialaryhmien käyttäminen on kaksivaiheinen prosessi.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-105">Using industry groups on contacts is a two-step process.</span></span> <span data-ttu-id="8fdfc-106">Ensin määritetään toimialaryhmän koodi.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-106">First, you define the industry group code.</span></span> <span data-ttu-id="8fdfc-107">Tämä vaihe suoritetaan vain kerran jokaiselle toimialaryhmälle.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-107">You only have to perform this step one time for each industry group.</span></span> <span data-ttu-id="8fdfc-108">Kun toimialaryhmän koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-108">Once you have an industry group code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="8fdfc-109">Jos aiot synkronisoida kontaktisi ohjelman muissa osissa olevien toimittajien, asiakkaiden tai pankkitilien kanssa, haluat ehkä määrittää niille liikesuhteen.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-an-industry-group-code"></a><span data-ttu-id="8fdfc-110">Toimialaryhmän koodin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8fdfc-110">To define an industry group code</span></span>
<span data-ttu-id="8fdfc-111">Toimialaryhmän koodi määrittää ryhmän tyypin tai luokan, joka voi olla esimerkiksi mainonnalle MAINOS tai televisiolle ja radiolle TIED.VÄL.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-111">The industry group code defines the type or category of the group, such as ADVERT for advertising, or PRESS, for TV and radio.</span></span> <span data-ttu-id="8fdfc-112">Toimialaryhmän koodeja voi olla useita.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-112">You can have several industry group codes.</span></span> <span data-ttu-id="8fdfc-113">Voit määrittää toimialaryhmät **Toimialaryhmät**-sivun avulla.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-113">To define the industry groups, you use the **Industry Groups** page.</span></span>

1. <span data-ttu-id="8fdfc-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimialaryhmät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Industry Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="8fdfc-115">Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="8fdfc-116">Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignIndustryGroupContact"></a> <span data-ttu-id="8fdfc-117">Toimialaryhmien määrittäminen kontaktille</span><span class="sxs-lookup"><span data-stu-id="8fdfc-117">To assign industry groups to a contact</span></span>
<span data-ttu-id="8fdfc-118">Toimialaryhmiä ei voi liittää kontaktihenkilöön, vaan ainoastaan yrityksiin.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-118">You cannot assign industry groups to a contact person - only companies.</span></span>

1. <span data-ttu-id="8fdfc-119">Avaa kontakti.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-119">Open the contact.</span></span>
2. <span data-ttu-id="8fdfc-120">Valitse **Yritys**-toiminto ja sitten **Toimialaryhmät**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-120">Choose the **Company** action, and then the **Industry Groups** action.</span></span> <span data-ttu-id="8fdfc-121">Näyttöön tulee **Kontaktin toimialaryhmät** -sivu.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-121">The **Contact Industry Groups** page opens.</span></span>
3. <span data-ttu-id="8fdfc-122">Valitse **Toimialaryhmien koodi** -kentässä toimialaryhmät, jotka haluat liittää.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-122">In the **Industry Groups Code** field, select the industry groups you want to assign.</span></span>

<span data-ttu-id="8fdfc-123">Toista nämä vaiheet ja luo niin monta toimialaryhmää kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-123">Repeat these steps to assign as many industry groups as you want.</span></span> <span data-ttu-id="8fdfc-124">Voit luoda samaan tapaan toimialaryhmiä kontaktiluettelosta.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-124">You can also assign industry groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="8fdfc-125">Kontaktille määritettyjen toimialaryhmien lukumäärä näkyy **Kontakti**-sivun **Segmentointi**-osan **Toimialaryhmien lkm** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-125">The number of industry groups that you have assigned to the contact is displayed in the **No. of Industry Groups** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="8fdfc-126">Kun olet liittänyt toimialaryhmiä kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi.</span><span class="sxs-lookup"><span data-stu-id="8fdfc-126">After you have assigned industry groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="8fdfc-127">Lisätietoja on ohjeaiheessa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="8fdfc-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8fdfc-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8fdfc-128">See Also</span></span>
[<span data-ttu-id="8fdfc-129">Kontaktiyrityksen luominen</span><span class="sxs-lookup"><span data-stu-id="8fdfc-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="8fdfc-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8fdfc-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

