---
title: Projektitilausten suunnittelu | Microsoft Docs
description: "Tämä suunnittelutehtävä aloitetaan myyntitilauksesta ja tehdään **Myyntitilaus suunnittelu** -ikkunan avulla. Kun projektituotantotilaus on luotu, voit jatkaa suunnittelua **Tilauksen suunnittelu** -ikkunassa."
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
ms.openlocfilehash: 08cd8c323e8f5221bd6915618582441a739e77c8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="plan-project-orders"></a>Projektitilausten suunnitteleminen
Tämä suunnittelutehtävä aloitetaan myyntitilauksesta ja tehdään **Myyntitilaus suunnittelu** -ikkunan avulla. Kun projektituotantotilaus on luotu, voit jatkaa suunnittelua **Tilauksen suunnittelu** -ikkunassa.  

## <a name="to-create-a-project-production-order"></a>Projektituotantotilauksen luominen  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.  
2.  Valitse tuotantoprojektia vastaava myyntitilaus ja valitse sitten **Suunnittelu**-toiminto.  
4.  Valitse **Myyntitilaus suunnittelu** -ikkunassa **Luo tuotantotilaus** -toiminto.  
5.  Valitse **Luo tilaus myynnistä** -ikkunan **Tilaustyyppi**-kentästä **Projektitilaus**.  
6.  Valitse **Kyllä**-painike.  
7.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotantotilaukset** ja valitse sitten liittyvä linkki.
8. Avaa juuri luotuun tuotantotilaukseen.  

    Huomaa, että tuotantotilauksen **Lähdetyyppi**-kentässä on **Myynnin tunnistetiedot** ja että tilaus sisältää useita rivejä (yhden kutakin tuotettavaa myyntirivin nimikettä kohden).  
9. Valitse **Suunnittelu**-toiminto.
10. Laske uusi kysyntä valitsemalla **Tilauksen suunnittelu** -ikkunassa **Päivitä**.  

Projektin tilauksen tilausotsikkorivillä näytetään kaikki täyttämättömät kysyntärivit, kun se laajennetaan. Vaikka tuotantotilauksessa on rivejä useille tuotantonimikkeille, kaikkien tuotantotilausrivien kokonaiskysyntä näkyy yhden tilausotsikkorivin alla **Tilauksen suunnittelu** -ikkunassa, ja alkuperäisen asiakkaan nimi näytetään. Voit nyt suunnitella kysynnän kohdassa [Uuden kysynnän tilauskohtainen suunnittelu](production-how-to-plan-for-new-demand.md) kuvatulla tavalla.  

> [!NOTE]  
>  Projektin tuotantotilauksen kysyntärivellä, joilla on **Tuotantotilaus** niiden **Täydennysjärjestelmä** -kentässä, edustavat perustana olevia tuotantotilauksia.. Kun olet luonut nämä tuotantotilaukset, suunnitelma on laskettava uudelleen **Tilauksen suunnittelu** -ikkunassa, jotta tunnistetaan niiden mahdolliset täyttämättömät osavaatimukset. Komponentit näytetään kysyntäriveinä normaalin tuotantotilausotsikon alla, eli projektisuhde ei enää näy ikkunassa. Jos kuitenkin käytetään tilauksen seurantaa, voidaan katsella ja selata kaikkia alkuperäisen myyntitilauksen johdannaisina tehtyjä toimitustilauksia.  

## <a name="see-also"></a>Katso myös
[Suunnittelu](production-planning.md)   
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md)   
[Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

