---
title: Myyntilaskun tai myyntitilauksen luominen | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten luodaan kauppakirja tai myyntilasku tai myyntitilaus kirjaamaan asiakkaan kanssa tehty sopimus tuotteiden myynnistä tietyin ehdoin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.date: 08/19/2019
ms.author: sgroespe
ms.openlocfilehash: 53f2356299bfa21efda3ec4c98dacfca68539dea
ms.sourcegitcommit: 81b6062194bf04d8052a3cd394cc0b41e3f53e6d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/20/2019
ms.locfileid: "1887597"
---
# <a name="invoice-sales"></a>Myynnin laskutus
Luo myyntilasku tai -tilaus tallentaaksesi sopimuksesi asiakkaan kanssa ja myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla.  

Myyntitilausta on käytettävä muutamissa skenaarioissa myyntilaskun sijaan:  

* Jos tilauksesta on toimitettava vain osa, koska esimerkiksi tilauksen koko määrä ei ole varastossa.  
* Jos myyt nimikkeitä, joita toimittaja toimittaa suoraan asiakkaalle. Tätä kutsutaan suoratoimitukseksi. Lisätietoja on kohdassa [Suoratoimitusten tekeminen](sales-how-drop-shipment.md).  

Kaikilta muilta osin myyntitilaukset ja myyntilaskut toimivat samalla tavalla. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).

Voit neuvotella asiakkaan kanssa luomalla ensin myyntitarjoukseen, jonka voit muuntaa myyntilaskuksi, kun hyväksyt myynnin. Lisätietoja on kohdassa [Myyntitarjousten tekeminen](sales-how-make-offers.md).

Jos asiakas päättää tehdä oston, luo liittyvä määrä- ja arvotapahtuma kirjaamalla myyntilasku. Kun kirjaat myyntilaskun, voit myös lähettää asiakirjan PDF-liitteenä sähköpostitse. Sähköpostin perusteksti voidaan esitäyttää laskun ja maksun tietojen yhteenvedolla. Tietoihin voi kuulua esimerkiksi PayPal-linkki. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md). Kun asiakas maksaa laskun, voit rekisteröidä maksun eri tavoilla organisaation koosta ja ensisijaisista työnkuluista riippuen. Lisätietoja on [Maksujen rekisteröiminen](#registering-payments) -osassa.  


Voit helposti korjata tai peruuttaa kirjatun myyntilaskun ennen kuin se on maksettu. Tästä on hyötyä esimerkiksi, jos haluat korjata kirjoitusvirheen tai jos asiakas pyytää muutosta prosessin alkuvaiheessa. Lisätietoja on kohdassa [Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](sales-how-correct-cancel-sales-invoice.md). Jos kirjattu myyntilasku maksetaan, sinun on luotava myyntihyvityslasku kaupan peruuttamiseksi. Lisätietoja on kohdassa [Myyntipalautusten tai -peruutusten käsitteleminen](sales-how-process-sales-returns-cancellations.md).

Nimikkeen kortin tyyppi voi olla **Varasto**, **Huolto** ja **Muu kuin huolto**. Se määrittää, onko nimike fyysisen varasto yksikkö, työn aikayksikkö vai fyysinen yksikkö, jota ei säilytetä varastossa. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md). Myyntilaskuprosessi on sama kaikille kolmelle nimiketyypeille.

Voit täyttää myyntilaskun asiakkaan kentät kahdella tavalla sen mukaan, onko asiakas jo rekisteröity. Katso vaiheet 2 ja 3 seuraavassa menettelyssä.

## <a name="to-create-a-sales-invoice"></a>Myyntilaskujen luominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut** ja valitse sitten liittyvä linkki.  
2. Syötä **Asiakas**-kenttään nykyisen asiakkaan nimi.

   Muut **Myyntilasku**-sivun kentät sisältävät vakiotietoja valitusta asiakkaasta. Jos asiakasta ei ole rekisteröity, toimi seuraavasti:
3. Syötä **Asiakas**-kenttään uuden asiakkaan nimi.
4. Valitse uuden asiakkaan rekisteröimisen valintaikkunassa **Kyllä**-painike.
5. Valitse **Valitse uuden asiakkaan malli** -sivulla malli uuden asiakkaan kortin perusteella ja valitse sitten **OK**-painike.
6. Uuden asiakkaan kortissa näkyy valitun asiakasmallin tiedot. Täytä jäljellä olevat kentät. Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).  
7. Kun olet määrittänyt asiakaskortin, valitse **OK**-painike palataksesi **Myyntilasku**-sivulle.

   Myyntilaskun useat kentät täytetään nyt tiedoilla, jotka olet määrittänyt uuden asiakkaan kortissa.  
8. Täytä tarvittaessa jäljellä olevat kentät **Myyntilasku**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Jos asiakas maksaa heti, esimerkiksi käteisellä tai PayPal-maksuna, täytä **Maksutavan koodi** -kenttä. Maksu kirjataan sitten heti, kun kirjaat myyntilaskun. Jos valitset käteismaksun, maksu kirjataan määritetylle vastatilille.

    Voit nyt täyttää asiakkaille myytävien tuotteiden tai KP-tilille kirjattavan asiakastapahtuman myyntilaskun rivit.   

    Jos olet määrittänyt toistuvien myyntien rivin asiakkaalle, kuten kuukausittainen täydennystilaus, voit lisätä nämä rivit tilaukseen valitsemalla **Nouda toistuvat myyntirivit** -toiminto.  
9. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä sen tuotteen, kulun tai tapahtuman tyyppi, jonka kirjaat myyntirivin asiakkaalle.
10. Valitse **Nro**-kenttään kirjattava tietue **Tyyppi**-kentän arvon mukaan.

    Jätä **Nro**-kenttä tyhjäksi seuraavissa tapauksissa:

    * Jos rivi on tarkoitettu kommentille. Kirjoita kommentti **Kuvaus**-kenttään.
    * Jos rivi on tarkoitettu luettelonimikkeelle. Valitse **Valitse luettelonimikkeet** -toiminto. Lisätietoja on kohdassa [Luettelonimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md).

11. Ilmoita **Määrä**-kentässä, kuinka monta tuote-, kulu- tai tapahtumayksikköä rivi kirjaa asiakkaalle.  

    > [!NOTE]  
    >   Jos nimikkeen tyyppi on **Palvelu** tai **Tyyppi**-kentässä on **Resurssi**, määrä on sitten aikayksikkö, esimerkiksi tunnit, kuten rivin **Mittayksikkökoodi**-kenttä osoittaa.  

    **Rivisumma**-kentän arvo lasketaan *Yksikköhinta* x *Määrä*.  

    Hinta ja rivin summat ilmaistaan ALV:n kanssa tai ilman sitä sen mukaan, mitä valitsit **Hinnat sisältävät verot** -kenttään asiakkaan kortissa.  
12. Jos haluat antaa alennuksen, anna prosentti **Rivialennus-%**-kentässä. **Rivisumma**-kentän arvo päivittyy vastaavasti.  

    Jos nimikkeiden erikoishinnat on määritetty asiakkaan tai nimikkeen kortin **Myyntihinnat ja myyntirivien alennukset**-pikavälilehdellä, myyntiriviin hinta ja summa päivittyvät automaattisesti, jos sovitut hinnan ehdot täyttyvät. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Toista vaiheet 9–12 jokaiselle tuotteelle tai kululle, jonka haluat laskuttaa asiakkaalta.  

    Rivien alla olevat summakentät päivitetään automaattisesti aina, kun luot tai muokkaat rivejä ja näytät summat, jotka kirjataan päiväkirjoihin.

    > [!NOTE]
    > Hyvin harvoin kirjatut summat ovat erilaisia kuin summakenttien summat. Tämä johtuu yleensä arvonlisäveroon liittyvistä pyöristyslaskelmista.<br /><br />Voit tarkistaa kirjattavat summat käyttämällä **Tilastot**-sivua. Sivulla otetaan huomioon pyöristyslaskelmat. Jos valitset **Vapauta**-toiminnon, summakentät päivitetään niin, että ne sisältävät pyöristyslaskelmat.
14. Syötä **Laskun alennussumma** -kenttään summa, joka vähennetään **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

    Jos asiakkaalle on määritetty laskualennukset, määritetty prosenttiluvun arvo lisätään automaattisesti **Asiakkaan laskun alennus-%** -kenttään, jos ehdot täyttyvät. Liittyvä summa lisätään **Laskun alennussumma ilman ALV:a** -kenttään. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).  
15. Kun myyntilaskun rivit ovat valmiit, valitse **Kirjaa ja lähetä** -toiminto.  

Asiakkaan ensisijainen asiakirjojen vastaanottomenetelmä näkyy **Kirjaa ja lähetä vahvistus** -valintaikkunassa. Voit muuttaa lähetysmenetelmän valitsemalla **Lähetä asiakirja kohteeseen** -kentän valintapainikkeen. Lisätietoja on kohdassa [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).

Nyt järjestelmässä luodaan liittyvä nimike ja asiakastapahtumat. Myyntilasku tulostetaan PDF-asiakirjana. Myyntilasku poistetaan myyntilaskujen luettelosta ja korvataan uudella asiakirjalla kirjattujen myyntilaskujen luettelosta.  

## <a name="registering-payments"></a>Maksujen rekisteröiminen

Voit saada maksun ja rekisteröidä maksun eri tavoilla liiketoimintatarpeistasi riippuen: manuaalisesti, automaattisesti tai maksupalveluiden avulla.  

Voit käsitellä maksut suoraan asiakkaan kortista. Hae asiakkaan maksamattomien laskujen yleiskatsaus **Rekisteröi asiakkaan maksut** -toiminnolla. Merkitse sitten lasku osittain tai kokonaan maksetuksi. Tämä maksun täsmäytys käsittelee asiakkaan maksut kohdistamalla pankkitilille vastaanotetut summat niihin liittyviin maksamattomiin myyntilaskuihin ja kirjaamalla maksut sen jälkeen. Lisätietoja on kohdassa [Maksujen täsmäyttäminen yksitellen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

Yritysympäristöissä, joissa asiakas maksaa jonkin aikaa toimituksen jälkeen maksuehtojen mukaisesti, kirjattu myyntilaskun pysyy avoimena (maksamattomana), kunnees myyntireskontraosasto vahvistaa, että maksu on vastaanotettu ja kohdistaa maksun kirjattuun myyntilaskuun. Tämä voidaan tehdä manuaalisesti tai automaattisesti. Lisätietoja on kohdissa [Asiakkaan maksujen täsmäyttäminen kassapäiväkirjan avulla tai asiakastapahtumista](receivables-how-apply-sales-transactions-manually.md) ja [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).  

Yritysympäristöissä, joissa asiakas maksaa heti (esimerkiksi PayPal-maksuna tai käteisenä) maksu kirjataan heti, kun kirjaat myyntilaskun. Toisin sanoen kirjattu myyntilaskun suljetaan kokonaan kohdistettuna. Valitset myyntitilauksen **Maksutavan koodi** -kentässä asianmukaisen koodin. Katso vaihe 8. Elektronisissa maksuissa, kuten PayPal-maksuissa, sinun täytyy myös täyttää **Maksupalvelu**-kenttä. Lisätietoja on kohdassa [Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta](sales-how-enable-payment-service-extensions.md).  

Voit luoda jopa suoraan maksettavia laskuja rekisteröimättömille asiakkaille, kun määrität ensin käteisasiakaskortin, jossa viitataan myyntilaskuun. Lisätietoja on ohjeaiheessa [Käteisasiakkaiden määrittäminen](finance-how-to-set-up-cash-customers.md).  

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Joukkolaskutus Business Centralin Microsoft Bookingsista ](finance-bookings.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
