---
title: Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen | Microsoft Docs
description: Voit tehostaa luetteloiden käsittelemistä hakemalla tietoja, lajittelemalla sarakkeita ja tarkentamalla tuloksia suodatussymboleiden ja pikanäppäinten avulla.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 11/16/2020
ms.author: jswymer
ms.openlocfilehash: d682f9e66075348785329cd13a12c3e02d0993c4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385847"
---
# <a name="sorting-searching-and-filtering"></a><span data-ttu-id="84fac-103">Lajitteleminen, hakeminen ja suodattaminen</span><span class="sxs-lookup"><span data-stu-id="84fac-103">Sorting, Searching, and Filtering</span></span>

<span data-ttu-id="84fac-104">Luettelossa, raportissa tai XMLportissa olevien tietueiden skannaamista, etsimistä ja rajaamista voi helpottaa muutamilla keinoilla.</span><span class="sxs-lookup"><span data-stu-id="84fac-104">There are a few things that you can do that will help you scan, find, and limit records on a list or in a report or XMLport.</span></span> <span data-ttu-id="84fac-105">Näitä keinoja ovat esimerkiksi lajitteleminen, etsiminen ja suodattaminen.</span><span class="sxs-lookup"><span data-stu-id="84fac-105">These include sorting, searching, and filtering.</span></span> <span data-ttu-id="84fac-106">Voit käyttää samanaikaisesti joitakin keinoja tai kaikkia keinoja, kun haluat etsiä tai analysoida tiedot nopeasti.</span><span class="sxs-lookup"><span data-stu-id="84fac-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

<span data-ttu-id="84fac-107">Raporteissa ja XMLporteissa suodattimet voidaan määrittää luetteloiden tavoin rajoittamaan raporttiin tai XMLportiin sisällytettäviä tietoja, mutta lajittelu ja haku ei ole mahdollista.</span><span class="sxs-lookup"><span data-stu-id="84fac-107">For reports and XMLports, as on lists, you can set filters to delimit which data to include in the report or XMLport, but you can't sort and search.</span></span>

> [!TIP]
> <span data-ttu-id="84fac-108">Kun tarkastelet tietoja ruutuina, voit hakea tietoja ja käyttää suodatusta.</span><span class="sxs-lookup"><span data-stu-id="84fac-108">When viewing your data as tiles, you can search and use filtering.</span></span> <span data-ttu-id="84fac-109">Jos haluat käyttää lajittelun, haun ja suodattamisen tehokkaita toimintoja, valitse ![Näytä luettelona](media/ui_show_as_list_icon.png "Näytä luettelona – nuoli vasemmalle") -kuvake, jolloin tietueita voidaan tarkastella luettelona.</span><span class="sxs-lookup"><span data-stu-id="84fac-109">To use the full set of powerful features for sorting, searching, and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to view the records as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="84fac-110">Lajittelu</span><span class="sxs-lookup"><span data-stu-id="84fac-110">Sorting</span></span>

<span data-ttu-id="84fac-111">Lajittelun avulla tiedoista saa nopeasti ja kätevästi yleiskuvan.</span><span class="sxs-lookup"><span data-stu-id="84fac-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="84fac-112">Jos esimerkiksi asiakkaita on useita, saat tarvitsemasi yleiskuvan lajittelemalla heidät esimerkiksi **Asiakasnro**-, **Valuuttakoodi**- tai **Maa-/aluekoodi** -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="84fac-112">For example, if you have many customers,  you could sort them by **Customer No.**, **Currency Code**, or **Country Region Code** to get the overview you need.</span></span>

<span data-ttu-id="84fac-113">Voit lajitella luettelon seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="84fac-113">To sort a list, you can either:</span></span>

- <span data-ttu-id="84fac-114">Valitse sarakkeen otsikkoteksti, mikä vaihtaa nousevan ja laskevan järjestyksen välillä.</span><span class="sxs-lookup"><span data-stu-id="84fac-114">Choose a column heading text to toggle between ascending and descending order, or</span></span>
- <span data-ttu-id="84fac-115">Valitse sarakeotsikossa avattava nuoli ja valitse **Nouseva** tai **Laskeva**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="84fac-115">Choose the drop-down arrow in the column heading, then choose the **Ascending** or **Descending** action.</span></span>  

> [!NOTE]  
> <span data-ttu-id="84fac-116">Lajittelua ei tueta kuvissa, BLOB-kentissä ja FlowFilter-suodattimissa, jotka eivät kuulu taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="84fac-116">Sorting isn't supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="84fac-117">Hakeminen</span><span class="sxs-lookup"><span data-stu-id="84fac-117">Searching</span></span>

<!--## Searching by using the Quick Filter -->
<span data-ttu-id="84fac-118">Kunkin luettelosivun yläosassa on ![Hakuluettelon](media/ui-search/search-list.png "Hakuluettelon kuvake") **Haku**-toiminto, jonka avulla luettelon tietueiden määrää on helppo vähentää. Näin näkyvissä ovat vain tietueet, jotka sisältävät käyttäjää kiinnostavia tietoja.</span><span class="sxs-lookup"><span data-stu-id="84fac-118">At the top of each list page, there's a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** action that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you're interested in seeing.</span></span>

<span data-ttu-id="84fac-119">Voit aloittaa haun valitsemalla **Haku**-toiminnon ja kirjoittamalla ruutuun tekstin, jota haetaan.</span><span class="sxs-lookup"><span data-stu-id="84fac-119">To search, just choose the **Search** action, and then in the box, type the text that you're looking for.</span></span> <span data-ttu-id="84fac-120">Voit syöttää kirjaimia, numeroita ja muita symboleita.</span><span class="sxs-lookup"><span data-stu-id="84fac-120">You can enter letters, numbers, and other symbols.</span></span>

<span data-ttu-id="84fac-121">Yleensä haussa yritetään hakea vastaavuuksia kaikista kentistä.</span><span class="sxs-lookup"><span data-stu-id="84fac-121">In general, search will attempt to match text across all fields.</span></span> <span data-ttu-id="84fac-122">Haussa ei erotella pieniä ja isoja kirjaimia (eli kirjainkoolla ei ole merkitystä) ja haussa otetaan huomioon kentän kaikissa kohdissa (alussa, lopussa tai keskellä) oleva teksti.</span><span class="sxs-lookup"><span data-stu-id="84fac-122">It doesn't distinguish between uppercase and lowercase characters (case insensitive) and will match text placed anywhere in the field, at the beginning, end, or in the middle.</span></span>

> [!TIP]
> <span data-ttu-id="84fac-123">Voit aktivoida hakuruudun ja poistaa aktivoinnin painamalla **F3**-näppäintä.</span><span class="sxs-lookup"><span data-stu-id="84fac-123">You can press **F3** to activate and deactivate the search box.</span></span> <span data-ttu-id="84fac-124">Lisätietoja on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="84fac-124">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

> [!NOTE]  
> <span data-ttu-id="84fac-125">Hakua ei vastaa kuvien, BLOB-, FlowFilters-, FlowFields- ja muiden taulukon ulkopuolisten kenttien arvoja.</span><span class="sxs-lookup"><span data-stu-id="84fac-125">Search won't match values in images, BLOB fields, FlowFilters, FlowFields, and other fields that aren't part of a table.</span></span>


### <a name="fine-tuning-the-search-with-filter-criteria"></a><span data-ttu-id="84fac-126">Haun hienosäätäminen suodatusehdoilla</span><span class="sxs-lookup"><span data-stu-id="84fac-126">Fine-tuning the Search with Filter criteria</span></span>

<span data-ttu-id="84fac-127">Voit tehdä täsmällisemään haun käyttämällä suodatusoperaattoreita, lausekkeita ja suodatustunnuksia.</span><span class="sxs-lookup"><span data-stu-id="84fac-127">You can make a more exact search by using filter operators, expressions, and filter tokens.</span></span> <span data-ttu-id="84fac-128">Toisin kuin suodattaminen, niitä käytetään kaikissa kentissä, kun niitä käytetään hakuruudussa, jolloin ne eivät ole yhtä tehokkaita kuin suodattaminen.</span><span class="sxs-lookup"><span data-stu-id="84fac-128">Unlike filtering, these are applied across all fields when used in the search box, making them less efficient than filtering.</span></span>

- <span data-ttu-id="84fac-129">Jos haluat etsiä vain ne kenttien arvot, jotka vastaavat koko tekstiä ja kirjainkokoa, aseta haettava teksti yksinkertaisten lainausmerkkien sisään (`''`, esimerkiksi `'man'`).</span><span class="sxs-lookup"><span data-stu-id="84fac-129">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="84fac-130">Jos haluat etsiä arvoja, joiden alussa on tietty teksti ja jotka vastaavat tiettyä kirjainkokoa, aseta `*`-merkki hakutekstin jälkeen (esimerkiksi `man*`).</span><span class="sxs-lookup"><span data-stu-id="84fac-130">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="84fac-131">Jos haluat etsiä arvoja, joiden lopussa on tietty teksti, ja jotka vastaavat tiettyä kirjainkokoa, aseta `*`-merkki hakutekstin eteen (esimerkiksi `*man`).</span><span class="sxs-lookup"><span data-stu-id="84fac-131">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="84fac-132">Kun käytössä on `''` tai `*`, kirjainkoolla ei ole merkitystä haussa.</span><span class="sxs-lookup"><span data-stu-id="84fac-132">When using  `''` or `*`, the search is case-sensitive.</span></span> <span data-ttu-id="84fac-133">Jos haluat, että kirjainkoolla ei ole merkitystä haussa, aseta `@`-merkki ennen hakutekstiä (esimerkiksi `@man*`).</span><span class="sxs-lookup"><span data-stu-id="84fac-133">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="84fac-134">Seuraavassa taulukossa on esimerkkejä haun käyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="84fac-134">The following table provides some examples to explain how you can use the search.</span></span>

|<span data-ttu-id="84fac-135">Hakuehdot</span><span class="sxs-lookup"><span data-stu-id="84fac-135">Search Criteria</span></span>|<span data-ttu-id="84fac-136">Etsii...</span><span class="sxs-lookup"><span data-stu-id="84fac-136">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="84fac-137">tai</span><span class="sxs-lookup"><span data-stu-id="84fac-137">or</span></span> <br />`Man`|<span data-ttu-id="84fac-138">Kaikki tietueet, joissa on **man**-tekstin sisältäviä kenttiä kirjankoosta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="84fac-138">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="84fac-139">Esimerkiksi **Manchester**, **manual** tai **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="84fac-139">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="84fac-140">Kaikki tietueet, joissa on vain **Man**-tekstin sisältäviä kenttiä. Kirjainkoko on merkitsevä.</span><span class="sxs-lookup"><span data-stu-id="84fac-140">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="84fac-141">Kaikki tietueet, joissa on <b>Man</b>-tekstillä alkavia kenttiä. Kirjainkoko on merkitsevä.</span><span class="sxs-lookup"><span data-stu-id="84fac-141">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="84fac-142">Esimerkiksi **Manchester**, mutta ei **manual** tai **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="84fac-142">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="84fac-143">Kaikki tietueet, joissa on **man**-tekstillä alkavia kenttiä kirjainkoosta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="84fac-143">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="84fac-144">Esimerkiksi **Manchester** ja **manual**, mutta ei **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="84fac-144">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="84fac-145">Kaikki tietueet, joissa on **man**-tekstiin päättyviä kenttiä kirjainkoosta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="84fac-145">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="84fac-146">Esimerkiksi **Sportsman**, mutta ei **Manchester** tai **manual**.</span><span class="sxs-lookup"><span data-stu-id="84fac-146">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|


## <a name="filtering"></a><a name="filtering"></a><span data-ttu-id="84fac-147">Suodattaminen</span><span class="sxs-lookup"><span data-stu-id="84fac-147">Filtering</span></span>

<span data-ttu-id="84fac-148">Suodattaminen sisältää kehittyneitä ja monipuolisia toimintoja, joiden avulla määritetään luetteloon, raporttiin tai XMLportiin sisällytettävät tietueet.</span><span class="sxs-lookup"><span data-stu-id="84fac-148">Filtering provides a more advanced and versatile way to control which records are included in a list, report, or XMLport.</span></span> <span data-ttu-id="84fac-149">Hakemisella ja suodattamisella on kaksi pääeroa, jotka kerrotaan alla olevassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="84fac-149">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="84fac-150">**Hakeminen**</span><span class="sxs-lookup"><span data-stu-id="84fac-150">**Searching**</span></span> | <span data-ttu-id="84fac-151">**Suodattaminen**</span><span class="sxs-lookup"><span data-stu-id="84fac-151">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="84fac-152">**Käytettävissä olevat kentät**</span><span class="sxs-lookup"><span data-stu-id="84fac-152">**Applicable Fields**</span></span> | <span data-ttu-id="84fac-153">Hakee kaikista sivulla näkyvistä kentistä.</span><span class="sxs-lookup"><span data-stu-id="84fac-153">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="84fac-154">Suodattaa taulukon minkä tahansa kentän tai useita kenttiä mukaan lukien kentät, jotka eivät näy sivulla.</span><span class="sxs-lookup"><span data-stu-id="84fac-154">Filters one or more fields individually, selecting from any field on the table, including fields that aren't visible on the page.</span></span> |
| <span data-ttu-id="84fac-155">**Kohdistus**</span><span class="sxs-lookup"><span data-stu-id="84fac-155">**Matching**</span></span> | <span data-ttu-id="84fac-156">Näyttää tietueet, joiden kentät vastaavat hakutekstiä tekstin kirjainkoosta tai sijoittelusta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="84fac-156">Displays records with fields that match the search text, no matter the text's case or placement in the field.</span></span> | <span data-ttu-id="84fac-157">Näyttää tietueet, joiden kentät vastaavat suodatinta täysin. Kirjainkoko on merkitsevä, jos erityisiä suodatussymboleita ei ole annettu.</span><span class="sxs-lookup"><span data-stu-id="84fac-157">Displays records where the field exactly matches the filter, including the text's case, unless special filter symbols are entered.</span></span>

<span data-ttu-id="84fac-158">Suodattaminen mahdollistaa tiettyjen tilien tai asiakkaiden, päivämäärien, summien ja muiden tietojen tietueiden näyttämisen suodatusehtojen määrittämisen avulla.</span><span class="sxs-lookup"><span data-stu-id="84fac-158">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="84fac-159">Vain määritettyjä ehtoja vastaavat tietueet näytetään luettelossa tai sisällytetään raporttiin, erätyöhön tai XMLportiin.</span><span class="sxs-lookup"><span data-stu-id="84fac-159">Only records that match the criteria are displayed on the list or included in the report, batch job, or XMLport.</span></span> <span data-ttu-id="84fac-160">Jos määrität ehtoja usealle kentälle, vain kaikkia ehtoja vastaavat tietueet näytetään.</span><span class="sxs-lookup"><span data-stu-id="84fac-160">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

<span data-ttu-id="84fac-161">Luetteloiden suodattimet näkyvät suodatinruudussa luettelon vasemmalla puolella, kun se aktivoidaan.</span><span class="sxs-lookup"><span data-stu-id="84fac-161">For lists, the filters are displayed on a filter pane that appears to the left of the list when you activate it.</span></span> <span data-ttu-id="84fac-162">Raporttien, erätöiden ja XMLportien suodattimet näkyvät suoraan pyyntösivulla.</span><span class="sxs-lookup"><span data-stu-id="84fac-162">For reports, batch jobs, and XMLports, the filters are visible directly on the request page.</span></span>

### <a name="filtering-with-option-fields"></a><span data-ttu-id="84fac-163">Vaihtoehtokenttien käyttäminen suodattamiseen</span><span class="sxs-lookup"><span data-stu-id="84fac-163">Filtering with Option Fields</span></span>

<span data-ttu-id="84fac-164">Tavallisissa tietoja, määrityspäivämäärän tai liiketoimintatietoja sisältävissä kentissä suodattimia voi määrittää sekä valitsemalla tietoja ja kirjoittamalla suodatinarvoja. Suodatusehtoja voi lisäksi tarkentaa symbolien avulla.</span><span class="sxs-lookup"><span data-stu-id="84fac-164">For "ordinary" fields that hold data, setup date, or business data, you can set filters both by selecting data and by typing filter values, and you can use symbols to define advanced filter criteria.</span></span> <span data-ttu-id="84fac-165">Lisätietoja on kohdassa [Suodatusehtojen antaminen](ui-enter-criteria-filters.md#entering-filter-criteria).</span><span class="sxs-lookup"><span data-stu-id="84fac-165">For more information, see [Entering Filter Criteria](ui-enter-criteria-filters.md#entering-filter-criteria).</span></span>

<span data-ttu-id="84fac-166">**Vaihtoehto**-tyyppisissä kentissä suodatin voidaan kuitenkin määrittää vain valitsemalla yhden vaihtoehdon tai useita vaihtoehtoja avattavasta käytettävissä olevien vaihtoehtojen luettelosta.</span><span class="sxs-lookup"><span data-stu-id="84fac-166">For fields of type **Option**, however, you can only set a filter by selecting one or more options from a drop-down list of the available options.</span></span> <span data-ttu-id="84fac-167">Esimerkki vaihtoehtokentästä on **Myyntitilaukset**-sivun **Tila**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="84fac-167">An example of an option field is the **Status** field on the **Sales Orders** page.</span></span>

> [!NOTE]
> <span data-ttu-id="84fac-168">Jos valitset suodatusarvoksi useita vaihtoehtoja, vaihtoehtojen välille määritetään *TAI*-suhde.</span><span class="sxs-lookup"><span data-stu-id="84fac-168">When you select multiple options as a filter value, the relationship between the options is defined as *OR*.</span></span> <span data-ttu-id="84fac-169">Jos valitset esimerkiksi sekä **Avoin**- ja **Vapautettu**-valintaruudun **Tila**-suodatuskentän **Myyntitilaukset**-sivulla, silloin näytetään myyntitilaukset, jotka ovat joko avoimia tai vapautettuja.</span><span class="sxs-lookup"><span data-stu-id="84fac-169">For example, if you select both the **Open** and the **Released** check box in the **Status** filter field on the **Sales Orders** page, it means that sales orders that are either open or released are displayed.</span></span>

### <a name="setting-filters-on-lists"></a><span data-ttu-id="84fac-170">Suodattimien määrittäminen luetteloissa</span><span class="sxs-lookup"><span data-stu-id="84fac-170">Setting Filters on Lists</span></span>

<span data-ttu-id="84fac-171">Luetteloiden suodattimet määritetään suodatinruudussa.</span><span class="sxs-lookup"><span data-stu-id="84fac-171">On lists, you set filters by using the filter pane.</span></span> <span data-ttu-id="84fac-172">Avaa luettelon suodatinruutu valitsemalla sivun nimen vieressä oleva avattavan luettelon nuoli ja valitse sitten **Näytä suodatinruutu** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="84fac-172">To display the filter pane for a list, choose the drop-down arrow next to the name of the page, and then choose the **Show filter pane** action.</span></span> <span data-ttu-id="84fac-173">Vaihtoehtoisesti voit painaa näppäinyhdistelmää **Vaihto+F3**.</span><span class="sxs-lookup"><span data-stu-id="84fac-173">Alternatively, press **Shift+F3**.</span></span>

<span data-ttu-id="84fac-174">Avaa luettelon sarakkeen suodatinruutu valitsemalla avattavan luettelon nuoli ja valitse sitten **Suodatus**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="84fac-174">To display the filter pane for a column on a list, choose the drop-down arrow, and then choose the **Filter** action.</span></span> <span data-ttu-id="84fac-175">Vaihtoehtoisesti voit painaa näppäinyhdistelmää **Vaihto+F3**.</span><span class="sxs-lookup"><span data-stu-id="84fac-175">Alternatively, press **Shift+F3**.</span></span> <span data-ttu-id="84fac-176">Valittu sarake näkyy avautuvassa suodatinruudussa suodatuskenttänä **Luettelon suodatusperuste** -osana.</span><span class="sxs-lookup"><span data-stu-id="84fac-176">The filter pane opens with the selected column shown as a filter field in the **Filter list by** section.</span></span>

<span data-ttu-id="84fac-177">Suodatinruudussa näkyvät luettelon nykyiset suodattimet. Sen avulla voi määrittää omia suodattimia yhdelle tai usealle kentälle **+ Suodatus** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="84fac-177">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields by choosing the **+ Filter** action.</span></span>

 <span data-ttu-id="84fac-178">Suodatinruutu on jaettu kolmeen osaan: **Näkymät**, **Luettelon suodatusperuste** ja **Kokonaisarvojen suodatusperuste**:</span><span class="sxs-lookup"><span data-stu-id="84fac-178">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="84fac-179">**Näkymät**</span><span class="sxs-lookup"><span data-stu-id="84fac-179">**Views**</span></span>

  <span data-ttu-id="84fac-180">Joissakin luetteloissa on **Näkymät**-osa.</span><span class="sxs-lookup"><span data-stu-id="84fac-180">Some lists include the **Views** section.</span></span> <span data-ttu-id="84fac-181">Näkymät ovat luettelon muunnoksia, jotka on esimääritetty suodattimien kanssa.</span><span class="sxs-lookup"><span data-stu-id="84fac-181">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="84fac-182">Voit määrittää ja tallentaa niin monta näkymää luetteloa kohti kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="84fac-182">You can define and save as many views as you want per list.</span></span> <span data-ttu-id="84fac-183">Näkymät ovat käytettävissäsi kaikissa laitteissa, joihin kirjaudut.</span><span class="sxs-lookup"><span data-stu-id="84fac-183">The views will be available to you on any device you sign into.</span></span> <span data-ttu-id="84fac-184">Lisätietoja on kohdassa [Luettelonäkymien tallentaminen ja mukauttaminen](ui-views.md).</span><span class="sxs-lookup"><span data-stu-id="84fac-184">For more information, see [Save and Personalize List Views](ui-views.md).</span></span>

- <span data-ttu-id="84fac-185">**Luettelon suodatusperuste**</span><span class="sxs-lookup"><span data-stu-id="84fac-185">**Filter list by**</span></span>

  <span data-ttu-id="84fac-186">Tässä osassa lisätään suodattimet tietyille kentille ja vähennetään näin näytettävien tietueiden määrää.</span><span class="sxs-lookup"><span data-stu-id="84fac-186">This section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="84fac-187">Lisää suodatin valitsemalla **+ Suodatin** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="84fac-187">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="84fac-188">Kirjoita sitten luettelon suodatusperusteena käytettävän kentän nimi tai valitsemalla kenttä avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="84fac-188">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

- <span data-ttu-id="84fac-189">**Kokonaisarvojen suodatusperuste**</span><span class="sxs-lookup"><span data-stu-id="84fac-189">**Filter totals by**</span></span>

  <span data-ttu-id="84fac-190">Jotkin laskettuja kenttiä, kuten summia ja määriä, näyttävät luettelot sisältävät **Kokonaisarvojen suodatusperuste** -osan. Siinä voi muokata erilaisia laskelmiin vaikuttavia dimensioita.</span><span class="sxs-lookup"><span data-stu-id="84fac-190">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="84fac-191">Lisää suodatin valitsemalla **+ Suodatin** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="84fac-191">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="84fac-192">Kirjoita sitten luettelon suodatusperusteena käytettävän kentän nimi tai valitsemalla kenttä avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="84fac-192">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="84fac-193">FlowFilter-suodattimet ohjaavat **Kokonaisarvojen suodatusperuste** -osan suodattimia sivun rakenteessa.</span><span class="sxs-lookup"><span data-stu-id="84fac-193">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="84fac-194">Teknisiä lisätietoja on kohdassa [FlowFilter-suodattimet](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="84fac-194">For technical information, see [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>

<span data-ttu-id="84fac-195">Voit määrittää yksinkertaisen suodattimen suoraan luettelossa käyttämällä suodatinruutua. Tällainen suodatin näyttää vain tietueet, joilla on sama arvo kuin valitussa solussa.</span><span class="sxs-lookup"><span data-stu-id="84fac-195">You can set a simple filter directly on a list within using the filter pane, namely a filter that displays only records with the same value as in the selected cell.</span></span> <span data-ttu-id="84fac-196">Valitse solu luettelossa valitsemalla ensin avattavan luettelon nuoli ja sitten **Suodata tähän arvoon** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="84fac-196">Select a cell on the list, choose the drop-down arrow, and then choose the **Filter to This Value** action.</span></span> <span data-ttu-id="84fac-197">Vaihtoehtoisesti voit painaa näppäinyhdistelmää **Alt+F3**.</span><span class="sxs-lookup"><span data-stu-id="84fac-197">Alternatively, press **Alt+F3**.</span></span>

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a><span data-ttu-id="84fac-198">Raporttien, erätöiden ja XMLportien suodattimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="84fac-198">Setting Filters in Reports, Batch Jobs, and XMLports</span></span>

<span data-ttu-id="84fac-199">Raporttien ja XMLportien suodattimet näkyvät suoraan pyyntösivulla.</span><span class="sxs-lookup"><span data-stu-id="84fac-199">For reports and XMLports, the filters are visible directly on the request page.</span></span> <span data-ttu-id="84fac-200">Viimeksi käytetyt suodattimet näkyvät pyyntösivulla **Käytä oletusarvoja kohteesta:** -kentän valinnan mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="84fac-200">The request page displays the last used filters according to your selection in the **Use default values from** field.</span></span> <span data-ttu-id="84fac-201">Lisätietoja on kohdassa [Tallennettujen asetusten käyttäminen](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="84fac-201">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="84fac-202">**Suodatuksen** pääosassa näkyy oletussuodatuskentät, joilla rajoitetaan raporttiin tai XMLportiin sisällytettäviä tietueita.</span><span class="sxs-lookup"><span data-stu-id="84fac-202">The main **Filter** section shows the default filter fields that you use to delimit which records to include in the report or XMLport.</span></span> <span data-ttu-id="84fac-203">Lisää suodatin valitsemalla **+ Suodatin** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="84fac-203">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="84fac-204">Kirjoita sitten suodatusperusteena käytettävän kentän nimi tai valitsemalla kenttä avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="84fac-204">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

<span data-ttu-id="84fac-205">Voit säätää **Kokonaisarvojen suodatusperuste** -osassa erilaisia dimensioita, jotka vaikuttavat raportin tai XMLportin laskelmiin.</span><span class="sxs-lookup"><span data-stu-id="84fac-205">In the **Filter totals by** section, you can adjust various dimensions that influence calculations in the report or XMLport.</span></span> <span data-ttu-id="84fac-206">Lisää suodatin valitsemalla **+ Suodatin** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="84fac-206">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="84fac-207">Kirjoita sitten suodatusperusteena käytettävän kentän nimi tai valitsemalla kenttä avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="84fac-207">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

## <a name="entering-filter-criteria"></a><span data-ttu-id="84fac-208">Suodatusehtojen antaminen</span><span class="sxs-lookup"><span data-stu-id="84fac-208">Entering Filter Criteria</span></span>

<span data-ttu-id="84fac-209">Voit antaa suodatinruudussa ja pyyntösivulla suodatusehdot suodatuskentän ruudussa.</span><span class="sxs-lookup"><span data-stu-id="84fac-209">Both in the filter pane and on a request page, you enter your filter criteria in the box under the filter field.</span></span>

<span data-ttu-id="84fac-210">Suodatettavan kentän tyyppi määrittää, millaisia ehtoja voi antaa.</span><span class="sxs-lookup"><span data-stu-id="84fac-210">The type of the filter field determines which criteria you can enter.</span></span> <span data-ttu-id="84fac-211">Jos esimerkiksi suodatetaan kenttä, jossa on kiinteitä arvoja, valittavissa on vain nämä arvot.</span><span class="sxs-lookup"><span data-stu-id="84fac-211">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="84fac-212">Lisätietoja erityisistä suodatussymboleista on kohdissa [Suodatusehdot](#FilterCriteria) ja [Suodatuksen tunnukset](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="84fac-212">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="84fac-213">Sarakkeet, joilla on jo suodattimia, löytyvät, kun käytössä on sarakeotsikon ![Suodatus-kuvake](media/ui-search/filter-icon.png "Suodatin-kuvake").</span><span class="sxs-lookup"><span data-stu-id="84fac-213">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") icon in the column heading.</span></span> <span data-ttu-id="84fac-214">Voit poistaa suodattimen valitsemalla avattavan luettelon nuolen ja valitsemalla sitten **Tyhjennä suodatin** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="84fac-214">To remove a filter, choose the drop-down arrow, and then choose the **Clear Filter** action.</span></span>

> [!TIP]
> <span data-ttu-id="84fac-215">Nopeuta tietojen etsimistä ja analysoimista pikanäppäinyhdistelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="84fac-215">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="84fac-216">Voit esimerkiksi valita kentän ja lisätä kentän suodatinruutuun **Vaihto+Alt+F3**-pikanäppäinten avulla, kirjoittaa suodatinehdot ja palata riveille **Ctrl+Enter**-pikanäppäinten avulla. Valitse toinen kenttä ja suodata sen arvot **Alt+F3**-pikanäppäimillä.</span><span class="sxs-lookup"><span data-stu-id="84fac-216">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span> <span data-ttu-id="84fac-217">Lisätietoja on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="84fac-217">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

### <a name="filter-criteria-and-operators"></a><span data-ttu-id="84fac-218"><a name="FilterCriteria"> </a>Suodatusehdot ja operaattorit</span><span class="sxs-lookup"><span data-stu-id="84fac-218"><a name="FilterCriteria"> </a>Filter Criteria and Operators</span></span>

<span data-ttu-id="84fac-219">Kun syötät kriteerejä, voit käyttää kaikkia numeroita ja kirjaimia, joita voi yleensäkin käyttää kentässä.</span><span class="sxs-lookup"><span data-stu-id="84fac-219">When you enter criteria, you can use all the numbers and letters that you normally use in the field.</span></span> <span data-ttu-id="84fac-220">Mutta on olemassa myös joukko erikoismerkkejä, joita voit käyttää operaattoreina suodattaaksesi tuloksia edelleen.</span><span class="sxs-lookup"><span data-stu-id="84fac-220">But there's also a set of special symbols that you can use as operators to further filter the results.</span></span> <span data-ttu-id="84fac-221">Seuraavissa osissa on kuvattu nämä symbolit ja niiden käyttö suodattimien operaattoreina.</span><span class="sxs-lookup"><span data-stu-id="84fac-221">The following sections describe these symbols and how to use them as operators in filters.</span></span>

> [!TIP]
> <span data-ttu-id="84fac-222">Lisätietoja päivämäärien ja aikojen suodatuksesta on kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="84fac-222">For more information about filtering dates and times, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="84fac-223">Voi olla tilanteita, joissa suodatettava arvo sisältää symbolin, joka on operaattori.</span><span class="sxs-lookup"><span data-stu-id="84fac-223">There may be situations where the value that you want to filter on contains a symbol that's an operator.</span></span> <span data-ttu-id="84fac-224">Lisätietoja näiden tilanteiden käsittelemiseksi on kohdassa [Symboleja sisältävien arvojen suodattaminen](#symbols).</span><span class="sxs-lookup"><span data-stu-id="84fac-224">For more information about handling these situtions, see [Filtering on Values That Contain Symbols](#symbols) for more instructions about handling this situation.</span></span>
>
> - <span data-ttu-id="84fac-225">Jos yhdessä suodattimessa on yli 200 operaattoria, järjestelmä ryhmittää jotkin lausekkeet sulkeisiin `()` käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="84fac-225">If there are more than 200 operators in a single filter, the system will automatically group some expressions in parentheses `()` for the purpose of processing.</span></span> <span data-ttu-id="84fac-226">Se ei vaikuta suodattimeen eikä tuloksiin.</span><span class="sxs-lookup"><span data-stu-id="84fac-226">This has no effect on the filter or the results.</span></span>  

#### <a name="-interval"></a><span data-ttu-id="84fac-227">(..) väli</span><span class="sxs-lookup"><span data-stu-id="84fac-227">(..) Interval</span></span>

|<span data-ttu-id="84fac-228">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-228">Sample Expression</span></span>|<span data-ttu-id="84fac-229">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-229">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="84fac-230">Numerot 1100 - 2100</span><span class="sxs-lookup"><span data-stu-id="84fac-230">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="84fac-231">Numeroon 2500 asti, 2500 mukaan lukien</span><span class="sxs-lookup"><span data-stu-id="84fac-231">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="84fac-232">Päivämäärät 31.12.00 asti, kyseinen päivämäärä mukaan lukien</span><span class="sxs-lookup"><span data-stu-id="84fac-232">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="84fac-233">Tiedot kirjanpitojaksosta 8 ja siitä eteenpäin</span><span class="sxs-lookup"><span data-stu-id="84fac-233">Information for accounting period 8 and after</span></span>|  
|`..23`|<span data-ttu-id="84fac-234">Alkupäivämäärästä lähtien päivään 23 nykyistä kuukautta nykyistä vuotta klo 23:59:59</span><span class="sxs-lookup"><span data-stu-id="84fac-234">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="84fac-235">Päivästä 23 nykyistä kuukautta nykyistä vuotta klo 00:00:00 ajan loppuun asti</span><span class="sxs-lookup"><span data-stu-id="84fac-235">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="84fac-236">Päivästä 22 nykyistä kuukautta nykyistä vuotta klo 0:00:00 päivään 23 nykyistä kuukautta nykyistä vuotta klo 23:59:59</span><span class="sxs-lookup"><span data-stu-id="84fac-236">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

#### <a name="124-eitheror"></a><span data-ttu-id="84fac-237">(&#124;) Joko/tai</span><span class="sxs-lookup"><span data-stu-id="84fac-237">(&#124;) Either/or</span></span>

|<span data-ttu-id="84fac-238">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-238">Sample Expression</span></span>|<span data-ttu-id="84fac-239">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-239">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1200|1300`|<span data-ttu-id="84fac-240">Numerot, joissa on 1200 tai 1300</span><span class="sxs-lookup"><span data-stu-id="84fac-240">Numbers with 1200 or 1300</span></span>|  

#### <a name="-not-equal-to"></a><span data-ttu-id="84fac-241">(<>) ei ole sama kuin</span><span class="sxs-lookup"><span data-stu-id="84fac-241">(<>) Not equal to</span></span>  

|<span data-ttu-id="84fac-242">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-242">Sample Expression</span></span>|<span data-ttu-id="84fac-243">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-243">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="84fac-244">Kaikki numerot paitsi 0</span><span class="sxs-lookup"><span data-stu-id="84fac-244">All numbers except 0</span></span><br /><br /> <span data-ttu-id="84fac-245">SQL Server -vaihtoehto sallii tämän symbolin yhdistämisen yleismerkkihakuun.</span><span class="sxs-lookup"><span data-stu-id="84fac-245">The SQL Server Option allows you to combine this symbol with a wild-card expression.</span></span> <span data-ttu-id="84fac-246">Esimerkiksi: <>A\* - ei teksti, joka alkaa kirjaimella A.</span><span class="sxs-lookup"><span data-stu-id="84fac-246">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

#### <a name="-greater-than"></a><span data-ttu-id="84fac-247">(>) suurempi kuin</span><span class="sxs-lookup"><span data-stu-id="84fac-247">(>) Greater than</span></span>  

|<span data-ttu-id="84fac-248">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-248">Sample Expression</span></span>|<span data-ttu-id="84fac-249">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-249">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="84fac-250">Numerot, jotka ovat suurempia kuin 1200</span><span class="sxs-lookup"><span data-stu-id="84fac-250">Numbers greater than 1200</span></span>|  

#### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="84fac-251">(>=) Suurempi tai yhtä suuri</span><span class="sxs-lookup"><span data-stu-id="84fac-251">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="84fac-252">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-252">Sample Expression</span></span>|<span data-ttu-id="84fac-253">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-253">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="84fac-254">Numerot, jotka ovat suurempia tai yhtä suuria kuin 1200</span><span class="sxs-lookup"><span data-stu-id="84fac-254">Numbers greater than or equal to 1200</span></span>|  

#### <a name="-less-than"></a><span data-ttu-id="84fac-255">(<) pienempi kuin</span><span class="sxs-lookup"><span data-stu-id="84fac-255">(<) Less than</span></span>  

|<span data-ttu-id="84fac-256">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-256">Sample Expression</span></span>|<span data-ttu-id="84fac-257">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-257">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="84fac-258">Numerot, jotka ovat pienempiä kuin 1200</span><span class="sxs-lookup"><span data-stu-id="84fac-258">Numbers less than 1200</span></span>|  

#### <a name="-less-than-or-equal-to"></a><span data-ttu-id="84fac-259">(<=) Pienempi tai yhtä suuri</span><span class="sxs-lookup"><span data-stu-id="84fac-259">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="84fac-260">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-260">Sample Expression</span></span>|<span data-ttu-id="84fac-261">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-261">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="84fac-262">Numerot, jotka ovat pienempiä tai yhtä suuria kuin 1200</span><span class="sxs-lookup"><span data-stu-id="84fac-262">Numbers less than or equal to 1200</span></span>|  

#### <a name="-and"></a><span data-ttu-id="84fac-263">(&) ja</span><span class="sxs-lookup"><span data-stu-id="84fac-263">(&) And</span></span>  

|<span data-ttu-id="84fac-264">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-264">Sample Expression</span></span>|<span data-ttu-id="84fac-265">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-265">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="84fac-266">Luvut, jotka ovat suurempia kuin 200 ja pienempiä kuin 1200.</span><span class="sxs-lookup"><span data-stu-id="84fac-266">Numbers greater than 200 and less than 1200</span></span>|  

#### <a name="-an-exact-character-match"></a><span data-ttu-id="84fac-267">('') Tarkka merkin vastine</span><span class="sxs-lookup"><span data-stu-id="84fac-267">('') An exact character match</span></span>  

|<span data-ttu-id="84fac-268">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-268">Sample Expression</span></span>|<span data-ttu-id="84fac-269">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-269">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="84fac-270">Teksti, joka vastaa täysin merkkijonoa **man** ja jossa isoilla ja pienillä kirjaimilla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="84fac-270">Text that matches **man** exactly and is case-sensitive.</span></span>|  

#### <a name="-case-insensitive"></a><span data-ttu-id="84fac-271">(@) Ei kirjainkokoon perustuva</span><span class="sxs-lookup"><span data-stu-id="84fac-271">(@) Case insensitive</span></span>  

|<span data-ttu-id="84fac-272">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-272">Sample Expression</span></span>|<span data-ttu-id="84fac-273">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-273">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="84fac-274">Teksti, joka alkaa **man** ja jossa isoilla ja pienillä kirjaimilla ei ole merkitystä.</span><span class="sxs-lookup"><span data-stu-id="84fac-274">Text that starts with **man** and is case insensitive.</span></span>|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="84fac-275">(\*) Rajoittamaton määrä tuntemattomia merkkejä</span><span class="sxs-lookup"><span data-stu-id="84fac-275">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="84fac-276">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-276">Sample Expression</span></span>|<span data-ttu-id="84fac-277">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-277">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="84fac-278">Teksti, joka sisältää **Co** ja jossa kirjainkoolla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="84fac-278">Text that contains **Co** and is case-sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="84fac-279">Teksti, jonka lopussa on **Co** ja jossa kirjainkoolla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="84fac-279">Text that ends with **Co"** and is case-sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="84fac-280">Teksti, jonka alussa on **Co** ja jossa kirjainkoolla on merkitystä.</span><span class="sxs-lookup"><span data-stu-id="84fac-280">Text that begins with **Co** and is case-sensitive.</span></span>|  

#### <a name="-one-unknown-character"></a><span data-ttu-id="84fac-281">(?) yksi tuntematon merkki</span><span class="sxs-lookup"><span data-stu-id="84fac-281">(?) One unknown character</span></span>  

|<span data-ttu-id="84fac-282">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-282">Sample Expression</span></span>|<span data-ttu-id="84fac-283">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-283">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="84fac-284">Teksti, kuten **Hansen** tai **Hanson**</span><span class="sxs-lookup"><span data-stu-id="84fac-284">Text such as **Hansen** or **Hanson**</span></span>|  

#### <a name="combined-format-expressions"></a><span data-ttu-id="84fac-285">Yhdistetyn muodon lausekkeet</span><span class="sxs-lookup"><span data-stu-id="84fac-285">Combined Format Expressions</span></span>  

|<span data-ttu-id="84fac-286">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-286">Sample Expression</span></span>|<span data-ttu-id="84fac-287">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-287">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|<span data-ttu-id="84fac-288">Sisällytä kaikki tietueet, joissa on numero 5999 tai numero väliltä 8100 ja 8490.</span><span class="sxs-lookup"><span data-stu-id="84fac-288">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|`..1299|1400..`|<span data-ttu-id="84fac-289">Sisällytä tietueet, joissa on numero, joka on pienempi tai yhtä suuri kuin 1299 tai suurempi tai yhtä suuri kuin 1400 (siis kaikki muut numerot paitsi 1300–1399).</span><span class="sxs-lookup"><span data-stu-id="84fac-289">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="84fac-290">Sisällytä tietueet, joissa on numero, joka on suurempi kuin 50 ja pienempi kuin 100 (siis numerot 51–99).</span><span class="sxs-lookup"><span data-stu-id="84fac-290">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  

### <a name="filtering-on-values-that-contain-symbols"></a><a name="symbols"></a><span data-ttu-id="84fac-291">Symboleita sisältävien arvojen suodattaminen</span><span class="sxs-lookup"><span data-stu-id="84fac-291">Filtering on Values That Contain Symbols</span></span>

<span data-ttu-id="84fac-292">Joissakin tapauksissa kenttäarvot sisältävät jonkin seuraavista symboleista:</span><span class="sxs-lookup"><span data-stu-id="84fac-292">There may be cases where field values contain the one of the following symbols:</span></span>

- &
- <span data-ttu-id="84fac-293">(</span><span class="sxs-lookup"><span data-stu-id="84fac-293">(</span></span>
- <span data-ttu-id="84fac-294">)</span><span class="sxs-lookup"><span data-stu-id="84fac-294">)</span></span>
- =
- <span data-ttu-id="84fac-295">&#124;</span><span class="sxs-lookup"><span data-stu-id="84fac-295">&#124;</span></span>

<span data-ttu-id="84fac-296">Jos haluat suodattaa jonkin näistä symboleista, sijoita suodatinlauseke lainausmerkkeihin ('').</span><span class="sxs-lookup"><span data-stu-id="84fac-296">If you want to filter on any of these symbols, place the filter expression in quotation marks ('').</span></span> <span data-ttu-id="84fac-297">Jos haluat esimerkiksi suodattaa tietueita, joiden alussa on teksti *J & V*, suodatuslauseke on `'J & V*'`.</span><span class="sxs-lookup"><span data-stu-id="84fac-297">For example, if you wanted to filter on records that start with the text *J & V*, the filter expression would be `'J & V*'`.</span></span>

<span data-ttu-id="84fac-298">Tämä vaatimus ei ole välttämätön muille symboleille.</span><span class="sxs-lookup"><span data-stu-id="84fac-298">This requirement isn't necessary for other symbols.</span></span>

### <a name="filter-tokens"></a><span data-ttu-id="84fac-299"><a name="FilterTokens"> </a>Suodatuksen tunnukset</span><span class="sxs-lookup"><span data-stu-id="84fac-299"><a name="FilterTokens"> </a>Filter Tokens</span></span>

<span data-ttu-id="84fac-300">Kun syötät suodatusehtoja, voit kirjoittaa myös sanoja, joilla on erityinen tarkoitus. Niitä kutsutaan suodatuksen tunnuksiksi.</span><span class="sxs-lookup"><span data-stu-id="84fac-300">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="84fac-301">Kun olet syöttänyt tunnussanan, sana korvataan arvolla tai arvoilla, joita se edustaa.</span><span class="sxs-lookup"><span data-stu-id="84fac-301">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="84fac-302">Suodatuksen tunnukset helpottavat suodattamista ja vähentää muille sivuille siirtymistä ja suodattimeen lisättävien arvojen etsimistä.</span><span class="sxs-lookup"><span data-stu-id="84fac-302">Filter tokens make filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="84fac-303">Taulukossa on joitakin tunnuksia, joita voit käyttää suodatusehtoina.</span><span class="sxs-lookup"><span data-stu-id="84fac-303">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="84fac-304">Organisaatio voi käyttää mukautettuja tunnuksia.</span><span class="sxs-lookup"><span data-stu-id="84fac-304">Your organization may use custom tokens.</span></span> <span data-ttu-id="84fac-305">Järjestelmänvalvojalta saa lisätietoja käytettävissä olevista tunnuksista ja mukautettujen tunnusten lisäämisestä.</span><span class="sxs-lookup"><span data-stu-id="84fac-305">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="84fac-306">Teknisiä tietoja on kohdassa [Suodatuksen tunnusten lisääminen](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span><span class="sxs-lookup"><span data-stu-id="84fac-306">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span></span>

#### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="84fac-307">(%me tai %userid) Sinulle määritetyt tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-307">(%me or %userid) Records Assigned to You</span></span>

<span data-ttu-id="84fac-308">Käytä `%me`- tai `%userid`-tunnusta suodattaessasi kenttiä, jotka sisältävät käyttäjätunnuksen. Tällainen kenttä on esimerkiksi **Liitetty käyttäjätunnukseen**, jossa näytetään kaikki käyttäjälle liitetyt kentät.</span><span class="sxs-lookup"><span data-stu-id="84fac-308">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="84fac-309">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-309">Sample Expression</span></span>|<span data-ttu-id="84fac-310">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-310">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="84fac-311">tai</span><span class="sxs-lookup"><span data-stu-id="84fac-311">or</span></span><br />`%userid`|<span data-ttu-id="84fac-312">Tietueet, jotka on liitetty käyttäjätiliisi.</span><span class="sxs-lookup"><span data-stu-id="84fac-312">Records that are assigned to your user account.</span></span> |  

#### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="84fac-313">(%mycustomers) Omat asiakkaat -kohdan asiakkaat</span><span class="sxs-lookup"><span data-stu-id="84fac-313">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="84fac-314">Käytä `%mycustomers`-tunnusta asiakkaan **Nro**-kentässä, kun haluat näyttää asiakkaan kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat asiakkaat** -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="84fac-314">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="84fac-315">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-315">Sample Expression</span></span>|<span data-ttu-id="84fac-316">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-316">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="84fac-317">Roolikeskuksen **Omat asiakkaat** -kohdan asiakkaat.</span><span class="sxs-lookup"><span data-stu-id="84fac-317">Customers in the **My Customers** on your Role Center.</span></span> |  

#### <a name="myitems-items-in-my-items"></a><span data-ttu-id="84fac-318">(%myitems) Omat nimikkeet -kohdan nimikkeet</span><span class="sxs-lookup"><span data-stu-id="84fac-318">(%myitems) Items in My Items</span></span>

<span data-ttu-id="84fac-319">Käytä `%myitems`-tunnusta nimikkeen **Nro**-kentässä, kun haluat näyttää nimikkeiden kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat nimikkeet** -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="84fac-319">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="84fac-320">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-320">Sample Expression</span></span>|<span data-ttu-id="84fac-321">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-321">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="84fac-322">Roolikeskuksen **Omat nimikkeet** -kohdan nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="84fac-322">Items in the **My Items** on your Role Center.</span></span> |  

#### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="84fac-323">(%myvendors) Omat toimittajat -kohdan toimittajat</span><span class="sxs-lookup"><span data-stu-id="84fac-323">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="84fac-324">Käytä `%myvendors`-tunnusta toimittajan **Nro**-kentässä, kun haluat näyttää toimittajien kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat toimittajat** -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="84fac-324">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="84fac-325">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="84fac-325">Sample Expression</span></span>|<span data-ttu-id="84fac-326">Näkyvät tietueet</span><span class="sxs-lookup"><span data-stu-id="84fac-326">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="84fac-327">Roolikeskuksen **Omat toimittajat** -kohdan toimittajat.</span><span class="sxs-lookup"><span data-stu-id="84fac-327">Vendors in the **My Vendors** on your Role Center.</span></span> |  

## <a name="see-also"></a><span data-ttu-id="84fac-328">Katso myös</span><span class="sxs-lookup"><span data-stu-id="84fac-328">See Also</span></span>

[<span data-ttu-id="84fac-329">Usein kysyttyjen kysymysten haku ja suodatus</span><span class="sxs-lookup"><span data-stu-id="84fac-329">Searching and Filtering FAQ</span></span>](ui-search-filter-faq.md)  
[<span data-ttu-id="84fac-330">Luettelonäkymien tallentaminen ja mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="84fac-330">Save and Personalize List Views</span></span>](ui-views.md)  
<span data-ttu-id="84fac-331">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="84fac-331">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]