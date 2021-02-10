---
title: Töiden aikatauluttaminen automaattisesti suoritettavaksi
description: Ajoitettuja tehtäviä hallitaan työjonon avulla. Näillä töillä suoritetaan raportteja ja codeuniteja. Voit määrittää töitä suoritettavaksi yhtä aikaa tai toistuvasti.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/12/2021
ms.author: edupont
ms.openlocfilehash: 29b5b3f633b0fd9fcac648f0bf7149b87ae0b20d
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013944"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Käytä työjonoja ajoitustehtäviin

[!INCLUDE[prod_short](includes/prod_short.md)]in työjonojen avulla käyttäjät voivat ajoittaa ja suorittaa tiettyjä raportteja ja codeuniteja. Voit määrittää töitä suoritettavaksi yhtä aikaa tai toistuvasti. Voit esimerkiksi haluta suorittaa **Myyjän myyntitilasto** -raportin viikoittain ja seurata näin myyjäkohtaista viikkomyynti. Vaihtoehtoisesti voit suorittaa **Delegoi hyväksymispyynnöt** -codeunitin päivittäin, jolloin asiakirjoja ei kasaudu odottamaan käsittelyä tai estämään muutoin työnkulkua.

**Työjonon tapahtumat** -sivulla on luettelo kaikista aiemmin luoduista töistä. Jos lisäät uuden aikataulutettavan työjonotapahtuman tiedot, sinun on ilmoitettava minkä tyyppisen objektin, kuten raportin tai codeunitin, haluat suorittaa, sekä suoritettavan objektin nimen ja tunnuksen. Voit myös lisätä parametrit, joilla määritetään työjonotapahtuman käytös. Voit esimerkiksi lisätä parametrin vain kirjattujen myyntitilausten lähettämistä varten. Sinulla tulee olla tietyn raportin tai codeunitin suoritusoikeus tai muutoin järjestelmä palauttaa virheen, kun työjonoa suoritetaan.  
> [!IMPORTANT]  
> Jos käytät [!INCLUDE[prod_short](includes/prod_short.md)]in mukana toimitettuja pääkäyttöoikeusjoukkoa, sinulla ja käyttäjillä oikeudet suorittaa kaikki lisenssiin kuuluvat objektit. Tämä ei edelleenkään riitä delegoidulle järjestelmänvalvolle tai käyttäjille, joilla on laitekäyttöoikeus ja jotka eivät voi luoda työjonotapahtumia.

Työjonossa voi olla useita tapahtumia, jotka ovat jonossa hallittavia ja suoritettavia töitä. Tapahtuman tiedot määrittävät, mikä codeunit tai raportti suoritetaan, milloin ja miten usein tapahtuma suoritetaan, missä luokassa työ suoritetaan ja miten se suoritetaan.  

Kun työjonot on määritetty ja käytössä, tila voi muuttua seuraavasti kunkin toistuvan jakson aikana:

* **Estossa**  
* **Valmis**  
* **Työn alla**  
* **Virhe**  
* **Valmis**  

Kun työ on valmis, se poistetaan työjonotapahtumien luettelosta, ellei se ole toistuva työ. Jos kyseessä on toistuva työ, **Aloituspvm ja -aika** -kentän arvo muokataan näyttämään seuraava aika, jolloin työ odotetaan suoritettavan.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Työjonon tilan tai virheiden näyttäminen

Työnjonon suorituksen aikana luotavat tiedot tallennetaan tietokantaan, jotta voit tehdä työjonon virheiden vianmäärityksen.  
Voit tarkastella ja muuttaa kunkin työjonotapahtuman tilaa. Kun luot työjonotapahtuman, sen tilaksi tulee **Estossa**. Voit määrittää tilaksi esimerkiksi **Valmis** ja takaisin tilaksi **Estossa**. Muuten tilatiedot päivitetään automaattisesti.

Seuraavassa taulukossa kuvataan **Tila**-kentän arvot.

| Tila | Kuvaus |
|--|--|
| Valmis | Ilmaisee, että työjonotapahtuma on valmis suoritettavaksi. |
| Työn alla | Ilmaisee, että työjonotapahtuma on keskeneräinen. Tämä kenttä päivitetään, kun työjonoa suoritetaan. |
| Estossa | Oletus. Ilmaisee työjonotapahtuman tilan, kun se luodaan. Valitse **Aseta tilaksi valmis** -toiminto, jotta tilaksi muuttuu **Valmis**. Valitse **Määritä pitoon**- tai **Keskeytä**-toiminto, jos haluat muuttaa tilaksi takaisin **Pidossa**. |
| Virhe | Ilmaisee, että on ilmennyt virhe. Valitse **Näytä virhe**, niin näyttöön tulee virhesanoma. |
| Valmis | Ilmaisee, että työjonotapahtuma valmis. |

### <a name="to-view-status-for-any-job"></a>Minkä tahansa työn tilan näyttäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Työjonotapahtumat** ja valitse sitten liittyvä linkki.
2. Valitse **Työjonotapahtumat**-sivulla ensin työjonotapahtuma ja sitten **Lokitapahtumat**-toiminto.  

> [!TIP]
> [!INCLUDE [prod_short](includes/prod_short.md)] onlinessa voit tarkastella työjonotapahtumien tilaa myös Microsoft Azuren Application Insightsissa. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeessa [Työjonon elinkaaren jäljityksen telemetrian analysoiminen](/dynamics365smb-devitpro\dev-itpro\administration\telemetry-job-queue-lifecycle-trace)[!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="the-my-job-queue-part"></a>Oma työjono -osa
Roolikeskuksen **Oma työjono** -osa sisältää työjonotapahtumat, jotka olet aloittanut mutta jotka eivät ole vielä valmiita. Oletusarvoisesti osa ei ole näkyvissä, joten se on lisättävä omaan roolikeskukseesi. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).  

Tässä osassa näkee, mitä asiakirjoja, joissa on tunnuksesi **Määritetty käyttäjätunnus** -kentässä, käsitellään tai mitkä ovat jonossa, mukaan lukien taustakirjaukseen liittyvät asiakirjat. Osa tietää yhdellä silmäyksellä, onko asiakirjan kirjaamisessa tai työjonon tapahtumissa tapahtunut virheitä. Osan avulla voit peruuttaa kun asiakirjan kirjaamisen, jos se ei ole käynnissä.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Tarkastele virhettä oma työjono -osasta
1. Valitse tapahtumassa, jonka tila on **Virhe**, **Näytä virhe** -toiminto.
2. Tarkastele virhesanomaa ja korjaa ongelma.


## <a name="examples-of-what-can-be-scheduled-using-job-queue"></a>Esimerkkejä siitä, mitä voidaan ajoittaa työjonon avulla

### <a name="schedule-reports"></a>Ajoita raportteja

Voit aikatauluttaa raportin tai erätyön ajon tietylle päivämäärälle ja kellonajalle. Aikataulutetut raportit ja erätyöt syötetään työjonoon ja käsitellään aikataulutettuna aikana vastaavasti kuin muut työt. **Aikataulu**-asetus valitaan sen jälkeen, kun **Lähetä kohteeseen** -toiminto on valittu, minkä jälkeen annetaan tiedot, kuten tulostin sekä päivämäärä ja kellonaika tai toistuvuus.  

Lisätietoja on kohdassa [Raportin ajoittaminen suoritettavaksi](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between-prod_short-and-prod_short"></a>Synkronoinnin aikatauluttaminen [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[prod_short](includes/cds_long_md.md)]n välillä

Jos [!INCLUDE[prod_short](includes/prod_short.md)] ja [!INCLUDE[prod_short](includes/cds_long_md.md)] on integroitu, voit ajoittaa työjonon avulla, milloin haluat synkronoida näiden kahden liiketoimintasovelluksen tietueiden tiedot. Integroinnille määritetyn suunnan ja sääntöjen mukaan synkronointityöt voivat myös luoda uusia tietueita kohdesovellukseen, jotta ne vastaavat lähdetietoja. Jos myyjä esimerkiksi luo uuden kontaktin [!INCLUDE[crm_md](includes/crm_md.md)]-ohjelmassa, synkronointityö voi luoda kontaktin linkitertylle myyjälle [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa. Lisätietoja on kohdassa [Business Centralin ja Dynamics 365 Salesin synkronoinnin ajoittaminen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)

### <a name="schedule-the-posting-of-sales-and-purchase-orders"></a>Ajoita myynti- ja ostotilausten kirjaus

Työjonot ovat tehokas työkalu taustalla suoritettavien liiketoimintaprosessien ajoittamiseen. Kyse voi olla esimerkiksi useista käyttäjistä, jotka yrittävät kirjata myyntitilauksia, kun vain yksi tilaus voidaan käsitellä kerralla.  

Lisätietoja on kohdassa [Taustakirjauksen määrittäminen työjonojen avulla](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## <a name="see-also"></a>Katso myös

[Hallinta](admin-setup-and-administration.md)  
[Business Central -sovelluksen määrittäminen](setup.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Työjonon elinkaaren jäljityksen telemetrian analysoiminen](/dynamics365smb-devitpro\dev-itpro\administration\telemetry-job-queue-lifecycle-trace)  
