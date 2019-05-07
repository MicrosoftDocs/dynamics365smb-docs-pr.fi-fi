---
title: Tietueiden yhdistäminen ja synkronoiminen manuaalisesti| Microsoft Docs
description: Kun integrointitaulukon yhdistämismääritys synkronoidaan, yhdistetyn Business Central- ja Dynamics 365 for Sales -objektin taulukon kaikkien tietueiden tiedot voidaan synkronoida.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 36f1a0fe8c50744d9ce13d1e6c3c899f4ceaf5e4
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "940121"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="25d03-103">Tietueiden yhdistäminen ja synkronoiminen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="25d03-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="25d03-104">Tässä ohjeaiheessa käsitellään vähintään yhden [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueen yhdistämistä [!INCLUDE[crm_md](includes/crm_md.md)]in tietueisiin.</span><span class="sxs-lookup"><span data-stu-id="25d03-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="25d03-105">Tietueiden yhdistämisen ansiosta voit tarkastella [!INCLUDE[crm_md](includes/crm_md.md)]in tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)]ista ja päin vastoin.</span><span class="sxs-lookup"><span data-stu-id="25d03-105">Coupling records lets you view [!INCLUDE[crm_md](includes/crm_md.md)] information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="25d03-106">Yhdistäminen mahdollistaa myös tietojen synkronoinnin tietueiden välillä.</span><span class="sxs-lookup"><span data-stu-id="25d03-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="25d03-107">Voit yhdistää aiemmin luotuja tietueita tai luoda ja yhdistää uusia tietueita.</span><span class="sxs-lookup"><span data-stu-id="25d03-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="25d03-108">Tietojen yhdistäminen ja synkronointi [!INCLUDE[crm_md](includes/crm_md.md)]in avulla on käytettävissä vain, jos järjestelmänvalvoja on muodostanut yhteyden [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in välille.</span><span class="sxs-lookup"><span data-stu-id="25d03-108">Coupling and synchronizing data with [!INCLUDE[crm_md](includes/crm_md.md)] is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="25d03-109">Asian voi tarkistaa nopeasti avaamalla **Asiakas**-kortin ja etsimällä **Määritä yhdistäminen** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="25d03-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="25d03-110">Jos toiminto on käytettävissä, sovellukset on yhdistetty.</span><span class="sxs-lookup"><span data-stu-id="25d03-110">If the action is available, the apps are connected.</span></span>   

## <a name="to-couple-a-record"></a><span data-ttu-id="25d03-111">Tietueen yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="25d03-111">To couple a record</span></span>  
1.  <span data-ttu-id="25d03-112">Avaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa sen tietueen kortti, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="25d03-112">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="25d03-113">Se voi olla esimerkiksi asiakkaan tai yhteyshenkilön kortti.</span><span class="sxs-lookup"><span data-stu-id="25d03-113">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="25d03-114">Voit myös avata luettelosivun ja valita tietueen, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="25d03-114">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="25d03-115">Valitse **Määritä yhdistäminen** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="25d03-115">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="25d03-116">Täytä kentät ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="25d03-116">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="25d03-117">Yhden tietueen synkronointi</span><span class="sxs-lookup"><span data-stu-id="25d03-117">To synchronize a single record</span></span>  
1.  <span data-ttu-id="25d03-118">Avaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa sen tietueen kortti, jonka haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="25d03-118">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="25d03-119">Se voi olla esimerkiksi asiakkaan tai yhteyshenkilön kortti.</span><span class="sxs-lookup"><span data-stu-id="25d03-119">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="25d03-120">Valitse **Synkronoi nyt** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="25d03-120">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="25d03-121">Jos tietue voidaan synkronoida joko [!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin tai [!INCLUDE[crm_md](includes/crm_md.md)]ista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin , valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="25d03-121">If a record can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="25d03-122">Useiden tietueiden synkronointi</span><span class="sxs-lookup"><span data-stu-id="25d03-122">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="25d03-123">Avaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tietueen luettelosivu, kuten asiakkaiden tai yhteyshenkilöiden luettelosivu.</span><span class="sxs-lookup"><span data-stu-id="25d03-123">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="25d03-124">Valitse ensin synkronoitavat tietueet ja sitten **Synkronoi nyt** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="25d03-124">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="25d03-125">Jos tietueet voidaan synkronoida joko [!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin tai [!INCLUDE[crm_md](includes/crm_md.md)]ista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin , valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="25d03-125">If records can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="25d03-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="25d03-126">See Also</span></span>  
[<span data-ttu-id="25d03-127">Dynamics 365 for Salesin käyttö Business Centralista</span><span class="sxs-lookup"><span data-stu-id="25d03-127">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
