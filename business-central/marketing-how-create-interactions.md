---
title: Vuorovaikutusten luominen kontakteille ja segmenteille| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten vuorovaikutukset luodaan Business Central -sovelluksessa asiakkaiden ja segmenttien kanssa käydylle viestinnälle. Kyse voi olla esimerkiksi suoramainonnasta.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 5536671877c2fa766f953fe6bc9a5af5d2861b3e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387947"
---
# <a name="create-interactions-on-contacts-and-segments"></a><span data-ttu-id="a32f5-103">Vuorovaikutusten luominen kontakteille ja segmenteille</span><span class="sxs-lookup"><span data-stu-id="a32f5-103">Create Interactions on Contacts and Segments</span></span>
<span data-ttu-id="a32f5-104">Voit luoda vuorovaikutuksia, kun haluat tallentaa kaikki vuorovaikutukset ja kaiken yhteydenpidon (esimerkiksi postin), joita sinulla on kontaktiesi ja segmenttiesi kanssa.</span><span class="sxs-lookup"><span data-stu-id="a32f5-104">You can create interactions to record all the interactions and communications you have with your contacts and segments, for example, direct mail.</span></span>

<span data-ttu-id="a32f5-105">Ennen vuorovaikutusten luomista sinun täytyy määrittää vuorovaikutusmallit.</span><span class="sxs-lookup"><span data-stu-id="a32f5-105">Before you create interactions, you must set up interaction templates.</span></span> <span data-ttu-id="a32f5-106">Lisätietoja on ohjeaiheessa [Vuorovaikutusmallien määrittäminen](marketing-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="a32f5-106">For more information, see  [Set Up Interaction Templates](marketing-interactions.md).</span></span>

## <a name="to-create-an-interaction"></a><span data-ttu-id="a32f5-107">Integroinnin luominen</span><span class="sxs-lookup"><span data-stu-id="a32f5-107">To create an interaction</span></span>
1. <span data-ttu-id="a32f5-108">Avaa kontakti-, myyjä- tai vuorovaikutuslokitapahtuma.</span><span class="sxs-lookup"><span data-stu-id="a32f5-108">Open the contact, salesperson, or interaction log entry.</span></span>
2. <span data-ttu-id="a32f5-109">Valitse **Luo vuorovaikutus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="a32f5-109">Choose the **Create Interaction** action.</span></span>
3. <span data-ttu-id="a32f5-110">Täytä kentät ja valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="a32f5-110">Fill in the fields, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="a32f5-111">Jos haluat suorittaa toisen tehtävän ennen vuorovaikutuksen suorittamista, valitse **Peruuta** ja valitse sitten yhteydenpidon suorittaminen myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="a32f5-111">If you need to perform another task before finishing the interaction, you can choose **Cancel** and then finish the interaction at a later time.</span></span> <span data-ttu-id="a32f5-112">Tällöin vuorovaikutusta lykätään.</span><span class="sxs-lookup"><span data-stu-id="a32f5-112">This postpones the interaction.</span></span>

## <a name="to-finish-and-delete-postponed-interactions"></a><span data-ttu-id="a32f5-113">Lykättyjen vuorovaikutusten lopettaminen ja poistaminen</span><span class="sxs-lookup"><span data-stu-id="a32f5-113">To finish and delete postponed interactions</span></span>
1. <span data-ttu-id="a32f5-114">Avaa kontakti-, myyjä- tai vuorovaikutuslokitapahtuma.</span><span class="sxs-lookup"><span data-stu-id="a32f5-114">Open the contact, salesperson, or interaction log entry.</span></span>
2. <span data-ttu-id="a32f5-115">Valitse **Lykätyt vuorovaikutukset**.</span><span class="sxs-lookup"><span data-stu-id="a32f5-115">Choose **Postponed Interactions**.</span></span>
3. <span data-ttu-id="a32f5-116">Valitse lopetettava vuorovaikutus ja valitse sitten **Jatka**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="a32f5-116">Select the interaction you want to finish, and then choose the **Resume** action.</span></span>

## <a name="to-create-an-interaction-on-a-segment"></a><span data-ttu-id="a32f5-117">Vuorovaikutusten luominen segmentille</span><span class="sxs-lookup"><span data-stu-id="a32f5-117">To create an interaction on a segment</span></span>
1. <span data-ttu-id="a32f5-118">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Segmentit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="a32f5-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Segments**, and then choose the related link.</span></span>
2. <span data-ttu-id="a32f5-119">Määritä, minkä vuorovaikutuksen haluat liittää segmenttiin, täyttämällä **Segmentti**-sivulla **Vuorovaikutus**-osan kentät.</span><span class="sxs-lookup"><span data-stu-id="a32f5-119">In the **Segment page**, in the **Interaction** section, fill in the fields to specify which interaction you want to assign to the segment.</span></span>

    <span data-ttu-id="a32f5-120">Kun olet liittänyt vuorovaikutuksen segmenttiin, voit tehdä jokaisen segmentin kontaktin vuorovaikutuksesta yksilöllisen, esimerkiksi valitsemalla toisen vuorovaikutusmallin **Segmentti**-sivun riveillä.</span><span class="sxs-lookup"><span data-stu-id="a32f5-120">After you have assigned an interaction to the segment, you can personalize the interaction for each particular contact within the segment, for example, by selecting another interaction template on the lines on the **Segment** page.</span></span>  
3. <span data-ttu-id="a32f5-121">Voit kirjata segmentin ja vuorovaikutukset lokiin valitsemalla **Loki**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="a32f5-121">To log the segment and interactions, choose the **Log** action.</span></span> <span data-ttu-id="a32f5-122">**Lokin segmentti** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="a32f5-122">The **Log Segment** page opens.</span></span>
4. <span data-ttu-id="a32f5-123">Jos haluat luoda uuden segmentin, joka sisältää samat kontaktit, valitse **Luo seurantasegmentti** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="a32f5-123">If you want to create a new segment containing the same contacts, select the **Create Follow-up Segment** check box.</span></span> <span data-ttu-id="a32f5-124">Jotta ohjelma luo seurantasegmentin, segmenttien numerosarja on määritettävä **Kontaktienhallinnan asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="a32f5-124">To create a follow-up segment, you must have specified number series for segments on the **Marketing Setup** page.</span></span>

<span data-ttu-id="a32f5-125">Vuorovaikutus tallennetaan kullekin kontaktille **Vuorovaikutuslokitapahtuma**-taulukon segmentissä. Tämän jälkeen segmentti kirjataan lokiin.</span><span class="sxs-lookup"><span data-stu-id="a32f5-125">An interaction is recorded for each contact within the segment in the **Interaction Log Entry** table, and the segment is logged.</span></span> <span data-ttu-id="a32f5-126">Lokiin kirjatut segmentit löytyvät **Lokiin kirjattu segmentti** -sivulta.</span><span class="sxs-lookup"><span data-stu-id="a32f5-126">Logged segments can be found on the **Logged Segment** page.</span></span>

<span data-ttu-id="a32f5-127">Jos olet valinnut **Luo seurantasegmentti** -valintaruudun, ohjelma luo automaattisesti uuden segmentin, jossa on samat kontaktit kuin juuri lokiin kirjaamassasi segmentissä.</span><span class="sxs-lookup"><span data-stu-id="a32f5-127">If you have selected the **Create Follow-up Segment** check box, a new segment is created that contains the same contacts as the segment you have just logged.</span></span>

## <a name="see-also"></a><span data-ttu-id="a32f5-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a32f5-128">See Also</span></span>
[<span data-ttu-id="a32f5-129">Vuorovaikutusten tallentaminen</span><span class="sxs-lookup"><span data-stu-id="a32f5-129">Recording Interactions</span></span>](marketing-interactions.md)  
[<span data-ttu-id="a32f5-130">Kontaktien hallinta</span><span class="sxs-lookup"><span data-stu-id="a32f5-130">Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="a32f5-131">Myyntimahdollisuuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="a32f5-131">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="a32f5-132">Business Centralin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="a32f5-132">Working with Business Central</span></span>](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]