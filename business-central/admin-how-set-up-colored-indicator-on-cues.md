---
title: "Pinon toiminnon visuaalisien signaalien mukauttaminen määrittämällä värilliset mittarit yritykselle tai yksittäisille käyttäjille | Microsoft Docs"
description: "Järjestelmänvalvojana voit määrittää pinot, jotka näkyvät käyttäjien Roolikeskuksissa sisällyttääksesi ilmaisimen, joka vaihtaa väriä pinojen arvojen mukaan."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5814a1719ccba38967ee64d28fddae617487b43c
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-a-colored-indicator-on-cues-for-the-company-or-individual-users"></a>Pinojen värillisen ilmaisimen määrittäminen yrityskäyttäjille tai yksittäisille käyttäjille
Järjestelmänvalvojana voit määrittää pinot, jotka näkyvät käyttäjien Roolikeskuksissa sisällyttääksesi ilmaisimen, joka vaihtaa väriä pinojen arvojen mukaan.  
  
Ilmaisin näkyy värillisenä palkkina pinon ruudun yläreunassa. Se antaa visuaalisen signaalin pinon toiminnan tilasta, joka voi ilmaista suotuisia tai epäsuotuisia olosuhteita ja kehottaa käyttäjää toimimaan. Esimerkiksi, jos pino näyttää myyntilaskujen jatkuvan, voit määrittää ilmaisimen näkymään vihreänä (hyvä), kun jatkuva myyntilaskujen määrä on alle 10, ja se muuttuu punaiseksi (epäsuotuisa) kun summa on yli 20.  
  
**Pinon asetukset** -ikkunasta voit asettaa ilmaisimet kaikille pinoille, jotka ovat saatavilla yhtiön tietokannassa. Voit määrittää ilmaisimia, joita käytetään kaikkiin yrityksen käyttäjiin tai vain yksittäiseen käyttäjään. **Pinon asetukset** -ikkunan ilmaisimen asetukset toimivat ilmaisimen oletusasetuksina. Jos käyttäjät voivat käyttää **Loppukäyttäjän pinon asetukset** -ikkunaa, he voivat mukauttaa **Pinon asetukset** -ikkunassa määritettäviä ilmaisinasetuksia.  
  
Jotta voit määrittää ilmaisimen, sinun on määritettävä korkeintaan kaksi raja-arvoa, jotka määrittävät kolme arvoaluetta (matala, keskisuuri ja korkea), joihin voit käyttää eri värejä (tai tyyliä).  
  
### <a name="to-set-up-colored-indicators-on-cues"></a>Värillisten ilmaisinten määrittäminen pinoissa  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Pinon asetukset** ja valitse sitten aiheeseen liittyvä linkki.  
  
     **Pinon asetukset** -ikkuna aukeaa. Ikkunassa on luettelo ilmaisimista, jotka on tällä hetkellä määritetty pinoissa. Kaikkia yrityksen käyttäjiä koskevissa ilmaisimissa on tyhjä **Käyttäjänimi**-kenttä. Tiettyä käyttäjää koskevat ilmaisimet sisältävät käyttäjän nimen **Käyttäjänimi**-kentässä.  
  
    > [!NOTE]  
    >  Jos asetat yrityksen laajuisen ilmaisimen ja käyttäjä muokkaa ilmaisinta myöhemmin, tälle käyttäjälle näkyy luettelossa erillinen ilmaisimen merkintä.  
  
2. Valitse **Muokkaa luetteloa** -toiminto.  
3. Voit määrittää ilmaisimen pinolle, jota ei ole ikkunan luettelossa, valitsemalla **Uusi**-toiminnon ja täyttämällä sitten seuraavaksi käsiteltävät kentät. Jos haluat muokata olemassa olevaa ilmaisinta, siirry seuraavaan vaiheeseen.  
  
    |  Kenttä  |  Description  |    
    |---------|---------------|  
    |**Käyttäjänimi**|Jos haluat asettaa ilmaisimen kaikille käyttäjille, jätä tämä kenttä tyhjäksi.<br /><br /> Jos haluat asettaa ilmaisimen tietylle käyttäjälle, aseta tämä kenttä käyttäjänimeen.|  
    |**Taulukon nro**|Määrittää taulukko-objektin tunnuksen, joka sisältää pinon. Etsi taulukko avattavan luettelon avulla. Avattava luettelo sisältää kaikki yrityksen tietokannassa olevat pinon taulukot.<br /><br /> **Taulukon nimi** -kenttä täytetään automaattisesti tehdyn valinnan perusteella.|  
    |**Kentän nro**|Määrittää pinon tunnuksen, jolle haluat asettaa ilmaisimen. Etsi avattavasta luettelosta haluamasi pino. **Huomautus:** Pinon tunnus vastaa taulukossa olevaan pinoon määritettyä kentän numeroa. <br /><br /> **Kentän nimi** -kenttä täytetään automaattisesti tehdyn valinnan perusteella.|  
  
4. Voit asettaa pinolle ilmaisimen asettamalla kentät seuraavan taulukon mukaisesti.  
  
    |  Kenttä  |  Description  |    
    |---------|---------------|  
    |**Matala tyyli**|Määrittää ilmaisimen värin, kun pinon arvo on pienempi kuin **Raja-arvo 1** -kentän arvo.|  
    |**Alaraja**|Määrittää arvon, jonka kohdalla tai yläpuolella ilmaisin muuttaa väriä **Keskialueen tyyli** -kentän määrittämällä tavalla.|  
    |**Keskimmäinen tyyli**|Määrittää ilmaisimen värin kun pinon arvo suurempi tai yhtä suuri kuin **Raja-arvo 1** -kentän arvo mutta pienempi tai yhtä suuri kuin **Raja-arvo 2** -kentän arvo.|  
    |**Yläraja**|Määrittää arvon, jonka yläpuolella ilmaisin muuttaa väriä **Korkean alueen tyyli** -kentän määrittämällä tavalla.|  
    |**Ylätyyli**|Määrittää käytettävän värin, kun pinon arvo on **Raja-arvo 2** -kentän arvon yläpuolella.|  
  
     Seuraava taulukko sisältää värit, jotka vastaavat **Matala tyyli**-, **Keskimmäinen tyyli**- ja **Ylätyyli**-kenttiä.  
  
    |  Asetus  |  Väri  |  
    |----------|---------|  
    |**Ei mitään**|Ei väriä (sama väri kuin pinon ruutu)|  
    |**Suotuisa**|Vihreä|  
    |**Epäsuotuisa**|Punainen|  
    |**Epäselvä**|Keltainen|  
    |**Alataso**|Harmaa|  
  
## <a name="see-also"></a>Katso myös  
[Värillisen ilmaisimen määrittäminen työtilan pinoille](ui-how-setup-colored-indicator-cues.md)  
