---
title: Myyntitilauksen luonti ja tuotteiden myynti | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten luodaan myyntitilaus kirjaamaan asiakkaan kanssa tehty sopimus tuotteiden myynnistä tai kaupasta tietyin ehdoin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a8e2d016cc47192bbb05439fa61bab1f246a53bd
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "924730"
---
# <a name="sell-products"></a>Tuotteiden myyminen
Luo myyntitilaus tai -lasku tallentaaksesi sopimuksesi asiakkaan kanssa ja myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla.

> [!NOTE]  
>   Myyntitilauksia käytetään, jos myyntiprosessi vaatii tilausmäärän osittaisen toimittamisen esimerkiksi silloin, kun koko määrä ei ole kerralla käytettävissä. Jos myyt nimikkeitä toimittamalla ne suoraan toimittajalta asiakkaalle (suoratoimituksena), myyntitilauksia on käytettävä. Lisätietoja on kohdassa [Suoratoimitusten tekeminen](sales-how-drop-shipment.md). Kaikilta muilta osin myyntitilaukset toimivat samalla tavalla kuin myyntilaskut. Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).

Voit neuvotella asiakkaan kanssa luomalla ensin myyntitarjoukseen, jonka voit muuntaa myyntitilaukseksi, kun hyväksyt myynnin. Lisätietoja on kohdassa [Myyntitarjousten tekeminen](sales-how-make-offers.md).

Sen jälkeen, kun asiakas on vahvistanut sopimuksen, esimerkiksi tarjousprosessin jälkeen, voit lähettää tilausvahvistuksen ja tallentaa velvollisuutesi toimittaa tuotteet sovitun mukaisesti.

Kun toimitat tuotteita kokonaan tai osittain, kirjaa myyntitilaus toimitetuksi tai toimitetuksi ja laskutetuksi. Näin järjestelmään luodaan liittyvä nimike ja asiakastapahtumat. Kun kirjaat myyntitilauksen, voit myös lähettää asiakirjan PDF-liitteenä sähköpostitse. Sähköpostin perusteksti voidaan esitäyttää tilauksen ja maksun tietojen yhteenvedolla. Tietoihin voi kuulua esimerkiksi PayPal-linkki. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md).

Yritysympäristöissä, joissa asiakas maksaa jonkin aikaa toimituksen jälkeen maksuehtojen mukaisesti, kirjattu myyntilaskun pysyy avoimena (maksamattomana), kunnees myyntireskontraosasto vahvistaa, että maksu on vastaanotettu ja kohdistaa maksun kirjattuun myyntilaskuun. Lisätietoja on kohdassa [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

Yritysympäristöissä, joissa asiakas maksaa heti (esimerkiksi PayPal-maksuna tai käteisenä) maksu kirjataan heti, kun kirjaat myyntitilauksen laskutettuna. Toisin sanoen kirjattu myyntilasku suljetaan kokonaan kohdistettuna. Valitset myyntitilauksen **Maksutavan koodi** -kentässä asianmukaisen koodin. Katso vaihe 8. Elektronisissa maksuissa, kuten PayPal-maksuissa, sinun täytyy myös täyttää **Maksupalvelu**-kenttä. Lisätietoja on kohdassa [Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta](sales-how-enable-payment-service-extensions.md).

Voit luoda jopa suoraan maksettavia tilauksia rekisteröimättömille asiakkaille, kun määrität ensin käteisasiakaskortin, jossa viitataan myyntitilaukseen. Lisätietoja on ohjeaiheessa [Käteisasiakkaiden määrittäminen](finance-how-to-set-up-cash-customers.md).

Voit korjata tai peruuttaa myyntitilauksen muodostaman kirjatun myyntilaskun helposti ennen sen maksamista. Tästä on hyötyä, jos haluat korjata kirjoitusvirheen tai jos asiakas pyytää muutosta prosessin alkuvaiheessa. Lisätietoja on kohdassa [Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](sales-how-correct-cancel-sales-invoice.md). Jos kirjattu myyntilasku maksetaan, sinun on luotava myyntihyvityslasku kaupan peruuttamiseksi. Lisätietoja on kohdassa [Myyntipalautusten tai -peruutusten käsitteleminen](sales-how-process-sales-returns-cancellations.md).

Nimikkeen kortin tyyppi voi olla **Varasto**, **Huolto** ja **Muu kuin huolto**. Se määrittää, onko nimike fyysisen varasto yksikkö, työn aikayksikkö vai fyysinen yksikkö, jota ei säilytetä varastossa. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md). Myyntitilausprosessi on sama kaikille kolmelle nimiketyypeille.

Voit täyttää myyntitilauksen asiakkaan kentät kahdella tavalla sen mukaan, onko asiakas jo rekisteröity. Katso vaiheet 2 ja 3 seuraavassa menettelyssä.

## <a name="to-create-a-sales-order"></a>Myyntitilauksen luominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.
2. Syötä **Asiakas**-kenttään nykyisen asiakkaan nimi.

    Muut **Myyntitilaus**-sivun kentät täytetään nyt valitun asiakkaan vakiotiedoilla. Jos asiakasta ei ole rekisteröity, toimi seuraavasti:
3. Syötä **Asiakas**-kenttään uuden asiakkaan nimi.
4. Valitse uuden asiakkaan rekisteröimisen valintaikkunassa **Kyllä**-painike.
5. Valitse **Valitse uuden asiakkaan malli** -sivulla malli uuden asiakkaan kortin perusteella ja valitse sitten **OK**-painike.

    Uuden asiakkaan kortti avautuu esitäytettynä valitun asiakasmallin tiedoilla. **Nimi**-kenttään esitäytetään myyntitilaukseen syöttämäsi uuden asiakkaan nimi.
6. Jatka täyttämällä asiakkaan kortin jäljellä olevat kentät. Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).  
7. Kun olet määrittänyt asiakaskortin, valitse **OK**-painike palataksesi **Myyntitilaus**-sivulle.

    Myyntitilauksen useat kentät täytetään nyt tiedoilla, jotka olet määrittänyt uuden asiakkaan kortissa.
8. Täytä tarvittaessa jäljellä olevat kentät **Myyntitilaus**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Jos asiakas maksaa heti, esimerkiksi luottokortilla tai PayPal-maksuna, täytä **Maksutavan koodi** -kenttä. Maksu kirjataan sitten heti, kun kirjaat myyntitilauksen laskutettuna. Jos valitset käteismaksun, maksu kirjataan määritetylle vastatilille.

    Voit nyt täyttää myyntitilausrivit varastonimikkeillä tai palveluilla, joita haluat myydä asiakkaalle.

    Jos olet määrittänyt toistuvien myyntien rivin asiakkaalle, kuten kuukausittainen täydennystilaus, voit lisätä nämä rivit tilaukseen valitsemalla **Nouda toistuvat myyntirivit** -toiminto.
9. Syötä **Rivit**-pikavälilehden **Nimike**-kenttään varastonimikkeen tai palvelun numero.  
10. Syötä myytävien nimikkeiden lukumäärä **Määrä**-kenttään.

    > [!NOTE]  
    >   Kun nimikkeen tyyppi on Huolto, sen määrä on aikayksikkö, kuten tunnit, rivin **Mittayksikkökoodi**-kentän mukaan.

    **Rivisumma**-kenttä päivitetään näyttämään arvoa, joka saadaan kertomalla **Yksikköhinta**-kentän arvo **Määrä**-kentän arvolla.

    Hinta ja rivin summat näytetään ALV:n kanssa tai ilman riippuen siitä, mitä valitsit **Hinnat verojen kanssa** -kenttään asiakkaan kortissa.
11. Syötä **Rivialennus-%**-kenttään prosentti, jos haluat myöntää asiakkaalle alennuksen tuotteesta. Sama arvo päivitetään **Rivisumma**-kenttään.

    Jos olet määrittänyt asiakkaan tai nimikkeen kortin **Myyntihinnat ja myyntirivien alennukset**-pikavälilehdellä erityisiä nimikehintoja, rivialennusprosentti, hinta ja summa päivitetään automaattisesti tarjousrivillä, jos sovitut hinnan ehdot täyttyvät. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).
12. Voit lisätä tarjousriviä koskevan huomautuksen, jonka asiakas näkee tulostetussa myyntitarjouksessa, kirjoittamalla tekstin **Kuvaus**-kentän tyhjälle riville.  
13. Toista vaiheet 9–12 jokaiselle nimikkeelle, jonka haluat myydä asiakkaalle.

    Rivien kokonaissummat lasketaan automaattisesti samalla, kun rivejä luodaan ja muokataan.
14. Uuden asiakkaan kortissa näkyy valitun asiakasmallin tiedot. Täytä jäljellä olevat kentät. Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).  
15. Kun olet määrittänyt asiakaskortin, valitse **OK**-painike palataksesi **Myyntitilaus**-sivulle.

    Myyntitilauksen useat kentät täytetään nyt tiedoilla, jotka olet määrittänyt uuden asiakkaan kortissa.
16. Täytä tarvittaessa jäljellä olevat kentät **Myyntitilaus**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Voit nyt täyttää asiakkaille myytävien tuotteiden tai KP-tilille kirjattavan asiakastapahtuman myyntitilauksen rivit.   

    Jos olet määrittänyt toistuvien myyntien rivin asiakkaalle, kuten kuukausittainen täydennystilaus, voit lisätä nämä rivit tilaukseen valitsemalla **Nouda toistuvat myyntirivit** -toiminto.  
17. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä sen tuotteen, kulun tai tapahtuman tyyppi, jonka kirjaat myyntirivin asiakkaalle.

18. Valitse **Nro**-kenttään kirjattava tietue **Tyyppi**-kentän arvon mukaan.

    Jätä **Nro**-kenttä tyhjäksi seuraavissa tapauksissa:

    * Jos rivi on tarkoitettu kommentille. Kirjoita kommentti **Kuvaus**-kenttään.
    * Jos rivi on tarkoitettu luettelonimikkeelle. Valitse **Valitse luettelonimikkeet** -toiminto. Lisätietoja on kohdassa [Luettelonimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md).

19. Ilmoita **Määrä**-kentässä, kuinka monta tuote-, kulu- tai tapahtumayksikköä rivi kirjaa asiakkaalle.  

    > [!NOTE]  
    >   Jos nimikkeen tyyppi on **Nimike - Palvelu** tai **Resurssi**, määrä on aikayksikkö, esimerkiksi tunnit, kuten rivin **Mittayksikkökoodi**-kenttä osoittaa. Lisätietoja on kohdassa [Nimikkeen mittayksiköiden määrittäminen](inventory-how-setup-units-of-measure.md).

    **Rivisumma**-kentän arvo lasketaan *Yksikköhinta* x *Määrä*.  

    Hinta ja rivin summat ilmaistaan ALV:n kanssa tai ilman sitä sen mukaan, mitä valitsit **Hinnat sisältävät verot** -kenttään asiakkaan kortissa.  
20. Jos haluat antaa alennuksen, anna prosentti **Rivialennus-%**-kentässä. **Rivisumma**-kentän arvo päivittyy vastaavasti.  

    Jos nimikkeiden erikoishinnat on määritetty asiakkaan tai nimikkeen kortin **Myyntihinnat ja myyntirivien alennukset**-pikavälilehdellä, myyntiriviin hinta ja summa päivittyvät automaattisesti, jos sovitut hinnan ehdot täyttyvät. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).  
21. Toista vaiheet 9–12 jokaiselle tuotteelle tai kululle, jonka haluat myydä asiakkaalle.  

    Rivien kokonaissummat lasketaan automaattisesti samalla, kun rivejä luodaan ja muokataan.  
22. Syötä **Laskun alennussumma** -kenttään summa, joka vähennetään **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

    Jos asiakkaalle on määritetty laskualennukset, määritetty prosenttiluvun arvo lisätään automaattisesti **Asiakkaan laskun alennus-%** -kenttään, jos ehdot täyttyvät. Liittyvä summa lisätään **Laskun alennussumma ilman ALV:a** -kenttään. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).
23. Jos haluat toimittaa osan tilausmäärästä, syötä määrä **Toimitettava määrä** -kenttään. Arvo kopioidaan **Laskutettava määrä** -kenttään.
24. Jos haluat laskuttaa osan toimitettavasta määrästä, syötä kyseinen määrä **Laskutettava määrä** -kenttään. Määrän on oltava pienempi kuin **Toimitettava määrä** -kentän arvo.   
25. Kun myyntitilausrivit ovat valmiit, valitse **Kirjaa ja lähetä** -toiminto.

Asiakkaan ensisijainen asiakirjojen vastaanottomenetelmä näkyy **Kirjaa ja lähetä vahvistus** -valintaikkunassa. Voit muuttaa lähetysmenetelmän valitsemalla **Lähetä asiakirja kohteeseen** -kentän valintapainikkeen. Lisätietoja on kohdassa [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).

Nyt järjestelmässä luodaan liittyvä nimike ja asiakastapahtumat. Myyntitilaus tulostetaan PDF-asiakirjana. Kun myyntitilaus on kirjattu kokonaan, se poistetaan myyntitilausluettelosta ja korvataan uusilla kirjattujen myyntilaskujen luettelon ja kirjattujen myyntitoimitusten luettelon asiakirjoilla.

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
