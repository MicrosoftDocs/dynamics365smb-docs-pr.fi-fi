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
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 63d414f4c81a9e20b4bb81b632edd9c91fb34a87
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="56025-103">Pääkirjanpito ja aitoustodistus</span><span class="sxs-lookup"><span data-stu-id="56025-103">Understanding the General Ledger and the COA</span></span>
<span data-ttu-id="56025-104">Pääkirjanpito sisältää taloustiedot ja tilikartta näyttää tilit, joihin kaikki pääkirjanpidon tapahtumat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="56025-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="56025-105"> sisältää tilikartan, joka on valmis tukemaan liiketoimintaasi.</span><span class="sxs-lookup"><span data-stu-id="56025-105"> includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="56025-106">Pääkirjanpidon asetukset ja yleiset kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="56025-106">General Ledger Setup and General Posting Setup</span></span>
<span data-ttu-id="56025-107">Pääkirjanpidon asetukset ovat keskeisiä rahoitusprosesseja, sillä niillä määritetään tietojen kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="56025-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="56025-108">**Pääkirjanpidon asetukset** -ikkunassa määritetään, miten esimerkiksi seuraavat yrityksen kirjanpitoasiat:</span><span class="sxs-lookup"><span data-stu-id="56025-108">In the **General Ledger Setup** window, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="56025-109">Laskun pyöristystiliedot</span><span class="sxs-lookup"><span data-stu-id="56025-109">Invoice rounding details</span></span>  
* <span data-ttu-id="56025-110">Osoitteen muodot</span><span class="sxs-lookup"><span data-stu-id="56025-110">Address formats</span></span>  
* <span data-ttu-id="56025-111">Talousraportointi</span><span class="sxs-lookup"><span data-stu-id="56025-111">Financial reporting</span></span>  

<span data-ttu-id="56025-112">Samaan tapaan määritetään **Yleiset kirjausasetukset** -ikkunassa, miten liiketoiminnan ja tuotteen yleisten kirjausryhmien yhdistelmät määritetään.</span><span class="sxs-lookup"><span data-stu-id="56025-112">Similarly, in the **General Posting Setup** window, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="56025-113">Kirjausryhmät yhdistävät objektit, kuten asiakkaat, toimittajat, nimikkeet, resurssit sekä myynti- ja ostoasiakirjoja pääkirjanpidon tileille.</span><span class="sxs-lookup"><span data-stu-id="56025-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="56025-114">Jokaiselle liiketoiminnan kirjausryhmän ja tuotteen kirjausryhmän yhdistelmälle täytetään rivi.</span><span class="sxs-lookup"><span data-stu-id="56025-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="56025-115">Lisätietoja on kohdassa [Kirjausryhmien asetukset](finance-posting-groups.md)</span><span class="sxs-lookup"><span data-stu-id="56025-115">For more information, see [Posting Group Setups](finance-posting-groups.md)</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="56025-116">Tilikartta</span><span class="sxs-lookup"><span data-stu-id="56025-116">The Chart of Accounts</span></span>
<span data-ttu-id="56025-117">Kaikki pääkirjanpidon tilit näkyvät tilikartassa.</span><span class="sxs-lookup"><span data-stu-id="56025-117">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="56025-118">Tilikartassa voi tehdä esimerkiksi seuraavia toimintoja:</span><span class="sxs-lookup"><span data-stu-id="56025-118">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="56025-119">Voit tarkastella pääkirjanpitotapahtumat- ja saldot näyttäviä raportteja.</span><span class="sxs-lookup"><span data-stu-id="56025-119">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="56025-120">Voit sulkea tuloslaskelman.</span><span class="sxs-lookup"><span data-stu-id="56025-120">Close your income statement.</span></span>  
* <span data-ttu-id="56025-121">Voita avata KP-tilikortin asetusten lisäämistä tai muuttamista varten.</span><span class="sxs-lookup"><span data-stu-id="56025-121">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="56025-122">Voit tarkastella luetteloa kirjausryhmistä, jotka tekevät kirjauksia kyseiselle tilille.</span><span class="sxs-lookup"><span data-stu-id="56025-122">See a list of posting groups that post to that account.</span></span>
* <span data-ttu-id="56025-123">Yhden tilin erillisten debet- ja kreditsaldojen näyttäminen</span><span class="sxs-lookup"><span data-stu-id="56025-123">View separate debit and credit balances for a single account</span></span>  

<span data-ttu-id="56025-124">Voit lisätä, muuttaa tai poistaa pääkirjanpidon tilejä.</span><span class="sxs-lookup"><span data-stu-id="56025-124">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="56025-125">Ristiriitojen estämiseksi et voi kuitenkaan poistaa pääkirjanpidon tiliä, jos sen tietoja käytetään tilikartassa.</span><span class="sxs-lookup"><span data-stu-id="56025-125">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="56025-126">Tililuokat</span><span class="sxs-lookup"><span data-stu-id="56025-126">Account Categories</span></span>
<span data-ttu-id="56025-127">Voit räätälöidä rahoituslaskelmien rakennetta yhdistämällä pääkirjanpidon tilit tililuokkiin.</span><span class="sxs-lookup"><span data-stu-id="56025-127">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="56025-128">**KP-tilin luokat** -ikkunassa on aiemmin luodut pää- ja alaluokat sekä niihin liitetyt KP-tilit.</span><span class="sxs-lookup"><span data-stu-id="56025-128">The **G/L Account Categories** window shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="56025-129">Voit luoda uusia alaluokkia ja liittää luokat aiemmin luotuihin tileihin.</span><span class="sxs-lookup"><span data-stu-id="56025-129">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="56025-130">Voit luoda luokkaryhmän sisentämällä **KP-tilin luokat** -ikkunan rivin alla olevia muita alaluokkia.</span><span class="sxs-lookup"><span data-stu-id="56025-130">You create a category group by indenting other subcategories under a line in the **G/L Account Categories** window.</span></span> <span data-ttu-id="56025-131">Tällöin yleiskuvauksen saaminen on helppoa, koska kunkin ryhmittelyn yhteydessä näytetään kokonaissaldo.</span><span class="sxs-lookup"><span data-stu-id="56025-131">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="56025-132">Voit luoda esimerkiksi alaluokkia eri käyttöomaisuustyypeille ja luoda sitten luokkaryhmiä esimerkiksi käyttöomaisuudelle ja nykyisille vastaaville.</span><span class="sxs-lookup"><span data-stu-id="56025-132">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="56025-133">Voit määrittää, onko kunkin alaluokan tilit sisällytettävä tietyn tyyppisiin raportteihin.</span><span class="sxs-lookup"><span data-stu-id="56025-133">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="56025-134">Tililuokat auttavat rahoituslaskelmien asettelun määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="56025-134">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="56025-135">Esimerkiksi oletussaldon tiliotteessa on Käteisvarat-alaluokka Vastaavaa-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="56025-135">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="56025-136">Jos haluat, että tiliote ottaa käteiskassan ja sekit huomioon, voit</span><span class="sxs-lookup"><span data-stu-id="56025-136">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="56025-137">lisätä kaksi uutta alaluokkaa.</span><span class="sxs-lookup"><span data-stu-id="56025-137">Add two new subcategories.</span></span> <span data-ttu-id="56025-138">Niistä toinen on tarkoitettu käteiskassalle ja toinen sekkitilille.</span><span class="sxs-lookup"><span data-stu-id="56025-138">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="56025-139">Määritä näille alaluokille lisäraporttimääritys **Käteistilit**.</span><span class="sxs-lookup"><span data-stu-id="56025-139">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="56025-140">Sisennä ne **Käteisvarat**-alaluokassa.</span><span class="sxs-lookup"><span data-stu-id="56025-140">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="56025-141">Kun luot seuraavan kerran KP-raporttimalleja, tiliotteessa näkyy käteisvarojen kokonaissaldo sekä käteiskassan ja sekkitilin saldojen kaksi riviä.</span><span class="sxs-lookup"><span data-stu-id="56025-141">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="56025-142">Katso myös</span><span class="sxs-lookup"><span data-stu-id="56025-142">See Also</span></span>
[<span data-ttu-id="56025-143">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="56025-143">Finance</span></span>](finance.md)  
[<span data-ttu-id="56025-144">Tilikartan määrittäminen tai muuttaminen</span><span class="sxs-lookup"><span data-stu-id="56025-144">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="56025-145">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="56025-145">Business Intelligence</span></span>](bi.md)  

