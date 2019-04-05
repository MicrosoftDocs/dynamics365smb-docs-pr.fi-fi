---
title: Käyttäjätoimien seuraaminen muutoslokissa | Microsoft Docs
description: Voit aktivoida käyttäjälokin niin, että saat historiatiedot kaikista seurattujen taulukoiden tietoihin tehdyistä muutoksista.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 11/14/2018
ms.author: edupont
ms.openlocfilehash: 2a71909faf66c13a0923a10bfc12369127642875
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/19/2019
ms.locfileid: "852882"
---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="4c3ef-103">Business Centralin tilintarkastuksen muutokset</span><span class="sxs-lookup"><span data-stu-id="4c3ef-103">Auditing Changes in Business Central</span></span>

<span data-ttu-id="4c3ef-104">Voit ottaa muutoslokin käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, joten saat käyttöösi toimintojen historian.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="4c3ef-105">Loki perustuu seuraamiesi taulukoiden tietoihin tehtyihin muutoksiin. **Muutoslokin tapahtumat** -sivulla tapahtumat järjestetään aikajärjestykseen. Sivulla näkyy muutokset, jotka tehdään määritettyjen taulukoiden kenttiin.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-105">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="4c3ef-106">Muutosloki kerää kaikki taulukkoon tehdyt muutokset.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-106">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="4c3ef-107">Käyttäjän muutokset eivät näy **Muutoslokin tapahtumat** -sivulla ennen kuin käyttäjä istunto on käynnistetty uudelleen, mikä tapahtuu seuraavissa tilanteissa:</span><span class="sxs-lookup"><span data-stu-id="4c3ef-107">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="4c3ef-108">Istunto vanhentui ja se päivitettiin.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-108">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="4c3ef-109">Käyttäjä valitsi toisen yrityksen tai roolikeskuksen.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-109">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="4c3ef-110">Käyttäjä kirjautui ensin ulos ja sitten takaisin sisään.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-110">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="4c3ef-111">Muutoslokin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="4c3ef-111">Working with the Change Log</span></span>

<span data-ttu-id="4c3ef-112">Virheiden ja tietomuutosten lähteen paikallistaminen on yleinen ongelma monissa rahoitusjärjestelmissä.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-112">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="4c3ef-113">Kyseessä voi olla mikä tahansa väärästä asiakkaan puhelinnumerosta väärään pääkirjanpitokirjaukseen.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-113">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="4c3ef-114">Voit seurata muutoslokiin avulla kaikkia suoria muutoksia, joita käyttäjä tekee tietokannan tietoihin.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-114">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="4c3ef-115">Jokainen taulukko ja kenttä niissä pitää haluttaessa määrittää erikseen seurattavaksi, ja sitten loki tulee aktivoida.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-115">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="4c3ef-116">Voit aktivoida muutoslokin ja poistaa sen aktivoinnin **Muutoslokin asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-116">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="4c3ef-117">Kun käyttäjä aktivoi muutoslokin tai poistaa sen aktivoinnin, tämä aktiviteetti kirjataan, joten näet aina, kuka käyttäjistä poisti muutoslokin aktivoinnin tai aktivoi sen uudelleen.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-117">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="4c3ef-118">Jos valitset **Muutoslokin asetukset** -sivulla **Taulukot**-toiminnon, voit määrittää sekä taulukot, joiden muutoksia seurataan, että seurattavat muutokset. [!INCLUDE[d365fin](includes/d365fin_md.md)] seuraa myös tiettyjä järjestelmätaulukoita.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-118">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="4c3ef-119">Kun olet määrittänyt muutoslokin, aktivoinut sen ja muuttanut tietoja, voit tarkastella ja suodattaa muutoksia **Muutoslokin tapahtumat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-119">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="4c3ef-120">Jos haluat poistaa merkintöjä, voit tehdä sen **Poista muutoslokin tapahtumat** -sivulla, jossa voit määrittää päivämääriin ja kellonaikaan perustuvia suodattimia.</span><span class="sxs-lookup"><span data-stu-id="4c3ef-120">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4c3ef-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4c3ef-121">See Also</span></span>
[<span data-ttu-id="4c3ef-122">Perusasetusten muuttaminen</span><span class="sxs-lookup"><span data-stu-id="4c3ef-122">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="4c3ef-123">Lajittelu</span><span class="sxs-lookup"><span data-stu-id="4c3ef-123">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="4c3ef-124">Kerro, mitä haluat tehdä -toiminnon käyttäminen toimintojen ja tietojen etsimisessä</span><span class="sxs-lookup"><span data-stu-id="4c3ef-124">Using Tell Me to Find Features and Information</span></span>](ui-search.md)  
<span data-ttu-id="4c3ef-125">[Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="4c3ef-125">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="4c3ef-126">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4c3ef-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
