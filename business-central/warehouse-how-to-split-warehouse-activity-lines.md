---
title: Varastotoimintorivien jakaminen | Microsoft Docs
description: Fyysisen varastoinnin hyllytyksissä, siirroissa ja poiminnoissa sekä varaston hyllytyksissä ja poiminnoissa ohjelma ehdottaa varastopaikkoja nimikkeiden poimintaa tai hyllytystä varten. Joskus voi käydä niin, että ohjelman ehdottamassa varastopaikassa oleva määrä ei ole riittävä tai että ehdotetussa varastopaikassa ei ole tarpeeksi tilaa hyllytettävälle määrälle. Tällöin rivi on jaettava, jotta yhden rivin nimikkeet voidaan siirtää useisiin varastopaikkoihin tai hakea useista varastopaikoista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d2d560781da717d062abf04b5ebaffe1c4d1999e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381879"
---
# <a name="split-warehouse-activity-lines"></a>Varastotoimintorivien jakaminen
Fyysisen varastoinnin hyllytyksissä, siirroissa ja poiminnoissa sekä varaston hyllytyksissä ja poiminnoissa ohjelma ehdottaa varastopaikkoja nimikkeiden poimintaa tai hyllytystä varten. Joskus voi käydä niin, että ohjelman ehdottamassa varastopaikassa oleva määrä ei ole riittävä tai että ehdotetussa varastopaikassa ei ole tarpeeksi tilaa hyllytettävälle määrälle. Tällöin rivi on jaettava, jotta yhden rivin nimikkeet voidaan siirtää useisiin varastopaikkoihin tai hakea useista varastopaikoista.  

Seuraavat toimet koskevat kaikkia fyysisen varaston asiakirjoja, kuten fyysisen varaston hyllytys-, siirto-, ja poimintarivejä tai varaston hyllytys, siirto-, ja poimintarivejä.  

## <a name="to-split-warehouse-activity-lines"></a>Jaa fyysisen varaston aktiviteettirivit  
1.  Avaa fyysisen varastoinnin toimintorivi, jolla yrität käsitellä riittämätöntä määrää.  
2.  Anna **Käsiteltävä määrä** -kentässä vähennetty määrä, jonka voit käsitellä.  
3.  Valitse **Rivit**-pikavälilehdessä ensin **Toiminnot**-, sitten **Toiminnot**- ja lopuksi **Jaa rivi** -toiminto. Näyttöön tulee uusi rivi, joka on muuten identtinen kopio alkuperäisestä rivistä, mutta sen **Käsiteltävä määrä** -kentässä on alkuperäiseltä riviltä poistamasi määrä.  
4.  Määritä tälle uudelle riville asianmukainen varastopaikka (ja alue, jos käytössä on ohjattu hyllytys ja poiminta) tai jatka tarvittaessa rivin jakamista siihen asti, kunnes löydät sopivat varastopaikat koko määrälle.  

> [!NOTE]  
>  Jos jaat rivit, kun sijainnissa on käytössä ohjattu hyllytys ja poiminta, sinun täytyy tuntea fyysinen varasto hyvin ja pystyä valitsemaan varastopaikka, joka vastaa nimikkeen varastointitarpeita ja joka täyttää fyysisen varastoinnin asiakirjan yleiset vaatimukset. Et esimerkiksi voi jakaa poiminta-asiakirjan riviä ja sijoittaa joitakin nimikkeitä irtotavaroiden varastoon.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]