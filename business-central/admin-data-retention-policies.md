---
title: Tietojen puhdistaminen säilytyskäytäntöjen avulla | Microsoft Docs
description: Voit määrittää, kuinka usein haluat poistaa tietyntyyppiset tiedot.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delete, data, retention, policy, policies
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 52f99b262dbfa5568650b72356ec43442fc75284
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378521"
---
# <a name="define-retention-policies"></a>Määritä säilytyskäytännöt
Järjestelmänvalvojat voivat määrittää säilytyskäytäntöjä ja määrittää, kuinka usein he haluavat [!INCLUDE[prod_short](includes/prod_short.md)]:n poistavan vanhentuneita tietoja lokimerkintöjä ja arkistoituja tietueita sisältävissä taulukoissa. Esimerkiksi lokitapahtumien puhdistaminen voi helpottaa todella merkityksellisten tietojen käyttöä. Käytännöt voivat sisältää kaikki niiden taulukoiden tiedot, joiden vanhentumispäivämäärä on kulunut, tai voit lisätä suodatusehtoja, jotka sisältävät vain tietyt käytännön vanhentuneet tiedot. 

## <a name="required-setups-and-permissions"></a>Pakolliset määritykset ja käyttöoikeudet
Seuraavat on määritettävä, ennen kuin voit määrittää säilytyskäytäntöjä.

|Määritys  |Kuvaus  |
|---------|---------|
|**Sallitut taulukot**     |Tarjoamme luettelon taulukoista, jotka voidaan sisällyttää säilytyskäytäntöihin. Jos kuitenkin haluat lisätä taulukkoja laajennuksesta säilytyskäytäntöihin, kehittäjän on lisättävä taulukot luetteloon. Lisätietoja on kohdassa [Laajennuksen lisääminen säilytyskäytäntöihin](admin-data-retention-policies.md#including-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Säilytysjaksot**     |Määrittää ajanjaksot, joiden tiedot säilytetään käytännön taulukoissa. Jaksot määrittävät, kuinka usein tiedot poistetaan.         |

Lisäksi sinulla on oltava PÄÄKÄYTTÄJÄN käyttöoikeudet tai säilytyskäytännön asetukset -oikeusjoukko. Käyttäjät, joille on myönnetty säilytyskäytännön asetukset -asetus, voivat määrittää taulujen säilytyskäytäntöjä, vaikka heillä ei olisi kyseisten taulukoiden luku- ja poisto-oikeuksia. Työjonomerkintä on suoritettava käyttäjänä, jolla on oikeus lukea ja poistaa tietoja. Microsoft suosittelee, että et myönnä säilytyskäytännön määritysoikeuksia käyttäjille, joiden ei sallita poistaa tietoja.

> [!NOTE]
> Jos käytät [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaa paikallisesti ja haluat kokeilla säilytyskäytäntöjä Cronus-esittelytietokannassa, sinun täytyy tehdä muutamia asioita. Esittely-yritys ei sisällä sellaisia taulukoita, joita voi käyttää säilytyskäytäntöjen kanssa, joten ne on lisättävä. Luo uusi, tyhjä yritysesittely tietokantaan. Tuo uudessa yrityksessä oman maasi RapidStart -konfigurointi paketti, joka vastaa vakio-NAV17.0.W1.ENU.STANDARD.rapidstart-pakettia. Säilytyskäytäntöjen asetustiedot ovat käytettävissä uudessa yrityksessä.

### <a name="to-create-retention-periods"></a>Säilytyskausien luominen
Säilytysjaksot voivat olla niin pitkiä tai lyhyitä kuin haluat. Voit luoda säilytysaikoja käyttämällä **Säilytyskäytännöt**-sivulla **Säilytysaika**-toimintoa. Määrittämäsi jaksot ovat kaikkien käytäntöjen käytettävissä.

> [!NOTE]
> Yhteensopivuussyistä olemme määritelleet joillekin taulukoille vähimmäissäilyttämisajan. Jos asetat vähimmäispitoajan, joka on vähimmäisvaatimusta lyhyempi, näyttöön tulee pakollinen jakso.

### <a name="set-up-a-retention-policy"></a>Säilytyskäytännön määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Säilytyskäytännöt** ja valitse sitten liittyvä linkki.
2. Valitse **Taulukon tunnus** -kentässä taulukko, jonka haluat sisällyttää käytäntöön.
3. **Määrittele säilytysaika** -kentässä, kuinka kauan taulukon tiedot säilytetään.
4. Valinnainen: Jos haluat kohdistaa käytännön taulukon tiettyihin tietoihin, poista Käytä kaikissa tietueissa- vaihtoehto käytöstä. Näyttöön tulee Tietueiden säilytyskäytäntö -pikavälilehti, jossa voit määrittää suodattimia, kun haluat luoda tietojen alijoukkoja kullekin riville. Lisätietoja on kohdassa [Suodattaminen](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Kullakin rivillä on oma säilytysaika. Jos määrität eri säilytysaikoja samoille tiedoille, ohjelma käyttää pisintä ajanjaksoa. Jotkin taulukot sisältävät myös suodattimia, joita ei voi muuttaa tai poistaa. Näiden suodattimien tunnistamisen helpottamiseksi ne näkyvät vaaleampana fonttina.

## <a name="applying-retention-policies"></a>Säilytyskäytäntöjen ottaminen käyttöön
Työjonotapahtuman avulla voit kohdistaa säilytyskäytäntöjä tietojen automaattiseen poistamiseen tai voit kohdistaa käytäntöjä manuaalisesti.

Jos haluat käyttää säilytyskäytäntöjä automaattisesti, luo ja ota käyttöön käytäntö. Kun otat käyttöön käytännön, luomme työjonotapahtuman, joka ottaa säilytyskäytännöt käyttöön määrittämäsi säilytysajan mukaan. Kaikki säilytyskäytännöt käyttävät samaa työjonotapahtumaa. Oletusarvon mukaan työjonotapahtuma kohdistaa käytännön joka päivä klo 02.00. Voit muuttaa oletusarvoa, mutta jos et tee sitä, suosittelemme sen suorittamista aukioloaikojen ulkopuolella. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md). 

Voit kohdistaa käytännön manuaalisesti **Säilytyskäytännöt**-sivun **Käytä manuaalista toimintoa** -toiminnolla. Jos haluat käyttää käytäntöä aina manuaalisesti, ota **Manuaalinen** vaihto käyttöön. Työjonotapahtuma ohittaa käytännön, kun se suoritetaan.

## <a name="viewing-retention-policy-log-entries"></a>Säilytyskäytäntölokin tapahtumien tarkasteleminen
Voit tarkastella säilytyskäytäntöihin liittyviä toimintoja **Säilytyskäytäntöloki**-sivulla. Tapahtumat luodaan esimerkiksi silloin, kun käytäntö otetaan käyttöön, tai jos tapahtui virheitä. 

## <a name="including-your-extension-in-a-retention-policy-requires-help-from-a-developer"></a>Laajennuksen käyttäminen säilytyskäytännön mukaan (edellyttää kehittäjän apua)
Säilytyskäytännöt kattavat oletusarvoisesti vain taulukot, jotka sisältyvät [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman tarjoamiin taulukoihin. Voit poistaa oletustaulukot luettelosta ja voit lisätä omistamiasi taulukoita. Et siis voi lisätä taulukkoa, jota et itse luonut. Et voi esimerkiksi lisätä muita taulukoita [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmasta tai ostamastasi laajennuksesta.

Jotta voisit lisätä taulukot sallittujen taulukoiden luetteloon, kehittäjän on lisättävä koodia esimerkiksi laajennuksen asennusohjelman codeunitia varten (codeunit, jossa on *asenna*-alatyyppi). 

Kun kehittäjä lisää taulukon, hän voi määrittää pakollisia ja oletussuodattimia. Pakollisia suodattimia ei voi poistaa tai muuttaa myöhemmin, kun taulukoita lisätään säilytyskäytännön määrittämistä varten. Oletussuodattimet ovat vain ystävällisiä ehdotuksia.

Seuraavassa on esimerkkejä siitä, kuinka voit lisätä taulukon sallittujen taulukoiden luetteloon pakollisten- tai oletussuodattimien avulla ja ilman niitä. Monimutkaisempaa esimerkkiä varten katso codeunit 3999 "Reten. Pol. Install-BaseApp". 

```
 trigger OnInstallAppPerCompany()
    var
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
    begin
        RetenPolAllowedTables.AddAllowedTable(Database::"Retention Policy Log Entry");
    end;
```

Seuraavassa esimerkissä on pakollinen suodatin.

```
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
[Business Centralin tilintarkastuksen muutokset](across-log-changes.md)  
[Suodattaminen](ui-enter-criteria-filters.md#filtering)  
[Työjonojen käyttäminen ajoitustehtäviin](admin-job-queues-schedule-tasks.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]