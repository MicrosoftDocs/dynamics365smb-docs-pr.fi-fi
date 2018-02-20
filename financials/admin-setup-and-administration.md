---
title: "Finance and Operations, Business editionin hallintatehtävät | Microsoft Docs"
description: "Osa Finance and Operations, Business editionin tehtävistä edellyttää keskitettyä hallintaa ja määrittämistä. Katso lisätietoja näistä tehtävistä ja niiden määrittämisestä."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: c64bc883031be28aa6634bdcf48f00c7ca77567d
ms.contentlocale: fi-fi
ms.lasthandoff: 02/02/2018

---
# <a name="setup-and-administration-in-finance-and-operations-business-edition"></a><span data-ttu-id="25679-104">Finance and Operations, Business editionin määrittäminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="25679-104">Setup and Administration in Finance and Operations, Business edition</span></span>
<span data-ttu-id="25679-105">Yleensä yksi rooli hoitaa yrityksen keskitetyt hallintatehtävät.</span><span class="sxs-lookup"><span data-stu-id="25679-105">Central administration tasks are usually performed by one role in the company.</span></span> <span data-ttu-id="25679-106">Tehtävien laajuus voi määräytyä yrityksen koon ja järjestelmänvalvojan vastuualueiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="25679-106">The scope of these tasks can depend on the company's size and the administrator's job responsibilities.</span></span> <span data-ttu-id="25679-107">Tehtäviin voi sisältyä esimerkiksi työ- ja sähköpostijonojen tietokantasynkronoinnin hallintaa, käyttäjien määritystä, käyttöliittymän mukautusta ja salausavainten hallintaa.</span><span class="sxs-lookup"><span data-stu-id="25679-107">These tasks can include managing database synchronization of job and email queues, setting up users, customizing the user interface, and managing encryption keys.</span></span>  

<span data-ttu-id="25679-108">Uuden liiketoimintaohjelmiston toimivuuden vuoksi on tärkeää, että syötettävät asetusarvot ovat oikeita alusta alkaen.</span><span class="sxs-lookup"><span data-stu-id="25679-108">Entering the correct setup values from the start is important to the success of any new business software.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="25679-109">issa on useita asetusoppaita, jotka helpottavat perustietojen määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="25679-109"> includes a number of setup guides that help you set up core data.</span></span> <span data-ttu-id="25679-110">Lisätietoja on kohdassa [Finance and Operations, Business editionin määrittäminen](setup.md).</span><span class="sxs-lookup"><span data-stu-id="25679-110">For more information, see [Setting Up Finance and Operations, Business edition](setup.md).</span></span>

<!--Whether you use [!INCLUDE[rim](../../includes/rim_md.md)] to implement setup values or you manually enter them in the new company, you can support your setup decisions with some general recommendations for selected setup fields that are known to potentially cause the solution to be inefficient if defined incorrectly.-->  

<span data-ttu-id="25679-111">Pääkäyttäjä tai järjestelmänvalvoja voi määrittää tietojen vaihtamiskehyksen, jonka avulla käyttäjät voivat viedä ja tuoda pankki- ja palkanlaskentatiedostojen tietoja esimerkiksi erilaisia kassanhallintaprosesseja varten.</span><span class="sxs-lookup"><span data-stu-id="25679-111">A super user or an administrator can set up the Data Exchange Framework to enable users to export and import data in bank and payroll files, for example for various cash management processes.</span></span>  

<span data-ttu-id="25679-112">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="25679-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="25679-113">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="25679-113">**To**</span></span>|<span data-ttu-id="25679-114">**Katso**</span><span class="sxs-lookup"><span data-stu-id="25679-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="25679-115">Lisää käyttäjiä, hallitse tietojen käyttöoikeuksia ja määritä rooleja.</span><span class="sxs-lookup"><span data-stu-id="25679-115">Add users, manage permissions and access to data, assign roles.</span></span>|[<span data-ttu-id="25679-116">Finance and Operations, Business editionin käyttäjät, profiilit ja roolikeskukset</span><span class="sxs-lookup"><span data-stu-id="25679-116">Users, Profiles, and Role Centers in Finance and Operations, Business edition</span></span>](admin-users-profiles-roles.md)|  
|<span data-ttu-id="25679-117">Seuraa kaikkia suoria muutoksia, joita käyttäjät tekevät tietokannan tietoihin. Muutoksia seuraamalla voidaan tunnistaa virheiden alkuperä ja tietojen muutokset.</span><span class="sxs-lookup"><span data-stu-id="25679-117">Track all direct modifications that users make to data in the database to identify the origin of errors and data changes.</span></span>|[<span data-ttu-id="25679-118">Muutosten kirjaaminen Finance and Operations, Business editionissa</span><span class="sxs-lookup"><span data-stu-id="25679-118">Logging Changes in Finance and Operations, Business edition</span></span>](across-log-changes.md)|  
|<span data-ttu-id="25679-119">Tue määritysten suhteen tekemiäsi päätöksiä valittujen kenttien suosituksilla, joiden tiedetään mahdollisesti aiheuttavan sen, että ratkaisu on tehoton, jos se määritetään virheellisesti.</span><span class="sxs-lookup"><span data-stu-id="25679-119">Support your setup decisions with recommendations for selected fields that are known to potentially cause the solution to be inefficient if set up incorrectly</span></span>|[<span data-ttu-id="25679-120">Monimutkaisten sovellusalueiden määrittäminen parhaiden käytäntöjen avulla</span><span class="sxs-lookup"><span data-stu-id="25679-120">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)|  
|<span data-ttu-id="25679-121">Näytä sivuja, koodiyksiköitä ja kyselyitä verkkopalveluina.</span><span class="sxs-lookup"><span data-stu-id="25679-121">Expose pages, codeunits, and queries as web services.</span></span>|[<span data-ttu-id="25679-122">Verkkopalvelun julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="25679-122">Publish a Web Service</span></span>](across-how-publish-web-service.md)|  
|<span data-ttu-id="25679-123">Finance and Operations, Business editionin sisäisen ja ulkoisen sähköpostiviestinnän mahdollistavan SMTP-palvelimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="25679-123">Set up an SMTP server to enable e-mail communication in and out of Finance and Operations, Business edition</span></span>| [<span data-ttu-id="25679-124">Sähköpostin määrittäminen manuaalisesti tai asetusten ohjatun määrityksen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="25679-124">Set Up Email Manually or Using the Assisted Setup</span></span>](madeira-how-setup-email.md)|  
|<span data-ttu-id="25679-125">Määritä yksittäisiä tai toistuvia pyyntöjä raporttien tai koodiyksiköiden suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="25679-125">Enter single or recurring requests to run reports or codeunits.</span></span>|[<span data-ttu-id="25679-126">Käytä työjonoja ajoitustehtäviin</span><span class="sxs-lookup"><span data-stu-id="25679-126">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)|  
|<span data-ttu-id="25679-127">Asiakirjojen hallinta, poistaminen ja pakkaaminen</span><span class="sxs-lookup"><span data-stu-id="25679-127">Manage, delete, or compress documents</span></span>|[<span data-ttu-id="25679-128">Asiakirjojen hallinta</span><span class="sxs-lookup"><span data-stu-id="25679-128">Manage Documents</span></span>](admin-manage-documents.md)|  
|<span data-ttu-id="25679-129">Uuden liiketoimintayksikön määrittäminen mallien avulla</span><span class="sxs-lookup"><span data-stu-id="25679-129">Set up a new business unit using templates</span></span>|<span data-ttu-id="25679-130">[Uusien yritysten luominen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa](about-new-company.md)</span><span class="sxs-lookup"><span data-stu-id="25679-130">[Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md)</span></span>|  

## <a name="see-also"></a><span data-ttu-id="25679-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="25679-131">See Also</span></span>
[<span data-ttu-id="25679-132">Liiketoiminnan toiminnallisuus</span><span class="sxs-lookup"><span data-stu-id="25679-132">Business Functionality</span></span>](madeira-business-functionality.md)  
[<span data-ttu-id="25679-133">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="25679-133">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="25679-134">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="25679-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="25679-135">[Tervetuloa [!INCLUDE[d365fin](includes/d365fin_md.md)]iin!](index.md)</span><span class="sxs-lookup"><span data-stu-id="25679-135">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

