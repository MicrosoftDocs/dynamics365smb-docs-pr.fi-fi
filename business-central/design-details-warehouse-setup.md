---
title: Rakennetiedot – Fyysisen varastoinnin asetukset | Microsoft Docs
description: Business Central-sovelluksen fyysisen varastoinnin toiminnolla on erilaisia monimutkaisuustasoja, jotka perustuvat valittavissa olevien yksiköiden käyttöoikeuksiin. Varastoratkaisun monimutkaisuuden taso määritellään laajasti binin asetusten mukaisesti sijaintikorteissa, joka vuorostaan on lisenssikontrolloitu niin, että binin määrityskenttien käyttö määritellään lisenssissä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/04/2020
ms.author: sgroespe
ms.openlocfilehash: cd2a282e95e324e3adbf06cb72c53467f63c227b
ms.sourcegitcommit: ccae3ff6aaeaa52db9d6456042acdede19fb9f7b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435229"
---
# <a name="design-details-warehouse-setup"></a>Rakennetiedot: f. varaston asetus

[!INCLUDE[d365fin](includes/d365fin_md.md)]in fyysisen varastoinnin toiminnolla on erilaisia monimutkaisuustasoja, jotka perustuvat valittavissa olevien yksiköiden käyttöoikeuksiin. Varastoratkaisun monimutkaisuuden taso määritellään laajasti binin asetusten mukaisesti sijaintikorteissa, joka vuorostaan on lisenssikontrolloitu niin, että binin määrityskenttien käyttö määritellään lisenssissä. Lisäksi lisenssin sovellusobjektit hallitsevat mitä käyttöliittymäasiakirjaa käytetään tuetuille varastotoiminnoille.  

Seuraavat varastoon liittyvät yksiköt ovat olemassa:  

- Perusvarasto (4010)  
- Varastopaikka (4170)  
- Hyllytys (4180)  
- F. varastoinnin vastaanotto (4190)  
- Poiminta (4200)  
- Fyysisen varaston toimitus (4210)  
- Varastoinninhallintajärjestelmät (4620)  
- Sisäiset poiminnat ja hyllytykset (4630)  
- Automaattinen tiedonkeruujärjestelmä (4640)
- Varastopaikan asetus (4660)  

Lisätietoja kustakin yksiköstä on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]in hinnastot](https://go.microsoft.com/fwlink/?LinkId=238341) (edellyttää PartnerSource-tiliä).  

Seuraavassa taulukossa käsitellään mitä yksiköitä vaaditaan määrittämään eri fyysisen varastoinnin monimutkaisuustasot, mitkä käyttöliittymäasiakirjat tukevat kutakin tasoa ja mitkä sijaintikoodit heijastavat näitä tasoja [!INCLUDE[d365fin](includes/d365fin_md.md)]in esittelytietokannassa.  

|Monimutkaisuustaso|Description|Käyttöliittymäasiakirja|CRONUS-sijainti|Yksikön vähimmäisvaatimus|  
|----------------|-----------|-----------|---------------|---------------------------|  
|1|Ei määritettyä fyysisen varaston toimintaa.<br /><br /> Vastaanotto-/toimituskirjaus tilauksista.|Tilaus|SININEN|Perusvarasto|  
|2|Ei määritettyä fyysisen varaston toimintaa.<br /><br /> Vastaanotto-/toimituskirjaus tilauksista.<br /><br /> Lokerokoodi vaaditaan.|Tilaus varastopaikkakoodilla|HOPEINEN|Perusvarasto/lokero|  
|3 <br /><br /> **Huomautus**: Vaikka asetusten nimenä on **Vaadi poiminta** ja **Vaadi hyllytys**, voit silti kirjata vastaanottoja ja toimituksia suoraan lähdeasiakirjoista sijainneissa, joissa olet valinnut nämä valintaruudut.|F. varaston perustoiminnot tilauskohtaisesti.<br /><br /> Vastaanotto-/toimituskirjaus varaston hyllytyksestä/poiminta-asiakirjoista. <br /><br /> Lokerokoodi vaaditaan.|Varaston hyllytys/varastosiirto/varaston poiminta, varastopaikkakoodilla|(HOPEA + vaadi hyllytys tai vaadi hyllytys)|Perusvarasto/lokero/hyllytys/poiminta|  
|4|Lisävarastoinnin toiminto useille tilauksille.<br /><br /> Konsolidoitu vastaanotto ja toimituksen kirjaus f. varaston hyllytys/poimintarekisteröintien perusteella.|Fyysisen varastoinnin vastaanotto / fyysisen varastoinnin hyllytys / fyysisen varastoinnin poiminta / fyysisen varastoinnin toimitus / poimintatyökirja|VIHREÄ|Perusvarasto/f. var. vastaanotto/hyllytys/poiminta/f. var. toimitus|  
|5|Lisävarastoinnin toiminto useille tilauksille.<br /><br /> Konsolidoitu vastaanotto ja toimituksen kirjaus f. varaston hyllytys/poimintarekisteröintien perusteella.<br /><br /> Lokerokoodi vaaditaan.|Fyysisen varastoinnin vastaanotto / fyysisen varastoinnin hyllytys / fyysisen varastoinnin poiminta / fyysisen varastoinnin toimitus / poimintatyökirja / hyllytystyökirja ja varastopaikan koodi|(VIHREÄ + varastopaikka pakollinen)|Perusvarasto/lokero/f. var. vastaanotto/hyllytys/poiminta/f. var. toimitus|  
|6 <br /><br /> **Huomautus**: Tätä tasoa kutsutaan nimellä VHJ, koska se edellyttää kaikkein laajimman yksikön eli varastoinninhallintajärjestelmän käyttöä.|Lisävarastoinnin toiminto useille tilauksille<br /><br /> Konsolidoitu vastaanotto ja toimituksen kirjaus f. varaston hyllytys/poimintarekisteröintien perusteella<br /><br /> Lokerokoodi vaaditaan.<br /><br /> Alueen/Luokan koodi on valinnainen.<br /><br /> Työnkulun ohjaamat varastotyöntekijät<br /><br /> Varastopaikan täydennyksen suunnittelu<br /><br /> Varastopaikan luokittelu<br /><br /> Varastopaikan asetus kapasiteetin mukaan<br /><br /> Sijoittelu <!-- Hand-held device integration -->|Fyysisen varastoinnin vastaanotto / fyysisen varastoinnin hyllytys / fyysisen varastoinnin poiminta / fyysisen varastoinnin toimitus / fyysisen varaston siirto / poimintatyökirja / hyllytystyökirja / sisäinen fyysisen varaston poiminta / sisäinen fyysisen varastoinnin hyllytys ja varastopaikan/luokan/alueen koodi<br /><br /> Varastopaikan hallinnan erilaiset työkirjat<br /><br /> ADCS-näytöt|VALKOINEN|Perusvarasto/varastopaikka/hyllytys/f. var. vastaanotto/poiminta/f. var. toimitus/varastoinninhallintajärjestelmät/sisäiset poiminnat ja hyllytykset/varastopaikan määritys<!-- Automated Data Capture System/ -->Varastopaikan asetus|  

Esimerkkejä käyttöliittymäasiakirjojen käytöstä kullakin fyysisen varaston monimutkaisuustasolla on kohdassa [Rakennetiedot: saapuvan fyysisen varastoinnin virta](design-details-inbound-warehouse-flow.md).  

## <a name="bin-and-bin-content"></a>Varastopaikka ja varastopaikan sisältö

Lokero on tallennuslaite, jonka tarkoituksena on tallentaa erilliset osat. Pienin [!INCLUDE[d365fin](includes/d365fin_md.md)]in varastoyksikkö. Varastopaikkojen nimikemääriä kutsutaan varastopaikan sisällöksi. **Nimike**- tai **Lokerokoodi**-kentästä suoritettu haku missä tahansa fyysiseen varastoon liittyvässä asiakirjassa näyttää lokerossa olevan nimikkeen lasketun saatavuuden.  

Lokero sisällölle voidaan antaa ominaisuudeksi kiinteä, erityisvarastopaikka tai oletus, joka määrittää kuinka lokeron sisältöä voidaan käyttää. Varastopaikkoja, joilla ei ole näitä ominaisuuksia kutsutaan määrittelemättömiksi varastopaikoiksi.  

Kiinteä lokero sisältää kohteita, jotka on määritelty kyseisen lokeron koodille. Kiinteä binin ominaisuus varmistaa, että vaikka binin sisältö on tällä hetkellä tyhjennetty, binin sisältö ei katoa ja tämän vuoksi bin valitaan uudelleen heti kun se on täydennetty.  

Erityisvarastopaikka sisältää lokeron sisällön, joka voidaan poimia vain erityiselle resurssille, kuten kuormitusryhmälle, joka käyttää kyseistä lokeroa. Muu ei poimittu sisältö, kuten lähtevät määrät toimituksen kirjauksessa, voidaan vielä kuluttaa erityisvarastopaikasta. Vain **Luo poiminta**-algoritmin huomioima varastopaikan sisältö on suojattu erityisvarastopaikassa.  

Bin-tiedoston oletusominaisuutta käytetään järjestelmässä ehdottamaan binejä varastoaktiviteeteille. WMS-sijainneissa ei käytetä oletuslokero-ominaisuutta. Paikoissa, joissa on lokerot vaaditaan, ominaisuutta käytetään saapuvissa virroissa määrittämään nimikkeiden sijoittamista. Lähtevissä virroissa ominaisuutta käytetään määrittämään mistä nimikkeet otetaan.  

> [!NOTE]  
>  Jos lähtevät nimikkeet sijoitetaan useisiin varastopaikkoihin, nimikkeet otetaan ensin ei oletusarvoisista varastopaikoista tämän varastopaikan sisällön tyhjentämiseksi ja sitten jäljellä olevat nimikkeet otetaan oletusvarastopaikasta.  

Sijainnin nimikkeellä voi olla vain yksi varastopaikka.  

## <a name="bin-type"></a>Varastopaikan tyyppi

WMS-asennuksissa voit rajoittaa varastopaikalle sallittuja varastotoimintoja määrittämällä sille varastotyypin. Käytössä on seuraavat lokerotyypit:  

|Varastopaikan tyyppi|Kuvaus|  
|------------------|---------------------------------------|  
|VAST.OTTO|Nimikkeet, jotka on kirjattu vastaanotetuiksi mutta niitä ei ole vielä hyllytetty.|  
|TOIM|Nimikkeet, jotka on poimittu fyysisen varastoinnin toimitusriveille, mutta joita ei ole vielä kirjattu toimitetuiksi.|  
|HYLLYTYS|Yleensä kohteet voidaan tallentaa suurina mittayksiköinä, mutta et halua käyttää sitä poimintatarkoituksiin. Koska näitä varastopaikkoja ei käytetä keräilyyn, niin tuotantotilauksia kuin toimituksiakaan varten, Hyllytys-tyyppisten varastopaikkojen käyttö voi olla rajallista, mutta tämä varastopaikan tyyppi voi olla hyödyllinen, jos olet ostanut suuren määrän nimikkeitä. Tämän tyyppisillä varastopaikoilla pitäisi aina olla matala varastopaikan luokitus, jotta kun vastaanotetut nimikkeet hyllytetään, muut nimikkeeseen liitetyt korkeamman luokituksen PUTPICK-varastopaikat hyllytetään ensin. Jos käytät tämän tyyppistä varastopaikkaa, sinun täytyy tehdä varastopaikan täydennys säännöllisesti, jotta näihin varastopaikkoihin varastoidut nimikkeet olisivat saatavilla myös HYLLPOIM- ja POIMINTA-tyyppisissä varastopaikoissa.|  
|POIMINTA|Vain poimintaan käytettävät nimikkeet. Vain siirtymä voi aiheuttaa näiden binien täytön, ei poisto.|  
|HYLLPOIM|Nimikkeet varastopaikoissa, joille on ehdotettu sekä hyllytys- että poimintatoimintoa. Tämän tyyppisillä varastopaikoilla on todennäköisesti eri varastopaikan luokitteluja. Voit määrittää irtotavaran varastopaikat tämän tyyppiseksi varastopaikaksi, jolla on matalia varastopaikan luokitteluja verrattuna tavallisiin poimintavarastopaikkoihin tai edelleen poimimisen alueiden varastopaikkoihin.|  
|QC|Tätä varastopaikkaa käytetään varastomuutoksille, jos varastopaikka määritetään sijaintikortissa **Muutosvarastopaikan koodi** -kentässä. Tämän tyyppisiä varastopaikkoja voi määrittää myös viallisille nimikkeille ja tarkastettaville nimikkeille. Nimikkeitä voi siirtää tämän tyyppiseen varastopaikkaan, jos haluat, että ne eivät ole saatavilla tavallisessa nimikevirrassa. **Huomautus:** Toisin kuin kaikki muut varastopaikkatyypit, **QC**-varastopaikkatyypillä ei ole valittuna nimikkeen käsittelyn valintaruutuja oletusarvoisesti. Tämä osoittaa, että QC-varastopaikkaan asetettu sisältö jää pois nimikevirroista.|  

Kaikkien varastopaikan tyyppien osalta, lukuun ottamatta POIMINTA-, HYLLYPOIMINTA- ja HYLLYTYS-tyyppejä, varastopaikalle ei sallita mitään muita toimintoja kuin mitä varastopaikan tyyppi määrittää. Esimerkiksi **Vastaanotto**-tyypin varastopaikkaa voidaan käyttää vain nimikkeiden vastaanottamiseksi tai nimikkeiden poimintaan.  

> [!NOTE]  
> Vain siirto voidaan luoda varastopaikkoihin joiden tyyppi on VASTAANOTTO ja QC. Samoin vain liikkeitä voidaan tehdä bineistä, joiden tyyppi on SHIP ja QC.  

## <a name="bin-ranking"></a>Varastopaikan luokittelu

Laajennetussa varastoinnissa voit automatisoida ja optimoida nimikkeiden keräystavan hyllytys- ja poimintatyökirjoissa luokittelemalla varastopaikat niin, että nimikkeet otetaan tai asetetaan luokitusehdon mukaisesti varaston käyttämiseksi optimaalisesti.  

Hyllytysprosessit on optimoitu varastopaikan luokittelun mukaan ehdottamalla korkeamman luokan varastopaikkoja ennen alemman luokan varastopaikkoja. Vastaavasti poimintaprosessit on optimoitu ehdottamalla varastopaikan sisällöstä ensin korkean luokan nimikkeitä. Lisäksi ehdotetaan varastopaikan täydennyksiä alemman luokan varastopaikoista korkean luokan varastopaikkoihin.  

Varastopaikan luokittelu yhdessä varastopaikan sisältötietojen kanssa ovat perusominaisuuksia, jotka antavat käyttäjälle mahdollisuuden lokeroida nimikkeitä f. varastossa.  

## <a name="bin-setup"></a>Varastopaikan asetus  
Laajennetussa varastoinnin varastopaikat voidaan määrittää kapasiteettiarvoilla, kuten määrä, kokonaiskuutiotilavuus ja paino, ja niiden perusteella hallitaan nimikkeiden varastointia varastopaikassa.  

Voit määrittää jokaiseen nimikkeen korttiin nimikkeelle mittayksikön, kuten kappaletta, kuormalavaa, litraa, grammaa tai laatikkoa. Nimikkeellä voi olla myös perusmittayksikkö, jolle voidaan määrittää siihen perustuvia suurempia mittayksiköitä. Voi esimerkiksi määrittää kuormalavan vastaamaan 16 kappaletta niin, että myöhempi perustuu perusmittayksikköön.  

Jos haluat määrittää tietyn nimikkeen tallennettavan enimmäismäärän tietyssä varastopaikassa ja nimikkeellä on useampi kuin yksi mittayksikkö, sinun on asetettava enimmäismäärä jokaiselle nimikkeen kortin mittayksikölle. Jos nimike on vastaavasti määritetty käsiteltäväksi kappaleina ja kuormalavoina, myös nimikkeen **Varastopaikan sisältö** -sivun **Enimmäismäärä**-kentän on oltava kappaleina ja kuormalavoina. Muussa tapauksessa kyseisen varastopaikan sallittua määrää ei lasketa oikein.  

Ennen kuin asetat lokerossa olevan lokeron sisällön kapasiteettirajoitukset, sinun on ensin varmistettava, että nimikkeen mittayksikkö ja dimensiot on määritetty nimikkeen kortissa.  

> [!NOTE]  
> Toiminta on mahdollista vain useiden mittayksiköiden kanssa WMS-asennuksissa. Kaikissa muissa määrityksissä varastopaikan sisältö voi olla vain perusmittayksikössä. Kaikissa tapahtumissa, joissa mittayksikkö on korkeampi kuin nimikkeen perusmittayksikkö, määrä muutetaan perusmittayksikköön.  

## <a name="zone"></a>Vyöhyke

Laajennetussa varastoinnissa varastopaikat voidaan ryhmitellä vyöhykkeisiin varastotoimintojen työnkulun hallitsemiseksi.  

Vyöhyke voi olla vastaanottava alue tai varastointivyöhyke ja jokainen vyöhyke voi koostua yhdestä tai useasta lokerosta.  

Useimmat vyöhykkeeseen kohdistetut ominaisuudet kohdistetaan oletusarvoisesti tästä vyöhykkeestä luotuun varastopaikkaan.  

## <a name="class"></a>Luokka  
Laajennetussa varastoinnissa voit määrittää nimikkeille, varastopaikoille ja vyöhykkeille fyysisen varastoinnin luokkakoodit joiden avulla voidaan hallita eri nimikeluokkien varastointia, kuten jäädytetyt tuotteet. Voit jakaa alueen useisiin fyysisen varastoinnin luokkiin. Esimerkiksi vastaanottavan vyöhykkeen nimikkeet voidaan tallentaa jäädytetyiksi, vaarallisiksi tai muuhun luokkaan.  

Kun käsittelet fyysisen varastoinnin luokkia ja vastaanoton/toimituksen oletusvarastopaikkaa, sopivat varastopaikat on täytettävä manuaalisesti fyysisen varastoinnin vastaanotto- ja toimitusriveille.  

Saapuvissa virroissa luokkakoodi korostetaan vain saapuvilla riveillä, kun luokkakoodi ei vastaa vastaanoton oletusvarastopaikkaa. Jos oikeita oletusvarastopaikkoja ei määritetä, määrää ei voida vastaanottaa.  

## <a name="location"></a>Sijainti

Sijainti on mahdollisesti lokeroihin järjestetty fyysinen rakenne tai paikka, jossa varasto vastaanotetaan, tallennetaan ja lähetetään. Sijainti voi olla varasto, huoltoauto, esittelytila, laitos tai laitoksen alue.  

## <a name="first-expired-first-out"></a>FEFO (ensin vanhentunut ensimmäisenä ulos)

Jos valitset **FEFO-poiminta**-valintaruudun sijaintikortin **Varastopaikkojen periaatteet** -pikavälilehdessä, nimikeseuratut nimikkeet poimitaan niiden vanhenemispäivämäärän mukaan. Nimikkeet, joissa on aikaisimmat erääntymispäivät, poimitaan ensin.  

Kaikkien poiminta- ja siirtoasiakirjojen fyysisen varaston toiminnot on lajiteltu FEFO-menetelmän mukaan, ellei kyseisille nimikkeille ole jo määritetty sarja- tai eränumeroa. Jos vain osalle rivin määrästä on jo määritetty erä- tai sarjanumerot, jäljellä oleva määrä järjestetään poimittavaksi FEFO:n mukaan.  

Kun FEFO-poiminta on käytössä, valitaan ensin vanhenevat käytettävissä olevat nimikkeet. Tällöin ohjelma luo väliaikaisen nimikkeiden seurantaluettelon vanhenemispäivämäärien perusteella. Jos kahdella nimikkeellä on sama vanhentumispäivämäärä, pienemmällä erä- tai sarjanumerolla varustettu poimitaan ensin. Jos erä- tai sarjanumerot ovat samoja, ensimmäisenä rekisteröity nimike valitaan ensin. Peruskriteereitä, kuten säiliön sijoitus ja kappaletavara, joita käytetään valitsemaan nimikkeitä poimintasäiliöissä, käytetään tähän väliaikaiseen FEFO-nimikkeenseurantaluetteloon.  

## <a name="put-away-template"></a>Hyllytysmalli

Poistettu malli voidaan kirjata nimikkeelle ja sijainnille. Poistettu malli määrittää sarjan priorisoituja sääntöjä, jotka täytyy ottaa huomioon, kun luodaan poistoja. Esimerkiksi hyllytysmalli voi vaatia, että nimike sijoitetaan varastopaikkaan sellaisella varastopaikan sisällöllä, joka vastaa mittayksikköä, ja jos vastaavaa varastopaikkaa riittävällä kapasiteetilla ei löydy, nimike tulee asettaa tyhjään varastopaikkaan.  

## <a name="see-also"></a>Katso myös

[Rakennetiedot: f. varaston hallinta](design-details-warehouse-management.md)   
[Rakennetiedot: saatavuus varastossa](design-details-availability-in-the-warehouse.md)
