---
title: Muutosten valvonta| Microsoft Docs
description: Voit aktivoida käyttäjälokin niin, että saat historiatiedot kaikista seurattujen taulukoiden tietoihin tehdyistä muutoksista. Voit seurata aktiviteetteja myös tietyn tyyppisillä toimintalokeilla.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: cb091a54b7b8da571117c807a621ed298842444c
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076657"
---
# <a name="auditing-changes-in-business-central"></a>Business Centralin tilintarkastuksen muutokset

Voit ottaa muutoslokin käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, joten saat käyttöösi toimintojen historian. Loki perustuu seuraamiesi taulukoiden tietoihin tehtyihin muutoksiin. **Muutoslokin tapahtumat** -sivulla tapahtumat järjestetään aikajärjestykseen. Sivulla näkyy muutokset, jotka tehdään määritettyjen taulukoiden kenttiin. Muutosloki kerää kaikki taulukkoon tehdyt muutokset.

> [!Important]
> Käyttäjän muutokset eivät näy **Muutoslokin tapahtumat** -sivulla ennen kuin käyttäjä istunto on käynnistetty uudelleen, mikä tapahtuu seuraavissa tilanteissa:
<br />
> * Istunto vanhentui ja se päivitettiin.
> * Käyttäjä valitsi toisen yrityksen tai roolikeskuksen.
> * Käyttäjä kirjautui ensin ulos ja sitten takaisin sisään.

## <a name="working-with-the-change-log"></a>Muutoslokin käyttäminen

Virheiden ja tietomuutosten lähteen paikallistaminen on yleinen ongelma monissa rahoitusjärjestelmissä. Kyseessä voi olla mikä tahansa väärästä asiakkaan puhelinnumerosta väärään pääkirjanpitokirjaukseen. Voit seurata muutoslokiin avulla kaikkia suoria muutoksia, joita käyttäjä tekee tietokannan tietoihin. Jokainen taulukko ja kenttä niissä pitää haluttaessa määrittää erikseen seurattavaksi, ja sitten loki tulee aktivoida.  

Voit aktivoida muutoslokin ja poistaa sen aktivoinnin **Muutoslokin asetukset** -sivulla. Kun käyttäjä aktivoi muutoslokin tai poistaa sen aktivoinnin, tämä aktiviteetti kirjataan, joten näet aina, kuka käyttäjistä poisti muutoslokin aktivoinnin tai aktivoi sen uudelleen.

Jos valitset **Muutoslokin asetukset** -sivulla **Taulukot**-toiminnon, voit määrittää sekä taulukot, joiden muutoksia seurataan, että seurattavat muutokset. [!INCLUDE[d365fin](includes/d365fin_md.md)] seuraa myös tiettyjä järjestelmätaulukoita.

Kun olet määrittänyt muutoslokin, aktivoinut sen ja muuttanut tietoja, voit tarkastella ja suodattaa muutoksia **Muutoslokin tapahtumat** -sivulla. Jos haluat poistaa merkintöjä, voit tehdä sen **Poista muutoslokin tapahtumat** -sivulla, jossa voit määrittää päivämääriin ja kellonaikaan perustuvia suodattimia.  

## <a name="working-with-activity-logs"></a>Toimintalokien käyttäminen

Joillakin [!INCLUDE [prodshort](includes/prodshort.md)]in sivuilla voi tarkastella toimintalokeja, joissa näkyy [!INCLUDE [prodshort](includes/prodshort.md)]ista vietävien ja sovellukseen tuotavien tiedostojen tila ja mahdolliset virheet.  

Tiedot näytetään **Toimintaloki**-sivulla sen kontekstin mukaan, josta ne avataan. Voit avata ikkunan esimerkiksi **Document Exchange -palvelun asetukset**-, **Saapuva asiakirja**-, **Kirjattu myyntilasku**- ja **Kirjattu myyntihyvityslasku** -sivuilta. Voit tyhjentää lokitapahtumaluettelon tai poistaa vain yli 7 päivää vanhemmat tapahtumat.  

## <a name="see-also"></a>Katso myös
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Lajitteleminen, hakeminen ja suodattaminen](ui-enter-criteria-filters.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
