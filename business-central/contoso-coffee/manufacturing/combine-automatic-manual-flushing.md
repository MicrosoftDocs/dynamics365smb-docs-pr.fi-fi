---
title: Yhdistä automaattinen ja manuaalinen materiaalinotto
description: 'Tuotantosuunnittelijan vaihekuvaus Contoso Coffeelle, jossa halutaan yhdistää automaattinen ja manuaalinen materiaalinotto.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Vaihekuvaus: Yhdistä automaattinen ja manuaalinen materiaalinotto

Tässä artikkelissa on tietoja Contoso Coffee -esittelyn tietojen käytöstä materiaalinotossa.  

## Esimerkkitilanne

Olet Contoso Coffeen tuotantosuunnittelija. Luo uusi tuotantotilaus SP-SCM1004, AutoDrip -nimikkeen 10 yksikölle. Jotkin komponentit ja toiminnot suoritetaan eteenpäin suuntautuvana materiaalinottona, toiset taaksepäin suuntautuvana materiaalinottona eri ehtojen perusteella.

## Vaiheet

> [Huomautus!] Muista oikaista varasto kirjaamalla alkusaldot nimikepäiväkirjaan.

1. Luo sitovasti suunniteltu tuotantotilaus **SP-SCM1004, AutoDrip** -nimikkeen 5 yksikölle sijainnissa *NORTH*. Katso ohjeet: [Vaihekuvaus: Luo sitovasti suunniteltu tuotantotilaus ja muuta sitä](create-firm-planned-production-order-change.md).  

2. Vapauta tuotantotilaus.

    1. Valitse **Vaihda tila** -toiminto.  

    2. Määritä näyttöön tulevassa sivussa **Uusi tila** -kenttä *vapautetuksi* ja valitse **Kyllä**-painike.  

        Näyttöön tulee sanoma, jossa on tilarivi, ja viittaus automaattiseen kulutukseen. Tätä seuraa vahvistussanoma siitä, että tilauksen tilaksi vaihtuu *Vapautettu*.  

    3. Sulje vahvistussanoma valitsemalla **OK**.

3. Tarkista tuotantotilauksen nimike- ja kapasiteettitapahtumat.

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vapautettu tuotantotilaus** ja valitse sitten vastaava linkki.  

    2. Avaa tuotantotilaus, jossa on AutoDrip-kahvinkeittimen 5 yksikköä.  

    3. Valitse **Nimiketapahtumakirjaukset**-toiminto.  

        Nimikkeen **SP-BOM1305 Screw Hex M3 Zink** materiaali otetaan välittömästi koko oletettuun määrään asti. Sulje **Nimiketapahtumakirjaukset**-sivu.  

    4. Valitse **Kapasiteettitapahtumakirjaukset**-toiminto.  Huomaa, että rungon kokoonpanotoimintojen merkintä suoritettiin myös silloin, kun tilaus vapautettiin. Sulje **Kapasiteettitapahtumakirjaukset**-ikkuna.

    Komponenttinimikkeille voi ottaa materiaalia manuaalisesti kulutus- tai tuotantopäiväkirjan avulla. Manuaalisen materiaalinoton avulla voit muuttaa määrää ennen kirjausta. Esimerkiksi, jos lisämäärä tarvitaan kattamaan huonolaatuisia raaka-aineita.
4. Ota komponenttien materiaali manuaalisesti.  
    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kulutuspäiväkirja** ja valitse sitten vastaava linkki.  

    2. Valitse **Laske kulutus** -toiminto.  

    3. Määritä **Laske kulutus** -pyyntösivun **Tuotantotilaus**-pikavälilehden **Tilauksen nro** -kentässä olevan tietyn tilauksen suodatus ja valitse sitten **OK**-painike. Kun eräajon pyyntösivu sulkeutuu, huomaa, että **Kulutuspäiväkirja**-sivuun täytetään komponentit, jotka vaativat manuaalista kulutusta.

    4. Valitse **Kirjaa**-toiminto. Sulje kulutuspäiväkirja.

5. Rekisteröi tuotos manuaalisesti sähköjohtojen asennusta varten.  

    Täytä **Asetusaika**- ja **Ajoaika**-kenttien tiedot manuaalisesti. Voit myös määrittää tosiasiallisesti tuotetun määrän ja hävikin. Syötä tuotoksen määräksi *3* ja kirjaa tuotos.

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotospäiväkirja** ja valitse sitten vastaava linkki.  

    2. Luo **tuotospäiväkirja**-sivulla uusi päiväkirjarivi.  

    3. Määritä **Tilausnro** -kentässä tilaus.  

    4. Valitse **Pura reititys** -toiminto.  

        **Tuotospäiväkirja**-sivu täyttää operaatiorivin vain sähköjohtoja varten.

    5. Määritä **ajoaika**-kentän arvoksi *10*.  

    6. Muuta **Määrä**-kenttä arvosta *5* arvoon *3*.

    7. Valitse **Kirjaa**.  
    8. Sulje tuotospäiväkirja.

6. Tarkista tuotantotilauksen nimiketapahtumat.

    1. Valitse tuotantotilauksen sivulla **Nimiketapahtumat**-toiminto.  

    Nimike **SP-BOM1302, Control panel display** on kirjattu määrällä *3* perustuen todelliseen tuotokseen, mutta **SP-BOM1303, Button** kirjataan koko oletetulle määrälle. Sulje **Nimiketapahtumakirjaukset**-sivu.

7. Viimeistele tuotantotilaus.  

    1. Valitse **Vaihda tila** -toiminto.
    2. Määritä näyttöön tulevassa sivussa **Uusi tila** -kenttä *valmiiksi* ja valitse **Kyllä**-painike.  

        Näyttöön tulee sanoma, jossa on tilarivi, joka kuvastaa automaattista kulutusta. Tätä seuraa vahvistussanoma siitä, että tilauksen tilaksi vaihtuu *Valmis*. Valmiissa tuotantotilauksessa on sama numero kuin siinä, jonka tila on *vapautettu*.
    3. Sulje vahvistussanoma valitsemalla **OK**.

8. Tarkista tuotantotilauksen nimike- ja kapasiteettitapahtumat uudelleen.

    1. Valitse **Kapasiteettitapahtumakirjaukset**-toiminto.  

        Pakkaustoimintojen tapahtuma valmistui sillä hetkellä, kun tilaus vapautettiin. Tuotettu (tuotos) määrä on *5*, riippumatta edellisen vaiheen tuotoksesta. Sulje **Kapasiteettitapahtumakirjaukset**-sivu.

    2. Valitse **Nimiketapahtumakirjaukset**-toiminto.  

        *Tuotos*-tyypin nimiketapahtuman määrä on yhtä suuri kuin kapasiteettitapahtuman tuotoksen määrä. Kohteiden **SP-BOM1301, Housing AutoDrip** ja **SP-BOM1304, Stainless still thermal carafe** kulutettu määrä on molemmille 5, koska odotettu ja todellinen tuotos ovat samat. 

    3. Sulje **Nimiketapahtumakirjaukset**-sivu.  

Tässä oli tietoa manuaalisesta ja automaattisesta materiaalinotosta komponenteille.

## Katso myös

[Komponenttien materiaalinotto toiminnan tuotoksen mukaan](../../production-how-to-flush-components-according-to-operation-output.md)  
[Johdatus Contoson kahvidemotietoihin](contoso-coffee-manufacturing-intro.md)  
