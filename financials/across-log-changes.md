---
title: "Käyttäjätoimien seuraaminen muutoslokissa | Microsoft Docs"
Description: "Voit aktivoida käyttäjälokin niin, että saat historiatiedot kaikista seurattujen taulukoiden tietoihin tehdyistä muutoksista."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c27c63ae26f2f97dd15d31978b967f6a08dd55b7
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="logging-changes-in-dynamics-365-for-financials"></a><span data-ttu-id="5e762-103">Muutosten kirjaaminen Dynamics 365 for Financialsissa</span><span class="sxs-lookup"><span data-stu-id="5e762-103">Logging Changes in Dynamics 365 for Financials</span></span>
<span data-ttu-id="5e762-104">Voit ottaa muutoslokin käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, joten saat käyttöösi toimintojen historian.</span><span class="sxs-lookup"><span data-stu-id="5e762-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="5e762-105">Loki perustuu seuraamiesi taulukoiden tietoihin tehtyihin muutoksiin. Muutoslokissa tapahtumat järjestetään aikajärjestykseen. Se näyttää muutokset, jotka tehdään määritettyjen taulukoiden kenttiin.</span><span class="sxs-lookup"><span data-stu-id="5e762-105">The log is based on changes that are made to data in the tables that you track. In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="5e762-106">Muutosloki kerää kaikki taulukkoon tehdyt muutokset.</span><span class="sxs-lookup"><span data-stu-id="5e762-106">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="5e762-107">Muutoslokin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="5e762-107">Working with the change log</span></span>
<span data-ttu-id="5e762-108">Virheiden ja tietomuutosten lähteen paikallistaminen on yleinen ongelma monissa rahoitusjärjestelmissä.</span><span class="sxs-lookup"><span data-stu-id="5e762-108">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="5e762-109">Kyseessä voi olla mikä tahansa väärästä asiakkaan puhelinnumerosta väärään pääkirjanpitokirjaukseen.</span><span class="sxs-lookup"><span data-stu-id="5e762-109">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="5e762-110">Voit seurata muutoslokiin avulla kaikkia suoria muutoksia, joita käyttäjä tekee tietokannan tietoihin.</span><span class="sxs-lookup"><span data-stu-id="5e762-110">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="5e762-111">Jokainen taulukko ja kenttä niissä pitää haluttaessa määrittää erikseen seurattavaksi, ja sitten loki tulee aktivoida.</span><span class="sxs-lookup"><span data-stu-id="5e762-111">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="5e762-112">Voit aktivoida muutoslokin ja poistaa sen aktivoinnin **Muutoslokin asetukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="5e762-112">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="5e762-113">Kun aktivoit muutoslokin tai poistat sen aktivoinnin, tämä aktiviteetti kirjataan, joten näet aina, kuka käyttäjistä poisti muutoslokin aktivoinnin tai aktivoi sen uudelleen.</span><span class="sxs-lookup"><span data-stu-id="5e762-113">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="5e762-114">Tätä ominaisuutta ei voi ottaa pois käytöstä.</span><span class="sxs-lookup"><span data-stu-id="5e762-114">This cannot be turned off.</span></span>  

<span data-ttu-id="5e762-115">Jos valitset **Muutoslokin asetukset** -ikkunassa **Taulukot**-toiminnon, voit määrittää sekä taulukot, joiden muutoksia seurataan, että seurattavat muutokset. [!INCLUDE[d365fin](includes/d365fin_md.md)] seuraa myös tiettyjä järjestelmätaulukoita.</span><span class="sxs-lookup"><span data-stu-id="5e762-115">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="5e762-116">Kun olet määrittänyt muutoslokin, aktivoinut sen ja muuttanut tietoja, voit tarkastella ja suodattaa muutoksia **Muutoslokin tapahtumat** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="5e762-116">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="5e762-117">Jos haluat poistaa merkintöjä, voit tehdä sen **Poista muutoslokin tapahtumat** -ikkunassa, jossa voit määrittää päivämääriin ja kellonaikaan perustuvia suodattimia.</span><span class="sxs-lookup"><span data-stu-id="5e762-117">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5e762-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5e762-118">See Also</span></span>
[<span data-ttu-id="5e762-119">Perusasetusten muuttaminen</span><span class="sxs-lookup"><span data-stu-id="5e762-119">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="5e762-120">Lajittelu</span><span class="sxs-lookup"><span data-stu-id="5e762-120">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="5e762-121">Etsi sivua tai raporttia -toiminnon käyttäminen</span><span class="sxs-lookup"><span data-stu-id="5e762-121">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="5e762-122">[Toimintaohje: Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="5e762-122">[How to: Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="5e762-123">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5e762-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

