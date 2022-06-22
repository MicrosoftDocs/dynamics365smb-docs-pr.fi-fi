---
title: Raporttien valinta Business Centralissa
description: Tietoja eri asiakirjatyyppien tulostamiseen tarvittavien raporttien määrittämisestä Business Centralissa.
author: edupont04
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.search.form: 306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917
ms.date: 03/11/2022
ms.author: edupont
ms.openlocfilehash: 9106b1ac3f6b179e26c8dfb01212b88e92b694fe
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950197"
---
# <a name="report-selection-in-business-central"></a>Raporttien valinta Business Centralissa

Voit määrittää oletusraportteja, joita käytetään myynti-ja ostoasiakirjojen, kuten tilausten, tarjousten ja laskujen, tulostamiseen. Jos sinulla on esimerkiksi myyntilaskuissa tietty asettelu, voit määrittää raportin **Raporttivalinnat – myynti** -sivulla, jotta sitä käytetään myyntilaskujen lähettämiseen tai tulostamiseen.  

**Raporttivalinnat**-sivu määrittää, mikä raportti tulostetaan eri tilanteissa. [!INCLUDE [prod_short](includes/prod_short.md)] tarjoaa oletusmääritykset, mutta voit muuttaa niitä tarvittaessa. Voit myös lisätä raportteja **Raporttivalinnat**-sivuille, jos haluat että ohjelmassa on esimerkiksi enemmän kuin yksi raportti asiakirjatyyppiä kohden.  

## <a name="available-report-selections"></a>Käytettävissä olevat raporttivalinnat

[!INCLUDE [prod_short](includes/prod_short.md)] sisältää eri **Raporttivalinta**-sivut eri alueille. Seuraavassa taulukossa kuvataan, mistä voit löytää tietoa eri sivuista.  

|Alue tai tehtävä  |Lisätietoja|
|--------------|----------|
|Esimerkki raporttivalinnan toiminnasta (myynti)|[Myyntiasiakirjojen raporttivalinta](#example-report-selection-for-sales-documents)|
|Myynti- ja ostoasiakirjojen sähköpostien oletusasettelu  |[Uudelleenkäytettävien sähköpostitekstien ja -asettelujen määrittäminen myynti- ja ostoasiakirjoille](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Sekkien asetteluiden määrittäminen     |[Sekin asettelun valitseminen](finance-how-define-check-layouts.md) |
|Raporttien määrittäminen ALV-raportointia varten (Saksa)|[ALV- ja Intrastat-raporttien määrittäminen](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> [!INCLUDE [prod_short](includes/prod_short.md)] voi lisätä **Raporttivalinta**-sivuja esimerkiksi sijainnista ja toimialasta riippuen. Voit aina tarkistaa asetukset valitsemalla ![Hehkulamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeen, syöttämällä **Raporttivalinnat** ja valitsemalla sitten vastaavan linkin.

[!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman oletusversio sisältää seuraavat **Raporttivalinta**-sivut:

* **Raporttivalinta - Myynti**  
* **Raporttivalinta - Osto**  
* **Raporttivalinta - Varasto**  
* **Raporttivalinta - Kassavirta**  
* **Raporttivalinta - Fyysinen varasto**  
* **Raporttivalinta - Pankkitili**  
* **Raporttivalinta – Muistutus-/viivästyskulu**  
* **Raporttivalinta – Projekti**  

## <a name="example-report-selection-for-sales-documents"></a>Esimerkki: Myyntiasiakirjojen raporttivalinta

**Raporttivalinta – Myynti** -sivu määrittää kullekin liittyvälle asiakirjatyypille eri skenaarioissa käytettävät oletusraportit. Valitse asiakirjatyyppi **Käyttö**-kentässä ja lisää tai tarkista raportin valinta. Voit määrittää useamman kuin yhden raportin sekä järjestyksen lajittelun, jossa raportit täytyy lähettää tai tulostaa.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Jotkin asiakirjatyypit voidaan lähettää sähköpostin liitteinä, toisia ei. Jos asiakirjatyyppi voidaan lähettää sähköpostitse, **Raporttivalinta**-sivu sisältää lisäkenttiä.  

Esimerkiksi **Raporttivalinta – Myynti** ja **Raporttivalinta – Osto** -sivuilla seuraavat kentät auttavat määrittämään sähköpostilla lähettämisen:

|Kentän nimi |Kuvaus  |
|-----------|-------------|
|**Käytä sähköpostin perustekstinä**| Lisää sähköpostiin yhteenvetotietoja, kuten laskunumero, eräpäivä tai maksupalvelulinkki.        |
|**Käytä sähköpostin liitteenä**| Liitä liittyvä asia kirja sähköpostiviestiin.|
|**Sähköpostin perustekstin asettelun kuvaus**|Määritä käytettävä sähköpostin perustekstin asettelu. Yleensä asettelu on mukautettu raporttiasettelu. |

## <a name="see-also"></a>Katso myös

[Uudelleenkäytettävien sähköpostitekstien ja -asettelujen määrittäminen](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Sekin asettelun valitseminen](finance-how-define-check-layouts.md)  
[ALV- ja Intrastat-raporttien määrittäminen (Saksa)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
[Asiakirja-asettelujen määrittäminen asiakkaille ja toimittajille](ui-define-customer-vendor-document-layouts.md)  
[Tulostimien määrittäminen](ui-specify-printer-selection-reports.md)  
[Talousraportit ja analytiikka Business Centralissa](finance-reports.md)  
[Myyntireskontran raportit ja analyysit Business Centralissa](receivables-reports.md) 
[Ostoreskontran raportit ja analyysit Business Centralissa](payables-reports.md)  
[Käyttöomaisuuden raportit ja analytiikka Business Centralissa](fa-reports.md)  
[Business Centralin projektiraportit ja analytiikka](project-reports.md)  
[Business Centralin myyntiraportit ja analytiikka](sales-reports.md)  
[Business Centralin ostoraportit ja analytiikka](purchase-reports.md)  
[Varasto, varastoraportit ja analytiikka Business Centralissa](inventory-WMS-reports.md)  
[Business Centralin kokoonpanoraportit ja analytiikka](assembly-reports.md)  
[Business Centralin tuotantoraportit ja analytiikka](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]