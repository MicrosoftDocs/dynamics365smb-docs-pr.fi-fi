---
title: Raporttien valinta Business Centralissa
description: Tietoja eri asiakirjatyyppien tulostamiseen tarvittavien raporttien määrittämisestä Business Centralissa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ba15a65317ebf52579c285c93dd59eba1b65ae1b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787105"
---
# <a name="report-selection-in-business-central"></a>Raporttien valinta Business Centralissa

Voit määrittää oletusraportit, joita käytetään, kun tulostat myynnin ja ostojen asiakirjoja, kuten tilauksia, tarjouksia, laskuja ja hyvityslaskuja. Jos sinulla on esimerkiksi myyntilaskuissa tietty asettelu, voit määrittää raportin **Raporttivalinnat – myynti** -sivulla, jotta sitä käytetään myyntilaskujen lähettämiseen tai tulostamiseen.  

**Raporttivalinnat**-sivu määrittää, mikä raportti tulostetaan eri tilanteissa. [!INCLUDE [prod_short](includes/prod_short.md)] sisältää oletuskokoonpanot, mutta tietysti voit muuttaa näitä oletusarvoja. Voit myös lisätä raportteja **Raporttivalinnat**-sivuille, jos haluat että ohjelmassa on esimerkiksi enemmän kuin yksi raportti asiakirjatyyppiä kohden.  

## <a name="available-report-selections"></a>Käytettävissä olevat raporttivalinnat

[!INCLUDE [prod_short](includes/prod_short.md)] sisältää eri **Raporttivalinta**-sivut eri alueille. Seuraavissa taulukoissa kuvataan, mistä voit löytää tietoa eri sivuista.  

|Alue tai tehtävä  |Lisätietoja|
|--------------|----------|
|Esimerkki raporttivalinnan toiminnasta (myynti)|[Myyntiasiakirjojen raporttivalinta](#example-report-selection-for-sales-documents)|
|Myynti- ja ostoasiakirjojen sähköpostien oletusasettelu  |[Uudelleenkäytettävien sähköpostitekstien ja -asettelujen määrittäminen myynti- ja ostoasiakirjoille](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|Sekkien asetteluiden määrittäminen     |[Sekin asettelun valitseminen](finance-how-define-check-layouts.md) |
|Raporttien määrittäminen ALV-raportointia varten (Saksa)|[ALV- ja Intrastat-raporttien määrittäminen](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> [!INCLUDE [prod_short](includes/prod_short.md)] voi lisätä **Raporttivalinta**-sivuja esimerkiksi sijainnista ja toimialasta riippuen. Voit aina tarkistaa asetukset valitsemalla ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -, kirjoittamalla **Raporttivalinnat** ja valitsemalla sitten liittyvän linkin.

[!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman oletusversio sisältää seuraavat **Raporttivalinta**-sivut:

* **Raporttivalinta - Myynti**  
* **Raporttivalinta - Osto**  
* **Raporttivalinta - Varasto**  
* **Raporttivalinta - Kassavirta**  
* **Raporttivalinta - Fyysinen varasto**  
* **Raporttivalinta - Pankkitili**  
* **Raporttivalinta – Muistutus-/viivästyskulu**  

## <a name="example-report-selection-for-sales-documents"></a>Esimerkki: Myyntiasiakirjojen raporttivalinta

**Raporttivalinta – Myynti** -sivu määrittää kullekin liittyvälle asiakirjatyypille eri skenaarioissa käytettävät oletusraportit. Valitse asiakirjatyyppi **Käyttö**-kentässä ja lisää tai tarkista raportin valinta. Voit määrittää useamman kuin yhden raportin sekä järjestyksen lajittelun, jossa raportit täytyy lähettää tai tulostaa.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Jotkin asiakirjatyypit voidaan lähettää sähköpostin liitteinä, toisia ei. Jokaisessa **Raporttivalinta**-sivussa on lisäkenttiä, jos tyyppi tukee sähköpostilla lähettämistä.  

Esimerkiksi **Raporttivalinta – Myynti** ja **Raporttivalinta – Osto** -sivuilla seuraavat kentät auttavat määrittämään sähköpostilla lähettämisen:

|Kentän nimi |Kuvaus  |
|-----------|-------------|
|**Käytä sähköpostin perustekstinä**| Määrittää, että yhteenvetotiedot – esimerkiksi laskunumero, eräpäivä ja maksupalvelun linkki – lisätään lähetettävän sähköpostin perustekstiin.        |
|**Käytä sähköpostin liitteenä**| Määrittää, että liittyvä asiakirja liitetään sähköpostiin.|
|**Sähköpostin perustekstin asettelun kuvaus**|Määrittää käytetyn sähköpostin perustekstin asettelun, yleensä mukautetun raporttiasettelun. |

## <a name="see-also"></a>Katso myös

[Uudelleenkäytettävien sähköpostitekstien ja -asettelujen määrittäminen myynti- ja ostoasiakirjoille](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[Sekin asettelun valitseminen](finance-how-define-check-layouts.md)  
[ALV- ja Intrastat-raporttien määrittäminen (Saksa)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
[Asiakirja-asettelujen määrittäminen asiakkaille ja toimittajille](ui-define-customer-vendor-document-layouts.md)  
[Tulostimien määrittäminen](ui-specify-printer-selection-reports.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]