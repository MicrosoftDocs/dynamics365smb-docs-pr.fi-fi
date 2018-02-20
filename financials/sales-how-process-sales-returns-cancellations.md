---
title: "Myynnin palautusten tai peruutusten käsittely myyntihyvityslaskujen avulla | Microsoft Docs"
description: "Ohjeaiheessa kerrotaan, miten luodaan myyntihyvityslasku joko suoraan tai myyntipalautustilauken kautta käsittelemään sellaisten nimikkeiden tai palvelujen palautus, peruutus tai hyvitys, joiden maksun olet vastaanottanut."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 09/08/2016
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: eac8f4fdd6a5333662e272c8c71e585cf1fb876a
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="process-sales-returns-or-cancellations"></a>Myynnin palautusten tai peruutusten käsittely
Jos asiakas haluaa palauttaa nimikkeitä tai saada hyvitystä nimikkeistä tai palveluista, jotka olet myynyt ja joista olet saanut maksun, sinun on luotava ja kirjattava myyntihyvityslasku, joka määrittää pyydetyn muutoksen. Voit sisällyttää oikeat myyntilaskun tiedot luomalla myyntihyvityslaskun suoraan kirjatusta myyntilaskusta. Vaihtoehtoiesti voi luoda uuden myyntihyvityslaskun, johon laskun tiedot on kopioitu.

Jos myyntipalautuskäsittelyä, kuten nimikkeen käsittelyn varastoasiakirjoja, on hallittava paremmin tai jos haluat paremman yleiskuvan, kun useiden myyntiasiakirjojen nimikkeitä vastaanotetaan yhtenä myyntipalautuksena, voit luoda myyntipalautustilauksia. Myyntipalautustilaus lähettää automaattisesti liittyvän myyntihyvityslaskun ja tarvittaessa muut palautukseen liittyvät asiakirjat, kuten korvaavan myyntitilauksen. Lisätietoja on kohdassa Myyntipalautustilauksen luominen vähintään yhden kirjatun myyntiasiakirjan perusteella.

> [!NOTE]  
>   Jos kirjattua myyntilaskua ei ole vielä maksettu, voit peruuttaa tapahtumat käyttämällä kirjatun myyntilaskun **Korjaa**- tai **Peruuta**-toimintoa. Nämä toiminnot toimivat vain maksamattomille laskuille, eivätkä ne tue osittaisia palautuksia tai peruutuksia. Lisätietoja on kohdassa [Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](sales-how-correct-cancel-sales-invoice.md).

Palautus tai hyvitys voi liittyä vain joihinkin alkuperäisen myyntilaskun nimikkeisiin tai palveluihin. Tällöin myyntihyvityslaskun tai myyntipalautustilauksen riveillä olevia tietoja on muokattava. Myyntihyvityslaskun tai myyntipalautustilauksen kirjaamisen yhteydessä myyntiasiakirjat, joihin muutos vaikuttaa, peruutetaan. Tämän jälkeen asiakkaalle voidaan luoda hyvitysmaksu. Lisätietoja on kohdassa [Maksujen suorittaminen](payables-make-payments.md).  

Alkuperäisen kirjatun myyntilaskun lisäksi voit kohdistaa myyntihyvityslaskun tai myyntipalautustilauksen muihin myyntilaskuihin, kuten toiseen kirjattuun myyntilaskuun, koska asiakas on myös palauttamassa tämän laskun kanssa toimitettuja nimikkeitä.

Voit lähettää kirjatun myyntihyvityslaskun asiakkaalle ja vahvistaa palautuksen tai peruutuksen ja kertoa, että liittyvä arvo korvataan, esimerkiksi silloin, kun nimikkeet palautetaan.

Hyvityslaskun kirjaaminen palauttaa myös mahdolliset kirjattuun asiakirjaan määritetyt nimikekulut, joten nimikkeen arvotapahtumat ovat samat kuin ennen nimikekulun määrittämistä.

## <a name="inventory-costing"></a>Varaston arvostus
Oikean varaston arvostuksen säilyttämistä varten palautetut nimikkeet viedään yleensä takaisin varastoon sillä yksikkökustannuksella, jolla ne myyntiin, eikä nykyisellä yksikkökustannuksella. Tätä kutsutaan todellisten kustannusten peruuttamiseksi.

Todellisten kustannusten peruuttamisen automaattista määrittämistä varten on kaksi toimintoa.   

|Toiminto|Kuvaus|  
|------------------|---------------------------------------|  
|**Myyntipalautustilaus**-ikkunan **Hae peruutettavat kirjatut asiakirjarivit** -toiminto|Kopioi vähintään yhden myyntipalautustilaukseksi käännettävän kirjatun asiakirjan rivit. Lisätietoja on kohdassa Myyntipalautustilauksen ja liittyvän myyntihyvityslaskun luominen vähintään yhdelle kirjatulle myyntilaskulle.|  
|**Myyntihyvityslasku**- ja **Myyntipalautustilaus**-ikkunoiden **Kopioi asiakirja** -toiminto|Kopioi sekä otsikon että yhden kirjatun asiakirjan rivit peruutusta varten.<br /><br /> Edellyttää, että **Todellisen kust. peruutt. pakollinen** -valintaruutu on valittuna **Myyntien ja myyntisaamisten asetukset** -ikkunassa.|

Jos haluat määrittää todellisten kustannusten peruuttamisen manuaalisesti, sinun on valittava **Kohdistus nimiketapahtumasta** -kenttä joltakin palautusasiakirjariviltä ja valittava sitten alkuperäisen myyntitapahtuman numero. Tämä linkittää myyntihyvityslaskun tai myyntipalautustilauksen alkuperäiseen myyntitapahtumaan ja varmistaa, että nimike arvostetaan alkuperäisissä yksikkökustannuksissa.

Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Varaston arvostus](design-details-inventory-costing.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Myyntihyvityslaskun luominen kirjatusta myyntilaskusta
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kirjatut myyntilaskut** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Kirjatut myyntilaskut** -ikkunassa kirjattu myyntilasku, jonka haluat peruuttaa, ja valitse sitten **Luo korjaava hyvityslasku** -toiminto.

    Ostohyvityslaskun otsikossa on tietoja kirjatusta myyntilaskusta. Voit muokata sitä esimerkiksi palautussopimusta vastaavilla uusilla tiedoilla.  
3. Muokkaa sopimuksen mukaan rivien tietoja, kuten palautettujen nimikkeiden määrää tai hyvitettävää summaa.
4. Valitse **Kohdista tapahtumat** -toiminto.
5. Valitse **Kohdista asiakastapahtumat** -ikkunassa rivi, joka sisältää myyntihyvityslaskuun kohdistettavan kirjatun myyntiasiakirjan. Valitse sitten **Kohdistetaan tunnisteeseen** -toiminto.

    Myyntihyvityslaskun tunniste näkyy **Kohdistetaan tunnisteeseen** -kentässä.
6. Anna **Kohdistettava summa** -kenttään kohdistettava summa, jos se on pienempi kuin alkuperäinen summa.  

    **Kohdista asiakastapahtumat** -ikkunan alaosassa näkyy kokonaissumma, joka kohdistetaan kaikkien mukaan kuuluvien tapahtumien peruuttamiseksi, kun **Saldo**-kentän arvo on nolla.
7. Valitse **OK**-painike. Kun myyntihyvityslasku kirjataan, se kohdistetaan kirjattuihin myyntiasiakirjoihin.

    Kun olet luonut tai muokannut ostohyvityslaskun rivejä, ja vähintään yksi sovellusalue on määritetty, voit kirjata myyntihyvityslaskun.   
8. Valitse **Kirjaa ja lähetä** -toiminto.  

**Kirjaa ja lähettää vahvistuksen** -valintaikkuna avautuu, jossa näkyy suositeltu tapa lähettää asiakkaalle. Voit muuttaa lähetysmenetelmän valitsemalla **Lähetä asiakirja kohteeseen** -kentän valintapainikkeen. Lisätietoja on kohdassa [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).  

Kirjatut myyntiasiakirjat, jotka kohdistettiin hyvityslaskuun, on nyt peruutettu, ja asiakkaalle voidaan luoda palautusmaksu. Myyntihyvityslasku poistetaan ja korvataan uudella kirjattujen myyntihyvityslaskujen luettelon asiakirjalla.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Myyntihyvityslaskun luominen kopioimalla kirjattu myyntilasku
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntihyvityslaskut** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa uusi tyhjä myyntihyvityslasku valitsemalla **Uusi**-toiminto.
3. Syötä **Asiakas**-kenttään nykyisen asiakkaan nimi.
4. Valitse **Kopioi asiakirja** -toiminto.
5. Valitse **Kopioi myyntiasiakirja** -ikkunan **Asiakirjan tyyppi** -kentässä **Kirjattu lasku**.
6. Valitse **Asiakirjanro**-kenttä, jos haluat avata **Kirjatut myyntilaskut** -ikkunan, ja valitse sitten kirjattu myyntilasku, joka sisältää peruutettavat rivit.
7. Valitse **Laske rivit uudelleen** -valintaruutu, jos haluat päivittää kopioidut kirjatut myyntilaskurivit nimikkeen hinta- ja yksikkökustannusten muutoksilla, jotka ovat tapahtuneet laskun kirjaamisen jälkeen.
8. Valitse **OK**-painike. Kopioidut laskurivit lisätään myyntihyvityslaskuun.
9. Täytä myyntihyvityslasku tämän ohjeaiheen "Myyntihyvityslaskun luominen kirjatusta myyntilaskusta" -osassa esitetyllä tavalla.

## <a name="to-create-a-sales-return-order-based-on-one-or-more-a-posted-sales-documents"></a>Myyntipalautustilauksen luominen vähintään yhden kirjatun myyntiasiakirjan perusteella
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntipalautustilaukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Uusi**-toiminto.  
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät.
4. Täytä **Rivit**-pikavälilehdessä rivit manuaalisesti. Jos kopioit tiedot muista asiakirjoista, rivit täytetään automaattisesti:

    - Voit kopioida vähintään yhden kirjatun asiakirjarivin vähintään yhdestä kirjatusta asiakirjasta **Hae peruutettavat kirjatut asiakirjarivit** -toiminnolla. Tämä toiminto peruuttaa aina todelliset kustannukset kirjatusta asiakirjarivistä. Tätä toimintoa käsitellään seuraavissa vaiheissa.    
    - Voit kopioida aiemmin luodun asiakirjan palautustilaukseen **Kopioi asiakirja** -toiminnolla. Käytä tätä toimintoa, kun kopioit koko asiakirjan. Se voi olla kirjattu asiakirja tai asiakirja, jota ei ole vielä kirjattu. Voit peruuttaa tällä toiminnolla todelliset kustannukset vain silloin, kun **Todellisen kust. peruutt. pakollinen** -valintaruutu on valittu**Myyntien ja saamisten asetukset** -ikkunassa.  

5. Valitse **Hae peruutettavat kirjatut asiakirjarivit** -toiminto.
6. Valitse **Kirjatut myyntiasiakirjarivit** -ikkunan yläosassa **Näytä vain peruutettavat rivit** -valintaruutu, jos haluat nähdä vain palauttamattomia määriä sisältävät rivit. Jos kirjattu myyntilaskun määrä on jo palautettu, et ehkä halua palauttaa uuden myyntipalautusasiakirjan määrää.

    > [!NOTE]  
    >  Tämä kenttä toimii vain kirjattujen toimitusten ja kirjattujen laskutusrivien kohdalla. Se ei toimi kirjattujen palautusten tai kirjattujen hyvityslaskurivien kohdalla.

    Ikkunan vasemmalla puolella on luettelossa eri asiakirjatyyppejä. Suluissa oleva luku ilmoittaa, kuinka monta asiakirjaa kyseistä asiakirjatyyppiä varten on käytettävissä.

7. Valitse **Asiakirjatyyppisuodatin**-kentässä kirjattujen asiakirjarivien tyyppi, jota haluat käyttää.  
8. Valitse uuteen asiakirjaan kopioitavat rivit.  

    > [!NOTE]  
    >  Jos käytät rivien kopioinnissa Ctrl+A -näppäimiä, ohjelma kopioi kaikki rivit määrittämäsi suodattimen mukaan. Ohjelma ei kuitenkaan huomioi **Näytä vain peruutettava määrä** -suodatinta. Oletetaan esimerkiksi, että olet suodattanut tietyn asiakirjanumeron rivit kahteen riviin, joista toinen on palautettu. Jos käytät kopioinnissa Ctrl+A-näppäimiä, kun **Näytä vain peruutettava määrä** -kenttä on valittuna, pelkän varaamattoman rivin sijaan kopioidaan molemmat rivit.  

9. Kopioi rivit uuteen asiakirjaan valitsemalla **OK**.  

    Seuraavat toimenpiteet suoritetaan:  

    -   Tyyppiä **Nimike** oleville kirjatuille asiakirjariveille luodaan uusi asiakirjarivi, joka on kirjatun asiakirjarivin kopio. Sillä on määrä, jota ei ole vielä peruutettu. **Kohdistus nimiketapahtumasta** -kenttä on täytetty soveltuvalla kirjatun asiakirjarivin nimiketapahtuman numerolla.  

    -   Niille kirjatuille asiakirjariveille, joiden tyyppi ei ole **Nimike** (kuten nimikekulut) ohjelma luo uuden asiakirjarivin, joka on alkuperäisen kirjatun asiakirjarivin kopio.  

    -   Laskee uuden rivin **Yksikkökustannus (PVA)** -kentän arvon vastaavan nimiketapahtumien kustannuksista.  

    -   Jos kopioitu asiakirja on kirjattu toimitus, kirjattu vastaanotto, kirjattu palautusvastaanotto tai kirjattu palautustoimitus, ohjelma laskee yksikköhinnan nimikekortista.  

    -   Jos kopioitu asiakirja on kirjattu lasku tai hyvityslasku, ohjelma kopioi kirjatun asiakirjarivin yksikköhinnan, laskualennukset ja rivialennukset.  

    -   Jos kirjattu asiakirjarivi sisältää nimikkeen seurantarivejä, ohjelma täyttää **Kohdistus nimiketapahtumasta** -kenttään kirjattujen nimikkeen seurantarivien soveltuvien nimiketapahtumien numerot.  

     Kun kopioit kirjatusta laskusta tai kirjatusta hyvityslaskusta, ohjelma kopioi kaikki asiakirjan kirjaushetkellä kelvolliset laskualennukset ja rivialennuksen kirjatusta asiakirjarivistä uuteen asiakirjariviin. Huomaa kuitenkin, että jos **Lask. laskun alennus** -asetus on määritettynä **Myyntien ja myyntisaamisten asetukset** -ikkunassa, laskun alennus lasketaan uudelleen, kun kirjaat uuden asiakirjarivin. Uuden rivin rivisumma voikin tämän vuoksi poiketa kirjatun asiakirjarivin rivisummasta laskun alennuksen uuden laskennan tuloksen mukaan.  

     > [!NOTE]  
     >  Jos osa kirjatun asiakirjarivin määrää on jo peruutettu (palautettu), myyty tai kulutettu, ohjelma luo rivin vain varastossa olevalle määrälle tai määrälle, jota ei ole palautettu. Jos kirjatun asiakirjarivin koko määrä on peruutettu (palautettu), ohjelma ei luo uutta asiakirjariviä.  
     >   
     >  Jos kirjatun asiakirjan tavaravirta on sama kuin uuden asiakirjan tavaravirta, ohjelma yksinkertaisesti luo alkuperäisen kirjatun asiakirjarivin kopion uuteen asiakirjaan. **Kohdistus nimiketapahtumasta** -kenttää ei täytetä, koska tässä tapauksessa todellisten kustannusten peruuttaminen ei ole mahdollista. Jos esimerkiksi käytät **Hae peruutettavat kirjatut asiakirjarivit** -toimintoa kirjatun myyntihyvityslaskurivin hakemisessa uuteen myyntihyvityslaskuun, ohjelma kopioi vain alkuperäisen kirjatun hyvityslaskurivin uuteen hyvityslaskuun.  

10. Valitse **Myyntipalautustilaus**-ikkunan kunkin rivin **Palautuksen syykoodi** -kentässä palautuksen syy.
11. Valitse **Kirjaa**-toiminto.

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a>Korvaavan myyntitilauksen luominen myyntipalautustilauksesta
Voit hyvittää asiakkaalle myymäsi nimikkeen vaihtamalla nimikkeen. Voit vaihtaa nimikkeen samaan tai eri nimikkeeseen. Tällainen tilanne voi syntyä esimerkiksi silloin, kun olet toimittanut asiakkaalle vahingossa väärän nimikkeen.  

1. Tee korvaavalle nimikkeelle aktiivisen palautuskäsittelyn **Myyntipalautustilaus**-ikkunan tyhjällä rivillä negatiivinen tapahtuma lisäämällä negatiivinen summa **Määrä**-kenttään.  
2. Valitse **Siirrä negatiiviset rivit** -toiminto.
3. Täytä **Siirrä negat. myyntirivit**-ikkunassa tarvittavat kentät.
4. Valitse **OK**-painike. Ohjelma poistaa vaihdettavan nimikkeen negatiivisen rivin myyntipalautustilauksesta ja sisällyttää sen uuteen **Myyntitilaus**-ikkunaan. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).

## <a name="to-create-return-related-documents-from-a-sales-return-order"></a>Palautuksiin liittyvien asiakirjojen luonti myyntipalautustilauksesta
Voit luoda korvaavia myyntitilauksia, ostopalautustilauksia ja korvaavia ostotilauksia automaattisesti myyntipalautuskäsittelyn aikana. Tämä on kätevää esimerkiksi silloin, kun haluat käsitellä nimikkeitä, joilla on toimittajan myöntämä takuu.

1. Valitse aktiivisen palautuskäsittelun **Myyntipalautustilaus**-ikkunassa **Luo palautuksiin liittyvät asiakirjat** -toiminto.
2. Anna **Toimittajan nro** -kentässä toimittajan numero, jos haluat toimittajan asiakirjat automaattisesti.
3. Jos palautettu nimike on palautettava toimittajalle, valitse **Luo ostopalautustilaus** -valintaruutu.
4. Jos palautettu nimike on tilattava toimittajalta, valitse  **Luo ostotilaus** -valintaruutu.
5. Jos korvaava myyntitilaus on luotava, valitse **Luo myyntitilaus** -valintaruutu.

## <a name="to-create-a-restock-charge"></a>Täydennysmaksun luominen
Voit veloittaa asiakkaaltasi täydennysmaksun kattamaan nimikkeen palauttamisesta aiheutuneet fyysiset käsittelykulut. Täydennysmaksu voidaan veloittaa esimerkiksi, jos asiakas tilasi vahingossa väärän nimikkeen tai muutti mieltänsä sen jälkeen, kun oli vastaanottanut myymäsi nimikkeen.

Voit kirjata tämän kasvaneen kustannuksen nimikekuluna hyvityslaskuun tai palautustilaukseen ja määritellä sen kirjattuun toimitukseen. Seuraavassa se käsitellään myyntipalautustilauksen osalta, mutta samat vaiheet koskevat myös myyntihyvityslaskua.

1. Avaa aktiivisen palautuskäsittelyn **Myyntipalautustilaus**-ikkuna.
2. Valitse uuden rivin **Tyyppi**-kentässä **Kulu (nimike)**.  
3. Täytä kentät samoin kuin muutkin nimikekulurivit. Lisätietoja on kohdassa [Kaupan lisäkustannusten huomiointi nimikekulujen avulla](payables-how-assign-item-charges.md)  

Kun kirjaat myyntipalautustilauksen, ohjelma lisää täydennysmaksun asianmukaisen myyntitapahtuman summaan. Tällä tavoin voit ylläpitää täsmällistä varaston arvostusta.  

## <a name="to-create-a-sales-allowance"></a>Myyntialennuksen luominen
Joskus asiakkaalle täytyy lähettää hyvityslasku, jossa on hinnanalennus, jos asiakas on esimerkiksi vastaanottanut nimikkeet hieman vahingoittuneina tai saanut ne myöhässä.  
Voit kirjata tämän alennushinnan nimikekuluna hyvityslaskuun tai palautustilaukseen ja määritellä sen kirjattuun toimitukseen. Seuraavassa se käsitellään myyntihyvityslaskun osalta, mutta samat vaiheet koskevat myös myyntipalautustilausta.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntihyvityslaskut** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa uusi tyhjä myyntihyvityslasku valitsemalla **Uusi**-toiminto.
3. Täytä hyvityslaskun otsikko asianmukaisilla tiedoilla asiakkaasta, jolle haluat antaa myyntialennuksen.  
4. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä **Kulu (nimike)**.  
5.  Valitse **Nro**-kenttään sopiva nimikekulun arvo.  
     Voit haluta luoda erityisen nimikekulunumeron myyntialennuksille.  
6.  Syötä **Määrä**-kenttään **1**.  
7.  Syötä **Yksikköhinta**-kenttään myyntialennuksen summa.  
8.  Määritä myyntialennus nimikekuluksi kirjatun toimituksen nimikkeille. Lisätietoja on kohdassa [Kaupan lisäkustannusten huomiointi nimikekulujen avulla](payables-how-assign-item-charges.md) Kun olet määrittänyt alennuksen, siirry takaisin **Myyntihyvityslasku**-ikkunaan.  

Kun kirjaat myyntipalautustilauksen, ohjelma lisää myyntialennuksen asianmukaisen myyntitapahtuman summaan. Tällä tavoin voit ylläpitää täsmällistä varaston arvostusta.

## <a name="to-combine-return-receipts"></a>Palautusvastaanottojen yhdistäminen
Tämä toiminto on hyödyllinen, jos asiakkaasi palauttaa useita nimikkeitä, jotka korvataan eri myyntipalautustilauksilla.  

Kun vastaanotat nimikkeet varastollesi, kirjaa asianmukaiset myyntipalautustilaukset vastaanotetuiksi. Tällä tavoin luodaan kirjatut palautusvastaanotot.  

Sitten kun olet valmis laskuttamaan asiakasta, voit luoda myyntihyvityslaskun ja kopioida automaattisesti kirjatut palautusvastaanottorivit tähän asiakirjaan, sen sijaan että laskuttaisit jokaisen myyntipalautustilauksen erikseen. Sen jälkeen voit kirjata myyntihyvityslaskun ja laskuttaa kaikki avoimet myyntipalautustilaukset kätevästi kerralla.  

**Asiakaskortti**-ikkunan **Tee koontilasku** -valintaruutu on valittava, jotta palautusvastaanottoja voidaan yhdistää.  

### <a name="to-manually-combine-return-receipts"></a>Palautusvastaanottojen yhdistäminen manuaalisesti  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntihyvityslasku** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Uusi**-toiminto.
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät.  
4. Valitse **Hae pal. vastaanottorivit** -toiminto.  
5. Valitse ne palautusvastaanottorivit, jotka haluat sisällyttää hyvityslaskuun:  

    -   Voit lisätä kaikki rivit valitsemalla ensin kaikki rivit ja sitten **OK**.  

    -   Voit lisätä tietyt rivit valitsemalla ensin rivit ja sitten **OK**.  

6.  Jos valitsit virheellisen rivin tai haluat aloittaa alusta, voit yksinkertaisesti poistaa hyvityslaskun rivit ja ajaa **Hae palautusvast.oton rivit** -toiminnon uudelleen.  
7.  Kirjaa lasku.  

### <a name="to-automatically-combine-return-receipts"></a>Palautusvastaanottojen yhdistäminen automaattisesti  
Voit yhdistää palautusvastaanotot automaattisesti. Voit myös kirjata hyvityslaskut automaattisesti  **Yhdistä palautusvastaanotot** -toiminnolla.  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Yhdistä palautusvastaanotot** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse soveltuvat palautusvastaanotot täyttämällä kentät **Yhdistä palautusvastaanotot** -ikkunassa.
3. Valitse **Kirjaa hyvityslaskut** -valintaruutu. Muussa tapauksessa saatavat ostohyvityslaskut on kirjattava manuaalisesti.
4.  Valitse **OK**-painike.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a>Vastaanotettujen ja laskutettujen palautustilausten poistaminen  
Kun laskutat palautusvastaanotot näin, säilyvät palautustilaukset, joista palautusvastaanotot kirjattiin, vaikka ne olisi vastaanotettu ja laskutettu täysin.  

Kun palautusvastaanotot yhdistetään hyvityslaskuun ja kirjataan, hyvitetyille riveille luodaan kirjattu myyntihyvityslasku. Alkuperäisen myyntipalautustilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän perusteella.   
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Poista laskutetut myyntipalautustilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Määritä **Numero** -kenttään , mitkä palautustilaukset poistetaan.  
3.  Valitse **OK**-painike.  

Voit myös poistaa manuaalisesti yksittäiset myyntipalautustilaukset.   

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

