---
title: Myyntiasiakirjojen kirjaaminen | Microsoft Docs
description: "Tutustu erilaisiin myyntiasiakirjojen kirjauksessa käytettäviin kirjaustoimintoihin."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 04807ffbb2d009ae309c499f62e48fa93437b8b5
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="posting-sales"></a><span data-ttu-id="6768c-103">Myynnin kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="6768c-103">Posting Sales</span></span>
<span data-ttu-id="6768c-104">Kun valitset myyntiasiakirjan **Kirjausryhmä**-painikkeen, voit valita seuraavista kirjaustoiminnoista:</span><span class="sxs-lookup"><span data-stu-id="6768c-104">In the **Posting group** on a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="6768c-105">**Kirjaa**</span><span class="sxs-lookup"><span data-stu-id="6768c-105">**Post**</span></span>
* <span data-ttu-id="6768c-106">**Testiraportti**</span><span class="sxs-lookup"><span data-stu-id="6768c-106">**Test Report**</span></span>
* <span data-ttu-id="6768c-107">**Kirjaa ja lähetä**</span><span class="sxs-lookup"><span data-stu-id="6768c-107">**Post and Send**</span></span>
* <span data-ttu-id="6768c-108">**Kirjaa ja tulosta**</span><span class="sxs-lookup"><span data-stu-id="6768c-108">**Post and Print**</span></span>
* <span data-ttu-id="6768c-109">**Kirjaa ja lähetä sähköpostitse**</span><span class="sxs-lookup"><span data-stu-id="6768c-109">**Post and Email**</span></span>
* <span data-ttu-id="6768c-110">**Kirjaa erä**</span><span class="sxs-lookup"><span data-stu-id="6768c-110">**Post Batch**</span></span>
* <span data-ttu-id="6768c-111">**Esikatsele kirjausta**</span><span class="sxs-lookup"><span data-stu-id="6768c-111">**Preview Posting**</span></span>

<span data-ttu-id="6768c-112">Kun olet täyttänyt kaikki rivit ja syöttänyt kaikki tiedot myyntitilaukseen, voit kirjata sen eli luoda vastaanoton ja laskun.</span><span class="sxs-lookup"><span data-stu-id="6768c-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="6768c-113">Tämä luo toimituksen ja laskun.</span><span class="sxs-lookup"><span data-stu-id="6768c-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="6768c-114">Kun myyntitilaus on kirjattu, asiakkaan tili, pääkirjanpito ja nimiketapahtumat päivitetään.</span><span class="sxs-lookup"><span data-stu-id="6768c-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="6768c-115">Jokaiselle myyntitilaukselle luodaan myyntitapahtuma **KP-tapahtuma**-taulukossa.</span><span class="sxs-lookup"><span data-stu-id="6768c-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="6768c-116">Myös **Toimittajatapahtuma**-taulukon asiakkaan tilille luodaan tapahtuma. Lisäksi luodaan pääkirjanpidon tapahtuma asianmukaiselle myyntisaamistilille.</span><span class="sxs-lookup"><span data-stu-id="6768c-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="6768c-117">Lisäksi tilauksen kirjauksen tuloksena saattaa olla ALV-tapahtuman ja KP-tapahtuman luonti alennussummalle.</span><span class="sxs-lookup"><span data-stu-id="6768c-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="6768c-118">Se, kirjataanko alennukselle tapahtuma, määräytyy **Ostojen ja ostovelkojen asetukset** -ikkunan **Alennuksen kirjaus** -kentän sisällön perusteella.</span><span class="sxs-lookup"><span data-stu-id="6768c-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field in the **Sales & Receivables Setup** window.</span></span>

<span data-ttu-id="6768c-119">Jokaiselle myyntitilausriville luodaan nimiketapahtuma **Nimiketapahtuma**-taulukkoon (jos myyntiriveillä on nimikenumeroita) tai pääkirjanpidon tapahtuma **KP-tapahtuma**-taulukkoon (jos myyntiriveillä on pääkirjanpitotili).</span><span class="sxs-lookup"><span data-stu-id="6768c-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="6768c-120">Tämän lisäksi myyntitilaukset tallennetaan aina **Lähtevän toimituksen otsikko**- ja **Myyntilaskun otsikko** -taulukoihin.</span><span class="sxs-lookup"><span data-stu-id="6768c-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="6768c-121">Kun kirjaat tilauksen, voit luoda sekä toimituksen että laskun.</span><span class="sxs-lookup"><span data-stu-id="6768c-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="6768c-122">Tämä voidaan tehdä samaan aikaan tai erikseen.</span><span class="sxs-lookup"><span data-stu-id="6768c-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="6768c-123">Voit luoda myös osittaisen toimituksen tai osittaisen laskun täyttämällä **Toimitettava määrä**- ja **Laskutettava määrä** -kentät yksittäisillä myyntitilausriveillä ennen kirjausta.</span><span class="sxs-lookup"><span data-stu-id="6768c-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="6768c-124">Huomaa, että laskua ei voi luoda jollekin, jota ei ole toimitettu.</span><span class="sxs-lookup"><span data-stu-id="6768c-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="6768c-125">Tämä tarkoittaa sitä, että ennen laskutusta on täytynyt tallentaa toimitus, tai täytyy valita yhtäaikainen toimitus ja laskutus.</span><span class="sxs-lookup"><span data-stu-id="6768c-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="6768c-126">Kun kirjaus on päättynyt, kirjatut myyntirivit poistuvat tilauksesta.</span><span class="sxs-lookup"><span data-stu-id="6768c-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="6768c-127">Viesti kertoo, milloin kirjaus on valmis.</span><span class="sxs-lookup"><span data-stu-id="6768c-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="6768c-128">Tämän jälkeen voit nähdä kirjatut tapahtumat kirjattuja tapahtumia sisältävissä ikkunoissa, kuten **Asiakastapahtumat**-, **KP-tapahtumat**-, **Nimiketapahtumat**-, **Kirjatut myyntitoimitukset**- ja**Kirjatut myyntilaskut** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="6768c-128">After this, you will be able to see the posted entries in the various windows that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="6768c-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6768c-129">See Also</span></span>
[<span data-ttu-id="6768c-130">Myynti</span><span class="sxs-lookup"><span data-stu-id="6768c-130">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="6768c-131">Asiakirjojen lähettäminen sähköpostitse</span><span class="sxs-lookup"><span data-stu-id="6768c-131">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="6768c-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6768c-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


