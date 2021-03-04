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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e9506697eacfb4bd411266078e4245e59a11353
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922415"
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

Suosittelemme, että siirrät avaussaldot seuraavassa järjestyksessä. <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. Siirrä pääkirjanpidon alkusaldot käyttämättä pääkirjanpidon tilin alareskontria. Käytä tiettyjä alkusaldon vastakirjauksen tilejä, yhtä kutakin alikirjausta varten. Määritä vastakirjauksen tilit sallimaan suorat kirjaukset.  
2. Avointen asiakastapahtumoen siirtäminen  <!--work on these-->
3. Siirrä avoimet nimiketapahtumat.  
4. Siirrä avoimet käyttöomaisuustapahtumat.  

## <a name="make-each-package-manageable"></a>Kunkin paketin tekeminen hallittavaksi

Jos siirrät tietoja määrityspakettien avulla, tietojen erottaminen erillisiksi paketeiksi helpottaa siirtämistä. Jos haluat siirtää esimerkiksi 20 vuoden kirjanpitotapahtumat, tuonti voi kestää useita tunteja tai useita päiviä. Jaa tiedot sen sijaan niin, että kunkin paketin hallittavuus paranee. Tällä hetkellä käytössä ei ole selkeitä paketin suorituskykyä koskevia sääntöjä, mutta paketin tuonnissa tai viennissä esiintyy ongelmia, pienennä paketin kokoa ja kokeile, jos se auttaa.  

## <a name="see-also"></a>Katso myös

[Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]