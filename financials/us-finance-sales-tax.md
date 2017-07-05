---
title: "Yhdysvaltojen ja Kanadan arvonlisävero ja veroryhmät | Microsoft Docs"
description: "Lisätietoja siitä, miten arvonlisävero määritetään ja miten veroryhmiä, verotoimialueita ja verojen tietoja käsitellään."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ff1981a428a2cd3b3864b7f0cc795a1abeab7a10
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="sales-tax-and-tax-groups-in-the-us-and-canada"></a>Yhdysvaltojen ja Kanadan arvonlisävero ja veroryhmät
Kun aloitat [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttämisen, voit määrittää arvonlisäverojen tiedot nopeasti ja helposti yritykselle, asiakkaille ja toimittajille avustetun asennusoppaan avulla. Muutamassa minuutissa voit aloittaa myynti- ja ostoasiakirjojen luomisen niin, että arvonlisävero lasketaan oikein. Lisätietoja on [blogiviestissämme](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy).
Jos siirryt tyhjään omaan yritykseen, aloita käyttämällä kutakin avustettua asennusopasta, myös arvonlisäveron asennusopasta. Tässä artikkelissa kerrotaan, mitä arvonlisäveron määrittämisessä tulee ottaa huomioon, jos haluat määrittää arvonlisäveron itse.  

## <a name="tax-groups-tax-areas-and-tax-jurisdictions"></a>Arvonlisäveroryhmät, veroalueet ja verotoimialueet
[!INCLUDE[d365fin](includes/d365fin_md.md)]issa veroluokkaan kuuluvat sellaiset varastonimikkeet tai resurssit, joilla on keskenään identtiset verotusehdot. Voit määrittää esimerkiksi veroryhmän verotettaville nimikkeille ja toisen veroryhmän muille kuin verotettaville nimikkeille. Määritä varastonimikkeille ja pääkirjanpidon tileille veroryhmäkoodit. Samoin on määritettävä asiakkaiden, sijaintien ja oman yrityksen asetusten veroaluekoodit. Avustettu asennusopas auttaa tässä.  

Kukin veroalue on arvonlisäverotoimialueen ryhmittely, joka perustuu tiettyyn maantieteelliseen sijaintiin. Esimerkiksi Floridassa sijaitsevan Miamin veroalue sisältää kolme arvonlisäverotoimialuetta: kaupunki (Miami), lääni (Dade) ja osavaltio (Florida). [!INCLUDE[d365fin](includes/d365fin_md.md)]in oletusmääritys sisältää rajoitetun määrän veroalueita. Voit kuitenkin muuttaa niitä ja lisätä uusia veroalueita.  

Jos olet määrittänyt uudet veroalueet ja verotoimialueet, varmista, että täytät kentät oikein. Yhdysvalloissa osavaltiot, läänit, kaupungit ja paikkakunnat voivat kerätä arvonlisäveroa. Kanadassa liittovaltio ja provinssit voivat kerätä arvonlisäveroa. Yritykset keräävät loppukäyttäjille myytävistä tuotteista arvonlisäveron ja maksavat sen julkishallinnolle. Arvonlisäveroa voidaan kerätä myös olemassa olevasta arvonlisäverosta. Vero voidaan laskea esimerkiksi myyntilaskun summasta, joka jo sisältää muiden toimialueiden veron.  

Kanadassa verosummat on eriteltävä kunkin verotoimialueen asiakirjoissa. Asiakirjassa voi olla enintään neljä toimialuetta. Toimialueet, joilla on sama tulostusjärjestys, yhdistetään tulostamisen yhteydessä.  

## <a name="tax-details"></a>Veroerittelyt
**Verotiedot**-ikkunassa näkyvät arvonlisäverotoimialueiden ja arvonlisäveroryhmien eri yhdistelmät, joiden mukaan muodostetaan arvonlisäveroprosentit. Jokaiselle verotoimialueelle kannattaa määrittää yksi veroryhmä normaalille arvonlisäverolle, toinen nimikkeille tai palveluille, joita ei veroteta, ja lisäveroryhmä jokaiselle sellaiselle nimike- tai palvelutyypille, joissa on eri arvonlisäveroprosentti kuin toimialueella.  

Kun Yhdysvalloissa myynti asiakkaalle tapahtuu paikassa, jolla ei ole *situs*-arvoa (eli juridista sijaintia kyseisessä osavaltiossa), arvonlisäveroa ei kerätä. Varmista, että sijainneilla, joilla ei ole situs-arvoa, on sekä **Enimmäisrajan alittava vero**- että **Enimmäisrajan ylittävä vero** -kentän arvoksi määritetty 0,00.  

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Kanadan arvonlisävero](ca-finance-tax.md)  
[Helposti suoritettava arvonlisäveron määrittäminen](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  
