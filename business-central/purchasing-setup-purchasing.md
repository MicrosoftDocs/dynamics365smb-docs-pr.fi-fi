---
title: Ostojen määritystehtävien yleiskatsaus
description: 'Ohjeaiheessa kerrotaan tehtävistä, joilla määritetään yrityksen hallintakäytäntöjä, ja määritetään ostoprosessit.'
author: brentholtorf
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '175, 176, 177, 178, 456, 460, 5727, 5729'
ms.date: 08/30/2022
ms.author: bholtorf
---
# Ostojen määrittäminen

Ennen ostoprosessien hallinnan aloittamista on määritettävä yrityksen ostokäytäntöjen säännöt ja arvot.

Määritä **Ostojen ja ostovelkojen asetukset** -sivun yleisasetukset. Tämä tehdään yleensä kerran alkuperäisen käyttöönoton yhteydessä. Lisätietoja on seuraavassa [Ostojen ja ostovelkojen asetukset](#purchases-and-payables-setup) -osassa.

Uusien toimittajien rekisteröintiin liittyy erillinen sarja tehtäviä, joilla kirjataan kunkin toimittajan mahdolliset erikoishinta- tai alennussopimukset.

Maksumenetelmiä ja valuuttoja sekä muita rahoitukseen liittyviä ostoasetuksia käsitellään Taloushallinnon asetukset -osassa. Lisätietoja kohdassa [Taloushallinnon määrittäminen](finance-setup-finance.md). Vastaavasti varastoon liittyvät ostomääritykset, kuten mittayksiköt ja nimikeseurannan koodit, löytyvät [Varaston määritys -osasta](inventory-setup-inventory.md).

## Ostojen ja ostovelkojen asetukset

Määritä ennen ostojen ja maksujen käsittelemistä **Ostojen ja ostovelkojen asetukset** -sivulla, miten ostojen arvot kirjataan ja numerosarjat, joita toimittajien asiakirjoissa ja ostoasiakirjoissa käytetään.

### Yleiset asetukset

**Yleinen**-pikavälilehdessä määritetään erilaisia vaihtoehtoja, esimerkiksi alennusten laskenta- ja kirjaustapa sekä se, onko laskujen summia tarkoitus pyöristää. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Osa kentistä vaatii erityishuomiota. Tällainen kenttä on esimerkiksi **Laske laskualen. per ALV-/verotunnus**, joka määrittää, lasketaanko laskualennus verotunnuksen vai laskun kokonaissumman mukaan. Lisätietoja on kohdassa [ALV-kirjausryhmien yhdistäminen ALV-kirjausasetuksissa](finance-setup-vat.md#combine-vat-posting-groups-in-vat-posting-setups).

Vastaavasti **Valuuttojen välinen kohdistus** -kentässä voi olla pieniä pyöristyseroja, kun kohdistetaan eri valuutoissa olevia tapahtumia toisiinsa. Lisätietoja on kohdassa [Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa](finance-how-enable-application-ledger-entries-different-currencies.md).

Jotkin kentät myös muuttavat toimintaa tai ne riippuvat siitä, miten muiden kenttien asetukset on määritetty. Esimerkiksi **Tarkista ennakkomaksu kirjattaessa** -ominaisuus vaikuttaa siihen, miten **Ennakkomaksun automaattinen päivitys** -kenttä määritetään odottavien ennakkomaksujen tarkistusta varten.

Lue lisää alla olevista [**Ulkois. asiakirjan nro pakoll.**](#external-document-number)- ja [**Todellisen kust. peruutt. pakollinen**](#exact-cost-reversing) -kentistä.

### Numerosarjojen asetukset

**Numerosarjat**-pikavälilehdessä on määritettävä yksilölliset tunnuskoodit, joita käytetään toimittajien asiakirjoissa, laskuissa ja muissa ostoasiakirjoissa. Numerointi ei ole tärkeää pelkästään sisäisten prosessien kannalta, vaan sen on ehkä myös noudatettava paikallisia säädöksiä. Kannattaa siis määrittää kaikki sarjat **Numerosarjat**-sivulla etukäteen sen sijaan, että luotaisiin uusia sarjoja **Ostojen ja ostovelkojen asetukset** -kohdassa. Lisätietoja on kohdassa [Numerosarjojen luominen](ui-create-number-series.md).

## Ulkoisen tiedoston numero

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## Todellisten kustannusten peruuttaminen

**Todellisen kust. peruutt. pakollinen** -toiminnon avulla voidaan varmistaa, että palautetut tuotteet arvostetaan samana kustannuksena kuin ne alun perin otettiin varastosta käyttämällä kiinteää kohdistusta FIFO (first in first out) -arvostusmenetelmän sijaan. Lisätietoja on [Rakennetiedot: Kiinteä kohdistus](design-details-item-application.md#fixed-application) -osassa. Jos alkuperäiseen ostoon liitetään myöhemmin lisäkustannuksia niin ohjelma päivittää ostopalautuksen arvon vastaavasti.

Kun toiminto on käytössä, palautustapahtuma voidaan kirjata vain määrittämällä nimiketapahtuman numero ostopalautustilauksen rivin **Kohdista nimiketapahtumaan** -kenttään. Kenttää ei oletusarvoisesti näytetä **Rivit**-pikavälilehdessä. Lisätietoja kenttien lisäämisestä sivuille on [Työtilan mukauttaminen](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner) -osassa.

[!INCLUDE[local-functionality](includes/local-functionality.md)]

## Lisää ostojen asetuksia

| Vastaanottaja | Katso |
| --- | --- |
| Luo toimittajakortti kullekin toimittajalle, jolta ostetaan. |[Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md) |
| Priorisoi toimittajat. |[Toimittajien priorisointi](purchasing-how-prioritize-vendors.md) |
| Syötä toimittajakorttiin pankkitilin tiedot IBAN- ja SWIFT-koodit mukaan luettuna. | [Toimittajien pankkitilien määrittäminen](purchasing-how-set-up-vendors-bank-accounts.md) |
| Määritä ostajat, määritä niille toimittajat ja määritä koodit tilastojen seuraamista varten. |[Ostajien määrittäminen](purchasing-how-setup-purchasers.md) |
| Toimittajien nimikkeiden, määrien ja/tai päivämäärien perusteella myöntäminen eri alennusten ja erikoishintojen antaminen. |[Ostohinnan, alennuksen ja maksusopimusten tallentaminen](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| Määritä, mitä maksat yrityksesi ostamista nimikkeistä ja palveluista.  | [Hintojen ja alennusten määrittäminen](across-prices-and-discounts.md) |
| Luo vakiorivejä, jotka lisätään toistuviin ostoasiakirjoihin. | [Toistuvien ostorivien määrittäminen](purchasing-how-work-recurring-purchase-lines.md) |
| Luo tehtäväsarjoja, joilla yhdistät eri käyttäjien suorittamia prosesseja, kuten ostotilausten pyytämisiä ja hyväksymisiä. | [Ostojen hyväksymistyönkulkujen määritys](across-set-up-workflows.md) |
| Hallitse liiketoimia toimittajiesi kanssa, tuo vastaanotettuja laskuasiakirjoja ja rekisteröi uusia toimittajia Outlook-sähköpostiohjelman avulla. | [Business Central -apuohjelman määrittäminen Outlookia varten](admin-outlook.md) |
| Tarkastele kulutositteita, muuta paperi- ja sähköisiä asiakirjoja kirjauskansioriveiksi ja digitalisoin toimittajien paperisia laskuja. | [Saapuvien asiakirjojen määrittäminen](across-how-setup-income-documents.md) |
| Määritä oletusraportteja, joita käytetään eri asiakirjatyypeille. |[Raporttien valinta Business Centralissa](across-report-selections.md)|
|Määritä, voivatko käyttäjät kirjata ostolaskuja ja pitäisikö heidän kirjata ne yhdessä toimituksen kanssa. |[Laskun kirjauskäytännön määrittäminen käyttäjille](admin-setup-invoice-posting-policy.md)|

## Katso myös

[Osto](purchasing-manage-purchasing.md)  
[Yleistä määrityksestä](setup.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
