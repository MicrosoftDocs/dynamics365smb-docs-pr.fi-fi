---
title: Pankkitilin täsmäytysavustaja (esiversio) Copilotin avulla - UKK
description: 'Tässä UKK:ssa on tietoa tekoälytekniikasta, jota käytetään pankkitilien ja tiliotteiden täsmäytykseen Business Centralissa. Siinä on tärkeitä seikkoja ja tietoja siitä, miten tekoälyä käytetään, miten sitä on testattu ja arvioitu, sekä tiettyjä rajoituksia.'
ms.date: 03/27/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI'
ms.collection:
  - bap-ai-copilot
---

# <a name="faq-for-bank-account-reconciliation-assist-with-copilot-preview"></a>Usein kysyttyjä kysymyksiä pankkitilin täsmäytysavustajasta Copilotin avulla (esiversio)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Nämä usein kysytyt kysymykset kuvaavat Copilot-avustajan tekoälyn vaikutusta pankkitilin täsmäytykseen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-bank-reconciliation-assist"></a>Mikä on pankkitilin täsmäytysavustaja?

Pankkitilin täsmäytys on yleinen kirjanpitotehtävä, jossa organisaatiot tarkistavat tiliotteensa ja tunnistavat kauppatapahtumat, jotka tulisi rekisteröidä [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. Tätä tehtävää käytetään esimerkiksi yksilöimään jaksoittaisia pankkimaksuja tai pieniä työntekijäkuluja. Tämä tehtävä on tyypillisesti monivaiheinen prosessi, joka alkaa tiliotteiden tuomisesta [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan, jota seuraa tapahtumien täsmäyttäminen pääkirjamerkintöjen kanssa ja uusien pääkirjamerkintöjen kirjaaminen vastaamaan mahdollisia jäljellä olevia tapahtumia, joita kirjanpitosi eivät aiemmin tienneet. Copilot [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa vähentää manuaalista työtä täsmäyttämällä useampia tapahtumia ja ehdottamalla kirjanpitotilejä, joihin voi kirjata. 

## <a name="what-are-capabilities-of-bank-reconciliation-assist"></a>Mitkä ovat pankkitilin täsmäytysavustajan valmiudet?

Copilotin avulla tekoälyä voi käyttää kahdessa erillisessä tehtävässä: 

- Tapahtumien ja kirjanpitotietojen yhteensovittamisen parantaminen 

   [!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa automaattisia sääntöjä, jotka vastaavat automaattisesti monia pankkitapahtumia ja kirjanpitotapahtumia. Nämä säännöt ovat kuitenkin joustamattomia, ja ne johtavat usein moniin vastaamattomiin tapahtumiin, joista jokainen edellyttää manuaalista tarkastusta ja vertailua. Copilot käyttää tekoälyteknologiaa, kun halutaan tarkastaa jäljellä olevat tapahtumat ja tunnistaa useampia vastaavuuksia päivämäärien, summien ja kuvausten perusteella. Jos asiakas esimerkiksi maksoi useita laskuja yhtenä kertakorvauksena, Copilot täsmäyttää yksittäisen tiliotteen rivin useiden laskutapahtumien kanssa. 
 
- Ehdotetut pääkirjanpitotilit 

   Jäljellä olevien pankkitapahtumien osalta, joita ei voida yhdistää mihinkään kirjanpitoon, Copilot käyttää tekoälyteknologiaa verratakseen tapahtumakuvausta KP-tilien nimiin ja ehdottaa todennäköisimpää KP-tiliä, jolle kirjataan. Copilot voi esimerkiksi ehdottaa, että narratiivisen "Bensa-asema 24" -tapahtuman tapahtuma kirjataan Kuljetus-tilille. 

Copilot ei muodosta yhteyttä pankkiisi noutaakseen tai lähettääkseen kauppatapahtumia. Tämä tehtävä on täysin sinun hallinnassasi, ja se on edellytys Copilotin avustajan käyttämiselle riippumatta siitä, lisätäänkö kyseiset tapahtumat [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan digitaalisen pankkiyhteyden avulla, tuomalla tiliotetiedostosta tai syöttämällä manuaalisesti. 

## <a name="what-is-the-intended-use-of-bank-reconciliation-assist"></a>Mitä pankkitilin täsmäytysavustajaa aiotaan käyttää?

Pankkitilin täsmäytysavustaja on suunniteltu auttamaan tunnistamaan uusia kauppatapahtumia, joista asiakkaiden tulisi ottaa huomioon [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa, jotta heidän kirjaustensa tarkkuus paranee. Tätä toimintoa ei ole tarkoitettu petosten havaitsemiseen tai sen tunnistamiseen ovatko asiakkaat maksaneet ajoissa.   

## <a name="how-was-bank-reconciliation-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Miten pankkitilin täsmäytysavustaja arvioitiin? Mitä mittareita suorituskyvyn mittaamiseen käytetään?

Tämä toiminto testattiin käyttämällä synteettisten pankkitapahtumatietojen ja vastaavien KP-tilien ja tapahtumien yhdistelmiä, jotka kattavat tavalliset vaihtelut ja datarajat kunkin kentän osalta sekä eri kielillä. Testitiedot kuvaavat sekä huonojen toimijoiden tavallista käyttöä että käyttöä. Suorituskykyä verrattiin samojen tietojen manuaaliseen täsmäytykseen. 

## <a name="what-are-the-limitations-of-bank-reconciliation-assist-how-can-users-minimize-the-impact-of-the-bank-reconciliation-limitations-when-using-the-system"></a>Mitkä ovat pankkitilin täsmäytysavustajan rajoitukset? Miten käyttäjät voivat minimoida pankkitilin täsmäytyksen rajoitukset, kun he käyttävät järjestelmää?

Pankkitilin täsmäytysavustaja toimii parhaiten, kun KP-tilien nimet, tapahtumakuvaukset ja pankin kauppatapahtumien kuvaukset ovat kaikki samalla kielellä. Sekoitetuilla kielillä tai transaktioiden kuvausten sekoitetuilla kielillä saadaan usein vähemmän vastauksia ja ehdotuksia. 

Ehdotetut kirjanpitotilit toimivat parhaiten englannin kielellä. Vaikka tätä ominaisuutta voidaan käyttää millä tahansa käytettävissä olevista [!INCLUDE[prod_short](includes/prod_short.md)] -kielistä, käyttäjät saattavat kokea vähemmän tapahtumien osumia ja harvemmin ehdotettuja pääkirjatilejä muilla kielillä. 
<!--

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>What operational factors and settings allow for effective and responsible use of the feature?


-->
## <a name="in-which-geographies-and-languages-is-bank-reconciliation-assist-available"></a>Millä maantieteellisillä alueilla ja kielillä pankkitilin täsmäytysavustaja on saatavilla?

Tämä ominaisuus on käytettävissä kaikissa ympäristöissä, maa- tai aluelokalisoinnissa ja millä tahansa käyttäjän kielellä. Asiakasympäristöissä, jotka sijaitsevat maissa tai alueilla, joissa Azure OpenAI Serviceä ei ole otettu käytöön, järjestelmänvalvojien on ensin annettava hyväksyntänsä tietojen siirtämiselle rajojen yli [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa, jotta he voivat muodostaa yhteyden Azure OpenAI Serviceen ja jotta tämä ominaisuus on käytettävissä. 

Lisätietoja kielestä on aiemmassa rajoituskysymyksessä.  

## <a name="what-is-expected-of-end-users-when-operating-bank-account-reconciliation-assist"></a>Mitä loppukäyttäjiltä odotetaan, kun he käyttävät pankkitilin täsmäytysavustajaa?

### <a name="while-using-bank-account-reconciliation"></a>Käytettäessä pankkitilin täsmäytystä

Tekoälykäyttöiset vastaavuudet ja ehdotukset voivat joskus olla virheellisiä tai epätäydellisiä. Pankkitilin täsmäytysavustajien käyttäjien on tarkistettava vastaavuudet ja Copilotin antamat ehdotukset, ennen kuin he valitsevat säilyttävänsä ne. Copilotin vastaavuuksia ja ehdotuksia ei tallenneta [!INCLUDE[prod_short](includes/prod_short.md)] -tietokantaan ennen kuin valitset Säilytä se -painikkeen ja poistut Copilot-ikkunasta. Voit myös muokata ja korjata osumia tai ehdotuksia ennen kuin valitset säilyttäväsi sen. 

### <a name="after-completing-bank-account-reconciliation"></a>Pankkitilin täsmäytyksen valmistumisen jälkeen

On suositeltavaa, että käyttäjät myös tarkistavat tarkkuuden ja korjaavat mahdolliset poikkeavuudet Copilot-ikkunasta poistumisen jälkeen, mukaan lukien seuraavat toiminnot: 

- Tarkista täsmäytystestiraportti. 
- Varmista, että organisaatiolla on käytössä asianmukaiset tarkistus- ja auditointiprosessit. 
- Avaa kaikki kirjatut täsmäytykset uudelleen Kumoa-toiminnolla. 
- Virheellisten tapahtumien korjaaminen tapahtumien vastakirjauksen avulla. 

## <a name="what-is-expected-of-administrators-and-end-users-when-operating-bank-account-reconciliation-assist"></a>Mitä järjestelmänvalvojilta ja loppukäyttäjiltä odotetaan, kun he käyttävät pankkitilin täsmäytysavustajaa?

Loppukäyttäjien, kuten kirjanpitäjien, varainhoitajien tai muiden liikekirjanpidon parissa työskentelevien, on aina tarkistettava Copilotin osumien ja ehdotusten tarkkuus, ennen kuin he valitsevat niiden säilyttämisen. Copilotin avulla tehdyn täsmäytyksen jälkeen on suositeltavaa tarkistaa täsmäytystestiraportti, jotta tarkkuus ja mahdolliset eroavaisuudet voidaan tunnistaa. 

Järjestelmänvalvojien on varmistettava, että kirjanpidon käyttäjille on myönnetty käyttöoikeus tähän toimintoon. 

## <a name="is-copilot-the-only-means-to-completing-bank-account-reconciliation"></a>Onko Copilot ainoa keino pankkitilin täsmäytyksen suorittamiseen?

Ei – Copilotin käyttö on valinnaista. [!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa perinteisen, ei-tekoälypohjaisen tiliotteiden tuomisen, ennalta määritettyjen täsmäytyssääntöjen suorittamisen sekä osumien manuaalisen kohdistamisen ja kirjauksen oikeille kirjanpitotileille. Sekä perinteistä lähestymistapaa että Copilotia voi käyttää samanaikaisesti organisaatiossa. 

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Miten annan palautetta tekoälyn luomasta sisällöstä?

Aina kun Copilot antaa vastaavuuksia tai ehdotuksia, voit antaa palautetta Microsoftille suoraan Copilot-ikkunasta käyttäen tykkää- ja ei tykkää -ohjausobjekteja. Palautteesi pysyy anonyyminä ja me käytämme näitä tietoja palvelun laadun parantamiseen.


## <a name="see-also"></a>Katso myös

[Pankkitilien täsmäyttäminen pankkitilin täsmäytysavustajan avulla (esiversio)](bank-reconciliation-with-copilot.md)
