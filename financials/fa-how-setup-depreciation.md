---
title: "Toimintaohje: Käyttöomaisuuden poiston määrittäminen| Microsoft Docs"
description: "Tässä artikkelissa kerrotaan, miten järjestelmä määritetään käyttöomaisuuden poisto varten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8d14eb7cc55abd8d7aaddf2f3a8edcf20354fdec
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-fixed-asset-depreciation"></a>Toimintaohje: Käyttöomaisuuden poiston määrittäminen
 Rahoituslaskelmien ja tuloveropalautusten valmistelussa voi käyttää useita poistomenetelmiä. Monet suuret yritykset käyttävät tasapoistoja rahoituslaskelmissaan, koska sen avulla voidaan yleensä raportoida suurempia tuloja. Tuloverotarkoituksia varten monet yritykset käyttävät kuitenkin degressiivistä poistomenetelmää. Lisätietoja on kohdassa [Poistotavat](fa-depreciation-methods.md).

 Kun olet luonut asianmukaiset poistokirjat, kuhunkin käyttöomaisuuserään tulee liittää yksi tai usea poistokirja. Käyttöomaisuuteen liitettyä poistokirjaa kutsutaan käyttöomaisuuden poistokirjaksi. Samaan tapaan liitettyjen poistokirjojen ikkuna on nimeltään **KO:n poistokirjat**.

## <a name="to-create-a-depreciation-book"></a>Poistokirjan luominen
Käyttöomaisuuden poistokirjaan voidaan määrittää, miten käyttöomaisuus poistetaan. Useiden erilaisten poistomenetelmien hallitsemiseksi voidaan määrittää useita poistokirjoja.  

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Poistokirjat** ja valitse sitten liittyvä linkki.
2. Valitse **Poistokirjaluettelo**-ikkunassa **Uusi**-toiminto.
3. Täytä **Poistokirjakortti**-ikkunassa tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    **Huomautus:** Voit tallentaa käyttöomaisuustapahtumat **Käyttöomaisuuden KP-päiväkirja**- tai **Käyttöomaisuuspäiväkirja**-ikkunaan sen mukaan, koskevatko tapahtumat talousraportointia vai sisäistä hallintaa. Määritä seuraavan vaiheen mukaisesti eri käyttöomaisuustoiminnoissa oletusarvoisesti käytettävien päiväkirjojen tyypit.
4. Valitse **Integrointi**-pikavälilehdessä niiden käyttöomaisuustoimintojen valintaruudut, jotka haluat kirjata **Käyttöomaisuuden KP-päiväkirja** -ikkunan avulla.
5. Toista vaiheet 2–4 jokaisen sellaisen poisto- tai kirjaustavan kohdalla, jonka haluat liittää käyttöomaisuuserään poistokirjana.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>Poistokirjan liittäminen käyttöomaisuuteen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Käyttöomaisuus** ja valitse sitten liittyvä linkki.
2. Valitse käyttöomaisuus, jolle haluat määrittää käyttöomaisuuden poistokirjan.
3. Täytä **Poistokirja**-pikavälilehden kentät tarvittaessa.
4. Jos käyttöomaisuuteen on liitettävä useita poistokirjoja, valitse **Lisää poistokirjoja** -toiminto.
5. Vaihtoehtoisesti voit valita **Poistokirjat**-toiminnon ja määrittää vähintään yhden käyttöomaisuuden poistokirjan.

    **Huomautus:** Kun käytössä on manuaalinen poistomenetelmä, poistot on vietävä manuaalisesti käyttöomaisuuden KP-päiväkirjaan. **Laske poisto** -toiminto jättää huomiotta käyttöomaisuuserät, joille käytetään manuaalista poistomenetelmää. Tätä tapaa voidaan käyttää omaisuuserille, joille ei tehdä poistoja, kuten maa-alueille.

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>Poistokirjan liittäminen useisiin käyttöomaisuuseriin eräajon avulla
Jos haluat määrittää poistokirjan moneen käyttöomaisuuteen, voit luoda **Luo KO:n poistokirjat** -eräajolla käyttöomaisuuden poistokirjat.  

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Käyttöomaisuus** ja valitse sitten liittyvä linkki.
2. Valitse käyttöomaisuus, jolle haluat määrittää ja liittää poistokirjan. Valitse sitten **Muokkaa**-toiminto.
3. Valitse **Poistokirjakortti**-ikkunassa **Luo KO:n poistokirjat** -toiminto.
4. Täytä **Luo KO:n poistokirjat** -ikkunan **Poistokirja**-kenttä.
5. Valitse **Kopioi KO:n nrosta** -kenttä ja valitse sen käyttöomaisuuserän numero, jota haluat käyttää pohjana luodessasi uusia käyttöomaisuuden poistokirjoja.

    Jos tämä kenttä täytetään, uusien KO-poistokirjojen poistokentissä on samat tiedot kuin kopioitavan KO-poistokirjan vastaavissa kentissä. Jätä kenttä tyhjäksi, jos haluat luoda uusia KO:n poistokirjoja, joissa on tyhjiä poistokenttiä.  
6. **Käyttöomaisuus**-pikavälilehteen voidaan asettaa suodatus valitsemaan se omaisuus, jolle halutaan luoda käyttöomaisuuden poistokirjat.
7. Valitse **OK**-painike.

## <a name="to-set-up-depreciation-posting-types"></a>Poiston kirjaustyyppien määrittäminen
Kunkin poistokirjan osalta on määritettävä, miten [!INCLUDE[d365fin](includes/d365fin_md.md)] käsittelee eri kirjaustyyppejä. Voit esimerkiksi määrittää, että tuleeko kirjauksen olla debet vai kredit, ja tuleeko kirjaustyyppi sisällyttää poistopohjaan.  

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Poistokirjat** ja valitse sitten liittyvä linkki.  
2. Valitse poistokirja, jonka. Valitse sitten **KO:n kirjaustyypin asetukset** -toiminto.
3. Täytä **KO:n kirjaustyypin asetukset** -ikkunassa tarvittavat kentät.

    **Huomautus:** **KO:n kirjaustyypin asetukset** -ikkunaan ei voi lisätä rivejä tai poistaa niitä. Ainoastaan olemassa olevia rivejä voi muuttaa.

    On hyvin suositeltavaa, ettei niiden poistokirjojen asetuksia muuteta, joiden osalta on jo kirjattu tapahtumia. Muutokset eivät vaikuta jo kirjattuihin tapahtumiin, mikä tekee poistokirjatilastoista harhaanjohtavia.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>Käyttöomaisuuden poiston oletusmallien ja -erien määrittäminen
Kunkin poistokirjan osalta määritellään mallien ja erien oletusasetukset. Voit monistaa näillä oletusarvoilla yhden päiväkirjan rivit toiseen päiväkirjaan, luomaan päiväkirjarivejä **Laske poisto**- tai **Tee indeksimuutos KO:teen** -eräajoilla ja monistamaan vakuutuspäiväkirjan hankintamenoja.  

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Poistokirjat** ja valitse sitten liittyvä linkki.  
2. Valitse poistokirja, jolle haluat määrittää oletuspäiväkirjat. Valitse sitten **KO-päiväkirjan asetukset** -toiminto.  
3. Jos haluat, että jokaisella käyttäjällä on oletusasetukset, valitse **Käyttäjätunnus**-kenttä, jotta voit tehdä valinnan **Käyttäjät**-ikkunassa.  
4. Valitse muille kentille oletusarvoisesti käytettävä päiväkirjamalli tai -erä.  

## <a name="see-also"></a>Katso myös
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuus](fa-manage.md)  
[Rahoitus](finance.md)  
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin](index.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)
