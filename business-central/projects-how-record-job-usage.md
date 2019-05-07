---
title: Projektiresurssien laskutettavien ja budjetoidun käytön kirjaaminen| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten projektien nimikkeiden tai resurssien kulutus tai käyttö tallennetaan projektinhallinnan helpottamiseksi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c723625bc54c7b885268946f0e7afdf54be20a2b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "923219"
---
# <a name="record-usage-for-jobs"></a>Projektien käytön kirjaaminen
**Projektin suunnittelurivit** -sivulla voi tarkastella ja tallentaa projektin eri osien käyttötietoja, jotka päivitetään automaattisesti, kun muokkaat ja siirrät tietoja projektin ja projektipäiväkirjan tai projektin laskujen välillä. Tämä edellyttää, että työ on määritetty siten, että **Käytä käyttölinkkiä oletusarvoisesti** on käytössä. Lisätietoja on kohdassa [Projektien määrittäminen](projects-how-setup-jobs.md).  

Voit syöttää esimerkiksi tyyppiä **Budjetti** oleville suunnitteluriveille resurssin määrän ja osoittaa, mikä määrä siirretään projektipäiväkirjaan. Jos suunnittelurivin tyyppi on **Laskutettava**, voit syöttää resurssin määrän ja määrittää laskulle siirrettävän määrän. Vertaamalla määrää, joka on siirretty päiväkirjaan tai jäljellä olevan määrän laskuun, voit tarkistaa nopeasti käyttötiedot.

Seuraavassa kuvataan, miten todelliset (laskutettavat) tai budjetoidut projektihinnat ja -kustannukset kirjataan. Lisätietoja budjetoitujen arvojen arvioinnista suunnittelun aikana on kohdassa [Projektibudjettien hallinta](projects-how-manage-budgets.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Käytön kirjaaminen Budjetti-tyypin projektin suunnitteluriville
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten liittyvä linkki.  
2. Valitse soveltuva projekti ja valitse sitten **Projektin suunnittelurivit** -toiminto.
3. Valitse projektin suunnittelurivin tyyppi, joka on **Budjetti** tai **Sekä budjetti että laskutettava** ja jolle haluat kirjata käytön.
4. Kirjoita **Päiväkirjaan siirrettävä määrä** -kenttään määrä, jonka haluat siirtää laskuun. Oletusmäärä on **Määrä**-kenttään syöttämäsi arvo.

    **Jäljellä oleva määrä** -kentässä näkyy määrä, joka on jäljellä projektin valmiiksi suorittamista ja päiväkirjaan siirtämistä varten.  
5. Valitse **Luo projektipäiväkirjan rivit** -toiminto.
6. Täytä **Projektin siirron projektisuunnittelurivi** -sivulla kenttiä tarpeen mukaan ja valitse sitten **OK**-painike. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Valitse **Avaa projektipäiväkirja** -toiminto.  
8. Valitse **Projektipäiväkirja**-sivulla asianmukainen rivi ja valitse sitten **Kirjaa**-toiminto.
9. Tarkista **Projektin suunnittelurivit** -sivulla kirjattu käyttö **Määrä**-, **Jäljellä oleva määrä**- ja **Päiväkirjaan siirrettävä määrä** -kentän avulla.  
10. Kirjaa lisäkäyttö toistamalla vaiheet 3–8.  

## <a name="to-record-usage-for-a-job-planning-line-of-type-billable"></a>Käytön kirjaaminen Laskutettava-tyypin projektin suunnitteluriville
Seuraavassa tehtävässä kirjaat myös käytön, mutta **Laskutettava**-tyyppistä projektin suunnitteluriviä varten. Yleensä tässä tapauksessa laskutat käytöstä, mutta voit myös siirtää sen päiväkirjaan. Kun teet tämän, luodaan **Budjetti**-tyyppinen projektin suunnittelurivi, joka vastaa laskutettavaa riviä. Lisätietoja on kohdassa [Projektibudjettien hallinta](projects-how-manage-budgets.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten liittyvä linkki.
2. Valitse soveltuva projekti ja valitse sitten **Projektin suunnittelurivit** -toiminto.  
3. Valitse projektin suunnittelurivin tyyppi **Laskutettava**, jolle haluat kirjata käytön.
4. Kirjoita **Laskuun siirrettävä määrä** -kenttään määrä, jonka haluat siirtää laskuun. Oletusmäärä on **Määrä**-kenttään syöttämäsi arvo.

    **Laskutettava määrä** -kentässä näkyy määrä, joka on jäljellä projektin valmiiksi suorittamista ja laskuttamista varten.  
5. Valitse **Luo myyntilasku** -toiminto.
6. Täytä **Siirrä projekti myyntilaskuun** -sivulla tarvittavat kentät ja valitse sitten **OK**-painike.
7. Valitse **Projektin suunnittelurivit** -sivulla asianmukainen rivi ja valitse sitten **Kirjaa**-toiminto.
8. Tarkista kirjattu käyttö **Määrä**-, **Laskutettava määrä**- ja **Laskuun siirrettävä määrä** -kentän avulla. Jos myyntilasku on kirjattu, käytä myös **Laskutettu määrä** -kenttää.
9. Kirjaa lisäkäyttö toistamalla vaiheet 3–8.  
10. Voit tarkastella liittyvää kirjattua myyntilaskua valitsemalla **Myyntilaskut/hyvityslaskut** -toiminnon.  
11. Valitse **Projektin laskut** -sivulla asianmukainen lasku ja valitse sitten **Avaa myyntilasku/hyvityslasku** -toiminto.         

## <a name="to-create-job-journal-lines-from-job-planning-lines"></a>Luo projektipäiväkirjan rivit projektin suunnitteluriveistä
Kun olet valmis kirjaamaan projektien taloustiedot, luo kirjattavat projektipäiväkirjan rivit.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten liittyvä linkki.  
2. Valitse asianmukainen avoin projekti ja valitse sitten **Projektin suunnittelurivit** -toiminto.  
3. Anna **Projektin suunnittelurivit** -sivulla asianmukaisen projektin suunnittelurivin **Päiväkirjaan siirrettävä määrä** -kenttään projektipäiväkirjaan siirrettävä määrä.  
4. Valitse **Luo projektipäiväkirjan rivit** -toiminto.
5. Täytä **Projektin siirron projektisuunnittelurivi** -sivulla tarvittavat kentät.  
6. Valitse **OK**-painike. Projektipäiväkirjan rivit luodaan.
7. Tarkista siirto avaamalla asianmukainen projektipäiväkirjan erä ja tarkastamalla tapahtumat.  
8. Kun projektipäiväkirjan rivit ovat valmiit, valitse **Kirjaa**-toiminto.  

## <a name="to-create-job-journal-lines-manually"></a>Luo projektipäiväkirjan rivit manuaalisesti
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten liittyvä linkki.  
2. Valitse **Erän nimi** -kentässä asianmukaisen projektipäiväkirjan erä.  
3. Kirjoita uudelle riville asiakirjan numero, projektinumero, projektin tehtävän numero, tyyppi ja kulutettavan tyypin määrä.  
4. Kun projektipäiväkirjan rivit ovat valmiit, valitse **Kirjaa**-toiminto.  

## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Projektitapahtuman suunnittelurivien tarkasteleminen
Kun olet kirjannut projektipäiväkirjan rivit, näkyvissä ovat suunnittelurivit, jotka liittyvät kirjattuihin projektitapahtumiin.

> [!NOTE]  
>   Tämä edellyttää, että työn **Käytä käyttölinkkiä oletusarvoisesti** -valintaruutu on valittu, tai että se on kaikkien töiden oletusasetus organisaatiossa. Lisätietoja on kohdassa [Projektien määrittäminen](projects-how-setup-jobs.md).  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten liittyvä linkki.  
2. Valitse asianmukaisen projektin päiväkirja ja valitse sitten **Tapahtumakirjaukset**-toiminto.  
3. Valitse **Projektitapahtumat**-sivulla **Näytä linkitetyt projektin suunnittelurivit** -toiminto.

## <a name="see-also"></a>Katso myös
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
