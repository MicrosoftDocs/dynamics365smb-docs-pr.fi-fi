---
title: XML-mallien käyttäminen tietojenvaihtomääritysten valmisteluun
description: Voit määrittää asiakirjojen vaihtokehyksen XML-mallien avulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 70e80403175c6a77d120a3b405b1b5758410c227
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781359"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="e1c80-103">XML-mallien käyttäminen tiedonsiirtomääritysten valmisteluun</span><span class="sxs-lookup"><span data-stu-id="e1c80-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>

<span data-ttu-id="e1c80-104">Voit ottaa XML-tiedostojen tietojen tuonnin ja viennin käyttöön [!INCLUDE[prod_short](includes/prod_short.md)]in tiedonsiirtokehyksessä määrittämällä [!INCLUDE[prod_short](includes/prod_short.md)]in kanssa vaihdettavat tietoelementit XML-mallien avulla.</span><span class="sxs-lookup"><span data-stu-id="e1c80-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[prod_short](includes/prod_short.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="e1c80-105">Se tehdään **XML-mallin tarkastelutoiminto** -sivulla lataamalla XML-rakennetiedosto, valitsemalla sopivat tietoelementit ja käynnistämällä siiten tiedonsiirtomääritys.</span><span class="sxs-lookup"><span data-stu-id="e1c80-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing a data exchange definition.</span></span>  

 <span data-ttu-id="e1c80-106">Kun olet määrittänyt XML-mallin perusteella sisällytettävät tietoelementit, voit käynnistää **Luo tiedonsiirtomääritys** -toiminnolla valittuihin tietoelementteihin perustuvan tiedonsiirtomäärityksen, joka sitten viimeistellään tiedonsiirtokehyksessä.</span><span class="sxs-lookup"><span data-stu-id="e1c80-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="e1c80-107">Tällä tavoin **Kirjauksen tiedonsiirtomääritykset** -sivulla luodaan tietue. Jatka sivulla määrittämällä, mitkä tiedoston elementit ja mitkä [!INCLUDE[prod_short](includes/prod_short.md)]in kentät yhdistetään toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="e1c80-107">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="e1c80-108">Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="e1c80-108">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="e1c80-109">Tämä ohjeaihe sisältää seuraavat menettelyt:</span><span class="sxs-lookup"><span data-stu-id="e1c80-109">This topic contains the following procedures:</span></span>  

- <span data-ttu-id="e1c80-110">XML-rakennetiedoston lataaminen</span><span class="sxs-lookup"><span data-stu-id="e1c80-110">To load an XML schema file</span></span>  

- <span data-ttu-id="e1c80-111">Solmujen valitseminen ja tyhjentäminen XML-rakenteessa</span><span class="sxs-lookup"><span data-stu-id="e1c80-111">To select or clear nodes in an XML schema</span></span>  

- <span data-ttu-id="e1c80-112">XML-rakenteeseen perustuvan tietojen vaihtamismäärityksen luominen</span><span class="sxs-lookup"><span data-stu-id="e1c80-112">To generate a data exchange definition that is based on an XML schema</span></span>  

## <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="e1c80-113">XML-rakennetiedoston lataaminen</span><span class="sxs-lookup"><span data-stu-id="e1c80-113">To load an XML schema file</span></span>

1. <span data-ttu-id="e1c80-114">Varmista, että sopiva XML-rakennetiedosto on saatavilla.</span><span class="sxs-lookup"><span data-stu-id="e1c80-114">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="e1c80-115">Tiedostotunniste on .xsd.</span><span class="sxs-lookup"><span data-stu-id="e1c80-115">The file extension is .xsd.</span></span>  

2. <span data-ttu-id="e1c80-116">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XML-mallit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="e1c80-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas**, and then choose the related link.</span></span>  

3. <span data-ttu-id="e1c80-117">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="e1c80-117">Choose the **New** action.</span></span>  

4. <span data-ttu-id="e1c80-118">Täytä kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="e1c80-118">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="e1c80-119">Kenttä</span><span class="sxs-lookup"><span data-stu-id="e1c80-119">Field</span></span>|<span data-ttu-id="e1c80-120">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="e1c80-120">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="e1c80-121">**Koodi**</span><span class="sxs-lookup"><span data-stu-id="e1c80-121">**Code**</span></span>|<span data-ttu-id="e1c80-122">Määritä koodi, jolla identifioit XML-kaavan.</span><span class="sxs-lookup"><span data-stu-id="e1c80-122">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="e1c80-123">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="e1c80-123">**Description**</span></span>|<span data-ttu-id="e1c80-124">Määritä XML-kaavan kuvaus.</span><span class="sxs-lookup"><span data-stu-id="e1c80-124">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="e1c80-125">**Kohdenimitila**-kenttä määrittää riville ladatun XML-mallitiedoston nimitilan (joka voi olla mikä tahansa).</span><span class="sxs-lookup"><span data-stu-id="e1c80-125">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5. <span data-ttu-id="e1c80-126">Valitse **Lataa malli** -toiminto ja valitse XML-mallitiedosto.</span><span class="sxs-lookup"><span data-stu-id="e1c80-126">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="e1c80-127">Kun tiedosto on ladattu, rivin muihin kenttiin lisätään tiedoston tiedot ja **Malli on ladattu** -valintaruutu valitaan.</span><span class="sxs-lookup"><span data-stu-id="e1c80-127">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e1c80-128">Ladatun XML-rakenteen puu on oletusarvoisesti tiivistettynä.</span><span class="sxs-lookup"><span data-stu-id="e1c80-128">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="e1c80-129">Solmun voi laajentaa **+**-painikkeella.</span><span class="sxs-lookup"><span data-stu-id="e1c80-129">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="e1c80-130">Kaikki solmut voi laajentaa käyttämällä **Laajenna kaikki** -painiketta valintanauhasta.</span><span class="sxs-lookup"><span data-stu-id="e1c80-130">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="e1c80-131">Solmujen valitseminen ja tyhjentäminen XML-rakenteessa</span><span class="sxs-lookup"><span data-stu-id="e1c80-131">To select or clear nodes in an XML schema</span></span>  

1. <span data-ttu-id="e1c80-132">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XML-mallin tarkastelutoiminto** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="e1c80-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2. <span data-ttu-id="e1c80-133">Täytä otsikon kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="e1c80-133">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="e1c80-134">Kenttä</span><span class="sxs-lookup"><span data-stu-id="e1c80-134">Field</span></span>|<span data-ttu-id="e1c80-135">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="e1c80-135">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="e1c80-136">**XML-mallin koodi**</span><span class="sxs-lookup"><span data-stu-id="e1c80-136">**XML Schema Code**</span></span>|<span data-ttu-id="e1c80-137">Määritä vaiheessa 5 ladattu XML-rakennetiedosto XML-rakennetiedosto -osiossa.</span><span class="sxs-lookup"><span data-stu-id="e1c80-137">Specify the XML schema file that you loaded in step 5 in the "To load an XML schema file" section.</span></span>|  
    |<span data-ttu-id="e1c80-138">**Uuden XMLportin numero**</span><span class="sxs-lookup"><span data-stu-id="e1c80-138">**New XMLport No.**</span></span>|<span data-ttu-id="e1c80-139">Määritä niiden XMLporttien määrä, jotka luodaan tästä XML-kaavasta, kun valitset **Luo XMLport** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="e1c80-139">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="e1c80-140">Rivit on nyt täytettä solmuilla, jotka edustavat kaikki XML-kaavan elementtejä.</span><span class="sxs-lookup"><span data-stu-id="e1c80-140">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="e1c80-141">XML-mallin mukaan pakolliset elementtien solmut valitaan oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="e1c80-141">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3. <span data-ttu-id="e1c80-142">Laajenna ensimmäisellä rivillä **Solmun nimi**-sarakkeessa **Asiakirja**-solmu ja laajenna sitten vähitellen alapuolella olevia solmuja, joita haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="e1c80-142">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="e1c80-143">Vaihtoehtoisesti, napsauta solmua hiiren kakkospainikkeella ja valitse sitten **Laajenna kaikki**.</span><span class="sxs-lookup"><span data-stu-id="e1c80-143">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4. <span data-ttu-id="e1c80-144">Valitse yksi seuraavista toiminnoista muuttaaksesi mitkä solmut näytetään.</span><span class="sxs-lookup"><span data-stu-id="e1c80-144">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="e1c80-145">**Toiminto**</span><span class="sxs-lookup"><span data-stu-id="e1c80-145">**Action**</span></span>|<span data-ttu-id="e1c80-146">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="e1c80-146">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="e1c80-147">**Näytä kaikki**</span><span class="sxs-lookup"><span data-stu-id="e1c80-147">**Show All**</span></span>|<span data-ttu-id="e1c80-148">Kaikki solmut ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="e1c80-148">All nodes are shown.</span></span>|  
    |<span data-ttu-id="e1c80-149">**Piilota ei-pakollinen**</span><span class="sxs-lookup"><span data-stu-id="e1c80-149">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="e1c80-150">Ainoastaan XML-rakenteen perusteella pakollisia elementtejä esittävät solmut näytetään.</span><span class="sxs-lookup"><span data-stu-id="e1c80-150">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="e1c80-151">Näiden solmujen merkintänä on yleensä **1** **MinOccurs**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e1c80-151">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="e1c80-152">Käännä näkymä valitsemalla **Näytä kaikki**.</span><span class="sxs-lookup"><span data-stu-id="e1c80-152">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="e1c80-153">**Piilota ei-valittu**</span><span class="sxs-lookup"><span data-stu-id="e1c80-153">**Hide Non-Selected**</span></span>|<span data-ttu-id="e1c80-154">Vain solmut, joissa **Valittu**-valintaruutu on valittuna näytetään.</span><span class="sxs-lookup"><span data-stu-id="e1c80-154">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="e1c80-155">Käännä näkymä valitsemalla **Näytä kaikki**.</span><span class="sxs-lookup"><span data-stu-id="e1c80-155">Choose **Show All** to reverse the view.</span></span>|  

5. <span data-ttu-id="e1c80-156">Valitse **Muokkaa** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e1c80-156">Choose the **Edit** action.</span></span>  

6. <span data-ttu-id="e1c80-157">Määritä **Valittu**-valintaruutu jokaiselle solmulle, jonka elementin haluat olevan tuettuna liittyvän SEPA-pankkitiedoston tiedonsiirtomäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="e1c80-157">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e1c80-158">Kun valitset pakollisen alisolmun, kaikki sen pääsolmut valitaan myös.</span><span class="sxs-lookup"><span data-stu-id="e1c80-158">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7. <span data-ttu-id="e1c80-159">Voit valita uudelleen kaikki solmut, jotka kuvaavat XML-mallin mukaan pakollisia elementtejä valitsemalla **Valitse kaikki pakolliset elementit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e1c80-159">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8. <span data-ttu-id="e1c80-160">Poista kaikki valinnat valitsemalla **Poista kaikkien valinta** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e1c80-160">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="e1c80-161">**Valinta**-kenttä määrittää, että solmulla on vähintään kaksi sisarussolmua, jotka toimivat vaihtoehtoina.</span><span class="sxs-lookup"><span data-stu-id="e1c80-161">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="e1c80-162">XML-rakenteeseen perustuvan tietojen vaihtamismäärityksen luominen</span><span class="sxs-lookup"><span data-stu-id="e1c80-162">To generate a data exchange definition that is based on an XML schema</span></span>  

1. <span data-ttu-id="e1c80-163">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XML-mallit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="e1c80-163">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2. <span data-ttu-id="e1c80-164">Valitse sopiva XML-malli ja valitse sitten **Avaa XML-mallin tarkastelutoiminto** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e1c80-164">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3. <span data-ttu-id="e1c80-165">Varmista, että tarvittavat solmut ovat valittuina.</span><span class="sxs-lookup"><span data-stu-id="e1c80-165">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="e1c80-166">Lisätietoja on kohdassa Solmujen valitseminen ja tyhjentäminen XML-rakenteessa.</span><span class="sxs-lookup"><span data-stu-id="e1c80-166">For more information, see the "To select or clear nodes in an XML schema" section.</span></span>  

4. <span data-ttu-id="e1c80-167">Valitse **XML-mallin tarkastelutoiminto** -sivulla **Luo tiedonsiirtomääritys** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e1c80-167">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="e1c80-168">Tiedonsiirtomääritys luodaan **Kirjauksen tiedonsiirtomääritykset** -sivulla, jossa sen voi viimeistellä määrittämällä, mitkä tiedoston elementit ja [!INCLUDE[prod_short](includes/prod_short.md)]in kentät yhdistetään toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="e1c80-168">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="e1c80-169">Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="e1c80-169">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="e1c80-170">Voit käyttää myös **Kirjauksen tiedonsiirtomääritykset** -sivun **Hae tiedostorakenne** -toimintoa. Tämä sivu täyttää **Sarakkeen määritykset** -pikavälilehden valmiiksi **XML-mallin tarkastelutoiminto** -sivun toiminnoilla.</span><span class="sxs-lookup"><span data-stu-id="e1c80-170">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

> [!NOTE]
> <span data-ttu-id="e1c80-171">Vuoden 2019 1. julkaisuaallossa ja sitä edeltävissä versioissa voitiin luoda rakenteeseen perustuva XMLport, joka sitten tuotiin ratkaisuun.</span><span class="sxs-lookup"><span data-stu-id="e1c80-171">In 2019 release wave 1 and earlier versions, you could generate an XMLport that was based on the schema and then import that into your solution.</span></span> <span data-ttu-id="e1c80-172">Tämä ei ole enää mahdollista.</span><span class="sxs-lookup"><span data-stu-id="e1c80-172">This is no longer supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1c80-173">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e1c80-173">See Also</span></span>

[<span data-ttu-id="e1c80-174">Tietojenvaihtomääritysten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e1c80-174">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="e1c80-175">Maksujen vienti pankkitiedostoon</span><span class="sxs-lookup"><span data-stu-id="e1c80-175">Export Payments to a Bank File</span></span>](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[<span data-ttu-id="e1c80-176">Maksujen kerääminen SEPA-suoraveloitusperintänä.</span><span class="sxs-lookup"><span data-stu-id="e1c80-176">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="e1c80-177">Tietoja tiedonvaihto-kehyksestä</span><span class="sxs-lookup"><span data-stu-id="e1c80-177">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]