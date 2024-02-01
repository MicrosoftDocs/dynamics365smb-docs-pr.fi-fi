---
title: Töiden aikatauluttaminen automaattisesti suoritettavaksi
description: Tietoja työjonotapahtumien käyttämisestä raporttien ja koodiyksiköiden suorittamiseen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 09/15/2023
ms.custom: bap-template
ms.search.form: '672, 673, 674, 671'
ms.service: dynamics-365-business-central
---
# <a name="use-job-queues-to-schedule-tasks"></a>Työjonojen käyttäminen tehtävien ajoittamisessa

Käytä **Työjonon tapahtumat** -sivua ajoittaaksesi ja suorittaaksesi tiettyjä raportteja ja codeuniteja. Voit määrittää töitä suoritettavaksi yhtä aikaa tai toistuvasti. Voit esimerkiksi haluta suorittaa **Myyjän * myyntitilasto** -raportin viikoittain ja seurata näin myyjäkohtaista viikkomyyntiä. Vaihtoehtoisesti voit suorittaa **Delegoi hyväksymispyynnöt** -codeunitin päivittäin, jolloin asiakirjoja ei kasaudu odottamaan käsittelyä.

Työjonon tapahtumat -sivulla on luettelo kaikista aiemmin luoduista töistä. Jos lisäät uuden työjonotapahtuman, jonka haluat suorittaa aikataulussa, sinun on annettava joitakin tietoja. Esimerkiksi:

* Suoritettavan objektin tyyppi, kuten raportti tai codeunit. Sinulla on oltava oikeus suorittaa kulloinenkin raportti tai codeunit.
* Objektin nimi ja objektitunnus.
* Parametrit, joilla määritetään työjonotapahtuman käytös. Voit esimerkiksi lisätä parametrin vain kirjattujen myyntitilausten lähettämistä varten.
* Milloin ja kuinka usein työjonotapahtuma suoritetaan.

> [!IMPORTANT]  
> Jos sinulle on määritetty [!INCLUDE[prod_short](includes/prod_short.md)]n mukana tuleva SUPER-käyttöoikeusjoukko, sinulla on oikeus suorittaa kaikkia käyttöoikeuteesi sisältyviä objekteja. Jos sinulla on delegoitu järjestelmänvalvojarooli, voit luoda ja ajoittaa työjonotapahtumia, mutta vain järjestelmänvalvojat ja lisensoidut käyttäjät voivat käyttää niitä.

Kun työjonot on määritetty ja käytössä, tila voi muuttua seuraavasti kunkin toistuvan jakson aikana:

* **Pidossa**  
* **Valmis**  
* **Työn alla**  
* **Virhe**  
* **Valmis**  
* **Estossa toimettomuuden vuoksi**

> [!NOTE]
> **Toimettomuudesta johtuvaa estossa** -tilaa käytetään pääasiassa työjonon tapahtumille, jotka ajoittavat synkronoinnin [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksen ja toisen sovelluksen kanssa, esimerkiksi [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Lisätietoja tästä tilasta on kohdassa [Tietoja toimettomuuden aikakatkaisuista](/dynamics365/business-central/admin-scheduled-synchronization-using-the-synchronization-job-queue-entries#about-inactivity-timeouts).

Kun työ on valmis, se poistetaan työjonotapahtumien luettelosta, ellei se ole toistuva työ. Toistuvien töiden yhteydessä **Aloituspvm ja -aika** -kentän arvo muokataan näyttämään seuraava aika, jolloin työ suoritetaan. 

## <a name="important-for-scheduling-recurring-jobs"></a>Tärkeitä tietoja toistuvien töiden aikatauluttamisesta

> [!IMPORTANT]  
> Toistuvat työjonot voivat vaikuttaa suorituskykyyn, joten niitä ei tulisi suorittaa liian usein. Yritä määrittää toistuvalle työlle niin pitkä toistoväli kuin mahdollista. Jos esimerkiksi olet määrittämässä viiden minuutin toistoväliä, harkitse, voisiko toistoväli olla sen sijaan 15 minuuttia tai jopa kerran tunnissa. Kun suunnittelet toistuvien töiden jonoja, ota huomioon sovelluksen alueet, joihin työ vaikuttaa. Onko se alue, jolla monet käyttäjät työskentelevät ja johon keskittyy paljon aktiviteettia? Ota huomioon yksittäisen työn suorituksen pituus ja yrityksen syyt töiden suoritukselle tietyllä aikavälillä.

## <a name="the-earliest-start-date"></a>Aikaisin aloituspvm

**Työjonon tapahtumakortti** -sivun **Varhaisin alkamispvm/aika** -kentän arvo näyttää, milloin työ seuraavan kerran suoritetaan. On useita tekijöitä, jotka voivat vaikuttaa siihen, suoritetaanko työjonotapahtuma silloin.

Yleisimmät tekijät ovat työjonon tapahtumien määrä ympäristössä ja ajoitettujen tehtävien kokonaismäärä. Suoritustasojen suojaamiseksi on asetettu toimintarajoja. Jos jonossa on paljon tapahtumia, ja jos esimerkiksi yksi niistä epäonnistuu tai tapahtumat vain vievät odotettua kauemmin, seuraava työ ei ehkä käynnisty oletettuna ajankohtana. Jos sinulla on koodiyksiköitä, jotka tuottavat vähintään 100 000 suunniteltua tehtävää, sinun on tutkittava tarvitsetko kaikki nämä tehtävät. Voit tarkastella kaikkien aikataulutettujen tehtävien luetteloa **Aikataulutetut tehtävät** -sivulla.

Lisätietoja työjonotapahtumien tilan valvonnasta on kohdassa [Minkä tahansa työn tilan tarkastelu](#to-view-status-for-any-job). Lisätietoja toimintarajoituksista saat kohdasta [Asynkroniset tehtävärajat](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#Task).

## <a name="monitor-status-or-errors-in-the-job-queue"></a>Työjonon tilan tai virheiden seuraaminen

Työnjonon luomat tiedot tallennetaan, jotta voit tehdä virheiden vianmäärityksen.  

Voit tarkastella ja muuttaa kunkin työjonotapahtuman tilaa. Kun luot työjonotapahtuman, sen tilaksi tulee **Estossa**. Voit määrittää tilaksi esimerkiksi **Valmis** ja takaisin tilaksi **Estossa**. Muuten tilatiedot päivitetään automaattisesti.

Seuraavassa taulukossa kuvataan **Tila**-kentän arvot.

| Tila | Kuvaus |
|--|--|
| Valmis | Työjonotapahtuma on valmis suoritettavaksi. |
| Työn alla | Työjonotapahtuma on keskeneräinen. Tämä kenttä päivittyy, kun työjonoa suoritetaan. |
| Pidossa | Työtapahtuman oletustila, kun se luodaan. Valitse **Aseta tilaksi valmis** -toiminto, jotta tilaksi muuttuu **Valmis**. Palauta tilaksi **Pidossa** valitsemalla **Määritä pitoon**. |
| Virhe | Tapahtui virhe. Valitse **Näytä virhe**, niin näyttöön tulee virhesanoma. |
| Valmis | Työjonotapahtuma on valmis. |

> [!Tip]  
> Työjonotapahtumien suoritus loppuu, kun tapahtuu virhe. Tämä voi olla ongelma esimerkiksi silloin, kun tapahtuma muodostaa yhteyden ulkoiseen palveluun, kuten pankkisyötteeseen. Jos palvelu ei ole väliaikaisesti saatavilla ja työjonotapahtuma ei pysty muodostamaan yhteyttä, tapahtuma näyttää virheen ja sen suorittaminen loppuu. Työjonotapahtuma on käynnistettävä manuaalisesti uudelleen. Voit kuitenkin välttää tämän tilanteen kentillä **Yritysten enimmäismäärä** ja **Uudelleenajon viive (s)**. **Yritysten enimmäismäärä** -kentän avulla voit määrittää, kuinka monta kertaa työjonotapahtuma voi epäonnistua, ennen kuin sen suorittamisen yrittäminen loppuu. **Uudelleenajon viive (s)** -kentän avulla voit määrittää yritysten välisen ajan sekunneissa. Näiden kahden kentän yhdistelmä saattaa pitää työjonotapahtuman käynnissä, kunnes ulkoinen palvelu on käytettävissä.

### <a name="to-view-status-for-any-job"></a>Minkä tahansa työn tilan näyttäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työjonon tapahtumat** ja valitse sitten vastaava linkki.
2. Valitse **Työjonotapahtumat**-sivulla ensin työjonotapahtuma ja sitten **Lokitapahtumat**-toiminto.  

> [!TIP]
> Voit telemetriaan perustuvaa syvällistä analyysiä varten voit käyttää Microsoft Azuren Application Insightsia tarkastellaksesi tehtävien jonotasojen tilaa. Saat lisätietoja telemetriasta kohdassa [Telemetrian seuranta ja analysointi](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) ja [Työjonon elinkaaren jäljitystelemetria](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

## <a name="view-scheduled-tasks"></a>Näytä ajoitetut tehtävät

**Ajoitetut tehtävät** -sivulla [!INCLUDE [prod_short](includes/prod_short.md)]issa näkyy, mitkä tehtävät ovat valmiita suoritettaviksi työjonossa. Sivulla näkyy myös tietoja yrityksestä, jossa kukin tehtävä on määritetty suoritettavaksi. Kuitenkin vain tehtävät, jotka on merkitty kuuluvaksi nykyiseen ympäristöön, voivat toimia.  

Esimerkiksi kaikki suunnitellut tehtävät pysäytetään, jos yritys on ympäristössä, joka on toisen ympäristön kopio. **Ajoitetut tehtävät** -sivulla voit määrittää tehtävät valmiiksi suoritettaviksi työjonossa.  

> [!NOTE]
> Sisäiset järjestelmänvalvojat ja lisensoidut käyttäjät voivat ajoittaa tehtäviä suoritettavaksi. Valtuutetut järjestelmänvalvojat voivat määrittää ja ajoittaa tehtäviä suoritettavaksi, mutta vain lisensoidut käyttäjät voivat käyttää niitä.

## <a name="the-my-job-queue-part"></a>Oma työjono -osa

Roolikeskuksen **Oma työjono** -osa sisältää työjonotapahtumat, jotka olet aloittanut mutta jotka eivät ole vielä valmiita. Oletusarvoisesti osa ei ole näkyvissä, mutta voit lisätä sen omaan roolikeskukseesi. Lue lisää mukauttamisesta kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).  

Osassa näkyvät seuraavat tiedot:

* Mitä asiakirjoja, joissa on tunnuksesi **Määritetty käyttäjätunnus** -kentässä, käsitellään tai mitkä ovat jonossa, mukaan lukien asiakirjat, jotka kirjataan taustalla. 
* Onko asiakirjan kirjaamisessa tai työjonotapahtumassa ilmennyt virhe. 

Oma työjono -osan avulla voit myös peruuttaa asiakirjan kirjaamisen.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Tarkastele virhettä oma työjono -osasta

1. Valitse tapahtumassa, jonka tila on **Virhe**, **Näytä virhe** -toiminto.
2. Tarkastele virhesanomaa ja korjaa ongelma.

## <a name="examples-of-what-you-can-schedule-using-job-queue-entries"></a>Esimerkkejä siitä, mitä voit ajoittaa työjonotapahtumien avulla

### <a name="schedule-reports"></a>Ajoita raportteja

Voit aikatauluttaa raportin tai erätyön ajon tietylle päivämäärälle ja kellonajalle. Aikataulutetut raportit ja erätyöt syötetään työjonoon ja käsitellään aikataulutettuna aikana vastaavasti kuin muut työt. **Aikataulu**-asetus valitaan sen jälkeen, kun **Lähetä kohteeseen** -toiminto on valittu, minkä jälkeen annetaan tiedot, kuten tulostin sekä päivämäärä ja kellonaika tai toistuvuus.  

Lisätietoja ajoittamisesta on ohjeaiheessa [Raportin suorittamisen aikatauluttaminen](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between--and-includeprod_short"></a>Synkronoinnin aikatauluttaminen [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[prod_short](includes/cds_long_md.md)]n välillä

Jos olet integroinut tuotteen [!INCLUDE[prod_short](includes/prod_short.md)] tuotteeseen [!INCLUDE[prod_short](includes/cds_long_md.md)], työjono mahdollistaa tietojen synkronoinnin ajoittamisen. Määrittämiesi suunnan ja sääntöjen mukaan työjonotapahtuma voi luoda yhdessä sovelluksessa toisen sovelluksen tietueita vastaavia tietueita. Hyvä esimerkki on yhteyshenkilön rekisteröiminen tuotteessa [!INCLUDE[crm_md](includes/crm_md.md)], jolloin työjonotapahtuma voi määrittää kyseissen yhteyshenkilön tuotteessa [!INCLUDE[prod_short](includes/prod_short.md)]. Lisätietoja on aikatauluttamisesta on kohdassa [Business Centralin ja Dynamics 365 Salesin synkronoinnin ajoittaminen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)

### <a name="schedule-when-to-post-sales-and-purchase-orders"></a>Ajoita milloin myynti- ja ostotilaukset kirjataan

Työjonotapahtumien avulla voit ajoittaa liiketoimintaprosesseja suoritettavaksi taustalla. Taustatehtävät voivat olla hyödyllisiä esimerkiksi, kun useat käyttäjät kirjaavat myyntitilauksia samanaikaisesti, mutta käsittelyssä voi olla vain yksi tilaus kerrallaan. Saat lisätietoja taustakirjaamisesta valitsemalla [Taustakirjauksen määrittäminen työjonojen avulla](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## <a name="handle-job-queue-entry-issues"></a>Käsittele työjonotapahtumien ongelmat

Jos työjonotapahtumassa näkyy virhe, ensimmäinen tapa ratkaista ongelma on käynnistää työjonotapahtuma uudelleen. Voit määrittää työjonotapahtuman tilaksi **Pidossa** ja sitten **Valmis** tai vain käynnistää sen uudelleen.

Jos uudelleenkäynnistys ei auta, ongelma saattaa olla koodissa. Voit löytää koodin omistaja (kutsutaan myös *julkaisijaksi*) työjonolokin AL-pinojäljityksestä. Jos virhe johtuu sovelluksesta/laajennuksesta, ota yhteyttä Microsoft-kumppaniisi. Jos virhe johtuu Microsoft-sovelluksesta, avaa Microsoftin tukipyyntö.

Jos otat yhteyttä Microsoft-kumppaniin tai Microsoft-tukeen, anna seuraavat tiedot:

* Sen työjonotapahtuman tunnus, jossa virhe tapahtui
* Virheen tapahtumisen aikaleima
* Aikavyöhyke

> [!TIP]
> Voit kerätä tiedot seuraavilla tavoilla sen mukaan, onko [!INCLUDE [prod_short](includes/prod_short.md)] -versio 22.1 aiempi vai myöhäisempi:
>
> * Jos kyseessä on aiempi versio, anna kuvakaappaus **työjono lokin tapahtumat** -sivusta.
> * Myöhempää versiota varten voit kopioida tiedot Työjonon loki tapahtumat -sivun **kopioi tiedot** -toiminnolla (Työjonon tunnus, aikaleima ja aikavyöhyke).

## <a name="monitor-the-job-queue-with-telemetry"></a>Työjonon valvominen telemetrian avulla

Järjestelmänvalvojat voivat käyttää [Azure Application Insightsia](/azure/azure-monitor/app/app-insights-overview) kerätäkseen ja analysoidakseen telemetriaa, joka auttaa tunnistamaan ongelmia. Saat lisätietoja telemetriasta kohdassa [Telemetrian seuranta ja analysointi](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) ja [Työjonon elinkaaren jäljitystelemetria](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

Telemetria mahdollistaa sen, että järjestelmänvalvojat voivat määrittää hälytyksiä työjono-ongelmista, jotka lähettävät tekstiviestin, sähköpostin tai Teams-viestin, jos jokin ei ole oikein. Lisätietoja näistä ilmoituksista on kohdassa [Telemetria-ilmoitus](/dynamics365/business-central/dev-itpro/administration/telemetry-alert).

## <a name="see-also"></a>Katso myös

[Hallinta](admin-setup-and-administration.md)  
[Business Central -sovelluksen määrittäminen](setup.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Työjonon elinkaaren jäljityksen telemetrian analysoiminen](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  
[Telemetria-ilmoitus](/dynamics365/business-central/dev-itpro/administration/telemetry-alert)

[!INCLUDE[footer-include](includes/footer-banner.md)]
