---
title: Talousprosessien määrittäminen| Microsoft Docs
description: Lisätietoja tehtävistä, joilla määritetään liiketoiminnan taloushallinto laskentatoimen, tilintarkastuksen tai kirjanpidon tarpeita varten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f93eaa38b07a5135aafa22b21253d1e99a8d0406
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788100"
---
# <a name="setting-up-finance"></a>Rahoituksen määrittäminen
Ennen kuin voit aloittaa yrityksesi pyörittämisen, sinun on määritettävä säännöt ja oletusarvot sille, miten haluat hallita kyseisen yrityksen rahoitusprosesseja. Aloita määrittämällä yrityksen tilitietueiden perusta - tilikartta. Sitten määritetään kirjausryhmät, mikä tehostaa pääkirjanpidon oletuskirjaustilien määrittämistä asiakkaille, toimittajille ja nimikkeille.

Jotkin rahoitusasetukset voidaan tehdä automaattisesti avustetun asennuksen ohjeiden avulla, ja jotkin niistä on tehtävä manuaalisesti. Lisätietoja on ohjeaiheessa [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).

Dimensioiden avulla jokaiseen tapahtumaan voi lisätä erityyppisiä tietoja. Voit määrittää yrityksen perusdimensiot, kuten Projektit ja Osastot. Voit lisätä dimensioita tarvittaessa myöhemmin ja määrittää väliaikaisia dimensioita rajoitetun ajanjakson ajaksi, esimerkiksi myyntikampanjan yhteydessä. Lisätietoja on kohdassa [Dimensioiden käyttäminen](finance-dimensions.md).

Useat asetustehtävistä on tehtävä valmiiksi ennen rahoitustapahtumien tallennuksen aloittamista. Useimpia asetuksia voi kuitenkin muuttaa myöhemmin. Jotkut asetustehtävät ovat valinnaisia, esimerkiksi määrität konsernin kirjauksia ja konsolidointeja vain, jos työskentelet useiden yritysten kanssa. Jotkut määritystehtävät, kuten sallitun kirjausajanjakson määrittäminen, on mahdollisesti toistettava säännöllisin väliajoin.  

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.

| Tehtävä | Katso |
| --- | --- |
| Määrittää, miten asiakkaat maksavat yrityksellesi ja kuinka haluat maksaa toimittajille. |[Maksutapojen määrittäminen](finance-payment-methods.md) |
| Maksuehtojen määrittäminen eräpäivien hallintaa ja mahdollisten maksualennusten laskentaa varten.|[Maksuehtojen määrittäminen](finance-payment-terms.md) |
| Määritä kirjausryhmät, jotka yhdistävät objektit, kuten asiakkaat, toimittajat, nimikkeet, resurssit sekä myynti- ja ostoasiakirjat, pääkirjanpidon tileille. |[Kirjausryhmien määrittäminen](finance-posting-groups.md)|
|Luo KP-raporttimallit ja määritä tililuokat, jos haluat määrittää talouskaavioiden ja -raporttien, kuten tase- ja tuloslaskelmaraporttien, sisällön.|[Talousraportoinnin valmisteleminen KP-raporttimallien ja tililuokkien avulla](bi-how-work-account-schedule.md)|
|Määritä toleranssi, jonka mukaan järjestelmä sulkee laskun, vaikka maksu ja mahdolliset alennukset eivät täysin vastaa laskun koko summaa.|[Maksutoleranssien ja maksualennustoleranssien käsitteleminen](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Määritä tilikaudet. |[Kirjanpitojaksojen ja tilikausien käyttäminen](finance-accounting-periods-and-fiscal-years.md) |
|Määritä muistutusehdot, jotka helpottavat erääntyneiden maksujen keräämistä.|[Muistutusehtojen ja -tasojen määrittäminen](finance-setup-reminders.md)|
| Määritä, miten myynnistä kerätyt arvonlisäverosummat raportoidaan veroviranomaisille. |[Määritä arvolisävero (ALV)](finance-setup-vat.md)|
|Valmistele ei-realisoituneen ALV:n käsittely kassaperusteisen kirjanpidon yhteydessä.|[Ei-realisoituneen arvonlisäveron määrittäminen kassaperusteista kirjanpitoa varten](finance-setup-unrealized-vat.md)|
| Määritä myynti- ja ostotoiminnot käsittelemään maksut ulkomaan valuuttana.|[Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa](finance-how-enable-application-ledger-entries-different-currencies.md)
|Määritä ainakin yksi lisävaluutta, jotta summat raportoidaan automaattisesti sekä PVA:na että lisäraportointivaluuttana kussakin KP-tapahtumassa ja muissa tapahtumissa.|[Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md)|
|Säädä lisävaluutta-arvoja säännöllisesti vaihtokurssien vaihtelun vuoksi.|[Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md)|
|Määritä useita korkoprosentteja käytettäväksi kauppatapahtumien viivästyneissä maksuissa eri jaksoilla.|[Useiden korkoprosenttien määrittäminen](finance-how-to-set-up-multiple-interest-rates.md)|
|Valmistele laskujen summien automaattinen pyöristys laskujen luonnin yhteydessä.|[Laskun pyöristyksen määrittäminen](finance-set-up-invoice-rounding.md)|
| Lisää aiemmin luotuun tilikarttaan uusia tilejä. |[Tilikartan määrittäminen](finance-setup-chart-accounts.md) |
| Määritä BI-kaaviot analysoimaan kassavirtaa. |[Kassavirta-analyysin määrittäminen](finance-setup-cash-flow-analyses.md) |
|Ota käyttöön sellaisen asiakkaan laskutus, jota ei ole määritetty järjestelmässä.|[Käteisasiakkaiden määrittäminen](finance-how-to-set-up-cash-customers.md)|
| Intrastat-raportoinnin määrittäminen ja raportin lähettäminen viranomaisille | [Intrastat-ilmoituksen määrittäminen ja raportoiminen](finance-how-setup-report-intrastat.md)|
|Varmista, että tapahtuma kohdistetaan yleisessä päiväkirjassa useisiin eri tileihin päiväkirjan kirjauksen yhteydessä. Kohdistuksen voi tehdä määrän, prosentin tai summan mukaan.|[Kohdistustunnusten käyttäminen yleisissä päiväkirjoissa](ui-how-use-allocation-keys-general-journals.md)|
|Määritä kirjausketjujen seurantaan käytettävät lähdekoodit ja syykoodit|[Kirjausketjujen lähdekoodien ja syykoodien määrittäminen](finance-setup-trail-codes.md)|
|Määritä oletusraportteja, joita käytetään eri asiakirjatyypeille.|[Raporttien valinta Business Centralissa](across-report-selections.md)|

> [!TIP]
> Maantieteellinen sijaintisi mukaan jotkin sivut voivat sisältää kenttiä, joita ei ole kuvattu tässä luettelossa, koska ne koskevat paikallisia toimintoja tai mukautuksia. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Rahoitus](finance.md)  
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Yrityksen kassavirran analysoiminen](finance-analyze-cash-flow.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]