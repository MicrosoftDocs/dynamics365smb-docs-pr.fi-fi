---
title: Muistutusehtojen ja -tasojen määrittäminen.
description: Lue, miten voit määrittää Business Centralin lähettämään asiakkaalle muistutuksen erääntyvästä maksusta ja miten maksuun lisätään myöhästymismaksu.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 01/21/2021
ms.author: edupont
ms.openlocfilehash: 1bef0a7598846f0ea3fe74b03bbef70bb5c940ef
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035379"
---
# <a name="set-up-reminder-terms-and-levels"></a>Muistutusehtojen ja -tasojen määrittäminen.

Muistutusten avulla voit muistuttaa asiakkaita erääntyneistä summista. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

## <a name="reminder-terms"></a>Muistutusehdot

Jos asiakkailla on erääntyneitä maksuja, sinun täytyy päättää, milloin ja miten heille lähetetään muistutus. Lisäksi saattaa olla tarpeen veloittaa heidän tileiltään korkoja tai maksuja. Muistutusehtoja voi määrittää kuinka monta tahansa.  

> [!NOTE]
> Jos haluat laskea erääntyneiden maksujen koron, voit tehdä sen muistutusten luomisen yhteydessä. Jos haluat laskea koron ja tiedottaa siitä asiakkaille lähettämättä muistutuksia, käytä [viivästyskululaskuja](finance-setup-finance-charges.md). Lisätietoja on vastaavasti kohdissa [Muistutukset](receivables-collect-outstanding-balances.md#reminders) tai [Viivästyskulut](receivables-collect-outstanding-balances.md#finance-charges).

### <a name="to-set-up-reminder-terms"></a>Muistutusehtojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Muistutusehdot** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Voit käyttää useita muistutusehtoyhdistelmä, kun määrität kullekin koodin.

## <a name="reminder-levels"></a>Muistutustasot

Voit määrittää kullekin muistutusehtojen koodille rajoittamattoman määrän muistutustasoja. Kun asiakkaalle luodaan ensimmäinen muistutus, ohjelma käyttää tason 1 asetuksia. Kun muistutus lähetetään, tason numero rekisteröidään muistutustapahtumiin, jotka luodaan ja linkitetään yksittäisiin asiakastapahtumiin. Jos asiakkaalle on tarpeen lähettää uusi muistutus, kaikki avoimiin asiakastapahtumiin linkitetyt muistutustapahtumat tarkistetaan suurimman tason numeron selvittämistä varten. Tämän jälkeen käytetään uutta muistutusta varten seuraavan tason numeron ehtoja.

Jos luot enemmän muistutuksia kuin mille olet määrittänyt tasoja, ohjelma käyttää ylimmän tason ehtoja. Luotavien muistutusten enimmäismäärä määräytyy muistutusehtojen **Muistutusten enimmäislukumäärä** -kentän mukaan.

### <a name="to-set-up-reminder-levels"></a>Muistutustasojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Muistutusehdot** ja valitse sitten liittyvä linkki.  
2. Valitse **Muistutusehdot**-sivulla rivi, jonka ehdoille haluat määrittää tasoja, ja valitse sitten **Tasot**-toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > **Laske korko** -kentän asetus määrittää, näkyykö muistutuksessa korko, kun muistutus lähetetään. **Muistutusehdot**-sivun **Kirjaa korko** -kenttä määrittää, kirjataanko laskettu korko KP- ja asiakastileille.
    >
    > Voit määrittää, että korko lasketaan, valitsemalla **Laske korko** -kentän.

    Jokaiselle muistutustasolle voidaan haluttaessa määrittää lisämaksuja sekä PVA:na että ulkomaan valuuttana. Kullekin **Muistutustasot**-sivun koodille voi määrittää useita ulkomaan valuutoissa olevia lisämaksuja.  

    Lisämaksut voidaan laskea kolmella eri tavalla, jotka on määritelty **Lisämaksun laskentatyyppi** -kentän arvon mukaan.  

    - **Kiinteä**

        Maksut lasketaan itse muistutustasolle rivin **Lisämaksu**-kenttien arvojen perusteella.  
    - **Yksittäinen dynaaminen**

        Maksut lasketaan kyseiselle muistutustasolle asianmukaisen rivin **Lisämaksun asetukset**-kenttien arvojen perusteella.
    - **Kumulatiivinen dynaaminen**

        Maksut lasketaan kyseiselle muistutustasolle yhdistettyjen rivien **Lisämaksun asetukset** -kenttien arvojen perusteella.

4. Valitse **Valuutat**-toiminto.
5. Määritä **Muistutustason valuutat** -sivulla jokaiselle muistutustason koodille ja vastaavalle muistutustason numerolle valuutan koodi ja lisämaksu.

    > [!NOTE]  
    > Kun luot muistutuksia ulkomaan valuuttana, tässä määritettäviä ulkomaan valuutan ehtoja käytetään muistutusten luontiin. Jos ulkomaan valuuttojen ehtoja ei ole määritetty, käytetään **Muistutustasot**-sivulla määritettyjä PVA:n muistutusehtoja ja ne muunnetaan soveltuvaan valuuttaan.

    Voit määrittää kutakin muistutustasoa varten tekstin, joka tulostetaan ennen muistutuksen merkintöjä (**Aloitusteksti**) tai niiden jälkeen (**Lopetusteksti**).

6. Valitse tilanteen mukaan joko **Aloitusteksti**- tai **Lopetusteksti**-toiminto ja täytä **Muistutusteksti**-sivun tiedot.
7. Voit lisätä liittyviä arvoja automaattisesti muistutustekstiin käyttämällä seuraavia paikkamerkkejä **Teksti**-kentässä.  

    |Paikkamerkki|Arvo|  
    |-----------------|-----------|  
    |%1|Muistutuksen otsikon **Asiakirjan pvm** -kentän sisältö|  
    |%2|Muistutuksen otsikon **Eräpäivä** -kentän sisältö|  
    |%3|Viivästyskuluehtojen **Korko**-kentän sisältö|  
    |%4|Muistutuksen otsikon **Jäljellä oleva summa** -kentän sisältö|  
    |%5|Muistutuksen otsikon **Korkosumma**-kentän sisältö|  
    |%6|Muistutuksen otsikon **Lisämaksu**-kentän sisältö|  
    |%7|Muistutuksen kokonaissumma|  
    |%8|Muistutuksen otsikon **Muistutustaso**-kentän sisältö|  
    |%9|Muistutuksen otsikon **Valuutan koodi** -kentän sisältö|  
    |%10|Muistutuksen otsikon **Kirjauspvm** -kentän sisältö|  
    |%11|Yrityksen nimi|  
    |%12|Muistutuksen otsikon **Lisämaksu riviä kohti** -kentän sisältö|  

    Jos kirjoitat kenttään esimerkiksi **Velkasi on %9 %7, joka erääntyy %2**, muistutustekstiksi tulee **Velkasi on 1200,50 PVA, joka erääntyy 2.2.2014.**.

    > [!NOTE]
    > Eräpäivä lasketaan annetun päivämääräkaavan mukaan. Lisätietoja on kohdassa [Päivämäärän kaavojen käyttäminen](ui-enter-date-ranges.md#using-date-formulas).

Kun olet määrittänyt muistutusehdot sekä lisätasot ja tekstin, määritä jokin koodeista kussakin asiakkaan kortissa. Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).  

## <a name="see-also"></a>Katso myös .

[Avointen saldojen perintä](receivables-collect-outstanding-balances.md)  
[Viivästyskuluehtojen määrittäminen](finance-setup-finance-charges.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
