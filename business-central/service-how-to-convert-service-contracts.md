---
title: Huoltosopimusten muuntaminen | Microsoft Docs
description: Koska ALV:n muutostyökalu ei voi muuntaa huoltosopimuksia, nämä sopimukset on muunnettava manuaalisesti. Tässä aiheessa kuvataan useita vaihtoehtoisia menetelmiä, joita voit käyttää palvelusopimuksen muuntamista varten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3da6d4144b1e35da864de7b69a425bb65800b2cb
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5770736"
---
# <a name="convert-service-contracts-that-include-vat-amounts"></a><span data-ttu-id="61071-104">ALV-summia sisältävien huoltosopimusten muuntaminen</span><span class="sxs-lookup"><span data-stu-id="61071-104">Convert Service Contracts that Include VAT Amounts</span></span>
<span data-ttu-id="61071-105">Koska ALV:n muutostyökalu ei voi muuntaa huoltosopimuksia, nämä sopimukset on muunnettava manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="61071-105">Because the VAT rate change tool cannot convert service contracts, these contracts must be converted manually.</span></span> <span data-ttu-id="61071-106">Tässä aiheessa kuvataan useita vaihtoehtoisia menetelmiä, joita voit käyttää palvelusopimuksen muuntamista varten.</span><span class="sxs-lookup"><span data-stu-id="61071-106">This topic describes several alternative methods that you can use for service contract conversion.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="61071-107">Tämä aihe tarjoaa korkeatasoisen työnkulun.</span><span class="sxs-lookup"><span data-stu-id="61071-107">This topic provides a high-level workflow.</span></span>  

 <span data-ttu-id="61071-108">Seuraavassa ohjeessa neuvotaan, miten korjataan etukäteen maksetun huoltosopimuksen lasku, joka on luotu vuoden etukäteen.</span><span class="sxs-lookup"><span data-stu-id="61071-108">The following procedure describes how to correct an invoice for a prepaid service contract that has been created a year in advance.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="61071-109">Määritä tässä esimerkissä käsittelypäivämääräksi 01.01.2017.</span><span class="sxs-lookup"><span data-stu-id="61071-109">For this example, you must change your work date to 01.01.2017.</span></span>  

### <a name="to-correct-an-invoice-for-a-prepaid-service-contract"></a><span data-ttu-id="61071-110">Korjaa ennakkoon maksetun huoltosopimuksen lasku</span><span class="sxs-lookup"><span data-stu-id="61071-110">To correct an invoice for a prepaid service contract</span></span>  
1. <span data-ttu-id="61071-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sopimuksen hallinta** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="61071-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Contract Management**, and then choose the related link.</span></span>  
2. <span data-ttu-id="61071-112">Valitse **Luettelot** -kohdan alta **Huoltosopimukset**.</span><span class="sxs-lookup"><span data-stu-id="61071-112">Under **Lists**, choose **Service Contracts**.</span></span>  
3. <span data-ttu-id="61071-113">Luo uusi ennakkoon maksettu huoltosopimus.</span><span class="sxs-lookup"><span data-stu-id="61071-113">Create a new prepaid service contract.</span></span> <span data-ttu-id="61071-114">Anna aloituspäiväksi **01.01.2017** ja laskukausi asiakkaalle **20000**.</span><span class="sxs-lookup"><span data-stu-id="61071-114">Enter a start date of **01.01.2017** and an invoice period year for customer **20000**.</span></span>  
4. <span data-ttu-id="61071-115">Voit allekirjoittaa sopimuksen valitsemalla **Allekirjoita sopimus** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="61071-115">To sign the contract, choose the **Sign Contract** action.</span></span>  
5. <span data-ttu-id="61071-116">Huoltolaskun luominen:</span><span class="sxs-lookup"><span data-stu-id="61071-116">Create a service invoice.</span></span>
6. <span data-ttu-id="61071-117">Lasku on merkitty kirjaamattomaksi huoltolaskuksi.</span><span class="sxs-lookup"><span data-stu-id="61071-117">The invoice is listed as an unposted service invoice.</span></span> <span data-ttu-id="61071-118">Tarkastele huoltolaskua valitsemalla **Huolto**-toiminto, valitse **Sopimuksen hallinta** -toiminto ja valitse sitten **Huoltolaskut**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="61071-118">To view the service invoice, choose the **Service** action, choose the **Contract Management** action, and then choose the **Service Invoices** action.</span></span>  
7. <span data-ttu-id="61071-119">Kirjaa huoltolasku.</span><span class="sxs-lookup"><span data-stu-id="61071-119">Post the service invoice.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="61071-120">Älä muuta kirjaamatonta huoltolaskua.</span><span class="sxs-lookup"><span data-stu-id="61071-120">Do not change the unposted service invoice.</span></span> <span data-ttu-id="61071-121">Koska palvelutapahtumat luodaan laskun luonnin yhteydessä, kirjaamattoman laskun muutos ei muuta jo luotuja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="61071-121">Since the service ledger entries are created when the invoice is created, a change in the unposted invoice will not change the already created service ledger entries.</span></span> <span data-ttu-id="61071-122">ALV-tapahtumat luodaan laskun kirjauksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="61071-122">However, the VAT entries are created when the invoice is posted.</span></span> <span data-ttu-id="61071-123">Tämän avulla voi muuttaa yleisiä tuotteen kirjausryhmiä ja GSP-tuotteen kirjausryhmiä kirjaamattomassa huoltolaskussa. </span><span class="sxs-lookup"><span data-stu-id="61071-123">This lets you change the general product posting group and the GSP product posting group on the unposted service invoice.</span></span>  

### <a name="to-create-a-credit-memo-for-vat-difference"></a><span data-ttu-id="61071-124">Luo ALV-erotuksen hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="61071-124">To create a credit memo for VAT difference</span></span>  
<span data-ttu-id="61071-125">Seuraavassa ohjeessa neuvotaan, miten luodaan hyvityslasku, joka sisältää vain jo laskutetun, **01.07.2017** alkaneen kauden ALV-erotus.</span><span class="sxs-lookup"><span data-stu-id="61071-125">The following procedure describes how to create a credit memo that only includes the VAT difference for the already invoiced period starting on **01.07.2017**.</span></span> <span data-ttu-id="61071-126">Tässä esimerkissä ALV-summa kirjataan vain varainhoidon moduulin, ei palveluiden hallinta-moduuliin.</span><span class="sxs-lookup"><span data-stu-id="61071-126">In this example, the VAT amount is only posted to the Financial Management module, not to the Service Management module.</span></span> <span data-ttu-id="61071-127">Huoltotapahtumaan linkitettyjä ALV-tapahtumia ei voi korjata.</span><span class="sxs-lookup"><span data-stu-id="61071-127">The VAT entries that are linked to the service ledger entry will not be corrected.</span></span>  

1. <span data-ttu-id="61071-128">Luo uusi pääkirjanpidon tili ALV-erolle.</span><span class="sxs-lookup"><span data-stu-id="61071-128">Create a new general ledger account for the VAT difference.</span></span> <span data-ttu-id="61071-129">Tätä tiliä käytetään ALV-korjausten suoraan kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="61071-129">This account will be used for direct posting of the VAT correction.</span></span>  
2. <span data-ttu-id="61071-130">Lisää uusi rivi ALV-kirjausasetuksiin.</span><span class="sxs-lookup"><span data-stu-id="61071-130">Add a new line to the VAT posting setup.</span></span>  

### <a name="to-create-contract-expiration-dates-in-contract-lines"></a><span data-ttu-id="61071-131">Luo sopimuksen vanhentumispäivämäärät sopimusriveille</span><span class="sxs-lookup"><span data-stu-id="61071-131">To create contract expiration dates in contract lines</span></span>  
<span data-ttu-id="61071-132">Seuraavassa ohjeessa neuvotaan, miten luodaan uusia sopimuksia käyttämällä sopimuksen vanhentumispäiviä huoltosopimusriveillä.</span><span class="sxs-lookup"><span data-stu-id="61071-132">The following procedure describes how to create new contracts by working with contract expiration dates in service contract lines.</span></span>  

1. <span data-ttu-id="61071-133">Määritä **Huoltosopimus**-sivulla sopimuksen vanhenemispäivämääräksi **30.06.2017**.</span><span class="sxs-lookup"><span data-stu-id="61071-133">On the **Service Contract** page, set the contract expiration date to **30.06.2017**.</span></span>  
2. <span data-ttu-id="61071-134">Valitse **Luo hyvityslasku** -toiminto, niin hyvityslasku luodaan automaattisesti aikavälille heinäkuusta 2017 joulukuuhun 2017.</span><span class="sxs-lookup"><span data-stu-id="61071-134">Choose the **Create Credit Memo** action to automatically create a credit memo for July 2017 to December 2017.</span></span>  
3. <span data-ttu-id="61071-135">Koska sopimus on vanhentunut, sinun on luotava uusi sopimus uudella ALV-arvolla ajalle 1. heinäkuuta 2017 ja 31. joulukuuta 2017.</span><span class="sxs-lookup"><span data-stu-id="61071-135">Because the contract has expired, you need to create a new contract for the period with the new VAT rate for July 1, 2017 to December 31, 2017.</span></span>  

### <a name="to-create-a-new-credit-memo"></a><span data-ttu-id="61071-136">Luo uusi hyvityslasku.</span><span class="sxs-lookup"><span data-stu-id="61071-136">To create a new credit memo</span></span>  
<span data-ttu-id="61071-137">Seuraavassa ohjeessa neuvotaan, miten luodaan uusi hyvityslasku käyttäen **Hae enn. maksetut sop. tapahtumat** -erä-ajoa.</span><span class="sxs-lookup"><span data-stu-id="61071-137">The following procedure describes how to create a new credit memo using the **Get Prepaid Contract Entries** batch job.</span></span> <span data-ttu-id="61071-138">Vuoden 2017 tammikuun ja kesäkuun väliset tapahtumat, joita et halua korjata, poistetaan.</span><span class="sxs-lookup"><span data-stu-id="61071-138">Entries that you do not want to correct from January 2017 to June 2017 will be deleted.</span></span>  

1. <span data-ttu-id="61071-139">Aja ALV-kannan muutostyökalu 1. heinäkuuta 2017.</span><span class="sxs-lookup"><span data-stu-id="61071-139">Run the VAT rate change tool on July 1, 2017.</span></span> <span data-ttu-id="61071-140">Yleinen tuotteen kirjausryhmä tai ALV-tuotteen kirjausryhmä muutetaan.</span><span class="sxs-lookup"><span data-stu-id="61071-140">The general product posting group or the VAT product posting group is changed.</span></span> <span data-ttu-id="61071-141">Lisätietoja on kohdassa [Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md).</span><span class="sxs-lookup"><span data-stu-id="61071-141">For more information, see [Work with VAT on Sales and Purchases](finance-work-with-vat.md).</span></span>  
2. <span data-ttu-id="61071-142">ALV-muutostyökalun suorittamisen jälkeen, kirjoita huoltosopimuksen vanhenemispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="61071-142">After running the VAT rate change tool, enter a contract expiration date for the service contract.</span></span> <span data-ttu-id="61071-143">Nyt voit poistaa huoltosopimuksen rivin ja luoda uuden rivin, joka on samanlainen kuin vanha.</span><span class="sxs-lookup"><span data-stu-id="61071-143">You can now delete the service contract line and create a new line that is identical to the old one.</span></span>  
3. <span data-ttu-id="61071-144">Luo uusi lasku kaudelle Tammikuu 2017 - Joulukuu 2012 uudella ALV-prosentilla.</span><span class="sxs-lookup"><span data-stu-id="61071-144">Create a new invoice for the period of January 2017 to December 2012 using the new VAT rate.</span></span>  
4. <span data-ttu-id="61071-145">Luo toinen hyvityslasku **Huollon hyvityslaskut** -sivulla valitsemalla **Uusi**-toiminto luodaksesi uuden huollon hyvityslaskun.</span><span class="sxs-lookup"><span data-stu-id="61071-145">To create another credit memo, on the **Service Credit Memos** page, choose the **New** action to create a new service credit memo.</span></span>  
5. <span data-ttu-id="61071-146">Valitse **Hae enn. maksetut sop.tapaht** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="61071-146">Choose the **Get Prepaid Contract Entries** action.</span></span>  
6. <span data-ttu-id="61071-147">Kun muuntaminen on valmis, ALV- ja huoltotapahtumasyötteet ovat oikeat.</span><span class="sxs-lookup"><span data-stu-id="61071-147">After the conversion is complete, VAT and service ledger entries will be correct.</span></span>  

## <a name="see-also"></a><span data-ttu-id="61071-148">Katso myös</span><span class="sxs-lookup"><span data-stu-id="61071-148">See Also</span></span>  
[<span data-ttu-id="61071-149">Huoltosopimusten ja huoltosopimustarjousten käyttäminen</span><span class="sxs-lookup"><span data-stu-id="61071-149">Work with Service Contracts and Service Contract Quotes</span></span>](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[<span data-ttu-id="61071-150">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="61071-150">Finance</span></span>](finance.md)  
[<span data-ttu-id="61071-151">ALV:n raportointi veroviranomaisille</span><span class="sxs-lookup"><span data-stu-id="61071-151">Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)  
[<span data-ttu-id="61071-152">Myynnin ja ostojen ALV:n käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="61071-152">Work with VAT on Sales and Purchases</span></span>](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]