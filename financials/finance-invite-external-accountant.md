---
title: "Ulkoisen kirjanpitäjän lisääminen Financialsiin | Microsoft Docs"
description: "Lisätietoja ulkoisen kirjanpitäjän kutsumisesta Dynamics 365 for Financialsiin."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting
ms.date: 06/23/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1b9f88f02b198ae8da0f3359a3ce7799b9535739
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="invite-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Ulkoisen kirjanpitäjän kutsuminen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin
Jos käytä ulkoista kirjanpitäjää kirjojen ja talousraportoinnin hallinnassa, voit kutsua kirjanpitäjän [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, jolloin he saavat käyttöönsä kirjanpitotietosi.

Kun kirjanpitäjä on saanut [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeudet, hän voi käyttää **Kirjanpitäjä**-roolikeskusta. josta pääsee kätevästi kirjanpitäjän työssään eniten käyttämiin ikkunoihin.  

> [!NOTE]  
>  Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on ohjeaiheessa [Financials-kokemuksen mukauttaminen](ui-experiences.md).  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a>Kirjanpitäjän kutsuminen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin
[!INCLUDE[d365fin](includes/d365fin_md.md)]in nykyisessä versiossa ulkoisen kirjanpitäjän kutsuminen edellyttää, että järjestelmänvalvoja lisää heidät Active Directory -vuokraajaan. Tämä toimenpiteen tekeminen käytännössä määräytyy sen tilin mukaan, jolla [!INCLUDE[d365fin](includes/d365fin_md.md)]iin kirjaudutaan. Tämän ohjeaiheen ohjeet perustuvat Office 365 -tiliin, jossa on käytössä Microsoft Azure Active Directory.  

> [!TIP]  
>  Lisätietoja kannattaa pyytää [!INCLUDE[d365fin](includes/d365fin_md.md)] -kumppanilta.  

Jos olet aktivoinut [!INCLUDE[d365fin](includes/d365fin_md.md)]in tilauksen etkä käytä enää arviointiyritystä, sinulla on Azure Active Directory -vuokraaja. Järjestelmänvalvoja tai [!INCLUDE[d365fin](includes/d365fin_md.md)]-kumppanin hallitsee tätä vuokraajaa [Azure-portaalissa](https://portal.azure.com). Uudet käyttäjät lisätään tässä portaalissa. Myös käyttöoikeudet otetaan käyttöön ja poistetaan siellä. Lisätietoja on ohjeaiheessa [Microsoft Azure -portaalin yleiskatsaus](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

### <a name="separate-license"></a>Erillinen käyttöoikeus
Yksi [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeustyypeistä on *ulkoisen kirjanpitäjän* käyttöoikeus. Tämä käyttöoikeustyyppi on tarkoitettu ulkoisen kirjanpitäjän kaltaisille käyttäjille. Tämä käyttöoikeustyyppi ei edellytä ylimääräisen asiakaskohtaisen käyttöoikeuden ostamista nykyiseen Active Directoryyn eikä nykyisen [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjätilin käyttöä ulkoiselle kirjanpitäjälle. Jos esimerkiksi nykyinen Office 365 -tilaus sisältää 10 [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöjää ja käytät tällä hetkellä 10 *täyttä käyttöoikeutta*, järjestelmänvalvoja voi vain lisätä ulkoisen kirjanpitäjän vieraskäyttäjänä Azure-portaaliin ja määrittää tälle käyttäjälle *ulkoisen kirjanpitäjän* käyttöoikeuden ilman lisäkustannuksia. *Ulkoisen kirjanpitäjän * käyttöoikeudet voi kuitenkin olla vain yhdellä käyttäjällä. Jos haluat lisätä enemmän käyttäjiä, Office 365 -tilausta on päivitettävä vastaavasti.  

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Dynamics 365 for Financialsin kirjanpitäjän käyttökokemukset](finance-accounting.md)  
[Financials for Accountants on Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

