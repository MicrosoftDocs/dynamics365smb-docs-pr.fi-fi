---
title: Myynnin toimituspäivämäärän laskenta
description: 'Sovellus laskee automaattisesti päivämäärän, jolloin nimike on tilattava sen saamiseksi tietyn päivän varastoon ja poimittavaksi.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/22/2022
ms.author: bholtorf
---
# Myynnin toimituspäivämäärän laskenta

[!INCLUDE[prod_short](includes/prod_short.md)] laskee automaattisesti varhaisimman mahdollisen päivämäärän, jolloin myyntitilausrivin nimike voidaan toimittaa.

* Jos asiakas on pyytänyt tietyn toimituspäivämäärän, ohjelma laskee päivämäärän, jolloin nimikkeiden tulee olla poimittavissa, jotta toimitus onnistuu sinä päivänä.
* Jos asiakas ei pyydä tiettyä toimituspäivämäärää, lasketaan päivämäärä, jona nimikkeet voidaan toimittaa. Laskenta alkaa päivämäärästä, jona nimikkeet ovat saatavilla poimintaa varten.

## Pyydetyn toimituspäivämäärän laskeminen

Jos myyntitilausrivillä on pyydetty toimitusottopäivämäärä, ohjelma käyttää tätä päivämäärää lähtökohtana seuraaville laskennoille:

- *Pyydetty toimituspvm - Toimitusaika = Suunniteltu lähetyspvm*
- *Suunniteltu toimituspvm - Lähtevä f.var. käsittelyaika = Toimituspäivä*

Jos nimikkeet ovat poimittavissa lähetyspäivämääränä, myyntiprosessi voi jatkua. Muussa tapauksessa näytetään varaston loppumisvaroitus.

> [!NOTE]
> Jos prosessi perustuu taaksepäin laskentaan ja esimerkiksi toimituspäivä saadaan käyttämällä suunniteltua toimituspäivää, on suositeltavaa käyttää päivämääräkaavoja, joiden kesto on kiinteä. Sellainen on esimerkiksi 5P viidelle päivälle tai 1V yhdelle viikolle. Päivämääräkaava, jonka kesto ei ole kiinteä, kuten KV kuluvalle viikolle tai KK kuluvalle kuukaudelle, voi aiheuttaa virheellisiä päivämäärälaskelmia. Lisätietoja päivämääräkaavoista on kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).

## Varhaisimman mahdollisen toimituspäivämäärän laskeminen

Jos et ole määrittänyt pyydettyä toimituspäivämäärää myyntitilausrivillä tai jos toimitus ei onnistu pyydettynä toimituspäivämääränä, ohjelma laskee varhaisimman päivämäärän, jolloin nimikkeet ovat saatavilla. Sen jälkeen ohjelma syöttää tämän päivämäärän rivin **Toimituspvm**-kenttään ja laskee päivämäärän, jolloin nimikkeet suunnitellaan lähetettävän, ja päivämäärän, jolloin ne toimitetaan asiakkaalle, seuraavien laskukaavojen mukaan:

- *Suunniteltu toimituspvm = lähtevä f.var. käsittelyaika + toimituspäivä*
- *suunniteltu lähetyspvm + toimitusaika = suunniteltu toimituspvm*

## Katso myös

[Ostojen päivämäärien laskeminen](purchasing-date-calculation-for-purchases.md)  
[Toimituksen lupaamisen päivämäärien laskeminen](sales-how-to-calculate-order-promising-dates.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
