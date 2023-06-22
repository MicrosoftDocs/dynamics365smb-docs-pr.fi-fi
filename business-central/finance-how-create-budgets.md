---
title: Luodaan KP-budjetteja
description: 'Tässä artikkelissa käsitellään, miten luodaan KP-budjetteja ennustamaan erilaisia taloudellisia toimintoja ja miten dimensiot määritetään liiketoimintatietoja varten.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 08/24/2022
ms.author: edupont
---
# <a name="create-gl-budgets" />KP-budjettien luominen

Sinulla voi olla useita budjetteja samalle ajanjaksolle, kun luot budjetit eri nimillä. Määrittele ensin budjetin nimi ja syötä budjettiluvut. Budjetin nimi tulee sitten kaikkiin luomiisi budjettitapahtumiin.  

Kun luot budjetin, voit määrittää kullekin budjetille neljä budjettikohtaista dimensiota, joita kutsutaan budjettidimensioiksi. Valitse budjettidimensiot niistä, jotka olet jo luonut. Budjettidimensioita voidaan käyttää, kun halutaan asettaa suodatin budjetille tai kun halutaan lisätä dimensiotietoa budjettitapahtumiin. Lisätietoja on kohdassa [Dimensioiden käsitteleminen](finance-dimensions.md).

Talousarviolla on tärkeä rooli liiketoiminnan älykkyyteen. Esimerkkejä ovat tilinpäätös, joka perustuu talousraportteihin, jotka sisältävät budjettimerkintöjä, tai kun analysoidaan budjetoituja ja todellisia summia tilikartassa. Lisätietoja on kohdassa [Business Intelligence](bi.md).

Voit käsitellä kustannusbudjetteja samalla tavoin kustannuslaskennassa. Lisätietoja on kohdassa [Kulubudjettien luominen](finance-create-cost-budgets.md).  

## <a name="to-create-a-new-gl-budget" />Uuden KP-budjetin luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KP-budjetit** ja valitse sitten vastaava linkki.  
2. Valitse **Muokkaa luetteloa** -toiminto, täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Valitse **Muokkaa budjettia** -toiminto.
4. Täyttämällä **Budjetti**-sivun yläosan kentät määrität, mitä näytetään.  

    Näytössä näkyvät vain ne tapahtumat, joilla on **Budjetin nimi** -kentässä annettu nimi. Koska budjetin nimi on juuri luotu, suodatinta vastaavia tapahtumia ei ole. Tämän vuoksi sivu on tyhjä.  
5. Jos haluat lisätä summan, napsauta solua matriisissa. **KP-budjetin tapahtumat** -sivu avautuu.  
6. Luo uusi rivi ja määritä **Summa**-kentän arvo. Sulje **KP-budjetin tapahtumat** -sivu.  
7. Toista vaiheet 5 ja 6, kunnes olet määrittänyt kaikki budjettisummat.  

> [!NOTE]  
> **Suodattimet** -pikavälilehdessä voit suodattaa budjettitietoja sen mukaan, mitä budjettidimensioita olet luonut budjetin nimen alle.

## <a name="exporting-and-importing-gl-budgets-with-excel" />KP-budjettien vieminen ja tuominen Excelissä

Niin kuin käytännössä kaikkia muitakin sivuja voit viedä budjettisivujen tiedot Microsoft Exceliin lisäkäsittelyä tai -analyysia varten. Lue lisää kohdasta [Liiketoimintatietojen vieminen Exceliin](about-export-data.md).

> [!NOTE]
> Tilikartassa, johon KP-budjetit perustuvat, on Otsikko-tilityypin rivejä, joissa ilmoitetaan otsikon alla olevien rivien määrä. Kun viet KP-budjetin, kaikkien rivien tiedot viedään tilityypistä riippumatta. Kuitenkin vain Kirjaus-tilityypin rivien tiedot voida tuoda takaisin. 

Siispä, kun tuot KP-budjetin, kaikki Otsikko-riveillä olevat arvot poistetaan. Tällä tavoin estetään virheelliset yhteissummat sen jälkeen, kun Excelissä luotuja tai muokattuja tietoja on tuotu.

### <a name="scenario" />Skenaario

Tiedät, että uudet budjetoidut palkkakustannukset tulevat olemaan paikallisena valuuttana (PVA:na) 1 200 000. Haluat antaa palkkaosaston budjetoida kolmelle erityiselle riville (kirjaustilityyppi) kokoaikaisille työntekijöille, osa-aikaisille työntekijöille ja tilapäiselle avustajalle. Nämä kolme riviä ryhmitellään Palkat-otsikkorivin kohdalle.

Lisää 1 200 000 Otsikko-riville, vie budjetti Exceliin ja lähetä se sitten palkkaosastolle ja pyydä heitä jakamaan PVA 1 200 000.

Palkkaosasto jakaa summan kolmelle kirjaustilille. Kun tuot KP-budjetin takaisin, uudet Excel-tiedot on täytetty kolmelle tilille. Niiden summa on PVA 1 200 000 ja otsikkorivi on tyhjä.

## <a name="see-related-microsoft-trainingtrainingmodulesbudgets-exchange-rates-dynamics--business-centralindex" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also" />Katso myös

[Liiketoimintatietojen vienti Exceliin](about-export-data.md)  
[Rahoitus](finance.md)  
[Business Intelligence](bi.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
