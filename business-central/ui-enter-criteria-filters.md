---
title: Tietojen etsiminen ja suodatusehtojen antaminen | Microsoft Docs
description: "Tässä ohjeaiheessa kerrotaan, miten suodattimilla, kuten pikasuodattimella, voi tarkentaa tietojen hakutuloksia."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a7fd74ad235e51b1793b02e19834bdb0bd17820b
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="searching-filtering-and-sorting-data"></a><span data-ttu-id="ac4ed-103">Tietojen etsiminen, suodattaminen ja lajitteleminen</span><span class="sxs-lookup"><span data-stu-id="ac4ed-103">Searching, Filtering, and Sorting Data</span></span>
<span data-ttu-id="ac4ed-104">Luettelossa olevien tietojen etsimistä, paikallistamista ja skannaamista voi helpottaa muutamilla keinoilla.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-104">There are a few things that you can do that will help you find, pinpoint, and scan records in a list.</span></span> <span data-ttu-id="ac4ed-105">Näitä keinoja ovat esimerkiksi lajitteleminen, etsiminen ja suodattaminen.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-105">These include sorting, searching and filtering.</span></span>

<span data-ttu-id="ac4ed-106">Syötä ehtoja, kun haluat etsiä tiettyjä tietoja, kuten asiakkaiden nimiä, osoitteita tai tuoteryhmiä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-106">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="ac4ed-107">Hakuehdoissa voi käyttää kaikkia numeroita ja kirjaimia, joita kentissä yleensä käytetään.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-107">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="ac4ed-108">Lisäksi voit käyttää tulosten suodatukseen erikoismerkkejä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-108">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="ac4ed-109">Käytössä on kaksi hakutapaa: pikasuodatin ja sarakesuodattimet.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-109">There are two ways to search: using the Quick Filter or column filters.</span></span>

## <a name="sorting"></a><span data-ttu-id="ac4ed-110">Lajittelu</span><span class="sxs-lookup"><span data-stu-id="ac4ed-110">Sorting</span></span>
<span data-ttu-id="ac4ed-111">Lajittelun avulla tiedoista saa nopeasti ja kätevästi yleiskuvan.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="ac4ed-112">Jos asiakkaita on useita, saat tarvitsemasi yleiskuvan lajittelemalla heidät esimerkiksi **Asiakasnro**-, **Asiakkaan kirjausryhmä**-, **Valuuttakoodi**-, **Maa-/aluekoodi**- tai **ALV-rekisteröintinro**-kohdan avulla,</span><span class="sxs-lookup"><span data-stu-id="ac4ed-112">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="ac4ed-113">Voit lajitella luettelon joko valitsemalla sarakkeen otsikkotekstin ja vaihtelemalla nousevaa ja laskevaa lajittelua tai valitsemalla sarakeotsikossa olevilla pienillä nuolilla **Nouseva**- tai **Laskeva** -vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-113">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small downs arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="ac4ed-114">Lajittelua taulukkoon kuulumattomien kuvien, BLOB-kenttien ja FlowFilter-suodattimien lajittelua ei tueta.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-114">Sorting is not supported images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching-by-using-the-quick-filter"></a><span data-ttu-id="ac4ed-115">Haku pikasuodattimen avulla</span><span class="sxs-lookup"><span data-stu-id="ac4ed-115">Searching by using the Quick Filter</span></span>
<span data-ttu-id="ac4ed-116">Pikasuodattimen avulla voit lisätä suodattimia kaikille sivuille.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-116">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="ac4ed-117">Pikasuodatin otetaan käyttöön valitsemalla sivun oikeassa yläkulmassa oleva suurennuslasikuvake.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-117">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="ac4ed-118">Tätä suodatustyyppiä käytetään ehtojen nopeassa syöttämisessä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-118">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="ac4ed-119">Pikasuodatin tarjoaa helpon pääsyn tietojen suodatukseen kirjaamalla pelkkä teksti, mutta ei tarjoa paljoa hakukriteerivaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-119">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="ac4ed-120">Pikasuodatin toimii eri tavalla riippuen siitä, kirjoitatko tekstiä tai tekstiä symboleilla.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-120">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="ac4ed-121">Jos kirjoitat hakuehtoon pelkän tekstin, hakuehto tulkitaan hauksi, joka ei huomioi kirjainkokoa ja joka sisältää tietyn tekstin.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-121">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="ac4ed-122">Jos kirjoitat hakuehtoon tekstiä, joka sisältää symboleja, hakuehto tulkitaan juuri siten kuin kirjoitit sen ja haun kirjainkoko on merkitsevä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-122">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="ac4ed-123">Pikasuodattimen ehdot</span><span class="sxs-lookup"><span data-stu-id="ac4ed-123">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="ac4ed-124">Hakuehdot</span><span class="sxs-lookup"><span data-stu-id="ac4ed-124">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="ac4ed-125">Tulkinta...</span><span class="sxs-lookup"><span data-stu-id="ac4ed-125">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="ac4ed-126">Palautukset...</span><span class="sxs-lookup"><span data-stu-id="ac4ed-126">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="ac4ed-127">man</span><span class="sxs-lookup"><span data-stu-id="ac4ed-127">man</span></span></TD>
    <TD><span data-ttu-id="ac4ed-128">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="ac4ed-128">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="ac4ed-129">Kaikki tietueet, jotka sisältävät tekstin <b>man</b> ja kirjainkokoa huomioimatta.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-129">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="ac4ed-130">se</span><span class="sxs-lookup"><span data-stu-id="ac4ed-130">se</span></span></TD>
    <TD><span data-ttu-id="ac4ed-131">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="ac4ed-131">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="ac4ed-132">Kaikki tietueet, jotka sisältävät tekstin <b>se</b> ja kirjainkokoa huomioimatta.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-132">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="ac4ed-133">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="ac4ed-133">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="ac4ed-134">Alussa <b>Man</b> ja kirjainkoolla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-134">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="ac4ed-135">Kaikki tietueet, jotka alkavat tekstillä <b>Man</b>.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-135">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="ac4ed-136">'man'</span><span class="sxs-lookup"><span data-stu-id="ac4ed-136">'man'</span></span></TD>
    <TD><span data-ttu-id="ac4ed-137">Täsmällinen teksti ja kirjainkoolla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-137">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="ac4ed-138">Kaikki tietueet, jotka vastaavat täsmälleen tekstiä <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-138">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="ac4ed-139">@man\*</span><span class="sxs-lookup"><span data-stu-id="ac4ed-139">@man\*</span></span> </TD>
    <TD><span data-ttu-id="ac4ed-140">Alkaa ja kirjainkoolla ei ole merkitystä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-140">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="ac4ed-141">Kaikki tietueet, jotka alkavat tekstillä <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-141">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="ac4ed-142">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="ac4ed-142">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="ac4ed-143">Päättyy ja kirjainkoolla ei ole merkitystä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-143">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="ac4ed-144">Kaikki tietueet, jotka päättyvät tekstiin <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-144">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="ac4ed-145">Yleismerkkejä ei voi käyttää luettelointikenttien suodattamiseen. Tällainen kenttä on esimerkiksi myyntitilausten **Tila**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-145">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="ac4ed-146">Voit syöttää suodattimen tämäntyyppiselle kentälle kirjoittamalla numeerisen arvon suodatusparametriksi.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-146">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="ac4ed-147">Esimerkiksi **Tila**-kenttä myyntitilauksessa, jolla on arvot **Avoin**, **vapautettu**,**Odottaa hyväksyntää** ja **Odottaa ennakkomaksua**, suodata nämä asetukset käyttämällä arvoja **0**,**1**,**2** ja **3**.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-147">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span> 

## <a name="searching-by-using-column-filters"></a><span data-ttu-id="ac4ed-148">Haku sarakkeen suodattimien avulla</span><span class="sxs-lookup"><span data-stu-id="ac4ed-148">Searching by using column Filters</span></span>
<span data-ttu-id="ac4ed-149">Voit lisätä suodattimen vähintään yhteen luettelon sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-149">You can add a filter on one or more columns in a list.</span></span> <span data-ttu-id="ac4ed-150">Sarakkeiden suodattaminen on pikasuodattimen käyttöä joustavampaa ja monipuolisempaa.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-150">Filtering on columns is more flexible and enhanced than the Quick Filter.</span></span> 

### <a name="to-add-a-filter-on-a-column"></a><span data-ttu-id="ac4ed-151">Suodattimen lisääminen sarakkeeseen</span><span class="sxs-lookup"><span data-stu-id="ac4ed-151">To add a filter on a column</span></span>
1.  <span data-ttu-id="ac4ed-152">Siirry ennen suodattimen lisäämistä luettelonäkymään valitsemalla ![Näytä luettelona](media/ui_show_as_list_icon.png "Näytä luettelona, vasen nuoli") -kuvake.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-152">Before you add a filter, choose ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to change to the list view.</span></span>
2. <span data-ttu-id="ac4ed-153">Valitse sarakkeen otsikossa ensin alanuoli ja sitten **Suodata**.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-153">Choose the downwards arrow in the column heading, and then choose **Filter**.</span></span>
3. <span data-ttu-id="ac4ed-154">Tee jompikumpi seuraavista toimista:</span><span class="sxs-lookup"><span data-stu-id="ac4ed-154">Do one of the following:</span></span> 
  -  <span data-ttu-id="ac4ed-155">Valitse luettelosta arvo valitsemalla ruudun vieressä *...*.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-155">Choose *...* next to the box to select a value from a list.</span></span>
  -  <span data-ttu-id="ac4ed-156">Anna suodatusehdot ruudussa.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-156">Enter filter criteria in the box.</span></span> <span data-ttu-id="ac4ed-157">Lisätietoja on seuraavassa osiossa.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-157">See the next section for details.</span></span>
4. <span data-ttu-id="ac4ed-158">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-158">Choose the **OK** button.</span></span>

## <a name="filter-criteria-and-symbols"></a><span data-ttu-id="ac4ed-159">Suodatusehdot ja merkit</span><span class="sxs-lookup"><span data-stu-id="ac4ed-159">Filter criteria and symbols</span></span>
<span data-ttu-id="ac4ed-160">Kun syötät kriteerejä, voit käyttää kaikkia numeroita ja kirjaimia, joita voi yleensäkin käyttää kentässä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-160">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="ac4ed-161">Voit käyttää tulosten suodatukseen myös erikoismerkkejä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-161">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="ac4ed-162">Seuraavassa taulukossa on esitelty symbolit, joita voi käyttää suodattimissa.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-162">The following tables show the symbols which can be used in filters.</span></span>  
  
> [!IMPORTANT]  
>  <span data-ttu-id="ac4ed-163">Joissakin tilanteissa kentät arvot voivat sisältää näitä merkkejä, ja haluat suodattaa niiden avulla.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-163">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="ac4ed-164">Siinä tapauksessa on merkki on lisättävä suodatuslausekkeeseen lainausmerkeissä (”).</span><span class="sxs-lookup"><span data-stu-id="ac4ed-164">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="ac4ed-165">Jos haluat esimerkiksi suodattaa tietueita, joiden alussa on teksti *S&R*, suodatuslauseke on **'S&R\*'**.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-165">For example, if you want to filter on records that start with the text *S&R*, the filter expression is **'S&R\*'**.</span></span>  
  
### <a name="-interval"></a><span data-ttu-id="ac4ed-166">(..) väli</span><span class="sxs-lookup"><span data-stu-id="ac4ed-166">(..) Interval</span></span>  
  
|<span data-ttu-id="ac4ed-167">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="ac4ed-167">Sample Expression</span></span>|<span data-ttu-id="ac4ed-168">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="ac4ed-168">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="ac4ed-169">1100..2100</span><span class="sxs-lookup"><span data-stu-id="ac4ed-169">1100..2100</span></span>|<span data-ttu-id="ac4ed-170">Numerot 1100 - 2100</span><span class="sxs-lookup"><span data-stu-id="ac4ed-170">Numbers 1100 through 2100</span></span>|  
|<span data-ttu-id="ac4ed-171">..2500</span><span class="sxs-lookup"><span data-stu-id="ac4ed-171">..2500</span></span>|<span data-ttu-id="ac4ed-172">Numeroon 2500 asti, 2500 mukaan lukien</span><span class="sxs-lookup"><span data-stu-id="ac4ed-172">Up to and including 2500</span></span>|  
|<span data-ttu-id="ac4ed-173">..12 31 00</span><span class="sxs-lookup"><span data-stu-id="ac4ed-173">..12 31 00</span></span>|<span data-ttu-id="ac4ed-174">Päivämäärät 31.12.00 asti, kyseinen päivämäärä mukaan lukien</span><span class="sxs-lookup"><span data-stu-id="ac4ed-174">Dates up to and including 12 31 00</span></span>|  
|<span data-ttu-id="ac4ed-175">P8..</span><span class="sxs-lookup"><span data-stu-id="ac4ed-175">P8..</span></span>|<span data-ttu-id="ac4ed-176">Tiedot kirjanpitojaksosta 8 ja siitä eteenpäin</span><span class="sxs-lookup"><span data-stu-id="ac4ed-176">Information for accounting period 8 and thereafter</span></span>|  
|<span data-ttu-id="ac4ed-177">..23</span><span class="sxs-lookup"><span data-stu-id="ac4ed-177">..23</span></span>|<span data-ttu-id="ac4ed-178">Alkupäivämäärästä lähtien päivään 23 nykyistä kuukautta nykyistä vuotta klo 23:59:59</span><span class="sxs-lookup"><span data-stu-id="ac4ed-178">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|<span data-ttu-id="ac4ed-179">23..</span><span class="sxs-lookup"><span data-stu-id="ac4ed-179">23..</span></span>|<span data-ttu-id="ac4ed-180">Päivästä 23 nykyistä kuukautta nykyistä vuotta klo 00:00:00 ajan loppuun asti</span><span class="sxs-lookup"><span data-stu-id="ac4ed-180">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|<span data-ttu-id="ac4ed-181">22..23</span><span class="sxs-lookup"><span data-stu-id="ac4ed-181">22..23</span></span>|<span data-ttu-id="ac4ed-182">Päivästä 22 nykyistä kuukautta nykyistä vuotta klo 0:00:00 päivään 23 nykyistä kuukautta nykyistä vuotta klo 23:59:59</span><span class="sxs-lookup"><span data-stu-id="ac4ed-182">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  
  
### <a name="124-eitheror"></a><span data-ttu-id="ac4ed-183">(&#124;) joko/tai</span><span class="sxs-lookup"><span data-stu-id="ac4ed-183">(&#124;) Either/or</span></span>  
  
|<span data-ttu-id="ac4ed-184">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="ac4ed-184">Sample Expression</span></span>|<span data-ttu-id="ac4ed-185">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="ac4ed-185">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="ac4ed-186">1200&#124;1300</span><span class="sxs-lookup"><span data-stu-id="ac4ed-186">1200&#124;1300</span></span>|<span data-ttu-id="ac4ed-187">Numerot, joissa on 1200 tai 1300</span><span class="sxs-lookup"><span data-stu-id="ac4ed-187">Numbers with 1200 or 1300</span></span>|  
  
### <a name="-not-equal-to"></a><span data-ttu-id="ac4ed-188">(<>) ei ole sama kuin</span><span class="sxs-lookup"><span data-stu-id="ac4ed-188">(<>) Not equal to</span></span>  
  
|<span data-ttu-id="ac4ed-189">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="ac4ed-189">Sample Expression</span></span>|<span data-ttu-id="ac4ed-190">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="ac4ed-190">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="ac4ed-191"><>0</span><span class="sxs-lookup"><span data-stu-id="ac4ed-191"><>0</span></span>|<span data-ttu-id="ac4ed-192">Kaikki numerot paitsi 0</span><span class="sxs-lookup"><span data-stu-id="ac4ed-192">All numbers except 0</span></span><br /><br /> <span data-ttu-id="ac4ed-193">SQL Server -vaihtoehto sallii tämän symbolin yhdistämisen yleismerkkihakuun.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-193">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="ac4ed-194">Esimerkiksi: <>A\* - ei teksti, joka alkaa kirjaimella A.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-194">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  
  
### <a name="-greater-than"></a><span data-ttu-id="ac4ed-195">(>) suurempi kuin</span><span class="sxs-lookup"><span data-stu-id="ac4ed-195">(>) Greater than</span></span>  
  
|<span data-ttu-id="ac4ed-196">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="ac4ed-196">Sample Expression</span></span>|<span data-ttu-id="ac4ed-197">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="ac4ed-197">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="ac4ed-198">>1200</span><span class="sxs-lookup"><span data-stu-id="ac4ed-198">>1200</span></span>|<span data-ttu-id="ac4ed-199">Numerot, jotka ovat suurempia kuin 1200</span><span class="sxs-lookup"><span data-stu-id="ac4ed-199">Numbers greater than 1200</span></span>|  
  
### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="ac4ed-200">(>=) Suurempi tai yhtä suuri</span><span class="sxs-lookup"><span data-stu-id="ac4ed-200">(>=) Greater than or equal to</span></span>  
  
|<span data-ttu-id="ac4ed-201">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="ac4ed-201">Sample Expression</span></span>|<span data-ttu-id="ac4ed-202">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="ac4ed-202">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="ac4ed-203">>=1200</span><span class="sxs-lookup"><span data-stu-id="ac4ed-203">>=1200</span></span>|<span data-ttu-id="ac4ed-204">Numerot, jotka ovat suurempia tai yhtä suuria kuin 1200</span><span class="sxs-lookup"><span data-stu-id="ac4ed-204">Numbers greater than or equal to 1200</span></span>|  
  
### <a name="-less-than"></a><span data-ttu-id="ac4ed-205">(<) pienempi kuin</span><span class="sxs-lookup"><span data-stu-id="ac4ed-205">(<) Less than</span></span>  
  
|<span data-ttu-id="ac4ed-206">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="ac4ed-206">Sample Expression</span></span>|<span data-ttu-id="ac4ed-207">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="ac4ed-207">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="ac4ed-208"><1200</span><span class="sxs-lookup"><span data-stu-id="ac4ed-208"><1200</span></span>|<span data-ttu-id="ac4ed-209">Numerot, jotka ovat pienempiä kuin 1200</span><span class="sxs-lookup"><span data-stu-id="ac4ed-209">Numbers less than 1200</span></span>|  
  
### <a name="-less-than-or-equal-to"></a><span data-ttu-id="ac4ed-210">(<=) Pienempi tai yhtä suuri</span><span class="sxs-lookup"><span data-stu-id="ac4ed-210">(<=) Less than or equal to</span></span>  
  
|<span data-ttu-id="ac4ed-211">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="ac4ed-211">Sample Expression</span></span>|<span data-ttu-id="ac4ed-212">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="ac4ed-212">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="ac4ed-213"><=1200</span><span class="sxs-lookup"><span data-stu-id="ac4ed-213"><=1200</span></span>|<span data-ttu-id="ac4ed-214">Numerot, jotka ovat pienempiä tai yhtä suuria kuin 1200</span><span class="sxs-lookup"><span data-stu-id="ac4ed-214">Numbers less than or equal to 1200</span></span>|  
  
### <a name="-and"></a><span data-ttu-id="ac4ed-215">(&) ja</span><span class="sxs-lookup"><span data-stu-id="ac4ed-215">(&) And</span></span>  
  
|<span data-ttu-id="ac4ed-216">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="ac4ed-216">Sample Expression</span></span>|<span data-ttu-id="ac4ed-217">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="ac4ed-217">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="ac4ed-218">>200&<1200</span><span class="sxs-lookup"><span data-stu-id="ac4ed-218">>200&<1200</span></span>|<span data-ttu-id="ac4ed-219">Luvut, jotka ovat suurempia kuin 200 ja pienempiä kuin 1200.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-219">Numbers greater than 200 and less than 1200</span></span>|  
  
### <a name="-an-exact-character-match"></a><span data-ttu-id="ac4ed-220">('') Tarkka merkin vastine</span><span class="sxs-lookup"><span data-stu-id="ac4ed-220">('') An exact character match</span></span>  
  
|<span data-ttu-id="ac4ed-221">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="ac4ed-221">Sample Expression</span></span>|<span data-ttu-id="ac4ed-222">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="ac4ed-222">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="ac4ed-223">'man'</span><span class="sxs-lookup"><span data-stu-id="ac4ed-223">'man'</span></span>|<span data-ttu-id="ac4ed-224">Teksti, joka vastaa täysin "man"ia ja jossa isoilla ja pienillä kirjaimilla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-224">Text that matches man exactly and is case sensitive.</span></span>|  
  
### <a name="-case-insensitive"></a><span data-ttu-id="ac4ed-225">(@) Ei kirjainkokoon perustuva</span><span class="sxs-lookup"><span data-stu-id="ac4ed-225">(@) Case insensitive</span></span>  
  
|<span data-ttu-id="ac4ed-226">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="ac4ed-226">Sample Expression</span></span>|<span data-ttu-id="ac4ed-227">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="ac4ed-227">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="ac4ed-228">@man\*</span><span class="sxs-lookup"><span data-stu-id="ac4ed-228">@man\*</span></span>|<span data-ttu-id="ac4ed-229">Teksti, joka alkaa "man" ja jossa isoilla ja pienillä kirjaimilla ei ole merkitystä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-229">Text that starts with man and is case insensitive.</span></span>|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="ac4ed-230">(\*) Rajoittamaton määrä tuntemattomia merkkejä</span><span class="sxs-lookup"><span data-stu-id="ac4ed-230">(\*) An indefinite number of unknown characters</span></span>  
  
|<span data-ttu-id="ac4ed-231">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="ac4ed-231">Sample Expression</span></span>|<span data-ttu-id="ac4ed-232">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="ac4ed-232">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="ac4ed-233">*Co*</span><span class="sxs-lookup"><span data-stu-id="ac4ed-233">*Co*</span></span>|<span data-ttu-id="ac4ed-234">Teksti, joka sisältyy ”Co” ja jossa kirjainkoolla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-234">Text that contains "Co" and is case sensitive.</span></span>|  
|<span data-ttu-id="ac4ed-235">\*Oy</span><span class="sxs-lookup"><span data-stu-id="ac4ed-235">\*Co</span></span>|<span data-ttu-id="ac4ed-236">Teksti, jonka lopussa on ”Co” ja jossa kirjainkoolla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-236">Text that ends with "Co" and is case sensitive.</span></span>|  
|<span data-ttu-id="ac4ed-237">Oy\*</span><span class="sxs-lookup"><span data-stu-id="ac4ed-237">Co\*</span></span>|<span data-ttu-id="ac4ed-238">Teksti, jonka alussa on ”Co” ja jossa kirjainkoolla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-238">Text that begins with "Co" and is case sensitive.</span></span>|  
  
### <a name="-one-unknown-character"></a><span data-ttu-id="ac4ed-239">(?) yksi tuntematon merkki</span><span class="sxs-lookup"><span data-stu-id="ac4ed-239">(?) One unknown character</span></span>  
  
|<span data-ttu-id="ac4ed-240">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="ac4ed-240">Sample Expression</span></span>|<span data-ttu-id="ac4ed-241">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="ac4ed-241">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="ac4ed-242">Hans?n</span><span class="sxs-lookup"><span data-stu-id="ac4ed-242">Hans?n</span></span>|<span data-ttu-id="ac4ed-243">Teksti, kuten Hansen tai Hanson</span><span class="sxs-lookup"><span data-stu-id="ac4ed-243">Text such as Hansen or Hanson</span></span>|  
  
### <a name="combined-format-expressions"></a><span data-ttu-id="ac4ed-244">Yhdistetyn muodon lausekkeet</span><span class="sxs-lookup"><span data-stu-id="ac4ed-244">Combined format expressions</span></span>  
  
|<span data-ttu-id="ac4ed-245">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="ac4ed-245">Sample Expression</span></span>|<span data-ttu-id="ac4ed-246">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="ac4ed-246">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="ac4ed-247">5999&#124;8100..8490</span><span class="sxs-lookup"><span data-stu-id="ac4ed-247">5999&#124;8100..8490</span></span>|<span data-ttu-id="ac4ed-248">Sisällytä kaikki tietueet, joissa on numero 5999 tai numero väliltä 8100 ja 8490.</span><span class="sxs-lookup"><span data-stu-id="ac4ed-248">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|<span data-ttu-id="ac4ed-249">..1299&#124;1400..</span><span class="sxs-lookup"><span data-stu-id="ac4ed-249">..1299&#124;1400..</span></span>|<span data-ttu-id="ac4ed-250">Sisällytä tietueet, joissa on numero, joka on pienempi tai yhtä suuri kuin 1299 tai suurempi tai yhtä suuri kuin 1400 (siis kaikki muut numerot paitsi 1300–1399).</span><span class="sxs-lookup"><span data-stu-id="ac4ed-250">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|<span data-ttu-id="ac4ed-251">>50&<100</span><span class="sxs-lookup"><span data-stu-id="ac4ed-251">>50&<100</span></span>|<span data-ttu-id="ac4ed-252">Sisällytä tietueet, joissa on numero, joka on suurempi kuin 50 ja pienempi kuin 100 (siis numerot 51–99).</span><span class="sxs-lookup"><span data-stu-id="ac4ed-252">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  
 
## <a name="see-also"></a><span data-ttu-id="ac4ed-253">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ac4ed-253">See Also</span></span>
<span data-ttu-id="ac4ed-254">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ac4ed-254">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

