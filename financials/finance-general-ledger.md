---
title: "Tietoja pääkirjanpidosta ja aitoustodistuksesta| Microsoft Docs"
description: "Tämä artikkeli sisältää tietoja pääkirjanpidosta, tilikartasta ja tililuokista."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 06becfd7e54803fea925e8364719576bef0a8bab
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="f0681-103">Pääkirjanpito ja aitoustodistus</span><span class="sxs-lookup"><span data-stu-id="f0681-103">Understanding the General Ledger and the COA</span></span>
<span data-ttu-id="f0681-104">Pääkirjanpito sisältää taloustiedot ja tilikartta näyttää tilit, joihin kaikki pääkirjanpidon tapahtumat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="f0681-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f0681-105"> sisältää tilikartan, joka on valmis tukemaan liiketoimintaasi.</span><span class="sxs-lookup"><span data-stu-id="f0681-105"> includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="f0681-106">Pääkirjanpidon asetukset ja yleiset kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="f0681-106">General Ledger Setup and General Posting Setup</span></span>
<span data-ttu-id="f0681-107">Pääkirjanpidon asetukset ovat keskeisiä rahoitusprosesseja, sillä niillä määritetään tietojen kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="f0681-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="f0681-108">**Pääkirjanpidon asetukset** -ikkunassa määritetään, miten esimerkiksi seuraavat yrityksen kirjanpitoasiat:</span><span class="sxs-lookup"><span data-stu-id="f0681-108">In the **General Ledger Setup** window, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="f0681-109">Laskun pyöristystiliedot</span><span class="sxs-lookup"><span data-stu-id="f0681-109">Invoice rounding details</span></span>  
* <span data-ttu-id="f0681-110">Osoitteen muodot</span><span class="sxs-lookup"><span data-stu-id="f0681-110">Address formats</span></span>  
* <span data-ttu-id="f0681-111">Talousraportointi</span><span class="sxs-lookup"><span data-stu-id="f0681-111">Financial reporting</span></span>  

<span data-ttu-id="f0681-112">Samaan tapaan määritetään **Yleiset kirjausasetukset** -ikkunassa, miten liiketoiminnan ja tuotteen yleisten kirjausryhmien yhdistelmät määritetään.</span><span class="sxs-lookup"><span data-stu-id="f0681-112">Similarly, in the **General Posting Setup** window, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="f0681-113">Kirjausryhmät yhdistävät objektit, kuten asiakkaat, toimittajat, nimikkeet, resurssit sekä myynti- ja ostoasiakirjoja pääkirjanpidon tileille.</span><span class="sxs-lookup"><span data-stu-id="f0681-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="f0681-114">Jokaiselle liiketoiminnan kirjausryhmän ja tuotteen kirjausryhmän yhdistelmälle täytetään rivi.</span><span class="sxs-lookup"><span data-stu-id="f0681-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="f0681-115">Lisätietoja on kohdassa [Kirjausryhmien asetukset](finance-posting-groups.md)</span><span class="sxs-lookup"><span data-stu-id="f0681-115">For more information, see [Posting Group Setups](finance-posting-groups.md)</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="f0681-116">Tilikartta</span><span class="sxs-lookup"><span data-stu-id="f0681-116">The Chart of Accounts</span></span>
<span data-ttu-id="f0681-117">Kaikki pääkirjanpidon tilit näkyvät tilikartassa.</span><span class="sxs-lookup"><span data-stu-id="f0681-117">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="f0681-118">Tilikartassa voi tehdä esimerkiksi seuraavia toimintoja:</span><span class="sxs-lookup"><span data-stu-id="f0681-118">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="f0681-119">Voit tarkastella pääkirjanpitotapahtumat- ja saldot näyttäviä raportteja.</span><span class="sxs-lookup"><span data-stu-id="f0681-119">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="f0681-120">Voit sulkea tuloslaskelman.</span><span class="sxs-lookup"><span data-stu-id="f0681-120">Close your income statement.</span></span>  
* <span data-ttu-id="f0681-121">Voita avata KP-tilikortin asetusten lisäämistä tai muuttamista varten.</span><span class="sxs-lookup"><span data-stu-id="f0681-121">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="f0681-122">Voit tarkastella luetteloa kirjausryhmistä, jotka tekevät kirjauksia kyseiselle tilille.</span><span class="sxs-lookup"><span data-stu-id="f0681-122">See a list of posting groups that post to that account.</span></span>  

<span data-ttu-id="f0681-123">Voit lisätä, muuttaa tai poistaa pääkirjanpidon tilejä.</span><span class="sxs-lookup"><span data-stu-id="f0681-123">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="f0681-124">Ristiriitojen estämiseksi et voi kuitenkaan poistaa pääkirjanpidon tiliä, jos sen tietoja käytetään tilikartassa.</span><span class="sxs-lookup"><span data-stu-id="f0681-124">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="f0681-125">Tililuokat</span><span class="sxs-lookup"><span data-stu-id="f0681-125">Account Categories</span></span>
<span data-ttu-id="f0681-126">Voit räätälöidä rahoituslaskelmien rakennetta yhdistämällä pääkirjanpidon tilit tililuokkiin.</span><span class="sxs-lookup"><span data-stu-id="f0681-126">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="f0681-127">**KP-tilin luokat** -ikkunassa on aiemmin luodut pää- ja alaluokat sekä niihin liitetyt KP-tilit.</span><span class="sxs-lookup"><span data-stu-id="f0681-127">The **G/L Account Categories** window shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="f0681-128">Voit luoda uusia alaluokkia ja liittää luokat aiemmin luotuihin tileihin.</span><span class="sxs-lookup"><span data-stu-id="f0681-128">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="f0681-129">Voit luoda luokkaryhmän sisentämällä **KP-tilin luokat** -ikkunan rivin alla olevia muita alaluokkia.</span><span class="sxs-lookup"><span data-stu-id="f0681-129">You create a category group by indenting other subcategories under a line in the **G/L Account Categories** window.</span></span> <span data-ttu-id="f0681-130">Tällöin yleiskuvauksen saaminen on helppoa, koska kunkin ryhmittelyn yhteydessä näytetään kokonaissaldo.</span><span class="sxs-lookup"><span data-stu-id="f0681-130">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="f0681-131">Voit luoda esimerkiksi alaluokkia eri käyttöomaisuustyypeille ja luoda sitten luokkaryhmiä esimerkiksi käyttöomaisuudelle ja nykyisille vastaaville.</span><span class="sxs-lookup"><span data-stu-id="f0681-131">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="f0681-132">Voit määrittää, onko kunkin alaluokan tilit sisällytettävä tietyn tyyppisiin raportteihin.</span><span class="sxs-lookup"><span data-stu-id="f0681-132">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="f0681-133">Tililuokat auttavat rahoituslaskelmien asettelun määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="f0681-133">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="f0681-134">Esimerkiksi oletussaldon tiliotteessa on Käteisvarat-alaluokka Vastaavaa-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="f0681-134">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="f0681-135">Jos haluat, että tiliote ottaa käteiskassan ja sekit huomioon, voit</span><span class="sxs-lookup"><span data-stu-id="f0681-135">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="f0681-136">lisätä kaksi uutta alaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="f0681-136">Add two new subcategories.</span></span> <span data-ttu-id="f0681-137">Niistä toinen on tarkoitettu käteiskassalle ja toinen sekkitilille.</span><span class="sxs-lookup"><span data-stu-id="f0681-137">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="f0681-138">Määritä näille alaluokille lisäraporttimääritys **Käteistilit**.</span><span class="sxs-lookup"><span data-stu-id="f0681-138">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="f0681-139">Sisennä ne **Käteisvarat**-alaluokassa.</span><span class="sxs-lookup"><span data-stu-id="f0681-139">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="f0681-140">Kun luot seuraavan kerran KP-raporttimalleja, tiliotteessa näkyy käteisvarojen kokonaissaldo sekä käteiskassan ja sekkitilin saldojen kaksi riviä.</span><span class="sxs-lookup"><span data-stu-id="f0681-140">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f0681-141">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f0681-141">See Also</span></span>
[<span data-ttu-id="f0681-142">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="f0681-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="f0681-143">Tilikartan määrittäminen tai muuttaminen</span><span class="sxs-lookup"><span data-stu-id="f0681-143">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="f0681-144">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="f0681-144">Business Intelligence</span></span>](bi.md)  

