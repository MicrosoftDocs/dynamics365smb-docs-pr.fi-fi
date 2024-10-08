---
title: EU-kolmikantatapahtumat
description: 'Tässä artikkelissa kerrotaan, miten Euroopan unionin (EU) kolmansien osapuolten ostotransaktiot määritetään ja käytetään.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.form: '50, 51, 52, 187, 317'
ms.search.keywords: 'EU3P, EU 3-P, EU 3-Party'
ms.date: 08/12/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="eu-third-party-purchase-transactions"></a>EU-kolmikantatapahtumat

Euroopan unionin (EU) kolmannen osapuolen kauppa toteutuu, kun vastaanotat ostolaskun yhdestä EU-maasta/-alueelta, ja tuotteet lähetetään eri EU-maahan/-alueelle ilman, että ne saapuvat asuinmaahan. Tapahtumasumma yksilöidä ja raportoida erikseen joidenkin EU-maiden/alueiden arvonlisäveron (ALV) raportointia ja ALV-tietojenvaihtojärjestelmää (VIES) koskevien vaatimusten täyttämiseksi. Microsoft Dynamics 365 Business Central mahdollistaa ostotapahtumien määrittämisen EU:n kolmannen osapuolten kaupaksi. Kirjatut EU:n kolmannen osapuolen tapahtumat voidaan suodattaa ALV-ilmoituksissa ja jättää pois **ALV-VIES-ilmoituksen verotodennusraportin** **Myynti asiakkaille** -sarakkeesta.

Vaikka ominaisuus olisi esiasennettu laajennukseksi, sitä ei oletusarvoisesti aktivoida. Ota toiminto käyttöön seuraavien ohjeiden mukaisesti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, siirry **Ominaisuuksien hallinta** -työtilaan ja valitse sitten vastaava linkki.
2. Etsi ja valitse luettelosta **Toiminnon päivitys: Uusi EU-kolmikantakauppa-laajennus korvaa nykyisen EU-kolmikanta-toiminnon**
3. Valitse **Otettu käyttöön** -sarakkeessa **Kaikki käyttäjät**.

> [!NOTE]
> Jos käytät saksalaista tai italialaista lokalisointia, et voi ottaa tätä sovellusta käyttöön, koska se ei ole yhteensopiva tiettyjen lokalisointien ALV-ominaisuuksien kanssa.  

## <a name="enable-eu-third-party-trade-functionality-for-a-purchase"></a>EU:n kolmannen osapuolen kaupan toimintojen ottaminen käyttöön oston yhteydessä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV:n määrittäminen** ja valitse sitten vastaava linkki.
2. Merkitse **ALV-asetukset**-sivulla **Ota käyttöön EU:n kolmannen osapuolen osto** -kenttä.

## <a name="use-eu-third-party-trade-functionality"></a>Käytä EU:n kolmannen osapuolen kauppatoimintoja

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, syötä **Ostolaskut**  (tai muu ostoasiakirja) ja valitse linkit.
2. Valitse olemassa oleva ostolasku tai luo uusi valitsemalla **Uusi**.
3. Valitse **Laskun tiedot** -pikavälilehdessä **EU:n kolmannen osapuolen kauppa** -valintaruutu.
4. Valitse **OK**.

## <a name="include-or-exclude-eu-third-party-trade-records-on-the-vat-statement"></a>Sisällytä tai jätä pois EU-kolmansien osapuolten kaupan kirjanpito ALV-ilmoituksessa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, syötä **ALV-ilmoitukset** ja valitse sitten liittyvä linkki.
2. Valitse **ALV-ilmoitus** -sivulla jokin seuraavista vaihtoehdoista, niin saat EU:n kolmannen osapuolen kauppatietueet näkyviin **EU:n kolmannen osapuolen kaupan suodatin** -kentän avulla.

    | Asetus | Kuvaus |
    |--------|-------------|
    | Kaikki | Näytä kaikki tietueet riippumatta siitä, oliko **EU:n kolmannen osapuolen kauppa** -kenttä asiakirjoissa merkitty. |
    | EU-kolmikanta | Näytä vain tietueet, joissa **EU:n kolmannen osapuolen kauppa** -kenttä asiakirjoissa oli merkitty. |
    | Ei EU-kolmikanta | Näytä vain tietueet, joissa **EU:n kolmannen osapuolen kauppa** -kenttä asiakirjoissa ei ollut merkitty. |

## <a name="see-also"></a>Katso myös
[Taloushallinto](finance.md)    
[Business Centralin käyttäminen](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
