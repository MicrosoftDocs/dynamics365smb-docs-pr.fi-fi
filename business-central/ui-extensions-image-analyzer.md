---
title: Kuvan analysointilaajennus
description: 'Voit analysoida tällä laajennuksella kontaktihenkilöiden ja nimikkeiden kuvia ja etsiä määritteitä, mikä nopeuttaa niiden määrittämistä Business Central -sovelluksessa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition'
ms.search.form: '2026, 2027, 2029,'
ms.date: 05/19/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Kuvan analysointilaajennus

Kuvan analysointilaajennus havaitsee Azure Cognitive Servicesin konenäön ohjelmointirajapinnan tehokkaalla kuva-analytiikalla määritteet nimikkeille ja kontaktihenkilöille tuoduissa kuvissa, mikä helpottaa kuvien tarkastelua ja määrittämistä. Nimikkeiden määritteet voivat ilmaista esimerkiksi, onko kyse pöydästä vai autosta ja onko se sininen vai punainen. Kontaktihenkilöiden määritteet voivat ilmaista sukupuolen tai iän.

Kuvan analysointitoiminto ehdottaa määritteitä konenäön ohjelmointirajapinnan löytämien tunnisteiden ja luotettavuustasoon perusteella. Se ehdotta oletusarvoisesti määritteitä vain, jos sen luottamus määritteen oikeellisuuteen on vähintään 80 %. Voit määrittää tarvittaessa jonkin toisen luotettavuustason. Lisätietoja tunnisteiden ja luotettavuustason määrittämisestä on ohjeaiheessa [Konenäön ohjelmointirajapinta](https://go.microsoft.com/fwlink/?linkid=851476).  

Kuvan analysointitoiminto on maksuton [!INCLUDE[prod_short](includes/prod_short.md)]issa, mutta tietyn ajanjakson aikana analysoitavien kuvien määrää on rajoitettu. Oletusarvoisesti kuukaudessa saa analysoida 100 kuvaa.

Kun laajennus on otettu käyttöön, kuvan analysointitoiminto suoritetaan aina, kun tuot nimikkeeseen tai kontaktihenkilöön kuvan. Näet määritteet, luottamustason ja tiedot heti ja voit määrittää, miten kutakin määritettä käsitellään. Jos toit kuvia ennen kuvan analysointilaajennuksen käyttöönottoa, sinun on siirryttävä nimikkeeseen tai kontaktikortteihin ja valittava **Analysoi kuva** -toiminto.  

## Tietosuojatiedot

Tämä laajennus käyttää Azure Cognitive Servicesin konenäön ohjelmointirajapintaa. Sen yhdenmukaisuussitoumusten tasot voivat olla erilaiset kuin [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa. Jos otat käyttöön kuvan analysointilaajennuksen, asiakastiedot, kuten kontaktin kuva ja nimikkeen kuva, lähetetään konenäön ohjelmointirajapinnalle. Kun asennat tämän laajennuksen, suostut siihen, että tämä rajoitettu määrä tietoja lähetetään konenäön ohjelmointirajapinnalle. Ota huomioon, että voit poistaa kuvan analysointilaajennuksen käytöstä ja poistaa sen asennuksen milloin tahansa, kun haluat keskeyttää tämän toiminnon käytön. Lisätietoja on [Microsoftin luottamuskeskuksessa](https://go.microsoft.com/fwlink/?linkid=851463).

## Tarpeet

Kuvavaatimukset:

* Kuvamuodot: JPEG, PNG, GIF, BMP  
* Tiedoston suurin koko: alle 4 Mt  
* Kuvan koko: yli 50 x 50 kuvapistettä  

## Ota käyttöön Kuvan analysointilaajennus

Kuvan analysointilaajennus sisältyy [!INCLUDE[prod_short](includes/prod_short.md)]iin. Sinun tarvitsee vain ottaa se käyttöön.

> [!NOTE]  
> Vain järjestelmänvalvojat voivat ottaa kuvan analysointilaajennuksen käyttöön. Varmista, että sinulle on määritetty **pääkäyttäjän** käyttöoikeusjoukko. Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md).

Ota kuvan analysointilaajennus käyttöön jollakin seuraavista toiminnoista:

* Avaa nimikkeen tai kontaktin kortti. Valitse ilmoituspalkissa **Analysoi kuvaa** ja noudata sitten asetusten ohjattua määritystä.  
* Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Palvelun yhteydet** ja valitse sitten **Kuva-analyysin asetukset**. Valitse **Ota kuvan analysointitoiminto käytötön** -valintaruutu ja noudata sitten asetusten ohjattua määritystä.  

    > [!TIP]  
    > **Kuva-analyysin asetukset** -sivulla voi muuttaa myös määrite-ehdotusten luotettavuustasoa. Jos esimerkiksi haluat käyttää suurempaa luotettavuustasoa, voit antaa korkeamman prosenttiluvun.

## Analysoi nimikkeen kuvaa

Seuraavaksi kerrotaan, miten analysoidaan kuva, joka oli tuotu ennen kuvan analysointilaajennuksen käyttöönottoa.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2. Valitse ensin nimike ja sitten **Analysoi kuva**-toiminto.  
3. **Kuvan analysoinnin määritteet** -sivulla on esillä havaitut määritteet, luotettavuustaso ja muita tietoja määritteestä. Käytä **Suoritettava toiminto** -asetuksia määrittääksesi, mitä määritteellä tehdään tai valitse **Lisää nimikkeen kuvaukseen** lisätäksesi määritteen nimen nimikkeen kuvaukseen. Tämä toiminto on kätevä esimerkiksi lisättäessä tietoja nopeasti.

**Suoritettava toiminto** -kentässä on seuraavat asetukset:

| Toiminto | Kuvaus |
| ------ | ----------- |
| *Ohita* | Toimintoja ei suoriteta. |
| *Käytä määritteenä* | Arvo lisätään nimikkeen määritteisiin. Lisätietoja on kohdassa [Nimikemääritteiden muokkaaminen](inventory-how-work-item-attributes.md). |
| *Käytä luokkana* | Valitsemasi arvo lisätään luokaksi. Lisätietoja on kohdassa [Nimikkeiden kategoriointi](inventory-how-categorize-items.md). |
| *Lisää estettyjen kohteiden luetteloon* | Jos analyysi ehdottaa määritettä, jota et halua nähdä, voit estää määritteen. Mieti kuitenkin tarkasti, kun teet sen. Estettyjä määritteitä ei ehdoteta myöskään muille nimikkeille. Jos et haluakaan estää määritettä, voit valita **Katso estettyjä määritteitä** ja poistaa määritteen sitten luettelosta. |

> [!NOTE]  
> Oletusarvoisesti **Nimikkeen määritteet** näyttää määritteet, joiden **Luotettavuuspistemäärä** on korkeampi kuin **Luotettavuuspistemäärän kynnysprosentti**, joka määritellään kohdassa **Kuva-analyysin asetukset**. Jos haluat nähdä kaikki havaitut määritteet, valitse **Näytä kaikki määritteet** -toiminto.

## Analysoi kontaktihenkilön kuva

Seuraavaksi kerrotaan, miten analysoidaan kuva, joka oli tuotu ennen kuvan analysointilaajennuksen käyttöönottoa.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kontaktit** ja valitse sitten vastaava linkki.  
2. Valitse ensin kontaktihenkilö ja sitten **Analysoi kuva**-toiminto.  
3. Arvioi **Profiilikysely**-pikavälilehdessä ehdotukset ja tee tarvittavat korjaukset. Lue lisätietoja kohdasta [Liiketoimintakontaktien luokittelu profiilikyselyiden avulla](marketing-create-contact-profile-questionnaire.md).  

    > [!NOTE]  
    >
    > Konenäön ohjelmointirajapinta palauttaa seuraavat määritteet:
    >
    > * *ikä*
    >
    >     Arvioitu "visuaalinen ikä" vuosissa. Biologisen iän sijaan kuvaa sitä, kuinka vanhalta henkilö näyttää.
    > * *sukupuoli*
    >
    >    Mies tai nainen.
    >
    > Konenäön ohjelmointirajapinta ei palauta ikä- ja sukupuolimääritteiden luottamustasoa.
  
## Käytä omaa konenäön ohjelmointirajapintatiliäsi

Voit käyttää konenäön ohjelmointirajapintana myös omaa tiliäsi, jos haluat esimerkiksi analysoida isomman määrän kuvia kuin mitä oletusintegraatio tarjoaa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kuva-analyysin asetukset** ja valitse sitten vastaava linkki.
2. Anna konenäön ohjelmointirajapinnan mukana toimitettu **API:n URI** ja **API-avain**.  

    > [!NOTE]  
    > API:n URI-osoitteen loppuun on lisättävä **/analyze**, jos se puuttuu. Esimerkiksi: ```https://cronus.api.cognitive.microsoft.com/vision/v2.0/analyze```.

## Kuluvan jakson jäljellä olevien analyysien näyttäminen

Voit tarkistaa, kuinka monta analyysia olet kuluvalla jaksolla tehnyt ja kuinka monta voit vielä tehdä.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kuva-analyysin asetukset** ja valitse sitten vastaava linkki.
2. **Rajatyyppi**-, **Raja-arvo**- ja **Suoritetut analyysit** -kentät sisältävät hyödyllisiä käyttötietoja.  

## Kuvan analysointilaajennuksen käytön lopettaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Palvelun yhteydet** ja valitse sitten **Kuva-analyysin asetukset**.  
2. Poista **Ota kuvan analysointitoiminto käyttöön** -kentän valinta.  

Vaihtoehtoisesti voit poistaa laajennuksen kokonaan. Voit hakea sen aina uudelleen AppSourcesta. Lisätietoja on kohdassa [Laajennusten asentaminen Business Centraliin ja asennusten poistaminen](ui-extensions-install-uninstall.md#uninstall-an-app).  

## Katso myös

[Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md)  
[Nimikkeiden luokitteleminen](inventory-how-categorize-items.md)  
[Liiketoimintakontaktien luokittelu profiilikyselyiden avulla](marketing-create-contact-profile-questionnaire.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
