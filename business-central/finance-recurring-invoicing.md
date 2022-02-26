---
title: Toistuvan tuoton käsitteleminen
description: Tietoja käytettävissä olevista vaihtoehdoista, jotka automatisoivat tilauslaskujen lähettämisen asiakkaille ja rekisteröivät toistuvan tuoton.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: recurring, invoicing, subscription, billing
ms.search.form: 283
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: andreipa
ms.openlocfilehash: 696ab59530c81cd19709f4e1bde3324bcaebbf5a
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2022
ms.locfileid: "7970987"
---
# <a name="work-with-recurring-revenue-in-prod_short"></a>Toistuvan tuoton käsitteleminen kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]

Monet yritykset ovat siirtymässä liiketoiminnan tuottomallista, jossa tuotto on tehty asiakkaan yhdestä ostosta tilausmalliin, jossa tuotto tehdään toistuvin perustein, kun halutaan saada yhdenmukainen käyttöoikeus tavaran tai palvelun toimittamiseen.
[!INCLUDE[prod_short](includes/prod_short.md)] on seuraavat vaihtoehdot sille, miten automatisoit tilauslaskujen lähettämisen asiakkaille ja rekisteröit toistuvan tuoton. 

## <a name="register-revenue-with-a-recurring-general-journal"></a>Rekisteröi tuotot toistuvassa yleisessä päiväkirjassa

Toistuvien tapahtumien päiväkirja on yleinen päiväkirja, jossa on erityiskenttiä sellaisten tapahtumien hallintaa varten, jotka kirjataan usein vähäisin muutoksin tai ilman muutoksia. Näitä ovat esimerkiksi vuokra, lehtitilaukset, sähkö tai lämmitys. Käyttämällä näitä kenttiä toistuviin tapahtumiin, voit kirjata sekä vakiosummia että muuttuvia summia. Toistuvassa päiväkirjassa säännöllisesti kirjattavat tapahtumat tarvitsee syöttää vain kerran. Siten tilit, dimensiot , dimension arvot ym. tiedot jotka syötät, säilyvät päiväkirjassa kirjauksen jälkeen. Jos sinun tarvitsee tehdä muutoksia, voit tehdä niitä jokaisen kirjauksen yhteydessä.

### <a name="why-use-this-option"></a>Miksi käyttää tätä asetusta

Tämän asetuksen avulla määritetään joustavat laskutusjaksot [päivämääräkaavojen](ui-enter-date-ranges.md#using-date-formulas) avulla.

Tämän asetuksen avulla et kuitenkaan voi tulostaa ja lähettää laskuja [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman oletusversiossa.  

Lisätietoja on kohdassa [Toistuvien päiväkirjojen käyttäminen](ui-work-general-journals.md#working-with-recurring-journals).  

## <a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a>Luo useita laskuja toistuvan projektipäiväkirjan perusteella

Toistuva projektipäiväkirja on kehittyneempi vaihtoehto yleiselle päiväkirjalle. Voit määrittää nimikkeet, resurssit ja KP-tilit, jotka täytyy toistaa jokaisen projektin osalta, ja määrittää toistumisen tiheyden.  

Kun olet kirjaamassa toistuvaa projektipäiväkirjaa, voit luoda useita laskuja **luomalla projektin myyntilasku** -tehtävän. Voit tarkastella ja kirjata luotuja laskuja **Myyntilaskut**-sivulla.

### <a name="why-use-this-option"></a>Miksi käyttää tätä asetusta

Tämän vaihtoehdon avulla voit noudattaa vakiolaskutusmenettelyä ja kaikkia sen etuja, kuten viestintäasetusten vakio- ja asiakasasettelua. Voit myös määrittää kunkin projektin hinnat yksittäin.

Sinun täytyy kuitenkin luoda uusi projekti jokaiselle uudelle asiakkaalle ja lisätä rivejä toistuvaan päiväkirjaan. 

Lisätietoja on kohdissa [Projektipäiväkirjarivien luominen](projects-how-record-job-usage.md#to-create-job-journal-lines-manually) ja [Useiden projektin myyntilaskujen luominen](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices).

## <a name="create-multiple-invoices-based-on-recurring-sales-lines"></a>Luo useita laskuja toistuvien myyntirivien perusteella

Jos sinun on usein luotava samankaltaisia tietoja sisältäviä myynti- ja ostorivejä, voit määrittää toistuvia myyntirivejä ja lisätä ne sitten toistuviin myynti- ja ostoasiakirjoihin, kuten toistuviin täydennystilauksiin. Luo **Luo toistuvia myyntilaskuja** -eräajolla myyntilaskuja asiakkaille määritettyjen toistuvien myyntirivien mukaan siten, että niiden kirjauspäivämäärät ovat toistuville myyntiriveille määritetyllä voimassaolon päivämäärävälillä.  

### <a name="why-use-this-option"></a>Miksi käyttää tätä asetusta

Tämän asetuksen avulla voit liittää samat toistuvat rivit usealle asiakkaalle. Voit määrittää tietyn asiakkaan toistuvien myyntirivien voimassaoloajan. Samalle asiakkaalle voi liittää useampia toistuvia rivejä, ja kaikki ne sisällytetään laskuun.

Nimikkeille ei kuitenkaan ole mahdollista määrittää kiinteitä hintoja, koska [!INCLUDE[prod_short](includes/prod_short.md)] käyttää todellisia hintoja ja alennuksia, jotka ovat voimassa asiakirjan päivämääränä ja jotka yrittävät löytää parhaan yhdistelmän, joka antaa alimman hinnan.  

Lisätietoja on kohdassa [Toistuvien myynti- ja ostorivien luominen](sales-how-work-standard-lines.md).

## <a name="recurring-invoices-with-service-contract"></a>Toistuvat laskut ja huoltosopimus

Huoltosopimus sisältää asiakkaiden ja oman yrityksen väliset huoltosopimukset. Huoltosopimukseen sisältyvät huoltotasosopimukset ja huoltosopimukset, jotka huolletaan osana sopimusta.  

Voit määrittää sopimuksen aloituspäivämäärän, laskutusjakson, sen, onko sopimus ennakkoon maksettu, hinnan päivityksen määritykset, jos aiot muuttaa hintoja, kun sopimus on aktiivinen. Huoltosopimusriveillä voi käyttää sekä huoltonimikkeitä että huoltosopimusnimikkeitä.
Sopimusmalleja voidaan luoda määrittämään sitä, miten tietyn tyyppisiä sopimuksia luodaan.  

### <a name="why-use-this-option"></a>Miksi käyttää tätä asetusta

Tämän asetuksen avulla voit käyttää kehittynyttä huollon hallintatoimintoa, joka ei rajoitu toistuvien laskujen myöntämiseen, vaan tukee korjaamo- ja field service -toimintoja.

Tämä toiminto vaatii kuitenkin Premium-lisenssin. Huoltohallinnon määrittäminen ja ylläpito ei välttämättä anna valtavia etuja yksinkertaisemmissa tilausskenaarioissa.  

Lisätietoja on kohdissa [Huoltosopimusten ja huoltosopimustarjousten käsitteleminen](service-how-to-create-service-contracts-and-service-contract-quotes.md) ja [Useiden huoltosopimusten laskuttaminen](service-how-create-invoices.md#to-invoice-several-service-contracts).

## <a name="related-features"></a>Aiheeseen liittyvät ominaisuudet
[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa on useita toisiinsa liittyviä toimintoja.

### <a name="blanket-sales-orders"></a>Puitemyyntitilaukset

Puitemyyntitilaus kuvastaa yrityksesi ja asiakkaan välisen pitkäaikaisen sopimuksen runkoa.
Puitetilaus tehdään yleensä silloin, kun asiakas on päättänyt ostaa suuria määriä, jotka toimitetaan useissa pienissä toimituserissä määritetyn aikajakson sisällä. Puitetilaukset kattavat usein vain yhden nimikkeen ja ennalta määritetyt toimituspäivämäärät. Pääsyy puitetilauksen käytölle myyntitilauksen käytön sijaan on se, että puitetilaukseen syötetyt määrät eivät vaikuta nimikkeen saatavuuteen, mutta sitä voidaan kuitenkin käyttää suunnittelutarkoituksiin.

#### <a name="why-use-this-option"></a>Miksi käyttää tätä asetusta

Tällä vaihtoehdolla käytät odotettua kysyntää, joten tiedot otetaan huomioon tavanomaisten kaavoitusrutiinien yhteydessä. Lisätietoja on kohdassa [Kysyntäennusteet ja puitetilaukset](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders).  

Oletusversio ei kuitenkaan tarjoa valmista mahdollisuutta käsitellä useaa puitetilausta joukkona.

Lisätietoja on kohdassa [Puitemyyntitilausten käyttäminen](sales-how-to-create-blanket-sales-orders.md).

### <a name="recurring-orders-norway"></a>Toistuvat tilaukset (Norja)

Toistuvien tilausten avulla voit luoda puitetilausmalleja, jotta myyntitilaukset voidaan luoda määrittämiesi päivämäärävälien perusteella. Jos esimerkiksi toimitat saman myyntitilauksen kahden viikon välein, voit käyttää puitemyyntitilausta ja luoda toistuvia tilauksia.
Toistuvien ryhmien avulla voit määrittää joukon parametreja, jotka ilmaisevat, miten tilaukset tehdään. Nämä ryhmät määritellään puitetilauksille, jotka täytyy luoda säännöllisesti. Toistuvien tilausten luomiseksi on suoritettava luo toistuvat tilaukset -prosessi säännöllisesti. 

#### <a name="why-use-this-option"></a>Miksi käyttää tätä asetusta

Tämän asetuksen avulla voit valita kiinteiden ja "parhaiden" hintojen väliltä.

Tämä asetus on kuitenkin käytettävissä vain Norjassa. Voimassaoloaika voidaan määrittää toistuvassa ryhmittelytasossa.

Lisätietoja on kohdassa [Toistuvat tilaukset](LocalFunctionality/Norway/recurring-orders.md).

### <a name="recurring-revenue-and-subscription-billing-by-other-providers"></a>Muiden palveluntarjoajien toistuva tuotto- ja tilauslaskutus

Osoitteessa [AppSource.microsoft.com](https://appsource.microsoft.com/) on laajennuksia Business Centralille. Jotkin ovat Microsoftin laajennuksia, jotkin muiden yritysten. Luettelo muiden yritysten laajennuksista kasvaa joka kuukausi. Sivustoa[AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) kannattaakin tarkkailla ja sieltä voi ladata Business Centralin käyttöä helpottavia sovelluksia.  

## <a name="see-also"></a>Katso myös

[Pvm-kaavat](ui-enter-date-ranges.md#using-date-formulas)  
[Toistuvien tapahtumien päiväkirjojen käyttäminen](ui-work-general-journals.md#working-with-recurring-journals)  
[Luo projektipäiväkirjan rivit](projects-how-record-job-usage.md#to-create-job-journal-lines-manually)  
[Luo monta projektin myyntilaskua](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices)  
[Toistuvien myynti- ja ostorivien luominen](sales-how-work-standard-lines.md)  
[Huoltosopimusten ja huoltosopimustarjousten käyttäminen](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Laskuta useita huoltosopimuksia](service-how-create-invoices.md#to-invoice-several-service-contracts)  
[Kysyntäennusteet ja puitetilaukset](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders)  
[Puitemyyntitilausten käyttäminen](sales-how-to-create-blanket-sales-orders.md)  
[Toistuvat tilaukset (Norja)](LocalFunctionality/Norway/recurring-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]