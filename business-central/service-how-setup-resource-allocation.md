---
title: Resurssien kohdistuksen määrittäminen | Microsoft Docs
description: Lisätietoja tavoista, joilla järjestelmä voi auttaa varmistamaan, että palvelun tarjoamiseen määritetyllä henkilöllä on siihen tarvittavat taidot.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 48d0f9f9e51a0da3f82abdb43e8c4bb6044a5f29
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757990"
---
# <a name="set-up-resource-allocation"></a><span data-ttu-id="7d2c9-103">Resurssien kohdistamisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7d2c9-103">Set Up Resource Allocation</span></span>
<span data-ttu-id="7d2c9-104">Huoltotehtävän onnistuneen suorittamisen kannalta on tärkeää löytää resurssi, jolla on työn edellyttävät taidot.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-104">To ensure that a service task is performed well, it's important to find a resource who is qualified to do the work.</span></span> <span data-ttu-id="7d2c9-105">Voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)] helpottamaan työhön vaadittavat taidot omaavan henkilön kohdistamista.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-105">You can set up [!INCLUDE[prod_short](includes/prod_short.md)] so that it's easy to allocate someone who has the right skills for the job.</span></span> <span data-ttu-id="7d2c9-106">[!INCLUDE[prod_short](includes/prod_short.md)]issa tätä kutsutaan _resurssien kohdistamiseksi_.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-106">In [!INCLUDE[prod_short](includes/prod_short.md)], we call this _resource allocation_.</span></span> <span data-ttu-id="7d2c9-107">Resursseja voi kohdistaa taitojen tai saatavuuden perusteella tai sen perusteella, onko resurssi samalla huoltoalueella kuin asiakas.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-107">You can allocate resources based on their skill, availability, or whether they are in the same service zone as the customer.</span></span> 

<span data-ttu-id="7d2c9-108">Resurssien kohdistaminen edellyttää seuraavia määrityksiä:</span><span class="sxs-lookup"><span data-stu-id="7d2c9-108">To use resource allocation, you must set up:</span></span>  
  
* <span data-ttu-id="7d2c9-109">Huoltonimikkeiden korjaamiseen ja ylläpitämiseen tarvittavat taidot.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-109">The skills required to repair and maintain service items.</span></span> <span data-ttu-id="7d2c9-110">Ne määritetään huoltonimikkeille ja resursseille.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-110">You assign these to service items and resources.</span></span>  
* <span data-ttu-id="7d2c9-111">Markkina-alueelle määritettävät alueeksi kutsutut maantieteelliset alueet.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-111">Geographic regions, called zones, that you define for your market.</span></span> <span data-ttu-id="7d2c9-112">Alueita voivat olla esimerkiksi itä, länsi, etelä ja pohjoinen.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-112">For example, East, West, Central, and so on.</span></span> <span data-ttu-id="7d2c9-113">Alueet määritetään asiakkaille ja toimittajille.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-113">You assign these to customers and resources.</span></span>  
* <span data-ttu-id="7d2c9-114">Näytetäänkö resurssin taidot ja alueet sekä näytetäänkö varoitus, jos joku valitsee resurssin, jonka ei täytä vaatimuksia tai joka ei ole asiakkaan alueella.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-114">Whether to display resource skills and zones, and whether to display a warning if someone chooses unqualified resource, or a resource that is not in the customer zone.</span></span>  

## <a name="to-set-up-skills"></a><span data-ttu-id="7d2c9-115">Taitojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7d2c9-115">To set up skills</span></span>
1. <span data-ttu-id="7d2c9-116">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Taidot** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Skills**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7d2c9-117">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a><span data-ttu-id="7d2c9-118">Taitojen määrittäminen huoltonimikkeille ja resursseille</span><span class="sxs-lookup"><span data-stu-id="7d2c9-118">To assign skills to service items and resources</span></span>
1. <span data-ttu-id="7d2c9-119">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltonimikkeet** tai **Resurssit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7d2c9-120">Avaa huoltonimikkeen tai resurssin kortti ja valitse sitten jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="7d2c9-120">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="7d2c9-121">Valitse huoltonimikkeille **Resurssin taidot**.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-121">For service items, choose **Resource Skills**.</span></span>  
    * <span data-ttu-id="7d2c9-122">Valitse resursseille **Taidot**.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-122">For resources, choose **Skills**.</span></span>  

## <a name="to-set-up-zones"></a><span data-ttu-id="7d2c9-123">Alueiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7d2c9-123">To set up zones</span></span>
1. <span data-ttu-id="7d2c9-124">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Vyöhykkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Zones**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7d2c9-125">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a><span data-ttu-id="7d2c9-126">Alueiden määrittäminen asiakkaille ja resursseille</span><span class="sxs-lookup"><span data-stu-id="7d2c9-126">To assign zones to customers and resources</span></span> 
1. <span data-ttu-id="7d2c9-127">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** tai **Resurssit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7d2c9-128">Avaa huoltonimikkeen tai resurssin kortti ja valitse sitten jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="7d2c9-128">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="7d2c9-129">Valitse asiakkaille alue **Huoltoalueen koodi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-129">For customers, choose a zone in the **Service Zone Code** field.</span></span>  
    * <span data-ttu-id="7d2c9-130">Valitse resursseille **Huoltoalueet**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-130">For resources, choose the **Service Zones** action.</span></span>  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a><span data-ttu-id="7d2c9-131">Resurssin valinnan yhteydessä näytettävien tietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7d2c9-131">To specify what to show when a resource is chosen</span></span>
1. <span data-ttu-id="7d2c9-132">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huollon hallinnan asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Management Setup**, and then choose the related link.</span></span> 
2. <span data-ttu-id="7d2c9-133">Valitse **Resurssin taitojen vaihtoehto** -kentässä jokin seuraavassa taulukossa käsiteltävistä vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-133">In the **Resource Skills Option** field, choose one of the options described in the following table.</span></span>  
  
    |<span data-ttu-id="7d2c9-134">**Vaihtoehto**</span><span class="sxs-lookup"><span data-stu-id="7d2c9-134">**Option**</span></span>|<span data-ttu-id="7d2c9-135">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="7d2c9-135">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="7d2c9-136">Koodi näytetty</span><span class="sxs-lookup"><span data-stu-id="7d2c9-136">Code Shown</span></span> | <span data-ttu-id="7d2c9-137">Näyttää vain koodin.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-137">Displays the code only.</span></span>|  
    |<span data-ttu-id="7d2c9-138">Varoitus näytetään</span><span class="sxs-lookup"><span data-stu-id="7d2c9-138">Warning Displayed</span></span> | <span data-ttu-id="7d2c9-139">Näyttää tiedot ja varoituksen, jos valitset resurssin, joka ei täytä vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-139">Shows the information and displays a warning if you choose a resource that is not qualified.</span></span>|  
    |<span data-ttu-id="7d2c9-140">Ei käytetty</span><span class="sxs-lookup"><span data-stu-id="7d2c9-140">Not Used</span></span> | <span data-ttu-id="7d2c9-141">Nämä tiedot eivät näy.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-141">Does not show this information.</span></span>|  

## <a name="to-update-resource-capacity"></a><span data-ttu-id="7d2c9-142">Resurssikapasiteetin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="7d2c9-142">To update resource capacity</span></span>  
<span data-ttu-id="7d2c9-143">Resurssien kapasiteetti on ehkä muutettava.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-143">You may need to change the capacity of resources.</span></span>  
  
1. <span data-ttu-id="7d2c9-144">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Resurssikapasiteetti** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Capacity**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7d2c9-145">Valitse ensin resurssi ja sitten **Aseta kapasiteetti** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-145">Choose the resource, and then choose the **Set Capacity** action.</span></span>  
3. <span data-ttu-id="7d2c9-146">Tee muutokset ja valitse sitten **Päivitä kapasiteetti**.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-146">Make the changes, and then choose **Update Capacity**.</span></span>  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a><span data-ttu-id="7d2c9-147">Nimikkeiden, huoltonimikkeiden tai huoltonimikeryhmien taitojen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="7d2c9-147">To update skills for items, service items, or service item groups</span></span>
<span data-ttu-id="7d2c9-148">Jos haluat muuttaa nimikkeille määritettyjä taitokoodeja (vaikkapa **kpl** eikä **PC**), voit tehdä muutoksen joko nimikkeelle, huoltonimikkeelle tai huoltonimikeryhmän kaikille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-148">If you want to change the skill codes assigned to items, for example from **PC** to **PCS**, you can do so either for an item, service item, or for all items in a service item group.</span></span>  
  
1. <span data-ttu-id="7d2c9-149">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet**, **Huoltonimike** tai **Huoltonimikeryhmä** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items** or **Service Item**, or **Service Item Group**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7d2c9-150">Valitse ensin päivitettävä objekti ja sitten **Resurssin taidot** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-150">Choose the entity to update, and then choose the **Resource Skills** action.</span></span>  
3. <span data-ttu-id="7d2c9-151">Valitse sopiva taitokoodi sen rivin **Taitokoodi**-kentässä, jolla muutettava koodi on.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-151">On the line with the code to be changed, in the **Skill Code** field, choose the relevant skill code.</span></span>  
4.  <span data-ttu-id="7d2c9-152">Jos nimikkeellä on siihen liittyviä huoltonimikkeitä, näyttöön tulee valintaruutu, jossa on kaksi vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-152">If the item has associated service items, a dialog box opens with the following two options:</span></span>  
  
    * <span data-ttu-id="7d2c9-153">Muuta taitokoodit valituksi arvoksi: Valitse tämä vaihtoehto, jos haluat korvata vanhan taitokoodin uudella kaikissa nimikkeeseen liittyvissä huoltonimikkeissä.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-153">Change the skill codes to the selected value: Select this option if you want to replace the old skill code with the new one on all the related service items.</span></span>  
    * <span data-ttu-id="7d2c9-154">Poista taitokoodit tai päivitä niiden suhteet: Valitse tämä vaihtoehto, jos haluat muuttaa vain nimikkeen taitokoodin.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-154">Delete the skill codes or update their relation: Select this option if you want to change the skill code on this item only.</span></span> <span data-ttu-id="7d2c9-155">Siihen liittyvien huoltonimikkeiden taitokoodit määritetään uudelleen, toisin sanoen **Määritetty kohteesta** -kenttä päivitetään.</span><span class="sxs-lookup"><span data-stu-id="7d2c9-155">The skill code on the related service items will be reassigned, that is, the **Assigned From** field will be updated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d2c9-156">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7d2c9-156">See Also</span></span>
[<span data-ttu-id="7d2c9-157">Resurssien kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="7d2c9-157">Allocate Resources</span></span>](service-how-to-allocate-resources.md)  
[<span data-ttu-id="7d2c9-158">Työ- ja huoltotuntien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7d2c9-158">Set Up Work Hours and Service Hours</span></span>](service-how-setup-work-service-hours.md)  
[<span data-ttu-id="7d2c9-159">Vian raportoinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7d2c9-159">Set Up Fault Reporting</span></span>](service-how-setup-fault-reporting.md)  
[<span data-ttu-id="7d2c9-160">Vakiohuoltokoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7d2c9-160">Set Up Codes for Standard Services</span></span>](service-how-setup-service-coding.md)  
 

