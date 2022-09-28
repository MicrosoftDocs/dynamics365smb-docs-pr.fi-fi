---
title: Myynnin päivämäärälaskenta
description: Sovellus laskee automaattisesti päivämäärän, jolloin nimike on tilattava sen saamiseksi tietyn päivän varastoon ja poimittavaksi.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 538392cd86dfc348877e8ef349d42a8961934262
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532563"
---
# <a name="date-calculation-for-sales"></a>Myynnin päivämäärälaskenta

[!INCLUDE[prod_short](includes/prod_short.md)] laskee automaattisesti varhaisimman mahdollisen päivämäärän, jolloin myyntitilausrivin nimike voidaan toimittaa.

Jos asiakas on pyytänyt tietyn toimituspäivämäärän, ohjelma laskee päivämäärän, jolloin nimikkeiden tulee olla poimittavissa, jotta toimitus onnistuu sinä päivänä.

Jos asiakas ei pyydä tiettyä toimituspäivämäärää, ohjelma laskee päivämäärän, jolloin nimikkeet voidaan toimittaa alkaen siitä päivästä, jolloin nimikkeet ovat poimittavissa.

## <a name="calculating-a-requested-delivery-date"></a>Laskeminen ilman pyydettyä toimituspäivämäärää

Jos myyntitilausrivillä on pyydetty toimitusottopäivämäärä, ohjelma käyttää tätä päivämäärää lähtökohtana seuraaville laskennoille:

- Pyydetty toimituspvm - Toimitusaika = Suunniteltu lähetyspvm
- Suunniteltu toimituspvm - Lähtevä f.var. käsittelyaika = Toimituspäivä

Jos nimikkeet ovat poimittavissa lähetyspäivämääränä, myyntiprosessi voi jatkua. Muussa tapauksessa näytetään varaston loppumisvaroitus.

> [!Note]
> Jos prosessi perustuu taaksepäin laskentaan ja esimerkiksi toimituspäivä saadaan käyttämällä suunniteltua toimituspäivää, on suositeltavaa käyttää päivämääräkaavoja, joiden kesto on kiinteä. Sellainen on esimerkiksi 5P viidelle päivälle tai 1V yhdelle viikolle. Päivämääräkaava, jonka kesto ei ole kiinteä, kuten KV kuluvalle viikolle tai KK kuluvalle kuukaudelle, voi aiheuttaa virheellisiä päivämäärälaskelmia. Lisätietoja päivämääräkaavoista on kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).

## <a name="calculating-the-earliest-possible-delivery-date"></a>Varhaisimman mahdollisen toimituspäivämäärän laskeminen

Jos myyntitilausrivillä ei ole pyydettyä toimituspäivämäärää, tai jos toimitus ei onnistu pyydettynä toimituspäivämääränä, ohjelma etsii varhaisimman päivämäärän, jolloin nimikkeet ovat saatavilla. Sen jälkeen ohjelma syöttää tämän päivämäärän rivin Toimituspvm -kenttään ja laskee päivämäärän, jolloin nimikkeet suunnitellaan lähetettävän, ja päivämäärän, jolloin ne toimitetaan asiakkaalle, seuraavien laskukaavojen mukaan:

- Suunniteltu toimituspvm = lähtevä f.var. käsittelyaika + toimituspäivä
- Suunniteltu toimituspvm + toimitusaika = suunniteltu toimituspvm

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/promising-sales-order-delivery-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

 [Ostojen päivämäärälaskenta](purchasing-date-calculation-for-purchases.md)  
 [Toimituksen lupaamisen päivämäärien laskeminen](sales-how-to-calculate-order-promising-dates.md)  
 [Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
