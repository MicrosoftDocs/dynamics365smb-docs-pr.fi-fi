---
title: Päivitä Valuutanvaihtokurssit | Microsoft Docs
description: Seuraa summia eri valuutoissa valuuttakoodeja käyttäen ja anna Bussiness Centralin auttaa sinua säätämään vaihtokursseja julkaistuille merkinnöille ulkoisen palvelun avulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: multiple currencies, adjust exchange rates
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6e9456a17ccf8dc6c3e3e8ae8272baa03f43f7da
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882660"
---
# <a name="update-currency-exchange-rates"></a>Valuutan vaihtokurssien päivittäminen
Yritysten toiminnan sijoittuessa yhä useamman maan/alueen alueelle niiden on entistä tärkeämpää pystyä tekemään kauppaa ja raportoimaan taloustiedot useana valuuttana. Kaikille valuutoille täytyy määrittää koodi, jos yritys ostaa tai myy käyttäen jotain muuta valuuttaa kuin paikallista valuuttaa, jos yrityksellä on myyntisaamisia tai ostovelkoja muissa valuutoissa; tai jos yritys tallentaa KP-kauppatapahtumia eri valuuttoina.

Pääkirjanpito määritetään käyttämään paikallista valuuttaa (PVA), mutta voit määrittää sen käyttämään myös toista valuuttaa, jolle määritetään ajantasainen vaihtokurssi. Kun toinen valuutta määritetään niin sanotuksi lisäraportointivaluutaksi, [!INCLUDE[d365fin](includes/d365fin_md.md)] tallentaa summat automaattisesti sekä PVA:na että lisäraportointivaluuttana kuhunkin KP-tapahtumaan sekä muihin tapahtumiin, kuten ALV-tapahtumiin. Lisätietoja on kohdassa [Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Vaihtokurssien muuttaminen
Koska vaihtokurssit vaihtelevat jatkuvasti, järjestelmän lisävaluutta-arvot on tarkistettava jaksoittain. Jos tarkistuksia ei tehdä, ulkomaisista valuutoista (tai lisävaluutoista) muunnetut summat voivat olla harhaanjohtavia, kun ne kirjataan pääkirjanpitoon PVA:na. Lisäksi päivittäiset tapahtumat, jotka on kirjattu ennen päivittäisen vaihtokurssin lisäämistä sovellukseen, on päivitettävä, kun päivittäinen vaihtokurssi on lisätty.

**Muuta vaihtokursseja** -eräajon avulla voi muuttaa manuaalisesti kirjattujen asiakas-, toimittaja- ja pankkitilitapahtumien vaihtokursseja. Sen avulla voi myös päivittää KP-tapahtumien lisäraportointivaluutan summia. Voit muuttaa vaihtokursseja myös automaattisesti käyttämällä palvelua. Lisätietoja on kohdassa [Valuutanvaihdon kurssipalvelun määrittäminen](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

### <a name="effect-on-customers-and-vendors"></a>Vaikutus asiakkaisiin ja toimittajiin
Asiakkaan ja toimittajan tileillä eräajo muuttaa valuutan käyttäen sitä vaihtokurssia, joka on kirjauspäivämääränä voimassa eräajossa. Eräajo laskee yksittäisten valuuttasaldojen erot ja kirjaa summat sille kirjanpitotilille, joka on määritetty **Valuutat**-sivun **Ei-realisoit. val.voitt. tili** -kentässä tai **Ei-realisoit. val.voitt. tili** -kentässä. Vastatapahtumat kirjataan automaattisesti ostoreskontran/myyntireskontran tilille pääkirjanpidossa.

Eräajo käsittelee kaikki avoimet asiakas- ja toimittajatapahtumat. Jos tapahtumassa on valuuttaero, eräajo luo uuden, eritellyn asiakas- tai toimittajatapahtuman, josta näkyy muutettu summa asiakas- tai toimittajatapahtumassa.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Asiakas- ja toimittajatapahtumien dimensiot
Muutostapahtumille on määritetty dimensiot asiakas-/toimittajatapahtumilta, ja muutokset on kirjattu dimensioarvojen kombinaatioiden mukaan.

### <a name="effect-on-bank-accounts"></a>Vaikutus pankkitileihin
Pankkitileillä eräajo muuttaa valuutan käyttäen sitä vaihtokurssia, joka on kirjauspäivämääränä voimassa eräajossa. Eräajo laskee eron jokaiselle tilille, jolla on valuuttakoodi ja kirjaa summat sille kirjanpitotilille, joka on määritetty **Valuutat**-sivun **Realisoitun. val.voitt. tili** -kentässä tai **Realisoit. val.tapp. tili** -kentässä. Vastatapahtumat kirjataan automaattisesti niille KP:n pankkitileille, jotka on määritelty pankkitilien postitusryhmissä. Eräajo laskee yhden tapahtuman valuuttaa ja kirjausryhmää kohden.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensiot pankkitilitapahtumilla
Muutostapahtumien pankkitilin KP-tilille ja voitto/tappio tileille määritetään oletusdimensiot.

### <a name="effect-on-gl-accounts"></a>Vaikutus KP-tileihin
Jos kirjaat lisäraportointivaluutan, voit eräajon avulla luoda uusia KP-tapahtumia PVA:n ja lisäraportointivaluutan välillä tapahtuvia kurssimuutoksia varten. Eräajo laskee jokaisen kirjanpitotapahtuman erotuksen ja muuttaa kirjanpitotapahtumaa sen mukaan, mitä **Vaihtokurssin muutos** -kentässä lukee kirjanpitotilin kohdalla.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensiot KP-tilin tapahtumille
Muutostapahtumille on määritetty niiden KP-tilien dimensiot, joille ne on kirjattu.

> [!Important]
> Syötä ennen eräajon käyttämistä vaihtokurssit, joita käytetään ulkomaisen valuutan saldoja muutettaessa. Se tehdään **Valuutan vaihtokurssit** -sivulla.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Valuutanvaihdon kurssipalvelun määrittäminen
Voit pitää valuutan vaihtokurssit ajan tasalla ulkoisen palvelun, kuten FloatRatesin avulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Valuutanvaihtokurssipalvelut** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät **Valuutanvaihtokurssipalvelut**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Ota palvelu käyttöön valitsemalla **Käytössä**.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Valuutan vaihtokurssien päivittäminen palvelun avulla
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Valuutat** ja valitse sitten liittyvä linkki.
2. Valitse **Päivitä valuutan vaihtokurssit** -toiminto.

**Valuutat**-sivun **Vaihtokurssi**-kentän arvo päivittyy uusimman valuutan vaihtokurssin mukaan.

## <a name="see-also"></a>Katso myös
[Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md)  
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
