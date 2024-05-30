---
title: Kestävyysmääritys
description: Tutustu kestävyysominaisuuksien määrittämiseen.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 05/08/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="sustainability-setup"></a>Vastuullisuusmääritys

Ennen kuin kestävyysmoduuli voi toimia oikein, sinun on määritettävä joitain perusohjausobjekteja ja ohjeita, jotka liittyvät koko toimintoon.

Määritä kestävyysmoduuli noudattamalla vaiheita:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kestävyyden asetukset** ja valitse sitten vastaava linkki.
2. Määritä **Yleinen**-pikavälilehdessä tähän kestävyysmoduuliin liittyvät pakolliset kentät.

    | Kenttä | Kuvaus |
    |-------|-------------|
    | **Päästön mittayksikön koodi** | Määrittää mittayksikön koodin, jota käytetään päästöjen rekisteröintiin. |
    | **Päästön desimaalit** | Määrittää desimaalien määrän, joka näkyy päästömäärille. Oletusasetus *2:5* tarkoittaa, että kaikki summat näyttävät vähintään 2 desimaalia ja enintään 5 desimaalia. Voit syöttää myös kiinteän luvun. Jos syötät esimerkiksi *2*, kaikille summille näytetään kaksi desimaalia. |
    | **Maa tai alue pakollinen** | Määritä, onko maa/alue pakollinen. Käyttäjät voivat asettaa maa-/aluekentän päiväkirjoihin, vaikka et valitsekaan tätä kenttää. Valitsemalla kentän kuitenkin vaadit, että käyttäjät määrittävät maa-/aluekentän ennen kirjausta. |
    | **Vastuupaikka pakollinen** | Määrittää, onko vastuupaikka pakollinen. Vastuupaikkaa voidaan käyttää laitoksena, jotta voidaan mitata tiloihin perustuvia päästöjä. Käyttäjät voivat asettaa vastuukeskuskentän päiväkirjoihin, vaikka et valitsekaan tätä kenttää. Valitsemalla kentän kuitenkin vaadit, että käyttäjät määrittävät vastuukeskuskentän ennen kirjausta. |
    | **Estä laskentaperusteen muutos, jos tapahtumakirjauksia on olemassa** | Määritä, estetäänkö tilikategoriatason laskentaperustan (kaavan) muutokset kestävän kehityksen kirjaamisen yhteydessä, kun kaavaa on jo käytetty. |
    | **Ota käyttöön taustavirheen tarkistus** | Määrittää, onko vastuullisuuspäiväkirjan rivien taustavirheen tarkistus käytössä. |

    > [!NOTE]
    > Kun olet ottaa taustavirhetarkistuksen käyttöön päiväkirjoissa tai poista sen käytöstä, kirjaudu uudelleen sisään ennen uusien asetusten aloittamista.

3. Määritä **Laskennat**-pikavälilehdessä pakolliset kentät, jotka liittyvät päästöjen laskennassa käytettyihin kaavoihin.

    | Kenttä | Kuvaus |
    |-------|-------------|
    | **Polttoaineen/sähkön desimaalit** | Määrittää polttoaine-/sähkömäärissä näytettävien desimaalien määrän. Oletusasetus *2:5* tarkoittaa, että kaikki summat näyttävät vähintään 2 desimaalia ja enintään 5 desimaalia. Voit syöttää myös kiinteän luvun. Jos syötät esimerkiksi *2*, kaikille summille näytetään kaksi desimaalia. |
    | **Etäisyyden desimaalit** | Määrittää etäisyysmittauksissa näytettävien desimaalien määrän. Oletusasetus *2:5* tarkoittaa, että kaikki summat näyttävät vähintään 2 desimaalia ja enintään 5 desimaalia. Voit syöttää myös kiinteän luvun. Jos syötät esimerkiksi *2*, kaikille summille näytetään kaksi desimaalia. |
    | **Mukautettu summan desimaalien määrä** | Määrittää desimaalien määrän, joka näkyy mukautetuille määrille. Oletusasetus *2:5* tarkoittaa, että kaikki summat näyttävät vähintään 2 desimaalia ja enintään 5 desimaalia. Voit syöttää myös kiinteän luvun. Jos syötät esimerkiksi *2*, kaikille summille näytetään kaksi desimaalia. |

4. Täytä **Raportointi**-pikavälilehden asetukset määrittämällä viranomaisille raportointiin liittyvät kentät.

    > [!NOTE]
    > Versiossa 24.0 [!INCLUDE[prod_short](includes/prod_short.md)] ei tue raportointia millekään viranomaiselle. Tämän vuoksi tämän ominaisuuden määrittämiseen liittyvät kentät **Raportointi**-pikavälilehdessä on tarkoitettu tuleville raportointiominaisuuksille. Kumppanit voivat kuitenkin käyttää näitä kenttiä myös lokalisoiduissa versioissa.

    | Kenttä | Kuvaus |
    |-------|-------------|
    | **Päästöraportoinnin mittayksikön koodi** | Määritä mittayksikön koodi, jota käytetään raportoitaessa päästöjä, koska eri mittayksikköä voidaan käyttää viranomaisille raportoitaessa. Tämä kenttä ei sovellu vakioraportteihin. |
    | **Raportoinnin UOM-kerroin** | Määritä mittayksikkökerroin, jota käytetään päästöjen rekisteröintiin, jos käytät eri mittayksikköä raportoidessasi viranomaisille. |
    | **Päästön pyöristystarkkuus** | Määritä sen välin suuruus, jota käytetään pyöristettäessä päästösummia viranomaisille raportoitaessa. |
    | **Päästön pyöristystyyppi** | Määritä, miten ohjelma pyöristää päästösummat, kun raportoidaan viranomaisille. Käytettävissä ovat seuraavat vaihtoehdot: **Lähin**, **Ylös** ja **Alas**. |

## <a name="see-also"></a>Katso myös

[Taloushallinto](finance.md)  
[Vastuullisuuden hallinnan yleiskatsaus](finance-manage-sustainability.md)  
[Kestävyystilien tilikartta ja kirjanpito](finance-sustainability-accounts-ledger.md)  
[Kestävyystapahtumien tallentaminen](finance-sustainability-journal.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
