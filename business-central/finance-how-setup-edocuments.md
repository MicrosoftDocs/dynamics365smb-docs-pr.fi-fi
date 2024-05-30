---
title: Sähköisten asiakirjojen määrittäminen
description: Lisätietoja sähköisten asiakirjojen toimintojen määrittämisestä.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 05/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="set-up-e-documents"></a>Sähköisten asiakirjojen määrittäminen

> [!IMPORTANT]
> Sähköisten asiakirjojen ydinmoduuli on kehys. Oletusarvoisesti **Palvelun integrointi** -kenttää ei ole. Jos löydät oletusarvoisesti  **Dokumenttimuoto** -vaihtoehdot, ota huomioon, että ne tarjotaan esimerkkinä ja että lokalisoinnin on tarjottava yksityiskohtainen muoto. Nämä tiedot ovat osa lokalisointisovelluksia, koska ne ovat paikallisia tarpeita koskevia.

> [!NOTE]
> Versiosta 23.2 lähtien PEPPOL-asiakirjan vakiomuoto on mukana **Asiakirjan muoto** -kentän yleisenä muotona. Muista, että et todennäköisesti voi käyttää tätä muotoa sellaisenaan. Se on W1-muoto, joka on tarkoitettu osoittamaan, kuinka tätä ominaisuutta käytetään. Suosittelemme, että testaat olemassa olevaa PEPPOL-muotoa ennen kuin alat käyttää tätä muotoa.

Sähköisten asiakirjojen määrityksen ensimmäinen vaihe on määrittää sähköinen asiakirjapalvelu. Tällöin määritetään järjestelmän koko toiminta, koska se liittyy sähköisten asiakirjojen viestintään.

## <a name="set-up-the-e-document-service"></a>Sähköisen asiakirjapalvelun määrittäminen

Määritä sähköinen asiakirjapalvelu alla olevien ohjeiden mukaan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköiset asiakirjapalvelut** ja valitse sitten vastaava linkki.
2. Valitse **Uusi** ja määritä sitten **Yleinen**-pikavälilehden **Sähköiset asiakirjapalvelut** -sivulla kentät alla olevan taulukon mukaan.

    | Kenttä | Kuvaus |
    |-------|-------------|
    | Postinumero | Valitse sähköisen viennin asetuskoodi. |
    | Kuvaus | Anna sähköisen viennin asetusten lyhyt kuvaus. |
    | Asiakirjan muoto | <p>Sähköisen viennin asetusten vientimuoto.</p><p>Tässä kentässä on oletusarvoisesti kaksi vaihtoehtoa. Voit valita **PEPPOL BIS 3** yleiseksi koodipohjaiseksi muodoksi tai **tiedonvaihdon** kun sinun on määritettävä ennalta tietyn muotoiset esiasiakirjat **Tietojen vaihdon määrityksen** pikavälilehdellä.</p> |
    | Palvelun integrointi | Valitse sähköisen viennin määrityksen integrointikoodi. Ainoa vaihtoehto 1. aallossa on **Ei integrointia**. |
    | Käytä eräkäsittelyä | Määritä, käyttääkö palvelu eräkäsittelyä vientiin. |

3. Määritä **Tuodut parametrit** -pikavälilehdessä alla olevassa taulukossa kuvatut kentät.

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

4. Jos valitsit **Tiedonvaihto**  **Dokumenttimuoto** -kentässä  **Yleiset**-pikavälilehdellä, aseta seuraavat kentät  **Tietojen vaihdon määritys** -pikavälilehdellä.

    | Kenttä | Kuvaus |
    |-------|-------------|
    | Asiakirjatyyppi | Määritä asiakirjatyyppi, joka käyttää tiedonsiirtoa tietojen tuontiin ja vientiin. Esimerkkejä ovat **myyntilasku**, **myynnin hyvityslasku** ja **ostolasku**. |
    | Tuo tiedonsiirtomäärityksen koodi | Määritä tietojen tuonnissa käytettävä tiedonsiirtokoodi. Käytä tätä kenttää vain saadaksesi asiakirjan ostoprosessissa. |
    | Vie tiedonsiirtomäärityksen koodi | Määritä tietojen viennissä käytettävä tiedonsiirtokoodi. Käytä tätä kenttää vain asiakirjojen toimittamiseen myyntiprosessissa. |

> [!NOTE]
> PEPPOL-formaatille on valmisteltu tiedonvaihtomääritykset, jotka liittyvät vakiomyynti- ja ostotositteeseen. Et kuitenkaan todennäköisesti voi käyttää näitä määritelmiä sellaisenaan. Ne ovat kaikki W1-muotoa, joka on tarkoitettu osoittamaan, kuinka tätä ominaisuutta käytetään. Suosittelemme, että testaat olemassa olevaa PEPPOL-muotoa ennen kuin alat käyttää niitä.

Jos olet määrittänyt lokalisoinnissa **Tiedonsiirtomääritys**-muodon, voit lisätä rivin jokaiselle tarvittavalle asiakirjatyypille. Lisää rivejä, jotka vastaavat W1 PEPPOL -muodon oletustiedonvaihtoesimerkkiä. Valitse kuitenkin ensin **Asiakirjatyyppi**-vaihtoehto jokaiselle tarvitsemallesi riville. Valitse kullekin tietotyypille **Tuo tiedonsiirtomäärityksen koodi**- tai **Vie tiedonsiirtomäärityksen koodi** -arvo, jota haluat käyttää.

Jos et käytä **Tiedonsiirtomääritys**-muotoa, voit luoda ja määrittää muotoja  [käyttöliittymän](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments) avulla. Säädä tietoja **Viennin yhdistämismäärityksessä** ja **Tuonnin yhdistämismäärityksessä** , joista löydät taulukot ja kentät muunnossääntöjen määrittämistä varten. Tässä tapauksessa sinun on lisättävä muotoosi liittyvä uusi vaihtoehto  **Asiakirjan muoto** -kenttään.  

### <a name="supported-document-types"></a>Tuetut asiakirjatyypit

Tuetut asiakirjatyypit perustuvat valittuun **asiakirjamuotoon**. Tarkista tuetut asiakirjatyypit valitsemalla **Sähköiset asiakirjapalvelut** -sivulla **Tuetut asiakirjatyypit** . **Sähköisen tiedostopalvelun tuetut lähdeasiakirjatyypit** avautuu ja **Lähdeasiakirjatyyppi**-sarakkeessa voit valita erilaisia asiakirjatyyppejä, jotta ne ovat tuettuja käyttämäsi muodon mukaan. Varmista, että et käytä asiakirjatyyppiä, jos kyseistä asiakirjaa ei ole valittu tällä sivulla.   

## <a name="set-up-a-document-sending-profile"></a>Asiakirjan lähetyksen profiilin määrittäminen

Voit määrittää kullekin asiakkaalle myyntiasiakirjojen lähettämisen ensisijaisen tavan. Näin lähetysvaihtoehtoa ei tarvitse valita aina, kun valitset **Kirjaa ja lähetä** -toiminnon. **Asiakirjan lähetyksen profiilit** -sivulla voi määrittää eri lähetyksen profiileja, joista voit valita asiakkaan kortin **Asiakirjan lähetyksen profiili** -kentässä. Valitse **Oletus**-valintaruutu, kun haluat, että asiakirjan lähetyksen profiili on kaikkien asiakkaiden oletusprofiili lukuun ottamatta niitä asiakkaita, joiden **Asiakirjan lähetyksen profiili** -kenttä on määritetty toiselle lähetyksen profiilille.

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
4. Valitse **Uusi työnkulku mallista** -toiminto, jos haluat valita mallin sähköisten asiakirjojen prosessia varten. Käytettävissä olevat mallit ovat **Lähetä yhteen palveluun** ja **Lähetä useisiin palveluihin**.
5. Valitse **OK**, jos haluat viimeistellä työnkulun asetuksen.
6. Valitse **Vastaus**-kentässä **Lähetä sähköinen asiakirja asetuksen avulla**, jos haluat määrittää työnkulun vastaukset.
7. Valitse vaihtoehtona luotu sähköinen asiakirjapalvelu. Valitse **OK** ja ota työnkulku käyttöön.

> [!NOTE]
> Voit luoda oman työnkulun sähköisille asiakirjoille ilman ennalta määritettyjä työnkulkumalleja. Jos palveluita on enemmän, voit käyttää eri työnkulkuja.

Jos haluat käyttää enemmän työnkulkuja, määritä ne eri asiakkaiden asiakirjojen lähetysprofiilien kautta. Kun määrität työnkulkua, määritä asiakirjan lähetysprofiili **Ehdolla** -sarakkeessa  **Työnkulun vaiheet** -pikavälilehdessä, koska sinulla ei voi olla kahta palvelua, jotka käyttävät samaa asiakirjan lähetysprofiilia työnkuluissa.

Kun määrität työnkulkusi **Työnkulut**-sivulla, osoita **Ehdolla**-kenttään **Työnkulun vaiheet** -pikavälilehdessä. Valitse  **Tapahtumaehdot** -sivun  **Suodatin**-kentästä asiakirjan lähetysprofiili, jota haluat käyttää.

## <a name="set-up-a-retention-policy-for-e-documents"></a>Sähköisten asiakirjojen säilytyskäytäntöjen määrittäminen

Sähköisiä asiakirjoja voivat koskea erilaiset paikalliset säädökset, jotka liittyvät sähköisten asiakirjojen säilytysjaksoon. Tämän vuoksi säilytyskäytännön asetukset on lisätty kaikkiin tärkeisiin tietoihin, jotka liittyvät sähköisiin asiakirjoihin. Järjestelmänvalvojat voivat määrittää säilytyskäytännöt, jotka määrittävät, miten usein Dynamics 365 Business Central poistaa sähköisiin asiakirjoihin liittyvät vanhentuneet tietueet. Lisätietoja säilytyskäytännöistä on kohdassa [Säilytyskäytäntöjen määrittäminen](admin-data-retention-policies.md).

Voit määrittää sähköiseen asiakirjaan liittyvät säilytyskäytännöt alla olevien ohjeiden avulla.

1. Suorita **Sähköiset asiakirjapalvelut** -sivulla **Säilytyskäytäntö**-toiminto.
2. Kun toiminto on valmis, valitse jokin seuraavista määritettävästä säilytyskäytännöistä:

    - Sähköisen asiakirjan loki
    - Sähköisen asiakirjan integrointiloki
    - Sähköisen asiakirjan yhdistämismääritysloki
    - Sähköisen asiakirjan tietojen tallennustila

## <a name="e-documents-demo-data"></a>E-asiakirjan demotiedot

> [!NOTE]
> Business Centralin versiosta 24.0 voidaan määrittää demotietoja E-asiakirjoille.

Microsoft on luonut uuden demomoduulin sähköisiä asiakirjoja varten, jotta **E-asiakirjojen** testaus- ja esittelyominaisuuksien käyttö on helpompaa. Voit ottaa tämän moduulin käyttöön noudattamalla seuraavia vaiheita:  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Contoso-demotyökalu** ja valitse sitten vastaava linkki.  
2.  Ennen kuin **E-asiakirjan Contoso-moduuli** otetaan käyttöön riippuvuussuhteiden takia, seuraavat moduulit on otettava käyttöön: **Yleinen moduuli** ja **Fyysisen varaston moduuli**. 
3.  Kun olet ottanut nämä moduulit käyttöön, valitse **E-asiakirjan Contoso-moduuli** ja valitse **Luo**-toiminto. 
4.  Toimi vaiheiden mukaisesti.  
5.  Sulje sivu.   

Kun käytössä oleva moduuli on otettu käyttöön, uudet demonimikkeet on luotu, kuusi sähköistä asiakirjaa on tuotu (Peppol BIS 3:een perustuen) ja **E-asiakirjapalvelut** on jo määritetty luotujen työnkulkujen avulla.  

## <a name="see-also"></a>Katso myös

[Tietoja sähköisten asiakirjojen käytöstä myynnissä](finance-how-use-edocuments.md)    
[Tietoja sähköisten asiakirjojen käytöstä ostossa](finance-how-use-edocuments-purchase.md)  
[Sähköisten asiakirjojen laajentaminen Business Centralissa](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Taloushallinto](finance.md)    
[Myynnin laskutus](sales-how-invoice-sales.md)    
[Ostojen kirjaaminen ostolaskujen ja tilausten avulla](purchasing-how-record-purchases.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
