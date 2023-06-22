---
title: Myyntipalautustilausten käsittely
description: 'Ohjeaiheessa kerrotaan, miten luodaan myyntipalautustilaus käsittelemään sellaisten nimikkeiden tai palvelujen palautus, peruutus tai hyvitys, joiden maksun olet vastaanottanut.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return, order'
ms.search.form: '44, 134, 144, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/08/2021
ms.author: edupont
---
# <a name="process-sales-return-orders" />Myyntipalautustilausten käsittely

Jos myyntipalautuskäsittelyä, kuten nimikkeen käsittelyn varastoasiakirjoja, on hallittava paremmin tai jos haluat paremman yleiskuvan, kun useiden myyntiasiakirjojen nimikkeitä vastaanotetaan yhtenä myyntipalautuksena, voit luoda myyntipalautustilauksia. Myyntipalautustilaus lähettää automaattisesti liittyvän myyntihyvityslaskun ja tarvittaessa muut palautukseen liittyvät asiakirjat, kuten korvaavan myyntitilauksen.

Alkuperäisen kirjatun myyntilaskun lisäksi voit kohdistaa myyntihyvityslaskun tai myyntipalautustilauksen muihin myyntilaskuihin, kuten toiseen kirjattuun myyntilaskuun, koska asiakas on myös palauttamassa tämän laskun kanssa toimitettuja nimikkeitä.

## <a name="create-a-sales-return-order-based-on-one-or-more-posted-sales-documents" />Myyntipalautustilauksen luominen vähintään yhden kirjatun myyntiasiakirjan perusteella

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntipalautustilaukset** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.  
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät.
4. Täytä **Rivit**-pikavälilehdessä rivit manuaalisesti. Jos kopioit tiedot muista asiakirjoista, rivit täytetään automaattisesti:

    - Voit kopioida vähintään yhden kirjatun asiakirjarivin vähintään yhdestä kirjatusta asiakirjasta **Hae peruutettavat kirjatut asiakirjarivit** -toiminnolla. Tämä toiminto peruuttaa aina todelliset kustannukset kirjatusta asiakirjarivistä. Tätä toimintoa käsitellään seuraavissa vaiheissa.    
    - Voit kopioida aiemmin luodun asiakirjan palautustilaukseen **Kopioi asiakirjasta** -toiminnolla. Käytä tätä toimintoa, kun kopioit koko asiakirjan. Se voi olla kirjattu asiakirja tai asiakirja, jota ei ole vielä kirjattu. Voit peruuttaa tällä toiminnolla todelliset kustannukset vain silloin, kun **Todellisen kust. peruutt. pakollinen** -valintaruutu on valittu **Myyntien ja saamisten asetukset** -sivulla.  

5. Valitse **Käsittele**-toiminto ja valitse sitten **Hae peruutettavat kirjatut asiakirjarivit** -toiminto.
6. Valitse **Kirjatut myyntiasiakirjarivit** -sivun yläosassa **Näytä vain peruutettavat rivit** -valintaruutu, jos haluat nähdä vain palauttamattomia määriä sisältävät rivit. Jos kirjattu myyntilaskun määrä on jo palautettu, et ehkä halua palauttaa uuden myyntipalautusasiakirjan määrää.

    > [!NOTE]  
    >  Tämä kenttä toimii vain kirjattujen toimitusten ja kirjattujen laskutusrivien kohdalla. Se ei toimi kirjattujen palautusten tai kirjattujen hyvityslaskurivien kohdalla.

    Sivun vasemmalla puolella on luettelossa eri asiakirjatyyppejä. Suluissa oleva luku ilmoittaa, kuinka monta asiakirjaa kyseistä asiakirjatyyppiä varten on käytettävissä.

7. Valitse **Asiakirjatyyppisuodatin**-kentässä kirjattujen asiakirjarivien tyyppi, jota haluat käyttää.  
8. Valitse uuteen asiakirjaan kopioitavat rivit.  

    > [!NOTE]  
    >  Jos kaikki rivit valitaan näppäinyhdistelmällä <kbd>Ctrl</kbd>+<kbd>A</kbd>, kaikki määritetyssä suodattimessa olevat rivit kopioidaan mutta **Näytä vain peruutettava määrä** -suodatin ohitetaan. Oletetaan esimerkiksi, että olet suodattanut tietyn asiakirjanumeron rivit kahteen riviin, joista toinen on palautettu. Jos käytät kopioinnissa <kbd>Ctrl</kbd>+<kbd>A</kbd>-näppäimiä, vaikka **Näytä vain peruutettava määrä** -kenttä on valittuna, molemmat rivit kopioidaan eikä vain rivi, jota ei ole vielä peruutettu.  

9. Kopioi rivit uuteen asiakirjaan valitsemalla **OK**.  

    Seuraavat toimenpiteet suoritetaan:  

    -   Tyyppiä **Nimike** oleville kirjatuille asiakirjariveille luodaan uusi asiakirjarivi, joka on kirjatun asiakirjarivin kopio. Sillä on määrä, jota ei ole vielä peruutettu. **Kohdistus nimiketapahtumasta** -kenttä on täytetty soveltuvalla kirjatun asiakirjarivin nimiketapahtuman numerolla.  

    -   Niille kirjatuille asiakirjariveille, joiden tyyppi ei ole **Nimike** (kuten nimikekulut) ohjelma luo uuden asiakirjarivin, joka on alkuperäisen kirjatun asiakirjarivin kopio.  

    -   Laskee uuden rivin **Yksikkökustannus (PVA)** -kentän arvon vastaavan nimiketapahtumien kustannuksista.  

    -   Jos kopioitu asiakirja on kirjattu toimitus, kirjattu vastaanotto, kirjattu palautusvastaanotto tai kirjattu palautustoimitus, ohjelma laskee yksikköhinnan nimikekortista.  

    -   Jos kopioitu asiakirja on kirjattu lasku tai hyvityslasku, ohjelma kopioi kirjatun asiakirjarivin yksikköhinnan, laskualennukset ja rivialennukset.  

    -   Jos kirjattu asiakirjarivi sisältää nimikkeen seurantarivejä, ohjelma täyttää **Kohdistus nimiketapahtumasta** -kenttään kirjattujen nimikkeen seurantarivien soveltuvien nimiketapahtumien numerot.  

     Kun kopioit kirjatusta laskusta tai kirjatusta hyvityslaskusta, sovellus kopioi kaikki asiakirjan kirjaushetkellä kelvolliset laskualennukset ja rivialennuksen kirjatusta asiakirjarivistä uuteen asiakirjariviin. Huomaa kuitenkin, että jos **Lask. laskun alennus** -asetus on määritettynä **Myyntien ja myyntisaamisten asetukset** -sivulla, laskun alennus lasketaan uudelleen, kun kirjaat uuden asiakirjarivin. Uuden rivin rivisumma voikin tämän vuoksi poiketa kirjatun asiakirjarivin rivisummasta laskun alennuksen uuden laskennan tuloksen mukaan.  

     > [!NOTE]  
     >  Jos osa kirjatun asiakirjarivin määrää on jo peruutettu (palautettu), myyty tai kulutettu, ohjelma luo rivin vain varastossa olevalle määrälle tai määrälle, jota ei ole palautettu. Jos kirjatun asiakirjarivin koko määrä on peruutettu (palautettu), ohjelma ei luo uutta asiakirjariviä.  
     >   
     >  Jos kirjatun asiakirjan tavaravirta on sama kuin uuden asiakirjan tavaravirta, ohjelma yksinkertaisesti luo alkuperäisen kirjatun asiakirjarivin kopion uuteen asiakirjaan. **Kohdistus nimiketapahtumasta** -kenttää ei täytetä, koska tässä tapauksessa todellisten kustannusten peruuttaminen ei ole mahdollista. Jos esimerkiksi käytät **Hae peruutettavat kirjatut asiakirjarivit** -toimintoa kirjatun myyntihyvityslaskurivin hakemisessa uuteen myyntihyvityslaskuun, ohjelma kopioi vain alkuperäisen kirjatun hyvityslaskurivin uuteen hyvityslaskuun.  

10. Valitse **Myyntipalautustilaus**-sivun kunkin rivin **Palautuksen syykoodi** -kentässä palautuksen syy.
11. Valitse **Kirjaa**-toiminto.

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order" />Korvaavan myyntitilauksen luominen myyntipalautustilauksesta
Voit hyvittää asiakkaalle myymäsi nimikkeen vaihtamalla nimikkeen. Voit vaihtaa nimikkeen samaan tai eri nimikkeeseen. Tällainen tilanne voi syntyä esimerkiksi silloin, kun olet toimittanut asiakkaalle vahingossa väärän nimikkeen.  

1. Tee korvaavalle nimikkeelle aktiivisen palautuskäsittelyn **Myyntipalautustilaus**-sivun tyhjällä rivillä negatiivinen tapahtuma lisäämällä negatiivinen summa **Määrä**-kenttään.  
2. Valitse **Siirrä negatiiviset rivit** -toiminto.
3. Täytä **Siirrä negat. myyntirivit** -sivulla tarvittavat kentät.
4. Valitse **OK**-painike. Ohjelma poistaa vaihdettavan nimikkeen negatiivisen rivin myyntipalautustilauksesta ja sisällyttää sen uudelle **Myyntitilaus**-sivulle. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).

## <a name="to-create-return-related-documents-from-a-sales-return-order" />Palautuksiin liittyvien asiakirjojen luonti myyntipalautustilauksesta
Voit luoda korvaavia myyntitilauksia, ostopalautustilauksia ja korvaavia ostotilauksia automaattisesti myyntipalautuskäsittelyn aikana. Tämä on kätevää esimerkiksi silloin, kun haluat käsitellä nimikkeitä, joilla on toimittajan myöntämä takuu.

1. Valitse aktiivisen palautuskäsittelyn **Myyntipalautustilaus**-sivulla **Luo palautuksiin liittyvät asiakirjat** -toiminto.
2. Anna **Toimittajan nro** -kentässä toimittajan numero, jos haluat toimittajan asiakirjat automaattisesti.
3. Jos palautettu nimike on palautettava toimittajalle, valitse **Luo ostopalautustilaus** -valintaruutu.
4. Jos palautettu nimike on tilattava toimittajalta, valitse  **Luo ostotilaus** -valintaruutu.
5. Jos korvaava myyntitilaus on luotava, valitse **Luo myyntitilaus** -valintaruutu.

## <a name="to-create-a-restock-charge" />Täydennysmaksun luominen
Voit veloittaa asiakkaaltasi täydennysmaksun kattamaan nimikkeen palauttamisesta aiheutuneet fyysiset käsittelykulut. Täydennysmaksu voidaan veloittaa esimerkiksi, jos asiakas tilasi vahingossa väärän nimikkeen tai muutti mieltänsä sen jälkeen, kun oli vastaanottanut myymäsi nimikkeen.

Voit kirjata tämän kasvaneen kustannuksen nimikekuluna hyvityslaskuun tai palautustilaukseen ja määritellä sen kirjattuun toimitukseen. Seuraavassa se käsitellään myyntipalautustilauksen osalta, mutta samat vaiheet koskevat myös myyntihyvityslaskua.

1. Avaa aktiivisen palautuskäsittelyn **Myyntipalautustilaus**-sivu.
2. Valitse uuden rivin **Tyyppi**-kentässä **Kulu (nimike)**.  
3. Täytä kentät samoin kuin muutkin nimikekulurivit. Lisätietoja on kohdassa [Kaupan lisäkustannusten huomiointi nimikekulujen avulla](payables-how-assign-item-charges.md)  

Kun kirjaat myyntipalautustilauksen, ohjelma lisää täydennysmaksun asianmukaisen myyntitapahtuman summaan. Tällä tavoin voit ylläpitää täsmällistä varaston arvostusta.  

## <a name="see-related-microsoft-trainingtrainingpathsreturn-items-dynamics--business-central" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/return-items-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Ostopalautusten tai peruutusten käsittely](purchasing-how-process-purchase-returns-cancellations.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
