---
title: Varaston laskeminen, muuttaminen ja uudelleenluokitus| Microsoft Docs
description: "Ohjeaiheessa kerrotaan, miten nimiketapahtumien tai varastotapahtumien inventointi suoritetaan, tehdään negatiivisia tai positiivisia oikaisuja ja muutetaan tietoja, kuten sijaintia tai erän numeroa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: db79c257585fe89237ef4e8d61fa49ce46ec682f
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-count-adjust-and-reclassify-inventory"></a>Varaston laskeminen, muuttaminen ja uudelleenluokitus
Vähintään kerran tilikauden aikana tulee suorittaa inventointi (eli laskea kaikki varastossa olevat nimikkeet), jotta nähtäisiin, onko tietokantaan rekisteröity määrä sama kuin varaston fyysinen määrä. Kun varaston fyysinen määrä on tiedossa, se on kirjattava pääkirjanpitoon osana kauden lopun varaston arvostusta.

Vaikka lasket kaikki varaston nimikkeet vähintään kerran vuodessa, voit päättää laskevasi joitain nimikkeitä useammin, koska ne ovat ehkä arvokkaampia tai ne liikkuvat nopeasti varastosta ja ovat suuri osa liiketoimintaa. Voit määrittää tätä varten erityisiä laskentajaksoja. Lisätietoja on kohdassa Inventoinnin suorittaminen.

Jos kirjattuja varastomääriä pitää muuttaa laskennan yhteydessä tai muita tarkoituksia varten, inventointitapahtumia voi muuttaa suoraan nimikepäiväkirjan avulla liiketoimintatapahtumia kirjaamatta. Vaihtoehtoisesti voit muuttaa yhden nimikkeen nimikekortissa.

Jos sekä nimiketapahtumien määritteitä että määriä pitää muuttaa, voidaan käyttää nimikkeen uudelleenluokituspäiväkirjaa. Tyypillisiä uudelleenluokiteltavia määritteitä ovat sarja- ja eränumerot, vanhentumispäivämäärät ja dimensiot.

## <a name="to-perform-a-physical-inventory"></a>Inventoinnin suorittaminen
Sinun tulee tehdä inventointi (eli laskea saatavilla olevat nimikkeet) nähdäksesi, onko ohjelmaan rekisteröity määrä sama kuin varaston fyysinen määrä, tilikauden lopussa ellei useamminkin. Jos löytyy eroja, ne tulee kirjata nimiketileille ennen varaston arvostusta.

Fyysisen laskentajakson lisäksi täydellinen prosessi käsittää seuraavat kolme tehtävää:

- Laske oletettu varasto.
- Tulosta raportti, jota käytetään laskennassa.
- Syötä ja kirjaa todellinen laskettu varasto.

### <a name="to-calculate-the-expected-inventory"></a>Laske oletettu varasto
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Varastopäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Laske varasto** -toiminto.
3. Määritä **Laske varasto** -ikkunassa ehdot, joita käytetään luotaessa päiväkirjarivejä, kuten sisällytetäänkö nimikkeet, joiden kirjattu varastomäärä on nolla.
4. Aseta suodattimia, jos haluat laskea vain varaston tiettyjä nimikkeitä, varastopaikkoja, sijainteja tai dimensioita.
5. Valitse **OK**-painike.

> [!NOTE]  
>   Ohjelma käsittelee nimiketapahtumat määrittämiesi tietojen mukaan ja luo rivejä inventointipäiväkirjaan. Huomaa, että **Määrä (inventointi)** -kenttään täytetään automaattisesti sama määrä kuin **Määrä (laskettu)** -kenttään. Tämän ominaisuuden ansiosta sinun ei tarvitse syöttää laskettua varastosaldoa niiden nimikkeiden osalta, joiden määrä on sama kuin laskettu määrä. Jos laskettu määrä kuitenkin eroaa **Määrä (laskettu)** -kenttään syötetystä määrästä, korvaa se todellisella lasketulla määrällä.

### <a name="to-print-the-report-used-when-counting"></a>Tulosta raportti, jota käytetään laskennassa
1. Valitse lasketun oletetun varaston sisältävän **Varastopäiväkirja** -ikkunassa **Tulosta**-toiminto.
2. Määritä **Inventointiluettelo**-ikkunassa, näytetäänkö raportissa laskettu määrä ja näkyykö raportissa varastonimikkeiden luettelo sarja ja eränumeroiden mukaan.
3. Määritä suodattimia, jos haluat tulostaa vain tiettyjä varastojen nimikkeiden, varastopaikkojen, sijaintien tai dimensioiden raportteja.
4. Valitse **Tulosta**-painike.

Työntekijät voivat nyt laskea varaston ja merkitä mahdolliset poikkeamat tulostettuun raporttiin.

### <a name="to-enter-and-post-the-actual-counted-inventory"></a>Syötä ja kirjaa todellinen laskettu varasto
1. Jos jollakin **Varastopäiväkirja**-ikkunan rivillä inventoinnissa määritetty todellinen saatavissa oleva varastomäärä poikkeaa lasketusta määrästä, anna **Määrä (varastotilanne)** -kentässä todellinen saatavissa oleva varastomäärä.

    Liittyvät kentät päivitetään tämän mukaisesti.

    > [!NOTE]  
>   Jos inventointi paljastaa eroja, jotka johtuvat siitä, että nimikkeitä on kirjattu virheellisten sijaintikoodien kanssa, älä syötä eroja inventointipäiväkirjaan. Käytä sen sijaan uudelleenluokituspäiväkirjaa tai siirtotilausta nimikkeiden ohjaamiseen oikeisiin sijainteihin. Lisätietoja on kohdassa Nimikkeen uudelleen luokittelun päiväkirja tai Siirtotilausten luominen.

2. Voit muokata lasketut määrät todellisten laskettujen määrien mukaiseksi valitsemalla **Kirjaus**-toiminnon.

    Sekä nimiketapahtumat että fyysiset inventointitapahtumat luodaan. Avaa nimikkeen kortti, jos halkuat tarkastella tuloksena saatavia inventointitapahtumia.

3. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikkeet** ja valitse sitten aiheeseen liittyvä linkki.
4. Voit tarkistaa inventoinnin avaamalla kyseisen nimikekortin ja valitsemalla sitten **Inventointitapahtumat** -toiminnon.

# <a name="to-perform-cycle-counting"></a>Inventoinnin suorittaminen
Vaikka inventoit kaikki varaston nimikkeet vähintään kerran vuodessa, voit päättää joillekin nimikkeille useammin tehtävän inventoinnin, vaikkapa niiden suuren arvon vuoksi tai koska ne liikkuvat nopeasti varastosta ja ovat suuri osa liiketoimintaa. Voit määrittää tätä varten erityisiä laskentajaksoja.

> [!NOTE]  
>   Jos sijaintiin on määritetty ohjattu hyllytys ja keräily, sinun on käytettävä ensin **Invent. varastopäiväk.** -ikkunaa ja sitten **Nimikepäiväkirja**-ikkunan **Laske f.var. muutos** -toimintoa.

## <a name="to-set-up-counting-periods"></a>Laskentajaksojen määrittäminen
Inventointi suoritetaan tavallisesti toistuvin aikavälein, esimerkiksi kuukausittain, neljännesvuosittain tai vuosittain. Voit määrittää mitä tahansa inventoinnin laskentajaksoja.

Määritä käytettävät inventointijaksot ja määritä yksi niistä kullekin nimikkeelle. Kun suoritat inventoinnin ja käytät inventointipäiväkirjassa **Laske laskentajakso** -vaihtoehtoa, nimikkeiden rivit luodaan automaattisesti.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Varastotilanteen laskentajaksot** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-counting-period-to-an-item"></a>Laskentajakson määritteleminen nimikkeelle  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikkeet** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse nimike, jolle haluat määrittää laskentajakson.  
3. Valitse **Inventointijakson koodi** -kentässä sopiva laskentajakso.  
4. Valitse **Kyllä**-painike vaihtaaksesi koodin ja laskeaksesi nimikkeelle ensimmäisen laskentajakson. Kun lasket seuraavan kerran inventointipäiväkirjassa laskentajakson, nimike näkyy rivinä **Inventoinnin nimikevalinta** -ikkunassa. Voit sitten aloittaa nimikkeen laskennan säännöllisin väliajoin.

## <a name="to-initiate-a-count-based-on-counting-periods"></a>Laskennan aloittaminen laskentajaksojen perusteella
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Varastopäiväkirja** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Laske laskentajakso** -toiminto.

    Avautuvassa **Inventoinnin nimikevalinta** -ikkunassa näkyvät nimikkeet, joille on määritetty laskentajaksot ja jotka on laskettava niiden laskentajaksojen mukaisesti.
3. Suorita inventointi. Lisätietoja on kohdassa Inventoinnin suorittaminen.

## <a name="to-adjust-the-inventory-of-one-item"></a>Yhden nimikkeen varastonimikkeen muuttaminen
Kun nimikkeen fyysinen laskenta on suoritettu varastoalueellasi, voit käyttää **Muuta varasto**-toimintoa todellisen varastomäärän kirjaamiseen.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikkeet** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse nimike, jonka varastoa haluat muuttaa, ja valitse sitten **Muuta varastoa** -toimintoa.
3. Syötä **Uusi varasto** -kenttään varastomäärä, jonka haluat tallentaa nimikkeelle.
4. Valitse **OK**-painike.

Nimikkeen varasto on nyt määritetty. Uusi määrä näytetään **Nykyinen varasto** -kentässä **Muokkaa varastoa** -ikkunassa ja **Varasto**-kentässä **Nimikekortti**-ikkunassa.

Voit käyttää **Muuta varastoa** -toimintoa myös yksinkertaisena tapana asettaa ostetut nimikkeet varastoon, jos et tallenna ostoja ostolaskuina tai -tilauksina. Lisätietoja on kohdassa [Toimintaohje: Ostojen kirjaaminen](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Kun olet muuttanut varastoa, se on päivitettävä nykyisellä lasketulla arvolla. Lisätietoja on kohdassa [Toimintaohje: Varaston uudelleenarvostus](inventory-how-revalue-inventory.md).

## <a name="to-adjust-the-inventory-quantity-of-one-or-more-items"></a>Vähintään yhden nimikkeen varastosaldon muuttaminen
Voit kirjata **Nimikepäiväkirja** -ikkunassa nimiketapahtuman suoraan ja muuttaa varastoa ostojen, myyntien ja positiivisten tai negatiivisten muutosten yhteydessä asiakirjoja käyttämättä.

Jos nimikepäiväkirjaan kirjataan usein samoja tai saman tyyppisiä päiväkirjan rivejä, jotka liittyvät esimerkiksi materiaalinkulutukseen, voit helpottaa toistuvien toimien suorittamista käyttämällä **Vakionimikepäiväkirja**-ikkunaa. Lisätietoja on ohjeaiheen [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md) kohdassa Vakiopäiväkirjat.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikepäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Tee muutokset varastoon valitsemalla **Kirjaa**-toiminto.

> [!NOTE]  
>   Kun olet muuttanut varastoa, se on päivitettävä nykyisellä lasketulla arvolla. Lisätietoja on kohdassa [Varaston uudelleenarvostus](inventory-how-revalue-inventory.md).

## <a name="to-reclassify-an-items-lot-number"></a>Nimikkeen eränumeron uudelleenluokittelu
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikkeen uudell.luokit. pvk:t** ja valitse sitten aiheeseen liittyvä linkki.
2. Täytä **Nimik. uud.luok.pvk** -ikkunassa tarvittavat kentät.
3. Anna **Eränro**-kentässä nimikkeen nykyinen eränumero.
4. Anna **Uusi eränro** -kentässä nimikkeen uusi eränumero.
5. Valitse **Kirjaa**-toiminto.

## <a name="see-also"></a>Katso myös
[Varasto](inventory-manage-inventory.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

