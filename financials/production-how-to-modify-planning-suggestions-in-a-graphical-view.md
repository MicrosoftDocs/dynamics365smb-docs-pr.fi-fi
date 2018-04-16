---
title: "Suunnitteluehdotusten muokkaaminen graafisessa näkymässä | Microsoft Docs"
description: "Tyypillinen suunnittelun tehtävä on muuttaa tai lisätä suunnittelutyökirjan rivejä ehdotettujen toimitustilausten muokkaamiseksi ennen kuin ne suoritetaan **Toteuta toimenpideviesti** -toiminnolla. Vaihtoehtona suunnittelutyökirjassa on graafinen esitys."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 9217d8707ab65d231a6759e86f6f2b2866835bb8
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="modify-planning-suggestions-in-a-graphical-view"></a>Suunnitteluehdotusten muokkaaminen graafisessa näkymässä
Tyypillinen suunnittelun tehtävä on muuttaa tai lisätä suunnittelutyökirjan rivejä ehdotettujen toimitustilausten muokkaamiseksi ennen kuin ne suoritetaan **Toteuta toimenpideviesti** -toiminnolla. Vaihtoehtona suunnittelutyökirjassa on graafinen esitys.

Voit muokata **Nimikkeen saatavuus aikajanalla** -ikkunassa tiettyjä toimitustilauksia ja ehdotuksia muuttamalla määrää vetämällä elementtejä x-akselilla tai muuttamalla eräpäivää vetämällä elementtejä y-akselilla.  

 **Nimikkeen saatavuus aikajanalla** -ikkunassa ja **Suunnittelutyökirja** -ikkunassa voi tehdä seuraavat muutokset:  

-   Muokkaa ehdotettua toimitustilausta, joka on olemassa vain suunnittelurivinä.  
-   Muokkaa olemassa olevaa toimitustilausta, jonka muuttamista suunnitttelujärjestelmä ehdottaa.  
-   Luo uusi ehdotettu toimitustilaus ja muokkaa sitä.  

Lisätietoja näytettävistä suunnitteluriveistä on **Tapahtumamuutokset**-välilehden Kuvaus-kentässä.  

Kun valitset **Tallenna muutokset** **Nimikkeen saatavuus aikajanalla** -ikkunassa, muutokset, jotka olet tehnyt, kopioidaan suunnittelu- tai hankintalistapöytäkirjaan. Voit nyt toteuttaa muutokset **Toteuta toim.pidviesti - Suun.** -toiminnoissa  

Seuraavassa ohjeessa neuvotaan, miten tarjontaehdotuksia voi muokata vetämällä ja pudottamalla. Vaihtoehtona, voit muuttaa **Eräpäivä**- ja **Määrä**-kenttiä **Tapahtumamuutokset**-pikavälilehdessä ja nähdä muutokset heti graafisesti **Aikajana**-pikavälilehdellä **Suunnittelutyökirja** -ikkunassa.  

## <a name="to-modify-suggested-supply-orders-in-the-graphical-view"></a>Muokkaa ehdotetut toimitustilaukset graafisessa näkymässä  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Nimikkeen saatavuus aikajanalla** ja valitse sitten aiheeseen liittyvä linkki.  

    **Nimikkeen saatavuus aikajanalla** -ikkuna näyttää auetessaan nimikkeen numeron, sijainnin ja variantin valitulla suunnittelurivillä, joka on esitäytetty **Asetukset**-pikavälilehden kenttien mukaisesti. **Aikajana**-pikavälilehdessä näkyy graafinen esitys nimikkeen suunnitellusta varastosta, mukaan lukien suunnitteluehdotuksista.  

2.  Varmista, että  **Sisällytä suunnitteluehdotukset** -kenttä on valittuna.  
3.  Etsi ehdotettu toimitustilaus, jota haluat muokata. Voit määrittää muokattavia osia vihreän ympyrän ja levykuvakeen avulla. Lisätietoja eri symboleista on kohdassa Symbolit ja kuvakkeet Aikajana-pikavälilehdellä.  
4.  Vie osoitin vihreän ympyrän päälle, kunnes se laajenee ja osoitin muuttuu siirtomuotoiseksi (neljä nuolta).  
5.  Pitämällä hiiripainiketta alhaalla vetäessäsi osoitinta ylös tai alas voit muokata määrää. Pitämällä hiiripainiketta alhaalla vetäessäsi osoitinta vasemmalle tai oikealle voit muokata eräpäivää.  
6.  Sen lisäksi että elementtejä voi siirtää vetämällä ja pudottamalla, voit muokata suunnitteluehdotuksia avattavan valikon toiminnoilla. Voit käyttää ehdotetun toimituselementin vihreän ympyrän avattavaa valikko ja valita jonkin seuraavista toiminnoista  

    |Toiminto|Kuvaus|  
    |--------------|---------------------------------------|  
    |**Luo uusi tarjonta**|Luo uuden elementin kohtaan, jossa käytät avattavaa valikkoa, joka vastaa ehdotettua uutta toimitustilausta. Siitä tulee uusi suunnittelutyökirjan rivi, kun valitset **Tallenna muutokset**.<br /><br /> **HUOMAUTUS:** Jos **Vaihtoehdot**-pikavälilehden **Sijaintisuodatus**- tai **Varianttisuodatus**-kenttä on tyhjä tai sillä on useita suodattimen arvoja, luodaan uusi tarjonta, joka tallennetaan myöhemmin suunnittelutyökirjan tai hankintalistalle seuraavien koodien kanssa:<br /><br /> * Jos suodatinkenttä on tyhjä, uusi toimitus luodaan ilman sijainti- tai varianttikoodia.<br /><br /> * Jos määritettäviä suodattimen arvoja on useita, ensimmäisen suodattimen arvolle luodaan uusi toimitus järjestämistavan mukaan.<br /><br /> Jos haluat toisen variantti- tai sijaintikoodin, sinun on muutettava manuaalisesti uuden suunnittelurivin arvoa.|  
    |**Automaattinen tarjonnan muuttaminen**|Optimoi uuden toimituksen, jonka olet luonut kaaviossa varmistamalla, että sen tuloksena on nollavarasto ennen seuraava toimitusta.|  
    |**Poista tarjonta**|Poistaa elementin **Aikajana**-pikavälilehdelä ja poistaa suunnittelurivin, kun valitset **Tallenna muutokset**. Kuvake muuttuu levyksi, jossa on punainen risti, kun tarjonta on poistettu.<br /><br /> **HUOMAUTUS:** Voit poistaa vain toimenpideviestin tyypin tarjonnan **Uusi**. Kun olet valinnut **Tallenna muutokset**, sinun on poistettava manuaalisesti kyseinen suunnittelurivi suunnittelun tai hankinnan työkirjasta.|  

7.  Valitse **Lataa uudelleen** -toiminto, jos haluat palauttaa kaikki muutokset, jotka olet tehnyt **Nimikkeen saatavuus aikajanalla** -ikkunan edellisen avaamisen tai **Lataa uudelleen** -valinnan jälkeen.  
8. Kun elementit sijoitetaan haluamallasi tavalla kaavioon, valitse **Tallenna muutokset** kopioidaksesi muokatun määrän ja päivämäärämuutokset suunnittelu- tai hankintariveille, jotka edustavat graafisia elementtejä.  

Toteuttaaksesi tarjonnan tuotantosuunnitelmien muutokset sinun täytyy seurata suunnittelun tai hankintalistan tuloksena olevia toimenpideviestejä. Lisätietoja on ohjeaiheessa Toteuta toim.pidviesti - Suun.

## <a name="symbols-and-icons-on-the-timeline-fasttab"></a>Symbolit ja kuvakkeet Aikajana-pikavälilehdellä

 |Symboli tai kuvake|Kuvaus|  
 |------------------|---------------------------------------|  
 |Musta risti|Tilaukset (sekä tarjonta että kysyntä).<br /><br /> -   Ei voida muokata.<br />-   Näkyy silloin, kun **Näytä suunniteltu varasto** -kenttä on valittu (oranssi kaavio).|  
 |Punainen ympyrä|Olemassa olevat toimitustilaukset, jotka eivät sisälly suunnitteluehdotuksiin.<br /><br /> -   Ei voida muokata.<br />-   Näkyy silloin, kun **Näytä suunniteltu varasto** -kenttä on valittu (oranssi kaavio).|  
 |Keltainen tähti|Ennustettu kysyntä.<br /><br /> -   Ei voida muokata.<br />-   Näkyy silloin, kun **Tuotantoennusteen nimi** -kentässä on arvo.<br /><br /> Kun sekä **Näytä suunniteltu varasto** että **Sisällytä suunnitteluehdotukset** -kentät on valittu, jokainen keltainen tähti on linkittäytynyt vastapainoksi vastakkaiseen kaavioon. Tämä osoittaa, miten ehdotettu tarjonta vastaa ennustettuun kysyntään.|  
 |Vihreä ympyrä ja kuvake, joka on levyn muotoinen ja jossa on punainen risti|Ehdotettu toimitustilaus, jossa toimenpideviesti *Peruuta*.<br /><br /> -   Ei voida muokata.<br />-   Näkyy silloin, kun **Sisällytä suunnitteluehdotukset** -kenttä on valittu (vihreä kaavio).|  
 |Vihreä ympyrä ja kuvake, joka on levyn muotoinen ja jossa on tähti|Ehdotettu toimitustilaus, jossa toimenpideviesti *Uusi*.<br /><br /> -   Voidaan muokata.<br />-   Näkyy silloin, kun **Sisällytä suunnitteluehdotukset** -kenttä on valittu (vihreä kaavio).|  
 |Vihreä ympyrä ja kuvake, joka on levyn muotoinen ja jossa on yksi tai kaksi nuolta|Toimenpide-ehdotus toimitustilauksille *Aikataul. uud.*, *Muuta määrä* tai *Aikataul. uud. ja muuta määrä*<br /><br /> -   Voidaan muokata.<br />-   Näkyy silloin, kun **Sisällytä suunnitteluehdotukset** -kenttä on valittu (vihreä kaavio).<br /><br /> Nuolet vastaavat suunnitteluehdotuksen suuntaa. Esimerkiksi vasen nuoli yhdessä ylänuolen kanssa ilmaisee *Aikatauluta uud. ja Muuta määrä* -toimenpideviestiä, joka sisältää aikataulutuksen taaksepäin ja määrän lisäyksen.|  

Jos käytät **Aikajana**-pikavälilehden avattavaa valikkoa, seuraavat toiminnot avautuvan tehdyn valinnan perusteella  

 |Toiminto|Kuvaus|  
 |--------------|---------------------------------------|  
 |**Luo uusi tarjonta**|Luo uuden elementin kohtaan, jossa käytät avattavaa valikkoa, joka vastaa ehdotettua uutta toimitustilausta. Siitä tulee uusi suunnittelutyökirjan rivi, kun valitset **Tallenna muutokset** **Käsittely**-välilehdessä.<br /><br /> Kaikki suodatinarvot, jotka on määritelty kentässä **Sijaintisuodatus** tai **Varianttisuodatus** **Asetukset**-välilehdellä, otetaan käyttöön uudessa toimitustilauksessa. **Huomautus:**  Jos suodatinkentät ovat tyhjiä tai niissä on useita suodattimen arvoja, uusi toimitustilaus luodaan seuraavien koodien avulla: <ul><li>Jos suodatinkenttä on tyhjä, uusi tarjonta luodaan ilman sijainti- tai varianttikoodia.</li><li>Jos määritettäviä suodattimen arvoja on useita, uusi toimitus luodaan käyttämällä ensimmäisen suodattimen arvoa lajittelujärjestyksen mukaan.</li></ul> Jos haluat uuteen toimitustilaukseen toisen variantti- tai sijaintikoodin, sinun on muutettava manuaalisesti uuden suunnittelurivin arvoa.|  
 |**Automaattinen tarjonnan muuttaminen**|Optimoi uuden toimituksen, jonka olet luonut kaaviossa varmistamalla, että se luo nollavaraston ennen seuraava toimitusta.|  
 |**Poista tarjonta**|Poistaa elementin **Aikajana**-pikavälilehdeltä ja poistaa suunnittelurivin, kun valitset vaihtoehdon**Tallenna muutokset** **Prosessi**-välilehdellä. Kuvake muuttuu levyksi, jossa on punainen risti, kun tarjonta on poistettu. **Huomautus:** Voit poistaa vain toimenpideviestin tyypin tarjonnan *Uusi*. Kun olet valinnut  **Tallenna muutokset** **Prosessi**-välilehdeltä, sinun on poistettava manuaalisesti kyseinen suunnittelurivi suunnittelun tai hankinnan työkirjasta.|  
 |**Näytä asiakirja**|Avaa tilauksen, suunnittelun rivin tai ennusteen, jota elementt edustaa.|  
 |**Loitonna (Ctrl++)**|Suurentaa x-akselin asteikkoa niin, että vähemmän päiviä on näkyvissä. **Huomautus:** Voit myös tehdä tämän painamalla Ctrl ja vierittämällä hiiren rullaa.|  
 |**Lähennä (Ctrl+-)**|Pienentää x-akselin asteikkoa niin, että enemmän päiviä on näkyvissä. **Huomautus:** Voit myös tehdä tämän painamalla Ctrl ja vierittämällä hiiren rullaa.|  
 |**Palauta zoomaus (Ctrl+0)**|Peruuttaa X-akselin asteikon, jota käytettiin ennen kuin zoomasit.|  

Aiemmin mainittujen näppäimistötoimintojen lisäksi voit käyttää myös **Aikajana**-pikavälilehden seuraavia näppäimistötoimintoja.  

 |Näppäimistötoiminto|Kuvaus|  
 |---------------------|---------------------------------------|  
 |CTRL + vieritä hiiren rullaa|Muuttaa x-akselin asteikkoa.|  
 |Valitse elementti ja paina Vaihto + Nuoli|Siirtää elementtiä nuolen suuntaisesti.|  
 |Sarkain|Siirtää seuraavaan elementtiin.|  
 |Vaihto+Sarkain|Siirtää edelliseen elementtiin.|  
 |Siirrettäessä osaa paina ESC-näppäintä.|Peruuttaa siirron. **Huomautus:**  Ei toimi, jos olet vapauttanut hiiren painikkeen.|

## <a name="see-also"></a>Katso myös  
[Suunnittelu](production-planning.md)   
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md)   
[Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

