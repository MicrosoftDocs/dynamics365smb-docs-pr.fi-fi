---
title: EU-kolmikantatapahtumat
description: 'Tässä artikkelissa kerrotaan, miten Euroopan unionin (EU) kolmansien osapuolten ostotapahtumia määritetään ja käytetään.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.form: '50, 51, 52, 187, 317'
ms.search.keywords: 'EU3P, EU 3-P, EU 3-Party'
ms.date: 07/07/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# EU-kolmikantatapahtumat

Euroopan unionin (EU) kolmannen osapuolen kauppa toteutuu, kun vastaanotat ostolaskun yhdestä EU-maasta/-alueelta, ja tuotteet lähetetään eri EU-maahan/-alueelle ilman, että ne saapuvat asuinmaahan. Tapahtumasumma yksilöidä ja raportoida erikseen joidenkin EU-maiden/alueiden arvonlisäveron (ALV) raportointia ja ALV-tietojenvaihtojärjestelmää (VIES) koskevien vaatimusten täyttämiseksi. Microsoft Dynamics 365 Business Central mahdollistaa ostotapahtumien määrittämisen EU:n kolmannen osapuolten kaupaksi. Kirjatut EU:n kolmannen osapuolen tapahtumat voidaan suodattaa ALV-ilmoituksissa ja jättää pois **ALV-VIES-ilmoituksen verotodennusraportin** **Myynti asiakkaille** -sarakkeesta.

Vaikka ominaisuus olisi esiasennettu laajennukseksi, sitä ei oletusarvoisesti aktivoida. Ota toiminto käyttöön seuraavien ohjeiden mukaisesti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, siirry **Ominaisuuksien hallinta** -työtilaan ja valitse sitten vastaava linkki.
2. Etsi ja valitse luettelosta **Toiminnon päivitys: Uusi EU-kolmikantakauppa-laajennus korvaa nykyisen EU-kolmikanta-toiminnon**
3. Valitse **Otettu käyttöön** -sarakkeessa **Kaikki käyttäjät**.

## EU:n kolmannen osapuolen kaupan toimintojen ottaminen käyttöön oston yhteydessä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV:n määrittäminen** ja valitse sitten vastaava linkki.
2. Merkitse **ALV-asetukset**-sivulla **Ota käyttöön EU:n kolmannen osapuolen osto** -kenttä.

## Käytä EU:n kolmannen osapuolen kauppatoimintoja

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Ostolasku** (tai joku muu ostoasiakirja) ja valitse sitten liittyvä linkki.
2. Valitse olemassa oleva ostolasku tai luo uusi valitsemalla **Uusi**.
3. Valitse **Laskun tiedot** -pikavälilehdessä **EU:n kolmannen osapuolen kauppa** -valintaruutu.
4. Valitse **OK**.

## Sisällytä tai jätä pois EU-kolmansien osapuolten kaupan kirjanpito ALV-ilmoituksessa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-ilmoitus** ja valitse sitten vastaava linkki.
2. Valitse **ALV-ilmoitus** -sivulla jokin seuraavista vaihtoehdoista, niin saat EU:n kolmannen osapuolen kauppatietueet näkyviin **EU:n kolmannen osapuolen kaupan suodatin** -kentän avulla.

    | Asetus | Kuvaus |
    |--------|-------------|
    | Kaikki | Näytä kaikki tietueet riippumatta siitä, oliko **EU:n kolmannen osapuolen kauppa** -kenttä asiakirjoissa merkitty. |
    | EU-kolmikanta | Näytä vain tietueet, joissa **EU:n kolmannen osapuolen kauppa** -kenttä asiakirjoissa oli merkitty. |
    | Ei EU-kolmikanta | Näytä vain tietueet, joissa **EU:n kolmannen osapuolen kauppa** -kenttä asiakirjoissa ei ollut merkitty. |


## Katso myös
[Taloushallinto](finance.md)  
[Business Centralin käyttäminen](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
