---
title: Verkkopankkitoiminta Suomessa
description: Business Central -sovelluksen verkkopankkitoimintojen avulla voi käsitellä elektronisia asiakas- ja toimittajamaksuja. Toiminto tukee verkkopankkimaksujen siirron kotimaan maksuja (LM03) ja ulkomaan maksuja (LUM2). Verkkopankkimaksujen vientiä tai tuontia varten on ensin määritettävä pankin viitetiedostot, joissa määritetään maksutiedostojen käsittelytapa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: ad1ddaa437a685a541a7a1ef628612d564842b64
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778377"
---
# <a name="electronic-banking-in-finland"></a><span data-ttu-id="cb3f6-105">Verkkopankkitoiminta Suomessa</span><span class="sxs-lookup"><span data-stu-id="cb3f6-105">Electronic Banking in Finland</span></span>
<span data-ttu-id="cb3f6-106">[!INCLUDE[d365fin](../../includes/d365fin_md.md)] -ohjelman verkkopankkitoimintojen avulla voi käsitellä elektronisia asiakas- ja toimittajamaksuja.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-106">The [!INCLUDE[d365fin](../../includes/d365fin_md.md)] electronic banking feature allows you to process electronic customer and vendor payments.</span></span> <span data-ttu-id="cb3f6-107">Toiminto tukee verkkopankkimaksujen siirron kotimaan maksuja (LM03) ja ulkomaan maksuja (LUM2).</span><span class="sxs-lookup"><span data-stu-id="cb3f6-107">This feature supports domestic payments (LM03) and foreign payments (LUM2) for transferring electronic bank payments.</span></span> <span data-ttu-id="cb3f6-108">Verkkopankkimaksujen vientiä tai tuontia varten on ensin määritettävä pankin viitetiedostot, joissa määritetään maksutiedostojen käsittelytapa.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-108">To export or import electronic payments, you must first set up bank reference files to determine how payment files are processed.</span></span>  

## <a name="customer-payments"></a><span data-ttu-id="cb3f6-109">Asiakasmaksut</span><span class="sxs-lookup"><span data-stu-id="cb3f6-109">Customer Payments</span></span>  
<span data-ttu-id="cb3f6-110">Kotimaan asiakasmaksut voidaan tuoda pankista ja linkittää liittyvään myyntisaatavatapahtumaan viitenumeron avulla.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-110">Domestic customer payments can be imported from the bank and linked to the associated accounts receivable entry with a reference number.</span></span> <span data-ttu-id="cb3f6-111">Tämä automaattinen toiminto mahdollistaa saapuvien maksujen linkittämisen suoraan avoimiin myyntisaataviin ilman manuaalisen käsittelyn aiheuttamaa viivettä.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-111">This type of automation enables incoming payments to be linked directly to open receivables without a delay in manual processing.</span></span> <span data-ttu-id="cb3f6-112">Seuraavissa vaiheissa kuvataan, miten asiakasmaksut tuodaan pankista tiedostoon ja miten nämä maksut linkitetään laskuihin viitenumeroiden avulla.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-112">The following steps explain how to import customer payments into a file from the bank and how to link these payments to invoices through their reference numbers.</span></span>  

- <span data-ttu-id="cb3f6-113">Luo myyntilasku ja liitä laskuun yksilöivä viitenumero.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-113">Create a sales invoice and assign a unique reference number to the invoice.</span></span> <span data-ttu-id="cb3f6-114">Asiakas käyttää tätä viitenumeroa maksaessaan laskun.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-114">This reference number will be used by the customer when paying the invoice.</span></span>  

- <span data-ttu-id="cb3f6-115">Tuo asiakasmaksut sisältävät maksutiedostot kassapäiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-115">Import the payment files that contain customer payments into the cash receipt journal.</span></span> <span data-ttu-id="cb3f6-116">Nämä tiedostot sisältävät pankilta saadut viitenumerot.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-116">These files contain the reference numbers received from the bank.</span></span> <span data-ttu-id="cb3f6-117">Maksut linkitetään myyntisaatavatapahtumaan viitenumeroiden avulla.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-117">The payments are linked to the accounts receivable entry through their reference numbers.</span></span>  

- <span data-ttu-id="cb3f6-118">Kirjaa tiedot kassapäiväkirjaan ja sulje avoimet myyntisaatavatapahtumat tiedoston kohdistettujen maksujen avulla.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-118">Post the cash receipt journal and close the open accounts receivable entries with the applied payments from the file.</span></span>  

## <a name="reference-number"></a><span data-ttu-id="cb3f6-119">Viitenumero</span><span class="sxs-lookup"><span data-stu-id="cb3f6-119">Reference Number</span></span>  
<span data-ttu-id="cb3f6-120">Viitenumero luodaan automaattisesti, kun lasku kirjataan tai tilaus kirjataan laskutettavaksi.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-120">A reference number is automatically created when an invoice is posted or when an order is posted for invoicing.</span></span> <span data-ttu-id="cb3f6-121">Myyntipäiväkirjan tapahtuman viitenumeron voi kuitenkin antaa myös manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-121">However, you can enter a reference number manually on a sales journal transaction.</span></span> <span data-ttu-id="cb3f6-122">Tämä viitenumero ei perustu **Myyntien ja myyntisaamisten asetukset** -sivun viitenumeroasetuksiin.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-122">This reference number is not based on the reference number options on the **Sales & Receivables Setup** page.</span></span> <span data-ttu-id="cb3f6-123">Jos syötät myyntipäiväkirjaan viitenumeron, vain viitenumeron oikeellisuus tarkistetaan.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-123">If you enter a reference number for the sales journal, only the validity of the reference number is checked.</span></span>  

## <a name="vendor-payments"></a><span data-ttu-id="cb3f6-124">Toimittajamaksut</span><span class="sxs-lookup"><span data-stu-id="cb3f6-124">Vendor Payments</span></span>  
<span data-ttu-id="cb3f6-125">Voit lähettää toimittajille verkkopankkimaksuja viemällä kotimaan tai ulkomaan toimittajamaksut pankille lähetettävään siirtotiedostoon.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-125">To send electronic bank payments to vendors, you can export domestic or foreign vendor payments into a transfer file that can be sent to the bank.</span></span> <span data-ttu-id="cb3f6-126">Seuraavissa vaiheissa kuvataan, miten toimittajamaksut viedään.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-126">The following steps show how to export vendor payments.</span></span>  

- <span data-ttu-id="cb3f6-127">Valitse **Lähetettävät pankkimaksut** -sivulla toimittajat, joille maksutiedostot luodaan.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-127">Use the **Bank Payments to Send** page to select the vendors for which you want to create payment files.</span></span>  
- <span data-ttu-id="cb3f6-128">Syötä maksutiedot jokaiselle maksupäiväkirjan tapahtumalle tai käytä **Ehdota toimittajamaksuja** -toimintoa, joka luo ehdotetut maksut.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-128">Enter payment information for each transaction in the payment journal or use **Suggest Vendor Payments** to create suggested payments.</span></span>  
- <span data-ttu-id="cb3f6-129">Luo ja esikatsele maksuraportti.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-129">Generate and preview the payment report.</span></span>  
- <span data-ttu-id="cb3f6-130">Luo siirtotiedosto kotimaan tai ulkomaan toimittajamaksuille.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-130">Create a transfer file for domestic or foreign vendor payments.</span></span>  
- <span data-ttu-id="cb3f6-131">Lähetä maksun siirtotiedosto pankkiin.</span><span class="sxs-lookup"><span data-stu-id="cb3f6-131">Send the payment transfer file to the bank.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cb3f6-132">Katso myös</span><span class="sxs-lookup"><span data-stu-id="cb3f6-132">See Also</span></span>  
 <span data-ttu-id="cb3f6-133">[Suomen paikalliset toiminnot](finland-local-functionality.md) </span><span class="sxs-lookup"><span data-stu-id="cb3f6-133">[Finland Local Functionality](finland-local-functionality.md) </span></span>  
 <span data-ttu-id="cb3f6-134">[Pankin viitetiedostojen määrittäminen](how-to-set-up-bank-reference-files.md) </span><span class="sxs-lookup"><span data-stu-id="cb3f6-134">[Set Up Bank Reference Files](how-to-set-up-bank-reference-files.md) </span></span>  
 <span data-ttu-id="cb3f6-135">[Maksutiedostojen luominen](how-to-generate-payment-files.md) </span><span class="sxs-lookup"><span data-stu-id="cb3f6-135">[Generate Payment Files](how-to-generate-payment-files.md) </span></span>  
 [<span data-ttu-id="cb3f6-136">Maksualennusten ohittaminen</span><span class="sxs-lookup"><span data-stu-id="cb3f6-136">Disregard Payment Discounts</span></span>](how-to-disregard-payment-discounts.md)   
