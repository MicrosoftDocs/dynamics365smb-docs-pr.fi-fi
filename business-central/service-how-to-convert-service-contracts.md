---
title: Huoltosopimusten muuntaminen
description: 'Tässä aiheessa kuvataan useita vaihtoehtoisia menetelmiä, joita voit käyttää ALV-summia sisältävän palvelusopimuksen muuntamista varten.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="convert-service-contracts-that-include-vat-amounts"></a><a name="convert-service-contracts-that-include-vat-amounts"></a>ALV-summia sisältävien huoltosopimusten muuntaminen
Koska ALV:n muutostyökalu ei voi muuntaa huoltosopimuksia, nämä sopimukset on muunnettava manuaalisesti. Tässä aiheessa kuvataan useita vaihtoehtoisia menetelmiä, joita voit käyttää palvelusopimuksen muuntamista varten.  

> [!NOTE]  
>  Tämä aihe tarjoaa korkeatasoisen työnkulun.  

 Seuraavassa ohjeessa neuvotaan, miten korjataan etukäteen maksetun huoltosopimuksen lasku, joka on luotu vuoden etukäteen.  

> [!NOTE]  
>  Määritä tässä esimerkissä käsittelypäivämääräksi 01.01.2017.  

### <a name="to-correct-an-invoice-for-a-prepaid-service-contract"></a><a name="to-correct-an-invoice-for-a-prepaid-service-contract"></a>Korjaa ennakkoon maksetun huoltosopimuksen lasku
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sopimuksen hallinta** ja valitse sitten vastaava linkki.  
2. Valitse **Luettelot** -kohdan alta **Huoltosopimukset**.  
3. Luo uusi ennakkoon maksettu huoltosopimus. Anna aloituspäiväksi **01.01.2017** ja laskukausi asiakkaalle **20000**.  
4. Voit allekirjoittaa sopimuksen valitsemalla **Allekirjoita sopimus** -toiminnon.  
5. Huoltolaskun luominen:
6. Lasku on merkitty kirjaamattomaksi huoltolaskuksi. Tarkastele huoltolaskua valitsemalla **Huolto**-toiminto, valitse **Sopimuksen hallinta** -toiminto ja valitse sitten **Huoltolaskut**-toiminto.  
7. Kirjaa huoltolasku.  

> [!NOTE]  
>  Älä muuta kirjaamatonta huoltolaskua. Koska palvelutapahtumat luodaan laskun luonnin yhteydessä, kirjaamattoman laskun muutos ei muuta jo luotuja tapahtumia. ALV-tapahtumat luodaan laskun kirjauksen yhteydessä. Tämän avulla voi muuttaa yleisiä tuotteen kirjausryhmiä ja GSP-tuotteen kirjausryhmiä kirjaamattomassa huoltolaskussa.   

### <a name="to-create-a-credit-memo-for-vat-difference"></a><a name="to-create-a-credit-memo-for-vat-difference"></a>Luo ALV-erotuksen hyvityslasku
Seuraavassa ohjeessa neuvotaan, miten luodaan hyvityslasku, joka sisältää vain jo laskutetun, **01.07.2017** alkaneen kauden ALV-erotus. Tässä esimerkissä ALV-summa kirjataan vain varainhoidon moduulin, ei palveluiden hallinta-moduuliin. Huoltotapahtumaan linkitettyjä ALV-tapahtumia ei voi korjata.  

1. Luo uusi pääkirjanpidon tili ALV-erolle. Tätä tiliä käytetään ALV-korjausten suoraan kirjaamiseen.  
2. Lisää uusi rivi ALV-kirjausasetuksiin.  

### <a name="to-create-contract-expiration-dates-in-contract-lines"></a><a name="to-create-contract-expiration-dates-in-contract-lines"></a>Luo sopimuksen vanhentumispäivämäärät sopimusriveille
Seuraavassa ohjeessa neuvotaan, miten luodaan uusia sopimuksia käyttämällä sopimuksen vanhentumispäiviä huoltosopimusriveillä.  

1. Määritä **Huoltosopimus**-sivulla sopimuksen vanhenemispäivämääräksi **30.06.2017**.  
2. Valitse **Luo hyvityslasku** -toiminto, niin hyvityslasku luodaan automaattisesti aikavälille heinäkuusta 2017 joulukuuhun 2017.  
3. Koska sopimus on vanhentunut, sinun on luotava uusi sopimus uudella ALV-arvolla ajalle 1. heinäkuuta 2017 ja 31. joulukuuta 2017.  

### <a name="to-create-a-new-credit-memo"></a><a name="to-create-a-new-credit-memo"></a>Luo uusi hyvityslasku.
Seuraavassa ohjeessa neuvotaan, miten luodaan uusi hyvityslasku käyttäen **Hae enn. maksetut sop. tapahtumat** -erä-ajoa. Vuoden 2017 tammikuun ja kesäkuun väliset tapahtumat, joita et halua korjata, poistetaan.  

1. Aja ALV-kannan muutostyökalu 1. heinäkuuta 2017. Yleinen tuotteen kirjausryhmä tai ALV-tuotteen kirjausryhmä muutetaan. Lisätietoja on kohdassa [Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md).  
2. ALV-muutostyökalun suorittamisen jälkeen, kirjoita huoltosopimuksen vanhenemispäivämäärä. Nyt voit poistaa huoltosopimuksen rivin ja luoda uuden rivin, joka on samanlainen kuin vanha.  
3. Luo uusi lasku kaudelle Tammikuu 2017 - Joulukuu 2012 uudella ALV-prosentilla.  
4. Luo toinen hyvityslasku **Huollon hyvityslaskut** -sivulla valitsemalla **Uusi**-toiminto luodaksesi uuden huollon hyvityslaskun.  
5. Valitse **Hae enn. maksetut sop.tapaht** -toiminto.  
6. Kun muuntaminen on valmis, ALV- ja huoltotapahtumasyötteet ovat oikeat.  

## <a name="see-also"></a><a name="see-also"></a>Katso myös
[Huoltosopimusten ja huoltosopimustarjousten käyttäminen](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Rahoitus](finance.md)  
[ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
