---
title: Maksujen kohdistaminen maksamattomiin myyntiasiakirjoihin | Microsoft Docs
description: Asiakkaiden maksamat summat kohdistetaan liittyviin myyntiasiakirjoihin ja asiakas-, pääkirjanpito- ja pankkitapahtumat päivitetään kirjaamalla maksu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts, customer payment
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: b437246b22583e8e040bef78811765297ae2e675
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795306"
---
# <a name="reconcile-customer-payments-from-a-list-of-unpaid-sales-documents"></a>Asiakkaan maksujen täsmäyttäminen maksamattomien myyntiasiakirjojen luettelosta
Kun asiakkaat ovat suorittaneet maksuja sähköiselle pankkitilille, sinun täytyy kohdistaa jokainen maksettu summa vastaavaan myyntiasiakirjaan ja kirjata maksu sitten ja päivittää asiakkaan, yleisen päiväkirjan ja pankkitilin tapahtumat. Voit saada maksun ja rekisteröidä maksun eri tavoilla liiketoimintatarpeistasi riippuen: manuaalisesti, automaattisesti tai maksupalveluiden avulla.  

> [!NOTE]  
>   Voit suorittaa samat tehtävät, kuten esimerkiksi toimittajan maksut, **Maksujen täsmäytyskirjauskansio** -sivulla pankin tiliotteen tuonnin, automaattisen kohdistamisen ja pankkitilin täsmäyttämisen toimintojen avulla. Lisätietoja on kohdassa [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

**Rekisteröi asiakkaan maksut** -sivu on tarkoitettu tukemaan tehtävissä, jotka kuuluvat sisäinen vastatilien täsmäämiseen todellisten kassalukujen tehokkaan keräämisen varmistamiseksi asiakkailta. Tämän maksunkäsittelytyökalun avulla voit nopeasti tarkistaa ja kirjata yksittäisiä tai maksujen kokonaissummia, käsitellä alennettuja maksuja ja etsiä tiettyjä maksamattomia asiakirjoja, joille maksu suoritetaan.

Eri asiakkaiden maksut, joilla on eri maksupäivät, täytyy kirjata yksittäisinä maksuina. Saman asiakkaan maksut, joilla on sama maksupäivämäärä, voidaan kirjata kokonaissummana. Tästä on hyötyä esimerkiksi silloin, kun asiakas on suorittanut yksittäisen maksun, joka kattaa useita myyntilaskuja.

## <a name="to-set-up-the-payment-registration-journal"></a>Voit määrittää maksukirjauspäiväkirjan
Koska voit kirjata eri maksulajeja eri vastatileille, sinun on valittava vastatili **Maksurekisteröinnin asetukset** -sivulla, ennen kuin alat käsitellä asiakkaan maksuja. Jos kirjaat aina samalle vastatilille, voit määrittää kyseisen tilin oletusarvoksi ja välttää tämän vaiheen aina, kun avaat **Rekisteröi asiakkaan maksut** -sivun.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksurekisteröinnin asetukset** ja valitse sitten liittyvä linkki.

    Vaihtoehtoisesti voit valita **Rekisteröi asiakkaan maksut** -sivulla **Asetus**-toiminnon.    
2. Täytä **Maksurekisteröinnin asetukset** -sivun kentät. Lue kentän lyhyt kuvaus valitsemalla kenttä tai siirry liittyviin tietoihin valitsemalla linkki.  

## <a name="to-register-customer-payments-individually"></a>Asiakkaan maksujen rekisteröiminen yksitellen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Rekisteröi asiakkaan maksut** ja valitse sitten liittyvä linkki.  

    **Rekisteröi asiakkaan maksut** -sivulla ovat kaikki kirjatut asiakirjat, joille maksun voi rekisteröidä. Sivu voidaan avata myös **Asiakkaat**- ja **Asiakaskortti**-sivuilla, jossa se suodatetaan automaattisesti tietyn asiakkaan mukaan.  
2. Valitse **Maksu suoritettu** -valintaruutu rivillä, joka edustaa sitä kirjattua asiakirjaa, josta maksu on suoritettu.

    Jos **Täytä vastaanottopäivämäärä automaattisesti** -valintaruutu on valittu **Maksurekisteröinnin asetukset** -sivulla, käsittelypäivämäärä annetaan **Vastaanottopvm** -kenttään.  
3. Syötä **Vastaanottopvm**-kenttään päivämäärä, jolloin maksu tehtiin. Tämä päivä voi olla eri kuin käsittelypäivämäärä.  
4. Syötä **Vastaanotettu summa** -kenttään summa, joka on maksettu.

    Täysille maksuille tämä on sama kuin rivin **Jäljellä oleva summa** -kentässä oleva summa. Osittaisille maksuille tämä on pienempi kuin rivin **Jäljellä oleva summa** -kentässä oleva summa.    
5. Toista vaiheet 2-4 muille riveille, jotka edustavat kirjattuja asiakirjoja, joista maksut suoritetaan.  
6. Valitse **Kirjaa maksut** -toiminto.  

Maksutiedot kirjataan asiakirjoille, joita edustavat ne rivit, joiden **Maksu suoritettu** -valintaruutu on valittuna.  

Maksutapahtumat kirjataan pääkirjanpitoon, pankkiin ja asiakastileille. Kukin maksu kohdistetaan siihen liittyvään myyntiasiakirjaan.  

## <a name="to-reconcile-lump-sum-payments"></a>Kokonaismaksujen täsmäyttäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksurekisteröinti** ja valitse sitten liittyvä linkki.
2. Valitse **Maksu suoritettu** -valintaruutu riveille, jotka edustavat saman asiakkaan kirjattuja asiakirjoja, joista kokonaissumma on suoritettu.  

    > [!NOTE]  
    >   **Nimi**-kentässä olevan asiakkaan on oltava sama kaikilla riveillä, jotka kirjataan kokonaissummana.  

    Jos **Täytä vastaanottopäivämäärä automaattisesti** -valintaruutu on valittu **Maksurekisteröinnin asetukset** -sivulla, käsittelypäivämäärä täytetään **Vastaanottopvm** -kenttään.  
3. Anna **Vastaanottopvm**-kenttään päivämäärä, jolloin maksu tehtiin. Tämä päivä voi olla eri kuin käsittelypäivämäärä.  

    > [!NOTE]  
    >   Tämän päivämäärän on oltava sama kaikille riveille, jotka kirjataan kokonaissummana.  
4. Syötä **Vastaanotettu summa** -kenttään niiden useiden rivien summat, jotka ovat yhteensä kokonaissumman suuruiset.  

    > [!TIP]  
    > Yritä kirjata mahdollisimman monta täyttää maksua kokonaissumman kanssa. Kirjoita summia, jotka ovat samat kuin **Jäljellä oleva summa** -kentän summa mahdollisimman monella rivillä.  
5. Toista vaiheet 2-4 muille riveille, jotka edustavat saman asiakkaan kirjattuja asiakirjoja, joista kokonaissumma on suoritettu.  
6. Valitse **Kirjaa kokonaismaksuna** -toiminto. Syötetyt maksutiedot kirjataan asiakirjoille, joita edustavat ne rivit, joiden **Maksu suoritettu** -valintaruutu on valittuna.  

Maksutapahtumat kirjataan pääkirjanpitoon, pankkiin ja asiakastileille. Kukin maksu kohdistetaan siihen liittyvään myyntiasiakirjaan.  

Jos pankissa suoritettua maksua ei kuitenkaan esitetä minkään rivin avulla **Maksurekisteröinti**-sivulla, liittyvää asiakirjaa ei ehkä ole vielä kirjattu. Tässä tapauksessa voit löytää asiakirjan hakutoiminnon avulla nopeasti ja kirjata sen maksukäsittelyä varten. Lisätietoja on kohdassa [Tietyn myyntiasiakirjan etsiminen, jota ei ole laskutettu kokonaan](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-find-a-specific-sales-document-that-is-not-fully-invoiced).  

Jos pankissa suoritettua maksua ei kuitenkaan esitetä minkään asiakirjan avulla [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, avaa esitäytetty yleinen päiväkirja **Maksurekisteröinti**-sivulla ja kirjaa maksu suoraan vastatilille kohdistamatta maksua asiakirjaan. Vaihtoehtoisesti voit haluta tallentaa maksun päiväkirjaan ennen kuin maksun alkuperä on ratkaistu. Lisätietoja on kohdassa [Maksun kirjaaminen tai lähettäminen ilman aiheeseen liittyvää asiakirjaa](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document),  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Alennettujen maksujen käsittely manuaalisesti
Jos olet sopinut asiakkaan kanssa maksualennuksesta, sitten maksusummat voivat olla pienempiä kuin laskun summat, jos maksu suoritetaan ennen sovitun alennuksen päivämäärää.  

Seuraavaksi käsitellään neljä erilaista menettelytapaa alennettujen maksujen kirjaamiseen **Maksurekisteröinti**-sivulla.  

* Sellaisen maksusumman käsittely, joka on yhtä suuri kuin jäljellä oleva alennettu summa, ja jonka maksupäivämäärä on ennen alennuspäivämäärää. Voit kirjata maksun sellaisenaan.  
* Sellaisen maksusumman käsittely, joka on yhtä suuri kuin jäljellä oleva alennettu summa, ja jonka maksupäivämäärä on alennuspäivämäärän jälkeen. Voit kirjata maksun osittain. Asiakirja pysyy avoimena ja kerää/maksaa jäljellä olevan summan. Vaihtoehtoisesti voit määrittää alennuksen päivämäärään myöhemmäksi, jotta maksu voidaan maksaa kokonaisuudessaan.  
* Sellaisen summan käsittely, joka on pienempi kuin jäljellä oleva alennettu määrä. Voit kirjata maksun osittain. Asiakirja pysyy avoimena ja kerää/maksaa jäljellä olevan summan.  
* Sellaisen summan käsittely, joka on suurempi kuin jäljellä oleva alennettu määrä. Voit kirjata maksut sellaisenaan. Vain jäljelle jäävä summa kirjataan. Ylimääräinen summa hyvitetään asiakkaalle.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Sellaisen maksusumman käsittely, joka on yhtä suuri kuin alennettu summa, ja jonka maksupäivämäärä on ennen alennuspäivämäärää.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksurekisteröinti** ja valitse sitten liittyvä linkki.  
2. Lisää maksusumma **Vastaanotettu summa** -kenttään. Summa on yhtä suuri kuin **Jäljellä oleva summa alennuksen jälkeen** -kentän summa.

    **Maksu suoritettu** -valintaruutu valitaan automaattisesti, ja **Vastaanottopvm**-kenttä täytetään käsittelypäivämäärällä.    
3. Syötä maksun päivämäärä **Vastaanottopvm**-kenttään. Päivämäärä on ennen **Maksualennuspvm**-kentän päivämäärää.
4. Varmista, että **Jäljellä oleva summa** -kentässä on nolla (0).  
5. Valitse **Kirjaa maksut** -toiminto, kun haluat kirjata koko maksun pääkirjanpitoon, pankkiin ja asiakastileille.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Sellaisen maksusumman käsittely, joka on yhtä suuri kuin alennettu summa, mutta jonka maksupäivämäärä on alennuspäivämäärän jälkeen.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksurekisteröinti** ja valitse sitten liittyvä linkki.  
2. Lisää maksusumma **Vastaanotettu summa** -kenttään. Summa on yhtä suuri kuin **Jäljellä oleva summa alennuksen jälkeen** -kentän summa.

    **Maksu suoritettu** -valintaruutu valitaan automaattisesti, ja **Vastaanottopvm**-kenttä täytetään käsittelypäivämäärällä.
3. Syötä **Vastaanottopvm**-kenttään maksupäivämäärä, joka on **Maksualennuspvm**-kentän päivämäärän jälkeen. Päivämääräkenttien fontti muuttuu punaiseksi ja sivun alaosassa näkyy virheviesti.

    > [!TIP]  
    >   Jos haluat tehdä poikkeuksen ja antaa alennusta, vaikka maksu on myöhässä, toimi seuraavasti:
4. Valitse **Tiedot**-toiminto.  
5. Anna **Maksurekisteröinnin tiedot** -sivun **Maksualennuspvm**-kentän **Maksualennus**-pikavälilehteen päivämäärä, joka on myöhempi kuin **Maksurekisteröinti**-sivun **Vastaanottopvm**-kentän päivämäärä.  

    Virhesanoma tulee ja punainen fontti katoavat, ja voit siirtyä käsittelemään alennettua maksua.    
6. Varmista, että **Jäljellä oleva summa** -kentässä on summa, joka jää maksettavaksi täytenä laskusummana.  
7. Valitse **Kirjaa maksut** -toiminto, kun haluat kirjata osittaisen maksun pääkirjanpitoon, pankkiin ja asiakastileille.  

Liittyvä asiakirja pysyy avoimena.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Sellaisen maksun käsittely, joka on pienempi kuin jäljellä oleva alennettu määrä.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksurekisteröinti** ja valitse sitten liittyvä linkki.  
2. Lisää maksusumma **Vastaanotettu summa** -kenttään. Summa on pienempi kuin **Jäljellä oleva summa alennuksen jälkeen** -kentän summa.

    **Maksu suoritettu** -valintaruutu valitaan automaattisesti, ja **Vastaanottopvm**-kenttä täytetään käsittelypäivämäärällä.  
3. Syötä maksun päivämäärä **Vastaanottopvm**-kenttään. Päivämäärä on ennen **Maksualennuspvm**-kentän päivämäärää.
4. Varmista, että **Jäljellä oleva summa** -kentässä on summa, joka jää maksettavaksi alennettuna summana.  
5. Valitse **Kirjaa maksut** -toiminto, kun haluat kirjata osittaisen maksun pääkirjanpitoon, pankkiin ja asiakastileille.  

Liittyvä asiakirja pysyy avoimena.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Sellaisen maksun käsittely, joka on suurempi kuin jäljellä oleva alennettu määrä.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksurekisteröinti** ja valitse sitten liittyvä linkki.  
2. Lisää maksusumma **Vastaanotettu summa** -kenttään. Summa on suurempi kuin **Jäljellä oleva summa alennuksen jälkeen** -kentän summa.  

    **Maksu suoritettu** -valintaruutu valitaan automaattisesti, ja **Vastaanottopvm**-kenttä täytetään käsittelypäivämäärällä.    
3. Syötä maksun päivämäärä **Vastaanottopvm**-kenttään. Päivämäärä on ennen **Maksualennuspvm**-kentän päivämäärää.
4. Varmista, että **Jäljellä oleva summa** -kentässä on nolla (0).  
5. Valitse **Kirjaa maksut** -toiminto, kun haluat kirjata koko maksun pääkirjanpitoon, pankkiin ja asiakastileille.  

Liittyvät asiakirja suljetaan ja asiakkaalle hyvitetään ylimääräinen maksusumma.  

## <a name="to-find-a-specific-sales-document-that-is-not-fully-invoiced"></a>Voit etsiä tietyn myyntiasiakirjan, jota ei ole laskutettu kokonaan
**Maksurekisteröinti**-sivu tukee tehtäviä, joita tarvitaan sisäisten tilien täsmäämiseen todellisten kassalukemien, jotta tehokas perintä asiakkailta voidaan varmistaa. Se näyttää avoimet saapuvat maksut riveinä, jotka edustavat myyntiasiakirjoja, joiden summa on erääntynyt maksettavaksi.  

Yleensä, kun maksu on tehty, tallennettu pankkiin tai muuten, liittyvä myynti- tai ostoasiakirja esitetään rivinä **Maksurekisteröinti**-sivulla, koska kyseinen asiakirja odottaa maksua kirjattavaksi avointa summaa vastaan. Joskus suoritettua maksua ei kuitenkaan esitetä **Maksurekisteröinti**-sivun rivillä. Yleensä syynä on, että kyseisiä asiakirjoja ei ole kirjattu täysin.

**Asiakirjahaku**-sivulla voi etsiä asiakirjoja, joita ei ole laskutettu kokonaan. Voit etsiä seuraavista yhden tai useamman ehdon perusteella:  

* Asiakirjanumero  
* Määrän tai summan alue  

Seuraavissa selitetään, kuinka etsiä määrättyä asiakirjaa molempien hakuehtojen avulla.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksurekisteröinti** ja valitse sitten liittyvä linkki.
2. Kun kohdistin on minkä tahansa rivin päällä, valitse **Etsi asiakirjoja** -toiminto.
3. Anna **Asiakirjahaku**-sivun **Asiakirjan nro** -kentässä hakuarvo.  

    > [!NOTE]  
    >   Tässä kentässä annetun arvon ympärillä on piilotettuihin yleismerkit. Tämä tarkoittaa sitä, että funktio etsii kaikkia asiakirjanumeroita, jotka sisältävät syötetyn arvon.    
4. Syötä **Summa**-kenttään etsittävässä asiakirjassa oleva määrätty summa.  
5. Syötä **Summan toleranssiprosentti** -kenttään prosenttiarvo määrittääksesi summien välin, josta haluat etsiä löytääksesi avoimen asiakirjan.  

    Jos syötät arvon 10, funktio etsii kymmenen prosenttia alhaisempia ja 10 prosenttia korkeampia summia kuin **Summa**-kentän arvo.    
6. Valitse **Hae**-toiminto.  

Hakutoiminto etsii sellaisten asiakirjojen joukosta, joita ei ole laskutettu kokonaan määrättyjen ehtojen perusteella.  

Jos yksi tai usea asiakirja vastaa hakuehtoja, myös **Asiakirjahaun tulos** -sivu avautuu ja näkyvissä on kyseisiä asiakirjoja vastaavat rivit. Kullakin rivillä on asiakirjanumero, kuvaus ja summa, joten löydät helposti tietyn asiakirjan, esimerkiksi pankin tiliotteen tietojen perusteella.  

Jos pankissa suoritettua maksua ei kuitenkaan esitetä minkään asiakirjan avulla [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, avaa esitäytetty yleinen päiväkirja **Maksurekisteröinti**-sivulla ja kirjaa maksu suoraan vastatilille kohdistamatta maksua asiakirjaan. Vaihtoehtoisesti voit haluta tallentaa maksun päiväkirjaan ennen kuin maksun alkuperä on ratkaistu.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Maksun kirjaaminen tai lähettäminen ilman aiheeseen liittyvää asiakirjaa
Jos pankissa suoritettua maksua ei kuitenkaan esitetä minkään asiakirjan avulla [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, avaa esitäytetty yleisen päiväkirjan rivi **Maksurekisteröinti**-sivulla ja kirjaa maksu suoraan vastatilille kohdistamatta maksua asiakirjaan. Vaihtoehtoisesti voit haluta tallentaa maksun päiväkirjaan ennen kuin maksun alkuperä on selvitetty.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksurekisteröinti** ja valitse sitten liittyvä linkki.  

    Siirry kirjaamaan dokumentoimaton maksu.  
2. Valitse **Yleinen päiväkirja** -toiminto.  

    **Yleinen päiväkirja** -sivu avautuu. Se sisältää yhden rivin, joka on esitäytetty **Maksurekisteröinnin asetukset** -sivulla määritetyllä päiväkirjaerän vastatilillä.  
3. Täytä jäljellä olevat kentät yleisen päiväkirjan rivillä, esimerkiksi summa ja asiakasnumero tai muita tietoja pankin tiliotteesta. Lisätietoja on kohdassa [Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md).  

Voit kirjata päiväkirjarivin päivittämään vastatilin yhteissummaa. Vaihtoehtoisesti voit jättää päiväkirjarivin kirjaamatta ja kenties liittää se huomautuksen kanssa siitä, että maksu tarvitsee tarkempia analyyseja.  

Jos jätät päiväkirjarivin kirjaamatta, se lisätään **Kirjaamaton saldo** -kentän arvoon **Maksurekisteröinti**-sivun alaosassa.  

## <a name="see-also"></a>Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
