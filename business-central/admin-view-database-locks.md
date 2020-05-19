---
title: Tietokannan lukitusten tarkasteleminen
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: abee0f31d66f648f4b0be567d8599b31c536a193
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324100"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="f4a51-102">Tietokannan lukitusten tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="f4a51-102">Viewing Database Locks</span></span>

## <a name="about-locks"></a><span data-ttu-id="f4a51-103">Tietoja lukituksista</span><span class="sxs-lookup"><span data-stu-id="f4a51-103">About Locks</span></span>

<span data-ttu-id="f4a51-104">Tietokannan lukitseminen ohjaa useiden käyttäjien samojen tietojen samanaikaista käyttöoikeutta.</span><span class="sxs-lookup"><span data-stu-id="f4a51-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="f4a51-105">Voit suojata tapahtuman niin, että muut tapahtumat eivät voi muokata samoja tietoja, jos ensimmäinen tapahtuma asettaa tiedoille lukituksen.</span><span class="sxs-lookup"><span data-stu-id="f4a51-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="f4a51-106">Lukitus säilyy tapahtuman valmistumiseen asti.</span><span class="sxs-lookup"><span data-stu-id="f4a51-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="f4a51-107">Käyttäjät eivät ehkä voi suorittaa tapahtumia lukittujen tietojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="f4a51-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="f4a51-108">Yleensä lukituksesta lähetetään viesti käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="f4a51-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="f4a51-109">Tietokannan lukitusten tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="f4a51-109">To view database locks</span></span>

<span data-ttu-id="f4a51-110">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Tietokannan lukitukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f4a51-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="f4a51-111">**Tietokannan lukitukset** -sivu sisältää kaikkien nykyisten tietokannan lukitusten tilannevedoksen.</span><span class="sxs-lookup"><span data-stu-id="f4a51-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="f4a51-112">Lisätietoja tietokannan lukituksesta on kohdassa [Tietokannan lukitusten valvonta](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) Business Centralin kehittäjän ja IT-ammattilaisen ohjeessa.</span><span class="sxs-lookup"><span data-stu-id="f4a51-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4a51-113">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f4a51-113">See Also</span></span>

[<span data-ttu-id="f4a51-114">Tietokannan lukitusten valvonta</span><span class="sxs-lookup"><span data-stu-id="f4a51-114">Monitor Database Locks</span></span>](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 
