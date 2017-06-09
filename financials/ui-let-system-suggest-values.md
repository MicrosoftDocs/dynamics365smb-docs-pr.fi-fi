---
title: Dynamics 365 for Financials saa ehdottaa arvoja | Microsoft Docs
description: "Tässä artikkelissa kerrotaan, miten järjestelmän voi määrittää niin, että se esitäyttää valittuihin kenttiin arvot, jotka muussa tapauksessa tulisi laskea ja täyttää manuaalisesti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 785ad537f81b8388aa14654f375599a13b66e3c5
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="letting-dynamics-365-for-financials-suggest-values"></a>Dynamics 365 for Financials saa ehdottaa arvoja
[!INCLUDE[d365fin](includes/d365fin_md.md)] voi auttaa tehtävien suorittamisessa nopeammin ja tarkemmin täyttämällä kentät tai rivit tiedoilla, jotka muussa tapauksessa olisi laskettava ja annettava manuaalisesti. Vaikka automaattinen tietojen syöte on aina oikea, voit halutessasi muuttaa arvoja myöhemmin.

Toiminto, joka syöttää arvot puolestasi, sisältyy yleensä tehtäviin, joissa syötetään suuria määriä tapahtumatietoja. Niissä halutaan välttää virheet ja säästää aikaa. Tämä ohjeaihe sisältää näiden toimintojen valikoiman. [!INCLUDE[d365fin](includes/d365fin_md.md)]in tulevat päivitykset sisältävät uusia osia.

## <a name="the-suggest-balancing-amount-check-box-in-the-general-journal-batches-window"></a>**Ehdota vastasummaa** -valintaruutu **Yleisen päiväkirjan erät** -ikkunassa
Kun esimerkiksi syötät yleisen päiväkirjan riveille useita kuluja, jotka on kirjattava samalle pankkitilille, kulun uuden päiväkirjan rivin syöttämisen yhteydessä pankkitilin rivin **Summa**-kenttään täytetään automaattisesti kulut täsmäyttävä summa. Lisätietoja yleisten päiväkirjojen käsittelemisestä on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>**Summa**-kentän täyttäminen automaattisesti yleisen päiväkirjan rivien täsmäyttämistä varten
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Yleiset päiväkirjat** ja valitse sitten liittyvä linkki.
2. Valitse haluamasi yleisen päiväkirjan erän rivillä **Ehdota vastasummaa** -valintaruutu.
3. Avaa yleinen päiväkirja ja jatka rekisteröitymiseen. Kirjaa tapahtumia edellä esiteltyjen toimintojen avulla, kun haluat, että kentän arvo syötetään automaattisesti.       

Lisätietoja henkilökohtaisen yleisen päiväkirjan erän määrittämisestä esimerkiksi kulujen käsittelemistä varten on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-in-the-payment-registration-window"></a>**Täytä vastaanottopäivämäärä automaattisesti** -kenttä **Maksurekisteröinti**-ikkunassa
**Maksurekisteröinti**-ikkuna näyttää avoimet saapuvat maksut riveinä, jotka edustavat myyntiasiakirjoja, joiden summa on erääntynyt maksettavaksi. Lisätietoja asiakkaan maksujen kohdistamisesta on kohdassa [Toimintaohje: Asiakasmaksujen täsmäyttäminen manuaalisesti maksamattomien myyntiasiakirjojen luettelosta](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

Tärkein ikkunassa tehtävät toiminnot ovat **Maksu suoritettu** -valintaruudun valitseminen ja **Vastaanottopvm**-kentän täyttäminen. Voit määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in siten, että se lisää päivämäärän automaattisesti **Vastaanottopvm**-kenttään silloin, kun valitset **Maksu suoritettu** -valintaruudun.

### <a name="to-have-the-date-received-field-in-the-payment-registration-window-filled-automatically"></a>**Maksurekisteröinti**-ikkunan **Täytä vastaanottopäivämäärä automaattisesti** -kentän automaattinen täyttäminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Maksurekisteröinnin asetukset** ja valitse sitten liittyvä linkki.
2. Valitse **Täytä vastaanottopäivämäärä automaattisesti** -valintaruutu.
3. Avaa **Maksurekisteröinti**-ikkuna ja jatka saapuvien asiakkaiden maksujen käsittelyyn edellä esiteltyjen toimintojen avulla, kun haluat, että kentän arvo syötetään automaattisesti.

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  
[Rahoitus](Finance.md)


