---
title: Myynnin laskutus
description: 'Tässä ohjeaiheessa kerrotaan, miten luodaan kauppakirja tai myyntilasku tai myyntitilaus kirjaamaan asiakkaan kanssa tehty sopimus tuotteiden myynnistä tietyin ehdoin.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bill, sale, invoice, order'
ms.search.form: '43, 48, 9301'
ms.date: 09/01/2022
ms.author: edupont
---
# <a name="invoice-sales"></a><a name="invoice-sales"></a>Myynnin laskutus

Voit yleensä luoda joko myyntitilauksen tai -laskun tallentaaksesi sopimuksesi asiakkaan kanssa ja myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla.  

Myyntitilausta täytyy kuitenkin käyttää myyntilaskun sijaan, jos:  

* Tilauksesta on toimitettava vain osa, koska esimerkiksi tilauksen koko määrä ei ole varastossa.  
* Tuotteet toimitetaan sen jälkeen, kun vastaavat myyntilaskut on kirjattu.
* Myy nimikkeitä, joita toimittaja toimittaa suoraan asiakkaalle. Tätä kutsutaan suoratoimitukseksi. Lisätietoja on kohdassa [Tee suoratoimituksia](sales-how-drop-shipment.md).  

Kaikissa muissa tapauksissa myyntitilaukset ja myyntilaskut toimivat samalla tavalla. Lue lisätietoja myyntitilausten käyttämisestä kohdasta [Tuotteiden myyminen](sales-how-sell-products.md).

Voit neuvotella asiakkaan kanssa luomalla ensin myyntitarjouksen, jonka voit muuntaa myyntilaskuksi, kun hyväksyt myynnin. Lue lisätietoja kohdasta [Myyntitarjousten tekeminen](sales-how-make-offers.md).

## <a name="create-sales-invoices"></a><a name="create-sales-invoices"></a>Luo myyntilaskut

Jos asiakas päättää tehdä oston, luo liittyvä määrä- ja arvotapahtuma kirjaamalla myyntilasku. Kun kirjaat myyntilaskun, voit myös lähettää sen PDF-liitteenä sähköpostitse. Voit täyttää sähköpostin tekstiosan yhteenvedolla lasku- ja maksutiedoista. Tietoihin voi kuulua esimerkiksi PayPal-linkki. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostilla](ui-how-send-documents-email.md). Kun asiakas maksaa laskun, voit rekisteröidä maksun eri tavoilla organisaation koosta ja ensisijaisista työnkuluista riippuen. Lisätietoja on kohdassa [Rekisteröintimaksut](#registering-payments).  

Nimikkeen kortin tyyppi voi olla **Varasto**, **palvelu** tai **Muu kuin varasto**. Se määrittää, onko nimike fyysisen varasto yksikkö, työn aikayksikkö vai fyysinen yksikkö, jota ei vastaavasti säilytetä varastossa. Lisätietoja on kohdassa [Uusien nimikkeiden rekisteröinti](inventory-how-register-new-items.md). Myyntilaskuprosessi on sama kaikille kolmelle nimiketyypeille.

Voit täyttää myyntilaskun asiakkaan kentät kahdella tavalla sen mukaan, onko asiakas jo rekisteröity. Katso vaihe 2 seuraavassa menettelyssä.

### <a name="to-create-a-sales-invoice"></a><a name="to-create-a-sales-invoice"></a>Myyntilaskujen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut**, valitse sitten vastaava linkki.  
2. Syötä **Asiakas**-kenttään nykyisen asiakkaan nimi. Jos asiakas kuitenkin on uusi eikä ole rekisteröitynyt, täytä asiakastiedot **myyntilasku**-sivulla seuraavien ohjeiden mukaan:

    1. Syötä **Asiakkaan nimi** -kenttään uuden asiakkaan nimi.
    2. Valitse uuden asiakkaan rekisteröimisen valintaikkunassa **Kyllä**.
    3. Valitse **Valitse uuden asiakkaan malli** -sivulla malli uuden asiakkaan kortin perusteella ja valitse sitten **OK**.
    4. Uuden asiakkaan kortissa näkyy valitun asiakasmallin tiedot. Täytä jäljellä olevat kentät. Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).  
    5. Kun olet määrittänyt asiakaskortin, valitse **Sulje** palataksesi **Myyntilasku**-sivulle.

   Myyntilaskun useat kentät täytetään nyt tiedoilla, jotka olet määrittänyt uuden asiakkaan kortissa.  
3. Täytä tarvittaessa jäljellä olevat kentät **Myyntilasku**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Jos asiakas maksaa heti, esimerkiksi käteisellä tai PayPal-maksuna, täytä **Maksutavan koodi** -kenttä. Maksu kirjataan sitten heti, kun kirjaat myyntilaskun. Jos valitset *käteismaksun*, maksu kirjataan määritetylle vastatilille.

    Voit nyt täyttää **Rivit**-pikavälilehden tuotteilla, joita myyt asiakkaalle, tai mitä tahansa asiakkaan kanssa tapahtuvaa tapahtumaa varten, jonka haluat kirjata pääkirjanpitotilille.

4. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä sen tuotteen, kulun tai tapahtuman tyyppi, jonka kirjaat myyntirivin asiakkaalle.
   * Jos olet määrittänyt toistuvien myyntien rivin asiakkaalle, kuten kuukausittainen täydennystilaus, voit näyttää sen järjestyksessä valitsemalla **Nouda toistuvat myyntirivit** -toiminnon.
5. Valitse **Nro**-kenttään kirjattava tietue **Tyyppi**-kentän arvon mukaan.

    Jätä **Nro**-kenttä tyhjäksi seuraavissa tapauksissa:

    * Jos rivi on tarkoitettu kommentille. Kirjoita kommentti **Kuvaus**-kenttään.
    * Jos rivi on tarkoitettu luettelonimikkeelle. Valitse **Valitse luettelonimikkeet** -toiminto. Lisätietoja on kohdassa [Luettelonimikkeiden muokkaaminen](inventory-how-work-nonstock-items.md).

6. Ilmoita **Määrä**-kentässä, kuinka monta tuote-, kulu- tai tapahtumayksikköä rivi kirjaa asiakkaalle.  

    > [!NOTE]  
    > Jos nimikkeen tyyppi on **Palvelu**-tyyppi tai **Tyyppi**-kentässä on **Resurssi**, määrä on sitten aikayksikkö, esimerkiksi tunnit, kuten rivin **Mittayksikkökoodi**-kenttä osoittaa. Lue lisätietoja on kohdassa [Nimikkeen mittayksiköiden määrittäminen](inventory-how-setup-units-of-measure.md)

    **Rivisumma**-kentän arvo lasketaan *Yksikköhinta* × *Määrä*.  

    Hinta ja rivin summat ilmaistaan ALV:n kanssa tai ilman sitä sen mukaan, mitä valitsit **Hinnat sisältävät verot** -kenttään asiakkaan kortissa.  
7. Jos haluat antaa alennuksen, anna prosentti **Rivialennus-%**-kentässä. **Rivisumma**-kentän arvo päivittyy vastaavasti.  

    Jos nimikkeiden erikoishinnat on määritetty asiakkaan tai nimikkeen kortin **Myyntihinnat ja myyntirivien alennukset**-pikavälilehdellä, myyntiriviin hinta ja summa päivittyvät automaattisesti, jos sovitut hinnan ehdot täyttyvät. Lue lisätietoja kohdasta [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Toista vaiheet 4–7 jokaiselle tuotteelle tai kululle, jonka haluat laskuttaa asiakkaalta.

    Rivien alla olevat summakentät päivitetään automaattisesti aina, kun luot tai muokkaat rivejä ja näytät summat, jotka kirjataan päiväkirjoihin.

    > [!NOTE]
    > Hyvin harvoin kirjatut summat ovat erilaisia kuin summakenttien summat. Tämä johtuu yleensä arvonlisäveroon liittyvistä pyöristyslaskelmista.<br /><br />Voit tarkistaa kirjattavat summat käyttämällä **Tilastot**-sivua. Sivulla otetaan huomioon pyöristyslaskelmat. Jos valitset **Vapauta**-toiminnon, summakentät päivitetään niin, että ne sisältävät pyöristyslaskelmat.
9. Syötä **Laskun alennussumma ilman veroja** -kenttään summa, joka vähennetään **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

    Jos asiakkaalle on määritetty laskualennukset, määritetty prosenttiluvun arvo lisätään automaattisesti **Asiakkaan laskun alennus-%** -kenttään, jos alennusehdot täyttyvät. Liittyvä summa lisätään **Laskun alennussumma ilman ALV:a** -kenttään. Lue lisätietoja kohdasta [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).

10. Kun myyntilaskun rivit ovat valmiit, valitse **Kirjaa ja lähetä** -toiminto.  

Asiakkaan ensisijainen asiakirjojen vastaanottomenetelmä näkyy **Kirjaa ja lähetä vahvistus** -valintaikkunassa. Voit muuttaa lähetysmenetelmän valitsemalla **Lähetä asiakirja kohteeseen** -kentän valintapainikkeen. Lue lisätietoja kohdasta [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).

Nyt järjestelmässä luodaan liittyvä nimike ja asiakastapahtumat. Myyntilasku tulostetaan PDF-asiakirjana. Myyntilasku poistetaan myyntilaskujen luettelosta ja korvataan uudella asiakirjalla kirjattujen myyntilaskujen luettelosta.  

### <a name="calculating-invoice-discounts-on-sales"></a><a name="calculating-invoice-discounts-on-sales"></a>Myynnin laskualennusten laskenta

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="posted-invoices"></a><a name="posted-invoices"></a>Kirjatut laskut

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Voit helposti korjata tai peruuttaa kirjatun myyntilaskun ennen kuin se on maksettu. Tästä on hyötyä, jos haluat korjata kirjoitusvirheen tai jos asiakas pyytää muutosta prosessin alkuvaiheessa. Lisätietoja kohdassa [Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](sales-how-correct-cancel-sales-invoice.md). Jos kirjattu myyntilasku maksetaan, sinun on luotava myyntihyvityslasku kaupan peruuttamiseksi. Lisätietoja kohdassa [Myyntipalautusten tai peruutusten käsittely](sales-how-process-sales-returns-cancellations.md).  

[Avaa **Kirjatut myyntilaskut** -luettelo](https://businesscentral.dynamics.com/?page=143) [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksessa.

## <a name="registering-payments"></a><a name="registering-payments"></a>Maksujen rekisteröiminen

Voit saada maksun ja rekisteröidä maksun eri tavoilla liiketoimintatarpeistasi riippuen: manuaalisesti, automaattisesti tai maksupalveluiden avulla.  

Voit käsitellä maksut suoraan asiakkaan kortista. Hae asiakkaan maksamattomien laskujen yleiskatsaus **Rekisteröi asiakkaan maksut** -toiminnolla. Merkitse sitten lasku osittain tai kokonaan maksetuksi. Tämä maksun täsmäytys käsittelee asiakkaan maksut kohdistamalla pankkitilille vastaanotetut summat niihin liittyviin maksamattomiin myyntilaskuihin ja kirjaamalla maksut sen jälkeen. Lue lisätietoja [Maksujen täsmäyttäminen yksitellen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually) -osassa.  

Yritysympäristöissä, joissa asiakas maksaa jonkin aikaa toimituksen jälkeen maksuehtojen mukaisesti, kirjattu myyntilaskun pysyy avoimena (maksamattomana), kunnees myyntireskontraosasto vahvistaa, että maksu on vastaanotettu ja kohdistaa sen kirjattuun myyntilaskuun. Tämä voidaan tehdä manuaalisesti tai automaattisesti. Lue lisätietoja on kohdissa [Asiakkaan maksujen täsmäyttäminen kassapäiväkirjan avulla tai asiakastapahtumista](receivables-how-apply-sales-transactions-manually.md) ja [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).  

Yritysympäristöissä, joissa asiakas maksaa heti (esimerkiksi PayPal-maksuna tai käteisenä) maksu kirjataan heti, kun kirjaat myyntilaskun. Toisin sanoen kirjattu myyntilaskun suljetaan kokonaan kohdistettuna. Valitset myyntitilauksen **Maksutavan koodi** -kentässä asianmukaisen koodin. Elektronisissa maksuissa, kuten PayPal-maksuissa, sinun täytyy myös täyttää **Maksupalvelu**-kenttä. Lue lisätietoa kohdasta [Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta](sales-how-enable-payment-service-extensions.md).

Voit luoda jopa suoraan maksettavia laskuja rekisteröimättömille asiakkaille, kun määrität heille käteisasiakaskortin, jossa viitataan myyntilaskuun. Lisätietoja kohdassa [Käteisasiakkaiden määrittäminen](finance-how-to-set-up-cash-customers.md).  

> [!TIP]
> Jos haluat lähettää asiakkaille muistutuksia erääntyneistä maksuista, sinun täytyy määrittää ensin muistutustasot ja -ehdot. Lue lisätietoja kohdasta [Muistutusehtojen ja -tasojen määrittäminen](finance-setup-reminders.md).  

## <a name="external-document-numbers"></a><a name="external-document-numbers"></a>Ulkoisen tiedoston numerot

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/invoicing-customers-dynamics-365-business-central/index).

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Tulosta poimintaluettelo](sales-how-print-picking-list.md)  
[Varasto](inventory-manage-inventory.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Avointen saldojen perintä](receivables-collect-outstanding-balances.md)  
[Joukkolaskutus Business Centralin Microsoft Bookingsista ](finance-bookings.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
