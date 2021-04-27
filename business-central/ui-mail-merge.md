---
title: Word-mallien käyttö joukkoviestinnässä | Microsoft Docs
description: Word-mallit helpottavat tietyille entiteeteille mukautettujen asiakirjojen joukkoluontia.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 118d8db1266bb7150965ec4d1ce44ece77638764
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788532"
---
# <a name="using-word-templates-for-bulk-communication"></a><span data-ttu-id="ca317-103">Word-mallien käyttö joukkoviestinnässä</span><span class="sxs-lookup"><span data-stu-id="ca317-103">Using Word Templates for Bulk Communication</span></span>
<span data-ttu-id="ca317-104">Microsoft Word -mallit helpottavat entiteettien, kuten asiakkaiden ja toimittajien, kanssa tapahtuvaa joukkoviestintää.</span><span class="sxs-lookup"><span data-stu-id="ca317-104">Microsoft Word templates can make it easier to mass communicate with entities such as customers and vendors.</span></span> <span data-ttu-id="ca317-105">Voit luoda esimerkiksi esitteitä, joissa kerrotaan asiakkaille myyntikampanjoista, kirjeitä, joissa toimittajille kerrotaan uudesta ostokäytännöstä, tai kutsuja, joilla houkutellaan yhteyshenkilöitä tulevaan tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="ca317-105">For example, you can create brochures to alert customers about a sales campaign, letters to inform vendors about a new purchasing policy, or invitations to attract contacts to an upcoming event.</span></span>

<span data-ttu-id="ca317-106">[!INCLUDE[prod_short](includes/prod_short.md)]in entiteettejä voi käyttää mallin tietolähteinä, ja asiakirjat voidaan mukauttaa kullekin entiteetille lisäämällä yhdistämiskenttiä.</span><span class="sxs-lookup"><span data-stu-id="ca317-106">You can use entities in [!INCLUDE[prod_short](includes/prod_short.md)] as the data source for the template, and add merge fields to personalize documents for each entity.</span></span> <span data-ttu-id="ca317-107">Yhdistämiskentät saadaan [!INCLUDE[prod_short](includes/prod_short.md)]in entiteetistä.</span><span class="sxs-lookup"><span data-stu-id="ca317-107">The merge fields come from the entity in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="ca317-108">Kun Word-mallia käytetään entiteetissä, yhdistämiskenttien tiedot lisätään asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="ca317-108">When you apply a Word template to an entity, data from the merge fields is inserted in the document.</span></span>

<span data-ttu-id="ca317-109">**Word-mallit**-sivulla on asetusten ohjatun määrityksen opas, jolla voi ladata DataSource.txt-tiedoston ja entiteetin Word-mallitiedoston sisältävän ZIP-tiedoston.</span><span class="sxs-lookup"><span data-stu-id="ca317-109">On the **Word Templates** page, you can use an assisted setup guide to download a ZIP file that contains a DataSource.txt and a Word template file for an entity.</span></span> <span data-ttu-id="ca317-110">Kun malli on määritetty ja yhdistämiskentät lisätty, mallin voi ladata takaisin samaa opasta käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="ca317-110">After you set up the template and add merge fields, you use the same guide to upload the template.</span></span> <span data-ttu-id="ca317-111">Voit käyttää vain [!INCLUDE[prod_short](includes/prod_short.md)]ista ladattuja Word-malli- ja tietolähdetiedostoja, ja nämä tiedostot on tallennettava samaan sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="ca317-111">You can only use the Word template and data source files that you download from [!INCLUDE[prod_short](includes/prod_short.md)], and you must store the files in the same location.</span></span>

> [!NOTE]
> <span data-ttu-id="ca317-112">Kun valitset entiteetin, jolle malli luodaan, luettelossa on näkyvissä kaikki [!INCLUDE[prod_short](includes/prod_short.md)]in entiteetit.</span><span class="sxs-lookup"><span data-stu-id="ca317-112">When you choose an entity for which to create a template, the list shows all entities in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="ca317-113">Malleja ei kuitenkaan voi luoda kaikille entiteeteille.</span><span class="sxs-lookup"><span data-stu-id="ca317-113">However, you cannot create templates for all entities.</span></span> <span data-ttu-id="ca317-114">Jos entiteetin nimessä on erikoismerkkejä, kuten **/**, **.**, **_** tai **-**, sille ei voi luoda mallia.</span><span class="sxs-lookup"><span data-stu-id="ca317-114">If the name of an entity contains special characters, such as **/**, **.**, **_**, or **-**, you cannot create a template for it.</span></span> <span data-ttu-id="ca317-115">Entiteetin nimi näkyy **Objektin otsikko** -sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="ca317-115">The name of the entity is shown in the **Object Caption** column.</span></span>

<span data-ttu-id="ca317-116">Kun mallia määritetään Wordissa, yhdistämiskentät voidaan lisätä **Postitukset**-välilehdessä valitsemalla **Lisää yhdistämiskenttä**.</span><span class="sxs-lookup"><span data-stu-id="ca317-116">When you are setting up the template in Word, on the **Mailings** tab you can add merge fields by choosing **Insert Merge Field**.</span></span>

> [!NOTE]
> <span data-ttu-id="ca317-117">Yhdistämiskenttiä ei voi käyttää, jos kentän nimessä on vähintään 40 merkkiä.</span><span class="sxs-lookup"><span data-stu-id="ca317-117">You cannot use merge fields if the name of the field contains 40 characters or more.</span></span> <span data-ttu-id="ca317-118">Esimerkiksi Company__Information_Customs_Permit_Date-kenttää ei voi käyttää, koska siinä on 40 merkkiä.</span><span class="sxs-lookup"><span data-stu-id="ca317-118">For example, you cannot use the Company__Information_Customs_Permit_Date field because it has 40 characters.</span></span> 

<span data-ttu-id="ca317-119">Kun Word-malli on valmis, asiakirjat voidaan luoda valitsemalla **Word-mallit**-sivulla **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="ca317-119">When your Word template is ready, on the **Word Templates** page you can choose **Apply** to generate the documents.</span></span> <span data-ttu-id="ca317-120">Voit luoda joko yhden asiakirjan, jossa on osa kullekin entiteetille, tai jakaa toiminnon luomaan uuden asiakirjan kullekin entiteetille.</span><span class="sxs-lookup"><span data-stu-id="ca317-120">You can either create one document that contains sections for each entity, or split the operation to create a new document for each entity.</span></span>

## <a name="to-create-a-word-template"></a><span data-ttu-id="ca317-121">Word-mallin luominen</span><span class="sxs-lookup"><span data-stu-id="ca317-121">To create a Word template</span></span>
1. <span data-ttu-id="ca317-122">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, kirjoita **Word-mallit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ca317-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Word Templates**, and then choose the related link.</span></span>
2. <span data-ttu-id="ca317-123">Noudata asetusten ohjatun määritysoppaan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="ca317-123">Follow the steps in the assisted setup guide.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="ca317-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ca317-124">See Also</span></span>
[<span data-ttu-id="ca317-125">Raporttien ja asiakirjojen asettelujen hallinta</span><span class="sxs-lookup"><span data-stu-id="ca317-125">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
