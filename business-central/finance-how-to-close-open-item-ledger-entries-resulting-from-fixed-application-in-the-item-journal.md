---
title: Nimikepäiväkirjan kiinteästä kohdistuksesta aiheutuvien avointen nimiketapahtumien sulkeminen | Microsoft Docs
description: Voit luoda **Nimikepäiväkirja**-sivun **Kohdistukset tapahtumista** -kentässä manuaalisesti kiinteän kohdistuksen saapuvan tapahtuman ja lähtevän alkuperäisen tapahtuman välille. Voit korjata esimerkiksi lähtevän tapahtuman tai käsitellä sen palautuksen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: e3f210b86168d34ec775f85b416b6d0e365cce88
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795460"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="42935-104">Nimikepäiväkirjan kiinteästä kohdistuksesta aiheutuvien avointen nimiketapahtumien sulkeminen</span><span class="sxs-lookup"><span data-stu-id="42935-104">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>
<span data-ttu-id="42935-105">Voit luoda **Nimikepäiväkirja**-sivun **Kohdistukset tapahtumista** -kentässä manuaalisesti kiinteän kohdistuksen saapuvan tapahtuman ja lähtevän alkuperäisen tapahtuman välille.</span><span class="sxs-lookup"><span data-stu-id="42935-105">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="42935-106">Voit korjata esimerkiksi lähtevän tapahtuman tai käsitellä sen palautuksen.</span><span class="sxs-lookup"><span data-stu-id="42935-106">For example, to correct the outbound transaction or to process its return.</span></span> <span data-ttu-id="42935-107">Lisätietoja on kohdassa Kohdistukset tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="42935-107">For more information, see Applies-from Entry.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="42935-108">Tällä tavoin tehdyt kiinteät kohdistukset koskevat vain kustannuksia, eivät määrää.</span><span class="sxs-lookup"><span data-stu-id="42935-108">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="42935-109">Näin ollen kirjattu positiivinen nimiketapahtuma ei sulje käytettyä lähtevää tapahtumaa, ja pysyy itse avoinna.</span><span class="sxs-lookup"><span data-stu-id="42935-109">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="42935-110">Tämä pätee myös silloin, kun positiivisen tapahtuman kiinteä kohdistus kirjataan negatiiviseen tapahtumaan, jota tavallinen positiivinen tapahtuma ei ole sulkenut, jolloin sekä negatiivinen että positiivinen tapahtuma jäävät avoimiksi.</span><span class="sxs-lookup"><span data-stu-id="42935-110">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>   
>  <span data-ttu-id="42935-111">Tämä tarkoittaa myös sitä, että varastokautta ei voi sulkea, jos tällainen tapahtuma on olemassa.</span><span class="sxs-lookup"><span data-stu-id="42935-111">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="42935-112">Seuraavassa ohjeessa neuvotaan, miten sulkea nämä tapahtumat suorittamalla kaksi korjaavaa kirjausta nimikepäiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="42935-112">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="42935-113">Sulje avoimet nimiketapahtumat, jotka aiheutuvat nimikepäiväkirjan kiinteästä kohdistuksesta</span><span class="sxs-lookup"><span data-stu-id="42935-113">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1.  <span data-ttu-id="42935-114">Kirjaa **Kohdistukset tapahtumista** -kentässä positiivinen muutos ja vastaava määrä.</span><span class="sxs-lookup"><span data-stu-id="42935-114">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="42935-115">Tämä sulkee alkuperäisen korjaavan negatiivisen tapahtuman, jossa on kiinteä kohdistus.</span><span class="sxs-lookup"><span data-stu-id="42935-115">This closes the original negative entry with a fixed application.</span></span>  
2.  <span data-ttu-id="42935-116">Kirjaa negatiivinen muutos **Kohdistetaan tapahtumaan** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="42935-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="42935-117">Tämä sulkee alkuperäisen korjaavan positiivisen tapahtuman, jossa on kiinteä kohdistus.</span><span class="sxs-lookup"><span data-stu-id="42935-117">This closes the original corrective positive entry with a fixed application.</span></span>  

## <a name="see-also"></a><span data-ttu-id="42935-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="42935-118">See Also</span></span>  
[<span data-ttu-id="42935-119"> Nimiketapahtumien poistaminen ja uudelleenkohdistaminen</span><span class="sxs-lookup"><span data-stu-id="42935-119"> Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
 <span data-ttu-id="42935-120">[Myynnin palautusten ja peruutusten käsittely](sales-how-process-sales-returns-cancellations.md) </span><span class="sxs-lookup"><span data-stu-id="42935-120">[Process Sales Returns and Cancellations](sales-how-process-sales-returns-cancellations.md) </span></span>  
 <span data-ttu-id="42935-121">[Varastonarvostuksen ja kustannuslaskennan määrittäminen](finance-set-up-inventory-valuation-and-costing.md) </span><span class="sxs-lookup"><span data-stu-id="42935-121">[Setting Up Inventory Valuation and Costing](finance-set-up-inventory-valuation-and-costing.md) </span></span>  
 <span data-ttu-id="42935-122">[Varaston kustannusten hallinta](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="42935-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="42935-123">Rakennetiedot: Arvostusmenetelmät</span><span class="sxs-lookup"><span data-stu-id="42935-123">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
