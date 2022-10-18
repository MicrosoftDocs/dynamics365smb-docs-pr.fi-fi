---
author: brentholtorf
ms.topic: include
ms.date: 10/05/2022
ms.author: bholtorf
ms.openlocfilehash: 8849f1c5d33cd1f826e7f53be317cb01e513fcd1
ms.sourcegitcommit: a9c778b65925435a4099fad45b3611f310e0b203
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/12/2022
ms.locfileid: "9652135"
---
Kun olet lisännyt kaikki nimikkeet riveille, laskun alennus voidaan laskea koko myyntiasiakirjalle valitsemalla **Laske laskun alennus** -toiminto.

Alennus lasketaan sen myyntiasiakirjan kaikkien rivien perusteella, jossa **Salli laskualennus** -valintaruutu on valittu. Oletusarvon mukaan laskualennukset ovat sallittuja. Kuitenkin esimerkiksi nimikekuluja sisältäviä rivejä ei sisällytetä laskualennuksen laskentaan. Voidaksesi kohdistaa alennuksen tällaisiin riveihin, sinun tulee syöttää arvot **Rivialennuksen määrä** -kentän riveille.  

> [!NOTE]
> Oletusarvon mukaan **Salli laskualennus**- ja **Rivin alennussumma** -kentät on piilotettu riveillä. Jos kenttiä ei ole käytettävissä, voit lisätä ne mukauttamalla sivua. Lisätietoja on kohdassa [Työtilan mukauttaminen](../ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

> [!TIP]
> Jos **Myyntien ja myyntisaamisten asetukset** -sivun **Lask. laskun alennus** -kentässä on valintamerkki, laskun alennus laskettiin automaattisesti. Laskentatapa vaihtelee käyttämäsi myyntiasiakirjan tyypin mukaan.
>
> Jos käytät myyntitilausta, alennus lasketaan rivin lisäämisen yhteydessä. Kaikkien muiden myyntiasiakirjojen, kuten myyntilaskujen, alennus lasketaan, kun teet jonkin seuraavista toimista:
>
> * Tarkastele tilastoja
> * Tarkastele testiraporttia
> * Tulostus
> * Kirjaus

Laskualennuksen ehdot määritetään **Asiakkaan laskualennukset** -sivulla. Myyntiasiakirjan valuuttakoodin avulla etsitään valuutalle määritetyt laskualennusehdot.

Jos et ole määrittänyt ulkomaanvaluutoille laskualennuksia, alennus lasketaan **Asiakkaan laskualennukset** -sivun alennusehtojen avulla. Laskennassa käytetään paikallista valuuttaa ja asiakirjan kirjauspäivämääränä voimassa olevaa vaihtokurssia.
