---
title: Business Central -sovelluksen SEPA-suoraveloitus | Microsoft Docs
description: "Voit periä maksut suoraan asiakkaan pankkitililtä SEPA-muodon mukaisesti."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 557d6411540cc778a8f6810e747d4113fccd8f4c
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="collecting-payments-with-sepa-direct-debit"></a><span data-ttu-id="eee51-103">Maksujen periminen SEPA-suoraveloituksena</span><span class="sxs-lookup"><span data-stu-id="eee51-103">Collecting Payments with SEPA Direct Debit</span></span>
<span data-ttu-id="eee51-104">Asiakkaan suostumuksella voit kerätä maksut suoraan asiakkaan pankkitililtä SEPA-muodon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="eee51-104">With your customer’s consent, you can collect payments directly from the customer’s bank account according to the SEPA format.</span></span>  

 <span data-ttu-id="eee51-105">Määritä ensin pankkitiedoston vientimuoto, joka ohjaa pankkia suorittamaan suoraveloituksen.</span><span class="sxs-lookup"><span data-stu-id="eee51-105">First, set up the export format of the bank file that instructs your bank to perform a direct debit.</span></span> <span data-ttu-id="eee51-106">Määritä sitten asiakkaan maksutapa.</span><span class="sxs-lookup"><span data-stu-id="eee51-106">Then, set up the customer’s payment method.</span></span> <span data-ttu-id="eee51-107">Määritä lopuksi asiakkaasi kanssa sovitun mukainen suoraveloitusvaltakirja, jolla heidän maksunsa peritään tietyllä sopimusjaksolla.</span><span class="sxs-lookup"><span data-stu-id="eee51-107">Last, set up the direct-debit mandate that reflects your agreement with the customer to collect their payments in a certain agreement period.</span></span>  

 <span data-ttu-id="eee51-108">Jos haluat ohjata pankkia siirtämään maksusumman asiakkaan pankkitililtä yrityksesi tilille, loit suoraveloitusperintämerkinnän, joka säilyttää tiedot pankkitileistä ja kyseessä olevista myyntilaskuista sekä suoraveloitusvaltakirjasta.</span><span class="sxs-lookup"><span data-stu-id="eee51-108">To instruct the bank to transfer the payment amount from the customer’s bank account to your company’s account, you create a direct-debit collection entry, which holds information about bank accounts, the affected sales invoices, and the direct-debit mandate.</span></span> <span data-ttu-id="eee51-109">Syntyvästä suoraveloitusperintämerkinnästä viet sitten perintämerkintään perustuvan XML-tiedoston, jonka lähetät tai lataat verkkopankkiin käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="eee51-109">You then export an XML file that is based on the collection entry, which you send to your bank for processing.</span></span> <span data-ttu-id="eee51-110">Kaikista maksuista, joita ei voitu käsitellä, tiedotetaan sinulle pankin toimesta. Sinun täytyy sitten manuaalisesti hylätä kyseessä olevat suoraveloitusmerkinnät.</span><span class="sxs-lookup"><span data-stu-id="eee51-110">Any payments that could not be processed will be communicated to you by your bank, and you must then manually reject the direct debit-collection entries in question.</span></span>  

 <span data-ttu-id="eee51-111">Voit määrittää vakioasiakasmyyntikoodin suoraveloitusmaksumenetelmällä ja valtakirjatiedoilla.</span><span class="sxs-lookup"><span data-stu-id="eee51-111">You can set up standard customer sales codes with the direct-debit payment method and mandate information.</span></span> <span data-ttu-id="eee51-112">Voit sitten käyttää **Luo vakioasiakaslaskut** -eräajoa ja luoda useita myyntilaskuja, joissa suoraveloitustiedot on täytetty valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="eee51-112">You can then use the **Create Standard Cust. Invoices** batch job to generate multiple sales invoices with the direct-debit information prefilled.</span></span> <span data-ttu-id="eee51-113">Tämä voidaan tehdä manuaalisesti tai automaattisesti maksun eräpäivän mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="eee51-113">This is can be done manually or automatically, according to the payment due date.</span></span>  

 <span data-ttu-id="eee51-114">Kun maksut on käsitelty onnistuneesti pankin tiedottamalla tavalla, voit kirjata maksukuitit joko suoraan **Suoraveloitusperintätapahtumat**-ikkunassa tai siirtää maksurivit päiväkirjaan, johon kirjaat maksukuitit, kuten **Kassapäiväkirja**-ikkuna.</span><span class="sxs-lookup"><span data-stu-id="eee51-114">When payments are successfully processed, as communicated by your bank, you can post the payment receipts either directly from the **Direct Debit Collect. Entries** window or by moving the payment lines to the journal where you post payment receipts, such as the **Cash Receipt Journal** window.</span></span> <span data-ttu-id="eee51-115">Vaihtoehtoisesti kassanhallintamenetelmästäsi riippuen, voit odottaa ja kohdistaa maksut osana pankin täsmäytystä.</span><span class="sxs-lookup"><span data-stu-id="eee51-115">Alternatively, depending on your cash management process, you can wait and just apply the payments as a part of bank reconciliation.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="eee51-116">Kun maksut kerätään SEPA-suoraveloituksen avulla, myyntilaskun valuutan on oltava EURO.</span><span class="sxs-lookup"><span data-stu-id="eee51-116">To collect payments using SEPA Direct Debit, the currency on the sales invoice must be EURO.</span></span>  

 <span data-ttu-id="eee51-117">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="eee51-117">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="eee51-118">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="eee51-118">**To**</span></span>|<span data-ttu-id="eee51-119">**Katso**</span><span class="sxs-lookup"><span data-stu-id="eee51-119">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="eee51-120">Valmistele pankkitilimuodot, maksutavat ja asiakkaan SEPA-suoraveloitussopimukset.</span><span class="sxs-lookup"><span data-stu-id="eee51-120">Prepare bank account formats, payment methods, and customer agreements for SEPA direct debit.</span></span>|[<span data-ttu-id="eee51-121">SEPA-suoraveloituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="eee51-121">Set Up SEPA Direct Debit</span></span>](finance-how-to-set-up-sepa-direct-debit.md)|  
|<span data-ttu-id="eee51-122">Ohjeista pankkisi siirtämään maksusummat asiakkaan pankkitileiltä yrityksesi pankkitilille SEPA-suoraveloitusasetustesi mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="eee51-122">Instruct your bank to transfer payment amounts from your customers’ bank accounts to your company’s account according to your setup of SEPA direct debit.</span></span>|[<span data-ttu-id="eee51-123">SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon</span><span class="sxs-lookup"><span data-stu-id="eee51-123">Create SEPA Direct Debit Collection Entries and Export to a Bank File</span></span>](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|<span data-ttu-id="eee51-124">Määritä asiakkaan vakiomyyntikoodit suoraveloituslaskuille ja luo myyntilaskuja suoraveloitustiedoilla, kun laskut erääntyvät maksettavaksi.</span><span class="sxs-lookup"><span data-stu-id="eee51-124">Set up standard customer sales codes for direct-debit invoices and generate sales invoices with direct-debit information when the invoices are due for payment.</span></span>|[<span data-ttu-id="eee51-125">Toistuvien myynti- ja ostorivien luominen</span><span class="sxs-lookup"><span data-stu-id="eee51-125">Create Recurring Sales and Purchase Lines</span></span>](sales-how-work-standard-lines.md)|  
|<span data-ttu-id="eee51-126">Kirjaa SEPA-suoraveloituksina suoritetut maksut.</span><span class="sxs-lookup"><span data-stu-id="eee51-126">Post payments made as SEPA direct debits.</span></span>|[<span data-ttu-id="eee51-127">SEPA-suoraveloitusmaksujen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="eee51-127">Post SEPA Direct Debit Payment Receipts</span></span>](finance-how-to-post-sepa-direct-debit-payment-receipts.md)|  

## <a name="see-also"></a><span data-ttu-id="eee51-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="eee51-128">See Also</span></span>  
[<span data-ttu-id="eee51-129">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="eee51-129">Managing Receivables</span></span>](receivables-manage-receivables.md)

