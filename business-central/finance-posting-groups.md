---
title: "Kirjausryhmän määrittäminen| Microsoft Docs"
description: "Yleiskatsaus kirjausryhmistä, joiden avulla voit säästää aikaa ja välttää virheitä tapahtumia kirjattaessa."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting setup, initialize
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4237bba8b7b3464242cacfcdbba954c321e5e04a
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-posting-groups"></a>Kirjausryhmien määrittäminen
Kirjausryhmät yhdistävät objektit, kuten asiakkaat, toimittajat, nimikkeet, resurssit sekä myynti- ja ostoasiakirjoja pääkirjanpidon tileille. Ne säästävät aikaa ja auttavat välttämään virheitä tapahtumia kirjattaessa. Tapahtuman arvot viedään kyseisen objektin kirjausryhmässä määritetylle tilille. Kirjausryhmiä varten tarvitaan vain tilikartta. Lisätietoja on kohdassa [Tilikartan määrittäminen](finance-setup-chart-accounts.md).  

Kirjausryhmiä on kolmenlaisia:  

* Yleiset – Määritä, kenelle myyt ja keneltä ostat sekä mitä myyt ja ostat. Voit myös yhdistää ryhmät määrittämään esimerkiksi tuloslaskelmatilit, joille kirjaukset tehdään, tai suodattaa raportteja ryhmien avulla.  
* Erityiset – Käytä esimerkiksi myyntiasiakirjoa sen sijaan, että kirjaisit suoraan pääkirjanpitoon. Kun luot asiakastapahtumia, vastaavat tapahtumat tulevat myös pääkirjanpitoon.  
* Vero – Määritä niitä henkilöitä koskevat veroprosentit ja laskentatyypit, joille myyt ja joilta ostat. Ne koskevat myös myymiäsi ja ostamiasi nimikkeitä.

Seuraavissa taulukoissa käsitellään kutakin kirjausryhmätyyppiä.  

| yleiset kirjausryhmät | Kuvaus |
| --- | --- |
| Yleiset liiketoiminnan kirjausryhmät |Liittämällä tämän ryhmän asiakkaisiin ja toimittajiin voi määrittää, kenelle myyt ja keneltä ostat. Määritä nämä asetukset **Yleiset liiketoim. kirj.ryhmät** -ikkunassa. Mieti määrityksiä tehdessäsi, kuinka monta ryhmää tarvitset myyntien ja ostojen erittelemiseen. Voit esimerkiksi ryhmitellä asiakkaat ja toimittajat maantieteellisen alueen tai liiketoiminnan tyypin mukaan. |
| Yleiset tuotteen kirjausryhmät |Liittämällä tämän ryhmän nimikkeisiin ja resursseihin voit määrittää, mitä myyt ja mitä ostat. Määritä nämä asetukset **Yleiset tuotteen kirjausryhmät** -ikkunassa. Mieti määrityksiä tehdessäsi, kuinka monta ryhmää tarvitse erittelemään tuotteiden (nimikkeiden ja resurssien) mukaisen myynnin ja nimikkeiden mukaiset ostot. Jaa nämä ryhmät esimerkiksi raaka-aineiden, resurssien ja kapasiteetin mukaan. |
| Yleiset kirjausasetukset |Yhdistä liiketoiminnan ja tuotteen kirjausryhmiä ja valitse tilit, joille kirjaukset tehdään. Kullekin liiketoiminnan ja tuotteen kirjausryhmien yhdistelmälle voi määrittää eri joukon pääkirjanpidon tilejä. Saman nimikkeen myynnin voi siis esimerkiksi kirjata eri myyntitileille pääkirjanpidossa, sillä asiakkaille on määritetty eri liiketoiminnan kirjausryhmät. Tee nämä määritykset **Yleiset kirjausasetukset** -ikkunassa. |

| erityiset kirjausryhmät | Kuvaus |
| --- | --- |
| Asiakkaan kirjausryhmät |Määritä tilit, joita käytetään, kun kirjaat myyntireskontran tapahtumia. Jos käytät varastoa, jossa on myyntisaatavia, asiakkaille määritetty yleinen liiketoiminnan kirjausryhmä ja varastonimikkeelle määritetty yleinen tuotteen kirjausryhmä määrittävät, mille tileille myyntitilausrivin tapahtumat kirjataan. Määritä nämä asetukset **Asiakkaan kirjausryhmät** -ikkunassa. |
| Toimittajan kirjausryhmät |Määritä, mihin ostovelkatilien, palveluveloitustilien ja maksualennustilien tapahtumat kirjataan. Tämä muistuttaa asiakkaan kirjausryhmiä. Määritä nämä asetukset **Toimittajan kirjausryhmät** -ikkunassa. |
| Varaston kirjausryhmät |Määrittää taseen varastotilit. Nämä tilit ovat kätevä tapa järjestää varasto, sillä voit erotella nimikkeet kirjausryhmien mukaan raportteja luotaessa. Määritä nämä asetukset **Varaston kirjausryhmät** -ikkunassa. |
| Pankkitilin kirjausryhmät |Määritä pankkitilien tilit. Tämä esimerkiksi yksinkertaistaa tapahtumien jäljittämistä ja pankkitilin täsmäyttämistä. Määritä nämä asetukset **Pankkitilin kirjausryhmät** -ikkunassa. |
| Käyttöomaisuuden kirjausryhmät |Määritä erilaisten kulujen ja kustannusten tilit. Näitä kuluja ja kustannuksia ovat esimerkiksi hankintamenot, kokonaispoistosummat, hankintamenot luovutettaessa, kokonaispoistot luovutettaessa, voitot luovutettaessa, tappiot luovutettaessa, ylläpitokulut ja poistokustannukset. Määritä nämä asetukset **KO:n kirjausryhmät** -ikkunassa. |

| Verokirjausryhmä | Kuvaus |
| --- | --- |
| Liiketoiminnan verokirjausryhmät |Määrittää, miten asiakkaiden ja toimittajien arvonlisävero lasketaan ja kirjataan. Määritä nämä asetukset **Liiketoiminnan verokirjausryhmät** -ikkunassa. Mieti määrityksiä tehdessäsi, kuinka monta ryhmää tarvitset. Siihen voi vaikuttaa esimerkiksi paikallinen lainsäädäntö ja se, käytkö sekä kotimaan- että ulkomaankauppaa. |
| Tuotteen verokirjausryhmät |Ilmoita, mitä verolaskelmia on tehtävä nimike- tai resurssityypeille, joita ostat tai myyt. |
| Verokirjausten asetukset |Yhdistä liiketoiminnan verokirjausryhmät ja tuotteen verokirjausryhmät. Kun täytät yleisen päiväkirjarivin, ostorivin tai myyntirivin, käytettävät tilit tunnistetaan yhdistelmän avulla. |

## <a name="example-of-linking-posting-groups"></a>Esimerkki kirjausryhmien linkittämisestä
Käytettävä skenaario.  

Asiakaskortista on valittu seuraavat kirjausryhmät:  

* Yleinen liiketoiminnan kirjausryhmä
* Asiakkaan kirjausryhmä  

Nimikekortista on valittu seuraavat kirjausryhmät:  

* Yleinen tuotteen kirjausryhmä  
* Varaston kirjausryhmä  

Kun luot myyntiasiakirjan, myyntiotsikko käyttää asiakaskortin tietoja ja myyntirivit käyttävät nimikekortin tietoja.  

* Tuottojen kirjaus (tuloslaskelma) määräytyy yleisen liiketoiminnan kirjausryhmän ja yleisen tuotteen kirjausryhmän yhdistelmän perusteella.  
* Myyntireskontran kirjaus (tase) määräytyy asiakkaan kirjausryhmän perusteella.  
* Varaston kirjaus (tase) määräytyy varaston kirjausryhmän perusteella.  
* Myytyjen tavaroiden kustannusten kirjaus (tuloslaskelma) määräytyy yleisen liiketoiminnan kirjausryhmän ja yleisen tuotteenkirjausryhmän yhdistelmän perusteella.  

Kirjausajankohta määräytyy asetusten mukaan. Esimerkiksi jaksoittaiset toiminnot, kuten varaston kustannusten kirjaus- tai kustannusnimikkeiden muutostapahtumat, vaikuttavat ajoitukseen.

## <a name="copying-posting-setup-lines"></a>Kirjausasetusrivien kopioiminen
Mitä enemmän tuotteen ja liiketoiminnan kirjausryhmiä on luotu, sitä enemmän rivejä näkyy Yleiset kirjausasetukset -ikkunassa. Yrityksen yleisten kirjausasetusten määrittäminen voi siis vaatia paljon tietojen syöttämistä. Vaikka liiketoiminnan ja tuotteen kirjausryhmiä saattaa olla useita, eri yhdistelmillä voi kuitenkin kirjata samoille pääkirjanpidon tileille. Manuaalisia vientejä voi rajoittaa kopioimalla pääkirjanpidon tilit aiemmin luodulta riviltä **Yleiset kirjausasetukset** -ikkunassa.

## <a name="see-also"></a>Katso myös .
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

