---
title: Huoltonimikkeiden huoltosopimusten vaihekuvaus
description: Tässä artikkelissa käsitellään erilaisia huoltonimikkeitä ja -sopimuksia koskevia tilanteita.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# <a name="walkthrough-of-service-contracts-for-service-items"></a>Huoltonimikkeiden huoltosopimusten vaihekuvaus

Tässä vaihekuvauksessa kuvataan useita ydinprosesseja:

- Huoltonimikkeiden luominen myynnin avulla
- Huoltosopimuksen luominen ja laskutus
- Huoltotilauksen luominen huoltosopimukselle
- Resurssin määrittäminen taitojen ja alueen perusteella
- Täytä huoltotilauksen aikatapahtuma
- Kirjaa ja laskuta sopimushuoltotilaus

## <a name="creation-of-service-items"></a>Huoltonimikkeiden luonti

### <a name="scenario"></a>Skenaario

Tilausten käsittelijä Susan kirjaa myyntitilauksen, jossa myydään huoltonimikkeen luomiseen määritettyä nimikettä.  

### <a name="steps"></a>Vaiheet

1. Tarkista, että **Nimike**-kohdassa on valittuna **Huoltonimikeryhmä**.
   
    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
    2. Valitse nimike *S-100* ja avaa se.
    3. Tarkista **Huoltonimikeryhmä**-kentän arvo.
       
2. Luo asiakkaalle huoltonimike kirjaamalla **myyntitilaus**.  

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
    2. Valitse asiakkaan 10000 tilaus. Ulkoisten tilausten nro on *SVC-1*.
    3. Toimita nimike asiakkaalle valitsemalla **Kirjaa**-toiminto.

### <a name="results"></a>Tulokset

- Asiakkaalle 10000 luodaan huoltonimike

## <a name="invoicing-a-service-contract"></a>Huoltosopimuksen laskuttaminen

### <a name="scenario-1"></a>Skenaario

Huoltopäällikkö Charles luo tämän jälkeen huoltosopimuksen tavallisten kunnossapitokäyntien laskuttamiseksi.

3. Luo uudelle huoltonimikkeelle **huoltosopimus**
    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimukset** ja valitse sitten vastaava linkki.
    2. Valitse **Uusi**-toiminto.  
    3. Luo sopimus mallia käyttämällä valitsemalla vahvistusikkunassa **Kyllä**. 
    4. Valitse *Ei enn.maksusop. - kk*.
    5. Kirjoita Huolto-pikavälilehden **Huoltotilauksen tyyppi** -kenttään **KUNNOSSA**.
    6. Lisää seuraavat tiedot riveille:

    |Huoltonimikkeen nro|Rivin arvo|  
    |----------------|----------|  
    |SV000001|6000|

    7. Valitse **Allekirjoita sopimus** -toiminto ja vahvista allekirjoitus.
    8. Vahvista huoltolaskun luonti valitsemalla **Kyllä**. Saat vahvistusviestin, jossa on huoltolaskun numero.

3. Kirjaa huoltolasku
   1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltolaskut** ja valitse sitten vastaava linkki.
   2. Etsi huoltolasku ja valitse **Kirjaa**-toiminto.

### <a name="results-1"></a>Tulokset

- Allekirjoitettu huoltosopimus ja tapahtumakirjaukset luodaan
- Kirjattu huoltolasku luodaan

## <a name="creating-a-service-order-for-a-service-contract-and-assign-resources"></a>Huoltotilauksen luominen huoltosopimukselle ja resurssien määritteleminen

### <a name="scenario-2"></a>Skenaario

Huoltopäällikkö Charles luo huoltotilaukset huoltosopimuksen mukaisille tavallisille kunnossapitotilauksille ja tarkistaa niiden määrittämisen lähetystaulukosta.

### <a name="steps-1"></a>Vaiheet

1. Suorita huoltotilaukset, jotka täyttävät aktiivisten huoltosopimusten velvoitteet.
   1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo sopimushuoltotilauksia** ja valitse sitten vastaava linkki.
   2. Määritä kuukauden alku- ja lopetuspäivämäärät Vaihtoehdot-pikavälilehden Aloituspvm- ja Lopetuspvm-kenttiin
   3. Vahvista huoltotilausten luonti valitsemalla **OK**. Saat vahvistusviestin, jossa on luotujen huoltotilausten määrä.

2. Tarkasta tilaukset, jotka odottavat määritystä, lähetystaulukon kautta
   1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Lähetystaulukko** ja valitse sitten vastaava linkki.
   2. Lähetystaulukossa näkyvät kaikki avoimet huoltotilaukset sekä **Kohdistusten lkm**, joka näyttää, onko huoltotilaukset määritelty resurssiin.
   3. Avaa huoltotilaus valitsemalla **Näytä asiakirjat** -toiminto.  Huoltonimikerivit-tietoruudussa näkyy, millä resursseilla on taidot käsitellä tätä nimikettä.

3. Resurssin määrittäminen huoltotilaukselle
   1. Valitse huoltotilauksesta rivitoiminto **Resurssin kohdistukset**
   2. Anna seuraavat tiedot resurssin kohdistukseen

    |Huoltonimikkeen nro|Resurssin nro|Kohdistuspvm|Kohdistetut tunnit|
    |----------------|------------|---------------|---------------|  
    |SV000001|RESOURCE1|t|1|

    3. Kohdistus muutetaan tilaksi Aktiivinen.
    4. Kun lähetystaulukko päivitetään, huoltotilauksen **Kohdistusten lkm** muuttuu 0:sta 1:een.

### <a name="results-2"></a>Tulokset

- Huoltotilaukset luodaan huoltosopimuksille
- Huoltotilaukset kohdistetaan resurssille työn loppuunsaattamiseksi

## <a name="complete-the-time-entry-for-the-service-order-and-post-the-service-order"></a>Täytä huoltotilauksen aikatapahtuma ja kirjaa huoltotilaus

### <a name="scenario-3"></a>Skenaario

Huoltoteknikko rekisteröi aikansa suoraan huoltotilausta vastaan ja merkitsee tilauksen valmiiksi.

> [!NOTE]
> Huoltotilausten aikatapahtuma voidaan syöttää tuntiraporttien avulla. Lisätietoja on kohdassa [linkki tuntiraporttiin, jos tässä huomautuksessa on järkeä].

### <a name="steps-2"></a>Vaiheet

1. Etsi huoltotilaus ja syötä aika huoltoriville
   1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** ja valitse sitten vastaava linkki.
   2. Etsi huoltotilaus, jolle aika määritetään.
   3. Valitse **Huoltorivi**-rivitoiminto.
   4. Lisää seuraavat tiedot

    |Tyyppi|Nro|Määrä|Kulutettava määrä|
    |----|---|--------|--------|   
    |Resurssi|RESOURCE1|2|2|

2. Kirjaa kulutus huoltotilauksessa
   1. Suorita huoltotilaus loppuun valitsemalla **Kirjaa**-toiminto, valitse **Toimitus ja kulutus** -toiminto ja valitse sitten **OK**.

### <a name="results-3"></a>Tulokset

- Huoltotapahtumat luodaan huoltonimikkeen, huoltosopimuksen ja resurssin kanssa

## <a name="see-also"></a>Katso myös
