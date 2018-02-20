---
title: "Konsernin asiakirjojen ja päiväkirjojen kirjaaminen| Microsoft Docs"
description: "Tapahtumien kirjaaminen yhdessä konsernikumppanien kanssa konsernin asiakirjojen avulla."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 98e0d9012dfdd998431aaed8dade02f592af47c8
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="work-with-intercompany-documents-and-journals"></a><span data-ttu-id="507cf-103">Konserniasiakirjojen ja -päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="507cf-103">Work with Intercompany Documents and Journals</span></span>
<span data-ttu-id="507cf-104">Voit kirjata tapahtumat konsernikumppanien kanssa konsernin asiakirjojen tai päiväkirjojen avulla.</span><span class="sxs-lookup"><span data-stu-id="507cf-104">You use intercompany documents or journals to post transactions with your intercompany partners.</span></span> <span data-ttu-id="507cf-105">Kun kirjaat konsernin asiakirja- tai päiväkirjarivin omassa yrityksessä, vastaava asiakirja- ja päiväkirjarivi luodaan konsernin Lähtevät-kansioon kumppanille lähettämistä varten.</span><span class="sxs-lookup"><span data-stu-id="507cf-105">When you post an intercompany document or journal line in your company, a corresponding document or journal line is created in your intercompany outbox that you can transfer to your partner.</span></span> <span data-ttu-id="507cf-106">Kumppaniyritys voi sitten kirjata vastaavan tapahtuman omassa yrityksessään ilman, että tiedot on annettava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="507cf-106">Your partner can then post the corresponding transaction in their company, without having to re-enter the data.</span></span>

<span data-ttu-id="507cf-107">Myynti- ja ostoasiakirjoissa oleva kyseisen asiakkaan tai toimittajan konsernikumppanikoodi varmistaa, että kaikki näihin yrityksiin liittyville tapahtumille muodostetut tilaukset ja laskut luovat vastaavat asiakirjat kumppaniyrityksessä. Tällä tavoin varmistetaan, että tilit täsmäytyvät oikein.</span><span class="sxs-lookup"><span data-stu-id="507cf-107">For sales and purchase documents, the intercompany partner code on the involved customer or vendor ensures that all orders and invoices generated pertaining to transactions with these companies will produce corresponding documents in the partner company, resulting in correct balancing of the accounts.</span></span>

<span data-ttu-id="507cf-108">Konsernin yleisen päiväkirjan riville ei tarvitse määrittää yksittäisten tilijoukkojen tilejä ei tarvitse määrittää vaan kumppaniyrityksen tunnus riittää.</span><span class="sxs-lookup"><span data-stu-id="507cf-108">For intercompany general journal lines, you do not need to specify the accounts for an individual set of books, but simply give the identification of the partner company.</span></span> <span data-ttu-id="507cf-109">Vastaavat konsernin yleisen päiväkirjan rivit luodaan sitten kumppaniyrityksessä siten, että kummankin tapahtuneen osallistuneen yrityksen tilit täsmäytetään.</span><span class="sxs-lookup"><span data-stu-id="507cf-109">Corresponding intercompany general journal lines are then created in the partner company that result in the balancing of the books of both companies involved in a transaction.</span></span>

## <a name="to-fill-in-and-send-an-intercompany-sales-order"></a><span data-ttu-id="507cf-110">Voit täyttää ja lähettää konsernin myyntitilauksen seuraavasti</span><span class="sxs-lookup"><span data-stu-id="507cf-110">To fill in and send an intercompany sales order</span></span>
<span data-ttu-id="507cf-111">Voit lähettää myynti- ja ostotilauksia sekä palauttaa tilauksia ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="507cf-111">You can send sales and purchase orders and return orders before posting.</span></span> <span data-ttu-id="507cf-112">Laskut ja hyvityslaskut voi lähettää vasta, kun ne on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="507cf-112">Invoices and credit memos cannot be sent until they are posted.</span></span>

<span data-ttu-id="507cf-113">Seuraavissa ohjeissa neuvotaan, kuinka voit täyttää ja lähettää konsernin myyntitilauksen.</span><span class="sxs-lookup"><span data-stu-id="507cf-113">The following procedure describes how to fill in and send an intercompany sales order.</span></span> <span data-ttu-id="507cf-114">Samat ohjeet koskevat myös konsernin osto- ja palautustilauksia sekä kirjattuja konsernin laskuja ja hyvityslaskuja.</span><span class="sxs-lookup"><span data-stu-id="507cf-114">The same steps apply to intercompany purchase orders and return orders, and to posted intercompany invoices and credit memos.</span></span>  

1. <span data-ttu-id="507cf-115">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="507cf-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="507cf-116">Luo uusi myyntitilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="507cf-116">Choose **New** to create a new sales order.</span></span> <span data-ttu-id="507cf-117">Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="507cf-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  
3. <span data-ttu-id="507cf-118">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="507cf-118">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="507cf-119">Varmista, että asiakas konsernikumppani.</span><span class="sxs-lookup"><span data-stu-id="507cf-119">Make sure the customer is an intercompany partner.</span></span>
5. <span data-ttu-id="507cf-120">Voit lähettää myyntitilauksen ennen sen kirjaamista valitsemalla **Lähetä konsernin myyntitilaus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="507cf-120">To send the sales order before you post it, choose the **Send IC Sales Order** action.</span></span>

> [!NOTE]
> <span data-ttu-id="507cf-121">Jos et tee vaihetta 4, myyntitilaus siirretään konsernin Lähtevät-kansioon, josta voit lähettää sen myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="507cf-121">If you do perform step 4, then the sales order will be moved to your intercompany outbox where you can send it later.</span></span> <span data-ttu-id="507cf-122">Lisätietoja on kohdassa [Konsernin Saapuneet- ja Lähtevät-kansion hallinta](intercompany-how-manage-intercompany-inbox.md).</span><span class="sxs-lookup"><span data-stu-id="507cf-122">For more information, see [Manage the Intercompany Inbox and Outbox](intercompany-how-manage-intercompany-inbox.md).</span></span>

## <a name="to-fill-in-and-post-an-intercompany-journal"></a><span data-ttu-id="507cf-123">Voit täyttää ja kirjata konsernin päiväkirjan seuraavasti</span><span class="sxs-lookup"><span data-stu-id="507cf-123">To fill in and post an intercompany journal</span></span>
<span data-ttu-id="507cf-124">Kun kirjaat konsernin yleisen päiväkirjan rivin omassa yrityksessä, vastaava päiväkirjarivi luodaan konsernin Lähtevät-kansioon kumppanille lähettämistä varten.</span><span class="sxs-lookup"><span data-stu-id="507cf-124">When you post an intercompany general journal line in your company, a corresponding journal line is created in your intercompany outbox that you can transfer to your partner.</span></span> <span data-ttu-id="507cf-125">Kumppaniyritys voi sitten kirjata vastaavan tapahtuman omassa yrityksessään ilman, että tiedot on annettava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="507cf-125">Your partner can then post the corresponding transaction in their company, without having to re-enter the data.</span></span>

1. <span data-ttu-id="507cf-126">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Konsernin yleiset päiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="507cf-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **IC General Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="507cf-127">Avaa käsiteltävä päiväkirjaerä.</span><span class="sxs-lookup"><span data-stu-id="507cf-127">Open the relevant journal batch.</span></span> <span data-ttu-id="507cf-128">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="507cf-128">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="507cf-129">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="507cf-129">Fill in the fields as necessary.</span></span>
4. <span data-ttu-id="507cf-130">Anna **Konsernikumppanin KP-tilinro** kentässä se konsernin kirjanpitotilin numero, jolle summa kirjataan kumppaniyrityksessä.</span><span class="sxs-lookup"><span data-stu-id="507cf-130">In the **IC Partner G/L Acc. No.** field, enter the intercompany general ledger account that the amount will be posted to in your partner's company.</span></span>

    > [!NOTE]
    > <span data-ttu-id="507cf-131">Tämä kenttä on täytettävä, jos rivin **Tilinro**- tai **Vastatilin nro** -kentässä on pankkitili tai kirjanpitotili.</span><span class="sxs-lookup"><span data-stu-id="507cf-131">This field must be filled in on a line with a bank account or general ledger account in either the **Account No.** field or the **Bal. Account No.** field.</span></span>  
5. <span data-ttu-id="507cf-132">Valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="507cf-132">Choose the **Post** action.</span></span>

<span data-ttu-id="507cf-133">Kyseiset tapahtumat kirjataan omaan yritykseen ja päiväkirjaan. Lisäksi vastaavat tapahtumat luodaan konsernin Lähtevät-kansioon, josta voit lähettää ne kumppaniyritykselle.</span><span class="sxs-lookup"><span data-stu-id="507cf-133">The involved entries are posted in your company and a journal with the corresponding entries are created in your intercompany outbox that you can send to your partner company.</span></span> <span data-ttu-id="507cf-134">Lisätietoja on kohdassa [Konsernin Saapuneet- ja Lähtevät-kansion hallinta](intercompany-how-manage-intercompany-inbox.md).</span><span class="sxs-lookup"><span data-stu-id="507cf-134">For more information, see [Manage the Intercompany Inbox and Outbox](intercompany-how-manage-intercompany-inbox.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="507cf-135">Katso myös</span><span class="sxs-lookup"><span data-stu-id="507cf-135">See Also</span></span>
[<span data-ttu-id="507cf-136">Konsernitapahtumien hallinta</span><span class="sxs-lookup"><span data-stu-id="507cf-136">Managing Intercompany Transactions</span></span>](intercompany-manage.md)  
[<span data-ttu-id="507cf-137">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="507cf-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="507cf-138">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="507cf-138">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="507cf-139">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="507cf-139">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="507cf-140">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="507cf-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

