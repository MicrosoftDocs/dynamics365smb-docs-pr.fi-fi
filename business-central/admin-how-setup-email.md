---
title: Business Central -sovelluksen sähköpostin määrittäminen | Microsoft Docs
description: Lisätietoja tavoista, joilla sähköpostiviestejä lähetetään ja vastaanotetaan Business Central -sovelluksessa SMTP-palvelimen kautta tai miten Office 365 -tilauksessa luotuja sähköpostipalvelimen asetuksia käytetään.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: b7f41e3630b818607dee18ad2b8afe6ba5daa3de
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245831"
---
# <a name="set-up-email-manually-or-using-the-assisted-setup"></a><span data-ttu-id="58b50-103">Sähköpostin määrittäminen manuaalisesti tai asetusten ohjatun määrityksen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="58b50-103">Set Up Email Manually or Using the Assisted Setup</span></span>
<span data-ttu-id="58b50-104">Jos haluat lähettää ja vastaanottaa sähköpostiviestejä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, **SMTP-sähköpostiasetukset**-sivun kentät on täytettävä.</span><span class="sxs-lookup"><span data-stu-id="58b50-104">To send and receive emails from within [!INCLUDE[d365fin](includes/d365fin_md.md)], you must fill in the fields on the **SMTP Mail Setup** page.</span></span>

> [!NOTE]  
>   <span data-ttu-id="58b50-105">Sen sijaan että kirjoittaisit SMTP-palvelimen tiedot, voit käyttää toimintoa, joka hakee nämä tiedot Office 365 -tilauksesta.</span><span class="sxs-lookup"><span data-stu-id="58b50-105">Instead of entering the SMTP server details, you can use a function to enter them with information from your Office 365 subscription.</span></span>

<span data-ttu-id="58b50-106">Voit määrittää sähköpostin joko manuaalisesti tai käyttää ohjattua **Sähköpostiasetukset**-määritystä.</span><span class="sxs-lookup"><span data-stu-id="58b50-106">You can either set email up manually or you can get help by using the **Email Setup** assisted setup guide.</span></span> <span data-ttu-id="58b50-107">Lisätietoja on ohjeaiheessa [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).</span><span class="sxs-lookup"><span data-stu-id="58b50-107">For more information, see [Getting Ready for Doing Business](ui-get-ready-business.md).</span></span>  

## <a name="to-set-up-email"></a><span data-ttu-id="58b50-108">Sähköpostin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="58b50-108">To set up email</span></span>
1. <span data-ttu-id="58b50-109">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **SMTP-sähköpostin asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="58b50-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="58b50-110">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="58b50-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="58b50-111">Vaihtoehtoisesti voit lisätä Office 365 -tilauksessa määritetyt tiedot valitsemalla **Käytä Office 365 Server -asetuksia** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="58b50-111">Alternatively, choose the **Apply Office 365 Server Settings** action to insert any information that is already defined for your Office 365 subscription.</span></span>
4. <span data-ttu-id="58b50-112">Kun kaikki kentät on täytetty oikein, valitse **Testisähköpostin asetukset** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="58b50-112">When all the fields are correctly filled in, choose the **Test Email Setup** action.</span></span>
5. <span data-ttu-id="58b50-113">Kun testi onnistuu, sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="58b50-113">When the test succeeds, close the page.</span></span>

## <a name="see-also"></a><span data-ttu-id="58b50-114">Katso myös</span><span class="sxs-lookup"><span data-stu-id="58b50-114">See Also</span></span>  
<span data-ttu-id="58b50-115">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="58b50-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="58b50-116">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="58b50-116">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="58b50-117">Asiakirjojen lähettäminen sähköpostitse</span><span class="sxs-lookup"><span data-stu-id="58b50-117">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="58b50-118">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="58b50-118">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="58b50-119">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen yrityssähköpostina Outlookissa](admin-outlook.md)</span><span class="sxs-lookup"><span data-stu-id="58b50-119">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as Your Business Inbox in Outlook](admin-outlook.md)</span></span>  
<span data-ttu-id="58b50-120">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in hakeminen mobiililaitteeseen](install-mobile-app.md)</span><span class="sxs-lookup"><span data-stu-id="58b50-120">[Getting [!INCLUDE[d365fin](includes/d365fin_md.md)] on My Mobile Device](install-mobile-app.md)</span></span>
