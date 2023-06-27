---
title: Kokoonpanon hallinta
description: Tietoja tuotteiden tarjoamisesta asiakkaille yhdistämällä komponentteja yksinkertaisin prosessein ilman tuotantotoimintoja.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="assembly-management" />Kokoonpanon hallinta

Yritykset voivat tarjota tuotteita asiakkaille yhdistämällä komponentteja ilman tuotantotoimintoja. Nimikkeiden kokoamistoiminnot integroituvat liittyviin toimintoihin, kuten myyntiin, suunnitteluun, varauksiin ja varastointiin:  

Kokoonpanon nimike on kokoonpanon tuoterakenteen sisältävä myytävä nimike. Lisätietoja kokoonpanon tuoterakenteesta on kohdassa [Kokoonpanon tuoterakenteiden käsitteleminen](assembly-how-work-assembly-boms.md).

Kokoonpanotilaukset ovat tuotantotilausten tavoin sisäisiä tilauksia. Kokoonpanotilausten avulla voidaan hallita kokoonpanoprosessia sekä yhdistää myynnin tarpeet ja fyysisen varaston toiminnot. Kokoonpanotilaukset koskevat sekä tulosta että kulutusta kirjattaessa. Kokoonpanotilauksen ylätunnistetiedot muistuttavat tuotospäiväkirjan rivejä. Kokoonpanotilauksen rivit muistuttavat kulutuspäiväkirjan rivejä.  

JIT-varastostrategia on käytettävissä, ja tuotteet voidaan mukauttaa asiakkaan tarpeita vastaaviksi. Kokoonpanotilaukset voidaan luodaan automaattisesti ja linkittää, kun myyntitilauksen rivi luodaan. Myynnin kysynnän ja kokoonpanon tarjonnan välinen linkki avaa useita mahdollisuuksia myyntitilausten käsittelyssä:

* Kokoonpanon nimikkeiden mukauttaminen lennossa.
* Toimituspäivämäärien lupaaminen komponentin saatavuuden perusteella.
* Kootun nimikkeen tuotoksen ja toimituksen kirjaaminen suoraan myyntitilauksista.

Lisätietoja kokoonpanon nimikkeiden myynnistä on kohdassa [Tilauksen mukaan koottujen nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).  

Myyntilausten riveillä voi olla varastosta poimittavia nimikkeitä ja tilausta varten koottavia nimikkeitä. Tilausta varten koottavien määrä priorisoidaan varastomäärien ohi osittaisessa toimituksessa. Lisätietoja varaston ja kokoonpanon nimikkeiden myynnistä on kohdassa [Yhdistelmäskenaariot](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

Kun tilausta varteen koottu määrä valmis toimitettavaksi, varastotyöntekijä vo kirjata myyntitilauksen rivien varaston poiminnan. Varaston poiminnan kirjaamisella on seuraavat vaikutukset:

* Komponenteille luodaan varastosiirto
* Kokoonpanon tuotoksen kirjaaminen ja myyntitilauksen toimitus.

Lisätietoja tilausta varten koottavista nimikkeistä ja varaston poiminnoista on kohdassa [Varaston poimintoja sisältävien tilausta varten koottavien nimikkeiden käsitteleminen](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Tietoja nimikkeiden kokoamisesta myyntilauksia ja varastointia varten.|[Tietoja Kokoonpano tilausta varten- ja Kokoonpano varastoon -toiminnoista](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Sijaintikorttien ja varastomääritysten avulla voidaan määrittää, miten nimikkeet virtaavat kokoonpanoon ja sieltä pois.|[Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Mukautetusta kokoonpanon nimikkeestä tehdään tarjous, joka sitten muunnetaan myynniksi, kun asiakas hyväksyy sen.|[Kokoonpano tilausta varten -myynnin tarjous](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Komponentit yhdistämällä luodaan nimike tilaukseen tai varastoon.|[Kokoa nimikkeet](assembly-how-to-assemble-items.md)|  
|Sellaiset kokoonpanon nimikkeet, jotka eivät ole tällä hetkellä saatavana, myydään luomalla linkitetty kokoonpanotilaus toimittamaan myyntilauksen koko määrä tai sen osa.|[Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md)|
|Kun tilausta varten kootut nimikkeet ovat jo varastossa, määrä vähennetään kokoonpanotilauksesta ja se varataan varastosta.|[Varastonimikkeiden myyminen kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Jos kokoonpanon nimikkeet eivät ole varastossa, osa määrästä tai koko määrä voidaan toimittaa kokoonpanotilauksen avulla.|[Kokoonpano tilausta varten -nimikkeiden ja varastonimikkeiden myyminen yhdessä](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Puitemyyntitilauksille voidaan tehdä mukautettuja kokoonpanon nimikkeitä ennen myyntitilausten luontia.|[Puitekokoonpanotilausten luominen](assembly-how-to-create-blanket-assembly-orders.md)|
|Kirjattu kokoonpanotilaus voidaan kumota esimerkiksi siksi, että kirjatussa tilauksessa on virheitä.|[Kokoonpanon kirjauksen kumoaminen](assembly-how-to-undo-assembly-posting.md)|
|Tietoja kokoonpanon tuoterakenteiden käyttämisestä ja niiden eroista tuotannon tuoterakenteisiin.|[Kokoonpanon tuoterakenteiden käyttäminen](assembly-how-work-assembly-boms.md)|
|Tietoja kokoonpanon kulutuksen ja tuotoksen kirjaamisesta ja tavasta, jolla [!INCLUDE [prod_short](includes/prod_short.md)] jakaa nimike- ja resurssikustannukset kirjanpitoon.|[Rakennetiedot: Kokoonpanotilauksen kirjaus](design-details-assembly-order-posting.md)|  

## <a name="see-related-microsoft-training" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Rakennetiedot: toimitusten suunnittelu](design-details-supply-planning.md)  
<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
<!-- [Walkthrough: Selling, Assembling, and Shipping Kits](walkthrough-selling-assembling-and-shipping-kits.md)   -->
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
