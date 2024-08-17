---
title: Sähköpostitulostuksen määrittäminen
description: Ohjeen kuvaus
author: jswymer
ms.author: jswymer
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---
# <a name="set-up-email-printers"></a>Sähköpostitulostuksen määrittäminen

Tässä artikkelissa käsitellään sähköpostitulostuksen määrittämistä [!INCLUDE[prod_short](includes/prod_short.md)]issa. [!INCLUDE[prod_short](includes/prod_short.md)] lähettää näissä tulostimissa tulostustyöt tulostimeen käyttämällä tulostimen sähköpostiosoitetta.

> [!TIP]
> Lisätietoja muista tulostinmahdollisuuksista on kohdassa [Tulostimien hallinnan yleiskatsaus](admin-printer-setup-overview.md). 

## <a name="prerequisites"></a>Vaatimukset

- [!INCLUDE[prod_short](includes/prod_short.md)]in vuoden 2020 1. julkaisuaalto tai uudempi
- **Lähetä sähköpostitulostimeen** -laajennus on asennettu

    Tämä laajennus asennetaan oletusarvoisesti. Lisätietoja laajennusten asentamisesta on kohdassa [Laajennusten asentaminen ja poistaminen Business Centralissa](ui-extensions-install-uninstall.md).
- Sähköpostitoiminnot on määritetty.

   Lisätietoja kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).

## <a name="add-an-email-printer"></a>Lisää sähköpostitulostin

**Tulostimen hallinta** -sivulla on näkyvissä tällä hetkellä määritetyt tulostimet. Sivu antaa myös kunkin tulostimen **Asetukset**-sivun käyttöoikeuden. Sivulla voi muokata nykyisiä määrityksiä ja määrittää uuden tulostimen.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tulostimien hallinta** ja valitse sitten vastaava linkki.
2. Valitse **Sähköpostitulostus** ja valitse sitten **Lisää sähköpostitulostin**.
3. Täytä tarvittavat kentät **Sähköpostitulostimen asetukset** -sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Tulostimelle on valittava manuaalisesti sopiva paperikoko, koska paikallista tulostinta tai käyttäjän asetuksia ei voi tallentaa.
    >
    > Huomaa, että sähköpostitulostinlaajennuksen oletusasetuksena on **A4**-paperikoko, joka ei ole käytössä esimerkiksi Pohjois-Amerikassa.

## <a name="privacy-notice"></a>Tietosuojatiedot

Jos käytät sähköpostitulostinlaajennusta, kaikki tai jotkin tulostustyöt lähetetään tulostimelle määritettyyn sähköpostiosoitteeseen. Yksilöllinen sähköpostitunnus kannattaa yhdistää tulostinlaitteeseen käyttämällä vain virallisia laitevalmistajan tarjoamia palveluita. Valmistaja voi olla esimerkiksi HP ePrint, KonicaMinolta EveryonePrint tai Epson Email Print.

Noudata varovaisuutta tietoturva-asioissa. Varmista esimerkiksi, että sähköpostitulostusratkaisun käyttöoikeudet, tietosuoja-asetukset ja tietojen säilyttämistä koskevat käytännöt on määritetty oikein. Vastuullasi on antaa oikea, varmistettu ja toimiva sähköpostiosoite. Lisätietoja on kohdassa [Microsoftin tietosuojatiedot](https://privacy.microsoft.com/privacystatement).

## <a name="next-steps"></a>Seuraavat vaiheet

[Oletustulostimien määrittäminen](ui-specify-printer-selection-reports.md)

## <a name="see-also"></a>Katso myös

[Tulostimien hallinnan yleiskatsaus](admin-printer-setup-overview.md)  
[Yleistulostuksen määrittäminen](admin-printer-setup-universal-print.md)
[Raportin tulostaminen](ui-work-report.md#PrintReport)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eräajojen ajaminen](ui-how-run-batch-jobs.md)  
