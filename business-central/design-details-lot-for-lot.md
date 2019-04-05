---
title: Rakennetiedot – erä-erästä | Microsoft Docs
description: Lisätietoja erä-erästä-käytännön käyttämisestä tarveperustaisen tilausmäärän laskemisesta.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 7bc65fdb33b94b313b7d2b5b046156ca1d0788a2
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795560"
---
# <a name="design-details-lot-for-lot"></a>Rakennetiedot: erä-erästä
Erä erästä -toiminto on kaikkein joustavin, koska järjestelmä reagoi vain ajankohtaiseen kysyntään, ja se toimii ennakkokysyntänä ennusteesta ja kestotilauksista, ja ratkaisee sitten tilausmäärän perustuen kysyntään. Erä erästä -toiminto on kohdistettu A- ja B-nimikkeille, joissa varasto voidaan hyväksyä, mutta tätä tulee välttää.  

Monilla tavoilla erä-erästä käytäntö näyttää tilauskäytännöltä, mutta sillä on yleinen lähestymistapa nimikkeisiin – se voi hyväksyä varastossa olevat määrät ja se kokoaa kysynnän ja vastaavan tarjonnan käyttäjän määrittämiin aikaväleihin.  

Aikaväli määritetään **Aikaväli**-kentässä. Järjestelmän käyttämä pienin aikaväli on yksi päivä. Se on kysyntä- ja tarjontatapahtumien ajan pienin mittayksikkö järjestelmässä. Käytännössä tosin tuotantotilausten ja komponenttitarpeiden ajan mittayksikkö voidaan määrittää sekunteina.  

Aikaväli määrittää myös rajat sille, milloin olemassa oleva toimitustilaus on ajoitettava uudelleen annettua kysyntää vastaavaksi. Jos tarjonta sijoittuu aikavälille, se aikataulutetaan uudelleen sisään tai ulos kysynnän täyttämiseksi. Muussa tapauksessa, jos se on aiemmin, se aiheuttaa tarpeetonta varaston kerääntymistä ja se tulisi peruuttaa. Jos se on myöhemmin, uusi toimitustilaus luodaan sen sijaan.  

Tämän käytännön avulla voi myös määrittää varmuusvaraston mahdollisten tarjonnan vaihteluiden kompensointia tai äkillisen kysynnän täyttämistä varten.  

Koska toimitustilauksen määrä perustuu todelliseen kysyntään, voi olla järkevää käyttää tilauksen muuttujakenttiä: pyöristä tilausmäärä ylös tietyn tilauskerrannaisen määrittämiseksi (tai mitan ostoyksikön), kasvata tilausta tiettyyn tilauksen vähimmäismäärään tai vähennä määrää määritettyyn enimmäismäärään (ja luo näin kaksi tai useampia toimituksia vaadittavan kokonaismäärän saavuttamiseksi).  

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: uusintatilauskäytännöt](design-details-reordering-policies.md)   
[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)   
[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)
