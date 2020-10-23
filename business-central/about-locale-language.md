---
title: Monikielisyys ja lokalisointi | Microsoft Docs
description: Tutustu, miten kieli ja alue vaikuttavat Business Centralin käyttökokemukseen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture, region, regional settings
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d47214392e3c0e48f436475a79407a752a95583d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914562"
---
# <a name="changing-language-and-region"></a>Kielen ja alueen muuttaminen

[!INCLUDE[d365fin](includes/d365fin_md.md)] on saatavana useilla markkina-alueilla ja kielillä eri puolilla maailmaa. Markkina-alueilla, joilla [!INCLUDE[d365fin](includes/d365fin_md.md)] on saatavana, lakisääteiset ominaisuudet auttavat yrityksiä lakisääteisten vaatimusten osalta. [!INCLUDE[d365fin](includes/d365fin_md.md)] on käytettävissä eri kielillä, ja voit vaihtaa kielen, jolla tekstit näkyvät. Tämä muutos on tapahtuu automaattisen ulos- ja sisäänkirjautumisen aikana. Tämä asetus koskee vain muutoksen tekevää käyttäjää – ei siis yrityksen kaikkia käyttäjiä.  

Jos käytät esimerkiksi käytä kanadalaista [!INCLUDE[d365fin](includes/d365fin_md.md)] -versiota, voit käyttää englannin-, saksan-, ranskan- tai muun kielistä käyttöliittymää. Kyse on kuitenkin kaikilta ominaisuuksiltaan kanadalaisesta [!INCLUDE[d365fin](includes/d365fin_md.md)] -versiosta. Se ei ole sama kuin esimerkiksi Britanniassa käytettävä [!INCLUDE[d365fin](includes/d365fin_md.md)], jossa toiminnot on sopeutettu kyseisen markkina-alueen vaatimuksiin.  

Voit vaihtaa käyttöliittymän kielen **Omat asetukset** -sivulla. Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md#language). 

> [!NOTE]  
> Kielivalinta palautetaan Microsoft 365 -profiilin asetukseen, jos järjestelmänvalvoja synkronoi käyttäjät Microsoft 365:stä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.

Sovellusdatana tallennettujen tekstien kielen muuttaminen ei ole osa monikielisyysominaisuutta. Tämä on sovelluksen suunnitteluun liittyvä asia. Nimikkeiden nimet varastossa ja asiakaskommentit ovat esimerkkejä tällaisista teksteistä. Toisin sanoen tämän tyyppisiä tekstejä ei käännetä.  

> [!NOTE]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] tukee ainoastaan yhtä merkistöä. Tämän vuoksi ympäristö ei välttämättä tue kaikkia merkkejä, ja saatat havaita ongelmia hakiessasi eri merkistöllä annettuja tietoja. Asennus voi tukea esimerkiksi vain englantilaisia tai venäläisiä merkkejä. Jos syötät tietoja eri kielellä, tiedot saattavat tallentua virheellisesti. Ota yhteys järjestelmänvalvojaan, jos haluat lisätietoja [!INCLUDE[d365fin](includes/d365fin_md.md)]in tukemista kielistä.  

## <a name="changing-the-region"></a>Alueen muuttaminen
Alue on eri asia kuin paikallisten markkina-alueiden kielivaatimukset ja lainsäädännölliset vaatimukset. Alue määrittää, käytetäänkö tietoja annettaessa esimerkiksi pilkkuerotinta ja tapahtuuko kohdistus vasemmalle vai oikealle. Alue määrittää myös jotkin selaimen järjestelmäelementit, kuten toiminnon, jolla luetteloon luodaan uusi nimike.  

Voit muuttaa alueen siinä selaimen välilehdessä, jossa käytät [!INCLUDE[d365fin](includes/d365fin_md.md)]ia. Tämä muutos koskee vain muutoksen tehnyttä käyttäjää – se ei siis koske yrityksen muita käyttäjiä.  Huomaa, että aluevalinta palautetaan Office-profiilin asetukseen, jos järjestelmänvalvoja synkronoi käyttäjät Microsoft 365:stä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.

> [!IMPORTANT]  
>  Kun muutat alueen asetuksia, näkyviin tulee pitkä kieli- ja alueluettelo. Alueen valinta ei kuitenkaan vaikuta kieleen.  

Voit muuttaa alueen **Omat asetukset** -sivulla. Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).  

## <a name="application-version"></a>Sovellusversio

Voit tarkistaa **Ohje ja tuki** -sivulla mihin [!INCLUDE[prodshort](includes/prodshort.md)] -versioon yrityksesi perustuu. Jos haluat perustaa yrityksen eri versioon, järjestelmänvalvoja voi luoda uuden tuotantoympäristön. Lisätietoja on kohdassa [Uuden tuotanto ympäristön luominen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-production-environment) Kehittäjän ja IT-ammattilaisen sisällössä.  

## <a name="languages-of-the-d365fin-help"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]-ohjeen kielet
[!INCLUDE[d365fin](includes/d365fin_md.md)]in perustoimintojen ohjesisältö julkaistaan Microsoft Docs -sivustossa ja on luettavissa useilla eri kielillä. Jos siirryt asiakirjoihin [!INCLUDE[d365fin](includes/d365fin_md.md)]ista, sisältö näkyy omalla kielelläsi. Jos tiettyä sivua ei ole vielä käännetty omalle kielellesi, se näkyy englanninkielisenä.

### <a name="how-do-i-change-the-language"></a>Kielen vaihtaminen
Kielen vaihtaminen on helppoa: siirry selainsivun alareunaan ja valitse vasemmassa kulmassa maapallokuvake.

> [!NOTE]  
> Avautuvassa luettelossa on kaikki Microsoft Docs-sivuston tukemat kielet. [!INCLUDE[d365fin](includes/d365fin_md.md)] on käytettävissä vain tietyissä maissa ja tietyillä alueilla, mutta ohjesisältö on luettavissa myös monilla muilla kielillä. Ohjesisältö ei kuitenkaan ole luettavissa kaikilla Microsoft Docs -sivuston tukemissa kielillä.

## <a name="see-also"></a>Katso myös

[Ohje- ja tukiresurssit](product-help-and-support.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Käytön aloittaminen](product-get-started.md)  
