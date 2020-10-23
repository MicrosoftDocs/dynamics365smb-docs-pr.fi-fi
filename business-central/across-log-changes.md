---
title: Muutosten valvonta| Microsoft Docs
description: Voit aktivoida käyttäjälokin niin, että saat historiatiedot kaikista seurattujen taulukoiden tietoihin tehdyistä muutoksista. Voit seurata aktiviteetteja myös tietyn tyyppisillä toimintalokeilla.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1497051beebd01839dfc4b4fe2dce6b46977eef4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922665"
---
# <a name="auditing-changes-in-business-central"></a>Business Centralin tilintarkastuksen muutokset
Monien liikkeenjohtosovellusten yhteisenä haasteena on välttää ei-toivottuja muutoksia tiedoissa. Kyseessä voi olla mikä tahansa väärästä asiakkaan puhelinnumerosta väärään pääkirjanpitokirjaukseen. Tässä ohjeaiheessa kuvataan, miten voidaan selvittää, mitä muutoksia on tehty, kuka sen muutoksen teki ja milloin se tehtiin.

## <a name="about-the-change-log"></a>Muutoslokista 
Voit seurata muutoslokiin avulla kaikkia suoria muutoksia, joita käyttäjä tekee tietokannan tietoihin. Jokainen taulukko ja kenttä niissä pitää haluttaessa määrittää erikseen seurattavaksi, ja sitten loki tulee aktivoida.  

Muutosloki perustuu seuraamiesi taulukoiden tietoihin tehtyihin muutoksiin. **Muutoslokin tapahtumat** -sivulla tapahtumat järjestetään aikajärjestykseen. Sivulla näkyy kaikki muutokset, jotka tehdään määrittämiesi taulukoiden kenttien arvoihin.

> [!Important]
> Muutokset näkyvät **Muutoslokin tapahtumat** -kohdassa vasta, kun käyttäjän istunto on käynnistetty uudelleen, mikä tapahtuu seuraavasti:
<br />
> * Istunto vanhentui ja se päivitettiin.
> * Käyttäjä valitsi toisen yrityksen tai roolikeskuksen.
> * Käyttäjä kirjautui ensin ulos ja sitten takaisin sisään.

### <a name="working-with-the-change-log"></a>Muutoslokin käyttäminen
Voit aktivoida muutoslokin ja poistaa sen aktivoinnin **Muutoslokin asetukset** -sivulla. Kun käyttäjä aktivoi muutoslokin tai poistaa sen aktivoinnin, tämä aktiviteetti kirjataan, joten näet aina, kuka käyttäjistä poisti muutoslokin aktivoinnin tai aktivoi sen uudelleen.

Jos valitset **Muutoslokin asetukset** -sivulla **Taulukot**-toiminnon, voit määrittää sekä taulukot, joiden muutoksia seurataan, että seurattavat muutokset. [!INCLUDE[d365fin](includes/d365fin_md.md)] seuraa myös tiettyjä järjestelmätaulukoita.

> [!NOTE]
> Voit valvoa tiettyjä muutoksia koskevia kenttiä, kuten arkaluonteisia tietoja sisältäviä kenttiä, määrittämällä kenttien seurannan. Jos teet niin, redundanssin välttämiseksi kenttää sisältävä taulukko ei ole käytettävissä muutoslokin määrityksessä. Lisätietoja on kohdassa [Herkkien kenttien valvonta](across-log-changes.md#monitoring-sensitive-fields).

Kun olet määrittänyt muutoslokin, aktivoinut sen ja muuttanut tietoja, voit tarkastella ja suodattaa muutoksia **Muutoslokin tapahtumat** -sivulla. Jos haluat poistaa merkintöjä, voit tehdä sen **Poista muutoslokin tapahtumat** -sivulla, jossa voit määrittää päivämääriin ja kellonaikaan perustuvia suodattimia.  

## <a name="about-activity-logs"></a>Tietoja tapahtumalokeista
Joillakin [!INCLUDE [prodshort](includes/prodshort.md)]in sivuilla voi tarkastella toimintalokeja, joissa näkyy [!INCLUDE [prodshort](includes/prodshort.md)]ista vietävien ja sovellukseen tuotavien tiedostojen tila ja mahdolliset virheet.  

### <a name="working-with-activity-logs"></a>Toimintalokien käyttäminen
Tiedot näytetään **Toimintaloki**-sivulla sen kontekstin mukaan, josta ne avataan. Voit esimerkiksi avata sivun **Document Exchange -palvelun asetukset**-, **Saapuva asiakirja**-, **Kirjattu myyntilasku**- ja **Kirjattu myyntihyvityslasku** -sivuilta. Voit tyhjentää lokitapahtumaluettelon tai poistaa vain yli seitsemän päivää vanhemmat tapahtumat.  

## <a name="monitoring-sensitive-fields"></a>Arkaluonteisten kenttien valvonta
Luottamuksellisten tietojen suojaaminen ja yksityisyys ovat useimmille yrityksille keskeinen huolenaihe. Jos haluat lisätä suojauskerroksen, voit seurata tärkeitä kenttiä ja saada ilmoituksen sähköpostilla, kun joku muuttaa arvoa. Saatat esimerkiksi haluta saada ilmoituksen, jos joku muuttaa yrityksesi IBAN-numeroa.

> [!NOTE]
> Ilmoitusten lähettäminen sähköpostitse edellyttää, että määrität sähköpostiominaisuuden [!INCLUDE[prodshort](includes/prodshort.md)] -ohjelmaan. Lisätietoja on kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).

### <a name="setting-up-field-monitoring"></a>Kentän valvonnan asetusten määrittäminen
**Kentän valvonnan asetusten määrittäminen** -avustetun asennusoppaan avulla kentät, joita haluat seurata suodatusehtojen, kuten kenttien tietojen arkaluonteisuusluokituksen perusteella. Lisätietoja on kohdassa [Tietojen arkaluontoisuuden luokitteleminen](admin-classifying-data-sensitivity.md). Oppaassa voidaan myös määrittää henkilö, joka saa sähköposti-ilmoituksen muutoksen tapahtuessa, sekä sähköpostitili, jolla ilmoitus lähetetään. Sinun täytyy määrittää sekä käyttäjä, jolle ilmoitetaan että tili, josta ilmoitus lähetetään. Kun ohjelma on valmis, voit hallita kentän seurannan asetuksia **Kentän seuranta-asetukset** -sivulla. 

**Tarkkailtavien kenttien lokitapahtumat** -sivun tapahtumaluettelo kasvaa ajan mittaan. Voit vähentää merkintöjen määrää luomalla säilytyskäytännön, joka poistaa tapahtumat tietyn ajanjakson jälkeen. Lisätietoja on kohdassa [Säilytyskäytäntöjen määrittäminen](admin-data-retention-policies.md).

Kun määrität kentän seurannan tai muutat asetuksia, tapahtumat luodaan muutoksesi. Voit määrittää, näytetäänkö seurannan asetuksiin liittyvät tapahtumat näyttämällä vai piilottamalla ne. 

Voit hallita kentän seurannan asetuksia, kuten sen, lähetetäänkö sähköposti-ilmoitus vai merkitäänkö vain lokiin muutos, kunkin **Tarkkailtavat kentät -työkirja** -sivun kentän osalta. Sivulla voit myös lisätä tai poistaa valvottuja kenttiä.

> [!NOTE]
> Kun olet lisännyt yhden tai useamman kentän ja käynnistät seurannan, sinun on kirjauduttava ulos [!INCLUDE[prodshort](includes/prodshort.md)] -ohjelmasta ja kirjautua uudelleen sisään, jotta voit ottaa asetukset käyttöön.

### <a name="working-with-field-monitoring"></a>Kentän seurannan käsitteleminen
Tarkkailtujen kenttien kaikkien muutettujen arvojen tapahtumat ovat käytettävissä **Tarkkailtavat kentät-lokin tapahtumat** -sivulla. Esimerkiksi tapahtumat sisältävät tietoja, kuten kentän, jonka arvoa on muutettu, alkuperäiset ja uudet arvot sekä kuka teki muutoksen ja milloin he tekivät sen. Jos haluat tutkia muutosta edelleen, valitse arvo, joka avaa sivun, jossa se on tehty. Voit tarkastella kaikkien tapahtumien luetteloa valitsemalla **Kentän muutostapahtumat**.

## <a name="defining-retention-policies"></a>Säilytyskäytäntöjen määrittäminen
Voit luoda säilytyskäytäntöjä, jotka poistavat tarpeettomia tietoja lokeista määrittämäsi ajanjakson jälkeen. Esimerkiksi ajan mittaan lokimerkintöjen määrä voi kasvaa. Puhdistamalla vanhoja tapahtumia voit helpottaa keskittymistä viimeaikaisiin ja todennäköisesti osuvimpiin tapahtumiin. Lisätietoja on kohdassa [Säilytyskäytäntöjen määrittäminen](admin-data-retention-policies.md).

## <a name="see-also"></a>Katso myös
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Lajitteleminen, hakeminen ja suodattaminen](ui-enter-criteria-filters.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Määritä säilytyskäytännöt](admin-data-retention-policies.md)  