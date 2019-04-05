---
title: Kulujen tai tuottojen kirjaaminen suoraan kirjanpitoon| Microsoft Docs
description: Liiketoiminnan aktiviteeteille, joihin ei liity asiakirjaa, kuten pienille kuluille tai käteissuorituksille voi luoda liittyvät tapahtumat kirjaamalla päiväkirjarivit Yleinen päiväkirja -sivulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 11/27/2018
ms.author: sgroespe
ms.openlocfilehash: a1e7137cdc08fb558b6a6d423ce9524fa47eec16
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795344"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="209fa-103">Tapahtumien kirjaaminen suoraan pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="209fa-103">Post Transactions Directly to the General Ledger</span></span>

<span data-ttu-id="209fa-104">Yleisiä päiväkirjoja käytetään rahoitustapahtumien kirjaamisessa suoraan pääkirjanpitotileille sekä muille tileille, kuten pankki-, asiakas-, toimittaja- ja työntekijätileille.</span><span class="sxs-lookup"><span data-stu-id="209fa-104">You use general journals to post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span>  

<span data-ttu-id="209fa-105">Yleiseen päiväkirjaan kirjataan tyypillisesti työntekijöiden liiketoimintaa varten käyttämät ovat varat myöhemmin hyvitettäväksi.</span><span class="sxs-lookup"><span data-stu-id="209fa-105">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="209fa-106">Lisätietoja on kohdassa [Työntekijöiden kulujen kirjaaminen ja hyvittäminen](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="209fa-106">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="209fa-107">Yleisiä päiväkirjoja käytetään rahoitustapahtumien kirjaamiseen suoraan kirjanpitotileille sekä muille tileille, kuten pankki-, asiakas-, toimittaja- ja työtekijätileille.</span><span class="sxs-lookup"><span data-stu-id="209fa-107">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="209fa-108">Yleisen päiväkirjan avulla kirjaaminen luo aina tapahtumia kirjanpitotileille.</span><span class="sxs-lookup"><span data-stu-id="209fa-108">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="209fa-109">Näin tapahtuu silloinkin, kun kirjataan esimerkiksi päiväkirjan rivi asiakkaan tilille, koska tapahtuma kirjataan pääkirjanpidon myyntisaamisten tilille kirjausryhmän kautta.</span><span class="sxs-lookup"><span data-stu-id="209fa-109">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="209fa-110">Voit mukauttaa yleistä päiväkirjaasi määrittämällä päiväkirjaerän tai -mallin.</span><span class="sxs-lookup"><span data-stu-id="209fa-110">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="209fa-111">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="209fa-111">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="209fa-112">Toisin kuin tapahtumat, jotka on kirjattu asiakirjasta ja edellyttävät hyvityslaskuprosessia, voit peruuttaa yleiseen päiväkirjaan kirjattuja tapahtumia oikein.</span><span class="sxs-lookup"><span data-stu-id="209fa-112">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="209fa-113">Lisätietoja on kohdassa [Kirjauksien peruuttaminen](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="209fa-113">For more information, see [Reverse Postings](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="209fa-114">Tapahtumien kirjaaminen suoraan pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="209fa-114">To post a transaction directly to a general ledger account</span></span>

1. <span data-ttu-id="209fa-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="209fa-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="209fa-116">Avaa liittyvä yleisen päiväkirjan erä.</span><span class="sxs-lookup"><span data-stu-id="209fa-116">Open the relevant general journal batch.</span></span> <span data-ttu-id="209fa-117">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="209fa-117">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="209fa-118">Täytä tarvittaessa uuden päiväkirjarivin kentät.</span><span class="sxs-lookup"><span data-stu-id="209fa-118">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="209fa-119">Toista vaihe 3 jokaiselle tapahtumalle, jonka haluat kirjata.</span><span class="sxs-lookup"><span data-stu-id="209fa-119">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="209fa-120">Jos haluat syöttää useita tapahtumarivejä yhden vastatilin rivin ylle, esimerkiksi yhdelle pankkitilille, valitse erän rivillä oleva **Ehdota vastasummaa** -valintaruutu **Yleisen päiväkirjan erät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="209fa-120">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="209fa-121">Tällöin vastatilin rivin **Summa**-kenttä täytetään automaattisesti arvolla, joka vaaditaan tapahtumien täsmäyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="209fa-121">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="209fa-122">Valitse **Kirjaa**-toiminto kirjataksesi tapahtumat määritetyille KP-tileille.</span><span class="sxs-lookup"><span data-stu-id="209fa-122">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="209fa-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="209fa-123">See Also</span></span>

[<span data-ttu-id="209fa-124">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="209fa-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="209fa-125">Työntekijöiden kulujen kirjaaminen ja hyvittäminen</span><span class="sxs-lookup"><span data-stu-id="209fa-125">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="209fa-126">Kirjausten peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="209fa-126">Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="209fa-127">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="209fa-127">Finance</span></span>](finance.md)  
<span data-ttu-id="209fa-128">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="209fa-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
