---
title: Ongelmien määritys- ja ratkaisutavat | Microsoft Docs
description: Lisätietoja Dynamics 365:n Accountant Hubin ongelmien ratkaisemisesta.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.openlocfilehash: 0ebd99e9097e4c701038f3b8be7a07d1e80a4b31
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795789"
---
# <a name="troubleshooting-include-d365acclongincludesd365acclongmdmd"></a>[!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]in vianmääritys
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

[!INCLUDE [d365acc](includes/d365acc_md.md)]iin rekisteröityminen on helppoa ja nopeaa. Vaikka asiakkaiden lisääminen koontinäyttöön on helppoa, tässä artikkelissa käsitellään mahdollisesti esiin tulevia ongelmia.

## <a name="what-email-address-can-i-use-with-include-d365accincludesd365accmdmd"></a>Mitä sähköpostiosoitetta käytetään [!INCLUDE [d365acc](includes/d365acc_md.md)]in kanssa?
[!INCLUDE [d365acc](includes/d365acc_md.md)] edellyttää kirjautumista työ- tai opiskelupaikan antamalla sähköpostiosoitteella. [!INCLUDE [d365acc](includes/d365acc_md.md)] ei tue kuluttajille tarkoitettujen sähköpostipalveluiden ja tietoliikennepalveluiden tarjoajien sähköpostiosoitteita. Näitä ovat esimerkiksi outlook.com, hotmail.com ja gmail.com.  

Jos yrität rekisteröityä käyttämällä henkilökohtaista sähköpostiosoitetta, saat viestin, jossa pyydetään käyttämään työ- tai opiskelupaikan antamaa sähköpostiosoitetta.  

## <a name="why-cant-i-connect-to-my-clients-data"></a>Miksi en voi muodostaa yhteyttä asiakkaani tietoihin?
Syy voi olla esimerkiksi jokin seuraavista:

- **Asiakkaan URL-osoite** -kentässä annettu URL-osoite ei kelpaa  

  Valitse **Asiakkaiden hallinta** ja avaa asiakas, johon et voi muodostaa yhteyttä. Valitse sitten **Testaa asiakkaan URL-osoite**.  
- Asiakkaan yritys on offline-tilassa esimerkiksi päivityksen vuoksi

  Valitse koontinäytössä ensin **Työkalut**-valikkovaihtoehto ja sitten **Tarkista virheet**. Jos avautuvassa teknisten tietojen luettelossa näkyy virheitä, järjestelmänvalvojaan on ehkä syytä ottaa yhteyttä. Jos virhesanoma esimerkiksi ilmoittaa, että palvelin on hylännyt asiakkaan tunnistetiedot, syynä on todennäköisesti puuttuvat käyttöoikeudet.  
- Et ole saanut asiakkaalta [!INCLUDE [d365fin](includes/d365fin_md.md)]:n käyttäjäksi kutsuvaa sähköpostiviestiä, et ole avannut sähköpostissa olevaa linkkiä tai et ole hyväksynyt kutsua

  Sinun on avattava kutsussa oleva linkki ja hyväksyttävä vaiheet, joilla sinut lisätään asiakkaan [!INCLUDE [d365fin](includes/d365fin_md.md)]:een. Pääset käyttämään asiakkaan tietoja vasta tämän jälkeen.  
- Sinulla ei ole kaikkien asiakkaan [!INCLUDE [d365fin](includes/d365fin_md.md)]:n yritysten käyttöoikeutta

  Asiakkaalla voi olla [!INCLUDE [d365fin](includes/d365fin_md.md)]:ssä useita liiketoimintayksiköitä tai yrityksiä, eivätkä kaikki yritykset aina sisälly kutsuun. Varmista yhdessä asiakkaan kanssa, että sinulla on kaikkien niiden yritysten käyttöoikeudet, joita asiakas haluaa sinun käsittelevän.  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a>Miksi koontinäytön tiedot eivät päivity?
Kun lisäät asiakkaat tai pyydät tietojen päivittämistä, [!INCLUDE [d365acc](includes/d365acc_md.md)] noutaa tiedot. Sinun on kuitenkin päivitettävä sivu itse valitsemalla esimerkiksi Näytä kaikki yritykset uudelleen -toiminnon, päivittämällä selaimen sivu tai poistumalla koontinäytöstä ja palaamalla siihen takaisin. Tämä on tunnettu ongelma, jota korjataan parhaillaan myöhempää päivitystä varten.  

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365acc](includes/d365acc_md.md)]in käytön aloittaminen](get-started.md)  
[Asiakkaiden lisääminen [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)in koontinäyttöön  
