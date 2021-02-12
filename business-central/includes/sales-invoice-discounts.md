---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035781"
---
Kun kaikki nimikkeet on syötetty myyntiriveille, laskun alennus voidaan laskea koko myyntiasiakirjalle valitsemalla **Laske laskun alennus** -toiminto.

Alennus lasketaan automaattisesti, jos **Myyntien ja myyntisaamisten asetukset** -ikkunassa valitaan **Lask. laskun alennus** -kenttä ja jos teet jonkin seuraavista myyntiasiakirjassa:

* Tarkastele tilastoja
* Tarkastele testiraporttia
* Tulosta
* Kirjaus

Alennus ositetaan kaikkien myyntiasiakirjan rivien osalta niille nimikkeille, joilla on ostorivin **Salli laskualennus** -kentässä **Kyllä**. Tämä on oletusasetus nimikkeille.

Ohjelma käyttää laskun alennuksen laskemiseen ehtoja, jotka on määritetty **Asiakkaan laskualennukset** -sivulla. Myyntiasiakirjan valuuttakoodin avulla etsitään valuutalle määritetyt laskualennusehdot.

Mikäli laskualennuksia ei ole määritetty ulkomaisille valuutoille, ohjelma käyttää laskualennusmäärityksiä, jotka on määritetty **Asiakkaan laskualennukset** -sivulla paikallisen valuutan summina ja myyntiasiakirjan kirjauspäivämäärän vaihtokurssia ulkomaanvaluuttamääräisen laskualennuksen laskemiseen.
