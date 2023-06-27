---
title: Ostojen päivämäärien laskeminen
description: 'Tässä artikkelissa kuvataan, miten ostoille voi laskea päivämäärät.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'purchase order, purchase, date, receipt, delivery, lead time'
ms.search.forms: null
ms.date: 10/28/2022
ms.author: bholtorf
---
# <a name="calculate-dates-for-purchases" />Ostojen päivämäärien laskeminen

Jos haluat, että nimikkeitä on varastossa tiettynä päivänä, [!INCLUDE[prod_short](includes/prod_short.md)] voi automaattisesti laskea päivämäärän, jona sinun on tilattava ne. 

Tuloksena on päivämäärä, jona voit poimia tilaamasi nimikkeet.  

Jos määrität pyydetyn vastaanottopäivämäärän ostotilausrivillä, laskettu tilauspäivämäärä on päivämäärä, jona sinun on tehtävä tilaus. Päivämäärä, jona nimikkeet ovat poimittavissa, tulee näkyviin **Oletettu vastaanottopvm** -kentässä.  

Jos et määritä pyydettyä vastaanottopäivämäärää, päivämäärä, jona oletat vastaanottavasi nimikkeet, perustuu rivin tilauspäivämäärään. 

Vastaanottopäivä on myös se päivämäärä, jona nimikkeet ovat poimittavissa.  

> [!TIP]
> Monet tässä artikkelissa mainitut päivämääräkentät ovat oletusarvoisesti piilotettuna ostotilausriveillä. Jos kenttä ei ole käytettävissä, voit lisätä sen mukauttamalla sivua. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

## <a name="calculating-with-a-requested-receipt-date" />Laskeminen pyydetyn vastaanottopäivämäärän avulla

Jos ostotilausrivillä on pyydetty vastaanottopäivämäärä, se on perustana seuraaville laskennoille:  

- Pyydetty vast.ottopvm - Toimitusajan laskenta = Tilauspvm  
- Pyydetty vast.otto pvm + Saapuva f.var. Käsittelyaika + Toimitusajan varmistus = Oletettu vast.otto pvm  

Jos määrität pyydetyn vastaanottopäivämäärän ostotilausrivillä, kyseinen päivämäärä osoitetaan uusille riveille, jotka luot. Voit muuttaa riveillä olevaa päivämäärää tai poistaa sen.  

> [!NOTE]
> Jos prosessi perustuu taaksepäin laskentaan ja esimerkiksi tilauspäivä saadaan käyttämällä pyydettyä vastaanottopäivää, on suositeltavaa käyttää päivämääräkaavoja, joiden kesto on kiinteä. Sellainen on esimerkiksi 5P viidelle päivälle tai 1V yhdelle viikolle. Päivämääräkaava, jonka kesto ei ole kiinteä, kuten KV kuluvalle viikolle tai KK kuluvalle kuukaudelle, voi aiheuttaa virheellisiä päivämäärälaskelmia. Lisätietoja päivämääräkaavoista on kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-receipt-date" />Laskeminen ilman pyydettyä vastaanottopäivämäärää

Jos lisäät ostotilausrivin ilman pyydettyä vastaanottopäivämäärää, ohjelma näyttää rivin **Tilauspvm**-kentässä ostotilauksen tunnistetietojen **Tilauspvm**-kentän päivämäärän. Tämä päivämäärä on joko lisäämäsi päivämäärä tai käsittelypäivämäärä. Ohjelma laskee sen jälkeen päivämäärät ostotilausriville käyttäen tilauspäivämäärää lähtökohtana seuraavasti:  

- tilauspvm + toimitusajan laskenta = suunniteltu vast.ottopvm.  
- Suunniteltu vast.otto pvm + Saapuva f.var. Käsittelyaika + Toimitusajan varmistus = Oletettu vast.otto pvm  

Jos muutat rivin tilauspäivämäärää, [!INCLUDE[prod_short](includes/prod_short.md)] laskee muut päivämäärät uudelleen.  

## <a name="default-values-for-lead-time-calculation" />Toimitusajan laskennan oletusarvot

[!INCLUDE[prod_short](includes/prod_short.md)] laskee tilauksen ja oletetut vastaanottopäivämäärät käyttäen ostotilausrivin **Toimitusajan laskenta** -kentän päivämääräkaavaa.  

Voit määrittää rivien päivämääräkaavan manuaalisesti. Muussa tapauksessa [!INCLUDE[prod_short](includes/prod_short.md)] käyttää seuraavilla sivulla määritettyjä kaavoja seuraavassa ensisijaisuusjärjestyksessä:

1. Nimike-/toimittajaluettelo
2. Nimikkeen kortti
3. Varastointiyksikön kortti
4. Toimittajan kortti

## <a name="see-related-microsoft-training" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/estimate-receipt-dates-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Myynnin päivämäärälaskenta](sales-date-calculation-for-sales.md)  
[Toimituksen lupaamisen päivämäärien laskeminen](sales-how-to-calculate-order-promising-dates.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
