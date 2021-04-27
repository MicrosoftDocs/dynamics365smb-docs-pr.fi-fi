---
title: Komponenttien siirtäminen toiminta-alueelle fyysisen varastoinnin perusmäärityksissä
description: Jos fyysisen varaston sijainnissa on nimikkeen käsittelytoimintoja, nimikkeitä on ehkä siirrettävä sisäisten varastopaikkojen välillä vastaamaan sisäisiä lähdeasiakirjoja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4b9a131b890efe1612ec05d6810d5b661447b26f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782657"
---
# <a name="move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Komponenttien siirtäminen toiminta-alueelle fyysisen varastoinnin perusmäärityksissä
Jos fyysisen varaston sijainnissa on nimikkeen käsittelytoimintoja, nimikkeitä on ehkä siirrettävä sisäisten varastopaikkojen välillä vastaamaan sisäisiä lähdeasiakirjoja, kuten sijainnin tuotantoa, kokoonpanoa tai huoltotilauksia.  

> [!NOTE]  
>  Lisätietoja nimikkeiden siirtämisestä varastopaikkojen välillä ilman lähdeasiakirjoja on ohjeaiheessa Sisäinen siirto.  

Laajennetuissa varastomäärityksissä eli sijainneissa, joissa käytetään **Ohjattu hyllytys ja poiminta** -asetuskenttää, nimikkeitä voi siirtää varastopaikkojen välillä **Var.siirtotyökirja**-sivulla. Lisätietoja on kohdassa [Nimikkeiden siirtäminen laajennetuissa varastomäärityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Fyysisen varaston perusmäärityksissä eli sijainneissa, joissa käytetään **Var.paikka pakollinen**- ja **Vaadi poiminta** -asetuskenttää, voi rekisteröidä nimikkeiden varastosiirron sisäisille toimintoalueille sisäisten lähdeasiakirjojen perusteella seuraavilla tavoilla:  

-   **Varaston siirto** -sivulla.  
-   **Varaston poiminta** -sivulla.  

> [!NOTE]  
>  Varaston poiminnat luovat lisäksi negatiiviset nimiketapahtumat kulutuksena, ja vain tuotantokomponentit tukevat niitä. Lisätietoja on Varaston poiminta -sivulla.  

Lisätietoja varastosiirroista on Varaston siirto-sivulla.  

Kaksi erilaista roolia voi luoda alkuperäisen varaston siirron. Esimerkiksi kokoonpanotyöntekijä voi luoda sen julkaistusta kokoonpanotilauksesta siten, että se näkyy varastotyöntekijän tehtäväluettelossa. Luodakseen kokoonpantilauksen niille riveille varastosiirto, joiden määritettyihin varastopaikkoihin voi siirtää osia, kokoonpanotyöntekijä käyttää **Luo varastosiirto** -funktiota.  

Myös varastotyöntekijä voi luoda sen valitsemalla kyseisen julkaistun kokoonpanotilauksen. Tämä kuvataan seuraavassa menettelytavassa.  

> [!NOTE]  
>  Jos siirto koskee kokoonpanotilausta, jossa nimike on koottu myyntitilaukseen, voit määrittää, että varastosiirtoasiakirja luodaan automaattisesti varaston poiminta-asiakirjan luonnin yhteydessä. Poiminta-asiakirja tallentaa valmiin kokoonpanon nimikkeen ja kirjaa toimituksen. Voit määrittää tämän valitsemalla **Luo siirrot automaattisesti** -kentän **Kokoonpanon asetukset** -sivulla  
>   
>  Lisätietoja kokoonpanotilauksista ja perusvarastointimäärityksistä on kohdassa [Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Tässä toimenpiteessä kuvataan, miten voit luoda varastosiirron **Varastosiirto**-sivulla viittaamalla vapautettuun kokoonpanotilaukseen lähdeasiakirjana. Menettely on sama kun siirrät tuotantotilausten ja huoltotilausten osia.  

## <a name="to-move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Komponenttien siirtäminen toiminta-alueelle fyysisen varastoinnin perusmäärityksissä  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varaston siirto** ja valitse sitten liittyvä linkki.  
2.  Täytä **Yleinen**-pikavälilehden **Nro** -kentässä. Jos painat Enter-näppäintä valitaksesi numerosarjoista.  
3.  Anna **Sijaintikoodi**-kentässä sijainti, jossa varaston siirto tapahtuu.  
4.  Valitse **Hae lähdeasiakirjat** -toiminto. Voit myös täyttää **Lähdeasiakirja**-kentän ja valita sitten **MuokkausApu**-painikkeen **Lähteen nro** -kentässä.  
5.  Valitse **Lähdeasiakirjat**-sivulla kokoonpanotilaus, jota varten haluat siirtää komponentteja, ja valitse sitten **OK**.  

    Jokaiselle tarvittavalle komponentille, joka voidaan siirtää, luodaan yksi Ota- ja yksi Aseta-rivi **Varastosiirrot**-sivulla. Kaikki kentät lukuun ottamatta **Käsiteltävä määrä** -kenttää täytetään valmiiksi lähdeasiakirjan rivien mukaan. **Käsiteltävä määrä** -kenttä on asetettu nollaan siihen asti, kun syötät siirtämäsi määrän.  

    Voit muuttaa varastopaikkakoodia Ota-rivillä, mutta vain saatavuuden mukaan. Jos valitset Ota-rivillä **Muokkausapu**-painikkeen **Varastopaikkakoodi**-kentässä, **Varastopaikan sisältö** -sivu avautuu. Sivulla näkyvät vain varastopaikat, joissa komponentti on käytettävissä.  

    Et voi muuttaa varastopaikan koodia Aseta-rivillä. Vain se varastopaikan koodi hyväksytään, joka on määritetty lähdeasiakirjan komponenttirivillä. Tämä tukee periaatetta, jonka mukaan rooli, joka pyytää osaa, joka on tässä toimenpiteessä kokoaja, tietää, mihin osa on sijoitettava. Jos haluat asettaa komponentit toiseen varastopaikkaan, muuta ensin komponenttirivin varastopaikkakoodi ja luo sitten varastosiirtorivit uudelleen  
6.  Anna **Käsiteltävä määrä** -kentässä koko määrä tai osittainen määrä, jonka olet todellisuudessa siirtänyt. Ota- ja Aseta-rivien arvojen on oltava samat. Muutoin et voi rekisteröidä siirtoa.  

    > [!NOTE]  
    >  Kuten muissakin varastotoiminnoissa, voit jakaa Paikka-rivin valitsemalla ensin **Toiminnot**- ja sitten **Jaa rivi** -toiminnot. Tässä tapauksessa kahden jaetun Aseta-rivin summan on oltava yhtä suuri kuin Ota-rivin määrä.  

7.  Kun olet valmis rekisteröimään tekemäsi siirrot, valitse **Rekisteröi varastosiirto** -toiminto.  

    Fyysisen varastoinnin tapahtumat luodaan kuvaten sitä, että osat ovat nyt olemassa määritetyissä varastopaikoissa kokoonpanotilausriveillä.  

    > [!NOTE]  
    >  Toisin kuin jos siirrät osia, joissa on varastopoiminta, kulutusta ei kirjata silloin, kun rekisteröidään varastosiirto. Tämä vaihe on suoritettava erikseen kirjaamalla kokoonpanotilauksen tuotto ja kulutus. Lisätietoja on kohdassa Kokoonpanotilaus.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]