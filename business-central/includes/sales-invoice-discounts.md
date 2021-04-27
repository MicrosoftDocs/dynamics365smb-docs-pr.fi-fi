---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 95121642b62f33ea1fc160c103ee845816706530
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778645"
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
