---
title: Markkinoinnin ja kontaktien hallinnan tietojen määrittäminen
description: Voit määrittää markkinoinnin ja kontaktien hallinnan Business Centralissa optimoimaan prospektien tai asiakkaiden suhteita sekä parantamaan kampanjoita ja tarjouksia.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'relationship, prospect, client, customer, campaign, promo'
ms.search.forms: '5172, 5173, 5170, 5094, 429'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="setting-up-relationship-management"></a>Kontaktienhallinnan määrittäminen

Ennen kuin aloitat kontaktien ja markkinoinnin käsittelemisen, määritä, miten markkinoinnissa hallitaan tiettyjä kontakteihin liittyviä asioita. Voit määrittää esimerkiksi sen, synkronoidaanko kontaktin kortti asiakkaan, toimittajan vai pankkitilin kortin kanssa, miten numerosarjat määritetään tai millainen vakiotervehdys kontakteille lähetetään.

Kontaktien hallinta ja strategian luominen asiakkaiden tunnistamiseksi, houkuttelemiseksi ja säilyttämiseksi auttaa liiketoiminnan optimoinnissa ja asiakastyytyväisyyden parantamisessa. Hyvän kontaktienhallintajärjestelmän käyttäminen auttaa myös asiakassuhteiden luomisessa ja ylläpitämisessä. Tärkein tekijä asiakassuhteissa on yhteydenpito. Yrityksen menestyksen kannalta on keskeistä, että yhteydenpito mahdollisiin ja olemassa oleviin asiakkaisiin, toimittajiin ja liikekumppaneihin pystytään mukauttamaan kulloisinkiin tarpeisiin. Strategian muodostaminen ja yhteystietojen käytön määrittäminen on ensimmäinen vaihe. Näitä tietoja tarkastelevat useat yrityksen ryhmät, joten hyvän järjestelmän avulla jokainen käyttäjä voi lisätä tuottavuuttaan.

Voit määrittää markkinoinnin ja kontaktien hallinnan **Kontaktienhallinnan asetukset** -sivulla. Avataksesi **Kontaktienhallinnan asetukset** -sivun valitse ![Kerro-ominaisuuden avaava hehkulamppu.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kontaktienhallinnan asetukset** ja valitse sitten vastaava linkki.

## <a name="automatically-copying-specific-information-from-contact-companies-to-contact-persons"></a>Tiettyjen tietojen kopioiminen automaattisesti kontaktiyrityksistä kontaktihenkilöille
Jotkin kontaktiyritysten tiedoista ovat samat kuin tämän yrityksen kontaktihenkilön tiedot, esimerkiksi osoitetiedot. Voit määrittää **Kontaktienhallinnan asetukset** -sivun **Periytyminen**-osassa sovelluksen, joka kopioi automaattisesti tietyt kentät kontaktiyrityksen kortista kontaktihenkilön korttiin aina, kun luot kontaktiyritykseen kontaktihenkilön. Voit esimerkiksi kopioida myyjän koodin, osoitetiedot (osoite, osoite 2, postinumero ja maa), yhteystiedot (faksinumero, teleksivastaus ja puhelinnumero) ja muita tietoja.

Kun muutat yhtä näistä kentistä kontaktiyrityksen kortilla, sovellus muuttaa kenttää automaattisesti kontaktihenkilön kortilla (jos et ole manuaalisesti muuttanut kenttää kontaktihenkilön kortilla).

Lisätietoja on kohdassa [Kontaktien luominen](marketing-create-contact-companies.md).

## <a name="use-predefined-defaults-on-new-contacts"></a>Ennalta määritettyjen oletusarvojen käyttäminen uusissa kontakteissa
Voit päättää, että sovellus liittää automaattisesti tietyn kielikoodin, territoriokoodin, myyjäkoodin ja maa-/aluekoodin oletusarvon jokaiseen luomaasi uuteen kontaktiin. Voit myös antaa myyntisyklin oletuskoodin, jonka sovellus sitten liittää jokaiseen luomaasi uuteen mahdollisuuteen.

Kenttien periytyminen syrjäyttää määrittämäsi oletusarvot. Jos olet esimerkiksi määrittänyt englannin oletuskieleksi, mutta kontaktiyrityksen kieli on saksa, sovellus liittää automaattisesti saksan kielikoodin yrityksen kontaktihenkilölle.

<!--You can also setup a default salutation that application automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, application will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-recording-interactions"></a>Vuorovaikutusten automaattinen tallennus
[!INCLUDE[prod_short](includes/prod_short.md)] voi tallentaa myynti- ja ostoasiakirjoja (esimerkiksi tilauksia, laskuja ja vastaanottoja) automaattisesti vuorovaikutukseksi, samoin sähköpostiviestejä, puhelinkeskusteluja ja kansilehtiä.

Lisätietoja on ohjeaiheessa [Kontaktien kanssa tapahtuvien vuorovaikutusten tallennus automaattisesti](marketing-auto-record-interactions.md).

## <a name="synchronizing-contacts-with-customers-and-more"></a>Kontaktien synkronoiminen esimerkiksi asiakkaiden kanssa
Kun haluat synkronisoida kontaktikortin asiakas-, toimittaja- ja pankkitilikortin kanssa, sinun täytyy valita liikesuhdekoodi asiakkaille, toimittajille ja pankkitileille. Voit esimerkiksi linkittää kontaktin olemassa olevaan asiakkaaseen vain, jos olet valinnut asiakkaille liikesuhdekoodin **Kontaktienhallinnan asetukset** -sivulla.

Lisätietoja on kohdassa [Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).  

## <a name="assigning-a-number-series-to-contacts-and-opportunities"></a>Numerosarjojen määrittäminen kontakteihin ja mahdollisuuksiin
Voit määrittää numerosarjan kontakteille ja mahdollisuuksille. Jos olet määrittänyt numerosarjat kontakteille kontaktin luomisen yhteydessä, ja valitset <kbd>Enter</kbd>-näppäimen kontaktin kortin Nro-kentässä, sovellus antaa automaattisesti seuraavan käytettävissä olevan kontaktinumeron.

Lisätietoja numerosarjoista on kohdassa [Numerosarjojen luominen](ui-create-number-series.md).

## <a name="searching-for-duplicate-contacts-when-contacts-are-created"></a>Kontaktien kopioiden etsiminen kontakteja luotaessa
Voit valita, että sovellus hakee kaksoiskappaleita automaattisesti aina, kun luot kontaktiyrityksen. Vaihtoehtoisesti voit valita, että haet kaksoiskappaleet manuaalisesti kontaktien luomisen jälkeen. Voit myös valita, että sovellus päivittää hakumerkkijonot automaattisesti aina, kun muutat kontaktin tietoja tai luot uuden kontaktin. Voit päättää Haun osuma-%:n, siis sen identtisten merkkijonojen prosenttiosuuden, joka kahdella kontaktilla täytyy olla, jotta sovellus tulkitsee ne kopioiksi.

## <a name="see-also"></a>Katso myös
[Kontaktien hallinta](marketing-contacts.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
