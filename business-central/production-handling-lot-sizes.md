---
title: Eräkokojen käsitteleminen
description: Tässä ohje aiheessa kuvataan eri tapoja käsitellä eräkokoja.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="handling-lot-sizes-in-production"></a><a name="handling-lot-sizes-in-production"></a>Eräkokojen käsitteleminen tuotannossa
Määrän osalta tuotantotoiminnossa tuotettujen nimikkeiden määrä ei välttämättä korreloi niiden myynnin kanssa. Voit esimerkiksi tuottaa satoja nimikkeitä yksittäisessä erässä, mutta myydä jokaisen nimikkeen yksittäin. Kun tuotantoreitit ja tuoterakenteet määritetään, on olemassa muutamia asioita, joita kannattaa miettiä eräkokojen osalta. Tässä ohjeaiheessa kuvataan, miten eräkoot vaikuttavat kustannusten laskentaan ja resurssien suunnitteluun.

## <a name="units-of-measure-in-production-bill-of-materials"></a><a name="units-of-measure-in-production-bill-of-materials"></a>Mittayksiköt tuotannon tuoterakenteessa
Vaikka nimikkeelle määritetään perusmittayksikkö, tuoterakenne voi käyttää valmiissa tuotteessa eri perusmittayksikköä. Esimerkiksi nimikkeen perusmittayksikkö voi olla "kappaletta", mutta tuoterakenne voi edellyttää kuormalavaa tai tonnia. Tämä on kätevää, kun koneet tai raakakomponentit määräävät määrän. Et esimerkiksi todennäköisesti halua leipoa yhtä muffinssia, koska on vaikea käyttää vain osaa kananmunasta. Sen sijaan leivot erän muffinsseja vähentääksesi hukkaa. Lisätietoja on kohdassa [Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md).

## <a name="lot-size-on-routing-lines"></a><a name="lot-size-on-routing-lines"></a>Erän koko reititysriveillä
Reitityksen näkökulmasta voit määrittää eräkoon reititysriveille, jotta ne vastaisivat nimikkeitä tuottavien koneiden kapasiteettia. Reititysivien suoritusaika vähenee suhteessa eräkokoon. 

Tämä toimii hyvin, kun tuotantotilauksen määrä on reitityksen eräkoon kerroin. Jos esimerkiksi leivinarkille mahtuu 10 muffinssia, sinun on leivottava 10, 20, 30 jne. kappaletta, ei 5 tai 15 kappaletta.  Tämä on paljon pienempi ongelma, jos käsittelet suuria määriä.

Eräkoko on suosittu myös tuotantoympäristöissä, joissa tuotos mitataan määränä, jonka voi tehdä tietyn ajanjakson aikana. Esimerkiksi, jos tuotettu tilavuus 9 tunnin työvuoron aikana on 700 kuutiometriä, voit asettaa suoritusajaksi 9 tuntia ja eräkooksi 700.
Tuotantotilauksen määrästä tulee vähemmän tärkeä, kun tuotantotilauksessa suoritusaika lasketaan suoritusaikana jaettuna eräkoolla saadaksesi kappalekohtaisen suoritusajan.
 
> [!NOTE]
> Eränkoko-kentässä määritetyllä arvolla ei ole vaikutusta reititysrivin **Määritysaika** -kentässä määritettyyn aikaan. Määritys tehdään vain kerran, vaikka eriä olisi useita. Esimerkiksi niin, että sinun ei tarvitse lämmittää uunia paistaaksesi toisen erän muffinsseja. Lisätietoja on kohdassa [Reititysten luominen](production-how-to-create-routings.md).

## <a name="lot-sizes-for-items-and-stockkeeping-units"></a><a name="lot-sizes-for-items-and-stockkeeping-units"></a>Nimikkeiden ja varastointiyksiköiden eräkoot
Reitityksille määritetyt eräkoot eivät ole samat kuin nimikkeiden tai varastointiyksiköiden eräkoot. Näitä arvoja käytetään eri tarkoitukseen, eivätkä ne vaikuta tuotantokapasiteettiin. 

## <a name="lot-size-on-item-and-stockkeeping-units"></a><a name="lot-size-on-item-and-stockkeeping-units"></a>Nimikkeiden ja varastointiyksiköiden eräkoko
Nimikkeille ja varastointiyksiköille eräkoilla on seuraavat vaikutukset kustannusten laskentaan ja toimitusten suunnitteluun:

* Jos otat vakiokustannuksen laskennassa käyttöön **Kust. sisältävät asetuksen** -asetuksen **Tuotannon asetukset** -sivulla, asetuksen kustannus lisätään vakiokustannuksiin. Jos määrität eräkoon, reititystoiminnon asetuskustannukset pienenevät eräkoon kasvaessa. Jos esimerkiksi eräkooksi on määritelty nimikeortissa on 10, ja uunin lämmittäminen kestää 15 minuuttia, energiakustannukset kohdistetaan 10 muffinssille noin 1,5 minuuttina. 

> [!NOTE]
> Asetuskustannukset käsitellään eri tavalla kuin vakiokustannuksen ja kapasiteetin kohdistuksen näkökulmasta. Jos tuotettu määrä ei vastaa nimikekortissa määritettyä eräkokoa, tämä johtaajoka variaatioon. Lisätietoja on kohdassa [Varaston kustannusten hallinta](finance-manage-inventory-costs.md). <!--not sure that I got this part right seems to repeat the first example.-->

Toimitusten suunnittelulle nimikkeiden eräkoon asetus toimii **Tuotannon asetukset** -sivun **Oletuspuskuri-%** -määrityksen kanssa. [!INCLUDE[prod_short](includes/prod_short.md)] ohittaa kysynnän muutokset, jotka ovat puskuriprosentin alapuolella eikä luo suunnitteluehdotuksia. Jos Oletuspuskuri-% -kentässä on määritetty 15, ja meillä on 20 muffinssin tuotantotilaus 20 vieraalle, mutta yksi vieras ei voi osallistua. [!INCLUDE[prod_short](includes/prod_short.md)] ohittaa yksittäisen puuttuvan vieraan, koska se on vain 10 % erän nimikkeelle määritetystä eräkoosta 10. Jos kuitenkin kaksi vierasta pääse paikalle, [!INCLUDE[prod_short](includes/prod_short.md)] ehdottaa, että tilausmäärää pienennetään, koska kaksi muffinssia on 20 % eräkoosta. Lisätietoja suunnittelusta on kohdassa [Suunnittelu](production-planning.md).

## <a name="see-also"></a><a name="see-also"></a>Katso myös
[Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md)  
[Tuotantoerän mittayksiköiden käyttäminen](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)
[Reititysten luonti](production-how-to-create-routings.md)  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
