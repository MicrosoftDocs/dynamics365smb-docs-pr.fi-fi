---
title: Palkkatapahtumien tuominen| Microsoft Docs
description: "Voit hallita palkkoja tuomalla ja kirjaamalla taloustapahtumia palkka-aineiston toimittajalta pääkirjanpitoon palkanlaskennan laajennusta, kuten Ceridian tai Quickbooks."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 06/16/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 52ed67b2f2e08cbb2f4104c2b0c26f662212a9f4
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="import-payroll-transactions"></a><span data-ttu-id="911dd-103">Tuo palkkatapahtumat</span><span class="sxs-lookup"><span data-stu-id="911dd-103">Import Payroll Transactions</span></span>
<span data-ttu-id="911dd-104">Jotta palkanmaksut ja liittyvät tapahtumat voidaan käsitellä, palkanlaskennan tarjoajan tekemät rahoitustapahtumat on tuotava ja kirjattava pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="911dd-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span> <span data-ttu-id="911dd-105">Voit tehdä tämän tuomalla ensin palkanlaskennan tarjoajalta saadun csv-tiedoston **Yleinen päiväkirja** -ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="911dd-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="911dd-106">Linkitä sitten ulkoiset tilit palkanlaskentatiedostoon soveltuvissa KP-tileissä.</span><span class="sxs-lookup"><span data-stu-id="911dd-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="911dd-107">Kirjaa lopuksi palkkatapahtumat tilin yhdistämisen perusteella.</span><span class="sxs-lookup"><span data-stu-id="911dd-107">Lastly, you post the payroll transactions according to the account mapping.</span></span>

> [!NOTE]  
>   <span data-ttu-id="911dd-108">Palkanlaskennan tuonnin laajennus on oltava asennettuna ja käytössä, jotta tätä toimintoa voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="911dd-108">To use this functionality, an extension for payroll import must be installed and enabled.</span></span> <span data-ttu-id="911dd-109">Ceridian Payroll- ja Quickbooks Payroll -tiedostojen tuontilaajennuksen on asennettu valmiiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="911dd-109">The Ceridian Payroll and the Quickbooks Payroll File Import extensions are pre-installed in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="911dd-110">Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="911dd-110">For more information, see [Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md).</span></span>

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="911dd-111">Palkanlaskentatiedoston tuominen</span><span class="sxs-lookup"><span data-stu-id="911dd-111">To import a payroll file</span></span>
1. <span data-ttu-id="911dd-112">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="911dd-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="911dd-113">Valitse kyseessä olevan yleisen päiväkirjan erän **Tuo palkkatapahtumat** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="911dd-113">In the relevant general journal batch, choose the **Import Payroll Transactions** action.</span></span> <span data-ttu-id="911dd-114">Avustettu määritysopas aukeaa.</span><span class="sxs-lookup"><span data-stu-id="911dd-114">An assisted setup guide opens.</span></span>
3. <span data-ttu-id="911dd-115">Noudata **Tuo palkkatapahtumat** -ikkunan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="911dd-115">Follow the steps in the **Import Payroll Transactions** window.</span></span>

    > [!TIP]  
    >   <span data-ttu-id="911dd-116">Ulkoisen palkanlaskennan tietueiden yhdistämisvaiheessa tekemäsi yhdistykset KP-tileihin säilytetään, kun samat tietueet tuodaan takaisin.</span><span class="sxs-lookup"><span data-stu-id="911dd-116">In the step about mapping the external payroll records to your G/L accounts, the mappings that you make will be remembered next time the same records are imported.</span></span> <span data-ttu-id="911dd-117">Tämä säästää aikaa, sillä ei tarvitse täyttää manuaalisesti yleisen päiväkirjan **Tilinro**-kenttää aina, kun tuot toistuvia palkanlaskentatapahtumia.</span><span class="sxs-lookup"><span data-stu-id="911dd-117">This will save you time as you do not have to manually fill in the **Account No.** field in the general journal every time you have imported recurring payroll transactions.</span></span>   

    <span data-ttu-id="911dd-118">Kun napsautat ohjatun määritystoiminnon **OK**-painiketta, ohjelma täyttää **yleinen päiväkirja** -ikkunan palkanlaskennan tiedoston tapahtumilla sekä asiaankuuluvat tilit **KP-tili** -kenttiin opastetussa toiminnossa tekemiesi yhdistysten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="911dd-118">When you choose the **OK** button in the assisted setup guide, the **General Journal** window is filled with lines representing the transactions that the payroll file contains and with the relevant accounts prefilled in the **G/L Account** fields according to mappings you made in the guide.</span></span>
4. <span data-ttu-id="911dd-119">Muokkaa tai kirjaa päiväkirjarivit samalla tavalla kuin muille pääkirjanpidon tapahtumille.</span><span class="sxs-lookup"><span data-stu-id="911dd-119">Edit or post the journal lines as for any other general ledger transactions.</span></span> <span data-ttu-id="911dd-120">Lisätietoja on kohdassa [Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="911dd-120">For more information, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>   

## <a name="see-also"></a><span data-ttu-id="911dd-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="911dd-121">See Also</span></span>
[<span data-ttu-id="911dd-122">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="911dd-122">Finance</span></span>](finance.md)  
<span data-ttu-id="911dd-123">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="911dd-123">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="911dd-124">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="911dd-124">Working with General Journals</span></span>](ui-work-general-journals.md)  

