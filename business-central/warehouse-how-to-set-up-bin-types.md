---
title: Varastopaikkatyyppien määrittäminen | Microsoft Docs
description: Ohjelma on rakennettu ohjaamaan nimikevirta varastopaikkojen läpi, jotka olet määritellyt tietyille fyysisen varastoinnin aktiviteeteille. Kullekin varastopaikalle annetaan nimikevirran perusaktiviteetit – ja samalla määritellään tapa, jolla ohjelma käyttää varastopaikkaa – määrittelemälle sille varastopaikan tyyppi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: e5543c19abb9d40a1ed19b7224a54d584af36635
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783805"
---
# <a name="set-up-bin-types"></a>Varastopaikkatyyppien määrittäminen
Voit ohjata nimikkeiden kulkua tietyille varastotoiminnoille määritettyjen varastopaikkojen kautta. Kullekin varastopaikalle annetaan nimikevirran perusaktiviteetit – ja samalla määritellään tapa, jolla ohjelma käyttää varastopaikkaa – määrittelemälle sille varastopaikan tyyppi.  

Tyyppejä on kuusi. Voit käyttää fyysistä varastointia kaikilla kuudella mahdollisella varastopaikan tyypillä tai voit valita käyttäväsi vain VASTOTTO-, HYLLPOIM-, LÄHETYS- JA QC-varastopaikan tyyppejä. Nämä neljä varastopaikan tyyppiä mahdollistavat sen, että ohjelma voi tehdä ehdotuksia nimikevirran tukemiseksi, ja ne mahdollistavat varaston eroavaisuuksien tallentamisen.  

## <a name="to-set-up-the-bin-types-you-want-to-use"></a>Haluamiesi varastopaikan tyyppien määrittäminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varastopaikkatyypit** ja valitse sitten liittyvä linkki.  
2.  Luo **Varastopaikkatyypit**-sivulla 10-merkkinen koodi varastopaikan tyypille.  
3.  Valitse aktiviteetti, jotka voidaan suorittaa kullekin varastopaikan tyypille.  

> [!NOTE]  
>  Varastopaikkatyypit ovat käytössä vain, jos sijainnissa on käytössä ohjattu hyllytys ja poiminta.  

Varastopaikan tyyppi määrittää, miten ohjelma käyttää tiettyä varastopaikkaa käsitellessään nimikkeiden virtaa varaston läpi. Voit aina ohittaa ohjelman ehdotukset missä tahansa fyysisen varastoinnin asiakirjassa ja voit siirtää nimikkeitä varastopaikkaan tai varastopaikasta tekemällä fyysisen varastoinnin siirron.  

Varastopaikat, joita voi luoda, on luetteloitu seuraavassa.  

|Varastopaikan tyyppi|Description|  
|------------------|---------------------------------------|  
|VAST.OTTO|Nimikkeet, jotka on rekisteröity kirjatuiksi vastaanotoiksi, mutta niitä ei ole vielä hyllytetty.|  
|LÄHETYS|Nimikkeet, jotka on poimittu fyysisen varastoinnin toimitusriveille, mutta joita ei ole vielä kirjattu toimitetuiksi.|  
|HYLLYTYS|Yleensä kohteet voidaan tallentaa suurina mittayksiköinä, mutta et halua käyttää sitä poimintatarkoituksiin. Koska näitä varastopaikkoja ei käytetä keräilyyn, niin tuotantotilauksia kuin toimituksiakaan varten, Hyllytys-tyyppisten varastopaikkojen käyttö voi olla rajallista, mutta tämä varastopaikan tyyppi voi olla hyödyllinen, jos olet ostanut suuren määrän nimikkeitä. Tämän tyyppisillä varastopaikoilla pitäisi aina olla matala varastopaikan luokitus, jotta kun vastaanotetut nimikkeet hyllytetään, muut nimikkeeseen liitetyt korkeamman luokituksen PUTPICK-varastopaikat hyllytetään ensin. Jos käytät tämän tyyppistä varastopaikkaa, sinun täytyy tehdä varastopaikan täydennys säännöllisesti, jotta näihin varastopaikkoihin varastoidut nimikkeet olisivat saatavilla myös HYLLPOIM- ja POIMINTA-tyyppisissä varastopaikoissa.|  
|POIMINTA|Nimikkeille, joita käytetään vain poimintaan, esimerkiksi nimikkeille, joiden vanhentumispäivämäärä lähestyy, ja jotka olet siirtänyt tämän tyyppiseen varastopaikkaan. Näille varastopaikoille olisi hyvä asettaa korkea varastopaikan luokittelu, jotta niiden poimimista ehdotetaan ensin.|  
|HYLLPOIM|Nimikkeet varastopaikoissa, joille on ehdotettu sekä hyllytys- että poimintatoimintoa. Tämän tyyppisillä varastopaikoilla on todennäköisesti eri varastopaikan luokitteluja. Voit määrittää irtotavaran varastopaikat tämän tyyppiseksi varastopaikaksi, jolla on matalia varastopaikan luokitteluja verrattuna tavallisiin poimintavarastopaikkoihin tai edelleen poimimisen alueiden varastopaikkoihin.|  
|QC|Tätä varastopaikkaa käytetään varastomuutoksille, jos varastopaikka määritetään sijaintikortissa **Muutosvarastopaikan koodi** -kentässä. Tämän tyyppisiä varastopaikkoja voi määrittää myös viallisille nimikkeille ja tarkastettaville nimikkeille. Nimikkeitä voi siirtää tämän tyyppiseen varastopaikkaan, jos haluat, että ne eivät ole saatavilla tavallisessa nimikevirrassa.<br /><br /> **HUOMAUTUS:** Toisin kuin kaikki muut varastopaikkatyypit, **QC** -varastopaikkatyypillä ei ole valittuna nimikkeen käsittelyn valintaruutuja oletusarvoisesti. Tämä osoittaa, että QC-varastopaikkaan asetettu sisältö jää pois nimikevirroista.|  

## <a name="see-also"></a>Katso myös
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
