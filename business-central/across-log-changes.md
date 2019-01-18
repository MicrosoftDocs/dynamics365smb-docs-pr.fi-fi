---
title: "Käyttäjätoimien seuraaminen muutoslokissa | Microsoft Docs"
description: "Voit aktivoida käyttäjälokin niin, että saat historiatiedot kaikista seurattujen taulukoiden tietoihin tehdyistä muutoksista."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 11/14/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 2a95e770f0b78732723ba0d9db5d343a3ed3a97f
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="logging-changes-in-business-central"></a>Business Central -sovelluksen muutosten kirjaaminen lokiin

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

## <a name="see-also"></a>Katso myös
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Lajittelu](ui-sorting.md)  
[Etsi sivua tai raporttia -toiminnon käyttäminen](ui-search.md)  
[Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

