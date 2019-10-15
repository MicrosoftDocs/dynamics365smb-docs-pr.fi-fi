---
title: Ehdotettujen kenttien arvojen määrittäminen | Microsoft Docs
description: Voit välttää manuaaliset laskutoimitukset sekä suorittaa tehtävät nopeasti ja tarkasti määrittämällä automaattisen tietojen antamisen, jolloin Business Central täyttää valitut kentät.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8d59462f89e8268bdb9def8c455388ccddcea3ac
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310850"
---
# <a name="letting-included365finincludesd365fin_mdmd-suggest-values"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] voi ehdottaa arvoja
[!INCLUDE[d365fin](includes/d365fin_md.md)] voi auttaa tehtävien suorittamisessa nopeammin ja tarkemmin täyttämällä kentät tai rivit tiedoilla, jotka muussa tapauksessa olisi laskettava ja annettava manuaalisesti. Vaikka automaattinen tietojen syöte on aina oikea, voit halutessasi muuttaa arvoja myöhemmin.

Toiminto, joka syöttää arvot puolestasi, sisältyy yleensä tehtäviin, joissa syötetään suuria määriä tapahtumatietoja. Niissä halutaan välttää virheet ja säästää aikaa. Tämä ohjeaihe sisältää näiden toimintojen valikoiman. [!INCLUDE[d365fin](includes/d365fin_md.md)]in tulevat päivitykset sisältävät uusia osia.

## <a name="the-suggest-balancing-amount-check-box-on-the-general-journal-batches-page"></a>**Ehdota vastasummaa** -valintaruutu **Yleisen päiväkirjan erät** -sivulla
Kun esimerkiksi syötät yleisen päiväkirjan riveille useita kuluja, jotka on kirjattava samalle pankkitilille, kulun uuden päiväkirjan rivin syöttämisen yhteydessä pankkitilin rivin **Summa**-kenttään täytetään automaattisesti kulut täsmäyttävä summa. Lisätietoja yleisten päiväkirjojen käsittelemisestä on ohjeaiheessa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>**Summa**-kentän täyttäminen automaattisesti yleisen päiväkirjan rivien täsmäyttämistä varten
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten liittyvä linkki.
2. Valitse haluamasi yleisen päiväkirjan erän rivillä **Ehdota vastasummaa** -valintaruutu.
3. Avaa yleinen päiväkirja ja jatka rekisteröitymiseen. Kirjaa tapahtumia edellä esiteltyjen toimintojen avulla, kun haluat, että kentän arvo syötetään automaattisesti.       

Lisätietoja henkilökohtaisen yleisen päiväkirjan erän määrittämisestä esimerkiksi kulujen käsittelemistä varten on ohjeaiheessa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-on-the-payment-registration-page"></a>**Täytä vastaanottopäivämäärä automaattisesti** -kenttä **Maksurekisteröinti**-sivulla
**Maksurekisteröinti**-sivu näyttää avoimet saapuvat maksut riveinä, jotka edustavat myyntiasiakirjoja, joiden summa on erääntynyt maksettavaksi. Lisätietoja asiakkaan maksujen kohdistamisesta on kohdassa [Asiakasmaksujen täsmäyttäminen maksamattomien myyntiasiakirjojen luettelosta](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

Tärkeimmät sivulla tehtävät toiminnot ovat **Maksu suoritettu** -valintaruudun valitseminen ja **Vastaanottopvm**-kentän täyttäminen. Voit määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in siten, että se lisää päivämäärän automaattisesti **Vastaanottopvm**-kenttään silloin, kun valitset **Maksu suoritettu** -valintaruudun.

### <a name="to-have-the-date-received-field-on-the-payment-registration-page-filled-automatically"></a>**Maksurekisteröinti**-sivun **Täytä vastaanottopäivämäärä automaattisesti** -kentän automaattinen täyttäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksurekisteröinnin asetukset** ja valitse sitten liittyvä linkki.
2. Valitse **Täytä vastaanottopäivämäärä automaattisesti** -valintaruutu.
3. Avaa **Maksurekisteröinti**-sivu ja jatka saapuvien asiakkaiden maksujen käsittelyyn edellä esiteltyjen toimintojen avulla, kun haluat, että kentän arvo syötetään automaattisesti.

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Rahoitus](finance.md)
