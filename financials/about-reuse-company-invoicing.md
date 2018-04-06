---
title: "Invoicingin ja Finance and Operations, Business editionin käyttäminen | Microsoft Docs"
description: "Ratkaisu Microsoft Invoicingin käyttämiseen, kun olet rekisteröitynyt Dynamics 365 for Finance and Operations, Business editioniin."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 803569ed99f00b9055c5a6ec6e4ffae67d9df2bd
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a>Saman Office 365 -tilin käyttäminen [!INCLUDE[d365fin](includes/d365fin_long_md.md)]:ssä ja Microsoft Invoicingissa
Kun rekisteröidyt [!INCLUDE[d365fin](includes/d365fin_md.md)]:n kokeiluversioon, voit siirtyä 30 päivän arviointivaiheeseen, aloittaa tilauksen tai lopettaa [!INCLUDE[d365fin](includes/d365fin_md.md)]:n käytön. Kaikissa näissä tapauksissa Office-portaaliin kirjautumisen jälkeen näkyvissä voi olla **Business center** -ruutu, jota voi napsauttaa. Se sisältyy Office 365 Business Premium -tilaukseen, joten kaikki Office-portaalin käyttäjät eivät näe ruutua.  

Jos Business center -ruutu on käytettävissä, siinä on **Invoicing**-osa. Jos yrität käyttää tätä osaa, saat ilmoituksen, jonka mukaan et voi käyttää Microsoft Invoicingia, koska tiliä käytetään [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä.  

Saat samanlaisen ilmoituksen, jos asennat Invoicingin mobiilisovelluksen.  

## <a name="workaround"></a>Ratkaisu
Invoicing ja [!INCLUDE[d365fin](includes/d365fin_md.md)] jakavat saman alustan. Tämän vuoksi sinut tunnistetaan [!INCLUDE[d365fin](includes/d365fin_md.md)]:n nykyiseksi käyttäjäksi, kun valitset Business center -ruudussa Invoicing. Syynä on se, että Invoicing ei voi käyttää samaa yritystä kuin [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Tämän vuoksi sinun on kirjauduttava [!INCLUDE[d365fin](includes/d365fin_md.md)]:een ja nimettävä aiemmin luotu yritys uudelleen. Seuraavaksi sinun on luotava uusi yritys, jota voit käyttää Invoicingissa. Mitään tietoja ei siirretä tai korvata tätä ratkaisua käytettäessä.

### <a name="to-rename-your-company"></a>Yrityksen nimeäminen uudelleen
1.  Kirjaudu [!INCLUDE[d365fin](includes/d365fin_md.md)]:een.  
2.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Omat yritykset** ja valitse sitten aiheeseen liittyvä linkki.  
3.  Valitse **Omat yritykset** -ikkunassa **Muokkaa luetteloa** -painike.  
4.  Vaihda *Oma yritys* -merkinnän nimi.  

    Odota useita minuutteja. Taustalla olevaan tietokantaa tehdä muutoksia, ja kestää jonkin aikaa.
5.  Kun järjestelmä on taas valmis, valitse **Luo uusi yritys** -painike.  
6.  Määritä avautuvassa valintaikkunassa nimeksi *Oma yritys* ja valitse **Tuotanto - Vain määritystiedot** -vaihtoehto.  

Myös tämä toiminto kestää useita minuutteja. Kun prosessi on valmis, voi käyttää Invoicingia Office 365 Business Premiumin osana.  

### <a name="what-about-my-data"></a>Mitä tiedoille tapahtuu?
Kun nimeät alkuperäisen oman yrityksen uudelleen, tietokantataulukot, joihin aiemmin luodut [!INCLUDE[d365fin](includes/d365fin_md.md)]:n tiedot on tallennettu, nimetään uudelleen mutta itse tietoihin ei kosketa.  

Jos käytät sekä Invoicingia että [!INCLUDE[d365fin](includes/d365fin_md.md)]:tä, tiedot tallennetaan kahteen eri säilöön (kahteen yritykseen). Mitään ei jaeta, joten kummankin yrityksen asiakkaita ja nimikkeitä on hallittava erikseen.  

## <a name="see-also"></a>Katso myös
[Usein kysytyt kysymykset](across-faq.md)  
[Asetukset ja hallinto](admin-setup-and-administration.md)  

