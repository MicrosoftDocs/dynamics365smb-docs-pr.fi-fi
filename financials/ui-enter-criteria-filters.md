---
title: "Suodattimien hakuehtojen määrittäminen | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten suodattimilla, kuten pikasuodattimella, voi tarkentaa tietojen hakutuloksia."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="entering-criteria-in-filters"></a><span data-ttu-id="d3ee0-103">Ehtojen syöttäminen suodattimiin</span><span class="sxs-lookup"><span data-stu-id="d3ee0-103">Entering Criteria in Filters</span></span>
<span data-ttu-id="d3ee0-104">Syötä ehtoja, kun haluat etsiä tiettyjä tietoja, kuten asiakkaiden nimiä, osoitteita tai tuoteryhmiä.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-104">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="d3ee0-105">Hakuehdoissa voi käyttää kaikkia numeroita ja kirjaimia, joita kentissä yleensä käytetään.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-105">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="d3ee0-106">Lisäksi voit käyttää tulosten suodatukseen erikoismerkkejä.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-106">In addition, you can use special symbols to further filter the results.</span></span>

## <a name="searching-using-the-quick-filter"></a><span data-ttu-id="d3ee0-107">Haku pikasuodattimen avulla</span><span class="sxs-lookup"><span data-stu-id="d3ee0-107">Searching using the Quick Filter</span></span>
<span data-ttu-id="d3ee0-108">Pikasuodattimen avulla voit lisätä suodattimia kaikille sivuille.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-108">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="d3ee0-109">Pikasuodatin otetaan käyttöön valitsemalla sivun oikeassa yläkulmassa oleva suurennuslasikuvake.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-109">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="d3ee0-110">Tätä suodatustyyppiä käytetään ehtojen nopeassa syöttämisessä.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-110">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="d3ee0-111">Pikasuodatin tarjoaa helpon pääsyn tietojen suodatukseen kirjaamalla pelkkä teksti, mutta ei tarjoa paljoa hakukriteerivaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-111">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="d3ee0-112">Pikasuodatin toimii eri tavalla riippuen siitä, kirjoitatko tekstiä tai tekstiä symboleilla.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-112">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="d3ee0-113">Jos kirjoitat hakuehtoon pelkän tekstin, hakuehto tulkitaan hauksi, joka ei huomioi kirjainkokoa ja joka sisältää tietyn tekstin.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-113">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="d3ee0-114">Jos kirjoitat hakuehtoon tekstiä, joka sisältää symboleja, hakuehto tulkitaan juuri siten kuin kirjoitit sen ja haun kirjainkoko on merkitsevä.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-114">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="d3ee0-115">Pikasuodattimen ehdot</span><span class="sxs-lookup"><span data-stu-id="d3ee0-115">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="d3ee0-116">Hakuehdot</span><span class="sxs-lookup"><span data-stu-id="d3ee0-116">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="d3ee0-117">Tulkinta...</span><span class="sxs-lookup"><span data-stu-id="d3ee0-117">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="d3ee0-118">Palautukset...</span><span class="sxs-lookup"><span data-stu-id="d3ee0-118">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="d3ee0-119">man</span><span class="sxs-lookup"><span data-stu-id="d3ee0-119">man</span></span></TD>
    <TD><span data-ttu-id="d3ee0-120">@&#42;valm&#42;</span><span class="sxs-lookup"><span data-stu-id="d3ee0-120">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="d3ee0-121">Kaikki tietueet, jotka sisältävät tekstin <b>mies</b> ja kirjainkokoa huomioimatta.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-121">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="d3ee0-122">se</span><span class="sxs-lookup"><span data-stu-id="d3ee0-122">se</span></span></TD>
    <TD><span data-ttu-id="d3ee0-123">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="d3ee0-123">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="d3ee0-124">Kaikki tietueet, jotka sisältävät tekstin <b>se</b> ja kirjainkokoa huomioimatta.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-124">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="d3ee0-125">Valm&#42;</span><span class="sxs-lookup"><span data-stu-id="d3ee0-125">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="d3ee0-126">Alussa <b>Valm</b> ja kirjainkoolla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-126">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="d3ee0-127">Kaikki tietueet, jotka alkavat tekstillä <b>Mies</b>.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-127">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="d3ee0-128">'man'</span><span class="sxs-lookup"><span data-stu-id="d3ee0-128">'man'</span></span></TD>
    <TD><span data-ttu-id="d3ee0-129">Täsmällinen teksti ja kirjainkoolla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-129">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="d3ee0-130">Kaikki tietueet, jotka vastaavat täsmälleen tekstiä <b>mies</b>.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-130">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="d3ee0-131">@man*</span><span class="sxs-lookup"><span data-stu-id="d3ee0-131">@man*</span></span> </TD>
    <TD><span data-ttu-id="d3ee0-132">Alkaa ja kirjainkoolla ei ole merkitystä.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-132">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="d3ee0-133">Kaikki tietueet, jotka alkavat tekstillä <b>mies</b>.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-133">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="d3ee0-134">@&#42;valm</span><span class="sxs-lookup"><span data-stu-id="d3ee0-134">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="d3ee0-135">Päättyy ja kirjainkoolla ei ole merkitystä.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-135">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="d3ee0-136">Kaikki tietueet, jotka päättyvät tekstiin <b>mies</b>.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-136">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="d3ee0-137">Yleismerkkejä ei voi käyttää luettelointikenttien suodattamiseen. Tällainen kenttä on esimerkiksi myyntitilausten **Tila**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-137">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="d3ee0-138">Voit syöttää suodattimen tämäntyyppiselle kentälle kirjoittamalla numeerisen arvon suodatusparametriksi.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-138">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="d3ee0-139">Esimerkiksi **Tila**-kenttä myyntitilauksessa, jolla on arvot **Avoin**, **vapautettu**,**Odottaa hyväksyntää** ja **Odottaa ennakkomaksua**, suodata nämä asetukset käyttämällä arvoja **0**,**1**,**2** ja **3**.</span><span class="sxs-lookup"><span data-stu-id="d3ee0-139">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d3ee0-140">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d3ee0-140">See Also</span></span>
<span data-ttu-id="d3ee0-141">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d3ee0-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

