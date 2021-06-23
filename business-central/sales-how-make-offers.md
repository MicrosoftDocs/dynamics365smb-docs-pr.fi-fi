---
title: Myyntitarjouksen tekeminen asiakkaalle
description: Ohjeaiheessa käsitellään, miten luodaan myyntitarjous- tai tarjouspyyntöasiakirja kirjaamaan asiakkaalle tehty tarjous tuotteiden myynnistä tietyin ehdoin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: a538b7099521b10227bf5aeaefad0a9c60971068
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115538"
---
# <a name="make-sales-quotes"></a>Myyntitarjousten tekeminen

Luot myyntitarjouksen tallentaaksesi tarjouksen asiakkaalle myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla. Voit lähettää myyntitarjouksen asiakkaalle kommunikoidaksenne tarjouksesta. Voit lähettää asiakirjan sähköpostitse PDF-liitteenä. Sähköpostin perusteksti voidaan esitäyttää tarjouksen yhteenvedolla. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md).

Kun neuvottelet asiakkaan kanssa, voit muuttaa ja lähettää myyntitarjouksen uudelleen niin paljon kuin tarvitaan. Kun asiakas hyväksyy tarjouksen, voit muuntaa myyntitarjouksen myyntilaskuksi tai -tilaukseksi, jossa myynti käsitellään. Lisätietoja on kohdassa [Myynnin laskuttaminen](sales-how-invoice-sales.md) tai [Tuotteiden myyminen](sales-how-sell-products.md).

Voit täyttää myyntitarjouksen asiakkaan kentät kahdella tavalla sen mukaan, onko asiakas jo rekisteröity. Katso vaiheet 2 ja 3 seuraavassa menettelyssä.

## <a name="to-create-a-sales-quote"></a>Myyntitarjousten luominen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitarjoukset** ja valitse sitten liittyvä linkki.
2. Syötä **Asiakas**-kenttään nykyisen asiakkaan nimi.

   Muut **Myyntitarjous**-sivun kentät sisältävät valitun asiakkaan vakiotiedot.  

    [!INCLUDE [sales-create-customer](includes/sales-create-customer.md)]

    Myyntitarjouksen useat kentät täytetään nyt tiedoilla, jotka olet määrittänyt uuden asiakkaan kortissa.  
3. Täytä tarvittaessa jäljellä olevat kentät **Myyntitarjous**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Voit nyt täyttää asiakkaille myytävien tuotteiden tai KP-tilille kirjattavan asiakastapahtuman myyntitilauksen rivit.  

    Jos olet määrittänyt toistuvien myyntien rivin asiakkaalle, kuten kuukausittainen täydennystilaus, voit lisätä nämä rivit tilaukseen valitsemalla **Nouda toistuvat myyntirivit** -toiminto.  

4. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä sen tuotteen, kulun tai tapahtuman tyyppi, jonka kirjaat myyntirivin asiakkaalle.
5. Valitse **Nro**-kenttään kirjattava tietue **Tyyppi**-kentän arvon mukaan.

    Jätä **Nro**-kenttä tyhjäksi seuraavissa tapauksissa:
    - Jos rivi on tarkoitettu kommentille. Kirjoita kommentti **Kuvaus**-kenttään.
    - Jos rivi on tarkoitettu luettelonimikkeelle. Valitse **Valitse luettelonimikkeet** -toiminto. Lisätietoja on kohdassa [Luettelonimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md).

6. Ilmoita **Määrä**-kentässä, kuinka monta tuote-, kulu- tai tapahtumayksikköä rivi kirjaa asiakkaalle.

    > [!NOTE]  
    >  Jos nimikkeen tyyppi on **Palvelu** tai **Tyyppi**-kentässä on **Resurssi**, määrä on sitten aikayksikkö, esimerkiksi tunnit, kuten rivin **Mittayksikkökoodi**-kenttä osoittaa. Lisätietoja on kohdassa [Nimikkeen mittayksiköiden määrittäminen](inventory-how-setup-units-of-measure.md).

    **Rivisumma**-kentän arvo lasketaan *Yksikköhinta* x *Määrä*.  

    Hinta ja rivin summat ilmaistaan ALV:n kanssa tai ilman sitä sen mukaan, mitä valitsit **Hinnat sisältävät verot** -kenttään asiakkaan kortissa.  
7. Jos haluat antaa alennuksen, anna prosentti **Rivialennus-%**-kentässä. **Rivisumma**-kentän arvo päivittyy vastaavasti.  

    Jos nimikkeiden erikoishinnat on määritetty asiakkaan tai nimikkeen kortin **Myyntihinnat ja myyntirivien alennukset**-pikavälilehdellä, myyntiriviin hinta ja summa päivittyvät automaattisesti, jos sovitut hinnan ehdot täyttyvät. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Toista vaiheet 4–7 jokaiselle tuotteelle, jonka haluat tarjota asiakkaalle.

    Rivien kokonaissummat lasketaan automaattisesti samalla, kun rivejä luodaan ja muokataan.  
9. Syötä **Laskun alennussumma** -kenttään summa, joka vähennetään **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

    Jos asiakkaalle on määritetty laskualennukset, määritetty prosenttiluvun arvo lisätään automaattisesti **Asiakkaan laskun alennus-%** -kenttään, jos ehdot täyttyvät. Liittyvä summa lisätään **Laskun alennussumma ilman ALV:a** -kenttään. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > Jos haluat, että **Tarjouksen voimassaolon päättymispäivä** -kohtaan täytetään automaattisesti tietty päivien määrä tarjouksen luonnin jälkeen, täytä **Tarjouksen voimassaolon laskenta** -kenttä **Myynti ja myyntisaamiset** -sivulla.

10. Kun myyntitarjouksen rivit ovat valmiit, valitse **Lähetä sähköpostitse** -toiminto.
11. Täytä **Lähetä sähköpost** -sivulla jäljellä olevat kentät ja tarkista upotettu myyntitarjous. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md).
12. Jos asiakas hyväksyy tarjouksen, valitse **Luo lasku**- tai **Tee tilaus** -toiminto.

Myyntitarjous on poistettu tietokannasta. Myyntilasku tai -tilaus luodaan myyntitarjouksen tietojen perusteella, jossa voit käsitellä myynnin. Myyntilaskun tai myyntitilauksen **Tarjouksen nro** -kenttä määrittää sen myyntitarjouksen numeron, josta tilaus on muunnettu. Lisätietoja on kohdassa [Myynnin laskuttaminen](sales-how-invoice-sales.md) tai [Tuotteiden myyminen](sales-how-sell-products.md).  

## <a name="external-document-number"></a>Ulkoisen tiedoston numero

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Katso myös

[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]