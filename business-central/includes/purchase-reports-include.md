---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ae96e5a3fc1cc7f4b17e5ef208650248cbe0b3c2
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104105"
---
Seuraavassa taulukossa kuvataan joitakin ostoraportoinnin keskeisiä raportteja.

|Raportti |Objektin tunnus|Kuvaus  |
|---------|---------|---------|
|**Ostotilastot**|312|[!INCLUDE [reports-purchase-statistics](reports-purchase-statistics.md)]|
|**10 päätoimittajaa**|311|Tässä raportissa näkyy tietoja toimittajilta tehdyistä ostoista valitulta ajanjaksolta. Voit valita raporttiin sisällytettävien toimittajien lukumäärän.<br>Toimittajat lajitellaan summan mukaan, ja voit valita, lajitellaanko ne ostosummittain vai saldoittain. Raportti antaa katsauksen toimittajista, joilta ostat eniten tai joille olet velkaa eniten.|
|**Toimittajakoht. nimikeluettelo** tai **Nimike-/toimittajaluettelo**|320 tai 720|Näyttää luettelon valittujen nimikkeiden toimittajista tai valittujen toimittajien nimikkeistä. Raportissa on jokaisen nimikkeen ja toimittajan osalta välitön yksikkökustannus, toimitusajan laskenta ja toimittajan nimikenumero.<br>Yhdysvalloissa, Kanadassa ja Meksikossa tämä raportti ei ole käytettävissä. Käytä sen sijaan **Nimike/toimittaja luettelo** (10164) -raporttia.|
|**Toimittaja-/nimikeostot**|313|Tässä raportissa näkyy luettelo nimiketapahtumista kunkin toimittajan osalta valitulta ajanjaksolta. Raportissa on tietoja laskutetusta määrästä, summasta ja mahdollisista alennuksista. Raporttia käytetään esimerkiksi analysoimaan yrityksen nimikeostoja ja näyttämään, onko alennuksilla ja nimikeostoilla yhteyttä.|
|**Varaston kust.- ja &hintaluett.**|716|Tässä raportissa on luettelo hintatiedoista valittujen nimikkeiden tai varastointiyksiköiden osalta: välitön yksikkökustannus, viimeinen välitön kustannus, yksikköhinta, tuottoprosentti ja tuotto.|
|**Varasto – Saatavuussuunnitelma**|707|Jos haluat yleiskatsauksen tietyistä nimikkeistä tai varastointiyksiköistä ja niiden saatavuudesta. Tässä raportissa näkyvät kumulatiiviset arvot, esimerkiksi bruttotarpeet, aikataulutetut ja suunnitellut vastaanotot ja varasto. |
|**Varasto – Ostot toimittajilta**|714|Tässä raportissa näkyy luettelo toimittajista, joilta yrityksesi on ostanut nimikkeitä tietyn ajanjakson aikana. Se näyttää laskutetun määrän, summan ja alennuksen. Raporttia voidaan käyttää analysoimaan yrityksen nimikeostoja.|
|**Varaston ostotilaukset**|709|Tässä raportissa on luettelo toimittajalta tilatuista nimikkeistä. Siinä on myös oletettu vastaanottopäivämäärä, määrä ja jälkitoimitusten summa. Raporttia voidaan käyttää esimerkiksi katsomaan sitä, milloin nimikkeet tulisi vastaanottaa, ja tulisiko jälkitoimituksesta lähettää muistutus.|
|**Ostovarauksen saatavuus**|409|Tässä raportissa näkyy nimikkeiden saatavuus toimitusta varten ostoasiakirjoissa, esimerkiksi palautustilauksissa. Määritä, näkyykö raportissa kunkin asiakirjan vai kunkin ostorivin tila. <br>Raporttia tulostaessasi voit myös päivittää toimitukseen saatavilla olevan määrän ostorivien **Vastaanotettava määrä** -kenttään. Ostohyvityslaskuissa ja negatiivisilla ostotilausriveillä **Vastaanotettava määrä** -kenttä sisältää toimitettavan määrän. Tämän jälkeen raporttia voidaan käyttää määrittämään, mitkä asiakirjat toimitetaan. **Huomautus**: Tämä raportti ei ole käytettävissä varaston lisätoiminnoissa.|
<!--|**Toimittajan erääntymiserittely**|11006| Erityistä DACHille: Raportti, jota voi käyttää ostaneen osaston ryhmän johtaja ja kirjanpito-osasto. Tässä on yleiskuvaus maksamattomista toimittajalaskuista sisältäen eräpäivät, valuutat ja rahamäärät. Perusta on avoimet toimittajan kirjanpitotapahtumat.| -->

