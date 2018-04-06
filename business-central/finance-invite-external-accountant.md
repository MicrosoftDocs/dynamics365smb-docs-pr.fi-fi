---
title: "Ulkoisen kirjanpitäjän lisääminen Financialsiin | Microsoft Docs"
description: "Lisätietoja ulkoisen kirjanpitäjän kutsumisesta Business Central -sovellukseen."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a252b967e910cb16179ef33fc9ec5e6b976056a7
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="inviting-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Ulkoisen kirjanpitäjän kutsuminen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin
Jos käytä ulkoista kirjanpitäjää kirjojen ja talousraportoinnin hallinnassa, voit kutsua kirjanpitäjän [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, jolloin he saavat käyttöönsä kirjanpitotietosi.

Kun kirjanpitäjä on saanut [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeudet, hän voi käyttää **Kirjanpitäjä**-roolikeskusta. josta pääsee kätevästi kirjanpitäjän työssään eniten käyttämiin ikkunoihin.  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a>Kirjanpitäjän kutsuminen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin
Ulkopuolisen kirjanpitäjän kutsumista on helpotettu [!INCLUDE[d365fin](includes/d365fin_md.md)]in uusimmassa versiossa. Avata vain **Käyttäjät**-ikkuna ja valitse sitten valintanauhassa **Kutsu ulkoinen kirjanpitäjä** -toiminto. Saat käyttöösi valmiin sähköpostiviestin, johon sinun tarvitsee vain lisätä kirjanpitäjän työsähköpostiosoite. Voit sitten lähettää kutsun.  

![Kirjanpitäjän kutsuminen](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
>  Kutsun lähettäminen, edellyttää, että SMTP-sähköposti on määritetty. Voit tehdä sen itse tai pyytää [!INCLUDE[d365fin](includes/d365fin_md.md)]-kumppania tekemään sen. Lisäksi sinun on kirjauduttava [!INCLUDE[d365fin](includes/d365fin_md.md)]iin käyttäjien järjestelmänvalvojana eikä liiketoiminnan omistajana tai muuna käyttäjänä. Lopuksi sinun on jätettävä kokeiluyritys, jotta sinulla on Azure Active Directoryn järjestelmänvalvoja.  

> [!IMPORTANT]  
>  Kirjanpitäjän sähköpostiosoitteen on oltava Active Directoryyn perustuva työsähköpostiosoite. Jos kirjanpitäjä käyttää jotakin muuta sähköpostityyppiä, kutsua ei voi lähettää.  

### <a name="separate-license"></a>Erillinen käyttöoikeus
Kirjanpitäjä lisätään taustalla Active Directory-vuokraajaan. Järjestelmänvalvoja voi varmistaa, että kirjanpitäjä hyväksyy kutsun ja että hänelle määritetään soveltuva käyttöoikeus. Tämä toimenpiteen tekeminen käytännössä määräytyy sen tilin mukaan, jolla [!INCLUDE[d365fin](includes/d365fin_md.md)]iin kirjaudutaan. Tämän ohjeaiheen ohjeet perustuvat Office 365 -tiliin, jossa on käytössä Microsoft Azure Active Directory.  

Jos olet aktivoinut [!INCLUDE[d365fin](includes/d365fin_md.md)]in tilauksen etkä käytä enää arviointiyritystä, sinulla on Azure Active Directory -vuokraaja. Järjestelmänvalvoja tai [!INCLUDE[d365fin](includes/d365fin_md.md)]-kumppanin hallitsee tätä vuokraajaa [Azure-portaalissa](https://portal.azure.com). Uudet käyttäjät lisätään tässä portaalissa. Myös käyttöoikeudet otetaan käyttöön ja poistetaan siellä. Lisätietoja on ohjeaiheessa [Microsoft Azure -portaalin yleiskatsaus](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

Yksi [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeustyypeistä on *ulkoisen kirjanpitäjän* käyttöoikeus. Tämä käyttöoikeustyyppi on tarkoitettu ulkoisen kirjanpitäjän kaltaisille käyttäjille. Tämä käyttöoikeustyyppi ei edellytä ylimääräisen asiakaskohtaisen käyttöoikeuden ostamista nykyiseen Active Directoryyn eikä nykyisen [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjätilin käyttöä ulkoiselle kirjanpitäjälle. Jos esimerkiksi nykyinen Office 365 -tilaus sisältää 10 [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjää ja käytät tällä hetkellä 10 *täyttä* käyttöoikeutta, järjestelmänvalvoja voi lisätä ulkoisen kirjanpitäjän vieraskäyttäjänä Azure-portaaliin ja määrittää kyseiselle käyttäjälle *ulkoisen kirjanpitäjän* käyttöoikeuden ilman lisäkustannuksia. *Ulkoisen kirjanpitäjän* käyttöoikeudet voi kuitenkin olla vain yhdellä käyttäjällä. Jos haluat lisätä enemmän käyttäjiä, Office 365 -tilausta on päivitettävä vastaavasti.  

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Sähköpostin määrittäminen manuaalisesti tai asetusten ohjatun määrityksen käyttäminen](admin-how-setup-email.md)  
[Kirjanpitäjän käyttökokemukset Business Central -sovelluksessa](finance-accounting.md)  
[Business Central Microsoft.com-sivustossa](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

