---
title: Vuorovaikutusten luominen kontakteille ja segmenteille| Microsoft Docs
description: "Tässä ohjeaiheessa kerrotaan, miten vuorovaikutukset luodaan Finance and Operations, Business editionissa asiakkaiden ja segmenttien kanssa käydylle viestinnälle. Kyse voi olla esimerkiksi suoramainonnasta."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/15/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 93d5bc9fd8189d5a8341faa252de9eac257901d2
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="create-interactions-on-contacts-and-segments"></a><span data-ttu-id="73db8-103">Vuorovaikutusten luominen kontakteille ja segmenteille</span><span class="sxs-lookup"><span data-stu-id="73db8-103">Create Interactions on Contacts and Segments</span></span>
<span data-ttu-id="73db8-104">Voit luoda vuorovaikutuksia, kun haluat tallentaa kaikki vuorovaikutukset ja kaiken yhteydenpidon (esimerkiksi postin), joita sinulla on kontaktiesi ja segmenttiesi kanssa.</span><span class="sxs-lookup"><span data-stu-id="73db8-104">You can create interactions to record all the interactions and communications you have with your contacts and segments, for example, direct mail.</span></span>

<span data-ttu-id="73db8-105">Ennen vuorovaikutusten luomista sinun täytyy määrittää vuorovaikutusmallit.</span><span class="sxs-lookup"><span data-stu-id="73db8-105">Before you create interactions, you must set up interaction templates.</span></span> <span data-ttu-id="73db8-106">Lisätietoja on ohjeaiheessa [Vuorovaikutusmallien määrittäminen](marketing-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="73db8-106">For more information, see  [Set Up Interaction Templates](marketing-interactions.md).</span></span>

## <a name="to-create-an-interaction"></a><span data-ttu-id="73db8-107">Integroinnin luominen</span><span class="sxs-lookup"><span data-stu-id="73db8-107">To create an interaction</span></span>
1. <span data-ttu-id="73db8-108">Avaa kontakti-, myyjä- tai vuorovaikutuslokitapahtuma.</span><span class="sxs-lookup"><span data-stu-id="73db8-108">Open the contact, salesperson, or interaction log entry.</span></span>
2. <span data-ttu-id="73db8-109">Valitse **Luo vuorovaikutus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="73db8-109">Choose the **Create Interaction** action.</span></span>
3. <span data-ttu-id="73db8-110">Täytä kentät ja valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="73db8-110">Fill in the fields, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="73db8-111">Jos haluat suorittaa toisen tehtävän ennen vuorovaikutuksen suorittamista, valitse **Peruuta** ja valitse sitten yhteydenpidon suorittaminen myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="73db8-111">If you need to perform another task before finishing the interaction, you can choose **Cancel** and then finish the interaction at a later time.</span></span> <span data-ttu-id="73db8-112">Tällöin vuorovaikutusta lykätään.</span><span class="sxs-lookup"><span data-stu-id="73db8-112">This postpones the interaction.</span></span>

## <a name="to-finish-and-delete-postponed-interactions"></a><span data-ttu-id="73db8-113">Lykättyjen vuorovaikutusten lopettaminen ja poistaminen</span><span class="sxs-lookup"><span data-stu-id="73db8-113">To finish and delete postponed interactions</span></span>
1. <span data-ttu-id="73db8-114">Avaa kontakti-, myyjä- tai vuorovaikutuslokitapahtuma.</span><span class="sxs-lookup"><span data-stu-id="73db8-114">Open the contact, salesperson, or interaction log entry.</span></span>
2. <span data-ttu-id="73db8-115">Valitse **Lykätyt vuorovaikutukset**.</span><span class="sxs-lookup"><span data-stu-id="73db8-115">Choose **Postponed Interactions**.</span></span>
3. <span data-ttu-id="73db8-116">Valitse lopetettava vuorovaikutus ja valitse sitten **Jatka**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="73db8-116">Select the interaction you want to finish, and then choose the **Resume** action.</span></span>

## <a name="to-create-an-interaction-on-a-segment"></a><span data-ttu-id="73db8-117">Vuorovaikutusten luominen segmentille</span><span class="sxs-lookup"><span data-stu-id="73db8-117">To create an interaction on a segment</span></span>
1. <span data-ttu-id="73db8-118">Valitse aloitussivulla **Aktiiviset segmentit** tai valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Segmentit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="73db8-118">On the Home page, choose **Active Segments**, or choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Segments**, and then choose the related link.</span></span>
2. <span data-ttu-id="73db8-119">Määritä, minkä vuorovaikutuksen haluat liittää segmenttiin, täyttämällä **Segmentti**-ikkunassa **Vuorovaikutus**-osan kentät.</span><span class="sxs-lookup"><span data-stu-id="73db8-119">In the **Segment window**, in the **Interaction** section, fill in the fields to specify which interaction you want to assign to the segment.</span></span>

    <span data-ttu-id="73db8-120">Kun olet liittänyt vuorovaikutuksen segmenttiin, voit tehdä jokaisen segmentin kontaktin vuorovaikutuksesta yksilöllisen, esimerkiksi valitsemalla toisen vuorovaikutusmallin **Segmentti**-ikkunan riveillä.</span><span class="sxs-lookup"><span data-stu-id="73db8-120">After you have assigned an interaction to the segment, you can personalize the interaction for each particular contact within the segment, for example, by selecting another interaction template on the lines in the **Segment** window.</span></span>  
3. <span data-ttu-id="73db8-121">Voit kirjata segmentin ja vuorovaikutukset lokiin valitsemalla **Loki**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="73db8-121">To log the segment and interactions, choose the **Log** action.</span></span> <span data-ttu-id="73db8-122">**Lokin segmentti**-luetteloikkuna aukeaa.</span><span class="sxs-lookup"><span data-stu-id="73db8-122">The **Log Segment** window opens.</span></span>
4. <span data-ttu-id="73db8-123">Jos haluat luoda uuden segmentin, joka sisältää samat kontaktit, valitse **Luo seurantasegmentti** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="73db8-123">If you want to create a new segment containing the same contacts, select the **Create Follow-up Segment** check box.</span></span> <span data-ttu-id="73db8-124">Jotta ohjelma luo seurantasegmentin, segmenttien numerosarja on määritettävä **Kontaktienhallinnan asetukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="73db8-124">To create a follow-up segment, you must have specified number series for segments in the **Marketing Setup** window.</span></span>

<span data-ttu-id="73db8-125">Vuorovaikutus tallennetaan kullekin kontaktille **Vuorovaikutuslokitapahtuma**-taulukon segmentissä. Tämän jälkeen segmentti kirjataan lokiin.</span><span class="sxs-lookup"><span data-stu-id="73db8-125">An interaction is recorded for each contact within the segment in the **Interaction Log Entry** table, and the segment is logged.</span></span> <span data-ttu-id="73db8-126">Lokiin kirjatut segmentit löytyvät **Lokiin kirjattu segmentti** -ikkunasta.</span><span class="sxs-lookup"><span data-stu-id="73db8-126">Logged segments can be found in the **Logged Segment** window.</span></span>

<span data-ttu-id="73db8-127">Jos olet valinnut **Luo seurantasegmentti** -valintaruudun, ohjelma luo automaattisesti uuden segmentin, jossa on samat kontaktit kuin juuri lokiin kirjaamassasi segmentissä.</span><span class="sxs-lookup"><span data-stu-id="73db8-127">If you have selected the **Create Follow-up Segment** check box, a new segment is created that contains the same contacts as the segment you have just logged.</span></span>

## <a name="see-also"></a><span data-ttu-id="73db8-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="73db8-128">See Also</span></span>
[<span data-ttu-id="73db8-129">Vuorovaikutusten tallentaminen</span><span class="sxs-lookup"><span data-stu-id="73db8-129">Recording Interactions</span></span>](marketing-interactions.md)  
[<span data-ttu-id="73db8-130">Kontaktien hallinta</span><span class="sxs-lookup"><span data-stu-id="73db8-130">Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="73db8-131">Myyntimahdollisuuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="73db8-131">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="73db8-132">Kontaktienhallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="73db8-132">Setting Up Relationship Management</span></span>](marketing-setup-marketing.md)  
[<span data-ttu-id="73db8-133">Finance and Operations, Business editionin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="73db8-133">Working with Finance and Operations, Business edition</span></span>](ui-work-product.md)

