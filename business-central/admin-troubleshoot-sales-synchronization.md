---
title: Synkronointivirheiden vianmääritys | Microsoft Docs
description: Sisältää ohjeita synkronointivirheiden määrittämistä ja ratkaisemista varten.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 729a767c0cb4bb330a463e14c7eb6a4f8fd7d909
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304247"
---
# <a name="troubleshooting-synchronization-errors"></a><span data-ttu-id="7c655-103">Synkronointivirheiden vianmääritys</span><span class="sxs-lookup"><span data-stu-id="7c655-103">Troubleshooting Synchronization Errors</span></span>
<span data-ttu-id="7c655-104">Sovellusten [!INCLUDE[d365fin](includes/d365fin_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] integrointi sisältää useita vaiheita, ja joskus tapahtuu virheitä.</span><span class="sxs-lookup"><span data-stu-id="7c655-104">There are lots of moving parts involved in integrating [!INCLUDE[d365fin](includes/d365fin_md.md)] with [!INCLUDE[crm_md](includes/crm_md.md)], and sometimes things go wrong.</span></span> <span data-ttu-id="7c655-105">Tässä ohjeaiheessa kerrotaan yleisimpiä virheitä ja annetaan vinkkejä niiden korjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="7c655-105">This topic points out some of the typical errors that occur and gives some pointers for how to fix them.</span></span>

<span data-ttu-id="7c655-106">Virheet johtuvat usein siitä, että käyttäjä on tehnyt jotain yhdistetyille tietueille tai integroinnin määrittämisessä on tapahtunut virhe.</span><span class="sxs-lookup"><span data-stu-id="7c655-106">Errors often occur either because of something that a user has done to coupled records or something is wrong with how the integration is set up.</span></span> <span data-ttu-id="7c655-107">Jos virheet ovat tapahtuneet yhdistettyjen tietueiden vuoksi, käyttäjät voivat ratkaista ne itse.</span><span class="sxs-lookup"><span data-stu-id="7c655-107">For errors related to coupled records, users can resolve those themselves.</span></span> <span data-ttu-id="7c655-108">Nämä virheet johtuvat esimerkiksi siitä, että poistat tietueita yhdestä liiketoimintasovelluksesta, mutta et molemmista, ja synkronoit tämän jälkeen.</span><span class="sxs-lookup"><span data-stu-id="7c655-108">These errors are caused by actions such as deleting a record in one, but not both, business apps and then synchronizing.</span></span> <span data-ttu-id="7c655-109">Lisätietoja on kohdassa [Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md).</span><span class="sxs-lookup"><span data-stu-id="7c655-109">For more information, see [View the Status of a Synchronization](admin-how-to-view-synchronization-status.md).</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

<span data-ttu-id="7c655-110">Integroinnin määrittämiseen liittyvät virheet vaativat yleensä järjestelmänvalvojan toimia.</span><span class="sxs-lookup"><span data-stu-id="7c655-110">Errors that are related to how the integration is set up typically require an administrator's attention.</span></span> <span data-ttu-id="7c655-111">Voit tarkastella näitä virheitä **Integroinnin synkronointivirheet** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="7c655-111">You can view these errors on the **Integration Synchronization Errors** page.</span></span> <span data-ttu-id="7c655-112">Seuraavassa esitellään tyypillisiä virheitä:</span><span class="sxs-lookup"><span data-stu-id="7c655-112">Examples of some typical issues include:</span></span>  
  
* <span data-ttu-id="7c655-113">Käyttäjille määritetyt käyttöoikeudet ja roolit ovat virheellisiä.</span><span class="sxs-lookup"><span data-stu-id="7c655-113">The permissions and roles assigned to users are not correct.</span></span>  
* <span data-ttu-id="7c655-114">Järjestelmänvalvojan tili on määritetty integroinnin käyttäjäksi.</span><span class="sxs-lookup"><span data-stu-id="7c655-114">The administrator account was specified as the integration user.</span></span>  
* <span data-ttu-id="7c655-115">Integroinnin käyttäjän salasana on määritetty vaihdettavaksi, kun käyttäjä kirjautuu sisään.</span><span class="sxs-lookup"><span data-stu-id="7c655-115">The integration user’s password is set to require a change when the user signs in.</span></span>  
* <span data-ttu-id="7c655-116">Valuuttojen vaihtokursseja ei ole määritetty yhdessä tai kummassakaan sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="7c655-116">The exchange rates for currencies are not specified in one or the other app.</span></span>  
  
<span data-ttu-id="7c655-117">Nämä virheet on ratkaistava manuaalisesti. Sivulla olevat toiminnot voivat kuitenkin auttaa tässä.</span><span class="sxs-lookup"><span data-stu-id="7c655-117">You must manually resolve the errors, but there are a few ways in which the page helps you.</span></span> <span data-ttu-id="7c655-118">Esimerkiksi:</span><span class="sxs-lookup"><span data-stu-id="7c655-118">For example:</span></span>  

* <span data-ttu-id="7c655-119">**Lähde**- ja **Kohde**-kentät voivat sisältää linkkejä tietueeseen, josta virhe löytyi.</span><span class="sxs-lookup"><span data-stu-id="7c655-119">The **Source** and **Destination** fields may contain links to the record where the error was found.</span></span> <span data-ttu-id="7c655-120">Valitse linkki, kun haluat avata tietueen ja tutkia virhettä.</span><span class="sxs-lookup"><span data-stu-id="7c655-120">Click the link to open the record and investigate the error.</span></span>  
* <span data-ttu-id="7c655-121">**Poista yli 7 päivää vanhat tapahtumat**- ja **Poista kaikki tapahtumat** -toiminnot tyhjentävät luettelon.</span><span class="sxs-lookup"><span data-stu-id="7c655-121">The **Delete Entries Older than 7 Days** and the **Delete All Entries** actions will clean up the list.</span></span> <span data-ttu-id="7c655-122">Näitä toimintoja käytetään yleensä sen jälkeen, kun useisiin tietueisiin vaikuttavan virheen syy on selvitetty.</span><span class="sxs-lookup"><span data-stu-id="7c655-122">Typically, you use these actions after you have resolved the cause of an error that affects many records.</span></span> <span data-ttu-id="7c655-123">Mieti kuitenkin tarkasti, kun teet sen.</span><span class="sxs-lookup"><span data-stu-id="7c655-123">Use caution, however.</span></span> <span data-ttu-id="7c655-124">Nämä toiminnot saattavat poistaa virheitä, jotka vielä vaikuttavat toimintaan.</span><span class="sxs-lookup"><span data-stu-id="7c655-124">These actions might delete errors that are still relevant.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c655-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7c655-125">See Also</span></span>
<span data-ttu-id="7c655-126">[Integrointi [!INCLUDE[crm_md](includes/crm_md.md)]in kanssa](admin-prepare-dynamics-365-for-sales-for-integration.md)</span><span class="sxs-lookup"><span data-stu-id="7c655-126">[Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span></span>  
<span data-ttu-id="7c655-127">[[!INCLUDE[crm_md](includes/crm_md.md)] -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)</span><span class="sxs-lookup"><span data-stu-id="7c655-127">[Setting Up User Accounts for Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span></span>  
<span data-ttu-id="7c655-128">[Yhteyden määrittäminen [!INCLUDE[crm_md](includes/crm_md.md)] -sovellukseen](admin-how-to-set-up-a-dynamics-crm-connection.md)</span><span class="sxs-lookup"><span data-stu-id="7c655-128">[Set Up a Connection to [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span></span>  
[<span data-ttu-id="7c655-129">Tietueiden yhdistäminen ja synkronoiminen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="7c655-129">Couple and Synchronize Records Manually</span></span>](admin-how-to-couple-and-synchronize-records-manually.md)  
[<span data-ttu-id="7c655-130">Synkronoinnin tilan näyttäminen</span><span class="sxs-lookup"><span data-stu-id="7c655-130">View the Status of a Synchronization</span></span>](admin-how-to-view-synchronization-status.md)  