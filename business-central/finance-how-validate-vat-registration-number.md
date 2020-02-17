---
title: ALV-rekisterinumeron vahvistaminen | Microsoft-dokumentit
description: ALV-rekisterinumeron vahvistaminen
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 01/06/2020
ms.author: andregu
ms.openlocfilehash: f4d5023acba2e0cc5600b3f6675c3dcc325489d7
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992219"
---
# <a name="validate-a-vat-registration-number"></a>ALV-rekisterinumeron vahvistaminen

## <a name="to-verify-vat-registration-numbers"></a>ALV-numeroiden tarkistaminen
On tärkeää, että käytössäsi olevat asiakkaiden, toimittajien ja yhteystietojen ALV-rekisteröintinumerot ovat oikeita. Yritykset esimerkiksi joskus muuttavat verovelkatilaansa, ja joissakin maissa veroviranomaiset voivat pyytää raportteja, kuten EU-myyntiluetteloraportin, joissa on luettelo liiketoiminnassasi käyttämistäsi ALV-rekisteröintinumeroista.

Euroopan komission sivustossa on julkinen ja maksuton ALV-tietojen vaihtojärjestelmä (VIES-palvelu). [!INCLUDE[d365fin](includes/d365fin_md.md)]ia käytettäessä sivustoon siirtyminen ei ole tarpeellista, sillä voit tarkistaa sovelluksessa VIES-palvelusta asiakkaiden, toimittajien ja yhteystietojen ALV-numerot asiakkaan, toimittajan ja yhteystiedon kortista. Voit myös seurata kyseisiä ALV-numeroita. [!INCLUDE[d365fin](includes/d365fin_md.md)]in palvelun nimi on **EU:n ALV-nron tarkistuspalvelun määritys**. Palvelua voi käyttää **Palvelun yhteydet** -sivulla ja sen käytön voi aloittaa heti. Palveluyhteys on maksuton eikä kirjautumista tarvita.

Ota **EU:n ALV-rekisterinumeron vahvistuspalvelu** käyttöön avaamalla tapahtuma **Huoltoyhteys**-sivulla. **Palvelun päätepiste** -kentän tulisi olla jo täytetty. Jos ei ole, voit käyttää **Määritä oletuspäätepiste** -toimintoa. Aseta **Käytössä**-kenttä ja olet valmis.

> [!Note]
> Voit ottaa käyttöön EU:n ALV-nron tarkistuspalvelun, jos sinulla on järjestelmänvalvojan käyttöoikeudet.

Kun käytät palveluyhteyttä, kunkin asiakkaan, toimittajan tai yhteystiedon ALV-numeroiden ja tarkistusten historiatiedot kirjataan **ALV-rekisteröintilokiin**, joten niiden seuraaminen on helppoa. Loki on asiakaskohtainen. Lokin avulla voi esimerkiksi kätevästi todistaa, että olet tarkistanut nykyisen ALV-numeron oikeellisuuden. Kun tarkistat ALV-numeron, lokin **Pyynnön tunnus** -sarake osoittaa, että olet tehnyt niin.

Voit tarkastella ALV-rekisteröintilokia asiakkaan, toimittajan tai kontaktin kortissa valitsemalla **Laskutus**-pikavälilehdessä **ALV-rekisterinro** -kentässä hakupainikkeen.  

Palvelu voi myös säästää aikaa asiakasta tai toimittajaa luotaessa. Jos tiedät asiakkaan ALV-numeron, voit antaa sen asiakkaan tai toimittajan kortin **ALV-rekisterinro** -kentässä, jolloin asiakkaan nimi täytetään valmiiksi. Joissakin maissa myös yrityksen osoitteet ilmoitetaan jäsennetyssä muodossa. Näissä maissa myös osoitetiedot täytetään valmiiksi.  

ALV-tietojen vaihtojärjestelmästä (VIES-palvelusta) on hyvä muistaa pari asiaa:

* Palvelu käyttää http-protokollaa, joten palvelun kautta siirretyt tiedot eivät ole salattuja.  
* Palvelu voi olla ajoittain pois käytöstä Microsoftista riippumattomista syistä. Palvelu on osa EU:n laajaa kansallisten ALV-rekisterien verkostoa.

## <a name="see-also"></a>Katso myös  
[Määritä arvonlisävero](finance-setup-vat.md)  
[Ei-realisoituneen arvonlisäveron määrittäminen](finance-setup-unrealized-vat.md)      
[ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  
[Business Centralin paikalliset toiminnot](about-localization.md)
