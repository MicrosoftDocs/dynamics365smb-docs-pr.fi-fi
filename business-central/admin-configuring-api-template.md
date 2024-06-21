---
title: API-mallien määritys
description: 'Kuvaa vaiheet, jotka sinun täytyy käydä läpi, jotta voit määrittää Dynamics 365 Business Centralin ohjelmointirajapintamalleja.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'API templates, configuring templates'
ms.search.form: 5469
ms.date: 06/07/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# API-mallien määritys

[!INCLUDE[prod_short_md](includes/prod_short.md)]:n API-kirjasto on taustalla olevien objektien yksinkertaistettu esitys. Sovelluksen kaiki ominaisuudet eivät näy liittyvän API:n kautta. **API-asetukset** -sivulla voidaan määrittää malleja, joita käytetään täyttämään objektin tyhjät ominaisuudet, kun luot POST-toiminnon API:n kautta 

Esimerkiksi, jos määritysmalli on määritetty nimikeobjektille luotaessa uutta nimiketietuetta nimikkeiden API:n kautta, kaikki uuden nimikkeen ominaisuudet, joita ei ole määritetty API-kutsussa, täytetään valitusta mallista. Jos esimerkiksi **Yleinen tuotteen kirjausryhmä** -kentälle ei ole määritetty arvoa API:n kautta, mutta arvo määritetään valitussa mallissa, tällöin mallissa määritettyä kirjausryhmän arvoa käytetään uuteen nimikkeeseen. 

## Objektimallin määrittäminen

Jotta voit käyttää malleja API-kirjaston kanssa, sinun tulee ensin määrittää mallien ominaisuudet. Voit määrittää nämä mallit **Määritysmallit**-sivulla. Lisätietoja hallintasisällössä: [Paikallisten tietojen siirtäminen Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) -ohjelmaan (vain englanniksi).  

## Mallin liittäminen APIin

Voit liittää mallin APIin suorittamalla seuraavat vaiheet.

> [!NOTE]  
> API-mallit voidaan määrittää vain seuraavilla API-sivuilla: contacts, countriesRegions, currencies, customers, employees, itemCategories, paymentMethods, paymentTerms, shipmentMethods, unitsOfMeasure ja vendors.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **API-määrittäminen** ja valitse sitten vastaava linkki.
2. Valitse **Uusi** ja sitten **Järjestys** tietueen arvoksi.  

    Jos API-liittymälle (Sivun tunnus) on valittu useita malleja, mallit otetaan käyttöön järjestyksessä, joka on määritetty **Järjestys**-sarakkeessa.  

    Kun jokaista mallia käytetään, mallissa määritettyjä kenttäarvoja käytetään vain kenttiin, joilla ei ole jo määritettyä arvoa joko eksplisiittisesti tai API-liittymässä tai järjestyksessä aiemmassa mallissa.  
3. Valitse **Sivun tunnus** -arvo.  

    Tämä on API:n sivu, johon malli kohdistetaan. **Sivun tunnus** -haku palauttaa kaikkien kirjastossa saatavilla olevien API-liittymien luettelon.
4. Valitse arvo **Mallin koodi** -kentässä.  

    Mallikoodi on sen mallin koodi, joka määritettiin **Määritysmallit**-sivulla. Määritettyjä mallin arvoja käytetään API-liittymään.  
5. Määritä **Ehdot**-kentässä, mitä mallia pitäisi käyttää.  

    Määritettyä mallia käytetään API:n kautta luotuun uuteen tietueeseen vain jos objektin uudelle esiintymälle jo määritetyt arvot täyttävät **Ehdot**-kentässä määritetyt ehdot.

## Katso myös

[API-dokumentaatio](/dynamics-nav/fin-graph)  
[Connect Appsin luominen ratkaisulle [!INCLUDE[prod_short_md](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[API-liittymien ottaminen käyttöön](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[API-liittymien päätepisteet](/dynamics-nav/endpoints-apis-for-dynamics)  
[Hallinta](admin-setup-and-administration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]