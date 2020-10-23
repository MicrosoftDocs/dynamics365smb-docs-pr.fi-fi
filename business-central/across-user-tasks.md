---
title: Tehtävien määrittäminen ja hallinta| Microsoft Docs
description: Tietoja tehtävien määrittämisestä käyttäjille, kuten esimerkiksi kirjanpitäjälle, Business Central -sovelluksessa
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: tasks, work
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c76751726f5cd680fafc0887fc57a1464d0ac3ca
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922615"
---
# <a name="define-user-tasks"></a><span data-ttu-id="27a15-103">Käyttäjätehtävien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="27a15-103">Define User Tasks</span></span>

<span data-ttu-id="27a15-104">Voit luoda [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa tehtäviä, jotka muistuttavat sinua tekemättömistä töistä.</span><span class="sxs-lookup"><span data-stu-id="27a15-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], you can create tasks to remind you of work to be done.</span></span> <span data-ttu-id="27a15-105">Voit luoda tehtäviä itsellesi, mutta voit määrittää tehtäviä myös muille. Samoin joku toinen käyttäjä organisaatiossa voi määrittää tehtäviä sinulle.</span><span class="sxs-lookup"><span data-stu-id="27a15-105">You can create tasks for yourself, but you can also assign tasks to others or be assigned a task by someone else in your organization.</span></span>  

## <a name="managing-user-tasks"></a><span data-ttu-id="27a15-106">Käyttäjätehtävien hallinta</span><span class="sxs-lookup"><span data-stu-id="27a15-106">Managing User Tasks</span></span>

<span data-ttu-id="27a15-107">**Käyttäjätehtävät**-sivulla näkyvät kaikki tehtävät. Voit luoda ja määrittää tehtäviä helposti.</span><span class="sxs-lookup"><span data-stu-id="27a15-107">The **User Tasks** page shows all tasks, and you can easily create and assign new tasks.</span></span> <span data-ttu-id="27a15-108">Kun luot tehtävän, määritä sille alku- ja määräpäivä. Voit lisätä linkin sivulle tai raporttiin [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa, jossa käyttäjän on suoritettava työ.</span><span class="sxs-lookup"><span data-stu-id="27a15-108">When you create a task, you can specify the start date and due date, and you can add a link to the page or report in [!INCLUDE[d365fin](includes/d365fin_md.md)] where the user must do the work.</span></span>  

<span data-ttu-id="27a15-109">Voit luoda itsellesi tai työtoverillesi esimerkiksi tehtävän, jossa tarkistetaan kaikki kirjatut myyntilaskut.</span><span class="sxs-lookup"><span data-stu-id="27a15-109">For example, you can create a task for yourself or a coworker to view all posted sales invoices.</span></span> <span data-ttu-id="27a15-110">Tässä tapauksessa tehtävä linkitetään sivulle 143, jonka nimi on **Kirjatut myyntilaskut**.</span><span class="sxs-lookup"><span data-stu-id="27a15-110">In that case, you link the task to page 143, **Posted Sales Invoices**.</span></span> <span data-ttu-id="27a15-111">Seuraavassa kuvakaappauksessa joku luo tehtävän MeganB:lle ja tarkastelee kirjattuja myyntilaskuja.</span><span class="sxs-lookup"><span data-stu-id="27a15-111">In the following screenshot, someone is creating a task for MeganB to review the posted sales invoices.</span></span>  

:::image type="content" source="media/across-user-tasks/sample-user-task.png" alt-text="Esimerkki käyttäjän tehtävästä":::

> [!TIP]  
> <span data-ttu-id="27a15-113">Käytä **Sivu**-kentän hakutoimintoa ja etsi sitten haluamasi sivu **Etsi**-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="27a15-113">Use the look-up in the **Page** field and then use the **Search** field to find the page that you want.</span></span>  
>
> <span data-ttu-id="27a15-114">Voit linkittää mihin tahansa sivuun, mutta et voi linkittää yksittäisiin tapahtumiin, joten tee kuvaus mahdollisimman eksplisiittisesti, esimerkiksi kirjoittamalla "Katso asiakasnumero</span><span class="sxs-lookup"><span data-stu-id="27a15-114">You can link to any page, but you cannot link to individual entries, so make the description as explicit as possible, such as writing "Please take a look at customer no.</span></span> <span data-ttu-id="27a15-115">10000 ja varmista, että heillä ei ole erääntyneitä maksuja.".</span><span class="sxs-lookup"><span data-stu-id="27a15-115">10000 and make sure they don't have overdue payments.".</span></span>

### <a name="picking-up-user-tasks"></a><span data-ttu-id="27a15-116">Käyttäjätehtävien poimiminen</span><span class="sxs-lookup"><span data-stu-id="27a15-116">Picking Up User Tasks</span></span>

<span data-ttu-id="27a15-117">Liiketoimintajohtajan ja kirjanpitäjän roolikeskuksissa ruutu näyttää kyseiselle käyttäjälle liitetyt odottavat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="27a15-117">In the Business Manager, Bookkeeper, and Accountant Role Centers, a tile shows pending tasks that are assigned to that user.</span></span> <span data-ttu-id="27a15-118">Voit poimia tehtävän yksinkertaisesti valitsemalla sen odottavien käyttäjätehtävien luettelosta.</span><span class="sxs-lookup"><span data-stu-id="27a15-118">To pick up a task, simply choose it from the list of pending user tasks.</span></span> <span data-ttu-id="27a15-119">Valintanauhan **Siirry tehtäväkohteeseen** -linkki avaa sivun, jossa voit suorittaa työn.</span><span class="sxs-lookup"><span data-stu-id="27a15-119">In the ribbon, the link **Go to Task Item** opens the page where you can do the work.</span></span>  

<span data-ttu-id="27a15-120">Kun tehtävä on suoritetty, voit merkitä sen valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="27a15-120">When you have completed a task, simply mark it as completed.</span></span>  

### <a name="deleting-user-tasks"></a><span data-ttu-id="27a15-121">Käyttäjätehtävien poistaminen</span><span class="sxs-lookup"><span data-stu-id="27a15-121">Deleting User Tasks</span></span>

<span data-ttu-id="27a15-122">Jos haluat poistaa kaikki tai osan käyttäjätehtävistä joukkotoiminnon avulla, voit käyttää **Poista käyttäjätehtävät** -raporttia.</span><span class="sxs-lookup"><span data-stu-id="27a15-122">If you want to bulk delete all or some user tasks, you can use the **Delete User Tasks** report.</span></span> <span data-ttu-id="27a15-123">Voit määrittää pyynnön sivulla suodattimet, joiden avulla poistettavat tehtävät määritetään.</span><span class="sxs-lookup"><span data-stu-id="27a15-123">In the request page, you can set filters to determine which tasks must be deleted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="27a15-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="27a15-124">See Also</span></span>

[<span data-ttu-id="27a15-125">Sivun tai raportin etsiminen</span><span class="sxs-lookup"><span data-stu-id="27a15-125">Searching for a Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="27a15-126">[Kirjanpitäjän käyttökokemukset [!INCLUDE[d365fin](includes/d365fin_md.md)]issa](finance-accounting.md)</span><span class="sxs-lookup"><span data-stu-id="27a15-126">[Accountant Experiences in [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)</span></span>  
