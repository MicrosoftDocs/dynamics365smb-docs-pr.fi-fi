---
title: Nimikkeiden vastaanottaminen
description: Tässä aiheessa on yleiskatsaus eri tavoista vastaanottaa nimikkeitä fyysisessä varastossa, esimerkiksi nimikkeistä, joilla on ostotilaus, tai nimikkeistä, joilla on fyysisen varaston vastaanotto.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5768, 7330, 7332, 7333, 7342, 7363, 8510
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: ebb230a7bd0e2008d16b33c0fb00bdbeac3177d6
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8519490"
---
# <a name="receive-items"></a>Nimikkeiden vastaanottaminen

Kun nimikkeet saapuvat fyysiseen varastoon, johon ei ole määritetty fyysisen varaston vastaanottokäsittelyä, vastaanotto vain kirjataan liittyvään asiakirjaan, kuten ostotilaukseen, myyntipalautustilaukseen tai saapuvaan siirtotilaukseen.

Kun nimikkeet saapuvat varastoon, jossa on käytössä fyysisen varastoinnin vastaanoton käsittely, rivit on noudettava niiden vastaanoton käynnistäneestä vapautetusta lähdeasiakirjasta. Jos käytössä on varastopaikkoja, voit hyväksyä kentässä olevan oletusvarastopaikan. Jos nimikettä ei ole käytetty aiemmin varastossa, kirjoita varastopaikka, johon nimike tulisi hyllyttää.  

## <a name="to-receive-items-with-a-purchase-order"></a>Nimikkeiden vastaanottaminen ostotilauksella

Seuraavaksi käsitellään, miten nimikkeitä vastaanotetaan ostotilauksella. Vaiheet ovat samankaltaiset myyntipalautustilauksille ja siirtotilauksille.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.
2. Avaa aiemmin luotu ostotilaus tai luo uusi myyntitilaus. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).
3. Anna **Vastaanotettava määrä** -kenttään vastaanotettu määrä.

  > [!NOTE]
  > Jos vastaanotettu määrä on suurempi kuin ostotilauksen tilattu **Määrä**-kentän mukainen määrä ja toimittajalle on määritetty vastaanoton ylittävän määrän salliminen, voit käsitellä ylimääräistä määrää **Vastaanoton ylitys** -kentän avulla. Lisätietoja on kohdassa [Tilattua määrää useampien nimikkeiden vastaanottaminen](warehouse-how-receive-items.md#to-receive-more-items-than-ordered).

4. Valitse **Kirjaa**-toiminto.

  **Määrä vast.otettu** -kentän arvo päivitetään. Jos kyse on osavastaanotosta, arvo on pienempi kuin **Määrä**-kentän arvo.

> [!NOTE]
> Jos käytät varastoasiakirjaa vastaanoton kirjaamisessa, et voi käyttää ostotilauksen **Kirjaa**-toimintoa. Sen sijaan varaston työntekijä on jo kirjannut ostotilauksen määrän vastaanotetuksi. Lisätietoja on kohdassa [Nimikkeiden vastaanottaminen varaston vastaanoton avulla](warehouse-how-receive-items.md#to-receive-items-with-a-warehouse-receipt).

## <a name="to-receive-items-with-a-warehouse-receipt"></a>Nimikkeiden vastaanottaminen fyysisen varasto vastaanottona

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston vastaanotot** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  

    Täytä **Yleinen**-pikavälilehden kentät. Kun haet lähdeasiakirjan rivit, ohjelma kopioi otsikon tiedot kullekin riville.  

    Jos fyysisen varaston määrityksissä on käytössä ohjattu hyllytys ja poiminta ja jos sijainnilla on oletusalue ja oletusvarastopaikka vastaanotoille, **Alueen koodi**- ja **Varastopaikkakoodi**-kentät täytetään automaattisesti, mutta voit muuttaa niiden arvoja tarpeen mukaan.  

    > [!NOTE]  
    > Jos haluat vastaanottaa nimikkeitä, joiden fyysisen varastoinnin luokkakoodi ei ole sama kuin asiakirjan otsikon **Varastopaikkakoodi**-kentässä olevan varastopaikan luokkakoodi, poista otsikon **Varastopaikkakoodi**-kentän sisältö ennen lähdeasiakirjan rivien hakemista nimikkeitä varten.  
3. Valitse **Hae lähdeasiakirjat** -toiminto. Näyttöön tulee **Lähdeasiakirjat**-sivu.

    Voit käyttää uuden tai avoimen fyysisen varastoinnin vastaanoton **Suod. lähdeasiakirj. saamisek.** -sivuai hakiessasi vastaanotettava tai toimitettavat nimikkeet määrittävän vapautetun lähdeasiakirjan rivit.

    1. Valitse **Käytä suodat. kun haet lähd.d** -toiminto.  
    2. Määritä uusi suodatin antamalla kuvaileva koodi **Koodi**-kenttään ja valitse **Muokkaa**-toiminto.  
    3. Määritä ne lähdeasiakirjan rivien tyypit, jotka haluat hakea, täyttämällä soveltuvat suodatinkentät.  
    4. Valitse **Aja**-toiminto.  

    Kaikki julkaistut lähdeasiakirjan rivit, jotka täyttävät suodatusehdot, on nyt lisätty **F. varastoinnin vastaanotto** -sivulla, josta aktivoit suodatustoiminnon.  

    Määrittämäsi suodatinyhdistelmät tallennetaan **Suod. lähdeasiakirj. saamisek.** -sivulle tulevaa käyttöä varten. Voit tehdä niin monta suodatinyhdistelmää kuin haluat. Voit muuttaa ehtoja milloin tahansa valitsemalla **Muokkaa**-toiminnon.

4. Valitse lähdeasiakirjat, joille haluat vastaanottaa nimikkeitä, ja valitse sitten **OK**.  

    Lähdeasiakirjojen rivit näkyvät **F. varastoinnin vastaanotto** -sivulla. Ohjelma on jo täyttänyt **Vastaanotettava määrä** -kenttään jokaisen rivin avoimen määrän, mutta määrää voi muuttaa tarpeen mukaan. Jos olet poistanut **Yleinen**-pikavälilehden **Varastopaikkakoodi**-kentän sisällön ennen rivien hakemista, kirjoita kullekin vastaanottoriville asianmukainen varastopaikkakoodi.  

    > [!NOTE]  
    >  Jos haluat, että **Vastaanotettava määrä** -kentän kaikki rivit täytetään arvolla nolla, valitse **Poista vastaanotettava määrä** -toiminto. Voit täyttää sen uudelleen avoimella määrällä valitsemalla **Täytä autom. vast.ot. määrä** -toiminto.  

    > [!NOTE]  
    >  Et voi vastaanottaa enempää nimikkeitä kuin määrä **Avoin määrä** -kentässä lähdeasiakirjan rivillä ilmaisee. Vastaanota enemmän nimikkeitä hakemalla toinen lähdeasiakirja, jossa on rivi nimikkeelle, käyttämällä suodatintoimintoa hakeaksesi lähdeasiakirjat ja nimike.  

5. Kirjaa fyysisen varastoinnin vastaanotto. Ohjelma päivittää lähdeasiakirjojen määräkentät ja kirjaa nimikkeet osaksi yrityksen varastoa.  

Jos käytössä on fyysisen varastoinnin hyllytys, ohjelma lähettää vastaanottorivit fyysisen varastoinnin hyllytystoimintoon. Vastaanotettuja nimikkeitä ei voi poimia ennen kuin ne on hyllytetty. Ohjelma tunnistaa vastaanotetut nimikkeet saatavilla olevaksi varastoksi vasta sitten, kun hyllytys on rekisteröity.  

Jos fyysisen varastoinnin hyllytys ei ole käytössä mutta käytät varastopaikkoja, ohjelma kirjaa nimikkeiden hyllytyksen lähdeasiakirjan rivillä määritettyyn varastopaikkaan.  

> [!NOTE]  
> Jos käytät **Kirjaa ja tulosta** -toimintoa, vastaanoton kirjauksen yhteydessä tulostetaan hyllytysohje, joka kertoo, mihin nimikkeet sijoitetaan varastossa.  
>
> Jos sijainnissa on käytössä ohjattu hyllytys ja poiminta, hyllytysmalleja käytetään parhaan nimikkeiden hyllytyspaikan laskemisessa. Tämä tulostetaan sitten hyllytysohjeeseen.

## <a name="to-receive-more-items-than-ordered"></a>Tilattua määrää useamman nimikkeen vastaanottaminen

Kun nimikkeitä vastaanotetaan tilattua suurempi määrä, haluat ehkä kuitenkin vastaanottaa ne vastaanoton peruuttamisen sijaan. Ylimenevä osa voi olla esimerkiksi halvempi varastoida kuin palauttaa tai toimittaa voi antaa alennuksen, jos pidät nimikkeet.

### <a name="to-set-up-over-receipts"></a>Vastaanoton ylittävän määrän määrittäminen

Sinun on määritettävä prosenttiosuus, jonka verran vastaanotto saa ylittää tilatun määrän. Määritä tämä vastaanoton ylittävän määrän koodin kohdassa. Se sisältää **Vastaanoton ylittävän määrän toleranssi-%** -kentän prosenttiosuuden. Tämän jälkeen koodi määritetään liittyvien nimikkeiden ja/tai toimittajien kortteihin.  

Seuraavassa kuvataan, miten nimikkeen vastaanoton ylittävän määrän koodi määritetään ja liitetään nimikkeelle. Toimittajaa koskevat vaiheet ovat samanlaisia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Avaa sen nimikkeen kortti, jonka vastaanotettava määrä voi joskus ylittää tilatun määrän.
3. Valitse **Vastaanoton ylittävän määrän koodi** -kentän valintapainike.
4. Valitse **Uusi**-toiminto.
5. Luo **Vastaanoton ylittävän määrän koodit** -sivulla vähintään yksi uusi rivi, joka määrittää vastaanoton ylittävän määrän käytännöt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
6. Valitse rivi ja valitse sitten **OK**-painike.

Vastaanoton ylittävän määrän koodi on määritetty nimikkeelle. Mikä tahansa nimikkeen ostotilaus tai varaston vastaanotto sallii nyt tilattua määrää suuremman määrän vastaanoton määritetyn vastaanoton ylittävän määrän toleranssin prosenttiosuuden mukaan.

> [!NOTE]
> Voit määrittää hyväksynnän työnkulun, jos vastaanoton ylittävät määrät on hyväksyttävä ennen käsittelemistä. Tässä tapauksessa on valittava **Hyväksyntä vaaditaan** -valintaruutu **Vastaanoton ylittävän määrän koodit** -sivulla. Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).

### <a name="to-perform-an-over-receipt"></a>Vastaanoton ylittävän määrän suorittaminen

Ostoriveillä ja varaston vastaanoton riveillä käytetään **Vastaanoton ylittävä määrä** -kenttää tallennettaessa vastaanoton ylittävät määrät. Nämä ovat määriä, jotka ylittävät tilatun määrän eli **Määrä**-kentän arvon.

Kun käsittelet vastaanoton ylittävää määrää, voit suurentaa arvoa **Vastaanotettava määrä** -kentässä vastaamaan todellisuudessa vastaanotettua määrää. **Vastaanoton ylittävä määrä** -kenttään päivitetään tämän jälkeen ylimääräinen määrä. Vaihtoehtoisesti voit syöttää ylimääräinen määrä **Vastaanoton ylittävä määrä** -kenttään. **Vastaanotettava määrä** -kenttään päivitetään tilatun määrän ja ylimääräisen määrän summa. Seuraavassa kerrotaan, miten **Vastaanotettu määrä** -kenttä täytetään.  

1. Jos ostotilauksen tai varaston vastaanoton asiakirjan vastaanotettu määrä on suurempi kuin tilattu, anna **Vastaanotettu määrä** -kenttään todellisuudessa vastaanotettu määrä.

    Jos lisäys on määritetyn vastaanoton ylittävän määrän koodin toleranssin rajoissa, **Vastaanoton ylittävä määrä** -kenttään päivitetään arvo, jonka mukaan **Määrä**-kenttä on ylitetty.

    Jos lisäys on määritetyn toleranssin yläpuolella, vastaanoton ylittävää määrää ei sallita. Tässä tapauksessa voidaan tutkia, voiko toinen vastaanoton ylittävän määrän koodi sallia tämän. Muussa tapauksessa voidaan vastaanottaa vain tilattu määrä ja ylimääinen määrä on käsiteltävä muulla tavalla. Se voi tarkoittaa esimerkiksi palauttamista toimittajalle.

2. Kirjaa vastaanotto samalla tavalla kuin muut vastaanotot.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] ei sisällä toimintoja, jotka käynnistävät automaattisesti ylimääräisten määrien vastaanoton hallinnan. Tämä on käsiteltävä manuaalisesti yhdessä toimittajan kanssa esimerkiksi niin, että toimittaja lähettää uuden tai päivitetyn laskun.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Katso myös

[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]