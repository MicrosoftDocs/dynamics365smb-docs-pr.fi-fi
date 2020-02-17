---
title: Töiden aikatauluttaminen automaattisesti suoritettavaksi | Microsoft Docs
description: Ajoitettuja tehtäviä hallitaan työjonon avulla. Näillä töillä suoritetaan raportteja ja codeuniteja. Voit määrittää töitä suoritettavaksi yhtä aikaa tai toistuvasti.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: b8470fa559d8a640e1c05cc6e03ca4caf3a9827e
ms.sourcegitcommit: 1c286468697d403b9e925186c2c05e724d612b88
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2020
ms.locfileid: "2999781"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Käytä työjonoja ajoitustehtäviin
[!INCLUDE[d365fin](includes/d365fin_md.md)]:n työjonojen avulla käyttäjät voivat ajoittaa ja suorittaa tiettyjä raportteja ja koodiyksiköitä. Voit määrittää töitä suoritettavaksi yhtä aikaa tai toistuvasti. Esimerkiksi **Myyjä - Myyntitilasto** -raportti saatetaan haluta suorittaa viikoittain myyjän viikkokohtaisen myynnin seurantaa varten. **Käsittele huoltosähköpostijono** -koodiyksikkö voidaan taas suorittaa päivittäin ja varmistaa näin, että huoltotilauksiin liittyvät odottavat sähköpostit lähetetään asiakkaille ajallaan.

**Työjonon tapahtumat** -sivulla on luettelo kaikista aiemmin luoduista töistä. Jos lisäät uuden aikataulutettavan työjonotapahtuman tiedot, sinun on ilmoitettava minkä tyyppisen objektin, kuten raportin tai codeunitin, haluat suorittaa, sekä suoritettavan objektin nimen ja tunnuksen. Voit myös lisätä parametrit, joilla määritetään työjonotapahtuman käytös. Voit esimerkiksi lisätä parametrin vain kirjattujen myyntitilausten lähettämistä varten. Sinulla tulee olla tietyn raportin tai koodiyksikön suoritusoikeus tai muutoin järjestelmä palauttaa virheen, kun työjonoa suoritetaan.  

Työjonossa voi olla useita tapahtumia, jotka ovat jonossa hallittavia ja suoritettavia töitä. Tapahtuman tiedot määrittävät, mikä koodiyksikkö tai raportti suoritetaan, milloin ja miten usein tapahtuma suoritetaan, missä luokassa työ suoritetaan ja miten se suoritetaan.  

## <a name="to-set-up-background-posting-with-job-queues"></a>Taustakirjauksen määrittäminen työjonojen avulla
Työjonot ovat tehokas työkalu taustalla suoritettavien liiketoimintaprosessien ajoittamiseen. Kyse voi olla esimerkiksi useista käyttäjistä, jotka yrittävät kirjata myyntitilauksia, kun vain yksi tilaus voidaan käsitellä kerralla. Vaihtoehtoisesti voit ajoittaa kirjaukset tunneille, jotka sopivat parhaiten organisaatiollesi. Saattaa olla hyödyllistä ajaa yrityksessä tietyt toiminnot sen jälkeen, kun suurin osa päivän tietojen syötöistä on suoritettu.

Tämä on mahdollista, kun määrität työjonon ajamaan useita eräkirjausraportteja, kuten **Eräkirjaa myyntitilaukset**-, **Eräkirjaa ostotilaukset**-, **Eräkirjaa myyntipal.tilaukset**- ja **Eräkirjaa myyntihyvityslaskut** -raportit. Lisätietoja on kohdassa [Työjonotapahtuman luonti myyntilausten taustakirjausta varten](admin-job-queues-schedule-tasks.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] tukee kaikkien myynti-, osto- ja huoltoasiakirjojen taustakirjausta.

> [!NOTE]
> Jotkin työt muuttavat samoja tietoja, eikä niitä tulisi käyttää samaan aikaan, koska ne voivat aiheuttaa ristiriitoja. Esimerkiksi myyntiasiakirjojen taustatyöt yrittävät muokata samoja tietoja samaan aikaan. Työjonoluokat auttavat estämään tällaisia ristiriitoja varmistamalla, että kun yksi työ on käynnissä, samaan työjonoluokkaan kuuluvaa työtä ei suoriteta ennen kuin suoritettava työ on valmis. Esimerkiksi projekti, joka kuuluu myyntityöjonoluokkaan, odottaa, kunnes kaikki muut myyntiin liittyvät työt on tehty. Voit määrittää työjonoluokan **Taustakirjaus**-pikavälilehdellä **Myynnin ja saatavien asetukset** -sivulla. 
> 
> [!INCLUDE[d365fin](includes/d365fin_md.md)] tarjoaa työjonoluokkia myyntejä, ostoja ja pääkirjanpidon kirjauksia varten. On suositeltavaa, että jokin näistä tai luomasi on aina määritetty. Jos kohtaat ristiriidoista johtuvia virhetilanteita, harkitse luokan määrittämistä myynnin, oston ja pääkirjanpidon taustakirjausta varten.

Seuraavaksi käsitellään myyntitilausten taustakirjausta. Ostojen ja huolloin vaiheet ovat samankaltaiset.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntien ja myyntisaamisten asetukset** ja valitse sitten liittyvä linkki.
2. Valitse **Myyntien ja myyntisaamisten asetukset** -sivulla **Kirjaa työjonolla** -valintaruutu.
3. Suodata myyntitilauksen kirjauksen työjonotapahtumat valitsemalla **Työjonoluokan koodi** -kentässä **SalesPost**-luokka.

    Näin luodaan työjono-objekti, codeunit 88 **Työjonon kautta kirjattu myynti**. Jatka ottamalla se käyttöön **Työjonotapahtumat**-sivulla.
4. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Työjonotapahtumat** ja valitse sitten liittyvä linkki.
5. Valitse **Työjonotapahtumat**-sivulla **Uusi**-toiminto.
6. Valitse **Suoritettavan objektin tyyppi** -kentässä **Codeunit**.  
7. Valitse **Suoritettavan objektin tunnus** -kentässä **88**. Kuvaus ja objektin otsikko suorita-kenttiin näyttää Myyntikirjauksen työjonosta.

    Muilla kentillä ei ole merkitystä tässä skenaariossa.
8. Valitse **Määritä tilaksi valmis** -toiminto.
9. Varmistaaksesi, että työjono toimii odotetulla tavalla, kirjaa myyntitilaus. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).
10. Tarkista **Työjonon lokitapahtumat** -sivulta, onnistuiko myyntitilauksen kirjaus. Lisätietoja on kohdassa [Työjonon tilan tai virheiden tarkasteleminen](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Jos haluat myös tulostaa kirjattavat myyntiasiakirjat, valitse **Kirjaa ja tulosta työjonolla** -valintaruutu **Myyntien ja myyntisaamisten asetukset** -sivulla.  

> [!IMPORTANT]  
> Jos määrität asiakirjat kirjaavan ja tulostavan työn ja tulostimessa avautuu valintaikkuna, kuten tunnistetietojen pyyntö tai tulostimen musteen loppumisesta ilmoittava varoitus, asiakirja kirjataan mutta sitä ei tulosteta. Vastaava työjonotapahtuma aikakatkaistaan lopulta, ja **Tila**-kentän arvoksi määritetään **Virhe**. Näin ollen suosittelemme, että et käytä tulostimen asetuksia, jotka edellyttävät vuorovaikutusta tulostimen näytön valintaruutujen kanssa taustakirjausten yhteydessä.

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Työjonotapahtuman luonti myyntitilausten eräkirjausta varten
Seuraavaksi selitetään, miten **Eräkirjaa myyntitilaukset** -raportti määritetään kirjaamaan vapautetut myyntitilaukset automaattisesti arkipäivisin kello 16.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Työjonotapahtumat** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3. Valitse **Suoritettavan objektin tyyppi** -kentässä **Raportti**.  
4. Valitse **Suoritettavan objektin tunnus** -kentässä 296, **Eräkirjaa myyntitilaukset**.
5. Valitse **Raporttipyyntösivu**-valintaruutu.
6. Määritä **Eräkirjaa myyntitilaukset** -pyyntösivulla, mitä myyntitilausten automaattiseen kirjaukseen sisältyy, ja valitse sitten **OK**-painike.
7. Valitse kaikki valintaruudut **Suorita maanantaisin** -kohdasta **Suorita perjantaisin** -kohtaan.
8. Anna **Aloitusaika**-kentässä arvoksi 16.00.
9. Valitse **Määritä tilaksi valmis** -toiminto.

Kirjaamista odottavat myyntitilaukset kirjataan nyt joka arkipäivä kello 16.

> [!NOTE]
> Jos työjono ei voi kirjata myyntitilausta, tilaksi muutetaan **Virhe** ja myyntitilaus lisätään niiden myyntitilausten luetteloon, jotka käyttäjän on käsiteltävä manuaalisesti. Lisätietoja on kohdassa [Työjonon tilan tai virheiden tarkasteleminen](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Kun työjonot on määritetty ja käytössä, tila voi muuttua seuraavasti kunkin toistuvan jakson aikana:

* **Estossa**  
* **Valmis**  
* **Työn alla**  
* **Virhe**  
* **Valmis**  

Kun työ on valmis, se poistetaan työjonotapahtumien luettelosta, ellei se ole toistuva työ. Jos kyseessä on toistuva työ, **Aloituspvm ja -aika** -kentän arvo muokataan näyttämään seuraava aika, jolloin työ odotetaan suoritettavan.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Työjonon tilan tai virheiden näyttäminen
Työnjonon suorituksen aikana luotavat tiedot tallennetaan tietokantaan, jotta voit tehdä työjonon virheiden vianmäärityksen.

### <a name="to-view-status-for-any-job"></a>Minkä tahansa työn tilan näyttäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Työjonotapahtumat** ja valitse sitten liittyvä linkki.
2. Valitse **Työjonotapahtumat**-sivulla ensin työjonotapahtuma ja sitten **Lokitapahtumat**-toiminto.  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Myynti- tai ostoasiakirjan tilan näyttäminen
1. Valitse asiakirjassa, jonka yritit kirjata työjonon avulla, **Työjonon tila** -kenttä, jossa on **Virhe**.
2. Tarkastele virhesanomaa ja korjaa ongelma.

## <a name="the-my-job-queue-part"></a>Oma työjono -osa
Roolikeskuksen **Oma työjono** -osa sisältää työjonotapahtumat, jotka olet aloittanut mutta jotka eivät ole vielä valmiita. Oletusarvoisesti osa ei ole näkyvissä, joten se on lisättävä omaan roolikeskukseesi. Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).  

Tässä osassa näkee, mitä asiakirjoja, joissa on tunnuksesi **Määritetty käyttäjätunnus** -kentässä, käsitellään tai mitkä ovat jonossa, mukaan lukien taustakirjaukseen liittyvät asiakirjat. Osa tietää yhdellä silmäyksellä, onko asiakirjan kirjaamisessa tai työjonon tapahtumissa tapahtunut virheitä. Osan avulla voit peruuttaa kun asiakirjan kirjaamisen, jos se ei ole käynnissä.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Tarkastele virhettä oma työjono -osasta
1. Valitse tapahtumassa, jonka tila on **Virhe**, **Näytä virhe** -toiminto.
2. Tarkastele virhesanomaa ja korjaa ongelma.

## <a name="security"></a>Suojaus  
Työjonon tapahtumien suoritus perustuu käyttöoikeuksiin. Kyseiset oikeudet on sallittava raportin tai koodiyksikön toteuttamiseen.  

Kun työjono on aktivoitu manuaalisesti, se suoritetaan käyttäjän tunnistetiedoilla. Kun työjono on aktivoitu ajoitettuna tehtävänä, se suoritetaan palvelininstanssin tunnistetiedoilla. Kun työ on suoritettu, se suoritetaan sen aktivoivan työjonon tunnistetiedoilla. Työjonon luoneella käyttäjällä on oltava myös käyttöoikeudet. Kun kyse suorita käyttäjäistunnossa -työnä (esimerkiksi taustakirjauksissa), se suoritetaan kyseisen työn luoneen käyttäjän tunnistetiedoilla.  

> [!IMPORTANT]  
>  Jos käytät [!INCLUDE[d365fin](includes/d365fin_md.md)]in mukana toimitettuja pääkäyttöoikeusjoukkoa, sinulla ja käyttäjillä oikeudet suorittaa kaikki objektit. Tässä tapauksessa kunkin käyttäjän käyttöoikeutta rajoittavat vain tietojen käyttöoikeudet.  

## <a name="using-job-queues-effectively"></a>Käytetään työjonoja tehokkaasti  
Työjonotapahtuma-tietueella on monta kenttää, joiden tarkoituksena on viedä parametrejä koodiyksikölle, jonka olet määrittänyt ajettavaksi työjonossa. Tämä tarkoittaa myös sitä, että koodiyksiköt, jotka suoritetaan työjonon kautta, on määritettävä työjonotapahtumatietueessa **OnRun**-käynnistimen parametrina. Tämä auttaa parantamaan tietoturvaa, sillä se estää käyttäjiä suorittamasta satunnaisia koodiyksiköitä työjonon kautta. Jos käyttäjän on välitettävä raportoitavat parametrit, raportti on suoritettava koodiyksikössä, joka jäsentää syöttöparametrit ja syöttää ne raporttiin ennen sen suoritusta.  

## <a name="scheduling-synchronization-between-included365finincludesd365fin_mdmd-and-includecrm_mdincludescrm_mdmd"></a>Synkronoinnin aikatauluttaminen [!INCLUDE[d365fin](includes/d365fin_md.md)] :n ja [!INCLUDE[crm_md](includes/crm_md.md)]:n välillä
Jos olet integroinut [!INCLUDE[d365fin](includes/d365fin_md.md)]:n [!INCLUDE[crm_md](includes/crm_md.md)] -ohjelman kanssa, voit ajoittaa työjonon avulla, milloin haluat synkronoida näiden kahden liiketoimintasovelluksen tietueiden tiedot. Integroinnille määritetyn suunnan ja sääntöjen mukaan synkronointityöt voivat myös luoda uusia tietueita kohdesovellukseen, jotta ne vastaavat lähdetietoja. Jos myyjä esimerkiksi luo uuden kontaktin [!INCLUDE[crm_md](includes/crm_md.md)]-ohjelmassa, synkronointityö voi luoda kontaktin linkitertylle myyjälle [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa. Lisätietoja on kohdassa [Business Centralin ja Dynamics 365 Salesin synkronoinnin ajoittaminen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)

## <a name="see-also"></a>Katso myös  
[Hallinta](admin-setup-and-administration.md)  
[Business Central -sovelluksen määrittäminen](setup.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
