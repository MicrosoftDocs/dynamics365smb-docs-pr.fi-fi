---
title: Ennakkomaksulaskujen luominen
description: 'Toiminta tilanteissa, joissa edellytät itse ennakkomaksua tai toimittajasi edellyttää sitä. Käytä kullekin myynti- tai ostoriville oletusprosenttiosuuksia tai muuta laskun summia tarpeen mukaan.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: how-to
ms.date: 10/04/2023
ms.custom: bap-template
ms.search.form: '42, 50, 9305, 9307'
---
# <a name="create-prepayment-invoices"></a>Ennakkomaksulaskujen luominen

Jos asiakkaiden on lähetettävä maksu, ennen kuin lähetät tilauksen heille, voit käyttää ennakkomaksuominaisuuksia. Näin voi toimia myös silloin, jos toimittaja edellyttää, että maksat ennen tilauksen toimittamista.  

Voit aloittaa ennakkomaksuprosessin, kun olet luonut ostotilauksen. Oletusarvoinen ennakkomaksuprosentti tilauksen nimikkeelle taikka asiakkaalle tai myyjälle sisällytetään ennakkomaksun laskuun. Voit määrittää ennakkomaksuprosentin myös koko asiakirjalle.

Kun olet luonut myynti- tai ostotilauksen, voit luoda sille ennakkomaksun laskun. Käytä joko kullekin myynti- tai ostoriville oletusprosenttiosuuksia tai muuta laskun summia. Voit määrittää esimerkiksi koko tilauksen yhteissumman.  

Seuraavaksi käsitellään myyntitilauksen ennakkomaksun laskuttamista. Ostotilausten vaiheet ovat vastaavanlaiset.  

## <a name="to-create-a-prepayment-invoice"></a>Ennakkomaksulaskun luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Luo uusi myyntitilaus asianomaiselle asiakkaalle. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).  

    **Ennakkomaksu**-pikavälilehden **Ennakkomaksuprosentti**-kenttä määrittää prosentin, jolla ennakkomaksun summa lasketaan. Jos asiakaskortissa on oletusarvoinen ennakkomaksuprosentti, kenttä täytetään automaattisesti. Prosenttia voi muuttaa. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Valitse **Tiivistä ennakkomaksu** -kenttä, jos haluat luoda ennakkomaksulaskuun rivejä, jotka yhdistää myyntitilauksen rivejä seuraavissa tilanteissa:  

    - Riveillä on sama KP-tili ennakkomaksuja varten (yleisten kirjausasetusten mukaisesti).  
    - Riveillä on samat dimensiot.  

    Jos haluat määrittää ennakkomaksulaskun, jossa on yksi rivi kutakin ennakkomaksuprosentin sisältävää myyntitilausriviä varten. älä valitse **Tiivistä ennakkomaksu** -kenttää.  

    Ennakkomaksun eräpäivä lasketaan automaattisesti **Ennakkomaksun maksuehtojen koodi** -arvon perusteella.

    > [!NOTE]
    > Jos jotkin laskun rivit edellyttävät 100 %:n ennakkomaksun ja toiset eivät, minkä lisäksi ennakkomaksutilillä on ALV, pyöristetty summa voi aiheuttaa virheen, kun ennakkomaksulasku luodaan. Virheen syynä on se, että ennakkomaksun summa on suurempi kuin asiakirjarivien summat. Ongelma korjataan muuttamalla summat niillä riveillä, jotka edellyttävät 100 %:n ennakkomaksua. Muutos laskee ALV-summan pyöristyksen uudelleen ja käyttää kumulatiivista pyöristyseroa viimeksi muokatulla rivillä.
    >
    > Ongelman voi lisäksi korjata kahdella seuraavalla tavalla:
    >
    > * Luomalla erillinen tuotteen ALV-kirjausryhmä ja ALV-kirjausryhmä, jossa on erillinen ALV-tunnus sekä käyttämällä sitä nimikkeissä tai riveillä, joilla on käytettävä 100 %:n ennakkomaksua. Kukin ALV-tunnus pyöristetään, jos erillinen pyöristys tehdään nimikkeille, jotka on määritetty tuotteen ALV-kirjausryhmään.
    > * Käyttämällä erillistä laskua nimikkeille tai riveille, jotka edellyttävät 100 %:n ennakkomaksua tai eivät edellytä sitä.

3. Täytä myyntirivit.  

    Jos olet määrittänyt oletusarvoisen ennakkomaksuprosentin joko asiakkaalle tai tämän asiakirjan **Ennakkomaksu**-pikavälilehdessä, tämä arvo kopioidaan kullekin riville. Voit muuttaa rivin **Ennakkomaksuprosentti**-kentän sisällön.  

    > [!TIP]
    > Jos et näe **Ennakkomaksuprosentti**-kenttää, voit lisätä sen mukauttamisen avulla.  Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

4. Valitse **Tilastot**-toiminto, jos haluat tarkastella ennakkomaksun kokonaissummaa.

    Jos haluat muuttaa ennakkomaksun kokonaissummaa, voit muuttaa **Myyntitilaustilastot**-sivun **Ennakkomaksun summa** -kentän sisältöä.  

    Jos **Hinnat sisältävät ALV:n** -kenttä on valittuna, **Ennakkomaksun summa sis. ALV:a** -kenttää voi muokata.  

    Jos muutat **Ennakkomaksun summa** -kentän sisältöä, summa jaetaan suhteellisesti muiden rivien kesken, paitsi rivien, joiden **Ennakkomaksuprosentti**-kentän arvo on **0**.  

5. Voit tulostaa testiraportin ennen ennakkomaksulaskun kirjaamista valitsemalla ensin **Ennakkomaksu**- ja sitten **Ennakkomaksun testiraportti** -toiminnon.  
6. Voit kirjata ennakkomaksulaskun valitsemalla ensin **Ennakkomaksu**- ja sitten **Kirjaa ennakkomaksulasku** -toiminnon.  

    Voit kirjata ja tulostaa ennakkomaksulaskun valitsemalla **Kirjaa ja tulosta ennakkomaksulasku** -toiminnon.  

Voit antaa muita tilauksen ennakkomaksulaskuja. Luo uusi lasku nostamalla yhden tai useamman rivin ennakkomaksua ja muuttamalla tarvittaessa asiakirjan päivämäärää ja kirjaamalla ennakkomaksulasku. Uusi lasku luodaan ennakkomaksun toistaiseksi laskutettujen summien ja uuden ennakkomaksun summan välisen eron vuoksi.  

> [!NOTE]  
> Jos sijaintisi on Pohjois-Amerikassa, et voi muuttaa ennakkomaksun osuutta sen jälkeen, kun ennakkomaksulasku on kirjattu. Tämä on estetty pohjoisamerikkalaisessa [!INCLUDE[prod_short](includes/prod_short.md)] -versiossa, koska arvonlisäveron laskutoimitus tuottaa muutoin väärän tuloksen.  

 Kun olet valmis kirjaamaan loput laskusta, kirjaa se kuten mikä tahansa lasku. Ennakkomaksusumma vähennetään automaattisesti erääntyvästä summasta.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Ennakkoon maksettujen tilausten ja laskujen tilan päivittäminen automaattisesti

Voit nopeuttaa tilausten ja laskujen käsittelemistä määrittämällä työjonotapahtumat, jotka päivittävät kyseisten asiakirjojen tilan automaattisesti. Kun ennakkomaksulasku on maksettu, työjonotapahtumat voivat automaattisesti muuttaa asiakirjan tilan **odottavasta ennakkomaksusta** **lähetetyksi**. Kun määrität työjonon tapahtumia, koodiyksiköt, joita tarvitset, ovat **384 Upd. Pending Prepmt. Sales** ja **384 Upd. Pending Prepmt. Purchase**. On suositeltavaa ajoittaa tapahtumat suoritettavaksi usein, esimerkiksi joka minuutti. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).

## <a name="see-also"></a>Katso myös

[Laskutuksen ennakkomaksut](finance-invoice-prepayments.md)  
[Vaihekuvaus: Myynnin ennakkomaksujen määrittäminen ja laskuttaminen](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Rahoitus](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Työtilan mukauttaminen](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
