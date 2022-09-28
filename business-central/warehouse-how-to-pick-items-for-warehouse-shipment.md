---
title: Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten
description: Tietoja fyysisen varaston poiminta-asiakirjojen käyttämisestä poimintatietojen luomista ja käsittelyä varten ennen fyysisen varaston toimituksen kirjaamista.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 23a730f79e3b5969243a1b176152496b6e20bdd2
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534721"
---
# <a name="pick-items-for-warehouse-shipment"></a>Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten

Kun varastossa on määritetty pakolliseksi sekä fyysisen varastoinnin poiminnan käsittely että fyysisen varastoinnin toimituksen käsittely, voit luoda ja käsitellä poimintatietoja fyysisen varastoinnin poiminta-asiakirjojen avulla.  

Fyysisen varastoinnin poiminta-asiakirjaa voi luoda alusta alkaen, koska poiminta-aktiviteetti on aina osa työnkulkua sekä veto- että työntötilanteessa.  

Voit luoda fyysisen varastoinnin poiminta-asiakirjoja pull muodissa avaamalla tyhjän varastotoimitusasiakirjan, tunnistamalla lähdeasiakirjat, jotka on luovutettu lähetettäväksi ja luomalla sitten varastonpoimintarivit kyseisille toimituksille. Voit käyttää **Hae lähdedokumentit** tai **Käytä suodatinta hakeaksesi lähdedokumentit** funktiota tunnistaaksesi lähdeasiakirjat, jotka ovat valmiita toimitusta varten.

Voit myös käyttää **Poimintatyökirja**-sivua ottaaksesi ja luodaksesi poimintarivejä erätilassa. Lisätietoja on kohdassa [Poimintojen suunnitteleminen työkirjassa](warehouse-how-to-plan-picks-in-worksheets.md).  

Voit myös luoda fyysisen varastoinnin poiminta-asiakirjat push-muodossa **F.var. toimitusrivit** -sivulla valitsemalla **Luo poiminta**.  

> [!NOTE]  
>  Toimitettavaa myyntitilausta varten kokoonpantavien nimikkeiden fyysisen varastoinnin toimituksessa noudatetaan samoja vaiheita kuin tavallisen fyysisen varastoinnin poiminnoissa toimitusta varten, kuten tässä ohjeaiheessa on kuvattu. Poimittavien rivien määrä toimitettavan määrän mukaan voi kuitenkin olla monta yhteen, koska poimittavana ovat komponentit eikä kokoonpanon nimike.  
>   
>  Fyysisen varastoinnin poimintarivit luodaan kokoonpanotilauksen **Jäljellä oleva määrä** -kentässä olevalle arvolle; kyseinen kokoonpanotilaus on linkitetty toimitettavaan myyntitilausriviin. Tämä varmistaa, että kaikki osat kerätään yhdellä kerralla.  
>   
>  Lisätietoja on kohdassa Kokoonpano tilausta varten -nimikkeiden käsitteleminen varastotoimituksissa.  
>   
>  Lisätietoja kokoonpanotilausten komponenttien poiminnasta yleensä (mukaan lukien tilanteet, joissa kokoonpanon nimike ei eräänny myyntitoimituksen yhteydessä) on kohdassa [Poiminta tuotantoon tai kokoonpanoon](warehouse-how-to-pick-for-production.md).  

## <a name="to-pick-items-for-warehouse-shipment"></a>Poimi fyysisen varastoinnin toimituksen nimikkeitä

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poiminnat** ja valitse sitten vastaava linkki.  

    Jos sinun pitää käsitellä tiettyä poimintaa, valitse poiminta luettelosta tai etsi sinulle määritetyt poiminnat suodattamalla luetteloa. Avaa poiminnan kortti.  
2.  Jos **Määritetty käyttäjätunnus** -kenttä on tyhjä, syötä tunnuksesi tarvittaessa itse.  
3.  Suorita todellinen nimikkeiden poiminta.  

    Jos fyysinen varasto on määritetty käyttämään varastopaikkoja, nimikkeen ottopaikkoja ehdotettaessa käytetään nimikkeen oletusvarastopaikkoja. Ohjelman ohjeet näkyvät kahtena erillisenä rivinä, joita on vähintään yksi kummallekin toiminnon tyypille, otolle ja asetukselle  

    Jos fyysinen varasto on määritetty käyttämään ohjattua hyllytystä ja poimintaa, parhaat poimintavarastopaikat lasketaan varastopaikan luokittelun avulla. Poimintariveille ehdotetaan näitä varastopaikkoja. Ohjelman ohjeet näkyvät kahtena erillisenä rivinä, joita on vähintään yksi kummallekin toiminnon tyypille, otolle ja asetukselle  

4.  Kun olet suorittanut poiminnan ja sijoittanut nimikkeet toimitusalueelle tai toimitusvarastopaikkaan, valitse **Rekisteröi poiminta** -toiminta.  

Toimituksesta vastaava voi nyt tuoda nimikkeet toimitusalueelle ja kirjata toimituksen, mukaan lukien liittyvän lähdeasiakirjan, **F.var. toimitus** -sivulla. Lisätietoja on kohdassa [Nimikkeiden toimittaminen](warehouse-how-ship-items.md).   

Sen lisäksi, että voit tässä ohjeaiheessa kuvatulla tavalla suorittaa poiminnan lähdeasiakirjojen mukaisesti, voit ottaa ja asettaa nimikkeitä varastopaikkojen välillä lähdeasiakirjoihin viittaamatta. Lisätietoja on kohdassa [Poimiminen ja hyllyttäminen ilman lähdeasiakirjaa](warehouse-how-to-create-put-aways-from-internal-put-aways.md).  

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a>Kokoonpano tilausta varten -nimikkeiden käsitteleminen fyysisen varastoinnin toimituksissa

Kokoonpano tilausta varten -tilanteissa fyysisen varaston toimitusrivin **Toimitettava määrä** -kenttää käytetään koottujen yksiköiden lukumäärän tallennukseen. Määritetty määrä kirjataan sitten kokoonpanon tuotoksena, kun fyysisen varastoinnin toimitus kirjataan.

Muiden fyysisen varastoinnin toimitusrivien **Toimitettava määrä** -kentän arvo on alussa nolla.

Kun kokoonpanosta vastaavat työntekijät saavat valmiiksi osien kokoamisen tai koko Kokoonpano tilausta varten -määrän, he tallentavat sen fyysisen varaston toimitusrivin **Toimitettava määrä** -kenttään ja valitsevat sitten **Kirjaa toimitus** -toiminnon. Tuloksena on, että vastaavan kokoonpanon tuotos kirjataan, mukaan lukien osien kulutus. Määrän myyntitoimitus on kirjattu myyntitilaukseen.

Valitse kokoonpanotilauksen **Kokoonpano tilausta varten: f. var. toimitusrivi**, kun haluat käyttää fyysisen varastoinnin toimitusriviä. Tämä on kätevä niiden työntekijöiden kannalta, jotka eivät yleensä käytä **Fyysisen varastoinnin toimituksen** -sivua.

Kun varastotoimitus on lähetetty, myyntitilauksen rivin kentät päivitetään varaston edistymisen näyttämiseksi. Seuraavat kentät päivitetään lisäksi näyttämään kuinka monta kokoonpanoa tilausta varten on vielä koottava ja toimitettava:

- **ATO-varaston avoin määrä**
- **ATO-varaston avoin määrä (perus)**

> [!NOTE]
> Yhdistelmätilanteissa, joissa osa määrästä on koottava ensin ja toinen toimitettava varastosta, luodaan kaksi fyysisen varaston toimitusriviä. Toinen on kokoonpano tilausta varten -määrälle ja toinen varastomäärälle.

> Tässä tapauksessa kokoonpano tilausta varten -määrää käsitellään tässä ohjeaiheessa kuvatulla tavalla ja varastomäärää samoin kuin mitä tahansa tavallista fyysisen varastoinnin toimitusriviä. Lisätietoja yhdistelmäskenaarioista on kohdassa [Tietoja Kokoonpano tilausta varten- tai Kokoonpano varastoon -toiminnoista](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/pick-ship-items-warehouse/)

## <a name="see-also"></a>Katso myös

[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
