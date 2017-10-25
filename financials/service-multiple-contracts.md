---
title: Useat sopimukset | Microsoft Docs
description: "Asiakkaan kanssa tehtyjen huoltotasosopimusten mukaan saatetaan sama huoltonimike joutua sisällyttämään useaan huoltosopimukseen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c4abfbcb3bc182fa14c44c427bc41ebd9d67f6cf
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="multiple-contracts"></a><span data-ttu-id="106d2-103">Useita sopimuksia</span><span class="sxs-lookup"><span data-stu-id="106d2-103">Multiple Contracts</span></span>
<span data-ttu-id="106d2-104">Asiakkaan kanssa tehtyjen huoltotasosopimusten mukaan sama huoltonimike on ehkä sisällytettävä useaan huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="106d2-104">Depending on your service level agreements with a customer, you may have to handle a service item under more than one service contract.</span></span>  
  
<span data-ttu-id="106d2-105">Sisällyttämällä huoltonimikkeen useaan sopimukseen voit tehdä seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="106d2-105">By handling a service item under multiple contracts, you can do the following:</span></span>  
  
* <span data-ttu-id="106d2-106">Tehdä samasta huoltonimikkeestä erilaisia sopimuksia.</span><span class="sxs-lookup"><span data-stu-id="106d2-106">Issue different contracts for the same service item.</span></span>  
* <span data-ttu-id="106d2-107">Huoltaa osat erikseen.</span><span class="sxs-lookup"><span data-stu-id="106d2-107">Service parts separately.</span></span>  
* <span data-ttu-id="106d2-108">Ottaa huomioon huoltonimikkeen eri osien, kuten mekaanisten osien ja ohjelmiston, huollon vaatimat eri taidot.</span><span class="sxs-lookup"><span data-stu-id="106d2-108">Consider different skills that are required to service different aspects of a service item, such as mechanical components and software.</span></span>  
* <span data-ttu-id="106d2-109">Määrittää huoltonimikkeen eri osien huollolle eri vastausajat ja tiheydet.</span><span class="sxs-lookup"><span data-stu-id="106d2-109">Specify different response times and frequencies in servicing different parts of a service item.</span></span>  
* <span data-ttu-id="106d2-110">Ottaa huomioon huoltonimikkeelle tehtävät erilaiset toimenpiteet, kun huoltonimike vaatii erityyppistä huolto eri aikoina.</span><span class="sxs-lookup"><span data-stu-id="106d2-110">Address different kinds of activities to be performed on a service item when the service item requires different types of service in different time periods.</span></span>  
* <span data-ttu-id="106d2-111">Valita ja määrittää huoltonimikeriville oikean sopimusnumero huoltotilausta luotaessa.</span><span class="sxs-lookup"><span data-stu-id="106d2-111">Select and assign an appropriate contract number to a service item line when you are creating a service order.</span></span>  
* <span data-ttu-id="106d2-112">Käsitellä huoltonimikkeiden ja huoltotasosopimusten taloudellisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="106d2-112">Handle relevant financial information about service items and service level agreements.</span></span>  
  
<span data-ttu-id="106d2-113">Seuraavassa on esimerkkejä usean sopimuksen käyttämisestä:</span><span class="sxs-lookup"><span data-stu-id="106d2-113">You can consider the following examples of using the multiple contracts functionality.</span></span>  
  
## <a name="creating-multiple-contracts-per-service-item"></a><span data-ttu-id="106d2-114">Usean sopimuksen luominen huoltonimikkeelle</span><span class="sxs-lookup"><span data-stu-id="106d2-114">Creating Multiple Contracts per Service Item</span></span>  
<span data-ttu-id="106d2-115">Huoltonimikkeille, jotka on jo rekisteröity saman asiakkaan ei-peruutettuihin sopimuksiin, voidaan luoda manuaalisesti huoltosopimus tai huoltotarjous.</span><span class="sxs-lookup"><span data-stu-id="106d2-115">You can manually create a service contract or contract quote for service items already registered in non-canceled contracts owned by the same customer.</span></span> <span data-ttu-id="106d2-116">Tämä tehdään noudattamalla normaalia huoltosopimusten ja huoltosopimustarjousten luontiprosessia.</span><span class="sxs-lookup"><span data-stu-id="106d2-116">To do this, follow the standard procedure of creating service contracts and service contract quotes.</span></span> <span data-ttu-id="106d2-117">Lisätietoja on kohdassa [Toimintaohje: Huoltosopimusten ja huoltosopimustarjousten käyttäminen](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span><span class="sxs-lookup"><span data-stu-id="106d2-117">For more information, see [How to: Work with Service Contracts and Service Contract Quotes](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span></span>  
  
<span data-ttu-id="106d2-118">Kun toiseen huoltosopimukseen tai sopimustarjoukseen jo rekisteröity huoltonimike lisätään sopimusriville, ohjelma näyttää varoitussanoman, jossa varoitetaan, että huoltonimike kuuluu jo yhteen tai useaan huoltosopimukseen tai sopimustarjoukseen.</span><span class="sxs-lookup"><span data-stu-id="106d2-118">When you add a service item on a contract line that is registered in other service contracts or contract quotes, a warning message is displayed stating that the service item already belongs to one or more service contracts or contract quotes.</span></span> <span data-ttu-id="106d2-119">Jos sanoma vahvistetaan, järjestelmä kopioi kaikki tarvittavat huoltonimikkeen tiedot juuri luodulle sopimusriville.</span><span class="sxs-lookup"><span data-stu-id="106d2-119">If you confirm this message, all relevant service item information is copied to a newly created contract line.</span></span>  
  
## <a name="copying-documents"></a><span data-ttu-id="106d2-120">Asiakirjojen kopioiminen</span><span class="sxs-lookup"><span data-stu-id="106d2-120">Copying Documents</span></span>  
<span data-ttu-id="106d2-121">Toiseen huoltosopimukseen tai sopimustarjoukseen jo rekisteröidylle huoltonimikkeille voidaan luoda automaattisesti huoltosopimus tai sopimustarjous **Kopioi asiakirja** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="106d2-121">You can automatically create a service contract or contract quote for service items that are already registered in other service contracts or contract quotes by using the **Copy Document** action.</span></span>  
  
## <a name="creating-service-orders-for-multiple-contracts"></a><span data-ttu-id="106d2-122">Huoltotilausten luominen usealle sopimukselle</span><span class="sxs-lookup"><span data-stu-id="106d2-122">Creating Service Orders for Multiple Contracts</span></span>  
<span data-ttu-id="106d2-123">Useaan voimassa olevaa sopimukseen rekisteröidylle huoltonimikkeelle voidaan luoda huoltotilaus manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="106d2-123">You can manually create a service order for a service item that is registered in multiple active contracts.</span></span> <span data-ttu-id="106d2-124">Huoltosopimus on voimassa, kun se on allekirjoitettu, eikä se ole vielä vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="106d2-124">A service contract is active when it is signed and not expired.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="106d2-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="106d2-125">See Also</span></span>  
[<span data-ttu-id="106d2-126">Huoltosopimusten toteuttaminen</span><span class="sxs-lookup"><span data-stu-id="106d2-126">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)  
[<span data-ttu-id="106d2-127">Toimintaohje: Huoltotilausten luominen</span><span class="sxs-lookup"><span data-stu-id="106d2-127">How to: Create Service Orders</span></span>](service-how-to-create-service-orders.md)  

