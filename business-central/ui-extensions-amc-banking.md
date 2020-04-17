---
title: AMC Banking 365 -perusteiden laajennuksen käyttäminen | Microsoft Docs
description: Voit helposti vaihtaa tietoja pankkiesi kanssa muuttamalla tietoja niiden edellyttämään muotoon.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: bank, format, data
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 493abf6f7309d6eb0274f4f416e6e5aea782b031
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194353"
---
# <a name="using-the-amc-banking-365-fundamentals-extension"></a>AMC Banking 365 -perusteiden laajennuksen käyttäminen
AMC Banking 365 -perusteiden laajennus helpottaa ja tarkentaa tietojen lähettämistä pankkeihin. Laajennus yhdistää [!INCLUDE[d365fin](includes/d365fin_md.md)]:n ja AMC Banking 365 -perusteet Microsoft Dynamics 365 Business Central -palveluun, joka voi muuntaa pankkitietoja [!INCLUDE[d365fin](includes/d365fin_md.md)]:sta muodoiksi, joita tarvitaan yli 600 pankissa ympäri maailmaa. Tämä helpottaa esimerkiksi maksujen ja hyvitysten siirtämistä toimittajille syöttämällä maksut [!INCLUDE[d365fin](includes/d365fin_md.md)]-ohjelmaan ja lataamalla ne sitten pankkiin. Muodot voivat myös tasoittaa pankin täsmäytysprosesseja. Lisätietoja on kohdassa [AMC Banking Microsoft Dynamics 365 Business Centralille](https://amcbanking.com/landing365bc/help).

> [!Note]
> AMC Banking on rakentanut lisälaajennuksia, jotka toimivat [!INCLUDE[d365fin](includes/d365fin_md.md)]:n kanssa. Tässä ohjeaiheessa kuvataan vain peruslaajennus.

## <a name="using-our-demonstration-account"></a>Esittelytilin käyttäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)]:n mukana on esittelytili, jonka avulla voit kokeilla AMC Banking 365 -perusteiden laajennusta. Microsoft tarjoaa oletusasetukset yhteyden muodostamiseen AMC Bankingiin. Niissä määritetään pankkitilit tietojen saamiseksi [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan sekä muutamia tiedonvaihtomäärityksiä. Voit tarkastella yhteysasetuksia **AMC Bankingin asetus** -sivulla. Laajennus kohdistaa pankkitileille arvot **Pankin nimi**-, **Hyvityksen siirtoviestinrot**-, **Tiliotteen tuontimuoto**- ja **Maksun viennin muoto** -kenttiin pankkitilin korteilla.

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
2. Valitse [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **AMC Banking -asetukset** ja valitse sitten liittyvä linkki.  
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
>  Kun viet tietoja AMC Banking 365 -perusteiden laajennuksen avulla, joitakin yritystietoja paljastetaan palvelun tarjoajalle. Palveluntarjoaja, AMC Consult A/S, vastaa näiden tietojen tietosuojasta. Lisätietoja on kohdassa [AMC:n tietosuojakäytäntö](https://go.microsoft.com/fwlink/?LinkId=510158).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten liittyvä linkki.
2. Luo ne päiväkirjan rivit, jotka haluat viedä.  

   > [!Note]
   > Muista valita jokaiselle riville **Sähköinen maksu** **Pankkimaksun tyyppi** -kentässä.
3. Valitse **Vie**-toiminto.

### <a name="to-import-and-apply-the-converted-file"></a>Muunnetun tiedoston tuominen ja käyttäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksujen täsmäytyskirjauskansio** ja valitse sitten liittyvä linkki.
2. Valitse **Tuo pankkitapahtuma** -toiminto ja valitse sitten muunnettu tiedosto.  

   [!INCLUDE[d365fin](includes/d365fin_md.md)] luo uuden maksun täsmäytyskirjauskansion, joka sisältää tiedoston tiedot. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
[Käytön aloittaminen](product-get-started.md)
