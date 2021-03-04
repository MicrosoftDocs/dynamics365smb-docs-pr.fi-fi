---
title: Rakennetiedot – Fyysisen varastoinnin yleiskatsaus | Microsoft Docs
description: Fyysisen varaston jokaisen tapahtuman ja siirron tiedot on voitava jäljittää, jotta nimikkeiden fyysistä käsittelyä voidaan tukea alue- ja varastopaikkatasolla. Tätä hallitaan **F. var. tapahtuma** -taulukossa. Jokainen tapahtuma tallennetaan varastorekisteriin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8842bd23f6d2d470599afe9b4382b35cec3d9251
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749541"
---
# <a name="design-details-warehouse-overview"></a>Rakennetiedot: f. varaston yleiskuvaus
Fyysisen varaston jokaisen tapahtuman ja siirron tiedot on voitava jäljittää, jotta nimikkeiden fyysistä käsittelyä voidaan tukea alue- ja varastopaikkatasolla. Tätä hallitaan **F. var. tapahtuma** -taulukossa. Jokainen tapahtuma tallennetaan varastorekisteriin.  

Fyysisen varastoinnin asiakirjoja ja fyysisen varastoinnin päiväkirjaa käytetään fyysisen varastoinnin nimikesiirtojen rekisteröimisessä. Jokaisen f. varaston nimikkeen siirron, vastaanoton, hyllytyksen, poiminnan, toimituksen tai muutoksen yhteydessä tapahtumat rekisteröidään tallentamaan fyysiset tiedot vyöhykkeestä, lokerosta ja määrästä.

**Bin-tiedoston sisältö** -taulukkoa käytetään käsiteltäessä kaikkia eri sisältödimensioita bineissä nimikettä kohden, kuten mittayksikkö, maksimimäärä ja minimimäärä. **Binin sisältö** -taulukko sisältää myös virtauskentät varastokirjauksiin, varaston ohjeisiin ja varaston lokiriveihin, mikä varmistaa sen, että nimikkeen saatavuus biniä kohden ja nimikkeen bin voidaan laskea nopeasti. Lisätietoja on kohdassa [Rakennetiedot: Saatavuus varastossa.](design-details-availability-in-the-warehouse.md)  

Kun nimikkeiden kirjaukset tapahtuvat fyysisen varastoinnin moduulin ulkopuolella, fyysisen varastoinnin tapahtumat ja varastotapahtumat synkronoidaan sijaintikohtaisten muutosten oletusvarastopaikan avulla. Varaston fyysisen inventoinnin aikana kaikki määritetyt ja lasketut määrät tallennetaan muutoslokeroon ja kirjataan tämän jälkeen korjaavina nimiketapahtumina. Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Integrointi varaston kanssa](design-details-integration-with-inventory.md).  

Seuraavassa kuvassa on luonnosteltu tyypillinen varaston kulku.  

![Varastoprosessien yleiskatsaus](media/design_details_warehouse_management_overview.png "Varastoprosessien yleiskatsaus")  

## <a name="basic-or-advanced-warehousing"></a>Perus tai lisävarastointi  
[!INCLUDE[prod_short](includes/prod_short.md)]in varastotoiminto voidaan toteuttaa yrityksen prosessien ja tilausmäärän mukaan valittavalla monimutkaisuustasolla. Pääero on, että toiminnot suoritetaan tilaus tilaukselta perusvarastoinnissa, kun ne yhdistetään useisiin tilauksiin kehittyneessä varastoinnissa.  

 Eri monimutkaisuuden tasojen erottamista varten tässä dokumentaatiossa käsitellään kahta yleistä nimitystä: Perus ja Lisävarastointi. Tämä yksinkertainen erottaminen kattaa tuoteosion ja sijainnin asetusten määrittämät monimutkaisuuden useat eri tasot, joita tukevat erilaiset käyttöliittymäasiakirjat. Katso lisätietoja kohdasta [Rakennetiedot: f. varaston asetus](design-details-warehouse-setup.md).  

> [!NOTE]  
>  Varaston kehittyneintä tasoa kutsutaan tässä asiakirjassa nimellä "WMS-asennukset", koska tämä taso vaatii kehittyneimmän yksikön, Warehouse Management Systems.  

 Seuraavia eri käyttöliittymäasiakirjoja käytetään perus- ja kehittyneessä varastoinnissa.  

## <a name="basic-ui-documents"></a>Peruskäyttöliittymäasiakirjat  

-   **Varastohyllytys**  
-   **Varaston poiminta**  
-   **Varaston siirto**  
-   **Nimikepäiväkirja**  
-   **Nimikkeen uudelleenluokituspäiväkirja**  
-   (Eri raportit)  

## <a name="advanced-ui-documents"></a>Käyttöliittymän lisäasiakirjat  

-   **F. varastoinnin vastaanotto**  
-   **Hyllytystyökirja**  
-   **F.varastoinnin hyllytys**  
-   **Poimintatyökirja**  
-   **F.varastoinnin poiminta**  
-   **Siirtotyökirja**  
-   **F. var. siirto**  
-   **Sisäinen f.var. poim.**  
-   **Sisäinen f.var. hyllytys**  
-   **Var.paikan luontityökirja**  
-   **Var.p. sisällön luontityökirja**  
-   **F.var. nimikepvk**  
-   **Var. nimik. uud.luok.pvk**  
-   (Eri raportit)  

Katso lisätietoja jokaisesta asiakirjasta kunkin sivun aiheista.  

### <a name="terminology"></a>Termit  
[!INCLUDE[prod_short](includes/prod_short.md)]in fyysisen varastoinnin ohjeistus käyttää seuraavia ostojen ja myyntien talouskäsitteiden mukaisia varaston nimikevirran termejä.  

|Kausi|Description|  
|----------|---------------------------------------|  
|Saapuva virta|Fyysisen varaston sijaintiin siirtyvät nimikkeet, kuten ostot ja saapuvat siirrot.|  
|Sisäinen virta|Fyysisen varaston sijainnin sisällä siirtyvät nimikkeet, kuten tuotantokomponentit ja tuotos.|  
|Lähtevä virta|Fyysisen varaston sijainnista ulos siirtyvät nimikkeet, kuten myynnit ja lähtevät siirrot.|  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]