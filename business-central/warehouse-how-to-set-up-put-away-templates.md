---
title: Hyllytysmallien määrittäminen
description: Käytä hyllytysmalleja, jotta nimikkeille ehdotetaan aina sopivimpia varastopaikkoja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7312, 7313, 7314, 7321, 7322, 7323, 7329
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 59cb78989d4926f3155d5ca3eb195a185b0031bd
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971221"
---
# <a name="set-up-put-away-templates"></a>Hyllytysmallien määrittäminen

Ohjatussa hyllytyksessä ja poiminnassa ohjelma etsii kunakin hetkenä sopivimman varastopaikan nimikkeille seuraavien tekijöiden mukaan: fyysisen varastoinnin määritetty hyllytysmalli, varastopaikoille annetut varastopaikan luokittelut ja kiinteille varastopaikoille määritetyt vähimmäis- ja enimmäismäärät.  

Voit määrittää useita hyllytysmalleja ja valita niistä yhden hallitaksesi hyllytyksiä yleisesti fyysisessä varastossa. Voit valita hyllytysmallin myös mille tahansa nimikkeelle tai varastointiyksikölle, jolla voisi olla erityisiä hyllytysvaatimuksia.  

## <a name="to-set-up-put-away-templates"></a>Hyllytysmallien määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyllytysmallit** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3. Syötä koodi, joka on yksilöivä tunniste mallille, jota olet luomassa.  
4. Syötä halutessasi lyhyt kuvaus.  
5. Täytä ensimmäiselle riville varastopaikan vaatimukset, jotka haluat ohjelman ensin ja ennen kaikkea täyttävän silloin, kun se ehdottaa hyllytystä.

    Jos esimerkiksi haluat oletushyllytystavan perustuvan kiinteisiin varastopaikkoihin, valitse **Etsi kiinteä varastopaikka** -kenttä. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. Täytä toiselle riville varastopaikan vaatimukset, jotka olisivat seuraava valinta etsittäessä varastopaikkaa hyllytystä varten. Toista riviä käytetään vain, jos varastopaikkaa, joka vastaisi ensimmäisen rivin vaatimuksia ei löydy.  
7. Jatka rivien täyttämistä siihen saakka, kune olet kuvannut kaikki hyväksyttävät varastopaikkojen sijoitukset, joita haluat ohjelman käyttävän hyllytysprosessissa.  
8. Valitse hyllytysmallin viimeisellä rivillä **Etsi määrittelemätön var.p.**-valintaruutu.  

Voit luoda useita hyllytysmalleja ja käyttää niitä yrityksesi tarpeisiin sopivalla tavalla. Ohjelma viittaa ensin nimikkeelle tai varastointiyksikölle mahdollisesti valitsemaasi hyllytysmalliin. Jos näitä kenttiä ei ole täytetty, käytetään sitä hyllytysmallia, jonka olet valinnut fyysiselle varastoinnille sijaintikortin **Var.paikkojen periaatteet** -pikavälilehdessä.  

## <a name="see-also"></a>Katso myös

[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]