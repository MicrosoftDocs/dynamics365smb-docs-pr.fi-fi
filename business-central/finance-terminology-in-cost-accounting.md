---
title: Kustannuslaskennan termejä | Microsoft Docs
description: Tässä aiheessa määritellään keskeiset ehdot, joita käytetään kustannuslaskennassa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ad6c208383aa5a92b3d4abf9132b4f2eb4654195
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746497"
---
# <a name="terminology-in-cost-accounting"></a>Termit kustannuslaskennassa
Tässä aiheessa määritellään kustannuslaskennan keskeiset termit.  

## <a name="key-terms"></a>Keskeiset termit  
 Seuraavassa taulukossa on esitetty keskeiset määritelmät kustannuslaskennassa.  

|**Kausi**|**Määritys**|  
|--------------|--------------------|  
|Kohdistustunnus|Kohdistustunnus on perusta, jonka avulla voit kohdistaa kustannukset. Se on yleensä määrä, kuten varattu neliömetrien määrä, työntekijöiden määrä tai käytettyjen työtuntien määrä. Esimerkiksi kaksi osastoa, joilla on 20 ja 10 työntekijää, jakavat kanttiiniin kustannukset. Kustannukset jaetaan osastojen välillä käyttämällä kohdistusavainta, joka vastaa työntekijöiden määrää. Kaksi kolmasosaa kustannuksista kohdistetaan ensimmäiselle osastolle ja yksi kolmasosa kustannuksista kohdistetaan toiselle osastolle.|  
|Kohdistamisen lähde|Kohdistuksen lähde määrittää, mitkä kustannukset kohdistetaan. Kohdistukset on määritetty kohdistuksen lähteen ja kohteen taulukoissa. Jokainen kohdistus koostuu kohdistuslähteestä ja yhdestä tai useammasta kohdistustavoitteesta. Esimerkiksi Lämmitys-kustannuslajin, joka on kohdistuksen lähde, kaikki kustannukset voidaan kohdistaa korjaamon, tuotannon ja myynnin kustannuspaikkoihin, jotka ovat kolme kohdistuksen kohdetta.|  
|Kohdistuskohde|Kohdistustavoitteet määrittävät, mihin kustannukset kohdistetaan. Kohdistukset on määritetty kohdistuksen lähteen ja kohteen taulukoissa. Jokainen kohdistus koostuu kohdistuslähteestä ja yhdestä tai useammasta kohdistustavoitteesta. Esimerkiksi Lämmitys-kustannuslajin, joka on kohdistuksen lähde, kaikki kustannukset voidaan kohdistaa korjaamon, tuotannon ja myynnin kustannuspaikkoihin, jotka ovat kolme kohdistuksen kohdetta.|  
|Kustannuslaskenta|Kustannuslaskennassa tallennetaan toimintojen, prosessien, osastojen tai tuotteiden toteutuneet kustannukset. Nämä kustannukset kohdistetaan kustannuspaikkoihin ja kustannuskohteisiin käyttämällä erilaisia kustannusten kohdistamistapoja. Päälliköt Esimiehet käyttävät tilastoja ja raportteja, kuten kustannusten jakolomaketta ja voitto- ja tappioanalyyseja, päätöksenteossa ja kustannusten vähentämisessä. Kustannuslaskenta hakee tiedot pääkirjanpidosta, mutta toimii itsenäisesti. Tämän vuoksi kustannuslaskentaan kirjatut tapahtumat eivät vaikuta pääkirjanpidon tietoihin.|  
|Kustannuslaji|Kustannustyyppikaaviolla on sama toiminnallisuus kuin pääkirjanpidon tilikartalla. Ne on usein järjestetty samalla tavalla. Tämän vuoksi on mahdollista siirtää pääkirjanpidon tilikartta kustannustyyppikaavioon ja sitten muokata sitä. Kustannustyyppikaavio voidaan myös luoda tyhjästä.|  
|Kustannuspaikka|Kustannuspaikat ovat useimmiten osastoja ja tulosyksiköitä, jotka ovat suurilta osin vastuussa yrityksen kustannuksista ja tuloista. Kustannuspaikat voidaan synkronoida pääkirjanpidon dimensioiden kanssa. On myös mahdollista lisätä uusia kustannuspaikkoja ja määrittää niiden lajittelu välisummien avulla.|  
|Kustannuskohde|Kustannuskohteet ovat yrityksen tuotteita, tuoteryhmiä tai palveluja; yrityksen valmiita tuotteita, jotka lopulta kattavat kustannukset. Kustannuskohteet voidaan synkronoida pääkirjanpidon dimensioiden kanssa. On myös mahdollista lisätä uusia kustannuskohteita ja määrittää niiden lajittelu välisummien avulla.|  
|Kustannusten kohdistus|Kustannusten kohdistus on prosessi, jossa kustannuspaikkoihin tai kustannusobjekteihin kohdistetaan kustannuksia. Esimerkiksi myyntiosaston kuorma-auton kuljettajan palkka on kohdistettu myyntiosaston kustannuspaikkaan. Ei ole tarpeen kohdistaa palkan kustannushintaa muihin kustannuspaikkoihin. Toinen esimerkki on kalliin tietokonejärjestelmän kustannusten kohdistaminen järjestelmää käyttävän yrityksen tuotteisiin.|  
|Dynaaminen kohdistaminen|Dynaamiset kohdistukset ovat riippuvaisia muuttuvista kohdistuskannoista, esimerkiksi osaston työntekijöuden määrästä tai projektin myyntituotosta tiettynä aikajaksona. Ohjelmassa on yhdeksän ennalta määritettyä dynaamista kohdistamisen perustetta, jotka käyttäjä voi määrittää viiden suodattimen avulla.|  
|Välitön kustannus|Välittömät kustannukset ovat kustannuksia, jotka voidaan suoraan kohdistaa kustannuskohteeseen, esimerkiksi tietyn tuotteen materiaaliostoksiin.|  
|Kiinteä kustannus|Kiinteät kustannukset ovat kustannuksia, jotka eivät riipu yrityksen tuottamien tavaroiden tai palveluiden tasosta. Ne ovat usein aikaan liittyviä, kuten palkat tai vuokra, jotka maksetaan kuukausittain. Ne ovat vastakohtana muuttuville kustannuksille, jotka perustuvat volyymiin ja joista maksetaan tuotetun määrän mukaan. |  
|Epäsuora kustannus|Välilliset kustannukset eivät ole suora suhteessa kustannuskohteeseen, kuten tiettyyn toimintoon tai tuotteeseen. Välilliset kustannukset voivat olla joko kiinteitä tai muuttuvia. Välilliset kustannukset voi olla vero-, hallinto-, henkilöstö- ja suojauskustannuksia, ja niitä kutsutaan myös yleiskustannuksiksi.|  
|Taso|Tasoa käytetään kohdistusjärjestyksen muuttamiseen. Taso määritetään numerona välillä 1-99. Kohdistuksen kirjaus noudattaa tasojen järjestystä. Esimerkiksi taso varmistaa, että ensimmäinen hallinto kohdistetaan korjaamoon, ennen kuin korjaamo kohdistetaan ajoneuvoon ja tuotantoon.|  
|Staattinen kohdistaminen|Staattinen kohdistaminen perustuu määriteltyihin arvoihin, kuten pinta-alaan tai vahvistettu-varaus -suhteeseen, esimerkiksi 5:2:4.|  
|Operatiivinen kustannus|Operatiiviset kustannukset ovat toistuvia kuluja, jotka liittyvät liiketoiminnan, laitteen ja komponentin toimintaan.|  
|Yleiskustannus|Yleiskustannuksilla tarkoitetaan yrityksen liiketoiminnan jatkuvia kuluja. Ne kaikki ovat tuloslaskelman kustannuksia, paitsi suora työ, suorat materiaalit ja suorat kulut. Yleiskustannuksia ovat kirjanpidon palkkiot, mainonnan, poistojen, vakuutusten ja korkojen kustannukset, oikeudelliset kustannukset, vuokra-, korjaus- ja tarvikekustannukset, verot, puhelinlaskut, matkakustannukset sekä sähkö- ja vesikustannukset.|  
|Portaittainen muuttuva kustannus|Portaittain muuttuvat kustannukset ovat kustannuksia, jotka muuttuvat huomattavasti tietyissä pisteissä, koska niihin sisältyy suuria ostoja, joita ei voi jakaa useammalle aikajaksolle. Esimerkiksi yksi työntekijä voi luoda 100 taulukkoa kuukauden aikana. Työntekijän palkka on vakio 1-100 taulukon tuotantoalueella. Jos yritys haluaa valmistaa 110 pöytää, yrityksellä on oltava kaksi työntekijää. Kustannukset ovat siis kaksinkertaiset.|  
|Osuus|Osa tai osio, joka on kohdistettu kustannuskeskusten tai kustannuskohteiden välille.|  
|Staattinen painotus|Kustannukset kohdistetaan kohdistustunnuksilla, joita voidaan muokata käyttämällä kertoimia. <br />Esimerkiksi kaksi osastoa, joilla on 20 ja 10 työntekijää, jakavat kanttiiniin kustannukset. Kustannukset jaetaan osastojen välillä käyttämällä kohdistusavainta, joka vastaa työpaikkaruokalassa lounastavien työntekijöiden määrää. Ensimmäisen osaston työntekijöistä vain viisi syö kanttiinissa, joten tämän osaston kerroin on 0,25. Kohdistusperuste on 20 x 0,25 = 5. Henkilöstöruokalassa ruokailevien työntekijöiden määrä on 15. Kolmasosa kustannuksista kohdistetaan ensimmäiselle osastolle ja kaksi kolmasosaa kustannuksista kohdistetaan toiselle osastolle.|  
|Muuttuva kustannus|Muuttuvat kustannukset ovat kuluja, jotka muuttuvat suhteessa yrityksen toimintaan. Muuttuvat kustannukset ovat kaikkien tuotettujen yksiköiden marginaalikustannusten summa. Kokonaiskustannusten kaksi osaa muodostuvat kiinteistä kustannuksista ja muuttuvista kustannuksista.|  
|Variantti|Varianttia käytetään valinnaisena käyttäjän määrittämänä nimenä määrityksille. Etiketin tarkoitus on suodattaa jakoryhmiä.|  

## <a name="see-also"></a>Katso myös  
 [Tietoja kustannuslaskennasta](finance-about-cost-accounting.md)   
 [Kustannuslaskenta](finance-manage-cost-accounting.md)  
 [[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]