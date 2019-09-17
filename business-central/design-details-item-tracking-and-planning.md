---
title: Rakennetiedot – Nimikkeen seuranta ja suunnittelu | Microsoft Docs
description: Nimikkeen seurantanumerot on sovitettu täysin yhteen tilausseurannan tietueiden kanssa, koska ne ovat tallennettu varausjärjestelmään.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/20/2019
ms.author: sgroespe
ms.openlocfilehash: 062cee5473de267a479bc76e166ed85948544a51
ms.sourcegitcommit: 81b6062194bf04d8052a3cd394cc0b41e3f53e6d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/20/2019
ms.locfileid: "1887666"
---
# <a name="design-details-item-tracking-and-planning"></a>Rakennetiedot: nimikkeen seuranta ja suunnittelu
Nimikkeen seurantanumerot on sovitettu täysin yhteen tilausseurannan tietueiden kanssa, koska ne ovat tallennettu varausjärjestelmään. Tämä tarkoittaa sitä, että nimikkeille, joilla on tilauksen seurantatietueet, voidaan määrittää nimikkeen seurantanumerot. Käänteisesti, seurantanumerot omaavat nimikkeet voivat muuttua tilauksen seurantatietueiksi. Lisätietoja on kohdassa [Rakennetiedot: nimikeseurannan rakenne](design-details-item-tracking-design.md).

Lisätietoja integroiduista järjestelmistä on kohdassa [Rakenteen tiedot: varaukset, tilauksen seuranta ja toimenpiteiden viestitys](design-details-reservation-order-tracking-and-action-messaging.md).

Koska tilauksen seuranta koskee vain tietyn nimikkeen sovellusta, koordinointi nimikkeen seurantanumeroilla kohdistuu ainoastaan nimikkeisiin, jotka on asetettu käyttämään tiettyä nimikeseurantaa. Tämä määritetään nimikekortin **SN-kohtainen seuranta**- ja **Eräkohtainen seuranta** -kentissä. Niissä määritetään seuraavat tiedot:

- Nimikkeellä tulee olla samaa sarja- tai eränumero, kun se kirjataan.
- Nimikkeen tulee käyttää samaa sarja- tai eränumeroa, kun se kirjataan lähteväksi.

Vakiotarjonnan/-kysynnän täsmäytysperiaatteiden mukaisesti suunnittelujärjestelmä ja liittyvä tilauksen seurannan ominaisuus kohdistavat vain tarjonnan ja kysynnän, joilla on nimikkeen seurantanumerot, jos kyseinen nimike käyttää tiettyä nimikeseurantaa. Kaikissa muissa tapauksissa suunnittelu- ja seurantajärjestelmät ohittavat nimikkeen seurantanumerot, kun ne asettavat tarjonnan vastaamaan kysyntää tai kysynnän vastaamaan tarjontaa. Lisätietoja on kohdassa [Rakennetiedot: varaus, tilauksen seuranta ja toimenpiteiden viestitys](design-details-reservation-order-tracking-and-action-messaging.md).

Kun tietyllä nimikkeellä on esimerkiksi tilauksen seuranta, se merkitsee sitä, että nimikkeen tietueet ovat jo **Varaustapahtuma**-taulukossa. Se on varausjärjestelmän ydin ennen nimikkeen seurantanumeroiden määrittämistä. Tämän vuoksi seuraavat yhdistämisrajoitukset koskevat seurattavan tilauksen nimikeseurannan numeroita:

- Sarja- tai eränumerolla varustettu kysyntä voi kattaa vain tarjonnan, jolla on sama sarja- tai eränumero.
- Kysyntä, jolla ei ole sarja- tai eränumeroa, voi kattaa minkä tahansa tarjonnan. Tarjonnalla voi olla sarja- tai eränumero, mutta ei välttämättä.

Riippumatta vaikutuksesta dynaamiseen tilausten seurantaan, nimikeseurannan rajoitukset eivät vaikuta merkittävästi suunnittelujärjestelmään.

Tarjonnassa sarja- tai eränumeroa ei tavallisesti syötetä välittömästi ennen kuin tilaus kirjataan esimerkiksi ostovastaanottona fyysiseen varastoon. Kun syötät sarja- tai eränumeron kysynnässä esimerkiksi myyntitilaukseen, numero löytyy jo varastosta. Tästä syystä nimikkeen seurantanumerot eivät ole tavallisesti ongelma tarjonnan suunnittelussa.

Erityistä nimikeseurantaa käyttävien nimikkeiden osalta kaikki sarja- tai eränumeroilla merkitty kysyntä tulee kohdistaa vastaavan tarjonnan kanssa. Useimmissa tapauksissa tietyn sarja- tai eränumeron uudelleenjärjestäminen ei ole järkevää, joten tämä ei todennäköisesti vaikuta oston tai tuotannon tarjonnan suunnitteluun. Siirrettäessä nimikkeitä sijainnista toiseen on kuitenkin todennäköistä, että siirto kohdistuu tiettyyn erään, joten siirtotoimitusten suunnitteluun saattaa vaikuttaa tietty yhdistämisrajoitus.

Lisätietoja on kohdassa [Rakennetiedot: siirrot suunnittelussa](design-details-transfers-in-planning.md).

## <a name="balancing-demand-and-supply"></a>Kysynnän ja tarjonnan täsmäytys
Jos nimike vaatii tietyn nimikeseurannan, tilauksen seurantalinkki luodaan koko nimikeseurannan kysynnästä mihin tahansa vastaavan nimikeseurannan tarjontaan. Ainoa rajoitus on, että tarjonnan tulee olla ennen kysyntää. Jos näissä olosuhteissa ei löydy nimikeseurantakohtaista kysyntää vastaavaa nimikeseurannan tarjontaa, järjestelmä luo välittömästi uuden nimikeseurannan tarjonnan huomioimatta tilauksen kokoa, suunnitteluparametreja tai olemassa olevan saman sarja- tai eränumeron tarjonnan uudelleen aikatauluttamista.

Jos nimikkeen seurantanumerot on määritetty kysynnälle tai tarjonnalle ilman erityistä nimikeseurantaa, tilauksen seurantalinkki on luotu kysynnästä tähän tarjontaan perustuen sopivimpaan ajoitukseen ja määrään, kuten tavallisessa täsmäytyksessä. Määritetty nimikkeen seurantanumero siirtyy tilaustenseurantatietueeseen samalla tavalla kuin mikä tahansa määritetty nimikeseurannan määrä määrittää yhden lopputilauksen seurantalinkin. Tämä tarkoittaa sitä, että syötetty nimikkeen seurantanumero säilytetään samalla, kun se on osa tilauksen seurantatietuetta.

Jos nimikkeen seurantanumerot määritetään tarjonnalle ilman erityisen nimikkeen seurantaa, suunnittelujärjestelmä katsoo tämän tarjonnan olevan kiinteää. Tälle tarjonnalle ei ehdoteta koon tai aikataulun muuttamista, mutta tarjonta otetaan huomioon, kun suunnittelujärjestelmä yrittää täyttää bruttovaatimukset.

Lisätietoja on kohdassa [Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md).  

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: nimikkeen seurannan rakenne](design-details-item-tracking-design.md)  
[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)  
[Rakennetiedot: varaus, tilauksen seuranta ja toimenpiteiden viestitys](design-details-reservation-order-tracking-and-action-messaging.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)  
