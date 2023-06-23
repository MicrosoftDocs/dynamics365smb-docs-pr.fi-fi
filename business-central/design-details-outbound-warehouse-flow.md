---
title: Fyysisen varaston lähtevän prosessin yleiskatsaus
description: Tässä artikkelissa käsitellään fyysisen varaston lähtevää työnkulkua.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/25/2022
ms.custom: bap-template
---
# <a name="outbound-warehouse-processes" />Fyysisen varaston lähtevät prosessit

Lähtevät varastot käynnistyvät fyysisissä varastoissa, kun lähdeasiakirja vapautetaan ottamaan nimikkeitä ulos fyysisestä varastosijainnista. Nimikkeet voidaan esimerkiksi toimittaa jonnekin tai siirtää yrityksen toiseen sijaintiin. Lähtevien tilausten toimitusprosessissa on periaatteessa kaksi toimintaa:

* Nimikkeiden poiminta hyllyiltä.
* Nimikkeiden toimitus fyysisen varaston ulkopuolelle.

Fyysisen varastoinnin lähtevien lähdeasiakirjat:  

* Myyntitilaus  
* Lähtevä siirtotilaus  
* Ostopalautustilaus  
* Huoltotilaus  

> [!NOTE]
> Myös komponenttitarpeita sisältävät tuotanto- ja kokoonpanotilaukset ilmaisevat lähtevien lähdeasiakirjoja. Tuotanto- ja kokoonpanotilaukset ovat hieman erilaisia, sillä ne ovat yleensä sisäisiä prosesseja, joihin ei liity toimitusta. Niitä käytetään sen sijaan hyllyttämään tuotettuja nimikkeitä tai siirtämään nimikkeen kokoonpanoon tarvittavia komponentteja kokoonpanoalueelle. Lisätietoja näistä prosesseista on kohdassa [Rakennetiedot: fyysisen varaston sisäiset työnkulut](design-details-internal-warehouse-flows.md).  

[!INCLUDE[prod_short](includes/prod_short.md)]issa nimikkeet poimintaan ja toimitukseen on käytettävissä neljä tapaa, jotka käsitellään seuraavassa taulukossa.

|Tapa|Lähtevien käsittely|Vaadi poiminta|Vaadi toimitus|Monimutkaisuustaso (lisätietoja on kohdassa [Varastoinninhallinnan yleiskatsaus](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Poiminnan ja toimituksen kirjaaminen tilausriviltä|||Ei määritettyä fyysisen varaston toimintaa.|  
|B|Poiminnan ja toimituksen kirjaaminen varaston poiminta-asiakirjasta|Otettu käyttöön||Perus: tilauksittain.|  
|S|Poiminnan ja toimituksen kirjaaminen fyysisen varastoinnin toimitusasiakirjasta||Otettu käyttöön|Perus: useiden tilausten konsolidoitu vastaanoton ja toimituksen kirjaus.|  
|P|Poiminnan kirjaaminen fyysisen varastoinnin poiminta-asiakirjasta ja toimituksen kirjaaminen fyysisen varastoinnin toimitusasiakirjasta|Otettu käyttöön|Otettu käyttöön|Lisäasetukset|  

Lähestymistavan valinta määräytyy fyysisen varaston käytäntöjen ja organisaation monimutkaisuustason mukaan. Seuraavat esimerkiksi voivat auttaa päätöksenteossa.

* Menetelmän A käyttäminen eli poiminta ja toimitus tilausriviltä on soveltuu yksinkertaisia prosesseja käyttävään tilauskohtaiseen ympäristöön, jossa käytetään yksinkertaista varastopaikkarakennetta.
* Jos tilausrivin nimikkeet otetaan useasta varastopaikasta tai jos varastotyöntekijät eivät voi käsitellä tilausasiakirjoja, kannattaa käyttää erillisiä poiminta-asiakirjoja eli menetelmää B.
* Jos poiminta- ja toimitusprosessit sisältävät useita tilauksia ja edellyttävät tarkempaa hallintaa, poiminta- ja toimitustehtävät kannattaa ehkä erottaa valitsemalla fyysisen varastoinnin toimitusasiakirjan ja fyysisen varastoinnin poiminta-asiakirjan käyttäminen eli menetelmät C ja D.  

Menetelmissä A, B ja C poiminta- ja toimitustoiminnot yhdistetään yhteen vaiheeseen, kun asiakirja kirjataan toimitetuksi. Menetelmässä D rekisteröidään ensin poiminta ja sitten toimitus kirjataan sitten myöhemmin eri asiakirjasta.

> [!NOTE]
> Vaikka fyysisen varaston hyllytykset ja varaston poiminnat vaikuttavat samanlaisilta, ne ovat eri asiakirjoja ja niitä käytetään eri prosesseissa.
> * Menetelmässä B käytetty varaston poiminta yhdessä poimintatietojen rekisteröinnin kanssa kirjaa myös lähdeasiakirjan toimituksen.
> * Menetelmässä D käytettyä fyysisen varaston poimintaa ei voi kirjata, ja se vain rekisteröi poiminnan. Rekisteröintiprosessi tuo nimikkeet saataville fyysisen varastoinnin toimitusta varten mutta ei kirjaa toimitusta. Lähtevässä työnkulussa fyysisen varaston poiminta edellyttää fyysisen varaston toimitusta.

## <a name="no-dedicated-warehouse-activity" />Ei määritettyä varastotoimintoa

Seuraavissa artikkeleissa on tietoja lähdeasiakirjojen vastaanottojen käsittelystä, jos varastotoimintoja ei ole määritetty.

* [Tuotteen myyminen](sales-how-sell-products.md)
* [Siirtotilaukset](inventory-how-transfer-between-locations.md)
* [Ostopalautusten tai peruutusten käsittely](purchasing-how-process-purchase-returns-cancellations.md)
* [Huoltotilausten luominen](service-how-to-create-service-orders.md)

## <a name="basic-warehouse-configurations" />Fyysisen varastoinnin perusmääritykset

Seuraavassa kaaviossa havainnollistetaan fyysisen varaston lähteviä prosesseja eri asiakirjatyyppien osalta fyysisen varastoinnin perusmäärityksissä. Kaavion luvut vastaavat vaiheita kaavion osa-alueiden mukaan.  

:::image type="content" source="media/design-details-warehouse-management-outbound-basic-flow.png" alt-text="Näkyvissä lähtevien perustyökulun vaiheet fyysisessä varastoinnissa":::

### <a name="1-release-a-source-document" />1: Lähdeasiakirjan vapauttaminen

Kun **Vapauta**-toimintoa käytetään lähdeasiakirjassa, kuten myynti- tai siirtotilauksessa, asiakirjan nimikkeet ovat valmiita käsiteltäväksi fyysisessä varastoinnissa. Kyse on esimerkiksi poimimisesta ja asiakirjassa määritettyyn varastopaikkaan asettamisesta. Vaihtoehtoisesti tilausten yksittäisille riveille voidaan luoda varaston poiminta-asiakirjoja push-menetelmällä määritettyjen varastopaikkojen ja käsiteltävien määrien perusteella.  

### <a name="2-create-an-inventory-pick" />2: Varaston poiminnan luominen

Varastotyöntekijä noutaa pull-menetelmällä lähdeasiakirjan rivit **Varaston poiminta**-sivulla. Vaihtoehtoisesti, varaston poiminnan rivit on jo luotu push-muodossa sen käyttäjän toimesta, joka on vastuussa lähdeasiakirjasta.  

### <a name="3-post-an-inventory-pick" />3: Varaston poiminnan kirjaaminen

Kaikkien osittain tai kokonaan poimittujen tai siirrettyjen nimikkeiden rivin osalta täytetään **Määrä**-kenttä ja kirjataan sitten varaston poiminta.. Lähdeasiakirjat, jotka liittyvät varaston poimintaan, on tiliöity lähetettyinä tai käytettyinä.  

Varastopoiminnoille luodaan negatiiviset nimiketapahtumat, varastomerkinnät luodaan ja poimintapyyntö poistetaan, jos käsittely on suorittu loppuun. Esimerkiksi **Toimitettu määrä** -kenttä lähtevän lähdeasiakirjan rivillä päivitetään. Luodaan kirjatun toimituksen asiakirja, joka vastaa esimerkiksi myyntitilausta ja toimitettuja nimikkeitä.  

## <a name="advanced-warehouse-configurations" />Laajennetut varastomääritykset

Seuraavassa kaaviossa havainnollistetaan fyysisen varaston lähteviä prosesseja eri asiakirjatyyppien osalta fyysisen varastoinnin laajennetuissa määrityksissä. Kaavion luvut vastaavat vaiheita kaavion osa-alueiden mukaan.  

:::image type="content" source="media/design_details_warehouse_management_outbound_advanced_flow.png" alt-text="Näkyvissä lähtevien laajennetun työkulun vaiheet fyysisessä varastoinnissa":::

### <a name="1-release-a-source-document" />1: Lähdeasiakirjan vapauttaminen

Lähdeasiakirjan vapauttamisen vaikutus on laajennetuissa määrityksissä sama kuin perusmäärityksissä. Nimikkeet tulevat käsiteltäviksi fyysisessä varastoinnissa. Niinpä ne voidaan sisällyttää esimerkiksi toimitukseen.  

### <a name="2-create-a-warehouse-shipment" />2: Fyysisen varaston toimituksen luominen

**Fyysisen varaston toimitus** -sivulla voidaan hakea vapautetut lähdeasiakirjan rivejä. Useiden lähdeasiakirjojen rivejä voidaan yhdistää yhdessä fyysisen varastoinnin toimituksessa.  

### <a name="3-create-a-warehouse-pick" />3: Fyysisen varaston poiminnan luominen

Fyysisen varastoinnin toimitusten fyysisen varastoinnin poimintatoiminnot luodaan **Fyysisen varaston toimitus** -sivulla jommallakummalla tavalla:

- Push-menetelmässä käytetään **Luo poiminta** -toimintoa. Poimittavat rivit valitaan ja poiminnat valmistellaan määrittämällä esimerkiksi, mistä varastopaikoista otetaan ja mihin asetetaan sekä kuinka monta yksikköä käsitellään. Varastopaikat voidaan määrittää ennalta fyysisen varaston sijainnissa tai resurssissa.
- Pull-menetelmässä käytetään **Vapauta**-toimintoa. Varastontyöntekijät voivat sitten käyttää **Poimintatyökirja**-sivulla **Hae f. varastoinnin asiakirjat** -toimintoa määritettyjen poimintojen hakemiseen. Kun fyysisen varastoinnin poiminnat on rekisteröity kokonaan, **Poimintatyökirja**-kohteen rivit poistetaan.

### <a name="4-register-a-warehouse-pick" />4: Fyysisen varastoinnin poiminnan rekisteröiminen

Varastotyöntekijä täyttää **F.varastoinnin poiminta** -sivulla **Määrä**-kentän kunkin osittain tai kokonaan poimittujen rivien osalta ja rekisteröi sitten poiminnan.

Fyysisen varastoinnin tapahtumat luodaan ja fyysisen varastoinnin poimintarivit poistetaan, jos ne on poimittu kokonaan. Fyysisen varastoinnin poiminta-asiakirja pysyy avoimena siihen saakka, että fyysisen varastoinnin toimituksen koko määrä on rekisteröity. **Määrä poimittu**-kenttä varaston lähetysriveillä on päivitetty sen mukaisesti.  

### <a name="5-post-the-warehouse-shipment" />5: Fyysisen varastoinnin toimituksen kirjaaminen

Kun fyysisen varastoinnin toimitusasiakirjan kaikki nimikkeet on rekisteröity poimituiksi, varastotyöntekijä kirjaa toimituksen. Kirjaaminen päivittää nimiketapahtumat vastaamaan varaston pienentymistä. Esimerkiksi **Toimitettu määrä** -kenttä lähtevän lähdeasiakirjan rivillä päivitetään.  

## <a name="see-also" />Katso myös

[Varastoinninhallinta](design-details-warehouse-management.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
