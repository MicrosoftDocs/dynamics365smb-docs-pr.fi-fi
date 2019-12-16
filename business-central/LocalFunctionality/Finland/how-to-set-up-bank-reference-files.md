---
title: Pankin viitetiedostojen määrittäminen
description: Elektronisten maksujen käsittelyä varten on ensin määritettävä pankin viitetiedostot, joiden avulla määritetään, miten maksutiedot tuodaan tai viedään.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/18/2019
ms.author: sgroespe
ms.openlocfilehash: f673af1a442b5a98b18dbb92fd78f1faef742a06
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879277"
---
# <a name="set-up-bank-reference-files"></a><span data-ttu-id="3115c-103">Pankin viitetiedostojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3115c-103">Set Up Bank Reference Files</span></span>
<span data-ttu-id="3115c-104">Elektronisten maksujen käsittelyä varten on ensin määritettävä pankin viitetiedostot, joiden avulla määritetään, miten maksutiedot tuodaan tai viedään.</span><span class="sxs-lookup"><span data-stu-id="3115c-104">To process electronic payments, you must first set up bank reference files to determine how payment data should be imported or exported.</span></span>  

## <a name="to-set-up-a-bank-reference-file"></a><span data-ttu-id="3115c-105">Pankin viitetiedoston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3115c-105">To set up a bank reference file</span></span>  

1.  <span data-ttu-id="3115c-106">Valitse ![Etsi sivu tai raportti](../../media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") kuvakkeen, anna **Pankin viitetiedoston asetukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3115c-106">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Reference File Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3115c-107">Täytä **Yleinen**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="3115c-107">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="3115c-108">Kenttä</span><span class="sxs-lookup"><span data-stu-id="3115c-108">Field</span></span>|<span data-ttu-id="3115c-109">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="3115c-109">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="3115c-110">**Ei.**</span><span class="sxs-lookup"><span data-stu-id="3115c-110">**No.**</span></span>|<span data-ttu-id="3115c-111">Määrittää pankkitilin koodin.</span><span class="sxs-lookup"><span data-stu-id="3115c-111">Specifies a bank account code.</span></span>|  
    |<span data-ttu-id="3115c-112">**Kohdistettujen hyvityslaskujen tiedot**</span><span class="sxs-lookup"><span data-stu-id="3115c-112">**Inform. of Appl. Cr. Memos**</span></span>|<span data-ttu-id="3115c-113">Kun valitset tämän, laskuihin kohdistetut hyvitykset näkyvät maksun vastaanottajan tiliotteessa.</span><span class="sxs-lookup"><span data-stu-id="3115c-113">Select to display credits applied to invoices on the payment recipient's account statement.</span></span>|  

3.  <span data-ttu-id="3115c-114">Täytä **Ulkomaan maksut** -pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="3115c-114">On the **Foreign Payments** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="3115c-115">Kenttä</span><span class="sxs-lookup"><span data-stu-id="3115c-115">Field</span></span>|<span data-ttu-id="3115c-116">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="3115c-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="3115c-117">**Eräpäivän käsittely**</span><span class="sxs-lookup"><span data-stu-id="3115c-117">**Due Date Handling**</span></span>|<span data-ttu-id="3115c-118">Määritä, miten eräpäivän käsittelyä käytetään ulkomaan maksuissa.</span><span class="sxs-lookup"><span data-stu-id="3115c-118">Select how due date processing should be applied to foreign payments.</span></span><br /><br /> <span data-ttu-id="3115c-119">**Erä** – Kaikki tiedoston maksut saavat saman maksupäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="3115c-119">**Batch** – All payments in the file receive the same payment date.</span></span><br /><br /> <span data-ttu-id="3115c-120">-tai-</span><span class="sxs-lookup"><span data-stu-id="3115c-120">–or–</span></span><br /><br /> <span data-ttu-id="3115c-121">**Tapahtuma** – Jokainen tiedoston maksu saa tapahtumakohtaisen maksupäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="3115c-121">**Transaction** – Each payment in the file receives a transaction-specific payment date.</span></span> <span data-ttu-id="3115c-122">Kysy pankista lisätietoja tämän asetuksen käytöstä.</span><span class="sxs-lookup"><span data-stu-id="3115c-122">Contact your bank to determine whether this setting should be used.</span></span>|  
    |<span data-ttu-id="3115c-123">**Palvelumaksun oletuskoodi**</span><span class="sxs-lookup"><span data-stu-id="3115c-123">**Default Service Fee Code**</span></span>|<span data-ttu-id="3115c-124">Valitse palvelumaksun oletuskoodi ulkomaan pankkeja varten.</span><span class="sxs-lookup"><span data-stu-id="3115c-124">Select a default service fee code for foreign banks.</span></span>|  
    |<span data-ttu-id="3115c-125">**Oletusmaksutapa**</span><span class="sxs-lookup"><span data-stu-id="3115c-125">**Default Payment Method**</span></span>|<span data-ttu-id="3115c-126">Valitse oletusmaksutapa ulkomaan pankkeja varten.</span><span class="sxs-lookup"><span data-stu-id="3115c-126">Select a default payment method for foreign payments.</span></span>|  
    |<span data-ttu-id="3115c-127">**Vaihtokurssin sopimusnro**</span><span class="sxs-lookup"><span data-stu-id="3115c-127">**Exchange Rate Contract No.**</span></span>|<span data-ttu-id="3115c-128">Anna vaihtokurssin sopimusnumero.</span><span class="sxs-lookup"><span data-stu-id="3115c-128">Enter the exchange rate contract number.</span></span>|  
    |<span data-ttu-id="3115c-129">**Salli ulkomaan maksujen yhdistäminen**</span><span class="sxs-lookup"><span data-stu-id="3115c-129">**Allow Comb. Foreign Pmts.**</span></span>|<span data-ttu-id="3115c-130">Yhdistä kaikki yhdelle vastaanottajalle tietyn päivän aikana samalta pankkitililtä tehdyt ulkomaan maksut.</span><span class="sxs-lookup"><span data-stu-id="3115c-130">Select to combine all foreign payments made to one recipient in one day from the same bank account.</span></span>|  

4.  <span data-ttu-id="3115c-131">Täytä **SEPA**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="3115c-131">On the **SEPA** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="3115c-132">Kenttä</span><span class="sxs-lookup"><span data-stu-id="3115c-132">Field</span></span>|<span data-ttu-id="3115c-133">Description</span><span class="sxs-lookup"><span data-stu-id="3115c-133">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="3115c-134">**Pankin tunnus**</span><span class="sxs-lookup"><span data-stu-id="3115c-134">**Bank Party ID**</span></span>|<span data-ttu-id="3115c-135">Anna SEPA-pankin tunnus.</span><span class="sxs-lookup"><span data-stu-id="3115c-135">Enter a SEPA bank party ID.</span></span> <span data-ttu-id="3115c-136">**Huomautus:** Tätä kenttää käytetään vain SEPA-standardissa pain.001.001.02.</span><span class="sxs-lookup"><span data-stu-id="3115c-136">**Note:**  This field is only used for the SEPA pain.001.001.02 standard.</span></span>|  
    |<span data-ttu-id="3115c-137">**Tiedostonimi**</span><span class="sxs-lookup"><span data-stu-id="3115c-137">**File Name**</span></span>|<span data-ttu-id="3115c-138">Anna SEPA-maksutiedoston koko polku.</span><span class="sxs-lookup"><span data-stu-id="3115c-138">Enter the full path of the SEPA payment file.</span></span> <span data-ttu-id="3115c-139">**Huomautus:** Tätä kenttää käytetään vain SEPA-standardissa pain.001.001.02.</span><span class="sxs-lookup"><span data-stu-id="3115c-139">**Note:**  This field is only used for the SEPA pain.001.001.02 standard.</span></span>|  

    > [!IMPORTANT]  
    >  <span data-ttu-id="3115c-140">Voit viedä toimittajan maksut SEPA-standardin avulla, kun täytät **Maksun vientimuoto** -kentän **Pankkitilin kortti** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="3115c-140">To export vendor payments using the SEPA standard, you must fill the **Payment Export Format** field on the **Bank Account Card** page.</span></span>  

5.  <span data-ttu-id="3115c-141">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="3115c-141">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3115c-142">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3115c-142">See Also</span></span>  
 <span data-ttu-id="3115c-143">[Verkkopankkitoiminta Suomessa](electronic-banking-in-finland.md) </span><span class="sxs-lookup"><span data-stu-id="3115c-143">[Electronic Banking in Finland](electronic-banking-in-finland.md) </span></span>  
 <span data-ttu-id="3115c-144">[Maksutiedostojen luominen](how-to-generate-payment-files.md) </span><span class="sxs-lookup"><span data-stu-id="3115c-144">[Generate Payment Files](how-to-generate-payment-files.md) </span></span>  
 [<span data-ttu-id="3115c-145">Maksualennusten ohittaminen</span><span class="sxs-lookup"><span data-stu-id="3115c-145">Disregard Payment Discounts</span></span>](how-to-disregard-payment-discounts.md)
