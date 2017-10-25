---
title: "ALV-rekisteröintinumeroiden tarkistaminen | Microsoft Docs"
description: "EU:n web-palvelun avulla voit varmistaa, että ALV-rekisteröintinumerot, jotka syötät asiakas-, toimittaja- tai kontaktikortteihin, ovat voimassa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a><span data-ttu-id="9758c-103">Toimintaohje: ALV-rekisteröintinumeroiden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="9758c-103">How to: Verify VAT Registration Numbers</span></span>
<span data-ttu-id="9758c-104">EU:n verkkopalvelun avulla voit varmistaa, että asiakas-, toimittaja- tai kontaktikortteissa annettavat ALV-rekisteröintinumerot ovat voimassa.</span><span class="sxs-lookup"><span data-stu-id="9758c-104">You can use an EU web service to verify that VAT registration numbers that you enter on customer, vendor, or contact cards are valid.</span></span>  

 <span data-ttu-id="9758c-105">Kun muokkaat **ALV-rekisterinro**-kenttää kortissa, jonka **Maa-/aluekoodi**-kentän arvona on EU-maa tai -alue, uusi ALV-rekisteröintinumero ja käyttäjätunnuksesi kirjataan **ALV-rekisteröintiloki**-ikkunaan.</span><span class="sxs-lookup"><span data-stu-id="9758c-105">When you modify the **VAT Registration No.** field on a card where the value in the **Country/Region Code** field is an EU country/region, then the new VAT registration number and your user ID are logged in the **VAT Registration Log** window.</span></span> <span data-ttu-id="9758c-106">Voit tarkistaa ALV-numeron valitsemalla **Tarkista ALV-numero** -painikkeen **ALV-rekisteröintiloki**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="9758c-106">You verify a VAT registration number by choosing the **Verify Registration No.** button in the **VAT Registration Log** window.</span></span> <span data-ttu-id="9758c-107">Uusi rivi luodaan aina, kun käytät tarkistustoimintoa.</span><span class="sxs-lookup"><span data-stu-id="9758c-107">A new line is created every time you use the verification function.</span></span> <span data-ttu-id="9758c-108">Jos numero on voitu vahvistaa, **Tila**-kentän arvona on **Kelvollinen**.</span><span class="sxs-lookup"><span data-stu-id="9758c-108">If the number could be verified, the **Status** field contains **Valid**.</span></span> <span data-ttu-id="9758c-109">Jos numeroa ei voitu vahvistaa, **Tila**-kentän arvona on **Virheellinen** ja sinun on muutettava numeroa kortin **ALV-rekisteröintinumero**-kentässä sekä käynnistää vahvistaminen uudelleen.</span><span class="sxs-lookup"><span data-stu-id="9758c-109">If the number could not be verified, the **Status** field contains **Invalid**, and you must then change the number in the **VAT Registration No.** field on the card and start the verification function again.</span></span>  

 <span data-ttu-id="9758c-110">Oletusarvoisen web-palvelun URL-osoite on määritetty **ALV-numeron tarkistus-URL** -kenttään **Pääkirjanpidon asetukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="9758c-110">The URL of the default web service is set up in the **VAT Reg. No. Validation URL** field in the **General Ledger Setup** window.</span></span>  

 <span data-ttu-id="9758c-111">Voit muuttaa **ALV-rekisterinron muoto** -taulukossa kullekin maalle tai alueelle sellaiset ALV-rekisteröintinumeron muodot, jotka käyttäjä saa antaa **ALV-rekisterinro**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9758c-111">In the **VAT Registration No. Format** table, you can change for each country/region the different formats of VAT registration number that users are allowed to enter in the **VAT Registration No.** field.</span></span>  

> [!WARNING]  
>  <span data-ttu-id="9758c-112">Tämä web-palvelu käyttää http-protokollaa, mikä tarkoittaa sitä, että palvelun kautta siirretyt tiedot eivät ole salattuja.</span><span class="sxs-lookup"><span data-stu-id="9758c-112">This web service uses the http protocol, which means that data transferred through the service is not encrypted.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9758c-113">Tämä palvelu saattaa ajoittain olla poissa käytöstä, koska palvelu on osa EU:n laajaa kansallisten ALV-rekistereiden verkostoa. Microsoft ei ole vastuussa palvelun käytettävyydestä.</span><span class="sxs-lookup"><span data-stu-id="9758c-113">You may experience downtime for this service for which Microsoft is not responsible, as the service is part of a broad EU network of national VAT registers.</span></span>  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a><span data-ttu-id="9758c-114">ALV-rekisteröintinumeron tarkistaminen asiakaskortista</span><span class="sxs-lookup"><span data-stu-id="9758c-114">To verify a VAT registration number from a customer card</span></span>  
<span data-ttu-id="9758c-115">Seuraavaksi käsitellään asiakkaan ALV-rekisterinumeron tarkistaminen.</span><span class="sxs-lookup"><span data-stu-id="9758c-115">The following describes how to verify a VAT registration number for a customer.</span></span> <span data-ttu-id="9758c-116">Vaiheet ovat samankaltaisia toimittajalle ja kontaktille.</span><span class="sxs-lookup"><span data-stu-id="9758c-116">The steps are similar for a vendor and a contact.</span></span>   
1.  <span data-ttu-id="9758c-117">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakkaat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="9758c-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="9758c-118">Avaa sen asiakkaan kortti, jonka ALV-rekisteröintinumeron haluat tarkistaa.</span><span class="sxs-lookup"><span data-stu-id="9758c-118">Open the card of a customer where you want to verify the VAT registration number.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="9758c-119">Asiakaskortin **Maa-/aluekoodi**-kentässä on oltava EU-maa tai -alue.</span><span class="sxs-lookup"><span data-stu-id="9758c-119">The **Country/Region Code** field on the customer card must contain an EU country/region.</span></span>  
3.  <span data-ttu-id="9758c-120">Valitse **Laskutus**-pikavälilehdessä Siirtyminen-painike **ALV-rekisterinro** -kentän vierestä.</span><span class="sxs-lookup"><span data-stu-id="9758c-120">On the **Invoicing** FastTab, choose the DrillDown button next to the **VAT Registration No.** field.</span></span>  

    <span data-ttu-id="9758c-121">**ALV-rekisteröintiloki** -ikkuna avautuu näyttäen yhden rivin, jossa **Tila**-kentän arvona on **Tarkistamaton**.</span><span class="sxs-lookup"><span data-stu-id="9758c-121">The **VAT Registration Log** window opens showing one line where the **Status** field contains **Not Verified**.</span></span>  
4.  <span data-ttu-id="9758c-122">Valitse **Tarkista rekisterinro** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="9758c-122">Choose the **Verify Registration No.** action.</span></span>  

     <span data-ttu-id="9758c-123">Uusi rivi luodaan, kun **Tila**-kentän arvona on joko **kelvollinen** tai **virheellinen**.</span><span class="sxs-lookup"><span data-stu-id="9758c-123">A new line is created where the **Status** field contains either **Valid** or **Invalid**.</span></span>  
5.  <span data-ttu-id="9758c-124">Jos **Tila**-kentän arvona on **Virheellinen**, vaihda numero kortin **ALV-rekisterinro**-kentässä ja toista vaiheet 3 ja 4.</span><span class="sxs-lookup"><span data-stu-id="9758c-124">If the **Status** field contains **Invalid**, change the number in the **VAT Registration No.** field on the card, and then repeat steps 3 through 4.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9758c-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="9758c-125">See Also</span></span>  
[<span data-ttu-id="9758c-126">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="9758c-126">Finance</span></span>](finance.md)  
[<span data-ttu-id="9758c-127">Toimintaohje: Uusien asiakkaiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="9758c-127">How to: Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="9758c-128">Toimintaohje: Uusien toimittajien rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="9758c-128">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="9758c-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9758c-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

