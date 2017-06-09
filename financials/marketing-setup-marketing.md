---
title: "Kontaktienhallinnan määrittäminen | Microsoft Docs"
description: "Tässä artikkelissa kerrotaan markkinoinnin ja kontaktienhallinta määrittämisestä Financialsissa"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, client, customer, campaign, promo
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ba5ed3df4ddbf39863509528a667848015312ab0
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-relationship-management"></a>Kontaktienhallinnan määrittäminen
Ennen kuin aloitat kontaktien ja markkinoinnin käsittelemisen, määritä, miten markkinoinnissa hallitaan tiettyjä kontakteihin liittyviä asioita. Voit määrittää esimerkiksi sen, synkronoidaanko kontaktin kortti asiakkaan, toimittajan vai pankkitilin kortin kanssa, miten numerosarjat määritetään tai millainen vakiotervehdys kontakteille lähetetään.

Kontaktien hallinta ja strategian luominen asiakkaiden tunnistamiseksi, houkuttelemiseksi ja säilyttämiseksi auttaa liiketoiminnan optimoinnissa ja asiakastyytyväisyyden parantamisessa. Hyvän kontaktienhallintajärjestelmän käyttäminen auttaa myös asiakassuhteiden luomisessa ja ylläpitämisessä. Tärkein tekijä asiakassuhteissa on yhteydenpito. Yrityksen menestyksen kannalta on keskeistä, että yhteydenpito mahdollisiin ja olemassa oleviin asiakkaisiin, toimittajiin ja liikekumppaneihin pystytään mukauttamaan kulloisinkiin tarpeisiin. Strategian muodostaminen ja yhteystietojen käytön määrittäminen on ensimmäinen vaihe. Näitä tietoja tarkastelevat useat yrityksen ryhmät, joten hyvän järjestelmän avulla jokainen käyttäjä voi lisätä tuottavuuttaan.

Voit määrittää markkinoinnin ja kontaktien hallinnan **Kontaktienhallinnan asetukset** -ikkunassa. Voit avata **Kontaktienhallinnan asetukset** -ikkunan valitsemalla oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvakkeen ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoittamalla **Kontaktienhallinnan asetukset** ja valitsemalla sitten liittyvän linkin.

## <a name="automatically-copy-specific-information-from-the-contact-companies-to-the-contact-persons"></a>Tiettyjen tietojen kopioiminen automaattisesti kontaktiyrityksistä kontaktihenkilöille
Jotkin kontaktiyritysten tiedoista ovat samat kuin tämän yrityksen kontaktihenkilön tiedot, esimerkiksi osoitetiedot. Voit määrittää **Kontaktienhallinnan asetukset** -ikkunan **Periytyminen**-osassa sovelluksen, joka kopioi automaattisesti tietyt kentät kontaktiyrityksen kortista kontaktihenkilön korttiin aina, kun luot kontaktiyritykseen kontaktihenkilön. Voit esimerkiksi kopioida myyjän koodin, osoitetiedot (osoite, osoite 2, postinumero ja maa), yhteystiedot (faksinumero, teleksivastaus ja puhelinnumero) ja muita tietoja.

Kun muutat yhtä näistä kentistä kontaktiyrityksen kortilla, ohjelma muuttaa kenttää automaattisesti kontaktihenkilön kortilla (jos et ole manuaalisesti muuttanut kenttää kontaktihenkilön kortilla).

Lisätietoja on kohdassa [Toimintaohje: Kontaktihenkilöiden luominen](marketing-how-create-contact-persons.md).

## <a name="use-predefined-defaults-on-new-contacts"></a>Ennalta määritettyjen oletusarvojen käyttäminen uusissa kontakteissa
Voit päättää, että sovellus liittää automaattisesti tietyn kielikoodin, territoriokoodin, myyjäkoodin ja maa-/aluekoodin oletusarvon jokaiseen luomaasi uuteen kontaktiin. Voit myös syöttää myyntisyklin koodin oletusarvon, jonka ohjelma sitten liittää jokaiseen luomaasi uuteen mahdollisuuteen.

Kenttien periytyminen syrjäyttää määrittämäsi oletusarvot. Jos olet esimerkiksi määrittänyt englannin oletuskieleksi, mutta kontaktiyrityksen kieli on saksa, ohjelma liittää automaattisesti saksan kielikoodin yrityksen kontaktihenkilölle.

<!--You can also setup a default salutation that the program automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, the program will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-record-interactions"></a>Vuorovaikutusten tallentaminen automaattisesti
[!INCLUDE[d365fin](includes/d365fin_md.md)] voi tallentaa myynti- ja ostoasiakirjoja (esimerkiksi tilauksia, laskuja ja vastaanottoja) automaattisesti vuorovaikutukseksi, samoin sähköpostiviestejä, puhelinkeskusteluja ja kansilehtiä.

Lisätietoja on kohdassa [Kontaktien kanssa tapahtuvien vuorovaikutusten tallentaminen automaattisesti](marketing-auto-record-interactions.md).

## <a name="synchronize-contacts-with-customers-and-more"></a>Kontaktien synkronoiminen esimerkiksi asiakkaiden kanssa
Kun haluat synkronisoida kontaktikortin asiakas-, toimittaja- ja pankkitilikortin kanssa, sinun täytyy valita liikesuhdekoodi asiakkaille, toimittajille ja pankkitileille. Voit esimerkiksi linkittää kontaktin olemassa olevaan asiakkaaseen vain, jos olet valinnut asiakkaille liikesuhdekoodin **Kontaktienhallinnan asetukset** -ikkunassa.

Lisätietoja on kohdassa [Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-synchronize-contacts-customers-vendors-bank-accounts.md).

## <a name="assign-a-number-series-to-contacts-and-opportunities"></a>Numerosarjojen liittäminen kontakteihin ja mahdollisuuksiin
Voit määrittää numerosarjan kontakteille ja mahdollisuuksille. Jos olet määrittänyt numerosarjat kontakteille kontaktin luomisen yhteydessä, ja painat Enter-näppäintä kontaktin kortin Nro-kentässä, ohjelma syöttää automaattisesti seuraavan käytettävissä olevan kontaktinumeron.

Lisätietoja numerosarjoista on kohdassa [Numerosarjojen luominen](ui-create-number-series.md).

## <a name="search-for-duplicate-contacts-when-contacts-are-created"></a>Kontaktien kopioiden etsiminen kontaktien luomisen yhteydessä
Voit valita, että ohjelma hakee kopioita automaattisesti aina kun luot kontaktiyrityksen; tai voit valita, että haet kopioita manuaalisesti kontaktien luomisen jälkeen. Voit myös valita, että ohjelma päivittää hakumerkkijonot automaattisesti aina kun muutat kontaktin tietoja tai luot uuden kontaktin. Voit päättää Haun osuma-%:in, siis sen identtisten merkkijonojen prosenttiosuuden, joka kahdella kontaktilla täytyy olla, jotta ohjelma tulkitsee ne kopioiksi.

## <a name="set-up-email-logging"></a>Sähköpostin lokiinkirjauksen määrittäminen
Voit vaihtaa sähköpostiviestejä kontaktien, asiakkaiden, toimittajien ja niin edelleen kanssa. Voit lähettää ja vastaanottaa sähköposteja sovelluksesta tai Outlookista. Ennen kuin voit vaihtaa viestejä tällä tavalla ja saada järjestelmän tallentamaan ne ja asettamaan ne jonoon, sinun on määritettävä joitakin parametreja, kuten esimerkiksi aikavälin, jolloin ohjelma tarkistaa, onko sähköposteja odottamassa käsittelyä, sähköpostin kirjaamisen profiilinimi ja niin edelleen.

## <a name="see-also"></a>Katso myös
[Kontaktien hallinta](marketing-contacts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  

