---
title: "Palautusten tai peruutusten käsittely ostohyvityslaskujen avulla | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten ostohyvityslasku luodaan kirjataan, kun haluat palauttaa nimikkeitä toimittajalle tai peruuttaa ostetut palvelut."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cancel, undo, correct
ms.date: 08/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 114448607d8b99252573912d2df08f91e1d27c76
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-process-purchase-returns-or-cancellations"></a>Toimintaohje: tavaran palautuksen tai peruutuksen käsittely
Jos haluat palauttaa nimikkeitä toimittajalle tai peruuttaa ostamiasi palveluita, voit luoda ja kirjata ostohyvityslaskun, joka määrittää pyydetyn muutoksen alkuperäisen ostolaskun suhteen. Voit sisällyttää oikeat ostolaskun tiedot luomalla ostohyvityslaskun suoraan kirjatusta ostolaskusta. Vaihtoehtoisesti voit luoda uuden ostohyvityslaskun, johon laskun tiedot on kopioitu.

Jos ostopalautuskäsittelyä, kuten nimikkeen käsittelyn varastoasiakirjoja, on hallittava paremmin tai jos haluat paremman yleiskuvan, kun useiden ostoasiakirjojen nimikkeitä lähetetään takaisin yhtenä ostopalautuksena, voit luoda ostopalautustilauksia. Ostopalautustilaus lähettää automaattisesti liittyvän ostohyvityslaskun. Lisätietoja on kohdassa Ostopalautustilauksen luominen vähintään yhden kirjatun ostoasiakirjan perusteella.

> [!NOTE]  
>   Jos kirjattua ostolaskua ei ole vielä maksettu, voit käyttää kirjatussa ostolaskussa olevia **Korjaa**- tai **Peruuta**-toimintoja kääntääksesi automaattisesti mukana olevat tapahtumat. Nämä toiminnot toimivat vain maksamattomille laskuille eivätkä ne osittaisia palautuksia tai peruutuksia. Lisätietoja on kohdassa [Toimintaohje: Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

Yleensä toimittajan lähettämän hyvityslaskun jälkeen luodaan ostohyvityslasku tai ostopalautustilaus. Ostohyvityslasku tai ostopalautustilaus toimii hyvityslaskuprosessin sisäisenä dokumentaationa kirjanpitoa varten, tai sen avulla voi hallita liittyvien nimikkeiden toimitusta.

Muutokset voivat liittyä alkuperäisen ostolaskun kaikkiin tuotteisiin tai vain joihinkin tuotteisiin. Näin ollen voit palauttaa osittain vastaanotetut nimikkeet tai vaatia vastaanotettujen palvelujen osittaista korvaamista. Tällöin ostohyvityslaskun tai ostopalautustilauksen tietoja on muokattava.

Alkuperäisen kirjatun ostolaskun lisäksi voit kohdistaa ostohyvityslaskun tai ostopalautustilauksen muihin ostolaskuihin, kuten toiseen kirjattuun ostolaskuun, koska olet palauttamassa tämän laskun kanssa toimitettuja nimikkeitä.

Hyvityslaskun kirjaaminen palauttaa myös mahdolliset kirjattuun asiakirjaan määritetyt nimikekulut, joten nimikkeen arvotapahtumat ovat samat kuin ennen nimikekulun määrittämistä.

## <a name="inventory-costing"></a>Varaston arvostus
Oikean varaston arvostuksen säilyttämistä varten palautetut nimikkeet poimitaan yleensä varastosta sillä yksikkökustannuksella, jolla ne ostettiin, eikä nykyisellä yksikkökustannuksella. Tätä kutsutaan todellisten kustannusten peruuttamiseksi.

Todellisten kustannusten peruuttamisen automaattista määrittämistä varten on kaksi toimintoa.  

|Toiminto|Kuvaus|  
|------------------|---------------------------------------|  
|**Ostopalautustilaus**-ikkunan **Hae peruutettavat kirjatut asiakirjarivit** -toiminto|Kopioi vähintään yhden ostopalautustilaukseksi peruutettavan kirjatun asiakirjan rivit. Lisätietoja on kohdassa Ostopalautustilauksen ja liittyvän ostohyvityslaskun luominen vähintään yhdelle kirjatulle ostolaskulle.|  
|**Ostohyvityslasku**- ja **Ostopalautustilaus**-ikkunoiden **Kopioi asiakirja** -toiminto|Kopioi sekä otsikon että yhden kirjatun asiakirjan rivit peruutusta varten.<br /><br /> Edellyttää, että **Todellisen kust. peruutt. pakollinen** -valintaruutu on valittuna **Ostojen ja ostovelkojen asetukset** -ikkunassa.|

Jos haluat määrittää todellisten kustannusten peruuttamisen manuaalisesti, sinun on valittava **Kohdistus nimiketapahtumasta** -kenttä joltakin palautusasiakirjariviltä ja valittava sitten alkuperäisen ostotapahtuman numero. Tämä linkittää ostohyvityslaskun tai ostopalautustilauksen alkuperäiseen ostotapahtumaan ja varmistaa, että nimike arvostetaan alkuperäisissä yksikkökustannuksissa.

Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Varaston arvostus](design-details-inventory-costing.md).

## <a name="to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice"></a>Ostohyvityslaskun luominen kirjatusta ostolaskusta
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kirjatut ostolaskut** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Kirjatut ostolaskut** -ikkunassa kirjattu ostolasku, jonka haluat peruuttaa, ja valitse sitten **Luo korjaava hyvityslasku** -toiminto.

    Useimpiin ostohyvityslaskun otsikon kenttiin täytetään kirjatun ostolaskun tiedot. Voit muokata kaikkia kenttiä, kuten esimerkiksi palautussopimusta vastaavia uusia tietoja.
3. Muokkaa sopimuksen mukaan rivien tietoja, kuten palautettujen nimikkeiden määrää tai hyvitettävää summaa.
4. Valitse **Kohdista tapahtumat** -toiminto.
5. Valitse **Kohdista toimittajatapaht.** -ikkunassa rivi, joka sisältää ostohyvityslaskuun kohdistettavan kirjatun ostoasiakirjan. Valitse sitten **Kohdistetaan tunnisteeseen** -toiminto. Ostohyvityslaskun numero lisätään **Kohdistetaan tunnisteeseen** -kenttään.
6. Syötä **Kohdistettava summa** -kenttään kohdistettava summa, jos se on pienempi kuin alkuperäinen summa.

    **Kohdista toimittajatapaht.** -ikkunan alaosassa näkyy kokonaissumma, joka kohdistetaan kaikkien mukaan kuuluvien tapahtumien peruuttamiseksi, kun **Saldo**-kentän arvo on nolla.
7. Valitse **OK**-painike. Kun ostohyvityslasku kirjataan, se kohdistetaan määritettyihin kirjattuihin ostoasiakirjoihin.

    Kun olet luonut tarvittavat ostohyvityslaskun rivit tai muokannut niitä ja yksi tai useita sovelluksia on määritetty, voit siirtyä kirjaamaan ostohyvityslaskun.
8. Valitse **Kirjaa**-toiminto.

Tiliöidyt ostolaskut, joita käytät hyvityslaskuun, on nyt kumottu. Jos olet jo maksanut alkuperäisen laskun, toimittajan pitäisi nyt hyvittää maksu sinulle. Jos hyvityslasku on vain osalle alkuperäisen laskun tuotetta, voit maksaa vain alkuperäisen ostolaskun jäljellä olevan summan sen sulkemiseksi.

Ostohyvityslasku poistetaan ja korvataan uudella kirjattujen ostohyvityslaskujen luettelon asiakirjalla.

## <a name="to-create-a-purchase-credit-memo-by-copying-a-posted-purchase-invoice"></a>Uuden ostohyvityslaskun luominen kopioimalla kirjattu ostolaskun
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostohyvityslaskut** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa uusi tyhjä ostohyvityslasku valitsemalla **Uusi**-toiminto.
3. Syötä **Toimittaja**-kenttään nykyisen toimittajan nimi.
4. Valitse **Kopioi asiakirja** -toiminto.
5. Valitse **Kopioi ostoasiakirja** -ikkunan **Asiakirjan tyyppi** -kentässä **Kirjattu lasku**.
6. Valitse **Asiakirjanro**-kenttä, jos haluat avata **Kirjatut ostolaskut** -ikkunan, ja valitse sitten kirjattu ostolasku, joka sisältää peruutettavat rivit.
7. Valitse **Laske rivit uudelleen** -valintaruutu, jos haluat päivittää kopioidut kirjatut ostolaskurivit nimikkeen hinta- ja yksikkökustannusten muutoksilla, jotka ovat tapahtuneet laskun kirjaamisen jälkeen.
8. Valitse **OK**-painike. Kopioidut laskurivit lisätään ostohyvityslaskuun.
9. Täytä ostohyvityslasku tämän ohjeaiheen "Ostohyvityslaskun luominen kirjatusta ostolaskusta" -osassa esitetyllä tavalla.

## <a name="to-create-a-purchase-return-order-based-on-one-or-more-a-posted-purchase-documents"></a>Ostopalautustilauksen luominen vähintään yhden kirjatun ostoasiakirjan perusteella
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostopalautustilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät.
4. Täytä **Rivit**-pikavälilehdessä rivit manuaalisesti. Jos kopioit tiedot muista asiakirjoista, rivit täytetään automaattisesti:

    - Voit kopioida vähintään yhden kirjatun asiakirjarivin vähintään yhdestä kirjatusta asiakirjasta **Hae peruutettavat kirjatut asiakirjarivit** -toiminnolla. Tämä toiminto peruuttaa aina todelliset kustannukset kirjatusta asiakirjarivistä. Tätä toimintoa käsitellään seuraavissa vaiheissa.    
    - Voit kopioida aiemmin luodun asiakirjan palautustilaukseen **Kopioi asiakirja** -toiminnolla. Käytä tätä toimintoa, kun kopioit koko asiakirjan. Se voi olla kirjattu asiakirja tai asiakirja, jota ei ole vielä kirjattu. Voit peruuttaa tällä toiminnolla todelliset kustannukset vain silloin, kun **Todellisen kust. peruutt. pakollinen** -valintaruutu on valittu**Myyntien ja saamisten asetukset** -ikkunassa.  

4. Valitse **Hae peruutettavat kirjatut asiakirjarivit** -toiminto.
5. Valitse **Kirjatut ostoasiakirjarivit** -ikkunan yläosassa **Näytä vain peruutettavat rivit** -valintaruutu, jos haluat nähdä vain palauttamattomia määriä sisältävät rivit. Jos esimerkiksi kirjattu ostolaskun määrä on jo palautettu, et ehkä halua sisällyttää määrää uuteen ostopalautusasiakirjaan.

    > [!NOTE]  
    >  Tämä kenttä toimii vain kirjattujen vastaanottojen ja kirjattujen laskutusrivien kohdalla. Se ei toimi kirjattujen palautusten tai kirjattujen hyvityslaskurivien kohdalla.  

    Ikkunan vasemmalla puolella on luettelossa eri asiakirjatyyppejä. Suluissa oleva luku ilmoittaa, kuinka monta asiakirjaa kyseistä asiakirjatyyppiä varten on käytettävissä.

6. Valitse **Asiakirjatyyppisuodatin**-kentässä kirjattujen asiakirjarivien tyyppi, jota haluat käyttää.  
7. Valitse uuteen asiakirjaan kopioitavat rivit.  

    > [!NOTE]  
    >  Jos käytät rivien kopioinnissa Ctrl+A -näppäimiä, ohjelma kopioi kaikki rivit määrittämäsi suodattimen mukaan. Ohjelma ei kuitenkaan huomioi **Näytä vain peruutettava määrä** -suodatinta. Oletetaan esimerkiksi, että olet suodattanut tietyn asiakirjanumeron rivit kahteen riviin, joista toinen on palautettu. Jos käytät kopioinnissa Ctrl+A-näppäimiä, kun **Näytä vain peruutettava määrä** -kenttä on valittuna, pelkän varaamattoman rivin sijaan kopioidaan molemmat rivit.  

8. Kopioi rivit uuteen asiakirjaan valitsemalla **OK**.  

    Seuraavat toimenpiteet suoritetaan:  

    -   Tyyppiä **Nimike** oleville kirjatuille asiakirjariveille luodaan uusi asiakirjarivi, joka on kirjatun asiakirjarivin kopio, jolla on määrä, jota ei ole vielä varattu. **Kohdista nimiketapahtumaan** -kenttä on täytetty soveltuvalla kirjatun asiakirjarivin nimiketapahtuman numerolla.  

    -   Niille kirjatuille asiakirjariveille, joiden tyyppi ei ole **Nimike** (kuten nimikekulut) ohjelma luo uuden asiakirjarivin, joka on alkuperäisen kirjatun asiakirjarivin kopio.  

    -   Laskee uuden rivin **Yksikkökustannus (PVA)** -kentän arvon vastaavan nimiketapahtumien kustannuksista.  

    -   Jos kopioitu asiakirja on kirjattu toimitus, kirjattu vastaanotto, kirjattu palautusvastaanotto tai kirjattu palautustoimitus, ohjelma laskee yksikköhinnan nimikekortista.  

    -   Jos kopioitu asiakirja on kirjattu lasku tai hyvityslasku, ohjelma kopioi kirjatun asiakirjarivin yksikköhinnan, laskualennukset ja rivialennukset.  

    -   Jos kirjattu asiakirjarivi sisältää nimikkeen seurantarivejä, ohjelma täyttää **Kohdista nimiketapahtumaan** -kenttään kirjattujen nimikkeen seurantarivien soveltuvien nimiketapahtumien numerot.  

     Kun kopioit kirjatusta laskusta tai kirjatusta hyvityslaskusta, ohjelma kopioi kaikki asiakirjan kirjaushetkellä kelvolliset laskualennukset ja rivialennuksen kirjatusta asiakirjarivistä uuteen asiakirjariviin. Huomaa kuitenkin, että jos **Lask. laskun alennus** -asetus on määritettynä **Ostojen ja ostovelkojen asetukset** -ikkunassa, laskun alennus lasketaan uudelleen, kun kirjaat uuden asiakirjarivin. Uuden rivin rivisumma voikin tämän vuoksi poiketa kirjatun asiakirjarivin rivisummasta laskun alennuksen uuden laskennan tuloksen mukaan.  

    > [!NOTE]  
    >  Jos osa kirjatun asiakirjarivin määrää on jo peruutettu (palautettu), myyty tai kulutettu, ohjelma luo rivin vain varastossa olevalle määrälle tai määrälle, jota ei ole palautettu. Jos kirjatun asiakirjarivin koko määrä on peruutettu (palautettu), ohjelma ei luo uutta asiakirjariviä.  
    >   
    >  Jos kirjatun asiakirjan tavaravirta on sama kuin uuden asiakirjan tavaravirta, ohjelma yksinkertaisesti luo alkuperäisen kirjatun asiakirjarivin kopion uuteen asiakirjaan. **Kohdistus nimiketapahtumasta** -kenttää ei täytetä, koska tässä tapauksessa todellisten kustannusten peruuttaminen ei ole mahdollista. Jos esimerkiksi käytät **Hae peruutettavat kirjatut asiakirjarivit** -toimintoa kirjatun ostohyvityslaskurivin hakemisessa uuteen ostohyvityslaskuun, vain alkuperäinen kirjattu hyvityslaskurivi kopioidaan uuteen hyvityslaskuun.  

8. Valitse **Ostopalautustilaus**-ikkunan kunkin rivin **Palautuksen syykoodi** -kentässä palautuksen syy.
9. Valitse **Kirjaa**-toiminto.

## <a name="to-create-a-replacement-purchase-order-from-a-purchase-return-order"></a>Korvaavan ostotilauksen luominen ostopalautustilauksesta
Voit sopia toimittajan kanssa, että toimittaja hyvittää ostetun nimikkeen vaihtamalla sen. Vaihdettava nimike voi olla joko sama nimike tai kokonaan eri nimike. Tällainen tilanne voi ilmetä, kun toimittaja on toimittanut epähuomiossa väärän nimikkeen.  
1.  Tee korvaavalle nimikkeelle aktiivisen palautuskäsittelyn **Ostopalautustilaus**-ikkunan tyhjällä rivillä negatiivinen tapahtuma lisäämällä negatiivinen summa **Määrä**-kenttään.  
2. Valitse **Siirrä negatiiviset rivit** -toiminto.  
3. Täytä **Siirrä negatiiviset ostorivit**-ikkunassa tarvittavat kentät.
4. Valitse **OK**-painike. Negatiivinen rivi poistetaan ostopalautustilauksesta ja uusi ostotilaus luodaan. Lisätietoja on ohjeaiheessa [Toimintaohje: Ostojen kirjaaminen](purchasing-how-record-purchases.md).  

## <a name="to-create-a-purchase-allowance"></a>Ostoalennuksen luominen  
Jos vastaanotat toimittajaltasi nimikkeitä, jotka eivät ole sellaisia kuin halusit – ne ovat esimerkiksi hieman vahingoittuneita, väärän värisiä tai väärän kokoisia – toimittaja voi tarjota ostoalennusta.  

Tämän alennetun ostokustannuksen voi kirjata nimikekuluna hyvityslaskuun tai palautustilaukseen sekä linkittää kirjattuun vastaanottoon. Seuraavassa se käsitellään ostopalautustilauksen osalta, mutta samat vaiheet koskevat myös ostohyvityslaskua.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostohyvityslaskut** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa uusi tyhjä ostohyvityslasku valitsemalla **Uusi**-toiminto.  
3.  Täytä hyvityslaskun otsikko sen toimittajan tiedoilla, joka on lähettänyt ostoalennuksen.  
4. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä **Kulu (nimike)**.  
5.  Valitse **Nro**-kenttään asiaankuuluva nimikekulun arvo.  

    Voit haluta luoda erityisen nimikekulunumeron koskemaan ostoalennuksia.  
6.  Syötä **Määrä**-kenttään **1**.  
7.  Syötä **Välitön yksikkökustannus** -kenttään ostoalennuksen summa.  
8.  Määritä ostoalennus nimikekuluna kirjatussa vastaanotossa oleville nimikkeille. Lisätietoja on kohdassa [Toimintaohje: Kaupan lisäkustannusten huomiointi nimikekulujen avulla](payables-how-assign-item-charges.md) Kun olet määrittänyt alennuksen, siirry takaisin **Ostohyvityslasku**-ikkunaan.

Kun kirjaat ostopalautustilauksen, ostoalennus lisätään liittyvän ostotapahtuman summaan. Tällä tavoin voit ylläpitää täsmällistä varaston arvostusta.  

## <a name="to-combine-return-shipments"></a>Palautustoimitusten yhdistäminen  
Jos haluat palauttaa eri ostopalautustilauksissa olevia nimikkeitä samalle toimittajalle, voit käyttää **Yhdistä palautustoimitukset** -funktiota.  

Kun toimitat nimikkeitä, kirjaat asianmukaiset ostopalautustilaukset toimitetuiksi eli luot kirjattuja ostopalautustoimituksia.  

Sitten kun olet valmis laskuttamaan nämä nimikkeet, voit luoda ostopalautustilauksen ja kopioida automaattisesti kirjatut ostohyvityslaskun tähän asiakirjaan, sen sijaan että laskuttaisit jokaisen ostopalautustilauksen rivit erikseen. Sen jälkeen voit kirjata ostohyvityslaskun ja laskuttaa kaikki avoimet ostopalautustilaukset kätevästi kerralla.  

Kun palautustilaukset yhdistetään hyvityslaskuun ja kirjataan, laskutetuista riveistä luodaan kirjattu ostohyvityslasku. Alkuperäisen ostopalautustilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän mukaan. Tätä alkuperäistä ostopalautustilausta ei kuitenkaan ole poistettu, vaikka se on kokonaan vastaanotettu ja laskutettu. Sen vuoksi ostopalautustilaus on poistettava manuaalisesti.

> [!NOTE]  
> Oletetaan esimerkiksi, että toimittajalla on useita toimitetuiksi kirjattuja ostopalautustilauksia.     

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostohyvityslaskut** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät.  
4. Valitse **Hae palautustoimitusrivit** -toiminto.  
5.  Valitse useat palautustoimituksen rivit, jotka haluat sisällyttää laskuun:  

    Jos on valittu väärä palautustoimitusrivi tai jos haluat aloittaa alusta, voit poistaa rivit ostohyvityslaskusta ja suorittaa **Hae palautustoimituksen rivit** -toiminnon uudelleen.  
6.  Valitse **Kirjaa**-toiminto.  

### <a name="to-remove-open-purchase-return-orders-after-combined-return-shipment-posting"></a>Poista avoin ostotilaus yhdistetyn palautustoimituksen kirjauksen jälkeen  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Poista laskutetut ostopalautustilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Täytä tarvittavat kentät ja valitse sitten **OK**-painike.  
3.  Voit poistaa yksittäiset ostopalautustilaukset myös manuaalisesti.

## <a name="see-also"></a>Katso myös
[Osto](purchasing-manage-purchasing.md)  
[Toimintaohje: Ostojen kirjaus](purchasing-how-record-purchases.md)  
[Toimintaohje: Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

