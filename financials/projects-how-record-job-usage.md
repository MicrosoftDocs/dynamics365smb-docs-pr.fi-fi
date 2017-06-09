---
title: "Toimintaohje: Projektien käytön kirjaaminen| Microsoft Docs"
description: Artikkelissa kerrotaan, miten projektien nimikkeet tai resurssit kirjataan.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 896b26e11042155860d6c933d937066f9c9aec73
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-usage-for-jobs"></a>Toimintaohje: Projektien käytön kirjaaminen
**Projektin suunnittelurivit** -ikkunassa voit tarkastella ja tallentaa projektin eri osien käyttötietoja, jotka päivitetään automaattisesti, kun muokkaat ja siirrät tietoja projektin ja projektipäiväkirjan tai projektin laskujen välillä. Tämä edellyttää, että työ on määritetty siten, että **Käytä käyttölinkkiä** on käytössä. Lisätietoja on kohdassa [Toimintaohje: Projektien määrittäminen](projects-how-setup-jobs.md).  

Voit syöttää esimerkiksi tyyppiä **Budjetti** oleville suunnitteluriveille resurssin määrän ja osoittaa, mikä määrä siirretään projektipäiväkirjaan. Jos suunnittelurivin tyyppi on **Laskutettava**, voit syöttää resurssin määrän ja määrittää laskulle siirrettävän määrän. Vertaamalla määrää, joka on siirretty päiväkirjaan tai jäljellä olevan määrän laskuun, voit tarkistaa nopeasti käyttötiedot.

Seuraavassa kuvataan, miten todelliset (laskutettavat) tai budjetoidut projektihinnat ja -kustannukset kirjataan. Lisätietoja budjetoitujen arvojen arvioinnista suunnittelun aikana on kohdassa [Tiomintaohje: Projektibudjettien hallinta](projects-how-manage-budgets.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Käytön kirjaaminen Budjetti-tyypin projektin suunnitteluriville
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektit** ja valitse sitten liittyvä linkki.  
2. Valitse asianmukainen projekti ja valitse sitten **Projektin suunnittelurivit** -toiminto.
3. Valitse projektin suunnittelurivin tyyppi, joka on **Budjetti** tai **Sekä budjetti että laskutettava** ja jolle haluat kirjata käytön.
4. Kirjoita **Päiväkirjaan siirrettävä määrä** -kenttään määrä, jonka haluat siirtää laskuun. Oletusmäärä on **Määrä**-kenttään syöttämäsi arvo.

    **Jäljellä oleva määrä** -kentässä näkyy määrä, joka on jäljellä projektin valmiiksi suorittamista ja päiväkirjaan siirtämistä varten.  
5. Valitse **Luo projektipäiväkirjan rivit** -toiminto.
6. Täytä **Projektin siirron projektisuunnittelurivi** -ikkunassa kenttiä tarpeen mukaan ja valitse sitten **OK**-painike. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Valitse **Avaa projektipäiväkirja** -toiminto.  
8. Valitse **Projektipäiväkirja**-ikkunassa asianmukainen rivi ja valitse sitten **Kirjaa**-toiminto.
9. Tarkista **Projektin suunnittelurivit** -ikkunassa kirjattu käyttö **Määrä**-, **Jäljellä oleva määrä**- ja **Päiväkirjaan siirrettävä määrä** -kentän avulla.  
10. Kirjaa lisäkäyttö toistamalla vaiheet 3–8.  

## <a name="to-record-usage-for-a-job-planning-line-of-type-billable"></a>Käytön kirjaaminen Laskutettava-tyypin projektin suunnitteluriville
Seuraavassa tehtävässä kirjaat myös käytön, mutta **Laskutettava**-tyyppistä projektin suunnitteluriviä varten. Yleensä tässä tapauksessa laskutat käytöstä, mutta voit myös siirtää sen päiväkirjaan. Kun teet tämän, luodaan **Budjetti**-tyyppinen projektin suunnittelurivi, joka vastaa laskutettavaa riviä. Lisätietoja on kohdassa [Toimintaohje: Projektibudjettien hallinta](projects-how-manage-budgets.md).

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektit** ja valitse sitten liittyvä linkki.
2. Valitse asianmukainen projekti ja valitse sitten **Projektin suunnittelurivit** -toiminto.  
3. Valitse projektin suunnittelurivin tyyppi **Laskutettava**, jolle haluat kirjata käytön.
4. Kirjoita **Laskuun siirrettävä määrä** -kenttään määrä, jonka haluat siirtää laskuun. Oletusmäärä on **Määrä**-kenttään syöttämäsi arvo.

    **Laskutettava määrä** -kentässä näkyy määrä, joka on jäljellä projektin valmiiksi suorittamista ja laskuttamista varten.  
5. Valitse **Luo myyntilasku** -toiminto.
6. Täytä **Siirrä projekti myyntilaskuun** -ikkunan tarvittavat kentät ja valitse sitten **OK**-painike.
7. Valitse **Projektin suunnittelurivit** -ikkunassa asianmukainen rivi ja valitse sitten **Kirjaa**-toiminto.
8. Tarkista kirjattu käyttö **Määrä**-, **Laskutettava määrä**- ja **Laskuun siirrettävä määrä** -kentän avulla. Jos myyntilasku on kirjattu, käytä myös **Laskutettu määrä** -kenttää.
9. Kirjaa lisäkäyttö toistamalla vaiheet 3–8.  
10. Voit tarkastella liittyvää kirjattua myyntilaskua valitsemalla **Myyntilaskut/hyvityslaskut** -toiminnon.  
11. Valitse **Projektin laskut** -ikkunassa asianmukainen lasku ja valitse sitten **Avaa myyntilasku/hyvityslasku** -toiminto.         

## <a name="to-create-job-journal-lines-from-job-planning-lines"></a>Luo projektipäiväkirjan rivit projektin suunnitteluriveistä
Kun olet valmis kirjaamaan projektien taloustiedot, luo kirjattavat projektipäiväkirjan rivit.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektit** ja valitse sitten liittyvä linkki.  
2. Valitse asianmukainen avoin projekti ja valitse sitten **Projektin suunnittelurivit** -toiminto.  
3. Syötä **Projektin suunnittelurivit** -ikkunan asianmukaisen projektin suunnittelurivin **Päiväkirjaan siirrettävä määrä** -kenttään projektipäiväkirjaan siirrettävä määrä.  
4. Valitse **Luo projektipäiväkirjan rivit** -toiminto.
5. Täytä **Projektin siirron projektisuunnittelurivi** -ikkunassa tarvittavat kentät.  
6. Valitse **OK**-painike. Projektipäiväkirjan rivit luodaan.
7. Tarkista siirto avaamalla asianmukainen projektipäiväkirjan erä ja tarkastamalla tapahtumat.  
8. Kun projektipäiväkirjan rivit ovat valmiit, valitse **Kirjaa**-toiminto.  

## <a name="to-create-job-journal-lines-manually"></a>Luo projektipäiväkirjan rivit manuaalisesti
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektipäiväkirjat** ja valitse sitten liittyvä linkki.  
2. Valitse **Erän nimi** -kentässä asianmukaisen projektipäiväkirjan erä.  
3. Kirjoita uudelle riville asiakirjan numero, projektinumero, projektin tehtävän numero, tyyppi ja kulutettavan tyypin määrä.  
4. Kun projektipäiväkirjan rivit ovat valmiit, valitse **Kirjaa**-toiminto.  

## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Projektitapahtuman suunnittelurivien tarkasteleminen
Kun olet kirjannut projektipäiväkirjan rivit, näkyvissä ovat suunnittelurivit, jotka liittyvät kirjattuihin projektitapahtumiin.

**Huomautus**: Tämä edellyttää, että **Käytä käyttölinkkiä** -valintaruutu on valittu, tai että se on kaikkien töiden oletusasetus organisaatiossa. Lisätietoja on kohdassa [Toimintaohje: Projektien määrittäminen](projects-how-setup-jobs.md).  

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektipäiväkirjat** ja valitse sitten liittyvä linkki.  
2. Valitse asianmukaisen projektin päiväkirja ja valitse sitten **Tapahtumakirjaukset**-toiminto.  
3. Valitse **Projektitapahtumat**-ikkunassa **Näytä linkitetyt projektin suunnittelurivit** -toiminto.

## <a name="see-also"></a>Katso myös
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  

