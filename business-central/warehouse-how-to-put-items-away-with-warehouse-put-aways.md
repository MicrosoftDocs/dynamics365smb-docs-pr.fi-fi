---
title: Nimikkeiden hyllyttäminen ja fyysisen varaston hyllytykset
description: Tietoja erilaisista tavoista käyttää fyysisen varaston hyllytyksiä vastaanotettujen nimikkeiden hyllyttämiseen.
author: bholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/24/2023
ms.custom: bap-template
ms.search.forms: '7352, 7333'
---
# Nimikkeiden hyllyttäminen ja fyysisen varaston hyllytykset

[!INCLUDE[prod_short](includes/prod_short.md)]issa nimikkeiden vastaanottoon ja hyllytykseen on neljä tapaa, jotka käsitellään seuraavassa taulukossa.

|Tapa|Saapuva prosessi|Vaadi vastaanotot|Vaadi hyllytykset|Monimutkaisuustaso (lisätietoja on kohdassa [Varastoinninhallinnan yleiskatsaus](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Vastaanoton ja hyllytyksen kirjaaminen tilausriviltä|||Ei määritettyä fyysisen varaston toimintaa.|  
|B|Vastaanoton ja hyllytyksen kirjaaminen varaston hyllytysasiakirjasta||Otettu käyttöön|Perus: tilauksittain.|  
|S|Kirjaa vastaanotto ja hyllytys fyysisen varastoinnin vastaanottoasiakirjasta|Otettu käyttöön||Perus: useiden tilausten konsolidoitu vastaanoton ja toimituksen kirjaus.|  
|P|Kirjaa vastaanotto fyysisen varastoinnin vastaanottoasiakirjasta ja kirjaa hyllytys varaston hyllytysasiakirjasta|Otettu käyttöön|Otettu käyttöön|Lisäasetukset|  

Lisätietoja on kohdassa [Saapuvien varastotyönkulku](design-details-inbound-warehouse-flow.md).

Tässä artikkelissa viitataan taulukon menetelmään D ja oletetaan, että vastaanotto on jo tehty. Lisätietoja on kohdassa [Nimikkeiden vastaanottaminen](warehouse-how-receive-items.md).

Jos sijainti on määritetty edellyttämään fyysisen varastoinnin hyllytyksen ja vastaanoton käsittelyä, nimikkeiden hyllytystä voidaan hallita fyysisen varastoinnin hyllytysasiakirjojen avulla. Fyysisen varastoinnin vastaanottoa kirjatessa lähdeasiakirjat, kuten osto-, saapuvat siirto- tai myyntipalautustilaukset, päivitetään. Vastaanotettu määrä kirjataan nimiketapahtumiin, ja vastaanotettujen nimikkeiden rivit lähetetään fyysisen varastoinnin hyllytystoimintoon.

**Sijaintikortin** **Käytä hyllytystyökirjaa** -kentän arvon mukaan rivit tulevat joko hyllytettäviksi hyllytystyökirjassa tai hyllytysasiakirjat luodaan niiden avulla heti. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

Tässä artikkelissa käsiteltyjen fyysisen varaston hyllytysten vakioluontitapojen lisäksi hyllytyksiä voidaan luoda liittyvästä kirjatusta fyysisen varaston vastaanotosta. Tämä on kätevää, jos hyllytysrivit on poistettu tai jos päätetään olla käyttämättä hyllytystyökirjaa, koska hyllytysohjeet voidaan luoda tai uudelleenluoda kirjatuilta vastaanottoriveiltä.

## Alueen ja varastopaikan koodit

Ohjattua hyllytystä ja poimintaa käyttämään määritetyissä sijainneissa seuraavat asetukset ovat pakollisia määritettäessä, mikä on paras paikka hyllytettäville nimikkeille:  

* Hyllytysmallien määrittäminen: Lisätietoja on kohdassa [Hyllytysmallien määrittäminen](warehouse-how-to-set-up-put-away-templates.md).  
* Nimikkeen tai varastointiyksikön paino, tilavuus ja varastoinnin erityisvaatimukset määritetään.
* Varastopaikoille määritetään kapasiteetti, varastopaikan tyyppi ja varastopaikan luokittelu.  

Varastopaikan luokittelua käytetään, jos hyllytysmallin ehtoja vastaavia varastopaikkoja on useita. Jos sekä hyllytysmallin ehdot että varastopaikan luokittelu ovat samat useissa varastopaikoissa, ohjelma valitsee varastopaikan, jonka numero on suurin.

## Hyllytysasiakirjojen joukkoluonti hyllytystyökirjan avulla  

Useille vastaanotoille voidaan luoda samanaikaisesti hyllytysasiakirjoja **Hyllytystyökirja**-sivulla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyllytystyökirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Hae f. varastoinnin asiakirjat** -toiminto. Näyttöön tulee **Hyllytyksen valinta** -sivu.  

    Luettelo sisältää kaikki hyllytykseen valmiit kirjatut vastaanotot, mukaan lukien vastaanotot, joille on jo luotu hyllytysohjeet. Asiakirjat, joissa on hyllytysrivejä, joita ei ole täysin hyllytetty ja rekisteröity, ei näytetä tässä luettelossa.  
3. Valitse käsiteltävät asiakirjat. Voit käsitellä samaan aikaan useista asiakirjoista peräisin olevia rivejä.  

    > [!NOTE]  
    >  Jos valittavalle vastaanoton tai sisäisen hyllytyksen asiakirjan kaikille riveille on jo luotu ohjeet, [!INCLUDE[prod_short](includes/prod_short.md)] ilmoittaa, että mitään käsiteltävää ei ole.  

4. Järjestä rivit täyttämällä **Järjestämistapa**-kenttä.  

    > [!NOTE]  
    >  Rivien lajittelu työkirjassa ei automaattisesti toteudu samanlaisena hyllytysohjeessa. Käytössä on kuitenkin samat järjestely- ja varastopaikan luokittelumahdollisuudet. Työkirjassa suunniteltu rivijärjestys voidaan siten luoda uudelleen, kun hyllytysohjeita luodaan tai hyllytysohjeissa tehdään järjestelyjä.

5. Täytä **Käsiteltävä määrä** -kenttä. Valitse **Täytä autom. käsitelt. määrä** -toiminto tai täytä kentät manuaalisesti.  
6. Rivejä voi tarvittaessa muokata manuaalisesti. Rivejä voidaan poistaa esimerkiksi silloin, jos jotkin nimikkeet on hyllytettävä varastopaikkaan, joka on kaukana muiden nimikkeiden varastopaikoista.  

    > [!NOTE]  
    > Rivejä poistettaessa rivit poistetaan kyseisestä työkirjasta. Niitä ei poisteta hyllytysvalinnasta.  

7. Valitse **Luo hyllytys** -toiminto. Avautuvalla **Luo asiakirja** -sivulla voi lisätä lisätietoja luotavaan hyllytykseen.  

    * Hyllytyksen voi määritellä tietylle työntekijälle.  
    * Hyllytysohjerivit voidaan lajitella samoin kuin työkirjassa tai varastopaikan luokittelun mukaan. Varastopaikan luokittelun mukaisessa järjestelyssä *Ota*-rivit näkyvät ensimmäisenä, koska vastaanoton varastopaikkojen luokitus on 0. *Aseta*-rivit näkyvät viimeisenä alkaen varastopaikoista, joiden varastopaikan luokittelu on pienin. Jos fyysinen varasto on järjestetty siten, että samoin luokitellut varastopaikat ovat vierekkäin, rivien järjesteleminen tällä tavoin säästää varastotyöntekijöiden askelia.  
    * Sellaisia rivejä, jotka [!INCLUDE[prod_short](includes/prod_short.md)] loi muuntaessaan suuren mittayksikön pienemmäksi mittayksiköksi, ei tarvitse sisällyttää. Tämä valinta tehdään valitsemalla **Aseta erottelusuodatin** -kenttä. Lisätietoja erottelusta on kohdassa [Irtotavaran ohjatulla hyllytyksellä ja poiminnalla tapahtuvan automaattisen erottelun ottaminen käyttöön](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    * Voit valita, että ohjelma ei täytä automaattisesti hyllytysohjeiden **Käsiteltävä määrä** -kenttää.  
    * Voit tulostaa asiakirjan heti.  

8. Luo hyllytys valitsemalla **OK**.  

## Luo hyllytys kirjatusta vastaanotosta

Jos sijainnissa käytetään sekä hyllytyksen että vastaanoton käsittelyä ja hyllytysrivit on poistettu tai jos käytössä ohjattua hyllytys ja poiminta, minkä lisäksi on päätetty olla käyttämättä hyllytystyökirjaa, kirjattujen vastaanottorivien hyllytysohjeet voidaan luoda tai luoda uudelleen.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut fyysisen varaston vastaanotot** ja valitse sitten vastaava linkki.  
2. Valitse hyllytettävä kirjattu vastaanotto.  
3. Valitse **Kortti**-toiminto.  

    Jos **Asiakirjan tila** -kenttä on tyhjä, vastaanottoa ei ole hyllytetty ollenkaan. Muutoin kenttä ilmaisee, onko vastaanotto hyllytetty osittain tai kokonaan.  

4. Jos vastaanotto on hyllytetty osittain tai sitä ei ole hyllytetty lainkaan, valitse **Luo hyllytys** -toiminto.  
5. Täytä tarvittavat kentät ja valitse sitten **OK**.  

## Nimikkeiden hyllyttäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston hyllytykset** ja valitse sitten vastaava linkki.

2. Avaa fyysisen varaston hyllytys, joka on valmis käsiteltäväksi.  
3. Jos fyysinen varastointi sitä edellyttää, anna käyttäjätunnus hyllytyksen käsittelyn alussa.  

    Hyllytysrivejä voidaan järjestellä erilaisten ehtojen, kuten nimikkeen, hyllynumeron tai eräpäivän, mukaan. Järjestäminen voi auttaa hyllytysprosessin optimoinnissa esimerkiksi seuraavasti:

    * Jos kunkin vastaanottorivin Ota- ja Aseta-rivit eivät ole peräkkäiset ja niiden halutaan olevan peräkkäisiä, järjestä rivit valitsemalla **Nimike** **Järjestämistapa**-kentässä.  
    * Jos varastopaikan luokittelut vastaavat fyysisen varaston fyysistä asettelua, työt järjestetään varastopaikkojen sijainnin perusteella käyttämällä **Varastopaikan luokittelu** -järjestämistapaa.

4. Suorita toiminnot.

    Jos varastopaikan koodia on sijainneissa pakollinen, jokaisesta vastaanottoriviestä tulee seuraavasti ainakin kaksi riviä fyysisen varaston hyllytyksessä.  

    * Ensimmäisellä rivillä, jolla **Toiminnon tyyppi** -kentässä on **Ota**, ilmaistaan, missä vastaanottoalueella nimikkeet sijaitsevat. Tällä rivillä olevaa aluetta ja varastopaikkaa ei voi muuttaa.  
    * Seuraava rivi, jonka **Toiminnon tyyppi** -kentässä lukee **Aseta**, osoittaa, minne nimikkeet on asetettava fyysisessä varastossa. Jos yhdellä vastaanottorivillä vastaanotetaan suuri määrä nimikkeitä, nimikkeet on ehkä hyllytettävä useisiin varastopaikkoihin, jolloin kullakin varastopaikalla on Aseta-rivi. 

    > [!NOTE]
    > Jos yhden rivin nimikkeet on asetettava useaan varastopaikkaan esimerkiksi siksi, että määritetty varastopaikka on täynnä, käytä **Rivit**-pikavälilehden **Jaa rivi** -toimintoa. Toiminto luo rivin jäljellä olevalle käsiteltävälle määrälle.

5. Kun olet asettanut kaikki nimikkeet varastopaikkoihin ohjeiden mukaisesti, valitse **Rekisteröi hyllytys** -toiminto.  

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/receive-put-away-items/)

## Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
