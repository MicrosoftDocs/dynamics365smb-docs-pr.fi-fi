---
title: Ostovelkojen hallintatehtävien yleiskatsaus
description: 'Tässä ohjeaiheessa käsitellään ostovelkojen hallintaan liittyviä tehtäviä, kuten maksamista velkojille tai laskujen tai hyvityslaskujen sulkemista kohdistamalla lähtevät maksut tapahtumiin.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: '161, 254, 256, 347, 574, 599, 9002'
ms.date: 07/12/2024
ms.service: dynamics-365-business-central
---

# <a name="managing-payables"></a>Ostovelkojen hallinta

Keskeinen osa ostoreskontran hoitoa on toimittajille maksamista tai kulujen hyvittämistä työntekijöille. Voit lisätä toiminnoilla erääntyviin ostolaskuihin maksurivejä **Maksupäiväkirja**-sivulla. Voit lähettää tapahtumia pankkiin viemällä useita maksupäiväkirjan rivejä tiedostoon ja ladata sitten tiedoston pankkiin. Voit myös maksaa sekeillä ja siirtää sekkejä sähköisinä maksuina.

Toinen tavallinen tehtävä on lähtevien maksujen kohdistaminen liittyviin toimittaja- tai työntekijätapahtumiin, jotta ostolaskut, ostohyvityslaskut tai työntekijätilit voidaan sulkea maksettuina. Voit tehdä tämän **Maksujen täsmäytyskirjauskansio** -sivulla tuomalla pankin tiliotteen ja rekisteröimällä maksut. Maksut kohdistetaan avoimiin toimittaja-, asiakas- tai työntekijätapahtumiin täsmäyttämällä maksuteksti ja tapahtumatiedot. Täsmäytykset voi tarkistaa tai niitä voi muuttaa eri tavoilla ennen päiväkirjan kirjaamista. Voit sulkea minkä tahansa kohdistettuun tapahtumakirjaukseen liittyvän avoimen pankkitapahtuman päiväkirjan kirjaamisen yhteydessä. Pankkitili täsmäytetään automaattisesti, kun kaikki maksut on kohdistettu.

Vaihtoehtoisesti voit kohdistaa lähtevät maksut manuaalisesti **Maksupäiväkirja**-sivulla tai liittyvistä toimittaja- tai työntekijätapahtumista.

Seuraavassa taulukossa on ostoreskontran tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.

| Vastaanottaja | Katso |
| --- | --- |
| Luo toimittajien maksuja tai työntekijöiden hyvityksiä, valmistele suoritettavat sekkimaksut ja vie maksut pankkitiedostoon kirjauksen yhteydessä. |[Maksujen suorittaminen](payables-make-payments.md) |
| Kohdista toimittajan maksut automaattisesti maksamattomiin ostolaskuihin tuomalla pankin tiliotetiedosto. |[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Kohdista toimittajan maksut maksamattomiin ostolaskuihin manuaalisesti. |[Toimittajamaksujen täsmäyttäminen maksukirjauskansiolla tai toimittajatapahtumista](payables-how-apply-purchase-transactions-manually.md) |
|Varmista varaston oikea arvostus määrittämällä lisätyt nimikekulut, kuten nimikkeiden ostamisessa syntyvät rahti-, käsittely-, vakuutus- ja kuljetuskulut.|[Kaupan lisäkustannusten huomiointi nimikekulujen avulla](payables-how-assign-item-charges.md)|
|Hyvitä työntekijöiden liiketoimintaan liittyvät henkilökohtaiset kulut suorittamalla maksu työntekijän pankkitilille.|[Työntekijöiden kulujen kirjaaminen ja hyvittäminen](finance-how-record-reimburse-employee-expenses.md)|

## <a name="see-also"></a>Katso myös
[Osto](purchasing-manage-purchasing.md)    
[Myyntisaamisten hallinta](receivables-manage-receivables.md)    
[Käytä nimikekuluja lisäkauppakustannusten tilittämiseen](payables-how-assign-item-charges.md)    
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
