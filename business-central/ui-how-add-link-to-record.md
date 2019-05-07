---
title: Linkin muodostaminen tietueista ulkoisiin tietoihin tai ohjelmiin | Microsoft Docs
description: Liitä hyperlinkki asiakirjaan tai sivusto tiettyyn tietueeseen, kuten asiakkaaseen tai asiakirjaan.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/12/2019
ms.author: jswymer
ms.openlocfilehash: 602d520043c5192109ccc4e2605ae0e231dafc1e
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/12/2019
ms.locfileid: "990175"
---
# <a name="add-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="653f8-103">Sivustojen, asiakirjojen tai ohjelmien linkkien lisääminen tietueissa</span><span class="sxs-lookup"><span data-stu-id="653f8-103">Add Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="653f8-104">Voit lisätä tiettyyn tietueeseen, kuten asiakkaaseen, asiakirjaan tai myyntitilaukseen, linkin ulkoiseen asiakirjaan, sivustoon tai ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="653f8-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="653f8-105">Voit myös lisätä linkin, joka avaa uuden, tyhjän sähköpostiviestin, joka on osoitettu tietylle vastaanottajalle.</span><span class="sxs-lookup"><span data-stu-id="653f8-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="653f8-106">Joidenkin tietueiden korttisivulla, kuten asiakas- tai toimittajakorteissa, on **Kotisivu**-kenttä, jossa voit antaa verkko- eli URL-osoitteen.</span><span class="sxs-lookup"><span data-stu-id="653f8-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="653f8-107">Toisaalla tässä artikkelissa on lisätietoja muiden linkkien sisällyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="653f8-107">To include other links, you can use the method described in this article.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="653f8-108">Tällä hetkellä tämä ominaisuus on käytettävissä vain paikallisissa [!INCLUDE [prodshort](includes/prodshort.md)] -käyttöönotoissa vanhan Dynamics NAV Windows -asiakasohjelman kanssa.</span><span class="sxs-lookup"><span data-stu-id="653f8-108">Currently, this capability is available only in [!INCLUDE [prodshort](includes/prodshort.md)] on-premises deployments with the legacy Dynamics NAV Windows client.</span></span>  

<span data-ttu-id="653f8-109">Kyse voi olla myös esimerkiksi tulostettujen laskujen vastaanottamisesta toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="653f8-109">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="653f8-110">Voit skannata ja tallentaa ne .pdf-tiedostoina SharePoint-sivustossa.</span><span class="sxs-lookup"><span data-stu-id="653f8-110">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="653f8-111">Tämän jälkeen voit muodostaa [!INCLUDE[d365fin_md](includes/d365fin_md.md)]in ostolaskusta linkin vastaavaan SharePointissa olevaan laskuun.</span><span class="sxs-lookup"><span data-stu-id="653f8-111">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="653f8-112">Voit muodostaa linkin nimikekortista vastaavaan sivuun toimittajan online-kuvastossa.</span><span class="sxs-lookup"><span data-stu-id="653f8-112">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>

## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="653f8-113">Linkin lisääminen tietueeseen</span><span class="sxs-lookup"><span data-stu-id="653f8-113">To add a link on a record</span></span>   

1.  <span data-ttu-id="653f8-114">Avaa tietue, johon haluat liittää linkin (esimerkiksi asiakaskortti tai myyntitilaus).</span><span class="sxs-lookup"><span data-stu-id="653f8-114">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="653f8-115">Jos haluat liittää linkin tietylle riville, kuten päiväkirjan riville, valitse kyseinen rivi.</span><span class="sxs-lookup"><span data-stu-id="653f8-115">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  

2.  <span data-ttu-id="653f8-116">Avaa **Linkit**-toiminnolla **Linkit**-sivut, joissa kaikki tietueeseen tällä hetkellä lisätyt linkit näkyvät.</span><span class="sxs-lookup"><span data-stu-id="653f8-116">Choose the **Links** action to open the **Links** pages that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="653f8-117">Lisää uusi linkki valitsemalla **+uusi**.</span><span class="sxs-lookup"><span data-stu-id="653f8-117">To add a new link, choose **+new**.</span></span>

4.  <span data-ttu-id="653f8-118">Anna **Linkin osoite** -kentässä</span><span class="sxs-lookup"><span data-stu-id="653f8-118">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="653f8-119">Jos haluat linkittää tietokoneessa tai verkossa olevan tiedoston, anna tiedostopolun ja tiedoston koko nimi, kuten **C:Omat tiedostotLasku1.doc**.</span><span class="sxs-lookup"><span data-stu-id="653f8-119">To link to a file on your computer or network, enter the full path and file name, such as  **C:My Documentsinvoice1.doc**.</span></span>
    -   <span data-ttu-id="653f8-120">Luo linkki sivustoon antamalla verkko- eli URL-osoite, kuten **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="653f8-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="653f8-121">Luo linkki sivustoon antamalla verkko- eli URL-osoite, kuten **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="653f8-121">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="653f8-122">Luo linkki ohjelmaan antamalla ohjelmaan avaava merkkijono.</span><span class="sxs-lookup"><span data-stu-id="653f8-122">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="653f8-123">Jos haluat esimerkiksi käynnistää OneNoten siten, että tietty sivu avautuu, anna **onenote:///C:Omat tiedostottesti.one**.</span><span class="sxs-lookup"><span data-stu-id="653f8-123">For example, to open OneNote with a specific page, enter **onenote:///C:My Documentstest.one**.</span></span> <span data-ttu-id="653f8-124">Tai jos haluat että tyhjä, tietylle sähköpostitunnukselle osoitettu Outlook-sähköpostiviesti käynnistyy, anna **mailto:testalias**.</span><span class="sxs-lookup"><span data-stu-id="653f8-124">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5.  <span data-ttu-id="653f8-125">Kirjoita **Kuvaus**-kenttään linkkiä kuvaavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="653f8-125">Fill in the **Description** field with information about the link.</span></span>  

6.  <span data-ttu-id="653f8-126">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="653f8-126">Choose the **Save** button.</span></span>  

## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="653f8-127">Linkin poistaminen tietueesta</span><span class="sxs-lookup"><span data-stu-id="653f8-127">To delete a link from a record</span></span>  

<span data-ttu-id="653f8-128">Poista linkki valitsemalla **Linkit**-sivulla ensin **...** ja sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="653f8-128">To delete a link, on the **Links** page, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="653f8-129">Jos poistat yksittäisen tietueen, kuten myyntitilausrivin, myyntitilauksen tai asiakkaan, kaikki tietueeseen liitetyt linkit poistetaan.</span><span class="sxs-lookup"><span data-stu-id="653f8-129">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="653f8-130">Jos sen sijaan poistat tietueita käyttämällä eräajoa, kuten **Poista laskutetut myyntitilaukset**, linkit säilyvät tietokantaan tallennettuina.</span><span class="sxs-lookup"><span data-stu-id="653f8-130">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="653f8-131">Voit poistaa linkit tietokannasta suorittamalla **Poista orvot tietuelinkit** -koodiyksikön.</span><span class="sxs-lookup"><span data-stu-id="653f8-131">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="653f8-132">Jos haluat tehdä näin, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poista orvot tietuelinkit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="653f8-132">To do this, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a><span data-ttu-id="653f8-133">Katso myös</span><span class="sxs-lookup"><span data-stu-id="653f8-133">See Also</span></span>  
<span data-ttu-id="653f8-134">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="653f8-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
