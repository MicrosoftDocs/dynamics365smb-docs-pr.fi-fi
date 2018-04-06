---
title: Vuorovaikutusten luominen kontakteille ja segmenteille| Microsoft Docs
description: "Tässä ohjeaiheessa kerrotaan, miten vuorovaikutukset luodaan Business Central -sovelluksessa asiakkaiden ja segmenttien kanssa käydylle viestinnälle. Kyse voi olla esimerkiksi suoramainonnasta."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/15/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: aa6be34f1b43dfe0b1f82cbb6a2cefd06edb0f83
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="create-interactions-on-contacts-and-segments"></a><span data-ttu-id="4ddf7-103">Vuorovaikutusten luominen kontakteille ja segmenteille</span><span class="sxs-lookup"><span data-stu-id="4ddf7-103">Create Interactions on Contacts and Segments</span></span>
<span data-ttu-id="4ddf7-104">Voit luoda vuorovaikutuksia, kun haluat tallentaa kaikki vuorovaikutukset ja kaiken yhteydenpidon (esimerkiksi postin), joita sinulla on kontaktiesi ja segmenttiesi kanssa.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-104">You can create interactions to record all the interactions and communications you have with your contacts and segments, for example, direct mail.</span></span>

<span data-ttu-id="4ddf7-105">Ennen vuorovaikutusten luomista sinun täytyy määrittää vuorovaikutusmallit.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-105">Before you create interactions, you must set up interaction templates.</span></span> <span data-ttu-id="4ddf7-106">Lisätietoja on ohjeaiheessa [Vuorovaikutusmallien määrittäminen](marketing-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="4ddf7-106">For more information, see  [Set Up Interaction Templates](marketing-interactions.md).</span></span>

## <a name="to-create-an-interaction"></a><span data-ttu-id="4ddf7-107">Integroinnin luominen</span><span class="sxs-lookup"><span data-stu-id="4ddf7-107">To create an interaction</span></span>
1. <span data-ttu-id="4ddf7-108">Avaa kontakti-, myyjä- tai vuorovaikutuslokitapahtuma.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-108">Open the contact, salesperson, or interaction log entry.</span></span>
2. <span data-ttu-id="4ddf7-109">Valitse **Luo vuorovaikutus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-109">Choose the **Create Interaction** action.</span></span>
3. <span data-ttu-id="4ddf7-110">Täytä kentät ja valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-110">Fill in the fields, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="4ddf7-111">Jos haluat suorittaa toisen tehtävän ennen vuorovaikutuksen suorittamista, valitse **Peruuta** ja valitse sitten yhteydenpidon suorittaminen myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-111">If you need to perform another task before finishing the interaction, you can choose **Cancel** and then finish the interaction at a later time.</span></span> <span data-ttu-id="4ddf7-112">Tällöin vuorovaikutusta lykätään.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-112">This postpones the interaction.</span></span>

## <a name="to-finish-and-delete-postponed-interactions"></a><span data-ttu-id="4ddf7-113">Lykättyjen vuorovaikutusten lopettaminen ja poistaminen</span><span class="sxs-lookup"><span data-stu-id="4ddf7-113">To finish and delete postponed interactions</span></span>
1. <span data-ttu-id="4ddf7-114">Avaa kontakti-, myyjä- tai vuorovaikutuslokitapahtuma.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-114">Open the contact, salesperson, or interaction log entry.</span></span>
2. <span data-ttu-id="4ddf7-115">Valitse **Lykätyt vuorovaikutukset**.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-115">Choose **Postponed Interactions**.</span></span>
3. <span data-ttu-id="4ddf7-116">Valitse lopetettava vuorovaikutus ja valitse sitten **Jatka**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-116">Select the interaction you want to finish, and then choose the **Resume** action.</span></span>

## <a name="to-create-an-interaction-on-a-segment"></a><span data-ttu-id="4ddf7-117">Vuorovaikutusten luominen segmentille</span><span class="sxs-lookup"><span data-stu-id="4ddf7-117">To create an interaction on a segment</span></span>
1. <span data-ttu-id="4ddf7-118">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Segmentit** ja valita sitten aiheeseen liittyvän linkin.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Segments**, and then choose the related link.</span></span>
2. <span data-ttu-id="4ddf7-119">Määritä, minkä vuorovaikutuksen haluat liittää segmenttiin, täyttämällä **Segmentti**-ikkunassa **Vuorovaikutus**-osan kentät.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-119">In the **Segment window**, in the **Interaction** section, fill in the fields to specify which interaction you want to assign to the segment.</span></span>

    <span data-ttu-id="4ddf7-120">Kun olet liittänyt vuorovaikutuksen segmenttiin, voit tehdä jokaisen segmentin kontaktin vuorovaikutuksesta yksilöllisen, esimerkiksi valitsemalla toisen vuorovaikutusmallin **Segmentti**-ikkunan riveillä.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-120">After you have assigned an interaction to the segment, you can personalize the interaction for each particular contact within the segment, for example, by selecting another interaction template on the lines in the **Segment** window.</span></span>  
3. <span data-ttu-id="4ddf7-121">Voit kirjata segmentin ja vuorovaikutukset lokiin valitsemalla **Loki**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-121">To log the segment and interactions, choose the **Log** action.</span></span> <span data-ttu-id="4ddf7-122">**Lokin segmentti**-luetteloikkuna aukeaa.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-122">The **Log Segment** window opens.</span></span>
4. <span data-ttu-id="4ddf7-123">Jos haluat luoda uuden segmentin, joka sisältää samat kontaktit, valitse **Luo seurantasegmentti** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-123">If you want to create a new segment containing the same contacts, select the **Create Follow-up Segment** check box.</span></span> <span data-ttu-id="4ddf7-124">Jotta ohjelma luo seurantasegmentin, segmenttien numerosarja on määritettävä **Kontaktienhallinnan asetukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-124">To create a follow-up segment, you must have specified number series for segments in the **Marketing Setup** window.</span></span>

<span data-ttu-id="4ddf7-125">Vuorovaikutus tallennetaan kullekin kontaktille **Vuorovaikutuslokitapahtuma**-taulukon segmentissä. Tämän jälkeen segmentti kirjataan lokiin.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-125">An interaction is recorded for each contact within the segment in the **Interaction Log Entry** table, and the segment is logged.</span></span> <span data-ttu-id="4ddf7-126">Lokiin kirjatut segmentit löytyvät **Lokiin kirjattu segmentti** -ikkunasta.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-126">Logged segments can be found in the **Logged Segment** window.</span></span>

<span data-ttu-id="4ddf7-127">Jos olet valinnut **Luo seurantasegmentti** -valintaruudun, ohjelma luo automaattisesti uuden segmentin, jossa on samat kontaktit kuin juuri lokiin kirjaamassasi segmentissä.</span><span class="sxs-lookup"><span data-stu-id="4ddf7-127">If you have selected the **Create Follow-up Segment** check box, a new segment is created that contains the same contacts as the segment you have just logged.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ddf7-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4ddf7-128">See Also</span></span>
[<span data-ttu-id="4ddf7-129">Vuorovaikutusten tallentaminen</span><span class="sxs-lookup"><span data-stu-id="4ddf7-129">Recording Interactions</span></span>](marketing-interactions.md)  
[<span data-ttu-id="4ddf7-130">Kontaktien hallinta</span><span class="sxs-lookup"><span data-stu-id="4ddf7-130">Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="4ddf7-131">Myyntimahdollisuuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="4ddf7-131">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="4ddf7-132">Kontaktienhallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4ddf7-132">Setting Up Relationship Management</span></span>](marketing-setup-marketing.md)  
[<span data-ttu-id="4ddf7-133">Business Central -sovelluksen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="4ddf7-133">Working with Business Central</span></span>](ui-work-product.md)

