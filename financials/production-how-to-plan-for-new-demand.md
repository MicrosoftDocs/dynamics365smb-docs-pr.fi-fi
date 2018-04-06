---
title: Tilauskohtainen suunnittelu | Microsoft Docs
description: "Tämä suunnittelutehtävä voidaan suorittaa **Tilauksen suunnittelu** -ikkunassa, jossa näkyvät kaikki uusi kysyntä, saatavuustiedot sekä tarjontaa koskevat ehdotukset. Ikkunan tietojen ja työkalujen avulla voidaan suunnitella tehokkaasti myynti- ja komponenttirivien synnyttämä kysyntä sekä luoda erityyppisiä toimitustilauksia suoraan."
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
ms.openlocfilehash: a7266eddba4293807a1e7e2a187c5002be771499
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="plan-for-new-demand-order-by-order"></a>Uuden kysynnän tilauskohtainen suunnittelu
Tämä suunnittelutehtävä voidaan suorittaa **Tilauksen suunnittelu** -ikkunassa, jossa näkyvät kaikki uusi kysyntä, saatavuustiedot sekä tarjontaa koskevat ehdotukset. Ikkunan tietojen ja työkalujen avulla voidaan suunnitella tehokkaasti myynti- ja komponenttirivien synnyttämä kysyntä sekä luoda erityyppisiä toimitustilauksia suoraan.  

Voit siirtyä **Tilauksen suunnittelu** -ikkunaan kahdella tavalla kohdistuksen mukaan: tilauksesta, jonka nimenomaisesti haluat suunnitella, tai erätilasta, koska haluat suunnitella kaikkea uutta kysyntää varten.  


## <a name="to-plan-for-new-production-order-demand"></a>Suunnittele uuden tuotantotilauksen kysyntä  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Suunnitellut tuotantotilaukset** ja valitse sitten aiheeseen liittyvä linkki. (Voit suorittaa nämä suunnitellun, sitovan suunnittelun tai vapautetun tuotantotilauksen vaiheet.)
2.  Avaa suunniteltava tuotantotilaus ja valitse **Suunnittelu**-toiminto.  
3.  Valitse **Tilauksen suunnittelu** -ikkunassa **Laske suunnitelma** -toiminto.  

Ikkunassa näkyvät suunnittelurivit on suodatettu  **Tuotantokysyntä**-suodatuksella – toisin sanoen ikkunassa näkyvät kaikkien tuotantotilausten täyttämätöntä kysyntää sisältävät komponenttirivit. Järjestelmä ei näytä ainoastaan käsiteltävän tuotantotilauksen kysyntää, sillä on riskialtista suunnitella tuotantotilaus ilman käsitystä mahdollisten aikaisempien komponenttirivien kysynnästä. Käsiteltävän tuotantotilauksen suunnittelurivit on laajennettu.  

## <a name="to-plan-for-any-new-demand"></a>Kaiken uuden kysynnän suunnitteleminen  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tilauksen suunnittelu** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Tilauksen suunnittelu** -ikkunassa **Laske suunnitelma** -toiminto.
3.  Napsauta **Kysyntäpvm**-kentän päivämäärän edellä olevaa **Laajenna (+)**-painiketta, niin saat näkyviin kaikki suunnittelurivit, jotka vastaavat täyttämätöntä kysyntää sisältäviä kysyntärivejä.  
4.  Ikkunan alaosassa on tietokenttiä, joissa on kutakin laajennettua suunnitteluriviä (kysyntäriviä) koskevia tietoja:  

    |Asetus|Description|  
    |----------------------------------|---------------------------------------|  
    |**Siirtoon saatavilla**|Näyttää, onko nimikettä muussa sijainnissa. Voit sitten hakea ja valita määrän.|  
    |**Korvaavia olemassa**|Korvaavia olemassa – onko nimikkeelle luotu korvaava nimike. Voit sitten hakea ja valita määrän. Huomaa, että tämä toiminto on mahdollinen vain komponenttien yhteydessä eli kysyntäriveillä, joiden tyyppi on **Tuotanto**.|  
    |**Saatavilla oleva määrä**|Saatavilla oleva määrä – näyttää nimikkeen kokonaissaatavuuden (oletetun saatavilla olevan saldon).|  
    |**Varhaisin mahdollinen päivämäärä**|Tässä kentässä näkyy sen saapuvan toimitustilauksen saapumispäivämäärä, jolla voidaan kattaa tarvittu määrä kysyntäpäivämäärän jälkeen.|  

5.  Valitse **Täydennysjärjestelmä**-kentästä luotavan toimitustilauksen tyyppi.  

    Kentässä on oletusarvona nimikkeen kortin (tai varastointiyksikön kortin) asetus, mutta voit muuttaa sen joksikin seuraavista kolmesta vaihtoehdosta:  

    |Asetus|Description|  
    |----------------------------------|---------------------------------------|  
    |**Osto**|Luo ostotilauksen.|  
    |**Siirto**|Luo siirtotilauksen|  
    |**Tuotantotilaus**|Tuotantotilauksen luominen|  

    **Tarjonta kohteesta** -kentästä on valittava arvo edellä valitun täydennysjärjestelmän mukaisesti.  

    > [!NOTE]  
    >  Jos kenttä jätetään tyhjäksi, järjestelmä antaa virhesanoman **Tee toimitustilaukset** -toimintoa käytettäessä, eikä kyseiselle suunnitteluriville luoda toimitustilausta. Ainoa poikkeus on, jos täydennysjärjestelmäksi valitaan **Tuot.til.**  

6.  Voit etsiä **Tarjonta kohteesta** -kentässä luettelon ja valita kohteen, josta tarjonta tulee:  

    - Jos täydennysjärjestelmä on **Osto**, kentän hakupainike etsii arvon **Nimikkeen toimittajaluettelo** -ikkunasta.  
    - Jos täydennysjärjestelmä on **Siirto**, kentän hakupainike etsii arvon **Sijaintiluettelo**-ikkunasta.  

    Jos nimikettä on toisessa sijainnissa, ikkunan alaosan **Siirtoon saatavilla** -kentässä on arvo. Voit tällöin valita sijainnin, josta nimikettä toimitetaan, kun teet siirtotilauksen.  

    Jos tarvittavalle nimikkeelle on olemassa korvaava nimike, ikkunan alaosan **Korvaavia olemassa** -kentässä lukee **Kyllä** ja korvaava nimike voidaan etsiä ja valita **Nimikekorvaustapahtumat**-ikkunasta.  

7.  Lisää **Varaa**-kenttään valintamerkki, jos haluat tehdä varauksen parhaillaan luotavan toimitustilauksen ja kysynnän luoneen kysyntärivin (myyntirivin tai komponenttirivin) välille. Kenttä on oletusarvoisesti tyhjä.  

    > [!NOTE]  
    >  Valintamerkki voidaan lisätä vain, jos nimikkeen kortin **Varaa**-kentässä on arvo **Valinnainen** tai **Aina**.  

8.  **Tilattava määrä** -kenttään voit antaa määrän, joka siirretään luotavaan toimitustilaukseen.   
    Kentässä on oletusarvona on sama määrä kuin **Tarvittu määrä** -kentässä. Nimikettä voidaan kuitenkin tilata enemmän tai vähemmän sen mukaan, mitä tiedetään yleisestä kysyntätilanteesta. Jos esimerkiksi huomaat **Tilauksen suunnittelu** -ikkunassa, että samalle ostonimikkeelle on useita toisiinsa liittymättömiä kysyntärivejä, jotka ovat erääntymässä samoihin aikoihin, voit yhdistää rivit määrittämällä tarvittavan kokonaismäärän yhden rivin **Tilattava määrä** -kenttään ja poistamalla muut nimikkeen suunnittelurivit.  

9.  **Eräpäivä**- ja **Tilauspvm**-kenttiin voit antaa päivämäärät, joita käytetään luoduissa toimitustilauksissa.  

    Nämä kaksi kenttää liittyvät toisiinsa **Oletustoimitusajan varmistus** -kentän mukaan, joka löytyy **Tuotannon asetukset** -ikkunasta. Oletusarvo on, että eräpäivä on sama kuin kysyntäpäivämäärä, mutta tätä voidaan haluttaessa muuttaa.  

> [!NOTE]  
>   Jos kirjoitat päivämäärän, joka on myöhäisempi kuin kysyntäpäivämäärä, näyttöön tulee varoitussanoma.  

## <a name="to-make-supply-orders"></a>Toimitustilausten tekeminen  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Suunnitellut tuotantotilaukset** ja valitse sitten aiheeseen liittyvä linkki. Voit suorittaa nämä suunnitellun, sitovasti suunnitellun tai vapautetustn tuotantotilauksen vaiheet.  
2.  Avaa suunniteltava tuotantotilaus ja valitse **Suunnittelu**-toiminto.  
3.  Siirrä kohdistin halutulle suunnitteluriville ja valitse sitten **Tee tilaukset** -toiminto.  
4.  Valitse **Tee toimitustilaukset** -ikkunan **Tilauksen suunnittelu** -pikavälilehden **Tee tilaukset** -kentässä jokin seuraavista vaihtoehdoista.  

    |Asetus|Description|  
    |----------------------------------|---------------------------------------|  
    |**Aktiivinen rivi**|Toimitustilaus tehdään vain sille riville, jolla kohdistin on.|  
    |**Aktiivinen tilaus**|Tee toimitustilaukset sen tilauksen kaikille riveille, jossa kohdistin on.|  
    |**Kaikki rivit**|Toimitustilaukset tehdään kaikille **Tilauksen suunnittelu** -ikkunan riveille.|  

5.  Määritä **Vaihtoehdot**-pikavälilehdessä, millaisia toimitustilauksista tai hankintalistan riveistä tehdään.  

    > [!NOTE]  
    >  **Tee toimitustilaukset** -ikkunassa viimeksi tehdyt asetukset tallennetaan käyttäjätietoihin niin, että ne säilyvät samoina ikkunan seuraavaa käyttökertaa varten.  

6.  Valitse **OK**, niin ohjelma luo ehdotetut toimitustilaukset tai hankintalistan rivit.  

Kysyntä on nyt täytetty luomalla sitä vastaavat toimitustilaukset. Työnkulun tarkemmat yksityiskohdat **Tilauksen suunnittelu** -ikkunaa käytettäessä määräytyvät yrityksen sisäisten käytäntöjen mukaan.  

Kun **Tilauksen suunnittelu** -ikkunan suunnitelma on valmis (nimikkeelle on esimerkiksi määritetty vaihtoehtoinen hankintatapa), voidaan siirtyä luomaan toimitustilaukset yhdelle suunnitteluriville tai useille suunnitteluriveille.  

> [!NOTE]  
>  Luodut toimitustilaukset saattavat synnyttää uuden, ei-itsenäisen kysynnän, esimerkiksi osakomponentin tuotantotilaustarpeen. Etsi ja käsittele tällainen kysyntä valitsemalla **Laske suunnitelma** -toiminto uudelleen, ennen kuin siirryt luettelossa eteenpäin.  

## <a name="see-also"></a>Katso myös  
[Suunnittelu](production-planning.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md)   
[Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

