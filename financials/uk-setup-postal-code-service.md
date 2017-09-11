---
title: "Toimintaohje: Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen | Microsoft Docs"
description: "Ohjeaiheessa kerrotaan yleisistä toiminnoista, joilla käsittelet tietoja Financialsissa. Kyse voi olla esimerkiksi arvojen antamisesta, tietojen lajittelusta ja näkymien vaihtamisesta."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="0a6c8-103">Toimintaohje: Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0a6c8-103">How to: Set Up the GetAddress.io UK Postcodes Extension</span></span>
<span data-ttu-id="0a6c8-104">Laajennuksen avulla on helppo antaa isobritannialaisten objektien, kuten asiakkaiden, kontaktien, työntekijöiden, toimittajien ja pankkitilien, osoitteita.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-104">This extension makes it easy to enter addresses in the UK for entities like customers, contacts, employees, vendors, bank accounts, and so on.</span></span> 

<span data-ttu-id="0a6c8-105">Ison-Britannian GetAddress.io-laajennus etsii isobritannialaisia postinumeroita getAddress-ohjelmistorajapinnan avulla.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-105">The GetAddress.io UK Postcodes extension uses the getAddress API to find addresses in postcodes in the UK.</span></span> <span data-ttu-id="0a6c8-106">Jos haluat käyttää laajennusta, tarvitset tilauksen ja getAddress-ohjelmistorajapinnan API-avaimen.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-106">To use the extension, you need to get a plan and an API Key for the getAddress API.</span></span> <span data-ttu-id="0a6c8-107">Niiden saaminen on helppoa ja autamme sinua niiden hankkimisessa, kun määrität Ison-Britannian postiosoitteiden GetAddress.io-laajennuksen.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-107">That's easy, and we help you do that when you set up the GetAddress.io UK Postcodes extension.</span></span> <span data-ttu-id="0a6c8-108">Tilaukset perustuvat käyttöön tai kutsuihin, niin kuin niihin joskus viitataan.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-108">Plans are based on use, or what's sometimes referred to as calls.</span></span> <span data-ttu-id="0a6c8-109">Kutsu tapahtuu tässä tapauksessa, kun [!INCLUDE[d365fin](includes/d365fin_md.md)] näyttää postinumeron osoitteiden luettelon.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-109">A call, in this case, is when [!INCLUDE[d365fin](includes/d365fin_md.md)] displays a list of addresses in a postcode.</span></span> <span data-ttu-id="0a6c8-110">Valitse tarpeitasi parhaiten vastaava tilaus sen mukaan, kuinka usein lisäät osoitteita.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-110">Depending on how often you add addresses, choose the plan that is best for you.</span></span> <span data-ttu-id="0a6c8-111">Jos valitsit sivulla vain **Hae API-avain** -kohdan, käytät **maksutonta** tilausta, joka sallii 20 osoitteen lisäämisen päivässä ja joka on voimassa 30 päivää.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-111">If you just choose **Get API Key** in the page, you'll use the **Free** plan, which lets you add 20 addresses per day, and is valid for 30 days.</span></span> 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="0a6c8-112">Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0a6c8-112">To set up the GetAddress.io UK Postcodes extension</span></span> 
1. <span data-ttu-id="0a6c8-113">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Palvelun yhteydet** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Connections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0a6c8-114">Valitse **Palvelun yhteydet** -ikkunassa **Ison-Britannian postinumeropalvelu**.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-114">In the **Service Connections** window, choose **UK Postcode Service**.</span></span>
3. <span data-ttu-id="0a6c8-115">Valitse **Postinumeropalvelun määritys** -sivulla **Poistettu käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-115">In the **Postcode provider configuration** page, choose **Disabled**.</span></span>
4. <span data-ttu-id="0a6c8-116">Valitse **Postinumeropalvelun valinta** -ikkunassa **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-116">In the **Postal code service selection** window, choose **GetAddress.io**.</span></span>
5. <span data-ttu-id="0a6c8-117">Valitse **GetAddress.io-määritys**-ikkunassa **Hae API-avain**, joka avaa **Tilaukset**-sivun getAddress-ohjelmointirajapinnan sivustossa.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-117">In the **GetAddress.io Config** window, choose **Get API Key** to open the **Plans** page on the website for the getAddress API.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="0a6c8-118">Ponnahdusikkunoiden avaaminen on ehkä sallittava selaimessa.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-118">You might need to allow pop-ups in your browser.</span></span>
6. <span data-ttu-id="0a6c8-119">Osta tilaus tai valitse pelkkä **Hae API-avain** ja anna sähköpostiosoitteesi.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-119">Purchase a plan, or just choose **Get API Key**, and then provide your email address.</span></span>
7. <span data-ttu-id="0a6c8-120">Avaa getAddress.io-sähköposti ja kopioi API-avain.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-120">Open the email from getAddress.io, and copy the API key.</span></span> <span data-ttu-id="0a6c8-121">Avain on **API-avaimesi**-otsikon alla.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-121">The key is under the **Your API Key** heading.</span></span>
8. <span data-ttu-id="0a6c8-122">Liitä API-avain **GetAddress.io-määritys**-ikkunassa **API-avain**-kenttään ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-122">In the **GetAddress.io Config** window, paste the API key in the **API Key** field, and then choose **OK**.</span></span>
9. <span data-ttu-id="0a6c8-123">Tarkista **Palvelun yhteydet** -sivulla, että **Osoitepalvelu**-kentässä on **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-123">In the **Service Connections** page, verify that the **Address Provider** field shows **GetAddress.io**.</span></span> <span data-ttu-id="0a6c8-124">Jos osoite on kentässä, palvelu on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="0a6c8-124">If it does, the service is enabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a6c8-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0a6c8-125">See Also</span></span>
<span data-ttu-id="0a6c8-126">[Ison-Britannian postinumeroiden GetAddress.io](ui-extensions-getaddressio.md)
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="0a6c8-126">[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="0a6c8-127">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0a6c8-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
