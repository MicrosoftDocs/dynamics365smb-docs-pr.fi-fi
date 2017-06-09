---
title: 'Toimintaohje: Myynnin laskutus| Microsoft Docs'
description: "Tässä artikkelissa kerrotaan, miten myyntilaskuja käytetään."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e9fbf7b6599c4136a4077f199feb8f2f00d3a959
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-invoice-sales"></a>Toimintaohje: Myynnin laskutus
Luo myyntilasku tai -tilaus tallentaaksesi sopimuksesi asiakkaan kanssa ja myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla.  

**Huomautus:** Myyntitilausta on käytettävä muutamissa skenaarioissa myyntilaskun sijaan:  

* Jos tilauksesta on toimitettava vain osa, koska esimerkiksi tilauksen koko määrä ei ole varastossa.  
* Jos myyt nimikkeitä, joita toimittaja toimittaa suoraan asiakkaalle. Tätä kutsutaan suoratoimitukseksi. Lisätietoja on kohdassa [Toimintaohje: Suoratoimitusten tekeminen](sales-how-drop-shipment.md).  

Kaikilta muilta osin myyntitilaukset ja myyntilaskut toimivat samalla tavalla. Lisätietoja on kohdassa [Toimintaohje: Tuotteiden myyminen](sales-how-sell-products.md).

Voit neuvotella asiakkaan kanssa luomalla ensin myyntitarjoukseen, jonka voit muuntaa myyntilaskuksi, kun hyväksyt myynnin. Lisätietoja on kohdassa [Toimintaohje: Tarjousten tekeminen](sales-how-make-offers.md).

Jos asiakas päättää tehdä oston, luo liittyvä määrä- ja arvotapahtuma kirjaamalla myyntilasku. Kun kirjaat myyntilaskun, voit myös lähettää asiakirjan PDF-liitteenä sähköpostitse. Sähköpostin perusteksti voidaan esitäyttää laskun ja maksun tietojen yhteenvedolla. Tietoihin voi kuulua esimerkiksi PayPal-linkki. Lisätietoja on kohdassa [Toimintaohje: Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md).

Liiketoimintaympäristöissä, joissa asiakkaan on maksettava ennen kuin tuotteet toimitetaan, kuten vähittäismyynti, sinun on odotettava maksukuittia ennen kuin toimitat tuotteet. Useimmissa tapauksissa saapuvia maksuja käsitellään joitakin viikkoja toimituksen jälkeen kohdistamalla maksut niihin liittyviin kirjattuihin ja maksamattomiin myyntilaskuihin. Lisätietoja on kohdassa [Toimintaohje: Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

Voit helposti korjata tai peruuttaa kirjatun myyntilaskun ennen kuin se on maksettu. Tästä on hyötyä esimerkiksi, jos haluat korjata kirjoitusvirheen tai jos asiakas pyytää muutosta prosessin alkuvaiheessa. Lisätietoja on kohdassa [Toimintaohje: Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](sales-how-correct-cancel-sales-invoice.md). Jos kirjattu myyntilasku maksetaan, sinun on luotava myyntihyvityslasku kaupan peruuttamiseksi. Lisätietoja on kohdassa [Toimintaohje: Myyntipalautusten tai -peruutusten käsitteleminen](sales-how-process-sales-returns-cancellations.md).

Nimikkeet voivat olla sekä varastonimikkeitä että palveluja, ja niiden tyypit ovat myyntiriveillä **Nimike - Varasto** ja **Nimike - Palvelu**. Myyntilaskuprosessi on sama molemmille nimiketyypeille. Lisätietoja on kohdassa [Toimintaohje: Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

Voit täyttää myyntilaskun asiakkaan kentät kahdella tavalla sen mukaan, onko asiakas jo rekisteröity. Katso vaiheet 2 ja 3 seuraavassa menettelyssä.

## <a name="to-create-a-sales-invoice"></a>Myyntilaskujen luominen
1. Valitse kotisivulla **Myyntilasku**-toiminto.  
2. Syötä **Asiakas**-kenttään nykyisen asiakkaan nimi.

   Muut **Myyntilasku**-ikkunan kentät sisältävät vakiotietoja valitusta asiakkaasta. Jos asiakasta ei ole rekisteröity, toimi seuraavasti:
3. Syötä **Asiakas**-kenttään uuden asiakkaan nimi.
4. Valitse uuden asiakkaan rekisteröimisen valintaikkunassa **Kyllä**-painike.
5. Valitse **Valitse uuden asiakkaan malli** -ikkunassa malli uuden asiakkaan kortin perusteella ja valitse sitten **OK**-painike.
6. Uuden asiakkaan kortissa näkyy valitun asiakasmallin tiedot. Täytä jäljellä olevat kentät. Lisätietoja on kohdassa [Toimintaohje: Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md).  
7. Kun olet määrittänyt asiakaskortin, valitse **OK**-painike palataksesi **Myyntilasku**-ikkunaan.

   Myyntilaskun useat kentät täytetään nyt tiedoilla, jotka olet määrittänyt uuden asiakkaan kortissa.  
8. Täytä tarvittaessa jäljellä olevat kentät **Myyntilasku**-ikkunassa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Voit nyt täyttää asiakkaille myytävien tuotteiden tai KP-tilille kirjattavan asiakastapahtuman myyntilaskun rivit.   

Jos olet määrittänyt toistuvien myyntien rivin asiakkaalle, kuten kuukausittainen täydennystilaus, voit lisätä nämä rivit tilaukseen valitsemalla **Nouda toistuvat myyntirivit** -toiminto.  
9. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä sen tuotteen, kulun tai tapahtuman tyyppi, jonka kirjaat myyntirivin asiakkaalle.
10. Valitse **Nro**-kenttään kirjattava tietue **Tyyppi**-kentän arvon mukaan.

 Jätä **Nro**-kenttä tyhjäksi seuraavissa tapauksissa: -Jos rivi on tarkoitettu kommentille. Kirjoita kommentti **Kuvaus**-kenttään.
 -Jos rivi on tarkoitettu ei-varastoitavalle nimikkeelle. Valitse **Valitse ei-varastoitavat nimikkeet** -toiminto. Lisätietoja on kohdassa [Toimintaohje: Ei-varastoitavien nimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md).

11. Ilmoita **Määrä**-kentässä, kuinka monta tuote-, kulu- tai tapahtumayksikkö rivi kirjaa asiakkaalle.  

    **Huomautus:** Jos nimikkeen tyyppi on **Nimike - Palvelu** tai **Resurssi**, määrä on aikayksikkö, esimerkiksi tunnit, kuten rivin **Mittayksikkökoodi**-kenttä osoittaa.  

    **Rivisumma**-kentän arvo lasketaan *Yksikköhinta* x *Määrä*.  

    Hinta ja rivin summat ilmaistaan ALV:n kanssa tai ilman sitä sen mukaan, mitä valitsit **Hinnat sisältävät verot** -kenttään asiakkaan kortissa.  
12. Jos haluat antaa alennuksen, anna prosentti **Rivialennus-%**-kentässä. **Rivisumma**-kentän arvo päivittyy vastaavasti.  

    Jos nimikkeiden erikoishinnat on määritetty asiakkaan tai nimikkeen kortin **Myyntihinnat ja myyntirivien alennukset**-pikavälilehdellä, myyntiriviin hinta ja summa päivittyvät automaattisesti, jos sovitut hinnan ehdot täyttyvät. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Toista vaiheet 9–12 jokaiselle tuotteelle tai kululle, jonka haluat myydä asiakkaalle.  

    Rivien kokonaissummat lasketaan automaattisesti samalla, kun rivejä luodaan ja muokataan.  
14. Syötä **Laskun alennussumma** -kenttään summa, joka vähennetään **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

    Jos asiakkaalle on määritetty laskualennukset, määritetty prosenttiluvun arvo lisätään automaattisesti **Asiakkaan laskun alennus-%** -kenttään, jos ehdot täyttyvät. Liittyvä summa lisätään **Laskun alennussumma ilman ALV:a** -kenttään. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).  
15. Kun myyntilaskun rivit ovat valmiit, valitse **Kirjaa ja lähetä** -toiminto.  

Asiakkaan ensisijainen asiakirjojen vastaanottomenetelmä näkyy **Kirjaa ja lähetä vahvistus** -valintaikkunassa. Voit muuttaa lähetysmenetelmän valitsemalla **Lähetä asiakirja kohteeseen** -kentän valintapainikkeen. Lisätietoja on kohdassa [Toimintaohje: Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).

Nyt järjestelmässä luodaan liittyvä nimike ja asiakastapahtumat. Myyntilasku tulostetaan PDF-asiakirjana. Myyntilasku poistetaan myyntilaskujen luettelosta ja korvataan uudella asiakirjalla kirjattujen myyntilaskujen luettelosta.

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Varasto](inventory-manage-inventory.md)  
[Toimintaohje: Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

