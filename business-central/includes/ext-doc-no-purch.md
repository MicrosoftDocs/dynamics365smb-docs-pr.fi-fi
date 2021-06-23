---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 59376b96dcd6f755040b07784ceca53e157bcf14
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115942"
---
Ostoasiakirjoissa ja päiväkirjoissa voit määrittää asiakirjanumeron, joka viittaa toimittajan numerointijärjestelmään. Tämän kentän avulla voit tallentaa numeron, jonka toimittaja on määrittänyt tilaukselle, laskulle tai hyvityslaskulle. Tätä numeroa voi käyttää myöhemmin, jos sinun tarvitsee etsiä kirjattua merkintää tätä numeroa käyttämällä.

**Ulkois. asiakirjan nro pakoll.** -kenttä **Ostojen ja ostovelkojen asetukset** -sivulla määrittää, onko ulkoisen asiakirjan numeron syöttäminen seuraavissa tilanteissa pakollista:

* **Toimittajan laskunro** -kentässä **Toimittajan tilausnro** kenttä tai **Toimittajan hyvityslaskunro** kenttä ostojen tunnistetiedoissa

* Yleisen päiväkirjan rivin **Ulkoisen asiakirjan nro** -kentässä, jossa **Asiakirjatyyppi**-kenttä on *Lasku*, *Hyvityslasku* tai *Viivästyskulu* ja **Tilityyppi** -kenttä on *Toimittaja*.

Jos valitset kentän, laskua, hyvityslaskua tai aiemmin kuvattua yleisen päiväkirjan rivin tyyppiä ei voi kirjata ilman ulkoisen asiakirjan numeroa.

Ulkoisen asiakirjan numero sisältyy kirjattuihin asiakirjoihin, joista voit hakea asianomaisen numeron perusteella. Voit myös etsiä käyttämällä ulkoisen asiakirjan numeroa, kun navigoit toimittajatapahtumien merkinnöissä.

Ulkoisen asiakirjan numeroita voi käsitellä myös käyttämällä **Viitteenne**-kenttää. Jos käytät **Viitteenne**-kenttää, numero sisällytetään kirjattuihin asiakirjoihin, ja voit hakea sen mukaan samalla tavalla kuin haet arvoja **Ulkoisen asiakirjan nro** -kentistä. Kenttä ei ole kuitenkaan käytettävissä päiväkirjan riveillä.
