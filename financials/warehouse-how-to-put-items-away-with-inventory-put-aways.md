---
title: "Nimikkeiden hyllyttäminen varastohyllytyksen avulla | Microsoft Docs"
description: "Kun sijainti on määritetty edellyttämään hyllytyskäsittelyä mutta ei vastaanottokäsittelyä, lähdeasiakirjojen hyllytys- ja vastaanottotiedot tallennetaan ja kirjataan **Varastohyllytys**-asiakirjaan. Saapuva lähdeasiakirja voi olla ostotilaus, myyntipalautustilaus, saapuva siirtotilaus tai tuotantilaus jonka tuotos odottaa hyllytystä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5de060d742401da62339fb67deff38d0a1e7bddb
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-put-items-away-with-inventory-put-aways"></a>Nimikkeiden hyllyttäminen varastohyllytyksen avulla
Kun sijainti on määritetty edellyttämään hyllytyskäsittelyä mutta ei vastaanottokäsittelyä, lähdeasiakirjojen hyllytys- ja vastaanottotiedot tallennetaan ja kirjataan **Varastohyllytys**-asiakirjaan. Saapuva lähdeasiakirja voi olla ostotilaus, myyntipalautustilaus, saapuva siirtotilaus tai kokoonpano- tai tuotantotilaus, jonka tuotos odottaa hyllytystä.  

Varastohyllytyksen voi luoda kolmella tavalla:  

- Luo hyllytys kahdessa vaiheessa luomalla ensin varastopyyntö lähdeasiakirjasta. Tämä toimii signaalina varastolle, että lähdeasiakirja odottaa hyllytystä.  Varaston hyllytys voidaan sitten luoda **Varaston hyllytys** -ikkunassa lähdeasiakirjan perusteella.  
- Luomalla varastohyllytys suoraan lähdeasiakirjasta.  
- Voit luoda varastohyllytyksen usealle asiakirjalle yhdellä kertaa eräajon avulla.  

## <a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a>Pyydä varaston hyllytys vapauttamalla lähdeasiakirja
Jos kyseessä on ostotilaus, myyntipalautustilaus, saapuva siirtotilaus tai kokoonpanotilaus, voit luoda fyysisen varastoinnin pyynnön vapauttamalla tilauksen. Seuraavaksi käsitellään, miten se tehdään ostotilauksesta.  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostotilaukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse ensin vapautettava ostotilaus ja sitten **Vapauta**-toiminto.  

    Tuotantotilausten fyysisen varastoinnin pyyntö luodaan luomalla saapuva pyyntö vapautetusta tuotantotilauksesta.  
3.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Vapautetut tuotantotilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
4. Valitse **Luo saapuva f. var. pyyntö** -toiminto.  

> [!NOTE]  
>  Voit luoda saapuvan fyysisen varastoinnin pyynnön myös valitsemalla **Luo saapuva pyyntö** -valintaruudun, kun päivität tuotantotilauksen. Lisätietoja on kohdassa [Toimintaohje: Tuotantotilausten päivittäminen tai uudelleensuunnitteleminen](production-how-to-replan-refresh-production-orders.md).  

Kun fyysisen varastoinnin pyyntö on luotu, varastossa hyllytystä tekevä työntekijä voi nähdä, että lähdeasiakirja odottaa hyllytystä ja hän voi luoda uuden hyllytysasiakirjan fyysisen varastoinnin pyynnöstä.  

## <a name="to-create-an-inventory-put-away-based-on-the-source-document"></a>Varastohyllytyksen lähdeasiakirjasta luominen
Nyt kun pyyntö on luotu, varastotyöntekijä voi luoda uuden varastohyllytyksen vapautetun lähdeasiakirjan perusteella.   
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Varastohyllytys** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3. Valitse **Lähdeasiakirja**-kentässä hyllytettävän lähdeasiakirjan tyyppi.  
4. Valitse **Lähteen nro** -kentässä lähdeasiakirja.  
5. Vaihtoehtoisesti voit valita **Hae lähdeasiakirja** -toiminnolla asiakirjan niiden saapuvien lähdeasiakirjojen luettelosta, jotka ovat valmiita hyllytykseen sijainnissa.  
6. Valitse **OK** täyttääksesi hyllytyksen rivit valitun lähdeasiakirjan mukaan.  

## <a name="to-create-an-inventory-put-away-from-the-source-document"></a>Varastohyllytyksen lähdeasiakirjasta luominen  
1.  Valitse **Luo varaston hyllytys tai poiminta** -toiminto lähdeasiakirjassa, joka voi olla ostotilaus, myyntipalautustilaus, saapuva siirtotilaus tai tuotantotilaus.  
2. Valitse **Luo varaston hyllytys** -valintaruutu.
3. Valitse **OK**-painike. Uusi varaston hyllytys on luotu.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a>Useiden varastohyllytysten luominen eräajon avulla  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Luo var. hyllytys/poiminta** ja valitse sitten aiheeseen liittyvä linkki.  
2.  **F.var. pyyntö** -pikavälilehdessä voit käyttää **Lähdeasiakirja**- ja **Lähdenro**-kenttiä ja suodattaa tietyn tyyppisiä asiakirjoja (esim. luoda poimintoja vain myyntitilaukselle) tai asiakirjanumerovälejä.  
3.  Valitse **Asetukset**-pikavälilehdessä **Luo varaston hyllytys** -valintaruutu.
4.  Valitse **OK**-painike. Määritetyt varastohyllytykset luodaan.

## <a name="to-record-the-inventory-put-away"></a>Varastohyllytyksen kirjaaminen  
1. Avaa aiemmin luodun hyllytysasiakirjan valitsemalla sen **Varaston hyllytykset** -ikkunassa.  
2. Hyllytysrivien **Varastopaikkakoodi**-kentän varastopaikka, johon nimikkeet on hyllytettävä, ehdotetaan nimikkeen oletusvarastopaikan mukaan. Voit tarvittaessa muuttaa varastopaikkaa tässä ikkunassa.  
3. Suorita hyllytys ja syötä tiedot koskien todellisia hyllytysmääriä **Käsiteltävä määrä** -kentässä.

    Jos yhden rivin nimikkeet on asetettava useaan varastopaikkaan esimerkiksi siksi, että määritetty varastopaikka on täynnä, käytä **Rivit**-pikavälilehden **Jaa rivi** -toimintoa. Lisätietoja rivien jakamisesta on kohdassa [Toimintaohje: Varastotoimintorivien jakaminen](warehouse-how-to-split-warehouse-activity-lines.md).  
4. Kun olet suorittanut hyllytyksen, valitse **Kirjaa**-toiminto.  

Kirjausprosessi kirjaa vastaanoton (tai tuotantotilauksille tuotoksen) lähdeasiakirjoista jotka on hyllytetty ja lisäksi jos sijainti käyttää var.paikkoja kirjaus luo myös f.var.tapahtumia kirjatakseen varastopaikan määrä muutoksia.

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

