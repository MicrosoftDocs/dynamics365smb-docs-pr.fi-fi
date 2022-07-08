---
title: Myyntitarjousten tekeminen
description: Ohjeaiheessa käsitellään, miten luodaan myyntitarjous- tai tarjouspyyntöasiakirja kirjaamaan asiakkaalle tai mahdolliselle asiakkaalle tehty tarjous tuotteiden myynnistä tietyin ehdoin.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.search.form: 41, 9300
ms.date: 07/12/2021
ms.author: edupont
ms.openlocfilehash: 7c3540b7ccc54cb4aed342e0963dd66a3a7adb88
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9076407"
---
# <a name="make-sales-quotes"></a>Myyntitarjousten tekeminen

Luot myyntitarjouksen tallentaaksesi tarjouksen asiakkaalle tai mahdolliselle asiakkaalle myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla. Voit lähettää myyntitarjouksen asiakkaalle kommunikoidaksenne tarjouksesta. Voit lähettää asiakirjan sähköpostitse PDF-liitteenä. Sähköpostin perusteksti voidaan esitäyttää tarjouksen yhteenvedolla. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md).

Kun neuvottelet asiakkaan tai mahdollisen asiakkaan kanssa, voit muuttaa ja lähettää myyntitarjouksen uudelleen niin usein kuin tarvitaan. Kun asiakas hyväksyy tarjouksen, voit muuntaa myyntitarjouksen myyntilaskuksi tai -tilaukseksi, jossa myynti käsitellään. Lisätietoja on kohdassa [Myynnin laskuttaminen](sales-how-invoice-sales.md) tai [Tuotteiden myyminen](sales-how-sell-products.md).

Useimmissa tapauksissa myyntitarjouksia lähetetään mahdollisille asiakkaille. Sinulla on usein yhteyshenkilö, jonka kanssa neuvottelet. Jos he hyväksyvät tarjouksesi, muutat myyntitarjouksen tilaukseksi ja rekisteröit mahdollisen asiakkaan asiakkaaksi [!INCLUDE [prod_short](includes/prod_short.md)]issa. Seuraavassa vaiheessa keskitymme kontakteihin, mutta voit myös lähettää tarjouksia nykyisille asiakkaille.  

## <a name="to-create-a-sales-quote"></a>Myyntitarjousten luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake, syötä **Myyntitarjoukset** ja valitse sitten vastaava linkki.
2. Määritä kontakti tai asiakas, jolle haluat lähettää myyntitarjouksen.

    - Jos myyntitarjous on aiemmin luodulle kontaktille, määritä nimi kohtaan **Kontaktin nro.** -kentässä.  

        Jos myyntitarjous on aiemmin luodulle asiakkaalle, määritä asiakas **Asiakas**-kenttään.
    - Jos kontaktia ei ole rekisteröity, toimi seuraavasti:

        1. **Kontaktin nro** - kentässä valitse muokkauspainike :::image type="icon" source="media/assist-edit-icon.png" border="false":::.
        2. Valitse kontaktin valintaa koskevassa valintaikkunassa **Uusi**-toiminto ja täytä sitten asianmukaiset kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Lisätietoja on kohdassa [Kontaktien luominen](marketing-create-contact-companies.md).  
        3. Kun olet täyttänyt kontaktikortin, valitse juuri luotu kontakti kontaktiluettelosta ja palaa sitten myyntitarjoukseen valitsemalla OK-painike.

        Myyntitarjouksen useat kentät täytetään nyt tiedoilla, jotka olet määrittänyt uuden kontaktin kortissa.

        > [!NOTE]
        > Laskeaksesi tarjouksen verot ja hinnat oikein, valitse asianmukainen asiakasmalli **Asiakasmallin koodi** -kentässä. Mallia käytetään kontaktin muuntamiseksi asiakkaaksi, kun tarjous on muunnettu myyntitilaukseksi tai laskuksi.
    -  Jos tarjous on uudelle asiakkaalle, sinun on lisättävä asiakas. Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).  

3. Täytä tarvittaessa jäljellä olevat kentät **Myyntitarjous**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Voit nyt täyttää asiakkaille tai mahdollisille asiakkaille myytävien tuotteiden tai KP-tilille kirjattavan asiakastapahtuman myyntitilauksen rivit.  

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
8. Toista vaiheet 4–7 jokaiselle tuotteelle, jonka haluat tarjota kontaktille.

    Rivien kokonaissummat lasketaan automaattisesti samalla, kun rivejä luodaan ja muokataan.  
9. Syötä **Laskun alennussumma** -kenttään summa, joka vähennetään **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

    Jos asiakkaalle on määritetty laskualennukset, määritetty prosenttiluvun arvo lisätään automaattisesti **Asiakkaan laskun alennus-%** -kenttään, jos ehdot täyttyvät. Liittyvä summa lisätään **Laskun alennussumma ilman ALV:a** -kenttään. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > Jos haluat, että **Tarjouksen voimassaolon päättymispäivä** -kohtaan täytetään automaattisesti tietty päivien määrä tarjouksen luonnin jälkeen, täytä **Tarjouksen voimassaolon laskenta** -kenttä **Myynti ja myyntisaamiset** -sivulla.

10. Kun myyntitarjouksen rivit ovat valmiit, valitse **Lähetä sähköpostitse** -toiminto.
11. Täytä **Lähetä sähköpost** -sivulla jäljellä olevat kentät ja tarkista upotettu myyntitarjous. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md).
12. Jos kontakti hyväksyy tarjouksen, valitse **Tee tilaus** -toiminto.  

    Voit valita myös **Tee lasku** -toiminnon, jos organisaatiosi suosii tätä prosessia.  
    > [!NOTE]
    > Jos lisäsit asiakkaan vaiheessa 2, sinua pyydetään vahvistamaan tarjouksen muuntaminen tilaukseksi.  
    >
    > Jos lisäsit mahdollisen asiakkaan yhteyshenkilön vaiheessa 2, sinua pyydetään tekemään seuraavat toimet:
    >
    >  - Muunna kontakti tai mahdollinen asiakas asiakkaaksi valitsemalla jokin kontaktin muuntomalleista. Lisätietoja on kohdassa [Asiakkaan, toimittajan, työntekijän tai pankkitilin luominen yhteyshenkilöstä](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  
    > - Vahvista tarjouksen muuntaminen tilaukseksi.

Muunnos poistaa myyntitarjouksen tietokannasta. Myyntilasku tai -tilaus luodaan myyntitarjouksen tietojen perusteella, jotta voit käsitellä myynnin. Myyntilaskun tai myyntitilauksen **Tarjouksen nro** -kenttä määrittää sen myyntitarjouksen numeron, josta tilaus on muunnettu. Lisätietoja on kohdassa [Myynnin laskuttaminen](sales-how-invoice-sales.md) tai [Tuotteiden myyminen](sales-how-sell-products.md).  

## <a name="external-document-number"></a>Ulkoisen tiedoston numero

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Asiakirjojen arkistointi](across-how-to-archive-documents.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]