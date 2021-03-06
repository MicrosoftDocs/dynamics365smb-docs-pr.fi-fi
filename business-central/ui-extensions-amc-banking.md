---
title: AMC Banking 365 Fundamentals -siirron käyttäminen | Microsoft Docs
description: Voit helposti vaihtaa tietoja pankkiesi kanssa muuttamalla tietoja niiden edellyttämään muotoon.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: bank, format, data
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: e9c7e20f73b154eeb4c9f47d9100222e0723c42f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773503"
---
# <a name="using-the-amc-banking-365-fundamentals-extension"></a>AMC Banking 365 Fundamentals -laajennuksen käyttäminen
AMC Banking 365 Fundamentals -laajennus helpottaa ja tarkentaa tietojen lähettämistä pankkeihin. Laajennus yhdistää [!INCLUDE[prod_short](includes/prod_short.md)]:n ja AMC Banking 365 Fundamentalsin Microsoft Dynamics 365 Business Central -palveluun, joka voi muuntaa pankkitietoja [!INCLUDE[prod_short](includes/prod_short.md)]:sta muodoiksi, joita tarvitaan yli 600 pankissa ympäri maailmaa. Tämä helpottaa esimerkiksi maksujen ja hyvitysten siirtämistä toimittajille syöttämällä maksut [!INCLUDE[prod_short](includes/prod_short.md)]-ohjelmaan ja lataamalla ne sitten pankkiin. Muodot voivat myös tasoittaa pankin täsmäytysprosesseja. Lisätietoja on kohdassa [AMC Banking Microsoft Dynamics 365 Business Centralille](https://www.amcbanking.com/bc-fundamentals/).

> [!Note]
> AMC Banking on rakentanut lisälaajennuksia, jotka toimivat [!INCLUDE[prod_short](includes/prod_short.md)]:n kanssa. Tässä ohjeaiheessa kuvataan vain peruslaajennus.

## <a name="using-our-demonstration-account"></a>Esittelytilin käyttäminen
[!INCLUDE[prod_short](includes/prod_short.md)]:n mukana on esittelytili, jonka avulla voit kokeilla AMC Banking 365 Fundamentals -laajennusta. Microsoft tarjoaa oletusasetukset yhteyden muodostamiseen AMC Bankingiin. Niissä määritetään pankkitilit tietojen saamiseksi [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan sekä muutamia tiedonvaihtomäärityksiä. Voit tarkastella yhteysasetuksia **AMC Bankingin asetus** -sivulla. Laajennus kohdistaa pankkitileille arvot **Pankin nimi**-, **Hyvityksen siirtoviestinrot**-, **Tiliotteen tuontimuoto**- ja **Maksun viennin muoto** -kenttiin pankkitilin korteilla.

Microsoft tarjoaa asetukset, mutta voit kokeilla laajennusta suorittamalla avustetun asennusoppaan. Voit käynnistää oppaan **AMC Banking -määritys** -sivulla valitsemalla **Asetusten ohjattu määritys** -toiminnon.

> [!Note]
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

Myönnä kullekin uudelle käyttöoikeuksien joukolle **Luku**-oikeudet **AMC Banking -asetustaulukolle (20101)**. Lisätietoja on kohdassa [Käyttöoikeuksien luominen tai muuttaminen manuaalisesti](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-connect-the-extension-to-amc-banking"></a>Voit liittää laajennuksen AMC Bankingiin
1. Hanki moduuli ja huoltosuunnitelma AMC Bankingille. Voit tehdä sen käymällä [AMC-lisenssi](https://license.amcbanking.com/register) -sivulla.
2. Valitse [!INCLUDE[prod_short](includes/prod_short.md)]:ssa ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **AMC Banking -asetukset** ja valitse sitten liittyvä linkki.  
3. **AMC Banking -määritys**-sivulla valitse **Asetusten ohjattu määritys** -toiminto.
4. Suorita asetusten ohjatun määrityksen oppaan vaiheet.

### <a name="to-connect-bank-accounts-to-the-extension"></a>Pankkitilit voidaan liittää laajennuksen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilit** ja valitse sitten liittyvä linkki.
2. Avaa sen pankkitilin kortti, jonka haluat liittää palveluun.
3. Valitse **Pankin nimi** -kentässä pankin tarvitsema muoto.  

   Muodot suodatetaan näyttämään vain ne, jotka ovat olennaisia pankkitilille määritetyn maan/alueen kannalta.
4. Valitse **Hyvityksen siirtoviestinrot** -kentässä numerosarja, jota käytetään maksuille toimitettavia viestejä varten.
5. **Pankin tiliotteen tuontimuoto** ja **Maksun vientimuoto** -kentissä pankin edellyttämät tiedonvaihtomääritykset.

## <a name="using-the-extension"></a>Laajennuksen käyttäminen
Tämän laajennuksen käyttäminen on vain asia, jossa tiedot viedään **Maksupäiväkirjat** -sivulle ja lähetetään sitten pankin verkkopalveluun. Lisätietoja on kohdassa [Maksujen suorittaminen pankkitietojen muunnospalvelulla tai SEPA-hyvityksen siirrolla](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).

> [!Note]
> Sinun täytyy täyttää **SWIFT-koodi** ja **IBAN**-kentät kunkin pankkitilin osalta.

### <a name="to-export-data-and-submit-it-to-your-bank"></a>Tietojen vieminen ja lähettäminen pankkiin
> [!CAUTION]  
>  Kun viet tietoja AMC Banking 365 Fundamentals -laajennuksen avulla, joitakin yritystietoja paljastetaan palvelun tarjoajalle. Palveluntarjoaja, AMC Consult A/S, vastaa näiden tietojen tietosuojasta. Lisätietoja on kohdassa [AMC:n tietosuojakäytäntö](https://go.microsoft.com/fwlink/?LinkId=510158).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten liittyvä linkki.
2. Luo ne päiväkirjan rivit, jotka haluat viedä.  

   > [!Note]
   > Muista valita jokaiselle riville **Sähköinen maksu** **Pankkimaksun tyyppi** -kentässä.
3. Valitse **Vie**-toiminto.

### <a name="to-import-and-apply-the-converted-file"></a>Muunnetun tiedoston tuominen ja käyttäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksujen täsmäytyskirjauskansio** ja valitse sitten liittyvä linkki.
2. Valitse **Tuo pankkitapahtuma** -toiminto ja valitse sitten muunnettu tiedosto.  

   [!INCLUDE[prod_short](includes/prod_short.md)] luo uuden maksun täsmäytyskirjauskansion, joka sisältää tiedoston tiedot. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

## <a name="see-also"></a>Katso myös
[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]