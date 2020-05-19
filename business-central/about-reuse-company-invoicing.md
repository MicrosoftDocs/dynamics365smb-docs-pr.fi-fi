---
title: Invoicing- ja Business Central -sovellusten käyttäminen | Microsoft Docs
description: Ratkaisu, jonka avulla voi käyttää Microsoft Invoicingia, kun olet rekisteröitynyt Dynamics 365 Business Centraliin.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Office 365
ms.date: 04/30/2020
ms.author: bholtorf
ms.openlocfilehash: 7776cd01218f5959734173226574bb4a0d043153
ms.sourcegitcommit: 866f0e6ed9df3397072b9df838e31c3a1f4b626d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2020
ms.locfileid: "3333858"
---
# <a name="using-the-same-office-365-account-in-d365fin-and-microsoft-invoicing"></a>Saman Office 365 -tilin käyttäminen [!INCLUDE[d365fin](includes/d365fin_long_md.md)]:ssä ja Microsoft Invoicingissa
Kun rekisteröidyt [!INCLUDE[d365fin](includes/d365fin_md.md)]:n kokeiluversioon, voit siirtyä 30 päivän arviointivaiheeseen, aloittaa tilauksen tai lopettaa [!INCLUDE[d365fin](includes/d365fin_md.md)]:n käytön. Joka tapauksessa, olet ehkä jossain vaiheessa nähnyt jotain, jonka nimi on **Microsoft Invoicing**, ja napsauttanut sitä. Tämä oli sovellus, joka oli osa sitä, mikä nyt Microsoft 365 Business Standard ja tunnettiin aiemmin nimellä Office 365 Business Premium Subscription, joten kaikki eivät ole nähneet sen ruutua Office 365 -kokemuksessaan.  

Microsoft Invoicingia ei ole enää saatavilla, mutta jos sinun täytyy kirjautua sisään laskutukseen tietojen hakemista varten, saatat nähdä viestin, että Microsoft Invoicingia ei voi käyttää, koska tiliäsi käytetään [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa.  

Saat samanlaisen ilmoituksen, jos asennat Invoicingin mobiilisovelluksen.  

## <a name="workaround"></a>Ratkaisu
Invoicing ja [!INCLUDE[d365fin](includes/d365fin_md.md)] jakavat saman alustan. Tämän vuoksi sinut tunnistetaan [!INCLUDE[d365fin](includes/d365fin_md.md)]:n nykyiseksi käyttäjäksi, kun valitset Microsoft 365 -hallintakeskusruudussa Invoicing. Syynä on se, että Invoicing ei voi käyttää samaa yritystä kuin [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Tämän vuoksi sinun on kirjauduttava [!INCLUDE[d365fin](includes/d365fin_md.md)]:een ja nimettävä aiemmin luotu yritys uudelleen. Seuraavaksi sinun on luotava uusi yritys, jota voit käyttää Invoicingissa. Mitään tietoja ei siirretä tai korvata tätä ratkaisua käytettäessä.

### <a name="to-rename-your-company"></a>Yrityksen nimeäminen uudelleen
1. Kirjaudu [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.
2. Valitse oikeassa yläkulmassa **Asetukset**-kuvake ![Asetukset](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") ja valitse sitten **Omat asetukset**.
3. Valitse toinen yritys **Yritys**-kentässä.
4. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yritykset** ja valitse sitten liittyvä linkki.  
5. Valitse **Omat yritykset** -sivulla **Muokkaa luetteloa**.  
6. Vaihda *Oma yritys* -merkinnän nimi.  

    Odota useita minuutteja. Taustalla olevaan tietokantaa tehdä muutoksia, ja kestää jonkin aikaa.
7.  Kun järjestelmä on taas valmis, valitse **Luo uusi yritys** -painike.  
8.  Määritä avautuvassa valintaikkunassa nimeksi *Oma yritys* ja valitse **Tuotanto - Vain määritystiedot** -vaihtoehto.  

Myös tämä toiminto kestää useita minuutteja. Kun prosessi on valmis, voi käyttää Invoicingia Microsoft 365 Business Standardin osana. Mutta vain tietojen viemiseen, koska Invoicing-sovellus on vanhentunut.  

### <a name="what-about-my-data"></a>Mitä tiedoille tapahtuu?
Kun nimeät alkuperäisen oman yrityksen uudelleen, tietokantataulukot, joihin aiemmin luodut [!INCLUDE[d365fin](includes/d365fin_md.md)]:n tiedot on tallennettu, nimetään uudelleen mutta itse tietoihin ei kosketa.  

Jos käytät sekä Invoicingia että [!INCLUDE[d365fin](includes/d365fin_md.md)]:tä, tiedot tallennetaan kahteen eri säilöön (kahteen yritykseen). Mitään ei jaeta, joten kummankin yrityksen asiakkaita ja nimikkeitä on hallittava erikseen.  

## <a name="see-also"></a>Katso myös
[Usein kysytyt kysymykset](across-faq.md)  
[Hallinta](admin-setup-and-administration.md)  
