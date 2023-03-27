---
title: Nimikeseurannan nimikkeiden jäljittäminen
description: 'Näet, missä nimikeseurannassa olevaa nimikettä on käytetty, mukaan lukien kuinka ja missä se oli vastaanotettu, tuotettu, tai palautettu, käyttäen nimikkeen jäljitys- ja etsi merkintöjä -ominaisuuksia.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '6520,'
ms.date: 06/16/2021
ms.author: edupont
---
# Nimikeseurannan nimikkeiden jäljittäminen

Näet, missä nimikeseurannassa olevaa nimikettä on käytetty, mukaan lukien kuinka ja missä se oli vastaanotettu tai tuotettu, siirretty, myyty, kulutettu tai palautettu. Voit myös etsiä kaikki nykyiset esiintymät tietystä sarja- tai eränumerosta tietokannassa. Voit tehdä tämän käyttämällä nimikkeen jäljitystä ja [Etsi tapahtumat](ui-find-entries.md) -toimintoja.  

Nämä toiminnot ovat erityisen hyödyllisiä laaduntarkkailussa, kun haluat tietää, kuka asiakas vastaanotti tietyllä eränumerolla olevia tuotteita tai mihin erään viallinen komponentti kuuluu.  

 Voit jäljittää **Nimikkeen jäljitys** -sivulla sarja- tai eränumeron järjestyksessä eteenpäin ja taaksepäin kirjatuissa varastotapahtumissa.  

 **Etsi tapahtumat** -sivulla ei näy tapahtumien järjestystä, mutta näet kuitenkin sarja- tai eränumeron kaikki tietueet – sekä kirjatut tapahtumat että avatut tietueet.  

 Kahta ominaisuutta voi käyttää yhdessä siirtämällä jäljitetty sarja- tai eränumero **Etsi tapahtumat** -sivulle viimeistelemään jäljitystilanne. <!-- For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).   -->

## Nimikeseurannan nimikkeiden jäljittäminen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeen jäljitys** ja valitse sitten vastaava linkki.  
2.  Anna sivun yläosan suodatinkenttiin tietyt nimikenumerot tai niiden nimikenumeroiden suodatin, joita haluat jäljittää.  
3.  Valitse **Näytä komponentit** -kentässä, tarkastetaanko myös se, mistä nimikkeiden komponentit ovat lähtöisin. Asetukset kuvaillaan seuraavassa taulukossa.  

    |Kenttä|Kuvaus|  
    |----------------------------------|---------------------------------------|  
    |**Nro**|Älä näytä komponentteja.|  
    |**Vain nimikeseuranta**|Näytä vain komponentit, joilla on erä-tai sarjanumero.|  
    |**Kaikki**|Näytä kaikki komponentit.|  

4.  Valitse **Jäljitysmenetelmä**-kentässä menetelmä, jota käytetään nimikkeen jäljityksessä. Asetukset kuvaillaan seuraavassa taulukossa.  

    |Kenttä|Kuvaus|  
    |----------------------------------|---------------------------------------|  
    |**Käyttö->alkuperä**|Jäljitä nimikettä lähtien siitä paikasta, josta sitä käytettiin, siihen paikkaan, josta se tuli. Jos esimerkiksi valmistettu nimike myytiin asiakkaalle, **Nimikkeen jäljitys** -sivulla näkyvät nämä tiedot niin, että lähtevän toimituksen rivi on ensimmäisenä. Voit laajentaa näkymää, jos haluat nähdä, mistä tuotantotilauksesta se tuli.|  
    |**Alkuperä-> Käyttö**|Jäljitä nimikettä lähtien siitä paikasta, josta se tuli varastoon, siihen paikkaan, jossa sitä käytettiin. Jos esimerkiksi valmistettu nimike myytiin asiakkaalle, **Nimikkeen jäljitys** -sivulla näkyvät nämä tiedot niin, että valmis tuotantotilaus on ensimmäisenä. Voit laajentaa näkymää, jos haluat nähdä ne lähtevän toimituksen rivit, joissa nimikettä käytettiin.|  

5.  Suorita jäljitys valitsemalla **Jäljitys**.  

> [!NOTE]  
>  Näytetään vain kohdistetut tapahtumat. Jos olet vastaanottanut saman erän useissa tapahtumissa, kaikki tapahtumat eivät ehkä näy **Nimikkeen jäljitys** -sivulla.   

> [!NOTE]  
>  Jos jäljitysrivin yläpuolinen rivi on jo jäljittänyt lisätapahtumahistorian, **Jo jäljitetty** -valintaruutu on valittuna. Yksinkertaisemman näkymän tarjoavia alla olevia rivejä ei näytetä.  
>   
>  Etsi kohteen jäljitysrivejä, joissa tapahtumahistoria on jo jäljitetty, ja valitse **Siirry jo jäljitetty** -painike. Nimikkeen jäljitysrivi on valittu, ja kaikki pohjana olevat rivit on laajennettu.  

## Voit etsiä nimikeseurannassa olevia nimikkeitä Etsi tapahtumat -toiminnolla  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Etsi merkintöjä** ja valitse sitten vastaava linkki.  
2. Valitse **Toiminnot** > **Etsi perusteella** > **Nimike viittauksen mukaan**.
3. Anna **Sarjanumero**- ja **Eränro**-kenttiin nimikeseurantanumerot, joita haluat seurata.  
4. Etsi kaikki sarja- tai eränumeron ilmentymät tietokannasta valitsemalla **Etsi**-toiminto.  

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/prepare-item-tracking/)

## Katso myös

[Varasto](inventory-manage-inventory.md)  
[Sarja-, erä- ja pakettinumeroiden käsitteleminen](inventory-how-work-item-tracking.md)  
[Rakennetiedot: Nimikkeen seuranta](design-details-item-tracking.md)  
[Rakennetiedot – nimikkeen seuranta ja varaukset](design-details-item-tracking-and-reservations.md)  
[Nimikkeiden varaaminen](inventory-how-to-reserve-items.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
<!-- [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)   -->
[Etsi tapahtumat](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
