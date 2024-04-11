---
title: Projektin budjetin määrittäminen ja hallinta
description: Käsittelyssä resurssien suunnittelu ja ennakointi sekä projektin kustannusten määrittäminen kullekin projektille.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'project budget, forecast'
ms.search.form: '1002, 1007'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="manage-project-budgets"></a>Projektin budjettien hallinta

Budjetti voidaan määrittää kullekin projektille. Budjettia käytetään projektille kohdistettavien resurssien suunnittelussa. Budjetti voi olla joko yleisluonteinen budjetti, joka sisältää vain vähän tapahtumia, tai se voi sisältää monia tapahtumia, jotka on jaettu toimintotasoille. Voit verrata budjetoituja summia projektipäiväkirjaan kirjattuun todelliseen käyttöön. Kun todellisen ja budjetoidun käytön välisiä eroja seuraamalla voidaan hallita meneillään olevaa projektia ja parantaa tulevien projektien laatua pienentämällä kustannusten aliarvioinnin riskiä.

Seuraavissa ohjeissa kerrotaan, miten budjetoituja kustannuksia arvioidaan suunnittelun aikana. Lisätietoja budjetoitujen ja todellisten projektihintojen ja -kustannusten kirjaamisesta on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md).  

## <a name="to-estimate-the-budgeted-costs-for-a-project"></a><a name="JobBudgetCosts"></a>Projektin budjetoitujen kustannusten arvioiminen

Kun asiakas haluaa tietää sellaisen projektin hinnan, joka laskutetaan käytön perusteella, on määritettävä projektin budjetoidut kustannukset. Se tehdään **Projektitehtävärivit**-sivulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.  
2. Avaa sopiva projekti.
3. Valitse tehtävärivin tyypiksi Kirjaus ja valitse sitten **Projektin suunnittelurivit** -toiminto.
4. Täytä tarvittaessa uuden rivin kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Viittaa **Rivityyppi**-kentässä seuraaviin tietoihin.  

| Rivityyppi | Kuvaus |
| --- | --- |
| **Sekä budjetti että laskutettava** |Suunnitteluriville annetut kustannus- ja hintasummat ovat tämän suunnittelurivin budjetoidut kustannukset sekä laskutettava hinta. Hinnaston summa laskutetaan. |
| **Budjetti** |Asiakasta ei veloiteta käytöstä. Käyttöä ei siirretä laskuun vaan käytetään keskeneräisten töiden laskemiseen. |
| **Laskutettava** |Asiakasta veloitetaan käytöstä. Laskutettava määrä on määritetty kunkin ostorivin **Laskuun siirrettävä määrä** -kentässä. |

> [!NOTE]  
> Suunnittelurivin **Suunniteltu toimituspvm** -kenttä sisältää päivämäärän, jona suunnitteluriviin liittyvän käytön odotetaan olevan valmis. Se on myös päivämäärä, jona suunnittelurivi voidaan siirtää myyntilaskuun ja kirjata. <br /><br /> **Projektikortti**-sivun taustalla olevan projektitehtävän **Aloituspäivämäärä**- ja **Päättymispäivämäärä**-kentät sisältävät **Suunniteltu toimituspvm** -kentän arvon ensimmäisillä ja viimeisellä projektin suunnittelurivillä liittyvällä **Projektin suunnittelurivit** -sivulla.

> [!NOTE]  
> Kun täytät **Määrä**-kentän, ohjelma laskee kaikki kokonaishinnan ja -kustannusten tiedot kyseistä suunnitteluriviä varten. Voit muokata niitä milloin tahansa.

**Projektikortti**-sivulla on nyt yhteenveto kunkin tehtävän budjetoiduista kokonaiskustannuksista, budjetoidusta hinnasta, laskutettavista kustannuksista ja laskutettavasta hinnasta.

Lisätietoja budjetoitujen ja todellisten projektihintojen ja -kustannusten kirjaamisesta on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md).

## <a name="see-also"></a>Katso myös

[Projektien hallinta](projects-manage-projects.md)  
[Taloushallinto](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
