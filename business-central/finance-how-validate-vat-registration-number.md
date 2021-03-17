---
title: ALV-rekisterinumeroiden vahvistaminen
description: Anna Business Centralin vahvistaa ALV-rekisterinumerot ja muut yrityksen tiedot kontakteillesi, asiakkaillesi ja toimittajillesi Euroopan unionin VIES ALV -numeron validointipalvelun perusteella.
author: andregu
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.reviewer: edupont
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 02/25/2021
ms.author: andregu
ms.openlocfilehash: 867ae5e726de5f2f78e4862a2d8c55dbc3d43ca0
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5492915"
---
# <a name="validate-vat-registration-numbers"></a>ALV-rekisterinumeroiden vahvistaminen

On tärkeää, että käytössäsi olevat asiakkaiden, toimittajien ja yhteystietojen ALV-rekisteröintinumerot ovat oikeita, jos käytät [!INCLUDE [prod_short](includes/prod_short.md)]ia maassa/alueella, joka käyttää arvonlisäveroa. Yritykset esimerkiksi joskus muuttavat verovelkatilaansa, ja joissakin maissa veroviranomaiset voivat pyytää raportteja, kuten **EU-myyntiluettelo**-raportin, joissa on luettelo liiketoiminnassasi käyttämistäsi ALV-rekisteröintinumeroista.

Euroopan komission sivustossa on julkinen ja maksuton ALV-tietojen vaihtojärjestelmä (VIES-palvelu). [!INCLUDE [prod_short](includes/prod_short.md)]ia käytettäessä sivustoon siirtyminen ei ole tarpeellista, sillä voit tarkistaa sovelluksessa VIES-palvelusta asiakkaiden, toimittajien ja yhteystietojen ALV-numerot ja muut tiedot. [!INCLUDE [prod_short](includes/prod_short.md)]in palvelun nimi on **EU:n ALV-nron tarkistuspalvelun määritys**. Palvelua voi käyttää **Palvelun yhteydet** -sivulla ja sen käytön voi aloittaa heti. Palveluyhteys on maksuton eikä lisärekisteröitymistä tarvita.

## <a name="configure-the-service-to-verify-vat-registration-numbers-automatically"></a>Määritä palvelu tarkistamaan ALV-rekisterinumerot automaattisesti

Ota **EU:n ALV-rekisterinumeron vahvistuspalvelu** käyttöön avaamalla tapahtuma **Palveluyhteys**-sivulla. Jos **palvelun päätepiste** -kenttää ei ole vielä täytetty, käytä **Aseta oletuspäätepiste** -toimintoa. Aseta **Käytössä**-kenttä ja olet valmis.  

> [!IMPORTANT]
> Voit ottaa tarkistuspalvelun käyttöön, jos sinulla on järjestelmänvalvojan käyttöoikeudet.

Vaihtoehtoisesti voit määrittää malleja niiden ALV-tietojen tyypeille, jotka haluat palvelun myös tarkistavan. Lisätietoja on kohdassa [Tarkistusmallit](#validation-templates).

Kun käytät palveluyhteyttä, kunkin asiakkaan, toimittajan tai yhteystiedon ALV-numeroiden ja tarkistusten historiatiedot kirjataan **ALV-rekisteröintilokiin**, joten niiden seuraaminen on helppoa. Loki on asiakaskohtainen. Lokin avulla voi esimerkiksi kätevästi todistaa, että olet tarkistanut nykyisen ALV-numeron oikeellisuuden. Kun tarkistat ALV-numeron, lokin **Pyynnön tunnus** -sarake osoittaa, että olet tehnyt niin.

Voit tarkastella ALV-rekisteröintilokia asiakkaan, toimittajan tai kontaktin kortissa valitsemalla **Laskutus**-pikavälilehdessä **ALV-rekisterinro** -kentässä hakupainikkeen.  

ALV-tietojen vaihtojärjestelmästä (VIES-palvelusta) on hyvä muistaa pari asiaa:

* Palvelu käyttää http-protokollaa, joten palvelun kautta siirretyt tiedot eivät ole salattuja.  
* Palvelu voi olla ajoittain pois käytöstä Microsoftista riippumattomista syistä. Palvelu on osa EU:n laajaa kansallisten ALV-rekisterien verkostoa.

> [!IMPORTANT]
> Sinun vastuullasi on tarkistaa, että tiedot ovat voimassa. Toisinaan VIES-ohjelman ALV-numeron vahvistuspalvelu palauttaa virheitä sisältävät tiedot. Jos vahvistus epäonnistuu, tarkista [sivuston](https://ec.europa.eu/taxation_customs/vies/) ALV-rekisterinumerot, tulosta tulos tai tallenna se jaettuun sijaintiin ja lisää sitten linkki asiakkaan, toimittajan tai kontaktin tietueeseen. Lue lisätietoja kohteesta [Korttien ja asiakirjojen liitteiden, linkkien ja muistioiden hallinta](ui-how-add-link-to-record.md)

## <a name="validation-templates"></a>Tarkistusmallit

[!INCLUDE [2020rw_online_only](includes/2020rw_online_only.md)]

Voit käyttää VIES-palvelua myös muiden yritystietojen, kuten osoitteen, sekä ALV-rekisterinumeron tarkastamiseen. **ALV-rekisterinumeron tarkistusmallit** -sivulla voit luoda merkinnän kullekin maalle/alueelle, jolle haluat lisätarkistuksen, ja määrittää sitten tiedot, jotka tarkistetaan automaattisesti.  

Lisää esimerkiksi tapahtuma Espanjalle, jolle haluat hakea nimen, kadun, paikkakunnan ja postinumeron, ja sitten toisen tapahtuman Saksalle, jossa haluat esimerkiksi tarkistuksen postinumerolle. Määritä sitten **EU:n ALV-rekisteröintinumeron tarkistuspalvelun asetukset** -sivulla oletusmalli.  

> [!NOTE]
> Varmista aina, että oletusmalli toimii tarpeidesi mukaan. Voit muuttaa oletusarvoa vastaamaan tarpeitasi, esimerkiksi tarkistaa kaikki kentät tai ei mitään kenttiä.

Kun seuraavan kerran määrität ALV-rekisterinumeron, palvelu tarkistaa numeron ja kaikki tarkistusmallien määrittämät lisätiedot. Jos määritetyt arvot poikkeavat palvelun palauttamasta arvosta, tiedot näkyvät **Tarkistustiedot**-sivulla, jossa voit hyväksyä tai nollata arvot.  

## <a name="see-also"></a>Katso myös

[Määritä arvolisävero](finance-setup-vat.md)  
[Ei-realisoituneen arvonlisäveron määrittäminen](finance-setup-unrealized-vat.md)  
[ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  
[Business Centralin paikalliset toiminnot](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
