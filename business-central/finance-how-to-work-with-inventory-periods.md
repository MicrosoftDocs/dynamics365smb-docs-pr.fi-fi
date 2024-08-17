---
title: Varastokausien käsitteleminen
description: 'Määrittämällä varastokauden voi hallita aikajaksoa, jolloin henkilöt voivat kirjata muutoksia varastoon.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'inventory, periods'
ms.search.form: 5828
ms.date: 07/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="work-with-inventory-periods"></a>Varastokausien käsitteleminen

Varastokaudet määrittävät aikajakson, jolloin voit kirjata varastoon muutoksia. Lopetuspäivämäärä määrittää, milloin varastokausi loppuu. Kun suljet varastokauden, et voi kirjata varastoon odotettuja tai laskutettuja muutoksia ennen tätä lopetuspäivämäärää. Et voi kirjata varastoon uusia arvoja ennen lopetuspäivämäärää. Jos suljetulla ajanjaksolla on avoimia nimiketapahtumia eli positiivisia määriä, joita ei ole vielä kohdistettu lähtevissä transaktioissa, voit silti kohdistaa lähteviä määriä näihin tapahtumiin, vaikka kausi olisi suljettu.  

Seuraavissa luvuissa kerrotaan, miten

* varastokausia luodaan  
* varastokausia suljetaan  
* varastokausia avataan uudelleen.  

## <a name="to-create-an-inventory-period"></a>Varastokauden luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastokaudet** ja valitse sitten vastaava linkki.  
2. Luo uusi rivi.  
3. Syötä **Lopetuspvm**-kenttään viimeinen päivämäärä, jonka haluat varastokaudelle määrittää. Kun kausi on suljettu, et voi kirjata varaston muutoksia ennen kyseistä päivämäärää.  
4. Anna **Nimi**-kenttään kuvaava nimi. Valitse **OK**-painike.  

## <a name="to-close-inventory-periods"></a>Varastokausien sulkeminen

**Suljettu**-kenttä osoittaa, onko varastokausi suljettu varaston arvon muutoksilta. Et voi muokata tätä kenttää.  

Voit sulkea minkä tahansa varastokauden, jos seuraavat ehdot täyttyvät:  

* Kaudella ei ole avoimia lähteviä nimiketapahtumia eli negatiivista varastoa.  
* Kaikkien nimikkeiden kustannus on muutettu **Muuta kustannuksia - Nimiketapahtumat** -eräajon avulla.  

Tällöin kaikki lähtevät transaktiot, kuten myyntitilausten, lähtevien siirtojen, myyntilaskujen, ostopalautusten ja ostohyvityslaskujen transaktiot, on kohdistettava varastomäärään.  

### <a name="to-close-an-inventory-period"></a>Sulje varastokausi

1. Valitse **Muuta kustannuksia - Nimiketapahtumat** -toiminto ennen varastokauden sulkemista. Näin voit varmistaa, että kaikkien kustannusten muutokset on kirjattu.

     **Suorita Sulje varastokausi - Testi -** raportti määrittääksesi, onko varastokaudella avoimia lähteviä nimiketapahtumia vai nimikkeitä, joiden kustannuksia ei ole vielä muutettu.  
2. Valitse **Testiraportti**-toiminto.  

    Suorittamalla **Kirjaa varaston kustannus KP:oon** -eräajon voit varmistaa, että kaikki kustannukset on viety pääkirjanpitoon.  
3. Valitse **Kirjaa varasto kirjanpitoon** -toiminto.  
4. Valitse suljettava varastokausi **Varastokaudet**-sivulla.  
5. Valitse **Sulje varastokausi** -toiminto. Kun varastokausi on suljettu, et voi kirjata varaston muutoksia ennen lopetuspäivämäärää. Kaikkien nimikkeiden kustannus on muutettava **Muuta kustannuksia - Nimiketapahtumat** -eräajolla ennen varastokauden sulkemista.  
6. Valitse **Kyllä** voit sulkea kauden tai valitse **Ei**, jos haluat peruuttaa sulkemisen.  
7. Varastokausi on suljettu, ja kun se on valmis, näyttöön tulee vahvistussanoma.  

## <a name="reopening-inventory-periods"></a>Varastokausien avaaminen uudelleen
Kun olet sulkenut varastokauden, et voi poistaa varastokautta. Voit kuitenkin avata sen uudelleen, jos haluat sallia kirjaukset ennen varastokauden lopetuspäivämäärää. Kauden avaaminen uudelleen avaa myös kaikki varastokaudet, joilla on avattua kautta myöhäisemmät lopetuspäivämäärät.  

### <a name="to-reopen-an-inventory-period"></a>Avaa varastokausi uudelleen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastokaudet** ja valitse sitten vastaava linkki.  
2. Valitse uudelleen avattava varastokausi.  
3. Valitse **Avaa kausi uudelleen** -toiminto. Vahvista, että haluat avata kauden uudelleen.  
4. Kaikki varastojaksot, joiden lopetuspäivämäärät ovat valittua myöhäisemmät, avataan uudelleen.  

## <a name="see-also"></a>Katso myös
[Suunnittelun yksityiskohdat: Varastokaudet](design-details-inventory-periods.md)    
[Rahoitus](finance.md)    
[Vaihto-omaisuus](inventory-manage-inventory.md)    
[Financialsin käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
