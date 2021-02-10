---
title: Älykkäiden ilmoitusten käyttäminen ja niiden esiintymisen määrittäminen | Microsoft Docs
description: Voit saada ilmoituksia, joilla ilmoitetaan tilan muutoksista tai tapahtumista, kuten erääntyneestä saldosta tai pienestä varastosta.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: a297fd8381cf0af9de825cdaced658521e0335c8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756640"
---
# <a name="manage-notifications"></a><span data-ttu-id="7d8c5-103">Ilmoitusten hallinta</span><span class="sxs-lookup"><span data-stu-id="7d8c5-103">Manage Notifications</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="7d8c5-104">voi auttaa työskentelemään älykkäämmin ilmoittamalla tietyistä tapahtumista tai tilamuutoksesta esimerkiksi silloin, kun olet laskuttamassa asiakasta, jolla on erääntynyttä saldoa, tai kun käytettävissä oleva varasto on pienempi kuin myytävä määrä.</span><span class="sxs-lookup"><span data-stu-id="7d8c5-104">can help you work smarter by notifying you about certain events or changes in status, such as when you are about to invoice a customer who has an overdue balance, or the available inventory is lower than the quantity you are about to sell, for example.</span></span> <span data-ttu-id="7d8c5-105">Nämä ilmoitukset näytetään hienovaraisina vihjeinä käsiteltävän tehtävän kontekstissa. Voit ohittaa ilmoituksen tai tarkastella sitä lähemmin.</span><span class="sxs-lookup"><span data-stu-id="7d8c5-105">These notifications are shown as discreet tips in the context of the task you are doing, and you can choose to ignore the notification or to see details about the issue.</span></span>  

<span data-ttu-id="7d8c5-106">Jos tarkastelet ilmoituksen tietoja, voit ratkaista asian tekemällä toimenpiteitä, kuten esimerkiksi ottaa yhteyttä asiakkaaseen tai ostaa lisää nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="7d8c5-106">If you choose to see details for a notification, you can take action to resolve the issue, such as contacting the customer, buying more inventory, and so on.</span></span> <span data-ttu-id="7d8c5-107">Valitset suoritettavat tehtävät, ja [!INCLUDE[prod_short](includes/prod_short.md)] antaa niitä koskevia neuvoja ja suosituksia.</span><span class="sxs-lookup"><span data-stu-id="7d8c5-107">It's your choice what to do, and [!INCLUDE[prod_short](includes/prod_short.md)] gives you advice and recommendations.</span></span>  

<span data-ttu-id="7d8c5-108">Ilmoitukset auttavat kokemattomia käyttäjiä tekemään uusia tehtäviä. Ilmoitukset eivät myöskään heikennä tottuneiden käyttäjien tuottavuutta.</span><span class="sxs-lookup"><span data-stu-id="7d8c5-108">Notifications can help untrained users complete unfamiliar tasks, and do not reduce productivity for the more trained user.</span></span>  

## <a name="to-turn-notifications-on-or-off-and-control-when-they-are-sent"></a><span data-ttu-id="7d8c5-109">Ilmoitusten ottaminen käyttöön ja käytöstä poistaminen sekä lähetystilanteiden hallinta</span><span class="sxs-lookup"><span data-stu-id="7d8c5-109">To turn notifications on or off, and control when they are sent</span></span>

<span data-ttu-id="7d8c5-110">Kun käytät [!INCLUDE[prod_short](includes/prod_short.md)]ia ensimmäisen kerran, kaikki ilmoitukset on otettu käyttöön, mutta voit valita, ovatko ne käytössä myös silloin, jos et ole kiinnostunut tietyistä tapahtumista tai tiloista.</span><span class="sxs-lookup"><span data-stu-id="7d8c5-110">When you first start with [!INCLUDE[prod_short](includes/prod_short.md)] all notifications are turned on, but you can turn them on or off, for example, if you aren't interested in a certain event or status.</span></span>  

<span data-ttu-id="7d8c5-111">Voit lisäksi määrittää joissakin ilmoituksissa ehdot, joiden mukaan ilmoitus lähetetään.</span><span class="sxs-lookup"><span data-stu-id="7d8c5-111">Additionally, some notifications let you specify the conditions under which they are sent.</span></span> <span data-ttu-id="7d8c5-112">Jos haluat esimerkiksi saada ilmoituksen, kun varasto on käymässä vähiin mutta vain niiden nimikkeiden osalta, jotka ostat tietyltä toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="7d8c5-112">For example, if you want to be notified when inventory is running low, but only for items you buy from a certain vendor.</span></span>  

<span data-ttu-id="7d8c5-113">Ilmoitusten ottaminen käyttöön tai niiden poistaminen käytöstä sekä ehtojen määrittäminen on käyttäjäkohtaista.</span><span class="sxs-lookup"><span data-stu-id="7d8c5-113">Turning notifications on or off, and specifying conditions, applies only to you.</span></span>  

1. <span data-ttu-id="7d8c5-114">Valitse oikeassa yläkulmassa **Asetukset**-kuvake ![Asetukset](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") ja valitse sitten **Omat asetukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="7d8c5-114">In the top right corner, choose the **Settings** icon ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center"), and then choose the **My Settings** action.</span></span>  
2. <span data-ttu-id="7d8c5-115">Valitse **Omat asetukset** -sivun **Ilmoitukset**-kentässä *Ilmoitusten vastaanottoajankohdan muuttaminen*.</span><span class="sxs-lookup"><span data-stu-id="7d8c5-115">On the **My Settings** page, in the **Notifications** field, choose the *Change when I receive notifications.*</span></span> <span data-ttu-id="7d8c5-116">linkki.</span><span class="sxs-lookup"><span data-stu-id="7d8c5-116">link.</span></span>  
3. <span data-ttu-id="7d8c5-117">Ota ilmoitus käyttöön tai poista ilmoitus käytöstä näyttöön tulevassa sivussa valitsemalla tai poistamalla **Käytössä**-valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="7d8c5-117">In the page that appears, turn on or turn off a notification by selecting or clearing the **Enabled** check box.</span></span>  
4. <span data-ttu-id="7d8c5-118">Voit määrittää ilmoituksen käynnistinehdot valitsemalla **Näkymän suodattimen tiedot** -linkin ja täyttämällä kentät.</span><span class="sxs-lookup"><span data-stu-id="7d8c5-118">To specify conditions that trigger a notification, choose the **View filter details** link, and then fill in the fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7d8c5-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7d8c5-119">See Also</span></span>

<span data-ttu-id="7d8c5-120">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7d8c5-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
