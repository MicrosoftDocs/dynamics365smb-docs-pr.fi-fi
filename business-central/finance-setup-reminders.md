---
title: Muistutusehtojen ja -tasojen määrittäminen.
description: 'Määritä Business Central niin, että voit lähettää muistutuksia erääntyvistä maksuista ja lisätä kuluja tai maksuja viiveen takia.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '431, 432, 436, 478'
ms.date: 03/12/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-reminder-terms-and-levels"></a>Muistutusehtojen ja -tasojen määrittäminen

Muistutusten avulla voidaan tiedottaa asiakkaille erääntyneistä summista ja pyytää maksua. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

> [!TIP]
> Kun muistutusehdot ja -tasot on määritetty, ne voidaan sisällyttää muistutusten automaattisiin luonti-, julkaisu- ja lähetysprosesseihin. Lisätietoja automaattisista prosesseista on kohdassa [Perinnän muistutusten automatisointi](finance-automate-reminders.md).

## <a name="reminder-terms"></a>Muistutusehdot

Jos asiakkailla on erääntyneitä maksuja, sinun täytyy päättää, milloin ja miten lähetetään muistutus. Lisäksi saattaa olla tarpeen veloittaa heidän tileiltään korkoja tai maksuja. Muistutusehtoja voi määrittää kuinka monta tahansa.  

> [!NOTE]
> Jos haluat laskea erääntyneiden maksujen koron, voit tehdä sen muistutusten luomisen yhteydessä. Jos halutaan kuitenkin laskea vain korko ja ilmoittaa se asiakkaille lähettämättä muistutuksia, käytä [viivästyskululaskua](finance-setup-finance-charges.md). Lisätietoja on kohdissa [Muistutukset](receivables-collect-outstanding-balances.md#reminders) tai [Viivästyskulut](receivables-collect-outstanding-balances.md#finance-charges).

### <a name="set-up-attachment-and-email-body-texts-for-communications"></a>Viestinnän liitteiden ja sähköpostin perustekstien määrittäminen

**Muistutusehtojen asetukset** -sivulla voidaan määrittää liitetekstit ja vakiosähköpostiviestit, joita käytetään kaikilla muistutustasoilla. Vaihtoehtoisesti viestit voidaan luoda tasokohtaisesti. Esimerkiksi ensimmäisellä muistutustasolla lähetettävän viestin sävy tai sisältö voi olla erilainen kuin toisella tai kolmannella tasolla. Kaikkien tasojen liite- ja sähköpostiviestitekstit luodaan valitsemalla **Asiakasviestit** sivun yläosassa. Tiettyjen rivien viestit luodaan valitsemalla **Muistutustaso**-pikavälilehdessä rivi ja valitsemalla sitten **Asiakasviesti**-toiminto pikavälilehdessä.

Liitteen ja sähköpostiviestin teksteissä käytetään oletusarvoisesti käyttäjän kieliasetusta. Jos muistutus lähetetään muiden maiden asiakkaille, viestintään halutaan ehkä käyttää eri kieltä. Jokaisella [!INCLUDE [prod_short](includes/prod_short.md)]in tukemalla kielellä voidaan luoda tekstejä **Lisää tekstiä kielelle** -toiminnolla. Siinä tapauksessa on varmistettava, että liiteteksteissä ja sähköpostiviestin teksteissä käytetään samaa kieltä. Jos ne eivät samat ja muistutusehdoissa on useita tasoja, automaatio ei ehkä pysty mukauttamaan viestiä yhdellä tai usealla tasolla. Kielien vastaavuus voidaan varmistaa **Viestien yleiskuvaus** -toiminnossa vertaamalla viestien tekstejä.

Kun sähköpostiviesti lähetetään, muistutus liitetään raporttina sähköpostiviestiin. Muistutuksen luova raportti määritetään **Raporttivalintojen muistutus-/viivästyskulu** -sivulla. Tällä sivulla voidaan valita myös raportti, joka sisältää sähköpostin perustekstin **Sähköpostin perustekstin asettelun nimi** -kentässä. Kun asiakkaille lähetetään sähköpostiviestejä, **Sähköpostiviestin teksti** -pikavälilehdessä olevat tekstit lisätään **Sähköpostin perustekstin asettelun nimi** -kentässä valittuun raporttiin. Vakioraportissa on tekstikenttä tätä tekstiä varten. Tätä raporttia voidaan tarvittaessa muokata esimerkiksi lisäämällä tai poistamalla sisältöä. Näiden raporttien asettelua muokataan **Raporttiasettelut**-sivulla. Lisätietoja raporttiasetteluista on kohdassa [Raporttiasettelujen luonnin aloittaminen](ui-get-started-layouts.md).

> [!NOTE]
> Sähköpostiviestintä suoraan [!INCLUDE [prod_short](includes/prod_short.md)]ista edellyttää, että kyseinen määritys on tehty. Lisätietoja sähköpostitilien yhdistämisestä [!INCLUDE [prod_short](includes/prod_short.md)]iin on kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).

### <a name="set-up-reminder-terms"></a>Muistutusehtojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutusehdot** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Voit käyttää useita muistutusehtoyhdistelmä, kun määrität kullekin koodin.

## <a name="reminder-levels"></a>Muistutustasot

Kullekin muistutusehdolle voidaan määrittää rajoittamaton määrä muistutustasoja, joskin useimmat yritykset käyttävät kahta tai kolmea tasoa. Kun asiakkaalle luodaan ensimmäinen muistutus, ohjelma käyttää tason 1 asetuksia. Kun muistutus lähetetään, tason numero rekisteröidään muistutustapahtumiin, jotka luodaan ja linkitetään yksittäisiin asiakastapahtumiin. Jos asiakkaalle on tarpeen lähettää uusi muistutus, kaikki avoimiin asiakastapahtumiin linkitetyt muistutustapahtumat tarkistetaan suurimman tason numeron selvittämistä varten. Tämän jälkeen käytetään uutta muistutusta varten seuraavan tason numeron ehtoja.

Jos luot enemmän muistutuksia kuin mille olet määrittänyt tasoja, ohjelma käyttää ylimmän tason ehtoja. Luotavien muistutusten enimmäismäärä määräytyy muistutusehtojen **Muistutusten enimmäislukumäärä** -kentän mukaan.

### <a name="to-set-up-reminder-levels"></a>Muistutustasojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutusehdot** ja valitse sitten vastaava linkki.  
2. Valitse **Muistutusehdot**-sivulla rivi, jonka ehdoille haluat määrittää tasoja, ja valitse sitten **Tasot**-toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > **Laske korko** -kentän asetus määrittää, näkyykö muistutuksessa korko, kun muistutus lähetetään. **Muistutusehdot**-sivun **Kirjaa korko** -kenttä määrittää, kirjataanko laskettu korko KP- ja asiakastileille.
    >
    > Voit määrittää, että korko lasketaan, valitsemalla **Laske korko** -kentän.

    Jokaiselle muistutustasolle voidaan haluttaessa määrittää lisämaksuja sekä paikallisena että ulkomaan valuuttana. Kullekin **Muistutustasot**-sivun koodille voi määrittää useita ulkomaan valuutoissa olevia lisämaksuja.  

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
7. Liittyviä arvoja voidaan lisätä automaattisesti muistutustekstiin käyttämällä seuraavia paikkamerkkejä **Teksti**-kentässä.  

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

    Jos kenttään kirjoitetaan esimerkiksi **Velkasi on %9 %7, ja se erääntyy %2.**, muistutustekstiksi tulee **Velkasi on 1200,50 USD, ja se erääntyy 2.2.2024.**.

    > [!NOTE]
    > [!INCLUDE [prod_short](includes/prod_short.md)] laskee eräpäivän annetun päivämääräkaavan mukaan. Lisätietoja on kohdassa [Päivämäärän kaavojen käyttäminen](ui-enter-date-ranges.md#use-date-formulas).

8. Sähköpostiviestin kieli määritetään valitsemalla **Lisää tekstiä kielelle** -toiminto. **Kielikoodi**-kenttä päivittyy näyttämään valinnan. Kirjoita **Sähköpostiviestin teksti** -pikavälilehdessä viestin sisältö valitulla kielellä.

Kun muistutusehdot on määritetty, ne voidaan määrittää asiakkaille Asiakaskortti-sivulla. Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).  

## <a name="see-also"></a>Katso myös

[Avointen saldojen perintä](receivables-collect-outstanding-balances.md)  
[Lähetä muistutuksia avoimista saldoista](receivables-send-reminders.md)  
[Viivästyskuluehtojen määrittäminen](finance-setup-finance-charges.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
