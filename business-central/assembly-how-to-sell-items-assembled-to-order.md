---
title: Kokoonpano tilausta varten -nimikkeiden myyminen
description: Jos kyse on kokoonpano tilausta varten -määritetystä nimikkeestä, nimikkeen ei odoteta olevan varastossa ja se on koottava myyntitilauksen mukaisesti.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting, substitute items
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 07/29/2021
ms.author: edupont
ms.openlocfilehash: ca22a5dc82e950b81829c356f5054ab7c8da1973
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534964"
---
# <a name="sell-items-assembled-to-order"></a>Kokoonpano tilausta varten -nimikkeiden myyminen

Jos kokoonpanon nimikkeen kortin **Kokoonpanokäytäntö**-kenttä sisältää **Kokoonpano tilausta varten** -kohdan, nimikettä ei oleteta olevan varastossa, vaan se on koottava myyntitilausta varten. Kun syötät nimikkeen myyntitilausriville, kokoonpanotilaus luodaan automaattisesti ja linkitetään myyntitilaukseen.  

> [!NOTE]  
>  Jos kokoonpano tilausta varten -nimikkeet ovat jo varastossa, voit vähentää kokoonpanotilauksen määrää ja varata sen varastosta. Lisätietoja on kohdassa [Varastonimikkeiden myyminen Kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Tässä toimenpiteessä käsittelet asiakkaan pyytämien määrittelyjen mukaan koottavan nimikkeen myyntiä. Vaiheita ovat myyntitilausrivin käynnistäminen, kokoonpanonimikkeen mukauttaminen muokkaamalla sen osia ja resursseja, saatavuuden tarkistaminen toimituspäivämäärän määrittämiseksi ja myyntitilauksen vapauttaminen kokoonpanoa ja välitöntä toimitusta varten.  

> [!NOTE]  
>  Seuraavassa toimenpiteessä ei tehdä myyntitilauksen vakiovaiheita ennen, kuin koontitilausnimike syötetään myyntitilauksen riville.  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Myy nimike, jok aon kokoonpano tilausta varten

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2.  Luo myyntitilaus. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).  
3.  Valitse **Nro**-kenttään nimike, jolle on määritetty kokoonpano tilausta varten.  
4.  Määritä **Sijaintikoodi**-kentässä sijainti, josta nimike myydään. Kokoonpanoprosessi tapahtuu kyseisessä sijainnissa.  
5.  Määritä **Määrä**-kentässä, miten monta yksikköä haluat myytävän.  

    > [!NOTE]  
    >  Jos vähintään yksi pyydetyn kokoonpanon nimikkeen määrän komponenteista ei ole saatavana, näyttöön avautuu yksityiskohtaisia saatavuustietoja sisältävä varoitussivu. Lisätietoja on kohdassa Kokoonpanon saatavuus.  

    Kokoonpanotilaus luodaan nyt automaattisesti ja linkitetään myyntitilauksen riviin. Kokoonpanotilauksen eräpäivä synkronoidaan myyntitilausrivin lähetyspäivämäärän kanssa.  

    Myytävä määrä on kopioitu **Kokoonpantava määrä tilausta varten** -kentästä, joka ilmaisee, että nimikkeen asennus vaatii myyntirivillä olevan täyden määrän kokoonpanon tilausta varten. Voit vähentää kokoonpano tilausta varten -määrää, jos tiedät, että jotkin osat ovat jo saatavilla. Lisätietoja on kohdassa [Varastonimikkeiden myyminen Kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6.  Jos asiakas haluaa tuotepakettiin lisänimikkeen, valitse **Rivit** -pikavälilehdessä ensin **Rivi**-toiminto, sitten **Kokoonpano tilausta varten** -toiminto ja lopuksi **Kokoonpano tilausta varten -rivit** -toiminnon. Voit nyt tarkastella ja muuta vakiokokoonpanon komponentteja. Voit myös valita **Kokoonpantava määrä tilausta varten** -kentän.  
7.  Luo **Kokoonpano tilausta varten -rivit** -sivulla pyydettyä lisäkokoonpanosisältöä varten uusi rivi, jonka tyyppi on **Nimike**. Rivi vastaa ylimääräistä kokoonpano-osaa.  

    Voit myös mukauttaa tilauksen kasvattamalla yhden perusnimikkeen paketin määrää. Voit tehdä tämän lisäämällä arvon **Määrä per** -kentässä tietylle kokoonpanon tilausriville.  

    > [!NOTE]  
    >  **Kokoonpano tilausta varten -rivit** -sivulla näytetään vain perustietokentät, joita myyjän on tarkoitus käyttää osaluettelon mukauttamiseen, nimikkeen seurantanumeroiden lisäämiseen tai osien saatavuuden ongelmanratkaisuun. Katso lisää kokoonpanotilauksen tietoja, kuten kokoonpanotilauksen aloituspäivämäärä, valitsemalla **Näytä asiakirjat**. Tämä avaa myyntitilausriviin linkitetyn kokoonpanotilauksen koko näkymän. Et voi muuttaa useimpien kenttien sisältöä kokoonpanotilauksen otsikossa, etkä voi kirjata kokoonpanon tuotosta siitä, koska koska sinun täytyy käyttää myyntitilausrivin tilauksen kirjausta.  
    >   
    >  Linkitettyjen kokoonpanotilausten otsikossa vain **Aloituspvm**-kenttää voidaan muuttaa niin, että kokoonpanotyöntekijät voivat määrittää päivämäärän, joka on ennen eräpäivää, kun he aloittavat prosessin. Linkitetyn kokoonpanotilauksen rivien kaikki kentät voidaan muuttaa siten, että varaston työntekijät voivat syöttää kulutuksen lukuja prosessin aikana.  

8.  Tarkista tai reagoi komponenttien saatavuusongelmiin. Valitse esimerkiksi saatavilla oleva korvaava nimike.  
9. Sulje **Kokoonpano tilausta varten -rivit** -sivu. Linkitetty kokoonpanotilaus on nyt valmiina mukautettujen nimikkeiden kokoonpanon aloittamiseen eräpäivään mennessä.  
10. Valitse myyntitilauksessa **Vapauta**-toiminto, jos haluat ilmoittaa kokoonpano-osastolle, että kokoonpanoprosessi voidaan aloittaa.  
11. Suorita kokoonpanoosastossa niiden nimikkeiden kokoamisvaiheet, jotka myydään tässä käsittelyssä. Lisätietoja on kohdassa [Nimikkeiden kokoaminen](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> Huomaa, että nimikkeen korvaaminen ei automaattisesti aiheuta nimikkeen korvaamista toisella nimikkeellä esimerkiksi myyntitilausta luotaessa tai tuoterakenteessa. Sen sijaan sinua varoitetaan siitä, että käytettävissäsi on korvaaminen.

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/assemble-to-order-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)  
[Varasto](inventory-manage-inventory.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
