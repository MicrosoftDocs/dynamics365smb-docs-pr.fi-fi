---
title: Asiakkaan myyntitilauksen luominen ja tuotteiden myyminen
description: Tässä ohjeaiheessa kerrotaan, miten luodaan myyntitilaus kirjaamaan asiakkaan kanssa tehty sopimus tuotteiden myynnistä tai kaupasta tietyin ehdoin.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, partial deliveries, customer sales order, shipping advice, partial shipments,
ms.search.form: 42, 48, 9305
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: 7d3363557e469344c1648c52b08393efc0f2dc69
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9535824"
---
# <a name="sell-products-with-a-customer-sales-order"></a>Tuotteiden myyminen asiakkaan myyntitilauksen avulla

Tämä artikkeli antaa ohjeita siitä, milloin sinun tulee käyttää asiakkaan myyntitilausta laskun lisäksi. Jos myyntiprosessi edellyttää, että lähetät vain osan tilauksesta, ehkä siksi, että koko määrä ei ole heti saatavilla, sinun on käsiteltävä kyseinen myynti tekemällä myyntitilaus.

Sinun on käytettävä myyntitilauksia myös, jos myyt tuotteita, jotka toimitetaan suoraan toimittajaltasi asiakkaallesi, niin sanotussa suoratoimituksessa. Lisätietoja on kohdassa [Tee suoratoimituksia](sales-how-drop-shipment.md). Kaikilta muilta osin myyntitilaukset toimivat samalla tavalla kuin myyntilaskut. Lisätietoja on kohdassa [Laskutus myynnissä](sales-how-invoice-sales.md).

Kun toimitat tuotteita kokonaan tai osittain, kirjaa myyntitilaus toimitetuksi tai toimitetuksi ja laskutetuksi. Näin järjestelmään luodaan liittyvä nimike ja asiakastapahtumat. Kun kirjaat myyntitilauksen, voit myös lähettää sen PDF-liitteenä sähköpostitse. Sähköpostin perusteksti voidaan esitäyttää tilauksen ja maksun tietojen yhteenvedolla. Tietoihin voi kuulua esimerkiksi PayPal-linkki. Lisätietoja on kohdassa [Nimikkeiden lähettäminen](warehouse-how-ship-items.md) ja [Asiakirjojen lähettäminen sähköpostilla](ui-how-send-documents-email.md).

Yritysympäristöissä, joissa asiakas maksaa heti (esimerkiksi PayPal-maksuna tai käteisenä) maksu kirjataan heti, kun kirjaat myyntitilauksen laskutettuna. Toisin sanoen kirjattu myyntilasku suljetaan kokonaan kohdistettuna. Valitset myyntitilauksen **Maksutavan koodi** -kentässä asianmukaisen koodin. Lisätietoja on alla vaiheessa 5. Elektronisissa maksuissa, kuten PayPal-maksuissa, sinun täytyy myös täyttää **Maksupalvelu**-kenttä. Lue lisätietoa kohdasta [Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta](sales-how-enable-payment-service-extensions.md).

Voit luoda jopa suoraan maksettavia tilauksia rekisteröimättömille asiakkaille, kun määrität ensin käteisasiakaskortin, jossa viitataan myyntitilaukseen. Lisätietoja kohdassa [Käteisasiakkaiden määrittäminen](finance-how-to-set-up-cash-customers.md).

## <a name="create-a-sales-order"></a>Luo myyntitilaus

> [!NOTE]  
> Seuraavassa oletetaan, että asiakas on jo määritetty. Lisätietoja tämän tekemisestä on kohdassa [Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset**, valitse sitten vastaava linkki.
2. Luo uusi merkintä valitsemalla **Uusi**.
3. Syötä **Asiakas**-kenttään nykyisen asiakkaan nimi.

    Muut **Myyntitilaus**-sivun kentät täytetään nyt valitun asiakkaan vakiotiedoilla.  

4. Täytä tarvittaessa jäljellä olevat kentät **Myyntitilaus**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Jos asiakas maksaa heti, esimerkiksi luottokortilla tai PayPal-maksuna, täytä **Maksutavan koodi** -kenttä. Maksu kirjataan sitten heti, kun kirjaat myyntitilauksen laskutettuna. Jos valitset *käteismaksun*, maksu kirjataan määritetylle vastatilille.

    Voit nyt täyttää myyntitilausrivit varastonimikkeillä tai palveluilla, joita haluat asiakkaan ostavan.

    Jos olet määrittänyt toistuvien myyntien rivin asiakkaalle, kuten kuukausittainen täydennystilaus, voit lisätä nämä rivit tilaukseen valitsemalla **Nouda toistuvat myyntirivit** -toiminto.
5. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä sen tuotteen, kulun tai tapahtuman tyyppi, jonka kirjaat asiakkaalle myyntirivillä.

6. Valitse **Nro**-kenttään varastonimikkeen tai palvelun numero.

    Jätä **Nro** -kenttä tyhjäksi, jos rivi on tarkoitettu:

    * Kommentti. Kirjoita kommentti **Kuvaus**-kenttään.
    * Luettelonimike. Valitse **Valitse luettelonimikkeet** -toiminto. Lisätietoja on kohdassa [Luettelonimikkeiden muokkaaminen](inventory-how-work-nonstock-items.md).
7. Syötä myytävien nimikkeiden lukumäärä **Määrä**-kenttään.

    > [!NOTE]  
    > Kun nimikkeen tyyppi on *Resurssi* tai *Huolto*, sen määrä on aikayksikkö, kuten tunnit, rivin **Mittayksikkökoodi**-kentän mukaan. Lue lisätietoja on kohdassa [Nimikkeen mittayksiköiden määrittäminen](inventory-how-setup-units-of-measure.md).

    **Rivisumma**-kenttä päivitetään näyttämään arvoa, joka saadaan kertomalla **Yksikköhinta**-kentän numerolla **Määrä**-kentän arvolla.

    Hinta ja rivin summat näytetään ALV:n kanssa tai ilman riippuen siitä, mitä valitsit **Hinnat verojen kanssa** -kenttään asiakkaan kortissa.
8. Syötä **Rivialennus-%**-kenttään prosentti, jos haluat myöntää asiakkaalle alennuksen tuotteesta. Sama arvo päivitetään **Rivisumma**-kenttään.

    Jos olet määrittänyt asiakkaan tai nimikkeen kortin **Myyntihinnat ja myyntirivien alennukset**-pikavälilehdellä erityisiä nimikehintoja, rivialennusprosentti, hinta ja summa päivitetään automaattisesti tarjousrivillä, jos sovitut hinnan ehdot täyttyvät. Lue lisätietoja kohdasta [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).
9. Voit lisätä tilausriviä koskevan huomautuksen, jonka asiakas näkee tulostetussa myyntitilauksessa, kirjoittamalla kommentin tyhjälle riville **Kuvaus**-kentässä.  
10. Toista vaiheet 5–9 jokaiselle nimikkeelle, jonka haluat asiakkaan osatavan.

    Rivien alla olevat summakentät päivitetään automaattisesti aina, kun luot tai muokkaat rivejä ja näytät summat, jotka kirjataan päiväkirjoihin.

    > [!NOTE]
    > Hyvin harvoin kirjatut summat ovat erilaisia kuin summakenttien summat. Tämä johtuu yleensä arvonlisäveroon (ALV) liittyvistä pyöristyslaskelmista.
    >
    > Voit tarkistaa kirjattavat summat käyttämällä **Tilastotiedot**-sivua. Sivulla otetaan huomioon pyöristyslaskelmat. Jos valitset **Vapauta**-toiminnon, summakentät päivitetään niin, että ne sisältävät pyöristyslaskelmat.  

11. Valinnaisesti voit syöttää **Laskun alennussumma** -kenttään summan, joka vähennetään **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

    Jos asiakkaalle on määritetty laskualennukset, määritetty prosenttiluvun arvo lisätään automaattisesti **Asiakkaan laskun alennus-%** -kenttään, jos ehdot täyttyvät. Liittyvä summa lisätään **Laskun alennussumma ilman ALV:a** -kenttään. Lue lisätietoja kohdasta [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).
12. Jos haluat toimittaa osan tilausmäärästä, syötä määrä **Toimitettava määrä** -kenttään. Arvo kopioidaan automaattisesti **Laskutettava määrä** -kenttään.

    > [!NOTE]
    > Jos **toimitusohje**-kentän arvo on **valmis** **Toimitus ja laskutus** -pikavälilehdessä, osittaisia toimituksia ei voi kirjata. Lisätietoja on kohdassa [Osittaisten toimitusten käsitteleminen](sales-how-send-partial-shipments.md).
13. Jos haluat laskuttaa osan toimitettavasta määrästä, syötä kyseinen määrä **Laskutettava määrä** -kenttään. Määrän on oltava pienempi kuin **Toimitettava määrä** -kentän arvo.  
14. Kun myyntitilausrivit ovat valmiit, valitse **Kirjaa ja lähetä** -toiminto.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Asiakkaan ensisijainen asiakirjojen vastaanottomenetelmä näkyy **Kirjaa ja lähetä vahvistus** -valintaikkunassa. Voit muuttaa lähetysmenetelmän valitsemalla **Lähetä asiakirja kohteeseen** -kentän valintapainikkeen. Lue lisätietoja kohdasta [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).

Nyt järjestelmässä luodaan liittyvä nimike ja asiakastapahtumat. Myyntitilaus tulostetaan PDF-asiakirjana. Kun myyntitilaus on kirjattu kokonaan, se poistetaan myyntitilausluettelosta ja korvataan uusilla kirjattujen myyntilaskujen luettelon ja kirjattujen myyntitoimitusten luettelon asiakirjoilla.  

## <a name="external-document-number"></a>Ulkoisen tiedoston numero

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/create-sales-documents-dynamics-365-business-central/).

## <a name="see-also"></a>Katso myös

[Myynnin laskutus](sales-how-invoice-sales.md)  
[Myynnin kirjaaminen](ui-post-sales.md)  
[Nimikkeiden lähettäminen](warehouse-how-ship-items.md)  
[Suoratoimitusten tekeminen](sales-how-drop-shipment.md)  
[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Tulosta poimintaluettelo](sales-how-print-picking-list.md)  
[Osittaisten toimitusten prosessointi](sales-how-send-partial-shipments.md)  
[Varasto](inventory-manage-inventory.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
