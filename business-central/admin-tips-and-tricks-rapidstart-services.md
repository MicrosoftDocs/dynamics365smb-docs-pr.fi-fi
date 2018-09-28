---
title: Vihjeet ja vinkit - RapidStart Services | Microsoft Docs
description: "Kun määrität yrityksiä, jotka käyttävät RapidStart Services -palvelua, on joitakin vihjeitä ja vinkkejä, joita voit hyödyntää, auttaaksesi toteutuksen sujumista."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 875ab6f5875a842fb4c2ab906f39ae95607f6ba8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="c5ee3-103">Vihjeet ja vinkit: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="c5ee3-103">Tips and Tricks: RapidStart Services</span></span>
<span data-ttu-id="c5ee3-104">Kun määrität yrityksiä, jotka käyttävät RapidStart Services -palvelua, on joitakin vihjeitä ja vinkkejä, joita voit hyödyntää, auttaaksesi toteutuksen sujumista.</span><span class="sxs-lookup"><span data-stu-id="c5ee3-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="c5ee3-105">Hyödyntää kokoonpano-malleja</span><span class="sxs-lookup"><span data-stu-id="c5ee3-105">Take advantage of configuration templates</span></span>  
<span data-ttu-id="c5ee3-106">Määritysmallien avulla voit tehostaa toteutusprosessiasi.</span><span class="sxs-lookup"><span data-stu-id="c5ee3-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="c5ee3-107">Niiden avulla voit sisällyttää samankaltaisia asiakkaita segmentteihin ja kehittää toteutusprotokollan, joka käsittelee kaikkia segmentin asiakkaita samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="c5ee3-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="c5ee3-108">Tällä tavoin voit esimäärittää kunkin segmentin ja jatkaa nopeaa täytäntöönpanoa.</span><span class="sxs-lookup"><span data-stu-id="c5ee3-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="c5ee3-109">Määrityskyselyt</span><span class="sxs-lookup"><span data-stu-id="c5ee3-109">Configuration questionnaires</span></span>  
<span data-ttu-id="c5ee3-110">Tukeaksesi kyselylomakkeen täyttämisprosessia, harkitse oletusarvoisten vastausten määrittämistä parhaiden käytäntöjen osoittamiseksi.</span><span class="sxs-lookup"><span data-stu-id="c5ee3-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="c5ee3-111">Päiväkirjarivien eräluonti</span><span class="sxs-lookup"><span data-stu-id="c5ee3-111">Batch creation of journal lines</span></span>  
<span data-ttu-id="c5ee3-112">Suosittelemme, että käytät tietojen siirron työkaluja siirtäessäsi päiväkirjamerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="c5ee3-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="c5ee3-113">Muutoin jos luot päiväkirjarivit eräajossa, sen kattavus on rajoitettu ja se luo päiväkirjaan vain esiasetettujen oletusten mukaiset kentät.</span><span class="sxs-lookup"><span data-stu-id="c5ee3-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="c5ee3-114">Loput kirjauskansiosta täytyy täyttää käsin.</span><span class="sxs-lookup"><span data-stu-id="c5ee3-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="c5ee3-115">Transaktioiden siirtäminen</span><span class="sxs-lookup"><span data-stu-id="c5ee3-115">Migrating transactions</span></span>  
<span data-ttu-id="c5ee3-116">Suosittelemme, että siirrät avaussaldot seuraavassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="c5ee3-116">We recommend that you migrate opening balances in the following order.</span></span>  

1.  <span data-ttu-id="c5ee3-117">Siirrä pääkirjanpidon alkusaldot käyttämättä pääkirjanpidon tilin alareskontria.</span><span class="sxs-lookup"><span data-stu-id="c5ee3-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="c5ee3-118">Käytä tiettyjä alkusaldon vastakirjauksen tilejä, yhtä kutakin alikirjausta varten.</span><span class="sxs-lookup"><span data-stu-id="c5ee3-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="c5ee3-119">Määritä vastakirjauksen tilit sallimaan suorat kirjaukset.</span><span class="sxs-lookup"><span data-stu-id="c5ee3-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2.  <span data-ttu-id="c5ee3-120">Avointen asiakastapahtumoen siirtäminen</span><span class="sxs-lookup"><span data-stu-id="c5ee3-120">Migrate open customer ledger entries.</span></span>  
3.  <span data-ttu-id="c5ee3-121">Siirrä avoimet nimiketapahtumat.</span><span class="sxs-lookup"><span data-stu-id="c5ee3-121">Migrate open item ledger entries.</span></span>  
4.  <span data-ttu-id="c5ee3-122">Siirrä avoimet käyttöomaisuustapahtumat.</span><span class="sxs-lookup"><span data-stu-id="c5ee3-122">Migrate open fixed asset entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c5ee3-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c5ee3-123">See Also</span></span>  
[<span data-ttu-id="c5ee3-124">Yrityksen määrittäminen RapidStart Services -palvelun avulla</span><span class="sxs-lookup"><span data-stu-id="c5ee3-124">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="c5ee3-125">Hallinta</span><span class="sxs-lookup"><span data-stu-id="c5ee3-125">Administration</span></span>](admin-setup-and-administration.md)

