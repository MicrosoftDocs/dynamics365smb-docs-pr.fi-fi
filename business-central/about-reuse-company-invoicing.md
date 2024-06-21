---
title: Laskutuksen Business Centralin käyttö
description: 'Ratkaisu, jonka avulla voi käyttää Microsoft Invoicingia, kun olet rekisteröitynyt Dynamics 365 Business Centraliin.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Invoicing, Microsoft 365'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Saman Microsoft 365 -tilin käyttäminen [!INCLUDE[prod_short](includes/prod_long.md)]issa ja Microsoft Invoicingissa
Kun rekisteröidyt [!INCLUDE[prod_short](includes/prod_short.md)]:n kokeiluversioon, voit siirtyä 30 päivän arviointivaiheeseen, aloittaa tilauksen tai lopettaa [!INCLUDE[prod_short](includes/prod_short.md)]:n käytön. Joka tapauksessa, olet ehkä jossain vaiheessa nähnyt jotain, jonka nimi on **Microsoft Invoicing**, ja napsauttanut sitä. Tämä oli sovellus, joka oli osa sitä, mikä nyt Microsoft 365 Business Standard ja tunnettiin aiemmin nimellä Microsoft 365 Business Premium Subscription, joten kaikki eivät ole nähneet sen ruutua Microsoft 365 -kokemuksessaan.  

Microsoft Invoicingia ei ole enää saatavilla, mutta jos sinun täytyy kirjautua sisään laskutukseen tietojen hakemista varten, saatat nähdä viestin, että Microsoft Invoicingia ei voi käyttää, koska tiliäsi käytetään [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa.  

Saat samanlaisen ilmoituksen, jos asennat Invoicingin mobiilisovelluksen.  

## Ratkaisu
Invoicing ja [!INCLUDE[prod_short](includes/prod_short.md)] jakavat saman alustan. Tämän vuoksi sinut tunnistetaan [!INCLUDE[prod_short](includes/prod_short.md)]:n nykyiseksi käyttäjäksi, kun valitset Microsoft 365 -hallintakeskuksessa Invoicing. Syynä on se, että Invoicing ei voi käyttää samaa yritystä kuin [!INCLUDE[prod_short](includes/prod_short.md)].  

Tämän vuoksi sinun on kirjauduttava [!INCLUDE[prod_short](includes/prod_short.md)]:een ja nimettävä aiemmin luotu yritys uudelleen. Seuraavaksi sinun on luotava uusi yritys, jota voit käyttää Invoicingissa. Mitään tietoja ei siirretä tai korvata tätä ratkaisua käytettäessä.

### Yrityksen nimeäminen uudelleen
1. Kirjaudu [!INCLUDE[prod_short](includes/prod_short.md)]iin.
2. Valitse oikeassa yläkulmassa **Asetukset**-kuvake ![Asetukset.](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") ja valitse sitten **Omat asetukset**.
3. Valitse toinen yritys **Yritys**-kentässä.
4. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yritykset** ja valitse sitten vastaava linkki.  
5. Valitse **Omat yritykset** -sivulla **Muokkaa luetteloa**.  
6. Vaihda *Oma yritys* -merkinnän nimi.  

    Odota useita minuutteja. Taustalla olevaan tietokantaa tehdä muutoksia, ja kestää jonkin aikaa.
7.  Kun järjestelmä on taas valmis, valitse **Luo uusi yritys** -painike.  
8.  Määritä avautuvassa valintaikkunassa nimeksi *Oma yritys* ja valitse **Tuotanto - Vain määritystiedot** -vaihtoehto.  

Myös tämä toiminto kestää useita minuutteja. Kun prosessi on valmis, voi käyttää Invoicingia Microsoft 365 Business Standardin osana. Mutta vain tietojen viemiseen, koska Invoicing-sovellus on vanhentunut.  

### Mitä tiedoille tapahtuu?
Kun nimeät alkuperäisen oman yrityksen uudelleen, tietokantataulukot, joihin aiemmin luodut [!INCLUDE[prod_short](includes/prod_short.md)]:n tiedot on tallennettu, nimetään uudelleen mutta itse tietoihin ei kosketa.  

Jos käytät sekä Invoicingia että [!INCLUDE[prod_short](includes/prod_short.md)]:tä, tiedot tallennetaan kahteen eri säilöön (kahteen yritykseen). Mitään ei jaeta, joten kummankin yrityksen asiakkaita ja nimikkeitä on hallittava erikseen.  

## Katso myös
[Usein kysytyt kysymykset](across-faq.yml)  
[Hallinta](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]