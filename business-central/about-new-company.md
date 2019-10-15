---
title: Uusien yritysten luominen asetusten ohjatun määritysoppaan avulla | Microsoft Docs
description: Business Central -sovellukseen on helppo luoda uusi, tyhjä yritys. Asetusten ohjattu määritysopas antaa tarkkoja ohjeita, ja voit tuoda aiemmin luomasi liiketoimintatiedot.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: e22b93182627a5954b2aa2f1fb1fa4938d89be89
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300735"
---
# <a name="creating-new-companies-in-included365finincludesd365fin_mdmd"></a>Uusien yritysten luominen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa
[!INCLUDE[d365fin](includes/d365fin_md.md)]in liiketoimintayksikölle tai yritykselle kuuluvia liiketoimintatietojen säilöjä kutsutaan *yrityksiksi*. Kun rekisteröidyt [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, saat käyttöösi esimerkkiyrityksen ja tyhjän yrityksen, jonka nimi on *Oma yritys*. Yritysten välillä siirtyminen on helppoa: valitse vain **Omat asetukset** ja siirry toiseen yritykseen. Voit myös luoda uusia yrityksiä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa yrityksen tarpeiden mukaan. Kun luot uuden yrityksen, asetusten ohjattu määritysopas auttaa varmistamaan, että perustoiminnot ovat kohdallaan. Voit tuoda tämän jälkeen tarvittavat tiedot vanhasta järjestelmästä tai toisesta [!INCLUDE[d365fin](includes/d365fin_md.md)]in yrityksestä.  

## <a name="create-new-company"></a>Luo uusi yritys
Jos päätät lisätä yrityksen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, pääset alkuun käyttämällä ohjattua **Luo uusi yritys** -asetusten määritystä. Ohjatun asetustoiminnon voi valita **Yritykset**-sivulla ja **Omat asetukset** -kohdassa **Yritys**-kentän valintaruudussa.  

Ohjatussa asennustoiminnossa on kolme mallia:

-   **Arviointi - Mallitiedot**  
    Näin luotu yritys muistuttaa esittely-yritystä, jossa on malli- ja asetustietoja.  
-   **Tuotanto - Vain määritystiedot**  
    Näin luotu yritys muistuttaa **omaa yritystä**, jossa on asetustietoja mutta mallitiedot puuttuvat.
-   **Laajennettu arviointi - Kaikki mallitiedot** Tämä luo yrityksen ja asetustiedot sekä kaikkien toimintojen täydelliset mallitiedot myös valmistukselle ja huoltohallinnolle.
-   **Luo uusi - Ei tietoja**  
    Näin luotu yritys on tyhjä eikä siinä ole asetustietoja.  

Jos haluat, että uuden yrityksen käytön aloittaminen on helppoa, valitse **Tuotanto - Vain määritystiedot** ja tuo omat liiketoimintatietosi, kuten asiakkaat, nimikkeet ja toimittajat. Valitse **Uusi**-malli, jos haluat määrittää kaiken itse alusta alkaen. Voit siinä tapauksessa aloittaa tärkeimpien asetustietojen käytön käyttämällä asetusten ohjatun **Yrityksen asennus** -määrityksen ohjeita.  

> [!NOTE]  
>   Kun luot uuden yrityksen, kestää joitakin minuutteja, ennen kuin sitä voi käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. **Yritykset**-sivulla oleva asennuksen tila ilmaisee, kun uusi yritys on valmis. Voit siirtyä sitten uuteen yritykseen **omissa asetuksissa**.  

30 päivän kokeilujakson aikana luotavien yritysten määrää ei ole rajoitettu, mutta niitä voi käyttää vain kokeilujakson aikana. Pyydä lisätietoja [!INCLUDE[d365fin](includes/d365fin_md.md)]-kumppanilta.  

## <a name="company-setup"></a>Yrityksen asennus
Kun kirjaudut uuteen yritykseen, ohjattu **Yrityksen asennus** -toiminto suoritetaan automaattisesti, mikä helpottaa aloittamista. Sinulta kysytään yritystä koskevia tietoja, kuten osoite, pankkitiedot ja varaston arvostusmenetelmä. Nämä tiedot kysytään, koska ne ovat perustietoja monilla [!INCLUDE[d365fin](includes/d365fin_md.md)]in alueilla ja tällä tavoin niitä ei tarvitse määrittää myöhemmin manuaalisesti.  

Esimerkiksi yrityksen osoitetta käytetään laskuissa ja muissa asiakirjoissa, pankkitietoja käytetään maksuissa ja arvostusmenetelmän avulla lasketaan varaston arvostuksen lisäksi myös hintoja.  

Kun perustiedot on annettu, voi määrittää loput keskeiset alueet. Sen jälkeen voi aloittaa liiketoimintatietojen, kuten asiakkaiden ja toimittajien, lisäämisen. Lisätietoja on ohjeaiheessa [[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md).  

## <a name="see-also"></a>Katso myös
[Business Central -sovelluksen mukauttaminen](ui-customizing-overview.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Käytön aloittaminen](product-get-started.md)  
