---
title: Rakennetiedot – Saatavuus varastossa | Microsoft Docs
description: Järjestelmän on valvottava varaston nimikkeiden saatavuutta jatkuvasti, jotta lähtevät tilaukset toimitetaan tehokkaasti ja toimitukset saadaan halutussa ajassa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 184591134706432ed1ea04afa86e1274b748cfe0
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215501"
---
# <a name="design-details-availability-in-the-warehouse"></a>Rakennetiedot: saatavuus varastossa
Järjestelmän on valvottava varaston nimikkeiden saatavuutta jatkuvasti, jotta lähtevät tilaukset toimitetaan tehokkaasti ja toimitukset saadaan halutussa ajassa.  

Saatavuus vaihtelee riippuen varauksista lokerotasolla, kun varastotoiminnot, kuten poiminnat ja liikkeet ilmenevät ja kun varaston varausjärjestelmä asettaa noudatettavat rajoitukset. Varsin monimutkainen algoritmi tarkistaa, että kaikki edellytykset täyttyvät ennen kuin poimintojen määrät määritetään lähteville virroille.

Jos yksi tai useampi ehdoista ei täyty, erilaisia virheilmoituksia saattaa ilmestyä, mukaanlukien geneerinen "Ei mitään käsiteltävää." viesti. "Ei mitään käsiteltävää." viesti voi esiintyä monissa tapauksissa, niin lähtevän tai saapuvan virran kanssa, kun suorasti tai epäsuorasti asiaan liittyvä dokumentti sisältää kentän **Käsiteltävä Määrä**

> [!NOTE]
> Lisätietoja "Ei mitään käsiteltävää" viestin syistä ja sen ratkaisuista julkaistaan pian täällä. viesti.

## <a name="bin-content-and-reservations"></a>Lokeron sisältö ja varaukset  
 Kaikissa varastoinninhallinnan asennuksissa nimikkeen määrät ovat olemassa sekä fyysisen varastoinnin tapahtumina fyysisen varaston sovellusalueella että nimiketapahtumina varaston sovellusalueella. Nämä kaksi tapahtumatyyppiä sisältävät eri tiedot nimikkeiden sijainnista ja niiden saatavuudesta. Fyysisen varastoinnin tapahtumat määrittävät nimikkeen saatavuuden varastopaikan ja varastopaikan tyypin mukaan. Jälkimmäistä kutsutaan myös varastopaikan sisällöksi. Nimiketapahtumat määrittävät nimikkeen saatavuuden lähtevien asiakirjojen varauksen perusteella.  

 Erikoistoiminta on olemassa poiminta-algoritmissa ja sen avulla voidaan laskea määrä, joka on käytettävissä poimimiseen, kun säiliön sisältö on yhdistetty varauksiin.  

## <a name="quantity-available-to-pick"></a>Saatavilla oleva poimintamäärä  
 Jos poiminta-algoritmi ei esimerkiksi ota huomioon nimikkeiden määriä, jotka on varattu odottavalle myyntitilauksen toimitukselle, nämä nimikkeet saatetaan poimia toiselle myyntitilaukselle, joka toimitetaan aiemmin ja tämä estää ensimmäisen myynnin täyttämisen. Tämä tilanne vältetään, kun poiminta-algoritmi vähentää muille lähteville asiakirjoille varatut määrät, olemassa olevien poiminta-asiakirjojen määrät ja määrät, jotka on jo poimittu, mutta joita ei ole vielä toimitettu tai kulutettu.  

 Tulos näytetään **Saatav. ol. määrä poimittav.** -kentässä **Poimintatyökirja**-sivulla, jossa kenttä lasketaan dynaamisesti. Arvo lasketaan myös silloin, kun käyttäjä luo fyysisen varastoinnin poiminnat suoraan lähteville asiakirjoille. Tällaiset lähtevät asiakirjat voisivat olla myyntitilauksia, tuotantomenekkiä tai saapuvia siirtoja, joiden tulos näkyy liittyvissä määräkentissä, kuten **Käsiteltävä määrä**.  

> [!NOTE]  
>  Varausten prioriteettiin liittyen varattava määrä vähennetään poimittavissa olevasta määrästä. Esimerkiksi, jos poimintalokeroissa käytettävissä oleva määrä on 5 yksikköä, mutta 100 yksikköä on hyllytyslokeroissa, ja kun yrität varata enemmän kuin 5 yksikköä toiselle tilaukselle, järjestelmä näyttää virheilmoituksen, koska poimintalokeroissa on oltava tämä lisämäärä.  

### <a name="calculating-the-quantity-available-to-pick"></a>Lasketaan poimittavissa olevaa määrää  
 Poimintaan käytettävissä oleva määrä lasketaan seuraavasti:  

 poimittavissa olevaa määrää = määrä poimintavarastopaikoissa - määrä poiminnoissa ja siirroissa- – (varattu määrä poimintavarastopaikoissa + varattu määrä poiminnoissa ja siirroissa-)  

 Seuraava kaavio sisältää laskelman eri elementit.  

 ![Käytettävissä poimintaan, kun varaus on päällekkäinen](media/design_details_warehouse_management_availability_2.png "Käytettävissä poimintaan, kun varaus on päällekkäinen")  

## <a name="quantity-available-to-reserve"></a>Varattavissa oleva määrä  
 Koska lokeron sisältö ja varaus ovat olemassa, varattavien nimikkeiden määrä tulee kohdistaa varauksilla lähtevän fyysisen varastoinnin asiakirjoihin.  

 Kaikkien varastossa olevien nimikkeiden varaamisen tulisi olla mahdollista, lähtevien käsittelyssä olevia nimikkeitä lukuun ottamatta. Näin ollen varattavissa oleva määrä määritetään kaikissa asiakirjoissa ja kaikissa lokerotyypeissä olevana määränä, lukuun ottamatta seuraavia lähteviä määriä:  

-   Määrä rekisteröimättömissä poiminta-asiakirjoissa  
-   Varastopaikoissa oleva määrä  
-   Määrä tuotannon valmisteluvarastopaikoissa  
-   Määrä avoimissa tuotannon varastopaikoissa  
-   Määrä kokoonpanon valmisteluvarastopaikoissa  
-   Muutosvarastopaikoissa oleva määrä  

 Tulos näkyy **Saatavilla oleva kokonaismäärä** -kenttään **Varaus**-sivulla.  

 Varausrivillä oleva määrä, jota ei ole mahdollista varata, koska se on varattu varastossa, näytetään **F.var. kohdistettu määrä** -kentässä **Varaus**-sivulla.  

### <a name="calculating-the-quantity-available-to-reserve"></a>Lasketaan varattavissa olevaa määrää  
 Varattava määrä lasketaan seuraavasti:  

 varattavissa oleva määrää = kokonaismäärä varastossa - määrä poiminnoissa ja siirroissa lähdeasiakirjoille - varattu määrä - määrä lähtevien varastopaikoissa  

 Seuraava kaavio sisältää laskelman eri elementit.  

 ![Varattavissa varaston kohdistusta kohden](media/design_details_warehouse_management_availability_3.png "Varattavissa varaston kohdistusta kohden")  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
 [Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]