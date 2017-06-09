---
title: Muutosten kirjaaminen Dynamics 365 for Financialsissa | Microsoft Docs
description: "Kirjaa käyttäjien tekemät muutokset."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 03/04/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 470931febc303ace8fa1e8015453c20b587762b0
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="logging-changes-in-dynamics-365-for-financials"></a>Muutosten kirjaaminen Dynamics 365 for Financialsissa
Voit ottaa muutoslokin käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, joten saat käyttöösi toimintojen historian. Loki perustuu seuraamiesi taulukoiden tietoihin tehtyihin muutoksiin. Muutoslokissa tapahtumat järjestetään aikajärjestykseen. Se näyttää muutokset, jotka tehdään määritettyjen taulukoiden kenttiin. Muutosloki kerää kaikki taulukkoon tehdyt muutokset.  

## <a name="working-with-the-change-log"></a>Muutoslokin käyttäminen
Virheiden ja tietomuutosten lähteen paikallistaminen on yleinen ongelma monissa rahoitusjärjestelmissä. Kyseessä voi olla mikä tahansa väärästä asiakkaan puhelinnumerosta väärään pääkirjanpitokirjaukseen. Voit seurata muutoslokiin avulla kaikkia suoria muutoksia, joita käyttäjä tekee tietokannan tietoihin. Jokainen taulukko ja kenttä niissä pitää haluttaessa määrittää erikseen seurattavaksi, ja sitten loki tulee aktivoida.  

Voit aktivoida muutoslokin ja poistaa sen aktivoinnin **Muutoslokin asetukset** -ikkunassa. Kun aktivoit muutoslokin tai poistat sen aktivoinnin, tämä aktiviteetti kirjataan, joten näet aina, kuka käyttäjistä poisti muutoslokin aktivoinnin tai aktivoi sen uudelleen. Tätä ominaisuutta ei voi ottaa pois käytöstä.  

Jos valitset **Muutoslokin asetukset** -ikkunassa **Taulukot**-toiminnon, voit määrittää, minkä taulukoiden muutoksia seurataan ja mitä muutoksia seurataan. [!INCLUDE[d365fin](includes/d365fin_md.md)] seuraava myös tiettyjä järjestelmätaulukoita.

Kun olet määrittänyt muutoslokin, aktivoinut sen ja muuttanut tietoja, voit tarkastella ja suodattaa muutoksia **Muutoslokin tapahtumat** -ikkunassa. Jos haluat poistaa merkintöjä, voit tehdä sen **Poista muutoslokin tapahtumat** -ikkunassa, jossa voit määrittää päivämääriin ja kellonaikaan perustuvia suodattimia.  

## <a name="see-also"></a>Katso myös
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Lajittelu](ui-sorting.md)  
[Etsi sivua tai raporttia -toiminnon käyttäminen](ui-search.md)  
[Toimintaohje: Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  

