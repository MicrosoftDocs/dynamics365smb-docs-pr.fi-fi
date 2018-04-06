---
title: Nimikkeiden toimittaminen | Microsoft Docs
description: "Fyysisen varaston määritysten mukaan voit joko kirjata toimituksen suoraan liittyvään lähtevään asiakirjaan, kuten myyntitilaukseen, tai voit käyttää fyysisen varaston toimitusasiakirjoja, jotka noudattavat työnkulkua tai integroituvat fyysisen varaston eri toimintoihin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 223eed1ca4e362b8209373fac71d20ab88b2aaff
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="ship-items"></a>Nimikkeiden toimittamimen
Kun toimitat nimikkeitä fyysisestä varastosta, johon ei ole määritetty fyysisen varaston toimituskäsittelyä, toimitus vain kirjataan liittyvään asiakirjaan, kuten myyntitilaukseen, huoltotilaukseen, ostopalautustilaukseen tai lähtevään siirtotilaukseen.

Kun toimitat nimikkeitä fyysisestä varastosta, johon määritetty toimituksen käsittely, nimikkeitä voi toimittaa vain sellaisten lähdeasiakirjojen perusteella, jotka muut yrityksen yksiköt ovat antaneet fyysiseen varastointiin toimintoa varten.

> [!NOTE]
> Jos fyysisessä varastoinnissa käytetään laiturointia ja varastopaikkoja, voit katsoa jokaisen rivin osalta niiden nimikkeiden määrän, jotka on sijoitettu laiturointivarastopaikkoihin. Ohjelma laskee nämä määrät automaattisesti aina, kun toimituksen kenttiä päivitetään. Jos kyseessä ovat nimikkeet, jotka sopivat valmisteltavaan toimitukseen, voit luoda poiminnan kaikille riveille ja sitten tehdä toimituksen loppuun. Lisätietoja on kohdassa [Nimikkeiden laiturointi](warehouse-how-to-cross-dock-items.md).

## <a name="to-ship-items-with-a-sales-order"></a>Nimikkeiden toimittaminen myyntitilauksella
Seuraavaksi käsitellään, miten nimikkeitä vastaanotetaan ostotilauksella. Vaiheet ovat samankaltaiset ostopalautustilaukset, huoltotilauksille ja lähtevät siirtotilauksille.  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa aiemmin luotu myyntitilaus tai luo uusi myyntitilaus. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).
3. Anna **Toimitettava määrä** -kenttään vastaanotettu määrä.

    **Toimitettava määrä** -kentän arvo päivitetään. Jos kyse on osatoimituksesta, arvo on pienempi kuin **Määrä**-kentän arvo.
4. Valitse **Kirjaa**-toiminto.

## <a name="to-ship-items-with-a-warehouse-shipment"></a>Nimikkeiden toimittaminen fyysisen varasto toimituksena
Luo ensin toimitusasiakirjan lähdeasiakirjasta. Poimi sitten toimitukseen määritetyt nimikkeet.

### <a name="to-create-a-warehouse-shipment"></a>Fyysisen varaston toimituksen luominen
Yleensä toimituksesta vastaava työntekijä luo fyysisen varastoinnin toimituksen.
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Fyysisen varaston toimitukset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  

    Täytä **Yleinen**-pikavälilehden kentät. Kun haet lähdeasiakirjan rivit, ohjelma kopioi otsikon tiedot kullekin riville.  

    Jos fyysisen varaston määrityksissä on käytössä ohjattu hyllytys ja poiminta ja jos sijainnilla on oletusalue ja oletusvarastopaikka toimituksille, **Alueen koodi**- ja **Varastopaikkakoodi**-kentät täytetään automaattisesti, mutta voit muuttaa niiden arvoja tarpeen mukaan.  

    > [!NOTE]  
    >  Jos haluat toimittaa nimikkeitä, joiden fyysisen varastoinnin luokkakoodi ei ole sama kuin asiakirjan otsikon **Varastopaikkakoodi**-kentässä olevan varastopaikan luokkakoodi, poista otsikon **Varastopaikkakoodi**-kentän sisältö ennen lähdeasiakirjan rivien hakemista nimikkeitä varten.  
3.  Valitse **Hae lähdeasiakirjat** -toiminto. **Lähdeasiakirjat**-ikkuna avautuu.

    Voit käyttää uuden tai avoimen fyysisen varastoinnin toimituksen **Suod. lähdeasiakirj. saamisek.** -ikkunaa hakiessasi toimitettavat nimikkeet määrittävän vapautetun lähdeasiakirjan rivit.

    1. Valitse **Käytä suodat. kun haet lähd.d** -toiminto.  
    2. Määritä uusi suodatin antamalla kuvaileva koodi **Koodi**-kenttään ja valitse **Muokkaa**-toiminto.  
    3. Määritä ne lähdeasiakirjan rivien tyypit, jotka haluat hakea, täyttämällä soveltuvat suodatinkentät.  
    4. Valitse **Aja**-toiminto.  

    Kaikki julkaistut lähdeasiakirjan rivit, jotka täyttävät suodatusehdot, on nyt lisätty **F.var. toimitus** -ikkunassa, josta aktivoit suodatustoiminnon.  

    Määrittämäsi suodatinyhdistelmät tallennetaan **Suod. lähdeasiakirj. saamisek.** -ikkunaan tulevaa käyttöä varten. Voit tehdä niin monta suodatinyhdistelmää kuin haluat. Voit muuttaa ehtoja milloin tahansa valitsemalla **Muokkaa**-toiminnon.

4.  Valitse lähdeasiakirjat, joiden osalta haluat toimittaa nimikkeitä, ja valitse sitten **OK**.  

Lähdeasiakirjojen rivit näkyvät **F.var. toimitus** -ikkunassa. **Toimitettava määrä** -kenttään on jo täytetty jokaisen rivin avoimen määrä, mutta määrää voi muuttaa tarpeen mukaan. Jos olet poistanut **Yleinen**-pikavälilehden **Varastopaikkakoodi**-kentän sisällön ennen rivien hakemista, kirjoita kullekin toimitusriville soveltuva varastopaikkakoodi.  

> [!NOTE]  
>  Et voi toimittaa enempää nimikkeitä kuin lähdeasiakirjan rivin **Avoin määrä** -kentässä oleva määrä ilmaisee. Voit toimittaa enemmän nimikkeitä hakemalla toisen lähdeasiakirjan, jossa on rivi nimikkeelle. Se onnistuu hakemalla nimikkeen sisältävät lähdeasiakirjat suodatintoiminnon avulla.  

Kun olet hakenut rivit, jotka haluat toimittaa, aloita seuraavassa kuvatulla tavalla prosessi, joka lähettää rivit fyysisen varastoinnin työntekijöille poimintaa varten.

### <a name="to-pick-and-ship"></a>Poiminta ja lähettäminen
Yleensä poiminnasta vastuussa oleva varastotyöntekijä luo poiminta-asiakirjan tai avaa jo luodun poiminta-asiakirjan.
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Fyysisen varaston toimitukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse ensin poimittava fyysisen varastoinnin toimitus ja sitten **Luo poiminta** -toiminto.
3. Täytä pyyntöikkunan kentät ja valitse sitten **OK**. Määritetty fyysisen varastoinnin poiminta-asiakirja luodaan.

    Vaihtoehtoisesti voit avata aiemmin luodun fyysisen varaston poiminnan.
4. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Poiminnat** ja valitse sitten aiheeseen liittyvä linkki. Valitse varastoinnin poiminta, jota haluat työstää.

    Jos fyysisessä varastoinnissa käytetään varastopaikkoja, poimintarivit on muunnettu "ota ja aseta" -toimintoriveiksi.

    Voit järjestellä rivit, määrittää poiminnalle työntekijän, asettaa erottelusuodatuksen (jos käytät ohjattua hyllytystä ja poimintaa) ja tulostaa poimintaohjeet.

5. Tee varsinainen nimikkeiden poiminta ja siirrä nimikkeet määritettyyn toimituksen varastopaikkaan (tai toimitusalueelle, jos et käytä varastopaikkoja).
6. Valitse **Rekisteröi poiminta** -toiminto.

    Ohjelma päivittää **Toimitettava määrä** -kentän ja **Asiakirjan tila** -kentän toimitusasiakirjan otsikossa. Poimimasi nimikkeet eivät ole enää poimittavissa muihin toimituksiin tai sisäisiin toimintoihin.
7. Tulosta toimitusasiakirjat, valmistele toimituskollit ja kirjaa sitten toimitus.

Lisätietoja poiminnasta fyysisen varaston toimituksia varten on kohdassa [Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Voit tehdä useista poimintaohjeista yhden ohjeen (useille toimituksille) myös poimintatyökirjan avulla. Näin poiminta tehostuu fyysisessä varastossa. Lisätietoja on kohdassa [Poimintojen suunnitteleminen työkirjassa](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Jos odotat tiettyjen nimikkeiden saapumista fyysiseen varastoon ja käytät laiturointitoimintoa, [!INCLUDE[d365fin](includes/d365fin_md.md)] laskee kullekin toimituksen tai poimintatyökirjan riville laiturointivarastopaikassa olevan nimikkeen määrän. Ohjelma päivittää kentän aina, kun lähdet toimituksesta tai työkirjasta ja kun avaat toimitusasiakirjan tai työkirjan. Lisätietoja on kohdassa [Nimikkeiden laiturointi](warehouse-how-to-cross-dock-items.md).

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

