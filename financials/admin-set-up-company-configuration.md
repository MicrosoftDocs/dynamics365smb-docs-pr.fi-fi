---
title: "Yrityksen konfiguroinnin määrittäminen | Microsoft Docs"
description: "Toteutusprosessi alkaa Business Central -ratkaisun edellytyksistä. Yhdistä kaikki tämä tieto konfigurointipakettien tietoihin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: eeca45a36e38ab80a63156995a2f11466262d512
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-company-configuration"></a><span data-ttu-id="996ef-104">Määritä yrityksen konfigurointi</span><span class="sxs-lookup"><span data-stu-id="996ef-104">Set Up Company Configuration</span></span>
<span data-ttu-id="996ef-105">Toteutus alkaa Microsoft-kumppanin kanssa.</span><span class="sxs-lookup"><span data-stu-id="996ef-105">The implementation process begins with the Microsoft partner.</span></span> <span data-ttu-id="996ef-106">Kumppani on vastuussa määritystietojen tarkistamisesta ja helposti asiakkaan käytettävissä olevan paketin luomisesta.</span><span class="sxs-lookup"><span data-stu-id="996ef-106">The partner is responsible for thinking through the configuration details and creating a package that a customer can easily apply.</span></span> <span data-ttu-id="996ef-107">Ennen kuin luot uuden yhtiön, suunnittele, miten se määritetään.</span><span class="sxs-lookup"><span data-stu-id="996ef-107">Before you create a new company, you should plan how it will be configured.</span></span> <span data-ttu-id="996ef-108">Ota huomioon perusasennuksen tiedot ja tietotyypit, joita [!INCLUDE[d365fin](includes/d365fin_md.md)] -ratkaisusi edellyttää.</span><span class="sxs-lookup"><span data-stu-id="996ef-108">You must consider basic setup data and the types of data that your [!INCLUDE[d365fin](includes/d365fin_md.md)] solution will require.</span></span> <span data-ttu-id="996ef-109">Yhdistä kaikki tämä tieto määrityspakettien tietoihin.</span><span class="sxs-lookup"><span data-stu-id="996ef-109">You bundle all of this information in configuration packages.</span></span>

<span data-ttu-id="996ef-110">RapidStart Services tarjoaa myös työkalut, joiden avulla voi siirtää vanhat tiedot, kuten asiakkaiden ja toimittajien tiedot.</span><span class="sxs-lookup"><span data-stu-id="996ef-110">RapidStart Services also provides you with the tools that you will use to migrate your legacy data, such as customers and vendors.</span></span>  

<span data-ttu-id="996ef-111">On suositeltavaa luoda määrityspaketit, joissa on useimmat asetustaulukot jo täytetty, niin, että asiakkaiden tulee vain muuttaa joitakin asetuksia paketin asentamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="996ef-111">We recommend that you create configuration packages with most of the setup tables already filled in, so that customers only have to change a few settings after the package is applied.</span></span> <span data-ttu-id="996ef-112">Kun esimerkiksi luot uuden yrityksen, **Nrosarja**- ja **Nrosarjan rivi** -taulukkoon täytetään numerosarjojen ja aloitusnumeroiden joukot.</span><span class="sxs-lookup"><span data-stu-id="996ef-112">For example, when you create a new company, the **No. Series** and the **No. Series Line** tables are filled in with a set of number series and starting numbers.</span></span> <span data-ttu-id="996ef-113">Vastaavat **Nrosarja** -kentät asetustaulukoissa täytetään myös automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="996ef-113">The corresponding **No. Series** fields in the setup tables are also filled in automatically.</span></span> <span data-ttu-id="996ef-114">Sinun ei tarvitse syöttää numerosarjoja ja muita perusasennuksen tietoja.</span><span class="sxs-lookup"><span data-stu-id="996ef-114">You do not have to do the work of entering number series and other basic setup data.</span></span> <span data-ttu-id="996ef-115">Voi muuttaa myös manuaalisesti kokoonpanotyökirjan avulla kaikki oletustiedot, joita RapidStart Services käyttää.</span><span class="sxs-lookup"><span data-stu-id="996ef-115">You can also manually change all default data that is used with RapidStart Services by using the configuration worksheet.</span></span>  

<span data-ttu-id="996ef-116">Kokoonpanopaketit on valmistettu esimääritellylle yritykselle.</span><span class="sxs-lookup"><span data-stu-id="996ef-116">The configuration packages are built on a preconfigured company.</span></span> <span data-ttu-id="996ef-117">Kun olet määrittänyt yhtiön, joka vastaa tarpeitasi, voit luoda määrityspaketin, joka sisältää tarvittavat tiedot kyseisestä yhtiöstä.</span><span class="sxs-lookup"><span data-stu-id="996ef-117">After you have set up a company that meets your needs, you can create a configuration package that contains relevant data from this company.</span></span> <span data-ttu-id="996ef-118">Voit sitten käyttää sitä, kun luot uuden yhtiön, joka on määritettävä samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="996ef-118">You can then use it when you create a new company that is to be configured in the same way.</span></span>  

<span data-ttu-id="996ef-119">Päätietojen, kuten asiakkaan ja toimittajan tietojen tuonnin helpottamiseksi voit käyttää kokoonpanomalleja.</span><span class="sxs-lookup"><span data-stu-id="996ef-119">To facilitate the import of master data, such as customer and vendor information, you can use configuration templates.</span></span> <span data-ttu-id="996ef-120">Määritysmallit sisältävät oletusasetukset, jotka määritetään automaattisesti tietueisiin, jotka tuodaan kohteeseen [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="996ef-120">Configuration templates contain a set of default settings that are automatically assigned to the records imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="996ef-121">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="996ef-121">The following table describes a sequence of tasks with links to topics that describe them.</span></span>

|<span data-ttu-id="996ef-122">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="996ef-122">**To**</span></span>|<span data-ttu-id="996ef-123">**Katso**</span><span class="sxs-lookup"><span data-stu-id="996ef-123">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="996ef-124">Suunnittele yrityksen määritystä täyttämällä määritystyökirja.</span><span class="sxs-lookup"><span data-stu-id="996ef-124">Plan a company configuration by filling in the configuration worksheet.</span></span>|[<span data-ttu-id="996ef-125">Yrityksen määrittämisen hallinta työkirjassa</span><span class="sxs-lookup"><span data-stu-id="996ef-125">Manage Company Configuration in a Worksheet</span></span>](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|<span data-ttu-id="996ef-126">Luo määrityspaketti, mukauta pakettia, liitä pakettiin taulukoita, tarkista olemassa olevat asiakastiedot tai muokkaa niitä, luo uusi yritys ja siirrä sitten testitiedot tuotantoympäristöön.</span><span class="sxs-lookup"><span data-stu-id="996ef-126">Create a configuration package, customize a package, assign tables to a package, review or edit existing customer data, create the new company and then move test data to the production environment.</span></span>|[<span data-ttu-id="996ef-127">Määrityspaketin valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="996ef-127">Prepare a Configuration Package</span></span>](admin-how-to-prepare-a-configuration-package.md)| 

## <a name="see-also"></a><span data-ttu-id="996ef-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="996ef-128">See Also</span></span>  
[<span data-ttu-id="996ef-129">Yrityksen määrittäminen RapidStart Services -palvelun avulla</span><span class="sxs-lookup"><span data-stu-id="996ef-129">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="996ef-130">Hallinta</span><span class="sxs-lookup"><span data-stu-id="996ef-130">Administration</span></span>](admin-setup-and-administration.md)

