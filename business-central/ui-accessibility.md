---
title: Aputoiminnot
description: Tässä artikkelissa on tietoja Business Centralin pikanäppäimista ja muista apuominaisuuksista vammaisille henkilöille.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, charts, tooltips, screen reader
ms.date: 06/23/2021
ms.author: jswymer
ms.openlocfilehash: 80e48acc1ded96c9958c1dd7a2a706e22dc3e82b
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/30/2021
ms.locfileid: "6319953"
---
# <a name="accessibility-and-keyboard-shortcuts"></a>Helppokäyttötoiminnot ja pikanäppäimet

Tässä artikkelissa on tietoja toiminnoista, joiden ansiosta [!INCLUDE[prod_short](includes/prod_short.md)] on jo toimintarajoitteisten käyttäjien käytettävissä. [!INCLUDE[prod_short](includes/prod_short.md)] tukee seuraavia helppokäyttötoimintoja:  

- Pikanäppäimet. Katso [Pikanäppäimet](keyboard-shortcuts.md).
- Tablettien ja puhelinten kosketuseleet ja kynän liikkeet. Katso [Kosketuseleet ja kynän liikkeet](touch-gestures.md).
- Siirtyminen  
- Otsikot  
- Kuvien ja linkkien vaihtoehtoinen teksti  
- Yleisten käyttöä tukevien tekniikoiden tuki 
- Lähennä tai loitonna millä tahansa sivulla
- Käyttöliittymän elementtien työkaluvihjeet

## <a name="navigation"></a><a name="Navigation"></a> Siirtyminen
  
Voit käyttää näppäimistön sarkain-, vaihto- ja nuolinäppäimiä, jos haluat siirtyä sivun elementtien välillä. Elementtejä ovat toiminnot, kentät ja sarakkeet, osat ja muut ohjausobjektit. Yleensä voit siirtyä seuraavaan tai edelliseen elementtiin painamalla sarkain- tai vaihto+sarkain-näppäimiä.

Kun keskitys tehdään toimintoja sisältävälle alueelle, siirry nuolinäppäinten avulla eri toimintojen ja ryhmien välillä. Toimintoja ovat esimerkiksi roolikeskuksen yläosan siirtymispalkki ja muiden sivujen toimintopalkit. Paina sen ryhmän Enter-näppäintä, jonka pohjana olevat toiminnot haluat avata, ja jatka sitten nuolinäppäinten avulla. Siitty toimintoalueelta pois sarkain- tai vaihto+sarkain-näppäinten avulla.

Voit siirtyä sarkaimella järjestyksessä pääselainsivun ja esimerkiksi vahvistusta pyytävän valintaikkunan tai kirjautumissivun välillä.  

## <a name="headings-in-content"></a><a name="Headings"></a>Sisällön otsikot

[!INCLUDE[prod_short](includes/prod_short.md)]:n sisällön HTML-lähde käyttää tunnisteita, jotka auttavat helppokäyttötoimintojen käyttäjiä ymmärtämään sivun rakennetta ja sisältöä. Esimerkiksi luettelosivuilla sarakkeet määritetään TH.-tunnisteilla ja sarakeotsikot määritetään tunnisteen sisällä olevalla TITLE-määritteellä. Otsikkotunnisteet (H1, H2, H3 ja H4) sisältävät elementtien, kuten pikavälilehtien, tietoruutujen ja kenttien, selosteet.  

## <a name="image-and-links"></a><a name="Images"></a> Kuva ja linkit

Kuvien kuvaileva teksti määritetään IMG-tunnisteeseen sisältyvällä ALT-määritteellä. Hyperlinkkien kuvaileva teksti määritetään A-tunnisteeseen sisältyvällä TITLE-määritteellä.  

## <a name="assistive-technologies"></a><a name="AssistiveTech"></a> Käyttöä tukevat tekniikat

[!INCLUDE[prod_short](includes/prod_short.md)] tukee erilaisia käyttöä helpottavia tekniikoita, kuten suurta kontrasti, näytönlukuohjelmia ja puheentunnistusohjelmistoja. Jotkin käyttöä helpottavat tekniikat eivät ehkä toimi hyvin tiettyjen [!INCLUDE[prod_short](includes/prod_short.md)]:n sivuelementtien kanssa.  

## <a name="zoom"></a><a name="zoom"></a>Zoomaa

Useimmat selaimet käyttävät vakiopikanäppäimiä, kun haluat lähentää ja loitontaa nykyistä sivua. Nämä pikanäppäimet eivät ole tuotteelle [!INCLUDE [prod_short](includes/prod_short.md)] ominaisia, mutta ne toimivat, kun [!INCLUDE [prod_short](includes/prod_short.md)] on käytössä selaimessa. Luettelo tuetuista pikanäppäimistä on kohdassa [Pikanäppäimet lähentämistä ja loitontamista varten](keyboard-shortcuts.md#zoomshortcuts).

## <a name="tooltips"></a>Työkaluvihjeet

Työkaluvihjeet ovat käytettävissä useimmissa käyttöliittymän elementeissä, kuten sivun kentissä ja sarakkeissa, toiminnoissa, pinoruuduissa ja kaavioissa. Työkalu Vihje sisältää lisä tekstin, jossa selitetään elementti, joka helpottaa sen tarkoituksen ymmärtämistä. 

Työkaluvihjeet ovat käytettävissä eri tavoilla asiakasohjelman (verkko tai mobiili) ja käyttämäsi laitteen mukaan. Käytä seuraavaa taulukkoa oppaana. Näytönlukuohjelmat voivat lukea osan työkaluvihjeistä. Tässä tapauksessa työkaluvihjeitä käytetään taulukossa kuvatulla tavalla. Tämän jälkeen siirrytään työkaluvihjeeseen näytönlukuohjelman avulla samalla tavalla kuin mihin tahansa muuhun elementtiin.

#### <a name="accessing-tooltips"></a>Työkaluvihjeiden käyttäminen

|Elementti|Hiiritoiminto verkkoasiakasohjelmassa|Verkkoasiakasohjelman pikanäppäimet|Mobiilisovelluksen kosketusele tabletissa/puhelimessa|Näytönlukuohjelman tuki|
|-------|-----------------|------------|--------------------------|---------------------|
|Sivun kenttien ja sarakkeiden otsikot|Valitse kentän tai sarakkeen otsikko osoittamalla tai napsauta sitä|Siirrä kohdistus kentän tai sarakkeen otsikkoon ja paina Alt+ylänuolinäppäin|Napauta kentän otsikkoa |kyllä|
|Kaavioiden elementit, kuten palkki, viiva ja ympyrän sektori|Valitse elementti osoittamalla|Siirrä kohdistus elementtiin käyttämällä esimerkiksi nuolinäppäimiä|Napauta elementtiä ja pidä sitä painettuna|kyllä|
|Toiminnot|Valitse toiminto osoittamalla|ei mitään|ei mitään |ei|
|Pinoruudut|Valitse ruutu osoittamalla |ei mitään|ei mitään|ei|


<!--
- With a mouse, hover over the element.
- With keyboard, press the Alt+Up Arrow keys.
- On a tablet or phone, tap and hold on the element. To learn about more gestures, see [Touch and Pen Gestures](touch-gestures.md)

-->

## <a name="for-more-accessibility-information"></a>Lisätietoja helppokäyttötoiminnoista

Lisätietoja Microsoftin tuotteiden helppokäyttötoiminnoista ja käyttöä helpottavista tekniikoista on [Microsoftin helppokäyttötoimintojen](https://go.microsoft.com/fwlink/?LinkId=262160) sivustossa.

## <a name="see-also"></a>Katso myös

[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Usein kysytyt kysymykset](across-faq.yml)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
