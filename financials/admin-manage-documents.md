---
title: Asiakirjojen hallinta, poistaminen tai pakkaaminen | Microsoft Docs
description: "Säilytä vanhat historiatiedot tai poista ne."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 60438f0b6f0d5da60925b5b9c309cc359a8422e3
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="manage-documents"></a><span data-ttu-id="23efc-103">Asiakirjojen hallinta</span><span class="sxs-lookup"><span data-stu-id="23efc-103">Manage Documents</span></span>
<span data-ttu-id="23efc-104">Keskitetyn roolin, kuten sovelluksen järjestelmänvalvojan, on huolehdittava säännöllisesti siitä, että vanhat asiakirjat joko poistetaan tai tiivistetään.</span><span class="sxs-lookup"><span data-stu-id="23efc-104">A central role, such as the application administrator, must regularly deal with accumulating historic documents by deleting or compressing them.</span></span>  

## <a name="delete-documents"></a><span data-ttu-id="23efc-105">Asiakirjojen poistaminen</span><span class="sxs-lookup"><span data-stu-id="23efc-105">Delete Documents</span></span>
<span data-ttu-id="23efc-106">Jossain tapauksissa voi olla tarpeen poistaa laskutettuja ostotilauksia, joita ei ole poistettu.</span><span class="sxs-lookup"><span data-stu-id="23efc-106">In certain situations, you may need to delete invoiced purchase orders that have not been deleted.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="23efc-107"> tarkistaa, että poistetut ostotilaukset on laskutettu kokonaan.</span><span class="sxs-lookup"><span data-stu-id="23efc-107"> checks that you have fully invoiced the deleted purchase orders.</span></span> <span data-ttu-id="23efc-108">Tilauksia, joita ei ole kokonaan laskutettu ja vastaanotettu, ei voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="23efc-108">You cannot delete orders that you have not fully invoiced and received.</span></span>  

<span data-ttu-id="23efc-109">Ohjelma poistaa palautustilaukset tavallisesti sen jälkeen, kun ne on laskutettu.</span><span class="sxs-lookup"><span data-stu-id="23efc-109">Return orders are usually deleted after they are invoiced.</span></span> <span data-ttu-id="23efc-110">Kun kirjaat laskun, se siirretään **Kirjattu ostohyvityslasku** -ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="23efc-110">When you post an invoice, it is transferred to the **Posted Purchase Credit Memo** window.</span></span> <span data-ttu-id="23efc-111">Jos kuitenkin olet valinnut  **Palautustoimitus hyvityslaskutettaessa** -valintaruudun **Ostojen ja ostovelkojen asetukset** -ikkunassa, lasku siirretään **Kirjattu palautustoimitus** -ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="23efc-111">If you selected the **Return Shipment on Credit Memo** check box in the **Purchases & Payable Setup** window, then the invoice is transferred to the **Posted Return Shipment** window.</span></span> <span data-ttu-id="23efc-112">Voit poistaa asiakirjat **Poista laskutetut ostopal.til.** -eräajolla.</span><span class="sxs-lookup"><span data-stu-id="23efc-112">You can delete the documents using the **Delete Invd Purch. Ret. Orders** batch job.</span></span> <span data-ttu-id="23efc-113">Eräajo tarkistaa ennen poistamista, onko ostopalautustilaukset toimitettu ja laskutettu kokonaan.</span><span class="sxs-lookup"><span data-stu-id="23efc-113">Before deleting, the batch job checks if the purchase return orders are fully shipped and invoiced.</span></span>  

<span data-ttu-id="23efc-114">Puiteostotilauksia ei poisteta sen jälkeen, kun kaikki liittyvät ostotilaukset on käsitelty ja laskutettu.</span><span class="sxs-lookup"><span data-stu-id="23efc-114">Blanket purchase orders are not deleted after you have processed and invoiced all the related purchase orders.</span></span> <span data-ttu-id="23efc-115">Puitetilaukset voi poistaa **Poista lask. puiteostotilaukset** -eräajolla.</span><span class="sxs-lookup"><span data-stu-id="23efc-115">You can delete blanket orders with the **Delete Invoiced Blanket Purchase Orders** batch job.</span></span>  

<span data-ttu-id="23efc-116">Laskutetut huoltotilaukset poistetaan ohjelmasta automaattisesti sen jälkeen, kun ne on laskutettu kokonaan.</span><span class="sxs-lookup"><span data-stu-id="23efc-116">Invoiced service orders are usually deleted automatically after having been fully invoiced.</span></span> <span data-ttu-id="23efc-117">Kun lasku on kirjattu, vastaava tapahtuma luodaan **Kirjatut huoltolaskut** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="23efc-117">When an invoice is posted, a corresponding entry is created in the **Posted Service Invoices** window.</span></span> <span data-ttu-id="23efc-118">Kirjattua asiakirjaa voi katsella **Kirjattu huoltolasku** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="23efc-118">The posted document can be viewed in the **Posted Service Invoice** window.</span></span>  

<span data-ttu-id="23efc-119">Ohjelma ei poista huoltotilauksia automaattisesti, jos tilauksen kokonaismäärä on kirjattu **Huoltolasku**-ikkunassa itse huoltotilauksen sijaan.</span><span class="sxs-lookup"><span data-stu-id="23efc-119">Service orders are not deleted automatically, however, if the total quantity on the order has been posted not from the service order itself, but from the **Service Invoice** window.</span></span> <span data-ttu-id="23efc-120">Tällöin sinun on ehkä poistettava laskutetut tilaukset, joita ei poistettu.</span><span class="sxs-lookup"><span data-stu-id="23efc-120">Then you may need to delete invoiced orders that were not deleted.</span></span> <span data-ttu-id="23efc-121">Voit tehdä sen suorittamalla **Poista laskutetut huoltotilaukset** -eräajon.</span><span class="sxs-lookup"><span data-stu-id="23efc-121">You can do this by running the **Delete Invoiced Service Orders** batch job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="23efc-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="23efc-122">See Also</span></span>  
[<span data-ttu-id="23efc-123">Finance and Operations, Business editionin määrittäminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="23efc-123">Setup and Administration in Finance and Operations, Business edition</span></span>](admin-setup-and-administration.md)  

