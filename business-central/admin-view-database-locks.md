---
title: Tietokannan lukitusten tarkasteleminen
description: Lue miten voit tarkastella minkä tahansa tietokantalukkojen tietoja suoraan Business Centralin asiakasliittymästä.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: b53677ab57d6c48b015bb0dd47ea6e315f8e80c3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776914"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="75a36-103">Tietokannan lukitusten tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="75a36-103">Viewing Database Locks</span></span>

<span data-ttu-id="75a36-104">Tietokannan lukitseminen ohjaa useiden käyttäjien samojen tietojen samanaikaista käyttöoikeutta.</span><span class="sxs-lookup"><span data-stu-id="75a36-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="75a36-105">Voit suojata tapahtuman niin, että muut tapahtumat eivät voi muokata samoja tietoja, jos ensimmäinen tapahtuma asettaa tiedoille lukituksen.</span><span class="sxs-lookup"><span data-stu-id="75a36-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="75a36-106">Lukitus säilyy tapahtuman valmistumiseen asti.</span><span class="sxs-lookup"><span data-stu-id="75a36-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="75a36-107">Käyttäjät eivät ehkä voi suorittaa tapahtumia lukittujen tietojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="75a36-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="75a36-108">Yleensä lukituksesta lähetetään viesti käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="75a36-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="75a36-109">Tietokannan lukitusten tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="75a36-109">To view database locks</span></span>

<span data-ttu-id="75a36-110">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Tietokannan lukitukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="75a36-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="75a36-111">**Tietokannan lukitukset** -sivu sisältää kaikkien nykyisten tietokannan lukitusten tilannevedoksen.</span><span class="sxs-lookup"><span data-stu-id="75a36-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="75a36-112">Lisätietoja tietokannan lukituksesta on kohdassa [Tietokannan lukitusten valvonta](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) Business Centralin kehittäjän ja IT-ammattilaisen ohjeessa.</span><span class="sxs-lookup"><span data-stu-id="75a36-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="75a36-113">Katso myös</span><span class="sxs-lookup"><span data-stu-id="75a36-113">See Also</span></span>

[<span data-ttu-id="75a36-114">Tietokannan lukitusten valvonta</span><span class="sxs-lookup"><span data-stu-id="75a36-114">Monitor Database Locks</span></span>](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]