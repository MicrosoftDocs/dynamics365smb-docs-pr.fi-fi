---
title: Rakennetiedot – saatavuus fyysisessä varastossa
description: 'Tietoja eri tekijöistä, jotka vaikuttavat nimikkeen saatavuuteen fyysisessä varastossa.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
---
# Rakennetiedot: saatavuus varastossa

Kun nimikkeen saatavuus on jatkuvasti tiedossa, voidaan varmistaa, että lähtevä tilausvirta on tehokas ja että toimitusajat ovat optimaaliset.  

Saatavuus voi vaihdella useiden tekijöiden vuoksi. Esimerkki:

* Kohdistukset varastopaikkatasolla fyysisen varaston toimintojen, kuten poimintojen ja varastosiirtojen, yhteydessä.
* Varaston varausjärjestelmä edellyttää rajoitusten noudattamista.

[!INCLUDE [prod_short](includes/prod_short.md)] tarkistaa ennen määrien kohdistamista lähtevien virtojen poimintoihin, että kaikki ehdot täyttyvät.

Jos ehdot eivät täyty, näkyviin tulee virhesanomia. Yksin tavallinen sanoma on yleinen Ei mitään käsiteltävää. viesti. Sanoma voidaan näyttää erilaisissa lähtevien ja saapuvien virtojen yhteyksissä, joissa asiakirjarivillä on **Käsiteltävä määrä** -kenttä.

## Varastopaikan sisältö ja varaukset  

Nimikemäärät ilmaistaan sekä fyysisen varaston tapahtumina että varaston nimiketapahtumina. Nämä kaksi tapahtumatyyppiä sisältävät erilaisia tietoja nimikkeiden sijainnista ja niiden saatavuudesta. Fyysisen varastoinnin tapahtumat määrittävät nimikkeen saatavuuden varastopaikan ja varastopaikan tyypin mukaan. Jälkimmäistä kutsutaan myös varastopaikan sisällöksi. Nimiketapahtumat määrittävät nimikkeen saatavuuden lähtevien asiakirjojen varauksen perusteella.  

[!INCLUDE [prod_short](includes/prod_short.md)] laskee poimintaan saatavissa olevan määrän, kun varastopaikan sisältö ja varaukset on yhdistetty.  

## Saatavilla oleva poimintamäärä  

[!INCLUDE [prod_short](includes/prod_short.md)] varaa nimikkeitä odottaviin myyntitilaustoimitukseen, jolloin niitä ei poimita muihin aiemmin toimitettaviin myyntitilauksiin. [!INCLUDE [prod_short](includes/prod_short.md)] vähentää jo käsiteltävien nimikkeiden määrän seuraavasti:

* Muihin lähtevien asiakirjoihin varatut määrät.
* Aiemmin luotujen poiminta-asiakirjojen määrät.
* Poimitut määrät, joita ei ole vielä toimitettu tai kulutettu.  

Tulos lasketaan dynaamisesti ja näytetään **Poimintatyökirja**-sivun **Saatav. ol. määrä poimittav.** -kentässä. Arvo lasketaan myös silloin, kun käyttäjä luo fyysisen varastoinnin poiminnat suoraan lähteville asiakirjoille. Esimerkkejä lähtevien asiakirjoista:

* Myyntitilaukset
* Tuotannon kulutus
* Lähtevät siirrot

Tulos on käytettävissä näiden asiakirjojen määräkentissä, kuten **Käsiteltävä määrä** -kentässä.  

> [!NOTE]  
> Varausten prioriteettiin liittyen varattava määrä vähennetään poimittavissa olevasta määrästä. Jos esimerkiksi poiminnan varastopaikassa saatavana oleva määrä on 5 yksikköä, mutta hyllytyksen varastopaikassa on 100 yksikköä ja toiseen tilaukseen yritetään varata enemmän kuin 5 yksikköä, näkyviin tulee virhesanoma, koska lisämäärä on oltava saatavana poiminnan varastopaikoissa.  

### Poimittavissa olevan määrän laskeminen  

[!INCLUDE [prod_short](includes/prod_short.md)] laskee poimittavissa olevan määrän seuraavasti:  

poimittavissa olevaa määrää = määrä poimintavarastopaikoissa - määrä poiminnoissa ja siirroissa- – (varattu määrä poimintavarastopaikoissa + varattu määrä poiminnoissa ja siirroissa-)  

Seuraava kaavio sisältää laskelman eri elementit.  

![Käytettävissä poimintaan, kun varaus on päällekkäinen.](media/design_details_warehouse_management_availability_2.png "Käytettävissä poimintaan, kun varaus on päällekkäinen")  

## Varattavissa oleva määrä

Koska sekä varastopaikan sisältö että varaus on luotu jo aiemmin, varattavissa olevien nimikkeiden määrä on kohdistettava fyysisen varastoinnin lähtevien asiakirjoihin.  

Kaikki muut varastonimikkeet voidaan varata paitsi nimikkeet, joiden lähtevä käsittely on alkanut. Varattavissa oleva määrä määritetään kaikissa asiakirjoissa ja varastopaikkatyypeissä olevana määränä. Seuraavat lähtevien määrät ovat poikkeuksia:  

* Määrä rekisteröimättömissä poiminta-asiakirjoissa  
* Varastopaikoissa oleva määrä  
* Määrä tuotannon valmisteluvarastopaikoissa  
* Määrä avoimissa tuotannon varastopaikoissa  
* Määrä kokoonpanon valmisteluvarastopaikoissa  
* Muutosvarastopaikoissa oleva määrä  

Tulos näkyy **Saatavilla oleva kokonaismäärä** -kenttään **Varaus**-sivulla.  

Varausrivillä oleva määrä, jota ei voi varata, koska se on kohdistettu fyysisessä varastossa, näytetään **Varaus**-sivun **F.var. kohdistettu määrä** -kentässä.  

### Varattavissa olevaan määrän laskeminen

[!INCLUDE [prod_short](includes/prod_short.md)] laskee varattavissa olevan määrän seuraavasti:  

varattavissa oleva määrää = kokonaismäärä varastossa - määrä poiminnoissa ja siirroissa lähdeasiakirjoille - varattu määrä - määrä lähtevien varastopaikoissa  

Seuraava kaavio sisältää laskelman eri elementit.  

![Varattavissa varaston kohdistusta kohden.](media/design_details_warehouse_management_availability_3.png "Varattavissa varaston kohdistusta kohden")  

## Katso myös  

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]