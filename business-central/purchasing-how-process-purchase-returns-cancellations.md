---
title: Palautusten tai peruutusten käsittely
description: 'Tässä ohjeaiheessa kerrotaan, miten ostohyvityslasku luodaan kirjataan, kun haluat palauttaa nimikkeitä toimittajalle tai peruuttaa ostetut palvelut.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'cancel, undo, correct'
ms.search.form: '6640, 6643, 9307, 9309, 9308, 6652, 145, 147'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Ostopalautusten tai peruutusten käsittely

Jos haluat palauttaa nimikkeitä toimittajalle tai peruuttaa ostamiasi palveluita, voit luoda ja kirjata ostohyvityslaskun, joka määrittää pyydetyn muutoksen alkuperäisen ostolaskun suhteen. Voit sisällyttää oikeat ostolaskun tiedot luomalla ostohyvityslaskun suoraan kirjatusta ostolaskusta. Vaihtoehtoisesti voit luoda uuden ostohyvityslaskun, johon laskun tiedot on kopioitu.

Jos ostopalautuskäsittelyä, kuten nimikkeen käsittelyn varastoasiakirjoja, on hallittava paremmin tai jos haluat paremman yleiskuvan, kun useiden ostoasiakirjojen nimikkeitä lähetetään takaisin yhtenä ostopalautuksena, voit luoda ostopalautustilauksia. Ostopalautustilaus lähettää automaattisesti liittyvän ostohyvityslaskun. Lisätietoja on kohdassa [Ostopalautustilauksen luominen vähintään yhden kirjatun ostoasiakirjan perusteella](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice).

> [!NOTE]  
> Jos kirjattua ostolaskua ei ole vielä maksettu, voit käyttää kirjatussa ostolaskussa olevia **Korjaa**- tai **Peruuta**-toimintoja kääntääksesi automaattisesti mukana olevat tapahtumat. Nämä toiminnot toimivat vain maksamattomille laskuille eivätkä ne osittaisia palautuksia tai peruutuksia. Myöskään ostotilauksia, joiden kirjaus sisältää vastaanottoja useammasta kuin yhdestä ostotilauksesta, ei voi korjata tai peruuttaa. Lisätietoja on kohdassa [Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

Yleensä toimittajan lähettämän hyvityslaskun jälkeen luodaan ostohyvityslasku tai ostopalautustilaus. Ostohyvityslasku tai ostopalautustilaus toimii hyvityslaskuprosessin sisäisenä dokumentaationa kirjanpitoa varten, tai sen avulla voi hallita liittyvien nimikkeiden toimitusta.

Muutokset voivat liittyä alkuperäisen ostolaskun kaikkiin tuotteisiin tai vain joihinkin tuotteisiin. Näin ollen voit palauttaa osittain vastaanotetut nimikkeet tai vaatia vastaanotettujen palvelujen osittaista korvaamista. Tällöin ostohyvityslaskun tai ostopalautustilauksen tietoja on muokattava.

Alkuperäisen kirjatun ostolaskun lisäksi voit kohdistaa ostohyvityslaskun tai ostopalautustilauksen muihin ostolaskuihin, kuten toiseen kirjattuun ostolaskuun, koska olet palauttamassa tämän laskun kanssa toimitettuja nimikkeitä.

Hyvityslaskun kirjaaminen palauttaa myös mahdolliset kirjattuun asiakirjaan määritetyt nimikekulut, joten nimikkeen arvotapahtumat ovat samat kuin ennen nimikekulun määrittämistä.

## Varaston arvostus
Oikean varaston arvostuksen säilyttämistä varten palautetut nimikkeet poimitaan yleensä varastosta sillä yksikkökustannuksella, jolla ne ostettiin, eikä nykyisellä yksikkökustannuksella. Tätä kutsutaan todellisten kustannusten peruuttamiseksi.

Todellisten kustannusten peruuttamisen automaattista määrittämistä varten on kaksi toimintoa.  

|Toiminto|Description|  
|------------------|---------------------------------------|  
|**Ostopalautustilaus**-sivun **Hae peruutettavat kirjatut asiakirjarivit** -toiminto|Kopioi vähintään yhden ostopalautustilaukseksi peruutettavan kirjatun asiakirjan rivit. Lisätietoja on kohdassa [Ostopalautustilauksen luominen vähintään yhden kirjatun ostoasiakirjan perusteella](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-return-order-based-on-one-or-more-posted-purchase-documents).|  
|**Ostohyvityslasku**- ja **Ostopalautustilaus**-sivujen **Kopioi asiakirjasta** -toiminto|Kopioi sekä otsikon että yhden kirjatun asiakirjan rivit peruutusta varten.<br /><br /> Edellyttää, että **Todellisen kust. peruutt. pakollinen** -valintaruutu on valittuna **Ostojen ja ostovelkojen asetukset** -sivulla.|

Jos haluat määrittää todellisten kustannusten peruuttamisen manuaalisesti, sinun on valittava **Kohdistus nimiketapahtumasta** -kenttä joltakin palautusasiakirjariviltä ja valittava sitten alkuperäisen ostotapahtuman numero. Tämä linkittää ostohyvityslaskun tai ostopalautustilauksen alkuperäiseen ostotapahtumaan ja varmistaa, että nimike arvostetaan alkuperäisissä yksikkökustannuksissa.

Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Varaston arvostus](design-details-inventory-costing.md).

## Ostohyvityslaskun luominen kirjatusta ostolaskusta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut ostolaskut** ja valitse sitten vastaava linkki.  
2. Valitse **Kirjatut ostolaskut** -sivulla kirjattu ostolasku, jonka haluat peruuttaa, ja valitse sitten **Luo korjaava hyvityslasku** -toiminto.

    Useimpiin ostohyvityslaskun otsikon kenttiin täytetään kirjatun ostolaskun tiedot. Voit muokata kaikkia kenttiä, kuten esimerkiksi palautussopimusta vastaavia uusia tietoja.
3. Muokkaa sopimuksen mukaan rivien tietoja, kuten palautettujen nimikkeiden määrää tai hyvitettävää summaa.
4. Valitse **Kohdista tapahtumat** -toiminto.
5. Valitse **Kohdista toimittajatapaht.** -sivulla rivi, joka sisältää ostohyvityslaskuun kohdistettavan kirjatun ostoasiakirjan. Valitse sitten **Kohdistetaan tunnisteeseen** -toiminto. Ostohyvityslaskun numero lisätään **Kohdistetaan tunnisteeseen** -kenttään.
6. Syötä **Kohdistettava summa** -kenttään kohdistettava summa, jos se on pienempi kuin alkuperäinen summa.

    **Kohdista toimittajatapahtumat** -sivun alaosassa näkyy kokonaissumma, joka kohdistetaan kaikkien mukaan kuuluvien tapahtumien peruuttamiseksi, kun **Saldo**-kentän arvo on nolla.
7. Valitse **OK**-painike. Kun ostohyvityslasku kirjataan, se kohdistetaan määritettyihin kirjattuihin ostoasiakirjoihin.

    Kun olet luonut tarvittavat ostohyvityslaskun rivit tai muokannut niitä ja yksi tai useita sovelluksia on määritetty, voit siirtyä kirjaamaan ostohyvityslaskun.
8. Valitse **Kirjaa**-toiminto.

Tiliöidyt ostolaskut, joita käytät hyvityslaskuun, on nyt kumottu. Jos olet jo maksanut alkuperäisen laskun, toimittajan pitäisi nyt hyvittää maksu sinulle. Jos hyvityslasku on vain osalle alkuperäisen laskun tuotetta, voit maksaa vain alkuperäisen ostolaskun jäljellä olevan summan sen sulkemiseksi.

Ostohyvityslasku poistetaan ja korvataan uudella kirjattujen ostohyvityslaskujen luettelon asiakirjalla.

## Uuden ostohyvityslaskun luominen kopioimalla kirjattu ostolaskun

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostohyvityslaskut** ja valitse sitten vastaava linkki.
2. Avaa uusi tyhjä ostohyvityslasku valitsemalla **Uusi**-toiminto.
3. Syötä **Toimittaja**-kenttään nykyisen toimittajan nimi.
4. Valitse **Kopioi asiakirjasta** -toiminto.
5. Valitse **Kopioi ostoasiakirja** -sivun **Asiakirjan tyyppi** -kentässä **Kirjattu lasku**.
6. Valitse **Asiakirjanro**-kenttä, jos haluat avata **Kirjatut ostolaskut** -sivun, ja valitse sitten kirjattu ostolasku, joka sisältää peruutettavat rivit.
7. Valitse **Laske rivit uudelleen** -valintaruutu, jos haluat päivittää kopioidut kirjatut ostolaskurivit nimikkeen hinta- ja yksikkökustannusten muutoksilla, jotka ovat tapahtuneet laskun kirjaamisen jälkeen.
8. Valitse **OK**-painike. Kopioidut laskurivit lisätään ostohyvityslaskuun.
9. Täytä ostohyvityslasku kohdan [Ostohyvityslaskun luominen kirjatusta ostolaskusta](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice) mukaisesti.

## Ostopalautustilauksen luominen vähintään yhden kirjatun ostoasiakirjan perusteella

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostopalautustilaukset** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät.
4. Täytä **Rivit**-pikavälilehdessä rivit manuaalisesti. Jos kopioit tiedot muista asiakirjoista, rivit täytetään automaattisesti:

    - Voit kopioida vähintään yhden kirjatun asiakirjarivin vähintään yhdestä kirjatusta asiakirjasta **Hae peruutettavat kirjatut asiakirjarivit** -toiminnolla. Tämä toiminto peruuttaa aina todelliset kustannukset kirjatusta asiakirjarivistä. Tätä toimintoa käsitellään seuraavissa vaiheissa.    
    - Voit kopioida aiemmin luodun asiakirjan palautustilaukseen **Kopioi asiakirjasta** -toiminnolla. Käytä tätä toimintoa, kun kopioit koko asiakirjan. Se voi olla kirjattu asiakirja tai asiakirja, jota ei ole vielä kirjattu. Voit peruuttaa tällä toiminnolla todelliset kustannukset vain silloin, kun **Todellisen kust. peruutt. pakollinen** -valintaruutu on valittu **Myyntien ja saamisten asetukset** -sivulla.  

5. Valitse **Hae peruutettavat kirjatut asiakirjarivit** -toiminto.
6. Valitse **Kirjatut ostoasiakirjarivit** -sivun yläosassa **Näytä vain peruutettavat rivit** -valintaruutu, jos haluat nähdä vain palauttamattomia määriä sisältävät rivit. Jos esimerkiksi kirjattu ostolaskun määrä on jo palautettu, et ehkä halua sisällyttää määrää uuteen ostopalautusasiakirjaan.

    > [!NOTE]  
    >  Tämä kenttä toimii vain kirjattujen vastaanottojen ja kirjattujen laskutusrivien kohdalla. Se ei toimi kirjattujen palautusten tai kirjattujen hyvityslaskurivien kohdalla.  

    Sivun vasemmalla puolella on luettelossa eri asiakirjatyyppejä. Suluissa oleva luku ilmoittaa, kuinka monta asiakirjaa kyseistä asiakirjatyyppiä varten on käytettävissä.

7. Valitse **Asiakirjatyyppisuodatin**-kentässä kirjattujen asiakirjarivien tyyppi, jota haluat käyttää.  
8. Valitse uuteen asiakirjaan kopioitavat rivit.  

    > [!NOTE]  
    >  Jos kaikki rivit valitaan näppäinyhdistelmällä <kbd>Ctrl</kbd>+<kbd>A</kbd>, kaikki määritetyssä suodattimessa olevat rivit kopioidaan mutta **Näytä vain peruutettava määrä** -suodatin ohitetaan. Oletetaan esimerkiksi, että olet suodattanut tietyn asiakirjanumeron rivit kahteen riviin, joista toinen on palautettu. Jos käytät kopioinnissa <kbd>Ctrl</kbd>+<kbd>A</kbd>-näppäimiä, vaikka **Näytä vain peruutettava määrä** -kenttä on valittuna, molemmat rivit kopioidaan eikä vain rivi, jota ei ole vielä peruutettu.  

9. Kopioi rivit uuteen asiakirjaan valitsemalla **OK**.  

    Seuraavat toimenpiteet suoritetaan:  

    - Tyyppiä **Nimike** oleville kirjatuille asiakirjariveille luodaan uusi asiakirjarivi, joka on kirjatun asiakirjarivin kopio, jolla on määrä, jota ei ole vielä varattu. **Kohdista nimiketapahtumaan** -kenttä on täytetty soveltuvalla kirjatun asiakirjarivin nimiketapahtuman numerolla.  

    - Niille kirjatuille asiakirjariveille, joiden tyyppi ei ole **Nimike** (kuten nimikekulut) ohjelma luo uuden asiakirjarivin, joka on alkuperäisen kirjatun asiakirjarivin kopio.  

    - Laskee uuden rivin **Yksikkökustannus (PVA)** -kentän arvon vastaavan nimiketapahtumien kustannuksista.  

    - Jos kopioitu asiakirja on kirjattu toimitus, kirjattu vastaanotto, kirjattu palautusvastaanotto tai kirjattu palautustoimitus, ohjelma laskee yksikköhinnan nimikekortista.  

    - Jos kopioitu asiakirja on kirjattu lasku tai hyvityslasku, ohjelma kopioi kirjatun asiakirjarivin yksikköhinnan, laskualennukset ja rivialennukset.  

    - Jos kirjattu asiakirjarivi sisältää nimikkeen seurantarivejä, ohjelma täyttää **Kohdista nimiketapahtumaan** -kenttään kirjattujen nimikkeen seurantarivien soveltuvien nimiketapahtumien numerot.  

     Kun kopioit kirjatusta laskusta tai kirjatusta hyvityslaskusta, sovellus kopioi kaikki asiakirjan kirjaushetkellä kelvolliset laskualennukset ja rivialennuksen kirjatusta asiakirjarivistä uuteen asiakirjariviin. Huomaa kuitenkin, että jos **Lask. laskun alennus** -asetus on määritettynä **Ostojen ja ostovelkojen asetukset** -sivulla, laskun alennus lasketaan uudelleen, kun kirjaat uuden asiakirjarivin. Uuden rivin rivisumma voikin tämän vuoksi poiketa kirjatun asiakirjarivin rivisummasta laskun alennuksen uuden laskennan tuloksen mukaan.  

    > [!NOTE]  
    >  Jos osa kirjatun asiakirjarivin määrää on jo peruutettu (palautettu), myyty tai kulutettu, ohjelma luo rivin vain varastossa olevalle määrälle tai määrälle, jota ei ole palautettu. Jos kirjatun asiakirjarivin koko määrä on peruutettu (palautettu), ohjelma ei luo uutta asiakirjariviä.  
    >
    >  Jos kirjatun asiakirjan tavaravirta on sama kuin uuden asiakirjan tavaravirta, ohjelma yksinkertaisesti luo alkuperäisen kirjatun asiakirjarivin kopion uuteen asiakirjaan. **Kohdistus nimiketapahtumasta** -kenttää ei täytetä, koska tässä tapauksessa todellisten kustannusten peruuttaminen ei ole mahdollista. Jos esimerkiksi käytät **Hae peruutettavat kirjatut asiakirjarivit** -toimintoa kirjatun ostohyvityslaskurivin hakemisessa uuteen ostohyvityslaskuun, vain alkuperäinen kirjattu hyvityslaskurivi kopioidaan uuteen hyvityslaskuun.  

10. Valitse **Ostopalautustilaus**-sivun kunkin rivin **Palautuksen syykoodi** -kentässä palautuksen syy.
11. Valitse **Kirjaa**-toiminto.

## Korvaavan ostotilauksen luominen ostopalautustilauksesta

Voit sopia toimittajan kanssa, että toimittaja hyvittää ostetun nimikkeen vaihtamalla sen. Vaihdettava nimike voi olla joko sama nimike tai kokonaan eri nimike. Tällainen tilanne voi ilmetä, kun toimittaja on toimittanut epähuomiossa väärän nimikkeen.  

1.  Tee korvaavalle nimikkeelle aktiivisen palautuskäsittelyn **Ostopalautustilaus**-sivun tyhjällä rivillä negatiivinen tapahtuma lisäämällä negatiivinen summa **Määrä**-kenttään.  
2. Valitse **Siirrä negatiiviset rivit** -toiminto.  
3. Täytä **Siirrä negat. ostorivit** -sivulla tarvittavat kentät.
4. Valitse **OK**-painike. Negatiivinen rivi poistetaan ostopalautustilauksesta ja uusi ostotilaus luodaan. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).  

## Ostoalennuksen luominen

Jos vastaanotat toimittajaltasi nimikkeitä, jotka eivät ole sellaisia kuin halusit – ne ovat esimerkiksi hieman vahingoittuneita, väärän värisiä tai väärän kokoisia – toimittaja voi tarjota ostoalennusta.  

Tämän alennetun ostokustannuksen voi kirjata nimikekuluna hyvityslaskuun tai palautustilaukseen sekä linkittää kirjattuun vastaanottoon. Seuraavassa se käsitellään ostopalautustilauksen osalta, mutta samat vaiheet koskevat myös ostohyvityslaskua.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostohyvityslaskut** ja valitse sitten vastaava linkki.
2. Avaa uusi tyhjä ostohyvityslasku valitsemalla **Uusi**-toiminto.  
3. Täytä hyvityslaskun otsikko sen toimittajan tiedoilla, joka on lähettänyt ostoalennuksen.  
4. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä **Kulu (nimike)**.  
5. Valitse **Nro**-kenttään asiaankuuluva nimikekulun arvo.  

    Voit haluta luoda erityisen nimikekulunumeron koskemaan ostoalennuksia.  
6. Syötä **Määrä**-kenttään **1**.  
7. Syötä **Välitön yksikkökustannus** -kenttään ostoalennuksen summa.  
8. Määritä ostoalennus nimikekuluna kirjatussa vastaanotossa oleville nimikkeille. Lisätietoja on kohdassa [Kaupan lisäkustannusten huomiointi nimikekulujen avulla](payables-how-assign-item-charges.md) Kun olet määrittänyt alennuksen, siirry takaisin **Ostohyvityslasku**-sivulle.

Kun kirjaat ostopalautustilauksen, ostoalennus lisätään liittyvän ostotapahtuman summaan. Tällä tavoin voit ylläpitää täsmällistä varaston arvostusta.  

## Palautustoimitusten yhdistäminen

Jos haluat palauttaa eri ostopalautustilauksissa olevia nimikkeitä samalle toimittajalle, voit käyttää **Yhdistä palautustoimitukset** -funktiota.  

Kun toimitat nimikkeitä, kirjaat asianmukaiset ostopalautustilaukset toimitetuiksi eli luot kirjattuja ostopalautustoimituksia.  

Sitten kun olet valmis laskuttamaan nämä nimikkeet, voit luoda ostopalautustilauksen ja kopioida automaattisesti kirjatut ostohyvityslaskun tähän asiakirjaan, sen sijaan että laskuttaisit jokaisen ostopalautustilauksen rivit erikseen. Sen jälkeen voit kirjata ostohyvityslaskun ja laskuttaa kaikki avoimet ostopalautustilaukset kätevästi kerralla.  

Kun palautustilaukset yhdistetään hyvityslaskuun ja kirjataan, laskutetuista riveistä luodaan kirjattu ostohyvityslasku. Alkuperäisen ostopalautustilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän mukaan. Tätä alkuperäistä ostopalautustilausta ei kuitenkaan ole poistettu, vaikka se on kokonaan vastaanotettu ja laskutettu. Sen vuoksi ostopalautustilaus on poistettava manuaalisesti.

> [!NOTE]  
> Oletetaan esimerkiksi, että toimittajalla on useita toimitetuiksi kirjattuja ostopalautustilauksia.     

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostohyvityslaskut** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät.  
4. Valitse **Hae palautustoimitusrivit** -toiminto.  
5. Valitse useat palautustoimituksen rivit, jotka haluat sisällyttää laskuun:  

    Jos on valittu väärä palautustoimitusrivi tai jos haluat aloittaa alusta, voit poistaa rivit ostohyvityslaskusta ja suorittaa **Hae palautustoimituksen rivit** -toiminnon uudelleen.  
6. Valitse **Kirjaa**-toiminto.  

### Poista avoin ostotilaus yhdistetyn palautustoimituksen kirjauksen jälkeen  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poista laskutetut ostopalautustilaukset** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät ja valitse sitten **OK**-painike.  
3. Voit poistaa yksittäiset ostopalautustilaukset myös manuaalisesti.

## Katso myös
[Osto](purchasing-manage-purchasing.md)  
[Ostojen kirjaaminen](purchasing-how-record-purchases.md)  
[Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Myynnin palautusten tai peruutusten käsittely](sales-how-process-sales-returns-cancellations.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
