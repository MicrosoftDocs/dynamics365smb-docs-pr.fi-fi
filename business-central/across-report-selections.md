---
title: Raporttien valinta Business Centralissa
description: Tietoja eri asiakirjatyyppien tulostamiseen tarvittavien raporttien määrittämisestä Business Centralissa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.date: 01/18/2021
ms.author: edupont
ms.openlocfilehash: 9d282ea35f7b4bdf317e818504f061d4145404bd
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378996"
---
# <a name="report-selection-in-business-central"></a><span data-ttu-id="6afa3-103">Raporttien valinta Business Centralissa</span><span class="sxs-lookup"><span data-stu-id="6afa3-103">Report Selection in Business Central</span></span>

<span data-ttu-id="6afa3-104">Voit määrittää oletusraportit, joita käytetään, kun tulostat myynnin ja ostojen asiakirjoja, kuten tilauksia, tarjouksia, laskuja ja hyvityslaskuja.</span><span class="sxs-lookup"><span data-stu-id="6afa3-104">You can set up default reports that will be used to print the various documents for sales and purchases, such as orders, quotes, invoices, and credit memos.</span></span> <span data-ttu-id="6afa3-105">Jos sinulla on esimerkiksi myyntilaskuissa tietty asettelu, voit määrittää raportin **Raporttivalinnat – myynti** -sivulla, jotta sitä käytetään myyntilaskujen lähettämiseen tai tulostamiseen.</span><span class="sxs-lookup"><span data-stu-id="6afa3-105">For example, if you have a specific layout for sales invoices, you can specify that report in the **Report Selections - Sales** page so that it will be used to send or print sales invoices.</span></span>  

<span data-ttu-id="6afa3-106">**Raporttivalinnat**-sivu määrittää, mikä raportti tulostetaan eri tilanteissa.</span><span class="sxs-lookup"><span data-stu-id="6afa3-106">The **Report Selections** pages specify which report will be printed in different situations.</span></span> <span data-ttu-id="6afa3-107">[!INCLUDE [prod_short](includes/prod_short.md)] sisältää oletuskokoonpanot, mutta tietysti voit muuttaa näitä oletusarvoja.</span><span class="sxs-lookup"><span data-stu-id="6afa3-107">[!INCLUDE [prod_short](includes/prod_short.md)] includes default configurations, but of course you can change these defaults.</span></span> <span data-ttu-id="6afa3-108">Voit myös lisätä raportteja **Raporttivalinnat**-sivuille, jos haluat että ohjelmassa on esimerkiksi enemmän kuin yksi raportti asiakirjatyyppiä kohden.</span><span class="sxs-lookup"><span data-stu-id="6afa3-108">You can also add reports to the **Report Selection** pages if you want to print more than one report per document type, for example.</span></span>  

## <a name="available-report-selections"></a><span data-ttu-id="6afa3-109">Käytettävissä olevat raporttivalinnat</span><span class="sxs-lookup"><span data-stu-id="6afa3-109">Available report selections</span></span>

<span data-ttu-id="6afa3-110">[!INCLUDE [prod_short](includes/prod_short.md)] sisältää eri **Raporttivalinta**-sivut eri alueille.</span><span class="sxs-lookup"><span data-stu-id="6afa3-110">[!INCLUDE [prod_short](includes/prod_short.md)] includes different **Report Selection** pages for different areas.</span></span> <span data-ttu-id="6afa3-111">Seuraavissa taulukoissa kuvataan, mistä voit löytää tietoa eri sivuista.</span><span class="sxs-lookup"><span data-stu-id="6afa3-111">The following tables describes where you can find information about the different pages.</span></span>  

|<span data-ttu-id="6afa3-112">Alue tai tehtävä</span><span class="sxs-lookup"><span data-stu-id="6afa3-112">Area or task</span></span>  |<span data-ttu-id="6afa3-113">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="6afa3-113">Learn more</span></span>|
|--------------|----------|
|<span data-ttu-id="6afa3-114">Esimerkki raporttivalinnan toiminnasta (myynti)</span><span class="sxs-lookup"><span data-stu-id="6afa3-114">Example of how report selection works (Sales)</span></span>|[<span data-ttu-id="6afa3-115">Myyntiasiakirjojen raporttivalinta</span><span class="sxs-lookup"><span data-stu-id="6afa3-115">Report selection for sales documents</span></span>](#example-report-selection-for-sales-documents)|
|<span data-ttu-id="6afa3-116">Myynti- ja ostoasiakirjojen sähköpostien oletusasettelu</span><span class="sxs-lookup"><span data-stu-id="6afa3-116">Default layout for emails with sales and purchase documents</span></span>  |[<span data-ttu-id="6afa3-117">Uudelleenkäytettävien sähköpostitekstien ja -asettelujen määrittäminen myynti- ja ostoasiakirjoille</span><span class="sxs-lookup"><span data-stu-id="6afa3-117">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|<span data-ttu-id="6afa3-118">Sekkien asetteluiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6afa3-118">Define check layouts</span></span>     |[<span data-ttu-id="6afa3-119">Sekin asettelun valitseminen</span><span class="sxs-lookup"><span data-stu-id="6afa3-119">Select a Check Layout</span></span>](finance-how-define-check-layouts.md) |
|<span data-ttu-id="6afa3-120">Raporttien määrittäminen ALV-raportointia varten (Saksa)</span><span class="sxs-lookup"><span data-stu-id="6afa3-120">Define reports for VAT reporting (Germany)</span></span>|[<span data-ttu-id="6afa3-121">ALV- ja Intrastat-raporttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6afa3-121">Set Up Reports for VAT and Intrastat</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> <span data-ttu-id="6afa3-122">[!INCLUDE [prod_short](includes/prod_short.md)] voi lisätä **Raporttivalinta**-sivuja esimerkiksi sijainnista ja toimialasta riippuen.</span><span class="sxs-lookup"><span data-stu-id="6afa3-122">Your [!INCLUDE [prod_short](includes/prod_short.md)] can include additional **Report Selection** pages, depending on your location and industry, for example.</span></span> <span data-ttu-id="6afa3-123">Voit aina tarkistaa asetukset valitsemalla ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -, kirjoittamalla **Raporttivalinnat** ja valitsemalla sitten liittyvän linkin.</span><span class="sxs-lookup"><span data-stu-id="6afa3-123">You can always check your setup by choosing the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, entering **Report Selections**, and then choose the relevant link.</span></span>

<span data-ttu-id="6afa3-124">[!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman oletusversio sisältää seuraavat **Raporttivalinta**-sivut:</span><span class="sxs-lookup"><span data-stu-id="6afa3-124">The default version of [!INCLUDE [prod_short](includes/prod_short.md)] includes the following **Report Section** pages:</span></span>

* <span data-ttu-id="6afa3-125">**Raporttivalinta - Myynti**</span><span class="sxs-lookup"><span data-stu-id="6afa3-125">**Report Selection - Sales**</span></span>  
* <span data-ttu-id="6afa3-126">**Raporttivalinta - Osto**</span><span class="sxs-lookup"><span data-stu-id="6afa3-126">**Report Selection - Purchase**</span></span>  
* <span data-ttu-id="6afa3-127">**Raporttivalinta - Varasto**</span><span class="sxs-lookup"><span data-stu-id="6afa3-127">**Report Selection - Inventory**</span></span>  
* <span data-ttu-id="6afa3-128">**Raporttivalinta - Kassavirta**</span><span class="sxs-lookup"><span data-stu-id="6afa3-128">**Report Selection - Cash Flow**</span></span>  
* <span data-ttu-id="6afa3-129">**Raporttivalinta - Fyysinen varasto**</span><span class="sxs-lookup"><span data-stu-id="6afa3-129">**Report Selection - Warehouse**</span></span>  
* <span data-ttu-id="6afa3-130">**Raporttivalinta - Pankkitili**</span><span class="sxs-lookup"><span data-stu-id="6afa3-130">**Report Selection - Bank Account**</span></span>  
* <span data-ttu-id="6afa3-131">**Raporttivalinta – Muistutus-/viivästyskulu**</span><span class="sxs-lookup"><span data-stu-id="6afa3-131">**Report Selections Reminder/Finance Charge**</span></span>  

## <a name="example-report-selection-for-sales-documents"></a><span data-ttu-id="6afa3-132">Esimerkki: Myyntiasiakirjojen raporttivalinta</span><span class="sxs-lookup"><span data-stu-id="6afa3-132">Example: Report selection for sales documents</span></span>

<span data-ttu-id="6afa3-133">**Raporttivalinta – Myynti** -sivu määrittää kullekin liittyvälle asiakirjatyypille eri skenaarioissa käytettävät oletusraportit.</span><span class="sxs-lookup"><span data-stu-id="6afa3-133">The **Report Selection - Sales** page defines the default reports to use in different scenarios for each related document type.</span></span> <span data-ttu-id="6afa3-134">Valitse asiakirjatyyppi **Käyttö**-kentässä ja lisää tai tarkista raportin valinta.</span><span class="sxs-lookup"><span data-stu-id="6afa3-134">Choose a document type in the **Usage** field, and then add or review the report selection.</span></span> <span data-ttu-id="6afa3-135">Voit määrittää useamman kuin yhden raportin sekä järjestyksen lajittelun, jossa raportit täytyy lähettää tai tulostaa.</span><span class="sxs-lookup"><span data-stu-id="6afa3-135">You can set up more than one report and the order of sequence that the reports must be sent or printed in.</span></span>  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="6afa3-136">Jotkin asiakirjatyypit voidaan lähettää sähköpostin liitteinä, toisia ei.</span><span class="sxs-lookup"><span data-stu-id="6afa3-136">Some types of document can be sent as email attachments, and others cannot.</span></span> <span data-ttu-id="6afa3-137">Jokaisessa **Raporttivalinta**-sivussa on lisäkenttiä, jos tyyppi tukee sähköpostilla lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="6afa3-137">Each **Report Selection** page shows additional fields if the type support email out of the box.</span></span>  

<span data-ttu-id="6afa3-138">Esimerkiksi **Raporttivalinta – Myynti** ja **Raporttivalinta – Osto** -sivuilla seuraavat kentät auttavat määrittämään sähköpostilla lähettämisen:</span><span class="sxs-lookup"><span data-stu-id="6afa3-138">For example, in the **Report Selection - Sales** and **Report Selection - Purchase** pages, the following fields help you set up emailing:</span></span>

|<span data-ttu-id="6afa3-139">Kentän nimi</span><span class="sxs-lookup"><span data-stu-id="6afa3-139">Field name</span></span> |<span data-ttu-id="6afa3-140">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="6afa3-140">Description</span></span>  |
|-----------|-------------|
|<span data-ttu-id="6afa3-141">**Käytä sähköpostin perustekstinä**</span><span class="sxs-lookup"><span data-stu-id="6afa3-141">**Use for Email Body**</span></span>| <span data-ttu-id="6afa3-142">Määrittää, että yhteenvetotiedot – esimerkiksi laskunumero, eräpäivä ja maksupalvelun linkki – lisätään lähetettävän sähköpostin perustekstiin.</span><span class="sxs-lookup"><span data-stu-id="6afa3-142">Specifies that summarized information, such as invoice number, due date, and payment service link, will be inserted in the body of the email that you send.</span></span>        |
|<span data-ttu-id="6afa3-143">**Käytä sähköpostin liitteenä**</span><span class="sxs-lookup"><span data-stu-id="6afa3-143">**Use for Email Attachment**</span></span>| <span data-ttu-id="6afa3-144">Määrittää, että liittyvä asiakirja liitetään sähköpostiin.</span><span class="sxs-lookup"><span data-stu-id="6afa3-144">Specifies that the related document will be attached to the email.</span></span>|
|<span data-ttu-id="6afa3-145">**Sähköpostin perustekstin asettelun kuvaus**</span><span class="sxs-lookup"><span data-stu-id="6afa3-145">**Email Body Layout Description**</span></span>|<span data-ttu-id="6afa3-146">Määrittää käytetyn sähköpostin perustekstin asettelun, yleensä mukautetun raporttiasettelun.</span><span class="sxs-lookup"><span data-stu-id="6afa3-146">Specifies the email body layout that is used, typically a custom report layout.</span></span> |

## <a name="see-also"></a><span data-ttu-id="6afa3-147">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6afa3-147">See also</span></span>

[<span data-ttu-id="6afa3-148">Uudelleenkäytettävien sähköpostitekstien ja -asettelujen määrittäminen myynti- ja ostoasiakirjoille</span><span class="sxs-lookup"><span data-stu-id="6afa3-148">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[<span data-ttu-id="6afa3-149">Sekin asettelun valitseminen</span><span class="sxs-lookup"><span data-stu-id="6afa3-149">Select a Check Layout</span></span>](finance-how-define-check-layouts.md)  
[<span data-ttu-id="6afa3-150">ALV- ja Intrastat-raporttien määrittäminen (Saksa)</span><span class="sxs-lookup"><span data-stu-id="6afa3-150">Set Up Reports for VAT and Intrastat (Germany)</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[<span data-ttu-id="6afa3-151">Raporttien ja asiakirjojen asettelujen hallinta</span><span class="sxs-lookup"><span data-stu-id="6afa3-151">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
[<span data-ttu-id="6afa3-152">Asiakirja-asettelujen määrittäminen asiakkaille ja toimittajille</span><span class="sxs-lookup"><span data-stu-id="6afa3-152">Define Document Layouts for Customers and Vendors</span></span>](ui-define-customer-vendor-document-layouts.md)  
[<span data-ttu-id="6afa3-153">Tulostimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6afa3-153">Set Up Printers</span></span>](ui-specify-printer-selection-reports.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]