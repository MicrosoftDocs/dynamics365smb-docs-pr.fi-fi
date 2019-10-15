---
title: Tietoja kustannuslaskennasta | Microsoft Docs
description: Kustannuslaskennan avulla voit ymmärtää käynnissä olevan liiketoiminnan kustannuksia.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 053a0ca21ff26b53cabcc8894ed1cd0e48c904b0
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302666"
---
# <a name="about-cost-accounting"></a>Tietoja kustannuslaskennasta
Kustannuslaskenta auttaa tiedostamaan liiketoimintaan sisältyviä kustannuksia. Kustannuslaskennan tiedot on suunniteltu analysoimaan:  

-   Millaisia kustannuksia voi syntyä yritysoiminnasta?  
-   Mistä kustannukset johtuvat?  
-   Kuka kestää kustannukset?  

Kustannuslaskennassa kohdistetaan toimintojen, osastojen, tuotteiden ja projektien toteutuneet ja budjetoidut kustannukset yrityksen tuottavuuden analysointia varten.  

## <a name="workflow-in-cost-accounting"></a>Työnkulku kustannuslaskennassa  
Kustannuslaskennassa on seuraavat pääosat:  

-   Kustannustyypit, kustannuspaikat ja kustannuskohteet  
-   Kustannustapahtumat ja kustannuspäiväkirjat  
-   Kustannusten kohdistukset  
-   Kustannusbudjetit
-   Kustannusraportti  

Seuraava kaavio näyttää työnkulun kustannuslaskennassa.  

![Yleistietoja kustannuslaskennasta](media/costaccountingoverview.png "CostAccountingOverview")  

## <a name="cost-types-cost-centers-and-cost-objects"></a>Kustannustyypit, kustannuspaikat ja kustannuskohteet  
Määritä kustannustyypit, kustannuspaikat ja kustannuskohteet analysoidaksesi mitä kustannukset ovat, mistä kustannukset ovat peräisin ja kuka vastaa kustannuksista.  

Voit määrittää kustannustyyppikaavion, jonka rakenne ja toiminnallisuus muistuttavat pääkirjanpidon tilikarttaa. Voit siirtää kirjanpidon tuloslaskelmatilit tai luoda oman kustannustyyppikaavion.  

Kustannuspaikat ovat osastoja ja tulosyksiköitä, jotka ovat vastuussa kustannuksista ja tuloista. Usein kustannuslaskennassa on enemmän kustannuspaikkoja kuin missään pääkirjanpitoon määritetyssä dimensiossa. Pääkirjanpidossa käytetään yleensä vain ensimmäisen tason kustannuspaikkoja ja alkuperäisiä kustannuksia. Kustannuslaskennassa luodaan lisäkohdistustasojen lisäkustannuspaikat.  

Kustannuskohteet ovat yrityksen tuotteita, tuoteryhmiä tai palveluja. Nämä ovat kustannuksista vastaavan yrityksen valmiita tuotteita.  

Voit linkittää osastojen kustannuspaikat ja projektien kustannuskohteet yritykseen. Voit kuitenkin linkittää kustannuspaikat ja kustannuskohteet pääkirjanpidon mihin tahansa dimensioon ja lisätä niille välisummat ja otsikot.  

## <a name="cost-entries-and-cost-journals"></a>Kustannustapahtumat ja kustannuspäiväkirjat  
Operatiiviset kustannukset voidaan siirtää pääkirjanpidosta. Voit siirtää automaattisesti tapahtumien kustannukset pääkirjanpidosta kustannustapahtumiin jokaisen kirjauksen yhteydessä. Voit myös käyttää eräajoa siirtääksesi pääkirjanpidon tapahtumat kustannustapahtumiin, jotka perustuvat päivittäisiin tai kuukausittaisiin yhteenvetoihin.  

Kustannuspäiväkirjoissa voi kirjata kustannukset ja toiminnot, joita ei saada pääkirjanpidosta tai jotka eivät ole kohdistusten luomia. Voit esimerkiksi kirjata pelkkiä operatiivisia kustannuksia, sisäisiä kuluja, kohdistuksia ja korjaavia tapahtumia kustannustyyppien, kustannuspaikkojen ja kustannuskohteiden välille yksitellen tai toistuvasti.  

## <a name="cost-allocations"></a>Kustannusten kohdistukset  
Kohdistukset siirtävät kustannukset ja tuotot eri kustannustyyppien, kustannuspaikkojen ja kustannuskohteiden välillä. Yleiskustannukset kirjataan ensin kustannuspaikkoihin ja myöhemmin kustannuskohteisiin. Tämä voidaan tehdä esimerkiksi myyntiosastossa, joka myy useita tuotteita samanaikaisesti. Välittömät kustannukset ovat kustannuksia, jotka voidaan suoraan kohdistaa kustannuskohteeseen, esimerkiksi tietyn tuotteen materiaaliostoksiin.  

Kohdistusperuste, jota käytetään, ja kohdistusmääritelmän paikkansapitävyyden kustannukset vaikuttavat kustannusten kohdistamisen tuloksiin. Kohdistusmääritelmällä voidaan kohdistaa kustannukset ensin pääkustannuspaikoille ja niin kutsutuille esikustannuskeskuksille, ja sitten kustannuspaikoilta kustannuskohteille.  

Jokainen kohdistus koostuu kohdistuslähteestä ja yhdestä tai useammasta kohdistustavoitteesta. Voit kohdistaa todelliset arvot tai budjetoidut arvot staattisen kohdistamismenetelmän avulla, joka perustuu määriteltyihin arvoihin, kuten pinta-alaan tai vahvistettuun varaussuhteeseen 5: 2: 4. Voit myös kohdentaa todelliset arvot tai budjetoidut arvot käyttämällä dynaamista kohdistamismenetelmää yhdeksän ennalta määritetyn kohdistuksen perusteen ja 12 dynaamisen päivämääräalueen kanssa.  

## <a name="cost-budgets"></a>Kustannusbudjetit  
Kustannusbudjetteja voi määrittää kuinka monta tahansa. Voit kopioida kustannusbudjetin pääkirjanpitoon ja päinvastoin. Voit siirtää budjetoidut kustannukset todellisina kustannuksina.  

## <a name="cost-reporting"></a>Kustannusraportointi  
Useimmat raportit ja tilastot perustuvat kirjattuihin kustannustapahtumiin. Voit asettaa tulosten lajittelun ja suodattimien avulla määrittää, mitkä tiedot täytyy näyttää. Voit luoda raportteja kustannusanalyysin jakelua varten. Voit lisäksi käyttää vakio KP-raporttimallia määrittääksesi miten raportit kustannustyyppikaaviossa näkyvät.  

## <a name="see-also"></a>Katso myös  
 [Kustannuslaskenta](finance-manage-cost-accounting.md)  
 [Rahoitus](finance.md)   
 [Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
