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
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7fa0d6b604a60e000208287546d831690a914931
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="2c133-103">Tapahtumien kirjaaminen suoraan pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="2c133-103">How to: Post Transactions Directly to the General Ledger</span></span>
<span data-ttu-id="2c133-104">Useimmat rahoitustapahtumat kirjataan pääkirjanpitoon erityisten yritysasiakirjojen, kuten ostolaskujen ja myyntitilausten välityksellä.</span><span class="sxs-lookup"><span data-stu-id="2c133-104">Most financial transactions are posted to the general ledger through dedicated business documents, such as purchase invoices and sales orders.</span></span> <span data-ttu-id="2c133-105">Liiketoiminnan aktiviteeteille, joihin ei liity [!INCLUDE[d365fin](includes/d365fin_md.md)]-asiakirjaa, kuten pienille kuluille tai käteissuorituksille voi luoda liittyvät tapahtumat kirjaamalla päiväkirjarivit **Yleinen päiväkirja** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="2c133-105">For business activities that are not represented by a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as smaller expenses or cash receipts, you can create the related transactions by posting journal lines in the **General Journal** window.</span></span>

<span data-ttu-id="2c133-106">Yleisiä päiväkirjoja käytetään rahoitustapahtumien kirjaamisessa suoraan kirjanpitotileille sekä muille tileille, kuten pankki-, asiakas- ja toimittajatileille.</span><span class="sxs-lookup"><span data-stu-id="2c133-106">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, and vendor accounts.</span></span> <span data-ttu-id="2c133-107">Yleisen päiväkirjan avulla kirjaaminen luo aina tapahtumia kirjanpitotileille.</span><span class="sxs-lookup"><span data-stu-id="2c133-107">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="2c133-108">Näin tapahtuu silloinkin, kun kirjataan esimerkiksi päiväkirjan rivi asiakkaan tilille, koska tapahtuma kirjataan pääkirjanpidon myyntisaamisten tilille kirjausryhmän kautta.</span><span class="sxs-lookup"><span data-stu-id="2c133-108">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="2c133-109">Voit mukauttaa yleistä päiväkirjaasi määrittämällä päiväkirjaerän tai -mallin.</span><span class="sxs-lookup"><span data-stu-id="2c133-109">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="2c133-110">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="2c133-110">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="2c133-111">Toisin kuin tapahtumat, jotka on kirjattu asiakirjasta ja edellyttävät hyvityslaskuprosessia, voit peruuttaa yleiseen päiväkirjaan kirjattuja tapahtumia oikein.</span><span class="sxs-lookup"><span data-stu-id="2c133-111">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="2c133-112">Lisätietoja on kohdassa [Päiväkirjakirjauksien peruuttaminen](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="2c133-112">For more information, see [How to: Reverse Journal Posting](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="2c133-113">Tapahtumien kirjaaminen suoraan pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="2c133-113">To post a transaction directly to a general ledger account</span></span>
1. <span data-ttu-id="2c133-114">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2c133-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="2c133-115">Avaa liittyvä yleisen päiväkirjan erä.</span><span class="sxs-lookup"><span data-stu-id="2c133-115">Open the relevant general journal batch.</span></span> <span data-ttu-id="2c133-116">Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="2c133-116">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="2c133-117">Täytä tarvittaessa uuden päiväkirjarivin kentät.</span><span class="sxs-lookup"><span data-stu-id="2c133-117">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. <span data-ttu-id="2c133-118">Toista vaihe 3 jokaiselle tapahtumalle, jonka haluat kirjata.</span><span class="sxs-lookup"><span data-stu-id="2c133-118">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="2c133-119">Jos haluat syöttää useita tapahtumarivejä yhden vastatilin rivin ylle, esimerkiksi yhdelle pankkitilille, valitse erän rivillä oleva **Ehdota vastasummaa** -valintaruutu **Yleisen päiväkirjan erät** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="2c133-119">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch in the **General Journal Batches** window.</span></span> <span data-ttu-id="2c133-120">Tällöin vastatilin rivin **Summa**-kenttä täytetään automaattisesti arvolla, joka vaaditaan tapahtumien täsmäyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="2c133-120">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="2c133-121">Valitse **Kirjaa**-toiminto kirjataksesi tapahtumat määritetyille KP-tileille.</span><span class="sxs-lookup"><span data-stu-id="2c133-121">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c133-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2c133-122">See Also</span></span>
[<span data-ttu-id="2c133-123">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="2c133-123">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="2c133-124">Päiväkirjakirjauksen peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="2c133-124">How to: Reverse Journal Posting</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="2c133-125">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="2c133-125">Finance</span></span>](finance.md)  
<span data-ttu-id="2c133-126">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2c133-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

