---
title: Tietoja kustannuslaskennasta
description: Kustannuslaskennan avulla voit ymmärtää käynnissä olevan liiketoiminnan kustannuksia. Kustannuslaskennan tiedot on suunniteltu analysoimaan monia seikkoja.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '1101, 1103, 1105, 1108, 1111, 1112, 1124, 1123'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Tietoja kustannuslaskennasta

Kustannuslaskennan avulla voit ymmärtää käynnissä olevan liiketoiminnan kustannuksia. Kustannuslaskennan tiedot on suunniteltu analysoimaan:  

- Minkä tyyppisiä kuluja yrityksen toiminnasta aiheutuu.  
- Mistä kustannukset johtuvat.
- Kuka vastaa kustannuksista.

Kustannuslaskennassa kohdistetaan toimintojen, osastojen, tuotteiden ja projektien toteutuneet ja budjetoidut kustannukset yrityksen tuottavuuden analysointia varten.  

## Työnkulku kustannuslaskennassa

Kustannuslaskennassa on seuraavat pääosat:  

- Kustannustyypit, kustannuspaikat ja kustannuskohteet  
- Kustannustapahtumat ja kustannuspäiväkirjat  
- Kustannusten kohdistukset  
- Kustannusbudjetit
- Kustannusraportti  

Seuraava kaavio näyttää työnkulun kustannuslaskennassa.  

![Kustannuslaskennan yleiskatsaus.](media/costaccountingoverview.png "CostAccountingOverview")  

## Kustannustyypit, kustannuspaikat ja kustannuskohteet

Määritä kustannustyypit, kustannuspaikat ja kustannuskohteet analysoidaksesi mitä kustannukset ovat, mistä kustannukset ovat peräisin ja kuka vastaa kustannuksista.  

Ensiksi, voit määrittää kustannustyyppikaavion, jonka rakenne ja toiminnallisuus muistuttavat pääkirjanpidon tilikarttaa. Voit luoda oman kustannuslajikaavion tai tehdä sen siirtämällä pääkirjanpidon tuloslaskelmatilejä.  

Kustannuspaikat ovat osastoja ja tulosyksiköitä, jotka ovat vastuussa kustannuksista ja tuloista. Usein kustannuslaskennassa on enemmän kustannuspaikkoja kuin missään pääkirjanpitoon määritetyssä dimensiossa. Pääkirjanpidossa käytetään tyypillisesti vain ensimmäisen tason kustannuspaikkoja ja alkuperäisiä kustannuksia. Kustannuslaskennassa luodaan lisäkohdistustasojen lisäkustannuspaikat.  

Kustannuskohteet ovat yrityksen tarjoamia tuotteita, tuoteryhmiä tai palveluja. Nämä kohteet ovat "valmiita tuotteita", jotka kantavat kustannukset.  

Voit linkittää osastojen kustannuspaikat ja projektien kustannuskohteet yritykseen. Pääkirjanpidon avulla voit linkittää kustannuspaikkoja ja kustannusobjekteja mihin tahansa dimensioihin ja täydentää näitä tietoja välisummilla ja otsikoilla.  

## Kustannustapahtumat ja kustannuspäiväkirjat

Operatiiviset kustannukset voidaan siirtää pääkirjanpidosta. Voit siirtää automaattisesti tapahtumien kustannukset pääkirjanpidosta kustannustapahtumiin jokaisen kirjauksen yhteydessä. Voit myös käyttää eräajoa siirtääksesi pääkirjanpidon tapahtumat kustannustapahtumiin, jotka perustuvat päivittäisiin tai kuukausittaisiin yhteenvetoihin.  

Kustannuspäiväkirjoissa voi kirjata kustannukset ja toiminnot, joita ei saada pääkirjanpidosta tai jotka eivät ole kohdistusten luomia. Voit esimerkiksi kirjata pelkkiä operatiivisia kustannuksia, sisäisiä kuluja, kohdistuksia ja korjaavia tapahtumia kustannustyyppien, kustannuspaikkojen ja kustannuskohteiden välille yksitellen tai toistuvasti.  

## Kustannusten kohdistukset

Kohdistukset siirtävät kustannukset ja tuotot eri kustannustyyppien, kustannuspaikkojen ja kustannuskohteiden välillä. Yleiskustannukset kirjataan ensin kustannuspaikkoihin ja myöhemmin kustannuskohteisiin. Tämä voidaan tehdä esimerkiksi myyntiosastossa, joka myy useita tuotteita samanaikaisesti. Osaston yleiskustannukset, kuten palkat, tarvikkeet ja matkakulut, määritellään aluksi myyntikustannuskeskukseen. Kustannukset kohdistetaan sitten myytyjen tuotteiden (kustannuskohteiden) ja ostettujen materiaalien (välittömien kustannusten) kesken.

Kohdistusperuste ja kohdistusmääritelmän paikkansapitävyyden kustannukset vaikuttavat kustannusten kohdistamisen tuloksiin. Kohdistusmääritelmällä voidaan kohdistaa kustannukset ensin pääkustannuspaikoille ja niin kutsutuille esikustannuskeskuksille, ja sitten kustannuspaikoilta kustannuskohteille.  

Jokainen kohdistus koostuu kohdistuslähteestä ja sekä vähintään yhdestä kohdistuskohteesta. Todellisia arvoja tai budjetoituja arvoja voi kohdistaa käyttämällä staattista kohdistusmenetelmää, joka perustuu määritettyihin arvoihin. Esimerkiksi pinta-ala tai vakiintunut kohdistussuhde 5:2:4. Voit myös kohdentaa todelliset arvot tai budjetoidut arvot käyttämällä dynaamista kohdistamismenetelmää yhdeksän ennalta määritetyn kohdistuksen perusteen ja 12 dynaamisen päivämääräalueen kanssa.  

## Kustannusbudjetit

Kirjanpidon budjetoinnin tavoin voit luoda budjetteja kustannusten suunnittelua varten tiettynä ajanjaksona (esimerkiksi tilikautena), joka voidaan kohdistaa kustannuskeskukseen (yrityksen osastoon) tai kustannusobjektiin (tuote tai palvelu). Kustannusbudjetteja voi määrittää niin monta kuin tarvitset. Voit sitten kopioida kustannusbudjetin pääkirjanpitoon ja päinvastoin. Ja voit siirtää budjetoidut kustannukset todellisina kustannuksina.

## Kustannusraportti

Useimmat raportit ja tilastot perustuvat kirjattuihin kustannustapahtumiin. Voit asettaa tulosten lajittelun ja suodattimien avulla määrittää, mitkä tiedot täytyy näyttää. Voit luoda raportteja kustannusanalyysin jakelua varten. Voit lisäksi käyttää vakiomuotoisia taloudellisia raportteja määrittääksesi miten raportit kustannustyyppikaaviossa näkyvät.  

## Katso myös

[Kustannuslaskenta](finance-manage-cost-accounting.md)  
[Taloushallinto](finance.md)  
[Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
