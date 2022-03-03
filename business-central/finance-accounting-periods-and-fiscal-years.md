---
title: Kirjanpitojaksojen ja tilikausien käyttäminen
description: Lisätietoja tilijaksojen käyttämisestä määrittämään, milloin yrityksen taloudellinen tulos raportoidaan.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 100
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 8d7927c8adcf19fae55af48ea699ea9b852d6974
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8136164"
---
# <a name="working-with-accounting-periods-and-fiscal-years"></a>Kirjanpitojaksojen ja tilikausien käyttäminen

Tilijaksot, joita kutsutaan myös raportointikausiksi, ovat ajanjaksoja, jolloin yritys tai organisaatio raportoi taloudellisen tuloksen luomalla esimerkiksi tuloslaskeman tai taseen. Yleensä kirjanpitojaksoilla viitataan yrityksen tilikauteen, joka voi koostua useista tilijaksoista, kuten kuukausista tai neljännesvuosista.

Tilikausi ja kalenterivuosi eivät ole samat monissa yrityksissä. Tilikausi voi esimerkiksi päättyä 30.6. eikä 31.12. Uusilla yrityksillä tilikausi voi myös olla pidempi kuin 12 kuukautta.  

[!INCLUDE[prod_short](includes/prod_short.md)] edellyttää kirjanpitojaksoja vain siinä tapauksessa, että haluat sulkea tuloslaskelman tai suorittaa tietojen tiivistystehtäviä. 

Voit käyttää kirjanpitojaksoja raportoinnissa. Näin tehdään esimerkiksi silloin, kun kirjattuja tapahtumia tarkastellaan **Saldo/budjetti**-sivulla, jossa raportointiväli voidaan määrittää. Yksi vaihtoehdoista on raportoinnin määrittäminen kirjanpitojakson mukaan. Voit myös muodostaa KP-raporttimallin, joka vertaa eri kirjanpitojaksojen tuloksia.

## <a name="creating-a-new-fiscal-year"></a>Uuden tilikauden luominen

Voit luoda kirjanpitojaksoja joukkotoiminnolla käyttämällä **Luo tilikausi** -eräajoa tai voit luoda ne manuaalisesti.

### <a name="how-to-create-accounting-periods-in-bulk"></a>Kirjanpitojaksojen luominen joukkotoiminnolla

Jaa tilikausi saman mittaisiksi jaksoiksi **Luo tilikausi** -eräajon avulla.  

1. Valitse ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Kirjanpitojaksot** ja valitse sitten vastaava linkki.  
2. Valitse **Luo vuosi** -toiminto.  <!--What about the Scheduling option? Should we mention that? There's also the Report Output Type field...-->
3. Anna **Aloituspvm**-kenttään päivämäärä, jolloin tilikausi alkaa.  
4. Määrittele **Jaksojen lukumäärä** -kentässä, kuinka moneen kirjanpitojaksoon tilikausi jaetaan. Vuodessa voi olla enintään 365 jaksoa.  
5. Määritä **Jakson pituus** -kentässä kunkin jakson kesto. Esimerkiksi yksi kuukausi on 1K, yksi neljännesvuosi on 1Q ja yksi vuosi 1V.  
6. Valitse **OK**.  

### <a name="how-to-create-accounting-periods-manually"></a>Kirjanpitojaksojen luominen manuaalisesti

Jos tilikauden kirjanpitojaksojen pituudet vaihtelevat, kuten vähittäismyynnissä käytetty 4-4-5-kalenteri, määritys voidaan tehdä manuaalisesti.  
  
1. Valitse ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Kirjanpitojaksot** ja valitse sitten vastaava linkki.  
2. Anna **Aloituspvm**-kenttään päivämäärä, jolloin tilikausi alkaa. **Nimi**-kentässä on kuukauden nimi.  
3. Ilmaise **Uusi tilikausi** -valintaruudun valinnalla, että kyse on vuoden ensimmäisestä jaksosta. [!INCLUDE[prod_short](includes/prod_short.md)] määrittää tämän jakson perusteella, mitkä jaksot sulkevat tilikauden.
4. Toista vaiheet 2 ja 3 kunkin jäljellä olevan jakson kohdalla.  

## <a name="closing-a-fiscal-year"></a>Tilikauden sulkeminen

Tilikauden sulkeminen on yksi kirjojen sulkemistehtävistä. Kun tilikausi on suljettu, **Suljettu**- ja **Pvm lukittu** -valintaruudut valitaan kaikille tilikauden jaksoille. Tilakautta ei voi avata uudelleen eikä valintaruutujen valintaa poistaa.

> [!NOTE]  
> Avoimena on oltava aina ainakin yksi tilikausi. Varmista tilikautta suljettaessa, että tilikausi on luotu. Huomaa myös, että kun tilikausi on suljettu, et voi muuttaa seuraavan tilikauden aloituspäivämäärää.

1. Valitse ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Kirjanpitojaksot** ja valitse sitten vastaava linkki.  
2. Valitse **Sulje vuosi** -toiminto.  

## <a name="posting-entries-to-a-closed-fiscal-year"></a>Tapahtumien kirjaaminen suljettuun tilikauteen

Vaikka tilikausi on suljettu, voit silti kirjata tilikaudelle KP-tapahtumia. Kun teet tämän, tapahtumat merkitään kirjatuiksi suljetulle tilikaudelle ja **Edellisen vuoden tapahtuma** -valintaruutu valitaan. Valintaruutu ei oletusarvoisesti näy sivulla, mutta voit lisätä sen. Seuraavaksi suljetaan tuloslaskelmatilit ja siirretään vuoden tulostaseessa olevalle tilille. Toista nämä vaiheet aina, kun kirjaat tapahtumia suljetulle tilikaudelle.

## <a name="see-also"></a>Katso myös

[Kirjojen sulkeminen](year-close-books.md)  
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[KP-raporttimallien käyttäminen](bi-how-work-account-schedule.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]