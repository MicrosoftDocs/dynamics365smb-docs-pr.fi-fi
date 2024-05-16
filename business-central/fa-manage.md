---
title: Käyttöomaisuuden hallinta (sisältää videon)
description: Saat tietoja käyttöomaisuustoiminnoista sekä yleiskuvan käyttöomaisuuserien käsittelystä ja hallinnasta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 05/06/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="manage-fixed-assets"></a>Käyttöomaisuuden hallinta

[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman Käyttöomaisuus-sovellusalueesta saat yleiskuvan käyttöomaisuudestasi, ja voit varmistaa, että poistot ovat oikein. Se mahdollistaa myös kunnossapitokulujen seuraamisen, vakuutussopimusten hallinnoimisen, käyttöomaisuustransaktioiden kirjaamisen sekä monenlaisten raporttien ja tilastojen luomisen.

## <a name="video-overview"></a>Videon yleiskatsaus

Seuraavassa videossa käsitellään käyttöomaisuuden perusteet:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## <a name="initial-setup-of-fixed-assets"></a>Käyttöomaisuuden alustavat asetukset

Ennen käyttöomaisuuden hallintaa on tehtävä seuraavat määritykset:

- Oletusarvot
- Käyttöomaisuuden kirjanpito
- Kirjausryhmät ja -tyypit
- Kohdistusavaimet
- Käyttöomaisuuspäiväkirjat

Lisätietoja on kohdassa [Käyttöomaisuuden määrittäminen](fa-setup.md).

## <a name="fixed-assets-analytics"></a>Käyttöomaisuuden analyysi

Tässä osassa kuvataan analyysityökaluja, joita voit käyttää, kun haluat saada tietoja käyttöomaisuudesta.

| Vastaanottaja... | Katso |
| --- | --- |
| Tutustu käyttöomaisuuserien tietojen analysointimahdollisuuksiin. | [Käyttöomaisuuden analyysin yleiskatsaus](fa-analytics-overview.md) |
| Tee käyttöomaisuustietojen ad-hoc-analyysi suoraan luettelosivuilla ja kyselyissä. | [Käyttöomaisuuden tapauskohtainen analyysi](ad-hoc-analysis-fa.md) |
| Tutustu käyttöomaisuuden valmiisiin raportteihin. | [Valmiit käyttöomaisuusraportit](fa-reports.md) |
| Valvo kunnossapitokustannuksia. | [Kunnossapitokustannusten valvonta](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Tarkkaile vakuutuksen kattavuutta. | [Vakuutuksen kattavuuden tarkkailu](fa-how-insure.md#to-monitor-insurance-coverage) |
| Katso luovutustapahtumia. | [Luovutustapahtumien tarkasteleminen](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Katso suunniteltuja luovutusarvoja. | [Suunniteltujen luovutusarvojen tarkasteleminen](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="register-fixed-assets"></a>Rekisteröi käyttöomaisuutta

Kunkin käyttöomaisuuserän osalta tulee määrittää kortti, joka sisältää tietoja niistä. Voit esimerkiksi määrittää rakennukset tai tuotantolaitteet voidaan pääkäyttöomaisuuseräksi, jolla on komponenttiluettelo. Resursseja voi ryhmitellä monella tavalla, esimerkiksi luokan, osaston tai sijainnin mukaan. Tämän jälkeen voit hankkia, kunnossapitää ja myydä käyttöomaisuutta. Voit myös määrittää budjetoitua käyttöomaisuutta. Budjetointi mahdollistaa minkä tahansa ennakoidun hankinnan ja myynnin sisällyttämisen raportteihin.

| Vastaanottaja  | Katso |
| --- | --- |
| Hallitse käyttöominaisuuserien budjetteja, budjetin hankintamenoja, käyttöomaisuuden luovutusten budjetointia ja poistojen budjetointia. |[Käyttöomaisuuden budjettien hallinta](fa-how-manage-budgets.md) |
| Luo käyttöomaisuus, liitä poistomenetelmät, kirjaa hankinnat ja jäännösarvot ja tulosta käyttöomaisuusluettelot. |[Käyttöomaisuuden hankkiminen](fa-how-acquire.md) |

## <a name="set-up-depreciations-for-your-fixed-assets"></a>Määritä käyttöomaisuuden poistot

Käyttöomaisuuden poistoja sekä muita käyttöomaisuuden rahoitustapahtumia voidaan seurata määrittämällä niistä jokaiselle vähintään yksi poistokirja. Resurssien poistaminen edellyttää muutamien vaiheiden suorittamista:

1. Aja raportti jaksottaisten poistojen laskemiseksi.
1. Täytä päiväkirja tuloksena olevilla merkinnöillä.
1. Kirjaa päiväkirja.

[!INCLUDE[prod_short](includes/prod_short.md)] tukee useita poistotapoja. Saat lisätietoja siirtymällä [Poistomenetelmät](fa-depreciation-methods.md) -kohtaan. Voit määrittää useita poistokirjoja käyttöomaisuutta kohti eri tarkoituksia varten. Poistokirjat voivat käsitellä esimerkiksi veroraportointia tai sisäistä raportointia.

| Vastaanottaja  | Katso |
| --- | --- |
| Lisätietoja käyttöomaisuuden erilaisista poistotavoista. |[Poistotavat](fa-depreciation-methods.md) |
| Laske ja kirjaa poisto sekä analysoi poisto käyttöomaisuusraporteissa. |[Käyttöomaisuuden poistaminen tai kuolettaminen](fa-how-depreciate-amortize.md) |
| Muuttuneiden poistokirja-arvojen tarkastelu. | [Muuttuneiden poistokirja-arvojen tarkasteleminen](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification) |
| Tallenna manuaalisesti käyttöomaisuustapahtumat **Käyttöomaisuuden KP-päiväkirja**- tai **Käyttöomaisuuspäiväkirja**-sivulle sen mukaan, koskevatko tapahtumat talousraportointia vai sisäistä hallintaa. | [Käyttöomaisuuden poiston määrittäminen](fa-how-setup-depreciation.md) |

## <a name="fixed-assets-maintenance-and-insurance"></a>Käyttöomaisuuden kunnossapito ja vakuutus

Voit tallentaa kunnossapitokulut ja seuraavan huoltopäivämäärän kullekin käyttöomaisuuserälle. Kunnossapitokulujen seuraaminen voi olla tärkeää budjetointia varten ja käyttöomaisuuden vaihtamisesta päätettäessä. Kukin käyttöoikeus voidaan liittää vähintään yhteen vakuutussopimukseen ja varmistaa, että sopimusmaksut vastaavat resurssien arvoa.

| Vastaanottaja  | Katso |
| --- | --- |
| Tallenna huoltokäynnit ja kirjaa kunnossapitokustannukset sekä seuraa niitä. |[Käyttöomaisuuden ylläpitäminen](fa-how-maintain.md) |
| Valvo kunnossapitokustannuksia. | [Kunnossapitokustannusten valvonta](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Päivitä vakuutustiedot, kirjaa hankintakustannukset vakuutussopimuksiin, muokkaa vakuutuksen kattavuutta, katsele vakuutustilastoja ja luetteloi vakuutussopimukset. |[Käyttöomaisuuden vakuuttaminen](fa-how-insure.md) |
| Tarkkaile vakuutuksen kattavuutta. | [Vakuutuksen kattavuuden tarkkailu](fa-how-insure.md#to-monitor-insurance-coverage) |

## <a name="reclassify-transfer-split-upcombine-adjust-value-write-down-and-dispose-fixed-assets"></a>Uudelleenluokittelu, siirto, jakaminen/yhdistäminen, arvon muuttaminen, arvonalennus ja käyttöomaisuuden luovuttaminen

| Vastaanottaja  | Katso |
| --- | --- |
| Luokittele käyttöomaisuus uudelleen, siirrä käyttöomaisuus eri sijainteihin, jaa käyttöomaisuuseriä tai yhdistä niitä. |[Käyttöomaisuuserien siirtäminen, jakaminen tai yhdistäminen](fa-how-trans-split-combine.md) |
| Muuta käyttöomaisuuserien arvoja ja kirjaa arvonkorotus- sekä arvonalennustransaktiot. |[Käyttöomaisuuden uudelleenarvostus](fa-how-revalue.md) |
| Kirjaa luovutustransaktiot, tarkastele luovutustapahtumia ja kirjaa osittaisia luovutuksia. |[Käyttöomaisuuden luovuttaminen tai poistaminen käytöstä](fa-how-dispose-retire.md) |
| Katso luovutustapahtumia. | [Luovutustapahtumien tarkasteleminen](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Katso suunniteltuja luovutusarvoja. | [Suunniteltujen luovutusarvojen tarkasteleminen](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="see-also"></a>Katso myös

[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuuden analyysin yleiskatsaus](fa-analytics-overview.md)  
[Talouden yleiskatsaus](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
