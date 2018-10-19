---
title: "Kirjanpitäjän portaalin käyttäminen | Microsoft Docs"
description: "Sisältää tietoja Kirjanpitäjän portaali -laajennuksesta."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, accountant
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 26b911718a9741cd070af131aef3d258fd85e1eb
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="the-accountant-portal-for-business-central-extension"></a><span data-ttu-id="2b35b-103">Business Central -laajennuksen kirjanpitäjän portaali</span><span class="sxs-lookup"><span data-stu-id="2b35b-103">The Accountant Portal for Business Central Extension</span></span>
<span data-ttu-id="2b35b-104">Tässä sovelluksessa on koontinäyttö, jossa on kirjanpitäjän jokaisen asiakasohjelman yhteenvetotiedot.</span><span class="sxs-lookup"><span data-stu-id="2b35b-104">This application provides a dashboard with summary data for each client of an accountant.</span></span> <span data-ttu-id="2b35b-105">Portaalissa on esillä taloushallinnon tunnuslukujen lisäksi myös suora linkki asiakasohjelman taloushallinnon sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="2b35b-105">The portal displays financial KPIs as well as a direct link to the client’s financial application.</span></span>  

<span data-ttu-id="2b35b-106">Koontinäyttö on erikoistunut roolikeskus, jonka kautta saa hyvän kokonaiskuvan asiakasohjelmista.</span><span class="sxs-lookup"><span data-stu-id="2b35b-106">The dashboard is a highly specialized Role Center for a better overview of your clients.</span></span>  
<span data-ttu-id="2b35b-107">[![Kirjanpitäjän portaali](./media/ui-extensions-accportal/accountant-portal.png)](https://go.microsoft.com/fwlink/?linkid=851257)</span><span class="sxs-lookup"><span data-stu-id="2b35b-107">[![Accountant Portal](./media/ui-extensions-accportal/accountant-portal.png)](https://go.microsoft.com/fwlink/?linkid=851257)</span></span>

<span data-ttu-id="2b35b-108">Kun laajennus asennetaan ensimmäisen kerran, pääset alkuun malliyrityksen avulla.</span><span class="sxs-lookup"><span data-stu-id="2b35b-108">When you first install the extension, a sample company helps you get started.</span></span> <span data-ttu-id="2b35b-109">Voit poistaa malliyrityksen koska tahansa.</span><span class="sxs-lookup"><span data-stu-id="2b35b-109">You can delete the sample company at any time.</span></span>  

## <a name="installing-the-extension"></a><span data-ttu-id="2b35b-110">Laajennuksen asentaminen</span><span class="sxs-lookup"><span data-stu-id="2b35b-110">Installing the Extension</span></span>
<span data-ttu-id="2b35b-111">Kun olet asentanut laajennuksen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, sinulta kysytään, haluatko käyttää sitä heti.</span><span class="sxs-lookup"><span data-stu-id="2b35b-111">When you install the extension in your [!INCLUDE[d365fin](includes/d365fin_md.md)], you will be asked if you want to use it now.</span></span> <span data-ttu-id="2b35b-112">Jos haluat aloittaa käytön heti, sinun on kirjauduttava ensin ulos ja sitten takaisin sisään, koska laajennus korvaa nykyisen roolikeskuksen ja lisää käyttöoikeudet käyttäjäprofiiliisi.</span><span class="sxs-lookup"><span data-stu-id="2b35b-112">If you do, then you must sign out and sign in again, because the extension replaces your current Role Center and adds permissions to your user profile.</span></span>  

<span data-ttu-id="2b35b-113">Lisätietoja on kohdassa [Business Central -sovelluksen kirjanpitäjän käyttökokemukset](finance-accounting.md).</span><span class="sxs-lookup"><span data-stu-id="2b35b-113">For more information, see [Accountant Experiences in Business Central ](finance-accounting.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2b35b-114">Laajennuksen nykyinen versio edellyttää, että asiakasohjelmassa on käytössä [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2b35b-114">The current version of the extension requires that your clients use [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="using-the-extension"></a><span data-ttu-id="2b35b-115">Laajennuksen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="2b35b-115">Using the extension</span></span>
<span data-ttu-id="2b35b-116">Laajennus poistetaan käytöstä muutaman kuukauden kuluttua.</span><span class="sxs-lookup"><span data-stu-id="2b35b-116">This extension will be deprecated in a few months.</span></span> <span data-ttu-id="2b35b-117">Tämän laajennuksen asentamista ei suositella. Rekisteröidy sen sijaan [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] -sovellukseen [Business Central for Accountants -sovelluksessa osoitteessa Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants).</span><span class="sxs-lookup"><span data-stu-id="2b35b-117">We recommend that you do not install this extension but sign up for [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] at [Business Central for Accountants on Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants) instead.</span></span>

<span data-ttu-id="2b35b-118">Lisätietoja on kohdassa [Tervetuloa käyttämään ohjelmaa Dynamics 365 – Accountant Hub](/dynamics365/accountants/index).</span><span class="sxs-lookup"><span data-stu-id="2b35b-118">For more information, see [Welcome to Dynamics 365 — Accountant Hub](/dynamics365/accountants/index).</span></span>  

## <a name="see-also"></a><span data-ttu-id="2b35b-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2b35b-119">See Also</span></span>
[<span data-ttu-id="2b35b-120">Kirjanpitäjän käyttökokemukset Business Central -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="2b35b-120">Accountant Experiences in Business Central </span></span>](finance-accounting.md)  
[<span data-ttu-id="2b35b-121">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="2b35b-121">Finance</span></span>](finance.md)  

