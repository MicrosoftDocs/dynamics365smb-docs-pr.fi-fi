---
title: Nimikkeiden varaaminen
description: 'Voit varata nimikkeitä myyntitilauksiin, ostotilauksiin ja tuotantotilauksiin. Voit myös varata nimikkeitä varastossa tai avoimien asiakirjarivien saapuvissa kohteissa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '498, 497'
ms.date: 08/11/2022
ms.author: bholtorf
---
# Nimikkeiden varaaminen

Voit varata nimikkeitä myyntitilauksiin, ostotilauksiin, huoltotilauksiin, kokoonpanotilauksiin, siirtotilauksiin ja tuotantotilauksiin. Voit myös varata nimikkeitä varastossa tai avoimien asiakirja- tai päiväkirjarivien saapuvissa kohteissa. Tämä tehdään **Varaus**-sivulla.

Jokaisella nimikkeiden varaamista varten avatulla **Varaus**-sivun rivillä on tietoja yhdestä rivin (myynti, osto, päiväkirja) tai varastotapahtuman tyypistä. Riveillä kuvataan, kuinka monta nimikettä on saatavilla varattavaksi kustakin rivin tai tapahtuman tyypistä.

## Varaa nimikkeitä myyntiä varten

Seuraava toiminto käsittelee, miten nimikkeitä varataan myyntitilauksesta. Samat ohjeet koskevat osto-, huolto-, siirto- ja kokoonpanotilauksia.
  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset**, valitse sitten vastaava linkki.  
2. Valitse myyntitilaus.
3. Valitse **Rivit**-pikavälilehdessä **Varaa**-toiminto. **Varaus**-sivu avautuu.  
4. Napsauta riviä, jolta haluat varata nimikkeet.  
5. Valitse yksi seuraavista toiminnoista.  

    |**Funktiot**|**Kuvaus**|
    |------------------|---------------------|  
    |**Automaattinen varaus**|Nimikkeiden automaattinen varaaminen **Varaus**-sivulla.|  
    |**Varaa nykyiseltä riviltä**|Nimikkeiden varaaminen asiakirjasta valitsemaltasi riviltä.|  
    |**Peruuta varaus nykyiseltä riviltä**|Nimikkeiden varauksen peruuttaminen asiakirjasta valitsemaltasi riviltä.|

> [!NOTE]  
> Jos myyntitilauksella on olemassa nimikkeen seurantarivejä, varausjärjestelmä ohjaa erikoistyövaiheiden läpi. Lue lisää [Tietyn erä- tai sarjanumeron varaaminen](inventory-how-to-reserve-items.md#reserve-a-specific-serial-or-lot-number) -osasta.  

## Varaa nimikkeitä tuotantotilauksen rivejä varten

Tuotantotilauksille voi varata nimikkeitä. Tuotantotilauksen rivit eli päänimike ja tuotantotilauksen komponentit on erotettava toisistaan.

Seuraavassa toimenpiteessä käytetään sitovasti suunniteltua tuotantotilausta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sitovasti suun. tuotantotil.**, valitse sitten vastaava linkki.  
2. Avaa sitovasti suunniteltu tuotantotilaus, jolle haluat varata päänimikkeitä.  
3. Valitse käsiteltävän tuotantotilauksen rivi.  
4. Valitse **Rivit**-pikavälilehdessä **Varaa**-toiminto.
5. Valitse **Varaus**-sivulla ensin **Myyntirivi, Tilaus** -rivi, sitten **Varaa nykyiseltä riviltä** -toiminto.  

Ohjelma on nyt varannut määrän, joka oli syötetty sitovasti suunnitellun tuotantotilausriville.

## Varaa nimikkeitä tuotantotilauksen komponentteja varten

Tuotantotilauksille voi varata nimikkeitä. Tuotantotilauksen rivit eli päänimike ja tuotantotilauksen komponentit on erotettava toisistaan.

Seuraavassa toimenpiteessä käytetään sitovasti suunniteltua tuotantotilausta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sitovasti suun. tuotantotil.**, valitse sitten vastaava linkki.  
2. Avaa sitovasti suunniteltu tuotantotilaus, jolle haluat varata komponenttinimikkeitä.  
3. Valitse käsiteltävän tuotantotilauksen rivi.  
4. Valitse **Rivit**-pikavälilehdessä ensin **Rivi**, sitten **Komponentit**.  
5. Valitse asianmukainen komponenttirivi.  
6. Valitse **Rivit**-pikavälilehdessä **Varaa**-toiminto.  
7. Valitse **Varaus**-sivulla ensin rivi, sitten **Varaa nykyiseltä riviltä** -toiminto.  

Ohjelma on nyt varannut määrän, joka oli syötetty sitovasti suunnitellun tuotantokomponentin riville.

## Muuta varausta

Joskus voit haluta muuttaa nimikevarausta.

1. Valitse sen asiakirjarivin, jossa olet tehnyt varauksen, **Rivit** -pikavälilehdessä **Varaa**-toiminto.  
2. Valitse **Varaus**-sivulla **Varaustapahtumat**-toiminto.
3. Päivitä **Varaustapahtumat**-sivulla muutettavan rivin **Määrä**-kenttä.
4. Vahvista avautuva sanoma valitsemalla **OK**.

## Peruuta varaus

Joskus voit haluta peruuttaa nimikevarauksen.

1. Valitse sen asiakirjarivin, jossa tehdyn varauksen haluat peruuttaa, **Rivit** -pikavälilehdessä **Varaa**-toiminto.  
2. Valitse **Varaus**-sivulla **Varaustapahtumat**-toiminto.  
3. Valitse **Varaustapahtumat**-sivulla **Peruuta varaus** -toiminto.  
4. Vahvista avautuva sanoma valitsemalla **Kyllä**.  

## Varaa tietty sarja- tai eränumero

Nimikeseurannassa olevien nimikkeiden lähtevien asiakirjojen, kuten myyntitilausten tai tuotannon komponenttiluetteloiden, tiettyjä sarja- tai eränumeroita voi varata. Tämä voi olla tarpeen, jos esimerkiksi tarvitaan tietyn erän tuotanto-osia, jotta varmistetaan yhdenmukaisuus aiempien tuotantoerien kanssa, tai koska asiakas on pyytänyt tiettyä sarjanumeroa. Lue lisää kohdassa [Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md).

Tätä käytäntöä kutsutaan määritetyksi varaukseksi, koska varataan erään X kuuluvan nimikkeen X määrästä. Sitä vastoin jos varataan vain nimikkeen X määristä, kyseessä on yksinkertaisesti normaali, määrittämätön varaus. Lisätietoja kohdassa [Rakennetiedot – Nimikkeen seuranta ja varaukset](design-details-item-tracking-and-reservations.md).

Seuraava toimenpide perustuu myyntitilaukseen.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Luo myyntitilausrivi nimikeseurannassa olevalle nimikkeelle.  
3. Määritä sarja- ja eränumerot myyntitilausriville. Lue lisää kohdassa [Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md).
4. Valitse myyntitilausrivillä **Varaa**-toiminto.  
5. Valitse **Kyllä** varataksesi tietyt sarja- tai eränumerot.  
6. Valitse **Nimikeseurantaluettelo**-sivulla sarja- ja eränumeron yhdistelmä, jonka olet määrittänyt.  
7. Valitse **OK**, jos haluat avata vain määritettyjen nimikkeen seurantanumeroiden tarjonnan näyttävän **Varaus**-sivun. Jos jollakin tälle riville määritetyllä nimikkeen seurantanumerolla on määrittämättömiä varauksia, saat ilmoituksen varatusta määrästä.  
8. Luo tiettyjen nimikkeen seurantanumeroiden varaus valitsemalla joko **Automaattinen varaus**- tai **Varaa nykyiseltä riviltä** -toiminto.

## Katso myös

[Varasto](inventory-manage-inventory.md)  
[Rakennetiedot: Varaus, tilauksen seuranta ja toimintojen viestintä](design-details-reservation-order-tracking-and-action-messaging.md)  
[Rakennetiedot: nimikkeen seuranta ja varaukset](design-details-item-tracking-and-reservations.md)  
[Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
