---
title: Yhdistäminen ja synkronointi | Microsoft Docs
description: Kun integrointitaulukon yhdistämismääritys synkronoidaan, yhdistettyjen Business Central- ja Dynamics 365 Sales -taulukoiden kaikkien tietueiden tiedot voidaan synkronoida.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: fa4d6cfe13662613a73c14d68542f8319798ea80
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752673"
---
# <a name="coupling-and-synchronizing"></a><span data-ttu-id="0f031-103">Yhdistäminen ja synkronointi</span><span class="sxs-lookup"><span data-stu-id="0f031-103">Coupling and Synchronizing</span></span>
<span data-ttu-id="0f031-104">Tässä ohjeaiheessa kerrotaan, miten yksi tietue tai useita tietueita yhdistetään [!INCLUDE[prod_short](includes/prod_short.md)]:ssä Dataverse- tai [!INCLUDE[crm_md](includes/crm_md.md)]-tietueisiin.</span><span class="sxs-lookup"><span data-stu-id="0f031-104">This topic describes how to couple one or more records in [!INCLUDE[prod_short](includes/prod_short.md)] with records in Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="0f031-105">Tietueiden yhdistämisen ansiosta voit tarkastella Dataversein tietoja [!INCLUDE[prod_short](includes/prod_short.md)]ista ja päin vastoin.</span><span class="sxs-lookup"><span data-stu-id="0f031-105">Coupling records lets you view Dataverse information from [!INCLUDE[prod_short](includes/prod_short.md)], and vice versa.</span></span> <span data-ttu-id="0f031-106">Yhdistäminen mahdollistaa myös tietojen synkronoinnin tietueiden välillä.</span><span class="sxs-lookup"><span data-stu-id="0f031-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="0f031-107">Voit yhdistää aiemmin luotuja tietueita tai luoda ja yhdistää uusia tietueita.</span><span class="sxs-lookup"><span data-stu-id="0f031-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="0f031-108">Tietojen yhdistäminen ja synkronointi on käytettävissä vain, jos järjestelmänvalvoja on muodostanut yhteyden [!INCLUDE[prod_short](includes/prod_short.md)]:n ja Dataversen tai [!INCLUDE[crm_md](includes/crm_md.md)]:n välille.</span><span class="sxs-lookup"><span data-stu-id="0f031-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[prod_short](includes/prod_short.md)] and Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="0f031-109">Asian voi tarkistaa nopeasti avaamalla **Asiakas**-kortin ja etsimällä **Määritä yhdistäminen** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="0f031-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="0f031-110">Jos toiminto on käytettävissä, sovellukset on yhdistetty.</span><span class="sxs-lookup"><span data-stu-id="0f031-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="0f031-111">Esimerkkivideo</span><span class="sxs-lookup"><span data-stu-id="0f031-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="0f031-112">Tietueen yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="0f031-112">To couple a record</span></span>  
1.  <span data-ttu-id="0f031-113">Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa sen tietueen kortti, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="0f031-113">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="0f031-114">Se voi olla esimerkiksi asiakkaan tai yhteyshenkilön kortti.</span><span class="sxs-lookup"><span data-stu-id="0f031-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="0f031-115">Voit myös avata luettelosivun ja valita tietueen, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="0f031-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="0f031-116">Valitse **Määritä yhdistäminen** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="0f031-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="0f031-117">Täytä kentät ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f031-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="0f031-118">Yhden tietueen synkronointi</span><span class="sxs-lookup"><span data-stu-id="0f031-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="0f031-119">Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa sen tietueen kortti, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="0f031-119">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="0f031-120">Se voi olla esimerkiksi asiakkaan tai yhteyshenkilön kortti.</span><span class="sxs-lookup"><span data-stu-id="0f031-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="0f031-121">Valitse **Synkronoi nyt** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="0f031-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="0f031-122">Jos tietue voidaan synkronoida yhteen suuntaan, valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f031-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="0f031-123">Yhden tietueen synkronointi [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksesta</span><span class="sxs-lookup"><span data-stu-id="0f031-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="0f031-124">Avaa [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksessa sen tietueen lomake, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="0f031-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="0f031-125">Se voi olla esimerkiksi tilikortin tai yhteyshenkilökortin lomake.</span><span class="sxs-lookup"><span data-stu-id="0f031-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="0f031-126">Valitse **[!INCLUDE[prod_short](includes/prod_short.md)]** -toiminto valintanauhasta. Tietue avataan ja yhdistetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="0f031-126">Choose the **[!INCLUDE[prod_short](includes/prod_short.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="0f031-127">Voit synkronoida yhden tietueen [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksesta automaattisesti vain, kun **Synkronoi vain yhdistetyt tietueet** on poistettu käytöstä ja synkronoinnin suunnaksi on määritetty Kaksisuuntainen tai Integrointitaulukosta tietueen **Integrointitaulukon yhdistämismääritys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="0f031-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="0f031-128">Lisätietoja on kohdassa [Taulukoiden ja kenttien yhdistäminen synkronointia varten](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="0f031-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="0f031-129">Useiden tietueiden synkronointi</span><span class="sxs-lookup"><span data-stu-id="0f031-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="0f031-130">Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa tietueen luettelosivu, kuten asiakkaiden tai yhteyshenkilöiden luettelosivu.</span><span class="sxs-lookup"><span data-stu-id="0f031-130">In [!INCLUDE[prod_short](includes/prod_short.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="0f031-131">Valitse ensin synkronoitavat tietueet ja sitten **Synkronoi nyt** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="0f031-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="0f031-132">Jos tietueet voidaan synkronoida yhteen suuntaan, valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f031-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="uncoupling-records"></a><span data-ttu-id="0f031-133">Tietueiden yhdistämisen poistaminen</span><span class="sxs-lookup"><span data-stu-id="0f031-133">Uncoupling Records</span></span>
<span data-ttu-id="0f031-134">Voit irrottaa yhden tai useamman tietueen luettelosivuilta tai **Yhdistettyjen tietojen synkronointivirheet** -sivulta valitsemalla yhden tai useamman rivin ja valitsemalla **Poista yhdistäminen**.</span><span class="sxs-lookup"><span data-stu-id="0f031-134">You can uncouple one or more records from list pages or the **Coupled Data Synchronization Errors** page by choosing one or more lines and choosing **Delete Coupling**.</span></span> <span data-ttu-id="0f031-135">Voit myös poistaa kaikki yhden tai useamman taulukon yhdistämismäärityksen yhdistämiset **Integrointitaulukon yhdistämismääritykset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="0f031-135">You can also remove all couplings for one or more table mappings on the **Integration Table Mappings** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f031-136">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0f031-136">See Also</span></span>  
[<span data-ttu-id="0f031-137">Dynamics 365 Salesin käyttäminen Business Centralissa</span><span class="sxs-lookup"><span data-stu-id="0f031-137">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
