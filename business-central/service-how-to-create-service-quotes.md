---
title: Huoltotarjousten luominen | Microsoft Docs
description: '**Huoltotarjous**-sivulla voidaan luoda asiakirjoja, joihin syötetään tietoja asiakkaan pyynnöstä tehtävästä huoltonimikkeiden huollosta (korjauksesta tai ylläpidosta). Voit käyttää huoltotarjousta huoltotilauksen luonnoksena ja muuntaa tarjouksen sitten huoltotilaukseksi.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 44ffab92930237c5496860771f41b4951b15b0ff
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250662"
---
# <a name="create-service-quotes"></a><span data-ttu-id="340ad-104">Huoltotarjousten luominen</span><span class="sxs-lookup"><span data-stu-id="340ad-104">Create Service Quotes</span></span>
<span data-ttu-id="340ad-105">Huoltotarjoukset voidaan mieltää huoltotilausten pohjaksi.</span><span class="sxs-lookup"><span data-stu-id="340ad-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="340ad-106">Ne ovatkin itse asiassa lähes samanlaisia.</span><span class="sxs-lookup"><span data-stu-id="340ad-106">In fact, they are almost identical.</span></span> <span data-ttu-id="340ad-107">Kummassakin on tietoja esimerkiksi asiakkaasta, tilaustyypistä, huollettavista nimikkeistä, laskutus- ja toimitustiedoista sekä tehtävästä huoltotyöstä.</span><span class="sxs-lookup"><span data-stu-id="340ad-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="340ad-108">Voit käyttää huoltotarjousta huoltotilauksen luonnoksena ja muuntaa tarjouksen sitten huoltotilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="340ad-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="340ad-109">Huoltotarjousten luominen</span><span class="sxs-lookup"><span data-stu-id="340ad-109">To create a service quote</span></span>  
1. <span data-ttu-id="340ad-110">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotarjoukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="340ad-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="340ad-111">Luo uusi huoltotarjous.</span><span class="sxs-lookup"><span data-stu-id="340ad-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="340ad-112">Valitse **Nro**-kenttään</span><span class="sxs-lookup"><span data-stu-id="340ad-112">In the **No.**</span></span> <span data-ttu-id="340ad-113">numero huoltotarjoukselle.</span><span class="sxs-lookup"><span data-stu-id="340ad-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="340ad-114">Vaihtoehtoisesti jos olet määrittänyt huoltotarjouksille numerosarjan **Huoltohallinnon asetukset** -sivulla, voit painaa Enter, jolloin ohjelma syöttää seuraavan saatavilla olevan huoltotarjouksen numeron.</span><span class="sxs-lookup"><span data-stu-id="340ad-114">Alternatively, if you have set up a number series for service quotes on the **Service Mgt. Setup** page, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="340ad-115">Syötä **Asiakasnro** -kentässä</span><span class="sxs-lookup"><span data-stu-id="340ad-115">In the **Customer No.**</span></span>  <span data-ttu-id="340ad-116">asiamukainen asiakas luettelosta.</span><span class="sxs-lookup"><span data-stu-id="340ad-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="340ad-117">Ohjelma täyttää automaattisesti asiakkaaseen liittyvät kentät tiedoilla **Asiakas**-kortilta.</span><span class="sxs-lookup"><span data-stu-id="340ad-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="340ad-118">Jos asiakkaalla ei ole **asiakkaan** korttia ja asiakasmalli on määritetty, voit luoda asiakkaan huoltotarjouksesta.</span><span class="sxs-lookup"><span data-stu-id="340ad-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="340ad-119">Täytä tarvittavat kentät ja valitse **Luo asiakas** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="340ad-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="340ad-120">**Huoltohallinnon asetukset** -sivun **Pakolliset kentät** -pikavälilehden asetusten mukaan **Huoltotilauksen tyyppi** -kenttä ja **Myyjäkoodi**-kenttä on ehkä täytettävä.</span><span class="sxs-lookup"><span data-stu-id="340ad-120">Depending on the settings on the **Mandatory Fields** FastTab on the **Service Mgt. Setup** page, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="340ad-121">Täytä huoltonimikerivit.</span><span class="sxs-lookup"><span data-stu-id="340ad-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="340ad-122">Rekisteröi arvioidut kustannukset huoltoriveille</span><span class="sxs-lookup"><span data-stu-id="340ad-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="340ad-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="340ad-123">See Also</span></span>  
[<span data-ttu-id="340ad-124">Huoltotilausten luominen</span><span class="sxs-lookup"><span data-stu-id="340ad-124">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="340ad-125">Huoltotehtävien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="340ad-125">Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 