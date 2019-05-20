---
title: Vihjeitä – RapidStart Services | Microsoft Docs
description: Kun määrität yrityksiä RapidStart Servicesillä, voit sujuvoittaa käyttöönottoa muutamien vihjeiden avulla.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/05/2018
ms.author: sgroespe
ms.openlocfilehash: 6a10ab0d2e4658eba4824e44527d45cbf0f33dd8
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243478"
---
# <a name="tips-and-tricks-rapidstart-services"></a>Vihjeitä: RapidStart Services
Kun määrität yrityksiä RapidStart Servicesillä, voit sujuvoittaa käyttöönottoa muutamien vihjeiden avulla.  

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
[Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)
