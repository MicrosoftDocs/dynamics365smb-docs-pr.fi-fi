---
title: Käyttöomaisuuden määrittäminen
description: 'Lue käyttöomaisuuden, kuten koneiden tai rakennusten määrittämiseen tarvittavasta tehtäväsarjasta.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5607,'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="setting-up-fixed-assets"></a>Käyttöomaisuuden määrittäminen

Ennen käyttöomaisuuden käsittelyä on määritettäviä muutamia toimintoja:  

* Käyttöomaisuuden poistaminen.  
* Hankintakustannusten, poistojen ja muiden arvojen kirjaaminen pääkirjanpitoon.  
* Valinnaisena käyttöomaisuuden vakuutuksen ja ylläpidon kirjaaminen.

Tämän artikkelin osat linkittävät lisätietoa käyttöomaisuuden määrittämisestä. Kun määritys on valmis, käyttöomaisuuden käytön voi aloittaa. Lisätietoja on kohdassa [Käyttöomaisuuden käyttäminen](fa-manage.md).  

> [!NOTE]  
> Voit tallentaa käyttöomaisuustapahtumat **Käyttöomaisuuden KP-päiväkirja**- tai **Käyttöomaisuuspäiväkirja**-sivulla sen mukaan, koskevatko tapahtumat talousraportointia vai sisäistä hallintaa. Käyttöomaisuuden ohjeartikkeleissa käsitellään vain **Käyttöomaisuuden KP-päiväkirja** -sivun käyttämistä.  

Kun käyttöomaisuusaktiviteetti otetaan käyttöön **Poistokirjakortti**-sivun **KP-integrointi**-osassa, **Käyttöomaisuuden KP-päiväkirja** -sivua käytetään kyseisen aktiviteetin tapahtumien kirjaamiseen.

## <a name="required-setup-tasks"></a>Pakolliset määritystehtävät

Seuraavassa taulukossa sarja tehtäviä, joilla käyttöomaisuus määritetään sekä linkit liittyviin artikkeleihin.

| Vastaanottaja | Katso |
|---|---|
| Määritä oletusarvoiset KP-tilit, kohdistustunnukset sekä päiväkirjamallit ja -erät käyttöomaisuuden kirjaamista varten. Määritä myös käyttöomaisuuden luokat ja alaluokat, kuten Aineellinen ja Aineeton. |[Käyttöomaisuuden yleisten tietojen määrittäminen](fa-how-setup-general.md) |
| Luo poistokirjat, määritä eri poistotavat, integroi pääkirjanpidon kanssa ja ota käyttöön tapahtumien monistaminen useissa poistokirjoissa. |[Käyttöomaisuuden poiston määrittäminen](fa-how-setup-depreciation.md) |

## <a name="optional-setup-tasks-insurance-maintenance-and-user-defined-depreciation-methods"></a>Valinnaiset määritystehtävät (vakuutus, ylläpito ja käyttäjän määrittämät poistomenetelmät)

Seuraavassa taulukossa sarja valinnaisia tehtäviä, kuten vakuutus, ylläpito ja poistomenetelmät, joilla käyttöomaisuus määritetään sekä linkit liittyviin artikkeleihin. 

| Vastaanottaja | Katso |
|---|---|
| Voit ottaa käyttöön käyttöomaisuuden vakuutuksen määrittämällä vakuutuksen tiedot ja sopimuskohtaisen vakuutuskortin sekä valmistelemalla päiväkirjat vakuutuskustannusten kirjaamista varten. |[Käyttöomaisuuserän määrittäminen](fa-how-setup-insurance.md) |
| Voit ottaa käyttöomaisuuden kunnossapidon määrittämällä yleiset kunnossapitotiedot, kunnossapidon kirjaustilit ja kunnossapitotyön tyypit. |[Käyttöomaisuuden kunnossapidon määrittäminen](fa-how-setup-maintenance.md) |
| Tietoja poistomenetelmien soveltamisesta. |[Käyttäjäkohtaisten poistomenetelmien määrittäminen](fa-how-setup-user-defined-depreciation-method.md) |

## <a name="see-also"></a>Katso myös

[Käyttöomaisuuden yleiskatsaus](fa-manage.md)  
[Käyttöomaisuuden analyysin yleiskatsaus](fa-analytics-overview.md)   
[Taloushallinto](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
