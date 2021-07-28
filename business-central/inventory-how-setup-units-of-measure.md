---
title: Nimikkeen mittayksikön määrittäminen| Microsoft Docs
description: Voit määrittää nimikkeelle useita mittayksiköitä, joten voit kohdistaa mittayksiköt nimikkeeseen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 92fc62cf5b1e2db5d1eb34ab2aa9f86823cfe3bb
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435545"
---
# <a name="set-up-units-of-measure"></a>Mittayksikön määrittäminen

Mittayksiköt määritetään [!INCLUDE [prod_short](includes/prod_short.md)]in määritysten osana **Mittayksikkö**-sivulla. Kun sitten rekisteröit uusia nimikkeitä, perusmittayksikkö määritetään **nimikkeen kortissa**. Mittayksiköt voi lisätä myös myöhemmin.  

Voit määrittää useita mittayksiköitä, jotka on määritetty kohteelle niin, että voit kohdistaa nimikkeen mittayksiköt seuraaviin tarkoituksiin:

- Määritä perusmittayksikkö nimikkeen nimikekortilla määrittämään, miten se tallennetaan varastoon. Perusmittayksikkö toimii myös muuntamisen perustana vaihtoehtoisille mittayksiköille.
- Määritä vaihtoehtoiset mittayksiköt osto-, tuotanto- tai myyntiasiakirjojoille määrittääksesi, kuinka monta perusmittayksikön yksikköä käsittelet kerrallaan kyseisissä prosesseissa. Voi esimerkiksi ostaa nimikkeen kuormalavoihin ja käyttää tuotannossa vain yksittäisiä kappaleita.

Jos nimike varastoidaan yhtä mittayksikköä ja tuotetaan toista mittayksikköä käyttäen, ohjelma voi laskea komponenttien oikean määrän **Päivitä tuotantotilaus** -eräajon aikana luomalla tuotantoerän mittayksikköä käyttävän tuotantotilauksen. Tuotantoerän mittayksikön laskentaa voidaan tarvita esimerkiksi, kun nimike varastoidaan kappaleina mutta tuotetaan tonneina. Lisätietoja on kohdassa [Tuotantoerän mittayksiköiden käyttäminen](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).  

## <a name="to-set-up-units-of-measure"></a>Mittayksikön määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Mittayksiköt** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto. Uusi tyhjä rivi lisätään.  
3. Täytä kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
4. Jos tiedät, että organisaatio myy tätä mittayksikköä käyttäviä nimikkeitä asiakkaille muissa maissa, voi lisätä käännökset.  
    1. Valitse koodi, jonka käännökset haluat määrittää, ja valitse sitten **Käännökset** -toiminto.
    2. Valitse **Kielikoodi**-kentässä alanuolipainike, jolloin näyttöön tulee luettelo saatavilla olevista kielikoodeista. Valitse kielikoodi, jolle haluat syöttää käännöksen, ja kopioi sitten koodi kenttään valitsemalla OK.
    3. Syötä **Kuvaus**-kenttään asianmukainen teksti.
5. Toista edelliset vaiheet kaikkien lisättävien mittayksiköiden osalta.  

Kun rekisteröit uuden nimikkeen, voit valita perusmittayksikön mittayksikköluettelosta, joka on nyt määritetty. Voit määrittää nimikkeelle myös useita mittayksikköitä.  

## <a name="to-set-up-multiple-item-units-of-measure"></a>Useiden nimikkeiden mittayksikön määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Avaa nimikkeen kortti, jolle haluat määrittää vaihtoehtoisen mittayksikön.
3. Valitse **Mittayksiköt**-toiminto. Näyttöön tulee **Nimikkeen mittayksiköt** -sivu.
4. Jos nimikekortin **Perusmittayksikkö**-kenttä on täytetty, kyseinen mittayksikkö on jo määritetty.
5. Valitse **Uusi**-toiminto. Uusi tyhjä rivi lisätään.
6. Syötä mittayksikön nimi **Koodi**-kentässä. Vaihtoehtoisesti voit valita kenttään tietokannassa olevat mittayksikön koodit.
7. Määritä **Määrä mittayksikköä kohti** -kentässä, kuinka monta perusmittayksikön yksikköä uusi mittayksikkö sisältää.
8. **Korkeus**-, **Leveys**-, **Pituus**- ja **Paino**-kenttiin on mahdollista määrittää myös tarkat tiedot yhden mittayksikön koosta siten, että [!INCLUDE [prod_short](includes/prod_short.md)] voi laskea, montako nimikeyksikköä voidaan sijoittaa kuhunkin varastopaikkaan. **Kuutiotilavuus**-kenttä lasketaan automaattisesti **korkeuden**, **leveyden** ja **pituuden** perusteella.

    Jos joissakin näistä kentistä on jokin muu arvo kuin 0, kyseistä arvoa käytetään kaikissa prosesseissa, joissa nimikkeitä sijoitetaan varastopaikkaan. Näitä prosesseja ovat hyllytys, vastaanotot, toimitukset, noudot ja oikaisut. [!INCLUDE [prod_short](includes/prod_short.md)] tarkastaa hyllytettävien ja jo varastopaikassa olevien nimikkeiden kunkin fyysisen mitan summan vertaamalla sitä varastopaikkaan sopivan nimikkeen enimmäiskokoon tai muuhun mittaan, joka on ilmaistu nimikkeen sijaintikortin varastopaikan kapasiteettina. Kussakin dimensiossa on siis käytettävä samaa mittayksikköä kaikissa nimikkeen mittayksiköissä – esimerkiksi painoyksikkönä voi siis käyttää kilogrammoja tai paunoja, mutta niitä on käytettävä johdonmukaisesti.
9. Toista vaiheet 5-7 määrittääksesi kaikki vaihtoehtoiset mittayksiköt, joita haluat käyttää tälle nimikkeelle eri prosesseissa.

    Nimikkeen perusmittayksikköä voi tarkastella ja muuttaa **Perusmittayksikkö**-kentässä ikkunan alaosassa. Perusmittayksikön voi lisäksi vaihtaa nimikkeen kortin **Perusmittayksikkö**-kentässä. **Nimikkeen mittayksikkö** -sivun **Määrä mittayksikköä kohti** -kentässä mittayksikön arvon on oltava **1**-

Vaihtoehtoista mittayksikköä voi nyt käyttää osto-, tuotanto- ja myyntiasiakirjoissa osassa [Oletusmittayksikön koodien määrittäminen myynti- ja ostotapahtumille](#to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions) kuvatulla tavalla.  

## <a name="to-set-up-unit-of-measure-translations"></a>Mittayksikön käännösten määrittäminen

Jos myyt nimikkeitä ulkomaisille asiakkaille, mittayksikkö halutaan enkä määrittää asiakkaan kielellä. Tällä tavalla voi tehdä sen jälkeen kun tarpeelliset mittayksiköiden käännökset on määritetty.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Mittayksiköt** ja valitse sitten vastaava linkki.
2. Valitse koodi, jonka käännökset haluat määrittää, ja valitse sitten **Käännökset** -toiminto.
3. Valitse **Kielikoodi**-kentässä alanuolipainike, jolloin näyttöön tulee luettelo saatavilla olevista kielikoodeista. Valitse kielikoodi, jolle haluat syöttää käännöksen, ja kopioi sitten koodi kenttään valitsemalla OK.
4. Syötä **Kuvaus**-kenttään asianmukainen teksti.
5. Toista vaiheet 2–4 niiden mittayksikön koodien ja kielien osalta, joille haluat antaa käännöksen.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Oletusmittayksikön koodien määrittäminen myynti- ja ostotapahtumille

Jos ostat tai myyt tavallisesti eri yksiköissä kuin perusmittayksiköissä, voit määrittää erillisiä mittayksiköitä ostoille ja myynneille. Tehdäksesi näin **Nimikkeen mittayksiköt** -sivulla tulee määrittää mittayksiköitä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Avaa sen nimikkeen kortti, jolle haluat määrittää myynnin tai oston oletusmittayksikön koodin.
3. Avaa myynnin osalta **Laskutus**-pikavälilehden **Myynnin mittayksikkö** -kentässä **Nimikkeen mittayksiköt** -sivu.
4. Avaa oston osalta **Täydennys**-pikavälilehden **Oston mittayksikkö** -kentässä **Nimikkeen mittayksiköt** -sivu.
5. Valitse myynnin tai oston oletusmittayksiköksi määritettävä koodi ja valitse sitten **OK**.

## <a name="see-also"></a>Katso myös

[Tuotantoerän mittayksiköiden käyttäminen](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varaston hallinta](inventory-manage-inventory.md)  
[Ostojen hallinta](purchasing-manage-purchasing.md)  
[Myynnin hallinta](sales-manage-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]