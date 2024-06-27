---
title: Maksujen kohdistaminen maksamattomiin myyntiasiakirjoihin
description: 'Asiakkaiden maksamat summat kohdistetaan liittyviin myyntiasiakirjoihin ja asiakas-, pääkirjanpito- ja pankkitapahtumat päivitetään kirjaamalla maksu.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts, customer payment'
ms.search.form: '1290, 1294, 1287'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="reconcile-customer-payments-from-a-list-of-unpaid-sales-documents"></a>Asiakkaan maksujen täsmäyttäminen maksamattomien myyntiasiakirjojen luettelosta

Tee seuraavat toiminnot sen jälkeen, kun asiakkaat ovat tehneet sähköisiä maksuja pankkitilillesi:

* Kukin maksettu summa kohdistetaan siihen liittyvään myyntiasiakirjaan.
* Maksu kirjataan asiakkaan, pääkirjanpidon ja pankkitapahtumien päivittämiseksi.

Yrityksesi tarpeista riippuen voit rekisteröidä maksuja manuaalisesti, automaattisesti ja maksupalvelujen kautta.  

> [!NOTE]  
> Voit tehdä samat tehtävät, kuten toimittajamaksut **Maksun täsmäytyspäiväkirja** -sivulla. Voit esimerkiksi tuoda tiliotteita, käyttää automaattista kohdistusta ja täsmäyttää pankkitilejä. Lisätietoja on kohdassa [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

Varmista, että maksut peritään, käyttämällä **Rekisteröi asiakkaan maksut** -sivun sisäisten tilien täsmäämistä todellisten kassalukemien avulla. Voit nopeasti tarkistaa ja kirjata yksittäisiä tai kerta suorituksina suoritettavia maksuja, käsitellä alennettuja maksuja ja etsiä maksamattomat asiakirjat.

Sinun on kirjattava eri asiakkaiden maksut, joilla on eri maksupäivät, yksittäisinä maksuina. Saman asiakkaan maksut, joilla on sama maksupäivämäärä, voidaan kirjata kokonaissummana. Kokonaissummamaksut ovat hyödyllisiä esimerkiksi silloin, kun asiakas on suorittanut yksittäisen maksun, joka kattaa useita myyntilaskuja.

## <a name="to-set-up-the-payment-registration-journal"></a>Voit määrittää maksukirjauspäiväkirjan

Koska voit kirjata eri maksulajeja eri vastatileille, sinun on valittava vastatili **Maksurekisteröinnin asetukset** -sivulla, ennen kuin alat käsitellä asiakkaan maksuja. Jos kirjaat aina samalle vastatilille, voit määrittää kyseisen tilin oletusarvoksi ja välttää tämän vaiheen aina, kun avaat **Rekisteröi asiakkaan maksut** -sivun.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksurekisteröinnin asetukset** ja valitse sitten liittyvä linkki. Vaihtoehtoisesti voit valita **Rekisteröi asiakkaan maksut** -sivulla **Asetus**-toiminnon.
2. Täytä **Maksurekisteröinnin asetukset** -sivun kentät. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)].  

> [!TIP]
> Voit määrittää kirjauskansioon tietyn numerosarjan. Tämä helpottaa tapahtumien tunnistamista myöhemmin maksukirjauskansiossa. Numerosarjoista on hyötyä, jos käytät maksujen täsmäytyskirjauskansioita käytetään maksujen rekisteröimiseen ja kohdistamiseen.

## <a name="to-register-customer-payments-individually"></a>Asiakkaan maksujen rekisteröiminen yksitellen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Rekisteröi asiakkaan maksut** ja valitse sitten vastaava linkki.  

    **Rekisteröi asiakkaan maksut** -sivulla ovat kaikki kirjatut asiakirjat, joille maksun voi rekisteröidä. Voit myös avata sivun **Asiakkaat**- ja **Asiakaskortti**-sivuilta, jotka on suodatettu määritetyn asiakkaan mukaan.  
2. Valitse **Maksu suoritettu** -valintaruutu rivillä, joka edustaa sitä kirjattua asiakirjaa, josta maksu on suoritettu.
3. Syötä **Vastaanottopvm**-kenttään päivämäärä, jolloin maksu tehtiin. Tämä päivä voi olla eri kuin käsittelypäivämäärä.  

   Jos **Täytä vastaanottopäivämäärä automaattisesti** -valintaruutu on valittu **Maksurekisteröinnin asetukset** -sivulla, **Vastaanottopvm**-kenttä sisältää käsittelypäivän.  
4. Syötä **Vastaanotettu summa** -kenttään summa, joka on maksettu.

    Täysille maksuille tämä summa on sama kuin rivin **Jäljellä oleva summa** -kentässä oleva summa. Osittaisille maksuille tämä summa on pienempi kuin rivin **Jäljellä oleva summa** -kentässä oleva summa.
5. Toista vaiheet 2-4 muille riveille, jotka edustavat kirjattuja asiakirjoja, joista maksut suoritetaan.  
6. Valitse **Kirjaa maksut** -toiminto.  

Maksutiedot kirjataan asiakirjoille, joita edustavat ne rivit, joiden **Maksu suoritettu** -valintaruutu on valittuna. Maksutapahtumat kirjataan pääkirjanpitoon, pankkiin ja asiakastileille.

## <a name="to-reconcile-lump-sum-payments"></a>Kokonaismaksujen täsmäyttäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Rekisteröi asiakkaan maksut** ja valitse sitten vastaava linkki.
2. Valitse **Maksu suoritettu** -valintaruutu riveille, jotka edustavat saman asiakkaan kirjattuja asiakirjoja, joista kokonaissumma on suoritettu.  

    > [!NOTE]  
    > **Nimi**-kentässä olevan asiakkaan on oltava sama kaikilla riveillä, jotka kuuluvat kokonaissummaan.  

    Jos **Täytä vastaanottopäivämäärä automaattisesti** -valintaruutu on valittu **Maksurekisteröinnin asetukset** -sivulla, **Vastaanottopvm**-kenttä sisältää käsittelypäivän.  
3. Syötä **Vastaanottopvm**-kenttään päivämäärä, jolloin maksu tehtiin. Tämä päivä voi olla eri kuin käsittelypäivämäärä.  

    > [!NOTE]  
    > Tämän päivämäärän on oltava sama kaikille riveille, jotka kirjataan kokonaissummana.  
4. Syötä **Vastaanotettu summa** -kenttään niiden useiden rivien summat, jotka ovat yhteensä kokonaissumman suuruiset.  

    > [!TIP]  
    > Yritä kirjata mahdollisimman monta täyttää maksua kokonaissumman kanssa. Kirjoita summia, jotka ovat samat kuin **Jäljellä oleva summa** -kentän summa mahdollisimman monella rivillä.  
5. Toista vaiheet 2-4 muille riveille, jotka edustavat saman asiakkaan kirjattuja asiakirjoja, joista kokonaissumma on suoritettu.  
6. Valitse **Kirjaa kokonaismaksuna** -toiminto.

   Maksutiedot kirjataan asiakirjoille, joita edustavat ne rivit, joiden **Maksu suoritettu** -valintaruutu on valittuna. Maksutapahtumat kirjataan pääkirjanpitoon, pankkiin ja asiakastileille. Kukin maksu kohdistetaan siihen liittyvään myyntiasiakirjaan.  

Jos pankissa suoritettua maksua ei kuitenkaan esitetä minkään rivin avulla **Rekisteröi asiakkaan maksut** -sivulla, liittyvää asiakirjaa ei ehkä ole vielä kirjattu. Tässä tapauksessa voit löytää asiakirjan hakutoiminnon avulla nopeasti ja kirjata sen maksukäsittelyä varten. Lisätietoja on kohdassa [Tietyn myyntiasiakirjan etsiminen, jota ei ole laskutettu kokonaan](#to-find-a-specific-sales-document-that-isnt-fully-invoiced).  

Jos pankissa suoritettua maksua ei kuitenkaan esitetä minkään asiakirjan avulla, avaa esitäytetty yleinen päiväkirja **Maksurekisteröinti**-sivulla ja kirjaa maksu suoraan vastatilille kohdistamatta maksua asiakirjaan. Vaihtoehtoisesti voit haluta tallentaa maksun päiväkirjaan ennen kuin maksun alkuperä on ratkaistu. Lisätietoja on kohdassa [Maksun kirjaaminen tai lähettäminen ilman aiheeseen liittyvää asiakirjaa](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document),  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Alennettujen maksujen käsittely manuaalisesti

Jos olet sopinut asiakkaan kanssa maksualennuksesta, sitten maksusummat voivat olla pienempiä kuin laskun summat, jos maksu suoritetaan ennen sovitun alennuksen päivämäärää.  

Seuraavaksi käsitellään erilaisia menettelytapaa alennettujen maksujen kirjaamiseen **Maksurekisteröinti**-sivulla.  

* Sellaisen maksusumman käsittely, joka on yhtä suuri kuin jäljellä oleva alennettu summa, ja jonka maksupäivämäärä on ennen alennuspäivämäärää. Voit kirjata maksun sellaisenaan.  
* Sellaisen maksusumman käsittely, joka on yhtä suuri kuin jäljellä oleva alennettu summa, ja jonka maksupäivämäärä on alennuspäivämäärän jälkeen. Voit kirjata maksun osittain. Asiakirja pysyy avoimena ja kerää/maksaa jäljellä olevan summan. Voit myös määrittää alennuksen päivämäärään myöhemmäksi, jotta maksu voidaan maksaa kokonaisuudessaan.  
* Sellaisen summan käsittely, joka on pienempi kuin jäljellä oleva alennettu määrä. Voit kirjata maksun osittain. Asiakirja pysyy avoimena ja kerää/maksaa jäljellä olevan summan.  
* Sellaisen summan käsittely, joka on suurempi kuin jäljellä oleva alennettu määrä. Voit kirjata maksut sellaisenaan. Vain jäljelle jäävä summa kirjataan. Lisäsumma hyvitetään asiakkaalle.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Sellaisen maksusumman käsittely, joka on yhtä suuri kuin alennettu summa, ja jonka maksupäivämäärä on ennen alennuspäivämäärää.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Rekisteröi asiakkaan maksut** ja valitse sitten vastaava linkki.  
2. Lisää maksusumma **Vastaanotettu summa** -kenttään. Summa on yhtä suuri kuin **Jäljellä oleva summa sis. alennuksen** -kentän summa.

    **Maksu suoritettu** -valintaruutu valitaan automaattisesti, ja **Vastaanottopvm**-kenttä täytetään käsittelypäivämäärällä.
3. Syötä maksun päivämäärä **Vastaanottopvm**-kenttään. Päivämäärä on ennen **Maksualennuspvm**-kentän päivämäärää.
4. Varmista, että **Jäljellä oleva summa** -kentässä on nolla (0).  
5. Valitse **Kirjaa maksut** -toiminto, kun haluat kirjata koko maksun pääkirjanpitoon, pankkiin ja asiakastileille.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Sellaisen maksusumman käsittely, joka on yhtä suuri kuin alennettu summa, mutta jonka maksupäivämäärä on alennuspäivämäärän jälkeen.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Rekisteröi asiakkaan maksut** ja valitse sitten vastaava linkki.  
2. Lisää maksusumma **Vastaanotettu summa** -kenttään. Summa on yhtä suuri kuin **Jäljellä oleva summa sis. alennuksen** -kentän summa.

    **Maksu suoritettu** -valintaruutu valitaan automaattisesti, ja **Vastaanottopvm**-kenttä täytetään käsittelypäivämäärällä.
3. Syötä **Vastaanottopvm**-kenttään maksupäivämäärä, joka on **Maksualennuspvm**-kentän päivämäärän jälkeen.

   Päivämääräkenttien fontti muuttuu punaiseksi ja sivun alaosassa näkyy virheviesti. Kaksi seuraavaa vaihetta korjaavat tämän.
4. Valitse **Tiedot**-toiminto.  
5. Anna **Maksurekisteröinnin tiedot** -sivun **Maksualennuspvm**-kentän **Maksualennus**-pikavälilehteen päivämäärä, joka on myöhempi kuin **Maksurekisteröinti**-sivun **Vastaanottopvm**-kentän päivämäärä.  

    Virhesanoma tulee ja punainen fontti katoavat, ja voit siirtyä käsittelemään alennettua maksua.
6. Varmista, että **Jäljellä oleva summa** -kentässä on summa, joka jää maksettavaksi täytenä laskusummana.  
7. Valitse **Kirjaa maksut** -toiminto, kun haluat kirjata osittaisen maksun pääkirjanpitoon, pankkiin ja asiakastileille.  

Liittyvä asiakirja pysyy avoimena.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Sellaisen maksun käsittely, joka on pienempi kuin jäljellä oleva alennettu määrä.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Rekisteröi asiakkaan maksut** ja valitse sitten vastaava linkki.  
2. Lisää maksusumma **Vastaanotettu summa** -kenttään. Summa on pienempi kuin **Jäljellä oleva summa sis. alennuksen** -kentän summa.

    **Maksu suoritettu** -valintaruutu valitaan automaattisesti, ja **Vastaanottopvm**-kenttä täytetään käsittelypäivämäärällä.  
3. Syötä maksun päivämäärä **Vastaanottopvm**-kenttään. Päivämäärä on ennen **Maksualennuspvm**-kentän päivämäärää.
4. Varmista, että **Jäljellä oleva summa** -kentässä on summa, joka jää maksettavaksi alennettuna summana.  
5. Valitse **Kirjaa maksut** -toiminto, kun haluat kirjata osittaisen maksun pääkirjanpitoon, pankkiin ja asiakastileille.  

Liittyvä asiakirja pysyy avoimena.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Sellaisen maksun käsittely, joka on suurempi kuin jäljellä oleva alennettu määrä.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Rekisteröi asiakkaan maksut** ja valitse sitten vastaava linkki.  
2. Lisää maksusumma **Vastaanotettu summa** -kenttään. Summa on suurempi kuin **Jäljellä oleva summa sis. alennuksen** -kentän summa.  

    **Maksu suoritettu** -valintaruutu valitaan automaattisesti, ja **Vastaanottopvm**-kenttä täytetään käsittelypäivämäärällä.
3. Syötä maksun päivämäärä **Vastaanottopvm**-kenttään. Päivämäärä on ennen **Maksualennuspvm**-kentän päivämäärää.
4. Varmista, että **Jäljellä oleva summa** -kentässä on nolla (0).  
5. Valitse **Kirjaa maksut** -toiminto, kun haluat kirjata koko maksun pääkirjanpitoon, pankkiin ja asiakastileille.  

Liittyvät asiakirja suljetaan ja asiakkaalle hyvitetään ylimääräinen maksusumma.  

## <a name="to-find-a-specific-sales-document-that-isnt-fully-invoiced"></a>Voit etsiä tietyn myyntiasiakirjan, jota ei ole laskutettu kokonaan

**Rekisteröi asiakasmaksut** -sivu tukee tehtäviä, joita tarvitaan sisäisten tilien täsmäämiseen todellisten kassalukemien, jotta tehokas perintä asiakkailta voidaan varmistaa. Se näyttää avoimet saapuvat maksut riveinä, jotka edustavat myyntiasiakirjoja, joiden summa on erääntynyt maksettavaksi.  

Tavallisesti kun maksu suoritetaan, tallennetaan pankkiin tai muutoin, myynti- tai ostoasiakirja esitetään rivinä **Rekisteröi asiakasmaksut** -sivulla. Asiakirja odottaa maksun kirjaamista avoimeen summaan. Joskus suoritettua maksua ei kuitenkaan esitetä rivillä **Rekisteröi asiakasmaksut** -sivulla, yleensä siksi, että asiakirjaa ei ole laskutettu kokonaan.

**Asiakirjahaku**-sivulla voi etsiä asiakirjoja, joita ei ole laskutettu kokonaan. Voit etsiä seuraavista yhden tai useamman ehdon perusteella:  

* Asiakirjanumero  
* Määrän tai summan alue  

Seuraavissa selitetään, kuinka etsiä määrättyä asiakirjaa molempien hakuehtojen avulla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Rekisteröi asiakkaan maksut** ja valitse sitten vastaava linkki.
2. Kun kohdistin on minkä tahansa rivin päällä, valitse **Etsi asiakirjoja** -toiminto.
3. Anna **Asiakirjahaku**-sivun **Asiakirjan nro** -kentässä hakuarvo.  

    > [!NOTE]  
    > Tässä kentässä annetun arvon ympärillä on piilotettuihin yleismerkit. Tämä tarkoittaa sitä, että toiminto etsii kaikkia asiakirjanumeroita, jotka sisältävät syötetyn arvon.
4. Syötä **Summa**-kenttään etsittävässä asiakirjassa oleva määrätty summa.  
5. Syötä **Summan toleranssiprosentti** -kenttään prosenttiarvo määrittääksesi summien välin, josta haluat etsiä löytääksesi avoimen asiakirjan.  

    Jos syötät 10, toiminto etsii summia, jotka ovat summavälissä, joka on plus tai miinus 10 prosenttia **Summa**-kentän arvosta.
6. Valitse **Hae**-toiminto.  

Jos yksi tai usea asiakirja vastaa hakuehtoja, myös **Asiakirjahaun tulos** -sivu avautuu ja näkyvissä on kyseisiä asiakirjoja vastaavat rivit. Jokaisella rivillä on asiakirjanumero, kuvaus ja summa.

Jos pankissa suoritettua maksua ei kuitenkaan esitetä minkään asiakirjan avulla, avaa esitäytetty yleinen päiväkirja **Maksurekisteröinti**-sivulla ja kirjaa maksu suoraan vastatilille kohdistamatta maksua asiakirjaan. Vaihtoehtoisesti voit haluta tallentaa maksun päiväkirjaan ennen kuin maksun alkuperä on ratkaistu.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Maksun kirjaaminen tai lähettäminen ilman aiheeseen liittyvää asiakirjaa

Jos pankissa olevaan maksuun ei ole liitetty asiakirjaa, voit avata valmiiksi täytetyn yleisen päiväkirjan rivin **Yleisen päiväkirjan** toiminnon avulla **Rekisteröi asiakasmaksut** -sivulta. Päiväkirjan käyttäminen maksun kirjaamiseen suoraan vastatilille kohdistamatta maksua asiakirjaan. Vaihtoehtoisesti voit haluta tallentaa maksun päiväkirjaan ennen kuin maksun alkuperä on ratkaistu.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Rekisteröi asiakkaan maksut** ja valitse sitten vastaava linkki.
2. Valitse **Yleinen päiväkirja** -toiminto.  

    **Yleinen päiväkirja** -sivu avautuu. Se sisältää yhden rivin, jolla on **Maksurekisteröinnin asetukset** -sivulla määritetty päiväkirjaerän vastatili.  
3. Täytä kunkin yleisen päiväkirjan rivin muut kentät. Anna esimerkiksi summa, asiakasnumero tai tiliotteen tiedot. Lisätietoja on kohdassa [Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md).  

Voit kirjata päiväkirjarivin päivittämään vastatilin yhteissummaa. Voit myös jättää päiväkirjarivin kirjaamatta ja kenties liittää se huomautuksen kanssa siitä, että maksu tarvitsee tarkempia analyyseja.  

Jos et kirjaa päiväkirjan riviä, sen arvo lisätään **Maksurekisteröinti**-sivun **Rem. summa sis. alennus** -kentän arvoon.  

## <a name="see-also"></a>Katso myös

[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
