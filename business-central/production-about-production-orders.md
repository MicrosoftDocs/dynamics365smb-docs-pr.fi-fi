---
title: Tietoja tuotantotilauksista | Microsoft Docs
description: Tuotantotilauksilla hallitaan ostettujen materiaalien muuntamista valmistetuiksi tuotteiksi. Tuotantotilaukset (työtilaukset) reitittävät työn tuotannon eri tuotantovälineisiin (tuotantosoluihin tai kuormitusryhmiin).
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: f11b92eb0a9941e72c8f6c87e0e052fcc0530fd1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786944"
---
# <a name="about-production-orders"></a>Tietoja tuotantotilauksista
Tuotantotilauksilla hallitaan ostettujen materiaalien muuntamista valmistetuiksi tuotteiksi. Tuotantotilaukset reitittävät työn tuotannon eri tuotantosoluihin tai kuormitusryhmiin.  

Ennen tuotannon aloittamista, useimmat yritykset suorittavat tuotantosuunnittelun (yleensä kerran viikossa). Tuotantosuunnittelussa lasketaan, kuinka monta tuotantotilausta ja ostotilausta on suoritettava, jotta viikon myyntikysyntä täytetään. Ostotilaukset määrittävät osat, joita tarvitaan tuotannon tuotantorakenteen mukaan lopputuotteiden valmistamiseen.

Tuotantotilaukset kuuluvat keskeisesti sovelluksen tuotantotoimintoihin, ja niissä on mukana seuraavat tiedot:  

-   tuotteet, joiden valmistamista suunnitellaan  
-   suunnitelluissa tuotantotilauksissa tarvittavat materiaalit  
-   hiljattain valmistetut tuotteet  
-   valmiiksi valitut materiaalit  
-   aiemmin valmistetut tuotteet  
-   edeltävissä tuotanto-operaatioissa käytetyt materiaalit.  

Tuotantotilaukset toimivat lähtökohtana  

-   tulevan tuotannon suunnittelussa  
-   meneillään olevan tuotannon hallinnassa  
-   valmistuneen tuotannon seurannassa.  

## <a name="production-order-creation"></a>Tuotantotilausten luominen  
Tuotantotilauksia voi luoda manuaalisesti tilaus kerrallaan **Tuotantotilaus**-sivulla, mutta niitä voi luoda myös **Myyntitilauksen suunnittelu**- tai **Tilauksen suunnittelu** -sivuilla. **Suunnittelutyökirja**-sivulla luodaan useita tilauksia.  

Seuraavien kohteiden tietoja käytetään tuotantotilausten luonnissa:  

- Nimikkeet  
- Tuotantotuoterakent.
- Reititykset  
- kuormitusryhmät  
- tuotantosolut.  

## <a name="limitations-on-production-order-creation"></a>Tuotantotilauksen luomiseen liittyviä rajoituksia  
Tuotantotilaukset varataan ja niitä seurataan automaattisesti lähteeseen, kun  

-   ne luodaan **suunnittelutyökirjasta**  
-   ne luodaan **Myyntitilauksen suunnittelu** -sivun tilaustoiminnolla  
-   ne luodaan **Tilauksen suunnittelu** -sivulla  
-   niissä käytetään tuotantotilausten **Uudelleensuunnittele**-toimintoa.  

Lisätietoja on kohdassa [Kysynnän ja tarjonnan välisten suhteiden seuranta](production-how-track-demand-supply.md).

Muilla keinoilla luotuja tuotantotilauksia ei varata eikä seurata automaattisesti.   

## <a name="production-order-status"></a>Tuotantotilauksen tila  
Tuotantotilauksen tilan avulla hallitaan tuotantotilauksen toimintaa sovelluksessa. Tilauksen tila määrittää tuotannon muodon ja sisällön. Tuotantotilaukset näkyvät tilansa mukaisesti eri sivuilla. Tuotantotilauksen tilaa ei voi muuttaa manuaalisesti; sen sijaan täytyy käyttää **Muuta tilaa** -toimintoa.  

### <a name="simulated-production-order"></a>Simuloitu tuotantotilaus  
Seuraavat ominaisuudet tekevät simuloidusta tuotantotilauksesta yksilöllisen:  

- Kuten nimi kertoo, kyseessä on simulaatio. Sen pääasiallinen tehtävä on tarjousten ja kustannusten laskenta. Sitä voi käyttää esimerkiksi, kun tutkimus- ja kehitysosasto haluaa ehdotetun nimikkeen kustannusarvion. Simuloitu tuotantotilaus toimii esimerkkinä tuotantotilauksesta.  
- Se ei vaikuta tilausten suunnitteluun. Suunnittelussa (tuotanto-ohjelmassa ja tarvelaskennassa) ei oteta huomioon simuloituja tuotantotilauksia, eikä niillä ole vaikutusta suunnitteluun. Simuloitua tuotantotilausta ei myöskään voi käyttää mallina, koska se häviää tilaa muutettaessa.  

### <a name="planned-production-order"></a>Suunniteltu tuotantotilaus  
Seuraavat ominaisuudet tekevät suunnitellusta tuotantotilauksesta yksilöllisen:  

- Suunnitellun tuotantotilauksen voi luoda automaattisesti myyntitilauksesta.  
- Suunnitellut tuotantotilaukset ovat samanlaisia kuin vapautetut tuotantotilaukset. Suunnitellut tuotantotilaukset näyttävät tuotantosolujen ja kuormitusryhmien kokonaiskapasiteettitarpeen, jota tarvitaan kapasiteettitarvelaskennassa.  
- Suunniteltu tuotantotilaus on käytettävissä olevien tietojen perusteella tehty paras arvio tuotantosolun tai kuormitusryhmän kuormituksen tulevasta kuormituksesta. Ne luodaan tavallisesti suunnittelulaskennassa, mutta myös manuaalinen luominen on mahdollista. Koska suunnitellut tuotantotilaukset poistetaan myöhempiä suunnitelmia luotaessa, manuaalinen luominen ei ole käytännöllistä.  
- Suunnittelun yhteydessä tehtävän luomisen tuloksena saadaan ehdotettu "suunniteltu tilausvapautus", jossa on määrä, vapautuspäivämäärä ja eräpäivä. Suunnittelujärjestelmän logiikka perustuu täydennysjärjestelmään, uusintatilauskäytäntöihin ja tilauksen määritteisiin, jotka tuleva esiin nettotarpeiden suunnittelutoimissa.  
- Voit tarkastella niiden vaikutusta tutustumalla kunkin tuotantosolun tai kuormitusryhmän kuormitukseen suunnitellun tuotantotilauksen reitityksessä.  

### <a name="firm-planned-production-order"></a>Sitovasti suunniteltu tuotantotilaus  
Seuraavat ominaisuudet tekevät sitovasti suunnitellusta tuotantotilauksesta yksilöllisen:  

- Sitovasti suunnitellun tuotantotilauksen voi luoda automaattisesti myyntitilauksesta.  
- Sitovasti suunniteltu tuotantotilaus toimii jonkin sellaisen tulevan työn paikanvaraajana suunnitelman aikataulussa, joka vapautetaan tuotantoon.  
- Sitovasti suunnitellun tuotantotilauksen voi luoda suunnitelmasta tai manuaalisesti myyntitilauksista. Niitä ei poisteta myöhemmissä suunnitelmissa.  
- Suunnittelun yhteydessä tehtävän luomisen tuloksena saadaan ehdotettu "suunniteltu tilausvapautus", jossa on määrä, vapautuspäivämäärä ja eräpäivä. Suunnittelujärjestelmän logiikka perustuu täydennysjärjestelmään, uusintatilauskäytäntöihin ja tilauksen määritteisiin, jotka tuleva esiin nettotarpeiden suunnittelutoimissa.  
- Voit tarkastella niiden vaikutusta tutustumalla kunkin tuotantosolun tai kuormitusryhmän kuormitukseen sitovasti suunnitellun tuotantotilauksen reitityksessä.  

### <a name="released-production-order"></a>Vapautettu tuotantotilaus  
Seuraavat ominaisuudet tekevät vapautetusta tuotantotilauksesta yksilöllisen:  

- Vapautetun tuotantotilauksen voi luoda automaattisesti myyntitilauksesta.  
- Kun tuotantotilaus on vapautettu, se ei välttämättä merkitse, että materiaalit on valittu tai työ on siirtynyt fyysisesti ensimmäiseen operaatioon.  
- Tilauspohjaisessa tuotannossa vapautetun tuotantotilauksen luominen heti myyntitilauksen syöttämisen jälkeen on sangen tavallista.  
- Materiaalin todellinen kulutus ja tuotteen tuotos voidaan kirjata manuaalisesti vapautetun tuotantotilauksen avulla. Kulutuksen ja tuotteen tuotoksen automaattinen materiaalinotto tehdään vain vapautetuille tuotantotilauksille.  

### <a name="finished-production-order"></a>Valmis tuotantotilaus  
Seuraavat ominaisuudet tekevät valmiista tuotantotilauksesta yksilöllisen:  

- Valmis tuotantotilaus on tavallisesti sellainen, jonka tuotanto on valmis.  
- Tuotantotilauksen valmistuminen on erittäin tärkeää tuotettavan nimikkeen kustannuselinkaaren päättämisen kannalta. Kun tuotantotilaus on valmis, kustannuksia voi muokata ja täsmäyttää.  
- Valmiita tuotantotilauksia käytetään tilastoraporteissa. Ne myös tukevat mahdollisuutta seurata tilausta muihin tilauksiin (esimerkiksi myynti-, tuotanto- ja ostotilauksiin). Voit tarkastella yksityiskohtaisia historiatietoja seuraamalla valmiita tuotantotilauksia taaksepäin.  
- Valmiita tuotantotilauksia ei missään vaiheessa voi muuttaa.  

## <a name="production-order-execution"></a>Tuotantotilauksen toteuttaminen  
Kun tuotantotilaus on luotu ja ajoitettu, se täytyy vapauttaa tuotantoon toteutettavaksi. Tilauksen toteuttamisen yhteydessä kirjataan  

- poimitut tai kulutetut materiaalit  
- tilauksen käsittelyyn kuluva aika  
- tuotetun päänimikkeen määrä.  

Nämä tiedot voidaan kirjata manuaalisesti tai automaattisen raportoinnin välityksellä sen mukaan, miten nimikkeet on määritetty Materiaalinottotapa-kentässä.  

### <a name="material-consumption"></a>Materiaalin kulutus  
Sovelluksessa on useita vaihtoehtoja sille, miten tuotantoyrityksen kannattaa kirjata materiaalikulutus. Esimerkiksi materiaalin kulutus voidaan tallentaa manuaalisesti. Tämä voi olla hyvä vaihtoehto, jos komponentteja korvataan usein toisilla tai hukkatavaran määrä on odotettua suurempi.  

Materiaalin kulutusta voi käsitellä kulutuspäiväkirjan avulla, mutta sovellus voi kirjata kulutuksen myös automaattisesti. Tätä kutsutaan automaattisesti raportoinniksi. Raportointimenetelmiä ovat  

-   Manuaalinen  
-   Eteenpäin  
-   Taaksepäin  

Manuaaliset kulutusraportit käyttävät kulutuspäiväkirjaa määrittämään materiaalin poiminta.  

Eteenpäin kulutusraportti - Tässä menetelmässä lähdetään siitä, että koko tilauksen kaikkien materiaalien oletettu määrä on automaattisesti kulutettu, kun tuotantotilaus vapautetaan, lukuun ottamatta tilanteita, joissa käytetään reitityslinkin koodeja. Kun reitityslinkin koodeja käytetään, tuotantopäiväkirjaan kirjataan toimintavaiheen alusta lähtien kulutettu materiaali. Koko tuotantotilauksen Eteenpäin-materiaalinottotavan käyttäminen edellyttää, että kaksi asiaa toteutuu:  

- Ylätason tuotannon tuotantorakenteen kaikilla nimikkeillä täytyy olla Eteenpäin-materiaalinottotapa valittuna omissa nimikkeen korteissaan.  
- Tuotannon tuotantorakenteen kaikki reitityslinkin koodit täytyy poistaa.  

Takautuva kulutusraportti – Tämä menetelmä on kaikkien automaattisesti valittujen tai kulutettujen materiaalien todellinen määrä, kun tuotantotilauksen tilaksi vaihdetaan *Valmis* – paitsi reitityslinkin koodeja käytettäessä. Reitityslinkin koodeja käytettäessä materiaali kulutetaan, kun toimintavaiheelle kirjataan tietty päänimikkeen määrä tuotospäiväkirjaan.  

Kun tuotantotilaus päivitetään, materiaalinottotapa kopioidaan nimikkeen kortista. Koska tuotantotilauksen kunkin komponentin materiaalinottotapa ohjaa kulutuksen kirjaamisen tapaa ja ajankohtaa, on tärkeää muistaa, että yksittäisten nimikkeiden materiaalinottotapaa voi muuttaa suoraan tuotantotilauksesta.  

#### <a name="automatic-consumption-posting-flushing"></a>Kulutuksen automaattinen kirjaaminen (materiaalinotto)  
Automaattisesta materiaalinotosta on se hyöty, että syötettävien tietojen määrä vähenee huomattavasti. Kun operaation materiaalinotto voidaan toteuttaa automaattisesti, kulutuksen ja tuotosten koko kirjausprosessi voidaan automatisoida. Se haitta automaattisessa materiaalinotossa kuitenkin on, että hukkatavaran kirjauksessa voi olla virheitä tai hukkatavara voi jäädä kokonaan huomaamatta. Automaattisia raportointimenetelmiä ovat  

- koko tilauksen Eteenpäin-materiaalinotto  
- operaatiokohtainen Eteenpäin-materiaalinotto  
- operaatiokohtainen Taaksepäin-materiaalinotto  
- koko tilauksen Taaksepäin-materiaalinotto.  

#### <a name="automatic-reporting---forward-flush-the-entire-order"></a>Automaattinen raportointi - koko tilauksen Eteenpäin-materiaalinotto  
Jos tuotantotilaukselle tehdään työn alussa Eteenpäin-materiaalinotto, sovellus toimii lähes samoin kuin manuaalista kulutusta käytettäessä. Suurin ero on siinä, että kulutus tapahtuu automaattisesti.  

- Tuotannon tuoterakenteen koko sisältö kulutetaan ja vähennetään varastosta, kun vapautettu tuotantotilaus päivitetään.  
- Kulutusmäärä on tuotannon tuoterakenteessa määritetyn kokoonpanokohtaisen määrän ja rakennettavien päänimikkeiden määrän tulo.  
- Kulutuspäiväkirjaan ei tarvitse kirjata tietoja, jos kaikille nimikkeille on tarkoitus tehdä materiaalinotto.  
- Kun varaston nimikkeitä kulutetaan, tuotospäiväkirjan tapahtumien kirjausajankohdalla ei ole merkitystä. Tuotospäiväkirjalla ei ole vaikutusta, kun kulutusta kirjataan tällä tavalla.  
- Reitityslinkin koodeja ei voi määrittää.  

Koko tilauksen Eteenpäin-materiaalinotto sopii tuotantoympäristöihin, joissa  

-   valmistusvirheitä on vähän  
-   toimenpiteitä on vähän  
-   alkupään toimenpiteissä kulutetaan paljon komponentteja.  

#### <a name="automatic-reporting---forward-flushing-by-operation"></a>Automaattinen raportointi - operaatiokohtainen Eteenpäin-materiaalinotto  
Operaatiokohtaisen materiaalinoton avulla voit vähentää varastoa tietyn päänimikkeen reitityksen operaation aikana. Materiaali on sidottu reititykseen reitityslinkin koodeilla, jotka vastaavat komponenteille tuotannon tuoterakenteessa määritettyjä reitityslinkin koodeja.  

Materiaalinotto tapahtuu, kun saman reitityslinkin koodin mukainen operaatio alkaa. Operaatio katsotaan alkaneeksi, kun sen tietoja kirjataan operaation tuotospäiväkirjaan. Kirjattavat tiedot voivat olla esimerkiksi asetusajan syöttäminen.  

Materiaalinoton määrä on tuotannon tuoterakenteessa määritetyn kokoonpanokohtaisen määrän ja rakennettavien päänimikkeiden määrän tulo (oletettu määrä).  

Tämä tekniikka sopii parhaiten tilanteisiin, joissa operaatioita on useita ja osaa komponenteista käytetään vasta loppupään kokoonpanovaiheessa. Just-in-Time (JIT) -mallissa nimikkeet eivät välttämättä edes ole käsillä, kun RPO aloitetaan.  

Materiaalia voi kuluttaa operaatioiden aikana reitityslinkin koodien avulla. Kaikkia komponentteja ei välttämättä käytetä ennen viimeisiä kokoonpano-operaatioita, eikä niitä tule ottaa varastosta ennen sitä.  

#### <a name="automatic-reporting---back-flushing-by-operation"></a>Automaattinen raportointi - operaatiokohtainen Taaksepäin-materiaalinotto  
Operaatiokohtaisessa Taaksepäin-materiaalinotossa kulutus kirjataan sen jälkeen, kun operaatio on kirjattu tuotospäiväkirjaan.  

Tästä menetelmästä on se hyöty, että operaation valmiiden osien määrä tunnetaan.  

Tuotannon tuoterakenteen materiaali on linkitetty reititystietueisiin reitityslinkin koodeilla. Taaksepäin-materiaalinotto tapahtuu, kun sellainen tietyn reitityslinkin koodin mukainen operaatio kirjataan, jonka määrä on valmis.  

Materiaalinoton määrä on tuotannon tuoterakenteessa määritetyn kokoonpanokohtaisen määrän ja kyseiseen operaatioon tuotoksen määränä kirjattujen päänimikkeiden määrän tulo. Se ei välttämättä ole sama kuin oletettu määrä.  

#### <a name="automatic-reporting---back-flushing-the-entire-order"></a>Automaattinen raportointi - koko tilauksen Taaksepäin-materiaalinotto  
Reitityslinkin koodeja ei oteta huomioon tässä raportointimenetelmässä.  

Komponentit valitaan vasta, kun vapautetun tuotantotilauksen tilaksi vaihtuu *Valmis*. Materiaalinoton määrä on tuotannon tuoterakenteessa määritetyn kokoonpanokohtaisen määrän ja valmistuneiden ja varastoon lisättyjen päänimikkeiden määrän tulo.  

Taaksepäin-materiaalinoton käyttäminen koko tuotantotilauksessa edellyttää, että määritykset ovat samat kuin eteenpäin-materiaalinotossa: raportointitavaksi täytyy määrittää taaksepäin jokaisen nimikkeen kortissa ja se täytyy tehdä päätuoterakenteen kaikille raportoitaville nimikkeille. Myös kaikki reitityslinkin koodit täytyy poistaa tuotannon tuoterakenteesta.  

### <a name="production-output"></a>Tuotannon tuotos  
Sovelluksen avulla voi seurata tuotantotilauksen käsittelyyn kuluvaa aikaa sekä kirjata tuotetun määrän. Näiden tietojen avulla tuotannon kustannusten määrittäminen sujuu aiempaa tarkemmin. Standardipohjaisia kustannuslaskentajärjestelmiä käyttävät valmistajat voivat myös halutessaan kirjata todellisia tietoja, joista on hyöytä entistä parempien standardien kehittämisessä.  

Tuotos voidaan käsitellä tuotospäiväkirjan avulla, mutta sovellus voi myös kirjata sen automaattisesti. Sovellus kopioi materiaalinottotavan kuormitusryhmä- tai tuotantosolukortista tuotantotilauksen reititykseen päivityksen yhteydessä. Tuotoksesta voidaan materiaalin kulutuksen tavoin raportoida kolmella tavalla:  

- Manuaalinen  
- Eteenpäin  
- Taaksepäin  

Manuaalisessa menetelmässä kulutettu aika ja tuotettu määrä määritetään tuotospäiväkirjan avulla.  

Eteenpäin-menetelmä kirjaa oletetun tuotoksen (ja ajan), joka kirjataan automaattisesti tuotantotilauksen vapautuessa. Reitityslinkin koodeilla ei ole vaikutusta tuotoksen Eteenpäin-materiaalinottoon.  

Taaksepäin-menetelmä on oletettu tuotos (ja aika), joka kirjataan automaattisesti tuotantotilauksen valmistuessa. Reitityslinkin koodeilla ei ole vaikutusta tuotoksen Taaksepäin-materiaalinottoon.  

### <a name="posting-consumption-and-output"></a>Kulutuksen ja tuotoksen kirjaaminen  
Sekä kulutuksessa että tuotoksessa voi käyttää mitä tahansa automaattisen materiaalinoton ja manuaalisesti kirjattujen tietojen yhdistelmää. Voit esimerkiksi käyttää komponenteissa automaattista Eteenpäin-materiaalinottoa ja kirjata hukkatavaran kulutuspäiväkirjan avulla. Vastaavasti voit myös kirjata tuotoksen automaattisesti ja päänimikkeen hukkatavaran tai tilaukseen kuluneen ylimääräisen ajan tuotospäiväkirjan avulla.  

Jos kulutus ja tuotos lisätään manuaalisesi, näiden tietojen kirjausjärjestys täytyy määrittää. Voit kirjata kulutuksen ensin ja lisätä tuotoksen oletettuun määrään perustuvat tiedot pikamenetelmällä. Voit myös lisätä tuotoksen ensin **Pura reititys** -toiminnolla. Tämän jälkeen voit kirjata kulutuksen tuotoksen todellisen määrän perusteella.  

### <a name="production-journal"></a>Tuotantopäiväkirja  
Tuotantopäiväkirjassa kulutus- ja tuotospäiväkirjojen toiminnot yhdistyvät yhdeksi päiväkirjaksi, joka voidaan avata suoraan vapautetusta tuotantotilauksesta.  

Tuotantopäiväkirjan tarkoitus on toimia yksittäisenä liittymänä, jonka avulla voit kirjata kulutuksen ja tuotoksen tuotantotilauksesta.  

Tuotantopäiväkirjassa on selkeä näkymä, jonka avulla voit  

- kirjata vaivattomasti tuotantotilaukseen liittyvät tuotokset ja kulutuksen  
- yhdistää komponentit operaatioihin  
- yhdistää operaatioiden todelliset tiedot tuotantotilauksen reititys- ja komponenttirivien vakioarvioihin  
- kirjata ja tulostaa tuotantotilauksen operaatioiden rekisteröityjen tietojen yleiskuvauksen.  

Tuotantopäiväkirja tekee useita samoja tehtäviä kuin kulutus- ja tuotospäiväkirjat. Dimensiot, nimikkeen seuranta ja varastopaikan sisältö käsitellään samalla tavalla kuin kulutus- ja tuotospäiväkirjoissa.  

Tuotantopäiväkirja eroaa kuitenkin seuraavilla tavoilla kulutus- ja tuotospäiväkirjasta:  

- Tuotantopäiväkirja kutsutaan suoraan vapautetusta tuotantotilausrivistä ja esiasetetaan asianmukaisten tietojen mukaisesti.  
- Tuotantopäiväkirjan materiaalinottotavan suodattimen avulla voit määrittää, minkä tyyppisiä komponentteja on tarkoitus käsitellä.  
- Tilauksen määrät ja ajat, jotka on jo kirjattu, näkyvät päiväkirjan alaosassa todellisina tapahtumina.  
- Kentät, joiden tiedoilla ei ole merkitystä, ovat tyhjiä, eikä niitä voi muokata.  
- Käyttäjä voi määrittää tavan, jolla tuotoksen määrät esiasetetaan päiväkirjaan – esimerkiksi, että viimeisimmän operaation Tuotoksen määrä -arvon täytyy olla nolla.  
- Jos suljet päiväkirjan epähuomiossa kirjaamatta muutoksia, näyttöön tulee ilmoitus, joka antaa mahdollisuuden palata takaisin päiväkirjaan.  
- Se tuo näkyviin sekä operaatiot että komponentit loogisessa rakenteessa, joka toimii tuotantoprosessin yleiskatsauksena.  

Tuotantopäiväkirjassa kulutusmäärät kirjataan negatiivisina nimiketapahtumina, tuotoksen määrät kirjataan positiivisina tapahtumina ja käytetyn ajan tiedot kirjataan kapasiteettitapahtumina.  

## <a name="see-also"></a>Katso myös
[Tuotanto](production-manage-manufacturing.md)    
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)      
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
