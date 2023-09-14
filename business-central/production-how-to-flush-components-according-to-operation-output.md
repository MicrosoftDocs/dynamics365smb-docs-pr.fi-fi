---
title: Komponenttien materiaalinotto toiminnan tuotoksen mukaan
description: 'Tässä ohjeaiheessa kuvataan, miten komponenttien materiaalinotto tehdään toiminnon tuotoksen ja muiden materiaalinottomenetelmien mukaan.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/22/2021
ms.author: bholtorf
---
# Komponenttien materiaalinotto toiminnan tuotoksen mukaan
Voit määrittää erilaisia materiaaliottostrategioita automatisoimaan komponenttien kulutuksen rekisteröintiä. 

Tämä toiminto on hyödyllinen seuraavista syistä:  

- **Varaston arvostus**

    Tuotoksen ja kulutuksen arvotapahtumat luodaan rinnakkain tuotantotilauksen edetessä. Ilman reitityslinkkien koodeja varastoarvo kasvaa, kun tuotos kirjataan ja vähenee sitten myöhemmin, kun komponentin kulutusarvo kirjataan yhdessä valmiin tuotantotilauksen kanssa.  
- **Varastosaatavuus**

    Asteittaista kulutuskirjausta käytettäessä komponenttinimikkeiden saatavuus on paremmin ajan tasalla, mikä on tärkeää kysynnän ja tarjonnan välisen sisäisen tasapainon ylläpitämiseksi. Ilman reitityslinkkien koodeja muut osan vaatimukset voivat olettaa, että se on käytettävissä, niin kauan kuin se odottaa viivästynyttä kulukirjausta.  
- **Just-in-Time**

    Voit mukauttaa tuotteita asiakkaan pyyntöjen mukaan ja siten minimoida jätteet varmistamalla, että työ- ja järjestelmämuutoksia tehdään vain tarvittaessa.  

- **Tietojen syötön vähentäminen**

    Kun operaation materiaalinotto voidaan toteuttaa automaattisesti, kulutuksen ja tuotosten koko kirjausprosessi voidaan automatisoida. Se haitta automaattisessa materiaalinotossa kuitenkin on, että hukkatavaran kirjauksessa voi olla virheitä tai hukkatavara voi jäädä kokonaan huomaamatta.

## Kulutuksen automaattisen kirjaamisen (materiaalinotto) menetelmät  

- koko tilauksen Eteenpäin-materiaalinotto  
- operaatiokohtainen Eteenpäin-materiaalinotto  
- operaatiokohtainen Taaksepäin-materiaalinotto  
- koko tilauksen Taaksepäin-materiaalinotto.  

### Automaattinen raportointi - koko tilauksen Eteenpäin-materiaalinotto  
Jos tuotantotilaukselle tehdään työn alussa Eteenpäin-materiaalinotto, sovellus toimii lähes samoin kuin manuaalista kulutusta käytettäessä. Suurin ero on siinä, että kulutus tapahtuu automaattisesti.  

- Tuotannon tuoterakenteen koko sisältö kulutetaan ja vähennetään varastosta, kun vapautettu tuotantotilaus päivitetään.  
- Kulutusmäärä on tuotannon tuoterakenteessa määritetyn kokoonpanokohtaisen määrän ja rakennettavien päänimikkeiden määrän tulo.  
- Kulutuspäiväkirjaan ei tarvitse kirjata tietoja, jos kaikille nimikkeille on tarkoitus tehdä materiaalinotto.  
- Kun varaston nimikkeitä kulutetaan, tuotospäiväkirjan tapahtumien kirjausajankohdalla ei ole merkitystä. Tuotospäiväkirjalla ei ole vaikutusta, kun kulutusta kirjataan tällä tavalla.  
- Reitityslinkin koodeja ei voi määrittää.  

Koko tilauksen Eteenpäin-materiaalinotto sopii tuotantoympäristöihin, joissa  

-   valmistusvirheitä on vähän  
-   toimenpiteitä on vähän  
-   alkupään toimenpiteissä kulutetaan paljon komponentteja.  

### Automaattinen raportointi - operaatiokohtainen Eteenpäin-materiaalinotto  
Operaatiokohtaisen materiaalinoton avulla voit vähentää varastoa tietyn päänimikkeen reitityksen operaation aikana. Materiaali on sidottu reititykseen reitityslinkin koodeilla, jotka vastaavat komponenteille tuotannon tuoterakenteessa määritettyjä reitityslinkin koodeja.  

Materiaalinotto tapahtuu, kun saman reitityslinkin koodin mukainen operaatio alkaa. Operaatio katsotaan alkaneeksi, kun sen tietoja kirjataan operaation tuotospäiväkirjaan. Kirjattavat tiedot voivat olla esimerkiksi asetusajan syöttäminen.  

Materiaalinoton määrä on tuotannon tuoterakenteessa määritetyn kokoonpanokohtaisen määrän ja rakennettavien päänimikkeiden määrän tulo (oletettu määrä).  

Tämä tekniikka sopii parhaiten tilanteisiin, joissa operaatioita on useita ja osaa komponenteista käytetään vasta loppupään kokoonpanovaiheessa. Just-in-Time (JIT) -mallissa nimikkeet eivät välttämättä edes ole käsillä, kun RPO aloitetaan.  

Materiaalia voi kuluttaa operaatioiden aikana reitityslinkin koodien avulla. Kaikkia komponentteja ei välttämättä käytetä ennen viimeisiä kokoonpano-operaatioita, eikä niitä tule ottaa varastosta ennen sitä.  

### Automaattinen raportointi - operaatiokohtainen Taaksepäin-materiaalinotto  
Operaatiokohtaisessa Taaksepäin-materiaalinotossa kulutus kirjataan sen jälkeen, kun operaatio on kirjattu tuotospäiväkirjaan.  

Tästä menetelmästä on se hyöty, että operaation valmiiden osien määrä tunnetaan.  

Tuotannon tuoterakenteen materiaali on linkitetty reititystietueisiin reitityslinkin koodeilla. Taaksepäin-materiaalinotto tapahtuu, kun sellainen tietyn reitityslinkin koodin mukainen operaatio kirjataan, jonka määrä on valmis.  

Materiaalinoton määrä on tuotannon tuoterakenteessa määritetyn kokoonpanokohtaisen määrän ja kyseiseen operaatioon tuotoksen määränä kirjattujen päänimikkeiden määrän tulo. Se ei välttämättä ole sama kuin oletettu määrä.  

### Automaattinen raportointi - koko tilauksen Taaksepäin-materiaalinotto  
Reitityslinkin koodeja ei oteta huomioon tässä raportointimenetelmässä.  

Komponentit valitaan vasta, kun vapautetun tuotantotilauksen tilaksi vaihtuu *Valmis*. Materiaalinoton määrä on tuotannon tuoterakenteessa määritetyn kokoonpanokohtaisen määrän ja valmistuneiden ja varastoon lisättyjen päänimikkeiden määrän tulo.  

Taaksepäin-materiaalinoton käyttäminen koko tuotantotilauksessa edellyttää, että määritykset ovat samat kuin eteenpäin-materiaalinotossa: raportointitavaksi täytyy määrittää taaksepäin jokaisen nimikkeen kortissa ja se täytyy tehdä päätuoterakenteen kaikille raportoitaville nimikkeille. Myös kaikki reitityslinkin koodit täytyy poistaa tuotannon tuoterakenteesta. 



Tuotantotilauksessa voidaan esimerkiksi määrittää, että 800 metrin tuottaminen vaatii 8 kg komponentteja. Jos tuotokseksi kirjataan 200 metriä, kulutukseksi kirjataan automaattisesti 2 kg. Se tehdään yhdistämällä taaksepäin suuntautuvan materiaalinottomenetelmä ja reitityslinkkien koodit siten, että materiaalinottomäärä toimintoa kohden on verrannollinen toiminnon todelliseen tuotokseen. Jos nimikkeiden määrityksessä on käytetty Taaksepäin-materiaalinottotapaa, oletustoiminto laskee ja kirjaa kulutuksen automaattisesti, kun vapautetun tuotantotilauksen tilaksi muutetaan **Valmis**. Jos määrität myös reitityslinkin koodeja, laskenta ja kirjaus tehdään toiminnon valmistuttua. Toiminnon kuluttama todellinen määrä kirjataan. Lisätietoja on kohdassa [Reititysten luominen](production-how-to-create-routings.md).  

## Voit tyhjentää osat toiminnon tuotoksen mukaan

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2.  Valitse **Muokkaa** -toiminto.  
3.  Valitse **Täydennys**-pikavälilehden **Materiaalinottotapa**-kentässä **Taaksepäin**.  

    > [!NOTE]  
    >  Valitse **Poiminta + taaksepäin**, jos komponenttia käytetään ohjatuille hyllytyksille ja poiminnoille määritetyssä sijainnissa.  

4.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Reititykset** ja valitse sitten vastaava linkki.  
5.  Määritä reitityslinkkikoodit jokaiselle työvaiheelle, joka kuluttaa komponentin. Lisätietoja on kohdassa [Reititysten luominen ](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > Älä käytä samaa reitityslinkkiä reitityksen eri toiminnoille, sillä silloin kunkin linkitetyn toiminnon komponentin kulutus rekisteröidään.  
6.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotannon tuoterakenne** ja valitse sitten vastaava linkki.  
7.  Määritä reitityslinkkikoodit kustakin komponentin esiintymästä toimintoon, jossa se kulutetaan.

Kulutus kirjataan automaattisesti, kun tuotos rekisteröidään. Lisätietoja on kohdassa [Tuotoksen ja ajoaikojen eräkirjaaminen](production-how-to-post-output-quantity.md).

## Materiaalinottotavat

Seuraavassa taulukossa käsitellään käytettävissä olevia materiaaliottomenetelmien vaihtoehtoja, jotka voidaan määrittää **Nimike**- ja **Varastointiyksikkö**-korteissa.

|Asetus|Kuvaus|
|------------|-------------|  
|Manuaalinen|Edellyttää, että annat ja kirjaat kulutuksen manuaalisesti kulutuspäiväkirjaan.|
|Eteenpäin|Kirjaa kulutuksen automaattisesti tuotantotilauksen osarivien mukaan. <br><br>Oletusarvon mukaan komponentin kulutuksen kirjaus tapahtuu, kun tuotantotilauksen tila muutetaan **vapautetuksi**. Jos kuitenkin käytät tuotantotilauksen komponenttirivien **Reitityslinkin** koodi -kenttää, kirjaukset tehdään toiminnoittain toiminnon käynnistyessä. Lisätietoja on kohdassa [Reitityslinkkien luominen](production-how-to-create-routings.md#to-create-routing-links). <br><br> **Huomautus**<br>Eteenpäin tapahtuvassa materiaalinotossa reitityslinkin koodien yhteydessä saatava toimintokohtainen kirjaus perustuu komponenttirivillä määritettyyn oletettuun määrään. Lisätietoja toimintokohtaisista materiaalinotoista toteutuneen tuloksen mukaan on tämän aiheen **Taaksepäin**-kuvauksessa.<br><br>Jos sijainnille tai resursseille, joissa tämä komponentti kulutetaan, on määritetty varastopaikan oletusrakenne, nimike kulutetaan **avoimen tuotannon varastopaikasta**. Lisätietoja on kohdassa [Toimintaohje: Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md). <br><br> **Tärkeää** <br>Eteenpäin suuntautuva materiaalinotto tapahtuu myös, kun valitset tyhjästä luodussa vapautetussa tuotantotilauksessa **Päivitä**. Näissä suoraan luoduissa vapautetuissa tuotantotilauksissa ei voi muuttaa varastopaikkatietoja, koska tuotantotilauksen komponenttirivit luodaan tilauksen päivityksen yhteydessä, jolloin komponentteja samalla siirretään eteenpäin. Jos siis halutaan muuttaa tuotantotilauksen osarivien varastopaikkatietoa ennen tyhjennyksen tapahtumista, luotavan tilauksen tilan on oltava *Suunniteltu* tai *Sitovasti suunniteltu*.|
|Taaksepäin|Laskee ja kirjaa kulutuksen automaattisesti tuotantotilauksen osarivien mukaan.<br><br> Oletusarvon mukaan komponentin kulutuksen laskenta ja kirjaus tapahtuu, kun vapautetun tuotantotilauksen tilaksi muutetaan **Valmis**. Jos kuitenkin käytät tuotantotilauksen komponenttirivien **Reitityslinkin koodi** -kenttää, laskennat ja kirjaukset tehdään kunkin toiminnon päättyessä.<br><br> **Huomautus** <br>Taaksepäin suuntautuvat materiaalinoton ja reitityslinkkien koodit voidaan yhdistää niin, että materiaalinottomäärä toimintoa kohden on verrannollinen toiminnon todelliseen tuotokseen. Lisätietoja on kohdassa [Komponenttien materiaalinotto toiminnan tuotoksen mukaan](#to-flush-components-according-to-operation-output).<br><br> Jos sijainnille tai kuormitusryhmälle, jossa tämä komponentti kulutetaan, on määritetty varastopaikan oletusrakenne, nimike kulutetaan **avoimen tuotannon varastopaikasta**.|
|Poiminta + eteenpäin|Sama kuin materiaalinottotapa eteenpäin lukuun ottamatta sitä, että toimintoa käytetään vain sijainneissa, joissa käytetään joko varastoinnin laajennettua määritystä tai varastoinnin perusmääritystä ja pakollisia varastopaikkoja.<br><br> Kulutus lasketaan ja kirjataan varastopaikasta, joka on määritetty **Tuotannon valm.var.paik.koodi** -kentässä sijainnissa tai kuormitusryhmässä sen jälkeen, kun komponentti on poimittu varastosta.<br><br> **Huomautus** <br>Jos komponentin materiaalinottotavaksi on määritetty Poiminta + Eteenpäin, sillä ei voi olla toiminnon reitityslinkkikoodia, jonka materiaalinottotavaksi on määritetty Eteenpäin. Osa poistetaan automaattisesti toiminnon alkaessa, minkä vuoksi poimintatoimintoa ei voi pyytää.|
|Poiminta + taaksepäin|Sama kuin materiaalinottotapa taaksepäin lukuun ottamatta sitä, että toimintoa käytetään vain sijainneissa, joissa käytetään joko varastoinnin laajennettua määritystä tai varastoinnin perusmääritystä ja pakollisia varastopaikkoja.<br><br> Kulutus lasketaan ja kirjataan varastopaikasta, joka on määritetty **Tuotannon valm.var.paik.koodi** -kentässä sijainnissa tai kuormitusryhmässä sen jälkeen, kun komponentti on poimittu varastosta.|

## Katso myös

[Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)  
[Suunnittelu](production-planning.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
