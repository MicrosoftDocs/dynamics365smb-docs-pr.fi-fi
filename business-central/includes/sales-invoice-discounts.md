---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ed62e60d3b5b1af2158d8adc6c411884ea4c12aa
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133574"
---
Kun kaikki nimikkeet on annettu riveinä, laskun alennus voidaan laskea koko myyntiasiakirjalle valitsemalla **Laske laskun alennus** -toiminto.

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
