---
title: ALV-ilmoituksen määrittäminen
description: 'Tässä ohjeaiheessa kerrotaan, miten ALV-ilmoitusmalli ja ALV-ilmoitusnimet määritetään vastaamaan muuttuvia veroviranomaisvaatimuksia.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '317, 318, 320, 474'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="set-up-vat-statement-templates-and-vat-statement-names"></a>ALV-ilmoitusmallien ja ALV-ilmoitusten nimien määrittäminen

Veroviranomaiset voivat muuttaa ALV:n kirjausvaatimuksia. ALV-ilmoitusmallit ja ALV-ilmoitusten nimet voivat auttaa tulevien muutosten valmistelemisessa. Niiden avulla siirtyminen uusiin vaatimuksiin on sujuva. ALV-ilmoitusmallien avulla voit määrittää erilaisia raportteja, kun valitset raportin tulostuksen. Jokaisessa ALV-ilmoitusmallissa voi olla useita ALV-ilmoituksen nimiä, jotka puolestaan määrittävät laskennat, ja voit luoda uuden ALV-ilmoituksen nimen tarpeidesi muuttuessa. Esimerkiksi yksi nimi voi laskea tämän vuoden ALV:in nykyisten vaatimusten ja toinen malli seuraavan vuoden vaatimusten perusteella. Nimien avulla voi myös ylläpitää ALV-ilmoitusten muotojen historiaa esimerkiksi niin, että voit katsoa, miten edellisen vuoden ALV laskettiin.

## <a name="to-define-a-vat-statement"></a>ALV-ilmoituksen määrittely

ALV-ilmoitusten avulla voi laskea ALV-laskelman summan tietyltä kaudelta, esimerkiksi neljännesvuoden ajalta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-ilmoitukset** ja valitse sitten vastaava linkki.  
2. Valitse **Nimi**-kenttä ja valitse sitten **ALV-ilmoitusten nimet** -sivulla **Uusi**.
3. Täytä vaaditut kentät. Tavallisesti halutaan määritys jokaiselle Liiketoiminnan kirjausryhmän/tuotteen ALV-kirjausryhmän yhdistelmälle. Rivinumeroiden osalta on järkevää käyttää samoja numeroita tai koodeja kuin virallisen ALV-ilmoituksen yhteydessä [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Voit suodattaa ilmoituksen sisältämät tiedot sen mukaan, mikä arvo **Tyyppi**-kentässä on valittu. **Tilien summat** -kohta on hyödyllinen silloin, kun haetaan tietyn tilin ALV.
**ALV-tapahtumien summat** hakee ALV:n **Yleinen kirjaustyyppi**-, **Liiketoiminnan ALV-kirjausryhmä**- ja/tai **Tuotteen ALV-kirjausryhmä** -kenttien valikoimaan liitetyistä tileistä. Voit syöttää arvon **Rivien summat** -kenttään tai pikasuodattimen ehdot **Rivien summat** -kenttään. Lisätietoja on kohdassa [Tietojen hakeminen, suodattaminen ja lajitteleminen](ui-enter-criteria-filters.md). **Kuvaus**-kohtaa käytetään usein, kun ilmoitukseen lisätään huomautus. Voit käyttää sitä esimerkiksi otsikkona, kun käytössä on rivien summa.

## <a name="to-preview-the-vat-statement"></a>ALV-ilmoituksen esikatseleminen

Kun ALV-ilmoitus on määritetty, voit esikatsella sitä ja varmistaa, että se täyttää tarpeet.
> [!Tip]
> On paras käytäntö varata yksi osio AVL-ilmoituksessa käyttämään **Tyyppiä** **ALV-tapahtuman kokonaismäärä** ja toinen osio alla käyttämään **Tyyppiä** **Tilin kokonaismäärä** **ALV-tapahtuma**-taulukon summien yhdistämiseen **KL-tileihin**. Tätä tarkoitusta varten voidaan käyttää myös **KP-ALV-täsmäytys**-raporttia.

1. Valitse **Esikatselu**.
2. Aseta päivämääräsuodatus, jos haluat rajoittaa ilmoituksen tietylle kaudelle. Lisätietoja sivun mukauttamisesta niin, että sivulla näkyy päivämääräsuodatin, on kohdassa [Tietojen hakeminen, suodattaminen ja lajitteleminen](ui-enter-criteria-filters.md).
3. Voit valita eri vaihtoehtoja ja siten määrittää, minkä tyyppiset ALV-tapahtumat sisällytetään ALV-ilmoitukseen.
4. Niillä riveillä, joiden **Tyyppi**-kentässä lukee **ALV-tapahtumien summat**, näkyy luettelo ALV-tapahtumista, kun valitset summan **Sarakkeen summa** -kentässä.
5. Voit käyttää mukauttamista, kun haluat näyttää lisää kenttiä riveillä. Esimerkiksi ei-realisoituneen perussumman ja ei-realisoituneen ALV:in summan, jos käytät ei-realisoitunutta ALV:ia.

## <a name="see-also"></a>Katso myös

[Arvonlisäveron määritys](finance-setup-vat.md)  
[Ei-realisoituneen arvonlisäveron määrittäminen](finance-setup-unrealized-vat.md)  
[ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  
[Business Centralin paikalliset toiminnot](about-localization.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
