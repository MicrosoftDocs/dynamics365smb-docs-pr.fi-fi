---
title: XML-malleihin perustuvien XMLports-kohteiden luominen | Microsoft Docs
description: "Voit määrittää tiedonsiirtokehyksen XML-mallien avulla."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 5b10eaff0d412ee26ead2137a353054c41d05113
ms.contentlocale: fi-fi
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="b7b38-103">Toimintaohje: XML-rakenteiden käyttäminen Tietojen vaihdon määritysten valmistelussa</span><span class="sxs-lookup"><span data-stu-id="b7b38-103">How to: Use XML Schemas to Prepare Data Exchange Definitions</span></span>
<span data-ttu-id="b7b38-104">Voit ottaa XML-tiedostojen tietojen tuonnin ja viennin käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]in tiedonsiirtokehyksessä määrittämällä [!INCLUDE[d365fin](includes/d365fin_md.md)]in kanssa vaihdettavat tietoelementit XML-mallien avulla.</span><span class="sxs-lookup"><span data-stu-id="b7b38-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="b7b38-105">Se tehdään **XML-mallin tarkastelutoiminto** -ikkunassa lataamalla XML-rakennetiedosto, valitsemalla sopivat tietoelementit ja käynnistämällä joko tietojen vaihdon määritys tai XMLport.</span><span class="sxs-lookup"><span data-stu-id="b7b38-105">You perform this work in the **XML Schema Viewer** window by loading the XML schema file, selecting the relevant data elements, and then initializing either a data exchange definition or an XMLport.</span></span>  

 <span data-ttu-id="b7b38-106">Kun olet määrittänyt XML-mallin perusteella sisällytettävät tietoelementit, voit luoda XMLport-objektin **Luo XMLport** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="b7b38-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate XMLport** action to create the XMLport object.</span></span>  

 <span data-ttu-id="b7b38-107">Voit myös käyttää **Luo tietojen vaihdon määritys** -toimintoa luodaksesi valittuihin tietoelementteihin perustuvan määrityksen, jonka sitten viimeistelet tietojen vaihtamiskehyksessä.</span><span class="sxs-lookup"><span data-stu-id="b7b38-107">Alternatively, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="b7b38-108">Tällä tavoin **Kirjauksen tiedonsiirtomääritykset** -ikkunassa luodaan tietue. Jatka ikkunassa määrittämällä, mitkä tiedoston elementit ja mitkä [!INCLUDE[d365fin](includes/d365fin_md.md)]in kentät yhdistetään toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="b7b38-108">This creates a record in the **Posting Exchange Definition** window where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="b7b38-109">Lisätietoja on kohdassa [Toimintaohje: Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="b7b38-109">For more information, see [How to: Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="b7b38-110">Tämä ohjeaihe sisältää seuraavat menettelyt:</span><span class="sxs-lookup"><span data-stu-id="b7b38-110">This topic contains the following procedures:</span></span>  

-   <span data-ttu-id="b7b38-111">XML-rakennetiedoston lataaminen</span><span class="sxs-lookup"><span data-stu-id="b7b38-111">To load an XML schema file</span></span>  

-   <span data-ttu-id="b7b38-112">Solmujen valitseminen ja tyhjentäminen XML-rakenteessa</span><span class="sxs-lookup"><span data-stu-id="b7b38-112">To select or clear nodes in an XML schema</span></span>  

-   <span data-ttu-id="b7b38-113">XML-rakenteeseen perustuvan tietojen vaihtamismäärityksen luominen</span><span class="sxs-lookup"><span data-stu-id="b7b38-113">To generate a data exchange definition that is based on an XML schema</span></span>  

-   <span data-ttu-id="b7b38-114">XML-rakenteeseen perustuvan XMLportin luominen</span><span class="sxs-lookup"><span data-stu-id="b7b38-114">To generate an XMLport for the file that is based on an XML schema</span></span>  

-   <span data-ttu-id="b7b38-115">XMLportin tuominen Objektien suunnittelu -sovellukseen</span><span class="sxs-lookup"><span data-stu-id="b7b38-115">To import an XMLport into the Object Designer</span></span>  

### <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="b7b38-116">XML-rakennetiedoston lataaminen</span><span class="sxs-lookup"><span data-stu-id="b7b38-116">To load an XML schema file</span></span>  

1.  <span data-ttu-id="b7b38-117">Varmista, että sopiva XML-rakennetiedosto on saatavilla.</span><span class="sxs-lookup"><span data-stu-id="b7b38-117">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="b7b38-118">Tiedostotunniste on .xsd.</span><span class="sxs-lookup"><span data-stu-id="b7b38-118">The file extension is .xsd.</span></span>  

2.  <span data-ttu-id="b7b38-119">Anna **Etsi**-ruudussa **XML-mallit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b7b38-119">In the **Search** box, enter **XML Schemas**, and then choose the related link.</span></span>  

3.  <span data-ttu-id="b7b38-120">Valitse **Kotisivu**-välilehden **Uusi**-ryhmässä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b7b38-120">On the **Home** tab, in the **New** group, choose **New**.</span></span>  

4.  <span data-ttu-id="b7b38-121">Täytä kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="b7b38-121">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="b7b38-122">Kenttä</span><span class="sxs-lookup"><span data-stu-id="b7b38-122">Field</span></span>|<span data-ttu-id="b7b38-123">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="b7b38-123">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="b7b38-124">**Koodi**</span><span class="sxs-lookup"><span data-stu-id="b7b38-124">**Code**</span></span>|<span data-ttu-id="b7b38-125">Määritä koodi, jolla identifioit XML-kaavan.</span><span class="sxs-lookup"><span data-stu-id="b7b38-125">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="b7b38-126">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="b7b38-126">**Description**</span></span>|<span data-ttu-id="b7b38-127">Määritä XML-kaavan kuvaus.</span><span class="sxs-lookup"><span data-stu-id="b7b38-127">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="b7b38-128">**Kohdenimitila**-kenttä määrittää riville ladatun XML-mallitiedoston nimitilan (joka voi olla mikä tahansa).</span><span class="sxs-lookup"><span data-stu-id="b7b38-128">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5.  <span data-ttu-id="b7b38-129">Valitse **Kotisivu**-välilehden **Käsittely**-ryhmässä **Lataa malli** ja valitse sitten XML-mallin tiedosto.</span><span class="sxs-lookup"><span data-stu-id="b7b38-129">On the **Home** tab, in the **Process** group, choose **Load Schema**, and then select the XML schema file.</span></span>  

     <span data-ttu-id="b7b38-130">Kun tiedosto on ladattu, rivin muihin kenttiin lisätään tiedoston tiedot ja **Malli on ladattu** -valintaruutu valitaan.</span><span class="sxs-lookup"><span data-stu-id="b7b38-130">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="b7b38-131">Ladatun XML-rakenteen puu on oletusarvoisesti tiivistettynä.</span><span class="sxs-lookup"><span data-stu-id="b7b38-131">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="b7b38-132">Solmun voi laajentaa **+**-painikkeella.</span><span class="sxs-lookup"><span data-stu-id="b7b38-132">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="b7b38-133">Kaikki solmut voi laajentaa käyttämällä **Laajenna kaikki** -painiketta valintanauhasta.</span><span class="sxs-lookup"><span data-stu-id="b7b38-133">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="b7b38-134">Solmujen valitseminen ja tyhjentäminen XML-rakenteessa</span><span class="sxs-lookup"><span data-stu-id="b7b38-134">To select or clear nodes in an XML schema</span></span>  

1.  <span data-ttu-id="b7b38-135">Anna **Etsi**-ruudussa **XML-mallin tarkastelutoiminto** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b7b38-135">In the **Search** box, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="b7b38-136">Täytä otsikon kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="b7b38-136">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="b7b38-137">Kenttä</span><span class="sxs-lookup"><span data-stu-id="b7b38-137">Field</span></span>|<span data-ttu-id="b7b38-138">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="b7b38-138">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="b7b38-139">**XML-mallin koodi**</span><span class="sxs-lookup"><span data-stu-id="b7b38-139">**XML Schema Code**</span></span>|<span data-ttu-id="b7b38-140">Määritä vaiheessa 5 lataamasi XML-rakennetiedosto "XML-rakenteen lataaminen" -osiossa.</span><span class="sxs-lookup"><span data-stu-id="b7b38-140">Specify the XML schema file that you loaded in step 5 in the “To load an XML schema file” section.</span></span>|  
    |<span data-ttu-id="b7b38-141">**Uuden XMLportin numero**</span><span class="sxs-lookup"><span data-stu-id="b7b38-141">**New XMLport No.**</span></span>|<span data-ttu-id="b7b38-142">Määritä sen XMLporttien määrä, joka luodaan tästä XML-kaavasta, kun valitset **Luo XMLport** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="b7b38-142">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="b7b38-143">Rivit on nyt täytettä solmuilla, jotka edustavat kaikki XML-kaavan elementtejä.</span><span class="sxs-lookup"><span data-stu-id="b7b38-143">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="b7b38-144">XML-mallin mukaan pakolliset elementtien solmut valitaan oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="b7b38-144">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3.  <span data-ttu-id="b7b38-145">Laajenna ensimmäisellä rivillä **Solmun nimi**-sarakkeessa **Asiakirja**-solmu ja laajenna sitten vähitellen alapuolella olevia solmuja, joita haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="b7b38-145">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="b7b38-146">Vaihtoehtoisesti, napsauta solmua hiiren kakkospainikkeella ja valitse sitten **Laajenna kaikki**.</span><span class="sxs-lookup"><span data-stu-id="b7b38-146">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4.  <span data-ttu-id="b7b38-147">Valitse **Kotisivu**-välilehden **Näytä**-ryhmässä yksi seuraavista toiminnoista muuttaaksesi mitkä solmut näytetään.</span><span class="sxs-lookup"><span data-stu-id="b7b38-147">On the **Home** tab, in the **View** group, choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="b7b38-148">**Toiminto**</span><span class="sxs-lookup"><span data-stu-id="b7b38-148">**Action**</span></span>|<span data-ttu-id="b7b38-149">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="b7b38-149">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="b7b38-150">**Näytä kaikki**</span><span class="sxs-lookup"><span data-stu-id="b7b38-150">**Show All**</span></span>|<span data-ttu-id="b7b38-151">Kaikki solmut ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="b7b38-151">All nodes are shown.</span></span>|  
    |<span data-ttu-id="b7b38-152">**Piilota ei-pakollinen**</span><span class="sxs-lookup"><span data-stu-id="b7b38-152">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="b7b38-153">Ainoastaan XML-rakenteen perusteella pakollisia elementtejä esittävät solmut näytetään.</span><span class="sxs-lookup"><span data-stu-id="b7b38-153">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="b7b38-154">Näiden solmujen merkintänä on yleensä **1** **MinOccurs**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b7b38-154">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="b7b38-155">Käännä näkymä valitsemalla **Näytä kaikki**.</span><span class="sxs-lookup"><span data-stu-id="b7b38-155">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="b7b38-156">**Piilota ei-valittu**</span><span class="sxs-lookup"><span data-stu-id="b7b38-156">**Hide Non-Selected**</span></span>|<span data-ttu-id="b7b38-157">Vain solmut, joissa **Valittu**-valintaruutu on valittuna näytetään.</span><span class="sxs-lookup"><span data-stu-id="b7b38-157">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="b7b38-158">Käännä näkymä valitsemalla **Näytä kaikki**.</span><span class="sxs-lookup"><span data-stu-id="b7b38-158">Choose **Show All** to reverse the view.</span></span>|  

5.  <span data-ttu-id="b7b38-159">Valitse **Kotisivu**-välilehden **Hallinta**-ryhmässä **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="b7b38-159">On the **Home** tab, in the **Manage** group, choose **Edit**.</span></span>  

6.  <span data-ttu-id="b7b38-160">Määritä **Valittu**-valintaruutu jokaiselle solmulle, jonka elementin haluat olevan tuettuna liittyvän SEPA-pankkitiedoston tiedonsiirtomäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="b7b38-160">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="b7b38-161">Kun valitset pakollisen alisolmun, kaikki sen pääsolmut valitaan myös.</span><span class="sxs-lookup"><span data-stu-id="b7b38-161">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7.  <span data-ttu-id="b7b38-162">Voit valita uudelleen kaikki solmut, jotka kuvaavat XML-mallin mukaan pakollisia elementtejä valitsemalla **Valitse kaikki pakolliset elementit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="b7b38-162">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8.  <span data-ttu-id="b7b38-163">Poista kaikki valinnat valitsemalla **Poista kaikkien valinta** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="b7b38-163">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="b7b38-164">**Valinta**-kenttä määrittää, että solmulla on vähintään kaksi sisarussolmua, jotka toimivat vaihtoehtoina.</span><span class="sxs-lookup"><span data-stu-id="b7b38-164">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="b7b38-165">XML-rakenteeseen perustuvan tietojen vaihtamismäärityksen luominen</span><span class="sxs-lookup"><span data-stu-id="b7b38-165">To generate a data exchange definition that is based on an XML schema</span></span>  

1.  <span data-ttu-id="b7b38-166">Anna **Etsi**-ruudussa **XML-mallit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b7b38-166">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="b7b38-167">Valitse oikea XML-rakenne ja sitten **Koti**-välilehden **Prosessi**-ryhmästä **Avaa XML-rakenteen tarkastelu**.</span><span class="sxs-lookup"><span data-stu-id="b7b38-167">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="b7b38-168">Varmista, että tarvittavat solmut ovat valittuina.</span><span class="sxs-lookup"><span data-stu-id="b7b38-168">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="b7b38-169">Lisätietoja on ohjeen kohdassa "Solmujen valitseminen ja tyhjentäminen XML-rakenteessa".</span><span class="sxs-lookup"><span data-stu-id="b7b38-169">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

4.  <span data-ttu-id="b7b38-170">Valitse **XML-mallin tarkastelutoiminto** -ikkunan **Kotisivu**-välilehden **Käsittely**-ryhmässä **Luo tiedonsiirtomääritys**.</span><span class="sxs-lookup"><span data-stu-id="b7b38-170">In the **XML Schema Viewer** window, on the **Home** tab, in the **Process** group, choose **Generate Data Exchange Definition**.</span></span>  

 <span data-ttu-id="b7b38-171">Tiedonsiirtomääritys luodaan **Kirjauksen tiedonsiirtomääritykset** -ikkunassa, jossa sen voi viimeistellä määrittämällä, mitkä tiedoston elementit ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in kentät yhdistetään toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="b7b38-171">A data exchange definition is created in the **Posting Exchange Definition** window, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="b7b38-172">Lisätietoja on kohdassa [Toimintaohje: Tiedonsiirtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="b7b38-172">For more information, see [How to: Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b7b38-173">Voit käyttää myös **Kirjauksen tiedonsiirtomääritykset** -ikkunan **Hae tiedostorakenne** -toimintoa. Tämä ikkuna täyttää **Sarakkeen määritykset** -pikavälilehden valmiiksi **XML-mallin tarkastelutoiminto** -ikkunan toiminnoilla.</span><span class="sxs-lookup"><span data-stu-id="b7b38-173">You can also use the **Get File Structure** function from the **Posting Exchange Definition** window, which uses the functionality of the **XML Schema Viewer** window to prefill the **Column Definitions** TastTab.</span></span>  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a><span data-ttu-id="b7b38-174">XML-rakenteeseen perustuvan XMLportin luominen</span><span class="sxs-lookup"><span data-stu-id="b7b38-174">To generate an XMLport that is based on an XML schema</span></span>  

1.  <span data-ttu-id="b7b38-175">Anna **Etsi**-ruudussa **XML-mallit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b7b38-175">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="b7b38-176">Valitse soveltuva XML-rakenne ja sitten **Kotisivun**-välilehden **Käsittely**-ryhmässä **Avaa XML-mallin tarkastelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="b7b38-176">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="b7b38-177">Määritä **Uuden XMLportin numero**</span><span class="sxs-lookup"><span data-stu-id="b7b38-177">In the **New XMLport No.**</span></span> <span data-ttu-id="b7b38-178">-kentässä numero, joka annetaan uudelle XMLport-objektille luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="b7b38-178">field, specify the number that the new XMLport object will be given when it is generated.</span></span>  

4.  <span data-ttu-id="b7b38-179">Varmista, että tarvittavat solmut ovat valittuina.</span><span class="sxs-lookup"><span data-stu-id="b7b38-179">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="b7b38-180">Lisätietoja on ohjeen kohdassa "Solmujen valitseminen ja tyhjentäminen XML-rakenteessa".</span><span class="sxs-lookup"><span data-stu-id="b7b38-180">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

5.  <span data-ttu-id="b7b38-181">Valitse **Kotisivu**-välilehdellä **Käsittely**-ryhmässä **Luo XMLport** ja tallenna objekti sitten .txt-tiedostona oikeaan paikkaan.</span><span class="sxs-lookup"><span data-stu-id="b7b38-181">On the **Home** tab, in the **Process** group, choose **Generate XMLport**, and then save the object as a .txt file in an appropriate location.</span></span>  

6. <span data-ttu-id="b7b38-182">Tuo uusi XMLport [!INCLUDE[d365fin](includes/d365fin_md.md)]in kehitysympäristöön ja käännä se.</span><span class="sxs-lookup"><span data-stu-id="b7b38-182">Import the new XMLport into the [!INCLUDE[d365fin](includes/d365fin_md.md)] development environment and compile it.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7b38-183">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b7b38-183">See Also</span></span>  
<span data-ttu-id="b7b38-184">[Toimintaohje: Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md) </span><span class="sxs-lookup"><span data-stu-id="b7b38-184">[How to: Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) </span></span>  
<span data-ttu-id="b7b38-185">[Kuinka maksut viedään pankkitiedostoon](payables-how-export-payments-bank-file.md) </span><span class="sxs-lookup"><span data-stu-id="b7b38-185">[How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md) </span></span>  
<span data-ttu-id="b7b38-186">[Maksujen kerääminen SEPA-suoraveloituksena](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="b7b38-186">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
[<span data-ttu-id="b7b38-187">Tietoja tiedonsiirtokehyksestä</span><span class="sxs-lookup"><span data-stu-id="b7b38-187">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)

