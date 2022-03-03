---
title: Käyttöomaisuuden käyttäjäkohtaisen poistomenetelmän määrittäminen
description: Business Centralissa voit käyttää käyttäjän määrittämää poistomenetelmää omaisuuserän poistomenetelmän määrittämiseen Käyttöomaisuuskortti-sivulla.
author: jill-kotel-andersson
ms.reviewer: edupont
ms.topic: conceptual
ms.search.keywords: user-depreciation
ms.date: 07/05/2021
ms.author: edupont
ms.openlocfilehash: 517c3cdb51762c3c0fadcf29ff1ad6dbf949f971
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144981"
---
# <a name="set-up-fixed-assets-with-user-defined-depreciation-methods"></a>Käyttöomaisuuden määrittäminen käyttäjän määrittämien poistomenetelmien avulla

Voit käyttää [!INCLUDE[prod_short](includes/prod_short.md)]ia käyttäjän määrittämien poistomenetelmien määrittämiseen tässä kuvatulla tavalla.

Jokaisessa käyttäjäkohtaisessa menetelmässä käytetään **Poistotaulukot**-sivua, johon tulee syöttää poistoprosentti kullekin jaksolle (kuukaudelle, vuosineljännekselle tai kirjanpitojaksolle). Kun käyttöomaisuudelle liitetään poistoirja, jossa on käyttäjän määrittämä menetelmä, sinun täytyy määrittää **Ens. käyttäjäkoht. poistopvm**- ja **Poiston aloituspvm** -kentät tietyn käyttöomaisuuserän **KO-poistokirjat**-sivulla.  

Poistosumman laskennan kaava on:  

*Poistosumma = (Poisto-% x Poistopäivien lkm x Poistopohja) / (100 x 360)*


> [!NOTE]  
> Päivämäärää kentässä **Ens. käyttäjäkoht. poistopvm** käytetään aikavälien määrittämiseen, ja kenttää **Poiston aloituspvm** käytetään poistopäivien lukumäärän määrittämiseen. Jos **Ens. käyttäjäkoht. poistopvm** on aikaisempi kuin **Poiston aloituspvm**, poistotaulukon ensimmäisen jakson prosenttiosuus käytetään vain osittain silloin, kun ohjelma laskee ensimmäistä poistoa. Tämä tarkoittaa sitä, että omaisuuserää ei poisteta kokonaan viimeisen jakson loppuun mennessä.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset-with-a-user-defined-depreciation-method"></a>Poistokirjan liittäminen käyttöomaisuuserään käyttäjän määrittämällä poistomenetelmällä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.
2. Valitse käyttöomaisuus, jolle haluat määrittää käyttöomaisuuden poistokirjan.
3. Valitse **Liittyvä**-toiminto, valitse **Käyttöomaisuus** ja valitse sitten **Poistokirjat**. Tämä avaa **KO:n poistokirjat** -sivun.

   Oletusarvon mukaan jotkin kentät, jotka on täytettävä alla olevien ohjeiden mukaisesti, on piilotettu, joten ne otettava näkyviin. Sen tehdäksesi sinun on muokattava sivua. Lisätietoja on kohdassa, jossa [Sivun mukauttaminen mukautusvalintanauhan avulla](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).
4. Valitse **Poistomenetelmä**-kentässä **Käyttäjän määrittämä**.
5. Valitse **Poistotaulukon koodi** -kentässä **Poistotaulukko**, jota haluat käyttää.
6. Valitse **Poiston aloituspvm** -kentässä poistolaskelman alkamispäivämäärä.
7. Kun käytät käyttäjän määrittämää menetelmää, **Ens. käyttäjäkoht. poistopvm** -kenttä on määritettävä niin, että sen päivämäärä on sama tai aikaisempi kuin  **Poiston aloituspvm** -kentässä. Jos olet valinnut arvon poistotaulukon **Jakson pituus** -kentässä, päivämäärän **Ens. käyttäjäkoht. poistopvm** -kentässä on oltava kirjanpitojakson aloituspäivämäärä.
8. Täytä joko **Poistovuosien lukumäärä** -kenttä tai **Poiston lopetuspvm** -kenttä. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

## <a name="to-set-up-user-defined-depreciation-methods"></a>Käyttäjäkohtaisten poistomenetelmien määrittäminen

**Poistotaulukon kortti** -sivulla voidaan määrittää käyttäjäkohtaiset poistomenetelmät. Voit esimerkiksi määrittää poiston yksiköiden määrän perusteella.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake, syötä **Poistotaulukot** ja valitse sitten vastaava linkki.  
2. Valitse **Poistotaulukkoluettelo**-sivulla **Uusi**-toiminto.  
3. Täytä **Poistotaulukkokortti**-sivun kentät tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Käytä **Luo numeroiden summataulukko** -funktiota, jotta voit määrittää poistotaulukon, joka perustuu *Numeroiden summa* -menetelmään.

Jos käyttöomaisuudelle tehdään poistoja neljän vuoden aikana, kunkin vuoden poisto lasketaan seuraavalla tavalla *Numeroiden summa* -menetelmällä:

Numeroiden summa = 1 + 2 + 3 + 4 = 10 Poisto:

* Vuosi 1 = 4/10  
* Vuosi 2 = 3/10  
* Vuosi 3 = 2/10  
* Vuosi 4 = 1/10  

### <a name="depreciation-based-on-number-of-units"></a>Yksiköiden lukumäärään perustuvat poistot

Tätä käyttäjäkohtaista menetelmää voidaan käyttää myös poistoissa, jotka perustuvat yksiköiden lukumäärään, esimerkiksi sellaisten tuotantokoneiden kohdalla, joiden eliniän kapasiteetti on vakio. **Poistotaulukot**-sivulle voidaan syöttää yksiköiden lukumäärä, joka voidaan tuottaa kullakin ajanjaksolla (kuukaudessa, neljännesvuodessa, vuodessa tai kirjanpitojakson aikana).  

### <a name="example---user-defined-depreciation"></a>Esimerkki - käyttäjän määrittämä poisto

Käytä poistomenetelmää, joka mahdollistaa poistojen tekemisen käyttöomaisuuseriin nopeutetusti tuloverotarkoituksia varten.  

Voit käyttää seuraavia poistoarvoja verotustarkoituksia varten käyttöomaisuudelle, jonka ikä on kolme vuotta:  

* Vuosi 1: 25 %  
* Vuosi 2: 38 %  
* Vuosi 3: 37 %  

Hankintameno on 100 000 PVA ja poistoaika on viisi vuotta. Poisto lasketaan vuosittain.  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 01/01/20 |Hankintameno |(Poiston aloituspvm) |100,000.00 |100,000.00 |
| 12/31/20 |Arvonalennus |360 |-25.000,00 |75,000.00 |
| 12/31/21 |Arvonalennus |360 |-38.000,00 |37,000.00 |
| 12/31/22 |Arvonalennus |360 |-37.000,00 |0 |
| 12/31/23 |Arvonalennus |Ei yhtään |Ei yhtään |0 |
| 12/31/24 |Arvonalennus |Ei yhtään |Ei yhtään |0 |

Edellisessä esimerkissä sekä **Ens. käyttäjäkoht. poistopvm**- ja **Poiston aloituspvm** -kentissä olisi arvo 01/01/20 tietyn käyttöomaisuuserän **KO-poistokirjat** -sivulla. Jos kuitenkin **Ens. käyttäjäkoht. poistopvm** -kentässä oli 1.1.20 ja **Poiston aloituspvm** -kentässä oli 1.4.20, tuloksena olisi:  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 01/01/20 |Hankintameno |(Poiston aloituspvm) |100,000.00 |100,000.00 |
| 12/31/20 |Arvonalennus |270 |-18.750,00 |81,250.00 |
| 12/31/21 |Arvonalennus |360 |-38.000,00 |42,250.00 |
| 12/31/22 |Arvonalennus |360 |-37.000,00 |6,250.00 |
| 12/31/23 |Arvonalennus |90 |-6.250,00 |0 |
| 12/31/24 |Arvonalennus |Ei yhtään |Ei yhtään |0 |


## <a name="see-also"></a>Katso myös
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden poiston määrittäminen](fa-how-setup-depreciation.md)  
[Käyttöomaisuuden poistomenetelmät](fa-depreciation-methods.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
