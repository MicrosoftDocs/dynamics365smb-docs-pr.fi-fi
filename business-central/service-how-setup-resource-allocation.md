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
ms.openlocfilehash: cac2d270fec47d35749d3ccf1ce1e3a3f130d097
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910328"
---
# <a name="set-up-resource-allocation"></a><span data-ttu-id="eb6c8-103">Resurssien kohdistamisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="eb6c8-103">Set Up Resource Allocation</span></span>
<span data-ttu-id="eb6c8-104">Huoltotehtävän onnistuneen suorittamisen kannalta on tärkeää löytää resurssi, jolla on työn edellyttävät taidot.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-104">To ensure that a service task is performed well, it's important to find a resource who is qualified to do the work.</span></span> <span data-ttu-id="eb6c8-105">Voit määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)] helpottamaan työhön vaadittavat taidot omaavan henkilön kohdistamista.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-105">You can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] so that it's easy to allocate someone who has the right skills for the job.</span></span> <span data-ttu-id="eb6c8-106">[!INCLUDE[d365fin](includes/d365fin_md.md)]issa tätä kutsutaan _resurssien kohdistamiseksi_.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], we call this _resource allocation_.</span></span> <span data-ttu-id="eb6c8-107">Resursseja voi kohdistaa taitojen tai saatavuuden perusteella tai sen perusteella, onko resurssi samalla huoltoalueella kuin asiakas.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-107">You can allocate resources based on their skill, availability, or whether they are in the same service zone as the customer.</span></span> 

<span data-ttu-id="eb6c8-108">Resurssien kohdistaminen edellyttää seuraavia määrityksiä:</span><span class="sxs-lookup"><span data-stu-id="eb6c8-108">To use resource allocation, you must set up:</span></span>  
  
* <span data-ttu-id="eb6c8-109">Huoltonimikkeiden korjaamiseen ja ylläpitämiseen tarvittavat taidot.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-109">The skills required to repair and maintain service items.</span></span> <span data-ttu-id="eb6c8-110">Ne määritetään huoltonimikkeille ja resursseille.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-110">You assign these to service items and resources.</span></span>  
* <span data-ttu-id="eb6c8-111">Markkina-alueelle määritettävät alueeksi kutsutut maantieteelliset alueet.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-111">Geographic regions, called zones, that you define for your market.</span></span> <span data-ttu-id="eb6c8-112">Alueita voivat olla esimerkiksi itä, länsi, etelä ja pohjoinen.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-112">For example, East, West, Central, and so on.</span></span> <span data-ttu-id="eb6c8-113">Alueet määritetään asiakkaille ja toimittajille.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-113">You assign these to customers and resources.</span></span>  
* <span data-ttu-id="eb6c8-114">Näytetäänkö resurssin taidot ja alueet sekä näytetäänkö varoitus, jos joku valitsee resurssin, jonka ei täytä vaatimuksia tai joka ei ole asiakkaan alueella.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-114">Whether to display resource skills and zones, and whether to display a warning if someone chooses unqualified resource, or a resource that is not in the customer zone.</span></span>  

## <a name="to-set-up-skills"></a><span data-ttu-id="eb6c8-115">Taitojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="eb6c8-115">To set up skills</span></span>
1. <span data-ttu-id="eb6c8-116">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Taidot** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Skills**, and then choose the related link.</span></span>  
2. <span data-ttu-id="eb6c8-117">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a><span data-ttu-id="eb6c8-118">Taitojen määrittäminen huoltonimikkeille ja resursseille</span><span class="sxs-lookup"><span data-stu-id="eb6c8-118">To assign skills to service items and resources</span></span>
1. <span data-ttu-id="eb6c8-119">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltonimikkeet** tai **Resurssit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="eb6c8-120">Avaa huoltonimikkeen tai resurssin kortti ja valitse sitten jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="eb6c8-120">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="eb6c8-121">Valitse huoltonimikkeille **Resurssin taidot**.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-121">For service items, choose **Resource Skills**.</span></span>  
    * <span data-ttu-id="eb6c8-122">Valitse resursseille **Taidot**.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-122">For resources, choose **Skills**.</span></span>  

## <a name="to-set-up-zones"></a><span data-ttu-id="eb6c8-123">Alueiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="eb6c8-123">To set up zones</span></span>
1. <span data-ttu-id="eb6c8-124">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Vyöhykkeet** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Zones**, and then choose the related link.</span></span>  
2. <span data-ttu-id="eb6c8-125">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a><span data-ttu-id="eb6c8-126">Alueiden määrittäminen asiakkaille ja resursseille</span><span class="sxs-lookup"><span data-stu-id="eb6c8-126">To assign zones to customers and resources</span></span> 
1. <span data-ttu-id="eb6c8-127">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** tai **Resurssit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="eb6c8-128">Avaa huoltonimikkeen tai resurssin kortti ja valitse sitten jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="eb6c8-128">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="eb6c8-129">Valitse asiakkaille alue **Huoltoalueen koodi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-129">For customers, choose a zone in the **Service Zone Code** field.</span></span>  
    * <span data-ttu-id="eb6c8-130">Valitse resursseille **Huoltoalueet**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-130">For resources, choose the **Service Zones** action.</span></span>  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a><span data-ttu-id="eb6c8-131">Resurssin valinnan yhteydessä näytettävien tietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="eb6c8-131">To specify what to show when a resource is chosen</span></span>
1. <span data-ttu-id="eb6c8-132">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huollon asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Setup**, and then choose the related link.</span></span> 
2. <span data-ttu-id="eb6c8-133">Valitse **Resurssin taitojen vaihtoehto** -kentässä jokin seuraavassa taulukossa käsiteltävistä vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-133">In the **Resource Skills Option** field, choose one of the options described in the following table.</span></span>  
  
    |<span data-ttu-id="eb6c8-134">**Vaihtoehto**</span><span class="sxs-lookup"><span data-stu-id="eb6c8-134">**Option**</span></span>|<span data-ttu-id="eb6c8-135">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="eb6c8-135">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="eb6c8-136">Koodi näytetty</span><span class="sxs-lookup"><span data-stu-id="eb6c8-136">Code Shown</span></span> | <span data-ttu-id="eb6c8-137">Näyttää vain koodin.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-137">Displays the code only.</span></span>|  
    |<span data-ttu-id="eb6c8-138">Varoitus näytetään</span><span class="sxs-lookup"><span data-stu-id="eb6c8-138">Warning Displayed</span></span> | <span data-ttu-id="eb6c8-139">Näyttää tiedot ja varoituksen, jos valitset resurssin, joka ei täytä vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-139">Shows the information and displays a warning if you choose a resource that is not qualified.</span></span>|  
    |<span data-ttu-id="eb6c8-140">Ei käytetty</span><span class="sxs-lookup"><span data-stu-id="eb6c8-140">Not Used</span></span> | <span data-ttu-id="eb6c8-141">Nämä tiedot eivät näy.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-141">Does not show this information.</span></span>|  

## <a name="to-update-resource-capacity"></a><span data-ttu-id="eb6c8-142">Resurssikapasiteetin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="eb6c8-142">To update resource capacity</span></span>  
<span data-ttu-id="eb6c8-143">Resurssien kapasiteetti on ehkä muutettava.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-143">You may need to change the capacity of resources.</span></span>  
  
1. <span data-ttu-id="eb6c8-144">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Resurssikapasiteetti** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Capacity**, and then choose the related link.</span></span>  
2. <span data-ttu-id="eb6c8-145">Valitse ensin resurssi ja sitten **Aseta kapasiteetti** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-145">Choose the resource, and then choose the **Set Capacity** action.</span></span>  
3. <span data-ttu-id="eb6c8-146">Tee muutokset ja valitse sitten **Päivitä kapasiteetti**.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-146">Make the changes, and then choose **Update Capacity**.</span></span>  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a><span data-ttu-id="eb6c8-147">Nimikkeiden, huoltonimikkeiden tai huoltonimikeryhmien taitojen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="eb6c8-147">To update skills for items, service items, or service item groups</span></span>
<span data-ttu-id="eb6c8-148">Jos haluat muuttaa nimikkeille määritettyjä taitokoodeja (vaikkapa **kpl** eikä **PC**), voit tehdä muutoksen joko nimikkeelle, huoltonimikkeelle tai huoltonimikeryhmän kaikille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-148">If you want to change the skill codes assigned to items, for example from **PC** to **PCS**, you can do so either for an item, service item, or for all items in a service item group.</span></span>  
  
1. <span data-ttu-id="eb6c8-149">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet**, **Huoltonimike** tai **Huoltonimikeryhmä** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items** or **Service Item**, or **Service Item Group**, and then choose the related link.</span></span>  
2. <span data-ttu-id="eb6c8-150">Valitse ensin päivitettävä objekti ja sitten **Resurssin taidot** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-150">Choose the entity to update, and then choose the **Resource Skills** action.</span></span>  
3. <span data-ttu-id="eb6c8-151">Valitse sopiva taitokoodi sen rivin **Taitokoodi**-kentässä, jolla muutettava koodi on.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-151">On the line with the code to be changed, in the **Skill Code** field, choose the relevant skill code.</span></span>  
4.  <span data-ttu-id="eb6c8-152">Jos nimikkeellä on siihen liittyviä huoltonimikkeitä, näyttöön tulee valintaruutu, jossa on kaksi vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-152">If the item has associated service items, a dialog box opens with the following two options:</span></span>  
  
    * <span data-ttu-id="eb6c8-153">Muuta taitokoodit valituksi arvoksi: Valitse tämä vaihtoehto, jos haluat korvata vanhan taitokoodin uudella kaikissa nimikkeeseen liittyvissä huoltonimikkeissä.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-153">Change the skill codes to the selected value: Select this option if you want to replace the old skill code with the new one on all the related service items.</span></span>  
    * <span data-ttu-id="eb6c8-154">Poista taitokoodit tai päivitä niiden suhteet: Valitse tämä vaihtoehto, jos haluat muuttaa vain nimikkeen taitokoodin.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-154">Delete the skill codes or update their relation: Select this option if you want to change the skill code on this item only.</span></span> <span data-ttu-id="eb6c8-155">Siihen liittyvien huoltonimikkeiden taitokoodit määritetään uudelleen, toisin sanoen **Määritetty kohteesta** -kenttä päivitetään.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-155">The skill code on the related service items will be reassigned, that is, the **Assigned From** field will be updated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb6c8-156">Katso myös</span><span class="sxs-lookup"><span data-stu-id="eb6c8-156">See Also</span></span>
[<span data-ttu-id="eb6c8-157">Resurssien kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="eb6c8-157">Allocate Resources</span></span>](service-how-to-allocate-resources.md)  
[<span data-ttu-id="eb6c8-158">Työ- ja huoltotuntien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="eb6c8-158">Set Up Work Hours and Service Hours</span></span>](service-how-setup-work-service-hours.md)  
[<span data-ttu-id="eb6c8-159">Vian raportoinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="eb6c8-159">Set Up Fault Reporting</span></span>](service-how-setup-fault-reporting.md)  
[<span data-ttu-id="eb6c8-160">Vakiohuoltokoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="eb6c8-160">Set Up Codes for Standard Services</span></span>](service-how-setup-service-coding.md)  
 

