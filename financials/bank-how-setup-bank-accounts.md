---
title: "Pankkitilien määrittäminen| Microsoft Docs"
description: "Voit täsmäyttää pankkitilit Financialsissa pankin tiliotteiden avulla."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f46e95e24ef39a93bc93cfda1b9c575b07273566
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-bank-accounts"></a><span data-ttu-id="486ce-103">Toimittajan pankkitilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="486ce-103">How to: Set Up Bank Accounts</span></span>
<span data-ttu-id="486ce-104">[!INCLUDE[d365fin](includes/d365fin_md.md)] seuraa pankkitapahtumia pankkitilien avulla.</span><span class="sxs-lookup"><span data-stu-id="486ce-104">You use bank accounts in the [!INCLUDE[d365fin](includes/d365fin_md.md)] to keep track of your banking transactions.</span></span> <span data-ttu-id="486ce-105">Tilit voidaan määrittää käyttämään paikallista valuuttaa tai ulkomaan valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="486ce-105">Accounts can be denominated in your local currency or in a foreign currency.</span></span> <span data-ttu-id="486ce-106">Kun olet määrittänyt pankkitilit, voit myös käyttää Sekin tulostus -vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="486ce-106">After you have set up bank accounts, you can also use the check printing option.</span></span>

## <a name="to-set-up-bank-accounts"></a><span data-ttu-id="486ce-107">Pankkitilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="486ce-107">To set up bank accounts</span></span>
1. <span data-ttu-id="486ce-108">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Pankkitilit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="486ce-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="486ce-109">Valitse **Pankkitilit**-ikkunassa **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="486ce-109">In the **Bank Accounts** window, choose the **New** action.</span></span>
3. <span data-ttu-id="486ce-110">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="486ce-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a><span data-ttu-id="486ce-111">Pankkitilin määrittäminen pankkitiedostojen tuontia tai vientiä varten</span><span class="sxs-lookup"><span data-stu-id="486ce-111">To set up your bank account for import or export of bank files</span></span>
<span data-ttu-id="486ce-112">**Pankkitilin kortti** -ikkunan **Siirto**-pikavälilehden kentät liittyvät pankkisyötteiden ja -tiedostojen tuontiin ja vientiin.</span><span class="sxs-lookup"><span data-stu-id="486ce-112">Fields on the **Transfer** FastTab in the **Bank Account Card** window are related to import and export of bank feeds and files.</span></span> <span data-ttu-id="486ce-113">Lisätietoja on kohdassa [Toimintaohje: Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md) ja [Toimintaohje: Envestnet Yodlee -pankkisyötepalvelun määrittäminen](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="486ce-113">For more information, see [How to: Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) and [How to: Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

1. <span data-ttu-id="486ce-114">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Pankkitilit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="486ce-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="486ce-115">Avaa sen pankkitilin kortti, josta viet tai johon tuot pankkitiedostot.</span><span class="sxs-lookup"><span data-stu-id="486ce-115">Open the card for a bank account that you will export or import bank files for.</span></span>
3. <span data-ttu-id="486ce-116">Täytä **Siirto**-pikavälilehdessä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="486ce-116">On the **Transfer** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="486ce-117">Eri tiedostojen vientipalvelut ja niiden tiedostomuodot edellyttävät erilaisia asetuksia **Pankkitilin kortti** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="486ce-117">Different file export services and their formats require different setup values in the **Bank Account Card** window.</span></span> <span data-ttu-id="486ce-118">Saat ilmoituksen virheellisistä tai puuttuvista asetusarvoista, kun yrität viedä tiedoston.</span><span class="sxs-lookup"><span data-stu-id="486ce-118">You will be informed about wrong or missing setup values as you try to export the file.</span></span> <span data-ttu-id="486ce-119">Lue huolellisesti kenttien lyhyet kuvaukset tai katso lisätietoja liittyvien toimenpiteiden ohjeaiheista.</span><span class="sxs-lookup"><span data-stu-id="486ce-119">So read the short descriptions of the fields carefully or refer to the related procedure topics.</span></span> <span data-ttu-id="486ce-120">Esimerkiksi maksutiedoston vienti pohjoisamerikkalaiseen sähköiseen rahansiirtoon (EFT-toiminto) edellyttää, että sekä **Viimeinen maksuosoitusehdotusnumero**- että **Siirtonro**-kenttä on täytetty.</span><span class="sxs-lookup"><span data-stu-id="486ce-120">For example, exporting a payment file for North American electronic funds transfer (EFT) requires that both the **Last Remittance Advice No.** field and the **Transit No.** field are filled in.</span></span> <span data-ttu-id="486ce-121">Lisätietoja on kohdassa [Toimintaohje: Maksujen vieminen pankkitiedostoon](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="486ce-121">For more information, see [How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a><span data-ttu-id="486ce-122">Toimittajan pankkitilien määrittäminen pankkitiedostojen vientiä varten</span><span class="sxs-lookup"><span data-stu-id="486ce-122">To set up vendor bank accounts for export of bank files</span></span>
<span data-ttu-id="486ce-123">**Toimittajan pankkitilin kortti** -ikkunan **Siirto**-pikavälilehden kentät liittyvät pankkisyötteiden ja -tiedostojen vientiin.</span><span class="sxs-lookup"><span data-stu-id="486ce-123">Fields on the **Transfer** FastTab in the **Vendor Bank Account Card** window are related to export of bank feeds and files.</span></span> <span data-ttu-id="486ce-124">Lisätietoja on kohdassa [Toimintaohje: Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md) ja [Toimintaohje: Maksujen vienti pankkitiedostoon](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="486ce-124">For more information, see [How to: Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) and [How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

1. <span data-ttu-id="486ce-125">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Toimittajat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="486ce-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="486ce-126">Avaa sen toimittajan kortti, jonka pankkitiliin viet maksujen pankkitiedostot.</span><span class="sxs-lookup"><span data-stu-id="486ce-126">Open the card for a vendor whose bank account you will export payment bank files to.</span></span>
3. <span data-ttu-id="486ce-127">Valitse **Pankkitilit**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="486ce-127">Choose the **Bank Accounts** action.</span></span>
3. <span data-ttu-id="486ce-128">Täytä tarvittaessa **Toimittajan pankkitilin kortti** -ikkunan **Siirto**-pikavälilehden kentät.</span><span class="sxs-lookup"><span data-stu-id="486ce-128">In the **Vendor Bank Account Card** window, on the **Transfer** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="486ce-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="486ce-129">See Also</span></span>
[<span data-ttu-id="486ce-130">Pankkitoiminnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="486ce-130">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="486ce-131">Pankkitilien hallinta</span><span class="sxs-lookup"><span data-stu-id="486ce-131">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
<span data-ttu-id="486ce-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="486ce-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

