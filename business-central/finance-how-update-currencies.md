---
title: Valuutan vaihtokurssien päivittäminen
description: Seuraa summia eri valuutoissa valuuttakoodeja käyttäen ja anna Bussiness Centralin auttaa sinua säätämään vaihtokursseja julkaistuille merkinnöille ulkoisen palvelun avulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: multiple currencies, adjust exchange rates
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d6132d84909509a76b196d6ae20d1fb8a2566309
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782303"
---
# <a name="update-currency-exchange-rates"></a>Valuutan vaihtokurssien päivittäminen

Yritysten toiminnan sijoittuessa yhä useamman maan/alueen alueelle niiden on entistä tärkeämpää pystyä tekemään kauppaa ja raportoimaan taloustiedot useana valuuttana. Kaikille valuutoille täytyy määrittää koodi, jos yritys ostaa tai myy käyttäen jotain muuta valuuttaa kuin paikallista valuuttaa, jos yrityksellä on myyntisaamisia tai ostovelkoja muissa valuutoissa; tai jos yritys tallentaa KP-kauppatapahtumia eri valuuttoina.

Pääkirjanpito määritetään käyttämään paikallista valuuttaa (PVA), mutta voit määrittää sen käyttämään myös toista valuuttaa, jolle määritetään ajantasainen vaihtokurssi. Kun toinen valuutta määritetään niin sanotuksi lisäraportointivaluutaksi, [!INCLUDE[prod_short](includes/prod_short.md)] tallentaa summat automaattisesti sekä PVA:na että lisäraportointivaluuttana kuhunkin KP-tapahtumaan sekä muihin tapahtumiin, kuten ALV-tapahtumiin. Lisätietoja on kohdassa [Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Vaihtokurssien muuttaminen

Koska vaihtokurssit vaihtelevat jatkuvasti, järjestelmän lisävaluutta-arvot on tarkistettava jaksoittain. Jos tarkistuksia ei tehdä, ulkomaisista valuutoista (tai lisävaluutoista) muunnetut summat voivat olla harhaanjohtavia, kun ne kirjataan pääkirjanpitoon PVA:na. Lisäksi päivittäiset tapahtumat, jotka on kirjattu ennen päivittäisen vaihtokurssin lisäämistä sovellukseen, on päivitettävä, kun päivittäinen vaihtokurssi on lisätty.

**Muuta vaihtokursseja** -eräajon avulla voi muuttaa manuaalisesti kirjattujen asiakas-, toimittaja- ja pankkitilitapahtumien vaihtokursseja. Sen avulla voi myös päivittää KP-tapahtumien lisäraportointivaluutan summia.  

> [!TIP]
> Voit käyttää palvelua vaihtokurssien päivittämiseen automaattisesti järjestelmässä. Lisätietoja on kohdassa [Valuutanvaihdon kurssipalvelun määrittäminen](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Jos kirjattujen tapahtumien vaihtokursseja ei kuitenkaan silloin muuteta. Voit päivittää kirjattujen tapahtumien vaihtokurssit käyttämällä **Muuta vaihtokursseja** -erätyötä.

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

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Valuutanvaihdon kurssipalvelun määrittäminen
Voit pitää valuutan vaihtokurssit ajan tasalla ulkoisen palvelun, kuten FloatRatesin avulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Valuutanvaihtokurssipalvelut** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät **Valuutanvaihtokurssipalvelut**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Ota palvelu käyttöön valitsemalla **Käytössä**.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Valuutan vaihtokurssien päivittäminen palvelun avulla
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Valuutat** ja valitse sitten liittyvä linkki.
2. Valitse **Päivitä valuutan vaihtokurssit** -toiminto.

**Valuutat**-sivun **Vaihtokurssi**-kentän arvo päivittyy uusimman valuutan vaihtokurssin mukaan.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös
[Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md)  
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]