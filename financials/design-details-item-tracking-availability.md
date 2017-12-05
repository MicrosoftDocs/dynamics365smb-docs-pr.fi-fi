---
title: "Rakennetiedot – Nimikeseurannan saatavuus | Microsoft Docs"
description: "**Nimikkeen seurantarivit**- ja **Nimikeseurannan yhteenveto** -ikkunoissa on dynaamista saatavuustietoa sarja- tai eränumeroista. Tämän tarkoituksena on kasvattaa käyttäjien läpinäkyvyyttä lähtevissä asiakirjoissa, kuten myyntitilaukset, näyttämälle heille, mitkä sarjanumerot tai kuinka monta yksikköä eränumeroita tällä hetkellä on kirjattuna toisiin avoimiin asiakirjoihin. Tämä poistaa kaksoiskohdistuksen aiheuttamaa epävarmuutta ja vahvistaa tilausten käsittelijöiden luottamusta siihen, että nimikkeen seurantanumerot ja kirjaamattomien myyntitilausten luvatut päivämäärät voidaan toteuttaa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bd69a3da7a0a5e766a232e8999056ac60109e7b1
ms.openlocfilehash: cdfb96475c46d56f32e5f0133efc7852a10ae446
ms.contentlocale: fi-fi
ms.lasthandoff: 10/02/2017

---
# <a name="design-details-item-tracking-availability"></a>Rakennetiedot: nimikkeen seurannan saatavuus
**Nimikkeen seurantarivit**- ja **Nimikeseurannan yhteenveto** -ikkunoissa on dynaamista saatavuustietoa sarja- tai eränumeroista. Tämän tarkoituksena on kasvattaa käyttäjien läpinäkyvyyttä lähtevissä asiakirjoissa, kuten myyntitilaukset, näyttämälle heille, mitkä sarjanumerot tai kuinka monta yksikköä eränumeroita tällä hetkellä on kirjattuna toisiin avoimiin asiakirjoihin. Tämä poistaa kaksoiskohdistuksen aiheuttamaa epävarmuutta ja vahvistaa tilausten käsittelijöiden luottamusta siihen, että nimikkeen seurantanumerot ja kirjaamattomien myyntitilausten luvatut päivämäärät voidaan toteuttaa. Katso lisätiedot kohdasta [Rakennetiedot: nimikkeen seurantarivit -ikkuna](design-details-item-tracking-lines-window.md).  

 Kun **Nimikkeen seurantarivit** -ikkuna avataan, saatavuustiedot haetaan **Nimiketapahtuma**- ja **Varaustapahtuma**-taulukosta ilman päivämääräsuodatinta. Kun valitset **Sarjanro**- tai **Eränro**-kentän, **Nimikeseurannan yhteenveto** -ikkuna avautuu. Ikkunassa näkyvät nimikkeen seurantatiedot **Varaustapahtuma**-taulukossa. Tämä yhteenveto sisältää nimikkeen seurantarivin jokaisen sarja- tai eränumeron seurantatiedot.  

|Kenttä|Kuvaus|  
|---------------------------------|---------------------------------------|  
|**Määrä yhteensä**|Varastossa tällä hetkellä oleva erä- tai sarjanumeron kokonaismäärä.|  
|**Pyydetty määrä yhteensä**|Tällä hetkellä kaikissa asiakirjoissa pyydettyjen erä- tai sarjanumeroiden kokonaismäärä.|  
|**Nykyinen odottava määrä**|Määrä, joka on kirjattu nykyiseen **Nimikkeenseurantarivit** -ikkunaan, mutta ei ole vielä lähetetty tietokantaan.|  
|**Saatavilla oleva kokonaismäärä**|Sarja- tai eränumeron määrä, joka on käyttäjän käytettävissä pyynnöstä.<br /><br /> Määrä lasketaan ikkunan toisten kenttien avulla seuraavasti:<br /><br /> kokonaismäärä – (pyydetty kokonaismäärä + nykyinen odottava määrä).|  

> [!NOTE]  
>  Voit tarkastella edellisen taulukon tietoja käyttämällä **Valitse tapahtumat** -toimintoa **Nimikkeen seurantarivit** -ikkunassa.  

 Saatavuustiedot haetaan tietokannasta vain kerran **Nimikkeen seurantarivit** -ikkunan avaamisen ja **Päivitä saatavuus** -toiminnon käyttämisen yhteydessä. Näin säilytetään tietokannan suorituskyky.  

## <a name="calculation-formula"></a>Laskentakaava  
 Kuten edellisessä taulukossa on kuvattu, määritetyn sarja- tai eränumeron saatavuus lasketaan seuraavasti.  

 saatavilla oleva kokonaismäärä = varastossa oleva määrä – (koko kysyntä + määrä, jota ei ole vielä siirretty tietokantaan)  

> [!IMPORTANT]  
>  Tämä kaava osoittaa, että sarja- tai eränumeron saatavuuden laskenta ottaa huomioon vain varaston, ei suunniteltuja vastaanottoja. Näin ollen tarjonta, jota ei ole vielä kirjattu varastoon, ei vaikuta nimikkeen seurannan saatavuuteen, toisin kuin tavallinen nimikkeen saatavuudessa, johon sisällytetään suunnitellut vastaanotot.  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: nimikkeen seuranta](design-details-item-tracking.md)

