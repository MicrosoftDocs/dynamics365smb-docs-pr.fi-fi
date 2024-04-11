---
title: Käyttöomaisuuden hallinta (sisältää videon)
description: Saat tietoja käyttöomaisuustoiminnoista sekä yleiskuvan käyttöomaisuuserien käsittelystä ja hallinnasta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Käyttöomaisuuden hallinta

[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman Käyttöomaisuus-sovellusalueesta saat yleiskuvan käyttöomaisuudestasi, ja se takaa oikeat jaksottaiset poistot. Se mahdollistaa myös kunnossapitokulujen seuraamisen, vakuutussopimusten hallinnoimisen, käyttöomaisuustransaktioiden kirjaamisen sekä monenlaisten raporttien ja tilastojen luomisen.

## Videon yleiskatsaus

Seuraavassa videossa käsitellään käyttöomaisuuden perusteet:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## Käyttöomaisuuden yleiskatsaus

Kunkin käyttöomaisuuserän osalta tulee määrittää kortti, joka sisältää tietoja kyseisestä käyttöomaisuuserästä. Voit määrittää rakennuksia tai tuotantolaitoksia pääkäyttöomaisuuseräksi. Voit myös ryhmitellä niitä eri tavoin, kuten esimerkiksi luokan, osaston ja sijainnin mukaan. Tämän jälkeen voit aloittaa käyttöomaisuuden hankinnan, kunnossapidon ja myynnin. Voit myös määrittää budjetoitua käyttöomaisuutta. Budjetointi mahdollistaa minkä tahansa ennakoidun hankinnan ja myynnin sisällyttämisen raportteihin.

> [!IMPORTANT]
> Ennen käyttöomaisuuden hallintaa on tehtävä seuraavat määritykset:
>
> * Oletusarvot
> * Käyttöomaisuuden kirjanpito
> * Kirjausryhmät
> * Kohdistusavaimet
> * Käyttöomaisuuspäiväkirjat
>
> Lisätietoja on kohdassa [Käyttöomaisuuden määrittäminen](fa-setup.md).

Käyttöomaisuuden poistoja sekä muita käyttöomaisuuden rahoitustapahtumia voidaan seurata määrittämällä niistä jokaiselle vähintään yksi poistokirja. Poisto tehdään suorittamalla raportti, joka laskee kausittaisen poiston, täyttää päiväkirjaan tapahtumat ja kirjaa sitten päiväkirjan. [!INCLUDE[prod_short](includes/prod_short.md)] tukee useita poistotapoja. Lisätietoja on kohdassa [Poistotavat](fa-depreciation-methods.md). Voit määrittää useita poistokirjoja käyttöomaisuutta kohti eri tarkoituksia varten. Poistokirjat voivat käsitellä esimerkiksi veroraportointia tai sisäistä raportointia.

Kunkin käyttöomaisuuserän osalta voidaan tallentaa kunnossapitokulut ja seuraava huoltopäivämäärä. Kunnossapitokulujen seuraaminen voi olla tärkeää budjetointia varten ja käyttöomaisuuden vaihtamisesta päätettäessä.

Kukin käyttöoikeus voidaan liittää vähintään yhteen vakuutussopimukseen ja varmistaa, että sopimusmaksut vastaavat resurssien arvoa.

> [!NOTE]  
> Voit tallentaa käyttöomaisuustapahtumat **Käyttöomaisuuden KP-päiväkirja**- tai **Käyttöomaisuuspäiväkirja**-sivulle sen mukaan, koskevatko tapahtumat talousraportointia vai sisäistä hallintaa. Käyttöomaisuuden ohje sisältää tietoja vain **Käyttöomaisuuden KP-päiväkirja** -sivun käyttämisestä. Lisätietoja on kohdassa [Käyttöomaisuuden poiston määrittäminen](fa-how-setup-depreciation.md).

## Käyttöomaisuuden käyttäminen

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.

| Vastaanottaja  | Katso |
| --- | --- |
| Käyttöoikeusominaisuuden käyttämiseen tarvittavien edellytysten määrittäminen (oletusarvojen, käyttöomaisuuden kirjanpidon, kirjausryhmien, kohdistusavaimien ja kirjaustyyppien määrittäminen). | [Käyttöomaisuuden määrittäminen](fa-setup.md)|
| Luo käyttöomaisuus, liitä poistomenetelmät, kirjaa hankinnat ja jäännösarvot ja tulosta käyttöomaisuusluettelot. |[Hankittu käyttöomaisuus](fa-how-acquire.md) |
| Tallenna huoltokäynnit ja kirjaa kunnossapitokustannukset sekä seuraa niitä. |[Käyttöomaisuuden ylläpito](fa-how-maintain.md) |
| Päivitä vakuutustiedot, kirjaa hankintakustannukset vakuutussopimuksiin, muokkaa vakuutuksen kattavuutta, katsele vakuutustilastoja ja luetteloi vakuutussopimukset. |[Käyttöomaisuuden vakuuttaminen](fa-how-insure.md) |
| Luokittele käyttöomaisuus uudelleen, siirrä käyttöomaisuus eri sijainteihin, jaa käyttöomaisuuseriä tai yhdistä niitä. |[Käyttöomaisuuserien siirtäminen, jakaminen tai yhdistäminen](fa-how-trans-split-combine.md) |
| Muuta käyttöomaisuuserien arvoja ja kirjaa arvonkorotus- sekä arvonalennustransaktiot. |[Käyttöomaisuuden uudelleenarvostus](fa-how-revalue.md) |
| Laske ja kirjaa poisto sekä analysoi poisto käyttöomaisuusraporteissa. |[Käyttöomaisuuden poistaminen tai kuolettaminen](fa-how-depreciate-amortize.md) |
| Lisätietoja käyttöomaisuuden erilaisista poistotavoista. |[Poistotavat](fa-depreciation-methods.md) |
| Kirjaa luovutustransaktiot, tarkastele luovutustapahtumia ja kirjaa osittaisia luovutuksia. |[Käyttöomaisuuden käytöstä poistaminen](fa-how-dispose-retire.md) |
| Hallitse käyttöominaisuuserien budjetteja, budjetin hankintamenoja, käyttöomaisuuden luovutusten budjetointia ja poistojen budjetointia. |[Käyttöomaisuuden budjettien hallinta](fa-how-manage-budgets.md) |
| Lisätietoja valmiista käyttöomaisuuden raportointi- ja analysointiominaisuuksista. | [Käyttöomaisuuden raportit ja analytiikka](fa-reports.md) |

## Katso myös

[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Talouden yleiskatsaus](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
