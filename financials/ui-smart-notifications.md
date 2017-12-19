---
title: "Älykkäiden ilmoitusten käyttäminen ja niiden esiintymisen määrittäminen | Microsoft Docs"
description: "Voit saada ilmoituksia, joilla ilmoitetaan tilan muutoksista tai tapahtumista, kuten erääntyneestä saldosta tai pienestä varastosta."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 08/17/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: cfe0eed4090ef458e774da8d0bc03910247570d7
ms.openlocfilehash: bb8b1ecf0f5e8f91598bf96c85ec70f0d385267e
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="smart-notifications"></a><span data-ttu-id="09350-103">Älykkäät ilmoitukset</span><span class="sxs-lookup"><span data-stu-id="09350-103">Smart Notifications</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="09350-104"> voi auttaa työskentelemään älykkäämmin ilmoittamalla tietyistä tapahtumista tai tilamuutoksesta esimerkiksi silloin, kun olet laskuttamassa asiakasta, jolla on erääntynyttä saldoa, tai kun käytettävissä oleva varasto on pienempi kuin myytävä määrä.</span><span class="sxs-lookup"><span data-stu-id="09350-104"> can help you work smarter by notifying you about certain events or changes in status, such as when you are about to invoice a customer who has an overdue balance, or the available inventory is lower than the quantity you are about to sell, for example.</span></span> <span data-ttu-id="09350-105">Nämä ilmoitukset näytetään hienovaraisina vihjeinä käsiteltävän tehtävän kontekstissa. Voit ohittaa ilmoituksen tai tarkastella sitä lähemmin.</span><span class="sxs-lookup"><span data-stu-id="09350-105">These notifications are shown as discreet tips in the context of the task you are doing, and you can choose to ignore the notification or to see details about the issue.</span></span>  

<span data-ttu-id="09350-106">Jos tarkastelet ilmoituksen tietoja, voit ratkaista asian tekemällä toimenpiteitä, kuten esimerkiksi ottaa yhteyttä asiakkaaseen tai ostaa lisää nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="09350-106">If you choose to see details for a notification, you can take action to resolve the issue, such as contacting the customer, buying more inventory, and so on.</span></span> <span data-ttu-id="09350-107">Valitset suoritettavat tehtävät, ja [!INCLUDE[d365fin](includes/d365fin_md.md)] antaa niitä koskevia neuvoja ja suosituksia.</span><span class="sxs-lookup"><span data-stu-id="09350-107">It's your choice what to do, and [!INCLUDE[d365fin](includes/d365fin_md.md)] gives you advice and recommendations.</span></span>  

<span data-ttu-id="09350-108">Ilmoitukset auttavat kokemattomia käyttäjiä tekemään uusia tehtäviä. Ilmoitukset eivät myöskään heikennä tottuneiden käyttäjien tuottavuutta.</span><span class="sxs-lookup"><span data-stu-id="09350-108">Notifications can help untrained users complete unfamiliar tasks, and do not reduce productivity for the more trained user.</span></span>  

## <a name="to-turn-notifications-on-or-off-and-control-when-they-are-sent"></a><span data-ttu-id="09350-109">Ilmoitusten ottaminen käyttöön ja käytöstä poistaminen sekä lähetystilanteiden hallinta</span><span class="sxs-lookup"><span data-stu-id="09350-109">To turn notifications on or off, and control when they are sent</span></span>
<span data-ttu-id="09350-110">Kun käytät [!INCLUDE[d365fin](includes/d365fin_md.md)]ia ensimmäisen kerran, kaikki ilmoitukset on otettu käyttöön, mutta voit valita, ovatko ne käytössä myös silloin, jos et ole kiinnostunut tietyistä tapahtumista tai tiloista.</span><span class="sxs-lookup"><span data-stu-id="09350-110">When you first start with [!INCLUDE[d365fin](includes/d365fin_md.md)] all notifications are turned on, but you can turn them on or off, for example, if you aren't interested in a certain event or status.</span></span>  

<span data-ttu-id="09350-111">Voit lisäksi määrittää joissakin ilmoituksissa ehdot, joiden mukaan ilmoitus lähetetään.</span><span class="sxs-lookup"><span data-stu-id="09350-111">Additionally, some notifications let you specify the conditions under which they are sent.</span></span> <span data-ttu-id="09350-112">Jos haluat esimerkiksi saada ilmoituksen, kun varasto on käymässä vähiin mutta vain niiden nimikkeiden osalta, jotka ostat tietyltä toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="09350-112">For example, if you want to be notified when inventory is running low, but only for items you buy from a certain vendor.</span></span>  

<span data-ttu-id="09350-113">Ilmoitusten ottaminen käyttöön tai niiden poistaminen käytöstä sekä ehtojen määrittäminen on käyttäjäkohtaista.</span><span class="sxs-lookup"><span data-stu-id="09350-113">Turning notifications on or off, and specifying conditions, applies only to you.</span></span>  

1. <span data-ttu-id="09350-114">Valitse ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, kirjoita **Omat ilmoitukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="09350-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **My Notifications**, and then choose the related link.</span></span>
2. <span data-ttu-id="09350-115">Ota ilmoitus käyttöön tai poista se käytöstä valitsemalla **Käytössä**-valintaruutu tai poistamalla sen valinta.</span><span class="sxs-lookup"><span data-stu-id="09350-115">To turn on or turn off a notification, select or clear the **Enabled** check box.</span></span>
3. <span data-ttu-id="09350-116">Voit määrittää ilmoituksen käynnistinehdot valitsemalla **Näkymän suodattimen tiedot** -linkin ja täyttämällä kentät.</span><span class="sxs-lookup"><span data-stu-id="09350-116">To specify conditions that trigger a notification, choose the **View filter details** link, and then fill in the fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="09350-117">Katso myös</span><span class="sxs-lookup"><span data-stu-id="09350-117">See Also</span></span>
<span data-ttu-id="09350-118">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="09350-118">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

