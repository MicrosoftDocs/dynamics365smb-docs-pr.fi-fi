---
title: Vihjeitä – RapidStart Services | Microsoft Docs
description: Kun määrität yrityksiä RapidStart Servicesillä, voit sujuvoittaa käyttöönottoa muutamien vihjeiden avulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: acdac865286577b30f9fe036cca8a50eb7e143a0
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878984"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="e62b0-103">Vihjeitä: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="e62b0-103">Tips and Tricks: RapidStart Services</span></span>
<span data-ttu-id="e62b0-104">Kun määrität yrityksiä RapidStart Servicesillä, voit sujuvoittaa käyttöönottoa muutamien vihjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="e62b0-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="e62b0-105">Hyödyntää kokoonpano-malleja</span><span class="sxs-lookup"><span data-stu-id="e62b0-105">Take advantage of configuration templates</span></span>  
<span data-ttu-id="e62b0-106">Määritysmallien avulla voit tehostaa toteutusprosessiasi.</span><span class="sxs-lookup"><span data-stu-id="e62b0-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="e62b0-107">Niiden avulla voit sisällyttää samankaltaisia asiakkaita segmentteihin ja kehittää toteutusprotokollan, joka käsittelee kaikkia segmentin asiakkaita samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="e62b0-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="e62b0-108">Tällä tavoin voit esimäärittää kunkin segmentin ja jatkaa nopeaa täytäntöönpanoa.</span><span class="sxs-lookup"><span data-stu-id="e62b0-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="e62b0-109">Määrityskyselyt</span><span class="sxs-lookup"><span data-stu-id="e62b0-109">Configuration questionnaires</span></span>  
<span data-ttu-id="e62b0-110">Tukeaksesi kyselylomakkeen täyttämisprosessia, harkitse oletusarvoisten vastausten määrittämistä parhaiden käytäntöjen osoittamiseksi.</span><span class="sxs-lookup"><span data-stu-id="e62b0-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="e62b0-111">Päiväkirjarivien eräluonti</span><span class="sxs-lookup"><span data-stu-id="e62b0-111">Batch creation of journal lines</span></span>  
<span data-ttu-id="e62b0-112">Suosittelemme, että käytät tietojen siirron työkaluja siirtäessäsi päiväkirjamerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="e62b0-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="e62b0-113">Muutoin jos luot päiväkirjarivit eräajossa, sen kattavus on rajoitettu ja se luo päiväkirjaan vain esiasetettujen oletusten mukaiset kentät.</span><span class="sxs-lookup"><span data-stu-id="e62b0-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="e62b0-114">Loput kirjauskansiosta täytyy täyttää käsin.</span><span class="sxs-lookup"><span data-stu-id="e62b0-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="e62b0-115">Transaktioiden siirtäminen</span><span class="sxs-lookup"><span data-stu-id="e62b0-115">Migrating transactions</span></span>  
<span data-ttu-id="e62b0-116">Suosittelemme, että siirrät avaussaldot seuraavassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="e62b0-116">We recommend that you migrate opening balances in the following order.</span></span>  

1.  <span data-ttu-id="e62b0-117">Siirrä pääkirjanpidon alkusaldot käyttämättä pääkirjanpidon tilin alareskontria.</span><span class="sxs-lookup"><span data-stu-id="e62b0-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="e62b0-118">Käytä tiettyjä alkusaldon vastakirjauksen tilejä, yhtä kutakin alikirjausta varten.</span><span class="sxs-lookup"><span data-stu-id="e62b0-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="e62b0-119">Määritä vastakirjauksen tilit sallimaan suorat kirjaukset.</span><span class="sxs-lookup"><span data-stu-id="e62b0-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2.  <span data-ttu-id="e62b0-120">Avointen asiakastapahtumoen siirtäminen</span><span class="sxs-lookup"><span data-stu-id="e62b0-120">Migrate open customer ledger entries.</span></span>  
3.  <span data-ttu-id="e62b0-121">Siirrä avoimet nimiketapahtumat.</span><span class="sxs-lookup"><span data-stu-id="e62b0-121">Migrate open item ledger entries.</span></span>  
4.  <span data-ttu-id="e62b0-122">Siirrä avoimet käyttöomaisuustapahtumat.</span><span class="sxs-lookup"><span data-stu-id="e62b0-122">Migrate open fixed asset entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e62b0-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e62b0-123">See Also</span></span>  
[<span data-ttu-id="e62b0-124">Yrityksen määrittäminen RapidStart Servicesin avulla</span><span class="sxs-lookup"><span data-stu-id="e62b0-124">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="e62b0-125">Hallinta</span><span class="sxs-lookup"><span data-stu-id="e62b0-125">Administration</span></span>](admin-setup-and-administration.md)
