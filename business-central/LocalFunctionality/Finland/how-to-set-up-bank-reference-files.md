---
title: "Pankin viitetiedostojen määrittäminen"
description: "Elektronisten maksujen käsittelyä varten on ensin määritettävä pankin viitetiedostot, joiden avulla määritetään, miten maksutiedot tuodaan tai viedään."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 5c288ba2235e798450c4ca8841a5201f9270e73a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-bank-reference-files"></a><span data-ttu-id="ca6d8-103">Pankin viitetiedostojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ca6d8-103">Set Up Bank Reference Files</span></span>
<span data-ttu-id="ca6d8-104">Elektronisten maksujen käsittelyä varten on ensin määritettävä pankin viitetiedostot, joiden avulla määritetään, miten maksutiedot tuodaan tai viedään.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-104">To process electronic payments, you must first set up bank reference files to determine how payment data should be imported or exported.</span></span>  

## <a name="to-set-up-a-bank-reference-file"></a><span data-ttu-id="ca6d8-105">Pankin viitetiedoston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ca6d8-105">To set up a bank reference file</span></span>  

1.  <span data-ttu-id="ca6d8-106">Valitse ![Etsi sivu tai raportti -kuvake](../../media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Pankin viitetiedoston asetukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-106">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Reference File Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ca6d8-107">Täytä **Yleinen**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-107">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ca6d8-108">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ca6d8-108">Field</span></span>|<span data-ttu-id="ca6d8-109">Description</span><span class="sxs-lookup"><span data-stu-id="ca6d8-109">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="ca6d8-110">**Nro**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-110">**No.**</span></span>|<span data-ttu-id="ca6d8-111">Määrittää pankkitilin koodin.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-111">Specifies a bank account code.</span></span>|  
    |<span data-ttu-id="ca6d8-112">**Vie viitemaksut**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-112">**Export Reference Payments**</span></span>|<span data-ttu-id="ca6d8-113">Anna vietävän maksutiedoston koko polku.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-113">Enter the full path of the payment file to export.</span></span>|  
    |<span data-ttu-id="ca6d8-114">**Tuo viitemaksut**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-114">**Import Reference Payments**</span></span>|<span data-ttu-id="ca6d8-115">Anna tuotavan maksutiedoston koko polku.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-115">Enter the full path of the payment file to import.</span></span>|  
    |<span data-ttu-id="ca6d8-116">**Valuutan vaihtokurssitiedosto**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-116">**Currency Exchange Rate File**</span></span>|<span data-ttu-id="ca6d8-117">Anna valuutan vaihtokurssitiedoston koko polku.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-117">Enter the full path of the currency exchange rate file.</span></span>|  
    |<span data-ttu-id="ca6d8-118">**Kohdistettujen hyvityslaskujen tiedot**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-118">**Inform. of Appl. Cr. Memos**</span></span>|<span data-ttu-id="ca6d8-119">Kun valitset tämän, laskuihin kohdistetut hyvitykset näkyvät maksun vastaanottajan tiliotteessa.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-119">Select to display credits applied to invoices on the payment recipient's account statement.</span></span>|  

3.  <span data-ttu-id="ca6d8-120">Täytä **Ulkomaan maksut** -pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-120">On the **Foreign Payments** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ca6d8-121">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ca6d8-121">Field</span></span>|<span data-ttu-id="ca6d8-122">Description</span><span class="sxs-lookup"><span data-stu-id="ca6d8-122">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="ca6d8-123">**Vie ulkomaan maksut**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-123">**Export Foreign Payments**</span></span>|<span data-ttu-id="ca6d8-124">Anna ulkomaan pankkeihin vietävän maksutiedoston koko polku.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-124">Enter the full path of the payment file to export to foreign banks.</span></span>|  
    |<span data-ttu-id="ca6d8-125">**Eräpäivän käsittely**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-125">**Due Date Handling**</span></span>|<span data-ttu-id="ca6d8-126">Määritä, miten eräpäivän käsittelyä käytetään ulkomaan maksuissa.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-126">Select how due date processing should be applied to foreign payments.</span></span><br /><br /> <span data-ttu-id="ca6d8-127">**Erä** – Kaikki tiedoston maksut saavat saman maksupäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-127">**Batch** – All payments in the file receive the same payment date.</span></span><br /><br /> <span data-ttu-id="ca6d8-128">-tai-</span><span class="sxs-lookup"><span data-stu-id="ca6d8-128">–or–</span></span><br /><br /> <span data-ttu-id="ca6d8-129">**Tapahtuma** – Jokainen tiedoston maksu saa tapahtumakohtaisen maksupäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-129">**Transaction** – Each payment in the file receives a transaction-specific payment date.</span></span> <span data-ttu-id="ca6d8-130">Kysy pankista lisätietoja tämän asetuksen käytöstä.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-130">Contact your bank to determine whether this setting should be used.</span></span>|  
    |<span data-ttu-id="ca6d8-131">**Palvelumaksun oletuskoodi**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-131">**Default Service Fee Code**</span></span>|<span data-ttu-id="ca6d8-132">Valitse palvelumaksun oletuskoodi ulkomaan pankkeja varten.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-132">Select a default service fee code for foreign banks.</span></span>|  
    |<span data-ttu-id="ca6d8-133">**Oletusmaksutapa**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-133">**Default Payment Method**</span></span>|<span data-ttu-id="ca6d8-134">Valitse oletusmaksutapa ulkomaan pankkeja varten.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-134">Select a default payment method for foreign payments.</span></span>|  
    |<span data-ttu-id="ca6d8-135">**Vaihtokurssin sopimusnro**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-135">**Exchange Rate Contract No.**</span></span>|<span data-ttu-id="ca6d8-136">Anna vaihtokurssin sopimusnumero.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-136">Enter the exchange rate contract number.</span></span>|  
    |<span data-ttu-id="ca6d8-137">**Salli ulkomaan maksujen yhdistäminen**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-137">**Allow Comb. Foreign Pmts.**</span></span>|<span data-ttu-id="ca6d8-138">Yhdistä kaikki yhdelle vastaanottajalle tietyn päivän aikana samalta pankkitililtä tehdyt ulkomaan maksut.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-138">Select to combine all foreign payments made to one recipient in one day from the same bank account.</span></span>|  

4.  <span data-ttu-id="ca6d8-139">Täytä **SEPA**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-139">On the **SEPA** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ca6d8-140">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ca6d8-140">Field</span></span>|<span data-ttu-id="ca6d8-141">Description</span><span class="sxs-lookup"><span data-stu-id="ca6d8-141">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="ca6d8-142">**Pankin tunnus**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-142">**Bank Party ID**</span></span>|<span data-ttu-id="ca6d8-143">Anna SEPA-pankin tunnus.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-143">Enter a SEPA bank party ID.</span></span> <span data-ttu-id="ca6d8-144">**Huomautus:** Tätä kenttää käytetään vain SEPA-standardissa pain.001.001.02.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-144">**Note:**  This field is only used for the SEPA pain.001.001.02 standard.</span></span>|  
    |<span data-ttu-id="ca6d8-145">**Tiedostonimi**</span><span class="sxs-lookup"><span data-stu-id="ca6d8-145">**File Name**</span></span>|<span data-ttu-id="ca6d8-146">Anna SEPA-maksutiedoston koko polku.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-146">Enter the full path of the SEPA payment file.</span></span> <span data-ttu-id="ca6d8-147">**Huomautus:** Tätä kenttää käytetään vain SEPA-standardissa pain.001.001.02.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-147">**Note:**  This field is only used for the SEPA pain.001.001.02 standard.</span></span>|  

    > [!IMPORTANT]  
    >  <span data-ttu-id="ca6d8-148">Voit viedä toimittajan maksut SEPA-standardin avulla, kun täytät **Maksun vientimuoto** -kentän **Pankkitilin kortti** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-148">To export vendor payments using the SEPA standard, you must fill the **Payment Export Format** field in the **Bank Account Card** window.</span></span>  

5.  <span data-ttu-id="ca6d8-149">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="ca6d8-149">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ca6d8-150">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ca6d8-150">See Also</span></span>  
 <span data-ttu-id="ca6d8-151">[Verkkopankkitoiminta Suomessa](electronic-banking-in-finland.md) </span><span class="sxs-lookup"><span data-stu-id="ca6d8-151">[Electronic Banking in Finland](electronic-banking-in-finland.md) </span></span>  
 <span data-ttu-id="ca6d8-152">[Maksutiedostojen luominen](how-to-generate-payment-files.md) </span><span class="sxs-lookup"><span data-stu-id="ca6d8-152">[Generate Payment Files](how-to-generate-payment-files.md) </span></span>  
 [<span data-ttu-id="ca6d8-153">Maksualennusten ohittaminen</span><span class="sxs-lookup"><span data-stu-id="ca6d8-153">Disregard Payment Discounts</span></span>](how-to-disregard-payment-discounts.md)

