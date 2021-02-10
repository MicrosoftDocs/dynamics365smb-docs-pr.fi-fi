---
title: Myyntitarjouksen luominen asiakkaalle | Microsoft Docs
description: Ohjeaiheessa käsitellään, miten luodaan myyntitarjous- tai tarjouspyyntöasiakirja kirjaamaan asiakkaalle tehty tarjous tuotteiden myynnistä tietyin ehdoin.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cd674e3c5f64889cb77e000fb823bf63a800bdb2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758240"
---
# <a name="make-sales-quotes"></a>Myyntitarjousten tekeminen
Luot myyntitarjouksen tallentaaksesi tarjouksen asiakkaalle myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla. Voit lähettää myyntitarjouksen asiakkaalle kommunikoidaksenne tarjouksesta. Voit lähettää asiakirjan sähköpostitse PDF-liitteenä. Sähköpostin perusteksti voidaan esitäyttää tarjouksen yhteenvedolla. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md).

Kun neuvottelet asiakkaan kanssa, voit muuttaa ja lähettää myyntitarjouksen uudelleen niin paljon kuin tarvitaan. Kun asiakas hyväksyy tarjouksen, voit muuntaa myyntitarjouksen myyntilaskuksi tai -tilaukseksi, jossa myynti käsitellään. Lisätietoja on kohdassa [Myynnin laskuttaminen](sales-how-invoice-sales.md) tai [Tuotteiden myyminen](sales-how-sell-products.md).

Voit täyttää myyntitarjouksen asiakkaan kentät kahdella tavalla sen mukaan, onko asiakas jo rekisteröity. Katso vaiheet 2 ja 3 seuraavassa menettelyssä.

## <a name="to-create-a-sales-quote"></a>Myyntitarjousten luominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitarjoukset** ja valitse sitten liittyvä linkki.
2. Syötä **Asiakas**-kenttään nykyisen asiakkaan nimi.

   Muut **Myyntitarjous**-sivun kentät sisältävät valitun asiakkaan vakiotiedot. Jos asiakasta ei ole rekisteröity, toimi seuraavasti:
3. Syötä **Asiakas**-kenttään uuden asiakkaan nimi.
4. Valitse uuden asiakkaan rekisteröimisen valintaikkunassa **Kyllä**-painike.
5. Valitse **Valitse uuden asiakkaan malli** -sivulla malli uuden asiakkaan kortin perusteella ja valitse sitten **OK**-painike.
6. Uuden asiakkaan kortissa näkyy valitun asiakasmallin tiedot. Täytä jäljellä olevat kentät. Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).  
7. Kun olet määrittänyt asiakaskortin, valitse **OK**-painike palataksesi **Myyntitarjous**-sivulle.

   Myyntitarjouksen useat kentät täytetään nyt tiedoilla, jotka olet määrittänyt uuden asiakkaan kortissa.  
8. Täytä tarvittaessa jäljellä olevat kentät **Myyntitarjous**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Voit nyt täyttää asiakkaille myytävien tuotteiden tai KP-tilille kirjattavan asiakastapahtuman myyntitilauksen rivit.   

    Jos olet määrittänyt toistuvien myyntien rivin asiakkaalle, kuten kuukausittainen täydennystilaus, voit lisätä nämä rivit tilaukseen valitsemalla **Nouda toistuvat myyntirivit** -toiminto.  

9. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä sen tuotteen, kulun tai tapahtuman tyyppi, jonka kirjaat myyntirivin asiakkaalle.
10. Valitse **Nro**-kenttään kirjattava tietue **Tyyppi**-kentän arvon mukaan.

    Jätä **Nro**-kenttä tyhjäksi seuraavissa tapauksissa:
    - Jos rivi on tarkoitettu kommentille. Kirjoita kommentti **Kuvaus**-kenttään.
    - Jos rivi on tarkoitettu luettelonimikkeelle. Valitse **Valitse luettelonimikkeet** -toiminto. Lisätietoja on kohdassa [Luettelonimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md).

11. Ilmoita **Määrä**-kentässä, kuinka monta tuote-, kulu- tai tapahtumayksikköä rivi kirjaa asiakkaalle.

    > [!NOTE]  
    >  Jos nimikkeen tyyppi on **Palvelu** tai **Tyyppi**-kentässä on **Resurssi**, määrä on sitten aikayksikkö, esimerkiksi tunnit, kuten rivin **Mittayksikkökoodi**-kenttä osoittaa. Lisätietoja on kohdassa [Nimikkeen mittayksiköiden määrittäminen](inventory-how-setup-units-of-measure.md).

    **Rivisumma**-kentän arvo lasketaan *Yksikköhinta* x *Määrä*.  

    Hinta ja rivin summat ilmaistaan ALV:n kanssa tai ilman sitä sen mukaan, mitä valitsit **Hinnat sisältävät verot** -kenttään asiakkaan kortissa.  
12. Jos haluat antaa alennuksen, anna prosentti **Rivialennus-%**-kentässä. **Rivisumma**-kentän arvo päivittyy vastaavasti.  

    Jos nimikkeiden erikoishinnat on määritetty asiakkaan tai nimikkeen kortin **Myyntihinnat ja myyntirivien alennukset**-pikavälilehdellä, myyntiriviin hinta ja summa päivittyvät automaattisesti, jos sovitut hinnan ehdot täyttyvät. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Toista vaiheet 9–12 jokaiselle tuotteelle, jonka haluat tarjota asiakkaalle.

    Rivien kokonaissummat lasketaan automaattisesti samalla, kun rivejä luodaan ja muokataan.  
14. Syötä **Laskun alennussumma** -kenttään summa, joka vähennetään **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

    Jos asiakkaalle on määritetty laskualennukset, määritetty prosenttiluvun arvo lisätään automaattisesti **Asiakkaan laskun alennus-%** -kenttään, jos ehdot täyttyvät. Liittyvä summa lisätään **Laskun alennussumma ilman ALV:a** -kenttään. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > Jos haluat, että **Tarjouksen voimassaolon päättymispäivä** -kohtaan täytetään automaattisesti tietty päivien määrä tarjouksen luonnin jälkeen, täytä **Tarjouksen voimassaolon laskenta** -kenttä **Myynti ja myyntisaamiset** -sivulla.

15. Kun myyntitarjouksen rivit ovat valmiit, valitse **Lähetä sähköpostitse** -toiminto.
16. Täytä **Lähetä sähköpost** -sivulla jäljellä olevat kentät ja tarkista upotettu myyntitarjous. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md).
17. Jos asiakas hyväksyy tarjouksen, valitse **Luo lasku**- tai **Tee tilaus** -toiminto.

Myyntitarjous on poistettu tietokannasta. Myyntilasku tai -tilaus luodaan myyntitarjouksen tietojen perusteella, jossa voit käsitellä myynnin. Myyntilaskun tai myyntitilauksen **Tarjouksen nro** -kenttä määrittää sen myyntitarjouksen numeron, josta tilaus on muunnettu. Lisätietoja on kohdassa [Myynnin laskuttaminen](sales-how-invoice-sales.md) tai [Tuotteiden myyminen](sales-how-sell-products.md).

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)
