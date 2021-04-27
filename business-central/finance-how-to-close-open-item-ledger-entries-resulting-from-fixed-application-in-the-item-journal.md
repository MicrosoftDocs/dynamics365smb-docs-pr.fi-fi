---
title: Sulje kiinteän kohdistuksen kautta tulleita nimiketapahtumia.
description: Ktaso, miten voit luoda kiinteän kohdistuksen saapuvan tapahtuman ja lähtevän alkuperäisen tapahtuman välille nimikepäiväkirjassa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4fac4871fdf42210dfd48ca6dd7d9c2fede0c7ef
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788281"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="afcc4-103">Nimikepäiväkirjan kiinteästä kohdistuksesta aiheutuvien avointen nimiketapahtumien sulkeminen</span><span class="sxs-lookup"><span data-stu-id="afcc4-103">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>

<span data-ttu-id="afcc4-104">Voit luoda **Nimikepäiväkirja**-sivun **Kohdistukset tapahtumista** -kentässä manuaalisesti kiinteän kohdistuksen saapuvan tapahtuman ja lähtevän alkuperäisen tapahtuman välille.</span><span class="sxs-lookup"><span data-stu-id="afcc4-104">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="afcc4-105">Voit korjata esimerkiksi lähtevän tapahtuman tai käsitellä sen palautuksen.</span><span class="sxs-lookup"><span data-stu-id="afcc4-105">For example, to correct the outbound transaction or to process its return.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="afcc4-106">Tällä tavoin tehdyt kiinteät kohdistukset koskevat vain kustannuksia, eivät määrää.</span><span class="sxs-lookup"><span data-stu-id="afcc4-106">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="afcc4-107">Näin ollen kirjattu positiivinen nimiketapahtuma ei sulje käytettyä lähtevää tapahtumaa, ja pysyy itse avoinna.</span><span class="sxs-lookup"><span data-stu-id="afcc4-107">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="afcc4-108">Tämä pätee myös silloin, kun positiivisen tapahtuman kiinteä kohdistus kirjataan negatiiviseen tapahtumaan, jota tavallinen positiivinen tapahtuma ei ole sulkenut, jolloin sekä negatiivinen että positiivinen tapahtuma jäävät avoimiksi.</span><span class="sxs-lookup"><span data-stu-id="afcc4-108">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>
> <span data-ttu-id="afcc4-109">Tämä tarkoittaa myös sitä, että varastokautta ei voi sulkea, jos tällainen tapahtuma on olemassa.</span><span class="sxs-lookup"><span data-stu-id="afcc4-109">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="afcc4-110">Voit tietyin edellytyksin muuttaa ja uudelleen käyttää kohdistustapahtumia **Kohdistustyökirja**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="afcc4-110">You can change and reapply application entries under certain conditions by using the **Application Worksheet** page.</span></span>  

<span data-ttu-id="afcc4-111">Seuraavassa ohjeessa neuvotaan, miten sulkea nämä tapahtumat suorittamalla kaksi korjaavaa kirjausta nimikepäiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="afcc4-111">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="afcc4-112">Sulje avoimet nimiketapahtumat, jotka aiheutuvat nimikepäiväkirjan kiinteästä kohdistuksesta</span><span class="sxs-lookup"><span data-stu-id="afcc4-112">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1. <span data-ttu-id="afcc4-113">Kirjaa **Kohdistukset tapahtumista** -kentässä positiivinen muutos ja vastaava määrä.</span><span class="sxs-lookup"><span data-stu-id="afcc4-113">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="afcc4-114">Tämä sulkee alkuperäisen korjaavan negatiivisen tapahtuman, jossa on kiinteä kohdistus.</span><span class="sxs-lookup"><span data-stu-id="afcc4-114">This closes the original negative entry with a fixed application.</span></span>  

    <span data-ttu-id="afcc4-115">**Kohdistukset tapahtumista** -kenttä määrittää lähtevän nimikepäiväkirjatapahtuman numeron, jonka kustannukset välitetään saapuvaan nimikepäiväkirjatapahtumaan silloin, kun kirjaat saapuvan transaktion tyyppiä **Posit. muutos** tai **Osto** nimikepäiväkirjan kanssa.</span><span class="sxs-lookup"><span data-stu-id="afcc4-115">The **Applies-from Entry** field specifies the number of the outbound item ledger entry whose cost is forwarded to the inbound item ledger entry when you post an inbound transaction of type **Positive Adjmt.** or **Purchase** with the item journal.</span></span>  
2. <span data-ttu-id="afcc4-116">Kirjaa negatiivinen muutos **Kohdistetaan tapahtumaan** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="afcc4-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="afcc4-117">Tämä sulkee alkuperäisen korjaavan positiivisen tapahtuman, jossa on kiinteä kohdistus.</span><span class="sxs-lookup"><span data-stu-id="afcc4-117">This closes the original corrective positive entry with a fixed application.</span></span>  

    <span data-ttu-id="afcc4-118">**Kohdistukset tapahtumista** -kenttä määrittää, onko nimikepäiväkirjan rivin määrä kohdistettava jo kirjattuun asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="afcc4-118">The **Applies-to Entry** field specifies if the quantity in the item journal line should be applied to an already-posted document.</span></span> <span data-ttu-id="afcc4-119">Jos rivi on kohdistettava jo kirjattuun asiakirjaan, anna sen nimiketapahtuman numero, johon haluat kohdistaa nimikepäiväkirjan rivin.</span><span class="sxs-lookup"><span data-stu-id="afcc4-119">If this is the case, enter the entry number of the item ledger entry to which the item journal line should be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="afcc4-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="afcc4-120">See Also</span></span>

[<span data-ttu-id="afcc4-121">Nimiketapahtumien poistaminen ja uudelleenkohdistaminen</span><span class="sxs-lookup"><span data-stu-id="afcc4-121">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
[<span data-ttu-id="afcc4-122">Myynnin palautusten ja peruutusten käsittely</span><span class="sxs-lookup"><span data-stu-id="afcc4-122">Process Sales Returns and Cancellations</span></span>](sales-how-process-sales-returns-cancellations.md)  
[<span data-ttu-id="afcc4-123">Varastonarvostuksen ja kustannuslaskennan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="afcc4-123">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="afcc4-124">Varaston kustannusten hallinta</span><span class="sxs-lookup"><span data-stu-id="afcc4-124">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="afcc4-125">Rakennetiedot: Arvostusmenetelmät</span><span class="sxs-lookup"><span data-stu-id="afcc4-125">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]