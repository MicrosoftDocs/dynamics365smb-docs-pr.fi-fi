---
title: 'Tuotannon, kokoonpanon tai projektin nimikkeiden poimiminen tai siirtäminen fyysisen varaston perusmäärityksissä'
description: 'Kun fyysisen varaston sijainnissa on pakollinen poiminnan käsittely mutta ei pakollista toimituksen käsittelyä, voit kirjata komponenttien poiminnan Varaston poiminta -sivun avulla.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.forms: '9330, 931, 990008, 89, 900, 902'
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Tuotanto-, kokoonpano- ja projektipoiminta perusvarastointimäärityksissä

Tuotantoon, projekteihin tai koonpanotilauksiin poimittujen komponenttien hyllytystapa määräytyy sen mukaan, miten fyysinen varasto on määritetty sijaintina. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

Lähtevän virran (poiminta) fyysisen varastoinnin perusmäärityksissä sijainnin **Sijaintikortti**-sivulla **Vaadi poiminta** otetaan käyttöön ja **Vaadi toimitus** poistetaan käytöstä vaihtopainikkeilla.

Käytössä on seuraavat sisäisten toimintojen asiakirjat:

* Varaston poiminta
* Varaston siirto

## <a name="inventory-picks"></a>Varaston poiminnat

* Kun sisäisen toiminnon, kuten tuotannon tai projektin, varaston poiminta rekisteröidään, poimittujen komponenttien kulutus kirjataan samanaikaisesti.
* **Sijaintikortti**-sivun **Var.paikka pakollinen** -valintapainike on valinnainen.
* Varaston poimintoja käytettäessä tuotantotilauksen komponentin rivillä tai projektin suunnitteluriveillä oleva **Varastopaikkakoodi**-kenttä määrittää *ota*-varastopaikan. Ottovarastopaikan komponenttien määrä vähenee, kun kulutus kirjataan.

## <a name="inventory-movements"></a>Varastosiirrot

* Varaston siirrot edellyttävät että **Varastopaikka pakollinen** otetaan vaihtopainikkeella käyttöön sijainnin **Sijaintikortti** -sivulla.
* Varaston siirrot toimivat vain tuotantotilauksen komponenttiriveillä ja kokoonpanotilauksen riveillä.
* Sisäisen toiminnon varaston siirtoa rekisteröitäessä kirjataan vain komponenttien fyysinen siirto varastopaikkaan toimenpidealueella. Kulutusta ei kirjata.
* Varaston siirtoja käytettäessä tuotantotilauksen komponenttirivien **Varastopaikkakoodi**-kenttä määrittää *asettamisen* varastopaikan toimenpidealueella. Varastotyöntekijöiden on asetettava komponentit asettamisen varastopaikkaan.
* Poimittujen komponenttien kulutus rekisteröidään erikseen kirjaamalla kulutuspäiväkirja tai kokoonpanotilaus.

>[!NOTE]
> Vaikka **Vaadi poiminta** olisi poistettu käytöstä vaihtopainikkeella, **F.varastoinnin poiminta** -asiakirjan käyttö on mahdollista. Fyysisen varastoinnin poiminta-asiakirjat muistuttavat **varaston poiminnan** asiakirjoja. Tämä on kätevää, jos toimenpiteiden poimintoja halutaan käyttää toimittamiseen fyysisen varaston lähtevissä virroissa.

### <a name="production"></a>Tuotanto

Tuotannon komponentteja voi poimia työkulussa tuotantoon **Varaston poiminta** -asiakirjojen avulla.

Jos sijainnissa käytetään varastopaikkoja, työnkulkua tuotantoon voidaan laajentaa käyttämällä **Varaston siirto** -asiakirjoja. Varaston siirrot ovat hyödyllisiä etenkin komponentin materiaaliotossa. Lisätietoja komponentin kulutuksen materiaaliotoista tuotannon valmistelun tai avoimista tuotannon varastopaikoista on kohdassa [Tuotannon komponenttien materiaaliotot fyysisen varastoinnin perusmäärityksissä](#flushing-production-components-in-a-basic-warehouse-configuration).

### <a name="assembly"></a>Kokoonpano

Kokoonpanon komponentit siirretään kokoonpanoalueelle **Varastosiirto**-asiakirjojen avulla.

> [!NOTE]
> Varastopaikat ovat pakollisia **Varaston siirto** -asiakirjoissa.

[!INCLUDE [prod_short](includes/prod_short.md)] tukee kokoonpanovirtoja, joiden tyyppi on kokoonpanoa varastoa varten ja kokoonpano tilausten varten. Lisätietoja fyysisen varaston lähtevän virran kokoonpanosta tilausten varten on kohdassa [Varaston poimintoja sisältävien kokoonpano tilausta varten -nimikkeiden käsitteleminen](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="project-management"></a>Projektinhallinta

Projektin komponentteja voi poimia työnkulussa projektinhallintaan **Varaston poiminta** -asiakirjojen avulla.

Jos sijainneissa käytetään varastopaikkoja, työnkulkua projekteihin voidaan laajentaa käyttämällä **Varaston siirto** -asiakirjoja.

> [!NOTE]
> Projektin suunnittelurivien komponenttien poimintamahdollisuus lisättiin [!INCLUDE[d365fin](includes/d365fin_md.md)]iin vuoden 2022 2. julkaisuaallossa. Ominaisuuden käytön aloittaminen edellyttää, että järjestelmänvalvojan on otettava käyttöön **Ominaisuuspäivitys: Ota käyttöön varaston ja fyysisen varaston poiminnat projekteista** **Ominaisuuksien hallinta** -sivulla.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] käyttää **Jäljellä oleva määrä** -kentän arvoa projektin suunnittelurivillä, kun se luo varastopoiminnat. Jos haluat käyttää töiden varastopoimintoja, **Käytä käyttölinkkiä** -vaihtopainike on otettava käyttöön työn **Projektikortti**-sivulla. Tämän ansiosta voit seurata, vastaako käyttö suunnitelmaa. Jos et ota vaihtopainiketta käyttöön, jäljelle jäävän määrän arvona pysyy **0** eikä varastopoimintaa luoda. Lisätietoja on kohdassa [Projektin käytön seurannan määrittäminen](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-project-usage-tracking).

## <a name="pick-or-move-for-production-assembly-and-projects-in-a-basic-warehouse-configuration"></a>Tuotantoon, kokoonpanoon ja projekteihin poimiminen tai siirtäminen fyysisen varastoinnin perusmäärityksissä

Varaston poiminnan tai varaston siirron voi luoda kolmella tavalla:  

* Varsinaisesta lähdeasiakirjasta.  
* Useille lähdeasiakirjoille samanaikaisesti eräajon avulla.  
* Kahdessa vaiheessa. Lähdeasiakirja vapautetaan valmistelemaan lähdeasiakirja poimintaa varten. Varaston poiminnan tai siirron luominen **Varaston poiminta**- tai **Varaston siirto** -asiakirjoista. Varaston poiminta tai siirto perustuu lähdeasiakirjaan.  

### <a name="to-create-an-inventory-pick-from-the-source-document"></a>Varastopoiminnan lähdeasiakirjasta luominen

1. Lähdeasiakirjassa, joka voi olla tuotantotilaus tai projekti, valitaan **Luo varaston hyllytys tai poiminta** -toiminto.  
2. Valitse **Luo varaston poiminta** -valintaruutu.
3. Valitse **OK**-painike.

### <a name="to-create-an-inventory-movement-from-the-source-document"></a>Varaston siirron luominen lähdeasiakirjasta

1. Lähdeasiakirjassa, joka voi olla tuotantotilaus, kokoonpanotilaus tai projekti, valitaan **Luo varaston hyllytys tai poiminta** -toiminto.  
2. Valitse **Luo varaston siirto** -valintaruutu.
3. Valitse **OK**-painike.

### <a name="to-create-multiple-inventory-picks-or-movements-with-a-batch-job"></a>Useiden varaston poimintojen tai siirtojen luominen eräajon avulla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo varaston hyllytys/poiminta/siirto** ja valitse sitten vastaava linkki.  
2. Käytä **F.varastoinnin pyyntö** -pikavälilehden **Lähdeasiakirja**- ja **Lähteen nro** -kenttiä suodattamiseen asiakirjatyyppien tai asiakirjanumeroalueiden perusteella. Poiminnat voidaan luoda esimerkiksi vain myyntitilauksille.
3. Ota **Asetukset**-pikavälilehdessä **Luo varaston poiminta** tai **Luo varaston siirto** käyttöön vaihtopainikkeella.
4. Valitse **OK**-painike.

### <a name="to-create-inventory-picks-or-movements-in-two-steps"></a>Varaston poimintojen tai siirtojen luominen kahdessa vaiheessa

Lähdeasiakirjojen komponenttien poimiminen tai siirtäminen kahdessa vaiheessa edellyttää lähdeasiakirjan vapauttamista poiminnan valmistelua varten. Vapauta sisäisten toimintojen lähdeasiakirjat seuraavilla tavoilla.  

|Lähdeasiakirja|Vapautustapa|  
|---------------------|--------------------|  
|Tuotantotilaus|Vaihda **Suunniteltu tuotantotilaus** -sivulla tilauksen tilaksi **Vapautettu** tai luo vapautettu tuotantotilaus **Vapautettu tuotantotilaus** -sivulla.|  
|Kokoonpanotilaus|Vaihda kokoonpanotilauksen tilaksi **Vapautettu**.|
|Projektit | Vaihda projektin tilaksi **Avoin** tai luo heti projekti, jonka tila on Avoin.|  

Varastotyöntekijä, jolle nimikkeiden poiminta on määritetty, voi luoda lähdeasiakirjalle varaston hyllytysasiakirjan.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston poiminnat** tai **Varastosiirrot** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Valitse **Lähdeasiakirja**-kentässä hyllytettävän lähdeasiakirjan tyyppi.

    > [!NOTE]
    > **Varaston poiminta** -asiakirjoja ei voi käyttää kokoonpanon komponenttien poimimiseen.
4. Valitse **Lähteen nro** -kentässä lähdeasiakirja.  
5. Vaihtoehtoisesti voit valita **Hae lähdeasiakirja** -toiminnolla asiakirjan niiden saapuvien lähdeasiakirjojen luettelosta, jotka ovat sijainnissa valmiita poimintaan.  
6. Täytä poiminnan tai varaston siirron rivit valitun lähdeasiakirjan mukaisesti valitsemalla **OK**.  

## <a name="to-record-the-inventory-pick"></a>Varaston poiminnan kirjaaminen

1. Avaa **Varaston poiminta** -sivulla asiakirja, johon poiminta kirjataan.  
2. Poimintarivien **Varastopaikkakoodi**-kentässä varastopaikka, josta nimikkeet on poimittava ja jossa nimike on saatavana. Varastopaikkaan voi muuttaa tarvittaessa.
3. Suorita poiminta ja syötä poimittu määrä **Käsiteltävä määrä** -kenttään.

    Jos rivin nimikkeitä on poimittava useammasta kuin yhdestä varastopaikasta esimerkiksi siksi, että varastopaikka ei sisällä koko määrää, käytä **Rivit**-pikavälilehden **Jaa rivi** -toimintoa. Toiminto luo rivin jäljellä olevalle käsiteltävälle määrälle.  
4. Valitse **Kirjaa**-toiminto.  

Kirjausprosessin sisältö:

* Lähdeasiakirjan poimittujen rivien kulutuksen kirjaaminen.
* Jos sijainti käyttää varastopaikkoja, kirjaus luo myös fyysiset varastotapahtumat, joilla muutokset varastopaikan määrään kirjataan.

[!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="to-record-the-inventory-movement"></a>Varastosiirron kirjaaminen

1. Avaa **Varastosiirto**-sivulla asiakirja, johon varaston siirto kirjataan.  
2. Varaston siirron rivien **Varastopaikkakoodi**-kentässä varastopaikkaa, josta nimikkeet poimitaan, ehdotetaan nimikkeen oletusvarastopaikan ja saatavuuden mukaan. Varastopaikkaan voi muuttaa tarvittaessa.  
3. Suorita varaston siirto ja syötä siirretty määrä **Käsiteltävä määrä** -kenttään. Ota- ja Aseta-rivien arvojen on oltava samat. Varaston siirron rekisteröiminen ei ole muutoin mahdollista.

    Jos rivin nimikkeitä on otettava useammasta kuin yhdestä varastopaikasta esimerkiksi siksi, että varastopaikka ei sisällä koko määrää, käytä **Rivit**-pikavälilehden **Jaa rivi** -toimintoa. Toiminto luo rivin jäljellä olevalle käsiteltävälle määrälle.  
4. Valitse **Rekisteröi varastosiirto** -toiminto.  

Kirjausprosessin sisältö:

* Fyysisen varastoinnin tapahtumat ilmaisevat nyt, että komponentit ovat lähdeasiakirjan tilausriveillä määritetyissä varastopaikoissa. Esimerkiksi kokoonpanotilauksen, tuotannon komponentin tai projektin suunnittelun rivi.

>[!NOTE]
> Toisin kuin siirrettäessä komponentteja varaston poimintoina kulutusta ei kirjata varastosiirron rekisteröinnin yhteydessä. Kulutus rekisteröidään erillisenä vaiheena kirjaamalla lähdeasiakirja.

## <a name="flushing-production-components-in-a-basic-warehouse-configuration"></a>Tuotannon komponenttien materiaaliotot fyysisen varastoinnin perusmäärityksissä

Materiaaliottotavat vaikuttavat komponenttien siirtymiseen tuotantoon. Lisätietoja on kohdassa [Komponenttien materiaalinotto toiminnan tuotoksen mukaan](production-how-to-flush-components-according-to-operation-output.md). Valitun materiaaliottomenetelmän mukaan komponentteja voidaan poimia tuotantoon seuraavilla tavoilla:

* Käyttämällä **Varaston poiminta** -asiakirjaa **Manuaalinen**-materiaaliottomenetelmää käyttävien nimikkeiden poiminnan kirjaamiseen. Kun rekisteröit varaston poiminnan, poimittujen komponenttien kulutus kirjataan. 
* Käyttämällä viitteen lähdeasiakirjaan sisältävää **Varastosiirto**-asiakirjaa kirjaamaan **Manuaalinen**-materiaaliottomenetelmää käyttävien komponenttien poiminnat. Kulutus on rekisteröitävä erikseen. Lisätietoja on kohdassa [Tuotannon kulutuksen eräkirjaus](production-how-to-post-consumption.md). 
* Käyttämällä viitteen lähdeasiakirjaan sisältävää **Varastosiirto**-asiakirjaa kirjaamaan **Poiminta + eteenpäin**- tai **Poiminta + taaksepäin** -materiaaliottomenetelmää käyttävien komponenttien poiminnat. Komponentteja kulutetaan automaattisesti, joko muutettaessa tuotantotilauksen tilaa taikka aloitettaessa tai lopetettaessa työvaihetta. Kaikkien pakollisten komponenttien on oltava saatavana. Muutoin kyseisen komponentin materiaalinoton kirjaus lopetetaan.
* Käyttämällä **Varastosiirto**-asiakirjaa viittaamatta lähdeasiakirjaan tai kirjaamalla muulla tavoin **Eteenpäin**- tai **Taaksepäin**-materiaaliottomenetelmää käyttävien komponenttien varaston siirrot. Komponentteja kulutetaan automaattisesti, joko muutettaessa tuotantotilauksen tilaa taikka aloitettaessa tai lopetettaessa työvaihetta. Kaikkien pakollisten komponenttien on oltava saatavana. Muutoin kyseisen komponentin materiaalinoton kirjaus lopetetaan. Lisätietoja on kohdassa [Nimikkeiden sisäinen siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="example"></a>Esimerkki

Nimikkeellä SP-SCM1004 on 15 kappaleen tuotantotilaus.. Joidenkin komponenttiluettelon nimikkeiden materiaaliotto on tehtävä manuaalisesti kulutuspäiväkirjassa, kun taas joidenkin nimikkeiden poiminta ja materiaaliotto voidaan tehdä automaattisesti käyttämällä **Poimi + taaksepäin** -materiaaliottomenetelmää.  

Seuraavissa vaiheissa on esimerkki toiminnoista, joita eri henkilöt tekevät ja niihin liittyviä vastauksia:  

1. Kaupan työnjohtaja vapauttaa tuotantotilauksen. Nimikkeet, jotka käyttävät **Eteenpäin**-materiaalinottotapaa ja joilla ei ole reitityslinkkiä, vähennetään avoimen tuotannon varastopaikasta.  
2. Tuotannon työnjohtaja valitsee tuotantotilauksessa **Luo varaston hyllytys tai poiminta** -toiminnon sekä ottaa **Luo varaston poiminta**- ja **Luo varastosiirto** -vaihtoehdot käyttöön vaihtopainikkeella. Nimikkeille luodaan varaston hyllytysasiakirja, jossa materiaaliottomenetelmänä on **Manuaalinen**. Nimikkeille luodaan varastosiirto, jossa materiaaliottomenetelminä on **Poiminta + eteenpäin** ja **Poiminta + taaksepäin**.
3. Varastopäällikkö määrittää poiminnat ja varaston siirrot varastotyöntekijälle.
4. Varastotyöntekijä poimii nimikkeet soveltuvista varastopaikoista ja asettaa ne tuotannon valmisteluvarastopaikkaan tai varastosiirrossa määritettyyn varastopaikkaan. Varastopaikka voi olla tuotantosolun tai kuormitusryhmän varastopaikka.  
5. Varastotyöntekijä kirjaa poiminnan. Määrä vähennetään varastopaikoista.
6. Varastotyöntekijä kirjaa varaston siirron. Määrää vähennetään poiminnan varastopaikoista ja lisätään kulutuksen varastopaikkaan. kaikkien poimittujen nimikkeiden **Poimittu määrä** -kenttä osaluettelossa on päivitetty.  
7. Koneenkäyttäjä tiedottaa tuotantojohtajaa, että loppukohdat ovat lopussa.  
8. Tuotannon työnjohtaja käyttää tuotospäiväkirjaa tai tuotantopäiväkirjaa tuotoksen kirjaamiseen. **Poiminta + eteenpäin**- tai **Poiminta + taaksepäin** -materiaaliottomenetelmää ja reitityslinkkejä käyttävien komponentin nimikkeiden määrä vähennetään tuotannon valmisteluvarastopaikasta.
9. Tuotantopäällikkö vaihtaa tuotantotilauksen tilaksi **Valmis**. Komponentin **Taaksepäin**-materiaaliottomenetelmää käyttävien komponentin nimikkeiden määrä vähennetään avoimesta tuotannon varastopaikasta ja sellaisten **Poiminta + taaksepäin** -materiaaliottomenetelmää käyttävien komponentin nimikkeiden määrä vähennetään tuotannon valmisteluvarastopaikasta, joissa ei ole reitityslinkkiä.  

 Seuraavassa kuvassa esitetään, milloin **Bin-koodi** -kenttä osaluettelossa täytetään sijainnin tai koneen/työkeskuksen asetusten mukaisesti.  

:::image type="content" source="media/binflow.png" alt-text="Yleiskatsaus Varastopaikkakoodi-kenttä täyttämisen ajankohdasta ja täyttämistavasta.":::

## <a name="see-also"></a>Katso myös

[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Varastonhallinnan yleiskatsaus](design-details-warehouse-management.md)
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
