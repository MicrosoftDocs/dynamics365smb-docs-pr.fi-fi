---
title: Myynnin hallintatehtävien yleiskatsaus | Microsoft Docs
description: Tässä artikkelissa määritetään, miten myyntiaktiviteetteja hallitaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6f80d2e1a1a864d5aaff0660d21603f91c5ce229
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251513"
---
# <a name="sales"></a>Myynti
Luo myyntilasku tai -tilaus tallentaaksesi sopimuksesi asiakkaan kanssa ja myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla.

Myyntitilauksia on käytettävä, jos myyntiprosessi vaatii tilausmäärän osittaisen toimittamisen esimerkiksi silloin, kun koko määrä ei ole kerralla käytettävissä. Jos myyt nimikkeitä toimittamalla ne suoraan toimittajalta asiakkaalle (suoratoimituksena), myyntitilauksia on käytettävä. Kaikilta muilta osin myyntitilaukset toimivat samalla tavalla kuin myyntilaskut. Voit ilmoittaa tietyt toimituspäivät asiakkaille myyntitilauksissa Toimituksen lupaaminen -toiminnon avulla.  

Voit neuvotella asiakkaan kanssa luomalla ensin myyntitarjoukseen, jonka voit muuntaa myyntilaskuksi tai -tilaukseksi, kun hyväksyt myynnin. Kun asiakas on vahvistanut sopimuksen, voit lähettää tilausvahvistuksen ja tallentaa velvollisuutesi toimittaa tuotteet sovitusti.

Voit helposti korjata tai peruuttaa kirjatun myyntilaskun ennen kuin se on maksettu. Tästä on hyötyä, jos haluat korjata kirjoitusvirheen tai jos asiakas pyytää muutosta prosessin alkuvaiheessa. Jos kirjattu myyntilasku maksetaan, sinun on peruutettava myynti luomalla myyntihyvityslasku tai myyntipalautustilaus.

Tärkeintä hyvissä myynti- ja markkinointikäytännöissä on tehdä oikeita päätöksiä oikeaan aikaan. [!INCLUDE[d365fin](includes/d365fin_md.md)]in markkinointitoiminnot tarjoavat yhteystietojen yleiskuvauksen tarkasti ja oikea-aikaisesti, mikä tehostaa mahdollisten asiakkaiden palvelemista ja parantaa asiakastyytyväisyyttä. Lisätietoja on kohdassa [Kontaktienhallinta](marketing-relationship-management.md).

Liiketoimintaympäristöissä, joissa asiakkaan on maksettava ennen kuin tuotteet toimitetaan, kuten vähittäismyynti, sinun on odotettava maksukuittia ennen kuin toimitat tuotteet. Useimmissa tapauksissa saapuvia maksuja käsitellään joitakin viikkoja toimituksen jälkeen kohdistamalla maksut niihin liittyviin kirjattuihin ja maksamattomiin myyntilaskuihin. Lisätietoja on kohdassa [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

Myyntiasiakirjat voidaan lähettää sähköpostin liitteenä PDF-tiedostoina. Sähköpostin perusteksti sisältää otteen myyntiasiakirjasta. Ote voi sisältää esimerkiksi tuotteet, kokonaissumman ja PayPal-sivuston linkin. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md).

Voit ottaa hyväksymistyönkulun käyttöön kaikissa myyntiprosesseissa esimerkiksi silloin, kun pyydät talouspäälliköltä hyväksyntää isolle myynnille tiettyä asiakasta varten. Lisätietoja on kohdassa [Työnkulkujen käyttäminen](across-use-workflows.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.

| Vastaanottaja | Katso |
| --- | --- |
|Luo asiakkaan kortti jokaiselle asiakkaalle, jolle myyt.|[Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md)|
| Luo myyntitarjous, jos tarjoat tuotteita siirtokelpoisilla ehdoilla ennen tarjouksen muuntamista myyntilaskuksi. |[Myyntitarjousten tekeminen](sales-how-make-offers.md) |
| Luot myyntilaskun tallentaaksesi sopimuksesi asiakkaan kanssa ja myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla. |[Myynnin laskutus](sales-how-invoice-sales.md) |
| Käsittele osittaista toimitusta tai suoratoimitusta käsittelevä myyntitilaus. |[Tuotteiden myyminen](sales-how-sell-products.md) |
|Määritä vakiomyynti- tai -ostorivit, jotka voit lisätä nopeasti asiakirjoihin, kuten toistuviin täydennystilauksiin.|[Toistuvien myynti- ja ostorivien luominen](sales-how-work-standard-lines.md)|  
| Linkitä myyntitilaus ostotilaukseen, jotta voit myydä suoratoimituksen nimikkeen, joka toimitetaan suoraan toimittajaltasi asiakkaallesi. |[Suoratoimitusten tekeminen](sales-how-drop-shipment.md) |
|Luettelonimike on toimitettava toimittajalta fyysiseen varastoon, jotta voit toimittaa nimikkeen asiakkaallesi.|[Erikoistilausten luominen](sales-how-to-create-special-orders.md)|
| Suorita toiminto maksamattomalle kirjatulle myyntilaskulle hyvityslaskun automaattiseksi luomiseksi ja joko peruuta myyntilasku tai luo se uudelleen, jotta voit tehdä korjauksia. |[Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](sales-how-correct-cancel-sales-invoice.md) |
| Luo myyntihyvityslasku palauttamaan vastaamaan määrätty kirjattu myyntilasku heijastamaan sitä, mitä tuotteita asiakas palauttaa toimittajalle ja minkä maksusumman palautat. |[Myynnin palautusten tai peruutusten käsittely](sales-how-process-sales-returns-cancellations.md) |
|Voit hallita asiakkaan suurta määrää koskevaa ostositoumusta, joka toimitetaan useassa erässä tietyn ajan kuluessa.|[Puitemyyntitilausten käyttäminen](sales-how-to-create-blanket-sales-orders.md)|
|Myy kokoonpanon nimikkeet, jotka eivät ole tällä hetkellä saatavilla, luomalla linkitetty kokoonpanotilaus toimittamaan myyntilauksen koko määrä tai sen osa.|[Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md)|
|Laskuta asiakasta vain kerran yhdistämällä useiden toimitusten toimitukset yhteen laskuun.|[Toimitusten yhdistäminen yhteen laskuun](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Ilmoitta tilauksen toimiaika asiakkaille laskemalla joko mahdollinen luvattavaksi- tai luvattavissa -päivämäärä.|[Toimituksen lupaamisen päivämäärien laskeminen](sales-how-to-calculate-order-promising-dates.md)|
|Rekisteröi nimike- ja kausikohtaisesti määritetyt tulevan myynnin arviot, jotka toimivat lähinnä tuotantosuunnittelun syöttötietoina.|[Ennusteen luominen](production-how-to-create-a-forecast.md)|
|Ratkaise ristiriita, kun samalla asiakkaalla on ainakin kaksi tietuetta.|[Tietueiden kaksoiskappaleiden yhdistäminen](sales-how-merge-duplicate-records.md)|

## <a name="see-also"></a>Katso myös
[Myynnin määrittäminen](sales-setup-sales.md)  
[Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Projektinhallinta](projects-manage-projects.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
