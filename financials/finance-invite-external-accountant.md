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
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b7efbb724f322d371e9e1b725612cb4eb0b3ceb2
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="inviting-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Ulkoisen kirjanpitäjän kutsuminen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin
Jos käytä ulkoista kirjanpitäjää kirjojen ja talousraportoinnin hallinnassa, voit kutsua kirjanpitäjän [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, jolloin he saavat käyttöönsä kirjanpitotietosi.

Kun kirjanpitäjä on saanut [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeudet, hän voi käyttää **Kirjanpitäjä**-roolikeskusta. josta pääsee kätevästi kirjanpitäjän työssään eniten käyttämiin ikkunoihin.  

> [!NOTE]  
>  Tämä toiminto edellyttää, että kokemukseksi on valittu **Suite**. Lisätietoja on ohjeaiheessa [Financials-kokemuksen mukauttaminen](ui-experiences.md).  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a>Kirjanpitäjän kutsuminen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin
Ulkopuolisen kirjanpitäjän kutsumista on helpotettu [!INCLUDE[d365fin](includes/d365fin_md.md)]in uusimmassa versiossa. Avata vain **Käyttäjät**-ikkuna ja valitse sitten valintanauhassa **Kutsu ulkoinen kirjanpitäjä** -toiminto. Saat käyttöösi valmiin sähköpostiviestin, johon sinun tarvitsee vain lisätä kirjanpitäjän työsähköpostiosoite. Voit sitten lähettää kutsun.  

![Kirjanpitäjän kutsuminen](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
>  Kutsun lähettäminen, edellyttää, että SMTP-sähköposti on määritetty. Voit tehdä sen itse tai pyytää [!INCLUDE[d365fin](includes/d365fin_md.md)]-kumppania tekemään sen. Lisäksi sinun on kirjauduttava [!INCLUDE[d365fin](includes/d365fin_md.md)]iin käyttäjien järjestelmänvalvojana eikä liiketoiminnan omistajana tai muuna käyttäjänä.  

### <a name="separate-license"></a>Erillinen käyttöoikeus
Kirjanpitäjä lisätään taustalla Active Directory-vuokraajaan. Järjestelmänvalvoja voi varmistaa, että kirjanpitäjä hyväksyy kutsun ja että hänelle määritetään soveltuva käyttöoikeus. Tämä toimenpiteen tekeminen käytännössä määräytyy sen tilin mukaan, jolla [!INCLUDE[d365fin](includes/d365fin_md.md)]iin kirjaudutaan. Tämän ohjeaiheen ohjeet perustuvat Office 365 -tiliin, jossa on käytössä Microsoft Azure Active Directory.  

Jos olet aktivoinut [!INCLUDE[d365fin](includes/d365fin_md.md)]in tilauksen etkä käytä enää arviointiyritystä, sinulla on Azure Active Directory -vuokraaja. Järjestelmänvalvoja tai [!INCLUDE[d365fin](includes/d365fin_md.md)]-kumppanin hallitsee tätä vuokraajaa [Azure-portaalissa](https://portal.azure.com). Uudet käyttäjät lisätään tässä portaalissa. Myös käyttöoikeudet otetaan käyttöön ja poistetaan siellä. Lisätietoja on ohjeaiheessa [Microsoft Azure -portaalin yleiskatsaus](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

Yksi [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeustyypeistä on *ulkoisen kirjanpitäjän* käyttöoikeus. Tämä käyttöoikeustyyppi on tarkoitettu ulkoisen kirjanpitäjän kaltaisille käyttäjille. Tämä käyttöoikeustyyppi ei edellytä ylimääräisen asiakaskohtaisen käyttöoikeuden ostamista nykyiseen Active Directoryyn eikä nykyisen [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjätilin käyttöä ulkoiselle kirjanpitäjälle. Jos esimerkiksi nykyinen Office 365 -tilaus sisältää 10 [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjää ja käytät tällä hetkellä 10 *täyttä* käyttöoikeutta, järjestelmänvalvoja voi lisätä ulkoisen kirjanpitäjän vieraskäyttäjänä Azure-portaaliin ja määrittää kyseiselle käyttäjälle *ulkoisen kirjanpitäjän* käyttöoikeuden ilman lisäkustannuksia. *Ulkoisen kirjanpitäjän* käyttöoikeudet voi kuitenkin olla vain yhdellä käyttäjällä. Jos haluat lisätä enemmän käyttäjiä, Office 365 -tilausta on päivitettävä vastaavasti.  

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Toimintaohje: Sähköpostin määrittäminen manuaalisesti tai asetusten ohjatun määrityksen käyttäminen](madeira-how-setup-email.md)  
[Dynamics 365 for Financialsin kirjanpitäjän käyttökokemukset](finance-accounting.md)  
[Financials for Accountants on Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

