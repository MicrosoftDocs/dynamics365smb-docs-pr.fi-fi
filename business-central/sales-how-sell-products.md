---
title: Myyntitilauksen luonti ja tuotteiden myynti | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten luodaan myyntitilaus kirjaamaan asiakkaan kanssa tehty sopimus tuotteiden myynnistä tai kaupasta tietyin ehdoin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 19b32e8faa6b9e56505379d1f06fd5ad79466614
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115513"
---
# <a name="sell-products"></a>Tuotteiden myyminen

Luo myyntitilaus tai -lasku tallentaaksesi sopimuksesi asiakkaan kanssa ja myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla.

> [!NOTE]  
> Myyntitilauksia käytetään, jos myyntiprosessi vaatii tilausmäärän osittaisen toimittamisen esimerkiksi silloin, kun koko määrä ei ole kerralla käytettävissä. Jos käytetään myyntilaskuja, [!INCLUDE [prod_short](includes/prod_short.md)] olettaa, että koko määrä toimitetaan, kun lasku kirjataan. Jos myyt nimikkeitä toimittamalla ne suoraan toimittajalta asiakkaalle (suoratoimituksena), myyntitilauksia on käytettävä. Lisätietoja on kohdassa [Suoratoimitusten tekeminen](sales-how-drop-shipment.md). Kaikilta muilta osin myyntitilaukset toimivat samalla tavalla kuin myyntilaskut. Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).

Voit neuvotella asiakkaan kanssa luomalla ensin myyntitarjoukseen, jonka voit muuntaa myyntitilaukseksi, kun hyväksyt myynnin. Lisätietoja on kohdassa [Myyntitarjousten tekeminen](sales-how-make-offers.md).

Sen jälkeen, kun asiakas on vahvistanut sopimuksen, esimerkiksi tarjousprosessin jälkeen, voit lähettää tilausvahvistuksen ja tallentaa velvollisuutesi toimittaa tuotteet sovitun mukaisesti.

Kun toimitat tuotteita kokonaan tai osittain, kirjaa myyntitilaus toimitetuksi tai toimitetuksi ja laskutetuksi. Näin järjestelmään luodaan liittyvä nimike ja asiakastapahtumat. Kun kirjaat myyntitilauksen, voit myös lähettää asiakirjan PDF-liitteenä sähköpostitse. Sähköpostin perusteksti voidaan esitäyttää tilauksen ja maksun tietojen yhteenvedolla. Tietoihin voi kuulua esimerkiksi PayPal-linkki. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md).

Yritysympäristöissä, joissa asiakas maksaa jonkin aikaa toimituksen jälkeen maksuehtojen mukaisesti, kirjattu myyntilaskun pysyy avoimena (maksamattomana), kunnees myyntireskontraosasto vahvistaa, että maksu on vastaanotettu ja kohdistaa maksun kirjattuun myyntilaskuun. Lisätietoja on kohdassa [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

Yritysympäristöissä, joissa asiakas maksaa heti (esimerkiksi PayPal-maksuna tai käteisenä) maksu kirjataan heti, kun kirjaat myyntitilauksen laskutettuna. Toisin sanoen kirjattu myyntilasku suljetaan kokonaan kohdistettuna. Valitset myyntitilauksen **Maksutavan koodi** -kentässä asianmukaisen koodin. Katso vaihe 8. Elektronisissa maksuissa, kuten PayPal-maksuissa, sinun täytyy myös täyttää **Maksupalvelu**-kenttä. Lisätietoja on kohdassa [Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta](sales-how-enable-payment-service-extensions.md).

Voit luoda jopa suoraan maksettavia tilauksia rekisteröimättömille asiakkaille, kun määrität ensin käteisasiakaskortin, jossa viitataan myyntitilaukseen. Lisätietoja on ohjeaiheessa [Käteisasiakkaiden määrittäminen](finance-how-to-set-up-cash-customers.md).

Voit korjata tai peruuttaa myyntitilauksen muodostaman kirjatun myyntilaskun helposti ennen sen maksamista. Tästä on hyötyä, jos haluat korjata kirjoitusvirheen tai jos asiakas pyytää muutosta prosessin alkuvaiheessa. Lisätietoja on kohdassa [Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](sales-how-correct-cancel-sales-invoice.md). Jos kirjattu myyntilasku maksetaan, sinun on luotava myyntihyvityslasku kaupan peruuttamiseksi. Lisätietoja on kohdassa [Myyntipalautusten tai -peruutusten käsitteleminen](sales-how-process-sales-returns-cancellations.md).

Nimikkeen kortin tyyppi voi olla **Varasto**, **Huolto** ja **Muu kuin huolto**. Se määrittää, onko nimike fyysisen varasto yksikkö, työn aikayksikkö vai fyysinen yksikkö, jota ei säilytetä varastossa. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md). Myyntitilausprosessi on sama kaikille kolmelle nimiketyypeille.

Voit täyttää myyntitilauksen asiakkaan kentät kahdella tavalla sen mukaan, onko asiakas jo rekisteröity. Katso vaihe 2 seuraavassa menettelyssä.

## <a name="to-create-a-sales-order"></a>Myyntitilauksen luominen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.
2. Syötä **Asiakas**-kenttään nykyisen asiakkaan nimi.

    Muut **Myyntitilaus**-sivun kentät täytetään nyt valitun asiakkaan vakiotiedoilla.  

    [!INCLUDE [sales-create-customer](includes/sales-create-customer.md)]  

    Myyntitilauksen useat kentät täytetään nyt tiedoilla, jotka olet määrittänyt uuden asiakkaan kortissa.
3. Täytä tarvittaessa jäljellä olevat kentät **Myyntitilaus**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Jos asiakas maksaa heti, esimerkiksi luottokortilla tai PayPal-maksuna, täytä **Maksutavan koodi** -kenttä. Maksu kirjataan sitten heti, kun kirjaat myyntitilauksen laskutettuna. Jos valitset käteismaksun, maksu kirjataan määritetylle vastatilille.

    Voit nyt täyttää myyntitilausrivit varastonimikkeillä tai palveluilla, joita haluat myydä asiakkaalle.

    Jos olet määrittänyt toistuvien myyntien rivin asiakkaalle, kuten kuukausittainen täydennystilaus, voit lisätä nämä rivit tilaukseen valitsemalla **Nouda toistuvat myyntirivit** -toiminto.
4. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä sen tuotteen, kulun tai tapahtuman tyyppi, jonka kirjaat myyntirivin asiakkaalle.

5. Valitse **Nro**-kenttään varastonimikkeen tai palvelun numero.

    Jätä **Nro**-kenttä tyhjäksi seuraavissa tapauksissa:

    * Jos rivi on tarkoitettu kommentille. Kirjoita kommentti **Kuvaus**-kenttään.
    * Jos rivi on tarkoitettu luettelonimikkeelle. Valitse **Valitse luettelonimikkeet** -toiminto. Lisätietoja on kohdassa [Luettelonimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md).
6. Syötä myytävien nimikkeiden lukumäärä **Määrä**-kenttään.

    > [!NOTE]  
    > Kun nimikkeen tyyppi on *Resurssi* tai *Huolto*, sen määrä on aikayksikkö, kuten tunnit, rivin **Mittayksikkökoodi**-kentän mukaan. Lisätietoja on kohdassa [Nimikkeen mittayksiköiden määrittäminen](inventory-how-setup-units-of-measure.md).

    **Rivisumma**-kenttä päivitetään näyttämään arvoa, joka saadaan kertomalla **Yksikköhinta**-kentän arvo **Määrä**-kentän arvolla.

    Hinta ja rivin summat näytetään ALV:n kanssa tai ilman riippuen siitä, mitä valitsit **Hinnat verojen kanssa** -kenttään asiakkaan kortissa.
7. Syötä **Rivialennus-%**-kenttään prosentti, jos haluat myöntää asiakkaalle alennuksen tuotteesta. Sama arvo päivitetään **Rivisumma**-kenttään.

    Jos olet määrittänyt asiakkaan tai nimikkeen kortin **Myyntihinnat ja myyntirivien alennukset**-pikavälilehdellä erityisiä nimikehintoja, rivialennusprosentti, hinta ja summa päivitetään automaattisesti tarjousrivillä, jos sovitut hinnan ehdot täyttyvät. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).
8. Voit lisätä tarjousriviä koskevan huomautuksen, jonka asiakas näkee tulostetussa myyntitarjouksessa, kirjoittamalla tekstin **Kuvaus**-kentän tyhjälle riville.  
9. Toista vaiheet 4–8 jokaiselle nimikkeelle, jonka haluat myydä asiakkaalle.

    Rivien alla olevat summakentät päivitetään automaattisesti aina, kun luot tai muokkaat rivejä ja näytät summat, jotka kirjataan päiväkirjoihin.

    > [!NOTE]
    > Hyvin harvoin kirjatut summat ovat erilaisia kuin summakenttien summat. Tämä johtuu yleensä arvonlisäveroon liittyvistä pyöristyslaskelmista.
    >
    > Voit tarkistaa kirjattavat summat käyttämällä **Tilastotiedot**-sivua. Sivulla otetaan huomioon pyöristyslaskelmat. Jos valitset **Vapauta**-toiminnon, summakentät päivitetään niin, että ne sisältävät pyöristyslaskelmat.  

10. Valinnaisesti voit syöttää **Laskun alennussumma** -kenttään summan, joka vähennetään **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

    Jos asiakkaalle on määritetty laskualennukset, määritetty prosenttiluvun arvo lisätään automaattisesti **Asiakkaan laskun alennus-%** -kenttään, jos ehdot täyttyvät. Liittyvä summa lisätään **Laskun alennussumma ilman ALV:a** -kenttään. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).
11. Jos haluat toimittaa osan tilausmäärästä, syötä määrä **Toimitettava määrä** -kenttään. Arvo kopioidaan **Laskutettava määrä** -kenttään.
12. Jos haluat laskuttaa osan toimitettavasta määrästä, syötä kyseinen määrä **Laskutettava määrä** -kenttään. Määrän on oltava pienempi kuin **Toimitettava määrä** -kentän arvo.  
13. Kun myyntitilausrivit ovat valmiit, valitse **Kirjaa ja lähetä** -toiminto.

Asiakkaan ensisijainen asiakirjojen vastaanottomenetelmä näkyy **Kirjaa ja lähetä vahvistus** -valintaikkunassa. Voit muuttaa lähetysmenetelmän valitsemalla **Lähetä asiakirja kohteeseen** -kentän valintapainikkeen. Lisätietoja on kohdassa [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).

Nyt järjestelmässä luodaan liittyvä nimike ja asiakastapahtumat. Myyntitilaus tulostetaan PDF-asiakirjana. Kun myyntitilaus on kirjattu kokonaan, se poistetaan myyntitilausluettelosta ja korvataan uusilla kirjattujen myyntilaskujen luettelon ja kirjattujen myyntitoimitusten luettelon asiakirjoilla.  

## <a name="external-document-number"></a>Ulkoisen tiedoston numero

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Katso myös

[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Tulosta poimintaluettelo](sales-how-print-picking-list.md)  
[Varasto](inventory-manage-inventory.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]