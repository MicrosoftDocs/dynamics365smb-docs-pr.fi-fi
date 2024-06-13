---
title: Usein kysyttyjä kysymyksiä sähköisten asiakirjojen yhdistämisestä ostotilauksiin
description: 'Usein kysytyt kysymykset sisältävät tietoja Business Centralin käyttämästä tekoälyteknologiasta sekä tärkeitä huomioita tekoälyn käyttämisestä, sen testaamisesta ja arvioimisesta sekä mahdollisista erityisistä rajoituksista.'
ms.date: 02/23/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.collection:
  - bap-ai-copilot
---

# <a name="faq-for-mapping-e-documents-with-purchase-orders-using-copilot-preview"></a>Usein kysyttyjä kysymyksiä sähköisten asiakirjojen yhdistämisestä ostotilauksiin Copilotin avulla (esiversio)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Nämä usein kysytyt kysymykset käsittelevät tekoälyn vaikutusta [!INCLUDE [prod_short](includes/prod_short.md)]in **Sähköisen asiakirjan kohdistusapuri**.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-e-documents-matching-assistance"></a>Mikä on sähköisten asiakirjojen kohdistusapuri?

Modernit liiketoimintatapahtumat ohjautuvat sähköisiin asiakirjoihin. Ne ovat keskeisiä dokumentteja, kuten laskuja ja kuitteja, jotka siirtävät kaksisuuntaisesti toimituksen ja vastaanoton välillä. Sähköisiä laskuja voidaan luoda ja lähettää digitaalisesti jäsennetyssä muodossa, joka helpottaa automaattista laskujen käsittelyä. Saapuvien digitaalisten laskujen käsittely voi kuitenkin olla haasteellista ostoreskontratiimeille.  

Pienissä ja keskisuurissa yrityksissä (PK-yrityksissä) ostoreskontratiimin merkitys on keskeinen toimittajan velvoitteiden tarkassa seurannassa. Tiimin keskeinen tehtävä on kirjata saapuvat laskut tarkasti. Tarkkuus voi kuitenkin olla haastavaa etenkin täsmäytettäessä ulkoisia toimittajien laskuja ja aiemmin luotuja ostotilauksia. Koodien, kuvausten ja mittayksiköiden ristiriidat ovat usein haastavia, sillä kyseiset elementit eivät aina täsmää eri järjestelmissä ja yrityksissä. Lisäksi odottamattomat kustannukset, kuten kuljetusmaksut, voivat näkyä erillisinä rivinimikkeinä, jotka on muutettava manuaalisesti. Kirjanpitäjien on sisällytettävä asiakirjoihin myös laskun numerot ja päivämäärät. On tärkeää huomata, että ostotilausten ja ulkoisten laskujen suhde ei ole aina yhden suhde yhteen. Samalle ostotilaukselle voidaan useita ulkoisia laskuja.

[!INCLUDE [prod_short](includes/prod_short.md)]issa voitiin historiallisesti luoda uusia ostolaskuja vastaanotettujen sähköisten laskujen perusteella. Laskujen ja aiemmin luotujen ostotilausten manuaalinen täsmäyttäminen on prosessi, joka vie paljon aikaa ja on virhealtis.

**Sähköisen asiakirjan kohdistusapuri** käyttää generatiivista tekoälyä sujuvoittamaan tätä prosessia automatisoimalla ulkoisten sähköisten laskujen analyysia. Ominaisuus antaa kirjanpitäjille mahdollisuuden pyytää Copilotia täsmäyttämään saapuvien sähköisten laskujen rivit ja ostotilausten rivit [!INCLUDE [prod_short](includes/prod_short.md)]issa.

## <a name="what-are-capabilities-of-the-e-documents-matching-assistance"></a>Mitä ominaisuuksia sähköisten asiakirjojen kohdistusapurissa on?

Copilotin ansiosta käytössä tekoälypohjaista avustusta kohdistettaessa vastaanotettu digitaalinen lasku aiemmin luotuihin ostotilauksiin [!INCLUDE [prod_short](includes/prod_short.md)]issa. Copilot kohdistaa rivit seuraavien perusteella:

- Kuvausten samankaltaisuus
- Mittayksiköt
- Laskutettavissa olevat määrät
- Summat

Copilot tunnistaa samankaltaiset kuvaukset, jos niissä on oikeat mittayksiköt ja hinnat. Se voi etsiä vastaavuuksia myös monimutkaisemmissa tapauksissa. Se voi esimerkiksi tunnistaa, onko sähköisessä laskussa kaksi riviä, joissa on saman nimikkeen variantti, mutta ostotilauksessa on vain yksi rivi; [!INCLUDE [prod_short](includes/prod_short.md)] kohdistaa nämä rivit, mikäli kuvaukset ovat samankaltaiset ja hinnat ovat samat.

Copilot ei yhdistä sähköisiä asiakirjoja päätepistepalveluun digitaalisten tositteiden noutoa tai lähettämistä varten. Tämä tehtävä pysyy täysin käyttäjän hallinnassa ja on edellytys Copilotin hyödyntämiseen. Näin toimitaan riippumatta siitä, onko digitaaliset asiakirjat lisätty [!INCLUDE [prod_short](includes/prod_short.md)]iin käyttämällä päätepistepalvelun yhteyttä tai syöttämällä manuaalisesti.  

## <a name="what-is-the-intended-use-of-the-e-documents-matching-assistance"></a>Mikä on sähköisten asiakirjojen kohdistusapurin käyttötarkoitus?

**Sähköisen asiakirjan kohdistusapuri** -ominaisuuden tavoite on auttaa ostoreskontratiimiä kohdistamaan aiemmin luodut ostotilaukset ja saapuvat sähköiset laskut. Suurin osa tästä toiminnasta koskee merkkijonojen kohdistusta. [!INCLUDE [prod_short](includes/prod_short.md)]issa on ominaisuus, joka automatisoi osan tästä toiminnasta, ja LLM-malleissa on tunnistettu mahdollisuus täydentää kyseistä ominaisuutta ja vähentää entisestään manuaalisia toimia.  

## <a name="how-was-e-documents-matching-assistance-evaluated-what-metrics-are-used-to-measure-performance"></a>Miten sähköisten asiakirjojen kohdistusapuri arvioitiin? Mitä mittareita suorituskyvyn mittaamiseen käytetään?

Ominaisuutta testattiin käyttämällä seuraavien tietojen yhdistelmiä:

- Ulkoisen nimikkeen kuvaukset
- Mittayksiköt
- Määrät ja summat
- Vakiomuotoiset nimikekuvaukset
- Eri kielet
- Muut parametrit, jotka koskevat kunkin kentän tyypillisiä vaihtelua ja tietorajoituksia 

Testitiedot ilmaisevat sekä tyypillistä käyttöä että haitallisten toimijoiden käyttöä. Suorituskykyä mitattiin vertaamalla sitä samojen sähköisten laskujen ja ostotilausten tietojen manuaaliseen kohdistamiseen.

## <a name="what-are-the-limitations-of-e-documents-matching-assistance-how-can-users-minimize-the-impact-of-the-e-documents-matching-assistance-limitations-when-using-the-system"></a>Mitä rajoituksia sähköisten asiakirjojen kohdistusapurissa on? Miten käyttäjät voivat minimoida sähköisten asiakirjojen kohdistusapurin rajoitukset, kun he käyttävät järjestelmää?

**Sähköisen asiakirjan kohdistusapuri** toimii parhaiten, kun ulkoinen (sähköinen lasku) ja sisäinen ([!INCLUDE [prod_short](includes/prod_short.md)]) nimikekuvaus sekä mittayksiköt ovat kaikki samankielisiä. Jos kieliä on useita tai nimikekuvauksia on useilla kielillä, tuloksena on usein vähemmän vastineita ja ehdotuksia.  

Sähköisten laskujen nimikkeiden ja ostotilausten nimikkeiden ehdotettu kohdistus toimii parhaiten englannin kieltä käytettäessä. Vaikka ominaisuutta voi käyttää millä tahansa kielellä, jota [!INCLUDE [prod_short](includes/prod_short.md)] tukee, muilla kielillä nimikevasteita saattaa olla vähemmän.

## <a name="in-which-geographies-and-languages-is-e-documents-matching-assistance-available"></a>Millä maantieteellisillä alueilla ja kielillä sähköisten asiakirjojen kohdistusapuri on saatavana?

Tämä ominaisuus on käytettävissä kaikissa ympäristöissä, maa- tai aluelokalisoinnissa ja millä tahansa käyttäjän kielellä Kanadaa lukuun ottamatta. Rajoitetun kielituen vuoksi ominaisuus ei ole aluksi kanadalaisten asiakkaiden käytettävissä, koska ominaisuus ei ole kielen osalta säädösten mukainen. 

Sellaisten maiden tai alueiden ympäristöissä, joissa Azure OpenAI Servicea ei ole otettu käyttöön, tämän ominaisuuden saatavuus edellyttää, että järjestelmänvalvojien on ensin suostuttava tietojen siirtämiseen rajojen yli [!INCLUDE [prod_short](includes/prod_short.md)]issa, sillä yhteys Azure OpenAI Serviceen ei ole muutoin mahdollista.  

Lisätietoja kielistä on kohdissa [Mitä rajoituksia sähköisten asiakirjojen kohdistusapurissa on? Miten käyttäjät voivat minimoida sähköisten asiakirjojen kohdistusapurin rajoitukset, kun he käyttävät järjestelmää?](#what-are-the-limitations-of-e-documents-matching-assistance-how-can-users-minimize-the-impact-of-the-e-documents-matching-assistance-limitations-when-using-the-system).   

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>Mitkä operatiiviset tekijät ja asetukset mahdollistavat ominaisuuden tehokkaan ja vastuullisen käytön?

Copilot täydentää [!INCLUDE [prod_short](includes/prod_short.md)]issa jo olevaa yhdistämismääritysalgoritmia ja yhdistää rivit, joita algoritmi ei yhdistänyt.

### <a name="what-is-expected-of-users-while-using-e-documents-matching-assistance"></a>Mitä loppukäyttäjien odotetaan tekevän sähköisten asiakirjojen kohdistusapuria käytettäessä?

<!--Not sure that this is the right content for this section. Seems like it belongs more in the overview article because it's more related to how to use the feature-->

Kun saapuvat sähköiset laskut on yhdistetty ostotilauksiin, asiakirjojen rivit on yhdistettävä.

**Ostotilauksen yhdistämismääritys** -sivulla on näkyvissä molempien asiakirjojen kaikki rivit. Yhdistämismääritys voidaan tehdä täällä manuaalisesti, mikä voi olla hankalaa, jos rivejä on paljon.

**Sähköisten asiakirjojen kohdistusapuria** voidaan käyttää yhdistämään rivit seuraavien ehtojen perusteella:

- Kuvausten samankaltaisuus
- Mittayksiköt
- Laskutettavissa olevat määrät
- Summat

Copilotin vastineet voivat on virheellisiä tai epätäydellisiä. Niiden tarkkuus onkin aina tarkistettava, ennen kuin ne päätetään säilyttää. Copilotin vastineet ja ehdotukset tallennetaan [!INCLUDE [prod_short](includes/prod_short.md)]iin, kun **Säilytä se** valitaan ja lopeta Copilot. Vastineita ja ehdotuksia voidaan muokata ja korjata osumia ennen niiden säilyttämisen valitsemista. 

### <a name="what-is-expected-of-administrators-and-users-when-operating-e-documents-matching-assistance"></a>Mitä järjestelmänvalvojilta ja loppukäyttäjiltä odotetaan sähköisten asiakirjojen kohdistusapuria käytettäessä?

Loppukäyttäjien, kuten kirjanpitäjien, tai muiden sähköisiä laskuja vastaanottavien on aina tarkistettava Copilotin vastineiden ja ehdotusten tarkkuus, ennen kuin he valitsevat niiden säilyttämisen. Ostotilausrivit kannattaa tarkistaa, sillä näin voidaan varmistaa näin niiden tarkkuus ja löytää mahdolliset ristiriidat. **Sähköisten asiakirjojen kohdistusapurin** käyttäminen on käyttäjän päätettävissä. Vaikka järjestelmänvalvoja on ottanut **sähköisten asiakirjojen kohdistusapurin** käyttöön ja se on käytettävissä, käyttäjä voi silti valita, käytetäänkö sitä aina, joskus vai ei koskaan.  

Järjestelmänvalvojat päättävät viime kädessä, käytetäänkö Copilotia [!INCLUDE [prod_short](includes/prod_short.md)]issa. Jos järjestelmänvalvojat ottavat Copilotin käyttöön, heidän on varmistettava, että he myöntävät sen käyttöoikeuden asianmukaisesti.

> [HUOMAUTUS!]
> - Ominaisuutta ei tueta [!INCLUDE [prod_short](includes/prod_short.md)]in paikallisissa versioissa tai yksityisissä pilvissä.
> - Kumppanit eivät voi laajentaa tätä ominaisuutta. Kumppanikehittäjät eivät voi muokata, korvata eivätkä laajentaa tätä ominaisuutta. 

## <a name="is-copilot-the-only-way-to-match-e-documents-to-purchase-orders"></a>Onko Copilot ainoa tapa kohdistaa sähköiset asiakirjat ostotilauksiin?

Ei. Käyttäjä päättää itse Copilotin käytöstä. [!INCLUDE [prod_short](includes/prod_short.md)]issa on muita kuin tekoälypohjaisia tapoja kohdistaa vastaanotetun sähköisen laskun nimikkeet ostotilausten nimikkeisiin [!INCLUDE [prod_short](includes/prod_short.md)]issa. Organisaatiot voivat myös käyttää molempia vaihtoehtoja samanaikaisesti.  

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Miten annan palautetta tekoälyn luomasta sisällöstä?

Aina kun Copilot antaa vastineita tai ehdotuksia, Microsoftille voidaan antaa palautetta suoraan Copilot-ikkunasta Tykkää- ja Ei tykkää -ohjausobjekteilla. Palautteesi pysyy anonyyminä ja me käytämme näitä tietoja palvelun laadun parantamiseen.  

## <a name="see-also"></a>Katso myös

[Sähköisten asiakirjojen yleiskatsaus](finance-edocuments-overview.md)
[Sähköisten asiakirjojen yhdistäminen ostotilausriveille Copilotin avulla](map-edocuments-with-copilot.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
