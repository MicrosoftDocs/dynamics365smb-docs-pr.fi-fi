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
ms.date: 09/14/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: a370002c08d8ef4cc46baa864f32b6ca2ef01b78
ms.contentlocale: fi-fi
ms.lasthandoff: 11/10/2017

---
# <a name="accountant-portal-for-dynamics-365-business-edition"></a><span data-ttu-id="f51a1-103">Dynamics 365 Business editionin kirjanpitäjän portaali</span><span class="sxs-lookup"><span data-stu-id="f51a1-103">Accountant Portal for Dynamics 365 Business edition</span></span>
<span data-ttu-id="f51a1-104">Tässä sovelluksessa on koontinäyttö, jossa on kirjanpitäjän jokaisen asiakasohjelman yhteenvetotiedot.</span><span class="sxs-lookup"><span data-stu-id="f51a1-104">This application provides a dashboard with summary data for each client of an accountant.</span></span> <span data-ttu-id="f51a1-105">Portaalissa on esillä taloushallinnon tunnuslukujen lisäksi myös suora linkki asiakasohjelman taloushallinnon sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="f51a1-105">The portal displays financial KPIs as well as a direct link to the client’s financial application.</span></span>  

<span data-ttu-id="f51a1-106">Koontinäyttö on erikoistunut roolikeskus, jonka kautta saa hyvän kokonaiskuvan asiakasohjelmista.</span><span class="sxs-lookup"><span data-stu-id="f51a1-106">The dashboard is a highly specialized Role Center for a better overview of your clients.</span></span>  
<span data-ttu-id="f51a1-107">[![Kirjanpitäjän portaali](./media/ui-extensions-accportal/accountant-portal.png)](https://go.microsoft.com/fwlink/?linkid=851257)</span><span class="sxs-lookup"><span data-stu-id="f51a1-107">[![Accountant Portal](./media/ui-extensions-accportal/accountant-portal.png)](https://go.microsoft.com/fwlink/?linkid=851257)</span></span>

<span data-ttu-id="f51a1-108">Kun laajennus asennetaan ensimmäisen kerran, pääset alkuun malliyrityksen avulla.</span><span class="sxs-lookup"><span data-stu-id="f51a1-108">When you first install the extension, a sample company helps you get started.</span></span> <span data-ttu-id="f51a1-109">Voit poistaa malliyrityksen koska tahansa.</span><span class="sxs-lookup"><span data-stu-id="f51a1-109">You can delete the sample company at any time.</span></span>  

## <a name="installing-the-extension"></a><span data-ttu-id="f51a1-110">Laajennuksen asentaminen</span><span class="sxs-lookup"><span data-stu-id="f51a1-110">Installing the Extension</span></span>
<span data-ttu-id="f51a1-111">Kun olet asentanut laajennuksen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, sinulta kysytään, haluatko käyttää sitä heti.</span><span class="sxs-lookup"><span data-stu-id="f51a1-111">When you install the extension in your [!INCLUDE[d365fin](includes/d365fin_md.md)], you will be asked if you want to use it now.</span></span> <span data-ttu-id="f51a1-112">Jos haluat aloittaa käytön heti, sinun on kirjauduttava ensin ulos ja sitten takaisin sisään, koska laajennus korvaa nykyisen roolikeskuksen ja lisää käyttöoikeudet käyttäjäprofiiliisi.</span><span class="sxs-lookup"><span data-stu-id="f51a1-112">If you do, then you must sign out and sign in again, because the extension replaces your current Role Center and adds permissions to your user profile.</span></span>  

<span data-ttu-id="f51a1-113">Lisätietoja on kohdassa [Dynamics 365 Business editionin kirjanpitäjän käyttökokemukset](finance-accounting.md).</span><span class="sxs-lookup"><span data-stu-id="f51a1-113">For more information, see [Accountant Experiences in Dynamics 365 Business edition ](finance-accounting.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f51a1-114">Laajennuksen nykyinen versio edellyttää, että asiakasohjelmassa on käytössä [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f51a1-114">The current version of the extension requires that your clients use [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="using-the-extension"></a><span data-ttu-id="f51a1-115">Laajennuksen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="f51a1-115">Using the extension</span></span>
<span data-ttu-id="f51a1-116">Laajennus poistetaan käytöstä muutaman kuukauden kuluttua.</span><span class="sxs-lookup"><span data-stu-id="f51a1-116">This extension will be deprecated in a few months.</span></span> <span data-ttu-id="f51a1-117">Tämän laajennuksen asentamista ei suositella. Rekisteröidy sen sijaan [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]iin [Financials for Accountants -sovelluksessa osoitteessa Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants).</span><span class="sxs-lookup"><span data-stu-id="f51a1-117">We recommend that you do not install this extension but sign up for [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] at [Financials for Accountants on Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants) instead.</span></span>

<span data-ttu-id="f51a1-118">Lisätietoja on kohdassa [Tervetuloa käyttämään ohjelmaa Dynamics 365 – Accountant Hub](/dynamics365/accountants/index.md).</span><span class="sxs-lookup"><span data-stu-id="f51a1-118">For more information, see [Welcome to Dynamics 365 — Accountant Hub](/dynamics365/accountants/index.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="f51a1-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f51a1-119">See Also</span></span>
[<span data-ttu-id="f51a1-120">Dynamics 365 Business editionin kirjanpitäjän käyttökokemukset</span><span class="sxs-lookup"><span data-stu-id="f51a1-120">Accountant Experiences in Dynamics 365 Business edition </span></span>](finance-accounting.md)  
[<span data-ttu-id="f51a1-121">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="f51a1-121">Finance</span></span>](finance.md)  

