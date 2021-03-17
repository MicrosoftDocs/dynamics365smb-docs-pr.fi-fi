---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470285"
---
Kun kaikki nimikkeet on syötetty myyntiriveille, laskun alennus voidaan laskea koko asiakirjalle valitsemalla **Laske laskun alennus** -toiminto.

Alennus lasketaan kaikkien myyntiasiakirjan rivien perusteella niille nimikkeille, joilla on ostorivin **Salli laskualennus** -kentässä **Kyllä**. Tämä on oletusasetus nimikkeille. Esimerkiksi nimikekuluja sisältäviä rivejä ei sisällytetä laskualennuksen laskentaan. Jos haluat kohdistaa alennuksen tällaisiin riveihin, sinun täytyy asettaa **Rivialennus-%**-kenttä asianmukaisille riveille.  

> [!TIP]
> Alennus lasketaan automaattisesti, jos **Myyntien ja myyntisaamisten asetukset** -sivulla valitaan **Lask. laskun alennus** -kenttä ja jos teet jonkin seuraavista myyntiasiakirjassa:
>
> * Tarkastele tilastoja
> * Tarkastele testiraporttia
> * Tulosta
> * Kirjaus

Asiakkaan laskualennuksen ehdot on määritetty **Asiakkaan laskualennukset** -sivulla. Myyntiasiakirjan valuuttakoodin avulla etsitään valuutalle määritetyt laskualennusehdot.

Mikäli laskualennuksia ei ole määritetty ulkomaisille valuutoille, ohjelma käyttää laskualennusmäärityksiä, jotka on määritetty **Asiakkaan laskualennukset** -sivulla paikallisen valuutan summina ja myyntiasiakirjan kirjauspäivämäärän vaihtokurssia ulkomaanvaluuttamääräisen laskualennuksen laskemiseen.
