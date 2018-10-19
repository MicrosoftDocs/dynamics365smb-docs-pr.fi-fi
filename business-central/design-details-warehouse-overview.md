---
title: "Rakennetiedot – Fyysisen varastoinnin yleiskatsaus | Microsoft Docs"
description: "Fyysisen varaston jokaisen tapahtuman ja siirron tiedot on voitava jäljittää, jotta nimikkeiden fyysistä käsittelyä voidaan tukea alue- ja varastopaikkatasolla. Tätä hallitaan **F. var. tapahtuma** -taulukossa. Jokainen tapahtuma tallennetaan varastorekisteriin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: cea5bb76f8fdb8c9c52a5f341d29a34bcb8f0cdc
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-warehouse-overview"></a>Rakennetiedot: f. varaston yleiskuvaus
Fyysisen varaston jokaisen tapahtuman ja siirron tiedot on voitava jäljittää, jotta nimikkeiden fyysistä käsittelyä voidaan tukea alue- ja varastopaikkatasolla. Tätä hallitaan **F. var. tapahtuma** -taulukossa. Jokainen tapahtuma tallennetaan varastorekisteriin.  

Fyysisen varastoinnin asiakirjoja ja fyysisen varastoinnin päiväkirjaa käytetään fyysisen varastoinnin nimikesiirtojen rekisteröimisessä. Jokaisen f. varaston nimikkeen siirron, vastaanoton, hyllytyksen, poiminnan, toimituksen tai muutoksen yhteydessä tapahtumat rekisteröidään tallentamaan fyysiset tiedot vyöhykkeestä, lokerosta ja määrästä. Lisätietoja on kohdassa [Rakennetiedot: Saapuva fyysisen varastoinnin virta](design-details-outbound-warehouse-flow.md).  

**Bin-tiedoston sisältö** -taulukkoa käytetään käsiteltäessä kaikkia eri sisältödimensioita bineissä nimikettä kohden, kuten mittayksikkö, maksimimäärä ja minimimäärä. **Binin sisältö** -taulukko sisältää myös virtauskentät varastokirjauksiin, varaston ohjeisiin ja varaston lokiriveihin, mikä varmistaa sen, että nimikkeen saatavuus biniä kohden ja nimikkeen bin voidaan laskea nopeasti. Lisätietoja on kohdassa [Rakennetiedot: Saatavuus varastossa.](design-details-availability-in-the-warehouse.md)  

Kun nimikkeiden kirjaukset tapahtuvat fyysisen varastoinnin moduulin ulkopuolella, fyysisen varastoinnin tapahtumat ja varastotapahtumat synkronoidaan sijaintikohtaisten muutosten oletusvarastopaikan avulla. Varaston fyysisen inventoinnin aikana kaikki määritetyt ja lasketut määrät tallennetaan muutoslokeroon ja kirjataan tämän jälkeen korjaavina nimiketapahtumina. Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Integrointi varaston kanssa](design-details-integration-with-inventory.md).  

Seuraavassa kuvassa on luonnosteltu tyypillinen varaston kulku.  

![Varastointiprosessien yleiskatsaus](media/design_details_warehouse_management_overview.png "Varastointiprosessien yleiskatsaus")  

## <a name="basic-or-advanced-warehousing"></a>Perus tai lisävarastointi  
[!INCLUDE[d365fin](includes/d365fin_md.md)]in varastotoiminto voidaan toteuttaa yrityksen prosessien ja tilausmäärän mukaan valittavalla monimutkaisuustasolla. Pääero on, että toiminnot suoritetaan tilaus tilaukselta perusvarastoinnissa, kun ne yhdistetään useisiin tilauksiin kehittyneessä varastoinnissa.  

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

Katso lisätietoja jokaisesta asiakirjasta kunkin ikkunan aiheista.  

### <a name="terminology"></a>Termit  
[!INCLUDE[d365fin](includes/d365fin_md.md)]in fyysisen varastoinnin ohjeistus käyttää seuraavia ostojen ja myyntien talouskäsitteiden mukaisia varaston nimikevirran termejä.  

|Kausi|Description|  
|----------|---------------------------------------|  
|Saapuva virta|Fyysisen varaston sijaintiin siirtyvät nimikkeet, kuten ostot ja saapuvat siirrot.|  
|Sisäinen virta|Fyysisen varaston sijainnin sisällä siirtyvät nimikkeet, kuten tuotantokomponentit ja tuotos.|  
|Lähtevä virta|Fyysisen varaston sijainnista ulos siirtyvät nimikkeet, kuten myynnit ja lähtevät siirrot.|  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)

