---
title: Uusien yritysten luominen asetusten ohjatun määritysoppaan avulla
description: Business Central -sovellukseen on helppo luoda uusi, tyhjä yritys. Asetusten ohjattu määritysopas antaa tarkkoja ohjeita, ja voit tuoda aiemmin luomasi liiketoimintatiedot.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.search.form: 1803
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8c0c9f03dada569ec19a4bf38d9d4fced1469c2b
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/19/2022
ms.locfileid: "8011411"
---
# <a name="creating-new-companies-in-prod_short"></a>Uusien yritysten luominen [!INCLUDE[prod_short](includes/prod_short.md)]issa

[!INCLUDE[prod_short](includes/prod_short.md)]in liiketoimintayksikölle tai yritykselle kuuluvaa liiketoimintatietojen säilöä kutsutaan *yritykseksi*. Kun rekisteröidyt [!INCLUDE[prod_short](includes/prod_short.md)]iin, saat käyttöösi esimerkkiyrityksen ja tyhjän yrityksen, jonka nimi on *Oma yritys*. Yritysten välillä siirtyminen on helppoa: valitse vain **Omat asetukset** ja siirry toiseen yritykseen. Voit myös luoda uusia yrityksiä [!INCLUDE[prod_short](includes/prod_short.md)]issa yrityksen tarpeiden mukaan. Kun luot uuden yrityksen, asetusten ohjattu määritysopas auttaa varmistamaan, että perustoiminnot ovat kohdallaan. Voit tuoda tämän jälkeen tarvittavat tiedot vanhasta järjestelmästä tai toisesta [!INCLUDE[prod_short](includes/prod_short.md)]in yrityksestä.  

## <a name="creating-a-new-company"></a>Luodaan uusi yritys

Jos päätät lisätä yrityksen [!INCLUDE[prod_short](includes/prod_short.md)]iin, pääset alkuun käyttämällä ohjattua **Luo uusi yritys** -asetusten määritystä. Ohjatun asetustoiminnon voi valita **Yritykset**-sivulla ja **Omat asetukset** -kohdassa **Yritys**-kentän valintaruudussa.  

Ohjatussa asennuksessa on kolme mallia ja tyhjä vaihtoehto:

- **Arviointi - Mallitiedot**  
    Näin luotu yritys muistuttaa esittely-yritystä, jossa on malli- ja asetustietoja.  
- **Tuotanto - Vain määritystiedot**  
    Näin luotu yritys muistuttaa **omaa yritystä**, jossa on asetustietoja mutta mallitiedot puuttuvat.
- **Laajennettu arviointi - Kaikki mallitiedot** Tämä luo yrityksen ja asetustiedot sekä kaikkien toimintojen täydelliset mallitiedot myös valmistukselle ja huoltohallinnolle.
- **Luo uusi - Ei tietoja**  
    Näin luotu yritys on tyhjä eikä siinä ole asetustietoja.  

Jos haluat, että uuden yrityksen käytön aloittaminen on helppoa, valitse **Tuotanto - Vain määritystiedot** ja tuo omat liiketoimintatietosi, kuten asiakkaat, nimikkeet ja toimittajat. Valitse **Uusi**-malli, jos haluat määrittää kaiken itse alusta alkaen. Voit siinä tapauksessa aloittaa tärkeimpien asetustietojen käytön käyttämällä asetusten ohjatun **Yrityksen asennus** -määrityksen ohjeita.  

> [!NOTE]  
> Kun luot uuden yrityksen, kestää joitakin minuutteja, ennen kuin sitä voi käyttää [!INCLUDE[prod_short](includes/prod_short.md)]issa. **Yritykset**-sivulla oleva asennuksen tila ilmaisee, kun uusi yritys on valmis. Voit siirtyä sitten uuteen yritykseen **omissa asetuksissa**.  

30 päivän kokeilujakson aikana luotavien yritysten määrää ei ole rajoitettu, mutta niitä voi käyttää vain kokeilujakson aikana. Pyydä lisätietoja [!INCLUDE[prod_short](includes/prod_short.md)]-kumppanilta.  

## <a name="copying-a-company"></a>Yrityksen kopioiminen

**Yritykset** -sivulla voit käyttää **Kopiointi**-toimintoa toisen yrityksen luomiseen olemassa olevan yrityksen sisällön perusteella. Tästä on hyötyä esimerkiksi silloin, kun haluat testata yritystä häiritsemättä tuotantotietoja.

> [!Important]
> Tätä toimintoa ei voi käyttää yrityksen varmuuskopiointiin. Yrityksen varmuuskopion ottaminen alkaa viemällä tietokanta .bacpac-tiedostona. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeaiheessa [Tietokantojen vieminen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export).

## <a name="company-setup"></a>Yrityksen asennus

Kun kirjaudut uuteen yritykseen, ohjattu **Yrityksen asennus** -toiminto suoritetaan automaattisesti, mikä helpottaa aloittamista. Sinulta kysytään yritystä koskevia tietoja, kuten osoite, pankkitiedot ja varaston arvostusmenetelmä. Nämä tiedot kysytään, koska ne ovat perustietoja monilla [!INCLUDE[prod_short](includes/prod_short.md)]in alueilla ja tällä tavoin niitä ei tarvitse määrittää myöhemmin manuaalisesti.  

Esimerkiksi yrityksen osoitetta käytetään laskuissa ja muissa asiakirjoissa, pankkitietoja käytetään maksuissa ja arvostusmenetelmän avulla lasketaan varaston arvostuksen lisäksi myös hintoja.  

Kun perustiedot on annettu, voi määrittää loput keskeiset alueet. Sen jälkeen voi aloittaa liiketoimintatietojen, kuten asiakkaiden ja toimittajien, lisäämisen. Lisätietoja on ohjeaiheessa [[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md).  

## <a name="companies-and-environments"></a>Yritykset ja ympäristöt

[!INCLUDE [company_environment](includes/company_environment.md)]

Lisätietoja on kohdassa [Siirtyminen toiseen yritykseen tai ympäristöön](ui-organization-switch.md). 

## <a name="changing-a-companys-name"></a>Yrityksen nimen muuttaminen

Kun yritys on luotu, sen nimeä ei voi muuttaa. Mutta voit muuttaa sen **näyttönimeä** eli tekstiä, joka näkyy kaikkialla sovelluksessa yrityksen nimenä.  

> [!TIP]
> Voit nimetä yrityksen uudelleen, jos käytät [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -versiota.

## <a name="see-also"></a>Katso myös

[Business Central -sovelluksen mukauttaminen](ui-customizing-overview.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]