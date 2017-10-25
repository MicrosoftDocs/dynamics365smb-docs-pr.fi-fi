---
title: "Sähköisten maksujen maksutavan valitseminen | Microsoft Docs"
description: "Käsittele maksut toimittajille viemällä tiedoston yhdessä maksutietojen kanssa päiväkirjan riveiltä."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 20ae505bc76b8971c678de9e2664653aa5032d6e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/27/2017

---
# <a name="make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a><span data-ttu-id="718d8-103">Suorita maksut pankkitietojen muunnospalvelulla tai SEPA-hyvityksen siirrolla</span><span class="sxs-lookup"><span data-stu-id="718d8-103">Make Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>
<span data-ttu-id="718d8-104">**Maksupäiväkirja**-ikkunassa voit käsitellä maksut toimittajillesi viemällä tiedoston yhdessä maksutietojen kanssa päiväkirjan riveiltä.</span><span class="sxs-lookup"><span data-stu-id="718d8-104">In the **Payment Journal** window, you can process payments to your vendors by exporting a file together with the payment information from the journal lines.</span></span> <span data-ttu-id="718d8-105">Voit sitten ladata tiedoston verkkopankkiin, jossa liittyvät rahansiirrot käsitellään.</span><span class="sxs-lookup"><span data-stu-id="718d8-105">You can then upload the file to your electronic bank where the related money transfers are processed.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="718d8-106"> tukee SEPA-hyvitysten siirtomuotoa, mutta maa- tai aluekohtaisesti voi olla käytettävissä muita sähköisiä maksumuotoja.</span><span class="sxs-lookup"><span data-stu-id="718d8-106"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>   

 <span data-ttu-id="718d8-107">Kun haluat ottaa SEPA-hyvityksen siirrot käyttöön, määritä ensin pankkitili, toimittaja ja yleinen päiväkirja, johon maksupäiväkirja perustuu.</span><span class="sxs-lookup"><span data-stu-id="718d8-107">To enable SEPA credit transfers, you must first set up a bank account, a vendor, and the general journal batch that the payment journal is based on.</span></span> <span data-ttu-id="718d8-108">Tämän jälkeen maksut valmistellaan toimittajia varten automaattisesti täyttämällä erääntyneet maksut ja määritetyt kirjauspäivämäärät **Maksupäiväkirja**-ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="718d8-108">You then prepare payments to vendors by automatically filling the **Payment Journal** window with due payments with specified posting dates.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="718d8-109">Kun olet varmistanut, että pankki on käsitellyt maksut onnistuneesti, voit jatkaa maksupäiväkirjan rivien kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="718d8-109">When you have verified that the payments are successfully processed by the bank, you can proceed to post the payment journal lines.</span></span>  

 <span data-ttu-id="718d8-110">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="718d8-110">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="718d8-111">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="718d8-111">**To**</span></span>|<span data-ttu-id="718d8-112">**Katso**</span><span class="sxs-lookup"><span data-stu-id="718d8-112">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="718d8-113">Voit aktivoida pankkitietojen muuntopalvelun minkä tahansa pankin tiliotteen muuttamiseksi tuotavaan muotoon, tai voit muuttaa viedyt maksutiedostot pankkisi vaatimaan muotoon.</span><span class="sxs-lookup"><span data-stu-id="718d8-113">Activate the Bank Data Conversion Service feature to have any bank statement file converted to a format that you can import or to have your exported payment files converted to the format that your bank requires.</span></span>|[<span data-ttu-id="718d8-114">Toimintaohje: Pankkitietojen muuntopalvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="718d8-114">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)|  
|<span data-ttu-id="718d8-115">Määritä pankkitili, myyjä ja maksuloki SEPA-tilisiirrolle.</span><span class="sxs-lookup"><span data-stu-id="718d8-115">Set up a bank account, a vendor, and a payment journal for SEPA credit transfer.</span></span>|[<span data-ttu-id="718d8-116">Toimintaohje: SEPA-hyvityksen siirron määrittäminen</span><span class="sxs-lookup"><span data-stu-id="718d8-116">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)|  
|<span data-ttu-id="718d8-117">Täytä maksupäiväkirja toimittajiin kohdistuvilla erääntyvillä maksuriveillä ja vaihtoehdolla lisätä kirjauspäivämäärät perustuen liittyvien ostoasiakirjojen eräpäivään.</span><span class="sxs-lookup"><span data-stu-id="718d8-117">Fill the payment journal with lines for due payments to vendors, with the option to insert posting dates based on the due date of the related purchase documents.</span></span>|[<span data-ttu-id="718d8-118">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="718d8-118">Manage Payables</span></span>](payables-manage-payables.md)|  
|<span data-ttu-id="718d8-119">Vie maksupäiväkirjan rivit tiedostoon SEPA-hyvityksen siirtomuodossa.</span><span class="sxs-lookup"><span data-stu-id="718d8-119">Export payment journal lines to a file in the SEPA Credit Transfer format.</span></span>|[<span data-ttu-id="718d8-120">Toimintaohje: Maksujen vieminen pankkitiedostoon</span><span class="sxs-lookup"><span data-stu-id="718d8-120">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  
|<span data-ttu-id="718d8-121">Tarkista, mitkä maksut on viety ja mihin tiedostoihin.</span><span class="sxs-lookup"><span data-stu-id="718d8-121">Review which payments have been exported and into which files.</span></span>|<span data-ttu-id="718d8-122">Hyvityksen siirron rekisterit</span><span class="sxs-lookup"><span data-stu-id="718d8-122">Credit Transfer Registers</span></span>|  
|<span data-ttu-id="718d8-123">Kirjaa maksut sen jälkeen, kun pankki on käsitellyt ne onnistuneesti.</span><span class="sxs-lookup"><span data-stu-id="718d8-123">When the electronic payment is successfully processed by the bank, post the payments.</span></span>|[<span data-ttu-id="718d8-124">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="718d8-124">Working with General Journals</span></span>](ui-work-general-journals.md)|  

## <a name="see-also"></a><span data-ttu-id="718d8-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="718d8-125">See Also</span></span>  
[<span data-ttu-id="718d8-126">Toimintaohje: Pankkitietojen muuntopalvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="718d8-126">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="718d8-127">Toimintaohje: SEPA-hyvityksen siirron määrittäminen</span><span class="sxs-lookup"><span data-stu-id="718d8-127">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)  
<span data-ttu-id="718d8-128">[Ostovelkojen hallinta](payables-manage-payables.md) </span><span class="sxs-lookup"><span data-stu-id="718d8-128">[Manage Payables](payables-manage-payables.md) </span></span>  
[<span data-ttu-id="718d8-129">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="718d8-129">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="718d8-130">Maksujen kerääminen SEPA-suoraveloitusperintänä</span><span class="sxs-lookup"><span data-stu-id="718d8-130">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)   

