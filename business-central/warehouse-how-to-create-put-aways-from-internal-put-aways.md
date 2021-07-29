---
title: Hyllytyksen luominen sisäisestä hyllytyksestä
description: 'Tässä aiheessa käsitellään sitä, miten poimitaan ja hyllytetään ilman lähdeasiakirjaa: sekä sisäisen poiminnan luominen että sisäisen hyllytyksen luominen.'
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 198c4fb8ead4179667e35957046b3446ce5d8065
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444178"
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
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **F.var. sis. poim.** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.
3. Anna **Nro** Kirjoita **Yleiset**-pikavälilehden **Sijaintikoodi**- ja **Varastopaikkakoodiin**-kentän arvot. **Varastopaikkakoodiin**-kentässä määritetään varastopaikka, johon haluat sijoittaa keräillyt nimikkeet. Tuotannon yhteydessä tämä varastopaikka olisi saapuvan tuotannon varastopaikka tai avoin tuotannon varastopaikka. Muita tarkoituksia varten tulee valita sellainen varastopaikkakoodi, jonka varastopaikan tyyppiä ei käytetä ohjelmassa poimimiseen – todennäköisesti se on välivarastoinnin, toimituksen tai erityistarkoituksen varastopaikka.  
4.  Valitse nimike **Nimikkeen nro** -kentästä ja täytä määrät, jotka haluat poimia.  
5. Valitse **Luo poiminta** -toiminto. Fyysisen varastoinnin poimintaohje on nyt valmis varaston työntekijälle suoritettavaksi. Vaihtoehtoisesti voit valita **Vapautus**-toiminnon ja luoda fyysisen varastoinnin poiminnat käyttämällä **poimintatyökirjaa**. Lisätietoja on kohdassa [Poimintojen suunnitteleminen työkirjassa](warehouse-how-to-plan-picks-in-worksheets.md)

## <a name="to-create-an-internal-put-away"></a>Sisäisen hyllytyksen luominen  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **F.var. sis. hyllytys** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.
3. Kirjoita uuden sisäisen hyllytyksen otsikkoon ainakin **Nro**-kentän arvo. ja **Sijaintikoodi**.
4. Täytä rivi jokaiselle nimikkeelle, jonka haluat siirtää fyysiseen varastoon. Vain **Nimikkeen nro**- ja **Määrä**-kenttien arvot on määritettävä.

  > [!NOTE]  
  > Kun valitset **Nimikkeen nro** -kentän, **Varastopaikan sisältöluettelo** avautuu **nimikeluettelon** sijasta. Näin tapahtuu siksi, että haluat hyllyttää nimikkeen, joka on tietyssä varastopaikassa (*varastopaikan sisällössä*), etkä mitä tahansa nimikettä, ja tiedät jo varastopaikan, josta nimike otetaan.  <!--If you filled in **From Bin Code** in the header, the bin content will be filtered by value defined in the **From Bin Code**.-->
5. Voit täyttää rivit sijainnin varastopaikkojen koko sisällöllä tai suodatetulla sisällöllä valitsemalla **Hae var.paikan sisältö** -toiminnon.  
6. Valitse **Luo hyllytys** -toiminto. Fyysisen varastoinnin hyllytysohje on nyt valmis varaston työntekijälle suoritettavaksi. Vaihtoehtoisesti voit valita **Vapautus**-toiminnon ja luoda fyysisen varastoinnin hyllytykset käyttämällä **hyllytystyökirjaa**. Lisätietoja on kohdassa [Hyllytysten suunnitteleminen työkirjoissa](warehouse-how-to-plan-put-aways-in-worksheets.md)

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
