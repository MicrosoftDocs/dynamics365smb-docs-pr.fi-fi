---
title: "Käyttöomaisuuden hallinta| Microsoft Docs"
description: "Saat tietoja Financialsin käyttöomaisuustoiminnoista sekä yleiskuvan käyttöomaisuuserien käsittelystä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c2a563d09d09e9772ab00fcffc48db9cbc5ee797
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="fixed-assets"></a>Käyttöomaisuus
[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman Käyttöomaisuus-sovellusalueesta saat yleiskuvan käyttöomaisuudestasi, ja se takaa oikeat jaksottaiset poistot. Se mahdollistaa myös kunnossapitokulujen seuraamisen, vakuutussopimusten hallinnoimisen, käyttöomaisuustransaktioiden kirjaamisen sekä monenlaisten raporttien ja tilastojen luomisen.

Kunkin käyttöomaisuuserän osalta tulee määrittää kortti, joka sisältää tietoja kyseisestä käyttöomaisuuserästä. Voit määrittää rakennuksia tai tuotantolaitoksia pääkäyttöomaisuuseräksi. Voit myös ryhmitellä niitä eri tavoin, kuten esimerkiksi luokan, osaston ja sijainnin mukaan. Tämän jälkeen voit aloittaa käyttöomaisuuden hankinnan, kunnossapidon ja myynnin. Voit myös määrittää budjetoitua käyttöomaisuutta. Tämän ansiosta raportteihin voidaan sisällyttää mitä tahansa ennakoituja hankintoja ja myyntejä.

Voit seurata käyttöomaisuuden poistoja sekä muita käyttöomaisuuteen liittyviä rahoitustapahtumia määrittämällä jokaiselle yrityksen käyttöomaisuuserälle vähintään yhden poistokirjan. Poisto tehdään suorittamalla raportti, joka laskee kausittaisen poiston ja täyttää päiväkirjaan tapahtumat, jotka ovat valmiita kirjattaviksi. [!INCLUDE[d365fin](includes/d365fin_md.md)] tukee useita poistotapoja. Lisätietoja on kohdassa [Poistotavat](fa-depreciation-methods.md). Voit määrittää useita poistokirjoja käyttöomaisuutta kohti eri tarkoituksia varten. Poistokirjat voivat käsitellä esimerkiksi veroraportointia tai sisäistä raportointia.

Kunkin käyttöomaisuuserän osalta voidaan tallentaa kunnossapitokulut ja seuraava huoltopäivämäärä. Kunnossapitokulujen seuraaminen voi olla tärkeää budjetointitarkoituksia varten ja käyttöomaisuuden vaihtamista koskevia päätöksiä varten.

Jokainen käyttöomaisuuserä voidaan liittää yhteen tai useampaan vakuutussopimukseen. Tämä helpottaa sen tarkastamista, että vakuutussopimussummat vastaavat sopimukseen linkitettyjen käyttöomaisuuserien arvoa. Tämä helpottaa myös vuosittaisten vakuutusmaksujen seuraamista.

> [!NOTE]  
>   Voit tallentaa käyttöomaisuustapahtumat **Käyttöomaisuuden KP-päiväkirja**- tai **Käyttöomaisuuspäiväkirja**-ikkunaan sen mukaan, koskevatko tapahtumat talousraportointia vai sisäistä hallintaa. Käyttöomaisuuden ohje sisältää tietoja vain **Käyttöomaisuuden KP-päiväkirja** -ikkunan käyttämisestä. Lisätietoja on kohdassa [Toimintaohje: Käyttöomaisuuden poiston määrittäminen](fa-how-setup-depreciation.md).

> [!NOTE]  
>   Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).

Oletusarvot, käyttöomaisuuden laskenta, kirjausryhmät, kohdistusavaimet, päiväkirjat ja kirjaustyypit on määritettävä ennen käyttöomaisuuden hallinnan aloittamista. Lisätietoja on kohdassa [Käyttöomaisuuden määrittäminen](fa-setup.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.

| Toiminta | Katso |
| --- | --- |
| Luo käyttöomaisuus, liitä poistomenetelmät, kirjaa hankinnat ja jäännösarvot ja tulosta käyttöomaisuusluettelot. |[Toimintaohje: Käyttöomaisuuden hankinta](fa-how-acquire.md) |
| Tallenna huoltokäynnit ja kirjaa kunnossapitokustannukset sekä seuraa niitä. |[Toimintaohje: Käyttöomaisuuden kunnossapito](fa-how-maintain.md) |
| Päivitä vakuutustiedot, kirjaa hankintakustannukset vakuutussopimuksiin, muokkaa vakuutuksen kattavuutta, katsele vakuutustilastoja ja luetteloi vakuutussopimukset. |[Toimintaohje: Käyttöomaisuuden vakuuttaminen](fa-how-insure.md) |
| Luokittele käyttöomaisuus uudelleen, siirrä käyttöomaisuus eri sijainteihin, jaa käyttöomaisuuseriä tai yhdistä niitä. |[Toimintaohje: Käyttöomaisuuden siirtäminen, jakaminen tai yhdistäminen](fa-how-trans-split-combine.md) |
| Muuta käyttöomaisuuserien arvoja ja kirjaa arvonkorotus- sekä arvonalennustransaktiot. |[Toimintaohje: Käyttöomaisuuden uudelleenarvostus](fa-how-revalue.md) |
| Laske ja kirjaa poisto sekä analysoi poisto käyttöomaisuusraporteissa. |[Toimintaohje: Käyttöomaisuuden poisto tai kuolettaminen](fa-how-depreciate-amortize.md) |
| Kirjaa luovutustransaktiot, tarkastele luovutustapahtumia ja kirjaa osittaisia luovutuksia. |[Toimintaohje: Käyttöomaisuuden luovuttaminen tai poistaminen käytöstä](fa-how-dispose-retire.md) |
| Hallitse käyttöominaisuuserien budjetteja, budjetin hankintamenoja, käyttöomaisuuden luovutusten budjetointia ja poistojen budjetointia. |[Toimintaohje: Käyttöomaisuuden budjettien hallinta](fa-how-manage-budgets.md) |

## <a name="see-also"></a>Katso myös
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttökokemuksen mukauttaminen](ui-experiences.md)  
[Rahoitus](finance.md)  
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
