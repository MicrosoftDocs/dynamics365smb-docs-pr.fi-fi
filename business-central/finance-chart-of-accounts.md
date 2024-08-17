---
title: Tilikartan ymmärtäminen
description: 'Tilikartan kuvaus, sen määrittäminen ja käyttötapa.'
author: kennienp
ms.topic: conceptual
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 08/06/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="understanding-the-chart-of-accounts"></a>Tilikartan ymmärtäminen

Tilikartta (COA) toimii rahoitustilien ja niitä vastaavien viitenumeroiden kattavana hakemistona. COA:ssa on yleensä kaksi tililuokkaa:

- Tasetilit: Nämä tilit seuraavat yrityksen resursseja, velkoja ja nettoarvoa.
- Tuloslaskelmatilit: Nämä tilit tallentavat tuloja eri lähteistä ja seuraavat myös kuluja.

Tasetilit luokitellaan edelleen kolmeen ryhmään:

1. Käyttöomaisuustilit: Näillä tileillä seurataan kaikkia yrityksesi omistamia arvokkaita resursseja.
1. Velkatilit: Ne tallentavat yrityksesi velat.
1. Pääomatilit: Kuvaa liiketoiminnan jäännösarvoa vähennettyään velat resursseista.

Tulotilit on jaettu kahteen ryhmään:

1. Tuottotilit: Nämä tilit tallentavat yrityksen tulot eri lähteistä.
1. Kustannustilit: Nämä tilit tallentavat kaikki yrityksesi kulut.

Käytä COA:a tallentaaksesi kauppatapahtumia organisaatiosi pääkirjanpitoon. Jokaisella tilillä on yleensä tunnus (tilinumero) ja kuvaava otsikko, ja ne koodataan systemaattisesti tilityypin perusteella.

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää tilikartan, joka on valmis tukemaan liiketoimintaasi.

Yrityksesi tilikartan kokoonpano on johdon tekemä strateginen päätös (tai maakohtaisen sääntelyn mukaan). Se vaihtelee yrityksesi toimialan, liiketoimintamallin ja rahoitusrakenteen mukaan. Toimialan mukaan sinulla voi esimerkiksi olla tiettyjä käyttöomaisuustilejä, jotka on räätälöity yrityksesi yksilöllisten toimintojen ja tarpeiden mukaan:

* Vähittäiskauppa voi korostaa varastoa ja myyntisaatavia.
* Teknologiayritys voisi keskittyä aineettomaan omaisuuteen, kuten patentteihin ja ohjelmistoihin.
* Tuotantolaitos seuraisi käyttöomaisuutta ja toimituksia.

## <a name="the-chart-of-accounts-page"></a>Tilikartta-sivu

Kaikki pääkirjanpidon tilit näkyvät tilikartassa. Tilikartassa voi tehdä esimerkiksi seuraavia toimintoja:  

* Voit tarkastella pääkirjanpitotapahtumat- ja saldot näyttäviä raportteja.  
* Voit sulkea tuloslaskelman.  
* Avaa pääkirjanpitotilikortti asetusten lisäämistä tai muuttamista varten.  
* Voit tarkastella luetteloa kyseisen tilin kirjausryhmistä.
* Yhden tilin erillisten debet- ja kreditsaldojen näyttäminen.

Voit lisätä, muuttaa tai poistaa pääkirjanpidon tilejä. Ristiriitojen estämiseksi et voi kuitenkaan poistaa pääkirjanpidon tiliä, jos sen tietoja käytetään tilikartassa. Voit myös estää tilien tahattoman poistamisen arkaluonteisissa jaksoissa. Lisätietoja tilien suojaamisesta poistolta on kohdassa [Tilien poisto](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="the-code-hierarchy-in-gl-accounts"></a>Koodihierarkia KP-tileillä

Yritykset luovat tyypillisesti hierarkkisen rakenteen KP-tilin koodeissa, jotta se heijastaa, mihin ne kuuluvat tilin luettelossa. Esimerkiksi joissakin täytäntöönpanoissa KP-tilien koodit, jotka alkavat numerosta **1**, viittaavat käyttöomaisuustileihin, kun taas KP-tilien koodit, jotka alkavat numerosta 3, viittaavat pääomatileihin. Joillakin alueilla on paikallisia sääntöjä vakiotilikartan käytöstä. Voit auttaa käyttäjiä ymmärtämään tätä hierarkiaa ilman sisäistä koodirakennetta määrittämällä tilikartassa otsikoita ja välisummia, jotka kapseloivat nämä sisäiset rakenteet.

## <a name="designing-your-chart-of-accounts"></a>Oman tilikartan rakentaminen

Kukin tilikauden rivi on yksi seuraavan tyyppisistä KP-tileistä:

* Kirjaus (päiväkirjat voivat kirjata rivejä näille tileille)
* Otsikko (määrittää tilikartan yleisotsikon)
* Yhteensä (määrittää laskukaavan välisummalle tilikartassa)
* Alkuperäinen saldo (määrittää aloitusotsikon välisummalle tilikartassa. Kaikki seuraavat rivit loppusummariviin asti sisennetään)
* Loppusumma (määrittää välisummalle loppuotsikon ja sen laskukaavan tilikartassa. Kaikki seuraavat rivit loppusummarivin jälkeen ulonnetaan)

Minimalistinen tilikartta voi koostua vain kirjaustilien riveistä. Neljän muun tyypin avulla voit määrittää, miten tilikartassa näkyy myös rahoituslaskelma, jossa on otsikot ja välisummat. Summaustilejä käytetään usein Financial Reportingissa.

> [!TIP]
> Jos käytät tilikartassasi muita tilityyppejä kuin **Kirjaus**, voit määrittää eri näkymiä, joissa näkyvät "raa'at" kirjaustilit, joilla ei ole raportointityyppistä tilityyppiä summaukselle ja otsikoille. Voit esimerkiksi näyttää vain kirjaustilit ja piilottaa suljettuja tilejä.

## <a name="use-dimensions-to-simplify-your-chart-of-accounts"></a>Dimensioiden käyttäminen tilikartan yksinkertaistamiseksi

Dimensiot ovat tapahtumia luokittelevia arvoja, jotta voit seurata ja analysoida tapahtumia asiakirjoissa, kuten myyntitilauksissa. Dimensioiden avulla voit esimerkiksi ilmaista, mistä projektista tai osastosta tapahtuma on lähtöisin. Sen sijaan, että määrittäisit kullekin osastolle ja projektille erilliset kirjanpitotilit, voit käyttää dimensioita analyysin perustana ja välttää monimutkaisen tilikartan luomisen.

Saat lisätietoja dimensioista siirtymällä kohtaan [Dimensioiden käyttäminen](finance-dimensions.md).

## <a name="get-a-quick-overview-of-your-finances"></a>Hanki nopea yleiskuva raha-asioistasi

**Tilikartat**-sivulla näkyvät hierarkkisessa luettelossa olevat tilit, jotka tarjoavat nopean pääsyn kunkin tilin avaintietoihin. Luettelo on kuitenkin staattinen, ja jos sinulla on paljon tilejä, sinun on ehkä vieritettävä nähdäksesi eri tilejä. Jos haluat vain nopean yleiskatsauksen perusasioista, kuten nettomuutoksista ja saldoista, **Tilikartan yleiskuvaus** -sivu on hyödyllinen vaihtoehto. Sivun sarakeasettelu on nyt sama kuin jonka löydät **tilikartta**-sivulta (vaikkakin vähemmillä sarakkeilla), joten se on helppo ymmärtää. Voit laajentaa tai kutistaa hierarkiatasoja. Jotta sivuja olisi helppo vaihtaa, **Tilikartan yleiskuvaus** -sivu on käytettävissä **Tilikartta**-sivulta.

## <a name="access-to-create-and-edit-the-chart-of-accounts"></a>Pääsy tilikartan luomiseen ja muokkaamiseen

Pienessä organisaatiossa, kuten CRONUS-esittely-yrityksessä, useimmat käyttäjät voivat muokata tilikarttaa lukuun ottamatta niitä käyttäjiä, joilla on TEAM MEMBER -käyttöoikeus. Suuremmissa organisaatioissa käytetään tyypillisesti rooleja ja käyttöoikeuksia rajoittamaan tilikartan muokkausoikeutta. Jos olet järjestelmänvalvoja tai sinulla on Liiketoimintajohtaja- tai Kirjanpitäjä-rooli, voit hallita käyttöoikeuksia antaaksesi oikeille käyttäjille oikeuden käyttää asianomaisia taulukoita. Lue lisätietoja kohdasta [Käyttäjän käyttöoikeuksien yleiskatsauksen hankkiminen](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).  


<!-- ## Standard chart of accounts in different regions
Uncomment when we have more examples added to our localization documentation

Some regions have defined standards for the chart of accounts structure you should use in your company. 

Here are some examples of such standards that have been implemented in localized versions of [!INCLUDE[prod_short](includes/prod_short.md)]:

* [Standard chart of accounts in Denmark](localfunctionality/denmark/how-to-set-up-standard-coa.md)
-->

## <a name="chart-of-accounts-best-practices"></a>Tilikartan parhaat käytännöt

Seuraavassa on joitakin parhaita toimintatapoja, joita kannattaa harkita tilikartan kehittämisessä ja ylläpidossa:

* Laadi yrityksesi tilikartta tukemaan talousraportointitarpeita, jotta hallinto voi tehdä strategisia päätöksiä.
* Harkitse yksinkertaista aloittamista vähemmillä KP-tileillä. Voit aina lisätä yksityiskohtaisempia tilejä tarvittaessa.
* Määritä tilikartan otsikot ja välisummat, joista on yhteenveto KP-tilien sisäisistä rakenteista.
* Dimensioiden käyttäminen tilikartan yksinkertaistamiseksi. Sinulla ei ole KP-tilejä kullekin tuotteelle tai osastolle.
* Lisää uusia KP-tilejä niiden edetessä, mutta poista tilit tilikartasta vain rahoitusjakson jakson lopussa.

## <a name="see-also"></a>Katso myös

[Tilikartan määrittäminen tai muuttaminen](finance-setup-chart-accounts.md)    
[Tietoja pääkirjanpidosta](finance-general-ledger.md)  
[Rahoitusanalytiikka](bi.md)    
[Talouden yleiskatsaus](finance.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
