---
title: Kirjanpitojaksojen ja tilikausien käyttäminen
description: 'Lisätietoja tilijaksojen käyttämisestä määrittämään, milloin yrityksen taloudellinen tulos raportoidaan.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 100
ms.date: 08/25/2022
ms.author: bholtorf
---
# Kirjanpitojaksojen ja tilikausien käyttäminen

Tilijaksot, joita kutsutaan myös raportointikausiksi, ovat ajanjaksoja, jolloin yritys tai organisaatio raportoi taloudellisen tuloksen luomalla esimerkiksi tuloslaskeman tai taseen. Yleensä kirjanpitojaksoilla viitataan yrityksen tilikauteen, joka voi koostua useista tilijaksoista, kuten kuukausista tai neljännesvuosista.

Monille yrityksille tilikausi ei ole sama kuin kalenterivuosi, esimerkiksi kun tilikausi päättyy 30. kesäkuuta eikä 31.12. Uusilla yrityksillä tilikausi voi myös olla jopa pidempi kuin 12 kuukautta.  

[!INCLUDE[prod_short](includes/prod_short.md)] edellyttää kirjanpitojaksoja siinä tapauksessa, että haluat sulkea tuloslaskelman tai suorittaa tietojen tiivistystehtäviä.

Voit käyttää tilikausia raportoinnissa, esimerkiksi tarkastellessasi merkintöjä **Saldo/budjetti**-sivulla, jossa raportointiväli määritetään. Yksi vaihtoehdoista on raportoinnin määrittäminen kirjanpitojakson mukaan. Voit myös muodostaa taloudellisen raportin, joka vertaa eri kirjanpitojaksojen tuloksia.

## Uuden tilikauden luominen

Voit luoda kirjanpitojaksoja joukkotoiminnolla käyttämällä **Luo tilikausi** -eräajoa tai voit luoda ne manuaalisesti.

### Kirjanpitojaksojen luominen joukkotoiminnolla

Jaa tilikausi saman mittaisiksi jaksoiksi **Luo tilikausi** -eräajon avulla.  

1. Valitse ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Kirjanpitojaksot**, valitse sitten vastaava linkki.  
2. Valitse **Luo vuosi** -toiminto.
3. Anna **Aloituspvm**-kenttään päivämäärä, jolloin tilikausi alkaa.  
4. Määrittele **Jaksojen lukumäärä** -kentässä, kuinka moneen kirjanpitojaksoon tilikausi jaetaan. Vuodessa voi olla enintään 365 jaksoa.  
5. Määritä **Jakson pituus** -kentässä kunkin jakson kesto. Keston tunnuksiin kuuluvat: yksi kuukausi on 1K, yksi neljännesvuosi on 1Q ja yksi vuosi 1V.  
6. Valitse **OK**.  

### Kirjanpitojaksojen luominen manuaalisesti

Jos tilikauden kirjanpitojaksojen pituudet vaihtelevat, kuten vähittäismyynnissä käytetty 4-4-5-kalenteri, määritys voidaan tehdä manuaalisesti.  
  
1. Valitse ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Kirjanpitojaksot**, valitse sitten vastaava linkki.  
2. Anna **Aloituspvm**-kenttään päivämäärä, jolloin tilikausi alkaa. **Nimi**-kentässä on kuukauden nimi.  
3. Ilmaise **Uusi tilikausi** -valintaruudun valinnalla, että kyse on vuoden ensimmäisestä jaksosta. [!INCLUDE[prod_short](includes/prod_short.md)] määrittää tämän jakson perusteella, mitkä jaksot sulkevat tilikauden.
4. Toista vaiheet 2 ja 3 kunkin jäljellä olevan jakson kohdalla.  

## Tilikauden sulkeminen

Tilikauden sulkeminen on yksi kirjojen sulkemistehtävistä. Kun tilikausi on suljettu, **Suljettu**- ja **Pvm lukittu** -valintaruudut valitaan kaikille tilikauden jaksoille. Tilakautta ei voi avata uudelleen eikä valintaruutujen valintaa poistaa.

> [!NOTE]  
> Avoimena on oltava aina ainakin yksi tilikausi. Varmista tilikautta suljettaessa, että tilikausi on luotu. Huomaa myös, että kun tilikausi on suljettu, et voi muuttaa seuraavan tilikauden aloituspäivämäärää.

1. Valitse ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Kirjanpitojaksot** ja valitse sitten vastaava linkki.  
2. Valitse **Sulje vuosi** -toiminto.  

## Tapahtumien kirjaaminen suljettuun tilikauteen

Vaikka tilikausi on suljettu, voit silti kirjata tilikaudelle KP-tapahtumia. Kun teet tämän, tapahtumat merkitään kirjatuiksi suljetulle tilikaudelle ja **Edellisen vuoden tapahtuma** -valintaruutu valitaan. Valintaruutu ei oletusarvoisesti näy sivulla, mutta voit lisätä sen. Seuraavaksi suljetaan tuloslaskelmatilit ja siirretään vuoden tulostaseessa olevalle tilille. Toista nämä vaiheet aina, kun kirjaat tapahtumia suljetulle tilikaudelle.

## Katso myös

[Kirjojen sulkeminen](year-close-books.md)  
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[Ohjeita talousraporttien käsittelemiseen](bi-how-work-account-schedule.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
