---
title: Linkin muodostaminen tietueista ulkoisiin tietoihin tai ohjelmiin | Microsoft Docs
description: "Liitä hyperlinkki asiakirjaan tai sivusto tiettyyn tietueeseen, kuten asiakkaaseen tai asiakirjaan."
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 876c91aad4463f499ca70d14ba4c0e649353e37b
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="c28f3-103">Sivustojen, asiakirjojen tai ohjelmien linkkien lisääminen tietueissa</span><span class="sxs-lookup"><span data-stu-id="c28f3-103">Adding Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="c28f3-104">Voit lisätä tiettyyn tietueeseen, kuten asiakkaaseen, asiakirjaan tai myyntitilaukseen, linkin ulkoiseen asiakirjaan, sivustoon tai ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="c28f3-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="c28f3-105">Voit myös lisätä linkin, joka avaa uuden, tyhjän sähköpostiviestin, joka on osoitettu tietylle vastaanottajalle.</span><span class="sxs-lookup"><span data-stu-id="c28f3-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="c28f3-106">Joidenkin tietueiden korttisivulla, kuten asiakas- tai toimittajakorteissa, on **Kotisivu**-kenttä, jossa voit antaa verkko- eli URL-osoitteen.</span><span class="sxs-lookup"><span data-stu-id="c28f3-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="c28f3-107">Toisaalla tässä artikkelissa on lisätietoja muiden linkkien sisällyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="c28f3-107">To include other links, you can use the method described in this article.</span></span>

<span data-ttu-id="c28f3-108">Kyse voi olla myös esimerkiksi tulostettujen laskujen vastaanottamisesta toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="c28f3-108">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="c28f3-109">Voit skannata ja tallentaa ne .pdf-tiedostoina SharePoint-sivustossa.</span><span class="sxs-lookup"><span data-stu-id="c28f3-109">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="c28f3-110">Tämän jälkeen voit muodostaa [!INCLUDE[d365fin_md](includes/d365fin_md.md)]in ostolaskusta linkin vastaavaan SharePointissa olevaan laskuun.</span><span class="sxs-lookup"><span data-stu-id="c28f3-110">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="c28f3-111">Voit muodostaa linkin nimikekortista vastaavaan sivuun toimittajan online-kuvastossa.</span><span class="sxs-lookup"><span data-stu-id="c28f3-111">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>

## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="c28f3-112">Linkin lisääminen tietueeseen</span><span class="sxs-lookup"><span data-stu-id="c28f3-112">To add a link on a record</span></span>   

1.  <span data-ttu-id="c28f3-113">Avaa tietue, johon haluat liittää linkin (esimerkiksi asiakaskortti tai myyntitilaus).</span><span class="sxs-lookup"><span data-stu-id="c28f3-113">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="c28f3-114">Jos haluat liittää linkin tietylle riville, kuten päiväkirjan riville, valitse kyseinen rivi.</span><span class="sxs-lookup"><span data-stu-id="c28f3-114">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  

2.  <span data-ttu-id="c28f3-115">Avaa **Linkit**-toiminnolla **Linkit**-ikkuna, jossa kaikki tietueeseen tällä hetkellä lisätyt linkit näkyvät.</span><span class="sxs-lookup"><span data-stu-id="c28f3-115">Choose the **Links** action to open the **Links** windows that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="c28f3-116">Lisää uusi linkki valitsemalla **+uusi**.</span><span class="sxs-lookup"><span data-stu-id="c28f3-116">To add a new link, choose **+new**.</span></span>

4.  <span data-ttu-id="c28f3-117">Anna **Linkin osoite** -kentässä</span><span class="sxs-lookup"><span data-stu-id="c28f3-117">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="c28f3-118">Jos haluat linkittää tietokoneessa tai verkossa olevan tiedoston, anna tiedostopolun ja tiedoston koko nimi, kuten **C:Omat tiedostotLasku1.doc**.</span><span class="sxs-lookup"><span data-stu-id="c28f3-118">To link to a file on your computer or network, enter the full path and file name, such as  **C:My Documentsinvoice1.doc**.</span></span>
    -   <span data-ttu-id="c28f3-119">Luo linkki sivustoon antamalla verkko- eli URL-osoite, kuten **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="c28f3-119">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="c28f3-120">Luo linkki sivustoon antamalla verkko- eli URL-osoite, kuten **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="c28f3-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="c28f3-121">Luo linkki ohjelmaan antamalla ohjelmaan avaava merkkijono.</span><span class="sxs-lookup"><span data-stu-id="c28f3-121">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="c28f3-122">Jos haluat esimerkiksi käynnistää OneNoten siten, että tietty sivu avautuu, anna **onenote:///C:Omat tiedostottesti.one**.</span><span class="sxs-lookup"><span data-stu-id="c28f3-122">For example, to open OneNote with a specific page, enter **onenote:///C:My Documentstest.one**.</span></span> <span data-ttu-id="c28f3-123">Tai jos haluat että tyhjä, tietylle sähköpostitunnukselle osoitettu Outlook-sähköpostiviesti käynnistyy, anna **mailto:testalias**.</span><span class="sxs-lookup"><span data-stu-id="c28f3-123">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5.  <span data-ttu-id="c28f3-124">Kirjoita **Kuvaus**-kenttään linkkiä kuvaavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="c28f3-124">Fill in the **Description** field with information about the link.</span></span>  

6.  <span data-ttu-id="c28f3-125">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="c28f3-125">Choose the **Save** button.</span></span>  

## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="c28f3-126">Linkin poistaminen tietueesta</span><span class="sxs-lookup"><span data-stu-id="c28f3-126">To delete a link from a record</span></span>  

<span data-ttu-id="c28f3-127">Poista linkki valitsemalla **Linkit**-ikkunassa ensin **...** ja sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="c28f3-127">To delete a link, in the **Links** window, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="c28f3-128">Jos poistat yksittäisen tietueen, kuten myyntitilausrivin, myyntitilauksen tai asiakkaan, kaikki tietueeseen liitetyt linkit poistetaan.</span><span class="sxs-lookup"><span data-stu-id="c28f3-128">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="c28f3-129">Jos sen sijaan poistat tietueita käyttämällä eräajoa, kuten **Poista laskutetut myyntitilaukset**, linkit säilyvät tietokantaan tallennettuina.</span><span class="sxs-lookup"><span data-stu-id="c28f3-129">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="c28f3-130">Voit poistaa linkit tietokannasta suorittamalla **Poista orvot tietuelinkit** -koodiyksikön.</span><span class="sxs-lookup"><span data-stu-id="c28f3-130">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="c28f3-131">Voit tehdä valitsemalla ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvakkeen, kirjoittamalla **Poista orvot tietuelinkit** ja valitsemalla sitten aiheeseen liittyvän linkin.</span><span class="sxs-lookup"><span data-stu-id="c28f3-131">To do this, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a><span data-ttu-id="c28f3-132">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c28f3-132">See Also</span></span>  
<span data-ttu-id="c28f3-133">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c28f3-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

