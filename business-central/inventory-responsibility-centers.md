---
title: 'Toimintaohje: Vastuupaikkojen käyttäminen'
description: Vastuupaikat hallintokeskuksina auttavat yrityksiä määrittämällä käyttäjäkohtaiset näkymät myynti- ja ostoasiakirjoista, jotka liittyvät yksinomaan tiettyyn vastuukeskukseen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 5714, 5715
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: e966e5050cf16ce60e07983f129be318706fbbf3
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059332"
---
# <a name="work-with-responsibility-centers"></a>Vastuupaikkojen käyttäminen

Vastuupaikat mahdollistavat hallintakeskusten käsittelemisen. Vastuupaikka voi olla kustannuspaikka, kannattavuuspaikka, sijoituspaikka tai muu yrityksen määrittämä hallintapaikka. Vastuupaikkoja ovat esimerkiksi myyntitoimistot, usean sijainnin osto-osastot sekä tehtaan suunnittelutoimistot. Tällä toiminolla yritykset voivat esimerkiksi määrittää käyttäjäkohtaiset näkymät ainoastaan tiettyyn vastuupaikkaan liittyville osto- ja myyntiasiakirjoille.  

Useiden sijaintien käyttäminen yhdessä vastuupaikan kanssa mahdollistaa yritystoimintojaan hallinnan joustavasti ja optimaalisesti.

Kun käytössä on useita sijainteja, yritykset voivat hallita varastoa useista sijanneista yhtä tietokantaa käyttäen. Tämän rakeen kaksi tärkeintä konseptia ovat sijainnit ja varastointiyksiköt. Sijainti on paikka, joka käsittelee nimikkeiden fyysistä sijoittelua ja määriä. Tähän konseptiin sisältyvät niin tehtaat ja tuotantolaitokset kuin jakelukeskukset, fyysiset varastoinnit, näyttelytilat ja huoltoajoneuvot. Varastointiyksikkö on tietyssä sijainnissa oleva nimike ja/tai variantti. Varastointiyksiköiden avulla useissa paikoissa toimivat yritykset voivat lisätä täydennystietoja, osoitteita ja taloudellisia kirjaustietoja sijaintitasolla. Näin ollen yritykset voivat täydentää saman nimikkeen variantteja kussakin sijainnissa sekä tilata nimikkeitä kuhunkin sijaintiin sijaintikohtaisten täydennystietojen perusteella.  

## <a name="to-set-up-a-responsibility-center"></a>Vastuupaikkojen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vastuupaikat** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Jos käytät vastuupaikkoja yrityksesi hallinnoimisessa, voi olla hyödyllistä määrittää yrityksen vastuupaikalle oletusarvo.
4. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yrityksen tiedot** ja valitse sitten vastaava linkki.
5. Anna vastuupaikan koodi **Vastuupaikka**-kentässä.

Tätä koodia käytetään kaikissa osto-, myynti- ja huoltoasiakirjoissa, jos käyttäjällä, asiakkaalla tai toimittajalla ei ole oletusvastuupaikkaa. Voit antaa kaikissa myynti-, osto- tai huoltoasiakirjassa jonkin muun kuin oletusvastuupaikan.

> [!NOTE]  
> Kun syötät asiakirjaan vastuupaikan koodin, se vaikuttaa asiakirjan osoitteeseen, dimensioihin ja hintoihin.  

## <a name="to-assign-responsibility-centers-to-users"></a>Vastuupaikkojen liittäminen käyttäjiin

Voit määrittää käyttäjät siten, että käyttäjien päivittäisissä työtehtävissä sovellus hakee vain kyseiseen aihealueeseen liittyvät asiakirjat. Käyttäjät on yleensä liitetty yhteen vastuupaikkaan, ja he työskentelevät vain sen vastuupaikan tiettyihin sovellusalueisiin liittyvien asiakirjojen parissa.  

Määritä tämä määrittämällä vastuupaikat käyttäjille kolmella toiminta-alueella: ostoissa, myynnissä ja huoltohallinnossa.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän määritys** ja valitse sitten vastaava linkki.  
2. Valitse **Käyttäjäasetukset**-sivulla se käyttäjä, johon haluat liittää vastuupaikan. Jos käyttäjä ei ole luettelossa, sinun täytyy syöttää käyttäjätunnus **Käyttäjätunnus**-kenttään.  
3. Anna **Myynnin vastuupaikan suodatus** -kentässä vastuupaikka, jossa käyttäjällä on myynteihin liittyviä tehtäviä.  
4. Anna **Ostovastuupaikan suodatus** -kentässä vastuupaikka, jossa käyttäjällä on ostoihin liittyviä tehtäviä.  
5. Anna **Huollon vastuupaikan suodatus** -kentässä vastuupaikka, jossa käyttäjällä on huoltohallintoon liittyviä tehtäviä.  

> [!NOTE]  
> Käyttäjät voivat tarkastella vain omaan vastuukeskukseensa liittyviä kirjattuja asiakirjoja. He voivat kuitenkin tarkastella kaikkia kirjapintotapahtuma ja siirtyä muihin kirjattuihin asiakirjoihin kirjanpitotapahtumista.

## <a name="see-also"></a>Katso myös

[Varaston määrittäminen](inventory-setup-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]