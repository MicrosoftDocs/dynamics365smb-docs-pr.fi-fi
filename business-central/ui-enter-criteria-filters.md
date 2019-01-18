---
title: "Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen | Microsoft Docs"
description: "Voit tehostaa luetteloiden käsittelemistä hakemalla tietoja, lajittelemalla sarakkeita ja tarkentamalla tuloksia tehokkaiden suodatussymboleiden ja pikanäppäinten avulla."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: f0cdb045d314a630e795ec744f2f4470d930835a
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="sorting-searching-and-filtering-lists"></a><span data-ttu-id="f4a15-103">Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen</span><span class="sxs-lookup"><span data-stu-id="f4a15-103">Sorting, Searching, and Filtering Lists</span></span>
<span data-ttu-id="f4a15-104">Luettelossa olevien tietueiden skannaamista, etsimistä ja rajaamista voi helpottaa muutamilla keinoilla.</span><span class="sxs-lookup"><span data-stu-id="f4a15-104">There are a few things that you can do that will help you scan, find, and limit records in a list.</span></span> <span data-ttu-id="f4a15-105">Näitä keinoja ovat esimerkiksi lajitteleminen, etsiminen ja suodattaminen.</span><span class="sxs-lookup"><span data-stu-id="f4a15-105">These include sorting, searching and filtering.</span></span> <span data-ttu-id="f4a15-106">Voit käyttää samanaikaisesti joitakin keinoja tai kaikkia keinoja, kun haluat etsiä tai analysoida tiedot nopeasti.</span><span class="sxs-lookup"><span data-stu-id="f4a15-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

> [!TIP]
> <span data-ttu-id="f4a15-107">Kun tarkastelet tietoja ruutuina, voit hakea tietoja ja käyttää perussuodatusta.</span><span class="sxs-lookup"><span data-stu-id="f4a15-107">When viewing your data as tiles, you can search and use basic filtering.</span></span> <span data-ttu-id="f4a15-108">Jos haluat käyttää lajittelun, haun ja suodattamisen tehokkaita toimintoja, valitse ![Näytä luettelona](media/ui_show_as_list_icon.png "Näytä luettelona - vasen nuoli") -kuvake, jolloin ne näytetään luettelona.</span><span class="sxs-lookup"><span data-stu-id="f4a15-108">To use the full set of powerful features for sorting, searching and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to show as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="f4a15-109">Lajittelu</span><span class="sxs-lookup"><span data-stu-id="f4a15-109">Sorting</span></span>
<span data-ttu-id="f4a15-110">Lajittelun avulla tiedoista saa nopeasti ja kätevästi yleiskuvan.</span><span class="sxs-lookup"><span data-stu-id="f4a15-110">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="f4a15-111">Jos asiakkaita on useita, saat tarvitsemasi yleiskuvan lajittelemalla heidät esimerkiksi **Asiakasnro**-, **Asiakkaan kirjausryhmä**-, **Valuuttakoodi**-, **Maa-/aluekoodi**- tai **ALV-rekisteröintinro**-kohdan avulla,</span><span class="sxs-lookup"><span data-stu-id="f4a15-111">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="f4a15-112">Voit lajitella luettelon joko valitsemalla sarakkeen otsikkotekstin ja vaihtelemalla nousevaa ja laskevaa lajittelua tai valitsemalla sarakeotsikossa olevilla pienillä nuolilla **Nouseva**- tai **Laskeva** -vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="f4a15-112">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small down arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="f4a15-113">Lajittelua ei tueta kuvissa, BLOB-kentissä ja FlowFilter-suodattimissa, jotka eivät kuulu taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="f4a15-113">Sorting is not supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="f4a15-114">Hakeminen</span><span class="sxs-lookup"><span data-stu-id="f4a15-114">Searching</span></span>
<span data-ttu-id="f4a15-115"><!--## Searching by using the Quick Filter --> Kunkin luettelosivun yläosassa on ![Hakuluettelo](media/ui-search/search-list.png "Hakuluettelo-kuvake") **Haku**-kuvake, jonka avulla luettelon tietueiden määrää on helppo vähentää. Näin näkyvissä ovat vain tietueet, jotka sisältävät käyttäjää kiinnostavia tietoja.</span><span class="sxs-lookup"><span data-stu-id="f4a15-115"><!--## Searching by using the Quick Filter --> At the top of each list page, there is a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** icon that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you are interested in seeing.</span></span>

<span data-ttu-id="f4a15-116">Voit aloittaa haun yksinkertaisesti valitsemalla hakukuvakkeen ja kirjoittamalla ruutuun teksti, jota haetaan.</span><span class="sxs-lookup"><span data-stu-id="f4a15-116">To search, simply select the search icon, and then in the box, type the text that you are looking for.</span></span> <span data-ttu-id="f4a15-117">Voit syöttää kirjaimia, numeroita ja muita symboleita.</span><span class="sxs-lookup"><span data-stu-id="f4a15-117">You can enter letters, numbers, and other symbols.</span></span>

### <a name="fine-tune-the-search"></a><span data-ttu-id="f4a15-118">Haun viimeisteleminen</span><span class="sxs-lookup"><span data-stu-id="f4a15-118">Fine-tune the search</span></span>
<span data-ttu-id="f4a15-119">Yleensä haussa yritetään hakea vastaavuuksia kaikista kentistä. Haussa ei erotella pieniä ja isoja kirjaimia (eli kirjainkoolla ei ole merkitystä) ja haussa otetaan huomioon kentän kaikissa kohdissa (alussa, lopussa tai keskellä) oleva teksti.</span><span class="sxs-lookup"><span data-stu-id="f4a15-119">In general, search will attempt to match text across all fields; it does not distinguish between uppercase and lowercase characters (in other words, case insensitive), and will match text placed anwhere in the field (at the beginning, end, or in the middle).</span></span>

<span data-ttu-id="f4a15-120">Voit kuitenkin tehdä tarkemman haun seuraavien erikoismerkkien avulla:</span><span class="sxs-lookup"><span data-stu-id="f4a15-120">However, you can make a more exact search by using the following special characters:</span></span>

- <span data-ttu-id="f4a15-121">Jos haluat etsiä vain ne kenttien arvot, jotka vastaavat koko tekstiä ja kirjainkokoa, aseta haettava teksti yksinkertaisten lainausmerkkien sisään (`''`, esimerkiksi `'man'`).</span><span class="sxs-lookup"><span data-stu-id="f4a15-121">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="f4a15-122">Jos haluat etsiä arvoja, joiden alussa on tietty teksti ja jotka vastaavat tiettyä kirjainkokoa, aseta `*`-merkki hakutekstin jälkeen (esimerkiksi `man*`).</span><span class="sxs-lookup"><span data-stu-id="f4a15-122">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="f4a15-123">Jos haluat etsiä arvoja, joiden lopussa on tietty teksti, ja jotka vastaavat tiettyä kirjainkokoa, aseta `*`-merkki hakutekstin eteen (esimerkiksi `*man`).</span><span class="sxs-lookup"><span data-stu-id="f4a15-123">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="f4a15-124">Kun käytössä on `''` tai `*`, kirjainkoolla ei ole merkitystä haussa.</span><span class="sxs-lookup"><span data-stu-id="f4a15-124">When using  `''` or `*`, the search is case sensitive.</span></span> <span data-ttu-id="f4a15-125">Jos haluat, että kirjainkoolla ei ole merkitystä haussa, aseta `@`-merkki ennen hakutekstiä (esimerkiksi `@man*`).</span><span class="sxs-lookup"><span data-stu-id="f4a15-125">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="f4a15-126">Seuraavassa taulukossa on esimerkkejä haun käyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-126">The following table provides some examples to explain how you can use the search.</span></span>


<!--
In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.-->

<!--
The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options. Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.  

* If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.  
* If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.
-->
<!--

|Search Criteria|Interpreted as...|Finds...|
|---------------|----------------|----------|
|`man`<br />or <br />`Man`|Contains the text; case insensitive|All records with fields that contain the text **man**, regardless of the case.|
|`'Man'`|Entire text match; case sensitive.|All records with fields that only contain **Man** exactly.|
|`Man*`|Starts with the text; case sensitive.|All records with fields that start with the text <b>Man</b> exactly.|
|`@Man*`|Starts with the text; case insensitive.|All records with fields that start with **man**, regardless of the case.|
|`@*man`|Ends with the text; case insensitive.|All records that end with **man**, regardless of the case.|
-->

|<span data-ttu-id="f4a15-127">Hakuehdot</span><span class="sxs-lookup"><span data-stu-id="f4a15-127">Search Criteria</span></span>|<span data-ttu-id="f4a15-128">Etsii...</span><span class="sxs-lookup"><span data-stu-id="f4a15-128">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="f4a15-129">tai</span><span class="sxs-lookup"><span data-stu-id="f4a15-129">or</span></span> <br />`Man`|<span data-ttu-id="f4a15-130">Kaikki tietueet, joissa on **man**-tekstin sisältäviä kenttiä kirjankoosta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="f4a15-130">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="f4a15-131">Esimerkiksi **Manchester**, **manual** tai **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="f4a15-131">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="f4a15-132">Kaikki tietueet, joissa on vain **Man**-tekstin sisältäviä kenttiä. Kirjainkoko on merkitsevä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-132">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="f4a15-133">Kaikki tietueet, joissa on <b>Man</b>-tekstillä alkavia kenttiä. Kirjainkoko on merkitsevä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-133">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="f4a15-134">Esimerkiksi **Manchester**, mutta ei **manual** tai **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="f4a15-134">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="f4a15-135">Kaikki tietueet, joissa on **man**-tekstillä alkavia kenttiä kirjainkoosta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="f4a15-135">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="f4a15-136">Esimerkiksi **Manchester** ja **manual**, mutta ei **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="f4a15-136">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="f4a15-137">Kaikki tietueet, joissa on **man**-tekstiin päättyviä kenttiä kirjainkoosta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="f4a15-137">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="f4a15-138">Esimerkiksi **Sportsman**, mutta ei **Manchester** tai **manual**.</span><span class="sxs-lookup"><span data-stu-id="f4a15-138">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|

> [!TIP]
> <span data-ttu-id="f4a15-139">Voit aktivoida hakuruudun ja poistaa aktivoinnin painamalla F3-näppäintä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-139">You can press F3 to activate and deactivate the search box.</span></span> <span data-ttu-id="f4a15-140">Lisätietoja on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="f4a15-140">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

## <a name="filtering"></a><span data-ttu-id="f4a15-141">Suodattaminen</span><span class="sxs-lookup"><span data-stu-id="f4a15-141">Filtering</span></span>
<span data-ttu-id="f4a15-142">Suodattaminen sisältää kehittyneitä ja monipuolisia toimintoja, joiden avulla määritetään luettelossa näkyvät tietueet.</span><span class="sxs-lookup"><span data-stu-id="f4a15-142">Filtering provides a more advanced and versatile way of controlling which records display in a list.</span></span> <span data-ttu-id="f4a15-143">Hakemisella ja suodattamisella on kaksi pääeroa, jotka kerrotaan alla olevassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="f4a15-143">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="f4a15-144">**Hakeminen**</span><span class="sxs-lookup"><span data-stu-id="f4a15-144">**Searching**</span></span> | <span data-ttu-id="f4a15-145">**Suodattaminen**</span><span class="sxs-lookup"><span data-stu-id="f4a15-145">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="f4a15-146">**Käytettävissä olevat kentät**</span><span class="sxs-lookup"><span data-stu-id="f4a15-146">**Applicable fields**</span></span> | <span data-ttu-id="f4a15-147">Hakee kaikista sivulla näkyvistä kentistä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-147">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="f4a15-148">Suodattaa taulukon minkä tahansa kentän tai useita kenttiä mukaan lukien kentät, jotka eivät näy sivulla.</span><span class="sxs-lookup"><span data-stu-id="f4a15-148">Filters one or more fields individually, selecting from any field on the table, including fields that are not visible on the page.</span></span> |
| <span data-ttu-id="f4a15-149">**Kohdistus**</span><span class="sxs-lookup"><span data-stu-id="f4a15-149">**Matching**</span></span> | <span data-ttu-id="f4a15-150">Näyttää tietueet, joiden kentät vastaavat hakutekstiä tekstin kirjainkoosta tai sijoittelusta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="f4a15-150">Displays records with fields that match the search text, irrespective of casing or placement of that text.</span></span> | <span data-ttu-id="f4a15-151">Näyttää tietueet, joiden kentät vastaavat suodatinta täysin. Kirjainkoko on merkitsevä, jos erityisiä suodatussymboleita ei ole annettu.</span><span class="sxs-lookup"><span data-stu-id="f4a15-151">Displays records where the field matches the filter exactly and is case sensitive, unless special filter symbols are entered.</span></span>

<span data-ttu-id="f4a15-152">Suodattaminen mahdollistaa tiettyjen tilien tai asiakkaiden, päivämäärien, summien ja muiden tietojen tietueiden näyttämisen suodatusehtojen määrittämisen avulla.</span><span class="sxs-lookup"><span data-stu-id="f4a15-152">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="f4a15-153">Näyttöön tulevat tällöin vain ne tietueet, jotka vastaavat määritettyjä ehtoja.</span><span class="sxs-lookup"><span data-stu-id="f4a15-153">Only records that match the criteria are displayed.</span></span> <span data-ttu-id="f4a15-154">Jos määrität ehtoja usealle kentälle, vain kaikkia ehtoja vastaavat tietueet näytetään.</span><span class="sxs-lookup"><span data-stu-id="f4a15-154">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

### <a name="working-in-the-filter-pane"></a><span data-ttu-id="f4a15-155">Suodatinruudun käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="f4a15-155">Working in the filter pane</span></span>
<span data-ttu-id="f4a15-156">Suodatinruudussa näkyvät luettelon nykyiset suodattimet. Sen avulla voi määrittää omia suodattimia yhdelle tai usealle kentälle.</span><span class="sxs-lookup"><span data-stu-id="f4a15-156">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields.</span></span> <span data-ttu-id="f4a15-157">Seuraavassa kuvassa on esimerkki myyntitarjousluettelon suodatinruudusta.</span><span class="sxs-lookup"><span data-stu-id="f4a15-157">The following figure shows an example filter pane for a Sales Quotes list.</span></span>

<span data-ttu-id="f4a15-158">![Suodatinruudun yleiskatsaus ](media/filter-pane-overview.png "Suodatin-kuvake")</span><span class="sxs-lookup"><span data-stu-id="f4a15-158">![Filter pane overview ](media/filter-pane-overview.png "Filter icon")</span></span>

<span data-ttu-id="f4a15-159">Jos haluat näyttää suodatinruudun, käytä **Vaihto+F3**-pikanäppäimiä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-159">To display the filter pane, use the **Shift+F3** keyboard shortcut.</span></span> <span data-ttu-id="f4a15-160">Voit valita roolikeskuksen luetteloissa sivun otsikon lähellä olevan alanuolen luettelon yläpuolella olevassa siirtymispalkissa ja valita sitten **Näytä suodatinruutu**.</span><span class="sxs-lookup"><span data-stu-id="f4a15-160">For lists within the Role Center, you can also choose the down arrow near the page title in the navigation bar above the list, and then choose **Show filter pane**.</span></span>

<span data-ttu-id="f4a15-161">![Näytä suodatinruutu](media/open-filter-pane.png "Näytä suodatinruutu")</span><span class="sxs-lookup"><span data-stu-id="f4a15-161">![Show filter pane](media/open-filter-pane.png "Show filter pane")</span></span>

<span data-ttu-id="f4a15-162">Suodatinruutu on jaettu kolmeen osaan: **Näkymät**, **Luettelon suodatusperuste** ja **Kokonaisarvojen suodatusperuste**:</span><span class="sxs-lookup"><span data-stu-id="f4a15-162">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="f4a15-163">**Näkymät**</span><span class="sxs-lookup"><span data-stu-id="f4a15-163">**Views**</span></span>

  <span data-ttu-id="f4a15-164">Joissakin luetteloissa on **Näkymät**-osa.</span><span class="sxs-lookup"><span data-stu-id="f4a15-164">Some lists will include the **Views** section.</span></span> <span data-ttu-id="f4a15-165">Näkymät ovat luettelon muunnoksia, jotka on esimääritetty suodattimien kanssa.</span><span class="sxs-lookup"><span data-stu-id="f4a15-165">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="f4a15-166">Voit vaihtaa luettelon toiseen näkymään yksinkertaisesti valitsemalla toisen linkin.</span><span class="sxs-lookup"><span data-stu-id="f4a15-166">To switch to a different view of your list, simply select another link.</span></span> <span data-ttu-id="f4a15-167">Voit muuttaa näkymän suodattimia väliaikaisesti, mutta muutoksia ei tallenneta pysyvästi.</span><span class="sxs-lookup"><span data-stu-id="f4a15-167">You can temporarily change the filters on a view, but the changes will not be permanently saved.</span></span>

- <span data-ttu-id="f4a15-168">**Luettelon suodatusperuste**</span><span class="sxs-lookup"><span data-stu-id="f4a15-168">**Filter list by**</span></span>

  <span data-ttu-id="f4a15-169">**Luettelon suodatusperuste** -osassa lisätään suodattimet tietyille kentille ja vähennetään näin näytettävien tietueiden määrää.</span><span class="sxs-lookup"><span data-stu-id="f4a15-169">The **Filter list by** section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="f4a15-170">Voit lisätä suodattimen valitsemalla **+ suodatin**, valitsemalla sitten haluamasi suodattimen mistä tahansa taulukon kentästä ja syöttämällä suodatusehdot ruutuun.</span><span class="sxs-lookup"><span data-stu-id="f4a15-170">To add a filter, select **+ Filter**, select the field that you want to filter from any field in the table, and then enter filter criteria in the box.</span></span>

- <span data-ttu-id="f4a15-171">**Kokonaisarvojen suodatusperuste**</span><span class="sxs-lookup"><span data-stu-id="f4a15-171">**Filter totals by**</span></span>

  <span data-ttu-id="f4a15-172">Jotkin laskettuja kenttiä, kuten summia ja määriä, näyttävät luettelot sisältävät **Kokonaisarvojen suodatusperuste** -osan. Siinä voi muokata erilaisia laskelmiin vaikuttavia dimensioita.</span><span class="sxs-lookup"><span data-stu-id="f4a15-172">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="f4a15-173">Voit esimerkiksi nopeasti analysoida tilikarttoja suodattamalla tietyn kauden summat tai tarkastella tietyn varaston myyntitilausten kokonaissummia.</span><span class="sxs-lookup"><span data-stu-id="f4a15-173">For example, you can quickly analyze your chart of accounts by filtering amounts to a specific period, or you can view the totals for sales orders only from a specific warehouse.</span></span>

  <span data-ttu-id="f4a15-174">Voit lisätä suodattimen valitsemalla **+ suodatin** valitsemalla esimääritetyt dimensiot ja lisäämällä suodatusehdot ruutuun.</span><span class="sxs-lookup"><span data-stu-id="f4a15-174">To add a filter, select **+ Filter**, select one of the predefined dimensions, and then add the filter criteria in the box.</span></span>

  > [!NOTE]
  > <span data-ttu-id="f4a15-175">FlowFilter-suodattimet ohjaavat **Kokonaisarvojen suodatusperuste** -osan suodattimia sivun rakenteessa.</span><span class="sxs-lookup"><span data-stu-id="f4a15-175">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="f4a15-176">Teknisiä lisätietoja on kohdassa [FlowFilter-suodattimet](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="f4a15-176">For technical information, see [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>


### <a name="entering-filter-criteria-in-the-filter-pane"></a><span data-ttu-id="f4a15-177">Suodatusehtojen syöttäminen suodatinruutuun</span><span class="sxs-lookup"><span data-stu-id="f4a15-177">Entering filter criteria in the filter pane</span></span>
<span data-ttu-id="f4a15-178">Jos haluat valita suodatettavan kentän, tee jokin seuraavista toiminnoista:</span><span class="sxs-lookup"><span data-stu-id="f4a15-178">To select a field to filter, do one of the following:</span></span>
  - <span data-ttu-id="f4a15-179">Valitse suodatinruudussa **+ kenttä**.</span><span class="sxs-lookup"><span data-stu-id="f4a15-179">In the filter pane, choose **+ Field**.</span></span> <span data-ttu-id="f4a15-180">Kirjoita suodatettavan kentän nimi tai valitse kenttä valikosta, jossa ovat kaikki taulukon kentät.</span><span class="sxs-lookup"><span data-stu-id="f4a15-180">Type the name of the field you wish to filter, or pick a field from the menu that displays all fields in the table.</span></span>

  - <span data-ttu-id="f4a15-181">Valitse sarakeotsikossa alanuoli ja valitse sitten **Suodata...**. Näyttöön avautuu suodatinruutu, johon lisätään sarake.</span><span class="sxs-lookup"><span data-stu-id="f4a15-181">In a column heading, choose the down arrow, and then choose **Filter...**. This will open the filter pane and add the column to the filter pane.</span></span>

<span data-ttu-id="f4a15-182">Nyt voit kirjoittaa tai valita suodatusehdot ruutuun.</span><span class="sxs-lookup"><span data-stu-id="f4a15-182">You can now type or select your filter criteria in the box.</span></span> <span data-ttu-id="f4a15-183">Suodatettavan kentän tyyppi määrittää, millaisia ehtoja voi syöttää.</span><span class="sxs-lookup"><span data-stu-id="f4a15-183">The type of field you filter determines which criteria you can enter.</span></span> <span data-ttu-id="f4a15-184">Jos esimerkiksi suodatetaan kenttä, jossa on kiinteitä arvoja, valittavissa on vain nämä arvot.</span><span class="sxs-lookup"><span data-stu-id="f4a15-184">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="f4a15-185">Lisätietoja erityisistä suodatussymboleista on kohdissa [Suodatusehdot](#FilterCriteria) ja [Suodatuksen tunnukset](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="f4a15-185">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="f4a15-186">Sarakkeet, joilla on jo suodattimia, löytyvät, kun käytössä on sarakeotsikon ![Suodatus-kuvake](media/ui-search/filter-icon.png "Suodatus-kuvake").</span><span class="sxs-lookup"><span data-stu-id="f4a15-186">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") in the column heading.</span></span> <span data-ttu-id="f4a15-187">Voit poistaa suodattimen valitsemalla sarakeotsikon ja valitsemalla sitten **Tyhjennä suodatin**.</span><span class="sxs-lookup"><span data-stu-id="f4a15-187">To remove a filter, select the column heading, then choose **Clear Filter**.</span></span>


### <a name="entering-filter-criteria-without-the-filter-pane"></a><span data-ttu-id="f4a15-188">Suodatusehtojen syöttäminen ilman suodatinruutua</span><span class="sxs-lookup"><span data-stu-id="f4a15-188">Entering filter criteria without the filter pane</span></span>
<span data-ttu-id="f4a15-189">Voit määrittää yksinkertaisia suodattimia suoraan luettelosta ilman suodatinruutua.</span><span class="sxs-lookup"><span data-stu-id="f4a15-189">You can specify simple filters directly within the list without having to use the filter pane.</span></span>
<span data-ttu-id="f4a15-190">Kun rivillä on valittu mikä tahansa kenttä, voit näyttää vain saman arvon sisältävät tietueet valitsemalla **Alt+F3**-pikanäppäimet.</span><span class="sxs-lookup"><span data-stu-id="f4a15-190">With any field selected on a row, use the **Alt+F3** keyboard shortcut to display only the records having that same value.</span></span> <span data-ttu-id="f4a15-191">Tämän jälkeen voit valita toisen kentän ja käyttää samoja pikanäppäimiä, kun haluat jatkaa suodattimien tarkentamista.</span><span class="sxs-lookup"><span data-stu-id="f4a15-191">You can then select another field and use the same shortcut again to continue refining your filters.</span></span> <span data-ttu-id="f4a15-192">Jos valittu kenttä on jo suodatettu, **Alt+F3** tyhjentää kyseisen suodattimen.</span><span class="sxs-lookup"><span data-stu-id="f4a15-192">If the selected field is already filtered, using **Alt+F3** will clear that filter.</span></span>

> [!TIP]
> <span data-ttu-id="f4a15-193">Nopeuta tietojen etsimistä ja analysoimista pikanäppäinyhdistelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="f4a15-193">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="f4a15-194">Voit esimerkiksi valita kentän ja lisätä kentän suodatinruutuun **Vaihto+Alt+F3**-pikanäppäinten avulla, kirjoittaa suodatinehdot ja palata riveille **Ctrl+Enter**-pikanäppäinten avulla. Valitse toinen kenttä ja suodata sen arvot **Alt+F3**-pikanäppäimillä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-194">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span>
<span data-ttu-id="f4a15-195">Lisätietoja on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="f4a15-195">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>


## <span data-ttu-id="f4a15-196"><a name="FilterCriteria"> </a>Suodatusehdot ja merkit</span><span class="sxs-lookup"><span data-stu-id="f4a15-196"><a name="FilterCriteria"> </a>Filter criteria and symbols</span></span>
<span data-ttu-id="f4a15-197">Kun syötät kriteerejä, voit käyttää kaikkia numeroita ja kirjaimia, joita voi yleensäkin käyttää kentässä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-197">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="f4a15-198">Voit käyttää tulosten suodatukseen myös erikoismerkkejä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-198">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="f4a15-199">Seuraavassa taulukossa on esitelty symbolit, joita voi käyttää suodattimissa.</span><span class="sxs-lookup"><span data-stu-id="f4a15-199">The following tables show the symbols which can be used in filters.</span></span> <span data-ttu-id="f4a15-200">Lisätietoja päivämääristä ja ajoista on myös kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="f4a15-200">For dates and times, you can also refer to [Working with Calendar Dates and Times](ui-enter-date-ranges.md) for more detailed information.</span></span>

> [!IMPORTANT]  
>  <span data-ttu-id="f4a15-201">Joissakin tilanteissa kentät arvot voivat sisältää näitä merkkejä, ja haluat suodattaa niiden avulla.</span><span class="sxs-lookup"><span data-stu-id="f4a15-201">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="f4a15-202">Siinä tapauksessa on merkki on lisättävä suodatuslausekkeeseen lainausmerkeissä (”).</span><span class="sxs-lookup"><span data-stu-id="f4a15-202">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="f4a15-203">Jos haluat esimerkiksi suodattaa tietueita, joiden alussa on teksti *S&R*, suodatuslauseke on `'S&R*'`.</span><span class="sxs-lookup"><span data-stu-id="f4a15-203">For example, if you want to filter on records that start with the text *S&R*, the filter expression is `'S&R*'`.</span></span>  

### <a name="-interval"></a><span data-ttu-id="f4a15-204">(..) väli</span><span class="sxs-lookup"><span data-stu-id="f4a15-204">(..) Interval</span></span>

|<span data-ttu-id="f4a15-205">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-205">Sample Expression</span></span>|<span data-ttu-id="f4a15-206">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-206">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="f4a15-207">Numerot 1100 - 2100</span><span class="sxs-lookup"><span data-stu-id="f4a15-207">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="f4a15-208">Numeroon 2500 asti, 2500 mukaan lukien</span><span class="sxs-lookup"><span data-stu-id="f4a15-208">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="f4a15-209">Päivämäärät 31.12.00 asti, kyseinen päivämäärä mukaan lukien</span><span class="sxs-lookup"><span data-stu-id="f4a15-209">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="f4a15-210">Tiedot kirjanpitojaksosta 8 ja siitä eteenpäin</span><span class="sxs-lookup"><span data-stu-id="f4a15-210">Information for accounting period 8 and thereafter</span></span>|  
|`..23`|<span data-ttu-id="f4a15-211">Alkupäivämäärästä lähtien päivään 23 nykyistä kuukautta nykyistä vuotta klo 23:59:59</span><span class="sxs-lookup"><span data-stu-id="f4a15-211">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="f4a15-212">Päivästä 23 nykyistä kuukautta nykyistä vuotta klo 00:00:00 ajan loppuun asti</span><span class="sxs-lookup"><span data-stu-id="f4a15-212">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="f4a15-213">Päivästä 22 nykyistä kuukautta nykyistä vuotta klo 0:00:00 päivään 23 nykyistä kuukautta nykyistä vuotta klo 23:59:59</span><span class="sxs-lookup"><span data-stu-id="f4a15-213">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

### <a name="124-eitheror"></a><span data-ttu-id="f4a15-214">(&#124;) joko/tai</span><span class="sxs-lookup"><span data-stu-id="f4a15-214">(&#124;) Either/or</span></span>  

|<span data-ttu-id="f4a15-215">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-215">Sample Expression</span></span>|<span data-ttu-id="f4a15-216">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-216">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="f4a15-217">\`1200</span><span class="sxs-lookup"><span data-stu-id="f4a15-217">\`1200</span></span>|<span data-ttu-id="f4a15-218">1300\`</span><span class="sxs-lookup"><span data-stu-id="f4a15-218">1300\`</span></span>|<span data-ttu-id="f4a15-219">Numerot, joissa on 1200 tai 1300</span><span class="sxs-lookup"><span data-stu-id="f4a15-219">Numbers with 1200 or 1300</span></span>|  

### <a name="-not-equal-to"></a><span data-ttu-id="f4a15-220">(<>) ei ole sama kuin</span><span class="sxs-lookup"><span data-stu-id="f4a15-220">(<>) Not equal to</span></span>  

|<span data-ttu-id="f4a15-221">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-221">Sample Expression</span></span>|<span data-ttu-id="f4a15-222">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-222">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="f4a15-223">Kaikki numerot paitsi 0</span><span class="sxs-lookup"><span data-stu-id="f4a15-223">All numbers except 0</span></span><br /><br /> <span data-ttu-id="f4a15-224">SQL Server -vaihtoehto sallii tämän symbolin yhdistämisen yleismerkkihakuun.</span><span class="sxs-lookup"><span data-stu-id="f4a15-224">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="f4a15-225">Esimerkiksi: <>A\* - ei teksti, joka alkaa kirjaimella A.</span><span class="sxs-lookup"><span data-stu-id="f4a15-225">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

### <a name="-greater-than"></a><span data-ttu-id="f4a15-226">(>) suurempi kuin</span><span class="sxs-lookup"><span data-stu-id="f4a15-226">(>) Greater than</span></span>  

|<span data-ttu-id="f4a15-227">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-227">Sample Expression</span></span>|<span data-ttu-id="f4a15-228">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-228">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="f4a15-229">Numerot, jotka ovat suurempia kuin 1200</span><span class="sxs-lookup"><span data-stu-id="f4a15-229">Numbers greater than 1200</span></span>|  

### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="f4a15-230">(>=) Suurempi tai yhtä suuri</span><span class="sxs-lookup"><span data-stu-id="f4a15-230">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="f4a15-231">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-231">Sample Expression</span></span>|<span data-ttu-id="f4a15-232">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-232">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="f4a15-233">Numerot, jotka ovat suurempia tai yhtä suuria kuin 1200</span><span class="sxs-lookup"><span data-stu-id="f4a15-233">Numbers greater than or equal to 1200</span></span>|  

### <a name="-less-than"></a><span data-ttu-id="f4a15-234">(<) pienempi kuin</span><span class="sxs-lookup"><span data-stu-id="f4a15-234">(<) Less than</span></span>  

|<span data-ttu-id="f4a15-235">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-235">Sample Expression</span></span>|<span data-ttu-id="f4a15-236">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-236">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="f4a15-237">Numerot, jotka ovat pienempiä kuin 1200</span><span class="sxs-lookup"><span data-stu-id="f4a15-237">Numbers less than 1200</span></span>|  

### <a name="-less-than-or-equal-to"></a><span data-ttu-id="f4a15-238">(<=) Pienempi tai yhtä suuri</span><span class="sxs-lookup"><span data-stu-id="f4a15-238">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="f4a15-239">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-239">Sample Expression</span></span>|<span data-ttu-id="f4a15-240">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-240">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="f4a15-241">Numerot, jotka ovat pienempiä tai yhtä suuria kuin 1200</span><span class="sxs-lookup"><span data-stu-id="f4a15-241">Numbers less than or equal to 1200</span></span>|  

### <a name="-and"></a><span data-ttu-id="f4a15-242">(&) ja</span><span class="sxs-lookup"><span data-stu-id="f4a15-242">(&) And</span></span>  

|<span data-ttu-id="f4a15-243">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-243">Sample Expression</span></span>|<span data-ttu-id="f4a15-244">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-244">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="f4a15-245">Luvut, jotka ovat suurempia kuin 200 ja pienempiä kuin 1200.</span><span class="sxs-lookup"><span data-stu-id="f4a15-245">Numbers greater than 200 and less than 1200</span></span>|  

### <a name="-an-exact-character-match"></a><span data-ttu-id="f4a15-246">('') Tarkka merkin vastine</span><span class="sxs-lookup"><span data-stu-id="f4a15-246">('') An exact character match</span></span>  

|<span data-ttu-id="f4a15-247">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-247">Sample Expression</span></span>|<span data-ttu-id="f4a15-248">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-248">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="f4a15-249">Teksti, joka vastaa täysin "man"ia ja jossa isoilla ja pienillä kirjaimilla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-249">Text that matches man exactly and is case sensitive.</span></span>|  

### <a name="-case-insensitive"></a><span data-ttu-id="f4a15-250">(@) Ei kirjainkokoon perustuva</span><span class="sxs-lookup"><span data-stu-id="f4a15-250">(@) Case insensitive</span></span>  

|<span data-ttu-id="f4a15-251">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-251">Sample Expression</span></span>|<span data-ttu-id="f4a15-252">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-252">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="f4a15-253">Teksti, joka alkaa "man" ja jossa isoilla ja pienillä kirjaimilla ei ole merkitystä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-253">Text that starts with man and is case insensitive.</span></span>|  

### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="f4a15-254">(\*) Rajoittamaton määrä tuntemattomia merkkejä</span><span class="sxs-lookup"><span data-stu-id="f4a15-254">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="f4a15-255">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-255">Sample Expression</span></span>|<span data-ttu-id="f4a15-256">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-256">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="f4a15-257">Teksti, joka sisältyy ”Co” ja jossa kirjainkoolla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-257">Text that contains "Co" and is case sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="f4a15-258">Teksti, jonka lopussa on ”Co” ja jossa kirjainkoolla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-258">Text that ends with "Co" and is case sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="f4a15-259">Teksti, jonka alussa on ”Co” ja jossa kirjainkoolla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-259">Text that begins with "Co" and is case sensitive.</span></span>|  

> [!NOTE]  
>   <span data-ttu-id="f4a15-260">Ei voi käyttää `*`-merkkiä käyttäessäsi suodattamisessa asetuskenttiä (luettelointikenttiä), kuten myyntitilausten **Tila**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="f4a15-260">You cannot use `*` when filtering on option (enumeration) fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="f4a15-261">Voit syöttää suodattimen tämäntyyppiselle kentälle kirjoittamalla numeerisen arvon suodatusparametriksi.</span><span class="sxs-lookup"><span data-stu-id="f4a15-261">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="f4a15-262">Jos esimerkiksi myyntitilauksen **Tila**-kentällä on arvot **Avoin**, **Vapautettu**, **Odottaa hyväksyntää** ja **Odottaa ennakkomaksua**, suodata vaihtoehdot arvojen `0`, `1`, `2` ja `3` avulla.</span><span class="sxs-lookup"><span data-stu-id="f4a15-262">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values `0`, `1`, `2`, and `3` to filter for these options.</span></span>

### <a name="-one-unknown-character"></a><span data-ttu-id="f4a15-263">(?) yksi tuntematon merkki</span><span class="sxs-lookup"><span data-stu-id="f4a15-263">(?) One unknown character</span></span>  

|<span data-ttu-id="f4a15-264">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-264">Sample Expression</span></span>|<span data-ttu-id="f4a15-265">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-265">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="f4a15-266">Teksti, kuten Hansen tai Hanson</span><span class="sxs-lookup"><span data-stu-id="f4a15-266">Text such as Hansen or Hanson</span></span>|  

### <a name="combined-format-expressions"></a><span data-ttu-id="f4a15-267">Yhdistetyn muodon lausekkeet</span><span class="sxs-lookup"><span data-stu-id="f4a15-267">Combined format expressions</span></span>  

|<span data-ttu-id="f4a15-268">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-268">Sample Expression</span></span>|<span data-ttu-id="f4a15-269">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-269">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="f4a15-270">\`5999</span><span class="sxs-lookup"><span data-stu-id="f4a15-270">\`5999</span></span>|<span data-ttu-id="f4a15-271">8100..8490\`</span><span class="sxs-lookup"><span data-stu-id="f4a15-271">8100..8490\`</span></span>|<span data-ttu-id="f4a15-272">Sisällytä kaikki tietueet, joissa on numero 5999 tai numero väliltä 8100 ja 8490.</span><span class="sxs-lookup"><span data-stu-id="f4a15-272">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|<span data-ttu-id="f4a15-273">\`..1299</span><span class="sxs-lookup"><span data-stu-id="f4a15-273">\`..1299</span></span>|<span data-ttu-id="f4a15-274">1400..\`</span><span class="sxs-lookup"><span data-stu-id="f4a15-274">1400..\`</span></span>|<span data-ttu-id="f4a15-275">Sisällytä tietueet, joissa on numero, joka on pienempi tai yhtä suuri kuin 1299 tai suurempi tai yhtä suuri kuin 1400 (siis kaikki muut numerot paitsi 1300–1399).</span><span class="sxs-lookup"><span data-stu-id="f4a15-275">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="f4a15-276">Sisällytä tietueet, joissa on numero, joka on suurempi kuin 50 ja pienempi kuin 100 (siis numerot 51–99).</span><span class="sxs-lookup"><span data-stu-id="f4a15-276">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  


## <span data-ttu-id="f4a15-277"><a name="FilterTokens"> </a>Suodatuksen tunnukset</span><span class="sxs-lookup"><span data-stu-id="f4a15-277"><a name="FilterTokens"> </a>Filter tokens</span></span>
<span data-ttu-id="f4a15-278">Kun syötät suodatusehtoja, voit kirjoittaa myös sanoja, joilla on erityinen tarkoitus. Niitä kutsutaan suodatuksen tunnuksiksi.</span><span class="sxs-lookup"><span data-stu-id="f4a15-278">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="f4a15-279">Kun olet syöttänyt tunnussanan, sana korvataan arvolla tai arvoilla, joita se edustaa.</span><span class="sxs-lookup"><span data-stu-id="f4a15-279">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="f4a15-280">Tämä helpottaa suodattamista ja vähentää muille sivuille siirtymistä ja suodattimeen lisättävien arvojen etsimistä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-280">This makes filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="f4a15-281">Taulukossa on joitakin tunnuksia, joita voit käyttää suodatusehtoina.</span><span class="sxs-lookup"><span data-stu-id="f4a15-281">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="f4a15-282">Organisaatio voi käyttää mukautettuja tunnuksia.</span><span class="sxs-lookup"><span data-stu-id="f4a15-282">Your organization may use custom tokens.</span></span> <span data-ttu-id="f4a15-283">Järjestelmänvalvojalta saa lisätietoja käytettävissä olevista tunnuksista ja mukautettujen tunnusten lisäämisestä.</span><span class="sxs-lookup"><span data-stu-id="f4a15-283">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="f4a15-284">Teknisiä lisätietoja on kohdassa [Suodatuksen tunnusten lisääminen](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)</span><span class="sxs-lookup"><span data-stu-id="f4a15-284">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)</span></span>


### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="f4a15-285">(%me tai %userid) Sinulle liitetyt tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-285">(%me or %userid) Records assigned to you</span></span>

<span data-ttu-id="f4a15-286">Käytä `%me`- tai `%userid`-tunnusta suodattaessasi kenttiä, jotka sisältävät käyttäjätunnuksen. Tällainen kenttä on esimerkiksi **Liitetty käyttäjätunnukseen**, jossa näytetään kaikki käyttäjälle liitetyt kentät.</span><span class="sxs-lookup"><span data-stu-id="f4a15-286">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="f4a15-287">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-287">Sample Expression</span></span>|<span data-ttu-id="f4a15-288">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-288">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="f4a15-289">tai</span><span class="sxs-lookup"><span data-stu-id="f4a15-289">or</span></span><br />`%userid`|<span data-ttu-id="f4a15-290">Tietueet, jotka on liitetty käyttäjätiliisi.</span><span class="sxs-lookup"><span data-stu-id="f4a15-290">Records the are assigned to your user account.</span></span> |  

### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="f4a15-291">(%mycustomers) Omat asiakkaat -kohdan asiakkaat</span><span class="sxs-lookup"><span data-stu-id="f4a15-291">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="f4a15-292">Käytä `%mycustomers`-tunnusta asiakkaan **Nro**-kentässä, kun haluat näyttää asiakkaan kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat asiakkaat** -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="f4a15-292">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="f4a15-293">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-293">Sample Expression</span></span>|<span data-ttu-id="f4a15-294">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-294">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="f4a15-295">Roolikeskuksen **Omat asiakkaat** -kohdan asiakkaat.</span><span class="sxs-lookup"><span data-stu-id="f4a15-295">Customers in the **My Customers** on your Role Center.</span></span> |  

### <a name="myitems-items-in-my-items"></a><span data-ttu-id="f4a15-296">(%myitems) Omat nimikkeet -kohdan nimikkeet</span><span class="sxs-lookup"><span data-stu-id="f4a15-296">(%myitems) Items in My Items</span></span>

<span data-ttu-id="f4a15-297">Käytä `%myitems`-tunnusta nimikkeen **Nro**-kentässä, kun haluat näyttää nimikkeiden kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat nimikkeet** -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="f4a15-297">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="f4a15-298">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-298">Sample Expression</span></span>|<span data-ttu-id="f4a15-299">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-299">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="f4a15-300">Roolikeskuksen **Omat nimikkeet** -kohdan nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="f4a15-300">Items in the **My Items** on your Role Center.</span></span> |  

### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="f4a15-301">(%myvendors) Omat toimittajat -kohdan toimittajat</span><span class="sxs-lookup"><span data-stu-id="f4a15-301">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="f4a15-302">Käytä `%myvendors`-tunnusta toimittajan **Nro**-kentässä, kun haluat näyttää toimittajien kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat toimittajat** -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="f4a15-302">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="f4a15-303">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="f4a15-303">Sample Expression</span></span>|<span data-ttu-id="f4a15-304">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="f4a15-304">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="f4a15-305">Roolikeskuksen **Omat toimittajat** -kohdan toimittajat.</span><span class="sxs-lookup"><span data-stu-id="f4a15-305">Venders in the **My Vendors** on your Role Center.</span></span> |  


## <a name="see-also"></a><span data-ttu-id="f4a15-306">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f4a15-306">See Also</span></span>
<span data-ttu-id="f4a15-307">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f4a15-307">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="f4a15-308">Hakemista ja suodattamista koskevat yleiset kysymykset</span><span class="sxs-lookup"><span data-stu-id="f4a15-308">Common questions about Searching and Filtering</span></span>](ui-search-filter-faq.md)

