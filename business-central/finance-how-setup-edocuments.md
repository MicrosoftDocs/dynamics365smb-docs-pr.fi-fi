---
title: Sähköisten asiakirjojen määrittäminen
description: Lisätietoja sähköisten asiakirjojen toimintojen määrittämisestä.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 10/05/2023
ms.author: altotovi
---

# <a name="set-up-e-documents"></a>Sähköisten asiakirjojen määrittäminen

> [!IMPORTANT]
> Sähköisten asiakirjojen ydinmoduuli on kehys. Oletusarvoisesti **Asiakirjan muoto**- ja **Palvelun integrointi** -kenttiä ei ole. Nämä tiedot ovat osa lokalisointisovelluksia, koska ne ovat molemmat paikallisia tarpeita koskevia.

> [!NOTE]
> Versiosta 23.1 lähtien PEPPOL-asiakirjan vakiomuoto on mukana **Asiakirjan muoto** -kentän yleisenä muotona.

Sähköisten asiakirjojen määrityksen ensimmäinen vaihe on määrittää sähköinen asiakirjapalvelu. Tällöin määritetään järjestelmän koko toiminta, koska se liittyy sähköisten asiakirjojen viestintään.

## <a name="set-up-the-e-document-service"></a>Sähköisen asiakirjapalvelun määrittäminen

Määritä sähköinen asiakirjapalvelu alla olevien ohjeiden mukaan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköiset asiakirjapalvelut** ja valitse sitten vastaava linkki.
2. Valitse **Uusi** ja määritä sitten **Yleinen**-pikavälilehden **Sähköinen asiakirjapalvelu** -sivulla kentät alla olevan taulukon mukaan.

    | Kenttä | Kuvaus |
    |-------|-------------|
    | Postinumero | Valitse sähköisen viennin asetuskoodi. |
    | Kuvaus | Anna sähköisen viennin asetusten lyhyt kuvaus. |
    | Asiakirjan muoto | <p>Sähköisen viennin asetusten vientimuoto.</p><p>Tässä kentässä ei oletusarvoisesti ole vaihtoehtoja 1. aallossa.</p> |
    | Palvelun integrointi | Valitse sähköisen viennin määrityksen integrointikoodi. Ainoa vaihtoehto 1. aallossa on **Ei integrointia**. |
    | Käytä eräkäsittelyä | Määritä, käyttääkö palvelu eräkäsittelyä vientiin. |

4. Määritä **Tuodut parametrit** -pikavälilehdessä alla olevassa taulukossa kuvatut kentät.

    | Kenttä | Kuvaus |
    |-------|-------------|
    | Tarkista vastaanottava yritys | Määritä, onko vastaanottavan yrityksen tiedot vahvistettava tuonnin aikana. |
    | Selvitä mittayksikkö | Määritä, onko mittayksikkö ratkaistava tuonnin aikana. |
    | Hae nimikeviittaus | Määritä, etsitäänkö tuotetta tuoteviitteen perusteella tuonnin aikana. |
    | Hakunimike GTIN | Määritä, etsitäänkö tuotetta GTIN-numeron perusteella tuonnin aikana. |
    | Hakutilin yhdistämismääritys | Määritä, etsitäänkö tiliä **tilin yhdistämismäärityksessä** tuonnin aikana saapuvan tekstin perusteella. |
    | Tarkista rivialennus | Määritä, tarkistetaanko rivialennus tuonnin aikana. |
    | Kohdista laskualennus | Määritä, sovelletaanko tuonnin aikana laskualennusta. |
    | Tarkista yhteissummat | Määritä, tarkistetaanko laskun loppusumma tuonnin aikana. |
    | Päivitä tilaus | Määritä, onko vastaava ostotilaus päivitettävä. |
    | Luo päiväkirjarivit | Määritä, onko ostoasiakirjan sijaan luotava päiväkirjarivi. Valitse tämä vaihtoehto, jos haluat käyttää päiväkirjoja laskujen kohteena. |
    | Yleisen päiväkirjan mallin nimi | Määritä kirjauskansion rivin luonnissa käytettävän yleisen päiväkirjamallin nimi. Tämä kenttä on käytettävissä, jos haluat käyttää päiväkirjoja laskujen kohteena. |
    | Yleisen päiväkirjan erän nimi | Määritä kirjauskansion rivin luonnissa käytettävän yleisen päiväkirjaerän nimi. Tämä kenttä on käytettävissä, jos haluat käyttää päiväkirjoja laskujen kohteena. |
    | Automaattinen tuonti | Määritä, tuodaanko asiakirjat palvelusta automaattisesti. |
    | Erän aloitusaika | Määritä tuontitöiden aloitusaika. |
    | Minuuttia suoritusten välillä | Määritä tuontitöiden suorittamisen välisen minuuttimäärän. |

Jos olet määrittänyt lokalisoinnissa **Tiedonsiirtomääritys**-muodon, voit lisätä rivin jokaiselle tarvittavalle asiakirjatyypille. Valitse kuitenkin ensin **Asiakirjatyyppi**-vaihtoehto jokaiselle tarvitsemallesi riville. Valitse kullekin tietotyypille **Tuo tiedonsiirtomäärityksen koodi**- tai **Vie tiedonsiirtomäärityksen koodi** -arvo, jota haluat käyttää.

Jos lopulta et käytä **Tiedonsiirtomääritys**-muotoa, voit määrittää muodot **Viennin yhdistämismääritys**- tai **Tuonnin yhdistämismääritys** -rivien avulla. Niissä voit etsiä taulukot ja kentät, joita käytetään tarvittavien muutossääntöjen käyttämisessä ja määrittämisessä.

## <a name="set-up-a-document-sending-profile"></a>Asiakirjan lähetyksen profiilin määrittäminen

Voit määrittää kullekin asiakkaalle myyntiasiakirjojen lähettämisen ensisijaisen tavan. Näin lähetysvaihtoehtoa ei tarvitse valita aina, kun **Kirjaa ja lähetä** -toiminto valitaan. **Asiakirjan lähetyksen profiilit** -sivulla voi määrittää eri lähetyksen profiileja, joista voit valita asiakkaan kortin **Asiakirjan lähetyksen profiili** -kentässä. Valitse **Oletus**-valintaruutu, kun haluat, että asiakirjan lähetyksen profiili on kaikkien asiakkaiden oletusprofiili lukuun ottamatta niitä asiakkaita, joiden **Asiakirjan lähetyksen profiili** -kenttä on määritetty toiselle lähetyksen profiilille.

Tätä toimintoa käytetään määritettäessä sähköisen laskutuksen automaatio. Kun valitset **Kirjaa ja lähetä** -toiminnon myyntiasiakirjassa, näkyviin tulee **Kirjaa ja lähetä vahvistus** -valintaikkuna, jossa näkyy käytetty lähetyksen profiili. Se on joko asiakkaalle määritetty profiili tai kaikille asiakkaille yhteinen oletusprofiili.

Alla olevien vaiheiden avulla voit määrittää asiakirjan lähetyksen profiilin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakirjan lähetyksen profiili** ja valitse aiheeseen liittyvä linkki.
2. Valitse **Asiakirjan lähetyksen profiilit** -sivulla **Uusi**.
3. Anna **Yleinen**-pikavälilehdessä vaaditut tiedot.
4. Määritä **Lähetysvaihtoehdot**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.

    | Kenttä | Kuvaus |
    |-------|-------------|
    | Sähköinen asiakirja | Määritä, lähetetäänkö asiakirja sähköisenä asiakirjana, jonka asiakas voi tuoda omaan järjestelmäänsä, kun valitset **Kirjaa ja lähetä** -painikkeen. Tätä vaihtoehtoa voi käyttää, jos myös **Muoto**- tai **Sähköinen asiakirjapalvelun työnkulkukoodi** -kenttä on määritetty. Vaihtoehtoisesti tiedoston voi tallentaa levylle. |
    | Muoto | Määritä sähköisen asiakirjan lähettämisen muoto. Tämä kenttä on pakollinen, jos valitset **Document Exchange -palvelun kautta** -arvon **Sähköinen asiakirja** -kentässä. |
    | Sähköinen asiakirjapalvelun työnkulkukoodi | Määritä asiakirjojen lähettämisessä käytettävä sähköisen palvelun työnkulku. Tämä kenttä on pakollinen, jos valitset **Laajennettu sähköisten asiakirjojen palvelutyönkulku** -arvon **Sähköinen asiakirja** -kentässä. |

    > [!NOTE]
    > Jos valitset **Laajennettu sähköisten asiakirjojen palvelutyönkulku** -kohdan **Sähköinen asiakirja** -kentässä, sähköisten asiakirjojen työnkulun määritys on oltava jo tehty.

## <a name="set-up-the-workflow"></a>Työnkulun määrittäminen

Alla olevien vaiheiden avulla voit määrittää työnkulun, jota käytetään sähköisen asiakirjan toiminnossa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulkumallit** ja valitse sitten vastaava linkki.
2. Jos **Sähköisen asiakirjan työnkulkumallit** -kohtaa ei löydy **Työnkulkumallit**-sivulta, valitse **Palauta Microsoft-mallit**. **Sen jälkeen pitäisi näkyä sähköisen asiakirjan työnkulkumallit**. Sulje sivu.
3. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut** ja valitse sitten vastaava linkki.
4. Suorita **Uusi työnkulku mallista** -toiminto, jos haluat valita mallin sähköisten asiakirjojen prosessia varten. Käytettävissä olevat mallit ovat **Lähetä yhteen palveluun** ja **Lähetä useisiin palveluihin**.
5. Valitse **OK**, jos haluat viimeistellä työnkulun asetuksen.
6. Valitse **Vastaus**-kentässä **Lähetä sähköinen asiakirja asetuksen avulla**, jos haluat määrittää työnkulun vastaukset.
7. Valitse vaihtoehtona luotu sähköinen asiakirjapalvelu. Valitse **OK** ja ota työnkulku käyttöön.

> [!NOTE]
> Voit luoda oman työnkulun sähköisille asiakirjoille ilman ennalta määritettyjä työnkulkumalleja. Jos palveluita on enemmän, voit käyttää eri työnkulkuja.

## <a name="set-up-a-retention-policy-for-e-documents"></a>Sähköisten asiakirjojen säilytyskäytäntöjen määrittäminen

Sähköisiä asiakirjoja voivat koskea erilaiset paikalliset säädökset, jotka liittyvät sähköisten asiakirjojen säilytysjaksoon. Tämän vuoksi säilytyskäytännön asetukset on lisätty kaikkiin tärkeisiin tietoihin, jotka liittyvät sähköisiin asiakirjoihin. Järjestelmänvalvojat voivat määrittää säilytyskäytännöt, jotka määrittävät, miten usein Dynamics 365 Business Central poistaa sähköisiin asiakirjoihin liittyvät vanhentuneet tietueet. Lisätietoja säilytyskäytännöistä on kohdassa [Säilytyskäytäntöjen määrittäminen](admin-data-retention-policies.md).

Voit määrittää sähköiseen asiakirjaan liittyvät säilytyskäytännöt alla olevien ohjeiden avulla.

1. Suorita **Sähköiset asiakirjapalvelut** -sivulla **Säilytyskäytäntö**-toiminto.
2. Kun toiminto on valmis, valitse jokin seuraavista määritettävästä säilytyskäytännöistä:

    - Sähköisen asiakirjan loki
    - Sähköisen asiakirjan integrointiloki
    - Sähköisen asiakirjan yhdistämismääritysloki
    - Sähköisen asiakirjan tietojen tallennustila

## <a name="see-also"></a>Katso myös

[Sähköisten asiakirjojen käyttäminen Business Centralissa](finance-how-use-edocuments.md)  
[Sähköisten asiakirjojen laajentaminen Business Centralissa](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Taloushallinto](finance.md)  
[Lasku – myynti](sales-how-invoice-sales.md)  
[Ostojen kirjaaminen ostolaskujen ja tilausten avulla](purchasing-how-record-purchases.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
