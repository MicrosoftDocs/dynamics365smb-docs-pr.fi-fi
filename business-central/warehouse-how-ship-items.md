---
title: Nimikkeiden toimittamimen
description: Tässä ohjeaiheessa kuvataan, miten nimikkeet toimitetaan varastosta sen mukaan, millainen fyysisen varastoinnin konfiguraatio toimituksen käsittelyä varten on.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7335, 7337, 7339, 7340, 7341, 7362, 9008
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 5af803495f90590e288ad3d4e919995bb60e06b2
ms.sourcegitcommit: cfe4e924af2c89c09250270245e7a1eef1184bfc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2022
ms.locfileid: "8626601"
---
# <a name="ship-items"></a>Nimikkeiden toimittamimen

Kun toimitat nimikkeitä fyysisestä varastosta, johon ei ole määritetty fyysisen varaston toimituskäsittelyä, toimitus vain kirjataan liittyvään asiakirjaan, kuten myyntitilaukseen, huoltotilaukseen, ostopalautustilaukseen tai lähtevään siirtotilaukseen.

Kun toimitat nimikkeitä fyysisestä varastosta, johon määritetty toimituksen käsittely, nimikkeitä voi toimittaa vain sellaisten lähdeasiakirjojen perusteella, jotka muut yrityksen yksiköt ovat antaneet fyysiseen varastointiin toimintoa varten.

> [!NOTE]
> Jos fyysisessä varastoinnissa käytetään laiturointia ja varastopaikkoja, voit katsoa jokaisen rivin osalta niiden nimikkeiden määrän, jotka on sijoitettu laiturointivarastopaikkoihin. Sovellus laskee nämä määrät automaattisesti aina, kun toimituksen kenttiä päivitetään. Jos kyseessä ovat nimikkeet, jotka sopivat valmisteltavaan toimitukseen, voit luoda poiminnan kaikille riveille ja sitten tehdä toimituksen loppuun. Lisätietoja on kohdassa [Nimikkeiden laiturointi](warehouse-how-to-cross-dock-items.md).

## <a name="to-ship-items-with-a-sales-order"></a>Nimikkeiden toimittaminen myyntitilauksella

Seuraavaksi käsitellään, miten nimikkeitä lähetetään myyntitilauksesta. Vaiheet ovat samankaltaiset ostopalautustilaukset, huoltotilauksille ja lähtevät siirtotilauksille.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.
2. Avaa aiemmin luotu myyntitilaus tai luo uusi myyntitilaus. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).
3. Anna **Toimitettava määrä** -kenttään lähetetty määrä.

    **Toimitettava määrä** -kentän arvo päivitetään. Jos kyse on osatoimituksesta, arvo on pienempi kuin **Määrä**-kentän arvo.
4. Valitse **Kirjaa**-toiminto.

> [!NOTE]
> Jos organisaatio ei käytä myyntitilauksia, [!INCLUDE [prod_short](includes/prod_short.md)] olettaa, että koko määrä on lähetetty, kun kirjaat myyntilaskun. Jos tämä on ristiriidassa organisaation toimintatavan kanssa, kannattaa käyttää myyntitilauksia ja rekisteröidä toimitukset tässä artikkelissa kuvatulla tavalla.

## <a name="to-ship-items-with-a-warehouse-shipment"></a>Nimikkeiden toimittaminen fyysisen varasto toimituksena

Luo ensin toimitusasiakirjan lähdeasiakirjasta. Poimi sitten toimitukseen määritetyt nimikkeet.

### <a name="to-create-a-warehouse-shipment"></a>Fyysisen varaston toimituksen luominen

Yleensä toimituksesta vastaava työntekijä luo fyysisen varastoinnin toimituksen. Seuraavaksi kuvataan tapa, jolla luodaan toimitus manuaalisesti [!INCLUDE[prod_short](includes/prod_short.md)]in oletusversiossa, mutta organisaatio on voinut myös automatisoida osan prosessista käyttämällä esimerkiksi ulkoisten palveluntarjoajien tukemia kannettavia tai kiinteitä skannereita.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston toimitukset** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  

    Täytä **Yleinen**-pikavälilehden kentät. Kun haet lähdeasiakirjan rivit, ohjelma kopioi otsikon tiedot kullekin riville.  

    Jos fyysisen varaston määrityksissä on käytössä ohjattu hyllytys ja poiminta ja jos sijainnilla on oletusalue ja oletusvarastopaikka toimituksille, **Alueen koodi**- ja **Varastopaikkakoodi**-kentät täytetään automaattisesti, mutta voit muuttaa niiden arvoja tarpeen mukaan.  

    > [!NOTE]  
    > Jos haluat toimittaa nimikkeitä, joiden fyysisen varastoinnin luokkakoodi ei ole sama kuin asiakirjan otsikon **Varastopaikkakoodi**-kentässä olevan varastopaikan luokkakoodi, poista otsikon **Varastopaikkakoodi**-kentän sisältö ennen lähdeasiakirjan rivien hakemista nimikkeitä varten.  
3. Valitse **Hae lähdeasiakirjat** -toiminto. Näyttöön tulee **Lähdeasiakirjat**-sivu.

    Voit käyttää uuden tai avoimen fyysisen varastoinnin toimituksen **Suod. lähdeasiakirj. saamisek.** -sivua hakiessasi toimitettavat nimikkeet määrittävän vapautetun lähdeasiakirjan rivit.

    1. Valitse **Käytä suodat. kun haet lähd.d** -toiminto.  
    2. Määritä uusi suodatin antamalla kuvaileva koodi **Koodi**-kenttään ja valitse **Muokkaa**-toiminto.  
    3. Määritä ne lähdeasiakirjan rivien tyypit, jotka haluat hakea, täyttämällä soveltuvat suodatinkentät.  
    4. Valitse **Aja**-toiminto.  

    Kaikki julkaistut lähdeasiakirjan rivit, jotka täyttävät suodatusehdot, on nyt lisätty **F.var. toimitus** -sivulla, josta aktivoit suodatustoiminnon.  

    Määrittämäsi suodatinyhdistelmät tallennetaan **Suod. lähdeasiakirj. saamisek.** -sivulle tulevaa käyttöä varten. Voit tehdä niin monta suodatinyhdistelmää kuin haluat. Voit muuttaa ehtoja milloin tahansa valitsemalla **Muokkaa**-toiminnon.

4. Valitse lähdeasiakirjat, joiden osalta haluat toimittaa nimikkeitä, ja valitse sitten **OK**.  

Lähdeasiakirjojen rivit näkyvät **Fyysisen varaston toimitus** -sivulla. **Toimitettava määrä** -kenttään on jo täytetty jokaisen rivin avoimen määrä, mutta määrää voi muuttaa tarpeen mukaan. Jos olet poistanut **Yleinen**-pikavälilehden **Varastopaikkakoodi**-kentän sisällön ennen rivien hakemista, kirjoita kullekin toimitusriville soveltuva varastopaikkakoodi.  

> [!NOTE]  
> Et voi toimittaa enempää nimikkeitä kuin lähdeasiakirjan rivin **Avoin määrä** -kentässä oleva määrä ilmaisee. Voit toimittaa enemmän nimikkeitä hakemalla toisen lähdeasiakirjan, jossa on rivi nimikkeelle. Se onnistuu hakemalla nimikkeen sisältävät lähdeasiakirjat suodatintoiminnon avulla.  

Kun olet hakenut rivit, jotka haluat toimittaa, aloita seuraavassa kuvatulla tavalla prosessi, joka lähettää rivit fyysisen varastoinnin työntekijöille poimintaa varten.

### <a name="to-pick-and-ship"></a>Poiminta ja lähettäminen

Yleensä poiminnasta vastuussa oleva varastotyöntekijä luo poiminta-asiakirjan tai avaa jo luodun poiminta-asiakirjan.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston toimitukset** ja valitse sitten vastaava linkki.
2. Valitse ensin poimittava fyysisen varastoinnin toimitus ja sitten **Luo poiminta** -toiminto.
3. Täytä pyyntösivun kentät ja valitse sitten **OK**. Määritetty fyysisen varastoinnin poiminta-asiakirja luodaan.

    Vaihtoehtoisesti voit avata aiemmin luodun fyysisen varaston poiminnan.
4. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poiminnat** ja valitse sitten vastaava linkki. Valitse varastoinnin poiminta, jota haluat työstää.

    Jos fyysisessä varastoinnissa käytetään varastopaikkoja, poimintarivit on muunnettu "ota ja aseta" -toimintoriveiksi.

    Voit järjestellä rivit, määrittää poiminnalle työntekijän, asettaa erottelusuodatuksen (jos käytät ohjattua hyllytystä ja poimintaa) ja tulostaa poimintaohjeet.

5. Tee varsinainen nimikkeiden poiminta ja siirrä nimikkeet määritettyyn toimituksen varastopaikkaan (tai toimitusalueelle, jos et käytä varastopaikkoja).
6. Valitse **Rekisteröi poiminta** -toiminto.

    Ohjelma päivittää **Toimitettava määrä** -kentän ja **Asiakirjan tila** -kentän toimitusasiakirjan otsikossa. Poimimasi nimikkeet eivät ole enää poimittavissa muihin toimituksiin tai sisäisiin toimintoihin.
7. Tulosta toimitusasiakirjat, valmistele toimituskollit ja kirjaa sitten toimitus.

Lisätietoja poiminnasta fyysisen varaston toimituksia varten on kohdassa [Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Voit tehdä useista poimintaohjeista yhden ohjeen (useille toimituksille) myös poimintatyökirjan avulla. Näin poiminta tehostuu fyysisessä varastossa. Lisätietoja on kohdassa [Poimintojen suunnitteleminen työkirjassa](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Jos odotat tiettyjen nimikkeiden saapumista fyysiseen varastoon ja käytät laiturointitoimintoa, [!INCLUDE[prod_short](includes/prod_short.md)] laskee kullekin toimituksen tai poimintatyökirjan riville laiturointivarastopaikassa olevan nimikkeen määrän. Ohjelma päivittää kentän aina, kun lähdet toimituksesta tai työkirjasta ja kun avaat toimitusasiakirjan tai työkirjan. Lisätietoja on kohdassa [Nimikkeiden laiturointi](warehouse-how-to-cross-dock-items.md).

## <a name="see-also"></a>Katso myös

[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]