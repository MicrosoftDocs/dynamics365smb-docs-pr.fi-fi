---
title: Myynnin toimituspäivämäärän laskeminen
description: 'Sovellus laskee automaattisesti päivämäärän, jolloin nimike on tilattava sen saamiseksi tietyn päivän varastoon ja poimittavaksi.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 03/06/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Myynnin toimituspäivämäärän laskeminen

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

Jos pyydettyä toimituspäivämäärää ei ole määritetty myyntitilausrivillä tai jos toimitus ei onnistu pyydettynä toimituspäivämääränä, lasketaan varhaisin päivämäärän, jolloin nimikkeet ovat saatavilla. Tämä päivämäärä syötetään sitten rivin **Toimituspvm**-kenttään. Nimikkeille lasketaan seuraavilla kaavoilla suunniteltu lähetyspäivämäärä ja päivämäärä, jolloin ne toimitetaan asiakkaalle:

- *Suunniteltu toimituspvm = lähtevä f.var. käsittelyaika + toimituspäivä*
- *suunniteltu lähetyspvm + toimitusaika = suunniteltu toimituspvm*

## Katso myös

[Ostojen päivämäärien laskeminen](purchasing-date-calculation-for-purchases.md)  
[Toimituksen lupaamisen päivämäärien laskeminen](sales-how-to-calculate-order-promising-dates.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
