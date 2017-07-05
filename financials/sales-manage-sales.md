---
title: Myynti| Microsoft Docs
description: "Tässä artikkelissa määritetään, miten myyntiaktiviteetteja hallitaan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell
ms.date: 04/27/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d8b73dcf1ee000bd13aec200c82275eb3c0f9d1d
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="sales"></a>Myynti
Luo myyntilasku tai -tilaus tallentaaksesi sopimuksesi asiakkaan kanssa ja myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla.

Myyntitilauksia on käytettävä, jos myyntiprosessi vaatii tilausmäärän osittaisen toimittamisen esimerkiksi silloin, kun koko määrä ei ole kerralla käytettävissä. Jos myyt nimikkeitä toimittamalla ne suoraan toimittajalta asiakkaalle (suoratoimituksena), myyntitilauksia on käytettävä. Kaikilta muilta osin myyntitilaukset toimivat samalla tavalla kuin myyntilaskut.

Tärkeintä hyvissä myynti- ja markkinointikäytännöissä on tehdä oikeita päätöksiä oikeaan aikaan. [!INCLUDE[d365fin](includes/d365fin_md.md)]in markkinointitoiminnot tarjoavat yhteystietojen yleiskuvauksen tarkasti ja oikea-aikaisesti, mikä tehostaa mahdollisten asiakkaiden palvelemista ja parantaa asiakastyytyväisyyttä. Lisätietoja on kohdassa [Kontaktienhallinta](marketing-relationship-management.md).

Voit neuvotella asiakkaan kanssa luomalla ensin myyntitarjoukseen, jonka voit muuntaa myyntilaskuksi, kun hyväksyt myynnin. Sen jälkeen, kun asiakas on vahvistanut sopimuksen, esimerkiksi tarjousprosessin jälkeen, voit lähettää tilausvahvistuksen ja tallentaa velvollisuutesi toimittaa tuotteet sovitun mukaisesti.

Kun toimitat tuotteita kokonaan tai osittain, kirjaa myyntilasku tai -tilaus toimitetuksi tai toimitetuksi ja laskutetuksi. Näin järjestelmään luodaan liittyvä nimike ja asiakastapahtumat.

Liiketoimintaympäristöissä, joissa asiakkaan on maksettava ennen kuin tuotteet toimitetaan, kuten vähittäismyynti, sinun on odotettava maksukuittia ennen kuin toimitat tuotteet. Useimmissa tapauksissa saapuvia maksuja käsitellään joitakin viikkoja toimituksen jälkeen kohdistamalla maksut niihin liittyviin kirjattuihin ja maksamattomiin myyntilaskuihin. Lisätietoja on kohdassa [Toimintaohje: Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

Voit helposti korjata tai peruuttaa kirjatun myyntilaskun ennen kuin se on maksettu. Tästä on hyötyä, jos haluat korjata kirjoitusvirheen tai jos asiakas pyytää muutosta prosessin alkuvaiheessa. Jos kirjattu myyntilasku maksetaan, sinun on luotava myyntihyvityslasku kaupan peruuttamiseksi.

Myyntiasiakirjat voidaan lähettää sähköpostin liitteenä PDF-tiedostoina. Sähköpostin perusteksti sisältää otteen myyntiasiakirjasta. Ote voi sisältää esimerkiksi tuotteet, kokonaissumman ja PayPal-sivuston linkin. Lisätietoja on kohdassa [Toimintaohje: Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md).

Voit ottaa hyväksymistyönkulun käyttöön kaikissa myyntiprosesseissa esimerkiksi silloin, kun pyydät talouspäälliköltä hyväksyntää isolle myynnille tiettyä asiakasta varten. Lisätietoja on kohdassa [Hyväksymistyönkulkujen käyttäminen](across-how-use-approval-workflows.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.

| Toiminta | Katso |
| --- | --- |
| Luo myyntitarjous, jos tarjoat tuotteita siirtokelpoisilla ehdoilla ennen tarjouksen muuntamista myyntilaskuksi. |[Toimintaohje: Tarjousten tekeminen](sales-how-make-offers.md) |
| Luot myyntilaskun tallentaaksesi sopimuksesi asiakkaan kanssa ja myydäksesi määrätyt tuotteet määrätyillä toimitus- ja maksuehdoilla. |[Toimintaohje: Myynnin laskutus](sales-how-invoice-sales.md) |
| Käsittele osittaista toimitusta tai suoratoimitusta käsittelevä myyntitilaus. |[Toimintaohje: Tuotteiden myyminen](sales-how-sell-products.md) |
| Linkitä myyntitilaus ostotilaukseen, jotta voit myydä suoratoimituksen nimikkeen, joka toimitetaan suoraan toimittajaltasi asiakkaallesi. |[Toimintaohje: Suoratoimitusten tekeminen](sales-how-drop-shipment.md) |
| Suorita toiminto maksamattomalle kirjatulle myyntilaskulle hyvityslaskun automaattiseksi luomiseksi ja joko peruuta myyntilasku tai luo se uudelleen, jotta voit tehdä korjauksia. |[Toimintaohje: Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](sales-how-correct-cancel-sales-invoice.md) |
| Luo myyntihyvityslasku palauttamaan vastaamaan määrätty kirjattu myyntilasku heijastamaan sitä, mitä tuotteita asiakas palauttaa toimittajalle ja minkä maksusumman palautat. |[Toimintaohje: Myynnin palautuksen tai peruutuksen käsittely](sales-how-process-sales-returns-cancellations.md) |
| Luo asiakkaan kortti jokaiselle asiakkaalle, jolle myyt. |[Toimintaohje: Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md) |

## <a name="see-also"></a>Katso myös
[Myynnin määrittäminen](sales-setup-sales.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Ostovelkojen hallinta](payables-manage-payables.MD)  
[Projektinhallinta](projects-manage-projects.md)    
[Toimitusketju](madeira-supply-chain.md)      
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]