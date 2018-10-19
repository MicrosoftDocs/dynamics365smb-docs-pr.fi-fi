---
title: "Hyllytyksen luominen sisäisestä hyllytyksestä | Microsoft Docs"
description: "Kun nimikkeet on hyllytetty ja ennen kuin ne poimitaan täyttämään tuotantotilauksen tai toimituksen tarpeita, ne varastoidaan fyysiseen varastoon osaksi saatavilla olevaa varastoa."
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
ms.openlocfilehash: 17955c3ea1294811cd7b9ac6f726d26b0de2755c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="pick-and-put-away-without-a-source-document"></a>Poimiminen ja hyllyttäminen ilman lähdeasiakirjaa
Kun nimikkeet on hyllytetty ja ennen kuin ne poimitaan täyttämään tuotantotilauksen tai toimituksen tarpeita, ne varastoidaan fyysiseen varastoon osaksi saatavilla olevaa varastoa.  

On mahdollista, että nimikkeitä täytyy poistaa tilapäisesti fyysisen varastoinnin poimintavarastopaikoista, esim. myyntiesittelyn mallikappaleiksi. Nämä kohteet ovat edelleen yhtiön omaisuutta ja osa varastoa, mutta ne eivät ole poimittavissa. Ne on rekisteröity tarkoitusta varten luotuun erityistarkoituksen varastopaikkaan; periaatteessa nimikkeet ovat fyysisessä varastossa, mutta todellisuudessa ne voivat olla kokous- tai esittelyhuoneessa.  

Muissa tilanteissa tuotantoyksikkö voi yllättäen tarvita joitain osia käsittelyä varten. Voit poimia nimikkeitä tuotannon varastopaikkoja varten käyttämällä sisäistä poimintaa. Kun prosessi on ohi ja tuotos on luotu, nimikkeiden kulutus kirjataan ja tuotannon varastopaikka tyhjennetään, mikä puolestaan vähentää nimikkeen määrää sijainnissasi.  

Samoin nimikkeitä voidaan palauttaa fyysiseen varastoon hyllytettäviksi. Nimikkeet on voitu ottaa saatavilla olevasta varastosta tuotantotilausta varten, mutta niitä ei olekaan käytetty. Jotta voisit tehdä niistä taas osan saatavilla olevaa varastoa, ne on hyllytettävä varastopaikkaan.  

**Sisäiset hyllytykset** -toiminnolla voi tehdä hyllytyksiä ilman, että tiettyyn lähdeasiakirjaan on viitattava. Voitkin määrittää helposti kaikki fyysisen varastoinnin hyllytysohjeen luontiin tarvittavat tiedot.  

> [!NOTE]  
>  Jos et käytä sisäisiä poimintoja ja hyllytyksiä, nämä muutokset voi tehdä käyttämällä nimikkeiden varastopaikasta toiseen siirron tai varastopaikkojen määrän muutosten kirjaamisen menetelmiä.  
>   
>  Kun sijainnissa on käytössä ohjattu hyllytys ja poiminta ja siten myös varastopaikkatyypit, nimikkeitä ei voi siirtää varastopaikkaan, jonka tyyppi on Vastaanotto, eikä myöskään pois tällaisesta varastopaikasta. Tämä johtuu siitä, että Vastaanotto-tyyppisen varastopaikan nimikkeet on rekisteröitävä hyllytettäviksi, ennen kuin ne voivat olla osa saatavilla olevaa varastoa.  

## <a name="to-create-an-internal-pick"></a>Sisäisen poiminnan luominen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **F.var. sisäinen poiminta** ja valitse sitten liittyvä linkki.  
2.  Syötä **Nro** Kirjoita **Yleinen**-pikavälilehden Nro-kentän ja **Varastopaikkakoodiin**-kentän arvot. **Varastopaikkakoodiin**-kentässä määritetään varastopaikka, josta haluat hakea nimikkeet. Tuotannon yhteydessä tämä varastopaikka olisi saapuvan tuotannon varastopaikka tai avoin tuotannon varastopaikka. Muita tarkoituksia varten tulee valita sellainen Varastopaikkakoodiin-koodi, jonka varastopaikan tyyppiä ei käytetä ohjelmassa poimimiseen – todennäköisesti se on välivarastoinnin, toimituksen tai erityistarkoituksen varastopaikka.  
3.  Valitse nimike **Nimikkeen nro** -kentästä ja täytä määrät, jotka haluat poimia.  
4. Valitse **Luo poiminta** -toiminto. Fyysisen varastoinnin poimintaohje on nyt valmis varaston työntekijälle suoritettavaksi.  

## <a name="to-create-an-internal-put-away"></a>Sisäisen hyllytyksen luominen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **F.var. sisäinen hyllytys** ja valitse sitten liittyvä linkki.  
2.  Anna **Nro** Täytä **Yleinen**-pikavälilehden Nro-kenttä ja **Var.paikasta**-kenttä. **Var.paikasta**-kentässä määritetään varastopaikka, jossa esimerkiksi tuotannosta fyysiseen varastoon palautetut nimikkeet sijaitsevat.  
3.  Täytä riveille nimikenumerot ja määrät.  
4.  Valitse **Luo hyllytys** -toiminto. Fyysisen varastoinnin hyllytysohje on nyt valmis varaston työntekijälle suoritettavaksi.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

