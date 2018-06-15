---
title: "Asiakkaiden hakeminen Dynamics 365 -kirjanpitäjäkokemukseen | Microsoft Docs"
description: "Lisätietoja nykyisten asiakkaiden lisäämisestä Dynamics 365:n Accountant Hubiin."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 8b8d92e114733d87b1866d66ee3111208e233ad3
ms.contentlocale: fi-fi
ms.lasthandoff: 05/15/2018

---
# <a name="add-clients-to-your-dashboard-in-include-d365acclongincludesd365acclongmdmd"></a><span data-ttu-id="597bb-103">Asiakkaiden lisääminen [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]in koontinäyttöön</span><span class="sxs-lookup"><span data-stu-id="597bb-103">Add Clients to Your Dashboard in [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]</span></span>
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

<span data-ttu-id="597bb-104">Voit lisätä asiakkaan **Asiakkaat**-ikkunassa, jonka voit avata valitsemalla **Hallitse asiakkaita** -toiminnon valintanauhassa.</span><span class="sxs-lookup"><span data-stu-id="597bb-104">You can add a client by using the **Clients** window, which you can open by choosing the **Manage Clients** action in the ribbon.</span></span> <span data-ttu-id="597bb-105">Valitse vain **Uusi** ja täytä sitten tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="597bb-105">Simply choose **New** and then fill in the fields.</span></span>  

![Asiakkaan lisääminen](./media/accountant-add-client/manage-client.png)

<span data-ttu-id="597bb-107">Kunkin asiakaskortin tiedot määrität sinä itse, ja voit myös muuttaa niitä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="597bb-107">The data in the card for each client is specified by you, and you can change it as needed.</span></span> <span data-ttu-id="597bb-108">**Asiakkaan URL-osoite** -kenttä on kuitenkin erityisen tärkeä – sitä tarvitaan asiakkaan [!INCLUDE [d365fin](includes/d365fin_md.md)]iin pääsyyn.</span><span class="sxs-lookup"><span data-stu-id="597bb-108">However, the **Client URL** field is critical - this is how you can access each client's [!INCLUDE [d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="597bb-109">Tarkista, että linkki on oikein valintanauhan **Testaa asiakkaan URL-osoite** -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="597bb-109">Use the **Test Client URL** action in the ribbon to test that you entered the right link.</span></span> <span data-ttu-id="597bb-110">URL-osoite, joka sinun täytyy syöttää, osoittaa asiakkaan [!INCLUDE [d365fin](includes/d365fin_md.md)] -sovellukseen, kuten *<https://mybusiness.financials.dynamics.com>*.</span><span class="sxs-lookup"><span data-stu-id="597bb-110">The URL that you must enter points at the client's [!INCLUDE [d365fin](includes/d365fin_md.md)], such as *<https://mybusiness.financials.dynamics.com>*.</span></span> <span data-ttu-id="597bb-111">Tätä URL-osoitetta käytetään, kun valitset **Siirry yritykseen** -valikkovaihtoehdon [!INCLUDE [d365acc](includes/d365acc_md.md)] -koontinäytössä.</span><span class="sxs-lookup"><span data-stu-id="597bb-111">This URL is then used when you choose the **Go To Company** menu item in the [!INCLUDE [d365acc](includes/d365acc_md.md)] dashboard.</span></span>  

### <a name="get-invited-to-a-clients-include-d365finlongincludesd365finlongmdmd"></a><span data-ttu-id="597bb-112">Kutsun saaminen asiakkaan [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)] -ympäristöön</span><span class="sxs-lookup"><span data-stu-id="597bb-112">Get Invited to a Client's [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)]</span></span>
<span data-ttu-id="597bb-113">[!INCLUDE [d365fin](includes/d365fin_md.md)]ia käyttävä yritys voi kutsua sinut [!INCLUDE [d365fin](includes/d365fin_md.md)] -ympäristöönsä ulkoiseksi kirjanpitäjäksi.</span><span class="sxs-lookup"><span data-stu-id="597bb-113">A company who use [!INCLUDE [d365fin](includes/d365fin_md.md)] can invite you to [!INCLUDE [d365fin](includes/d365fin_md.md)] as their external accountant.</span></span> <span data-ttu-id="597bb-114">Kutsun saaminen edellyttää [!INCLUDE [d365acc](includes/d365acc_md.md)]issa käytettävän sähköpostiosoitteen, kuten <em>me@accountant.com</em>, antamista. Asiakkaan järjestelmänvalvoja voi sitten lisätä sinut järjestelmään ohjatulla **Kutsu ulkoinen kirjanpitäjä** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="597bb-114">To get invited, you must give them the email that you use with [!INCLUDE [d365acc](includes/d365acc_md.md)], such as <em>me@accountant.com</em>. Your client's administrator can then add you to their system by running the **Invite External Accountant** wizard.</span></span>  

<span data-ttu-id="597bb-115">Saat nyt asiakkaalta sähköpostiviestin, jossa on linkit asiakkaan [!INCLUDE [d365fin](includes/d365fin_md.md)]:een.</span><span class="sxs-lookup"><span data-stu-id="597bb-115">As a result, you will receive email from your client with links to their [!INCLUDE [d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="597bb-116">Ensimmäinen linkki on kutsu, jolla saa yrityksen käyttöoikeuden. Avaa linkki ja hyväksy vaiheet, joilla sinut lisätään asiakkaan [!INCLUDE [d365fin](includes/d365fin_md.md)]:een.</span><span class="sxs-lookup"><span data-stu-id="597bb-116">The first link is an invitation to get access to their company - open the link and accept the steps that adds you to your client's [!INCLUDE [d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="597bb-117">Toisen linkin avulla kyseinen asiakas lisätään [!INCLUDE [d365acc](includes/d365acc_md.md)]in koontinäyttöön edellä kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="597bb-117">The second link is for adding this client to your dashboard in [!INCLUDE [d365acc](includes/d365acc_md.md)] as described above.</span></span>  

<span data-ttu-id="597bb-118">Hyväksymällä kutsun kirjaudut sisään ja saat asiakkaan taloustietojen käyttöoikeuden **Kirjanpitäjä**-roolikeskuksesta.</span><span class="sxs-lookup"><span data-stu-id="597bb-118">When you have accepted the invitation, you are logged in and can access the client's financial data from the **Accountant** Role Center.</span></span> <span data-ttu-id="597bb-119">Lisätietoja on kohdassa [Kirjanpitäjän käyttökokemukset [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).</span><span class="sxs-lookup"><span data-stu-id="597bb-119">For more information, see [Accountant Experiences in [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).</span></span>  

## <a name="see-also"></a><span data-ttu-id="597bb-120">Katso myös</span><span class="sxs-lookup"><span data-stu-id="597bb-120">See Also</span></span>
<span data-ttu-id="597bb-121">[[!INCLUDE[d365acc](includes/d365acc_md.md)]in käytön aloittaminen](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="597bb-121">[Get Started with [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span></span>  
<span data-ttu-id="597bb-122">[[!INCLUDE[d365acc](includes/d365acc_md.md)]in vianmääritys](troubleshooting.md)</span><span class="sxs-lookup"><span data-stu-id="597bb-122">[Troubleshooting [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)</span></span>  

