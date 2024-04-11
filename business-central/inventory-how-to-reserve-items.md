---
title: Nimikkeiden varaaminen
description: 'Lue lisää nimikkeiden varaamisesta myyntitilauksiin, ostotilauksiin ja tuotantotilauksiin.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: null
ms.search.forms: '498, 497'
ms.date: 02/22/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="reserve-items"></a>Nimikkeiden varaaminen

Voit varata nimikkeitä myyntitilauksiin, ostotilauksiin, huoltotilauksiin, kokoonpanotilauksiin, siirtotilauksiin ja tuotantotilauksiin. Voit myös varata nimikkeitä varastossa tai avoimien asiakirja- tai päiväkirjarivien saapuvissa kohteissa. Tämä tehdään **Varaus**-sivulla.

Jokaisella nimikkeiden varaamista varten avatulla **Varaus**-sivun rivillä on tietoja yhdestä rivin (myynti, osto, päiväkirja) tai varastotapahtuman tyypistä. Riveillä kuvataan, kuinka monta nimikettä on saatavilla varattavaksi kustakin rivin tai tapahtuman tyypistä.

> [!TIP]
> Varastossa varaamiesi määrien perusteella [!INCLUDE [prod_short](includes/prod_short.md)] näyttää asiakirjoissa tilan, josta tiedät nopeasti seuraavan vaiheen. Näkyvissä voi esimerkiksi olla, että voit toimittaa myyntitilauksen tai aloittaa projektin, kokoonpanon tai tuotantotilauksen käsittelemisen. Tila auttaa myös vähentämään osittaisten toimitusten tai viivytysten vaaraa, joka johtuu puuttuvasta varastosta tuotanto- ja kokoonpanotilausten osalta.
>
> **Varattu varastosta** -kenttä voi auttaa sinua ymmärtämään, voiko tietyn tilauksen tai tilausrivin toimittaa vai poimia. Riveillä Varattu varastosta -kenttä on käytettävissä tietoruuduissa. Saat koko tilauksen tiedot näyttöön, kun kenttä on **Tilasto**-sivulla.

## <a name="reserve-items-for-sales"></a>Varaa nimikkeitä myyntiä varten

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

## <a name="reserve-an-item-for-a-production-order-line"></a>Varaa nimikkeitä tuotantotilauksen rivejä varten

Tuotantotilauksille voi varata nimikkeitä. Tuotantotilauksen rivit eli päänimike ja tuotantotilauksen komponentit on erotettava toisistaan.

Seuraavassa toimenpiteessä käytetään sitovasti suunniteltua tuotantotilausta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sitovasti suun. tuotantotil.**, valitse sitten vastaava linkki.  
2. Avaa sitovasti suunniteltu tuotantotilaus, jolle haluat varata päänimikkeitä.  
3. Valitse käsiteltävän tuotantotilauksen rivi.  
4. Valitse **Rivit**-pikavälilehdessä **Varaa**-toiminto.
5. Valitse **Varaus**-sivulla ensin **Myyntirivi, Tilaus** -rivi, sitten **Varaa nykyiseltä riviltä** -toiminto.  

Ohjelma on nyt varannut määrän, joka oli syötetty sitovasti suunnitellun tuotantotilausriville.

## <a name="reserve-items-for-production-order-components"></a>Varaa nimikkeitä tuotantotilauksen komponentteja varten

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

## <a name="reserve-items-in-bulk"></a>Varaa nimikkeitä joukkotoimintona

Varaa ja kohdista saapuvat tavarat joukkotoiminnolla **Varaustyökirja**-sivulla. Esimerkiksi joukkovaraukset voivat auttaa varmistamaan, että määriä on saatavilla myynti- ja tuotantotilauksille. Eriä voi olla useita eri tarkoituksia varten. Voit esimerkiksi kohdistaa tuotantotilauksia viikoittain, mutta varata ne päivittäin myynteihin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaustyökirja** ja valitse sitten vastaava linkki.  
2. Valitse **Hae kysyntä** -toiminto ja määritä sitten, minkälaisen kysynnän haluat varata saatavilla olevasta varastosta.
3. Täytä tarvittavat suodattimet. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
4. Valinnainen: Voit kohdistaa nimikkeet heti valitsemalla **Kohdista**-toiminnon.
5. Valitse jokaiselle vaiheelle jokin menettelytapa **Kohdistuskäytäntö**-sivulla

   |Kohdistuskäytäntö  |Kuvaus  |
   |---------|---------|
   |Perus     | Kohdistaa varastot kysyntään, jos ristiriitoja ei ole ja kysyntä voidaan kattaa kokonaan. Sinulla on esimerkiksi myyntitilaus A, jonka määrä on 10, ja työ, jonka määrä on 7. Jos varastossa on 20, molemmat vaatimukset saavat täyden määrän. Jos varastosi on 12, varastoa ei kohdisteta. Määrä tulee kohdistaa manuaalisesti.        |
   |Tasan    | Jakaa saatavilla olevan varaston kysyntään tasan. Sinulla on esimerkiksi myyntitilaus, jonka määrä on 10, ja työ, jonka määrä on 7. Jos varastotasosi on 20, molemmat kysynnät saavat täyden määrän. Jos varastosi on 12, molemmat kysynnät saavat 6.        |
   |Asiakkaan prioriteetin mukaan|Jako **Asiakaskortti**-sivun **Prioriteetti**-kentän perusteella. Jos varastomäärät ovat alhaisia, Business Central toimittaa ensin korkean prioriteetin asiakkaille.|

6. Jos haluat varata kaikki rivit, joilla **Hyväksy** on otettu käyttöön, valitse **Tee varaus** -toiminto.
    
## <a name="change-a-reservation"></a>Muuta varausta

Nimikevarausta voi muuttaa.

1. Valitse sen asiakirjarivin, jossa olet tehnyt varauksen, **Rivit** -pikavälilehdessä **Varaa**-toiminto.  
2. Valitse **Varaus**-sivulla **Varaustapahtumat**-toiminto.
3. Päivitä **Varaustapahtumat**-sivulla muutettavan rivin **Määrä**-kenttä.
4. Vahvista avautuva sanoma valitsemalla **OK**.

## <a name="cancel-a-reservation"></a>Peruuta varaus

Nimikevarauksen voi peruuttaa.

1. Valitse sen asiakirjarivin, jossa tehdyn varauksen haluat peruuttaa, **Rivit** -pikavälilehdessä **Varaa**-toiminto.  
2. Valitse **Varaus**-sivulla **Varaustapahtumat**-toiminto.  
3. Valitse **Varaustapahtumat**-sivulla **Peruuta varaus** -toiminto.  
4. Vahvista avautuva sanoma valitsemalla **Kyllä**.  

## <a name="reserve-a-specific-serial-or-lot-number"></a>Varaa tietty sarja- tai eränumero

Nimikeseurannassa olevien nimikkeiden lähtevien asiakirjojen, kuten myyntitilausten tai tuotannon komponenttiluetteloiden, tiettyjä sarja- tai eränumeroita voi varata. Esimerkiksi tiettyjen sarja- tai eränumeroiden varaaminen voi olla hyödyllistä seuraavissa tilanteissa:

* Jos tietyn erän tuotannon komponentteja tarvitaan, jotta varmistutaan johdonmukaisuudesta aikaisempien tuotantoerien kanssa.
* Koska asiakas on pyytänyt tiettyä sarjanumeroa. 

Lue lisää kohdassa [Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md).

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

## <a name="see-also"></a>Katso myös

[Varasto](inventory-manage-inventory.md)  
[Rakennetiedot: Varaus, tilauksen seuranta ja toimintojen viestintä](design-details-reservation-order-tracking-and-action-messaging.md)  
[Rakennetiedot: nimikkeen seuranta ja varaukset](design-details-item-tracking-and-reservations.md)  
[Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
