---
title: Kuvan analysointilaajennuksen käyttäminen | Microsoft Docs
description: Voit analysoida tällä laajennuksella kontaktihenkilöiden ja nimikkeiden kuvia ja etsiä määritteitä, mikä nopeuttaa niiden määrittämistä Business Central -sovelluksessa.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 5e7312e6e660d74089b0dce43ddf015be60ab446
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315491"
---
# <a name="the-image-analyzer-extension"></a>Kuvan analysointilaajennus
Kuvan analysointilaajennus havaitsee Microsoftin kognitiivisten palveluiden konenäön ohjelmointirajapinnan tehokkaalla kuva-analytiikalla määritteet nimikkeille ja kontaktihenkilöille tuoduissa kuvissa, mikä helpottaa kuvien tarkastelua ja määrittämistä. Nimikkeiden määritteet voivat ilmaista esimerkiksi, onko kyse pöydästä vai autosta ja onko se sininen vai punainen. Kontaktihenkilöiden määritteet voivat ilmaista sukupuolen tai iän.

Kuvan analysointitoiminto ehdottaa määritteitä konenäön ohjelmointirajapinnan löytämien tunnisteiden ja luotettavuustasoon perusteella. Se ehdotta oletusarvoisesti määritteitä vain, jos sen luottamus määritteen oikeellisuuteen on vähintään 80 %. Voit määrittää tarvittaessa jonkin toisen luotettavuustason. Lisätietoja tunnisteiden ja luotettavuustason määrittämisestä on ohjeaiheessa [Konenäön ohjelmointirajapinta](https://go.microsoft.com/fwlink/?linkid=851476).  

Kuvan analysointitoiminto on maksuton [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, mutta tietyn ajanjakson aikana analysoitavien kuvien määrää on rajoitettu. Oletusarvoisesti kuukaudessa saa analysoida 100 kuvaa.

Kun laajennus on otettu käyttöön, kuvan analysointitoiminto suoritetaan aina, kun tuot nimikkeeseen tai kontaktihenkilöön kuvan. Näet määritteet, luottamustason ja tiedot heti ja voit määrittää, miten kutakin määritettä käsitellään. Jos toit kuvia ennen kuvan analysointilaajennuksen käyttöönottoa, sinun on siirryttävä nimikkeeseen tai kontaktikortteihin ja valittava **Analysoi kuva** -toiminto.  

## <a name="privacy-notice"></a>Tietosuojatiedot
Tämä laajennus käyttää Microsoftin kognitiivisten palveluiden konenäön ohjelmointirajapintaa. Sen yhdenmukaisuussitoumusten tasot voivat olla erilaiset kuin [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa. Jos otat käyttöön kuvan analysointilaajennuksen, asiakastiedot, kuten kontaktin kuva ja nimikkeen kuva, lähetetään konenäön ohjelmointirajapinnalle. Kun asennat tämän laajennuksen, suostut siihen, että tämä rajoitettu määrä tietoja lähetetään konenäön ohjelmointirajapinnalle. Ota huomioon, että voit poistaa kuvan analysointilaajennuksen käytöstä tai poistaa sen asennuksen milloin tahansa, kun haluat keskeyttää tämän toiminnon käytön. Lisätietoja on [Microsoftin luottamuskeskuksessa](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Tarpeet
Kuvavaatimukset:

* Kuvamuodot: JPEG, PNG, GIF, BMP  
* Tiedoston suurin koko: alle 4 Mt  
* Kuvan koko: yli 50 x 50 kuvapistettä  

## <a name="to-enable-image-analyzer"></a>Kuvan analysointitoiminnon ottaminen käyttöön
Kuvan analysointilaajennus sisältyy [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Sinun tarvitsee vain ottaa se käyttöön.

> [!NOTE]  
> Vain järjestelmänvalvojat voivat ottaa kuvan analysointilaajennuksen käyttöön. Varmista, että sinulle on määritetty **pääkäyttäjän** käyttöoikeusjoukko.

1. Ota kuvan analysointilaajennus käyttöön jollakin seuraavista tavoista:

* Avaa nimikkeen tai kontaktin kortti. Valitse ilmoituspalkissa **Analysoi kuvia** ja noudata sitten asetusten ohjattua määritystä.  
* Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Palvelun yhteydet** ja valitse sitten **Kuva-analyysin asetukset**. Valitse **Ota kuvan analysointitoiminto käytötön** -valintaruutu ja noudata sitten asetusten ohjattua määritystä.  

    > [!TIP]  
    > **Kuva-analyysin asetukset** -sivulla voi muuttaa myös määrite-ehdotusten luotettavuustasoa. Jos esimerkiksi haluat käyttää suurempaa luotettavuustasoa, voit antaa korkeamman prosenttiluvun.

## <a name="to-analyze-an-image-of-an-item"></a>Nimikkeen kuvan analysointi
Seuraavaksi kerrotaan, miten analysoidaan kuva, joka oli tuotu ennen kuvan analysointilaajennuksen käyttöönottoa.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.  
2. Valitse ensin nimike ja sitten **Analysoi kuva**-toiminto.  
3. **Kuvan analysoinnin määritteet** -sivulla on esillä havaitut määritteet, luotettavuustaso ja muita tietoja määritteestä. Määritä **suoritettavan toiminnon** vaihtoehdoilla, mitä määritteellä tehdään.  

    > [!TIP]  
    > Voit lisätä määritteen nimen nimikkeen kuvaukseen valitsemalla **Lisää nimikkeen kuvaukseen**. Tämä on kätevä esimerkiksi lisättäessä tietoja nopeasti.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Kontaktihenkilön kuvan analysointi
Seuraavaksi kerrotaan, miten analysoidaan kuva, joka oli tuotu ennen kuvan analysointilaajennuksen käyttöönottoa.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kontaktit** ja valitse sitten liittyvä linkki.  
2. Valitse ensin kontaktihenkilö ja sitten **Analysoi kuva**-toiminto.  
3. Arvioi **Profiilikysely**-pikavälilehdessä ehdotukset ja tee tarvittavat korjaukset.  

## <a name="blacklisting-suggested-attributes"></a>Ehdotettujen määritteiden asettaminen mustalle listalle
Jos analyysi ehdottaa määritettä, jota et halua nähdä, voit asettaa määritteen mustalle listalle. Mieti kuitenkin tarkasti, kun teet sen. Mustalle listalle asetettuja määritteitä ei ehdota myöskään muille nimikkeille tai kontaktihenkilöille. Jos et haluakaan asettaa määritettä mustalle listalle, valitse **Mustalle listalle asetetut määritteet** ja poista määrite sitten luettelosta.

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Oman tilin käyttäminen konenäön ohjelmointirajapintana
Voit käyttää konenäön ohjelmointirajapintana myös omaa tiliäsi, jos haluat esimerkiksi analysoida rajoituksen ylittävän määrän kuvia.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kuvan analysointitoiminnon asetukset** ja valitse sitten liittyvä linkki.  
2. Anna konenäön ohjelmointirajapinnan mukana toimitettu **API:n URI** ja **API-avain**.  

    > [!NOTE]  
    > API:n URI-osoitteen loppuun on lisättävä **/analyze**, jos se puuttuu. Esimerkki: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Kuluvan jakson jäljellä olevien analyysien näyttäminen
Voit tarkistaa, kuinka monta analyysia olet kuluvalla jaksolla tehnyt ja kuinka monta voit vielä tehdä.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kuvan analysointitoiminnon asetukset** ja valitse sitten liittyvä linkki.  
2. **Rajatyyppi**, **Raja-arvo** ja **Suoritetut analyysit** sisältävät hyödyllisiä käyttötietoja.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Kuvan analysointilaajennuksen käytön lopettaminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Palvelun yhteydet** ja valitse sitten **Kuvan analysointitoiminnon asetukset**.  
2. Poista **Ota kuvan analysointitoiminto käyttöön** valintaruudun valinta.  

## <a name="see-also"></a>Katso myös
[Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[Käytön aloittaminen](product-get-started.md)  
