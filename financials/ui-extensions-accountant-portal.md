---
title: "Kirjanpitäjän portaalin käyttäminen | Microsoft Docs"
description: "Sisältää tietoja Kirjanpitäjän portaali -laajennuksesta."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, accountant
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 84b2331f14b8c7e8d73921189e2df33fa709626e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="accountant-portal-for-dynamics-365-for-financials"></a><span data-ttu-id="bacc1-103">Dynamics 365 for Financialsin kirjanpitäjän portaali</span><span class="sxs-lookup"><span data-stu-id="bacc1-103">Accountant Portal for Dynamics 365 for Financials</span></span>
<span data-ttu-id="bacc1-104">Tässä sovelluksessa on koontinäyttö, jossa on kirjanpitäjän jokaisen asiakasohjelman yhteenvetotiedot.</span><span class="sxs-lookup"><span data-stu-id="bacc1-104">This application provides a dashboard with summary data for each client of an accountant.</span></span> <span data-ttu-id="bacc1-105">Portaalissa on esillä taloushallinnon tunnuslukujen lisäksi myös suora linkki asiakasohjelman taloushallinnon sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="bacc1-105">The portal displays financial KPIs as well as a direct link to the client’s financial application.</span></span>  

<span data-ttu-id="bacc1-106">Koontinäyttö on erikoistunut roolikeskus, jonka kautta saa hyvän kokonaiskuvan asiakasohjelmista.</span><span class="sxs-lookup"><span data-stu-id="bacc1-106">The dashboard is a highly specialized Role Center for a better overview of your clients.</span></span>  
<span data-ttu-id="bacc1-107">[![Kirjanpitäjän portaali](./media/ui-extensions-accportal/accountant-portal.png)](https://go.microsoft.com/fwlink/?linkid=851257)</span><span class="sxs-lookup"><span data-stu-id="bacc1-107">[![Accountant Portal](./media/ui-extensions-accportal/accountant-portal.png)](https://go.microsoft.com/fwlink/?linkid=851257)</span></span>

<span data-ttu-id="bacc1-108">Kun laajennus asennetaan ensimmäisen kerran, pääset alkuun malliyrityksen avulla.</span><span class="sxs-lookup"><span data-stu-id="bacc1-108">When you first install the extension, a sample company helps you get started.</span></span> <span data-ttu-id="bacc1-109">Voit poistaa malliyrityksen koska tahansa.</span><span class="sxs-lookup"><span data-stu-id="bacc1-109">You can delete the sample company at any time.</span></span>  

## <a name="installing-the-extension"></a><span data-ttu-id="bacc1-110">Laajennuksen asentaminen</span><span class="sxs-lookup"><span data-stu-id="bacc1-110">Installing the Extension</span></span>
<span data-ttu-id="bacc1-111">Kun olet asentanut laajennuksen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, sinulta kysytään, haluatko käyttää sitä heti.</span><span class="sxs-lookup"><span data-stu-id="bacc1-111">When you install the extension in your [!INCLUDE[d365fin](includes/d365fin_md.md)], you will be asked if you want to use it now.</span></span> <span data-ttu-id="bacc1-112">Jos haluat aloittaa käytön heti, sinun on kirjauduttava ensin ulos ja sitten takaisin sisään, koska laajennus korvaa nykyisen roolikeskuksen ja lisää käyttöoikeudet käyttäjäprofiiliisi.</span><span class="sxs-lookup"><span data-stu-id="bacc1-112">If you do, then you must sign out and sign in again, because the extension replaces your current Role Center and adds permissions to your user profile.</span></span>  

<span data-ttu-id="bacc1-113">Lisätietoja on ohjeaiheessa [Dynamics 365 for Financialsin kirjanpitäjän käyttökokemukset](finance-accounting.md).</span><span class="sxs-lookup"><span data-stu-id="bacc1-113">For more information, see [Accountant Experiences in Dynamics 365 for Financials](finance-accounting.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="bacc1-114">Laajennuksen nykyinen versio edellyttää, että asiakasohjelmassa on käytössä [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bacc1-114">The current version of the extension requires that your clients use [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="using-the-extension"></a><span data-ttu-id="bacc1-115">Laajennuksen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="bacc1-115">Using the extension</span></span>
<span data-ttu-id="bacc1-116">Laajennusta käytetään, kun kirjaudut [Financials for Accountantsiin Microsoft.comissa](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants). Jos asennat laajennuksen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, se korvaa nykyisen roolikeskuksesi.</span><span class="sxs-lookup"><span data-stu-id="bacc1-116">This extension is used when you sign up at [Financials for Accountants on Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants). If you install the extension in your [!INCLUDE[d365fin](includes/d365fin_md.md)], it will replace your current Role Center.</span></span> <span data-ttu-id="bacc1-117">Jos haluat sitten palata toiseen roolikeskukseen, voit tehdä sen omissa asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="bacc1-117">If you then want to return to the other Role Center, then you can do that in My Settings.</span></span> <span data-ttu-id="bacc1-118">Lisätietoja on kohdassa [Toimintaohje: Roolikeskuksen vaihtaminen](change-role.md).</span><span class="sxs-lookup"><span data-stu-id="bacc1-118">For more information, see [How to: Change the Role Center](change-role.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="bacc1-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="bacc1-119">See Also</span></span>
[<span data-ttu-id="bacc1-120">Dynamics 365 for Financialsin kirjanpitäjän käyttökokemukset</span><span class="sxs-lookup"><span data-stu-id="bacc1-120">Accountant Experiences in Dynamics 365 for Financials</span></span>](finance-accounting.md)  
[<span data-ttu-id="bacc1-121">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="bacc1-121">Finance</span></span>](finance.md)  

