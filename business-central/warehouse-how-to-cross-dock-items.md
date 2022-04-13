---
title: Nimikkeiden laiturointi
description: Laiturointitoiminto on käytettävissä, jos olet määrittänyt fyysisen varastoinnin vastaanoton ja hyllytyksen käsittelyn pakolliseksi sijainnissa.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 15, 5703, 7302, 7332, 5768
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a9621393c09de1a4d6cf21789fa1141763d94efe
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8513313"
---
# <a name="cross-dock-items"></a>Nimikkeiden laiturointi
Laiturointitoiminto on käytettävissä, jos olet määrittänyt fyysisen varastoinnin vastaanoton ja hyllytyksen käsittelyn pakolliseksi sijainnissa.  

Kun laituroit nimikkeitä, käsittele nimikkeitä vastaanotossa ja toimituksessa ilman varastointia, nopeuatat nimikkeen hyllytys- ja poimintaprosesseja ja rajoitat nimikkeiden fyysistä käsittelyä. Voit laituroida nimikkeet sekä toimitus- että tuotantotilauksille. Kun valmisteleta toimitusta tai poimit nimikkeittä tuotantoon ja käytät varastopaikkoja, nimike keräillään automaattisesti laiturointivarastopaikasta ennen muita varastopaikkoja. Sinun tulee tarkistaa laiturointialue nähdäksesi, onko starvitsemasi nimikkeet käytettävissä siellä, ennen kuin haet nimikkeet normaalille varastointialueelle.  

Jos olet laskenut laiturointimääriä, ohjelma luo laiturointilaskelmien hyllytysrivejä laiturointivarastopaikkaan silloin, kun kirjaat vastaanoton. Muita hyllytysrivejä luodaan tavalliseen tapaan.  

Jos haluat kirjata laiturointinimikkeet heti saadaksesi ne poimittaviksi, hyllytys on rekisteröitävä myös muiden vastaanottoriviltä peräisin olevien varastoitavien nimikkeiden osalta. Jos vastaanottoriviltä laituroidaan vain muutama nimike, jäljelle jäävät nimikkeet tulisi hyllyttää niin pian kuin mahdollista. Toisaalta fyysisen varastoinnin toimintaohjeissa tulisi kannustaa kokonaisten vastaanottorivien laiturointiin aina, kun se on mahdollista.  

Voit poistaa hyllytysohjeesta omaksi eduksesi ohjerivejä (sekä Ota- että Aseta-rivejä kunkin vastaanottorivin osalta), jotka koskevat vastaanottoja, jotka hyllytetään kokonaan varastoon. Näistä riveistä voidaan myöhemmin luoda hyllytysrivejä hyllytystyökirjasta tai kirjatusta vastaanotosta. Kun rivejä poistetaan, tämän jälkeen voidaan hyllyttää ja rekisteröidä rivit, jotka koskevat laiturointinimikkeitä.  

Jos olet lisännyt rastin sijaintikortin  **Käytä hyllytystyökirjaa** -kenttään ja olet kirjannut vastaanoton, jossa on laskettuja laiturointeja, kaikki vastaanottorivit tulevat saataville työkirjaan. Laiturointitiedot häviävät, eikä niitä voi luoda uudelleen. Joten jos haluat käyttää laiturointiominaisuutta, rivit tulisi siirtää hyllytystyökirjaan mieluummin poistamalla hyllytysohjeet kuin käyttämällä automaattista siirtotoimintoa, joka löytyy **Käytä hyllytystyökirjaa** -kentästä.  

Kun kirjaat fyysisen varaston vastaanoton (**Käytä hyllytystyökirjaa** -kentässä ei ole rastia), laituroitavat nimikkeet tulevat näkyviin hyllytysohjeeseen erillisinä riveinä. Jokaisen hyllytysrivin **Laiturointitiedot**-kentässä näkyy, onko rivillä laiturointinimikkeitä, nimikkeitä samasta vastaanotosta, jotka kaikki tulee varastoida, vai varastoitavia nimikkeitä, jotka ovat peräisin vastaanottoriviltä, josta joitain nimikkeitä laituroidaan. Tämän kentän avulla työntekijät näkevät helposti, miksi koko vastaanottomäärää ei sijoiteta varastoon.  

Sovellus ei ylläpidä erillisiä tietueita nimikkeistä, jotka on laituroitu, vaan se rekisteröi ne tavallisiksi hyllytysohjeiksi.  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a>Fyysisen varastoinnin määrittäminen laiturointia varten  
1.  Määritä ainakin yksi laiturointivarastopaikka, jos käytät varastopaikkoja. Määritä laiturointialue, jos käytät ohjattua hyllytystä ja poimintaa.  

    Laiturointivar.paikassa on **Laiturointivar.paikka**-kenttä valittuna ja sekä **Vastaanotto** että **Poiminta** -paikkatyypit on valittu. Lisätietoja on kohdissa [Varastopaikkojen luominen](warehouse-how-to-create-individual-bins.md) ja [Varastopaikkatyyppien määrittäminen](warehouse-how-to-set-up-bin-types.md).  

    Jos käytät alueita, luo alue laiturointivarastopaikoille ja valitse **Laiturointivar.paikan alue** -kenttä. Lisätietoja on kohdassa [Sijaintien määrittäminen varastopaikkojen käyttämistä varten](warehouse-how-to-set-up-locations-to-use-bins.md).  

2.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainti** ja valitse sitten vastaava linkki.  
3.  Valitse **Sijainti**-sivulla ensin sijainti, jolle haluat määrittää fyysisen varaston laiturointia varten ja sitten **Muokkaa**-toiminto.  
4.  Valitse **Fyysinen varasto** -pikavälilehdessä **Käytä laiturointia** -valintaruutu ja täytä **Laituroinnin eräpvm lask.** -kenttään jakso, jonka ajalta laiturointimahdollisuuksia etsitään.

    **Käytä laiturointia** -vaihtoehto on käytettävissä vain, jos **Vaadi vastaanotto**-, **Vaadi toimitus**-, **Vaadi poiminta**- ja **Vaadi hyllytys** -kenttiin on asetettu valintamerkki.  

5.  Jos käytät varastopaikkoja, täytä sijaintikortin **Varastopaikat**-pikavälilehden **Laiturointivar.paikan koodi** -kenttään sen varastopaikan koodi, jota haluaisit käyttää oletusarvoisena laiturointivarastopaikkana.  
6.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastointiyksikkö** ja valitse sitten vastaava linkki.  
7.  Valitse kunkin laituroitavan nimikkeen tai varastointiyksikön kohdalla ensin nimike ja sitten **Muokkaa**-toiminto.
8. Valitse **Varastointiyksikön kortti** -sivulla **Käytä laiturointia** -valintaruutu.  

> [!NOTE]  
>  Laiturointi on mahdollista sijainnissa vain, jos sijainnissa on määritetty fyysisen varastoinnin vastaanoton ja hyllytyksen käsittely pakolliseksi.  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a>Nimikkeiden laituroiminen ilman mahdollisuuksien tarkastelua  
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

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a>Nimikkeiden laiturointi mahdollisuuksien tarkastelemisen jälkeen  
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

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a>Laituroitujen nimikkeiden tarkasteleminen toimituksissa tai poimintatyökirjassa  
Jos käytät varastopaikkoja, näet aina toimituksen tai poimintatyökirjan avauksen yhteydessä kaikkien laiturointivarastopaikoissa olevien nimikkeiden määrän päivitetyn laskelman. Tämä on tärkeä tieto silloin, jos odotat nimikkeen saapumista. Kun näet, että nimike on saatavilla laiturointivarastopaikassa, voit nopeasti luoda poiminnan kaikille toimituksen nimikkeille. Poimintatyökirjassa voit muokata rivejä tarpeen mukaan ja sitten luoda poiminnan.  

Etsi nimikkeitä laiturointialueelta, ennen kuin poimit niitä toimitusta varten. Jos olet huomioinut vastaanottoprosessin aikana lähdeasiakirjat, jotka toimivat laituroinnin pohjana, tiedät paremmin, löytyykö nimike laiturointialueelta.  

Kun tuotantotilaus on vapautettu, rivit ovat saatavilla poimintatyökirjassa. **Määrä laitur.var.paikassa** -kentässä näet, ovatko odottamasi nimikkeet saapuneet ja onko ne sijoitettu laiturointivarastopaikkoihin. Kun luot poimintaohjeen, sovellus ehdottaa, että ensin poimitaan laituroidut nimikkeet ja nimikettä haetaan vasta myöhemmin varaston varastopaikoista.  

Jos et käytä varastopaikkoja, muista tarkastaa laiturointialue ajoittain tai turvaudu vastaanottoilmoituksiin siitä, että tuotannon nimikkeet ovat saapuneet.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]