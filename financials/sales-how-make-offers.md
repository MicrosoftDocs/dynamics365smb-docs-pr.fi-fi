---
title: Myyntitarjouksen luominen asiakkaalle | Microsoft Docs
description: "Ohjeaiheessa käsitellään, miten luodaan myyntitarjous- tai tarjouspyyntöasiakirja kirjaamaan asiakkaalle tehty tarjous tuotteiden myynnistä tietyin ehdoin."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 552fbf283a9149c430ea1ed94bcea4bd22e43fea
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="make-offers"></a>Tarjousten tekeminen
Luot myyntitarjouksen tallentaaksesi tarjouksen asiakkaalle myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla. Voit lähettää myyntitarjouksen asiakkaalle kommunikoidaksenne tarjouksesta. Voit lähettää asiakirjan sähköpostitse PDF-liitteenä. Sähköpostin perusteksti voidaan esitäyttää tarjouksen yhteenvedolla. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md).

Kun neuvottelet asiakkaan kanssa, voit muuttaa ja lähettää myyntitarjouksen uudelleen niin paljon kuin tarvitaan. Kun asiakas hyväksyy tarjouksen, voit muuntaa myyntitarjouksen myyntilaskuksi tai -tilaukseksi, jossa myynti käsitellään. Lisätietoja on kohdassa [Myynnin laskuttaminen](sales-how-invoice-sales.md) tai [Tuotteiden myyminen](sales-how-sell-products.md).

Voit täyttää myyntitarjouksen asiakkaan kentät kahdella tavalla sen mukaan, onko asiakas jo rekisteröity. Katso vaiheet 2 ja 3 seuraavassa menettelyssä.

## <a name="to-create-a-sales-quote"></a>Myyntitarjousten luominen
Valitse aloitussivulla **Myyntitarjous**-toiminto.  
2. Syötä **Asiakas**-kenttään nykyisen asiakkaan nimi.

   Muut **Myyntitarjous**-ikkunan kentät sisältävät valitun asiakkaan vakiotiedot. Jos asiakasta ei ole rekisteröity, toimi seuraavasti:
3. Syötä **Asiakas**-kenttään uuden asiakkaan nimi.
4. Valitse uuden asiakkaan rekisteröimisen valintaikkunassa **Kyllä**-painike.
5. Valitse **Valitse uuden asiakkaan malli** -ikkunassa malli uuden asiakkaan kortin perusteella ja valitse sitten **OK**-painike.
6. Uuden asiakkaan kortissa näkyy valitun asiakasmallin tiedot. Täytä jäljellä olevat kentät. Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).  
7. Kun olet määrittänyt asiakaskortin, valitse **OK**-painike palataksesi **Myyntitarjous**-ikkunaan.

   Myyntitarjouksen useat kentät täytetään nyt tiedoilla, jotka olet määrittänyt uuden asiakkaan kortissa.  
8. Täytä tarvittaessa jäljellä olevat kentät **Myyntitarjous**-ikkunassa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Voit nyt täyttää asiakkaille myytävien tuotteiden tai KP-tilille kirjattavan asiakastapahtuman myyntitilauksen rivit.   

Jos olet määrittänyt toistuvien myyntien rivin asiakkaalle, kuten kuukausittainen täydennystilaus, voit lisätä nämä rivit tilaukseen valitsemalla **Nouda toistuvat myyntirivit** -toiminto.  
9. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä sen tuotteen, kulun tai tapahtuman tyyppi, jonka kirjaat myyntirivin asiakkaalle.
10. Valitse **Nro**-kenttään kirjattava tietue **Tyyppi**-kentän arvon mukaan.

 Jätä **Nro**-kenttä tyhjäksi seuraavissa tapauksissa: -Jos rivi on tarkoitettu kommentille. Kirjoita kommentti **Kuvaus**-kenttään.
 -Jos rivi on tarkoitettu ei-varastoitavalle nimikkeelle. Valitse **Valitse ei-varastoitavat nimikkeet** -toiminto. Lisätietoja on kohdassa [Ei-varastoitavien nimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md).

11. Ilmoita **Määrä**-kentässä, kuinka monta tuote-, kulu- tai tapahtumayksikköä rivi kirjaa asiakkaalle.

    > [!NOTE]  
>   Jos nimikkeen tyyppi on **Nimike - Palvelu** tai **Resurssi**, määrä on aikayksikkö, esimerkiksi tunnit, kuten rivin **Mittayksikkökoodi**-kenttä osoittaa.  

    **Rivisumma**-kentän arvo lasketaan *Yksikköhinta* x *Määrä*.  

    Hinta ja rivin summat ilmaistaan ALV:n kanssa tai ilman sitä sen mukaan, mitä valitsit **Hinnat sisältävät verot** -kenttään asiakkaan kortissa.  
12. Jos haluat antaa alennuksen, anna prosentti **Rivialennus-%**-kentässä. **Rivisumma**-kentän arvo päivittyy vastaavasti.  

    Jos nimikkeiden erikoishinnat on määritetty asiakkaan tai nimikkeen kortin **Myyntihinnat ja myyntirivien alennukset**-pikavälilehdellä, myyntiriviin hinta ja summa päivittyvät automaattisesti, jos sovitut hinnan ehdot täyttyvät. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Toista vaiheet 9–12 jokaiselle tuotteelle, jonka haluat tarjota asiakkaalle.  

    Rivien kokonaissummat lasketaan automaattisesti samalla, kun rivejä luodaan ja muokataan.  
14. Syötä **Laskun alennussumma** -kenttään summa, joka vähennetään **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

    Jos asiakkaalle on määritetty laskualennukset, määritetty prosenttiluvun arvo lisätään automaattisesti **Asiakkaan laskun alennus-%** -kenttään, jos ehdot täyttyvät. Liittyvä summa lisätään **Laskun alennussumma ilman ALV:a** -kenttään. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).
15. Kun myyntitarjouksen rivit ovat valmiit, valitse **Lähetä sähköpostitse** -toiminto.
16. Täytä **Lähetä sähköpost** -ikkunassa jäljellä olevat kentät ja tarkista upotettu myyntitarjous. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md).
17. Jos asiakas hyväksyy tarjouksen, valitse **Luo lasku**- tai **Tee tilaus** -toiminto.

Myyntitarjous on poistettu tietokannasta. Myyntilasku tai -tilaus luodaan myyntitarjouksen tietojen perusteella, jossa voit käsitellä myynnin. Myyntilaskun tai myyntitilauksen **Tarjouksen nro** -kenttä määrittää sen myyntitarjouksen numeron, josta tilaus on muunnettu. Lisätietoja on kohdassa [Myynnin laskuttaminen](sales-how-invoice-sales.md) tai [Tuotteiden myyminen](sales-how-sell-products.md).

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

