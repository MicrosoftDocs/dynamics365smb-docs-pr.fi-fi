---
title: "Käteisasiakkaiden määrittäminen | Microsoft Docs"
description: "Tässä ohjeaiheessa käsitellään vaiheet, joilla käteisellä maksava asiakas määritetään."
services: project-madeira
documentationcenter: 
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
ms.openlocfilehash: b904daec68261af855e789829791505e69f3f07a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-cash-customers"></a><span data-ttu-id="258e2-103">Käteisasiakkaiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="258e2-103">Set Up Cash Customers</span></span>
<span data-ttu-id="258e2-104">Laskua ei voi luoda ilman asiakasnumeroa.</span><span class="sxs-lookup"><span data-stu-id="258e2-104">You cannot create an invoice without a customer number.</span></span> <span data-ttu-id="258e2-105">Näin on, vaikka teet käteismyynnin, eikä asiakastilille ole mitään tallennettavaa.</span><span class="sxs-lookup"><span data-stu-id="258e2-105">This is true, even if you make a cash sale and do not have anything to record in a customer account.</span></span>  

## <a name="to-set-up-a-cash-customer"></a><span data-ttu-id="258e2-106">Käteisasiakkaiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="258e2-106">To set up a cash customer</span></span>  
1.  <span data-ttu-id="258e2-107">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="258e2-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="258e2-108">Luo uusi **Asiakkaan** kortti.</span><span class="sxs-lookup"><span data-stu-id="258e2-108">Create a new **Customer** card.</span></span> <span data-ttu-id="258e2-109">Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="258e2-109">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>
3.  <span data-ttu-id="258e2-110">Valitse **Nro**-kenttään</span><span class="sxs-lookup"><span data-stu-id="258e2-110">In the **No.**</span></span> <span data-ttu-id="258e2-111">esimerkiksi **Käteismyynti**.</span><span class="sxs-lookup"><span data-stu-id="258e2-111">field, enter **Cash**, for example.</span></span>  
4.  <span data-ttu-id="258e2-112">Syötä **Nimi**-kenttään esimerkiksi **Käteismyynti**.</span><span class="sxs-lookup"><span data-stu-id="258e2-112">In the **Name** field, enter **Cash Sale**, for example.</span></span>  
5.  <span data-ttu-id="258e2-113">Täytä **Laskutus**-pikavälilehden **Asiakkaan kirjausryhmä**- ja **Ylein. liiketoim. kirjausryhmä** -kentät.</span><span class="sxs-lookup"><span data-stu-id="258e2-113">On the **Invoicing** FastTab, fill in the **Customer Posting Group** and the **Gen. Bus. Posting Group** fields.</span></span>  

 <span data-ttu-id="258e2-114">Nyt asiakas on määritetty, ja se sisältää riittävästi tietoa laskutusta varten.</span><span class="sxs-lookup"><span data-stu-id="258e2-114">Now you have set up a customer that contains sufficient information for invoicing.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="258e2-115">Olet voinut valita kirjausryhmän, jota on käytetty myös kotimaisiin luottomyynteihin.</span><span class="sxs-lookup"><span data-stu-id="258e2-115">You may have chosen a posting group that is also used for domestic credit sales.</span></span> <span data-ttu-id="258e2-116">Jos haluat ylläpitää erillistä tietoa käteismyynneistä esimerkiksi erityisellä myynti- tai myyntisaamistilillä, voit määrittää tätä varten ylimääräisen kirjausryhmän.</span><span class="sxs-lookup"><span data-stu-id="258e2-116">If you want to maintain separate data on cash sales, for example, with a special sales or receivables account, you can set up an extra posting group for this purpose.</span></span>  
>   
>  <span data-ttu-id="258e2-117">Myyntisaamistilille täytyy syöttää numero kirjausryhmää varten, vaikka tilin saldo on aina 0 laskun kirjaamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="258e2-117">You must enter a number for a receivables account for the posting group, even though the balance in this account will always be 0 after you post an invoice.</span></span>  

## <a name="see-also"></a><span data-ttu-id="258e2-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="258e2-118">See Also</span></span>
[<span data-ttu-id="258e2-119">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="258e2-119">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="258e2-120">[Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md)  </span><span class="sxs-lookup"><span data-stu-id="258e2-120">[Register New Customers](sales-how-register-new-customers.md)  </span></span>  
[<span data-ttu-id="258e2-121">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="258e2-121">Finance</span></span>](finance.md)  


