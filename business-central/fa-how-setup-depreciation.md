---
title: Poistomenetelmien määrittäminen| Microsoft Docs
description: Voit määrittää poistokirjaan, miten haluat käyttöomaisuuden poiston tai alaskirjauksen tapahtuvan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c9eea613db52d327caa1c3d5449864900fc867d1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749267"
---
# <a name="set-up-fixed-asset-depreciation"></a>Käyttöomaisuuden poiston määrittäminen
 Rahoituslaskelmien ja tuloveropalautusten valmistelussa voi käyttää useita poistomenetelmiä. Monet suuret yritykset käyttävät tasapoistoja rahoituslaskelmissaan, koska sen avulla voidaan yleensä raportoida suurempia tuloja. Tuloverotarkoituksia varten monet yritykset käyttävät kuitenkin nopeutettua poistomenetelmää, kuten vähenevän saldon poistoa. Käyttöomaisuuden poistomenetelmä määritetään **Poistomenetelmä**-kentässä **Käyttöomaisuuden kortti** -sivulla. Lisätietoja eri menetelmistä on kohdassa [Poistomenetelmät](fa-depreciation-methods.md).

 Poistokirjoissa määritetään eri käyttöomaisuuksien poistojen laskentatavat. Kussakin kirjassa voidaan määrittää yksittäisiä poistoehtoja. Voidaan määrittää esimerkiksi, että käyttöomaisuudelle tulisi tehdä poisto kolmen vuoden jaksolla yhteen kirjaan ja viiden vuoden jaksolla toiseen kirjaan.

 Kun olet luonut asianmukaiset poistokirjat, kuhunkin käyttöomaisuuserään tulee liittää yksi tai usea poistokirja. Käyttöomaisuuteen liitettyä poistokirjaa kutsutaan käyttöomaisuuden poistokirjaksi. Poistokirjoja käyttöomaisuudelle voi määrittää kuinka monta tahansa. 

## <a name="to-create-a-depreciation-book"></a>Poistokirjan luominen
Käyttöomaisuuden poistokirjaan voidaan määrittää, miten käyttöomaisuus poistetaan. Useiden erilaisten poistomenetelmien hallitsemiseksi voidaan määrittää useita poistokirjoja.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poistokirjat** ja valitse sitten liittyvä linkki.
2. Valitse **Poistokirjaluettelo**-sivulla **Uusi**-toiminto.
3. Täytä **Poistokirjakortti**-sivun kentät tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Voit tallentaa käyttöomaisuustapahtumat **Käyttöomaisuuden KP-päiväkirja**- tai **Käyttöomaisuuspäiväkirja**-sivulle sen mukaan, koskevatko tapahtumat talousraportointia vai sisäistä hallintaa. Määritä seuraavan vaiheen mukaisesti eri käyttöomaisuustoiminnoissa oletusarvoisesti käytettävien päiväkirjojen tyypit.
4. Valitse **Integrointi**-pikavälilehdessä niiden käyttöomaisuustoimintojen valintaruudut, jotka haluat kirjata **Käyttöomaisuuden KP-päiväkirja** -sivun avulla.
5. Toista vaiheet 2–4 jokaisen sellaisen poisto- tai kirjaustavan kohdalla, jonka haluat liittää käyttöomaisuuserään poistokirjana.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>Poistokirjan liittäminen käyttöomaisuuteen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuus** ja valitse sitten liittyvä linkki.
2. Valitse käyttöomaisuus, jolle haluat määrittää käyttöomaisuuden poistokirjan.
3. Täytä **Poistokirja**-pikavälilehden kentät tarvittaessa.
4. Jos käyttöomaisuuteen on liitettävä useita poistokirjoja, valitse **Lisää poistokirjoja** -toiminto.
5. Vaihtoehtoisesti voit valita **Poistokirjat**-toiminnon ja määrittää vähintään yhden käyttöomaisuuden poistokirjan.

    > [!NOTE]  
    >   Kun käytössä on manuaalinen poistomenetelmä, poistot on vietävä manuaalisesti käyttöomaisuuden KP-päiväkirjaan. **Laske poisto** -toiminto jättää huomiotta käyttöomaisuuserät, joille käytetään manuaalista poistomenetelmää. Tätä tapaa voidaan käyttää omaisuuserille, joille ei tehdä poistoja, kuten maa-alueille.

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>Poistokirjan liittäminen useisiin käyttöomaisuuseriin eräajon avulla
Jos haluat määrittää poistokirjan moneen käyttöomaisuuteen, voit luoda **Luo KO:n poistokirjat** -eräajolla käyttöomaisuuden poistokirjat.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuus** ja valitse sitten liittyvä linkki.
2. Valitse käyttöomaisuus, jolle haluat määrittää ja liittää poistokirjan. Valitse sitten **Muokkaa**-toiminto.
3. Valitse **Poistokirjakortti**-sivulla **Luo KO:n poistokirjat** -toiminto.
4. Täytä **Luo KO:n poistokirjat** -sivun **Poistokirja**-kenttä.
5. Valitse ensin **Kopioi KO:sta nro** -kenttä ja valitse sen käyttöomaisuuserän numero, jota haluat käyttää pohjana uusien käyttöomaisuuspoistokirjojen luomisessa.

    Jos tämä kenttä täytetään, uusien KO-poistokirjojen poistokentissä on samat tiedot kuin kopioitavan KO-poistokirjan vastaavissa kentissä. Jätä kenttä tyhjäksi, jos haluat luoda uusia KO:n poistokirjoja, joissa on tyhjiä poistokenttiä.  
6. **Käyttöomaisuus**-pikavälilehteen voidaan asettaa suodatus valitsemaan se omaisuus, jolle halutaan luoda käyttöomaisuuden poistokirjat.
7. Valitse **OK**-painike.

## <a name="to-set-up-depreciation-posting-types"></a>Poiston kirjaustyyppien määrittäminen
Kunkin poistokirjan osalta on määritettävä, miten [!INCLUDE[prod_short](includes/prod_short.md)] käsittelee eri kirjaustyyppejä. Voit esimerkiksi määrittää, että tuleeko kirjauksen olla debet vai kredit, ja tuleeko kirjaustyyppi sisällyttää poistopohjaan.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poistokirjat** ja valitse sitten liittyvä linkki.  
2. Valitse poistokirja, jonka. Valitse sitten **KO:n kirjaustyypin asetukset** -toiminto.
3. Täytä **KO:n kirjaustyypin asetukset** -sivulla tarvittavat kentät.

    > [!NOTE]  
    >   **KO:n kirjaustyypin asetukset** -sivulla ei voi lisätä rivejä eikä poistaa niitä. Ainoastaan olemassa olevia rivejä voi muuttaa.

On hyvin suositeltavaa, ettei niiden poistokirjojen asetuksia muuteta, joiden osalta on jo kirjattu tapahtumia. Muutokset eivät vaikuta jo kirjattuihin tapahtumiin, mikä tekee poistokirjatilastoista harhaanjohtavia.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>Käyttöomaisuuden poiston oletusmallien ja -erien määrittäminen
Kunkin poistokirjan osalta määritellään mallien ja erien oletusasetukset. Voit monistaa näillä oletusarvoilla yhden päiväkirjan rivit toiseen päiväkirjaan, luomaan päiväkirjarivejä **Laske poisto**- tai **Tee indeksimuutos KO:teen** -eräajoilla ja monistamaan vakuutuspäiväkirjan hankintamenoja.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poistokirjat** ja valitse sitten liittyvä linkki.  
2. Valitse poistokirja, jolle haluat määrittää oletuspäiväkirjat. Valitse sitten **KO-päiväkirjan asetukset** -toiminto.  
3. Jos haluat, että jokaisella käyttäjällä on oletusasetukset, valitse **Käyttäjätunnus**-kenttä, jotta voit tehdä valinnan **Käyttäjät**-sivulla.  
4. Valitse muille kentille oletusarvoisesti käytettävä päiväkirjamalli tai -erä.  

## <a name="see-also"></a>Katso myös
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuus](fa-manage.md)  
[Rahoitus](finance.md)  
[Käytön aloittaminen](product-get-started.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)
