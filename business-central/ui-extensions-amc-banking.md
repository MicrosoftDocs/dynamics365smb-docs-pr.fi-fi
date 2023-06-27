---
title: AMC Banking 365 Fundamentals -laajennuksen käyttäminen
description: 'Tietoa siitä, miten voit helposti vaihtaa tietoja pankkiesi kanssa muuttamalla tietoja niiden edellyttämään muotoon.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bank, format, data'
ms.search.form: '20100, 20101, 20102, 20105, 20106, 20107, 20109,'
ms.date: 09/20/2022
ms.author: bholtorf
---

# <a name="use-the-amc-banking-365-fundamentals-extension"></a>Käytä AMC Banking 365 Fundamentals -laajennusta

AMC Banking 365 Fundamentals -laajennus helpottaa ja tarkentaa tietojen lähettämistä pankkeihin. Laajennus yhdistää [!INCLUDE[prod_short](includes/prod_short.md)]:n ja AMC Banking 365 Fundamentalsin Microsoft Dynamics 365 Business Central -palveluun, joka voi muuntaa pankkitietoja [!INCLUDE[prod_short](includes/prod_short.md)]:sta muodoiksi, joita tarvitaan yli 600 pankissa ympäri maailmaa. Tämä helpottaa esimerkiksi maksujen ja hyvitysten siirtämistä toimittajille syöttämällä maksut [!INCLUDE[prod_short](includes/prod_short.md)]-ohjelmaan ja lataamalla ne sitten pankkiin. Muodot voivat myös tasoittaa pankin täsmäytysprosesseja. Lisätietoja on kohdassa [AMC Banking Microsoft Dynamics 365 Business Centralille](https://www.amcbanking.com/bc-fundamentals/).

> [!NOTE]
> AMC Banking on rakentanut lisälaajennuksia, jotka toimivat [!INCLUDE[prod_short](includes/prod_short.md)]:n kanssa. Tässä ohjeaiheessa kuvataan vain peruslaajennus.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)]in yleisessä versiossa asetetaan ja yhdistetään yleiset palvelut pankkitietojen muuntamiseen mihin tahansa pankkisi vaatimaan muotoon. Pohjois-Amerikan versioissa samaa palvelua voi käyttää maksutiedostojen lähettämiseen sähköisenä rahansiirtona (EFT), esimerkkinä usein käytetty ACH-verkko (Automated Clearing House), joskin prosessi on hieman erilainen.

## <a name="use-our-demonstration-account"></a>Esittelytilin käyttäminen

[!INCLUDE[prod_short](includes/prod_short.md)]:n mukana on esittelytili, jonka avulla voit kokeilla AMC Banking 365 Fundamentals -laajennusta. Microsoft tarjoaa oletusasetukset yhteyden muodostamiseen AMC Bankingiin. Niissä määritetään pankkitilit tietojen saamiseksi [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan sekä muutamia tiedonvaihtomäärityksiä. Voit tarkastella yhteysasetuksia **AMC Bankingin asetus** -sivulla. Laajennus kohdistaa pankkitileille arvot **Pankin nimi**-, **Hyvityksen siirtoviestinrot**-, **Tiliotteen tuontimuoto**- ja **Maksun viennin muoto** -kenttiin pankkitilin korteilla.

Microsoft tarjoaa asetukset, mutta voit kokeilla laajennusta suorittamalla avustetun asennusoppaan. Voit käynnistää oppaan **AMC Banking -määritys** -sivulla valitsemalla **Asetusten ohjattu määritys** -toiminnon.

> [!NOTE]
> Esittelytilillä on joitakin rajoituksia. Kun esimerkiksi muunnat maksuja, muunnetun tiedoston summa ei vastaa todellista summaa. Summa on sen sijaan aina viisi yksikköä valuutasta, jota käytät maksuissa.  

## <a name="setting-up-the-extension"></a>Laajennuksen määrittäminen

Laajennuksen käytön aloittaminen edellyttää vain muutamia helppoja vaiheita, ja avustettu asennusopas muodostaa yhteyden ja käynnistää laajennuksen. Opas tekee asioita, kuten asentaa tiedonsiirtomääritelmät tiliotteiden vienti-/tuontiasetuksille ja käynnistää tilisiirtosanomien numerosarjat.  

### <a name="to-set-up-the-required-permission-sets"></a>Tarvittavien käyttöoikeusjoukkojen määrittäminen

Ennen kuin käyttäjät voivat käyttää tätä laajennusta, sinun täytyy kopioida seuraavat käyttöoikeusjoukot, muokata niitä ja määrittää uudet käyttöoikeusjoukot käyttäjille alkuperäisten sijaan:

* **D365 Perus**
* **D365 Tiiminjäsen**
* **D365 Lue**
* **IntelligentCloudBC**

Lisätietoja on kohdassa [Käyttöoikeuksien joukon kopioiminen](ui-define-granular-permissions.md#to-copy-a-permission-set).

Myönnä kullekin uudelle käyttöoikeuksien joukolle **Luku**-oikeudet **AMC Banking -asetustaulukolle (20101)**. Lisätietoja on kohdassa [Käyttöoikeuksien luominen tai muuttaminen manuaalisesti](ui-define-granular-permissions.md#to-create-a-permission-set).

### <a name="to-connect-the-extension-to-amc-banking"></a>Voit liittää laajennuksen AMC Bankingiin

1. Hanki moduuli ja huoltosuunnitelma AMC Bankingille. Voit tehdä sen käymällä [AMC-lisenssi](https://license.amcbanking.com/register) -sivulla.
2. Valitse [!INCLUDE[prod_short](includes/prod_short.md)]issa ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **AMC Banking -määritys** ja valitse sitten vastaava linkki.  
3. **AMC Banking -määritys**-sivulla valitse **Asetusten ohjattu määritys** -toiminto.
4. Suorita asetusten ohjatun määrityksen oppaan vaiheet.

### <a name="to-connect-bank-accounts-to-the-extension"></a>Pankkitilit voidaan liittää laajennuksen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.
2. Avaa sen pankkitilin kortti, jonka haluat liittää palveluun.
3. Valitse **Pankin nimi** -kentässä pankin tarvitsema muoto.  

   Muodot suodatetaan näyttämään vain ne, jotka ovat olennaisia pankkitilille määritetyn maan/alueen kannalta.
4. Valitse **Hyvityksen siirtoviestinrot** -kentässä numerosarja, jota käytetään maksuille toimitettavia viestejä varten.
5. **Pankin tiliotteen tuontimuoto** ja **Maksun vientimuoto** -kentissä pankin edellyttämät tiedonvaihtomääritykset.

## <a name="use-the-extension"></a>Käytä laajennusta

Tämän laajennuksen käyttäminen on vain asia, jossa tiedot viedään **Maksupäiväkirjat** -sivulle ja lähetetään sitten pankin verkkopalveluun. Lisätietoja on kohdassa [Maksujen suorittaminen pankkitietojen muunnospalvelulla tai SEPA-hyvityksen siirrolla](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).

> [!NOTE]
> Sinun täytyy täyttää **SWIFT-koodi** ja **IBAN**-kentät kunkin pankkitilin osalta.

### <a name="to-export-data-and-submit-it-to-your-bank"></a>Tietojen vieminen ja lähettäminen pankkiin

> [!CAUTION]  
> Kun viet tietoja AMC Banking 365 Fundamentals -laajennuksen avulla, joitakin yritystietoja paljastetaan palvelun tarjoajalle. Palveluntarjoaja, AMC Consult A/S, vastaa näiden tietojen tietosuojasta. Lisätietoja on kohdassa [AMC:n tietosuojakäytäntö](https://go.microsoft.com/fwlink/?LinkId=510158).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten vastaava linkki.
2. Luo ne päiväkirjan rivit, jotka haluat viedä.  

   > [!NOTE]
   > Muista valita jokaiselle riville **Sähköinen maksu** **Pankkimaksun tyyppi** -kentässä.
3. Valitse **Vie**-toiminto.

### <a name="to-import-and-apply-the-converted-file"></a>Muunnetun tiedoston tuominen ja käyttäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksujen täsmäytyskirjauskansio** ja valitse sitten liittyvä linkki.
2. Valitse **Tuo pankkitapahtuma** -toiminto ja valitse sitten muunnettu tiedosto.  

   [!INCLUDE[prod_short](includes/prod_short.md)] luo uuden maksun täsmäytyskirjauskansion, joka sisältää tiedoston tiedot. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

## <a name="see-also"></a>Katso myös

[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
