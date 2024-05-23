---
title: Nimikkeiden hyllyttäminen varaston hyllytyksen avulla
description: Tietoja hyllytys- ja vastaanottotietojen tallentamisesta ja kirjaamisesta varaston hyllytysasiakirjan avulla.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 09/19/2023
ms.custom: bap-template
ms.search.forms: '7375,'
---
# Nimikkeiden hyllyttäminen varastohyllytyksen avulla

[!INCLUDE[prod_short](includes/prod_short.md)]issa nimikkeiden vastaanottoon ja hyllytykseen on neljä tapaa, jotka käsitellään seuraavassa taulukossa.

|Tapa|Saapuva prosessi|Vaadi vastaanotot|Vaadi hyllytykset|Monimutkaisuustaso (lisätietoja on kohdassa [Varastoinninhallinnan yleiskatsaus](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Vastaanoton ja hyllytyksen kirjaaminen tilausriviltä|||Ei määritettyä fyysisen varaston toimintaa.|  
|B|Vastaanoton ja hyllytyksen kirjaaminen varaston hyllytysasiakirjasta||Otettu käyttöön|Perus: tilauksittain.|  
|S|Kirjaa vastaanotto ja hyllytys fyysisen varastoinnin vastaanottoasiakirjasta|Otettu käyttöön||Perus: useiden tilausten konsolidoitu vastaanoton ja toimituksen kirjaus.|  
|P|Kirjaa vastaanotto fyysisen varastoinnin vastaanottoasiakirjasta ja kirjaa hyllytys varaston hyllytysasiakirjasta|Otettu käyttöön|Otettu käyttöön|Lisäasetukset|  

Lisätietoja on kohdassa [Saapuvien varastotyönkulku](design-details-inbound-warehouse-flow.md).

Tässä artikkelissa viitataan taulukon menetelmään B.

Kun sijainti on määritetty edellyttämään hyllytyskäsittelyä mutta ei vastaanottokäsittelyä, lähdeasiakirjojen hyllytys- ja vastaanottotiedot tallennetaan ja kirjataan **Varastohyllytys**-asiakirjaan. Saapuvien lähdeasiakirjat voivat olla ostotilauksia, myyntipalautustilauksia ja saapuvia siirtotilauksia.

> [!NOTE]
> Myös tuotannon ja kokoonpanon tulokset ovat saapuvien lähdeasiakirjoja. Lisätietoja sisäisten prosessien tuotannon ja kokoonpanon tuotosten käsittelemisestä on kohdassa [Rakennetiedot: fyysisen varaston sisäiset virrat](design-details-internal-warehouse-flows.md).

Varastohyllytyksen voi luoda kolmella tavalla:  

* Luomalla varastohyllytys suoraan lähdeasiakirjasta.  
* Varaston hyllytykset voidaan luoda useille lähdeasiakirjoille samalla kertaa eräajon avulla.  
* Hyllytys luodaan kahdessa vaiheessa vapauttamalla ensin lähdeasiakirja, jolla nimikkeistä tehdään hyllytettäviä. Varaston hyllytys voidaan sitten luoda lähdeasiakirjan perusteella **Varaston hyllytys** -sivulla.  

## Varastohyllytyksen lähdeasiakirjasta luominen

1. Valitse **Luo varaston hyllytys tai poiminta** -toiminto lähdeasiakirjassa, joka voi olla ostotilaus, myyntipalautustilaus tai saapuva siirtotilaus.  
2. Valitse **Luo varaston hyllytys** -valintaruutu.
3. Valitse **OK**-painike. Uusi varaston hyllytys on luotu.

## Useiden varastohyllytysten luominen eräajon avulla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo varaston hyllytys/poiminta/siirto** ja valitse sitten vastaava linkki. 
2. Suodata **F.varastoinnin pyyntö** -pikavälilehden **Lähdeasiakirja**- ja **Lähteen nro** -kenttien avulla tietyntyyppiset asiakirjat tai asiakirjanumerovälit. Hyllytyksiä voi luoda esimerkiksi vain ostotilauksille.
3. Valitse **Asetukset**-pikavälilehdessä **Luo varaston hyllytys** -valintaruutu.
4. Valitse **OK**-painike. Määritetyt varastohyllytykset luodaan.

## Hyllytyksen luominen kahdessa vaiheessa

### Pyydä varaston hyllytys vapauttamalla lähdeasiakirja

Kun ostotilaukset, myyntipalautustilaukset ja saapuvat siirtotilaukset vapautetaan, tilausten nimikkeet ovat hyllytettävissä. Seuraavissa vaiheissa käsitellään ostotilauksen nimikkeiden valmistelua hyllytystä varten.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.
2. Valitse ensin vapautettava ostotilaus ja sitten **Vapauta**-toiminto.  

### Varastohyllytyksen lähdeasiakirjasta luominen

Varastotyöntekijä voi luoda uuden varaston hyllytyksen vapautetun lähdeasiakirjan perusteella.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston hyllytys** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Valitse **Lähdeasiakirja**-kentässä hyllytettävän lähdeasiakirjan tyyppi.  
4. Valitse **Lähteen nro** -kentässä lähdeasiakirja.  
5. Vaihtoehtoisesti voit valita **Hae lähdeasiakirja** -toiminnolla asiakirjan niiden saapuvien lähdeasiakirjojen luettelosta, jotka ovat valmiita hyllytykseen sijainnissa.  
6. Valitse **OK** täyttääksesi hyllytyksen rivit valitun lähdeasiakirjan mukaan.  

## Varastohyllytyksen kirjaaminen

1. Avaa aiemmin luotu hyllytysasiakirja **Varaston hyllytykset** -sivulla.  
2. Hyllytysrivien **Varastopaikkakoodi**-kentän varastopaikkaa, johon nimikkeet on hyllytettävä, ehdotetaan nimikkeiden oletusvarastopaikan mukaan. Varastopaikkaan voi muuttaa tarvittaessa.  
3. Suorita hyllytys ja syötä sitten todelliset hyllytysmäärät **Käsiteltävä määrä** -kentässä.

    Jos yhden rivin nimikkeet on asetettava useaan varastopaikkaan esimerkiksi siksi, että määritetty varastopaikka on täynnä, käytä **Rivit**-pikavälilehden **Jaa rivi** -toimintoa. Toiminto luo rivin jäljellä olevalle käsiteltävälle määrälle.  
4. Kun nimikkeet on hyllytetty, valitse **Kirjaa**-toiminto.  

    * Hyllytettyjen lähdeasiakirjan rivien vastaanoton kirjaaminen
    * Jos sijainti käyttää varastopaikkoja, kirjaus luo myös fyysisiä varastotapahtumia varastopaikan määrän muutosten kirjaamista varten.

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
