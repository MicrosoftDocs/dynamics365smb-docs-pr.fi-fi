---
title: Nimiketapahtumien poistaminen ja uudelleenkohdistaminen
description: 'Voit tarkastella ja muuttaa manuaalisesti tietyn nimikkeen kohdistustapahtumia, jotka on luotu automaattisesti varastotapahtumien yhteydessä.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '506, 521, 9125'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="remove-and-reapply-item-ledger-entries"></a><a name="remove-and-reapply-item-ledger-entries"></a>Nimiketapahtumien poistaminen ja uudelleenkohdistaminen
Voit tarkastella ja muuttaa **Kohdistustyökirja**-sivulla manuaalisesti tietyn nimikkeen kohdistustapahtumia, jotka on luotu automaattisesti varastotapahtumien yhteydessä.  

Kun kirjaat tapahtuman, jossa nimikkeitä siirretään varastosta tai varastoon, nimikesovellus luodaan jookaisen varastoarvon nousun varastoarvon laskun väliin. Nämä kohdistukset määrittävät varastoon vastaanotettavien tavaroiden ja varastosta otettavien tavaroiden kustannusvirran. Yksikkökustannuksen laskentatavan mukaan nimikkeen virheellinen kohdistus voi johtaa vääristyneeseen keskimääräiseen kustannukseen ja yksikkökustannukseen. Katso lisätiedot kohdasta Rakennetiedot: nimikkeen kohdistus.

Seuraavat tilanteet saattavat vaatia, että kohdistus peruutetaan tai nimiketapahtumat kohdistetaan uudelleen:

- Unohdit tehdä kiinteän kohdistuksen.
- Teit virheellisen kiinteän kohdistuksen.
- Sinun on palautettava nimike, johon myynti on jo kohdistettu.

Käytä asiakirjaa nimiketapahtuman kohdistamisessa uudelleen, jos mahdollista. Jos esimerkiksi teet ostopalautuksen nimikkeelle, jonka myynti on jo kohdistettu, voit tehdä uudelleenkohdistuksen yksinkertaisesti luomalla ja kirjaamalla oikean kohdistuksen sisältävän ostopalautusasiakirjan ostopalautusrivin **Kohdista nimiketapahtumaan** -kentässä. Voit käyttää **Hae peruutettavat kirjatut asiakirjarivit** -toimintoa tai **Kopioi asiakirjasta** -toimintoa ostopalautusasiakirjassa, jolloin kohdistus on helpompaa. Kun kirjaat asiakirjan, nimiketapahtuma otetaan automaattisesti uudelleen käyttöön. Lisätietoja on kohdassa [Ostopalautusten tai -peruutusten käsitteleminen](purchasing-how-process-purchase-returns-cancellations.md).

Jos et tehdä uudelleenkohdistusta, kuten korjata kiinteää kohdistusta, asiakirjassa, korjaa kohdistus **Kohdistustyökirja**-sivulla.

> [!Warning]  
> Seuraavassa on tärkeitä muistettavia asioita, kun käsitellään kohdistustyökirjaa:
    - Älä jätä kohdistustapahtumia pitkäksi aikaa käyttämättä, koska muut käyttäjät eivät voi käsitellä nimikkeitä ennen kuin käytät kohdistustapahtumia uudelleen tai suljet **Sovellustyökirja**-sivun. Käyttäjät, jotka yrittävät tehdä toimia, joihin liittyy manuaalisesti kohdistamattoman kohdistustapahtuman saavat seuraavan virhesanoman: "Tätä toimintoa ei voi suorittaa, koska kohteen XXX tapahtumia ei ole käytetty sovelluksen asiakirjasta käyttäjän XXX toimesta."
    - Nimiketapahtumien uudelleenkohdistus on suositeltavaa tehdä muuna kuin työaikana. Tällöin vältetään ristiriidat muiden käyttäjien kirjatessa tapahtumia samalle nimikkeelle.
    - Kun suljet kohdistustyökirjan, [!INCLUDE[prod_short](includes/prod_short.md)] suorittaa tarkistuksen ja varmistaa, että kaikki tapahtumat on kohdistettu. Jos esimerkiksi poistat määrän kohdistuksen, mutta et luo uutta kohdistusta, ja suljet sen jälkeen kohdistustyökirjan, ohjelma luo uuden kohdistuksen jos mahdollista. Tällöin kustannukset pysyvät samoina. Huomaa kuitenkin, että jos poistat kiinteän kohdistuksen, ohjelma ei luo uutta kiinteää kohdistusta automaattisesti työarkin sulkemisen yhteydessä. Sinun on luotava uusi kohdistus manuaalisesti työarkissa.
    - Voit poistaa usean tapahtuman kohdistukset samanaikaisesti kohdistustyökirjassa. Koska tapahtumien kohdistaminen vaikuttaa useisiin kohdistuksen käytettävissä oleviin tapahtumiin, voit luoda kohdistuksen vain yhdelle tapahtumalle samanaikaisesti.
    - Kohdistustyökirja ei voi tehdä kohdistusta seuraavassa tilanteessa: Jos varastossa ei ole tarpeeksi kohdistettavaa määrää, kohdistustyökirja ei voi tehdä kohdistusta, jos yrität kohdistaa varaston vähennystapahtumaa, jolla ei ole nimikeseurannan tietoja, sellaiseen varaston lisäystapahtumaan, jolla on nimikeseurannan tiedot.

## <a name="to-remove-an-item-application-by-using-the-application-worksheet"></a><a name="to-remove-an-item-application-by-using-the-application-worksheet"></a>Nimikkeen kohdistuksen ja kohdistustyökirjan poistaminen

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kohdistustyökirja** ja valitse sitten vastaava linkki.  
2.  **Kohdistustyökirja**-sivu aukeaa näyttäen kaikkia nimikkeitä koskevat nimiketapahtumat.  
3.  Syötä suodattimet **Yleinen**-pikavälilehdelle, jotta on helpompi löytää nimiketapahtumat, joille haluat muuttaa sovelluksen.  
4.  Valitse ensin nimiketapahtuma ja sitten **Kohdistetut tapahtumat** -toiminto. **Näytä kohdistetut tapahtumat - Kohdistetut tapahtumat** -sivu avautuu ja sivulla näkyvä valittuun tapahtumaan kohdistetut nimiketapahtumat.  
5.  Valitse nimiketapahtuma, jonka kohdistuksen haluat poistaa.  
6.  Valitse **Poista kohdistus** -toiminto. Nämä kaksi nimiketapahtumaa linkittävä nimikkeen kohdistustapahtuma poistetaan ja siirretään **Nimikkeen kohdistustapahtumahistoria** -sivulle.  
7.  Sulje **Näytä kohdistetut tapahtumat - Kohdistetut tapahtumat** -sivu.  

 Kahden nimiketapahtuman **Jäljellä oleva määrä** -kenttien määrä lisääntyy sillä määrällä, jolta poistettiin kohdistus. Poistettu nimiketapahtuma voidaan nyt kohdistaa uudelleen **Näytä kohdistetut tapahtumat - kohdistamattomat tapahtumat** -sivulla.  

> [!IMPORTANT]  
>  Älä jätä kohdistustapahtumia pitkäksi aikaa käyttämättä, koska muut käyttäjät eivät voi käsitellä nimikkeitä ennen kuin käytät kohdistustapahtumia uudelleen tai suljet **Kohdistustyökirja**-sivun. Seuraava virhesanoma näytetään, jos yrität suorittaa toimintoja, jotka liittyvät manuaalisesti peruutettuun kohdistustapahtumaan:  
>   
>  **Et voi suorittaa tätä toimintoa, koska käyttäjä \<user\> on peruuttanut nimikkeen \<item\> kohdistuksen kohdistustyökirjassa.**  

## <a name="to-reapply-an-item-application-by-using-the-application-worksheet"></a><a name="to-reapply-an-item-application-by-using-the-application-worksheet"></a>Nimikkeen kohdistuksen ja kohdistustyökirjan luominen

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kohdistustyökirja** ja valitse sitten vastaava linkki.  
2.  **Kohdistustyökirja**-sivu aukeaa näyttäen kaikkia nimikkeitä koskevat nimiketapahtumat.  
3.  Voit kohdistaa työkirjan avaamisen jälkeen poistetut tapahtumat uudelleen valitsemalla uudelleenkohdistettavan nimiketapahtuman ja valitsemalla sitten **Kohdista uudelleen** -toiminto.  

    > [!NOTE]  
    >  Tämä uudelleenkohdistus alkuperäiseen saldoon tapahtuu automaattisesti, kun **Kohdistustyökirja**-sivu suljetaan.  
4.  Käytä saatavilla olevaa nimiketapahtumaa toiseen tapahtumaan valitsemalla se nimiketapahtuma, jota haluat käyttää. Valitse **Kohdistamattomat tapahtumat**-toiminto. **Näytä kohdistetut tapahtumat - Kohdistamattomat tapahtumat** -sivu avautuu.  
5.  Valitse **Kohdistustyökirja**-sivulla valittuun tapahtumaan kohdistettavat nimiketapahtumat ja valitse **OK**.  

     Ohjelma luo nimikkeen kohdistustapahtuman näiden kahden nimiketapahtuman välille. Kahden tapahtuman **Jäljellä oleva määrä** -kenttien arvoja vähennetään kohdistetulla määrällä.  

    > [!NOTE]  
    >  Jos olet valinnut sellaisen kohdistuksen tekemisen, joka loisi päättymättömän silmukan kustannusten muutosprosessiin, ehdottamaasi kohdistusta ei tehdä. Näin voi tapahtua, kun alkuperäiset tapahtumat loivat negatiivisen varaston. Sovellusta ei ole tehty. Tämän vuoksi on valittava sovellukselle eri tapahtuma.  
6.  Jos **varastonhallinnan asetusten** **Automaattinen kustannusten muuttaminen** -kentän arvoksi määritetään **Aina**, kustannusten muuttamisen eräajo suoritetaan automaattisesti uudelleenkohdistuksen jälkeen. Muussa tapauksessa voit varmistaa suorittamalla **Muuta kustannuksia - Nimiketapahtumat** -eräajon, että kaikki kustannukset on päivitetty.  

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Nimikepäiväkirjan kiinteästä kohdistuksesta aiheutuvien avointen nimiketapahtumien sulkeminen](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
 [Ostopalautusten tai peruutusten käsittely](purchasing-how-process-purchase-returns-cancellations.md)  
 [Varaston kustannusten hallinta](finance-manage-inventory-costs.md)   
 [Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md)  
 [Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
