---
title: Rakennetiedot – Nimikeseurannan saatavuus
description: 'Nimikkeen seurantarivit- ja Nimikeseurannan yhteenveto -sivuilla on sarja- tai eränumeroista dynaamista saatavuustietoa, joka lisää läpinäkyvyyttä käyttäjille.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-availability" />Rakennetiedot: Nimikkeen seurannan saatavuus
**Nimikkeen seurantarivit**- ja **Nimikeseurannan yhteenveto** -sivuilla on dynaamista saatavuustietoa sarja- tai eränumeroista. Tämän tarkoituksena on kasvattaa käyttäjien läpinäkyvyyttä lähtevissä asiakirjoissa, kuten myyntitilaukset, näyttämälle heille, mitkä sarjanumerot tai kuinka monta yksikköä eränumeroita tällä hetkellä on kirjattuna toisiin avoimiin asiakirjoihin. Tämä poistaa kaksoiskohdistuksen aiheuttamaa epävarmuutta ja vahvistaa tilausten käsittelijöiden luottamusta siihen, että nimikkeen seurantanumerot ja kirjaamattomien myyntitilausten luvatut päivämäärät voidaan toteuttaa. Katso lisätiedot kohdasta [Rakennetiedot: Nimikkeen seurantarivit -sivu](design-details-item-tracking-lines-window.md).  

 Kun **Nimikkeen seurantarivit** -sivu avataan, saatavuustiedot haetaan **Nimiketapahtuma**- ja **Varaustapahtuma**-taulukosta ilman päivämääräsuodatinta. Kun valitset **Sarjanro**- tai **Eränro**-kentän, **Nimikeseurannan yhteenveto** -sivu avautuu. Sivulla näkyvät nimikkeen seurantatiedot **Varaustapahtuma**-taulukossa. Tämä yhteenveto sisältää nimikkeen seurantarivin jokaisen sarja- tai eränumeron seurantatiedot.  

|Kenttä|Kuvaus|  
|---------------------------------|---------------------------------------|  
|**Määrä yhteensä**|Varastossa tällä hetkellä oleva erä- tai sarjanumeron kokonaismäärä.|  
|**Pyydetty määrä yhteensä**|Tällä hetkellä kaikissa asiakirjoissa pyydettyjen erä- tai sarjanumeroiden kokonaismäärä.|  
|**Nykyinen odottava määrä**|Määrä, joka on kirjattu nykyiselle **Nimikkeenseurantarivit** -sivulle, mutta ei ole vielä lähetetty tietokantaan.|  
|**Saatavilla oleva kokonaismäärä**|Sarja- tai eränumeron määrä, joka on käyttäjän käytettävissä pyynnöstä.<br /><br /> Määrä lasketaan sivun muiden kenttien avulla seuraavasti:<br /><br /> kokonaismäärä – (pyydetty kokonaismäärä + nykyinen odottava määrä).|  

> [!NOTE]  
>  Voit tarkastella edellisen taulukon tietoja käyttämällä **Valitse tapahtumat** -toimintoa **Nimikkeen seurantarivit** -sivulla.  

 Saatavuustiedot haetaan tietokannasta vain kerran **Nimikkeen seurantarivit** -sivun avaamisen ja **Päivitä saatavuus** -toiminnon käyttämisen yhteydessä. Näin säilytetään tietokannan suorituskyky.  

## <a name="calculation-formula" />Laskentakaava
 Kuten edellisessä taulukossa on kuvattu, määritetyn sarja- tai eränumeron saatavuus lasketaan seuraavasti.  

 saatavilla oleva kokonaismäärä = varastossa oleva määrä – (koko kysyntä + määrä, jota ei ole vielä siirretty tietokantaan)  

> [!IMPORTANT]  
>  Tämä kaava osoittaa, että sarja- tai eränumeron saatavuuden laskenta ottaa huomioon vain varaston, ei suunniteltuja vastaanottoja. Näin ollen tarjonta, jota ei ole vielä kirjattu varastoon, ei vaikuta nimikkeen seurannan saatavuuteen, toisin kuin tavallinen nimikkeen saatavuudessa, johon sisällytetään suunnitellut vastaanotot.  

## <a name="see-also" />Katso myös
 [Rakennetiedot: nimikkeen seuranta](design-details-item-tracking.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
