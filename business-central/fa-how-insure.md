---
title: Käyttöomaisuuden vakuuttaminen
description: Voit liittää käyttöomaisuuserän vakuutussopimukseen kirjaamalla vakuutuksen kattavuustapahtuman **Vakuutuspäiväkirja**-sivulta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'policy, coverage'
ms.search.form: '5647, 5644, 5653, 5651, 5655, 5652, 5645, 5656, 5646, 5648, 9275'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="insure-fixed-assets"></a>Käyttöomaisuuden vakuuttaminen

Käytä Vakuutuskortti-sivua **määrittääksesi** vakuutussopimuksen kattamaan yhtä tai useampaa käyttöomaisuuserää. Yhteen vakuutussopimukseen voi määritellä yhden käyttöomaisuuserän tai useita käyttöomaisuuserää.

Voit liittää käyttöomaisuuserän vakuutussopimukseen kirjaamalla vakuutuksen kattavuustapahtuman **Vakuutuspäiväkirja**-sivulta.

Lisäksi voit liittää käyttöomaisuuserän vakuutussopimukseen ja luoda kattavuustapahtumia sen hankintamenon kirjaamisen yhteydessä. Hankintameno kirjataan käyttöomaisuuspäiväkirjasta Vakuutusnro-kentän **avulla.** -kenttä täytetty. Automaattinen vakuutuskirjaus **-vaihto** tulee ottaa käyttöön **Käyttöomaisuuden asetukset -** sivulla. Lisätietoja on kohdassa [Käyttöomaisuuden hankkiminen käyttöomaisuuden KP-päiväkirjaa](fa-how-acquire.md#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal) käyttämällä.

 **Jos Käyttöomaisuuden asetukset -** sivulla olevaa **Automaattinen vakuutuskirjaus** -vaihtoa ei ole otettu käyttöön, hankintamenojen kirjaaminen käyttöomaisuuspäiväkirjasta luo rivejä **Vakuutuspäiväkirja-sivulle** . Rivit täytyy kirjata manuaalisesti.

> [!WARNING]  
> Jos Käyttöomaisuuden asetukset -sivulla ei ota käyttöön **Automaattinen vakuutuskirjaus** - **vaihtoa**, vakuutuspäiväkirjan tulisi perustua päiväkirjamalliin, jolla ei ole numerosarjaa. Tämä johtuu siitä, että käyttöomaisuuspäiväkirjan rivistä lisätyt asiakirjanumerot ovat muussa tapauksessa ristiriidassa vakuutuspäiväkirjan numerosarjojen kanssa. Lisätietoja päiväkirjojen malleista ja eristä on kohdassa [Käyttöomaisuuden yleisten tietojen määrittäminen](fa-how-setup-general.md).

Sen jälkeen kun käyttöomaisuus on määritelty vakuutussopimukseen, **käyttöomaisuuskortin Vakuutus-kentässä** lukee **Kyllä**. Kun käyttöomaisuutta myydään, vaihto poistetaan automaattisesti käytöstä.

## <a name="to-create-or-modify-an-insurance-card"></a>Vakuutuskortin luominen tai muokkaaminen

Kun saat tiedon kattavuussumman muutoksista, uudet tiedot on annettava **Vakuutuskortti**-sivulla, jotta vakuutussopimuksen kattavuus voitaisiin analysoida oikein.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vakuutus** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto, kun haluat luoda vakuutussopimukselle uuden kortin. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vaihtoehtoisesti voit valita muutettavan vakuutussopimuksen ja valita sitten **Muokkaa**-toiminnon.

## <a name="to-assign-a-fixed-asset-to-an-insurance-policy-by-posting-from-the-insurance-journal"></a>Käyttöomaisuuden liittäminen vakuutussopimukseen vakuutuspäiväkirjasta kirjaamalla

Liitä käyttöomaisuus vakuutussopimukseen vakuutuksen kattavuustapahtumaan kirjaamalla.  

Seuraavassa kerrotaan, miten vakuutuspäiväkirjan rivi luodaan manuaalisesti.  **Jos Automaattinen vakuutuskirjaus** -vaihto on käytössä **Käyttöomaisuuden asetukset -** sivulla, vakuutuspäiväkirjan rivit luodaan automaattisesti silloin, kun hankintamenoja kirjataan. Tällöin ei tarvitse tehdä muuta kuin kirjata päiväkirja.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vakuutuspäiväkirjat** ja valitse sitten vastaava linkki.  
2. Avaa kyseessä oleva päiväkirja ja täytä vaaditut päiväkirjarivit.  
3. Voit liittää yhteen vakuutussopimukseen useita käyttöomaisuuseriä luomalla päiväkirjarivejä, joiden **Vakuutusnro**-kentässä on sama arvo ja **KO-nro**-kentässä on eri arvot.  
4. Valitse **Kirjaa**-toiminto.  

    > [!NOTE]  
    > Vakuutuspäiväkirjan tapahtumat kirjataan vain vakuutuksen kattavuuskirjauksiin.  

## <a name="to-update-the-insurance-value-of-a-fixed-asset"></a>Käyttöomaisuuden vakuutusarvon päivittäminen

**Tee indeksimuutos vakuutuksiin** -eräajoa voidaan käyttää päivittämään katetun käyttöomaisuuden arvoa.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tee indeksimuutos vakuutuksiin** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät.

    > [!NOTE]  
    >   **Indeksiluku**-kenttään annetaan esimerkiksi 5 %:n pienentämistä varten 95, kun taas 2 %:n suurentamiseksi annetaan 102.  
3. Valitse **OK**-painike.  

   Eräajo laskee uudeksi summaksi prosenttiosuuden vakuutetusta kokonaisarvosta **Vakuutustilastot**-sivun arvon mukaan. Tämän jälkeen luodaan rivi vakuutuspäiväkirjaan.  
4. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vakuutuspäiväkirjat** ja valitse sitten vastaava linkki.  
5. Avaa kyseinen vakuutuspäiväkirja, tarkista luodut arvot ja kirjaa ne vakuutuksen kattavuustapahtumiin.  

## <a name="to-monitor-insurance-coverage"></a>Vakuutuksen kattavuuden valvonta

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää vakuutussopimusten analysoimiseen ja käyttöomaisuuserien yli- ja alivakuuttamisen määrittämiseen tarkoitettuja raportti- ja tilastosivuja.  

### <a name="overview-of-insurance-policies"></a>Yleiskuva vakuutussopimuksista

Saat yleiskuvan vakuutussopimuksista esikatselemalla tai tulostamalla **Vakuutus – Luettelo** -raportin. Raportti näyttää kaikki käytännöt ja vakuutuskorttien tärkeimmät kentät.  

### <a name="insurance-coverage"></a>Vakuutusturva

Tarkastele, mitä käyttöomaisuuseriä vakuutussopimukset kattavat ja millaisista summista on kyse, esikatselemalla tai tulostamalla **Vakuutus – Vakuut. arvo yht.** -raportin.  

#### <a name="overunder-coverage"></a>Yli-/alikattavuus

Voit tarkastaa seuraavilla tavoilla, onko käyttöomaisuus yli- vai alivakuutettu:  

* **Vakuutustilastot**-sivu. Jos **Ali-/ylivakuutus**-kentässä on positiivinen summa, käyttöomaisuus on ylivakuutettu. Negatiivinen summa tarkoittaa, että omaisuuserä on alivakuutettu.  
* **Käyttöomaisuustilastot**-sivu. Valitse **Kokonaisvakuutusarvo**-kenttä, kun haluat tarkastella **Vakuutuksen kattav.tapahtumat** -sivua.  
* **Yli-/alikattavuus**-raportti.  
* **Vakuutusanalyysi**-raportti.  

### <a name="uninsured-fixed-assets"></a>Vakuuttamaton käyttöomaisuus

Tarkastaaksesi, unohditko määritellä käyttöomaisuuden vakuutussopimukseen, voit tulostaa tai esikatsella **Vakuutus – Vakuuttamaton KO -raporttia** . Tässä raportissa näkyvät käyttöomaisuuserät, joiden osalta ei kirjata summia vakuutuksen kattavuustapahtumiin.  

## <a name="to-view-insurance-coverage-ledger-entries"></a>Vakuutuksen kattavuustapahtumien katsominen

Vakuutuksen kattavuuskirjauksiin tehtyjä tapahtumia voi katsoa.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vakuutus** ja valitse sitten vastaava linkki.  
2. Valitse haluamasi vakuutussopimus ja valitse sitten **Vakuutuksen kattav.tapahtumat** -toiminto.  

## <a name="to-view-the-total-insurance-value-of-fixed-assets"></a>Käyttöomaisuuden kokonaisvakuutusarvon tarkasteleminen

Matriisi-sivulla näkyvät vakuutusarvot, jotka on rekisteröity kullekin vakuutussopimukselle kunkin käyttöomaisuuserän osalta, joka on seurausta kirjatuista vakuutukseen liittyvistä summista.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vakuutus** ja valitse sitten vastaava linkki.  
2. Valitse haluamasi vakuutussopimus ja valitse sitten **Vakuutusarvo KO-erää kohti** -toiminto.  
3. Täytä tarvittavat kentät.  
4. Valitse **Näytä matriisi** -toiminto.  
5. Voit tarkastella perusteena olevia vakuutuksen kattavuustapahtumia valitsemalla arvon matriisista.  

## <a name="to-correct-insurance-coverage-entries"></a>Vakuutuksen kattavuustapahtumien korjaaminen

Jos käyttöomaisuus määriteltiin väärään vakuutussopimukseen, sen voi korjata luomalla kaksi uudelleenluokitustapahtumaa vakuutuspäiväkirjasta.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vakuutuspäiväkirjat** ja valitse sitten vastaava linkki.  
2. Luo käyttöomaisuudelle yksi päiväkirjarivi ja korjaa vakuutussopimus, jonka **Summa**-kentän arvo on positiivinen.  
3. Luo käyttöomaisuudelle toinen päiväkirjarivi ja virheellinen vakuutussopimus, jonka **Summa**-kentän arvo on negatiivinen.  
4. Valitse **Kirjaa**-toiminto.  

Käyttöomaisuus poistetaan toisen rivin virheellisistä vakuutussopimuksista. Omaisuuserä määritellään oikeaan vakuutussopimukseen päiväkirjan ensimmäisellä rivillä.  

## <a name="see-also"></a>Katso myös

[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Taloushallinto](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
