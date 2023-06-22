---
title: Talousprosessien määrittäminen
description: 'Lisätietoja vaadittavista tehtävistä, joilla määritetään liiketoiminnan taloushallinto laskentatoimen, tilintarkastuksen tai kirjanpidon tarpeita varten.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.date: 08/19/2022
ms.author: edupont
---
# <a name="setting-up-finance" />Rahoituksen määrittäminen

Ennen kuin voit aloittaa yrityksesi pyörittämisen, sinun on määritettävä, miten haluat hallita yrityksen rahoitusprosesseja. Aloita määrittämällä yrityksen tilitietueiden perusta – tilikartta. Sitten määritetään kirjausryhmät. Tämä tehostaa pääkirjanpidon oletuskirjaustilien määrittämistä asiakkaille, toimittajille ja nimikkeille.

Jotkin rahoitusasetukset voidaan tehdä automaattisesti avustetun asennuksen ohjeiden avulla, ja jotkin niistä on tehtävä manuaalisesti. Lue lisätietoja kohdasta [Valmistautuminen liiketoimintaan](ui-get-ready-business.md). **Pääkirjanpidon asetukset** -sivulla määritetään, miten yrityksen erilaisia kirjanpitoprosesseja käsitellään. Tällä sivulla voit esimerkiksi määritellä laskun pyöristyksen yksityiskohdat, paikallisen valuutan valuuttakoodin, osoitemuodot, ja sen, haluatko käyttää lisäraportointivaluuttaa. Lisätietoja on kohdassa [Tietoja pääkirjanpidosta ja tilikartasta](finance-general-ledger.md).  

Dimensioiden avulla jokaiseen tapahtumaan voi lisätä erityyppisiä tietoja. Voit määrittää yrityksen perusdimensiot, kuten *Projektit* ja *Osastot*. Lisää tarvittaessa dimensioita myöhemmin. Voit esimerkiksi määrittää väliaikaisia dimensioita käytettäväksi rajoitettuna ajan jaksona, esimerkiksi myyntikampanjan aikana. Lisätietoja on kohdassa [Dimensioiden käsitteleminen](finance-dimensions.md).

Useat asetustehtävistä on tehtävä valmiiksi ennen rahoitustapahtumien tallennuksen aloittamista. Useimpia asetuksia voi kuitenkin muuttaa tarvittaessa. Osa määritystehtävistä on valinnaisia. Esimerkiksi konsernin kirjaukset ja konsolidoinnit määritetään vain, jos työskentelet useiden yritysten kanssa. Toisaalta jotkin määritystehtävät, kuten sallitun kirjausajanjakson määrittäminen, on mahdollisesti toistettava säännöllisin väliajoin.  

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.

| Vastaanottaja | Katso |
| --- | --- |
|Tarkastele tai muokkaa KP-tilejä, joihin kaikki pääkirjanpidon tapahtumat kirjataan|[Tilikartan määrittäminen tai muuttaminen](finance-setup-chart-accounts.md)|
| Määrittää, miten asiakkaat maksavat yrityksellesi ja kuinka haluat maksaa toimittajille. |[Maksutapojen määrittäminen](finance-payment-methods.md) |
| Maksuehtojen määrittäminen eräpäivien hallintaa ja mahdollisten maksualennusten laskentaa varten.|[Maksuehtojen määrittäminen](finance-payment-terms.md) |
| Määritä kirjausryhmät, jotka yhdistävät objektit, kuten asiakkaat, toimittajat, nimikkeet, resurssit sekä myynti- ja ostoasiakirjat, pääkirjanpidon tileille. |[Määritä kirjanpidon kirjausryhmät](finance-posting-groups.md)|
|Luo talousraportit ja määritä tililuokat, jos haluat määrittää talouskaavioiden ja -raporttien, kuten tase- ja tuloslaskelmaraporttien, sisällön.|[Talousraportoinnin valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md)|
|Määritä toleranssi, jonka mukaan järjestelmä sulkee laskun, vaikka maksu ja mahdolliset alennukset eivät täysin vastaa laskun koko summaa.|[Maksutoleranssien ja maksualennustoleranssien käsitteleminen](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Määritä tilikaudet. |[Kirjanpitojaksojen ja tilikausien käyttäminen](finance-accounting-periods-and-fiscal-years.md) |
|Määritä laskutusehdot, jotka muistuttavat asiakkaitasi maksamisesta.|[Muistutusehtojen ja -tasojen määrittäminen](finance-setup-reminders.md)|
| Määritä, miten myynnistä kerätyt arvonlisäverosummat raportoidaan veroviranomaisille. |[Määritä arvolisävero (ALV)](finance-setup-vat.md)|
|Valmistele ei-realisoituneen ALV:n käsittely kassaperusteisen kirjanpidon yhteydessä.|[Ei-realisoituneen arvonlisäveron määrittäminen kassaperusteista kirjanpitoa varten](finance-setup-unrealized-vat.md)|
|Määritä ulkomaan valuutat, joilla käyt kauppaa tai joiden avulla raportoit tapahtumia.|[Valuuttojen määrittäminen](finance-set-up-currencies.md)|
| Määritä myynti- ja ostotoiminnot käsittelemään maksut ulkomaan valuuttana.|[Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa](finance-how-enable-application-ledger-entries-different-currencies.md)
|Määritä ainakin yksi lisävaluutta, jotta summat raportoidaan automaattisesti sekä paikallisena valuuttana (PVA:na) että lisäraportointivaluuttana kussakin pääkirjanpidon (KP) tapahtumassa ja muissa tapahtumissa.|[Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md)|
|Säädä lisävaluutta-arvoja säännöllisesti vaihtokurssien vaihtelun vuoksi.|[Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md)|
|Määritä useita korkoprosentteja käytettäväksi kauppatapahtumien viivästyneissä maksuissa eri jaksoilla.|[Useiden korkoprosenttien määrittäminen](finance-how-to-set-up-multiple-interest-rates.md)|
|Järjestä laskujen luonnin yhteydessä automaattisesti pyöristettävät summat.|[Laskun pyöristyksen määrittäminen](finance-set-up-invoice-rounding.md)|
| Lisää aiemmin luotuun tilikarttaan uusia tilejä. |[Tilikartan määrittäminen](finance-setup-chart-accounts.md) |
| Määritä BI-kaaviot analysoimaan kassavirtaa. |[Kassavirta-analyysin määrittäminen](finance-setup-cash-flow-analyses.md) |
|Ota käyttöön sellaisten asiakkaiden laskutus, joita ei ole määritetty järjestelmässä.|[Käteisasiakkaiden määrittäminen](finance-how-to-set-up-cash-customers.md)|
| Määritä Intrastat-raportointi ja raportin lähettäminen viranomaisille. | [Intrastat-ilmoituksen määrittäminen ja raportoiminen](finance-how-setup-report-intrastat.md)|
|Varmista, että kirjauskansiotapahtuma kohdistetaan useisiin eri tileihin, kuten määrään, prosenttiosuuteen ja summaan, kun se kirjataan päiväkirjaan.|[Kohdistustunnusten käyttäminen yleisissä päiväkirjoissa](ui-how-use-allocation-keys-general-journals.md)|
|Määritä kirjausketjujen seurannassa auttavat lähdekoodit ja syykoodit.|[Kirjausketjujen lähdekoodien ja syykoodien määrittäminen](finance-setup-trail-codes.md)|
|Määritä oletusraportteja, joita käytetään eri asiakirjatyypeille.|[Raporttien valinta Business Centralissa](across-report-selections.md)|

> [!TIP]
> Maantieteellinen sijaintisi mukaan jotkin Business Central -sivut voivat sisältää kenttiä, joita ei ole kuvattu yllä olevassa luettelossa, koska ne koskevat paikallisia toimintoja tai mukautuksia. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-microsoft-trainingtrainingpathsset-up-financial-management-dynamics--business-central" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Rahoitus](finance.md)  
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Yrityksen kassavirran analysoiminen](finance-analyze-cash-flow.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
