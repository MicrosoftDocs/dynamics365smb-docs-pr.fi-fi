---
title: "Toimintaohje: Projektien aikaraporttien käyttäminen| Microsoft Docs"
description: Artikkelissa kerrotaan, miten projekteja hallitaan aikaraporttien avulla.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1796436b964f5e1e4220f885e97713848d94bdfb
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-use-time-sheets-for-jobs"></a>Toimintaohje: Aikaraporttien käyttäminen projekteissa
Käytä **Luo aikaraportit** -eräajoa, kun määrität aikaraportit tietylle määrälle ajanjaksoja tai viikkoja. Sinulla on oltava oikeudet luoda aikaraportteja.

Voit kopioida projektin suunnittelurivit aikaraportista ja käyttää niitä. Näin tehtäessä tiedot on syötettävä vain yhteen paikkaan, ja ne ovat aina ajantasaisia.

Kun olet hyväksynyt projektin aikaraportin tapahtumia, voit julkaista ne asianmukaiseen projekti- tai resurssipäiväkirjaan.

Ennen kuin käytät aikaraportteja, sinun on määritettävä aikaraporttien yleistiedot, järjestelmänvalvoja ja vähintään yksi hyväksyjä. Lisätietoja on kohdassa [Toimintaohje: Aikaraporttien määrittäminen](projects-how-setup-time-sheets.md).

**Huomautus**: Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]-kokemuksen mukauttaminen](ui-experiences.md).

## <a name="to-create-a-time-sheet"></a>Aikaraportin luominen
Käytä **Luo aikaraportit** -eräajoa, kun määrität aikaraportit tietylle määrälle ajanjaksoja tai viikkoja. Tämän jälkeen aikaraportin omistaja voi avata sen ja kirjata ajan, joka tehtävään on kulunut.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Aikaraportit** ja valitse sitten liittyvä linkki.
2. Valitse **Aikaraporttiluettelo**-ikkunassa **Luo aikaraportit** -toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Huomautus**: Aikaraportin resurssikortin **Käytä aikaraporttia**- ja **Aikaraportin omistajan käyttäjätunnus** -kenttä on täytettävä.

1. Valitse **OK**-painike.  

Voit tarkastella samoja aikaraportteja, jotka olet luonut **Aikaraporttiluettelo**-ikkunassa.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Kopioi työn suunnittelurivit aikaraporttiin
Seuraavassa ohjeessa neuvotaan, miten lisätään projektin suunnittelurivejä nopeasti aikaraportille.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Aikaraportit** ja valitse sitten liittyvä linkki.  
2. Valitse **Aikaraporttiluettelo**-ikkunassa kyseisen ajanjakson aikaraportti. Valitse sitten **Muokkaa aikaraporttia** -toiminto.  
3. Valitse **Luo rivejä projektin suunnittelusta** -toiminto. Kaikki aikaraportin ajanjakson projektin suunnittelurivit kopioidaan sen henkilön tai koneen aikaraporttiin, joka mainitaan **Resurssin nro** -kentässä aikaraportissa.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Työtyyppien määrittäminen ja yhden työtyypin lisääminen aikaraporttiin
Voit määrittää projektien kaikille aikaraporttiriveille työtyypin. Tällä tavalla voit lisätä tiedot, joita tarvitse asiakkaan laskuttamiseen erityyppisistä töistä.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Aikaraportit** ja valitse sitten liittyvä linkki.   
2. Avaa asianmukainen aikaraportti.
3. Valitse **Kuvaus**-kenttä.  
4. Valitse **Aikaraporttirivin projektierittely** -ikkunassa **Työtyyppikoodi**-kenttä. Valitse sitten luettelosta työtyyppi, kuten **Mailit**.  
5. Jos työtyyppiä ei ole, valitse **Uusi**-toiminto.
6. Täytä **Työtyypit**-ikkunassa tarvittavat kentät.
7. Määritä uusi työtyyppi aikaraporttiin toistamalla vaihe 4.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Aikaraportin rivien käyttäminen uudelleen muissa aikaraporteissa
Jos aikaraportin tiedot pysyvät samoina ajanjaksosta toiseen, voit tallentaa ajan kopioimalla rivit edelliseltä ajanjaksolta. Sitten vain kirjoitetaan käytetty aika uudelle jaksolle.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Aikaraportit** ja valitse sitten liittyvä linkki.  
2. Avaa aikaraportti jaksolle, joka on myöhempi kuin olemassa oleva aikaraportti ja sen rivit.  
3. Valitse **Kopioi rivit aiemmasta aikaraportista** -toiminto.

Rivit kopioidaan, mukaan lukien tarkat tiedot, kuten tyyppi ja kuvaus. Jos rivi liittyy esimerkiksi projektiin, **Projektinro**. kopioidaan. Kaikki kopioitujen rivien tila on **Avoin**. Voit nyt muokata rivejä tarpeen mukaan.

## <a name="to-fill-in-a-time-sheet-lines-and-submit-for-approval"></a>Aikaraporttirivien täyttäminen ja lähettäminen hyväksyttäväksi
Aikaraportin rekisteröintiä seurataan tunneissa, resurssien perusmittayksikköissä. Oletusarvon mukaan aikaraportti näyttää yleiset työpäivät maanantaista perjantaihin.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Aikaraportit** ja valitse sitten liittyvä linkki.  
2. Valitse kyseisen ajanjakson aikaraportti ja valitse sitten **Muokkaa aikaraporttia** -toiminto.  
3. Täytä tarvittaessa rivin kentät. Syötä resurssin kunkin viikonpäivän käyttötunnit.

    **Vihje**: Voit esikatsella aikaraportin tuntimäärää, jonka olet syöttänyt **Toteutunut/budjetoitu yhteenveto** -tietoruutuun.  
4. Toista vaihe 3 muille resurssin suorittamille työtyypeille.
5. Valitse **Lähetä**-toiminto. Lähetä sitten kaikki rivit valitsemalla **Kaikki avoimet rivit** -toiminto tai lähetä vain **Aikaraportti**-ikkunassa valitut rivit valitsemalla **Vain valitut rivit** -toiminto.  

    **Huomautus**: Voit lähettää vain ne aikaraporttirivit, joille on syötetty aika.  
6. Muokkaa tietoja rivillä, jonka tilaksi on määritetty **Lähetetty**, valitsemalla rivi ja valitsemalla sitten **Avaa uudelleen** -toiminto.

    **Huomautus**: Päällikkö voi hylätä aikaraporttirivin, joka on lähetetty hyväksyttäväksi. Jos rivin tila on **Hylätty**, voit muuttaa riviä ja valita sitten uudelleen **Lähetä**-kohdan.  
7. Valitse **OK**-painike.

## <a name="to-approve-or-reject-a-time-sheet"></a>Hyväksy tai hylkää aikaraportti
Aikaraportti on lähetettävä hyväksyttäväksi, jotta sitä voidaan käyttää. Voit hyväksyä ja hylätä aikarapportin yksittäisiä rivenä tai lähettää ne takaisin lähettäjälle lisätoimenpiteitä varten. Aikaraportti voidaan hyväksyä kahdella seuraavalla tavalla:

* aikaraportin järjestelmänvalvoja voi hyväksyä minkä tahansa aikaraportin
* henkilö, joka on määritetty resurssikortin **Aikaraportin hyväksyjän käyttäjätunnus** -kentässä, voi hyväksyä kyseisen resurssin aikaraportteja. Lisätietoja on kohdassa [Toimintaohje: Aikaraporttien määrittäminen](projects-how-setup-time-sheets.md).

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Päällikön aikaraportti** ja valitse sitten liittyvä linkki.
2. Valitse aikaraportti luettelosta.  
3. Valitse **Aikaraportti**-ikkunassa **Hyväksy**-toiminto. Hyväksy sitten kaikki rivit valitsemalla **Kaikki lähetetyt rivit** -toiminto tai hyväksy vain **Aikaraportti**-ikkunassa valitut rivit valitsemalla **Vain valitut rivit** -toiminto.
4. Valitse **OK**-painike.  
5. Vaihtoehtoisesti voit valita **Hylkää**-toiminnon ja suorittaa vaiheet 4 ja 5.  

**Vihje**: Saat nopean yleiskuvauksen aikaraportin tiedoista **Aikaraportin tila**- ja **Toteutunut/budjetoitu yhteenveto** -tietoruudun avulla.

Kun olet hyväksynyt tai hylännyt aikaraportin, sitä voi muokata vasta sitten, kun aikaraportti on avattu uudelleen. Seuraavassa kerrotaan, miten hyväksytty tai hylätty aikaraportti avataan uudelleen.

## <a name="to-reopen-a-time-sheet"></a>Avaa aikaraportti uudelleen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Päällikön aikaraportti** tai **Aikaraportit**ja valitse sitten liittyvä linkki.
2. Avaa aikaraportti luettelosta.  

    **Huomautus**: Voit avata uudelleen vain rivit, joiden tila on **Hyväksytty**. Et voi avata uudelleen rivejä, joiden tila on **Hylätty**. Et voi avata uudelleen aikaraporttia, jos se on kirjattu.  
3. Valitse **Aikaraportti**-ikkunassa **Avaa uudelleen** -toiminto. Avaa sitten kaikki rivit uudelleen valitsemalla **Kaikki lähetetyt rivit** -toiminto tai avaa uudelleen vain **Aikaraportti**-ikkunassa valitut rivit valitsemalla **Vain valitut rivit** -toiminto.
4. Valitse **OK**-painike. Aikaraporttien rivin tai rivien tilaksi tulee **Lähetetty**.  

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Aikaraporttirivien kirjaaminen resurssipäiväkirjaan
Kun olet hyväksynyt resurssin aikaraportin tapahtumia, voit julkaista ne asianmukaiseen resurssipäiväkirjaan.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Resurssipäiväkirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Ehdota rivejä aikaraporteista** -toiminto.  
3. Täytä tarvittavat kentät.  
4. Valitse **OK**-painike. Käytön tapahtumat luodaan resurssipäiväkirjaan. Siellä voit muokata tietoja tarvittaessa.  
5. Valitse **Kirjaa**-toiminto.  
6. Vahvista kirjaus valitsemalla **Tapahtumakirjaukset**-toiminto. Näyttöön avautuu **Resurssitapahtumat**-ikkuna, jossa näkyvät resurssipäiväkirjan kirjausten tulokset.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Aikaraporttirivien kirjaaminen projektipäiväkirjaan
Kun olet hyväksynyt työn aikaraportin tapahtumia, voit julkaista ne asianmukaiseen projektipäiväkirjaan.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektipäiväkirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Ehdota rivejä aikaraporteista** -toiminto.  
3. Täytä tarvittavat kentät.  
4. Valitse **OK**-painike. Käytön tapahtumat luodaan projektipäiväkirjaan. Siellä voit muokata tietoja tarvittaessa.  

    **Huomautus**: Tietoja työn tyypistä ja siitä, onko työ on veloitettavissa, kopioidaan aikaraporttiriviltä. Voit tarvittaessa vähentää tuntien määrää ja tehdä osittaisen kirjauksen. Jos vähennät määrää, luotava rivi sisältää jäljellä olevat tunnit, kun valitse seuraavan kerran **Ehdota rivejä aikaraporteista** -toiminto.  
5. Valitse **Kirjaa**-toiminto.  
6. Vahvista kirjaus valitsemalla **Tapahtumakirjaukset**-toiminto. Näyttöön avautuu **Projektitapahtumat**-ikkuna, jossa näkyvät resurssipäiväkirjan kirjausten tulokset.

## <a name="to-archive-time-sheets"></a>Arkistoi aikaraportit
Kun olet kirjannut aikaraportit, voit arkistoida ne myöhempää käyttöä varten. Kaikki aikaraporttirivit on kirjattava, ennen kuin aikaraportti voidaan arkistoida.

**Huomautus**: Kun arkistoit aikaraportin, se poistetaan sekä **Aikaraportit**-ikkunan että **Päällikon aikaraportit** -ikkunan luettelosta.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Siirrä aikaraportit arkistoon** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät ja valitse sitten **OK**-painike.  
3. Voit tarkastella arkistoituja aikaraportteja valitsemalla oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Aikaraporttiarkistot** tai **Päällikön aikaraporttiarkistot**ja valitse sitten liittyvä linkki.

## <a name="see-also"></a>Katso myös
[Projektinhallinta](projects-manage-projects.md)  
[Projektinhallinnan määrittäminen](projects-setup-projects.md)    
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)     
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  

