---
title: Yhdistäminen ja synkronointi | Microsoft Docs
description: Kun integrointitaulukon yhdistämismääritys synkronoidaan, yhdistettyjen Business Central- ja Dynamics 365 Sales -taulukoiden kaikkien tietueiden tiedot voidaan synkronoida.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 53b12b6ab7e53a20bb1b8fcc659b2f1454e85321
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779930"
---
# <a name="coupling-and-synchronizing"></a><span data-ttu-id="dfac8-103">Yhdistäminen ja synkronointi</span><span class="sxs-lookup"><span data-stu-id="dfac8-103">Coupling and Synchronizing</span></span>
<span data-ttu-id="dfac8-104">Tässä ohjeaiheessa kerrotaan, miten yksi tietue tai useita tietueita yhdistetään [!INCLUDE[prod_short](includes/prod_short.md)]:ssä Dataverse- tai [!INCLUDE[crm_md](includes/crm_md.md)]-tietueisiin.</span><span class="sxs-lookup"><span data-stu-id="dfac8-104">This topic describes how to couple one or more records in [!INCLUDE[prod_short](includes/prod_short.md)] with records in Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="dfac8-105">Tietueiden yhdistämisen ansiosta voit tarkastella Dataversein tietoja [!INCLUDE[prod_short](includes/prod_short.md)]ista ja päin vastoin.</span><span class="sxs-lookup"><span data-stu-id="dfac8-105">Coupling records lets you view Dataverse information from [!INCLUDE[prod_short](includes/prod_short.md)], and vice versa.</span></span> <span data-ttu-id="dfac8-106">Yhdistäminen mahdollistaa myös tietojen synkronoinnin tietueiden välillä.</span><span class="sxs-lookup"><span data-stu-id="dfac8-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="dfac8-107">Voit yhdistää aiemmin luotuja tietueita tai luoda ja yhdistää uusia tietueita.</span><span class="sxs-lookup"><span data-stu-id="dfac8-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="dfac8-108">Tietojen yhdistäminen ja synkronointi on käytettävissä vain, jos järjestelmänvalvoja on muodostanut yhteyden [!INCLUDE[prod_short](includes/prod_short.md)]:n ja Dataversen tai [!INCLUDE[crm_md](includes/crm_md.md)]:n välille.</span><span class="sxs-lookup"><span data-stu-id="dfac8-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[prod_short](includes/prod_short.md)] and Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="dfac8-109">Asian voi tarkistaa nopeasti avaamalla **Asiakas**-kortin ja etsimällä **Määritä yhdistäminen** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="dfac8-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="dfac8-110">Jos toiminto on käytettävissä, sovellukset on yhdistetty.</span><span class="sxs-lookup"><span data-stu-id="dfac8-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="dfac8-111">Esimerkkivideo</span><span class="sxs-lookup"><span data-stu-id="dfac8-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="dfac8-112">Tietueen yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="dfac8-112">To couple a record</span></span>  
1.  <span data-ttu-id="dfac8-113">Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa sen tietueen kortti, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="dfac8-113">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="dfac8-114">Se voi olla esimerkiksi asiakkaan tai yhteyshenkilön kortti.</span><span class="sxs-lookup"><span data-stu-id="dfac8-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="dfac8-115">Voit myös avata luettelosivun ja valita tietueen, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="dfac8-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="dfac8-116">Valitse **Määritä yhdistäminen** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="dfac8-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="dfac8-117">Täytä kentät ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfac8-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="dfac8-118">Yhden tietueen synkronointi</span><span class="sxs-lookup"><span data-stu-id="dfac8-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="dfac8-119">Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa sen tietueen kortti, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="dfac8-119">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="dfac8-120">Se voi olla esimerkiksi asiakkaan tai yhteyshenkilön kortti.</span><span class="sxs-lookup"><span data-stu-id="dfac8-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="dfac8-121">Valitse **Synkronoi nyt** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="dfac8-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="dfac8-122">Jos tietue voidaan synkronoida yhteen suuntaan, valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfac8-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="dfac8-123">Yhden tietueen synkronointi [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksesta</span><span class="sxs-lookup"><span data-stu-id="dfac8-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="dfac8-124">Avaa [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksessa sen tietueen lomake, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="dfac8-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="dfac8-125">Se voi olla esimerkiksi tilikortin tai yhteyshenkilökortin lomake.</span><span class="sxs-lookup"><span data-stu-id="dfac8-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="dfac8-126">Valitse **[!INCLUDE[prod_short](includes/prod_short.md)]** -toiminto valintanauhasta. Tietue avataan ja yhdistetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="dfac8-126">Choose the **[!INCLUDE[prod_short](includes/prod_short.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="dfac8-127">Voit synkronoida yhden tietueen [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksesta automaattisesti vain, kun **Synkronoi vain yhdistetyt tietueet** on poistettu käytöstä ja synkronoinnin suunnaksi on määritetty Kaksisuuntainen tai Integrointitaulukosta tietueen **Integrointitaulukon yhdistämismääritys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="dfac8-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="dfac8-128">Lisätietoja on kohdassa [Taulukoiden ja kenttien yhdistäminen synkronointia varten](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="dfac8-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="dfac8-129">Useiden tietueiden synkronointi</span><span class="sxs-lookup"><span data-stu-id="dfac8-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="dfac8-130">Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa tietueen luettelosivu, kuten asiakkaiden tai yhteyshenkilöiden luettelosivu.</span><span class="sxs-lookup"><span data-stu-id="dfac8-130">In [!INCLUDE[prod_short](includes/prod_short.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="dfac8-131">Valitse ensin synkronoitavat tietueet ja sitten **Synkronoi nyt** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="dfac8-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="dfac8-132">Jos tietueet voidaan synkronoida yhteen suuntaan, valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfac8-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="uncoupling-records"></a><span data-ttu-id="dfac8-133">Tietueiden yhdistämisen poistaminen</span><span class="sxs-lookup"><span data-stu-id="dfac8-133">Uncoupling Records</span></span>
<span data-ttu-id="dfac8-134">Voit irrottaa yhden tai useamman tietueen luettelosivuilta tai **Yhdistettyjen tietojen synkronointivirheet** -sivulta valitsemalla yhden tai useamman rivin ja valitsemalla **Poista yhdistäminen**.</span><span class="sxs-lookup"><span data-stu-id="dfac8-134">You can uncouple one or more records from list pages or the **Coupled Data Synchronization Errors** page by choosing one or more lines and choosing **Delete Coupling**.</span></span> <span data-ttu-id="dfac8-135">Voit myös poistaa kaikki yhden tai useamman taulukon yhdistämismäärityksen yhdistämiset **Integrointitaulukon yhdistämismääritykset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="dfac8-135">You can also remove all couplings for one or more table mappings on the **Integration Table Mappings** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="dfac8-136">Katso myös</span><span class="sxs-lookup"><span data-stu-id="dfac8-136">See Also</span></span>  
[<span data-ttu-id="dfac8-137">Dynamics 365 Salesin käyttäminen Business Centralissa</span><span class="sxs-lookup"><span data-stu-id="dfac8-137">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]