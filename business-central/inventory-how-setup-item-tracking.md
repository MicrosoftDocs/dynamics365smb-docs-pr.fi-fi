---
title: Sarja-, erä- ja pakettinumeroita sisältävien nimikkeiden seurannan määrittäminen
description: Sarja-, erä- ja pakettinumeroita sisältävien nimikkeiden seurannan määrittäminen
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/31/2021
ms.author: edupont
ms.openlocfilehash: ae490b4694aaa852962968cb80fef9f770767a57
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141045"
---
# <a name="set-up-item-tracking-with-serial-lot-and-package-numbers"></a>Sarja-, erä- ja pakettinumeroita sisältävien nimikkeiden seurannan määrittäminen

Varastonimikkeitä voi seurata myös monimutkaisissa fyysisen varastonnin määrityksillä käyttämällä nimikekohtaisia numeroita, jotka koskevat yksittäistä kohdetta, erää tai pakettia. Nimikeseurannan avulla voidaan jäljittää nimikkeiden siirtoja fyysisen varastoinnin sisällä sekä lähtevissä ja saapuvissa asiakirjoissa.

Nimikkeet, joiden sarja- ja eränumeroita voidaan jäljittää toimitusketjussa eteen- ja taaksepäin. Tämä kätevää yleisessä laadunvarmistuksessa ja tuotteen takaisinvedossa. Lisätietoja on kohdassa [Nimikeseurannan nimikkeiden jäljittäminen](inventory-how-to-trace-item-tracked-items.md)  

> [!TIP]
> Vuoden 2021 1. julkaisuaallossa ja myöhemmissä versioissa *Käytä seurantaa varaus- ja seurantajärjestelmän pakettinumeron perusteella* -ominaisuuspäivitys on otettava käyttöön, jos sarja- ja eränumeroiden ohella halutaan käyttöön myös pakettinumeroita. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](admin-feature-management.md). Kun ominaisuus on otettu käyttöön, pakettinumeroita voidaan määrittää lähtevillä ja saapuville asiakirjoilla samalla tavoin kuin eränumeroita käytettäessä.  

## <a name="numbers-and-item-tracking"></a>Numerot ja nimikeseuranta

Fyysisen varastointiprosessien osana varastoa voidaan niputtaa esimerkiksi paketeiksi, laatikoiksi ja konteiksi. Nimikkeiden seuranta kuitenkin edellyttää yksilöivien numeroiden määrittämistä tunnisteiksi. Kyse voi olla esimerkiksi valmistettavasta ja myytävästä tuolista, jonka nimikenumero on *1900-S*. Jokaisella yksittäisellä tuolilla on sarjanumero *1001*, minkä lisäksi neljä tuolia niputetaan eräksi *LOT0001*. Tuolit toimitetaan sitten kontissa käyttämällä pakettinumeroa *CONTAINER010*, joka sisältää myös muita nimikkeitä, kuten sivupöydistä koostuvan erän *LOT0100* ja lampuista koostuvan erän *LOT200*.  

Määritysten mukaan näiden erilaisten numeroiden avulla varastoa seurataan [!INCLUDE [prod_short](includes/prod_short.md)]issa esimerkiksi osto-, myynti- ja varastointitoimintojen aikana.

## <a name="to-set-up-item-tracking-codes"></a>Nimikkeen seurantakoodien määrittäminen

Nimikkeen seurantakoodi kuvastaa niitä asioita, jotka yritys on ottanut huomioon koskien sarja-/eränumeroiden käyttöä nimikkeiden kohdalla, jotka kulkevat varaston läpi.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikeseurannan koodit** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Määritä **Sarjanumero**-, **Eränumero**- ja **Paketin numero** -pikavälilehdissä nimikeseurantakäytännöt vastaavien sarja-, erä- ja pakettinumeroiden avulla.  

> [!NOTE]  
> Jos haluat seurata tiettyjä nimikkeitä tai tiettyjä eriä koko niiden elinkaaren ajana, sinun on valittava vastaavasti joko **SN-kohtainen seuranta**- tai **Eräkohtainen seuranta** -kenttä. Tällöin tämän nimikeseurannan koodin mukaista nimikkeen lähtevää yksikköä käsiteltäessä tulee aina määrittää, mitä olemassa olevaa sarjanumeroa tai mitä olemassa olevaa eränumeroa käsitellään. Tämä tarkoittaa sitä, että nimikkeen yksikköä myytäessä se tulee olla kohdistettu tiettyyn sarjanumeroiden tai eränumeroiden pooliin varastossa. Toisin sanoen nimikkeelle varastoon tullessa määritellyn sarjanumeron tai eränumeron tulee seurata kyseistä nimiketyyppiä ulos varastosta.

Koska kyseinen asetuskenttä kattaa kaikki mahdolliset nimikkeen transaktiot, myös yksittäisiin saapuvien/lähtevien kentät valitaan. Yksittäisillä saapuvilla/lähtevillä kentillä ei ole kuitenkaan mitään tekemistä varastossa kohdistuksen kanssa – ne ainoastaan määrittelevät yrityksen tehtävienhallintaa koskien sitä, milloin määritellään nimikeseurantanumeroita.  

> [!NOTE]  
>  Kun määrität nimikeseurantanumeroita fyysisen varaston toiminnoille, **SN F.varastoinnin seuranta**- ja **Erän fyysisen varaston seuranta** -kenttien on oltava valittuna nimikkeen nimikeseurantakoodin kortissa.  

## <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Vanhentumissääntöjen määrittäminen sarja-/eränumeroille

Voit haluta määrittää tiettyjen nimikkeiden osalta erityisiä vanhenemispäivämääriä ja sääntöjä nimikkeen seurantakoodille. Tämän ominaisuuden ansiosta voit seurata sitä, milloin tietyt sarja-/eränumerot vanhenevat.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikeseurannan koodit** ja valitse sitten vastaava linkki.
2. Valitse ensin aiemmin luotu nimikkeen seurantakoodi ja valitse sitten **Muokkaa**-toiminto.  
3. Valitse **Muut**-pikavälilehdessä seuraavat kentät:  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Tiukka vanhentumisen kirj.**|Määrittää, että nimikeseurantanumerolle varastoon tullessa määritettyä vanhentumispäivämäärää tulee noudattaa silloin, kun numero poistuu varastosta.|  
    |**Vaadi vanhentumisen päivämäärämerkintä**|Määrittää, että nimikkeen seurantariville pitää syöttää vanhentumispäivämäärä.|  
    |**Käytä vanhentumispäivämääriä**|Määrittää, että haluat laskea vanhentumispäivämääriä. |  

## <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Takuiden määrittäminen sarja-/eränumeroille

Voit haluta määrittää tiettyjen nimikkeiden osalta erityisiä takuita nimikkeen seurantakoodille. Tämän ominaisuuden avulla voit seurata sitä, milloin varastossa olevien tiettyjen sarja-/eränumeroiden takuut menevät umpeen.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikeseurannan koodit** ja valitse sitten vastaava linkki.  
2. Valitse ensin aiemmin luotu nimikkeen seurantakoodi ja valitse sitten **Muokkaa**-toiminto.  
3. Määritä **Sekalainen**-pikavälilehden **Takuun laskentakaava** -kentän arvo ja valitse sitten kentät seuraavasti:  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Takuupvm:n kaava**|Määrittää tuotteen viimeisen takuupäivän.|  
    |**Vaadi takuun päivämäärämerkintä**|Määrittää, että sinun täytyy syöttää nimikeseurantariville takuupäivämäärä manuaalisesti.|  


## <a name="to-set-up-items-for-tracking-with-the-correct-item-tracking-codes"></a>Nimikkeiden määrittäminen seurantaa varten, joilla on oikeat nimikkeen seurantakoodit

Jotta nimikkeen seuranta voidaan ottaa käyttöön, nimikkeelle on ensin määritettävä nimikkeen seurantakoodit. Nimikkeen seurantakoodeja voi lisätä kahdella tavalla: valitsemalla koodi ennalta määritetystä luettelosta tai määrittämällä uuden yksilöllisen koodin. Lue lyhyt kuvaus siirtämällä kohdistin kenttien päälle.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimike** ja valitse sitten vastaava linkki.
2. Valitse luettelosta aiemmin luotu kohde ja avaa **Nimikekortti**-sivu.  
3. Määritä **Nimikkeen seuranta** -pikavälilehdessä asianmukaiset nimikeseurantakoodit ja valitse **Nimikkeen seurantakoodi**, **Sarjanrot** ja **Eränrot**.
    1. Vaihtoehtoisesti voit myös luoda uuden nimikkeen seurantakoodin valitsemalla **Uusi**-toiminnon.

## <a name="see-also"></a>Katso myös

[Sarja- ja eränumeroiden työstäminen ](inventory-how-work-item-tracking.md)
[Jäljitä nimikeseurattuja nimikkeitä](inventory-how-to-trace-item-tracked-items.md)  
[Varasto](inventory-manage-inventory.md)  
[Rakennetiedot: Nimikkeen seuranta](design-details-item-tracking.md)  
[Rakennetiedot – nimikkeen seuranta ja varaukset](design-details-item-tracking-and-reservations.md)  
[Nimikkeiden varaaminen](inventory-how-to-reserve-items.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]