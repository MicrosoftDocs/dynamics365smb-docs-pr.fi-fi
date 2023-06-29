---
title: Laskun kirjauskäytännön määrittäminen käyttäjille
description: 'Laskun kirjauskäytäntöjen avulla voit määrittää, voiko käyttäjä kirjata myynti- ja ostolaskuja.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 03/09/2023
ms.custom: bap-template
ms.search.forms: '119, 9807,'
---

# <a name="define-an-invoice-posting-policy-for-users"></a><a name="define-an-invoice-posting-policy-for-users"></a>Laskun kirjauskäytännön määrittäminen käyttäjille

Yrityksillä on usein yksilöllisiä prosesseja myynti- ja ostolaskujen sekä toimitusten kirjaamista varten. Prosessit voivat vaihdella esimerkiksi yhdestä henkilöstä, joka kirjaa kaiken ostotilaukseen, useisiin työntekijöihin. Voit rajoittaa käyttäjiä kirjaamalla laskuja tai vaatia, että laskut kirjataan yhdessä toimitusten tai vastaanottojen kanssa.

## <a name="to-specify-a-posting-policy"></a><a name="to-specify-a-posting-policy"></a>Kirjauskäytännön määrittäminen

Valitse **Käyttäjäasetukset** -sivun **Myyntilaskun kirjaustapa**- ja **Ostolaskun kirjaustapa** -kentät, valitse jokin seuraavista vaihtoehdoista:

* **Sallittu** (oletus) - Säilytä tämänhetkinen toiminta, jossa käyttäjä voi valita käytettävän kirjausvaihtoehdon, kuten **Toimitus**, **Lasku** ja **Toimitus ja lasku**. 
* **Kielletty** - Estä käyttäjää kirjaamasta laskuja. Business Central näyttää vahvistusikkunan, jossa on vain **Lähetys**- ja **Vastaanotto** -vaihtoehdot.
* **Pakollinen** - Anna käyttäjän kirjata laskut yhdessä vastaanottojen tai toimitusten kanssa. Business Central näyttää vahvistusikkunan, jossa on **Lähetys ja laskutus**- tai **Vastaanotto ja laskutus** -vaihtoehdot.

## <a name="effect-on-documents"></a><a name="effect-on-documents"></a>Vaikutus asiakirjoihin

Seuraavassa taulukossa kuvataan, miten laskun kirjauskäytännöt vaikuttavat asiakirjoihin.

|Asiakirja | Vaihtoehto 1: Salli <br>Näyttää useita vaihtoehtoja| Vaihtoehto 2: Kielletty <br>Vahvistusvalintaikkuna | Vaihtoehto 3: Pakollinen <br>Vahvistusvalintaikkuna|
|--|--|--|--|
|Myyntitilaus |- Toimitus <br>- Lasku <br>- Toimitus ja lasku |Haluatko kirjata toimituksen? |Haluatko kirjata toimituksen ja laskun?|
|Myynnin palautustilaus |- Vast.otto <br>- Lasku <br>- Vastaanota ja laskuta |Haluatko kirjata vastaanoton? |Haluatko kirjata vastaanoton ja laskun?|
|Varaston poiminta |- Toimitus <br>- Toimitus ja lasku |Haluatko kirjata toimituksen? |Haluatko kirjata toimituksen ja laskun?|
|Ostotilaus |- Vast.otto <br>- Lasku <br>- Vastaanota ja laskuta |Haluatko kirjata vastaanoton? |Haluatko kirjata vastaanoton ja laskun?|
|Ostopalautustilaus |- Toimitus <br>- Lasku <br>- Toimitus ja lasku |Haluatko kirjata toimituksen? |Haluatko kirjata toimituksen ja laskun?|
|Varastohyllytys |- Vast.otto <br>- Vastaanota ja laskuta |Haluatko kirjata vastaanoton? |Haluatko kirjata vastaanoton ja laskun?|
|Fyysisen varaston toimitus |- Toimitus <br>- Toimitus ja lasku | Haluatko kirjata toimituksen? |Haluatko kirjata toimituksen ja laskun?|

   > [!Note]
   > Asetus ei vaikuta yleisen päiväkirjan rivien kirjaukseen, jossa voit valita **Asiakirjatyyppi**-kentässä **Lasku**.

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Myynnin laskutus](sales-how-invoice-sales.md)  
[Ostojen kirjaaminen ostolaskujen ja tilausten avulla](purchasing-how-record-purchases.md)  
[Ostonimikkeet myyntiä varten luomalla ostolaskuja](purchasing-how-purchase-products-sale.md)
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
