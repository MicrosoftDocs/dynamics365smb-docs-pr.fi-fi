---
title: Freelance-tulojen ilmoitukset (lomake 1099) USA:ssa | Microsoft Docs
description: "IRS edellyttää 1099-verolomakkeen käyttöä toimittajille tehtävissä maksuissa, ja voit määrittää, että 1099-lomake koskee ostoasiakirjaa. Voit myös määrittää toimittajan 1099-koodin."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c20c52927aa979e56aeef7975fbcee1564ca4dd7
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="reporting-transactions-as-1099-liable-in-the-us"></a>Tapahtumien ilmoittaminen 1099-lomakkeella USA:ssa

Yhdysvaltain verohallinto (IRS) vaatii vähintään yhdenlaisen version 1099-lomakkeella tehdystä veroilmoituksesta, joka käsittelee toimittajille suoritettuja maksuja. Kopiot näistä lomakkeista on lähetettävä toimittajille vuosittain tai ennen tammikuun viimeistä päivää. Voit määrittää ostoasiakirjoissa, että asiakirja on 1099-lomakkeen alainen sekä määrittää toimittajan 1099-verokoodin.  

## <a name="1099-codes"></a>1099-verokoodit
[!INCLUDE[d365fin](includes/d365fin_md.md)]issa yleisimmät 1099-koodit on määritetty valmiiksi, eli olet valmis luomaan vaadittavat raportit. Koodit on määritetty **IRS 1099 -lomakkeen ruutu** -ikkunassa, jossa voit myös lisätä uusia 1099-koodeja. Voit sitten määrittää kullekin verovelvolliselle toimittajalle oikean 1099-koodin toimittajakortin **Maksut**-pikavälilehdessä.  

**Toimittajan 1099-verotiedot** -raportilla voit tarkastella tietyn kauden aikana maksettuja 1099-tapahtumia. Voit tulostaa 1099-tapahtumat esitäytetyille lomakkeille vuoden lopussa.  

## <a name="printing-1099-tax-forms"></a>1099-verolomakkeiden tulostus
Voit käyttää seuraavia verolomakkeita **IRS 1099-verolomakkeen ruutu** -ikkunassa:  

* Toimittajan 1099 Div  

  Tulostaa liittovaltion 1099-DIV -lomakkeen, joka koskee osinkoja ja osakeantia. Voit tulostaa kaikki tai tietyt 1099-DIV -lomakkeet. Raportti käyttää koodeja **IRS 1099 -verolomakkeen ruutu** -ikkunasta, jotka koskevat DIV-lomakkeen määrä-ruutuja.  
* Toimittajan 1099 Int -lomake  

  Tulostaa liittovaltion 1099-INT -lomakkeen, joka koskee korkotuloja. Voit tulostaa kaikki tai tietyt 1099-INT -lomakkeet. Raportti käyttää koodeja **IRS 1099 -verolomakkeen ruutu** -ikkunasta, jotka koskevat INT-lomakkeen määrä-ruutuja.  
* Toimittajan 1099 Misc -lomake - Sekalaiset tulot  

  Tulostaa liittovaltion 1099-MISC -lomakkeen, joka koskee sekalaisia tuloja. Voti tulostaa kaikki tai tietyt 1099-MISC -lomakkeet. Raportti käyttää koodeja **IRS 1099 -verolomakkeen ruutu** -ikkunasta, jotka koskevat MISC-lomakkeen määrä-ruutuja.  

Tätä raporttia ja taulukkotietoja koskevat lainsäädännölliset muutokset käsitellään yleensä vuodenvaihteen päivityksissä.
**Toimittajan 1099-tiedot** -raportin suorittaminen ja tarkastus ennen lomakkeiden tulostamista voi olla tarpeen.

## <a name="submitting-1099-tax-forms-electronically"></a>1099-veroilmoituksen lähettäminen sähköisesti
Voit lähettää 1099-veroilmoituksen sähköisesti käyttämällä **Toimittajan 1099-lomake magneettisella tallennusvälineellä** -raporttia. Määrittää 1099-lomakkeet, jotka voidaan viedä. Tämän raportin viemät lomaketiedot ovat samat kuin aikaisemmassa osassa kuvattujen raporttien, jotka tulostavat 1099-lomakkeen.  

Raportti käyttää koodeja **IRS 1099 -verolomakkeen ruutu** -ikkunasta, jotka koskevat lomakkeen määrä-ruutuja. Koodit on yhdistetty tämän raportin tiedostoasetteluiden lomakeruutuihin, joten taulukon tietojen ja raportin version on vastattava tiettyä verovuotta. Jos taulukkoon on lisätty mukautettuja koodeja, ne on yhdistettävä lomakeruutuihin tässä objektissa.  

Tätä raporttia ja taulukkotietoja koskevat lainsäädännölliset muutokset käsitellään yleensä vuodenvaihteen päivityksissä.
**Toimittajan 1099-tiedot** -raportin suorittaminen ja tarkastus ennen tiedoston luontia voi olla tarpeen.  

## <a name="see-also"></a>Katso myös
[Toimintaohje: Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md)  
[Toimintaohje: Ostojen kirjaus](purchasing-how-record-purchases.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

