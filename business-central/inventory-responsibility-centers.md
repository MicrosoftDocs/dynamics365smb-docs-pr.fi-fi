---
title: "Vastuupaikkojen käyttäminen | Microsoft Docs"
description: "Vastuupaikat mahdollistavat hallintakeskusten käsittelemisen. Vastuupaikka voi olla kustannuspaikka, kannattavuuspaikka, sijoituspaikka tai muu yrityksen määrittämä hallintapaikka."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7b8d12d597930824aba96cc894b11419f9ae00b0
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="work-with-responsibility-centers"></a>Vastuupaikkojen käyttäminen
Vastuupaikat mahdollistavat hallintakeskusten käsittelemisen. Vastuupaikka voi olla kustannuspaikka, kannattavuuspaikka, sijoituspaikka tai muu yrityksen määrittämä hallintapaikka. Vastuupaikkoja ovat esimerkiksi myyntitoimistot, usean sijainnin osto-osastot sekä tehtaan suunnittelutoimistot. Tällä toiminolla yritykset voivat esimerkiksi määrittää käyttäjäkohtaiset näkymät ainoastaan tiettyyn vastuupaikkaan liittyville osto- ja myyntiasiakirjoille.  

Useiden sijaintien käyttäminen yhdessä vastuupaikan kanssa mahdollistaa yritystoimintojaan hallinnan joustavasti ja optimaalisesti.

Kun käytössä on useita sijainteja, yritykset voivat hallita varastoa useista sijanneista yhtä tietokantaa käyttäen. Tämän rakeen kaksi tärkeintä konseptia ovat sijainnit ja varastointiyksiköt. Sijainti on paikka, joka käsittelee nimikkeiden fyysistä sijoittelua ja määriä. Tähän konseptiin sisältyvät niin tehtaat ja tuotantolaitokset kuin jakelukeskukset, fyysiset varastoinnit, näyttelytilat ja huoltoajoneuvot. Varastointiyksikkö on tietyssä sijainnissa oleva nimike ja/tai variantti. Varastointiyksiköiden avulla useissa paikoissa toimivat yritykset voivat lisätä täydennystietoja, osoitteita ja taloudellisia kirjaustietoja sijaintitasolla. Näin ollen yritykset voivat täydentää saman nimikkeen variantteja kussakin sijainnissa sekä tilata nimikkeitä kuhunkin sijaintiin sijaintikohtaisten täydennystietojen perusteella.  

Vastuupaikat lisäävät usean sijainnin toiminnon käyttömahdollisuuksia, sillä niiden avulla käyttäjät voivat käsitellä hallintapaikkoja. Vastuupaikka voi olla kustannuspaikka, kannattavuuspaikka, sijoituspaikka tai muu yrityksen määrittämä hallintapaikka. Vastuupaikkoja ovat esimerkiksi myyntitoimistot, usean sijainnin osto-osastot sekä tehtaan suunnittelutoimistot. Tällä toiminolla yritykset voivat esimerkiksi määrittää käyttäjäkohtaiset näkymät ainoastaan tiettyyn vastuupaikkaan liittyville osto- ja myyntiasiakirjoille.

## <a name="to-set-up-a-responsibility-center"></a>Vastuupaikkojen luominen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vastuupaikat** ja valitse sitten liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Jos käytät vastuupaikkoja yrityksesi hallinnoimisessa, voi olla hyödyllistä määrittää yrityksen vastuupaikalle oletusarvo.
4. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yrityksen tiedot** ja valitse sitten liittyvä linkki.
5. Anna vastuupaikan koodi **Vastuupaikka**-kentässä.

Tätä koodia käytetään kaikissa osto-, myynti- ja huoltoasiakirjoissa, jos käyttäjällä, asiakkaalla tai toimittajalla ei ole oletusvastuupaikkaa. Voit antaa kaikissa myynti-, osto- tai huoltoasiakirjassa jonkin muun kuin oletusvastuupaikan.

> [!NOTE]  
>  Kun syötät asiakirjaan vastuupaikan koodin, se vaikuttaa asiakirjan osoitteeseen, dimensioihin ja hintoihin.  

## <a name="to-assign-responsibility-centers-to-users"></a>Vastuupaikkojen liittäminen käyttäjiin  
Voit määrittää käyttäjät siten, että käyttäjien päivittäisissä työtehtävissä ohjelma hakee vain kyseiseen aihealueeseen liittyvät asiakirjat. Käyttäjät on yleensä liitetty yhteen vastuupaikkaan, ja he työskentelevät vain sen vastuupaikan tiettyihin sovellusalueisiin liittyvien asiakirjojen parissa.  

Määritä tämä määrittämällä vastuupaikat käyttäjille kolmella toiminta-alueella: ostoissa, myynnissä ja huoltohallinnossa.  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjäasetukset** ja valitse sitten liittyvä linkki.  
2.  Valitse **Käyttäjäasetukset**-ikkunassa se käyttäjä, johon haluat liittää vastuupaikan. Jos käyttäjä ei ole luettelossa, sinun täytyy syöttää käyttäjätunnus **Käyttäjätunnus**-kenttään.  
3.  Anna **Myynnin vastuupaikan suodatus** -kentässä vastuupaikka, jossa käyttäjällä on myynteihin liittyviä tehtäviä.  
4.  Anna **Ostovastuupaikan suodatus** -kentässä vastuupaikka, jossa käyttäjällä on ostoihin liittyviä tehtäviä.  
5.  Anna **Huollon vastuupaikan suodatus** -kentässä vastuupaikka, jossa käyttäjällä on huoltohallintoon liittyviä tehtäviä.  

> [!NOTE]  
>  Käyttäjät pystyvät edelleen tarkastelemaan kaikkia kirjattuja asiakirjoja ja tapahtumia, eivät vain oman vastuupaikkansa asiakirjoja ja tapahtumia.

## <a name="see-also"></a>Katso myös  
[Varaston määrittäminen](inventory-setup-inventory.md)  
[Varastoinninhallinnan määrittäminen.](warehouse-setup-warehouse.md)
[Varasto](inventory-manage-inventory.md)[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varastoinninhallinta](warehouse-manage-warehouse.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

