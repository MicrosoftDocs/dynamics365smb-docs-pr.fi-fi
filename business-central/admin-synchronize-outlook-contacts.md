---
title: Jaa kontaktit Business Centralin ja Outlookin välillä | Microsoft Docs
description: Palvelulla on laaja integrointi Office 365:n kanssa, jotta voit jakaa kontakteja Outlookin ja Business Centralin välillä.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Office 365
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: c28118ad9aa894678e4630800c638cf252c4f524
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307755"
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Business Centralin kontaktien synkronisointi Microsoft Outlookin yhteystietojen kanssa
Näet samat kontaktit [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa kuin Outlookissa, jos synkronointi määritetään. Esimerkiksi jos olet myyjä, sinun kannattaa tehdä joitakin töitä Outlookissa ja joitakin töitä [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä. Jos kontaktit ovat samat molemmissa, työ on yksinkertaisempaa.  

Kiinteä Outlook-kansio helpottaa yhteystietojen löytämistä ja voit asettaa suodattimen synkronoidaksesi vain ne kontaktit [!INCLUDE[d365fin](includes/d365fin_md.md)]:sta, jotka haluat nähdä Outlookissa. Kun yhteyshenkilön synkronointi on käytössä, voit aloittaa synkronoinnin manuaalisesti tai määrittää automaattisen synkronoinnin, joka säilyttää synkronoinnin aikataulun mukaisesti.  

## <a name="set-up-synchronization"></a>Synkronoinnin määritys
Määrität, miten haluat synkronoida Outlookin yhteystiedot [!INCLUDE[d365fin](includes/d365fin_md.md)]:n **Exchangen synkronointiasetukset** -sivulla. Tämä edellyttää, että [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjäprofiilissasi määritetään oma Office 365 -sähköpostitilisi. Voit tarkistaa tämän **Käyttäjät**-luettelossa oman käyttäjäprofiilisi **Office 365 -todennus** -osassa.  

Tarkista sitten **Exchangen synkronointiasetukset** -sivulla, että yhteys Exchangeen toimii ja määritä synkronointi. Avaa **Kontaktin synkronointiasetukset** -sivu ja käynnistä synkronointi. Voit myös asettaa suodattimen sille, mitkä kontaktit synkronoidaan [!INCLUDE[d365fin](includes/d365fin_md.md)]:n ja Outlookin välillä. Voit esimerkiksi asettaa suodattimen nimen, tyypin, yrityksen tai vastaavan tiedon perusteella. Voi myös muuttaa sen kansion oletusnimeä, johon yhteystiedot synkronoidaan Outlookissa. Oletusnimi on *Business Central*.  

Kun tämä synkronointi on määritetty, tekemäsi muutokset kontaktiin joko Outlookissa tai [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa synkronoidaan aina molempiin sovelluksiin.  

Kunkin työtovereistasi voi myös määrittää oman Exchange-synkronointinsa ja määrittää suodattimen sille, mitkä kontaktit halutaan synkronoida.  

## <a name="synchronize-contacts"></a>Kontaktien synkronointi
Jos olet tottunut käyttämään yhteyshenkilöitä [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa, sinun on helppo aloittaa synkronointi manuaalisesti aina, kun se sinulle sopii,  **Kontaktit**-luettelosta. Valitse vain **Synkronoi Office 365:n kanssa** -toiminto, ja päätä, haluatko muuttaa suodatinta, joka on määritetty. Kun valitset OK-painikkeen, synkronointi alkaa välittömästi ja uusimmat muutokset kohdistetaan Outlook-yhteystietoihisi.  

Voit **Kontaktit**-luettelossa synkronoida kontaktejasi kahdella tavalla:

* **Synkronoi Office 365:nn kanssa**

  Tämä toiminto synkronoi kaikki edellisen synkronoinnin jälkeiset muutokset [!INCLUDE[d365fin](includes/d365fin_md.md)]:sta Office 365:een viimeisimmän muokkauksen päivämäärän perusteella. Kaikki uudet yhteystiedot Office 365:ssä synkronoidaan myös takaisin [!INCLUDE[d365fin](includes/d365fin_md.md)]:een. Tämä on yleensä nopeampaa kuin täydellisen synkronoinnin suorittaminen.  

* **Täysi synkronointi Office 365:n kanssa**

  Tämä toiminto synkronoi kaikki yhteyshenkilöt molempiin suuntiin riippumatta viimeisen synkronoinnin päivämäärästä tai viimeksi muokattu -päivämäärästä.  

Molemmissa tapauksissa kontaktit synkronoidaan Outlookista vain jos niiden pakolliset kentät on täytetty. Pakolliset kentät  Office 365:een synkronointiin ovat **Nimi** ja **Sähköpostiosoite** ja kontaktien on oltava tyyppiä Henkilö. [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa on kontaktien päätiedot, joten [!INCLUDE[d365fin](includes/d365fin_md.md)] -yhteystiedot tallennetaan, jos kaksoiskappaleita esiintyy.  

Outlookissa kontaktit [!INCLUDE[d365fin](includes/d365fin_md.md)]:sta näytetään **Muut kontaktit** -kansiossa **Henkilöt**-näkymässä. Jos et tunne Outlookin Henkilöt-näkymää, pääset siihen siirtymisvaihtoehdoista Outlookin vasemmassa alakulmassa.  

## <a name="see-also"></a>Katso myös
[Käytön aloittaminen](product-get-started.md)  
[Rahoitus](finance.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Kontaktien (Henkilöt) käyttäminen Outlookin verkkoversiossa](https://support.office.com/en-us/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  
