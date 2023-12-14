---
title: Myynnin palautusten tai peruutusten käsittely
description: 'Ohjeaiheessa kerrotaan, miten luodaan myyntihyvityslasku käsittelemään sellaisten nimikkeiden tai palvelujen palautus, peruutus tai hyvitys, joiden maksun olet vastaanottanut.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '44, 134, 143, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/27/2021
ms.author: bholtorf
---
# <a name="process-sales-returns-or-cancellations"></a>Myynnin palautusten tai peruutusten käsittely

Jos asiakas haluaa palauttaa nimikkeitä tai saada hyvitystä nimikkeistä tai palveluista, jotka olet myynyt ja joista olet saanut maksun, sinun on luotava ja kirjattava myyntihyvityslasku, joka määrittää pyydetyn muutoksen. Voit sisällyttää oikeat myyntilaskun tiedot seuraavasti:  

- Luo myyntihyvityslaskun suoraan kirjatusta myyntilaskusta.
- Luo uusi myyntihyvityslasku, jossa on kopioidut laskutiedot.

Jos myyntipalautuskäsittelyä, kuten nimikkeen käsittelyn varastoasiakirjoja, on hallittava paremmin tai jos haluat paremman yleiskuvan, kun useiden myyntiasiakirjojen nimikkeitä vastaanotetaan yhtenä myyntipalautuksena, voit luoda myyntipalautustilauksia. Myyntipalautustilaus lähettää automaattisesti liittyvän myyntihyvityslaskun ja tarvittaessa muut palautukseen liittyvät asiakirjat, kuten korvaavan myyntitilauksen. Lisätietoja on kohdassa [Myyntipalautustilausten käsittely](sales-how-process-sales-returns-orders.md).

> [!NOTE]  
> Jos kirjattua myyntilaskua ei ole vielä maksettu, voit peruuttaa tapahtumat käyttämällä kirjatun myyntilaskun **Korjaa**- tai **Peruuta**-toimintoa. Nämä toiminnot toimivat vain maksamattomille laskuille eivätkä ne osittaisia palautuksia tai peruutuksia. Lisätietoja on kohdassa [Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](sales-how-correct-cancel-sales-invoice.md).

Palautus tai hyvitys voi liittyä vain joihinkin alkuperäisen myyntilaskun nimikkeisiin tai palveluihin. Tällöin myyntihyvityslaskun tai myyntipalautustilauksen riveillä olevia tietoja on muokattava. Myyntihyvityslaskun tai myyntipalautustilauksen kirjaamisen yhteydessä myyntiasiakirjat, joihin muutos vaikuttaa, peruutetaan. Tämän jälkeen asiakkaalle voidaan luoda hyvitysmaksu. Lisätietoja on kohdassa [Maksujen suorittaminen](payables-make-payments.md).  

Hyvityslaskun kirjaaminen palauttaa myös mahdolliset kirjattuun asiakirjaan määritetyt nimikekulut, joten nimikkeen arvotapahtumat ovat samat kuin ennen nimikekulun määrittämistä.

> [!NOTE]
> Myyntipalautusten kirjanpitonäkökohtia, kuten asiakkaille maksettavia maksuja, pidetään kirjanpitona, eikä niitä ole kuvattu tässä. Lisätietoja on kohdassa [Ostovelkojen hallinta](payables-manage-payables.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Myyntihyvityslaskun luominen kirjatusta myyntilaskusta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntilaskut** ja valitse sitten vastaava linkki.  
2. Valitse **Kirjatut myyntilaskut** -sivulla kirjattu myyntilasku, jonka haluat peruuttaa, ja valitse **Peruuta**-toiminto ja sitten **Luo korjaava hyvityslasku** -toiminto.

    Ostohyvityslaskun otsikossa on tietoja kirjatusta myyntilaskusta. Voit muokata sitä esimerkiksi palautussopimusta vastaavilla uusilla tiedoilla.  
3. Muokkaa sopimuksen mukaan rivien tietoja, kuten palautettujen nimikkeiden määrää tai hyvitettävää summaa.
4. Valitse **Valmistele**-toiminto ja valitse sitten **Kohdista tapahtumat** -toiminto.
5. Valitse **Kohdista asiakastapahtumat** -sivulla rivi, joka sisältää myyntihyvityslaskuun kohdistettavan kirjatun myyntiasiakirjan. Valitse sitten **Kohdistetaan tunnisteeseen** -toiminto.

    Myyntihyvityslaskun tunniste näkyy **Kohdistetaan tunnisteeseen** -kentässä.
6. Anna **Kohdistettava summa** -kenttään kohdistettava summa, jos se on pienempi kuin alkuperäinen summa.  

    **Kohdista asiakastapahtumat** -sivun alaosassa näkyy kokonaissumma, joka kohdistetaan kaikkien mukaan kuuluvien tapahtumien peruuttamiseksi, kun **Saldo**-kentän arvo on nolla.
7. Valitse **OK**-painike. Kun myyntihyvityslasku kirjataan, se kohdistetaan kirjattuihin myyntiasiakirjoihin.

    Kun olet luonut tai muokannut ostohyvityslaskun rivejä, ja vähintään yksi sovellusalue on määritetty, voit kirjata myyntihyvityslaskun.  
8. Valitse ensin **Kirjaus**-toiminto ja sitten **Kirjaa ja lähetä**-toiminto.  

**Kirjaa ja lähettää vahvistuksen** -valintaikkuna avautuu, jossa näkyy suositeltu tapa lähettää asiakkaalle. Voit muuttaa lähetysmenetelmän valitsemalla **Lähetä asiakirja kohteeseen** -kentän valintapainikkeen. Lisätietoja on kohdassa [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).  

Kirjatut myyntiasiakirjat, jotka kohdistettiin hyvityslaskuun, on nyt peruutettu, ja asiakkaalle voidaan luoda palautusmaksu. Myyntihyvityslasku poistetaan ja korvataan uudella kirjattujen myyntihyvityslaskujen luettelon asiakirjalla.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Myyntihyvityslaskun luominen kopioimalla kirjattu myyntilasku

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntihyvityslaskut** ja valitse sitten vastaava linkki.
2. Avaa uusi tyhjä myyntihyvityslasku valitsemalla **Uusi**-toiminto.
3. Syötä **Asiakkaan nimi**-kenttään nykyisen asiakkaan nimi.
4. Valitse **Valmistele**-toiminto ja valitse sitten **Kopioi asiakirjat** -toiminto.
5. Valitse **Kopioi myyntiasiakirja** -sivun **Asiakirjan tyyppi** -kentässä **Kirjattu lasku**.
6. Valitse **Asiakirjanro**-kenttä, jos haluat avata **Kirjatut myyntilaskut** -sivun, ja valitse sitten kirjattu myyntilaskutietue, joka sisältää peruutettavat rivit.
7. Valitse **Laske rivit uudelleen** -valintaruutu, jos haluat päivittää kopioidut kirjatut myyntilaskurivit nimikkeen hinta- ja yksikkökustannusten muutoksilla, jotka ovat tapahtuneet laskun kirjaamisen jälkeen.
8. Valitse **OK**-painike. Kopioidut laskurivit lisätään myyntihyvityslaskuun.
9. Täytä myyntihyvityslasku kohdan [Myyntihyvityslaskun luominen kirjatusta myyntilaskusta](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice) mukaisesti.

## <a name="to-create-a-sales-allowance"></a>Myyntialennuksen luominen
Joskus asiakkaalle täytyy lähettää hyvityslasku, jossa on hinnanalennus, jos asiakas on esimerkiksi vastaanottanut nimikkeet hieman vahingoittuneina tai saanut ne myöhässä.  
Voit kirjata tämän alennushinnan nimikekuluna hyvityslaskuun tai palautustilaukseen ja määritellä sen kirjattuun toimitukseen. Seuraavassa se käsitellään myyntihyvityslaskun osalta, mutta samat vaiheet koskevat myös myyntipalautustilausta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntihyvityslaskut** ja valitse sitten vastaava linkki.
2. Avaa uusi tyhjä myyntihyvityslasku valitsemalla **Uusi**-toiminto.
3. Täytä hyvityslaskun otsikko asianmukaisilla tiedoilla asiakkaasta, jolle haluat antaa myyntialennuksen.  
4. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä **Kulu (nimike)**.  
5. Valitse **Nro**-kenttään sopiva nimikekulun arvo.  
     Voit haluta luoda erityisen nimikekulunumeron myyntialennuksille.  
6. Syötä **Määrä**-kenttään **1**.  
7. Syötä **Yksikköhinta Ilman ALV** -kenttään myyntialennuksen summa.  
8. Määritä myyntialennus nimikekuluksi kirjatun toimituksen nimikkeille. Lisätietoja on kohdassa [Kaupan lisäkustannusten huomiointi nimikekulujen avulla](payables-how-assign-item-charges.md) Kun olet määrittänyt alennuksen, siirry takaisin **Hyvityslasku**-sivulle.  

Kun kirjaat myyntipalautustilauksen, ohjelma lisää myyntialennuksen asianmukaisen myyntitapahtuman summaan. Tällä tavoin voit ylläpitää täsmällistä varaston arvostusta.

## <a name="to-combine-return-receipts"></a>Palautusvastaanottojen yhdistäminen
Tämä toiminto on hyödyllinen, jos asiakkaasi palauttaa useita nimikkeitä, jotka korvataan eri myyntipalautustilauksilla.  

Kun vastaanotat nimikkeet varastollesi, kirjaa asianmukaiset myyntipalautustilaukset vastaanotetuiksi. Tällä tavoin luodaan kirjatut palautusvastaanotot.  

Sitten kun olet valmis laskuttamaan asiakasta, voit luoda myyntihyvityslaskun ja kopioida automaattisesti kirjatut palautusvastaanottorivit tähän asiakirjaan, sen sijaan että laskuttaisit jokaisen myyntipalautustilauksen erikseen. Sen jälkeen voit kirjata myyntihyvityslaskun ja laskuttaa kaikki avoimet myyntipalautustilaukset kätevästi kerralla.  

**Asiakaskortti**-sivun **Tee koontilasku** -valintaruutu on valittava, jotta palautusvastaanottoja voidaan yhdistää.  

### <a name="to-manually-combine-return-receipts"></a>Palautusvastaanottojen yhdistäminen manuaalisesti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntihyvityslaskut** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät.  
4. Valitse **Hae pal. vastaanottorivit** -toiminto.  
5. Valitse ne palautusvastaanottorivit, jotka haluat sisällyttää hyvityslaskuun:  

    - Voit lisätä kaikki rivit valitsemalla ensin kaikki rivit ja sitten **OK**.  

    - Voit lisätä tietyt rivit valitsemalla ensin rivit ja sitten **OK**.  
6.  Jos valitsit virheellisen rivin tai haluat aloittaa alusta, voit yksinkertaisesti poistaa hyvityslaskun rivit ja ajaa **Hae palautusvast.oton rivit** -toiminnon uudelleen.  
7.  Kirjaa lasku.  

### <a name="to-automatically-combine-return-receipts"></a>Palautusvastaanottojen yhdistäminen automaattisesti

Voit yhdistää palautusvastaanotot automaattisesti. Voit myös kirjata hyvityslaskut automaattisesti  **Yhdistä palautusvastaanotot** -toiminnolla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yhdistä palautusvastaanotot** ja valitse sitten vastaava linkki.
2. Valitse soveltuvat palautusvastaanotot täyttämällä kentät **Yhdistä palautusvastaanotot** -sivulla.
3. Valitse **Kirjaa hyvityslaskut** -valintaruutu. Muussa tapauksessa saatavat ostohyvityslaskut on kirjattava manuaalisesti.
4. Valitse **OK**-painike.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a>Vastaanotettujen ja laskutettujen palautustilausten poistaminen

Kun laskutat palautusvastaanotot näin, säilyvät palautustilaukset, joista palautusvastaanotot kirjattiin, vaikka ne olisi vastaanotettu ja laskutettu täysin.  

Kun palautusvastaanotot yhdistetään hyvityslaskuun ja kirjataan, hyvitetyille riveille luodaan kirjattu myyntihyvityslasku. Alkuperäisen myyntipalautustilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän perusteella.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poista laskutetut myyntipalautustilaukset** ja valitse sitten vastaava linkki.  
2. Määritä **Numero** -kenttään , mitkä palautustilaukset poistetaan.  
3. Valitse **OK**-painike.  

Voit myös poistaa manuaalisesti yksittäiset myyntipalautustilaukset.  

## <a name="inventory-costing"></a>Varaston arvostus

Oikean varaston arvostuksen säilyttämistä varten palautetut nimikkeet viedään yleensä takaisin varastoon sillä yksikkökustannuksella, jolla ne myyntiin, eikä nykyisellä yksikkökustannuksella. Tätä kutsutaan todellisten kustannusten peruuttamiseksi.

Todellisten kustannusten peruuttamisen automaattista määrittämistä varten on kaksi toimintoa:  

|Toiminto|Kuvaus|  
|------------------|---------------------------------------|  
|**Myyntipalautustilaus**-sivun **Hae peruutettavat kirjatut asiakirjarivit** -toiminto|Kopioi vähintään yhden myyntipalautustilaukseksi käännettävän kirjatun asiakirjan rivit. Lisätietoja on kohdassa [Myyntipalautustilauksen luominen vähintään yhden kirjatun myyntiasiakirjan perusteella](sales-how-process-sales-returns-orders.md#create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|**Myyntihyvityslasku**- ja **Myyntipalautustilaus**-sivujen **Kopioi asiakirja** -toiminto|Kopioi sekä otsikon että yhden kirjatun asiakirjan rivit peruutusta varten.<br /><br /> Edellyttää, että **Todellisen kust. peruutt. pakollinen** -valintaruutu on valittuna **Myyntien ja myyntisaamisten asetukset** -sivulla.|

Jos haluat määrittää todellisten kustannusten peruuttamisen manuaalisesti, sinun on valittava **Kohdistus nimiketapahtumasta** -kenttä joltakin palautusasiakirjariviltä ja valittava sitten alkuperäisen myyntitapahtuman numero. Tämä linkittää myyntihyvityslaskun tai myyntipalautustilauksen alkuperäiseen myyntitapahtumaan ja varmistaa, että nimike arvostetaan alkuperäisissä yksikkökustannuksissa.

Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Varaston arvostus](design-details-inventory-costing.md).

## <a name="see-also"></a>Katso myös

[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Ostopalautusten tai peruutusten käsittely](purchasing-how-process-purchase-returns-cancellations.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
