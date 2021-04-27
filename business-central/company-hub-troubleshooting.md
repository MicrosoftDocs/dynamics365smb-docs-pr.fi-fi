---
title: Yrityksen keskittimen vianmääritys
description: Tietoja siitä, miten voit kiertää ongelmia käyttäessäsi Dynamics 365 Business Centralin yrityskeskusta useiden yritysten väliseen hallintaan.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: fc015058079e30b2db6989b246dc38498cd7a1f4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786510"
---
# <a name="troubleshooting-your-company-hub"></a><span data-ttu-id="e8805-103">Yrityksen keskittimen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="e8805-103">Troubleshooting Your Company Hub</span></span>

<span data-ttu-id="e8805-104">Yritysten lisääminen yrityksen keskittimeen on helppoa, mutta tässä artikkelissa käsitellään mahdollisesti esiin tulevia ongelmia.</span><span class="sxs-lookup"><span data-stu-id="e8805-104">Adding companies to the company hub dashboard is easy enough, but this article addresses issues that you may have on the way.</span></span>  

## <a name="check-errors"></a><span data-ttu-id="e8805-105">Tarkista virheet</span><span class="sxs-lookup"><span data-stu-id="e8805-105">Check errors</span></span>

<span data-ttu-id="e8805-106">Voit tarkastella viimeaikaisten virheiden luetteloa **Tarkista virheet** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="e8805-106">Use the **Check Errors** action to view a list of recent errors.</span></span> <span data-ttu-id="e8805-107">Voit nähdä kunkin virheen lisätiedot, ja voit siivota lokin poistamalla vanhoja tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="e8805-107">You can see additional details for each error, and you can clean up the log by deleting older entries.</span></span>  

## <a name="connection-failed"></a><span data-ttu-id="e8805-108">Yhteyden muodostus epäonnistui</span><span class="sxs-lookup"><span data-stu-id="e8805-108">Connection failed</span></span>

<span data-ttu-id="e8805-109">Voi olla muutamia syitä siihen, miksi et pysty muodostamaan yhteyttä yritykseen, mukaan lukien seuraavat:</span><span class="sxs-lookup"><span data-stu-id="e8805-109">There can be a couple of reasons why you cannot connect to a company, including the following:</span></span>

- <span data-ttu-id="e8805-110">**Ympäristölinkki**-kentässä annettu URL-osoite ei kelpaa</span><span class="sxs-lookup"><span data-stu-id="e8805-110">The URL in the **Environment Link** field is not valid</span></span>  

  <span data-ttu-id="e8805-111">Siirry **ympäristölinkit** -sivulle, avaa ympäristö, johon et voi muodostaa yhteyttä, ja valitse sitten **Testaa yhteyden muodostus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e8805-111">Go to the **Environment Links** page, open the environment that you cannot connect to, and then choose the **Test the connection** action.</span></span>  
- <span data-ttu-id="e8805-112">Asiakkaan yritys on offline-tilassa esimerkiksi päivityksen vuoksi</span><span class="sxs-lookup"><span data-stu-id="e8805-112">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="e8805-113">Valitse koontinäytössä ensin **Työkalut**-valikkovaihtoehto ja sitten **Tarkista virheet**.</span><span class="sxs-lookup"><span data-stu-id="e8805-113">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="e8805-114">Jos avautuvassa teknisten tietojen luettelossa näkyy virheitä, järjestelmänvalvojaan on ehkä syytä ottaa yhteyttä.</span><span class="sxs-lookup"><span data-stu-id="e8805-114">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="e8805-115">Jos virhesanoma esimerkiksi ilmoittaa, että *Palvelin on hylännyt asiakkaan tunnistetiedot*, syynä on todennäköisesti puuttuvat käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="e8805-115">For example, the error message "*The server has rejected the client credentials*" suggests that you do not have access.</span></span>  
- <span data-ttu-id="e8805-116">Sinulla ei ole oikeuksia kaikkiin yrityksiin ympäristössä, johon yrität muodostaa yhteyttä</span><span class="sxs-lookup"><span data-stu-id="e8805-116">You do not have access to all companies in the environment that you are trying to connect to</span></span>

  <span data-ttu-id="e8805-117">[!INCLUDE [prod_short](includes/prod_short.md)]:ssa organisaatiossa voi olla monta liiketoimintayksikköä, joita kutsutaan yrityksiksi, ja sinulla ei ehkä ole käyttöoikeuksia kaikkiin yrityksiin.</span><span class="sxs-lookup"><span data-stu-id="e8805-117">In [!INCLUDE [prod_short](includes/prod_short.md)], an organization can have multiple business units called companies, and you might not have access to all companies.</span></span> <span data-ttu-id="e8805-118">Varmista yhdessä järjestelmänvalvojan tai asiakkaan kanssa, että sinulla on kaikkien niiden yritysten käyttöoikeudet, joita haluat käsitellä.</span><span class="sxs-lookup"><span data-stu-id="e8805-118">Work with your administrator or client to make sure that you have access to the companies that you have to work in.</span></span>  

## <a name="data-does-not-refresh"></a><span data-ttu-id="e8805-119">Tietoja ei päivitetä</span><span class="sxs-lookup"><span data-stu-id="e8805-119">Data does not refresh</span></span>

<span data-ttu-id="e8805-120">Kun lisäät yrityksen tai pyydät tietojen päivittämistä, [!INCLUDE [prod_short](includes/prod_short.md)] noutaa tiedot.</span><span class="sxs-lookup"><span data-stu-id="e8805-120">When you add a company or request a refresh of the data, [!INCLUDE [prod_short](includes/prod_short.md)] fetches the data.</span></span> <span data-ttu-id="e8805-121">Sinun on kuitenkin päivitettävä sivu itse valitsemalla esimerkiksi **Lataa kaikki yritykset uudelleen** -toiminnon, päivittämällä selaimen sivu tai poistumalla koontinäytöstä ja palaamalla siihen takaisin.</span><span class="sxs-lookup"><span data-stu-id="e8805-121">But you must refresh the page yourself, such as choosing the **Reload all companies** action, refresh the browser page, navigate away from the dashboard and then back again, or similar.</span></span>  

<span data-ttu-id="e8805-122">Jos olet lisännyt yrityksen, mutta se ei näy luettelossa, voit päivittää luettelon myös **Lataa kaikki yritykset uudelleen** -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="e8805-122">If you've added a company but it is not displaying in the list, you can also use the **Reload all companies** action to update the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8805-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e8805-123">See also</span></span>

[<span data-ttu-id="e8805-124">Työnhallinta useiden yritysten välillä yrityksen keskittimessä</span><span class="sxs-lookup"><span data-stu-id="e8805-124">Manage Work across Multiple Companies in the Company Hub</span></span>](company-hub.md)  
[<span data-ttu-id="e8805-125">Yritysten lisääminen yrityksen keskittimeen</span><span class="sxs-lookup"><span data-stu-id="e8805-125">Add companies to your company hub</span></span>](company-hub-add-company.md)  
[<span data-ttu-id="e8805-126">Kirjanpitäjän käyttökokemukset Business Centralissa</span><span class="sxs-lookup"><span data-stu-id="e8805-126">Accountant Experiences in Business Central</span></span>](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]