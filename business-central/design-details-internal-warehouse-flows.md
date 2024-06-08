---
title: 'Rakennetiedot – tuotanto-, kokoonpano- ja projektityönkulut'
description: 'Tietoja komponenttien poiminnan ja kokoonpano-, tuotanto- tai projektitilausten loppunimikkeiden hyllytyksen varastopaikkojen välisestä työnkulusta.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 02/05/2024
ms.custom: bap-template
---
# <a name="flows-for-production-assembly-and-projects"></a>Tuotanto-, kokoonpano- ja projektityönkulut

Sisäiset työnkulut, kuten komponenttien poimiminen ja kokoonpano-, projekti- ja tuotantotilausten loppunimikkeiden hyllyttäminen, muistuttavat saapuvia tai lähteviä virtoja. Monet prosessit voivatkin vaikuttaa tutuilta. Tässä artikkelissa on tietoja fyysisen varaston sisäisten, monimutkaisuudeltaan eritasoisten työnkulkujen käsittelemisestä.

## <a name="overview-of-different-configuration-options"></a>Erilaisten määritysvaihtoehtojen yleiskatsaus

Fyysisen varaston ominaisuuksia voidaan määrittää eri tavoin. On tärkeää, että valittavat vaihtoehdot parantavat prosesseja yleiskustannuksia lisäämättä. Seuraavissa taulukoissa käsitellään tavanomaisia määrityksiä, joilla käsitellään fyysisten tavaroiden tuotanto-, projekti- ja kokoonpanotilauksia.

### <a name="inbound-flow-put-away"></a>Saapuva virta (hyllytys)

|Monimutkaisuustaso|Kuvaus|Asetukset|Varastopaikan koodi|Tuotantotilauksen saapuva virta|Kokoonpanotilauksen saapuva virta|Esimerkki saapuvasta projektityönkulusta|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ei määritettyä fyysisen varaston toimintaa.|Kirjaaminen tilauksista ja päiväkirjoista.||Valinnainen. Hallitaan **Varastopaikka on pakollinen** -vaihtopainikkeella.|Tuotantopäiväkirja -> tuotospäiväkirja</br><br/> **HUOMAUTUS**: tuotos voidaan kirjata käyttämällä **tuotantopäiväkirjaa**.|Kokoonpanotilaus|Hyllytys ei ole saatavana projekteissa|  
|Perus|Tilauksittain.|Vaadi hyllytys. </br><br/> **HUOMAUTUS**: vaikka asetuksen nimi on **Vaadi hyllytys**, tuotos voidaan silti kirjata lähdeasiakirjoista sijainneissa, joissa tämä valintaruutu valitaan. |Valinnainen. Hallitaan **Varastopaikka on pakollinen** -vaihtopainikkeella.|Tuotantotilaus -> varaston hyllytys|Kokoonpanotilaus|Hyllytys ei ole saatavana projekteissa|
|Lisäasetukset|Useiden lähdeasiakirjojen konsolidoidut hyllytystoiminnot.|Vaadi vastaanotto + vaadi hyllytys|Valinnainen. Hallitaan **Varastopaikka on pakollinen** -vaihtopainikkeella.|Tuotantotilaukset -> Kulutuspäiväkirja|Kokoonpanotilaukset -> sisäiset siirrot | Hyllytys ei ole saatavana projekteissa|
|Lisäasetukset|Sama kuin edellä + ohjatut poiminta- ja hyllytystoiminnot|Ohjattu poiminta ja hyllytys (kyseiset vaihtopainikkeet otetaan käyttöön automaattisesti)|Pakollinen|Sama kuin edellä|Sama kuin edellä| Hyllytys ei ole saatavana projekteissa|

Jotkin määritykset eivät salli hyllytysten rekisteröintiä käyttämällä erillisiä fyysisen varastoinnin asiakirjoja. Jos sijainnissa kuitenkin käytetään varastopaikkoja, tuotettuja tai koottuja nimikkeitä voidaan siirtää fyysiseen varastoon yleisillä varaston siirtoasiakirjoilla. Lisätietoja on kohdassa [Nimikkeiden sisäinen siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="outbound-flow-pick"></a>Lähtevä virta (poiminta)

|Monimutkaisuustaso|Kuvaus|Asetukset|Varastopaikan koodi|Tuotantotilauksen lähtevä virta|Kokoonpanotilauksen lähtevä virta|Lähtevä projektityönkulku|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ei määritettyä fyysisen varaston toimintaa.|Kirjaaminen tilauksista ja päiväkirjoista.||Valinnainen. Hallitaan **Varastopaikka on pakollinen** -vaihtopainikkeella.|Tuotantopäiväkirja -> Kulutuspäiväkirja </br><br/> **HUOMAUTUS**: kulutus voidaan kirjata käyttämällä **tuotantopäiväkirjaa**.|Kokoonpanotilaus|Projekti -> Projektipäiväkirja|  
|Perus|Tilauksittain.|Vaadi poiminta. </br><br/> **HUOMAUTUS**: vaikka asetuksen nimi on **Vaadi poiminta**, tuotos voidaan silti kirjata lähdeasiakirjoista sijainneissa, joissa tämä valintaruutu valitaan. <!-- ToDo Test prod output-->|Valinnainen. Hallitaan **Varastopaikka on pakollinen** -vaihtopainikkeella.|Tuotantotilaus -> Varaston poiminta|Kokoonpanotilaus -> Varastosiirto</br><br/>**Varastosiirtoa** voidaan käyttää vain varastopaikkoja käytettäessä.|Projekti -> Varaston poiminta|
|Lisäasetukset|Useiden lähdeasiakirjojen konsolidoidut poimintatoiminnot.|Vaadi toimitus + vaadi poiminta|Valinnainen. Hallitaan Varastopaikka on pakollinen -vaihtopainikkeella|Tuotantotilaukset -> Fyysisen varastoinnin poiminta -> kulutuspäiväkirja |Kokoonpanotilaukset -> Fyysisen varastoinnin poiminta| Projektit -> Fyysisen varastoinnin poiminta -> Projektipäiväkirja |
|Lisäasetukset|Sama kuin edellä + ohjatut poiminta- ja hyllytystoiminnot|Ohjattu poiminta ja hyllytys (kyseiset vaihtopainikkeet otetaan käyttöön automaattisesti)|Pakollinen|Sama kuin edellä|Sama kuin edellä| Projektit eivät tue ohjattua poimintaa ja hyllytystä|

Samoin kuin saapuvassa virrassa jotkin määritykset eivät salli hyllytysten rekisteröintiä käyttämällä erillisiä fyysisen varastoinnin asiakirjoja. Jos sijainnissa käytetään varastopaikkoja, tuotettuja tai koottuja nimikkeitä voidaan siirtää yleisillä varaston siirtoasiakirjoilla. Lisätietoja on kohdassa [Nimikkeiden siirtäminen varastossa](warehouse-move-items.md).

## <a name="warehouses-without-dedicated-warehouse-activity"></a>Fyysiset varastot, joissa ei ole erillistä varastotoimintoa

Esimerkiksi kulutusta ja tuotannon tuotosta halutaan todennäköisesti seurata, vaikka käytössä ei olisikaan erillisiä varastotoimintoja. Seuraavissa artikkeleissa on tietoja lähdeasiakirjojen vastaanottojen käsittelemisestä.

* [Yhden vapautetun tuotantotilausrivin kulutuksen ja tuotoksen rekisteröiminen](production-how-to-register-consumption-and-output.md)
* [Nimikkeiden kokoonpano](assembly-how-to-assemble-items.md)
* [Projektien kulutuksen tai käytön kirjaaminen](projects-how-record-job-usage.md)

## <a name="basic-warehouse-configuration"></a>Fyysisen varastoinnin perusmääritykset

Fyysisen varastoinnin perusmääritysten saapuviin ja lähteviin virtoihin liittyvät seuraavat sijainnin **Sijaintikortit**-sivulla olevat asetukset:

* Saapuvien virrassa (hyllytyksessä) **Vaadi hyllytys** otetaan käyttöön vaihtopainikkeella mutta **Vaadi vastaanotto** poistetaan käytöstä vaihtopainikkeella.
* Lähtevien virrassa (poiminnassa) **Vaadi poiminta** otetaan käyttöön vaihtopainikkeella mutta **Vaadi toimitus** poistetaan käytöstä vaihtopainikkeella.

### <a name="flows-to-and-from-production-in-a-basic-warehouse-configuration"></a>Fyysisen varastoinnin perusmääritysten tuotannon tulevat ja lähtevät työnkulut

Tuotannon komponentteja voi poimia työkulussa tuotantoon **Varaston poiminta** -asiakirjojen avulla. Tuotettavat tuotteet hyllytetään **Varaston hyllytys** -asiakirjojen avulla.

Varastopaikkoja käyttävissä sijainneissa komponentin materiaaliottojen tekemiseen kannattaa käyttää varastosiirtoasiakirjoja. Lisätietoja komponentin kulutuksen materiaaliotoista tuotannon valmistelun tai avoimista tuotannon varastopaikoista on kohdassa [Tuotannon komponenttien materiaaliotot fyysisessä varastossa](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Varastosiirrot ovat tärkeitä asiakirjoja, jos materiaaliottomenetelmänä on käytössä **Poiminta + eteenpäin** tai **Poiminta + taaksepäin**. Lisätietoja on kohdassa [Materiaaliottomenetelmät](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* Sijaintikortin taikka kuormitusryhmän tai tuotantosolun **Tuotannon valm.var.paik.koodi**-, **Valm. tuot.nim. var.paik.koodi**- ja **Avoin tuotannon var.paik.koodi** -kentät määrittävät tuotantoalueen tulevat ja lähtevät oletustyönkulut.
* Tuotettujen nimikkeiden varaston siirtoa voidaan hallita **Varastosiirto**-sivulla ilman suhdetta tuotantotilaukseen.

### <a name="flows-to-and-from-assembly-in-a-basic-warehouse-configuration"></a>Fyysisen varastoinnin perusmääritysten kokoonpanoon tulevat lähtevät työnkulut

Kokoonpanon tuotos ja kulutus kirjataan suoraan kokoonpanotilauksesta.

> [!NOTE]
> Kokoonpanotilaukset eivät tue **Varaston poiminta**-ja **Varaston hyllytys** -asiakirjoja.

Varastopaikkoja käyttävät sijainnit:

* Kokoonpanon komponentit siirretään kokoonpanoalueelle **Varastosiirto**-asiakirjojen avulla.
* Sijaintikortin **Kokoonpanoon-varastop.koodi**- ja **Kokoonpanosta-varastop.koodi** -kentät määrittävät kokoonpanoalueiden saapuvat ja lähtevät oletustyönkulut.
* Koottujen nimikkeiden varaston siirtoa voidaan hallita **Sisäinen siirto** -sivulla ilman suhdetta kokoonpanotilaukseen.

[!INCLUDE [prod_short](includes/prod_short.md)] tukee kokoonpanotyönkulkuja, joissa on kyse kokoonpanosta varastoon ja kokoonpanosta tilausta varten. Lisätietoja on kohdassa [Tietoja kokoonpanosta tilausta varten ja kokoonpanosta varastoon](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock) Suhteessa fyysiseen varaston hallintaan kokoonpano varastoon on osa sisäistä fyysisen varastoinnin työnkulkuja, kun taas kokoonpano tilausta varten tapahtuu fyysisen varaston lähtevässä virrassa. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="flows-for-project-management-in-a-basic-warehouse-configuration"></a>Fyysisen varaston perusmääritysten projektinhallinnan työnkulut

Projektin komponentteja voi poimia työnkulussa projektinhallintaan **Varaston poiminta** -asiakirjojen avulla.

Varastopaikkoja käyttävässä sijainnissa sijainnin **Projektin valmisteluvarastopaikkakoodiin** -kenttää määrittää oletustyönkulut projektinhallintaan.

## <a name="advanced-warehouse-configurations"></a>Laajennetut varastomääritykset

Fyysisen varastoinnin laajennettujen määritysten saapuviin ja lähteviin virtoihin liittyvät seuraavat sijainnin **Sijaintikortit**-sivulla olevat asetukset:

* Saapuvien virrassa (hyllytyksessä) **Vaadi vastaanotto** ja **Vaadi hyllytys** otetaan vaihtopainikkeilla käyttöön.
* Lähtevien virrassa (poiminnassa) **Vaadi toimitus** ja **Vaadi vastaanotto** otetaan vaihtopainikkeilla käyttöön.

### <a name="flows-to-and-from-production-in-advanced-warehouse-configurations"></a>Fyysisen varastoinnin laajennettujen määritysten tuotannon tulevat ja lähtevät työnkulut

Komponentteja poimitaan tuotantoon käyttämällä **F.varastoinnin poiminta** -asiakirjoja ja **Poimintatyökirja**-sivua.

Varastopaikkoja käyttävät sijainnit:

* Etenkin **Fyysisen varaston siirto** -asiakirjat ja **Siirtotyökirja**-sivu ovat käteviä komponentin materiaaliotoissa. Lisätietoja on kohdassa [Tuotannon komponenttien materiaaliotot fyysisessä varastossa](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
* Sijaintikortin taikka kuormitusryhmän tai tuotantosolun **Tuotannon valm.var.paik.koodi**-, **Valm. tuot.nim. var.paik.koodi**- ja **Avoin tuotannon var.paik.koodi** -kentät määrittävät tuotantoalueen tulevat ja lähtevät oletustyönkulut. 
* Tuotettujen nimikkeiden varaston siirtoa voidaan hallita **Siirtotyökirja**- tai **F.var. sis. hyllytys**-sivuilla ilman suhdetta tuotantotilaukseen.

### <a name="flows-to-and-from-assembly-in-advanced-warehouse-configurations"></a>Fyysisen varastoinnin laajennettujen määritysten kokoonpanon tulevat ja lähtevät työnkulut

Komponentteja poimitaan kokoonpanoon käyttämällä **F.varastoinnin poiminta** -asiakirjoja ja **Poimintatyökirja**-sivua.

Varastopaikkoja käyttävät sijainnit:

* Sijainnin **Kokoonpanoon-varastop.koodi**- ja **Kokoonpanosta-varastop.koodi**-kentät määrittävät kokoonpanoalueiden saapuvat ja lähtevät oletustyönkulut.
* Kokoonpanon nimikkeiden varaston siirtoa voidaan hallita **Siirtotyökirja**- tai **F.var. sis. hyllytys**-sivuilla ilman suhdetta kokoonpanotilaukseen.

[!INCLUDE [prod_short](includes/prod_short.md)] tukee kokoonpanotyönkulkuja, joissa on kyse kokoonpanosta varastoon ja kokoonpanosta tilausta varten. Lisätietoja on kohdassa [Tietoja kokoonpanosta tilausta varten ja kokoonpanosta varastoon](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock) 

Kokoonpano varastoon on osa sisäistä fyysisen varastoinnin työnkulkuja, kun taas kokoonpano tilausta varten tapahtuu fyysisen varaston lähtevässä virrassa. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden käsitteleminen fyysisen varastoinnin toimituksissa](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### <a name="flows-to-project-management-in-advanced-warehouse-configurations"></a>Fyysisen varaston laajennettujen määritysten projektinhallinnan työnkulut

Komponentteja poimitaan projektinhallinnan työnkulussa käyttämällä **F.varastoinnin poiminta** -asiakirjoja ja **Poimintatyökirja**-sivua.

Varastopaikkoja käyttävissä sijainneissa sijainnin **Projektin valmisteluvarastopaikkakoodiin** -kenttää määrittää oletustyönkulut projektialueelle.

## <a name="see-also"></a>Katso myös

[Varastoinninhallinnan yleiskatsaus](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
