---
title: "SEPA-hyvityksen siirron määrittäminen | Microsoft Docs"
description: "Lisätietoja SEPA-hyvityksen siirron määrittämisestä Finance and Operations, Business editionissa."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sepa, credit, transfer, payment,
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 66f24ea238eed97ffe7f76f3c979cc2843875860
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-sepa-credit-transfer"></a><span data-ttu-id="0b175-103">SEPA-hyvityksen siirron määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0b175-103">Set Up SEPA Credit Transfer</span></span>
<span data-ttu-id="0b175-104">Voit viedä maksuja **Maksupäiväkirja**-ikkunasta tiedostoon siirrettäväksi verkkopankkiisi liittyvien tilisiirtojen käsittelemiseksi.</span><span class="sxs-lookup"><span data-stu-id="0b175-104">From the **Payment Journal** window, you can export payments to a file for upload to your electronic bank for processing of the related money transfers.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="0b175-105"> tukee SEPA-hyvitysten siirtomuotoa, mutta maa- tai aluekohtaisesti voi olla käytettävissä muita sähköisiä maksumuotoja.</span><span class="sxs-lookup"><span data-stu-id="0b175-105"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>  

<span data-ttu-id="0b175-106">Jos haluat ottaa käyttöön sellaisten pankkitiedostomuotojen viennin, joita [!INCLUDE[d365fin](includes/d365fin_md.md)] ei tue suoraan, voit määrittää tiedonsiirtomäärityksen tiedonsiirtokehyksen avulla.</span><span class="sxs-lookup"><span data-stu-id="0b175-106">To enable export of a bank file formats that are not supported out of the box in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can set up a data exchange definition by using the data exchange framework.</span></span> <span data-ttu-id="0b175-107">Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="0b175-107">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

<span data-ttu-id="0b175-108">Ennen kuin voit käsitellä maksun sähköisesti viemällä maksutiedostot SEPA-hyvityksen siirto -muodossa, sinun on suoritettava seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="0b175-108">Before you can process payment electronically by exporting payment files in the SEPA Credit Transfer format, you must perform the following setup steps:</span></span>  

* <span data-ttu-id="0b175-109">Määritä kyseinen pankkitilin käsittelemään SEPA-hyvityksen siirtomuoto</span><span class="sxs-lookup"><span data-stu-id="0b175-109">Set up the bank account in question to handle the SEPA Credit Transfer format</span></span>  
* <span data-ttu-id="0b175-110">Määritä toimittajan kortit, jotta voit käsitellä maksut viemällä tiedostot SEPA-hyvityksen siirtomuotoon</span><span class="sxs-lookup"><span data-stu-id="0b175-110">Set up vendor cards to process payments by exporting files in the SEPA Credit Transfer format</span></span>  
* <span data-ttu-id="0b175-111">Määritä liittyvä yleisen päiväkirja erä ottamaan käyttöön maksujen vienti **Maksupäiväkirja**-ikkunasta</span><span class="sxs-lookup"><span data-stu-id="0b175-111">Set up the related general journal batch to enable payment export from the **Payment Journal** window</span></span>  
* <span data-ttu-id="0b175-112">Yhdistä vähintään yhden maksutyypin tiedonsiirtomääritys liittyvään maksutapaan</span><span class="sxs-lookup"><span data-stu-id="0b175-112">Connect the data exchange definition for one or more payment types with the relevant payment method or methods</span></span>  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a><span data-ttu-id="0b175-113">Pankkitilin määrittäminen SEPA-hyvityksen siirtoa varten</span><span class="sxs-lookup"><span data-stu-id="0b175-113">To set up a bank account for SEPA Credit Transfer</span></span>  
1. <span data-ttu-id="0b175-114">Syötä **Etsi**-ruudussa **Pankkitilit** ja valitse sitten vastaava linkki.</span><span class="sxs-lookup"><span data-stu-id="0b175-114">In the **Search** box, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0b175-115">Avaa sen pankkitilin kortti, josta viet maksutiedostot SEPA-hyvitys siirtomuodossa.</span><span class="sxs-lookup"><span data-stu-id="0b175-115">Open the card of the bank account from which you will export payment files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="0b175-116">Valitse **Siirto**-välilehden **Maksun vientimuoto** -kentässä **SEPADD**.</span><span class="sxs-lookup"><span data-stu-id="0b175-116">On the **Transfer** FastTab, in the **Payment Export Format** field, choose **SEPADD**.</span></span>  
4. <span data-ttu-id="0b175-117">Valitse **SEPA CT -viestitunnus nrosarja** -kentässä numerosarjat, joista numerot määritetään SEPA-hyvityksen siirtotapahtumille.</span><span class="sxs-lookup"><span data-stu-id="0b175-117">In the **SEPA CT Msg. ID No. Series** field, choose a number series from which numbers are assigned to SEPA credit transfer entries.</span></span>  
5. <span data-ttu-id="0b175-118">Varmista, että **IBAN**-kenttä on täytetty.</span><span class="sxs-lookup"><span data-stu-id="0b175-118">Make sure the **IBAN** field is filled.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="0b175-119">**Valuuttakoodi**-kentän asetuksena on oltava **EUR**, koska SEPA-hyvityksen siirrot voidaan tehdä vain euroina.</span><span class="sxs-lookup"><span data-stu-id="0b175-119">The **Currency Code** field must be set to **EUR**, because SEPA credit transfers can only be made in the EURO currency.</span></span>  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a><span data-ttu-id="0b175-120">Toimittajan kortin määrittäminen SEPA-hyvityksen siirtoa varten</span><span class="sxs-lookup"><span data-stu-id="0b175-120">To set up a vendor card for SEPA Credit Transfer</span></span>  
1. <span data-ttu-id="0b175-121">Syötä **Etsi**-ruudussa **Toimittajat** ja valitse sitten vastaava linkki.</span><span class="sxs-lookup"><span data-stu-id="0b175-121">In the **Search** box, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0b175-122">Avaa sen toimittajan kortti, josta maksat sähköisesti viemällä maksutiedostot SEPA-hyvitys siirtomuodossa.</span><span class="sxs-lookup"><span data-stu-id="0b175-122">Open the card of the vendor whom you will pay electronically by export payment files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="0b175-123">Valitse **Maksu**-pikavälilehden **Maksutavan koodi** -kentässä **PANKKI**.</span><span class="sxs-lookup"><span data-stu-id="0b175-123">On the **Payment** FastTab, in the **Payment Method Code** field, choose **BANK**.</span></span>  
4. <span data-ttu-id="0b175-124">Valitse **Ensisijainen pankkitili** -kentässä pankki, johon rahat siirretään, kun ne käsitellään verkkopankissasi.</span><span class="sxs-lookup"><span data-stu-id="0b175-124">In the **Preferred Bank Account** field, choose the bank to which the money will be transferred when it is processed by your electronic bank.</span></span>  

     <span data-ttu-id="0b175-125">**Ensisijainen pankkitili** -kentän arvo kopioidaan **Maksupäiväkirja**-ikkunan **Vastaanottajan pankkitili** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b175-125">The value in the **Preferred Bank Account** field is copied to the **Recipient Bank Account** field in the **Payment Journal** window.</span></span>  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a><span data-ttu-id="0b175-126">Maksupäiväkirjan määrittäminen maksutiedostojen vientiä varten</span><span class="sxs-lookup"><span data-stu-id="0b175-126">To set the payment journal up to export payment files</span></span>  
1. <span data-ttu-id="0b175-127">Syötä **Etsi**-ruudussa **Maksupäiväkirjat** ja valitse sitten vastaava linkki.</span><span class="sxs-lookup"><span data-stu-id="0b175-127">In the **Search** box, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0b175-128">Avaa maksupäiväkirja, jota käytät maksujen käsittelyyn viemällä tiedostot SEPA-hyvitys siirtomuodossa.</span><span class="sxs-lookup"><span data-stu-id="0b175-128">Open the payment journal that you use to process payments by exporting files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="0b175-129">Valitse **Erän nimi** -kentässä avattava luettelon painike.</span><span class="sxs-lookup"><span data-stu-id="0b175-129">In the **Batch Name** field, choose the drop\-down button.</span></span>  
4. <span data-ttu-id="0b175-130">Valitse **Yleisen päiväkirjan erät** -ikkunan **Kotisivun**-välilehden **Hallinta**-ryhmässä **Muokkaa luetteloa**.</span><span class="sxs-lookup"><span data-stu-id="0b175-130">In the **General Journal Batches** window, on the **Home** tab, in the **Manage** group, choose **Edit List**.</span></span>  
5. <span data-ttu-id="0b175-131">Valitse sen maksupäiväkirjan rivillä, jonka avulla viet maksut, **Salli maksun vienti** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="0b175-131">On the line for the payment journal that you will use to export payments, select the **Allow Payment Export** check box.</span></span>  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a><span data-ttu-id="0b175-132">Vähintään yhden maksutyypin tiedonsiirtomäärityksen yhdistäminen liittyvään maksutapaan</span><span class="sxs-lookup"><span data-stu-id="0b175-132">To connect the data exchange definition for one or more payment types with the relevant payment method or methods</span></span>  
1. <span data-ttu-id="0b175-133">Syötä **Etsi**-ruudussa **Maksutavat** ja valitse sitten vastaava linkki.</span><span class="sxs-lookup"><span data-stu-id="0b175-133">In the **Search** box, enter **Payment Methods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0b175-134">Valitse **Maksutavat** -ikkunassa ensin maksutapa, jolla maksut viedään, ja sitten **Maksun vientirivin määritys** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="0b175-134">In the **Payment Methods** window, select the payment method that is used to export payments from, and then choose the **Pmt. Export Line Definition** field.</span></span>  
3. <span data-ttu-id="0b175-135">Valitse **Maksun vientirivin määritykset** -ikkunassa koodi, jonka määritit **Rivimääritykset**-pikavälilehden **Koodi**-kentässä ohjeaiheen [Tiedonsiirtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md) kohdan Tiedoston rivien ja sarakkeiden muotoilun kuvaaminen vaiheessa 4.</span><span class="sxs-lookup"><span data-stu-id="0b175-135">In the **Pmt. Export Line Definitions** window, select the code that you specified in the **Code** field on the **Line Definitions** FastTab in step 4 in the “To describe the formatting of lines and columns in the file” section in the [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) procedure.</span></span>  

    <span data-ttu-id="0b175-136">Suoraveloitusvaltakirja lisätään automaattisesti **Suoraveloitusvaltakirjan tunnus** -kenttään, kun luot myyntilaskun vaiheessa 2 valitulle asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="0b175-136">The direct-debit mandate is automatically inserted in the **Direct Debit Mandate ID** field when you create a sales invoice for the customer that you selected in step 2.</span></span> <span data-ttu-id="0b175-137">Lisätietoja on kohdassa [Toistuvien myynti- ja ostorivien luominen](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="0b175-137">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="0b175-138">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0b175-138">See Also</span></span>  
[<span data-ttu-id="0b175-139">Maksujen kerääminen SEPA-suoraveloitusperintänä</span><span class="sxs-lookup"><span data-stu-id="0b175-139">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="0b175-140">Tietojenvaihtomääritysten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0b175-140">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="0b175-141">Toistuvien myynti- ja ostorivien luominen</span><span class="sxs-lookup"><span data-stu-id="0b175-141">Create Recurring Sales and Purchase Lines</span></span>](sales-how-work-standard-lines.md)  
[<span data-ttu-id="0b175-142">Sähköinen tiedonsiirto</span><span class="sxs-lookup"><span data-stu-id="0b175-142">Exchanging Data Electronically</span></span>](across-data-exchange.md)  

