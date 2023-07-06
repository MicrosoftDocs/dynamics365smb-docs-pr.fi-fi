---
title: Varastonimikkeiden myyminen kokoonpano tilausta varten -työnkuluissa
description: Tilausta varten kokoonpantavat nimikkeet kokoonpannaan myyntitilauksiin kokoonpanotilauksen avulla.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="selling-inventory-items-in-assemble-to-order-flows"></a><a name="selling-inventory-items-in-assemble-to-order-flows"></a><a name="selling-inventory-items-in-assemble-to-order-flows"></a>Varastonimikkeiden myyminen kokoonpano tilausta varten -virroissa

Jos kokoonpanon nimikkeen kortin **Kokoonpanokäytäntö**-kenttä sisältää **Kokoonpano tilausta varten** -kohdan, myyntitilausprosessi olettaa, että nimikettä ei ole varastossa vaan se on kokoonpantava myyntitilauksia varten. Kun nimike lisätään myyntitilauksen riville, [!INCLUDE [prod_short](includes/prod_short.md)] luo myyntitilaukseen linkitetyn kokoonpanotilauksen. Lisätietoja tilausta varten kokoonpantavien nimikkeiden myynnistä on kohdassa [Tilausta varten kokoonpantujen nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md). Jos osa myyntitilauksen määrästä on kuitenkin jo saatavana varastossa, kokoonpanotilauksen määrää voidaan pienentää muuttamalla myyntitilausrivin **Kokoonpantava määrä tilausta varten** -kentän arvoa.  

On melko harvinaista, että yritykset myyvät varastonimikkeitä tilausta varten kokoonpantavina nimikkeinä. Tilausta varten kokoonpantavat nimikkeet eivät yleensä ole vakionimikkeitä. Sen sijaan nimikkeet mukautetaan asiakkaiden tarpeita vastaaviksi. Varastossa voi kuitenkin olla tilausta varten kokoonpantavia nimikkeitä palautusten tai peruutettujen tilausten vuoksi. Nämä määrät on poimittava ja myytävä, ennen kuin uusia kokoonpannaan.  

> [!NOTE]  
> Myyntitilauksen **Myyntirivin tiedot** -tietoruudun avulla voidaan tarkistaa, onko kokoonpanotilauksiin jo saatavana tilausta varten kokoonpantavia nimikkeitä.  

Vastaavasti voidaan toimia, kun kokoonpanon nimikkeitä myydään varastosta ja osittainen tai koko määrä ei ole saatavana. Puuttuva määrä toimitetaan kokoonpanotilauksen avulla. Lisätietoja varaston ja kokoonpanon nimikkeiden myymisestä on kohdassa [Tilausta varten kokoonpantavien nimikkeiden ja varastonimikkeiden myyminen yhdessä](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
> Tietyt säännöt koskevat **Toimitettava määrä** -kenttää myyntitilauksen riveillä, jotka sisältävät tilausta varten kokoonpantavien määrien ja varastomäärien yhdistelmiä. Lisätietoja säännöistä on kohdassa [Yhdistelmäskenaariot](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

Tässä toimenpiteessä korvaat tilausta varten kokoonpantavat määrät myyntitilauksen rivin varastomäärillä. Yleiskatsaus saadaan seuraavasti:

1. Saatavuuden määrittäminen.
2. Määrän vähentäminen linkitetystä kokoonpanotilauksesta.
3. Varastomäärän varaaminen varmistaa, että se poimitaan ja toimitetaan tilaukseen.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a><a name="to-sell-inventory-items-in-assemble-to-order-flows"></a><a name="to-sell-inventory-items-in-assemble-to-order-flows"></a>Myy varastonimikkeidtä kokoonpano tilausta varten -virroissa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Luo myyntitilaus. Lisätietoja myyntitilausten luonnista on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).  
3. Syötä arvo tilausta varten kokoonpantavan nimikkeen sisältävän myyntitilausrivin **Määrä**-kenttään.  
4. Määritä **Myyntirivin tiedot** -tietoruudussa, onko koko määrä tai osa määrästä saatavana.  
5. Vähennä **Kokoonpantava määrä tilausta varten** -kentässä saatavilla olevaa määrää niin, että ei saatavilla oleva määrä kootaan tilaukseen. **Varattu määrä** -kenttä väheni vastaamaan sitä, että tilauksesta-tilaukseen -linkki tai varaus koskee vain koottavaa määrää.  
6. Valitse **Rivit**-pikavälilehdessä ensin **Toiminnot** ja sitten **Varaa**-toiminto.  
7. Valitse **Varaus**-sivulla nimiketapahtumarivit, joilla saatavilla olevat määrät ovat. Valitse sitten **Varaa nykyiseltä riviltä** -toiminto ja lopuksi **OK**.  

    **Myyntitilaus**-sivun **Varausmäärä**-kentässä näkyy nyt, että tilausrivin koko määrä on varattu. **Kokoonpantava määrä tilausta varten** -kentässä näkyy edelleen kokoonpantava määrä.  

8. Vapauta myyntitilaus mahdollistamaan nimikkeiden poiminta ja ei saatavana olevien nimikkeiden kokoonpano. Lisätietoja nimikkeiden kokoonpanemista kohdassa [Nimikkeiden kokoaminen](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Myyntitilauksen **Varastopaikkakoodi**-kentässä saattaa olla sijaintikortin **Kokoonpanot. toim. var.p.koodi**- tai **Kokoonpanosta-varastop.koodi** -kentän arvo. Siinä tapauksessa myyntitilauksen rivin **Varastopaikkakoodi** saattaa olla virheellinen tämän tilausten varten kokoonpantavien ja varastoon kokoonpantavien määrien yhdistelmässä. Kannattaakin varmistaa uudelleen **Varastopaikkakoodi**-kentässä oleva varastopaikka sopii kaikille määrille. Voit myös kirjoittaa kaksi eri määrää myyntitilauksen eri riveille.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/assemble-to-order-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Nimikkeiden varaaminen](inventory-how-to-reserve-items.md)  
[Kokoonpanon tuoterakenteiden käyttäminen](assembly-how-work-assembly-boms.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastonhallinnan yleiskatsaus](design-details-warehouse-management.md)
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
