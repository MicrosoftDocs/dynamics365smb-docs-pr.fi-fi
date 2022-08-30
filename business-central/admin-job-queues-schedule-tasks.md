---
title: Töiden aikatauluttaminen automaattisesti suoritettavaksi
description: Ajoitettuja tehtäviä hallitaan työjonon avulla. Näillä töillä suoritetaan raportteja ja codeuniteja. Voit määrittää töitä suoritettavaksi yhtä aikaa tai toistuvasti.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 672, 673, 674, 671
ms.date: 10/01/2021
ms.author: edupont
ms.openlocfilehash: 081f900836f97d6630608aade4251272ee1a1ff1
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317432"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Käytä työjonoja ajoitustehtäviin

Työjonojen avulla käyttäjät voivat ajoittaa ja suorittaa tiettyjä raportteja ja codeuniteja. Voit määrittää töitä suoritettavaksi yhtä aikaa tai toistuvasti. Voit esimerkiksi haluta suorittaa **Myyjä - myyntitilasto** -raportin viikoittain ja seurata näin myyjäkohtaista viikkomyyntiä. Vaihtoehtoisesti voit suorittaa **Delegoi hyväksymispyynnöt** -codeunitin päivittäin, jolloin asiakirjoja ei kasaudu odottamaan käsittelyä.

**Työjonon tapahtumat** -sivulla on luettelo kaikista aiemmin luoduista töistä. Jos lisäät uuden työjonotapahtuman, jonka haluat ajoittaa, sinun on annettava joitakin tietoja. Esimerkki:
* Suoritettavan objektin tyyppi, kuten raportti tai codeunit. Sinulla on oltava oikeus suorittaa kulloinenkin raportti tai codeunit.
* Objektin nimi ja objektitunnus. 
* Parametrit, joilla määritetään työjonotapahtuman käytös. Voit esimerkiksi lisätä parametrin vain kirjattujen myyntitilausten lähettämistä varten. 
* Milloin ja kuinka usein työjonotapahtuma suoritetaan.

> [!IMPORTANT]  
> Jos käytät [!INCLUDE[prod_short](includes/prod_short.md)]in mukana toimitettuja pääkäyttöoikeusjoukkoa, sinulla ja käyttäjillä oikeudet suorittaa kaikki lisenssiin kuuluvat objektit. Tämä ei edelleenkään riitä delegoidulle järjestelmänvalvolle tai käyttäjille, joilla on laitekäyttöoikeus ja jotka eivät voi luoda työjonotapahtumia.

Kun työjonot on määritetty ja käytössä, tila voi muuttua seuraavasti kunkin toistuvan jakson aikana:

* **Estossa**  
* **Valmis**  
* **Työn alla**  
* **Virhe**  
* **Valmis**  

Kun työ on valmis, se poistetaan työjonotapahtumien luettelosta, ellei se ole toistuva työ. Toistuvien töiden yhteydessä **Aloituspvm ja -aika** -kentän arvo muokataan näyttämään seuraava aika, jolloin työ odotetaan suoritettavan.  

## <a name="monitor-status-or-errors-in-the-job-queue"></a>Työjonon tilan tai virheiden seuraaminen

Työnjonon luomat tiedot tallennetaan tietokantaan, jotta voit tehdä työjonon virheiden vianmäärityksen.  

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
> Voit myös tarkastella työjonotapahtumien tilaa käyttämällä Microsoft Azuren Application Insightsin telemetriaan perustuvaa analyysia. Lisätietoja on kohdassa [Telemetrian seuranta ja analysointi](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) sekä [Työjonon elinkaaren jäljitystelemetrian analysointi](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) [!INCLUDE [prod_short](includes/prod_short.md)] kehittäjän ja hallinnan sisällössä.

## <a name="view-scheduled-tasks"></a>Näytä ajoitetut tehtävät

**Ajoitetut tehtävät** -sivulla [!INCLUDE [prod_short](includes/prod_short.md)]issa näkyy, mitkä tehtävät ovat valmiita suoritettaviksi työjonossa. Sivulla näkyy myös tietoja yrityksestä, jossa kukin tehtävä on määritetty suoritettavaksi. Kuitenkin vain tehtävät, jotka on merkitty kuuluvaksi nykyiseen ympäristöön, voivat toimia.  

Esimerkiksi kaikki suunnitellut tehtävät pysäytetään, jos yritys on ympäristössä, joka on toisen ympäristön kopio. **Ajoitetut tehtävät** -sivulla voit määrittää tehtävät valmiiksi suoritettaviksi työjonossa.  

> [!NOTE]
> Sisäiset järjestelmänvalvojat ja käyttäjät voivat ajoittaa tehtäviä suoritettavaksi. Delegoidut järjestelmänvalvojat eivät voi.

## <a name="the-my-job-queue-part"></a>Oma työjono -osa

Roolikeskuksen **Oma työjono** -osa sisältää työjonotapahtumat, jotka olet aloittanut mutta jotka eivät ole vielä valmiita. Oletusarvoisesti osa ei ole näkyvissä, mutta voit lisätä sen omaan roolikeskukseesi. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).  

Osassa näkyvät seuraavat tiedot:

* Mitä asiakirjoja, joissa on tunnuksesi **Määritetty käyttäjätunnus** -kentässä, käsitellään tai mitkä ovat jonossa, mukaan lukien asiakirjat, jotka kirjataan taustalla. 
* Onko asiakirjan kirjaamisessa tai työjonotapahtumassa ilmennyt virhe. 

Oma työjono -osan avulla voit myös peruuttaa asiakirjan kirjaamisen.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Tarkastele virhettä oma työjono -osasta

1. Valitse tapahtumassa, jonka tila on **Virhe**, **Näytä virhe** -toiminto.
2. Tarkastele virhesanomaa ja korjaa ongelma.

## <a name="examples-of-what-can-be-scheduled-using-job-queue"></a>Esimerkkejä siitä, mitä voidaan ajoittaa työjonon avulla

### <a name="schedule-reports"></a>Ajoita raportteja

Voit aikatauluttaa raportin tai erätyön ajon tietylle päivämäärälle ja kellonajalle. Aikataulutetut raportit ja erätyöt syötetään työjonoon ja käsitellään aikataulutettuna aikana vastaavasti kuin muut työt. **Aikataulu**-asetus valitaan sen jälkeen, kun **Lähetä kohteeseen** -toiminto on valittu, minkä jälkeen annetaan tiedot, kuten tulostin sekä päivämäärä ja kellonaika tai toistuvuus.  

Lisätietoja on kohdassa [Raportin ajoittaminen suoritettavaksi](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between-prod_short-and-prod_short"></a>Synkronoinnin aikatauluttaminen [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[prod_short](includes/cds_long_md.md)]n välillä

Jos olet integroinut tuotteen [!INCLUDE[prod_short](includes/prod_short.md)] tuotteeseen [!INCLUDE[prod_short](includes/cds_long_md.md)], työjono mahdollistaa tietojen synkronoinnin ajoittamisen. Määrittämiesi suunnan ja sääntöjen mukaan työjonotapahtuma voi luoda yhdessä sovelluksessa toisen sovelluksen tietueita vastaavia tietueita. Hyvä esimerkki on yhteyshenkilön rekisteröiminen tuotteessa [!INCLUDE[crm_md](includes/crm_md.md)], jolloin työjonotapahtuma voi määrittää kyseissen yhteyshenkilön tuotteessa [!INCLUDE[prod_short](includes/prod_short.md)]. Lisätietoja on kohdassa [Business Centralin ja Dynamics 365 Salesin synkronoinnin ajoittaminen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)

### <a name="schedule-the-posting-of-sales-and-purchase-orders"></a>Ajoita myynti- ja ostotilausten kirjaus

Työjonotapahtumien avulla voit ajoittaa liiketoimintaprosesseja suoritettavaksi taustalla. Taustatehtävät voivat olla hyödyllisiä esimerkiksi, kun useat käyttäjät kirjaavat myyntitilauksia samanaikaisesti, mutta käsittelyssä voi olla vain yksi tilaus kerrallaan. Lisätietoja on kohdassa [Taustakirjauksen määrittäminen työjonojen avulla](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## <a name="monitor-the-job-queue-with-telemetry"></a>Työjonon valvominen telemetrian avulla

Järjestelmänvalvojana voit [Application Insightsin](/azure/azure-monitor/app/app-insights-overview) avulla kerätä ja analysoida telemetriaa, jonka avulla voit tunnistaa ongelmia. Lisätietoja on kehittäjien ja järjestelmänvalvojien ohjeessa [Telemetrian seuranta ja analysoiminen](/dynamics365/business-central/dev-itpro/administration/telemetry-overview).  

## <a name="see-also"></a>Katso myös

[Hallinta](admin-setup-and-administration.md)  
[Business Central -sovelluksen määrittäminen](setup.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Työjonon elinkaaren jäljityksen telemetrian analysoiminen](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]