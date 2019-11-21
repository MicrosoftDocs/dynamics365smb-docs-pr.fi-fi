---
title: XML-malleihin perustuvien XMLports-kohteiden luominen | Microsoft Docs
description: Voit määrittää tiedonsiirtokehyksen XML-mallien avulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0d028206d1e17c7a1093cf2b93da02894909deb5
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554444"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="f2ff4-103">XML-mallien käyttäminen tietojenvaihtomääritysten valmisteluun</span><span class="sxs-lookup"><span data-stu-id="f2ff4-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>
<span data-ttu-id="f2ff4-104">Voit ottaa XML-tiedostojen tietojen tuonnin ja viennin käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]in tiedonsiirtokehyksessä määrittämällä [!INCLUDE[d365fin](includes/d365fin_md.md)]in kanssa vaihdettavat tietoelementit XML-mallien avulla.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f2ff4-105">Se tehdään **XML-mallin tarkastelutoiminto** -sivulla lataamalla XML-rakennetiedosto, valitsemalla sopivat tietoelementit ja käynnistämällä joko tietojen vaihdon määritys tai XMLport.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing either a data exchange definition or an XMLport.</span></span>  

 <span data-ttu-id="f2ff4-106">Kun olet määrittänyt XML-mallin perusteella sisällytettävät tietoelementit, voit luoda XMLport-objektin **Luo XMLport** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate XMLport** action to create the XMLport object.</span></span>  

 <span data-ttu-id="f2ff4-107">Voit myös käyttää **Luo tietojen vaihdon määritys** -toimintoa luodaksesi valittuihin tietoelementteihin perustuvan määrityksen, jonka sitten viimeistelet tietojen vaihtamiskehyksessä.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-107">Alternatively, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="f2ff4-108">Tällä tavoin **Kirjauksen tiedonsiirtomääritykset** -sivulla luodaan tietue. Jatka sivulla määrittämällä, mitkä tiedoston elementit ja mitkä [!INCLUDE[d365fin](includes/d365fin_md.md)]in kentät yhdistetään toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-108">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f2ff4-109">Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="f2ff4-109">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="f2ff4-110">Tämä ohjeaihe sisältää seuraavat menettelyt:</span><span class="sxs-lookup"><span data-stu-id="f2ff4-110">This topic contains the following procedures:</span></span>  

-   <span data-ttu-id="f2ff4-111">XML-rakennetiedoston lataaminen</span><span class="sxs-lookup"><span data-stu-id="f2ff4-111">To load an XML schema file</span></span>  

-   <span data-ttu-id="f2ff4-112">Solmujen valitseminen ja tyhjentäminen XML-rakenteessa</span><span class="sxs-lookup"><span data-stu-id="f2ff4-112">To select or clear nodes in an XML schema</span></span>  

-   <span data-ttu-id="f2ff4-113">XML-rakenteeseen perustuvan tietojen vaihtamismäärityksen luominen</span><span class="sxs-lookup"><span data-stu-id="f2ff4-113">To generate a data exchange definition that is based on an XML schema</span></span>  

-   <span data-ttu-id="f2ff4-114">XML-rakenteeseen perustuvan XMLportin luominen</span><span class="sxs-lookup"><span data-stu-id="f2ff4-114">To generate an XMLport for the file that is based on an XML schema</span></span>  

-   <span data-ttu-id="f2ff4-115">XMLportin tuominen objektien suunnitteluohjelmaan</span><span class="sxs-lookup"><span data-stu-id="f2ff4-115">To import an XMLport into the Object Designer</span></span>  

### <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="f2ff4-116">XML-rakennetiedoston lataaminen</span><span class="sxs-lookup"><span data-stu-id="f2ff4-116">To load an XML schema file</span></span>  

1.  <span data-ttu-id="f2ff4-117">Varmista, että sopiva XML-rakennetiedosto on saatavilla.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-117">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="f2ff4-118">Tiedostotunniste on .xsd.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-118">The file extension is .xsd.</span></span>  

2.  <span data-ttu-id="f2ff4-119">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XML-mallit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas**, and then choose the related link.</span></span>  

3.  <span data-ttu-id="f2ff4-120">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-120">Choose the **New** action.</span></span>  

4.  <span data-ttu-id="f2ff4-121">Täytä kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-121">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="f2ff4-122">Kenttä</span><span class="sxs-lookup"><span data-stu-id="f2ff4-122">Field</span></span>|<span data-ttu-id="f2ff4-123">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="f2ff4-123">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f2ff4-124">**Koodi**</span><span class="sxs-lookup"><span data-stu-id="f2ff4-124">**Code**</span></span>|<span data-ttu-id="f2ff4-125">Määritä koodi, jolla identifioit XML-kaavan.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-125">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="f2ff4-126">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="f2ff4-126">**Description**</span></span>|<span data-ttu-id="f2ff4-127">Määritä XML-kaavan kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-127">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="f2ff4-128">**Kohdenimitila**-kenttä määrittää riville ladatun XML-mallitiedoston nimitilan (joka voi olla mikä tahansa).</span><span class="sxs-lookup"><span data-stu-id="f2ff4-128">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5.  <span data-ttu-id="f2ff4-129">Valitse **Lataa malli** -toiminto ja valitse XML-mallitiedosto.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-129">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="f2ff4-130">Kun tiedosto on ladattu, rivin muihin kenttiin lisätään tiedoston tiedot ja **Malli on ladattu** -valintaruutu valitaan.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-130">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f2ff4-131">Ladatun XML-rakenteen puu on oletusarvoisesti tiivistettynä.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-131">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="f2ff4-132">Solmun voi laajentaa **+**-painikkeella.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-132">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="f2ff4-133">Kaikki solmut voi laajentaa käyttämällä **Laajenna kaikki** -painiketta valintanauhasta.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-133">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="f2ff4-134">Solmujen valitseminen ja tyhjentäminen XML-rakenteessa</span><span class="sxs-lookup"><span data-stu-id="f2ff4-134">To select or clear nodes in an XML schema</span></span>  

1.  <span data-ttu-id="f2ff4-135">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XML-mallin tarkastelutoiminto** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="f2ff4-136">Täytä otsikon kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-136">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="f2ff4-137">Kenttä</span><span class="sxs-lookup"><span data-stu-id="f2ff4-137">Field</span></span>|<span data-ttu-id="f2ff4-138">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="f2ff4-138">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f2ff4-139">**XML-mallin koodi**</span><span class="sxs-lookup"><span data-stu-id="f2ff4-139">**XML Schema Code**</span></span>|<span data-ttu-id="f2ff4-140">Määritä vaiheessa 5 lataamasi XML-rakennetiedosto "XML-rakenteen lataaminen" -osiossa.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-140">Specify the XML schema file that you loaded in step 5 in the “To load an XML schema file” section.</span></span>|  
    |<span data-ttu-id="f2ff4-141">**Uuden XMLportin numero**</span><span class="sxs-lookup"><span data-stu-id="f2ff4-141">**New XMLport No.**</span></span>|<span data-ttu-id="f2ff4-142">Määritä niiden XMLporttien määrä, jotka luodaan tästä XML-kaavasta, kun valitset **Luo XMLport** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-142">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="f2ff4-143">Rivit on nyt täytettä solmuilla, jotka edustavat kaikki XML-kaavan elementtejä.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-143">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="f2ff4-144">XML-mallin mukaan pakolliset elementtien solmut valitaan oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-144">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3.  <span data-ttu-id="f2ff4-145">Laajenna ensimmäisellä rivillä **Solmun nimi**-sarakkeessa **Asiakirja**-solmu ja laajenna sitten vähitellen alapuolella olevia solmuja, joita haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-145">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="f2ff4-146">Vaihtoehtoisesti, napsauta solmua hiiren kakkospainikkeella ja valitse sitten **Laajenna kaikki**.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-146">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4.  <span data-ttu-id="f2ff4-147">Valitse yksi seuraavista toiminnoista muuttaaksesi mitkä solmut näytetään.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-147">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="f2ff4-148">**Toiminto**</span><span class="sxs-lookup"><span data-stu-id="f2ff4-148">**Action**</span></span>|<span data-ttu-id="f2ff4-149">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="f2ff4-149">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="f2ff4-150">**Näytä kaikki**</span><span class="sxs-lookup"><span data-stu-id="f2ff4-150">**Show All**</span></span>|<span data-ttu-id="f2ff4-151">Kaikki solmut ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-151">All nodes are shown.</span></span>|  
    |<span data-ttu-id="f2ff4-152">**Piilota ei-pakollinen**</span><span class="sxs-lookup"><span data-stu-id="f2ff4-152">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="f2ff4-153">Ainoastaan XML-rakenteen perusteella pakollisia elementtejä esittävät solmut näytetään.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-153">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="f2ff4-154">Näiden solmujen merkintänä on yleensä **1** **MinOccurs**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-154">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="f2ff4-155">Käännä näkymä valitsemalla **Näytä kaikki**.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-155">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="f2ff4-156">**Piilota ei-valittu**</span><span class="sxs-lookup"><span data-stu-id="f2ff4-156">**Hide Non-Selected**</span></span>|<span data-ttu-id="f2ff4-157">Vain solmut, joissa **Valittu**-valintaruutu on valittuna näytetään.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-157">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="f2ff4-158">Käännä näkymä valitsemalla **Näytä kaikki**.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-158">Choose **Show All** to reverse the view.</span></span>|  

5.  <span data-ttu-id="f2ff4-159">Valitse **Muokkaa** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-159">Choose the **Edit** action.</span></span>  

6.  <span data-ttu-id="f2ff4-160">Määritä **Valittu**-valintaruutu jokaiselle solmulle, jonka elementin haluat olevan tuettuna liittyvän SEPA-pankkitiedoston tiedonsiirtomäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-160">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f2ff4-161">Kun valitset pakollisen alisolmun, kaikki sen pääsolmut valitaan myös.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-161">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7.  <span data-ttu-id="f2ff4-162">Voit valita uudelleen kaikki solmut, jotka kuvaavat XML-mallin mukaan pakollisia elementtejä valitsemalla **Valitse kaikki pakolliset elementit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-162">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8.  <span data-ttu-id="f2ff4-163">Poista kaikki valinnat valitsemalla **Poista kaikkien valinta** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-163">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="f2ff4-164">**Valinta**-kenttä määrittää, että solmulla on vähintään kaksi sisarussolmua, jotka toimivat vaihtoehtoina.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-164">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="f2ff4-165">XML-rakenteeseen perustuvan tietojen vaihtamismäärityksen luominen</span><span class="sxs-lookup"><span data-stu-id="f2ff4-165">To generate a data exchange definition that is based on an XML schema</span></span>  

1.  <span data-ttu-id="f2ff4-166">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä  **XML-mallit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-166">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="f2ff4-167">Valitse sopiva XML-malli ja valitse sitten **Avaa XML-mallin tarkastelutoiminto** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-167">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3.  <span data-ttu-id="f2ff4-168">Varmista, että tarvittavat solmut ovat valittuina.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-168">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="f2ff4-169">Lisätietoja on ohjeen kohdassa "Solmujen valitseminen ja tyhjentäminen XML-rakenteessa".</span><span class="sxs-lookup"><span data-stu-id="f2ff4-169">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

4.  <span data-ttu-id="f2ff4-170">Valitse **XML-mallin tarkastelutoiminto** -sivulla **Luo tiedonsiirtomääritys** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-170">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="f2ff4-171">Tiedonsiirtomääritys luodaan **Kirjauksen tiedonsiirtomääritykset** -sivulla, jossa sen voi viimeistellä määrittämällä, mitkä tiedoston elementit ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in kentät yhdistetään toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-171">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f2ff4-172">Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="f2ff4-172">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f2ff4-173">Voit käyttää myös **Kirjauksen tiedonsiirtomääritykset** -sivun **Hae tiedostorakenne** -toimintoa. Tämä sivu täyttää **Sarakkeen määritykset** -pikavälilehden valmiiksi **XML-mallin tarkastelutoiminto** -sivun toiminnoilla.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-173">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a><span data-ttu-id="f2ff4-174">XML-rakenteeseen perustuvan XMLportin luominen</span><span class="sxs-lookup"><span data-stu-id="f2ff4-174">To generate an XMLport that is based on an XML schema</span></span>  

1.  <span data-ttu-id="f2ff4-175">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä  **XML-mallit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-175">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="f2ff4-176">Valitse sopiva XML-malli ja valitse sitten **Avaa XML-mallin tarkastelutoiminto** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-176">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3.  <span data-ttu-id="f2ff4-177">Määritä **Uuden XMLportin numero**</span><span class="sxs-lookup"><span data-stu-id="f2ff4-177">In the **New XMLport No.**</span></span> <span data-ttu-id="f2ff4-178">-kentässä numero, joka annetaan uudelle XMLport-objektille luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-178">field, specify the number that the new XMLport object will be given when it is generated.</span></span>  

4.  <span data-ttu-id="f2ff4-179">Varmista, että tarvittavat solmut ovat valittuina.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-179">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="f2ff4-180">Lisätietoja on ohjeen kohdassa "Solmujen valitseminen ja tyhjentäminen XML-rakenteessa".</span><span class="sxs-lookup"><span data-stu-id="f2ff4-180">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

5.  <span data-ttu-id="f2ff4-181">Valitse Luo **Luo XMLport** -toiminto ja tallenna objekti sitten .txt-tiedostona oikeaan paikkaan.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-181">Choose the **Generate XMLport** action, and then save the object as a .txt file in an appropriate location.</span></span>  

6. <span data-ttu-id="f2ff4-182">Tuo uusi XMLport [!INCLUDE[d365fin](includes/d365fin_md.md)]in kehitysympäristöön ja käännä se.</span><span class="sxs-lookup"><span data-stu-id="f2ff4-182">Import the new XMLport into the [!INCLUDE[d365fin](includes/d365fin_md.md)] development environment and compile it.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2ff4-183">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f2ff4-183">See Also</span></span>  
<span data-ttu-id="f2ff4-184">[Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md) </span><span class="sxs-lookup"><span data-stu-id="f2ff4-184">[Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) </span></span>  
<span data-ttu-id="f2ff4-185">[Maksujen vienti pankkitiedostoon](payables-how-export-payments-bank-file.md) </span><span class="sxs-lookup"><span data-stu-id="f2ff4-185">[Export Payments to a Bank File](payables-how-export-payments-bank-file.md) </span></span>  
<span data-ttu-id="f2ff4-186">[Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="f2ff4-186">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
[<span data-ttu-id="f2ff4-187">Tietoja tiedonvaihto-kehyksestä</span><span class="sxs-lookup"><span data-stu-id="f2ff4-187">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)
