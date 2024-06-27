---
title: Usein kysyttyjä kysymyksiä pankkitilin täsmäytysavustajasta Copilotin avulla (esiversio)
description: 'Tässä UKK:ssa on tietoa tekoälytekniikasta, jota käytetään pankkitilien ja tiliotteiden täsmäytykseen Business Centralissa. Niissä käsitellään tärkeitä huomioitavia ja niissä on tietoja siitä, miten tekoälyä käytetään sekä miten sitä on testattu ja arvioitu. Lisäksi käsitellään mahdollisia rajoituksia.'
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

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Nämä usein kysytyt kysymykset kuvaavat Microsoft Copilotin tekoälyn vaikutusta pankkitilin täsmäytykseen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-bank-reconciliation-assist"></a>Mikä on pankkitilin täsmäytysavustaja?

Pankkitilin täsmäytys on yleinen kirjanpitotehtävä, jossa organisaatiot tarkistavat tiliotteensa ja tunnistavat kauppatapahtumat, jotka tulisi rekisteröidä [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. Tätä tehtävää käytetään esimerkiksi yksilöimään jaksoittaisia pankkimaksuja tai pieniä työntekijäkuluja.

Pankkitäsmäytys on yleensä monivaiheinen prosessi. Pankin tiliotteet tuodaan ensin [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. Seuraavaksi tapahtumat täsmäytetään kirjanpitotietoihin. Uudet tapahtumat kirjataan siten, että ne vastaavat mahdollisia jäännöstransaktioita, jotka eivät aiemmin olleet tapahtumakirjauksissasi tiedossa.

Copilot [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa vähentää manuaalista työtä täsmäyttämällä useampia tapahtumia ja ehdottamalla kirjanpitotilejä (KP), joihin voi kirjata.

## <a name="what-are-the-capabilities-of-bank-reconciliation-assist"></a>Mitkä ovat pankkitilin täsmäytysavustajan valmiudet?

Copilotin avulla tekoälyä voi käyttää kahdessa erillisessä tehtävässä:

- Tapahtumien ja kirjanpitotietojen yhteensovittamisen parantaminen

    [!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa automaattisia sääntöjä, jotka vastaavat automaattisesti monia pankkitapahtumia ja kirjanpitotapahtumia. Nämä säännöt ovat kuitenkin joustamattomia, ja ne johtavat usein moniin vastaamattomiin tapahtumiin, joista jokainen edellyttää manuaalista tarkastusta ja vertailua. Copilot käyttää tekoälyteknologiaa, kun halutaan tarkastaa täsmäyttämättömät tapahtumat ja tunnistaa useampia vastaavuuksia päivämäärien, summien ja kuvausten perusteella. Jos asiakas esimerkiksi maksoi useita laskuja yhtenä kertakorvauksena, Copilot täsmäyttää yksittäisen tiliotteen rivin useiden laskutapahtumien kanssa.

- Suositellut KP-tilit

    Jäljellä olevien pankkitapahtumien osalta, joita ei voida yhdistää mihinkään kirjanpitoon, Copilot käyttää tekoälyteknologiaa verratakseen tapahtumakuvausta KP-tilien nimiin ja ehdottaa sitten todennäköisimpää KP-tiliä, jolle kirjataan. Jos esimerkiksi täsmäyttämättömillä tapahtumilla on *Bensa-asema 24* -narratiivi Copilot saattaa ehdottaa, että ne kirjataan *Kuljetus*-tilille.

Copilot ei muodosta yhteyttä pankkiisi noutaakseen tai lähettääkseen kauppatapahtumia. Tehtävä pysyy täysin hallinnassasi. Se on edellytys Copilotin avustajan käyttämiselle riippumatta siitä, lisätäänkö kyseiset tapahtumat [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan digitaalisen pankkiyhteyden avulla, tuomalla tiliotetiedostosta tai syöttämällä manuaalisesti.

## <a name="what-is-the-intended-use-of-bank-reconciliation-assist"></a>Mitä pankkitilin täsmäytysavustajaa aiotaan käyttää?

Pankkitilien täsmäytysapu on suunniteltu parantamaan kirjanpidon tarkkuutta auttamalla asiakkaita tunnistamaan uudet tapahtumat, jotka heidän tulee ottaa huomioon [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa. Sitä ei ole tarkoitettu petosten havaitsemiseen tai sen tunnistamiseen ovatko asiakkaat maksaneet ajoissa.

## <a name="how-was-bank-reconciliation-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Miten pankkitilin täsmäytysavustaja arvioitiin? Mitä mittareita suorituskyvyn mittaamiseen käytetään?

Pankkitilien täsmäytysavustaja testattiin käyttämällä synteettisten pankkitapahtumatietojen ja vastaavien KP-tilien ja tapahtumien yhdistelmiä, jotka kattavat tavalliset vaihtelut ja datarajat kunkin kentän osalta sekä eri kielillä. Testitiedot kuvaavat sekä huonojen toimijoiden tavallista käyttöä että käyttöä. Suorituskykyä verrattiin samojen tietojen manuaaliseen täsmäytykseen.

## <a name="what-are-the-limitations-of-bank-reconciliation-assist-how-can-users-minimize-the-impact-of-these-limitations-when-they-use-the-system"></a>Mitkä ovat pankkitilin täsmäytysavustajan rajoitukset? Miten käyttäjät voivat minimoida nämä rajoitukset, kun he käyttävät järjestelmää?

Pankkitilin täsmäytysavustaja toimii parhaiten, kun KP-tilien nimet, tapahtumakuvaukset ja pankin kauppatapahtumien kuvaukset ovat kaikki samalla kielellä. Sekoitetuilla kielillä tai transaktioiden kuvausten sekoitetuilla kielillä saadaan usein vähemmän vastauksia ja ehdotuksia.

Ehdotetut kirjanpitotilit toimivat parhaiten jollakin tuetuista kielistä (lisätietoja on kieliluettelon seuraavassa osassa). Käyttäjillä saattaa olla vähemmän tapahtumien vastaavuuksia ja vähemmän ehdotettuja kirjanpitotilejä muilla kielillä.

## <a name="in-which-geographies-and-languages-is-bank-reconciliation-assist-available"></a>Millä maantieteellisillä alueilla ja kielillä pankkitilin täsmäytysavustaja on saatavilla?

- Saatavilla olevat maantieteelliset tilat

  Pankkitilin täsmäytysavustaja on käytettävissä kaikilla tuetuilla [Business Centralin maissa/alueilla](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Asiakasympäristöissä, jotka sijaitsevat maissa/alueilla, joissa Azure OpenAI Serviceä ei ole otettu käyttöön, edellytetään sitä, että järjestelmänvalvojien on ensin annettava suostumus tietojen siirtämiseen yli rajojen, jotta [!INCLUDE [prod_short](includes/prod_short.md)] voi muodostaa yhteyden Azure OpenAI Serviceen. Lisätietoja kohdassa [Copilot-tietojen siirtäminen maantieteellisten alueiden välillä](ai-copilot-data-movement.md).

- Käytettävissä olevat kielet

  [!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

Lisätietoja kielistä on aiemmassa rajoituskysymyksessä.

## <a name="what-is-expected-of-system-users-when-they-operate-bank-account-reconciliation-assist"></a>Mitä järjestelmäkäyttäjiltä odotetaan, kun he käyttävät pankkitilin täsmäytysavustajaa?

### <a name="during-bank-account-reconciliation"></a>Pankkitilin täsmäytyksen aikana

Tekoälykäyttöiset vastaavuudet ja ehdotukset voivat joskus olla virheellisiä tai epätäydellisiä. Pankkitilin täsmäytysavustajien käyttäjien on tarkistettava vastaavuudet ja Copilotin antamat ehdotukset, ennen kuin he valitsevat säilyttävänsä ne. Copilotin vastaavuuksia ja ehdotuksia ei tallenneta [!INCLUDE[prod_short](includes/prod_short.md)] -tietokantaan ennen kuin valitset **Säilytä se** -painikkeen ja suljet Copilot-ikkunan. Vastineita ja ehdotuksia voidaan muokata ja korjata osumia ennen niiden säilyttämisen valitsemista.

### <a name="after-bank-account-reconciliation-is-completed"></a>Sen jälkeen, kun pankkitilin täsmäytys valmistuu

Suosittelemme, että käyttäjät myös tarkistavat tarkkuuden ja korjaavat mahdolliset poikkeavuudet Copilot-ikkunasta poistumisen jälkeen. Tähän prosessiin tulisi sisältyä seuraavat toimenpiteet:

- Tarkista täsmäytystestiraportti.
- Varmista, että organisaatiolla on käytössä asianmukaiset tarkistus- ja auditointiprosessit.
- Avaa kaikki kirjatut täsmäytykset uudelleen **Kumoa**-toiminnolla.
- Virheellisten tapahtumien korjaaminen tapahtumien vastakirjauksen avulla.

## <a name="what-is-expected-of-administrators-and-system-users-when-they-operate-bank-account-reconciliation-assist"></a>Mitä järjestelmänvalvojilta ja järjestelmäkäyttäjiltä odotetaan, kun he käyttävät pankkitilin täsmäytysavustajaa?

Järjestelmäkäyttäjien, kuten kirjanpitäjien, rahastonhoitajan tai muiden yritysten kirjanpidon parissa työskentelevien, tulee aina tarkistaa Copilotin tarjoamien osumien ja ehdotusten tarkkuus ennen kuin he päättävät pitää ne. Copilotin avulla tehdyn täsmäytyksen jälkeen on suositeltavaa, että nämä käyttäjät tarkistavat täsmäytystestiraportin, jotta tarkkuus ja mahdolliset eroavaisuudet voidaan tunnistaa.

Järjestelmänvalvojien on varmistettava, että kirjanpidon käyttäjille on myönnetty käyttöoikeus tähän toimintoon.

## <a name="is-copilot-the-only-means-of-completing-bank-account-reconciliation"></a>Onko Copilot ainoa keino pankkitilin täsmäytyksen suorittamiseen?

Nro Copilotin käyttö on valinnaista. [!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa perinteisen, ei-tekoälypohjaisen tiliotteiden tuomisen, ennalta määritettyjen täsmäytyssääntöjen suorittamisen sekä osumien manuaalisen kohdistamisen ja kirjauksen oikeille kirjanpitotileille. Sekä perinteistä lähestymistapaa että Copilotia voi käyttää samanaikaisesti organisaatiossa.

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Miten annetaan palautetta tekoälyn luomasta sisällöstä?

Aina, kun Copilot antaa vastineita tai ehdotuksia, Microsoftille voidaan antaa palautetta suoraan Copilot-ikkunasta käyttämällä Tykkää- (peukalo ylös) ja Ei tykkää (peukalo alas) -ohjausobjekteilla. Palautteesi pysyy anonyyminä ja me käytämme näitä tietoja palvelun laadun parantamiseen.

## <a name="see-also"></a>Katso myös

[Pankkitilien täsmäyttäminen Copilotin avulla (esiversio)](bank-reconciliation-with-copilot.md)
