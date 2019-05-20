---
title: Myyntiasiakirjojen kirjaaminen | Microsoft Docs
description: Tutustu erilaisiin myyntiasiakirjojen kirjauksessa käytettäviin kirjaustoimintoihin.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: d1b2d29c4c5b8397bd6e9e05088e7ea50d68fd20
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247902"
---
# <a name="posting-sales"></a><span data-ttu-id="3d3da-103">Myynnin kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="3d3da-103">Posting Sales</span></span>
<span data-ttu-id="3d3da-104">Kun valitset myyntiasiakirjan **Kirjausryhmä**-painikkeen, voit valita seuraavista kirjaustoiminnoista:</span><span class="sxs-lookup"><span data-stu-id="3d3da-104">In the **Posting group** on a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="3d3da-105">**Kirjaa**</span><span class="sxs-lookup"><span data-stu-id="3d3da-105">**Post**</span></span>
* <span data-ttu-id="3d3da-106">**Testiraportti**</span><span class="sxs-lookup"><span data-stu-id="3d3da-106">**Test Report**</span></span>
* <span data-ttu-id="3d3da-107">**Kirjaa ja lähetä**</span><span class="sxs-lookup"><span data-stu-id="3d3da-107">**Post and Send**</span></span>
* <span data-ttu-id="3d3da-108">**Kirjaa ja tulosta**</span><span class="sxs-lookup"><span data-stu-id="3d3da-108">**Post and Print**</span></span>
* <span data-ttu-id="3d3da-109">**Kirjaa ja lähetä sähköpostitse**</span><span class="sxs-lookup"><span data-stu-id="3d3da-109">**Post and Email**</span></span>
* <span data-ttu-id="3d3da-110">**Kirjaa erä**</span><span class="sxs-lookup"><span data-stu-id="3d3da-110">**Post Batch**</span></span>
* <span data-ttu-id="3d3da-111">**Esikatsele kirjausta**</span><span class="sxs-lookup"><span data-stu-id="3d3da-111">**Preview Posting**</span></span>

<span data-ttu-id="3d3da-112">Kun olet täyttänyt kaikki rivit ja syöttänyt kaikki tiedot myyntitilaukseen, voit kirjata sen eli luoda vastaanoton ja laskun.</span><span class="sxs-lookup"><span data-stu-id="3d3da-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="3d3da-113">Tämä luo toimituksen ja laskun.</span><span class="sxs-lookup"><span data-stu-id="3d3da-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="3d3da-114">Kun myyntitilaus on kirjattu, asiakkaan tili, pääkirjanpito ja nimiketapahtumat päivitetään.</span><span class="sxs-lookup"><span data-stu-id="3d3da-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="3d3da-115">Jokaiselle myyntitilaukselle luodaan myyntitapahtuma **KP-tapahtuma**-taulukossa.</span><span class="sxs-lookup"><span data-stu-id="3d3da-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="3d3da-116">Myös **Toimittajatapahtuma**-taulukon asiakkaan tilille luodaan tapahtuma. Lisäksi luodaan pääkirjanpidon tapahtuma asianmukaiselle myyntisaamistilille.</span><span class="sxs-lookup"><span data-stu-id="3d3da-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="3d3da-117">Lisäksi tilauksen kirjauksen tuloksena saattaa olla ALV-tapahtuman ja KP-tapahtuman luonti alennussummalle.</span><span class="sxs-lookup"><span data-stu-id="3d3da-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="3d3da-118">Se, kirjataanko alennukselle tapahtuma, määräytyy **Ostojen ja ostovelkojen asetukset** -sivun **Alennuksen kirjaus** -kentän sisällön perusteella.</span><span class="sxs-lookup"><span data-stu-id="3d3da-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field on the **Sales & Receivables Setup** page.</span></span>

<span data-ttu-id="3d3da-119">Jokaiselle myyntitilausriville luodaan nimiketapahtuma **Nimiketapahtuma**-taulukkoon (jos myyntiriveillä on nimikenumeroita) tai pääkirjanpidon tapahtuma **KP-tapahtuma**-taulukkoon (jos myyntiriveillä on pääkirjanpitotili).</span><span class="sxs-lookup"><span data-stu-id="3d3da-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="3d3da-120">Tämän lisäksi myyntitilaukset tallennetaan aina **Lähtevän toimituksen otsikko**- ja **Myyntilaskun otsikko** -taulukoihin.</span><span class="sxs-lookup"><span data-stu-id="3d3da-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="3d3da-121">Kun kirjaat tilauksen, voit luoda sekä toimituksen että laskun.</span><span class="sxs-lookup"><span data-stu-id="3d3da-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="3d3da-122">Tämä voidaan tehdä samaan aikaan tai erikseen.</span><span class="sxs-lookup"><span data-stu-id="3d3da-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="3d3da-123">Voit luoda myös osittaisen toimituksen tai osittaisen laskun täyttämällä **Toimitettava määrä**- ja **Laskutettava määrä** -kentät yksittäisillä myyntitilausriveillä ennen kirjausta.</span><span class="sxs-lookup"><span data-stu-id="3d3da-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="3d3da-124">Huomaa, että laskua ei voi luoda jollekin, jota ei ole toimitettu.</span><span class="sxs-lookup"><span data-stu-id="3d3da-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="3d3da-125">Tämä tarkoittaa sitä, että ennen laskutusta on täytynyt tallentaa toimitus, tai täytyy valita yhtäaikainen toimitus ja laskutus.</span><span class="sxs-lookup"><span data-stu-id="3d3da-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="3d3da-126">Kun kirjaus on päättynyt, kirjatut myyntirivit poistuvat tilauksesta.</span><span class="sxs-lookup"><span data-stu-id="3d3da-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="3d3da-127">Viesti kertoo, milloin kirjaus on valmis.</span><span class="sxs-lookup"><span data-stu-id="3d3da-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="3d3da-128">Tämän jälkeen voit nähdä kirjatut tapahtumat kirjattuja tapahtumia sisältävillä sivuilla, kuten **Asiakastapahtumat**-, **KP-tapahtumat**-, **Nimiketapahtumat**-, **Kirjatut myyntitoimitukset**- ja**Kirjatut myyntilaskut** -sivuilla.</span><span class="sxs-lookup"><span data-stu-id="3d3da-128">After this, you will be able to see the posted entries in the various pages that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** pages.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d3da-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3d3da-129">See Also</span></span>
[<span data-ttu-id="3d3da-130">Myynti</span><span class="sxs-lookup"><span data-stu-id="3d3da-130">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="3d3da-131">Asiakirjojen lähettäminen sähköpostitse</span><span class="sxs-lookup"><span data-stu-id="3d3da-131">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="3d3da-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3d3da-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

