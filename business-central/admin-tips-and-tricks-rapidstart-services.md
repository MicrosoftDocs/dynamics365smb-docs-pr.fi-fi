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
ms.date: 08/18/2020
ms.author: edupont
ms.openlocfilehash: e1c3dfe37e6288934d05c4e2d9294cf87da49537
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786119"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="adaba-103">Vihjeitä: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="adaba-103">Tips and Tricks: RapidStart Services</span></span>

<span data-ttu-id="adaba-104">Kun määrität yrityksiä RapidStart Servicesillä, voit sujuvoittaa käyttöönottoa muutamien vihjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="adaba-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="adaba-105">Hyödyntää kokoonpano-malleja</span><span class="sxs-lookup"><span data-stu-id="adaba-105">Take advantage of configuration templates</span></span>

<span data-ttu-id="adaba-106">Määritysmallien avulla voit tehostaa toteutusprosessiasi.</span><span class="sxs-lookup"><span data-stu-id="adaba-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="adaba-107">Niiden avulla voit sisällyttää samankaltaisia asiakkaita segmentteihin ja kehittää toteutusprotokollan, joka käsittelee kaikkia segmentin asiakkaita samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="adaba-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="adaba-108">Tällä tavoin voit esimäärittää kunkin segmentin ja jatkaa nopeaa täytäntöönpanoa.</span><span class="sxs-lookup"><span data-stu-id="adaba-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="adaba-109">Määrityskyselyt</span><span class="sxs-lookup"><span data-stu-id="adaba-109">Configuration questionnaires</span></span>

<span data-ttu-id="adaba-110">Tukeaksesi kyselylomakkeen täyttämisprosessia, harkitse oletusarvoisten vastausten määrittämistä parhaiden käytäntöjen osoittamiseksi.</span><span class="sxs-lookup"><span data-stu-id="adaba-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="adaba-111">Päiväkirjarivien eräluonti</span><span class="sxs-lookup"><span data-stu-id="adaba-111">Batch creation of journal lines</span></span>

<span data-ttu-id="adaba-112">Suosittelemme, että käytät tietojen siirron työkaluja siirtäessäsi päiväkirjamerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="adaba-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="adaba-113">Muutoin jos luot päiväkirjarivit eräajossa, sen kattavus on rajoitettu ja se luo päiväkirjaan vain esiasetettujen oletusten mukaiset kentät.</span><span class="sxs-lookup"><span data-stu-id="adaba-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="adaba-114">Loput kirjauskansiosta täytyy täyttää käsin.</span><span class="sxs-lookup"><span data-stu-id="adaba-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="adaba-115">Transaktioiden siirtäminen</span><span class="sxs-lookup"><span data-stu-id="adaba-115">Migrating transactions</span></span>

<span data-ttu-id="adaba-116">Suosittelemme, että siirrät avaussaldot seuraavassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="adaba-116">We recommend that you migrate opening balances in the following order.</span></span> <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. <span data-ttu-id="adaba-117">Siirrä pääkirjanpidon alkusaldot käyttämättä pääkirjanpidon tilin alareskontria.</span><span class="sxs-lookup"><span data-stu-id="adaba-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="adaba-118">Käytä tiettyjä alkusaldon vastakirjauksen tilejä, yhtä kutakin alikirjausta varten.</span><span class="sxs-lookup"><span data-stu-id="adaba-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="adaba-119">Määritä vastakirjauksen tilit sallimaan suorat kirjaukset.</span><span class="sxs-lookup"><span data-stu-id="adaba-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2. <span data-ttu-id="adaba-120">Avointen asiakastapahtumoen siirtäminen</span><span class="sxs-lookup"><span data-stu-id="adaba-120">Migrate open customer ledger entries.</span></span>  <!--work on these-->
3. <span data-ttu-id="adaba-121">Siirrä avoimet nimiketapahtumat.</span><span class="sxs-lookup"><span data-stu-id="adaba-121">Migrate open item ledger entries.</span></span>  
4. <span data-ttu-id="adaba-122">Siirrä avoimet käyttöomaisuustapahtumat.</span><span class="sxs-lookup"><span data-stu-id="adaba-122">Migrate open fixed asset entries.</span></span>  

## <a name="make-each-package-manageable"></a><span data-ttu-id="adaba-123">Kunkin paketin tekeminen hallittavaksi</span><span class="sxs-lookup"><span data-stu-id="adaba-123">Make each package manageable</span></span>

<span data-ttu-id="adaba-124">Jos siirrät tietoja määrityspakettien avulla, tietojen erottaminen erillisiksi paketeiksi helpottaa siirtämistä.</span><span class="sxs-lookup"><span data-stu-id="adaba-124">When you use configuration packages to migrate data, separate the data into separate packages for easier portability.</span></span> <span data-ttu-id="adaba-125">Jos haluat siirtää esimerkiksi 20 vuoden kirjanpitotapahtumat, tuonti voi kestää useita tunteja tai useita päiviä.</span><span class="sxs-lookup"><span data-stu-id="adaba-125">For example, if you want to migrate 20 years of ledger entries, the import might take many hours and days.</span></span> <span data-ttu-id="adaba-126">Jaa tiedot sen sijaan niin, että kunkin paketin hallittavuus paranee.</span><span class="sxs-lookup"><span data-stu-id="adaba-126">Instead, split the data up so that each package becomes more manageable.</span></span> <span data-ttu-id="adaba-127">Tällä hetkellä käytössä ei ole selkeitä paketin suorituskykyä koskevia sääntöjä, mutta paketin tuonnissa tai viennissä esiintyy ongelmia, pienennä paketin kokoa ja kokeile, jos se auttaa.</span><span class="sxs-lookup"><span data-stu-id="adaba-127">Currently, there are no firm rules for what makes a package performant, but if you see problems importing or exporting a package, try making it smaller and see if that helps.</span></span>  

## <a name="see-also"></a><span data-ttu-id="adaba-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="adaba-128">See Also</span></span>

[<span data-ttu-id="adaba-129">Yrityksen määrittäminen RapidStart Servicesin avulla</span><span class="sxs-lookup"><span data-stu-id="adaba-129">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="adaba-130">Hallinta</span><span class="sxs-lookup"><span data-stu-id="adaba-130">Administration</span></span>](admin-setup-and-administration.md)  
