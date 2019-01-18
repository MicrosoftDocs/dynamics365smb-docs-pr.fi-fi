---
title: "API-mallien määrittäminen | Microsoft Docs"
description: "Kuvaa vaiheet, jotka sinun täytyy käydä läpi,l jotta voit määrittää Dynamics 365 Business Centralin API-malleja."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 7420bd1b8c1c246b608910a35a47ac025eec6b8b
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---

# <a name="configuring-api-templates"></a>API-mallien määritys
[!INCLUDE[d365fin_md](includes/d365fin_md.md)]:n API-kirjasto on taustalla olevien objektien yksinkertaistettu esitys. Sovelluksen kaiki ominaisuudet eivät näy liittyvän API:n kautta. **API-asetukset** -sivulla voidaan määrittää malleja, joita käytetään täyttämään objektin tyhjät ominaisuudet, kun luot POST-toiminnon API:n kautta 

Esimerkiksi, jos määritysmalli on määritetty nimikeobjektille luotaessa uutta nimiketietuetta nimikkeiden API:n kautta, kaikki uuden nimikkeen ominaisuudet, joita ei ole määritetty API-kutsussa, täytetään valitusta mallista. Jos esimerkiksi **Yleinen tuotteen kirjausryhmä** -kentälle ei ole määritetty arvoa API:n kautta, mutta arvo määritetään valitussa mallissa, tällöin mallissa määritettyä kirjausryhmän arvoa käytetään uuteen nimikkeeseen. 

## <a name="setting-up-the-entity-template"></a>Objektimallin määrittäminen
Jotta voit käyttää malleja API-kirjaston kanssa, sinun tulee ensin määrittää mallien ominaisuudet. Voit määrittää nämä mallit **Määritysmallit**-sivulla. Lisätietoja on ohjeaiheessa [Asiakastietojen siirtämisen valmisteleminen](admin-use-templates-to-prepare-customer-data-for-migration.md). 

## <a name="assign-the-template-to-an-api"></a>Mallin liittäminen APIin

Voit liittää mallin APIin suorittamalla seuraavat vaiheet.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **API-asetukset** ja valitse liittyvä linkki.
2. Valitse **Uusi** ja sitten **Järjestys** tietueen arvoksi.  
Jos API-liittymälle (Sivun tunnus) on valittu useita malleja, mallit otetaan käyttöön järjestyksessä, joka on määritetty **Järjestys**-sarakkeessa.   
Kun jokaista mallia käytetään, mallissa määritettyjä kenttäarvoja käytetään vain kenttiin, joilla ei ole jo määritettyä arvoa joko eksplisiittisesti tai API-liittymässä tai järjestyksessä aiemmassa mallissa. 
3. Valitse **Sivun tunnus** -arvo.  
Tämä on API:n sivu, johon malli kohdistetaan. **Sivun tunnus** -haku palauttaa kaikkien kirjastossa saatavilla olevien API-liittymien luettelon.
4. Valitse arvo **Mallin koodi** -kentässä.  
Mallikoodi on sen mallin koodi, joka määritettiin **Määritysmallit**-sivulla. Määritettyjä mallin arvoja käytetään API-liittymään. 
5. Määritä **Ehdot**-kentässä, mitä mallia pitäisi käyttää.  
Määritettyä mallia käytetään API:n kautta luotuun uuteen tietueeseen vain jos objektin uudelle esiintymälle jo määritetyt arvot täyttävät **Ehdot**-kentässä määritetyt ehdot.

## <a name="see-also"></a>Katso myös
[API-dokumentaatio](/dynamics-nav/fin-graph)  
[Connect-sovellusten luominen ratkaisulle [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[API-liittymien ottaminen käyttöön](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[API-liittymien päätepisteet](/dynamics-nav/endpoints-apis-for-dynamics)  
[Yrityksen määrittäminen RapidStart Services -palvelun avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)
