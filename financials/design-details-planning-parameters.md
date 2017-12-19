---
title: "Rakennetiedot – Suunnitteluparametrit | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, mitä suunnitteluparametreja voi käyttää Dynamics 365:ssä."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, design
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 5ab63063b5ad2ae453ecb9953ba4547f31536ee8
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-planning-parameters"></a>Rakennetiedot: suunnittelun parametrit
Tässä ohjeaiheessa kerrotaan, mitä suunnitteluparametreja [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa voi käyttää.  

Tapa, jolla suunnittelujärjestelmä ohjaa nimikkeen tarjontaa, määritetään nimikekortin tai varastointiyksikön kortin asetuksissa ja tuotannon asetusten asetuksissa. Seuraavassa taulukossa esitetään, kuinka näitä parametreja käytetään suunnittelussa.  

|Tarkoitus|Parametri|  
|-------------|---------------|  
|Määritä suunnitellaanko nimike|Uusintatilauskäytäntö = tyhjä|  
|Määritä uudelleentilauksen ajankohta|Aikaväli<br /><br /> Uusintatilauspiste<br /><br /> Toimitusajan varmistus|  
|Määritä uusintatilauksen määrä|Varmuusvaraston määrä<br /><br /> Uusintatilauskäytäntö:<br /><br /> -   Kiinteä uusintatil. määrä lisättynä uusintatilausmäärällä<br />-   Enimmäismäärä lisättynä enimmäisvarastolla<br />-   Järjestys<br />-   Erä-erästä|  
|Optimoi milloin ja kuinka paljon järjestetään uudelleen|Uudelleenajoitusjakso<br /><br /> Erän koontijakso<br /><br /> Puskuriaika|  
|Toimitustilausten muuttaminen|Vähimmäistilausmäärä<br /><br /> Enimmäistilausmäärä<br /><br /> Tilauskerrannainen|  
|Rajaa suunniteltu nimike|Tuotantotapa:<br /><br /> -   Varasto-ohjautuva<br />-   Tilausohjattu|  

## <a name="define-if-the-item-will-be-planned"></a>Määritä suunnitellaanko nimike  
Voit sisällyttää nimikkeen/varastointiyksikön suunnitteluprosessiin, kun sillä on uusintatilaustapa. Muussa tapauksessa se on suunniteltava manuaalisesti esimerkiksi tilaustensuunnittelutoiminnon avulla.  

## <a name="define-when-to-reorder"></a>Määritä uudelleentilauksen ajankohta  
Jälkitilausehdotukset julkaistaan yleensä vain, kun arvioitu käytettävissä oleva määrä on tippunut alle annetun määrän. Uusintatilauspiste määrittää tämän määrän. Muussa tapauksessa se on nolla. Voit muuttaa nollan syöttämällä varmuusvaraston määrän. Jos käyttäjä on määrittänyt toimitusajan varmistuksen, se aiheuttaa ehdotuksen toimittamisen jaksolla ennen vaadittavaa eräpäivää.  

Uusintatilauspistekäytännöt (**Kiinteä uusintatil. määrä** ja **Maksimimäärä**) käyttävät **Aikaväli**-kenttää, jossa varastomäärä tarkistetaan kunkin aikavälin jälkeen. Ensimmäinen ajanjakso alkaa suunnittelun alkamispäivämääränä.  

> [!NOTE]  
>  Suunnittelujärjestelmä ei ota huomioon aikavälien laskennassa työkalentereita, jotka on määritetty **Yritystiedot**- tai **Sijaintikortti**-ikkunan **Peruskalenterin koodi** -kentässä.  

Oletusarvoinen varmuusläpimenoaika **Tuotannon asetukset** -ikkunassa, tulee olla asetettuna vähintään yhteen päivään. Kysynnän eräpäivä voi olla tiedossa, mutta ei kellonaika. Suunnitteluaikataulut vastaavat nettokysyntää taantuvasti ja jos varmuusläpimenoaikaa ei ole määritetty, tavarat voivat saapua liian myöhään vastatakseen kysyntää.  

Kolme uudelleentilausjakson kenttää, **Uudelleenajoitusjakso**, **Erän koontijakso** ja **Puskuriaika**, ottavat myös osaa uudelleentilauksen ajankohdan määrittämiseen. Lisätietoja on kohdassa Uusintatilauksen ajankohdan ja määrän optimointi.  

## <a name="define-how-much-to-reorder"></a>Määritä uusintatilauksen määrä  
Jos suunnittelujärjestelmä havaitsee uusintatilauksen tarpeen, uusintatilaustapaa käytetään määrittämään, milloin ja kuinka paljon tilataan.  

Suunnittelujärjestelmä noudattaa tavallisesti tätä logiikka uusintatilaustavasta riippumatta:  

1. Tilausehdotuksen määrä lasketaan vastaamaan nimikkeen määritettyä minimivarastotasoa, yleensä varmuusvaraston määrää. Jos mitään ei määritetä, varaston vähimmäistaso on nolla.  
2. Jos oletettu saatavilla oleva varasto alittaa varmuusvaraston määrän, järjestelmä ehdottaa taaksepäin aikataulutettua toimitustilausta. Tilausmäärä täyttää vähintään varmuusvarastomäärän, ja sitä voidaan lisätä bruttokysynnällä ajanjakson sisällä jälkitilaustavan ja tilauksen muokkaajien avulla.  
3. Jos ennustettu varastosaldo on lisätilauspisteessä tai sen alla (lasketaan kootuista muutoksista aikajaksolla) ja yli varaston turvamäärän, järjestelmä ehdottaa poikkeustilausta tulevalle päivämäärälle. Sekä täytettävä bruttokysyntä että uusintatilaustapa määrittävät tilauksen määrän. Tilauksen määrä vastaa vähintään uusintatilauspistettä.  
4. Jos bruttokysyntää on jäljellä enemmän ennen tulevaisuuteen aikataulutetun ehdotuksen päättymispäivämäärää ja tämä kysyntä tuo tällä hetkellä lasketun oletetun saatavilla olevan varaston varmuusvaraston määrän alapuolelle, tilauksen määrää kasvatetaan alijäämän hyvittämiseksi. Ehdotettu tarjontatilaus aikataulutetaan sitten taaksepäin nettokysynnän eräpäivästä, joka on saattanut vahingoittaa varmuusvaraston määrää.  
5. Jos **Aikaväli**-kenttää ei ole täytetty, vain saman eräpäivän bruttokysyntä lisätään.  

     Kolme uudelleentilausjakson kenttää, **Uudelleenajoitusjakso**, **Erän koontijakso** ja **Puskuriaika**, ottavat myös osaa uudelleentilausmäärien määrittämiseen. Lisätietoja on kohdassa Uusintatilauksen ajankohdan ja määrän optimointi.  

### <a name="reordering-policies"></a>Uusintatilauskäytännöt  
Seuraavat uudelleenjärjestysohjeet vaikuttavat jälkitilattavaan määrään.  

|Uusintatilaustapa|Kuvaus|  
|-----------------------|---------------------------------------|  
|**Kiinteä uusintatil. määrä**|Tilausmäärä vastaa vähimmillään uusintatilausmäärää. Sitä voidaan kasvattaa vastaamaan kysyntää tai haluttua varastotasoa. Tätä uusintatilaustapaa käytetään yleensä uusintatilauspisteen kanssa.|  
|**Enimmäismäärä**|Tilausmäärä lasketaan vastaamaan maksimivarastoa. Jos määrän muuttujia käytetään, enimmäisvarasto-käytäntö on rikottavissa. Aikavälin ja enimmäismäärän käyttämistä samanaikaisesti ei suositella. Aikaväli korvataan tavallisesti. Tätä uusintatilaustapaa käytetään yleensä uusintatilauspisteen kanssa.|  
|**Tilaus**|Tilausmäärä lasketaan vastaamaan jokaista yksittäistä kysyntätapahtumaa ja kysyntä-tarjonta-sarja pysyy liitettynä täytäntöönpanoon saakka. Suunnitteluparametreja ei harkita.|  
|**Erä-erästä**|Määrä lasketaan vastaamaan kysynnän summaa, joka on seurausta ajanjaksosta.|  

##  <a name="optimize-when-and-how-much-to-reorder"></a>Optimoi milloin ja kuinka paljon järjestetään uudelleen  
Rationaalinen toimitussuunnitelma saadaan, kun suunnittelija hienosäätää suunnitteluparametreja ja näin rajoittaa uudelleenajoituksen ehdotuksia, kokoaa kysynnän (dynaaminen uudelleentilausmäärä) ja välttää merkityksettömät suunnittelutoimenpiteet. Seuraavat jälkitilausjakson kentät auttavat optimoimaan milloin ja kuinka paljon jälkitilataan.  

|Kenttä|Kuvaus|  
|---------------------------------|---------------------------------------|  
|**Uudelleenajoitusjakso**|Tämän kentän avulla määritetään, tuleeko toimenpideviestin ajoittaa olemassa oleva tilaus uudelleen vai peruuttaa se ja luoda uusi tilaus. Olemassa oleva tilaus aikataulutetaan uudelleen yhden uudelleenaikataulutuskauden sisällä ennen tämänhetkistä tarjontaa ja yhteen tämänhetkisen tarjonnan ylittämään uudelleenaikataulutuskauteen.|  
|**Erän koontijakso**|Kun on uusintatilausmenetelmä on erä-erästä, tätä kenttää käytetään useiden tarjontatarpeiden keräämisessä yhteen toimitustilaukseen. Järjestelmä kokoaa ensimmäisestä suunnitellusta tarjonnasta alkaen kaikki tarjonnan tarpeet seuraavalla erän koontijaksolla yhdeksi tarjonnaksi, joka asetetaan ensimmäisen tarjonnan päivämääränä. Tämä toimitus ei kata kysyntää, joka on erän koontijakson ulkopuolella.|  
|**Puskuriaika**|Tätä kenttää käytetään olemassa olevan tarjonnan vähäisten uudelleenajoitusten välttämisessä. Muutokset toimituspäivämäärästä siihen hetkeen, kun yksi toimituspäivämäärän puskuriaika ei luo mitään toimenpideviestejä.<br /><br /> Seurauksena uuden tarjonnan päivämäärän ja alkuperäisen tarjonnan päivämäärän välisen positiivisen deltan muutos on aina suurempi kuin puskuriaika.|  

Uudelleenajoitusjakson, puskuriajan ja erän koontijakson ajoitus perustuu tarjonnan päivämäärään. Aikaväli perustuu suunnittelun alkupäivämäärään seuraavassa kuvassa esitetyllä tavalla.  

![Aikavälin elementit](media/supply_planning_5_time_bucket_elements.png "supply_planning_5_time_bucket_elements")  

Seuraavassa esimerkissä mustat nuolet kuvaavat olemassa olevaa tarjontaa (ylöspäin) ja kysyntää (alaspäin). Punaiset, vihreät ja oranssit nuolet ovat suunnitteluehdotuksia.  

**Esimerkki 1**: muutettu päivämäärä on uudelleenajoitusjakson ulkopuolella, joka aiheuttaa olemassa olevan tarjonnan peruutuksen. Uutta tarjontaa on ehdotettu kattamaan kysyntää erän koontijaksossa.  

![Uudelleenajoitusjakso, Erän koontijakso](media/supply_planning_5_recheduling_period_lot_accumulation_period.png "supply_planning_5_recheduling_period_lot_accumulation_period")  

**Esimerkki 2**: muutettu päivämäärä on uudelleenajoitusjaksolla, joka aiheuttaa olemassa olevan tarjonnan uudelleenajoittamisen. Uutta tarjontaa on ehdotettu kattamaan kysyntää erän koontijakson ulkopuolella.  

![Uudelleenajoitusjakso, Erän koontijakso, Aikataul. uud.](media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png "supply_planning_5_recheduling_period_lot_accum_period_reschedule")  

**Esimerkki 3**: puskuriajalla on kysyntää ja tarjonnan määrä erän koontijaksolla vastaa tarjonnan määrää. Seuraava kysyntä on katteeton ja uutta tarjontaa esitetään.  

![Puskuriaika, Erän koontijakso](media/supply_planning_5_dampener_period_lot_accumulation_period.png "supply_planning_5_dampener_period_lot_accumulation_period")  

**Esimerkki 4**: puskuriajalla on kysyntää ja tarjonta pysyy samalla päivämäärällä. Nykyisen tarjonnan määrä ei kuitenkaan riitä kattamaan kysyntää erän koontijaksolla, joten järjestelmä ehdottaa muuta määrä -toimenpidettä olemassa olevalle toimitustilaukselle.  

![Puskuriaika, Erän koontijakso, Muuta määrä](media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png "supply_planning_5_dampener_period_lot_accum_period_change_qty")  

**Oletusarvot:** **Aikaväli**-kentän ja kolmen uudelleenjärjestelyjakson kentän oletusarvo on tyhjä. **Puskuriaika**-kenttää lukuun ottamatta arvo on muissa kentissä 0D (nolla päivää). Jos **Puskuriaika**-kenttä on tyhjä, käytetään **Tuotannon asetukset** -ikkunassa olevan **Oletuspuskuriaika**-kentän arvoa.  

## <a name="modify-the-supply-orders"></a>Toimitustilausten muuttaminen  
Kun tilausehdotuksen määrä on laskettu, yksi tai usea tilauksen määrite voi muuttaa sitä. Esimerkiksi enimmäistilausmäärä on suurempi tai yhtä suuri kuin vähimmäistilausmäärä, joka on suurempi tai yhtä suuri kuin tilauskerrannainen.  

Määrää vähennetään, jos se ylittää maksimitilausmäärän. Tämän jälkeen se kasvaa, jos se on pienempi kuin vähimmäistilausmäärä. Lopuksi se pyöristetään ylöspäin siten, että se vastaa tiettyä tilauskerrannaista. Jäljellä oleva määrä käyttää samoja oikaisuja, kunnes kokonaiskysyntä on muutettu tilausehdotuksiksi.  

## <a name="delimit-the-item"></a>Rajaa nimike  
**Tuotantotapa** -vaihtoehto määrittää mitä lisätilauksia MRP-laskelma ehdottaa.  

Jos käytetään **Varasto-ohjautuva**-vaihtoehtoa, tilaukset koskevat vain kysymyksessä olevaa nimikettä.  

Jos käytetään **Tilausohjattu**-vaihtoehtoa, suunnittelujärjestelmä analysoi nimikkeen tuotannon tuoterakenteen ja luo ylimääräiset linkitetyt tilausehdotukset näille alemman tason nimikkeille, joilla on myös Tilausohjattu-määritys. Tämä jatkuu niin kauan kunnes laskevissa tuoterakenteissa on tilausohjautuvia nimikkeitä.  

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)   
[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)   
[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)

