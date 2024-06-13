---
title: Aikaraporttien ja niiden hyväksymisen määrittäminen
description: 'Tietoja siitä, miten aikaraportteja käytetään projektien ja resurssien ajan seuraamiseen.'
ms.reviewer: jswymer
author: brentholtorf
ms.author: bholtorf
mw.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77, 462'
ms.date: 07/27/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-time-sheets"></a>Tuntiraporttien määrittäminen

[!INCLUDE[prod_short](includes/prod_short.md)]in aikaraportit käsittelevät aikarekisteröintiä viikoittain seitsemän päivän välein. Voit käyttää niitä projekteissa käytettävän ajan seuraamiseen ja yksinkertaisen resurssin aikarekisteröinnin kirjaamiseen. Ennen kuin käytät tuntiraportteja, sinun täytyy määrittää tuntiraportteja lähettävät käyttäjät ja tavan, jolla määrität tuntiraportteja.  

> [!TIP]
> Tuntiraportteja käyttävät henkilöt ovat *resursseja*. Voit esimerkiksi käyttää tuntiraportteja muiden kuin työntekijöiden työn seuraamista varten. Jotta voit seurata työntekijöiden työtä tai seurata heidän poissaoloaan käyttämällä tuntiraportteja, sinun täytyy liittää työntekijät resursseihin. Mukana on asetusten ohjattu määritys, joka voi auttaa tämän tekemisessä. Lisätietoja oppaasta on ohjeessa [Määritä aikaraportit tuetun asetusoppaan avulla](#set-up-time-sheets-with-the-assisted-setup-guide).  

Voit myös määrittää, milloin ja miten tuntiraportit hyväksytään. Organisaation tarpeista riippuen voit määrittää seuraavat vaihtoehdot:

* Vähintään yhden käyttäjän aikaraportin järjestelmänvalvojaksi ja hyväksyjäksi kaikkia aikaraportteja varten.
* Kunkin resurssin aikaraportin hyväksyjän.

Kun olet määrittänyt tuntiraportit, voit luoda resursseille tuntiraportit ja resurssit voivat kirjata tuntiraporttirivit. Voit myös määrittää tuntiraportit projektin suunnitteluriveille. Lisätietoja on kohdassa [Käytä tuntiraportteja](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Määritä aikaraportit tuetun asetusoppaan avulla

Asetusten ohjattu määritys avulla voi auttaa tuntiraporttien määrittämisessä.  

> [!TIP]
> Jos käytössäsi on versio, joka on aikaisempi kuin vuoden 2023 julkaisuaalto 1 (v22), sinun täytyy ottaa käyttöön **Ominaisuuden päivitys: Uusi tuntiraporttikokemus** -ominaisuus [Ominaisuuksien hallinta](https://businesscentral.dynamics.com/?page=2610) -sivulla, jotta voit käyttää tätä ominaisuutta.
>
> Tämän asetuksen avulla voit myös käyttää tuntiraportteja mobiililaitteissa.

Avaa **Aikaraporttien määrittäminen** -avustettu määritysopas [Ohjattu määritys](https://businesscentral.dynamics.com/?page=1801) -sivulla.

Avustava asetusopas johdattaa sinut alusta loppuun seuraavat vaiheet:

1. Määritä osallistujat tuntiraporttiprosesseihin.

    Kohteen [!INCLUDE [prod_short](includes/prod_short.md)] käyttäjien määrä näkyy oppaan ensimmäisellä sivulla. Siinä näkyy myös muita pakollisia ja valinnaisia tietoja.  
2. Määrittele työviikon ensimmäinen päivä tässä organisaatiossa.

    Työviikon ensimmäinen päivä on kaikkien aikataulukkojen oletusarvoinen ensimmäinen päivä.
3. Työaikalomakkeita ylläpitävän henkilön määrittäminen.

    Tämä henkilö voi muokata ja poistaa kaikkia tuntiraportteja. Vaihtoehtoisesti voit lisätä saman roolin muille käyttäjille **Käyttäjäasetukset**-sivulla.
4. Määritä resurssit, jotka käyttävät tuntiraportteja, ja henkilöt, jotka hyväksyvät tuntiraportteja.

Asennusoppaan lopussa voit määrittää, että [!INCLUDE [prod_short](includes/prod_short.md)] luo tuntiraportteja kokoonpanon perusteella. Voit tarkastella uusia tuntiraportteja **Tuntiraportit**-sivulla, jonka voit avata [tästä](https://businesscentral.dynamics.com/?page=951). Vaihtoehtoisesti voit suorittaa avustetun asennusoppaan uudelleen tai viimeistellä asetukset manuaalisesti.

> [!IMPORTANT]
> Jos käytät vuoden 2023 julkaisuaaltoa 1 (v22) tai uudempaa, varmistaaksesi, että voit hallita tuntiraportteja mobiililaitteilla, ota tuntiraportin asetusten **Käytä uutta tuntiraporttikokemusta** -vaihtoehto manuaalisesti käyttöön seuraavassa ohjeaiheessa kuvatulla tavalla.

## <a name="set-up-time-sheets-manually"></a>Aikaraporttien määrittäminen manuaalisesti

Seuraavissa osissa kuvataan, miten voit määrittää tuntiraportteja, jos et käytä avusteista **Määritä tuntiraportteja** -asetusopasta.  

### <a name="set-up-general-information-for-time-sheets-manually"></a>Aikaraporttien yleistietojen määrittäminen manuaalisesti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssienhallinnan asetukset** ja valitse sitten vastaava linkki.  
1. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!IMPORTANT]
   > Jos käytät vuoden 2023 julkaisuaaltoa 1 (v22) tai uudempaa, varmista, että voit hallita tuntiraportteja mobiililaitteissa, ota käyttöön **Käytä uutta tuntiraporttikokemusta** -vaihtoehto.
1. Valitse **Aikaraportin projektihyväksyntä** -kenttään jokin seuraavista valinnoista.

| Asetus | Kuvaus |
| --- | --- |
| **Ei koskaan** |Resurssikortin **Aikaraportin hyväksyjän käyttäjätunnus** -kenttä hyväksyy aikaraportin. |
| **Aina** |Projektikortin **Vastuuhenkilö**-kenttä hyväksyy aikaraportin. |
| **Vain kone** |Jos koneen aikaraportti on linkitetty projektiin, projektikortin **Vastuuhenkilö**-kentässä mainittu käyttäjä hyväksyy aikaraportin. Jos koneen aikaraportti on linkitetty resurssiin, resurssikortin **Aikaraportin hyväksyjän käyttäjätunnus** -kentässä mainittu käyttäjä hyväksyy aikaraportin. |

### <a name="assign-a-time-sheet-administrator-manually"></a>Aikaraportin järjestelmänvalvojan määrittäminen manuaalisesti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän määritys** ja valitse sitten vastaava linkki.  
2. Valitse ensin käyttäjä, josta tulee aikaraportin järjestelmänvalvoja, ja valitse sitten **Tuntiraportin valvoja** -valintaruutu.  

> [!TIP]  
> Yrityksen aikaraportin järjestelmänvalvojaksi kannattaa nimetä vain yksi käyttäjä. Seuraavassa toimenpiteessä määritetään aikaraportin omistaja ja hyväksyjä. Aikaraportin hyväksyjä määritetään jokaiselle resurssille.  

### <a name="assign-a-time-sheets-owner-and-approver-manually"></a>Aikaraportin omistajan ja hyväksyjän määrittäminen manuaalisesti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssit** ja valitse sitten vastaava linkki.
2. Valitse resurssi, jolle haluat määrittää aikaraporttien käyttömahdollisuuden. Valitse sitten **Käytä aikaraporttia** -valintaruutu.  
3. Syötä aikaraportin omistajan tunnus **Aikaraportin omistajan käyttäjätunnus** -kenttään. Omistaja voi syöttää ajankäytön aikaraporttiin ja lähettää sen hyväksyttäväksi. Jos resurssi on henkilö, tämä henkilö on tyypillisesti myös omistaja.  
4. Syötä aikaraportin hyväksyjän tunnus **Aikaraportin hyväksyjän käyttäjätunnus** -kenttään. Hyväksyjä voi hyväksyä, hylätä tai uudelleenavata aikaraportin.  

> [!NOTE]  
> Aikaraportin hyväksyjän tunnusta ei voi muuttaa, jos on aikaraportteja, joita ei ole vielä käsitelty ja joiden tila on **Lähetetty** tai **Auki**.

## <a name="see-also"></a>Katso myös

[Tuntiraporttien käyttäminen projekteissa](projects-how-use-time-sheets.md)  
[Aikaraporttien luonti](projects-how-use-time-sheets.md#create-time-sheets)  
[Projektien kulutuksen tai käytön kirjaaminen](projects-how-record-job-usage.md)  
[Projektinhallinnan määrittäminen](projects-setup-projects.md)  
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
