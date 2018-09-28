---
title: Asiakirjojen hallinta, poistaminen tai pakkaaminen | Microsoft Docs
description: "Säilytä vanhat historiatiedot tai poista ne."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 01b20f74d631a81085ffcaf205dd556c54d6369c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="manage-documents"></a><span data-ttu-id="894a4-103">Asiakirjojen hallinta</span><span class="sxs-lookup"><span data-stu-id="894a4-103">Manage Documents</span></span>
<span data-ttu-id="894a4-104">Keskitetyn roolin, kuten sovelluksen järjestelmänvalvojan, on huolehdittava säännöllisesti siitä, että vanhat asiakirjat joko poistetaan tai tiivistetään.</span><span class="sxs-lookup"><span data-stu-id="894a4-104">A central role, such as the application administrator, must regularly deal with accumulating historic documents by deleting or compressing them.</span></span>  

## <a name="delete-documents"></a><span data-ttu-id="894a4-105">Asiakirjojen poistaminen</span><span class="sxs-lookup"><span data-stu-id="894a4-105">Delete Documents</span></span>
<span data-ttu-id="894a4-106">Jossain tapauksissa voi olla tarpeen poistaa laskutettuja ostotilauksia, joita ei ole poistettu.</span><span class="sxs-lookup"><span data-stu-id="894a4-106">In certain situations, you may need to delete invoiced purchase orders that have not been deleted.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="894a4-107">tarkistaa, että poistetut ostotilaukset on laskutettu kokonaan.</span><span class="sxs-lookup"><span data-stu-id="894a4-107"> checks that you have fully invoiced the deleted purchase orders.</span></span> <span data-ttu-id="894a4-108">Tilauksia, joita ei ole kokonaan laskutettu ja vastaanotettu, ei voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="894a4-108">You cannot delete orders that you have not fully invoiced and received.</span></span>  

<span data-ttu-id="894a4-109">Ohjelma poistaa palautustilaukset tavallisesti sen jälkeen, kun ne on laskutettu.</span><span class="sxs-lookup"><span data-stu-id="894a4-109">Return orders are usually deleted after they are invoiced.</span></span> <span data-ttu-id="894a4-110">Kun kirjaat laskun, se siirretään **Kirjattu ostohyvityslasku** -ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="894a4-110">When you post an invoice, it is transferred to the **Posted Purchase Credit Memo** window.</span></span> <span data-ttu-id="894a4-111">Jos kuitenkin olet valinnut  **Palautustoimitus hyvityslaskutettaessa** -valintaruudun **Ostojen ja ostovelkojen asetukset** -ikkunassa, lasku siirretään **Kirjattu palautustoimitus** -ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="894a4-111">If you selected the **Return Shipment on Credit Memo** check box in the **Purchases & Payable Setup** window, then the invoice is transferred to the **Posted Return Shipment** window.</span></span> <span data-ttu-id="894a4-112">Voit poistaa asiakirjat **Poista laskutetut ostopal.til.** -eräajolla.</span><span class="sxs-lookup"><span data-stu-id="894a4-112">You can delete the documents using the **Delete Invd Purch. Ret. Orders** batch job.</span></span> <span data-ttu-id="894a4-113">Eräajo tarkistaa ennen poistamista, onko ostopalautustilaukset toimitettu ja laskutettu kokonaan.</span><span class="sxs-lookup"><span data-stu-id="894a4-113">Before deleting, the batch job checks if the purchase return orders are fully shipped and invoiced.</span></span>  

<span data-ttu-id="894a4-114">Puiteostotilauksia ei poisteta sen jälkeen, kun kaikki liittyvät ostotilaukset on käsitelty ja laskutettu.</span><span class="sxs-lookup"><span data-stu-id="894a4-114">Blanket purchase orders are not deleted after you have processed and invoiced all the related purchase orders.</span></span> <span data-ttu-id="894a4-115">Puitetilaukset voi poistaa **Poista lask. puiteostotilaukset** -eräajolla.</span><span class="sxs-lookup"><span data-stu-id="894a4-115">You can delete blanket orders with the **Delete Invoiced Blanket Purchase Orders** batch job.</span></span>  

<span data-ttu-id="894a4-116">Laskutetut huoltotilaukset poistetaan ohjelmasta automaattisesti sen jälkeen, kun ne on laskutettu kokonaan.</span><span class="sxs-lookup"><span data-stu-id="894a4-116">Invoiced service orders are usually deleted automatically after having been fully invoiced.</span></span> <span data-ttu-id="894a4-117">Kun lasku on kirjattu, vastaava tapahtuma luodaan **Kirjatut huoltolaskut** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="894a4-117">When an invoice is posted, a corresponding entry is created in the **Posted Service Invoices** window.</span></span> <span data-ttu-id="894a4-118">Kirjattua asiakirjaa voi katsella **Kirjattu huoltolasku** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="894a4-118">The posted document can be viewed in the **Posted Service Invoice** window.</span></span>  

<span data-ttu-id="894a4-119">Ohjelma ei poista huoltotilauksia automaattisesti, jos tilauksen kokonaismäärä on kirjattu **Huoltolasku**-ikkunassa itse huoltotilauksen sijaan.</span><span class="sxs-lookup"><span data-stu-id="894a4-119">Service orders are not deleted automatically, however, if the total quantity on the order has been posted not from the service order itself, but from the **Service Invoice** window.</span></span> <span data-ttu-id="894a4-120">Tällöin sinun on ehkä poistettava laskutetut tilaukset, joita ei poistettu.</span><span class="sxs-lookup"><span data-stu-id="894a4-120">Then you may need to delete invoiced orders that were not deleted.</span></span> <span data-ttu-id="894a4-121">Voit tehdä sen suorittamalla **Poista laskutetut huoltotilaukset** -eräajon.</span><span class="sxs-lookup"><span data-stu-id="894a4-121">You can do this by running the **Delete Invoiced Service Orders** batch job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="894a4-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="894a4-122">See Also</span></span>  
[<span data-ttu-id="894a4-123">Hallinta</span><span class="sxs-lookup"><span data-stu-id="894a4-123">Administration</span></span>](admin-setup-and-administration.md)  

