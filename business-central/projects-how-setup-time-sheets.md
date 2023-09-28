---
title: Aikaraporttien ja niiden hyväksymisen määrittäminen
description: 'Tuntiraportit määritetään seuraamaan tehtäviin ja projekteihin käytettyä aikaa ja resurssien käyttöä, mikä auttaa projektinhallinnan, henkilöstön ja kapasiteetin suhteen'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77'
ms.date: 12/13/2021
ms.author: bholtorf
---
# Aikaraporttien määrittäminen

[!INCLUDE[prod_short](includes/prod_short.md)]in aikaraportit käsittelevät aikarekisteröintiä viikoittain seitsemän päivän välein. Voit käyttää niitä projekteissa käytettävän ajan seuraamiseen ja yksinkertaisen resurssin aikarekisteröinnin kirjaamiseen. Ennen kuin voit käyttää tuntiraportteja, sinun täytyy määrittää tuntiraportteja lähettävät käyttäjät ja tavan, jolla määrität tuntiraportteja.  

> [!TIP]
> Tuntiraporttien käyttäjät kohteessa [!INCLUDE [prod_short](includes/prod_short.md)] ovat *resursseja*. Tällä tavalla voit esimerkiksi käyttää tuntiraportteja muiden kuin työntekijöiden työn seuraamista varten. Jotta voit seurata työntekijöiden työtä tai seurata heidän poissaoloaan käyttämällä tuntiraportteja, sinun täytyy liittää *työntekijät* *resursseihin* asetusoppaassa.  

Voit myös määrittää, milloin ja miten tuntiraportit hyväksytään. Organisaation tarpeista riippuen voit määrittää seuraavat vaihtoehdot:

* Vähintään yhden käyttäjän aikaraportin järjestelmänvalvojaksi ja hyväksyjäksi kaikkia aikaraportteja varten.
* Kunkin resurssin aikaraportin hyväksyjän.

Kun olet määrittänyt tuntiraportit, voit luoda resursseille tuntiraportit ja resurssit voivat kirjata tuntiraporttirivit. Voit myös määrittää tuntiraportit projektin suunnitteluriveille. Lisätietoja on kohdassa [Aikaraporttien käyttäminen](projects-how-use-time-sheets.md).  

## Määritä aikaraportit tuetun asetusoppaan avulla

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

Vuoden 2021 2. julkaisuaallosta eteenpäin voit määrittää tuntiraportteja avustetun asetusoppaan avulla.  

> [!TIP]
> Ota **Ominaisuuden päivitys: Uusi tuntiraporttikokemus** -ominaisuus käyttöön [Ominaisuuksien hallinta](https://businesscentral.dynamics.com/?page=2610) -sivulla, jotta voit käyttää tätä ominaisuutta.
>
> Saman ominaisuuden avulla on myös helppo hallita mobiililaitteen työaikataulukoita.

Avaa **Aikaraporttien määrittäminen** -avustettu määritysopas [Ohjattu määritys](https://businesscentral.dynamics.com/?page=1801) -sivulla.

Avustava asetusopas johdattaa sinut alusta loppuun seuraavat vaiheet:

1. Määritä osallistujat tuntiraporttiprosesseihin

    Kohteen [!INCLUDE [prod_short](includes/prod_short.md)] käyttäjien määrä näkyy oppaan ensimmäisellä sivulla. Siinä näkyy myös muita pakollisia ja valinnaisia tietoja.  
2. Määrittele työviikon ensimmäinen päivä tässä organisaatiossa

    Työviikon ensimmäinen päivä on kaikkien aikataulukkojen oletusarvoinen ensimmäinen päivä.
3. Työaikalomakkeita ylläpitävän henkilön määrittäminen

    Tämä henkilö voi muokata ja poistaa kaikkia tuntiraportteja. Vaihtoehtoisesti voit lisätä saman roolin muille käyttäjille **Käyttäjäasetukset**-sivulla.
4. Määritä resurssit, jotka käyttävät tuntiraportteja, ja henkilöt, jotka hyväksyvät tuntiraportteja.

Asennusoppaan lopussa voit määrittää, että [!INCLUDE [prod_short](includes/prod_short.md)] luo tuntiraportteja kokoonpanon perusteella. Voit tarkastella uusia tuntiraportteja **Tuntiraportit**-sivulla, jonka voit avata [tästä](https://businesscentral.dynamics.com/?page=951). Vaihtoehtoisesti voit suorittaa avustetun asennusoppaan uudelleen tai viimeistellä asetukset manuaalisesti.  

## Aikaraporttien määrittäminen manuaalisesti

Seuraavissa osissa kuvataan, miten voit määrittää tuntiraportteja, jos et käytä avusteista **Määritä tuntiraportteja** -asetusopasta.  

### Aikaraporttien yleistietojen määrittäminen manuaalisesti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssienhallinnan asetukset** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Aikaraportin projektihyväksyntä** -kenttään jokin seuraavista valinnoista.

| Asetus | Kuvaus |
| --- | --- |
| **Ei koskaan** |Resurssikortin **Aikaraportin hyväksyjän käyttäjätunnus** -kenttä hyväksyy aikaraportin. |
| **Aina** |Projektikortin **Vastuuhenkilö**-kenttä hyväksyy aikaraportin. |
| **Vain kone** |Jos koneen aikaraportti on linkitetty projektiin, projektikortin **Vastuuhenkilö**-kentässä mainittu käyttäjä hyväksyy aikaraportin. Jos koneen aikaraportti on linkitetty resurssiin, resurssikortin **Aikaraportin hyväksyjän käyttäjätunnus** -kentässä mainittu käyttäjä hyväksyy aikaraportin. |

### Aikaraportin järjestelmänvalvojan määrittäminen manuaalisesti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän määritys** ja valitse sitten vastaava linkki.  
2. Lisää uusi käyttäjä, jos käyttäjäluettelo ei sisällä henkilöä, jonka haluat olevan aikaraportin järjestelmänvalvoja. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).
3. Valitse ensin käyttäjä, josta tulee aikaraportin järjestelmänvalvoja, ja valitse sitten **Tuntiraportin valvoja** -valintaruutu.  

> [!TIP]  
> Yrityksen aikaraportin järjestelmänvalvojaksi kannattaa nimetä vain yksi käyttäjä. Seuraavassa toimenpiteessä määritetään aikaraportin omistaja ja hyväksyjä. Aikaraportin hyväksyjä määritetään jokaiselle resurssille.  

### Aikaraportin omistajan ja hyväksyjän määrittäminen manuaalisesti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssit** ja valitse sitten vastaava linkki.
2. Valitse resurssi, jolle haluat määrittää aikaraporttien käyttömahdollisuuden. Valitse sitten **Käytä aikaraporttia** -valintaruutu.  
3. Syötä aikaraportin omistajan tunnus **Aikaraportin omistajan käyttäjätunnus** -kenttään. Omistaja voi syöttää ajankäytön aikaraporttiin ja lähettää sen hyväksyttäväksi. Jos resurssi on henkilö, tämä henkilö on yleensä myös omistaja.  
4. Syötä aikaraportin hyväksyjän tunnus **Aikaraportin hyväksyjän käyttäjätunnus** -kenttään. Hyväksyjä voi hyväksyä, hylätä tai uudelleenavata aikaraportin.  

> [!NOTE]  
> Aikaraportin hyväksyjän tunnusta ei voi muuttaa, jos on aikaraportteja, joita ei ole vielä käsitelty ja joiden tila on **Lähetetty** tai **Auki**.

## Katso myös

[Tuntiraporttien käyttäminen projekteissa](projects-how-use-time-sheets.md)  
[Aikaraporttien luonti](projects-how-use-time-sheets.md#to-create-time-sheets)  
[Projektien kulutuksen tai käytön kirjaaminen](projects-how-record-job-usage.md)  
[Projektinhallinnan määrittäminen](projects-setup-projects.md)  
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
