---
title: Saat esikatselun uusista markkinoista
description: "Lue lisää Business Central -sovelluksen esikatseluiden käyttöoikeudesta."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: preview, trial, sandbox
ms.date: 01/05/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 3e7c5ca600a5f64b44fca419ce33cad868f15595
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="access-to-the-included365finlongincludesd365finlongmdmd-preview"></a>[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] -esikatselun käyttöoikeus
[!INCLUDE[d365fin](includes/d365fin_md.md)] on saatavissa uusissa maissa keväästä 2018 alkaen. Jotta varmistamme, että [!INCLUDE[d365fin](includes/d365fin_md.md)] on juuri oikea ratkaisu asiakkaille, tarjoamme palvelusta esikatseluversion kevään julkaisussa. Tanskan esikatselu tuli käyttöön tammikuussa 2018. Se on pian käytettävissä myös muilla markkinoilla.  

## <a name="getting-started-with-previews-and-sandboxes"></a>Esikatseluiden ja sandbox-ympäristöjen käytön aloittaminen
Esikatselut ja sandbox-ympäristöt ovat erinomainen tapa aloittaa [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttö. Esikatseluesiintymä sisältää toimintoja, jotka ovat lisäyksiä nykyiseen versioon. Esikatseluiden avulla kumppanit ja asiakkaat voivat kokeilla julkaisua odottavia toimintoja ja antaa niistä palautetta. Vaikka esikatselut on tarkoitettu ensisijaisesti kumppaneille, asiakkaat voivat myös käyttää niitä rajoitetun ajanjakson ajan. [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen nykyinen esikatselu sisältää suurimman osan Dynamics NAV 2018:n ominaisuuksista. Niiden määrittäminen vaatii yleensä kumppanin apua.

Voit aloittaa esikatselun käytön siirtymällä [tälle sivulla](https://go.microsoft.com/fwlink/?linkid=866045) ja kirjoittamalla työsähköpostiosoitteen. Saat lisätietoja [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksesta ja sen tarjoamista ominaisuuksista tämän sivuston dokumentaatiosta.

Voit ajatella sandbox-ympäristöä muuna kuin tuotantoympäristönä, jota voi käyttää tuotannon tai [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen esikatseluesiintymän lisäksi. Sandbox-ympäristön avulla voi turvallisesti luoda ja testata laajennuksia ja kehittää uusia toimintoja palvelun mukauttamista varten niin, että tuotannon tai esikatseluesiintymien tiedot tai asetukset eivät muutu. Juuri nyt asiakkaat, joilla on tuotanto- tai esikatseluversio, voivat käyttää sandbox-ympäristöä.

Saat lisätietoja sandbox-ympäristön käytön aloittamisesta alla olevista ohjeista.

## <a name="creating-a-sandbox-environment"></a>Sandbox-ympäristön luominen
Sandbox-ympäristön käyttö edellyttää [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen tilauksen. Kutakin tilausta kohden voi olla vain yksi sandbox-ympäristö.

### <a name="advanced-functionality-available-in-a-sandbox-environment"></a>Sandbox-ympäristön käytettävissä olevat lisätoiminnot
Sandbox-ympäristöt sisältävät asiakasohjelman suunnittelutoiminnon. Se mahdollistaa sivujen suunnittelemisen vedä ja pudota -käyttöliittymän avulla ja laajennusten luomisen asiakasohjelmassa lisäämällä ja järjestämällä kenttiä.

Lisätietoja on kohdassa [Suunnittelutoiminnon käyttäminen](https://docs.microsoft.com/en-us/dynamics-nav/developer/devenv-inclient-designer).

### <a name="to-create-a-sandbox-environment"></a>Sandbox-ympäristön luominen
1.  Kirjaudu [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman tuotanto- tai esikatseluesiintymään.  
2.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sandbox-ympäristö** ja valitse liittyvä linkki.
3.  Valitse **Luo**. Esiin tulevassa välilehdessä voit määrittää sandbox-ympäristön asetukset valmiiksi.

    > [!Note]
    > Jos ponnahdusikkunoiden esto on käytössä selaimessa, vaihda sen asetukset sallimaan *.financials.dynamics.com*-osoitteen URL-osoitteet.  

4.  Kun sandbox-ympäristö on valmis, näyttöön tulee aloitussivu.  
5.  Jos haluat lukea sandbox-ympäristössä kokeiltavista skenaarioista, kuten esimerkiksi laajennusten kehittämisestä, valitse **Lisätietoja**-linkki. Muussa tapauksessa valitse **Sulje** ja jatka [!INCLUDE[d365fin](includes/d365fin_md.md)] -sanbox-esiintymän roolikeskukseen.  
6.  Roolikeskuksen yläreunaan avautuvassa ilmoituksessa ilmoitetaan, että kyse on sandbox-ympäristöstä. Ympäristön tyyppi näkyy myös asiakasohjelman otsikkopalkissa.

    > [!Note]
    > Sandbox-ympäristö sisältää kuvitteellisen CRONUS-yrityksen esittelytiedot. Mitään tietoja ei kopioida tai muutoin siirretä tuotantoympäristöstä.  

7.  Voit palata koska tahansa Sandbox-ympäristöt-sivulle ja palauttaa sandbox-ympäristön alkuasetuksiin.

    > [!Note]
    > Sandbox-ympäristön palauttaminen alkuasetuksiin poistaa sen kokonaan. Tämän jälkeen se luodaan uudelleen oletusesittelytietojen avulla.  

8.  Voit siirtyä tuotanto- ja sandbox-ympäristön välillä Dynamics 365 -valikon tai Dynamics-kotisivun avulla.

    > [!Note]
    > Järjestelmänvalvoja tai toinen käyttäjä voi rajata tai jopa estää sandbox-ympäristön käyttöoikeuden käyttämällä [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman vakiotietoturvaominaisuuksien, kuten käyttäjäkortin, käyttäjäryhmien tai käyttöoikeusjoukkojen avulla.  

### <a name="building-new-solutions-and-intellectual-property"></a>Uusien ratkaisujen kehittäminen ja immateriaalioikeudet
[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää joukon kehitystyökaluja ja nykyaikaisen ympäristön, jossa voi kehittää omia lisäsovelluksia ja upottaa ratkaisuja [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yhteydenmuodostusta tai laajentamista varten.

[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää työkaluja, joiden avulla voit ottaa käyttöön omat lisäosat ja upottaa toimintoja, joiden avulla lisätään toimialakohtaisia kokonaisvaltaisia käyttökokemuksia tai integroidaan kolmannen osapuolen ratkaisuja. Voit esimerkiksi kehittää ohjelmointirajapinnan avulla yhdistetyn sovelluksen, jolla vaihdetaan tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman ja palkkasovelluksen välillä. Yhdistetyt sovellukset voivat käyttää myös laajennuksia ja luoda sivuja, joita käytetään asetuksissa, määrityksissä tai sovelluskohtaisten toimintojen tukemisessa. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman sovellusten kehittäminen](https://aka.ms/getstartedwithapps).

##<a name="see-also"></a>Katso myös
[Käytön aloittaminen](product-get-started.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

