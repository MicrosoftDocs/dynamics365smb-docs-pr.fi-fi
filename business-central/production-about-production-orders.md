---
title: Tietoja tuotantotilauksista
description: 'Tietoja tuotantotilauksista ja siitä, miten niillä hallitaan ostettujen materiaalien muuntamista valmistetuiksi tuotteiksi.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000813, 99000814, 99000815, 99000816, 99000829, 99000830, 99000831, 99000832, 99000833, 99000838, 99000839, 99000867, 99000868, 99000882, 99000897, 99000898, 99000900, 99000912, 99000913, 99000914, 99000917'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="about-production-orders"></a>Tietoja tuotantotilauksista

Tuotantotilauksilla hallitaan ostettujen materiaalien muuntamista valmistetuiksi tuotteiksi. Tuotantotilaukset reitittävät työn tuotannon eri tuotantosoluihin tai kuormitusryhmiin.  

Ennen tuotannon aloittamista useimmat yritykset suorittavat tuotantosuunnittelun (yleensä kerran viikossa). Tuotantosuunnittelussa lasketaan, kuinka monta tuotantotilausta ja ostotilausta on suoritettava, jotta viikon myyntikysyntä täytetään. Ostotilaukset määrittävät osat, joita tarvitaan tuotannon tuotantorakenteen mukaan lopputuotteiden valmistamiseen.

Tuotantotilaukset kuuluvat keskeisesti tuotantotoimintoihin, ja niissä on mukana seuraavat tiedot:  

- tuotteet, joiden valmistamista suunnitellaan  
- suunnitelluissa tuotantotilauksissa tarvittavat materiaalit  
- valmistetut tuotteet  
- valmiiksi valitut materiaalit  
- aiemmin valmistetut tuotteet  
- edeltävissä tuotanto-operaatioissa käytetyt materiaalit.  

Tuotantotilaukset toimivat lähtökohtana  

- tulevan tuotannon suunnittelussa  
- meneillään olevan tuotannon hallinnassa  
- valmistuneen tuotannon seurannassa.  

## <a name="production-order-creation"></a>Tuotantotilausten luominen

Tuotantotilauksia voidaan luoda manuaalisesti tilaus kerrallaan **Tuotantotilaus**-sivulla, mutta niitä voi luoda myös **Myyntitilauksen suunnittelu**- tai **Tilauksen suunnittelu** -sivuilla. **Suunnittelutyökirja**-sivulla voidaan luoda myös useita tilauksia.  

Tuotantotilauksen luodaan käyttämällä seuraavien kohteiden tietoja:  

- Nimikkeet  
- Tuotantotuoterakent.
- Reititykset  
- kuormitusryhmät  
- tuotantosolut.  

## <a name="limitations-on-creating-production-orders"></a>Tuotantotilauksen luomiseen liittyviä rajoituksia

Tuotantotilaukset varataan ja niitä seurataan automaattisesti lähteeseen, kun  

- ne luodaan [suunnittelutyökirjasta](production-how-to-run-mps-and-mrp.md)  
- Luotu [Myyntitilaus suunnittelu](production-how-to-create-production-orders-from-sales-orders.md) -sivulta  
- ne luodaan [Tilauksen suunnittelu](production-how-to-plan-for-new-demand.md) -sivulla  
- niissä käytetään tuotantotilausten [Uudelleensuunnittele](production-how-to-replan-refresh-production-orders.md)-toimintoa.  

Lisätietoja on kohdassa [Kysynnän ja tarjonnan välisten suhteiden seuranta](production-how-track-demand-supply.md).

Muilla keinoilla luotuja tuotantotilauksia ei varata eikä seurata automaattisesti.

## <a name="production-order-status"></a>Tuotantotilauksen tila

Tuotantotilauksen tilan avulla hallitaan tuotantotilauksen toimintaa sovelluksessa. Tilauksen tila määrittää tuotannon muodon ja sisällön. Tuotantotilaukset näkyvät tilansa mukaisesti eri sivuilla. Tuotantotilauksen tilaa ei voi muuttaa manuaalisesti. **Muuta tilaa** -toimintoa on käytettävä yksittäisessä tuotantotilauksessa tai **Muuta tuotantotilauksen tila** -sivulla.  

### <a name="simulated-production-order"></a>Simuloitu tuotantotilaus

Simuloitu tuotantotilaus yksilöivä, ja se perustuu seuraaviin ominaisuuksiin:  

- Nimen mukaisesti kyse on tarjouksissa ja kustannuslaskennassa käytettävästä simulaatiosta. Esimerkki: tuotekehitysosasto haluaa saada ehdotetun nimikkeen kustannusarvion. Simuloitu tuotantotilaus toimii esimerkkinä tuotantotilauksesta.  
- Ne eivät vaikuta tilausten suunnitteluun. Suunnittelussa (tuotanto-ohjelmassa ja tarvelaskennassa) ei oteta huomioon simuloituja tuotantotilauksia, eikä niillä ole vaikutusta suunnitteluun. Simuloitua tuotantotilausta ei myöskään voi käyttää mallina, koska se häviää tilaa muutettaessa.  

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
- Sitovasti suunniteltu tuotantotilaus toimii jonkin sellaisen tulevan projektin paikkamerkkinä suunnitelman aikataulussa, joka vapautetaan tuotantoon.  
- Sitovasti suunnitellun tuotantotilauksen voi luoda suunnitelmasta tai manuaalisesti myyntitilauksista. Niitä ei poisteta myöhemmissä suunnitelmissa.  
- Suunnittelun yhteydessä tehtävän luomisen tuloksena saadaan ehdotettu "suunniteltu tilausvapautus", jossa on määrä, vapautuspäivämäärä ja eräpäivä. Suunnittelujärjestelmän logiikka perustuu täydennysjärjestelmään, uusintatilauskäytäntöihin ja tilauksen määritteisiin, jotka tuleva esiin nettotarpeiden suunnittelutoimissa.  
- Voit tarkastella niiden vaikutusta tutustumalla kunkin tuotantosolun tai kuormitusryhmän kuormitukseen sitovasti suunnitellun tuotantotilauksen reitityksessä.  

### <a name="released-production-order"></a>Vapautettu tuotantotilaus

Seuraavat ominaisuudet tekevät vapautetusta tuotantotilauksesta yksilöllisen:  

- Vapautetun tuotantotilauksen voi luoda automaattisesti myyntitilauksesta.  
- Vaikka tuotantotilaus on vapautettu, se ei välttämättä merkitse sitä, että materiaalit on kerätty tai että projekti on siirtynyt fyysisesti ensimmäiseen työvaiheeseen.  
- Tilauspohjaisessa tuotannossa vapautetun tuotantotilauksen luominen heti myyntitilauksen syöttämisen jälkeen on sangen tavallista.  
- Materiaalin todellinen kulutus ja tuotteen tuotos voidaan kirjata manuaalisesti vapautetun tuotantotilauksen avulla. Kulutuksen ja tuotteen tuotoksen automaattinen materiaalinotto tehdään vain vapautetuille tuotantotilauksille.  

### <a name="finished-production-order"></a>Valmis tuotantotilaus

Seuraavat ominaisuudet tekevät valmiista tuotantotilauksesta yksilöllisen:  

- Valmis tuotantotilaus on tavallisesti sellainen, jonka tuotanto on valmis.  
- Tuotantotilauksen valmistuminen on erittäin tärkeää tuotettavan nimikkeen kustannuselinkaaren päättämisen kannalta. Kun tuotantotilaus on valmis, kustannuksia voi muokata ja täsmäyttää.  
- Valmiita tuotantotilauksia käytetään tilastoraporteissa. Ne myös tukevat mahdollisuutta seurata tilausta muihin tilauksiin (esimerkiksi myynti-, tuotanto- ja ostotilauksiin). Voit tarkastella yksityiskohtaisia historiatietoja seuraamalla valmiita tuotantotilauksia taaksepäin.  
- Valmiita tuotantotilauksia ei missään vaiheessa voi muuttaa.  

## <a name="production-order-execution"></a>Tuotantotilauksen toteuttaminen

Kun tuotantotilaus on luotu ja ajoitettu, se on vapautettava tuotantoon toteutettavaksi. Tilauksen toteuttamisen yhteydessä kirjataan  

- poimitut tai kulutetut materiaalit  
- tilauksen käsittelyyn kuluva aika  
- tuotetun päänimikkeen määrä.  

Nämä tiedot voidaan kirjata manuaalisesti tai automaattisella raportoinnilla. Menetelmä määräytyy nimikkeen ja tuotantosolun Materiaaliottotapa-kentän määrityksistä.  

### <a name="material-consumption"></a>Materiaalin kulutus

[!INCLUDE [prod_short](includes/prod_short.md)] sisältää erilaisia vaihtoehtoja materiaalin kulutuksen kirjaamiseen. Materiaalin kulutus voidaan tallentaa esimerkiksi manuaalisesti. Tämä voi olla hyvä vaihtoehto, jos komponentteja korvataan usein toisilla tai hukkatavaran määrä on odotettua suurempi.  

Materiaalin kulutusta voi käsitellä [kulutuspäiväkirjan](production-how-to-post-consumption.md) avulla, mutta [!INCLUDE [prod_short](includes/prod_short.md)] voi kirjata kulutuksen myös automaattisesti. Tätä kutsutaan automaattisesti raportoinniksi (materiaaliotto). Saatavana olevat raportointimenetelmät: manuaalinen sekä eteenpäin ja taaksepäin suuntautuva raportointi.

Manuaaliset kulutusraportit käyttävät kulutuspäiväkirjaa määrittämään materiaalin poiminta.  

Eteenpäin kulutusraportti - Tässä menetelmässä lähdetään siitä, että koko tilauksen kaikkien materiaalien oletettu määrä on automaattisesti kulutettu, kun tuotantotilaus vapautetaan, lukuun ottamatta tilanteita, joissa käytetään reitityslinkin koodeja. Kun reitityslinkin koodeja käytetään, tuotantopäiväkirjaan kirjataan toimintavaiheen alusta lähtien kulutettu materiaali. Koko tuotantotilauksen Eteenpäin-materiaalinottotavan käyttäminen edellyttää, että kaksi asiaa toteutuu:  

- Ylätason tuotannon tuotantorakenteen kaikilla nimikkeillä täytyy olla Eteenpäin-materiaalinottotapa valittuna omissa nimikkeen korteissaan.  
- Tuotannon tuotantorakenteen kaikki reitityslinkin koodit täytyy poistaa.  

Takautuva kulutusraportti – Tämä menetelmä on kaikkien automaattisesti valittujen tai kulutettujen materiaalien todellinen määrä, kun tuotantotilauksen tilaksi vaihdetaan *Valmis* – paitsi reitityslinkin koodeja käytettäessä. Reitityslinkin koodeja käytettäessä materiaali kulutetaan, kun toimintavaiheelle kirjataan tietty päänimikkeen määrä tuotospäiväkirjaan.  

Kun tuotantotilaus päivitetään, materiaalinottotapa kopioidaan nimikkeen kortista. Koska tuotantotilauksen kunkin komponentin materiaalinottotapa ohjaa kulutuksen kirjaamisen tapaa ja ajankohtaa, on tärkeää muistaa, että yksittäisten nimikkeiden materiaalinottotapaa voi muuttaa suoraan tuotantotilauksesta. Lisätietoja on kohdassa [Komponenttien materiaalinotto toiminnan tuotoksen mukaan](production-how-to-flush-components-according-to-operation-output.md).

### <a name="production-output"></a>Tuotannon tuotos

[!INCLUDE [prod_short](includes/prod_short.md)] mahdollistaa tuotantotilauksen käsittelyyn kuluvan ajan seurannan sekä tuotetun määrän kirjaamisen. Näiden tietojen avulla tuotannon kustannusten määrittäminen sujuu aiempaa tarkemmin. Standardipohjaisia kustannuslaskentajärjestelmiä käyttävät valmistajat voivat myös halutessaan kirjata todellisia tietoja, joista on hyöytä entistä parempien standardien kehittämisessä.  

Tuotos voidaan käsitellä [tuotospäiväkirjan](production-how-to-post-output-quantity.md) avulla, minkä lisäksi se voidaan kirjata myös automaattisesti. [!INCLUDE [prod_short](includes/prod_short.md)] kopioi materiaalinottotavan kuormitusryhmä- tai tuotantosolukortista tuotantotilauksen reititykseen päivityksen yhteydessä. Tuotos raportoidaan materiaalin kulutuksen tavoin manuaalisesti, eteenpäin tai taaksepäin.

Manuaalisessa menetelmässä kulutettu aika ja tuotettu määrä määritetään tuotospäiväkirjan avulla.  

Eteenpäin-menetelmä kirjaa oletetun tuotoksen (ja ajan), joka kirjataan automaattisesti tuotantotilauksen vapautuessa. Reitityslinkin koodeilla ei ole vaikutusta tuotoksen Eteenpäin-materiaalinottoon.  

Taaksepäin-menetelmä on oletettu tuotos (ja aika), joka kirjataan automaattisesti tuotantotilauksen valmistuessa. Reitityslinkin koodeilla ei ole vaikutusta tuotoksen Taaksepäin-materiaalinottoon.  

### <a name="posting-consumption-and-output"></a>Kulutuksen ja tuotoksen kirjaaminen

Sekä kulutuksessa että tuotoksessa voi käyttää mitä tahansa automaattisen materiaalinoton ja manuaalisesti kirjattujen tietojen yhdistelmää. Voit esimerkiksi käyttää komponenteissa automaattista Eteenpäin-materiaalinottoa ja kirjata hukkatavaran kulutuspäiväkirjan avulla. Voit kirjata vastaavasti tuotoksen automaattisesti ja päänimikkeen hukkatavaran tai tilaukseen kuluneen ylimääräisen ajan tuotospäiväkirjan avulla.  

Jos kulutus ja tuotos lisätään manuaalisesti, näiden tietojen kirjausjärjestys on määritettävä. Voit kirjata kulutuksen ensin ja lisätä tuotoksen oletettuun määrään perustuvat tiedot pikamenetelmällä. Voit myös lisätä tuotoksen ensin **Pura reititys** -toiminnolla. Tämän jälkeen voit kirjata kulutuksen tuotoksen todellisen määrän perusteella.  

### <a name="production-journal"></a>Tuotantopäiväkirja

[Tuotantopäiväkirjassa](production-how-to-register-consumption-and-output.md) kulutus- ja tuotospäiväkirjojen toiminnot yhdistyvät yhdeksi päiväkirjaksi, joka voidaan avata suoraan vapautetusta tuotantotilauksesta.  

Tuotantopäiväkirjan tarkoitus on toimia yksittäisenä liittymänä, jonka avulla voit kirjata kulutuksen ja tuotoksen tuotantotilauksesta.  

Tuotantopäiväkirjassa on selkeä näkymä, jonka avulla voit  

- kirjata vaivattomasti tuotantotilaukseen liittyvät tuotokset ja kulutuksen  
- yhdistää komponentit operaatioihin  
- yhdistää työvaiheiden todelliset tiedot tuotantotilauksen reititys- ja komponenttirivien vakioarvioihin  
- kirjata ja tulostaa tuotantotilauksen operaatioiden rekisteröityjen tietojen yleiskuvauksen.  

Tuotantopäiväkirja suorittaa monia samoja tehtäviä kuin kulutus- ja tuotospäiväkirjat. Dimensiot, nimikeseuranta ja varastopaikan sisältö käsitellään samalla tavoin.  

Tuotantopäiväkirjat eroavat kuitenkin seuraavilla tavoilla kulutus- ja tuotospäiväkirjoista:  

- Tuotantopäiväkirja kutsutaan suoraan vapautetusta tuotantotilausrivistä ja esimääritetään asianmukaisten tietojen mukaisesti.  
- Tuotantopäiväkirjan materiaalinottotavan suodattimen avulla voit määrittää, minkä tyyppisiä komponentteja on tarkoitus käsitellä.  
- Tilaukselle jo kirjatut määrät ja ajat näkyvät todellisina tapahtumina päiväkirjan alaosassa.  
- Kentät, joiden tiedoilla ei ole merkitystä, ovat tyhjiä, eikä niitä voi muokata.  
- Käyttäjä voi määrittää tavan, jolla tuotoksen määrät esiasetetaan päiväkirjaan – esimerkiksi, että viimeisimmän operaation Tuotoksen määrä -arvon täytyy olla nolla.  
- Jos suljet päiväkirjan epähuomiossa kirjaamatta muutoksia, näyttöön tulee ilmoitus, joka antaa mahdollisuuden palata takaisin päiväkirjaan.  
- Se tuo näkyviin sekä operaatiot että komponentit loogisessa rakenteessa, joka toimii tuotantoprosessin yleiskatsauksena.  

Tuotantopäiväkirjassa kulutusmäärät kirjataan negatiivisina nimiketapahtumina, tuotoksen määrät kirjataan positiivisina tapahtumina ja käytetyn ajan tiedot kirjataan kapasiteettitapahtumina.  

## <a name="see-also"></a>Katso myös

[Tuotanto](production-manage-manufacturing.md)
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
