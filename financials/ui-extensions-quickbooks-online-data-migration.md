---
title: "QuickBooksin siirtolaajennuksen käyttäminen | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten laajennuksella siirretään asiakkaita, toimittajia, nimikkeitä ja tilejä QuickBooks Onlinesta Financialsiin."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 05/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: fe87a108d132ff25f0c93a51df58bb88fb12f421
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---

# <a name="the-quickbooks-online-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="d766b-103">Dynamics 365 for Financialsin QuickBooks Onlinen tietojen siirron laajennus</span><span class="sxs-lookup"><span data-stu-id="d766b-103">The QuickBooks Online Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="d766b-104">Tämä laajennus sisältää **tietojen siirron** asetusten ohjattuun määritykseen, joka auttaa siirtämään tärkeitä liiketoimintatietoja QuickBooks Onlinesta [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="d766b-104">This extension is included in the **Data Migration** assisted setup guide to help you migrate important business data from QuickBooks Online to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d766b-105">Tämä on kätevää esimerkiksi tilanteessa, jossa liiketoiminta kasvaa ja olet päättänyt päivittää liiketoiminnan hallintasovelluksen aloittamalla [!INCLUDE[d365fin](includes/d365fin_md.md)]in käytön.</span><span class="sxs-lookup"><span data-stu-id="d766b-105">For example, this is useful when your business is growing, and you've decided to upgrade your business management app by starting to use [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="what-data-can-i-import-from-quickbooks-online"></a><span data-ttu-id="d766b-106">QuickBooks Onlinesta siirrettävät tiedot</span><span class="sxs-lookup"><span data-stu-id="d766b-106">What data can I import from QuickBooks Online?</span></span>
<span data-ttu-id="d766b-107">QuickBooks Onlinesta voi tuoda seuraavat tiedot [!INCLUDE[d365fin](includes/d365fin_md.md)]iin:</span><span class="sxs-lookup"><span data-stu-id="d766b-107">You can import the following data from QuickBooks Online to [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

* <span data-ttu-id="d766b-108">Asiakkaat</span><span class="sxs-lookup"><span data-stu-id="d766b-108">Customers</span></span>
* <span data-ttu-id="d766b-109">Toimittajat</span><span class="sxs-lookup"><span data-stu-id="d766b-109">Vendors</span></span>
* <span data-ttu-id="d766b-110">Nimikkeet</span><span class="sxs-lookup"><span data-stu-id="d766b-110">Items</span></span>
* <span data-ttu-id="d766b-111">Tilikartta</span><span class="sxs-lookup"><span data-stu-id="d766b-111">Chart of accounts</span></span> 
* <span data-ttu-id="d766b-112">Pääkirjanpidon alkusaldotapahtuma</span><span class="sxs-lookup"><span data-stu-id="d766b-112">Beginning balance transaction in the general ledger</span></span>
* <span data-ttu-id="d766b-113">Varastonimikkeiden varastomäärä</span><span class="sxs-lookup"><span data-stu-id="d766b-113">On-hand quantities for inventory items</span></span>
* <span data-ttu-id="d766b-114">Asiakkaiden ja toimittajien avoimet asiakirjat, kuten laskut, hyvityslaskut ja maksut</span><span class="sxs-lookup"><span data-stu-id="d766b-114">Open documents for customers and vendors, such as invoices, credit memos, and payments</span></span>

<span data-ttu-id="d766b-115">Myynti- ja ostoasiakirjoissa vain täydet summat siirretään.</span><span class="sxs-lookup"><span data-stu-id="d766b-115">We migrate only full amounts on sales and purchase documents.</span></span> <span data-ttu-id="d766b-116">Osittain maksettuja summia ei päivitetä.</span><span class="sxs-lookup"><span data-stu-id="d766b-116">We do not update partially paid amounts.</span></span> <span data-ttu-id="d766b-117">Jos asiakas on esimerkiksi maksanut myyntilaskun 500 dollarista 300, siirrettävä summa on kuitenkin 500.</span><span class="sxs-lookup"><span data-stu-id="d766b-117">For example, if a customer has paid 300 of a total of 500 dollars on a sales invoice, we migrate the full 500.</span></span> <span data-ttu-id="d766b-118">Jos olet vastaanottanut osittaisia maksuja, ne on päivitettävä manuaalisesti ennen tietojen siirtoa tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="d766b-118">If you have received partial payments, you must update these manually, either before or after you migrate data.</span></span> <span data-ttu-id="d766b-119">Avoimet tapahtumat on syytä kohdistaa ennen siirtoa, sillä se helpottaa toimintaa siirron jälkeen.</span><span class="sxs-lookup"><span data-stu-id="d766b-119">We recommend that you apply outstanding transactions before you migrate, just to make things easier afterward.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d766b-120">Osto- tai myyntitilauksia ei siirretä.</span><span class="sxs-lookup"><span data-stu-id="d766b-120">We do not migrate purchase orders or sales orders.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="d766b-121">Ennen kuin aloitat</span><span class="sxs-lookup"><span data-stu-id="d766b-121">Before you start</span></span>
<span data-ttu-id="d766b-122">Siirtoprosessiin olennaisesti kuuluva osa on määrittää tilit, joihin tapahtumat siirretään.</span><span class="sxs-lookup"><span data-stu-id="d766b-122">An important part of the migration process is to specify the accounts to migrate transactions to.</span></span> <span data-ttu-id="d766b-123">Nämä yhdistämismääritykset on hyvä suunnitella ennen tietojen siirtoa.</span><span class="sxs-lookup"><span data-stu-id="d766b-123">It's a good idea to plan this mapping before you migrate data.</span></span> <span data-ttu-id="d766b-124">Kyse on esimerkiksi tileistä, joille seuraavat tapahtumat kirjataan:</span><span class="sxs-lookup"><span data-stu-id="d766b-124">For example, the accounts where you post transactions for:</span></span>  
  
* <span data-ttu-id="d766b-125">Nimikkeiden tai palvelujen myynti asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="d766b-125">The sale of items or services to customers.</span></span>
* <span data-ttu-id="d766b-126">Nimikkeiden tai palvelujen osto toimittajilta.</span><span class="sxs-lookup"><span data-stu-id="d766b-126">The purchase of items or services from vendors.</span></span>  
* <span data-ttu-id="d766b-127">Pääkirjanpidon oikaisut.</span><span class="sxs-lookup"><span data-stu-id="d766b-127">Adjustments in the general ledger.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="d766b-128"> edellyttää, että KP-tileille on määritetty tilinumerot.</span><span class="sxs-lookup"><span data-stu-id="d766b-128"> requires that general ledger accounts have account numbers assigned to them.</span></span> <span data-ttu-id="d766b-129">Varmista, että QuickBooks Online -tileille on määritetty tilinumerot.</span><span class="sxs-lookup"><span data-stu-id="d766b-129">Make sure that account numbers are assigned to your accounts in QuickBooks Online.</span></span>

<span data-ttu-id="d766b-130">QuickBooks Onlinen tapahtumissa on verosummia, [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on määritettävä veroalueen verotili ennen tapahtumien kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="d766b-130">If transactions in QuickBooks Online have tax amounts, you must set up a tax account for your tax jurisdictions in [!INCLUDE[d365fin](includes/d365fin_md.md)] before you can post transactions.</span></span>

## <a name="how-do-i-start-using-the-extension"></a><span data-ttu-id="d766b-131">Laajennuksen käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="d766b-131">How do I start using the extension?</span></span>
<span data-ttu-id="d766b-132">Aloittaminen on helppoa.</span><span class="sxs-lookup"><span data-stu-id="d766b-132">Getting started is easy.</span></span> <span data-ttu-id="d766b-133">Sinun tarvitsee vain suorittaa **tietojen siirron** asetusten ohjattu määritys.</span><span class="sxs-lookup"><span data-stu-id="d766b-133">All you need to do is run the **Data Migration** assisted setup guide.</span></span> <span data-ttu-id="d766b-134">Ohjeet:</span><span class="sxs-lookup"><span data-stu-id="d766b-134">Here's how:</span></span>

1. <span data-ttu-id="d766b-135">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asetusten ohjattu määritys** ja valitse **Siirrä liiketoimintatiedot**.</span><span class="sxs-lookup"><span data-stu-id="d766b-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose **Migrate business data**.</span></span>
2. <span data-ttu-id="d766b-136">Noudata asetusten ohjatun määrityksen ohjeita.</span><span class="sxs-lookup"><span data-stu-id="d766b-136">Follow the instructions on each step in the assisted setup guide.</span></span>

## <a name="what-do-i-do-after-i-migrate-data"></a><span data-ttu-id="d766b-137">Toimenpiteet tietojen siirtämisen jälkeen</span><span class="sxs-lookup"><span data-stu-id="d766b-137">What do I do after I migrate data?</span></span>
<span data-ttu-id="d766b-138">Tietojen siirron jälkeen tapahtumien tila on **Kirjaamaton**, joten voit tarkastella niitä ja tehdä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="d766b-138">After you migrate data, transactions have the status **Unposted**, so you can review them and make adjustments.</span></span> <span data-ttu-id="d766b-139">Voit tarkastella tapahtumia siirtymällä sivulle, jossa ne yleensä ovat.</span><span class="sxs-lookup"><span data-stu-id="d766b-139">To review the transactions, go to the page where you would normally find them.</span></span> <span data-ttu-id="d766b-140">Voit tarkastella kirjaamattomia myyntilaskuja esimerkiksi siirtymällä **Myyntilaskut**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="d766b-140">For example, to review unposted sales invoices, go to the **Sales Invoices** page.</span></span> <span data-ttu-id="d766b-141">Voit tarkastella maksupäiväkirjoja siirtymällä **Maksupäiväkirjat**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="d766b-141">To review payment journals, go to the **Payment Journals** page.</span></span>   

<span data-ttu-id="d766b-142">Tietyt toimenpiteet kannattaa tehdä:</span><span class="sxs-lookup"><span data-stu-id="d766b-142">There are a few things in particular that you should do:</span></span>

* <span data-ttu-id="d766b-143">Jos QuickBooks Onlinen tapahtumissa oli korotettuja ja alennettuja summia, nämä summat on lisättävä manuaalisesti liittyviin tapahtumiin [!INCLUDE[d365fin](includes/d365fin_md.md)]issa ennen niiden kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="d766b-143">If the transactions in QuickBooks Online had markup or discount amounts, you must manually add the amounts to the related transactions in [!INCLUDE[d365fin](includes/d365fin_md.md)] before you post them.</span></span>
* <span data-ttu-id="d766b-144">Jos käytät arvolisäveroa (ALV:tä), liiketoiminnan kirjausryhmä ja tuotteen kirjausryhmä on ehkä lisättävä kirjausasetuksiin ALV-summien kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="d766b-144">If you are using value added tax (VAT), you may need to add a business posting group and a product posting group to the posting setup so that you can post VAT amounts.</span></span>
* <span data-ttu-id="d766b-145">Tarkista pääkirjanpidon tilien alkusaldot.</span><span class="sxs-lookup"><span data-stu-id="d766b-145">Verify the beginning balances for accounts in the general ledger.</span></span> <span data-ttu-id="d766b-146">QuickBooks Online ei tallenna kaikkien tilien ajankohtaisia saldoja, joten alkusaldoja on ehkä korjattava.</span><span class="sxs-lookup"><span data-stu-id="d766b-146">QuickBooks Online does not store the current balance for all accounts, so you might need to correct beginning balances.</span></span>

## <a name="see-also"></a><span data-ttu-id="d766b-147">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d766b-147">See Also</span></span>
[<span data-ttu-id="d766b-148">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="d766b-148">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="d766b-149">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="d766b-149">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  

