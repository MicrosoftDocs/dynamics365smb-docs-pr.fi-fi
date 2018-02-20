---
title: Kulujen tai tuottojen kirjaaminen suoraan kirjanpitoon| Microsoft Docs
description: "Liiketoiminnan aktiviteeteille, joihin ei liity asiakirjaa, kuten pienille kuluille tai käteissuorituksille voi luoda liittyvät tapahtumat kirjaamalla päiväkirjarivit Yleinen päiväkirja -ikkunassa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6925c2ddb45973e060c7694a83bc03c7fbabcf41
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="fbae7-103">Tapahtumien kirjaaminen suoraan pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="fbae7-103">Post Transactions Directly to the General Ledger</span></span>
<span data-ttu-id="fbae7-104">Useimmat rahoitustapahtumat kirjataan pääkirjanpitoon erityisten yritysasiakirjojen, kuten ostolaskujen ja myyntitilausten välityksellä.</span><span class="sxs-lookup"><span data-stu-id="fbae7-104">Most financial transactions are posted to the general ledger through dedicated business documents, such as purchase invoices and sales orders.</span></span> <span data-ttu-id="fbae7-105">Liiketoiminnan aktiviteeteille, joihin ei liity [!INCLUDE[d365fin](includes/d365fin_md.md)]-asiakirjaa, kuten pienille kuluille tai käteissuorituksille voi luoda liittyvät tapahtumat kirjaamalla päiväkirjarivit **Yleinen päiväkirja** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="fbae7-105">For business activities that are not represented by a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as smaller expenses or cash receipts, you can create the related transactions by posting journal lines in the **General Journal** window.</span></span>

<span data-ttu-id="fbae7-106">Yleiseen päiväkirjaan kirjataan tyypillisesti työntekijöiden liiketoimintaa varten käyttämät ovat varat myöhemmin hyvitettäväksi.</span><span class="sxs-lookup"><span data-stu-id="fbae7-106">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="fbae7-107">Lisätietoja on kohdassa [Työntekijöiden kulujen kirjaaminen ja hyvittäminen](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="fbae7-107">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="fbae7-108">Yleisiä päiväkirjoja käytetään rahoitustapahtumien kirjaamiseen suoraan kirjanpitotileille sekä muille tileille, kuten pankki-, asiakas-, toimittaja- ja työtekijätileille.</span><span class="sxs-lookup"><span data-stu-id="fbae7-108">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="fbae7-109">Yleisen päiväkirjan avulla kirjaaminen luo aina tapahtumia kirjanpitotileille.</span><span class="sxs-lookup"><span data-stu-id="fbae7-109">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="fbae7-110">Näin tapahtuu silloinkin, kun kirjataan esimerkiksi päiväkirjan rivi asiakkaan tilille, koska tapahtuma kirjataan pääkirjanpidon myyntisaamisten tilille kirjausryhmän kautta.</span><span class="sxs-lookup"><span data-stu-id="fbae7-110">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="fbae7-111">Voit mukauttaa yleistä päiväkirjaasi määrittämällä päiväkirjaerän tai -mallin.</span><span class="sxs-lookup"><span data-stu-id="fbae7-111">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="fbae7-112">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="fbae7-112">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="fbae7-113">Toisin kuin tapahtumat, jotka on kirjattu asiakirjasta ja edellyttävät hyvityslaskuprosessia, voit peruuttaa yleiseen päiväkirjaan kirjattuja tapahtumia oikein.</span><span class="sxs-lookup"><span data-stu-id="fbae7-113">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="fbae7-114">Lisätietoja on kohdassa [Kirjauksien peruuttaminen](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="fbae7-114">For more information, see [Reverse Postings](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="fbae7-115">Tapahtumien kirjaaminen suoraan pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="fbae7-115">To post a transaction directly to a general ledger account</span></span>
1. <span data-ttu-id="fbae7-116">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="fbae7-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="fbae7-117">Avaa liittyvä yleisen päiväkirjan erä.</span><span class="sxs-lookup"><span data-stu-id="fbae7-117">Open the relevant general journal batch.</span></span> <span data-ttu-id="fbae7-118">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="fbae7-118">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="fbae7-119">Täytä tarvittaessa uuden päiväkirjarivin kentät.</span><span class="sxs-lookup"><span data-stu-id="fbae7-119">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. <span data-ttu-id="fbae7-120">Toista vaihe 3 jokaiselle tapahtumalle, jonka haluat kirjata.</span><span class="sxs-lookup"><span data-stu-id="fbae7-120">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="fbae7-121">Jos haluat syöttää useita tapahtumarivejä yhden vastatilin rivin ylle, esimerkiksi yhdelle pankkitilille, valitse erän rivillä oleva **Ehdota vastasummaa** -valintaruutu **Yleisen päiväkirjan erät** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="fbae7-121">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch in the **General Journal Batches** window.</span></span> <span data-ttu-id="fbae7-122">Tällöin vastatilin rivin **Summa**-kenttä täytetään automaattisesti arvolla, joka vaaditaan tapahtumien täsmäyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="fbae7-122">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="fbae7-123">Valitse **Kirjaa**-toiminto kirjataksesi tapahtumat määritetyille KP-tileille.</span><span class="sxs-lookup"><span data-stu-id="fbae7-123">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="fbae7-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="fbae7-124">See Also</span></span>
[<span data-ttu-id="fbae7-125">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="fbae7-125">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="fbae7-126">Työntekijöiden kulujen kirjaaminen ja hyvittäminen</span><span class="sxs-lookup"><span data-stu-id="fbae7-126">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="fbae7-127">Kirjausten peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="fbae7-127">Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="fbae7-128">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="fbae7-128">Finance</span></span>](finance.md)  
<span data-ttu-id="fbae7-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fbae7-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

