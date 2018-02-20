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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 1f3f30673f8235377a581b398e1281fba92501e5
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="multiple-contracts"></a><span data-ttu-id="a1292-103">Useita sopimuksia</span><span class="sxs-lookup"><span data-stu-id="a1292-103">Multiple Contracts</span></span>
<span data-ttu-id="a1292-104">Asiakkaan kanssa tehtyjen huoltotasosopimusten mukaan sama huoltonimike on ehkä sisällytettävä useaan huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="a1292-104">Depending on your service level agreements with a customer, you may have to handle a service item under more than one service contract.</span></span>  
  
<span data-ttu-id="a1292-105">Sisällyttämällä huoltonimikkeen useaan sopimukseen voit tehdä seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="a1292-105">By handling a service item under multiple contracts, you can do the following:</span></span>  
  
* <span data-ttu-id="a1292-106">Tehdä samasta huoltonimikkeestä erilaisia sopimuksia.</span><span class="sxs-lookup"><span data-stu-id="a1292-106">Issue different contracts for the same service item.</span></span>  
* <span data-ttu-id="a1292-107">Huoltaa osat erikseen.</span><span class="sxs-lookup"><span data-stu-id="a1292-107">Service parts separately.</span></span>  
* <span data-ttu-id="a1292-108">Ottaa huomioon huoltonimikkeen eri osien, kuten mekaanisten osien ja ohjelmiston, huollon vaatimat eri taidot.</span><span class="sxs-lookup"><span data-stu-id="a1292-108">Consider different skills that are required to service different aspects of a service item, such as mechanical components and software.</span></span>  
* <span data-ttu-id="a1292-109">Määrittää huoltonimikkeen eri osien huollolle eri vastausajat ja tiheydet.</span><span class="sxs-lookup"><span data-stu-id="a1292-109">Specify different response times and frequencies in servicing different parts of a service item.</span></span>  
* <span data-ttu-id="a1292-110">Ottaa huomioon huoltonimikkeelle tehtävät erilaiset toimenpiteet, kun huoltonimike vaatii erityyppistä huolto eri aikoina.</span><span class="sxs-lookup"><span data-stu-id="a1292-110">Address different kinds of activities to be performed on a service item when the service item requires different types of service in different time periods.</span></span>  
* <span data-ttu-id="a1292-111">Valita ja määrittää huoltonimikeriville oikean sopimusnumero huoltotilausta luotaessa.</span><span class="sxs-lookup"><span data-stu-id="a1292-111">Select and assign an appropriate contract number to a service item line when you are creating a service order.</span></span>  
* <span data-ttu-id="a1292-112">Käsitellä huoltonimikkeiden ja huoltotasosopimusten taloudellisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="a1292-112">Handle relevant financial information about service items and service level agreements.</span></span>  
  
<span data-ttu-id="a1292-113">Seuraavassa on esimerkkejä usean sopimuksen käyttämisestä:</span><span class="sxs-lookup"><span data-stu-id="a1292-113">You can consider the following examples of using the multiple contracts functionality.</span></span>  
  
## <a name="creating-multiple-contracts-per-service-item"></a><span data-ttu-id="a1292-114">Usean sopimuksen luominen huoltonimikkeelle</span><span class="sxs-lookup"><span data-stu-id="a1292-114">Creating Multiple Contracts per Service Item</span></span>  
<span data-ttu-id="a1292-115">Huoltonimikkeille, jotka on jo rekisteröity saman asiakkaan ei-peruutettuihin sopimuksiin, voidaan luoda manuaalisesti huoltosopimus tai huoltotarjous.</span><span class="sxs-lookup"><span data-stu-id="a1292-115">You can manually create a service contract or contract quote for service items already registered in non-canceled contracts owned by the same customer.</span></span> <span data-ttu-id="a1292-116">Tämä tehdään noudattamalla normaalia huoltosopimusten ja huoltosopimustarjousten luontiprosessia.</span><span class="sxs-lookup"><span data-stu-id="a1292-116">To do this, follow the standard procedure of creating service contracts and service contract quotes.</span></span> <span data-ttu-id="a1292-117">Lisätietoja on kohdassa [Huoltosopimusten ja huoltosopimustarjousten käyttäminen](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span><span class="sxs-lookup"><span data-stu-id="a1292-117">For more information, see [Work with Service Contracts and Service Contract Quotes](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span></span>  
  
<span data-ttu-id="a1292-118">Kun toiseen huoltosopimukseen tai sopimustarjoukseen jo rekisteröity huoltonimike lisätään sopimusriville, ohjelma näyttää varoitussanoman, jossa varoitetaan, että huoltonimike kuuluu jo yhteen tai useaan huoltosopimukseen tai sopimustarjoukseen.</span><span class="sxs-lookup"><span data-stu-id="a1292-118">When you add a service item on a contract line that is registered in other service contracts or contract quotes, a warning message is displayed stating that the service item already belongs to one or more service contracts or contract quotes.</span></span> <span data-ttu-id="a1292-119">Jos sanoma vahvistetaan, järjestelmä kopioi kaikki tarvittavat huoltonimikkeen tiedot juuri luodulle sopimusriville.</span><span class="sxs-lookup"><span data-stu-id="a1292-119">If you confirm this message, all relevant service item information is copied to a newly created contract line.</span></span>  
  
## <a name="copying-documents"></a><span data-ttu-id="a1292-120">Asiakirjojen kopioiminen</span><span class="sxs-lookup"><span data-stu-id="a1292-120">Copying Documents</span></span>  
<span data-ttu-id="a1292-121">Toiseen huoltosopimukseen tai sopimustarjoukseen jo rekisteröidylle huoltonimikkeille voidaan luoda automaattisesti huoltosopimus tai sopimustarjous **Kopioi asiakirja** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="a1292-121">You can automatically create a service contract or contract quote for service items that are already registered in other service contracts or contract quotes by using the **Copy Document** action.</span></span>  
  
## <a name="creating-service-orders-for-multiple-contracts"></a><span data-ttu-id="a1292-122">Huoltotilausten luominen usealle sopimukselle</span><span class="sxs-lookup"><span data-stu-id="a1292-122">Creating Service Orders for Multiple Contracts</span></span>  
<span data-ttu-id="a1292-123">Useaan voimassa olevaa sopimukseen rekisteröidylle huoltonimikkeelle voidaan luoda huoltotilaus manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="a1292-123">You can manually create a service order for a service item that is registered in multiple active contracts.</span></span> <span data-ttu-id="a1292-124">Huoltosopimus on voimassa, kun se on allekirjoitettu, eikä se ole vielä vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="a1292-124">A service contract is active when it is signed and not expired.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1292-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a1292-125">See Also</span></span>  
[<span data-ttu-id="a1292-126">Huoltosopimusten toteuttaminen</span><span class="sxs-lookup"><span data-stu-id="a1292-126">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)  
[<span data-ttu-id="a1292-127">Huoltotilausten luominen</span><span class="sxs-lookup"><span data-stu-id="a1292-127">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  

