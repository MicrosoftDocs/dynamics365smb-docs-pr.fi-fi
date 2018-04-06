---
title: Ostoasiakirjojen kirjaaminen | Microsoft Docs
description: "Tutustu erilaisiin ostoasiakirjojen kirjauksessa käytettäviin kirjaustoimintoihin."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 06c22658518d504c80a5a379d579cf7f7e8a0757
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="posting-purchases"></a><span data-ttu-id="e409f-103">Ostojen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="e409f-103">Posting Purchases</span></span>
<span data-ttu-id="e409f-104">Kun valitset ostoasiakirjan **Kirjausryhmä**-painikkeen, voit valita seuraavista kirjaustoiminnoista:</span><span class="sxs-lookup"><span data-stu-id="e409f-104">In the **Posting group** on a purchase document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="e409f-105">**Kirjaa**</span><span class="sxs-lookup"><span data-stu-id="e409f-105">**Post**</span></span>
* <span data-ttu-id="e409f-106">**Esikatsele kirjausta**</span><span class="sxs-lookup"><span data-stu-id="e409f-106">**Preview Posting**</span></span>
* <span data-ttu-id="e409f-107">**Kirjaa ja tulosta**</span><span class="sxs-lookup"><span data-stu-id="e409f-107">**Post and Print**</span></span>
* <span data-ttu-id="e409f-108">**Testiraportti**</span><span class="sxs-lookup"><span data-stu-id="e409f-108">**Test Report**</span></span>
* <span data-ttu-id="e409f-109">**Kirjaa erä**</span><span class="sxs-lookup"><span data-stu-id="e409f-109">**Post Batch**</span></span>

<span data-ttu-id="e409f-110">Kun olet täyttänyt kaikki rivit ja syöttänyt kaikki tiedot ostotilaukseen, voit kirjata sen eli luoda vastaanoton ja laskun.</span><span class="sxs-lookup"><span data-stu-id="e409f-110">When you have completed all the lines and entered all the information on the purchase order, you can post it, that is, create a receipt and an invoice.</span></span>

<span data-ttu-id="e409f-111">Kun ostotilaus on kirjattu, toimittajan tili, pääkirjanpito ja nimiketapahtumat päivitetään.</span><span class="sxs-lookup"><span data-stu-id="e409f-111">When a purchase order is posted, the vendor's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="e409f-112">Jokaiselle ostotilaukselle luodaan ostotapahtuma **KP-tapahtuma**-taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="e409f-112">For each purchase order, a purchase entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="e409f-113">Myös toimittajan tilille **Toimittajatapahtuma**-taulukkoon luodaan tapahtuma ja lisäksi luodaan KP-tapahtuma asianmukaiselle ostovelkatilille.</span><span class="sxs-lookup"><span data-stu-id="e409f-113">An entry is also created in the vendor's account in the **Vendor Ledger Entry** table and a G/L entry is created in the relevant payables account.</span></span> <span data-ttu-id="e409f-114">Lisäksi tilauksen kirjauksen tuloksena saattaa olla ALV-tapahtuman ja KP-tapahtuman luonti alennussummalle.</span><span class="sxs-lookup"><span data-stu-id="e409f-114">In addition, posting the order may result in a VAT entry and a G/L entry for the discount amount.</span></span> <span data-ttu-id="e409f-115">Se, kirjataanko alennukselle tapahtuma, määräytyy **Ostojen ja ostovelkojen asetukset** -taulukon **Alennuksen kirjaus** -kentän sisällön perusteella.</span><span class="sxs-lookup"><span data-stu-id="e409f-115">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field in the **Purchases & Payables Setup** window.</span></span>

<span data-ttu-id="e409f-116">Kullekin ostotilausriville luodaan nimiketapahtuma **Nimiketapahtuma**-taulukkoon (jos ostorivit sisältävät nimikenumeroita) tai KP-tapahtuma **KP-tapahtuma**-taulukkoon (jos ostorivit sisältävät KP-tilin).</span><span class="sxs-lookup"><span data-stu-id="e409f-116">For each purchase order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the purchase lines contain item numbers) or a G/L entry will be created in the **G/L Entry** table (if the purchase lines contain a G/L account).</span></span> <span data-ttu-id="e409f-117">Lisäksi ostotilaukset tallennetaan aina **Tavaran vastaanoton otsikko**- ja **Ostolaskun otsikko** -taulukoihin.</span><span class="sxs-lookup"><span data-stu-id="e409f-117">In addition, purchase orders are always recorded in the **Purch. Recpt. Header** and **Purch. Inv. Header** tables.</span></span>

<span data-ttu-id="e409f-118">Ennen kirjausta voit tulostaa testiraportin, jossa on kaikki tiedot ostotilauksesta ja joka osoittaa mahdolliset virheet.</span><span class="sxs-lookup"><span data-stu-id="e409f-118">Before you start to post, you can print a test report that contains all the information in the purchase order and indicates any errors there.</span></span> <span data-ttu-id="e409f-119">Kun haluat tulostaa raportin, valitse **Kirjaus** ja valitse sitten **Testiraportti**.</span><span class="sxs-lookup"><span data-stu-id="e409f-119">To print the report, choose **Posting**, and then choose **Test Report**.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="e409f-120">Kun kirjaat tilauksen, voit luoda sekä vastaanoton että laskun.</span><span class="sxs-lookup"><span data-stu-id="e409f-120">When you post an order, you can create both a receipt and an invoice.</span></span> <span data-ttu-id="e409f-121">Nämä voidaan luoda joko yhtäaikaa tai erikseen.</span><span class="sxs-lookup"><span data-stu-id="e409f-121">These can be done simultaneously or independently.</span></span> <span data-ttu-id="e409f-122">Voit luoda osittaisen vastaanoton ja osittaisen laskutuksen täyttämällä **Vastaanotettava määrä** ja **Laskutettava määrä** -kentät yksittäisillä ostotilausriveillä ennen kirjausta.</span><span class="sxs-lookup"><span data-stu-id="e409f-122">You can also create a partial receipt and a partial invoice by completing the **Qty. to Receive** and **Qty. to Invoice** fields on the individual purchase order lines before you post.</span></span> <span data-ttu-id="e409f-123">Huomaa, et voi luoda laskua jos sellaista ei ole vastaanotettu.</span><span class="sxs-lookup"><span data-stu-id="e409f-123">Note that you cannot create an invoice for something that has not been received.</span></span> <span data-ttu-id="e409f-124">Siispä ennen laskuttamista on täytynyt tallentaa vastaanotto, tai sinun täytyy valita samanaikainen vastaanotto ja laskutus.</span><span class="sxs-lookup"><span data-stu-id="e409f-124">That is, before you can invoice, you must have recorded a receipt, or you must choose to receive and invoice at the same time.</span></span>

<span data-ttu-id="e409f-125">Voit kirjata tai kirjata ja tulostaa.</span><span class="sxs-lookup"><span data-stu-id="e409f-125">You can either post, or post and print.</span></span> <span data-ttu-id="e409f-126">Jos valitset kirjaamisen ja tulostamisen, raportti tulostetaan tilauksen kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e409f-126">If you choose to post and print, a report is printed when the order is posted.</span></span> <span data-ttu-id="e409f-127">**Kirjaa erä** -toiminnolla voit kirjata useita tilauksia samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="e409f-127">You can also choose the **Post Batch** function, which lets you post several orders at the same time.</span></span>

<span data-ttu-id="e409f-128">Kun kirjaus on päättynyt, kirjatut ostorivit poistuvat tilauksesta.</span><span class="sxs-lookup"><span data-stu-id="e409f-128">When the posting is completed, the posted purchase lines are removed from the order.</span></span> <span data-ttu-id="e409f-129">Viesti kertoo, milloin kirjaus on valmis.</span><span class="sxs-lookup"><span data-stu-id="e409f-129">A message tells you when the posting is completed.</span></span> <span data-ttu-id="e409f-130">Tämän jälkeen voit nähdä kirjatut tapahtumat useissa kirjattuja tapahtumia sisältävissä ikkunoissa, kuten **Toimittajatapahtumat**-, **KP -tapahtumat**-, **Nimiketapahtumat**-, **Ostovastaanotot**- ja **Kirjatut ostolaskut** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="e409f-130">After this, you will be able to see the posted entries in the various windows that contain posted entries, such as the **Vendor Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Purchase Receipts**, and **Posted Purchase Invoices** windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="e409f-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e409f-131">See Also</span></span>
[<span data-ttu-id="e409f-132">Osto</span><span class="sxs-lookup"><span data-stu-id="e409f-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="e409f-133">Asiakirjojen ja päiväkirjojen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="e409f-133">Post Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="e409f-134">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e409f-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


