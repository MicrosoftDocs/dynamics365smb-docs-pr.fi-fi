---
title: Sijaintien määrittäminen käyttämään varastopaikkoja | Microsoft Docs
description: Varastopaikkat edustavat varastoinnin perusrakennetta ja niitä käytetään ehdotusten tekemiseksi nimikkeiden sijoittelusta. Kun olet luonut varastopaikat, voit määrittää hyvin tarkkaan sisällön, jonka haluat ohjelman sijoittavan kuhunkin varastopaikkaan, tai varastopaikka voi toimia määrittelemättömänä varastopaikkana, jolla ei ole määritettyä sisältöä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f2d7ecc163737c103c91b2a28a6a8072fad89279
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310178"
---
# <a name="set-up-locations-to-use-bins"></a>Sijaintien määrittäminen varastopaikkojen käyttämistä varten
Varastopaikat ovat varastoinnin perusrakenne, ja niitä niillä ehdotetaan nimikkeiden sijoittelua. Kun olet luonut varastopaikat, voit määrittää hyvin tarkkaan sisällön, jonka haluat ohjelman sijoittavan kuhunkin varastopaikkaan, tai varastopaikka voi toimia määrittelemättömänä varastopaikkana, jolla ei ole määritettyä sisältöä.  

A. Jotta voisit käyttää varastopaikan toimintoja sijainnissa, ne on otettava käyttöön **Sijainti**-kortissa Sitten voi suunnitella nimikevirran sijainnissa määrittämällä varastopaikkakoodit määrityskentistä, jotka edustavat eri virtoja.  

> [!NOTE]  
>  Ennen kuin voit määrittää varastopaikkakoodeja sijaintikortissa, on luotava varastopaikkakoodit. Lisätietoja on kohdassa [Varastopaikkojen luominen](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a>Määritä sijainti käyttääksesi varastopaikkoja  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten liittyvä linkki.  
2.  Valitse sijainti, jossa haluat käyttää varastopaikkoja.  
3.  Valitse **Muokkaa** -toiminto.  
4.  Valitse **Fyysinen varasto** -pikavälilehdessä **Var.paikka pakollinen** -valintaruutu.  
5.  Jos et käytä ohjattua hyllytystä ja poimintaa sijainnissa, kirjoita **Oletusvar.paikan valinta** -kenttään menetelmä, jolla haluat järjestelmän määrittävän nimikkeelle oletusvarastopaikan.  
6.  Avaa sen sijainnin kortti, johon haluat määrittää varastopaikkoja.
7.  Valitse **Varastopaikat**-pikavälilehdessä varastopaikat, joita haluat käyttää oletuksena vastaanotoille, toimituksille sekä saapuville, lähteville ja avoimille tuotannon varastopaikoille.  
8.  Tähän täyttämäsi varastopaikkakoodit tulevat automaattisesti näkyviin useiden eri fyysisen varastoinnin asiakirjojen otsikoihin (ja sitä myötä myös riveille, ellet muuta niitä). Oletusarvoiset varastopaikat määrittelevät nimikkeiden kaikki alku- ja loppusijoitukset fyysisessä varastossa.  
9.  Jos käytät ohjattua hyllytystä ja poimintaa, valitse varastopaikka fyysisen varastoinnin muutoksille. Varastopaikkakoodi **Muutosvarastopaikan koodi** -kentässä määrittää virtuaalisen varastopaikan, johon tallennetaan eroavaisuudet silloin, kun kirjataan joko varaston nimikepäiväkirjassa havaittuja eroja tai varaston inventoinnin yhteydessä laskettuja eroja.  
10. Täytä **Var.paikkojen periaatteet** -pikavälilehden kentät, jotka ovat olennaisia käytetyn fyysisen varastoinnin kannalta. Tärkeimmät kentät ovat **Var.paikan kapasiteettitapa**, **Salli erottelu** ja **Hyllytysmallin koodi**.  
11. Täytä **F. varastointi** -pikavälilehdessä kentät **Lähtevä f. var. käsittelyaika**, **Saapuva f. var. käsittelyaika** ja  **Peruskalenterin koodi**. Lisätietoja on kohdassa [Peruskalentereiden määrittäminen](across-how-to-assign-base-calendars.md).

## <a name="filling-the-consumption-bin"></a>Kulutuksen varastopaikan täyttäminen
Tämä työnkulkukaavio näyttää, miten tuotantotilauksen osarivien **Varastopaikkakoodi**-kenttä täytetään sijaintiasetusten mukaisesti.

![Varastopaikkojen vuokaavio](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Katso myös
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
