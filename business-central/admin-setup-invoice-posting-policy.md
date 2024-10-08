---
title: Laskun kirjauskäytännön määrittäminen käyttäjille
description: 'Laskun kirjauskäytäntöjen avulla voit määrittää, voiko käyttäjä kirjata myynti- ja ostolaskuja.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 06/12/2024
ms.custom: bap-template
ms.search.forms: '119, 9807,'
ms.service: dynamics-365-business-central
---

# <a name="define-an-invoice-posting-policy-for-users"></a>Laskun kirjauskäytännön määrittäminen käyttäjille

Yrityksillä on usein yksilöllisiä prosesseja myynti- ja ostolaskujen sekä toimitusten kirjaamista varten. Prosessit voivat vaihdella esimerkiksi yhdestä henkilöstä, joka kirjaa kaiken ostotilaukseen, useisiin työntekijöihin. Voit rajoittaa käyttäjiä kirjaamalla laskuja tai vaatia, että laskut kirjataan yhdessä toimitusten tai vastaanottojen kanssa.

## <a name="to-specify-a-posting-policy"></a>Kirjauskäytännön määrittäminen

Valitse **Käyttäjäasetukset** -sivun **Myyntilaskun kirjaustapa**- ja **Ostolaskun kirjaustapa** -kentät, valitse jokin seuraavista vaihtoehdoista:

* **Sallittu** (oletus) - Säilytä tämänhetkinen toiminta, jossa käyttäjä voi valita käytettävän kirjausvaihtoehdon, kuten **Toimitus**, **Lasku** ja **Toimitus ja lasku**. 
* **Kielletty** - Estä käyttäjää kirjaamasta laskuja. [!INCLUDE [prod_short](includes/prod_short.md)] näyttää vahvistusikkunan, jonka ainoat vaihtoehdot ovat **Toimitus** ja **Lasku**.
* **Pakollinen** - Anna käyttäjän kirjata laskut yhdessä vastaanottojen tai toimitusten kanssa. [!INCLUDE [prod_short](includes/prod_short.md)] näyttää vahvistusikkunan, jossa on **Lähetys ja laskutus**- tai **Vastaanotto ja laskutus** -vaihtoehdot.

## <a name="effect-on-documents"></a>Vaikutus asiakirjoihin

Seuraavassa taulukossa kuvataan, miten laskun kirjauskäytännöt vaikuttavat asiakirjoihin.

> [!NOTE]
> Kun kirjaat myynti- ja ostolaskuja ja hyvityslaskuja, kirjausvaihtoehtoja ei ole. Asiakirjat kirjataan aina fyysisten tapahtumien ja rahoitustapahtumien kanssa. Laskuja ja hyvityslaskuja ei voi kirjata osittain.

|Asiakirja | Vaihtoehto 1: Salli <br>Näyttää useita vaihtoehtoja| Vaihtoehto 2: Kielletty <br>Vahvistusvalintaikkuna | Vaihtoehto 3: Pakollinen <br>Vahvistusvalintaikkuna|
|--|--|--|--|
|Myyntitilaus |- Toimitus <br>- Lasku <br>- Toimitus ja lasku |Haluatko kirjata toimituksen? |Haluatko kirjata toimituksen ja laskun?|
|Myyntilasku|Ei vaihtoehtoja| Kirjaus on kielletty käyttäjäasetuksissa|Haluatko kirjata laskun?|
|Myyntihyvityslasku|Ei vaihtoehtoja|Kirjaus on kielletty käyttäjäasetuksissa|Haluatko kirjata hyvityslaskun?|
|Myyntipalautustilaus |- Vast.otto <br>- Lasku <br>- Vastaanota ja laskuta |Haluatko kirjata vastaanoton? |Haluatko kirjata vastaanoton ja laskun?|
|Varaston poiminta |- Toimitus <br>- Toimitus ja lasku |Haluatko kirjata toimituksen? |Haluatko kirjata toimituksen ja laskun?|
|Ostotilaus |- Vast.otto <br>- Lasku <br>- Vastaanota ja laskuta |Haluatko kirjata vastaanoton? |Haluatko kirjata vastaanoton ja laskun?|
|Ostolasku|Ei vaihtoehtoja|Kirjaus on kielletty käyttäjäasetuksissa|Haluatko kirjata laskun?|
|Ostohyvityslasku|Ei vaihtoehtoja|Kirjaus on kielletty käyttäjäasetuksissa|Haluatko kirjata hyvityslaskun?|
|Palautettu ostotilaus |- Toimitus <br>- Lasku <br>- Toimitus ja lasku |Haluatko kirjata toimituksen? |Haluatko kirjata toimituksen ja laskun?|
|Varastohyllytys |- Vast.otto <br>- Vastaanota ja laskuta |Haluatko kirjata vastaanoton? |Haluatko kirjata vastaanoton ja laskun?|
|Fyysisen varaston toimitus |- Toimitus <br>- Toimitus ja lasku | Haluatko kirjata toimituksen? |Haluatko kirjata toimituksen ja laskun?|

   > [!Note]
   > Asetus ei vaikuta yleisen päiväkirjan rivien kirjaukseen, jossa voit valita **Asiakirjatyyppi**-kentässä **Lasku**.

## <a name="see-also"></a>Katso myös

[Myynnin laskutus](sales-how-invoice-sales.md)  
[Ostojen kirjaaminen ostolaskujen ja tilausten avulla](purchasing-how-record-purchases.md)  
[Ostonimikkeet myyntiä varten luomalla ostolaskuja](purchasing-how-purchase-products-sale.md)
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
