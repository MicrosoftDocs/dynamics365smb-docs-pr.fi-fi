---
title: "Valuutan vaihtokurssien päivittäminen| Microsoft Docs"
description: "Voit käyttää yrityksessä useita valuuttoja määrittämällä kullekin valuutalle koodin ja käyttämällä ulkoista vaihtokurssipalvelua, kuten FloatRatesia."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 23940bd1e5fd29dc92e8285c08679135889701e9
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="update-currency-exchange-rates"></a>Valuutan vaihtokurssien päivittäminen
Kaikille valuutoille täytyy määrittää koodi, jos yritys ostaa tai myy käyttäen jotain muuta valuuttaa kuin paikallista valuuttaa, jos yrityksellä on myyntisaamisia tai ostovelkoja muissa valuutoissa; tai jos yritys tallentaa KP-kauppatapahtumia eri valuuttoina.  

Yritysten toiminnan ollessa yhä useamman maan/alueen laajuista niiden on entistä tärkeämpää pystyä tarkistamaan ja raportoimaan taloustiedot useana valuuttana. Ohjelma tukee usean valuutan käyttöä. Ohjelman sisällä pääkirjanpito määritetään käyttäen paikallista valuuttaa (PVA) ja toinen valuutta määritetään lisävaluutaksi, jolle asetetaan ajantasainen vaihtokurssi.  

 Määrittämällä toisen valuutan lisäraportointivaluutaksi [!INCLUDE[d365fin](includes/d365fin_md.md)] kirjaa summat automaattisesti sekä paikallisena valuuttana että lisäraportointivaluuttana kuhunkin KP-tapahtumaan sekä muihin tapahtumiin, kuten ALV-tapahtumiin. Kun KP-tapahtumien summat lasketaan lisäraportointivaluuttana, oikea vaihtokurssi etsitään **Valuutan vaihtokurssit** -sivun tietoja avulla.  

> [!WARNING]  
>  Lisäraportointivaluutta-toimintoa EI saa käyttää rahoituslaskelmien käännösten perustana. Tällä työkalulla ei pysty kääntämään ulkomaisten tytäryritysten tilinpäätöksiä osana yrityksen konsolidointia. Lisäraportointivaluutta antaa ainoastaan mahdollisuuden laatia raportteja muuta valuuttaa käyttäen, ikään kuin tämä valuutta olisi yrityksen paikallinen valuutta.

## <a name="adjusting-exchange-rates"></a>Vaihtokurssien muuttaminen  
Koska vaihtokurssit vaihtelevat jatkuvasti, järjestelmän lisävaluutta-arvot on tarkistettava jaksoittain. Jos tarkistuksia ei tehdä, ulkomaisista valuutoista (tai lisävaluutoista) muunnetut summat voivat olla harhaanjohtavia, kun ne kirjataan pääkirjanpitoon PVA:na. Lisäksi päivittäiset tapahtumat, jotka on kirjattu ennen päivittäisen vaihtokurssin lisäämistä ohjelmaan, on päivitettävä, kun päivittäinen vaihtokurssi on lisätty. Muuta vaihtokursseja -eräajon avulla voi muuttaa kirjattujen asiakas-, toimittaja- ja pankkitilitapahtumien vaihtokursseja. Sen avulla voi myös päivittää KP-tapahtumien lisäraportointivaluutan summia.  

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a>Raporttien ja summien näyttäminen lisäraportointivaluuttana  
Lisäraportointivaluutan käyttäminen voi helpottaa yrityksen raportointiprosessia seuraavissa tapauksissa:  

- Yritys toimii EU:n ulkopuolella ja suuri osa sen liiketoimista tapahtuu EU:ssa toimivien yritysten kanssa. Tässä tapauksessa EU:n ulkopuolisen yrityksen kannattaa ehkä raportoida euroina, jotta sen finanssiraportit olisivat helpommin EU-liikekumppanien käytettävissä.  

- Yritys haluaa esittää raporttinsa oman paikallisen valuuttansa lisäksi myös laajemmin kansainvälisesti käytetyssä valuutassa.  

Monet Pääkirjanpito-sovellusalueen raportit perustuvat KP-tapahtumiin. Voit näyttää raportin taloudelliset tiedot lisäraportointivaluuttana valitsemalla vain **Näytä lisäraportointivaluuttana** -kentän kyseisessä KP-raportti-sivulla.  

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Valuutanvaihdon kurssipalvelun määrittäminen
Voit pitää valuutan vaihtokurssit ajan tasalla ulkoisen palvelun, kuten FloatRatesin avulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Valuutanvaihtokurssipalvelut** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät **Valuutanvaihtokurssipalvelut**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Ota palvelu käyttöön valitsemalla **Käytössä**.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Valuutan vaihtokurssien päivittäminen palvelun avulla
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Valuutat** ja valitse sitten liittyvä linkki.
2. Valitse **Päivitä valuutan vaihtokurssit** -toiminto.

**Valuutat**-sivun **Vaihtokurssi**-kentän arvo päivittyy uusimman valuutan vaihtokurssin mukaan.

## <a name="see-also"></a>Katso myös
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

