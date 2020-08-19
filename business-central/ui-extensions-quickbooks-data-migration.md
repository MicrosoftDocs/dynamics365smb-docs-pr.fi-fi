---
title: QuickBooksin siirtolaajennus | Microsoft Docs
description: Tässä ohjeaiheessa käsitellään, miten laajennuksella tuodaan asiakkaita, toimittajia, nimikkeitä ja tilejä QuickBooks Desktopista Business Centraliin.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 07/23/2020
ms.author: edupont
ms.openlocfilehash: f603ce9391a3c971b719a1aae367a2f578166f94
ms.sourcegitcommit: 7b5c927ea9a59329daf1b60633b8290b552d6531
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/23/2020
ms.locfileid: "3617809"
---
# <a name="the-quickbooks-data-migration-extension"></a><span data-ttu-id="1cdcf-103">QuickBooks-tietojen siirtolaajennus</span><span class="sxs-lookup"><span data-stu-id="1cdcf-103">The QuickBooks Data Migration Extension</span></span>

<span data-ttu-id="1cdcf-104">Tämän laajennuksen avulla asiakkaat, toimittajat, nimikkeet ja tilit on helppo siirtää QuickBooksista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1cdcf-105">Jos yrityksessä on käytössä QuickBooks, voit viedä tarpeelliset tiedot ja ladata ne sitten [!INCLUDE[d365fin](includes/d365fin_md.md)]iin avaamalla avustetun asennusoppaan.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="1cdcf-106">Lisätietoja on kohdassa [Tietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="1cdcf-106">For more information, see [Importing Business Data from Other Finance Systems](across-import-data-configuration-packages.md).</span></span>

## <a name="data-from-quickbooks-desktop"></a><span data-ttu-id="1cdcf-107">Tietoja QuickBooks Desktopista</span><span class="sxs-lookup"><span data-stu-id="1cdcf-107">Data from QuickBooks Desktop</span></span>

<span data-ttu-id="1cdcf-108">Voit tuoda seuraavat tiedot QuickBooks Onlinesta Business Centraliin:</span><span class="sxs-lookup"><span data-stu-id="1cdcf-108">You can import the following data from QuickBooks Online to Business Central:</span></span>

- <span data-ttu-id="1cdcf-109">Asiakkaat</span><span class="sxs-lookup"><span data-stu-id="1cdcf-109">Customers</span></span>  
- <span data-ttu-id="1cdcf-110">Toimittajat</span><span class="sxs-lookup"><span data-stu-id="1cdcf-110">Vendors</span></span>  
- <span data-ttu-id="1cdcf-111">Nimikkeet</span><span class="sxs-lookup"><span data-stu-id="1cdcf-111">Items</span></span>  
- <span data-ttu-id="1cdcf-112">Tilikartta</span><span class="sxs-lookup"><span data-stu-id="1cdcf-112">Chart of Accounts</span></span>  
- <span data-ttu-id="1cdcf-113">Pääkirjanpidon alkusaldotapahtuma</span><span class="sxs-lookup"><span data-stu-id="1cdcf-113">Beginning Balance transactions in General Ledger</span></span>  
- <span data-ttu-id="1cdcf-114">Varastonimikkeiden varastomäärä</span><span class="sxs-lookup"><span data-stu-id="1cdcf-114">On-hand Quantities for Inventory Items</span></span>  
- <span data-ttu-id="1cdcf-115">Asiakkaiden ja toimittajien avoimet asiakirjat, kuten laskut, hyvityslaskut ja maksut</span><span class="sxs-lookup"><span data-stu-id="1cdcf-115">Open documents for customers and vendors, such as invoices, credit memos and payments</span></span>  

<span data-ttu-id="1cdcf-116">Myynti- ja ostoasiakirjoissa vain täydet summat siirretään.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-116">We migrate only full amounts on sales and purchase documents.</span></span> <span data-ttu-id="1cdcf-117">Osittain maksettuja summia ei päivitetä.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-117">We do not update partially paid amounts.</span></span> <span data-ttu-id="1cdcf-118">Jos asiakas on esimerkiksi maksanut myyntilaskun 500 dollarista 300, siirrettävä summa on kuitenkin 500.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-118">For example, if a customer has paid 300 of a total of 500 dollars on a sales invoice, we migrate the full 500.</span></span> <span data-ttu-id="1cdcf-119">Jos olet vastaanottanut osittaisia maksuja, ne on päivitettävä manuaalisesti ennen tietojen siirtoa tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-119">If you have received partial payments, you must update these manually, either before or after you migrate data.</span></span> <span data-ttu-id="1cdcf-120">Avoimet tapahtumat on syytä kohdistaa ennen siirtoa, sillä se helpottaa toimintaa siirron jälkeen.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-120">We recommend that you apply outstanding transactions before you migrate, just to make things easier afterward.</span></span>

> [!NOTE]
> <span data-ttu-id="1cdcf-121">Osto- tai myyntitilauksia ei siirretä.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-121">We do not migrate purchase orders or sales orders.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="1cdcf-122">Ennen aloittamista</span><span class="sxs-lookup"><span data-stu-id="1cdcf-122">Before You Start</span></span>

<span data-ttu-id="1cdcf-123">Siirtoprosessiin olennaisesti kuuluva osa on määrittää tilit, joihin tapahtumat siirretään.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-123">An important part of the migration process is to specify the accounts to migrate transactions to.</span></span> <span data-ttu-id="1cdcf-124">Nämä yhdistämismääritykset on hyvä suunnitella ennen tietojen siirtoa.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-124">It's a good idea to plan this mapping before you migrate data.</span></span> <span data-ttu-id="1cdcf-125">Kyse on esimerkiksi tileistä, joille seuraavat tapahtumat kirjataan:</span><span class="sxs-lookup"><span data-stu-id="1cdcf-125">For example, the accounts where you post transactions for:</span></span>

- <span data-ttu-id="1cdcf-126">Nimikkeiden tai palvelujen myynti asiakkaille</span><span class="sxs-lookup"><span data-stu-id="1cdcf-126">The sale of items or services to customers</span></span>  
- <span data-ttu-id="1cdcf-127">Nimikkeiden tai palvelujen osto toimittajilta</span><span class="sxs-lookup"><span data-stu-id="1cdcf-127">The purchase of items or services from vendors</span></span>  
- <span data-ttu-id="1cdcf-128">Pääkirjanpidon oikaisut</span><span class="sxs-lookup"><span data-stu-id="1cdcf-128">Adjustments in the general ledger</span></span>  

<span data-ttu-id="1cdcf-129">Business Central edellyttää, että KP-tileille on määritetty tilinumerot.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-129">Business Central requires that general ledger accounts have account numbers assigned to them.</span></span> <span data-ttu-id="1cdcf-130">Varmista, että QuickBooks-tileille on määritetty tilinumerot.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-130">Make sure that account numbers are assigned to your accounts in QuickBooks.</span></span>
<span data-ttu-id="1cdcf-131">QuickBooksin tapahtumissa on verosummia, Business Centralissa on määritettävä veroalueen verotili ennen tapahtumien kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-131">If transactions in QuickBooks have tax amounts, you must set up a tax account for your tax jurisdictions in Business Central before you can post transactions.</span></span>

<span data-ttu-id="1cdcf-132">Tietojen saaminen QuickBooks Desktop -sovelluksesta edellyttää Microsoftin tietojen vientityökalun lataamista.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-132">In order to get your data out of the QuickBooks desktop application you will need to download the Microsoft Data Exporter Tool.</span></span>  <span data-ttu-id="1cdcf-133">Työkalun ohjeet ovat [!INCLUDE[d365fin](includes/d365fin_md.md)]in ohjatussa tietojen siirtotoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-133">The instructions for the tool are in the Data Migration Wizard in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1cdcf-134">Työkalu muodostaa yhteyden QuickBooks-sovellukseen ja vie soveltuvat tiedot .zip-tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-134">The tool will connect to your QuickBooks application and export the applicable data to a .zip file.</span></span>  

> [!NOTE]
> <span data-ttu-id="1cdcf-135">Tällä hetkellä tietojen vientityökalua voi käyttää vain QuickBooks 2017:n ja 2018:n kanssa.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-135">Currently the data exporter tool only works with QuickBooks 2017 and 2018.</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="1cdcf-136">QuickBooks-tietojen siirtolaajennuksen etsiminen</span><span class="sxs-lookup"><span data-stu-id="1cdcf-136">Finding the QuickBooks Data Migration Extension</span></span>

<span data-ttu-id="1cdcf-137">QuickBooks-tietojen siirtolaajennus on asennettu ja valmis käytettäväksi tietojen siirtoasetusten ohjatun määrityksen osana.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-137">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="1cdcf-138">Jos olet valmis aloittamaan käytön nyt ja olet vienyt tiedot QuickBooksista, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asetusten ohjattu määritys** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-138">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="1cdcf-139">Valitse **Siirrä liiketoimintatiedot** ja noudata oppaan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-139">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="what-do-i-do-after-i-migrate-data"></a><span data-ttu-id="1cdcf-140">Toimenpiteet tietojen siirtämisen jälkeen</span><span class="sxs-lookup"><span data-stu-id="1cdcf-140">What do I do after I migrate Data?</span></span>

<span data-ttu-id="1cdcf-141">Tietojen siirron jälkeen tapahtumien tila on Kirjaamaton, joten voit tarkastella niitä ja tehdä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-141">After you migrate data, transactions have the status Unposted, so you can review them and make adjustments.</span></span> <span data-ttu-id="1cdcf-142">Voit tarkastella tapahtumia siirtymällä sivulle, jossa ne yleensä ovat.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-142">To review the transactions, go to the page where you would normally find them.</span></span> <span data-ttu-id="1cdcf-143">Voit tarkastella kirjaamattomia myyntilaskuja esimerkiksi siirtymällä Myyntilaskut-sivulle.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-143">For example, to review unposted sales invoices, go to the Sales Invoices page.</span></span> <span data-ttu-id="1cdcf-144">Voit tarkastella maksupäiväkirjoja siirtymällä Maksupäiväkirjat-sivulle.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-144">To review payment journals, go to the Payment Journals page.</span></span>
<span data-ttu-id="1cdcf-145">Tietyt toimenpiteet kannattaa tehdä: Jos QuickBooks Onlinen tapahtumissa oli korotettuja ja alennettuja summia, nämä summat on lisättävä manuaalisesti liittyviin tapahtumiin Business Centralissa ennen niiden kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-145">There are a few things in particular that you should do: If the transactions in QuickBooks had markup or discount amounts, you must manually add the amounts to the related transactions in Business Central before you post them.</span></span>
<span data-ttu-id="1cdcf-146">Jos käytät arvolisäveroa (ALV:tä), liiketoiminnan kirjausryhmä ja tuotteen kirjausryhmä on ehkä lisättävä kirjausasetuksiin ALV-summien kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-146">If you are using value added tax (VAT), you may need to add a business posting group and a product posting group to the posting setup so that you can post VAT amounts.</span></span>
<span data-ttu-id="1cdcf-147">Tarkista pääkirjanpidon tilien alkusaldot.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-147">Verify the beginning balances for accounts in the general ledger.</span></span> <span data-ttu-id="1cdcf-148">QuickBooks ei tallenna kaikkien tilien ajankohtaisia saldoja, joten alkusaldoja on ehkä korjattava.</span><span class="sxs-lookup"><span data-stu-id="1cdcf-148">QuickBooks does not store the current balance for all accounts, so you might need to correct beginning balances.</span></span>

## <a name="see-also"></a><span data-ttu-id="1cdcf-149">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1cdcf-149">See Also</span></span>

[<span data-ttu-id="1cdcf-150">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="1cdcf-150">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="1cdcf-151">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="1cdcf-151">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  
