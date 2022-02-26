---
title: Verkkopankkitoiminta Suomessa
description: Business Central -sovelluksen verkkopankkitoimintojen avulla voi käsitellä elektronisia asiakas- ja toimittajamaksuja.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 32000000, 32000001, 32000002, 32000004, 32000005, 32000006
ms.date: 06/18/2021
ms.author: edupont
ms.openlocfilehash: 200268a771eb9c6493e125f68b7f0018c0276dd0
ms.sourcegitcommit: c05806689d289d101bd558696199cefbd989473e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2022
ms.locfileid: "8115020"
---
# <a name="electronic-banking-in-finland"></a>Verkkopankkitoiminta Suomessa
[!INCLUDE[prod_short](../../includes/prod_short.md)] -ohjelman verkkopankkitoimintojen avulla voi käsitellä elektronisia asiakas- ja toimittajamaksuja. Toiminto tukee verkkopankkimaksujen siirron kotimaan maksuja (LM03) ja ulkomaan maksuja (LUM2). Verkkopankkimaksujen vientiä tai tuontia varten on ensin määritettävä pankin viitetiedostot, joissa määritetään maksutiedostojen käsittelytapa.  

## <a name="customer-payments"></a>Asiakasmaksut  
Kotimaan asiakasmaksut voidaan tuoda pankista ja linkittää liittyvään myyntisaatavatapahtumaan viitenumeron avulla. Tämä automaattinen toiminto mahdollistaa saapuvien maksujen linkittämisen suoraan avoimiin myyntisaataviin ilman manuaalisen käsittelyn aiheuttamaa viivettä. Seuraavissa vaiheissa kuvataan, miten asiakasmaksut tuodaan pankista tiedostoon ja miten nämä maksut linkitetään laskuihin viitenumeroiden avulla.  

- Luo myyntilasku ja liitä laskuun yksilöivä viitenumero. Asiakas käyttää tätä viitenumeroa maksaessaan laskun.  

- Tuo asiakasmaksut sisältävät maksutiedostot kassapäiväkirjaan. Nämä tiedostot sisältävät pankilta saadut viitenumerot. Maksut linkitetään myyntisaatavatapahtumaan viitenumeroiden avulla.  

- Kirjaa tiedot kassapäiväkirjaan ja sulje avoimet myyntisaatavatapahtumat tiedoston kohdistettujen maksujen avulla.  

## <a name="reference-number"></a>Viitenumero  
Viitenumero luodaan automaattisesti, kun lasku kirjataan tai tilaus kirjataan laskutettavaksi. Myyntipäiväkirjan tapahtuman viitenumeron voi kuitenkin antaa myös manuaalisesti. Tämä viitenumero ei perustu **Myyntien ja myyntisaamisten asetukset** -sivun viitenumeroasetuksiin. Jos syötät myyntipäiväkirjaan viitenumeron, vain viitenumeron oikeellisuus tarkistetaan.  

## <a name="vendor-payments"></a>Toimittajamaksut  
Voit lähettää toimittajille verkkopankkimaksuja viemällä kotimaan tai ulkomaan toimittajamaksut pankille lähetettävään siirtotiedostoon. Seuraavissa vaiheissa kuvataan, miten toimittajamaksut viedään.  

- Valitse **Lähetettävät pankkimaksut** -sivulla toimittajat, joille maksutiedostot luodaan.  
- Syötä maksutiedot jokaiselle maksupäiväkirjan tapahtumalle tai käytä **Ehdota toimittajamaksuja** -toimintoa, joka luo ehdotetut maksut.  
- Luo ja esikatsele maksuraportti.  
- Luo siirtotiedosto kotimaan tai ulkomaan toimittajamaksuille.  
- Lähetä maksun siirtotiedosto pankkiin.  

## <a name="see-also"></a>Katso myös  
 [Suomen paikalliset toiminnot](finland-local-functionality.md)   
 [Pankin viitetiedostojen määrittäminen](how-to-set-up-bank-reference-files.md)   
 [Maksutiedostojen luominen](how-to-generate-payment-files.md)   
 [Maksualennusten ohittaminen](how-to-disregard-payment-discounts.md)   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]