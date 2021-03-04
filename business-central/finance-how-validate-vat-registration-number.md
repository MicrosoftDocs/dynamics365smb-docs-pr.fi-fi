---
title: ALV-rekisterinumeroiden vahvistaminen
description: Anna Business Centralin käyttää VIES-palvelua ALV-rekisterinumeroiden vahvistamiseen automaattisesti.
author: kielkenny
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 10/01/2020
ms.author: andregu
ms.openlocfilehash: 80e955e96a64c5a0bd91d0a72297b32d67ff4ab6
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750554"
---
# <a name="validate-vat-registration-numbers"></a>ALV-rekisterinumeroiden vahvistaminen

On tärkeää, että käytössäsi olevat asiakkaiden, toimittajien ja yhteystietojen ALV-rekisteröintinumerot ovat oikeita. Yritykset esimerkiksi joskus muuttavat verovelkatilaansa, ja joissakin maissa veroviranomaiset voivat pyytää raportteja, kuten EU-myyntiluetteloraportin, joissa on luettelo liiketoiminnassasi käyttämistäsi ALV-rekisteröintinumeroista.

Euroopan komission sivustossa on julkinen ja maksuton ALV-tietojen vaihtojärjestelmä (VIES-palvelu). [!INCLUDE[prod_short](includes/prod_short.md)]ia käytettäessä sivustoon siirtyminen ei ole tarpeellista, sillä voit tarkistaa sovelluksessa VIES-palvelusta asiakkaiden, toimittajien ja yhteystietojen ALV-numerot asiakkaan, toimittajan ja yhteystiedon kortista. Voit myös seurata kyseisiä ALV-numeroita. [!INCLUDE[prod_short](includes/prod_short.md)]in palvelun nimi on **EU:n ALV-nron tarkistuspalvelun määritys**. Palvelua voi käyttää **Palvelun yhteydet** -sivulla ja sen käytön voi aloittaa heti. Palveluyhteys on maksuton eikä rekisteröitymistä tarvita.

## <a name="to-verify-vat-registration-numbers"></a>ALV-numeroiden tarkistaminen

Ota **EU:n ALV-rekisterinumeron vahvistuspalvelu** käyttöön avaamalla tapahtuma **Huoltoyhteys**-sivulla. **Palvelun päätepiste** -kentän tulisi olla jo täytetty. Jos ei ole, voit käyttää **Määritä oletuspäätepiste** -toimintoa. Aseta **Käytössä**-kenttä ja olet valmis.

> [!NOTE]
> Voit ottaa käyttöön EU:n ALV-nron tarkistuspalvelun, jos sinulla on järjestelmänvalvojan käyttöoikeudet.

Kun käytät palveluyhteyttä, kunkin asiakkaan, toimittajan tai yhteystiedon ALV-numeroiden ja tarkistusten historiatiedot kirjataan **ALV-rekisteröintilokiin**, joten niiden seuraaminen on helppoa. Loki on asiakaskohtainen. Lokin avulla voi esimerkiksi kätevästi todistaa, että olet tarkistanut nykyisen ALV-numeron oikeellisuuden. Kun tarkistat ALV-numeron, lokin **Pyynnön tunnus** -sarake osoittaa, että olet tehnyt niin.

Voit tarkastella ALV-rekisteröintilokia asiakkaan, toimittajan tai kontaktin kortissa valitsemalla **Laskutus**-pikavälilehdessä **ALV-rekisterinro** -kentässä hakupainikkeen.  

Palvelu voi myös säästää aikaa asiakasta tai toimittajaa luotaessa. Jos tiedät asiakkaan ALV-numeron, voit antaa sen asiakkaan tai toimittajan kortin **ALV-rekisterinro** -kentässä, jolloin asiakkaan nimi täytetään valmiiksi. Joissakin maissa myös yrityksen osoitteet ilmoitetaan jäsennetyssä muodossa. Näissä maissa myös osoitetiedot täytetään valmiiksi.  

ALV-tietojen vaihtojärjestelmästä (VIES-palvelusta) on hyvä muistaa pari asiaa:

* Palvelu käyttää http-protokollaa, joten palvelun kautta siirretyt tiedot eivät ole salattuja.  
* Palvelu voi olla ajoittain pois käytöstä Microsoftista riippumattomista syistä. Palvelu on osa EU:n laajaa kansallisten ALV-rekisterien verkostoa.

> [!IMPORTANT]
> Sinun vastuullasi on tarkistaa, että tiedot ovat voimassa. Toisinaan VIES-ohjelman ALV-numeron vahvistuspalvelu palauttaa virheitä sisältävät tiedot. Jos vahvistus epäonnistuu, tarkista [sivuston](https://ec.europa.eu/taxation_customs/vies/) ALV-rekisterinumerot, tulosta tulos tai tallenna se jaettuun sijaintiin ja lisää sitten linkki asiakkaan, toimittajan tai kontaktin tietueeseen. Lue lisätietoja kohteesta [Korttien ja asiakirjojen liitteiden, linkkien ja muistioiden hallinta](ui-how-add-link-to-record.md)

## <a name="see-also"></a>Katso myös

[Määritä arvolisävero](finance-setup-vat.md)  
[Ei-realisoituneen arvonlisäveron määrittäminen](finance-setup-unrealized-vat.md)  
[ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  
[Business Centralin paikalliset toiminnot](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]