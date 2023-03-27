---
title: Nimikkeiden laiturointi
description: 'Laiturointitoiminto on käytettävissä, jos olet määrittänyt fyysisen varastoinnin vastaanoton ja hyllytyksen käsittelyn pakolliseksi sijainnissa.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '15, 5703, 7302, 7332, 5768'
ms.date: 04/01/2021
ms.author: edupont
---
# Nimikkeiden laiturointi

Laituroidut nimikkeet ovat nimikkeitä, jotka vastaanotetaan ja toimitetaan ilman hyllytystä. Hyllytys- ja poimintaprosessit edellyttävät nimikkeiden rajoitettua käsittelyä. Toimitus- että tuotantotilausten nimikkeet voidaan laituroida.

## Laituroinnin varastopaikat ja vyöhykkeet

Varastopaikkoja käytettäessä määritetään ainakin yksi laituroinnin varastopaikka ja sen jälkeen varastopaikka sijaintien **Laiturointivar.paikan koodi** -kentässä. Laiturointialue määritetään, jos käytössä on ohjattu hyllytys ja poiminta.

Kun toimitusta valmistellaan tai nimikkeitä poimintaan tuotantoon ja varastopaikat ovat käytössä, nimike poimitaan automaattisesti laiturointivarastopaikasta ennen muita varastopaikkoja. Laiturointialueella on tarkistettava, ovatko tarvittavat nimikkeet käytettävissä siellä, ennen kuin nimikkeet haetaan normaalille varastointialueelle.  

Jos laiturointimäärät on laskettu, laiturointilaskelmien hyllytysrivit luodaan laiturointivarastopaikkaan vastaanoton kirjauksen yhteydessä. Muita hyllytysrivejä luodaan tavalliseen tapaan.  

## Vastaanoton laituroinnin valintarivit

<!--If a receipt contains items that you want to store, that is, items that you are not cross-docking, you must register a put-away for those items.-->

Jos haluat kirjata laiturointinimikkeet heti saadaksesi ne poimittaviksi, hyllytys on rekisteröitävä myös muiden vastaanottoriviltä peräisin olevien varastoitavien nimikkeiden osalta. Jos vastaanottoriviltä laituroidaan vain muutama nimike, jäljelle jäävät nimikkeet tulisi hyllyttää niin pian kuin mahdollista. Toisaalta fyysisen varastoinnin toimintaohjeissa tulisi kannustaa kokonaisten vastaanottorivien laiturointiin aina, kun se on mahdollista.

Kunkin hyllytettävän nimikkeen vastaanottorivin otto- ja asetusohjerivit poistetaan hyllytysohjeissa. Ohjerivit voidaan luoda myöhemmin uudelleen hyllytysriveinä hyllytystyökirjasta tai kirjatusta vastaanotosta. Kun ohjerivit on poistettu, laiturointinimikkeiden rivit voidaan hyllyttää ja rekisteröidä.  

## Tietoja hyllytystyökirjasta

Jos **Käytä hyllytystyökirjaa** otetaan käyttöön vaihtopainikkeella Sijaintikortti-sivulla ja laskettuja laiturointeja sisältävä vastaanotto on kirjattu, kaikki vastaanottorivit tulevat saataville työkirjaan. Laiturointitiedot häviävät, eikä niitä voida luoda uudelleen. Niinpä laiturointitoimintoja käytettäessä rivit on siirrettävä hyllytystyökirjaan mieluummin poistamalla hyllytysohjeet kuin käyttämällä automaattista siirtotoimintoa, joka sisältyy **Käytä hyllytystyökirjaa** -kenttään.  

Kun fyysisen varaston vastaanotto kirjataan eikä **Käytä hyllytystyökirjaa** ole otettu käyttöön vaihtopainikkeella, laituroitavat nimikkeet muuttuvat erillisiksi riveiksi hyllytysohjeeseen. Kun hyllytysrivin **Laiturointitiedot**-kentässä näkyy, onko rivillä seuraavat tiedot:

* Laituroidut nimikkeet.
* Kaikki vastaanoton nimikkeet on varastoitava.
* Jotkin vastaanoton nimikkeet on varastoitava ja jotkin laituroidaan.

Työntekijöiden on helppo hahmottaa, miksi koko määrää ei aseteta varastoon.  

[!INCLUDE [prod_short](includes/prod_short.md)] ei säilytä erillisiä laituroitujen nimikkeiden tietueita vaan rekisteröi ne tavallisina hyllytysohjeina.  

## Fyysisen varastoinnin määrittäminen laiturointia varten  

1. Varastopaikkoja käytettäessä on määritettävä ainakin yksi laiturointivarastopaikka. Laiturointialue määritetään, jos käytössä on ohjattu hyllytys ja poiminta.  

    Laiturointivar.paikassa on **Laiturointivar.paikka**-kenttä valittuna ja sekä **Vastaanotto** että **Poiminta** -paikkatyypit on valittu. Lisätietoja on kohdissa [Varastopaikkojen luominen](warehouse-how-to-create-individual-bins.md) ja [Varastopaikkatyyppien määrittäminen](warehouse-how-to-set-up-bin-types.md).  

    Jos käytät alueita, luo alue laiturointivarastopaikoille ja valitse **Laiturointivar.paikan alue** -kenttä. Lisätietoja on kohdassa [Sijaintien määrittäminen varastopaikkojen käyttämistä varten](warehouse-how-to-set-up-locations-to-use-bins.md).  

2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainti** ja valitse sitten vastaava linkki.  
3. Valitse **Sijainti**-sivulla ensin sijainti, jolle haluat määrittää fyysisen varaston laiturointia varten ja sitten **Muokkaa**-toiminto.  
4. Ota **Käytä laiturointia** vaihtopainikkeella käyttöön **Fyysinen varasto** -pikavälilehdessä ja täytä **Laituroinnin eräpvm lask.** -kenttään jakso, jonka ajalta laiturointimahdollisuuksia etsitään.

    **Käytä laiturointia** -vaihtoehto on käytettävissä vain, jos **Vaadi vastaanotto**-, **Vaadi toimitus**-, **Vaadi poiminta**- ja **Vaadi hyllytys** -kenttiin on asetettu valintamerkki.  

5.  Jos käytät varastopaikkoja, täytä sijaintikortin **Varastopaikat**-pikavälilehden **Laiturointivar.paikan koodi** -kenttään sen varastopaikan koodi, jota haluaisit käyttää oletusarvoisena laiturointivarastopaikkana.  
6.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastointiyksikkö** ja valitse sitten vastaava linkki.  
7.  Valitse kunkin laituroitavan nimikkeen tai varastointiyksikön kohdalla ensin nimike ja sitten **Muokkaa**-toiminto.
8. Valitse **Varastointiyksikön kortti** -sivulla **Käytä laiturointia** -valintaruutu.  

> [!NOTE]  
>  Laiturointi on mahdollista sijainnissa vain, jos sijainnissa on määritetty fyysisen varastoinnin vastaanoton ja hyllytyksen käsittely pakolliseksi.  

## Nimikkeiden laituroiminen ilman mahdollisuuksien tarkastelua  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston vastaanotot** ja valitse sitten vastaava linkki.  
2.  Luo varaston vastaanotot nimikkeelle, joka on saapunut ja voidaan ehkä laituroida. Lisätietoja on kohdassa [Nimikkeiden vastaanottaminen](warehouse-how-receive-items.md).  
3.  Täytä **Vastaanotettava määrä** -kenttä ja valitse sitten **Laske laiturointi** -toiminto.  

    Näin tunnistetaan lähtevät lähdeasiakirjat, joissa pyydetään päivämääräkaavan ajanjakson aikana varastolta lähteviksi aikataulutettuja nimikkeitä.  [!INCLUDE[prod_short](includes/prod_short.md)] laskee määrät siten, että laituroitava määrä on mahdollisimman suuri ja ettei nimikkeitä tarvitse hyllyttää. Laskelma tehdään kuitenkin niin, ettei laiturointialueelle keräänny liian paljon nimikkeitä. **Laituroitava määrä** -kentässä oleva arvo on siis yhteenlaskettu summa kaikista lähtevistä riveistä, joilla pyydetään nimikettä määritetyn ajanjakson aikana, vähennettynä laiturointialueelle sijoitetulla nimikkeen määrällä – tai se on vastaanottorivin **Vastaanotettava määrä** -kentän arvo – sen mukaan, kumpi näistä arvoista on pienempi. Laituroinnin määrä ei voi olla suurempi kuin vastaanotettu määrä.  

4.  Jos haluat laituroida määrän ehdotuksen mukaan, kirjaa vastaanotto. Voit myös päättää muuttaa laituroitavaa määrää suuremmaksi tai pienemmäksi arvoksi ja sitten kirjata vastaanoton.  

    Laituroitavat summat näkyvät nyt riveinä hyllytysohjeessa (jos **Käytä hyllytystyökirjaa**-kenttä on tyhjennetty). Myös ei-laituroitavat määrät tulevat näkyviin riveinä hyllytysohjeeseen.  

    Jos käytät varastopaikkoja, ohjelma on määrittänyt laiturointinimikkeet sijaintikortissa määritettyyn oletusarvoiseen laiturointivarastopaikkaan.  

5.  Poista **Ota**- ja **Aseta**-rivit niiden nimikkeiden osalta, joita ei laituroida ollenkaan.  
6.  Tulosta jäljellä oleville riveille hyllytysohje ja sijoita vastaanoton varastoitavat määrät sopiviin varastopaikkoihin tai sopivalle fyysisen varaston alueelle. Sijoita laiturointinimikkeet alueelle tai varastopaikkaan, joka osoitetaan niille fyysisen varastoinnin menettelytavoissa. Joskus fyysisen varastoinnin menettelytavoissa voidaan haluta nimikkeiden jättäminen vastaanottoalueelle.  
7.  Rekisteröi laituroidut nimikkeet hyllytetyiksi ja poimintaan käytettäviksi valitsemalla **Rekisteröi**-toiminto.  

## Nimikkeiden laiturointi mahdollisuuksien tarkastelemisen jälkeen  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston vastaanotot** ja valitse sitten vastaava linkki.  
2.  Luo varaston vastaanotot nimikkeelle, joka on saapunut ja joka voidaan ehkä laituroida. Lisätietoja on kohdassa [Nimikkeiden vastaanottaminen](warehouse-how-receive-items.md).  

    Haluat tarkastella lähdeasiakirjan rivejä, joilla pyydetään nimikettä, ennen vastaanoton kirjaamista.  
3.  Valitse **Laske laiturointi** -toiminto.  

    **Laiturointimahdollisuudet**-sivu sisältää tärkeimmät tiedot riveistä, joilla pyydetään nimikettä. Näitä tietoja ovat esimerkiksi asiakirjan tyyppi, pyydetty määrä ja eräpäivä. Näiden tietojen avulla voit päättää, kuinka paljon laituroidaan, mihin nimikkeet sijoitetaan laiturointialueella tai miten niitä ryhmitellään.  

4.  Valitsemalla **Täytä laiturointimäärä automaattisesti** toiminnot, näet, vastaanottorivien määrät lasketaan. Kun muutat nimikkeiden määrää **Laituroitava määrä** -kentässä jokaisella rivillä, laskelma päivitetään, kun teet muutoksia. Tämä ei tarkoita sitä, että tietty toimitus tai tuotantotilaus tosiasiassa vastaanottaa laituroitaviksi ehdotetut nimikkeet, koska tämä menettely on tarkoitettu vain testaamista varten. Prosessista voi kuitenkin olla hyötyä useita mittayksikköjä käytettäessä.  
5.  Jos haluat varata nimikemäärän tietylle tilausriville, siirrä osoitin kyseiselle riville ja valitse **Varaa**-toiminto. Voit nyt varata **Varaus**-sivulla nimikettä tilaukseen saatavilla olevan määrän. Tämä varaus on kuin mikä tahansa muu varaus, eikä sillä ole suurempaa prioriteettia, koska se luotiin laituroinnin yhteydessä. Lisätietoja on kohdassa [Nimikkeiden varaaminen](inventory-how-to-reserve-items.md).   
6.  Kun olet saanut uudelleenlaskennan tai varaamisen valmiiksi, tuo korjattu laskennan vastaanottorivi **Laituroitava määrä** -kenttään valitsemalla **OK** tai valitse **Peruuta**, jos haluat palata fyysisen varastoinnin vastaanottoon, jossa voit laskea laituroinnin uudelleen.  
7.  Kirjaa nyt vastaanotto, niin voit jatkaa hyllytysohjeeseen osan ”Nimikkeiden laituroiminen ilman mahdollisuuksien tarkastelua” vaiheissa 3 - 7.  

> [!NOTE]  
>  Fyysisen varastoinnin hyllytyksessä voit jatkaa tarpeen mukaan niiden määrien muuttamista, jotka hyllytetään varastoon tai laituroidaan. Voit esimerkiksi päättää laituroida ylimääräisen määrän nopeuttaaksesi laituroinnin rekisteröimistä.  

## Laituroitujen nimikkeiden tarkasteleminen toimituksissa tai poimintatyökirjassa  
Jos käytät varastopaikkoja, näet aina toimituksen tai poimintatyökirjan avauksen yhteydessä kaikkien laiturointivarastopaikoissa olevien nimikkeiden määrän päivitetyn laskelman. Tämä on tärkeä tieto silloin, jos odotat nimikkeen saapumista. Kun näet, että nimike on saatavilla laiturointivarastopaikassa, voit nopeasti luoda poiminnan kaikille toimituksen nimikkeille. Poimintatyökirjassa voit muokata rivejä tarpeen mukaan ja sitten luoda poiminnan.  

Etsi nimikkeitä laiturointialueelta, ennen kuin poimit niitä toimitusta varten. Jos olet huomioinut vastaanottoprosessin aikana lähdeasiakirjat, jotka toimivat laituroinnin pohjana, tiedät paremmin, löytyykö nimike laiturointialueelta.  

Kun tuotantotilaus on vapautettu, rivit ovat saatavilla poimintatyökirjassa. **Määrä laitur.var.paikassa** -kentässä näet, ovatko odottamasi nimikkeet saapuneet ja onko ne sijoitettu laiturointivarastopaikkoihin. Kun luot poimintaohjeen, sovellus ehdottaa, että ensin poimitaan laituroidut nimikkeet ja nimikettä haetaan vasta myöhemmin varaston varastopaikoista.  

Jos et käytä varastopaikkoja, muista tarkastaa laiturointialue ajoittain tai turvaudu vastaanottoilmoituksiin siitä, että tuotannon nimikkeet ovat saapuneet.  

## Katso myös  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Varastonhallinnan yleiskatsaus](design-details-warehouse-management.md)
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]