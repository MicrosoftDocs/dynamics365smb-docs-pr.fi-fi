---
title: Vihjeet ja vinkit - RapidStart Services | Microsoft Docs
description: Kun määrität yrityksiä, jotka käyttävät RapidStart Services -palvelua, on joitakin vihjeitä ja vinkkejä, joita voit hyödyntää, auttaaksesi toteutuksen sujumista.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 875ab6f5875a842fb4c2ab906f39ae95607f6ba8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "796293"
---
# <a name="tips-and-tricks-rapidstart-services"></a>Vihjeet ja vinkit: RapidStart Services
Kun määrität yrityksiä, jotka käyttävät RapidStart Services -palvelua, on joitakin vihjeitä ja vinkkejä, joita voit hyödyntää, auttaaksesi toteutuksen sujumista.  

## <a name="take-advantage-of-configuration-templates"></a>Hyödyntää kokoonpano-malleja  
Määritysmallien avulla voit tehostaa toteutusprosessiasi. Niiden avulla voit sisällyttää samankaltaisia asiakkaita segmentteihin ja kehittää toteutusprotokollan, joka käsittelee kaikkia segmentin asiakkaita samalla tavalla. Tällä tavoin voit esimäärittää kunkin segmentin ja jatkaa nopeaa täytäntöönpanoa.  

## <a name="configuration-questionnaires"></a>Määrityskyselyt  
Tukeaksesi kyselylomakkeen täyttämisprosessia, harkitse oletusarvoisten vastausten määrittämistä parhaiden käytäntöjen osoittamiseksi.  

## <a name="batch-creation-of-journal-lines"></a>Päiväkirjarivien eräluonti  
Suosittelemme, että käytät tietojen siirron työkaluja siirtäessäsi päiväkirjamerkintöjä. Muutoin jos luot päiväkirjarivit eräajossa, sen kattavus on rajoitettu ja se luo päiväkirjaan vain esiasetettujen oletusten mukaiset kentät. Loput kirjauskansiosta täytyy täyttää käsin.  

## <a name="migrating-transactions"></a>Transaktioiden siirtäminen  
Suosittelemme, että siirrät avaussaldot seuraavassa järjestyksessä.  

1.  Siirrä pääkirjanpidon alkusaldot käyttämättä pääkirjanpidon tilin alareskontria. Käytä tiettyjä alkusaldon vastakirjauksen tilejä, yhtä kutakin alikirjausta varten. Määritä vastakirjauksen tilit sallimaan suorat kirjaukset.  
2.  Avointen asiakastapahtumoen siirtäminen  
3.  Siirrä avoimet nimiketapahtumat.  
4.  Siirrä avoimet käyttöomaisuustapahtumat.  

## <a name="see-also"></a>Katso myös  
[Yrityksen määrittäminen RapidStart Services -palvelun avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)
