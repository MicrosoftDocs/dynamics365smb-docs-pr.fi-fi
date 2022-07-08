---
title: Varastopaikan sisältöjen luominen
description: Kun olet määrittänyt varastopaikat, voit määrittää ne nimikkeet, jotka haluat säilyttää, ja määrittää säännöt, jotka määrittävät, kuinka usein varastopaikat täytetään uudelleen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7374
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9135514b6f788aab99b3433a04ad28ec36064e30
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9074352"
---
# <a name="create-bin-contents"></a>Varastopaikan sisältöjen luominen

Kun olet määrittänyt varastopaikat, voit määrittää varastopaikan sisällön. Voit määrittää varastopaikkoihin varastoitavat nimikkeet ja säännöt, joita noudatetaan, kun varastopaikkaa täytetään tietyllä nimikkeellä. Voit tehdä sen manuaalisesti **Varastopaikan sisältö** -sivulla tai automaattisesti **Var.p. sisällön luontityökirja** -sivulla.

## <a name="to-create-bin-content-manually"></a>Varastopaikan sisällön luominen manuaalisesti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
2. Valitse sijainti, jossa haluat määrittää varastopaikan sisällön, ja valitse sitten **Varastopaikat**-toiminto.  
3. Valitse varastopaikka, jossa haluat määrittää sisällön, ja valitse sitten **Sisältö**-toiminto.  
4. Kirjoita kunkin varastopaikkaan varastoitavan nimikkeen riville asianmukaiset tiedot **Varastopaikan sisältö** -sivulla. Ohjelma on jo täyttänyt joihinkin kenttiin varastopaikan tiedot.  
5. Täytä ensin **Nimikenro**-kenttä ja sitten muut kentät, kuten **Mittayksikkökoodi**, **Enimmäismäärä** ja **Vähimmäismäärä**, jos käytät ohjattua hyllytystä ja poimintaa.  

Valitse tarvittaessa **Kiinteä**-kenttä. Jos varastopaikkaa käytetään nimikkeen oletusvarastopaikkana, valitse **Oletusvarastopaikka**-kenttä.  

Jos käytät ohjattua hyllytystä ja poimintaa ja olet syöttänyt (nimikkeen kortin kautta) oikeat mittatiedot kunkin nimikkeen mittayksiköistä (Pituus, Leveys, Korkeus ja Paino), ohjelma tarkistaa **Varastopaikan sisältö** -sivulla antamasi enimmäismäärän vertaamalla sitä varastopaikan fyysisiin rajoihin. Ohjelma käyttää sitten vähimmäis- ja enimmäismääriä laskiessaan varastopaikan täydennystä ja antaessaan hyllytysehdotuksia.  

Jos lisäät valintamerkin **Kiinteä**-kenttään, nimike asetetaan varastopaikkaan eli [!INCLUDE[prod_short](includes/prod_short.md)] yrittää panna nimikettä varastopaikkaan, jos sille on tilaa, ja se säilyttää tietueen nimikkeen asettamisesta varastopaikkaan, vaikka varastopaikan määrä on 0. Muita nimikkeitä voi panna varastopaikkaan, vaikka tietty nimike on asetettu varastopaikkaan.  

> [!NOTE]  
> Useita varastopaikan sisältöjä voi määrittää samaan aikaan **Var.p. sisällön luontityökirja** -sivulla.  

## <a name="to-create-bin-content-with-a-worksheet"></a>Varastopaikan sisällön luominen työkirjan avulla

Kun olet luonut varastopaikat, voit luoda varastopaikan sisällön, jonka haluat kullekin varastopaikalle varastopaikan sisällön luomisen työkirjassa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Var.p. sisällön luontityökirja** ja valitse sitten vastaava linkki.  
2. Valitse työkirjan otsikon **Nimi**-kentässä sen sijainnin työkirja, jossa haluat luoda varastopaikan sisällön.  
3. Valitse **Varastopaikkakoodi**-kentässä sen varastopaikan koodi, jolle haluat määrittää varastopaikan sisällön.  

    Jos sijainnissa on käytössä ohjattu hyllytys ja poiminta, ohjelma täyttää automaattisesti kyseiseen varastopaikkaan liittyvät kentät, kuten **Varastopaikan tyyppi**-, **F. var. luokkakoodi**- ja **Varastopaikan luokittelu** -kentät. Nämä tiedot kannattaa ottaa huomioon varastopaikan sisällön määrittämisessä.  
4. Valitse nimike, jonka haluat määrittää varastopaikkaan, ja täytä varastopaikan sisältöön liittyvät kentät. Jos käytät ohjattua hyllytystä ja poimintaa ja haluat käyttää **Laske varastopaikan täydennys** -toimintoa, täytä **Enimmäismäärä**- ja **Vähimmäismäärä**-kentät.  

    Määritä tämä varastopaikka nimikkeen tapahtuman ensisijaiseksi varastopaikaksi, vaikka varastopaikan määrä on **0** ja kaikki muut hyllytyskriteerit yhtä suure valitsemalla **Kiinteä** -kenttä.  
5. Toista nämä vaiheet kunkin varastopaikkaan määritettävän nimikkeen osalta.  
6. Voit esikatsella työkirjaan lisättyä varastopaikan sisältöä ja tulostaa sen valitsemalla **Tulosta**-toiminnon. Jatka varastopaikan sisällön muokkaamista, kunnes se on halutunlainen.  
7. Kun olet valmis, valitse **Luo var.paikan sisältö** -toiminto.  

Tässä työkirjassa voi työskennellä useiden varastopaikan sisältörivien parissa useiden varastopaikkojen osalta ja sen ansiosta voi saada hyvän yleiskuvan siitä, mitä olet panemassa eri varastopaikkoihin tietyllä alueella, käytävällä tai hyllyllä.  

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/set-up-zones-bins/)

## <a name="see-also"></a>Katso myös

[Laske var.paikan täydennys](warehouse-how-to-calculate-bin-replenishment.md)  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Rakennetiedot: f. varaston asetus](design-details-warehouse-setup.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]