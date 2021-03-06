---
title: Nimikkeiden siirtäminen laajennetuissa varastomäärityksissä | Microsoft Docs
description: Fyysisen varaston laajennetuissa määrityksissä eli sijainneissa, joissa on käytössä ohjattu hyllytys ja poiminta, fyysisen varaston siirrot varastopaikkojen välillä suorittaa johtava työntekijä. Hän valmistelee fyysisen varaston siirrot fyysisen varaston työkirjaan ja luo varastotyöntekijöille suoritettavat fyysisen varaston siirrot.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e843b048c117539d077dc4a8ecba33f265a2e826
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782632"
---
# <a name="move-items-in-advanced-warehouse-configurations"></a>Nimikkeiden siirtäminen laajennetuissa varastomäärityksissä
Fyysisen varaston laajennetuissa määrityksissä eli sijainneissa, joissa on käytössä ohjattu hyllytys ja poiminta, fyysisen varaston siirrot varastopaikkojen välillä suorittaa johtava työntekijä. Hän valmistelee fyysisen varaston siirrot fyysisen varaston työkirjaan ja luo varastotyöntekijöille suoritettavat fyysisen varaston siirrot.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Siirrä nimikkeitä fyysisen varastoinnin siirtotyökirjan kanssa
**Siirtotyökirja**-sivulla on kaksi toimintoa, jotka auttavat rivien automaattisessa täyttämisessä. Ensimmäinen näistä on **Laske varastopaikan täydennys** -toiminto. Tämä toiminto ehdottaa täydennystä korkean luokittelun varastopaikoista matalamman luokittelun varastopaikkoihin. Toinen toiminto on **Hae var.paikan sisältö**-toiminto, joka täyttää työkirjan riveille määrittämiesi varastopaikkojen koko sisällön.

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Siirtotyökirja** ja valitse sitten liittyvä linkki.  
2.  Kirjoita työkirjan riveille asianmukaiset f. varaston siirtotiedot.  
3. Luo fyysisen varaston siirtoasiakirja **Luo siirto** -toiminto. Voit sitten rekisteröidä asiakirjan, kun fyysisen varaston siirto on valmis.  

### <a name="to-register-the-warehouse-movement"></a>F. varasoinnin siirron rekisteröinti  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirrot** ja valitse sitten liittyvä linkki.  
2.  Avaa fyysisen varastoinnin siirto, jota haluat käsitellä.  
3.  Määritä **Aseta**-toimintotyypin riveillä missä, mitä ja minne kyseessä oleva nimike siirretään, muokkaamalla kenttiä **Alueen koodi**, **Varastopaikan koodi**, **Käsiteltävä määrä** tai **Eräpäivä**.  

    Jos fyysinen varastointi on määritetty siten, että varastopaikkakoodit noudattavat varaston fyysistä järjestystä, voit ottaa useiden nimikkeiden määriä peräkkäisistä irtotavaran varastopaikoista ja asettaa ne sitten edelleen poiminnan varastopaikkoihin, jotka myös voivat olla lähekkäin.  
4.  Määritä **Ota**-toimintotyypin rivien **Käsiteltävä määrä** -kentässä varastopaikan sisällön osittainen määrä, jonka haluat siirtää. Kaikki muut kentät, joilla on toiminnon tyyppi **Ota**, ovat vain luku -tilassa.  
5.  Siirrä kaikki ehdotetut määrät määritysten mukaisesti valitsemalla **Määrä**-kentässä **Täytä autom. käsiteltävä määrä** -toiminto.  
6. Valitse **Rekisteröi**-toiminto.  

> [!NOTE]  
>  Kun sijainnissa on käytössä ohjattu hyllytys ja poiminta sekä varastopaikan tyypit, nimikkeitä ei voi siirtää varastopaikkaan, jonka tyyppi on Vastaanotto, eikä myöskään pois tällaisesta varastopaikasta. Tämä johtuu siitä, että Vastaanotto-tyyppisen varastopaikan nimikkeet on rekisteröitävä hyllytettäviksi, ennen kuin ne voivat olla osa saatavilla olevaa varastoa.

## <a name="to-register-the-movement-of-an-item-that-has-already-occurred"></a>Jo tapahtuneen nimikkeiden siirron rekisteröiminen  
Jos sijainnissa on käytössä ohjattu hyllytys ja poiminta ja nimikkeitä täytyy siirtää muihin varastopaikkoihin ilman olemassa olevaa fyysisen varastoinnin hyllytystä, poimintaa tai siirtoa, voit rekisteröidä nimikkeiden oikean sijoituksen fyysisessä varastossa **F. var. uudelleenluokituspvk** -päiväkirjan avulla.

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **F.var. uudellenluokituspvk** ja valitse sitten liittyvä linkki.  
2.  Täytä **Nimikkeen nro**-, **Aluekoodista**-, **Var.paikasta**-, **Aluekoodiin**- ja **Varastopaikkakoodiin**-kentät.  
3.  Valitse **Rekisteröi**-toiminto.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]