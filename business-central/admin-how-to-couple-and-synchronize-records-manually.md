---
title: Tietueiden yhdistäminen ja synkronoiminen manuaalisesti| Microsoft Docs
description: Kun integrointitaulukon yhdistämismääritys synkronoidaan, yhdistetyn Business Central- ja Dynamics 365 Sales -entiteetin taulukon kaikkien tietueiden tiedot voidaan synkronoida.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: fdc407ef26d238ba54a2566cdd9003c29da2eeb3
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196661"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="18fd4-103">Tietueiden yhdistäminen ja synkronoiminen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="18fd4-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="18fd4-104">Tässä ohjeaiheessa kerrotaan, miten yksi tietue tai useita tietueita yhdistetään [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä Common Data Service- tai [!INCLUDE[crm_md](includes/crm_md.md)]-tietueisiin.</span><span class="sxs-lookup"><span data-stu-id="18fd4-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="18fd4-105">Tietueiden yhdistämisen ansiosta voit tarkastella Common Data Servicein tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)]ista ja päin vastoin.</span><span class="sxs-lookup"><span data-stu-id="18fd4-105">Coupling records lets you view Common Data Service information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="18fd4-106">Yhdistäminen mahdollistaa myös tietojen synkronoinnin tietueiden välillä.</span><span class="sxs-lookup"><span data-stu-id="18fd4-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="18fd4-107">Voit yhdistää aiemmin luotuja tietueita tai luoda ja yhdistää uusia tietueita.</span><span class="sxs-lookup"><span data-stu-id="18fd4-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="18fd4-108">Tietojen yhdistäminen ja synkronointi on käytettävissä vain, jos järjestelmänvalvoja on muodostanut yhteyden [!INCLUDE[d365fin](includes/d365fin_md.md)]:n ja Common Data Servicen tai [!INCLUDE[crm_md](includes/crm_md.md)]:n välille.</span><span class="sxs-lookup"><span data-stu-id="18fd4-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="18fd4-109">Asian voi tarkistaa nopeasti avaamalla **Asiakas**-kortin ja etsimällä **Määritä yhdistäminen** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="18fd4-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="18fd4-110">Jos toiminto on käytettävissä, sovellukset on yhdistetty.</span><span class="sxs-lookup"><span data-stu-id="18fd4-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="18fd4-111">Esimerkkivideo</span><span class="sxs-lookup"><span data-stu-id="18fd4-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="18fd4-112">Tietueen yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="18fd4-112">To couple a record</span></span>  
1.  <span data-ttu-id="18fd4-113">Avaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa sen tietueen kortti, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="18fd4-113">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="18fd4-114">Se voi olla esimerkiksi asiakkaan tai yhteyshenkilön kortti.</span><span class="sxs-lookup"><span data-stu-id="18fd4-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="18fd4-115">Voit myös avata luettelosivun ja valita tietueen, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="18fd4-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="18fd4-116">Valitse **Määritä yhdistäminen** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="18fd4-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="18fd4-117">Täytä kentät ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="18fd4-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="18fd4-118">Yhden tietueen synkronointi</span><span class="sxs-lookup"><span data-stu-id="18fd4-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="18fd4-119">Avaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa sen tietueen kortti, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="18fd4-119">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="18fd4-120">Se voi olla esimerkiksi asiakkaan tai yhteyshenkilön kortti.</span><span class="sxs-lookup"><span data-stu-id="18fd4-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="18fd4-121">Valitse **Synkronoi nyt** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="18fd4-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="18fd4-122">Jos tietue voidaan synkronoida yhteen suuntaan, valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="18fd4-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="18fd4-123">Yhden tietueen synkronointi [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksesta</span><span class="sxs-lookup"><span data-stu-id="18fd4-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="18fd4-124">Avaa [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksessa sen tietueen lomake, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="18fd4-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="18fd4-125">Se voi olla esimerkiksi tilikortin tai yhteyshenkilökortin lomake.</span><span class="sxs-lookup"><span data-stu-id="18fd4-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="18fd4-126">Valitse **[!INCLUDE[d365fin](includes/d365fin_md.md)]** -toiminto valintanauhasta. Tietue avataan ja yhdistetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="18fd4-126">Choose the **[!INCLUDE[d365fin](includes/d365fin_md.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="18fd4-127">Voit synkronoida yhden tietueen [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksesta automaattisesti vain, kun **Synkronoi vain yhdistetyt tietueet** on poistettu käytöstä ja synkronoinnin suunnaksi on määritetty Kaksisuuntainen tai Integrointitaulukosta tietueen **Integrointitaulukon yhdistämismääritys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="18fd4-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="18fd4-128">Lisätietoja on kohdassa [Taulukoiden ja kenttien yhdistäminen synkronointia varten](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="18fd4-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="18fd4-129">Useiden tietueiden synkronointi</span><span class="sxs-lookup"><span data-stu-id="18fd4-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="18fd4-130">Avaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tietueen luettelosivu, kuten asiakkaiden tai yhteyshenkilöiden luettelosivu.</span><span class="sxs-lookup"><span data-stu-id="18fd4-130">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="18fd4-131">Valitse ensin synkronoitavat tietueet ja sitten **Synkronoi nyt** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="18fd4-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="18fd4-132">Jos tietueet voidaan synkronoida yhteen suuntaan, valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="18fd4-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="18fd4-133">Katso myös</span><span class="sxs-lookup"><span data-stu-id="18fd4-133">See Also</span></span>  
[<span data-ttu-id="18fd4-134">Dynamics 365 Salesin käyttäminen Business Centralissa</span><span class="sxs-lookup"><span data-stu-id="18fd4-134">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
