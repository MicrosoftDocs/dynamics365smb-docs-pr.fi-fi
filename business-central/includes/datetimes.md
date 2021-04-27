---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7ead218d289668d893a659f730a4c64e31195f10
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788531"
---
Kun syötät päivämääriä ja aikoja, joissa päivämäärä ja aika on yhdistetty yhdeksi kentäksi, päivämäärän ja ajan välissä on oltava välilyönti. Päivämääräosa voi sisältää välilyöntejä vain alueasetusten virallisen päivämääräerottimen muodossa. Ajan välilyönnit voivat olla AM/PM-osoittimen ympärillä soveltuvissa alueasetuksissa.

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

Seuraavassa taulukossa on luettelo eri tavoista, joilla päivämääriä ja aikoja voi syöttää ja miten niitä tulkitaan:  

|Tapahtuma|Tulkinta|
|---------------|------------------------|
|08-01-2022 05:48:12 PM|08\-01\-2022 05:48:12 PM|
|131222 132455|13-12-22 13:24:55|
|1-12-22 10|01-12-22 10:00:00|
|1.12.22 5|01-12-22 05:00:00|
|1.12.22|01-12-22 00:00:00|
|11 12|11.nykyinen kuukausi.nykyinen vuosi 12:00:00|
|1112 12|11.12.nykyinen vuosi 12:00:00|
|t tai tänään|tämän päivän päivämäärä 00:00:00|
|a aika|tämän päivän pvm tämänhetkinen aika|
|t 10:30:00|tämän päivän päivämäärä 10:30:00|
|t 3:3:3|tämän päivän päivämäärä 03:03:03|
|k tai käsittelypvm|käsittelypvm 00:00:00|
|ma tai maanantai|nykyisen viikon maanantai 00:00:00|
|ti tai tiistai|nykyisen viikon tiistai 00:00:00|
|ke tai keskiviikko|nykyisen viikon keskiviikko 00:00:00|
|to tai torstai|nykyisen viikon torstai 00:00:00|
|pe tai perjantai|nykyisen viikon perjantai 00:00:00|
|la tai lauantai|nykyisen viikon lauantai 00:00:00|
|su tai sunnuntai|nykyisen viikon sunnuntai 00:00:00|
|ti 10:30:00|nykyisen viikon tiistai 10:30:00|
|ti 3:3:3|nykyisen viikon tiistai 03:03:03|
|t23 t|Käsittelypvm:n vuoden viikon 23 tiistai, nykyinen aika|
|t23|Käsittelypvm:n vuoden viikon 23 tiistai|
|t 23|Tänään 23:00:00|
|t-1|Käsittelypvm:n vuoden viikon 1 tiistai|


