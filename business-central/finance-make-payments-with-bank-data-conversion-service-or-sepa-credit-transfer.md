---
title: Maksujen suorittaminen pankkitietojen muunnospalvelulla tai SEPA-tilisiirrolla | Microsoft Docs
description: "Käsittele maksut toimittajille viemällä tiedoston yhdessä maksutietojen kanssa päiväkirjan riveiltä."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1e0c88184d2b453e9eb3d31a2b140fbe9002d849
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="making-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a><span data-ttu-id="7dac4-103">Maksujen suorittaminen pankkitietojen muunnospalvelulla tai SEPA-tilisiirrolla</span><span class="sxs-lookup"><span data-stu-id="7dac4-103">Making Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>
<span data-ttu-id="7dac4-104">**Maksupäiväkirja**-ikkunassa voit käsitellä maksut toimittajillesi viemällä tiedoston yhdessä maksutietojen kanssa päiväkirjan riveiltä.</span><span class="sxs-lookup"><span data-stu-id="7dac4-104">In the **Payment Journal** window, you can process payments to your vendors by exporting a file together with the payment information from the journal lines.</span></span> <span data-ttu-id="7dac4-105">Voit sitten ladata tiedoston verkkopankkiin, jossa liittyvät rahansiirrot käsitellään.</span><span class="sxs-lookup"><span data-stu-id="7dac4-105">You can then upload the file to your electronic bank where the related money transfers are processed.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="7dac4-106">tukee SEPA-hyvitysten siirtomuotoa, mutta maa- tai aluekohtaisesti voi olla käytettävissä muita sähköisiä maksumuotoja.</span><span class="sxs-lookup"><span data-stu-id="7dac4-106"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>   

 <span data-ttu-id="7dac4-107">Kun haluat ottaa SEPA-hyvityksen siirrot käyttöön, määritä ensin pankkitili, toimittaja ja yleinen päiväkirja, johon maksupäiväkirja perustuu.</span><span class="sxs-lookup"><span data-stu-id="7dac4-107">To enable SEPA credit transfers, you must first set up a bank account, a vendor, and the general journal batch that the payment journal is based on.</span></span> <span data-ttu-id="7dac4-108">Tämän jälkeen maksut valmistellaan toimittajia varten automaattisesti täyttämällä erääntyneet maksut ja määritetyt kirjauspäivämäärät **Maksupäiväkirja**-ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="7dac4-108">You then prepare payments to vendors by automatically filling the **Payment Journal** window with due payments with specified posting dates.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="7dac4-109">Kun olet varmistanut, että pankki on käsitellyt maksut onnistuneesti, voit jatkaa maksupäiväkirjan rivien kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="7dac4-109">When you have verified that the payments are successfully processed by the bank, you can proceed to post the payment journal lines.</span></span>  

 <span data-ttu-id="7dac4-110">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="7dac4-110">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="7dac4-111">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="7dac4-111">**To**</span></span>|<span data-ttu-id="7dac4-112">**Katso**</span><span class="sxs-lookup"><span data-stu-id="7dac4-112">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="7dac4-113">Voit aktivoida pankkitietojen muuntopalvelun minkä tahansa pankin tiliotteen muuttamiseksi tuotavaan muotoon, tai voit muuttaa viedyt maksutiedostot pankkisi vaatimaan muotoon.</span><span class="sxs-lookup"><span data-stu-id="7dac4-113">Activate the Bank Data Conversion Service feature to have any bank statement file converted to a format that you can import or to have your exported payment files converted to the format that your bank requires.</span></span>|[<span data-ttu-id="7dac4-114">Pankkitietojen muuntopalvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7dac4-114">Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)|  
|<span data-ttu-id="7dac4-115">Määritä pankkitili, myyjä ja maksuloki SEPA-tilisiirrolle.</span><span class="sxs-lookup"><span data-stu-id="7dac4-115">Set up a bank account, a vendor, and a payment journal for SEPA credit transfer.</span></span>|[<span data-ttu-id="7dac4-116">SEPA-hyvityksen siirron määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7dac4-116">Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)|  
|<span data-ttu-id="7dac4-117">Täytä maksupäiväkirja toimittajiin kohdistuvilla erääntyvillä maksuriveillä ja vaihtoehdolla lisätä kirjauspäivämäärät perustuen liittyvien ostoasiakirjojen eräpäivään.</span><span class="sxs-lookup"><span data-stu-id="7dac4-117">Fill the payment journal with lines for due payments to vendors, with the option to insert posting dates based on the due date of the related purchase documents.</span></span>|[<span data-ttu-id="7dac4-118">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="7dac4-118">Managing Payables</span></span>](payables-manage-payables.md)|  
|<span data-ttu-id="7dac4-119">Vie maksupäiväkirjan rivit tiedostoon SEPA-hyvityksen siirtomuodossa.</span><span class="sxs-lookup"><span data-stu-id="7dac4-119">Export payment journal lines to a file in the SEPA Credit Transfer format.</span></span>|[<span data-ttu-id="7dac4-120">Maksujen vienti pankkitiedostoon</span><span class="sxs-lookup"><span data-stu-id="7dac4-120">Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  
|<span data-ttu-id="7dac4-121">Kirjaa maksut sen jälkeen, kun pankki on käsitellyt ne onnistuneesti.</span><span class="sxs-lookup"><span data-stu-id="7dac4-121">When the electronic payment is successfully processed by the bank, post the payments.</span></span>|[<span data-ttu-id="7dac4-122">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="7dac4-122">Working with General Journals</span></span>](ui-work-general-journals.md)|  

## <a name="see-also"></a><span data-ttu-id="7dac4-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7dac4-123">See Also</span></span>  
[<span data-ttu-id="7dac4-124">Pankkitietojen muuntopalvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7dac4-124">Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="7dac4-125">SEPA-hyvityksen siirron määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7dac4-125">Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)  
<span data-ttu-id="7dac4-126">[Ostovelkojen hallinta](payables-manage-payables.md) </span><span class="sxs-lookup"><span data-stu-id="7dac4-126">[Managing Payables](payables-manage-payables.md) </span></span>  
[<span data-ttu-id="7dac4-127">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="7dac4-127">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="7dac4-128">Maksujen kerääminen SEPA-suoraveloitusperintänä</span><span class="sxs-lookup"><span data-stu-id="7dac4-128">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)   

