---
title: Nimikkeiden varaaminen | Microsoft Docs
description: Voit varata nimikkeitä myyntitilauksiin, ostotilauksiin ja tuotantotilauksiin. Voit varata nimikkeitä varastossa tai avoimien asiakirjarivien saapuvissa kohteissa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 6196fa9f090e13a2ce9217b5bf008b345e65e608
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785919"
---
# <a name="reserve-items"></a>Nimikkeiden varaaminen
Voit varata nimikkeitä myyntitilauksiin, ostotilauksiin, huoltotilauksiin, kokoonpanotilauksiin ja tuotantotilauksiin. Voit varata nimikkeitä varastossa tai avoimien asiakirja- tai päiväkirjarivien saapuvissa kohteissa. Käsittely tapahtuu **Varaus**-sivulla.

Jokaisella nimikkeiden varaamista varten avatulla **Varaus**-sivun rivillä on tietoja yhdestä rivin (myynti, osto, päiväkirja) tai varastotapahtuman tyypistä. Riveillä kuvataan, kuinka monta nimikettä on saatavilla varattavaksi kustakin rivin tai tapahtuman tyypistä.

## <a name="to-reserve-items-for-sales"></a>Nimikkeiden varaaminen myyntiä varten
Seuraavaksi käsitellään, miten nimikkeitä varataan myyntitilauksesta. Samat ohjeet koskevat osto-, huolto- ja kokoonpanotilauksia.  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.  
2.  Valitse myyntitilauksen **Rivit**-pikavälilehdessä **Varaa**-toiminto. **Varaus**-sivu avautuu.  
3. Napsauta riviä, jolta haluat varata nimikkeet.  
4. Valitse yksi seuraavista toiminnoista.  

    |**Funktiot**|**Kuvaus**|
    |------------------|---------------------|  
    |**Automaattinen varaus**|Nimikkeiden automaattinen varaaminen **Varaus**-sivulla.|  
    |**Varaa nykyiseltä riviltä**|Nimikkeiden varaaminen asiakirjasta valitsemaltasi riviltä.|  
    |**Peruuta varaus nykyiseltä riviltä**|Nimikkeiden varauksen peruuttaminen asiakirjasta valitsemaltasi riviltä.|

> [!NOTE]  
>  Jos myyntitilauksella on olemassa nimikkeen seurantarivejä, varausjärjestelmä ohjaa erikoistyövaiheiden läpi. Lisätietoja on kohdassa [Tietyn erä- tai sarjanumeron varaaminen](inventory-how-to-reserve-items.md#to-reserve-a-specific-serial-or-lot-number).  

## <a name="to-reserve-an-item-for-a-production-order-line"></a>Nimikkeiden varaaminen tuotantotilauksen rivejä varten  
Tuotantotilauksille voi varata nimikkeitä. Tuotantotilauksen rivit eli päänimike ja tuotantotilauksen komponentit on erotettava toisistaan.

Seuraavassa toimenpiteessä käytetään sitovasti suunniteltua tuotantotilausta.   
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sitovasti suunn. tuotantotil.** ja valitse sitten liittyvä linkki.  
2. Avaa sitovasti suunniteltu tuotantotilaus, jolle haluat varata päänimikkeitä.  
3. Valitse käsiteltävän tuotantotilauksen rivi.  
4. Valitse **Rivit**-pikavälilehdessä **Varaa**-toiminto.
5. Valitse **Varaus**-sivulla ensin **Myyntirivi, Tilaus** -rivi ja sitten **Varaa nykyiseltä riviltä** -toiminto.  

Ohjelma on nyt varannut määrän, joka oli syötetty sitovasti suunnitellun tuotantotilausriville.

## <a name="to-reserve-items-for-production-order-components"></a>Nimikkeiden varaaminen tuotantotilauksen komponentteja varten  
Tuotantotilauksille voi varata nimikkeitä. Tuotantotilauksen rivit eli päänimike ja tuotantotilauksen komponentit on erotettava toisistaan.

Seuraavassa toimenpiteessä käytetään sitovasti suunniteltua tuotantotilausta.    
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sitovasti suunn. tuotantotil.** ja valitse sitten liittyvä linkki.  
2. Avaa sitovasti suunniteltu tuotantotilaus, jolle haluat varata komponenttinimikkeitä.  
3. Valitse käsiteltävän tuotantotilauksen rivi.  
4. Valitse **Rivit**-pikavälilehdessä ensin **Rivi** ja sitten **Komponentit**.  
5. Valitse asianmukainen komponenttirivi.  
6. Valitse **Rivit**-pikavälilehdessä **Varaa**-toiminto.  
7. Valitse **Varaus**-sivulla ensin rivi ja sitten **Varaa nykyiseltä riviltä** -toiminto.  

Ohjelma on nyt varannut määrän, joka oli syötetty sitovasti suunnitellun tuotantokomponentin riville.

## <a name="to-change-a-reservation"></a>Varausten muuttaminen  
Joskus voit haluta muuttaa nimikevarausta.   
1. Valitse sen asiakirjarivin, jossa olet tehnyt varauksen, **Rivit** -pikavälilehdessä **Varaa**-toiminto.  
2. Valitse **Varaus**-sivulla **Varaustapahtumat**-toiminto.
3. Päivitä **Varaustapahtumat**-sivulla muutettavan rivin **Määrä**-kenttä.
4. Vahvista avautuva sanoma valitsemalla **OK**.

## <a name="to-cancel-a-reservation"></a>Varausten peruuttaminen  
Joskus voit haluta peruuttaa nimikevarauksen.   
1. Valitse sen asiakirjarivin, jossa tehdyn varauksen haluat peruuttaa, **Rivit** -pikavälilehdessä **Varaa**-toiminto.  
2. Valitse **Varaus**-sivulla **Varaustapahtumat**-toiminto.  
3.  Valitse **Varaustapahtumat**-sivulla **Peruuta varaus** -toiminto.  
4.  Vahvista avautuva sanoma valitsemalla **OK**.  

## <a name="to-reserve-a-specific-serial-or-lot-number"></a>Varaa tietty sarja- tai eränumero  
Nimikeseurannassa olevien nimikkeiden lähtevien asiakirjojen, kuten myyntitilausten tai tuotannon komponenttiluetteloiden, tiettyjä sarja- tai eränumeroita voi varata. Tämä voi olla tarpeen, jos esimerkiksi tarvitaan tietyn erän tuotanto-osia, jotta varmistetaan yhdenmukaisuus aiempien tuotantoerien kanssa, tai koska asiakas on pyytänyt tiettyä sarjanumeroa. Lisätietoja on kohdassa [Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md).

Tätä kutsutaan määritetyksi varaukseksi, koska varataan erään X kuuluvan nimikkeen X määrästä. Jos varataan vain nimikkeen X määristä, kyseessä on normaali, määrittämätön varaus. Lisätietoja on kohdassa [Rakennetiedot: Nimikkeen seuranta ja varaukset](design-details-item-tracking-and-reservations.md).

Seuraava toimenpide perustuu myyntitilaukseen.    
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.  
2. Luo myyntitilausrivi nimikeseurannassa olevalle nimikkeelle.  
3. Määritä sarja- ja eränumerot myyntitilausriville. Lisätietoja on kohdassa [Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md).
4. Valitse myyntitilausrivillä **Varaa**-toiminto.  
5. Valitse **Kyllä** varataksesi tietyt sarja- tai eränumerot.  
6. Valitse **Nimikeseurantaluettelo**-sivulla sarja- ja eränumeron yhdistelmä, jonka olet juuri määrittänyt.  
7. Valitse **OK**, jos haluat avata vain määritettyjen nimikkeen seurantanumeroiden tarjonnan näyttävän **Varaus**-sivun. Jos jollakin tälle riville määritetyllä nimikkeen seurantanumerolla on määrittämättömiä varauksia, saat ilmoituksen varatusta määrästä.  
8. Luo tiettyjen nimikkeen seurantanumeroiden varaus valitsemalla joko **Automaattinen varaus**- tai **Varaa nykyiseltä riviltä** -toiminto.

## <a name="see-also"></a>Katso myös
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Rakennetiedot: varaus, tilauksen seuranta ja toimenpiteiden viestitys](design-details-reservation-order-tracking-and-action-messaging.md)  
[Rakennetiedot – nimikkeen seuranta ja varaukset](design-details-item-tracking-and-reservations.md)  
[Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
