---
title: Monikielisyys ja lokalisointi
description: Tutustu, miten kieli ja alue vaikuttavat Business Centralin käyttökokemukseen. Voit vaihtaa käyttöliittymän kielen Omat asetukset -sivulla.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture, region, regional settings
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 39927cc6adb02768a4358b2b7480a22cf68bc73a
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588399"
---
# <a name="changing-language-and-region"></a>Kielen ja alueen muuttaminen

[!INCLUDE[prod_short](includes/prod_short.md)] on saatavana useilla markkina-alueilla ja kielillä eri puolilla maailmaa. Markkina-alueilla, joilla [!INCLUDE[prod_short](includes/prod_short.md)] on saatavana, lakisääteiset ominaisuudet auttavat yrityksiä lakisääteisten vaatimusten osalta. [!INCLUDE[prod_short](includes/prod_short.md)] on käytettävissä eri kielillä, ja voit vaihtaa kielen, jolla tekstit näkyvät. Tämä muutos on tapahtuu automaattisen ulos- ja sisäänkirjautumisen aikana. Tämä asetus koskee vain muutoksen tekevää käyttäjää – ei siis yrityksen kaikkia käyttäjiä.  

Jos käytät esimerkiksi käytä kanadalaista [!INCLUDE[prod_short](includes/prod_short.md)] -versiota, voit käyttää englannin-, saksan-, ranskan- tai muun kielistä käyttöliittymää. Kyse on kuitenkin kaikilta ominaisuuksiltaan kanadalaisesta [!INCLUDE[prod_short](includes/prod_short.md)] -versiosta. Se ei ole sama kuin esimerkiksi Britanniassa käytettävä [!INCLUDE[prod_short](includes/prod_short.md)], jossa toiminnot on sopeutettu kyseisen markkina-alueen vaatimuksiin.  

Voit vaihtaa käyttöliittymän kielen **Omat asetukset** -sivulla. Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md#language). 

> [!NOTE]  
> Kielivalinta palautetaan Microsoft 365 -profiilin asetukseen, jos järjestelmänvalvoja synkronoi käyttäjät Microsoft 365:stä [!INCLUDE[prod_short](includes/prod_short.md)]iin.

Sovellusdatana tallennettujen tekstien kielen muuttaminen ei ole osa monikielisyysominaisuutta. Tämä on sovelluksen suunnitteluun liittyvä asia. Nimikkeiden nimet varastossa ja asiakaskommentit ovat esimerkkejä tällaisista teksteistä. Toisin sanoen tämän tyyppisiä tekstejä ei käännetä.  

> [!NOTE]  
> [!INCLUDE[prod_short](includes/prod_short.md)] tukee ainoastaan yhtä merkistöä. Tämän vuoksi ympäristö ei välttämättä tue kaikkia merkkejä, ja saatat havaita ongelmia hakiessasi eri merkistöllä annettuja tietoja. Asennus voi tukea esimerkiksi vain englantilaisia tai venäläisiä merkkejä. Jos syötät tietoja eri kielellä, tiedot saattavat tallentua virheellisesti. Ota yhteys järjestelmänvalvojaan, jos haluat lisätietoja [!INCLUDE[prod_short](includes/prod_short.md)]in tukemista kielistä.  

## <a name="changing-your-region-setting"></a>Alueasetuksen muuttaminen
Alue on eri asia kuin paikallisten markkina-alueiden kielivaatimukset ja lainsäädännölliset vaatimukset. Alue määrittää, käytetäänkö tietoja annettaessa esimerkiksi pilkkuerotinta ja tapahtuuko kohdistus vasemmalle vai oikealle. Alue määrittää myös jotkin selaimen järjestelmäelementit, kuten toiminnon, jolla luetteloon luodaan uusi nimike.  

Voit muuttaa alueen siinä selaimen välilehdessä, jossa käytät [!INCLUDE[prod_short](includes/prod_short.md)]ia. Tämä muutos koskee vain muutoksen tehnyttä käyttäjää – se ei siis koske yrityksen muita käyttäjiä.  Aluevalinta palautetaan Microsoft 365 -profiilin asetukseen, jos järjestelmänvalvoja synkronoi käyttäjät Microsoft 365:stä [!INCLUDE[prod_short](includes/prod_short.md)]iin.

> [!IMPORTANT]  
> Kun muutat alueen asetuksia, näkyviin tulee pitkä kieli- ja alueluettelo. Alueen valinta ei kuitenkaan vaikuta kieleen.  

Voit muuttaa alueen **Omat asetukset** -sivulla. Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).  

## <a name="changing-the-region-setting-for-customers-contacts-and-vendors"></a>Asiakkaiden, kontaktien ja toimittajien alueasetuksen muuttaminen
Jotkin yritykset käyttävät ulkoista palvelua, joka tarkistaa maan tai alueen osoitetiedot. Jos kuitenkin osoite tiedot on päivitettävä, näiden palveluiden käytössä oleva rakenteellinen lähestymistapa ei välttämättä aina ole oikea ratkaisu joissakin tilanteissa. Business Central tarjoaa joustavamman keinon osoitetietojen syöttämiseen.

Jos **Pääkirjanpidon asetukset** -sivulla otat käyttöön **Vaadi osoitteessa maa-/aluekoodi** -valitsimen, **Maa-/aluekoodi** -kentän muuttaminen asiakkaille, yhteyshenkilöille tai toimittajille nollaavat muiden osoitekenttien arvot.

## <a name="application-version"></a>Sovellusversio

Voit tarkistaa **Ohje ja tuki** -sivulla mihin [!INCLUDE[prod_short](includes/prod_short.md)] -versioon yrityksesi perustuu. Jos haluat perustaa yrityksen eri versioon, järjestelmänvalvoja voi luoda uuden tuotantoympäristön. Lisätietoja on kohdassa [Uuden tuotanto ympäristön luominen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-production-environment) Kehittäjän ja IT-ammattilaisen sisällössä.  

## <a name="languages-of-the-prod_short-help"></a>[!INCLUDE[prod_short](includes/prod_short.md)]-ohjeen kielet

[!INCLUDE[prod_short](includes/prod_short.md)]in perustoimintojen ohjesisältö julkaistaan Microsoft Docs -sivustossa ja on luettavissa useilla eri kielillä. Jos siirryt asiakirjoihin [!INCLUDE[prod_short](includes/prod_short.md)]ista, sisältö näkyy omalla kielelläsi. Jos tiettyä sivua ei ole vielä käännetty omalle kielellesi, se näkyy englanninkielisenä.

### <a name="how-do-i-change-the-language-of-the-microsoft-docs-site"></a>Miten Microsoft Docs -sivuston kieli muutetaan?

Kielen vaihtaminen on helppoa: siirry selainsivun alareunaan ja valitse vasemmassa kulmassa maapallokuvake.

> [!NOTE]  
> Avautuvassa luettelossa on kaikki Microsoft Docs-sivuston tukemat kielet. [!INCLUDE[prod_short](includes/prod_short.md)] on saatavana vain tietyissä maissa ja tietyillä alueilla eikä [!INCLUDE [prod_short](includes/prod_short.md)] -ohjesisältö ole saatavana kaikilla kielillä, joita Microsoft Docs -sivusto tukee.

## <a name="see-also"></a>Katso myös

[Ohje- ja tukiresurssit](product-help-and-support.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]