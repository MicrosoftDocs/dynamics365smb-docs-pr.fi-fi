---
title: Yrityksen keskittimen vianmääritys
description: Tietoja siitä, miten voit kiertää ongelmia käyttäessäsi Dynamics 365 Business Centralin yrityskeskusta useiden yritysten väliseen hallintaan.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.search.form: 1151
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 585e23a25397952ede809a76d4e001df9c60b449
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8128815"
---
# <a name="troubleshooting-your-company-hub"></a>Yrityksen keskittimen vianmääritys

Yritysten lisääminen yrityksen keskittimeen on helppoa, mutta tässä artikkelissa käsitellään mahdollisesti esiin tulevia ongelmia.  

## <a name="check-errors"></a>Tarkista virheet

Voit tarkastella viimeaikaisten virheiden luetteloa **Tarkista virheet** -toiminnolla. Voit nähdä kunkin virheen lisätiedot, ja voit siivota lokin poistamalla vanhoja tapahtumia.  

## <a name="connection-failed"></a>Yhteyden muodostus epäonnistui

Voi olla muutamia syitä siihen, miksi et pysty muodostamaan yhteyttä yritykseen, mukaan lukien seuraavat:

- **Ympäristölinkki**-kentässä annettu URL-osoite ei kelpaa  

  Siirry **ympäristölinkit** -sivulle, avaa ympäristö, johon et voi muodostaa yhteyttä, ja valitse sitten **Testaa yhteyden muodostus** -toiminto.  
- Asiakkaan yritys on offline-tilassa esimerkiksi päivityksen vuoksi

  Valitse koontinäytössä ensin **Työkalut**-valikkovaihtoehto ja sitten **Tarkista virheet**. Jos avautuvassa teknisten tietojen luettelossa näkyy virheitä, järjestelmänvalvojaan on ehkä syytä ottaa yhteyttä. Jos virhesanoma esimerkiksi ilmoittaa, että *Palvelin on hylännyt asiakkaan tunnistetiedot*, syynä on todennäköisesti puuttuvat käyttöoikeudet.  
- Sinulla ei ole oikeuksia kaikkiin yrityksiin ympäristössä, johon yrität muodostaa yhteyttä

  [!INCLUDE [prod_short](includes/prod_short.md)]:ssa organisaatiossa voi olla monta liiketoimintayksikköä, joita kutsutaan yrityksiksi, ja sinulla ei ehkä ole käyttöoikeuksia kaikkiin yrityksiin. Varmista yhdessä järjestelmänvalvojan tai asiakkaan kanssa, että sinulla on kaikkien niiden yritysten käyttöoikeudet, joita haluat käsitellä.  

## <a name="data-does-not-refresh"></a>Tietoja ei päivitetä

Kun lisäät yrityksen tai pyydät tietojen päivittämistä, [!INCLUDE [prod_short](includes/prod_short.md)] noutaa tiedot. Sinun on kuitenkin päivitettävä sivu itse valitsemalla esimerkiksi **Lataa kaikki yritykset uudelleen** -toiminnon, päivittämällä selaimen sivu tai poistumalla koontinäytöstä ja palaamalla siihen takaisin.  

Jos olet lisännyt yrityksen, mutta se ei näy luettelossa, voit päivittää luettelon myös **Lataa kaikki yritykset uudelleen** -toiminnon avulla.

## <a name="see-also"></a>Katso myös

[Työnhallinta useiden yritysten välillä yrityksen keskittimessä](company-hub.md)  
[Yritysten lisääminen yrityksen keskittimeen](company-hub-add-company.md)  
[Kirjanpitäjän käyttökokemukset Business Centralissa](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]