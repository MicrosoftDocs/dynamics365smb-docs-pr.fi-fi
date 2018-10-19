---
title: "Microsoft Flow -integroinnin vianmääritys| Microsoft Docs"
description: "Suorita vianmääritys ja selvitä, miten voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla rakennat automaattisen työkulun."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0818550021bf17e5a269d3e11f8db54b9ff80dfa
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a><span data-ttu-id="745b5-103">Microsoft Flow -integroinnin vianmääritys – pyynnön URL-osoite on liian pitkä</span><span class="sxs-lookup"><span data-stu-id="745b5-103">Troubleshooting Integration with Microsoft Flow - Request URL Too Long</span></span>
<span data-ttu-id="745b5-104">Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja työnkulun osana Microsoft Flow'ssa.</span><span class="sxs-lookup"><span data-stu-id="745b5-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="745b5-105">Sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja Flow-tili.</span><span class="sxs-lookup"><span data-stu-id="745b5-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

<span data-ttu-id="745b5-106">Jos olet luomassa Microsoft Flow'n [!INCLUDE[d365fin](includes/d365fin_md.md)] -yhdistimellä, voit saada työnkulun luomisen jälkeen virhesanoman, jonka mukaan pyydetty URL-osoite on liian pitkä. Viesti voi olla esimerkiksi seuraavanlainen: **RequestUriTooLong**.</span><span class="sxs-lookup"><span data-stu-id="745b5-106">If you are creating a Microsoft Flow using the [!INCLUDE[d365fin](includes/d365fin_md.md)] connector, you may receive an error message stating that the requsted URL is too long after creating the flow, such as the following: **RequestUriTooLong**.</span></span>

## <a name="cause"></a><span data-ttu-id="745b5-107">Syy</span><span class="sxs-lookup"><span data-stu-id="745b5-107">Cause</span></span>
<span data-ttu-id="745b5-108">Työnkulun käynnistyminen edellyttää, että se havaitsee tiedoissa muutoksia.</span><span class="sxs-lookup"><span data-stu-id="745b5-108">For a flow to trigger, it looks for changes in your data.</span></span> <span data-ttu-id="745b5-109">Kun liittimet selvittävät, onko tiedoissa muutoksia, ne vertaavat välimuistiin tallennettuja tietoja lähteestä pyydettyihin uusiin tietoihin.</span><span class="sxs-lookup"><span data-stu-id="745b5-109">When determining if your data has changed, the connectors compare the cached data to the new data requested from the source.</span></span>  

<span data-ttu-id="745b5-110">Jos tietopyyntö luo liian pitkän URL-osoitteen, pyyntö epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="745b5-110">If the data request creates a URL that is too long, it will fail.</span></span> <span data-ttu-id="745b5-111">Yleisiä syitä ovat esimerkiksi seuraavat:</span><span class="sxs-lookup"><span data-stu-id="745b5-111">Common causes may include:</span></span>
- <span data-ttu-id="745b5-112">Yleisesti mikä tahansa taulukko, jossa on yli 250 riviä.</span><span class="sxs-lookup"><span data-stu-id="745b5-112">Generally, any source table with over 250 rows</span></span>
- <span data-ttu-id="745b5-113">Lähdetaulukot, joissa on useita tuhansia tietueita.</span><span class="sxs-lookup"><span data-stu-id="745b5-113">Source tables containing multiple thousands of records</span></span>

## <a name="workaround"></a><span data-ttu-id="745b5-114">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="745b5-114">Workaround</span></span>
<span data-ttu-id="745b5-115">Ongelman voi kiertää seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="745b5-115">Follow these steps as a workaround.</span></span>
1. <span data-ttu-id="745b5-116">Valitse epäonnistuneen työnkulun muokkaus.</span><span class="sxs-lookup"><span data-stu-id="745b5-116">Choose to edit the flow that is failing.</span></span>
2. <span data-ttu-id="745b5-117">Laajenna **Näytä lisäasetukset** työnkulun käynnistimessä.</span><span class="sxs-lookup"><span data-stu-id="745b5-117">Expand the **Show advanced options** on the flow trigger.</span></span>
3. <span data-ttu-id="745b5-118">Anna **Ohita määrä** -kenttään ohitettavien tietueiden määrä.</span><span class="sxs-lookup"><span data-stu-id="745b5-118">In the **Skip Count** field, enter the number of records to skip.</span></span>  
<span data-ttu-id="745b5-119">Jos tietolähteenä käyttämässäsi taulukossa on esimerkiksi 4 000 tietuetta, anna ohittavien tietueiden määräksi 4 000.</span><span class="sxs-lookup"><span data-stu-id="745b5-119">For example, if the table that you are using as a data source has 4,000 records, enter 4,000 as the number of records to skip.</span></span>
4. <span data-ttu-id="745b5-120">Päivitä työnkulku.</span><span class="sxs-lookup"><span data-stu-id="745b5-120">Update your flow.</span></span>

> [!NOTE]  
> <span data-ttu-id="745b5-121">Yhdistimestä on tällä hetkellä käytössä beetaversio.</span><span class="sxs-lookup"><span data-stu-id="745b5-121">The connector is currently in Beta.</span></span> <span data-ttu-id="745b5-122">Tietojen muutokset tullaan ottamaan huomioon tulevien versioiden päivityksissä.</span><span class="sxs-lookup"><span data-stu-id="745b5-122">Updates to how data changes are targeted for a future release.</span></span>


## <a name="see-also"></a><span data-ttu-id="745b5-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="745b5-123">See Also</span></span>
<span data-ttu-id="745b5-124">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="745b5-124">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md)</span></span>  
[<span data-ttu-id="745b5-125">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="745b5-125">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="745b5-126">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="745b5-126">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="745b5-127">[Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="745b5-127">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="745b5-128">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="745b5-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="745b5-129">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="745b5-129">Finance</span></span>](finance.md)  

