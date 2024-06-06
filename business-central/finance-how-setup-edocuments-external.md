---
title: Sähköisten asiakirjojen yhdistimen määrittäminen ulkoisten päätepisteiden kanssa
description: 'Tässä artikkelissa kerrotaan, kuinka sähköiset asiakirjat-toiminto määritetään, kun se on yhdistetty ulkoisiin päätepisteisiin.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, access-point, endpoint'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 12/13/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="set-the-e-documents-connector-with-external-endpoints"></a>Sähköisten asiakirjojen yhdistimen määrittäminen ulkoisten päätepisteiden kanssa

Tässä artikkelissa kerrotaan, kuinka sähköiset asiakirjat-toiminto määritetään, kun se on yhdistetty ulkoisiin päätepisteisiin.

Ennen kuin käytät tässä artikkelissa kuvattuja toimintoja, asenna **Sähköiset asiakirjat -käynnistin ulkoisilla päätepisteillä** -sovellus yleisen **Sähköisen asiakirjan ydin** -sovelluksen päälle. Tätä sovellusta voidaan käyttää oletusintegraatioon ulkoisten (kolmannen osapuolen) tukiasemien kanssa sähköisten asiakirjojen työnkulun automatisoimiseksi. Koska tämä sovellus edustaa vain osaa valituista käynnistimistä, et rajoitu sen olemassa oleviin integraatioihin. Suurin osa käynnistimistä on saatavilla tulevaisuudessa AppSourcessa.

## <a name="set-up-the-connection"></a>Yhteyden määrittäminen

Aloita määritys noudattamalla [Sähköisen asiakirjan ydinsovelluksen](finance-how-setup-edocuments.md) ohjeita. Kun olet suorittanut nämä vaiheet, palaa tähän artikkeliin ja suorita seuraavat vaiheet:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköiset asiakirjapalvelut** ja valitse sitten vastaava linkki.
2. Valitse **Palveluintegrointi**-kentässä yksi integrointikoodeista, joita tarjotaan päätepisteen palveluasetuksiin.
3. Valitse **Määritä palvelun integrointi**.
4. Valitse **Sähköisen asiakirjan ulkoisen yhteyden määritys** -sivulla **Pyydä valtuutuskoodi**. Sinut ohjataan ulkoisen palvelun valtuutuksen verkkosivulle ja sinua pyydetään antamaan kirjautumistietosi.
5. Kopioi valtuutuskoodi **Anna valtuutuskoodi** -kenttään.
6. Valitse **Päivitä käyttöoikeustunnus** varmistaaksesi, että voit päivittää tunnuksen.

    > [!NOTE]
    > Tämä yhteys edellyttää yhteydenpitoa ulkopuolisten palveluntarjoajien kanssa, jotka saattavat olla lisämaksullisia ja edellyttävät sopimuksia heidän kanssaan. Ota yhteyttä palveluntarjoajiin saadaksesi kaikki tarvittavat tunnistetiedot.

7. Täytä **Sähköisen asiakirjan ulkoisen yhteyden asetukset** -sivulla seuraavat kentät:

    | Kentän nimi | Kuvaus |
    |---|---|
    | FileAPI:n URL-osoite | Määritä tiedoston ohjelmointirajapinnan URL-osoite. |
    | Tiedosto-osan URL-osoite | Määritä tiedosto-osan URL-osoite. |
    | DocumentAPI:n URL-osoite | Määritä asiakirjan ohjelmointirajanpinnan URL-osoite. |
    | Yrityksen tunnus | Määritä yrityksen tunnus. |
    | Lähetystila | Määritä lähetystila. Voit valita tilaksi **Tuotanto**, **Testi** tai **Sertifiointi**. |

    > [!NOTE]
    > Pyydä palveluntarjoajaltasi kaikki aikaisemmat tiedot yhteyden muodostamiseksi tukiasemaan.

## <a name="set-up-company-information"></a>Yrityksen tietojen määrittäminen

Ennen kuin alat käyttää sähköisiä asiakirjoja, päivitä **Yritystiedot**-sivusi suorittamalla seuraavat vaiheet:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yrityksen tiedot** ja valitse sitten vastaava linkki.
2. Tavallisten kenttien täyttämisen lisäksi sinun tulee täyttää myös seuraavat kentät:

    | Kentän nimi | Kuvaus |
    |---|---|
    | SWIFT-koodi | Määritä oletuspankkitilisi SWIFT-koodi (kansainvälisen pankkitunnisteen). |
    | Pankkikonttorin nro | Määritä nelinumeroinen pankin haarakonttorin numero. |
    | ALV-rekisteröintinumero. | Määritä yrityksen arvonlisäverorekisterinumero (ALV). |

3. Sulje sivu.

## <a name="set-up-customers-to-receive-e-documents"></a>Määritä asiakkaat vastaanottamaan sähköisiä asiakirjoja

Jotta asiakkaat voivat vastaanottaa sähköisiä asiakirjojasi, suorita seuraavat vaiheet:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Avaa **asiakas**-kortti.
3. Määritä **GLN**-kentässä tavallisten kenttien täyttämisen lisäksi asiakas sähköisten asiakirjojen lähettämisen yhteydessä.
4. Merkitse **Käytä GLN:ää sähköisissä asiakirjoissa** -kenttä osoittaaksesi, käytetäänkö maailmanlaajuista sijaintinumeroa (GLN) osapuolen tunnistenumerona sähköisissä asiakirjoissa.
5. Sulje sivu.

## <a name="other-setup"></a>Muut asetukset

Ennen kuin alat käsitellä sähköisiä asiakirjoja, määritä sähköisten asiakirjojen **työnkulut** ja **asiakirjan lähetyksen profiilit** käyttämään työnkulkujasi. Kun palveluyhteys on muodostettu, voit aloittaa sähköisen asiakirjaratkaisusi käytön.

## <a name="available-service-providers"></a>Saatavilla olevat palveluntarjoajat

Microsoft haluaa kannustaa liityntäpisteiden tarjoajia lisäämään yhdistimiensä päälle **Sähköisen asiakirjan ydin** -kehyksen.

Tällä hetkellä Pagero on ainoa tukiaseman tarjoaja, joka kuuluu tämän järjestelmän piiriin. Microsoftilla ei ole sopimusvelvoitteita Pageron kanssa. Siksi sinun on tehtävä sopimus heidän kanssaan saadaksesi kaikki tarvittavat tunnistetiedot.

Päivitämme tätä luetteloa sitä mukaa, kun saamme uusia sähköisten asiakirjojen vaihtotukipisteiden tarjoajia.

## <a name="see-also"></a>Katso myös

[Sähköisten asiakirjojen määrittäminen Business Centralissa](finance-how-setup-edocuments.md)  
[Sähköisten asiakirjojen käyttäminen Business Centralissa](finance-how-use-edocuments.md)  
[Sähköisten asiakirjojen laajentaminen Business Centralissa](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Taloushallinto](finance.md)  
[Lasku – myynti](sales-how-invoice-sales.md)  
[Ostojen kirjaaminen ostolaskujen ja tilausten avulla](purchasing-how-record-purchases.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
