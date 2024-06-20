---
title: Kokoonpano tilausta varten -nimikkeiden myyminen
description: 'Opettele myymään nimike, joka on koottu tilausta varten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting, substitute items'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# <a name="sell-items-assembled-to-order"></a>Kokoonpano tilausta varten -nimikkeiden myyminen

Tilausta varten koottujen nimikkeiden ei odoteta olevan varastossa, ja ne kootaan, kun ne sisällytetään myyntitilaukseen. Nimike on määritetty tilausta varten koottavaksi, kun nimikkeen kortin **Kokoonpanokäytäntö**-kentässä lukee **Kokoonpano tilausta varten**. Kun syötät nimikkeen myyntitilausriville, kokoonpanotilaus luodaan ja linkitetään myyntitilaukseen automaattisesti.  

> [!NOTE]  
> Jos varastossa on jo Kokoonpano tilausta varten -nimikkeitä, voit vähentää kyseisen määrän kokoonpanotilauksesta ja varata sen varastosta. Lisätietoja on kohdassa [Varastonimikkeiden myyminen kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Tässä toimenpiteessä käsittelet asiakkaan pyytämien määrittelyjen mukaan koottavan nimikkeen myyntiä. Näihin vaiheisiin sisältyy: 

* Myyntitilausrivin luominen.
* Kokoonpanon nimikkeen mukauttaminen muokkaamalla sen komponentteja ja resursseja.
* Saatavuuden tarkastaminen toimituspäivän määrittämiseksi.
* Myyntitilauksen vapauttaminen kokoamista ja välitöntä toimitusta varten.  

> [!NOTE]  
> Seuraava toimenpide ei sisällä vakiomyyntitilauksen luomisen vaiheita, jotka tapahtuvat ennen kuin syötät Kokoonpano tilaukseen -nimikkeen myyntitilausriville. Lisätietoja myyntitilausten luomisesta on kohdassa [Tuotteiden myyminen asiakkaan myyntitilauksen avulla](sales-how-sell-products.md).  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Myy nimike, jok aon kokoonpano tilausta varten

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Luo myyntitilaus. 
3. Valitse **Nro**-kenttään nimike, jolle on määritetty kokoonpano tilausta varten.  
4. Määritä **Sijaintikoodi**-kentässä sijainti, josta nimike myydään. Kokoonpanoprosessi tapahtuu kyseisessä sijainnissa.  
5. Määritä **Määrä**-kentässä, miten monta yksikköä haluat myytävän.  

    > [!NOTE]  
    >  Jos yksi tai useampi pyydetyn kokoonpanon nimikkeen määrän komponenteista ei ole saatavilla, saatavuutta koskevan varoituksen sivu avautuu. <!-- Check whether the field help would be useful. For more information, see Assembly Availability.  -->

    Kokoonpanotilaus luodaan ja linkitetään myyntitilausriviin. Kokoonpanotilauksen eräpäivä on myyntitilausrivin toimituspäivämäärä.  

    Myytävä määrä kopioidaan **Kokoonpantava määrä tilausta varten** -kenttään, joka ilmaisee, että nimikkeen asennus odottaa sinun kokoavan myyntirivillä olevan täyden määrän. Voit vähentää koottavaa määrää, jos esimerkiksi tiedät, että jotkin nimikkeet ovat jo saatavilla. Lisätietoja on kohdassa [Varastonimikkeiden myyminen kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6. Jos asiakas haluaa tuotepakettiin lisänimikkeen, valitse **Rivit**-pikavälilehdestä **Rivi**-toiminto, valitse **Kokoonpano tilausta varten** -toiminto ja valitse sitten **Kokoonpano tilausta varten -rivit** -toiminto tarkastellaksesi ja muuttaaksesi vakiokokoonpanon komponentteja. Voit myös valita **Kokoonpantava määrä tilausta varten** -kentän.  
7. Luo **Kokoonpano tilausta varten -rivit** -sivulta kokoonpanon lisäkomponentille uusi rivi, jonka tyyppi on **Nimike**.  

    Voit myös mukauttaa tilausta kasvattamalla paketin yhden vakionimikkeen määrää. Voit tehdä tämän lisäämällä arvon **Määrä per** -kentässä tietylle kokoonpanon tilausriville.  

    > [!NOTE]  
    >  **Kokoonpano tilausta varten -rivit** -sivu sisältää vain peruskentät, joilla voi mukauttaa komponenttien luetteloa, lisätä nimikkeiden seurantanumeroita tai ratkaista osien saatavuusongelmia. Jos haluat lisätä kokoonpanotilauksen tietoja, kuten kokoonpanotilauksen alkamispäivän, valitse **Näytä asiakirjat** -toiminto. Tämä avaa myyntitilausriviin linkitetyn kokoonpanotilauksen koko näkymän. Et voi muuttaa useimpien kokoonpanotilauksen otsikon kenttien sisältöä tai kirjata kokoonpanon tuotosta siitä. Sinun täytyy kirjata myyntitilausrivien toimitus.  
    >
    >  Linkitetyissä kokoonpanotilauksissa vain **Aloituspvm**-kenttää voidaan muuttaa. Aloituspäivämäärän muuttaminen sallii kokoajien määrittää, että he aloittavat kokoamisen ennen eräpäivää. Linkitetyn kokoonpanotilauksen rivien kaikki kentät voidaan muuttaa siten, että varaston työntekijät voivat syöttää kulutuksen lukuja prosessin aikana.  

8. Tarkista tai reagoi komponenttien saatavuusongelmiin. Valitse esimerkiksi korvaava nimike.  
9. Sulje **Kokoonpano tilausta varten -rivit** -sivu. Linkitetty kokoonpanotilaus on nyt valmis ja työntekijät voivat aloittaa mukautettujen nimikkeiden kokoamisen.  
10. Valitse myyntitilauksessa **Vapauta**-toiminto, jos haluat ilmoittaa kokoonpano-osastolle, että kokoonpanoprosessi voidaan aloittaa. Lisätietoja on kohdassa [Kokoa nimikkeet](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> Korvaavat nimikkeet eivät korvaa nimikettä automaattisesti toisella nimikkeellä esimerkiksi myyntitilausta luotaessa tai tuoterakenteessa. Sen sijaan sinulle ilmoitetaan, että korvaava vaihtoehto on saatavilla.

## <a name="see-also"></a>Katso myös

[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Kokoonpanon tuoterakenteiden käyttäminen](assembly-how-work-assembly-boms.md)  
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastonhallinnan yleiskatsaus](design-details-warehouse-management.md)
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
