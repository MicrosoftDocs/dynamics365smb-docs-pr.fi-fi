---
title: Dynamics 365 for Sales -integroinnissa käytettävien käyttäjätilien määrittäminen | Microsoft Docs
description: Tietoja niiden käyttäjätilien määrittämisestä, joilla sovellukset vaihtavat tietoja ja joiden avulla käytetään ja synkronoidaan sovellusten tietoja.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: c318346c62b7776a550a77a2947173e33d5f17c0
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2019
ms.locfileid: "940124"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Dynamics 365 for Sales -integroinnissa käytettävien käyttäjätilien määrittäminen
Tässä artikkelissa on yleiskatsaus [!INCLUDE[crm_md](includes/crm_md.md)]in ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in integroinnissa tarvittavien käyttäjätilien määrittämisestä.  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-admininstrator-user-account-in-sales"></a>Järjestelmänvalvojan käyttäjätilin määrittäminen Salesissa
[!INCLUDE[d365fin](includes/d365fin_md.md)]in järjestelmänvalvojan käyttäjätili on lisättävä ensin käyttäjänä [!INCLUDE[crm_md](includes/crm_md.md)]iin ja siirrettävä käyttäjä sitten [!INCLUDE[crm_md](includes/crm_md.md)]in järjestelmänvalvojaksi. Järjestelmänvalvojan käyttäjätilillä on oltava [!INCLUDE[crm_md](includes/crm_md.md)]issa myös järjestelmän mukauttajan rooli ja ainakin yksi ei-hallinnollinen käyttäjärooli, kuten myyntipäällikkö.

## <a name="setting-up-the-user-account-for-the-integration"></a>Käyttäjätilin määrittäminen integrointia varten
Office 365 -tilauksessa on luotava erillinen käyttäjätili, jota sekä [!INCLUDE[d365fin](includes/d365fin_md.md)] että [!INCLUDE[crm_md](includes/crm_md.md)] voi käyttää tietojen synkronoimiseen. Tällä käyttäjätilillä on voitava kirjautua [!INCLUDE[crm_md](includes/crm_md.md)]iin, joten kyseisellä käyttäjällä on oltava [!INCLUDE[crm_md](includes/crm_md.md)]in käyttöoikeus. Tämän tili on lisäksi oltava ei-vuorovaikutteinen tili [!INCLUDE[crm_md](includes/crm_md.md)]issa. Lisätietoja käyttäjien luomisesta [!INCLUDE[crm_md](includes/crm_md.md)]issa on kohdassa [Tietoturvan, käyttäjien ja tiimien hallinta](http://go.microsoft.com/fwlink/?LinkID=616518). Kun yhteys on määritetty, [!INCLUDE[d365fin](includes/d365fin_md.md)] määrittää käyttäjätilille käyttöoikeusroolin, jota se tarvitsee [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.

![Asetusten ohjattu määritys osoittaa paikan, johon synkronoinnin käyttäjätiedot annetaan](media/sync-user-setup.png "Visualisointina asetusten ohjattu määrityssivu osoittaa paikan, johon synkronoinnin käyttäjätiedot annetaan")

> [!IMPORTANT]  
> Älä käytä [!INCLUDE[crm_md](includes/crm_md.md)]in järjestelmänvalvojan tiliä synkronointiin, sillä se katkaisee synkronoinnin.
> Jotta synkronointi ei olisi jatkuvaa, integroinnin käyttäjätilin tietoihin tekemiä muutoksia ei myöskään synkronoida. <!--What changes would this account make?--> Kun yhteys on muodostettu, on suositeltavaa määrittää integroinnin käyttäjätilin käyttöoikeus [!INCLUDE[crm_md](includes/crm_md.md)]issa ei-vuorovaikutteiseen tilaan. Lisätietoja on kohdassa [Ei-vuorovaikutteisen käyttäjätilin luominen](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-sales-people"></a>Myyjien tilien määrittäminen
[!INCLUDE[crm_md](includes/crm_md.md)]issa on luotava käyttäjätilit [!INCLUDE[d365fin](includes/d365fin_md.md)]in myyjille. Tämän helpottamiseksi Microsoft 365:n hallintakeskuksessa on Excel-malli, jota voit käyttää. Valitse **Aktiiviset käyttäjät** -sivulla ensin **Lisää** ja sitten **Tuo useita käyttäjiä**. Valitse **Lataa vain otsikot sisältävä CSV-tiedosto** ja anna myyjien tiedot. Jos haluat nähdä esimerkin, valitse **Lataa otsikot sisältävä CSV-tiedosto ja esimerkkikäyttäjätiedot**. Kun olet antanut käyttäjien tiedot, tuontiprosessin seuraava vaihe on määrittää käyttäjien käyttöoikeudet Dynamics 365 Customer Engagement -palvelupakettiin.  

Kun olet tuonut käyttäjät ja määrittänyt heille Dynamics 365 Customer Engagementin käyttöoikeudet, sinun on määritettävä käyttäjille **myyjän** rooli [!INCLUDE[crm_md](includes/crm_md.md)]issa.

![Myyjien yhdistäminen käyttäjiin Dynamics 365 for Salesissa](media/couple-salespeople.png "Visualisointina myyjien yhdistäminen käyttäjiin Dynamics 365 for Salesissa")

## <a name="see-also"></a>Katso myös  
[Integrointi Dynamics 365 for Salesin kanssa](admin-prepare-dynamics-365-for-sales-for-integration.md)  
