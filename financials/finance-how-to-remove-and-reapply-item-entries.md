---
title: Nimiketapahtumien poistaminen ja uudelleenkohdistaminen | Microsoft Docs
description: "Voit tarkastella ja muuttaa manuaalisesti tietyn nimikkeen kohdistustapahtumia, jotka on luotu automaattisesti varastotapahtumien yhteydessä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 12bde7fc508bb29e56ad63d76b526a80b5073f03
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="remove-and-reapply-item-ledger-entries"></a>Nimiketapahtumien poistaminen ja uudelleenkohdistaminen
Voit tarkastella ja muuttaa **Kohdistustyökirja**-ikkunassa manuaalisesti tietyn nimikkeen kohdistustapahtumia, jotka on luotu automaattisesti varastotapahtumien yhteydessä.  

Kun kirjaat tapahtuman, jossa nimikkeitä siirretään varastosta tai varastoon, nimikesovellus luodaan jookaisen varastoarvon nousun varastoarvon laskun väliin. Nämä kohdistukset määrittävät varastoon vastaanotettavien tavaroiden ja varastosta otettavien tavaroiden kustannusvirran. Yksikkökustannuksen laskentatavan mukaan nimikkeen virheellinen kohdistus voi johtaa vääristyneeseen keskimääräiseen kustannukseen ja yksikkökustannukseen. Katso lisätiedot kohdasta Rakennetiedot: nimikkeen kohdistus.

Seuraavat tilanteet saattavat vaatia, että kohdistus peruutetaan tai nimiketapahtumat kohdistetaan uudelleen:

- Unohdit tehdä kiinteän kohdistuksen.
- Teit virheellisen kiinteän kohdistuksen.
- Sinun on palautettava nimike, johon myynti on jo kohdistettu.

Käytä asiakirjaa nimiketapahtuman kohdistamisessa uudelleen, jos mahdollista. Jos esimerkiksi teet ostopalautuksen nimikkeelle, jonka myynti on jo kohdistettu, voit tehdä uudelleenkohdistuksen yksinkertaisesti luomalla ja kirjaamalla oikean kohdistuksen sisältävän ostopalautusasiakirjan ostopalautusrivin **Kohdista nimiketapahtumaan** -kentässä. Voit käyttää **Hae peruutettavat kirjatut asiakirjarivit** -toimintoa tai **Kopioi asiakirja** -toimintoa ostopalautusasiakirjassa, jolloin kohdistus on helpompaa. Kun kirjaat asiakirjan, nimiketapahtuma otetaan automaattisesti uudelleen käyttöön. Lisätietoja on kohdassa [Ostopalautusten tai -peruutusten käsitteleminen](purchasing-how-process-purchase-returns-cancellations.md).

Jos et tehdä uudelleenkohdistusta, kuten korjata kiinteää kohdistusta, asiakirjassa, korjaa kohdistus **Kohdistustyökirja**-ikkunassa.

> [!Warning]
> Seuraavassa on tärkeitä muistettavia asioita, kun käsitellään kohdistustyökirjaa:
>     - Älä jätä kohdistustapahtumia pitkäksi aikaa käyttämättä, koska muut käyttäjät eivät voi käsitellä nimikkeitä ennen kuin käytät kohdistustapahtumia uudelleen tai suljet **Sovellustyökirja** -ikkunan. Käyttäjät, jotka yrittävät tehdä toimia, joihin liittyy manuaalisesti kohdistamattoman kohdistustapahtuman saavat seuraavan virhesanoman: "Tätä toimintoa ei voi suorittaa, koska kohteen XXX tapahtumia ei ole käytetty sovelluksen asiakirjasta käyttäjän XXX toimesta."
>     - Nimiketapahtumien uudelleenkohdistus on suositeltavaa tehdä muuna kuin työaikana. Tällöin vältetään ristiriidat muiden käyttäjien kirjatessa tapahtumia samalle nimikkeelle.
>     - Kun suljet kohdistustyökirjan, [!INCLUDE[d365fin](includes/d365fin_md.md)] suorittaa tarkistuksen ja varmistaa, että kaikki tapahtumat on kohdistettu. Jos esimerkiksi poistat määrän kohdistuksen, mutta et luo uutta kohdistusta, ja suljet sen jälkeen kohdistustyökirjan, ohjelma luo uuden kohdistuksen jos mahdollista. Tällöin kustannukset pysyvät samoina. Huomaa kuitenkin, että jos poistat kiinteän kohdistuksen, ohjelma ei luo uutta kiinteää kohdistusta automaattisesti työarkin sulkemisen yhteydessä. Sinun on luotava uusi kohdistus manuaalisesti työarkissa.
>     - Voit poistaa usean tapahtuman kohdistukset samanaikaisesti kohdistustyökirjassa. Koska tapahtumien kohdistaminen vaikuttaa useisiin kohdistuksen käytettävissä oleviin tapahtumiin, voit luoda kohdistuksen vain yhdelle tapahtumalle samanaikaisesti.
>     - Kohdistustyökirja ei voi tehdä kohdistusta seuraavassa tilanteessa: Jos varastossa ei ole tarpeeksi kohdistettavaa määrää, kohdistustyökirja ei voi tehdä kohdistusta, jos yrität kohdistaa varaston vähennystapahtumaa, jolla ei ole nimikeseurannan tietoja, sellaiseen varaston lisäystapahtumaan, jolla on nimikeseurannan tiedot.

## <a name="to-remove-an-item-application-by-using-the-application-worksheet"></a>Nimikkeen kohdistuksen ja kohdistustyökirjan poistaminen  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kohdistustyökirja** ja valitse sitten aiheeseen liittyvä linkki.  
2. **Kohdistustyökirja**-ikkuna aukeaa näyttäen kaikkia nimikkeitä koskevat nimiketapahtumat.  
3. Syötä suodattimet **Yleinen**-pikavälilehdelle, jotta on helpompi löytää nimiketapahtumat, joille haluat muuttaa sovelluksen.  
4. Valitse ensin nimiketapahtuma ja sitten **Kohdistetut tapahtumat** -toiminto. **Näytä kohdistetut tapahtumat - Kohdistetut tapahtumat** -ikkuna avautuu ja ikkunassa näkyvä valittuun tapahtumaan kohdistetut nimiketapahtumat.  
5. Valitse nimiketapahtuma, jonka kohdistuksen haluat poistaa.  
6. Valitse **Poista kohdistus** -toiminto. Nämä kaksi nimiketapahtumaa linkittävä nimikkeen kohdistustapahtuma poistetaan ja siirretään **Nimikkeen kohdistustapahtumahistoria** -ikkunaan.  
7. Sulje **Näytä kohdistetut tapahtumat - Kohdistetut tapahtumat** -ikkuna.  

   Kahden nimiketapahtuman **Jäljellä oleva määrä** -kenttien määrä lisääntyy sillä määrällä, jolta poistettiin kohdistus. Poistettu nimiketapahtuma voidaan nyt kohdistaa uudelleen **Näytä kohdistetut tapahtumat - kohdistamattomat tapahtumat** -ikkunassa.  

> [!IMPORTANT]  
>  Älä jätä kohdistustapahtumia pitkäksi aikaa käyttämättä, koska muut käyttäjät eivät voi käsitellä nimikkeitä ennen kuin käytät kohdistustapahtumia uudelleen tai suljet **Kohdistustyökirja**-ikkunan. Seuraava virhesanoma näytetään, jos yrität suorittaa toimintoja, jotka liittyvät manuaalisesti peruutettuun kohdistustapahtumaan:  
>   
>  **Et voi suorittaa tätä toimintoa, koska käyttäjä <user> on peruuttanut nimikkeen <item> kohdistuksen kohdistustyökirjassa.**  

## <a name="to-reapply-an-item-application-by-using-the-application-worksheet"></a>Nimikkeen kohdistuksen ja kohdistustyökirjan luominen  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kohdistustyökirja** ja valitse sitten aiheeseen liittyvä linkki.  
2.  **Kohdistustyökirja**-ikkuna aukeaa näyttäen kaikkia nimikkeitä koskevat nimiketapahtumat.  
3.  Voit kohdistaa työkirjan avaamisen jälkeen poistetut tapahtumat uudelleen valitsemalla uudelleenkohdistettavan nimiketapahtuman. Valitse **Toiminnot**-välilehden **Funktiot**-ryhmässä **Käytä uudelleen**.  

    > [!NOTE]  
    >  Tämä uudelleenkohdistus alkuperäiseen saldoon tapahtuu automaattisesti, kun **Kohdistustyökirja**-ikkuna suljetaan.  
4.  Käytä saatavilla olevaa nimiketapahtumaa toiseen tapahtumaan valitsemalla se nimiketapahtuma, jota haluat käyttää. Valitse **Kohdistamattomat tapahtumat**-toiminto. **Näytä kohdistetut tapahtumat - Kohdistamattomat tapahtumat** -ikkuna avautuu.  
5.  Valitse **Kohdistustyökirja**-ikkunassa valittuun tapahtumaan kohdistettavat nimiketapahtumat ja valitse **OK**.  

     Ohjelma luo nimikkeen kohdistustapahtuman näiden kahden nimiketapahtuman välille. Kahden tapahtuman **Jäljellä oleva määrä** -kenttien arvoja vähennetään kohdistetulla määrällä.  

    > [!NOTE]  
    >  Jos olet valinnut sellaisen kohdistuksen tekemisen, joka loisi päättymättömän silmukan kustannusten muutosprosessiin, ehdottamaasi kohdistusta ei tehdä. Näin voi tapahtua, kun alkuperäiset tapahtumat loivat negatiivisen varaston. Sovellusta ei ole tehty. Tämän vuoksi on valittava sovellukselle eri tapahtuma.  
6.  Jos **varastonhallinnan asetusten** **Automaattinen kustannusten muuttaminen** -kentän arvoksi määritetään **Aina**, kustannusten muuttamisen eräajo suoritetaan automaattisesti uudelleenkohdistuksen jälkeen. Muussa tapauksessa voit varmistaa suorittamalla **Muuta kustannuksia - Nimiketapahtumat** -eräajon, että kaikki kustannukset on päivitetty.  

## <a name="see-also"></a>Katso myös  
[Nimikepäiväkirjan kiinteästä kohdistuksesta aiheutuvien avointen nimiketapahtumien sulkeminen](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
 [Ostopalautusten tai peruutusten käsittely](purchasing-how-process-purchase-returns-cancellations.md)  
 [Varaston kustannusten hallinta](finance-manage-inventory-costs.md)   
 [Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

