---
title: "Rakennetiedot – Saatavuus varastossa | Microsoft Docs"
description: "Järjestelmän on valvottava varaston nimikkeiden saatavuutta jatkuvasti, jotta lähtevät tilaukset toimitetaan tehokkaasti ja toimitukset saadaan halutussa ajassa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 5fd4bedcef6fcec79b1b2c8744c7c08d8170d97e
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="design-details-availability-in-the-warehouse"></a>Rakennetiedot: saatavuus varastossa
Järjestelmän on valvottava varaston nimikkeiden saatavuutta jatkuvasti, jotta lähtevät tilaukset toimitetaan tehokkaasti ja toimitukset saadaan halutussa ajassa.  

 Saatavuus vaihtelee riippuen varauksista lokerotasolla, kun varastotoiminnot, kuten poiminnat ja liikkeet ilmenevät ja kun varaston varausjärjestelmä asettaa noudatettavat rajoitukset. Varsin monimutkainen algoritmi tarkistaa, että kaikki edellytykset täyttyvät ennen kuin poimintojen määrät määritetään lähteville virroille.  

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

 ![Poimittavissa, varauksen päällekkäisyys](media/design_details_warehouse_management_availability_2.png "Poimittavissa, varauksen päällekkäisyys")  

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

 ![Varattavissa varaston kohdistusten mukaisesti](media/design_details_warehouse_management_availability_3.png "Varattavissa varaston kohdistusten mukaisesti")  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)

