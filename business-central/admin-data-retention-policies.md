---
title: Tietojen puhdistaminen säilytyskäytäntöjen avulla
description: 'Voit määrittää, kuinka usein haluat poistaa tietyntyyppiset tiedot.'
author: brentholtorf
ms.topic: conceptual
ms.author: bholtorf
ms.search.keywords: 'delete, data, retention, policy, policies'
ms.search.form: '3903, 3901'
ms.date: 12/15/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="define-retention-policies"></a>Määritä säilytyskäytännöt

Tämä artikkeli kuvaa, miten Järjestelmänvalvojat voivat määrittää säilytyskäytäntöjä ja määrittää, kuinka usein vanhentuneita tietoja poistetaan lokimerkintöjä ja arkistoituja tietueita sisältävistä taulukoista. Esimerkiksi lokitapahtumien puhdistaminen voi helpottaa merkityksellisempien tietojen käyttöä. Käytännöt voivat poistaa tietoja vanhenemispäivän perusteella tai voit lisätä suodattimia, jotka sisältävät vain tietyt vanhentuneet tiedot.

## <a name="required-setups-and-permissions"></a>Pakolliset määritykset ja käyttöoikeudet

Ennen kuin voit luoda säilytyskäytäntöjä, sinun on määritettävä sisällytettävät taulukot ja ajat säilyttääksesi tiedot.

|Asennus  |Kuvaus  |
|---------|---------|
|**Sallitut taulukot**     |Tarjoamme luettelon taulukoista, jotka voit sisällyttää säilytyskäytäntöihin. Jos haluat lisätä taulukkoja laajennuksesta säilytyskäytäntöihin, kehittäjän on lisättävä taulukot luetteloon. Lue lisätietoja kohdasta [Laajennuksen lisääminen säilytyskäytäntöihin](admin-data-retention-policies.md#include-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Säilytysjaksot**     |Määrittää ajanjaksot, joiden tiedot säilytetään käytännön taulukoissa. Jaksot määrittävät, kuinka usein tiedot poistetaan.         |

Lisäksi sinulla on oltava **PÄÄKÄYTTÄJÄN** käyttöoikeudet tai **säilytyskäytännön asetukset** -oikeusjoukko. Käyttäjät, joilla on säilytyskäytännön asetukset, voivat määrittää taulukoille säilytyskäytännöt. Se on totta, vaikka heillä ei olisi taulukoiden luku- ja poisto-oikeuksia. Työjonomerkintä on suoritettava käyttäjänä, jolla on oikeus lukea ja poistaa tietoja. Älä myönnä säilytyskäytännön määritysoikeuksia käyttäjille, joiden ei sallita poistaa tietoja.

> [!NOTE]
> Jos käytät [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaa paikallisesti ja haluat kokeilla säilytyskäytäntöjä Cronus-esittelytietokannassa, sinun täytyy tehdä muutamia asioita. Esittely-yritys ei sisällä sellaisia taulukoita, joita voi käyttää säilytyskäytäntöjen kanssa, joten ne on lisättävä. Luo uusi, tyhjä yritysesittely tietokantaan. Tuo uudessa yrityksessä oman maasi tai alueesi RapidStart -konfigurointi paketti, joka vastaa vakio-NAV17.0.W1.ENU.STANDARD.rapidstart-pakettia. Säilytyskäytäntöjen asetustiedot ovat käytettävissä uudessa yrityksessä.

### <a name="create-retention-periods"></a>Säilytyskausien luominen

Säilytysjaksot voivat olla niin pitkiä tai lyhyitä kuin haluat. Voit luoda säilytysaikoja käyttämällä **Säilytyskäytännöt**-sivulla **Säilytysaika**-toimintoa. Määrittämäsi jaksot ovat kaikkien käytäntöjen käytettävissä.

> [!NOTE]
> Yhteensopivuussyistä olemme määritelleet joillekin taulukoille vähimmäissäilyttämisajan. Jos asetat vähimmäispitoajan, joka on vähimmäisvaatimusta lyhyempi, näyttöön tulee pakollinen jakso.

### <a name="set-up-a-retention-policy"></a>Säilytyskäytännön määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Säilytyskäytännöt** ja valitse sitten vastaava linkki.
2. Valitse **Taulukon tunnus** -kentässä taulukko, jonka haluat sisällyttää käytäntöön.
3. **Määrittele säilytysaika** -kentässä, kuinka kauan taulukon tiedot säilytetään.
4. Valinnainen: Voit soveltaa käytäntöä tiettyihin taulukon tietoihin kaikkien tietueiden sijaan suodattamalla kunkin rivin tiedot. Käytäntö koskee vain tietueita, jotka suodattimet palauttavat. Määritä suodatusehdot poistamalla **Käytä kaikkiin tietueisiin** -valitsin. Näkyviin tulee **tietueiden säilytyskäytäntö** -pikavälilehti, jossa voit asettaa suodatusehtoja. Saat lisätietoja suodattimien toiminnasta siirtymällä kohtaan [Suodattaminen](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Kullakin rivillä on oma säilytysaika. Jos määrität eri säilytysaikoja samoille tiedoille, ohjelma käyttää pisintä ajanjaksoa. Jotkin taulukot sisältävät myös suodattimia, joita ei voi muuttaa tai poistaa. Näiden suodattimien tunnistamisen helpottamiseksi ne näkyvät vaaleampana fonttina.

#### <a name="video-guidance"></a>Video-opastus

Tässä videossa on esimerkki säilytyskäytännön määrittämisestä.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1fLeJ]

## <a name="apply-retention-policies"></a>Säilytyskäytäntöjen ottaminen käyttöön

Työjonotapahtuman avulla voit kohdistaa säilytyskäytäntöjä tietojen automaattiseen poistamiseen tai voit kohdistaa käytäntöjä manuaalisesti.

Jos haluat käyttää säilytyskäytäntöjä automaattisesti, luo ja ota käyttöön käytäntö. Kun otat käyttöön käytännön, [!INCLUDE [prod_short](includes/prod_short.md)] luo työjonotapahtuman, joka käyttää sitä sen säilytysajan mukaan. Kaikki säilytyskäytännöt käyttävät samaa työjonotapahtumaa. Oletusarvon mukaan työjonotapahtuma kohdistaa käytännön joka päivä klo 02.00. Voit muuttaa oletusarvoa, mutta jos et tee sitä, suosittelemme sen suorittamista aukioloaikojen ulkopuolella. Lue lisätietoja kohdasta [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md). 

Voit kohdistaa käytännön manuaalisesti **Säilytyskäytännöt**-sivun **Käytä manuaalista toimintoa** -toiminnolla. Jos haluat käyttää käytäntöä aina manuaalisesti, ota **Manuaalinen** vaihto käyttöön. Työjonotapahtuma ohittaa käytännön, kun se suoritetaan.

## <a name="view-retention-policy-log-entries"></a>Säilytyskäytäntölokin tapahtumien tarkasteleminen

Voit tarkastella säilytyskäytäntöihin liittyviä toimintoja **Säilytyskäytäntöloki**-sivulla. Tapahtumat luodaan esimerkiksi silloin, kun käytäntö otetaan käyttöön, tai jos tapahtui virheitä.

## <a name="include-your-extension-in-a-retention-policy-requires-help-from-a-developer"></a>Laajennuksen käyttäminen säilytyskäytännön mukaan (edellyttää kehittäjän apua)

Säilytyskäytännöt kattavat oletuksena vain [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman toimittamassamme luettelossa. Voit poistaa oletustaulukot luettelosta ja voit lisätä omistamiasi taulukoita. Et siis voi lisätä taulukkoa, jota et itse luonut. Et voi esimerkiksi lisätä muita taulukoita [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmasta tai ostamastasi laajennuksesta.

Jos haluat lisätä taulukosi sallittujen taulukkojen luetteloon, kehittäjän on lisättävä koodi. Esimerkiksi laajennuksen asennusohjelman codeunitiin (codeunit, jonka alatyyppi on *asenna* ).

Kun kehittäjä lisää taulukon, hän voi määrittää pakollisia ja oletussuodattimia. Pakollisia suodattimia ei voi poistaa tai muuttaa myöhemmin, kun taulukoita lisätään säilytyskäytännön määrittämistä varten. Oletussuodattimet ovat vain ehdotuksia.

Seuraavassa on esimerkkejä siitä, kuinka voit lisätä taulukon sallittujen taulukoiden luetteloon pakollisten- tai oletussuodattimien avulla ja ilman niitä. Monimutkaisempaa esimerkkiä varten katso codeunit 3999 "Reten. Käyt. Install-BaseApp".

```al
 trigger OnInstallAppPerCompany()
    var
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
    begin
        RetenPolAllowedTables.AddAllowedTable(Database::"Retention Policy Log Entry");
    end;
```

Seuraavassa esimerkissä on pakollinen suodatin.

```al
 trigger OnInstallAppPerCompany()
    var
        ChangeLogEntry: Record "Change Log Entry";
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
        RetentionPeriod: Enum "Retention Period Enum";
        RecRef: RecordRef;
        TableFilters: JsonArray;
        Enabled: Boolean;
        Mandatory: Boolean;
    begin
        ChangeLogEntry.Reset();
        ChangeLogEntry.SetFilter("Field Log Entry Feature", '%1|%2', ChangeLogEntry."Field Log Entry Feature"::"Monitor Sensitive Fields", ChangeLogEntry."Field Log Entry Feature"::All);
        RecRef.GetTable(ChangeLogEntry);
        Enabled := true;
        Mandatory := true;
        RetenPolAllowedTables.AddTableFilterToJsonArray(TableFilters, RetentionPeriod::"28 Days", ChangeLogEntry.FieldNo(SystemCreatedAt), Enabled, Mandatory, RecRef);
        RetenPolAllowedTables.AddAllowedTable(Database::"Change Log Entry", ChangeLogEntry.FieldNo(SystemCreatedAt), TableFilters);
    end;
```

Kun kehittäjä on lisännyt taulukoita luetteloon, järjestelmänvalvoja voi sisällyttää ne säilytyskäytäntöihin. 

## <a name="see-also"></a>Katso myös

[Säilytyskäytännön jäljityksen telemetrian analysoiminen](/dynamics365/business-central/dev-itpro/administration/telemetry-retention-policy-trace)  
[Business Centralin tilintarkastuksen muutokset](across-log-changes.md)  
[Suodattaminen](ui-enter-criteria-filters.md#filtering)  
[Työjonojen käyttäminen ajoitustehtäviin](admin-job-queues-schedule-tasks.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
