---
title: Pankkitilien täsmäyttäminen ja maksujen kohdistaminen automaattisesti
description: 'Ohjeaiheessa kerrotaan tehtävistä, joilla täsmäytetään pankki-, myyntisaamis- ja ostovelkatilit, kirjataan kassaanmaksut ja kassakulut sekä kohdistetaan maksut automaattisesti.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1291, 1293, 1294'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen

Pankin, myyntisaamisten ja ostovelkojen tilit on täsmäytettävä säännöllisesti kohdistamalla pankkiin tallennetut maksut niiden vastaaviin avoimiin (maksamattomiin) laskuihin ja hyvityslaskuihin tai muihin avoimiin tapahtumiin [!INCLUDE[prod_short](includes/prod_short.md)]issa.  

Voit suorittaa tämän tehtävän **Maksujen täsmäytyskirjauskansio** -sivulla tuomalla esimerkiksi pankin tiliotteen tai syötteen maksujen nopeaa rekisteröintiä varten. Maksut kohdistetaan avoimiin asiakas- tai toimittajatapahtumiin maksutekstin ja tapahtumatietojen välisen täsmäytyksen perusteella. Voit tarkastella ja muuttaa automaattisia kohdistuksia, ennen kuin kirjaat päiväkirjan. Voit sulkea minkä tahansa kohdistettuun tapahtumakirjaukseen liittyvän avoimen pankkitapahtuman päiväkirjan kirjaamisen yhteydessä. Pankkitili täsmäytetään automaattisesti, kun kaikki maksut on kohdistettu.

**Maksusovelluksen säännöt** -sivulla voit määrittää tärkeysjärjestyssääntöjä, jotka säätelevät, kuinka maksuteksti yhdistetään automaattisesti merkintätietoihin.

Voit täsmäyttää pankkitilejä myös niin, että maksuja ei kohdisteta samanaikaisesti. Voit tehdä tämän **Pankkitilin täsmäytys** -sivulla. Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen](bank-how-reconcile-bank-accounts-separately.md).

Voit tuoda pankin tiliotteet pankkisyötteenä määrittämällä ensin Envestnet Yodlee Bank Feeds -palvelun ja linkittämällä sitten pankkitilit liittyviin verkkopankkitileihin. Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Tiliotetiedostoja voi tuoda myös pilkuin tai puolipistein erotellussa muodossa (.CSV). Tiliotteen tuontimuodot voidaan määrittää ja muoto liittää pankkitiliin käyttämällä asetusten ohjattua määritystä **Määritä tiliotetiedoston tuontimuoto**. Näitä muotoja voi sitten käyttää, kun tiliotteita tuodaan **Pankkitilin täsmäytys** -sivulla.

Vaihtoehtoisesti voit käyttää AMC Banking 365 Fundamentals -laajennusta muuntamaan tiliotteen tiedostomuodosta riippumatta tietovirraksi, jonka voit tämän jälkeen tuoda [!INCLUDE[prod_short](includes/prod_short.md)]iin. Lisätietoja on kohdassa [AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md).  

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.  

| Vastaanottaja | Katso |
| --- | --- |
| Kohdista maksut avoimiin asiakas- tai toimittajatapahtumiin tuomalla tiliote. Täsmäytä pankkitili sitten, kun olet kohdistanut kaikki maksut. |[Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md) |
| Voit kohdistaa maksut manuaalisesti tarkastelemalla jokaisen kohdistetun tiedon tietoja ja ehdotuksia avoimista tapahtumista joihin maksut kohdistetaan. |[Maksujen tarkastelu tai käyttäminen automaattisen kohdistuksen jälkeen](receivables-how-review-apply-payments-auto-application.md) |
| Ratkaise maksut, joita ei voi kohdistaa automaattisesti niihin liittyviin avoimiin tapahtumiin. Syynä voi olla esimerkiksi se, että summat ovat erilaiset tai liittyvää tapahtumaa ei ole. |[Niiden maksujen täsmäyttäminen, joita ei voi kohdistaa automaattisesti](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Linkitä maksujen teksti tiettyyn asiakkaaseen, toimittajaan tai kirjanpitotileihin, jotta toistuvat käteiskuitit tai kulut kirjataan aina näille tileille, kun kohdistettavia asiakirjoja ei ole. |[Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Määritä säännöt, jotka hallinnoivat sitä, kuinka maksuja/pankkitapahtumia sovelletaan automaattisesti niihin liittyviin avoimiin kirjanpitotapahtumiin, kun käytät **Sovella automaattisesti** -toimintoa **Maksujen täsmäytyskirjauskansio** -sivulla.|[Sääntöjen määrittäminen maksujen automaattista kohdistusta varten](receivables-how-set-up-payment-application-rules.md)|

## Katso myös

[Pankkitilien täsmäyttäminen](bank-how-reconcile-bank-accounts-separately.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
