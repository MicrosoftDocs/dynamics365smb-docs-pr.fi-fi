---
title: Varaston hallinta myynnin ja varaston ennustelaajennuksen avulla | Microsoft Docs
description: "Tällä laajennuksella voi ennakoida myyntiä ja saada selkeän käsityksen odotettavissa olevista varaston loppumisesta. Se myös auttaa luomaan täydennyspyyntöjä toimittajille."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: edddda48fe91ed2e31b9c709a546730ce50dc6d4
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="sales-and-inventory-forecast-for-business-central"></a>Business Central -sovelluksen myynti- ja varastoennuste 
Varaston hallintaan kuuluvat sekä asiakaspalvelu että kustannusten hallinta. Pieni varasto vaatii vähemmän liikepääomaa, mutta toisaalta varaston loppumiset voivat aiheuttaa myyntimenetyksiä. Myynti- ja varastoennuste -laajennus ennustaa mahdollisen myynnin aiempien tietojen avulla. Se tarjoaa selvän yleiskuvan odotetuista varaston loppumisista. Ennusteen perusteella laajennus auttaa luomaan täydennyspyyntöjä toimittajille, ja säästää näin aikaasi.  

## <a name="setting-up-forecasting"></a>Ennusteiden määrittäminen
[Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) -yhteys on muodostettu valmiiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Voit kuitenkin määrittää ennusteen niin, että se käyttää raportoinnissa erityyppistä kautta. Ennuste voidaan laatia esimerkiksi kuukauden sijaan neljännesvuosittain. Voit myös valita ennustelaskelmassa käytettävien kausien määrän sen mukaan, miten hajautetun ennusteen haluat. Ennusteen voi tehdä esimerkiksi kuukautta kohti 12 kuukauden ajalle.  

## <a name="using-the-forecasts"></a>Ennusteiden käyttäminen
Laajennus ennustaa Cortana Intelligencen avulla tulevan myynnin myyntihistorian perusteella. Näin voidaan välttää puutteet varastossa. Jos esimerkiksi valitset nimikkeen **Nimikkeet**-ikkunassa, kaavion **Nimikkeen ennuste** -ruudussa näkyy tämän nimikkeen arvioitu myynti tulevan kauden aikana. Näin näet, onko nimike loppumassa varastosta lähiaikoina.  

Voit käyttää laajennusta myös varaston täydennysajankohdan ehdottamisessa. Jos esimerkiksi luot ostotilauksen Fabrikamille, koska haluat ostaa heiltä uuden työtuolin, Myynti- ja varastoennuste -laajennus ehdottaa, että samalla kannattaa ostaa LONDON-toimistotuoleja, joita yleensä ostat kyseiseltä toimittajalta. Laajennus ehdottaa tätä sen vuoksi, koska se ennustaa LONDON-toimistotuolien loppuvan varastosta kahden seuraavan kuukauden aikana. Tuoleja siis kannattaa ostaa lisää jo nyt.  

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Varasto](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
