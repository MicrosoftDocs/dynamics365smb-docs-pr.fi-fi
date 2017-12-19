---
title: "Käyttäjätoimien seuraaminen muutoslokissa | Microsoft Docs"
Description: You can activate a user log so that you have a history of any changes made to data in tracked tables.
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
ms.sourcegitcommit: cfe0eed4090ef458e774da8d0bc03910247570d7
ms.openlocfilehash: 9f3db97203e09608ea0776f5571d6179778283b6
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="logging-changes-in-dynamics-365-business-edition"></a><span data-ttu-id="6b08e-102">Muutosten kirjaaminen lokiin Dynamics 365, Business editionissa</span><span class="sxs-lookup"><span data-stu-id="6b08e-102">Logging Changes in Dynamics 365, Business edition</span></span> 
<span data-ttu-id="6b08e-103">Voit ottaa muutoslokin käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, joten saat käyttöösi toimintojen historian.</span><span class="sxs-lookup"><span data-stu-id="6b08e-103">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="6b08e-104">Loki perustuu seuraamiesi taulukoiden tietoihin tehtyihin muutoksiin. Muutoslokissa tapahtumat järjestetään aikajärjestykseen. Se näyttää muutokset, jotka tehdään määritettyjen taulukoiden kenttiin.</span><span class="sxs-lookup"><span data-stu-id="6b08e-104">The log is based on changes that are made to data in the tables that you track. In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="6b08e-105">Muutosloki kerää kaikki taulukkoon tehdyt muutokset.</span><span class="sxs-lookup"><span data-stu-id="6b08e-105">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="6b08e-106">Muutoslokin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="6b08e-106">Working with the Change Log</span></span>
<span data-ttu-id="6b08e-107">Virheiden ja tietomuutosten lähteen paikallistaminen on yleinen ongelma monissa rahoitusjärjestelmissä.</span><span class="sxs-lookup"><span data-stu-id="6b08e-107">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="6b08e-108">Kyseessä voi olla mikä tahansa väärästä asiakkaan puhelinnumerosta väärään pääkirjanpitokirjaukseen.</span><span class="sxs-lookup"><span data-stu-id="6b08e-108">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="6b08e-109">Voit seurata muutoslokiin avulla kaikkia suoria muutoksia, joita käyttäjä tekee tietokannan tietoihin.</span><span class="sxs-lookup"><span data-stu-id="6b08e-109">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="6b08e-110">Jokainen taulukko ja kenttä niissä pitää haluttaessa määrittää erikseen seurattavaksi, ja sitten loki tulee aktivoida.</span><span class="sxs-lookup"><span data-stu-id="6b08e-110">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="6b08e-111">Voit aktivoida muutoslokin ja poistaa sen aktivoinnin **Muutoslokin asetukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="6b08e-111">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="6b08e-112">Kun aktivoit muutoslokin tai poistat sen aktivoinnin, tämä aktiviteetti kirjataan, joten näet aina, kuka käyttäjistä poisti muutoslokin aktivoinnin tai aktivoi sen uudelleen.</span><span class="sxs-lookup"><span data-stu-id="6b08e-112">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="6b08e-113">Tätä ominaisuutta ei voi ottaa pois käytöstä.</span><span class="sxs-lookup"><span data-stu-id="6b08e-113">This cannot be turned off.</span></span>  

<span data-ttu-id="6b08e-114">Jos valitset **Muutoslokin asetukset** -ikkunassa **Taulukot**-toiminnon, voit määrittää sekä taulukot, joiden muutoksia seurataan, että seurattavat muutokset. [!INCLUDE[d365fin](includes/d365fin_md.md)] seuraa myös tiettyjä järjestelmätaulukoita.</span><span class="sxs-lookup"><span data-stu-id="6b08e-114">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="6b08e-115">Kun olet määrittänyt muutoslokin, aktivoinut sen ja muuttanut tietoja, voit tarkastella ja suodattaa muutoksia **Muutoslokin tapahtumat** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="6b08e-115">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="6b08e-116">Jos haluat poistaa merkintöjä, voit tehdä sen **Poista muutoslokin tapahtumat** -ikkunassa, jossa voit määrittää päivämääriin ja kellonaikaan perustuvia suodattimia.</span><span class="sxs-lookup"><span data-stu-id="6b08e-116">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6b08e-117">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6b08e-117">See Also</span></span>
[<span data-ttu-id="6b08e-118">Perusasetusten muuttaminen</span><span class="sxs-lookup"><span data-stu-id="6b08e-118">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="6b08e-119">Lajittelu</span><span class="sxs-lookup"><span data-stu-id="6b08e-119">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="6b08e-120">Etsi sivua tai raporttia -toiminnon käyttäminen</span><span class="sxs-lookup"><span data-stu-id="6b08e-120">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="6b08e-121">[Toimintaohje: Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="6b08e-121">[How to: Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="6b08e-122">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6b08e-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

