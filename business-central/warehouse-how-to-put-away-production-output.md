---
title: "Tuotannon tuotoksen hyllyttäminen | Microsoft Docs"
description: "Tuotannon hyllytystapa määräytyy sen mukaan, miten fyysinen varasto on määritetty sijaintina"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a7918a962f3349c68cd7245e9b12f83975aee5ac
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="put-away-production-or-assembly-output"></a>Tuotannon tai kokoonpanon tuotoksen hyllyttäminen
Tuotannon hyllytystapa määräytyy sen mukaan, miten fyysinen varasto on määritetty sijaintina Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

Jos fyysisen varastoinnin perusmääritykset edellyttävät sijainnissa on hyllytyksen käsittely muttei vastaanoton käsittelyä, tuotoksen hyllytys järjestetään ja kirjataan **Varaston hyllytys** -asiakirjan avulla.  

Jos laajennetut varastomääritykset edellyttävät sijainnissa sekä hyllytyksen että vastaanoton käsittelyä, voit hyllyttää tuotoksen luomalla joko sisäisen hyllytysasiakirjan tai siirtoasiakirjan.  

Tuotoksen hyllytyksen luonnin ensimmäinen vaihe on saapuvan varastoinnin pyynnön luonti. Tämä pyyntö ilmaisee fyysiselle varastolle, että tuotanto- tai kokoonpanotilauksen tuotos on valmis hyllytettäväksi.

## <a name="to-create-the-inbound-warehouse-request"></a>Saapuvan f. varastoinnin pyyntö  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Vapautettu tuotantotilaus** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse hyllytystä odottavassa tuotantotilauksessa **Luo saapuva f. var. pyyntö** -toiminto.  

> [!NOTE]  
>  Voit luoda saapuvan fyysisen varastoinnin pyynnön myös valitsemalla **Luo saapuva pyyntö** -valintaruudun, kun päivität tuotantotilauksen. Lisätietoja on kohdassa [Tuotantotilausten päivittäminen tai uudelleensuunnitteleminen](production-how-to-replan-refresh-production-orders.md).  

## <a name="to-put-output-away-with-an-inventory-put-away"></a>Nimikkeiden hyllyttäminen varastohyllytyksen avulla  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Varastohyllytys** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Luo uusi varaston hyllytys. Lisätietoja on kohdassa [Nimikkeiden hyllyttäminen varaston hyllytyksillä](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Voit tarkastella tuotantotilauksen tuotosta valitsemalla ensin **Hae lähdedokumentit** -toiminnon ja sitten vapautetun tuotantotilauksen.  
4.  Kirjoita hyllytysriveille halutut tiedot.
5.  Kun rivit ovat valmiit kirjaamista varten, valitse **Kirjaa**-toiminto. Kirjaus luo tarvittavat fyysisen varaston tapahtumat ja kirjaa nimikkeiden tuotoksen.  

Voit myös luoda **Varaston hyllytyksen** suoraan vapautetusta tuotantotilauksesta. Lisätietoja on kohdassa [Nimikkeiden hyllyttäminen varaston hyllytyksillä](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Kun kirjaat varastohyllytyksen, oletuksena on, että kaikki toiminnot kirjataan vakioreitityksen mukaan; toisien sanoen viimeisen toiminnon tuotoksen määrä kirjataan. Voit käyttää tuotospäiväkirjaa kirjataksesi varianssit tuotoksen määrässä sekä asennuksen ja ajoajat. Jos osittainen kirjaus vaaditaan varaston hyllytyksen luonnin jälkeen, näin voidaan tehdä kaikkien paitsi viimeisen toiminnon asetusaikojen ja määrien osalta. Tässä tapauksessa varaston hyllytys ohjaa viimeistä työvaihetta.  

Jos vain viimeisen toiminnon asetus- tai ajoaika on kirjattava, määritä viimeisen toiminnon tuotoksen määräksi 0. Vaihtoehtoisesti voit jättää viimeisen rivin kirjaamatta yksinkertaisesti poistamalla sen.  

## <a name="to-put-output-away-with-a-warehouse-internal-put-away"></a>Tuotoksen hyllytys sisäisen hyllytyksen tai siirron avulla
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **F.var. sisäinen hyllytys** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Uusi**-toiminto.
3. Kirjoita uuden sisäisen hyllytyksen otsikkoon ainakin **Sijaintikoodi**-kentän arvo.  
4. Täytä rivi jokaiselle nimikkeelle, jonka haluat siirtää fyysiseen varastoon. Vain **Nimikkeen nro**- ja **Määrä**-kenttien arvot on määritettävä.  

    > [!NOTE]  
    >  Kun valitset **Nimikkeen nro** -kentän, **Varastopaikan sisältöluettelo** avautuu **nimikeluettelon** sijasta. Näin tapahtuu siksi, että haluat hyllyttää nimikkeen, joka on tietyssä varastopaikassa (varastopaikan sisällössä), etkä mitä tahansa nimikettä, ja tiedät jo varastopaikan, josta nimike otetaan.  

4.  Voit täyttää työkirjan rivit sijainnin varastopaikkojen koko sisällöllä tai suodatetulla sisällöllä valitsemalla **Hae var.paikan sisältö** -toiminnon.  
5.  Valitse **Luo hyllytys** -toiminto. Tuotannosta siirrettävät nimikkeet ovat nyt hyllytysohjeissa ja odottavat varastointia fyysiseen varastoon.  

> [!NOTE]  
>  Kun fyysisen varastoinnin sijainti on määritetty käyttämään ohjattua hyllytystä ja poimintaa, varasto on linkitetty valmistus-toimintoon tuotannon oletusvarastopaikkojen kautta: saapuvat ja lähtevät tuotannon varastopaikat ja avoin tuotannon varastopaikka, jotka voit määrittää **Varastopaikat** -pikavälilehdestä sijainti-kortissa. Kun kirjaat tuotantotilauksen tuotoksen, ohjelma sijoittaa tuotoksen automaattisesti **lähtevään tuotannon varastopaikkaan**. Tuotannon tuotoksen hyllytys tapahtuu muuten edellä kuvatulla tavalla, paitsi että nimikkeen oletusvarastopaikan käytön asemesta nimikkeet siirretään tai hyllytetään **lähtevästä tuotannon varastopaikasta** nimikkeen oletusvarastopaikkaan.  

## <a name="to-manually-specify-a-bin-to-store-items-from-production-output"></a>Määrittele manuaalisesti varastopaikka, jonne tallennat tuotannon tuotoksen nimikkeitä  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Siirtotyökirja** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Täytä Siirtotyökirja-ikkunassa otsikon tiedot ja luo rivi kullekin nimikkeelle, jonka haluat siirtää fyysiseen varastoon.  
3.  Täytä sekä **Var.paikasta**- että **Varastopaikkakoodiin**-kentät ja kirjoita määrä **Määrä**-kenttään.  
4.  Voit täyttää työkirjan rivit sijainnin varastopaikkojen koko sisällöllä tai suodatetulla sisällöllä valitsemalla **Hae var.paikan sisältö** -toiminnon.  
5. Valitse **Luo siirto** -toiminto. Ohjelma luo fyysisen varaston siirto-ohjeen, jossa on Ota- ja Aseta-rivejä, suoritettavaksi varaston työntekijöille.  

> [!NOTE]  
>  Lähdeasiakirjan numeroa (tuotantotilauksen numeroa) ei voi syöttää sisäisen hyllytyksen, hyllytyksen tai siirron asiakirjoihin kummankaan menettelyn osalta.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

