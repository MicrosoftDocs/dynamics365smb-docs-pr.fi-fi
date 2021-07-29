---
title: Yodlee Bank Feedsin määrittäminen
description: Voit muuntaa maksutiedot mihin tahansa tietomuotoon, jota pankkisi edellyttää ja ottaa käyttöön pankkitiedostojen tuonnin tai viennin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, payment process
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a01bbbcb158e975c2b6f21ce2dd2468f8b3fa431
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443521"
---
# <a name="set-up-the-envestnet-yodlee-bank-feeds-service"></a>Envestnet Yodlee Bank Feeds -palvelun määrittäminen

Voit tuoda pankistasi sähköisiä tiliotteita ja täyttää nopeasti **Maksujen täsmäytyskirjauskansio** -sivun maksujen kohdistamiseksi ja pankkitilin täsmäyttämiseksi. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!IMPORTANT]
> Eurooppalaisen maksupalveludirektiivin vuoksi (PSD2) tiliotteita ei voi enää 14.9.2019 jälkeen tuoda automaattisesti [!INCLUDE[prod_short](includes/prod_short.md)]iin brittiläisistä pankeista. Tutkimme mahdollisuutta ottaa tämä ominaisuus uudelleen käyttöön tulevaisuudessa.

> [!NOTE]
> Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Business Central -sovelluksen online-versiossa. Tämän toiminnon paikallista käyttöä varten on hankittava yhteistili Envestnetistä ja lisättävä koodi Yodlee-ohjelmointirajapinnan integrointia varten.
>
> Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Yhdysvalloissa ja Kanadassa.
> Vain näissä maissa sijaitsevia pankkeja tuetaan, vaikka muiden maiden pankit voivat näkyä Envestnet Yodlee Bank Feeds -pankin valintaikkunassa [!INCLUDE[prod_short](includes/prod_short.md)]:ssa.

> [!IMPORTANT]
> Jos haluat teknistä apua Envestnet Yodlee -toimintojen kanssa, ota yhteyttä Microsoft-tukeen. Älä ota yhteyttä Envestnet Yodleen. Lisätietoja on kohdassa [Dynamics 365 Business Central -sovelluksen teknisen tuen määrittäminen](/dynamics365/business-central/dev-itpro/technical-support)

Envestnet Yodlee Bank Feeds -palvelu on asennettu [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen online-versioon laajennuksena. Se on valmis käyttöönottoa varten tuetuissa maissa. Lisätietoja on kohdassa [[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md).

Kun olet ottanut pankkisyötepalvelun käyttöön, pankkitili on linkitettävä siihen verkkopankkitiliin, josta syöte tulee. Voit linkittää pankkitilit verkkopankkitileihin seuraavissa erilaisissa skenaarioissa:

* Verkkopankkitilille ei ole määritetty [!INCLUDE[prod_short](includes/prod_short.md)]in pankkitiliä. Tämän vuoksi luodaan pankkitili linkittämällä se verkkopankkitilistä.
* [!INCLUDE[prod_short](includes/prod_short.md)]issa on pankkitili, jonka haluat linkittää verkkopankkitiliin.
* Linkitetyn pankkitilin linkitys on peruutettava, koska haluat lopettaa tilin pankkisyötepalvelun käyttämisen.
* Verkkopankkitilejä on muutettu, ja haluat päivittää [!INCLUDE[prod_short](includes/prod_short.md)]in pankkitilien tiedot.

Kun pankkisyötepalvelu on otettu käyttöön, voit määrittää pankkitilille uusien tiliotteiden automaattisen tuonnin **Maksujen täsmäytyskirjauskansio** -sivun kahden tunnin välein. Niiden maksujen tapahtumia, jotka on jo kohdistettu ja/tai täsmäytetty **Maksujen täsmäytyskirjauskansio** -sivulla, ei tuoda. Lisätietoja on “Pankin tiliotteiden automaattisen tuonnin ottaminen käyttöön” -osassa.

> [!NOTE]  
> Jos käytössä on yrityksen määrittämisen avustettu määritys, jotkin seuraavien toimenpiteiden yrityksen pankkitilin asennusvaiheet suoritetaan automaattisesti. Lisätietoja on ohjeaiheessa [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).

## <a name="to-enable-the-bank-feed-service"></a>Pankkisyötepalvelun ottaminen käyttöön
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.
2. Avaa pankkisyötepalvelussa käytettävä pankkitili.
3. Valitse **Pankkitili**-sivun **Pankin tiliotteen tuontimuoto** -kenttään YODLEEBANKFEED.  

Pankkisyötepalvelu otetaan käyttöön, kun linkität pankkitilin siihen liittyvään verkkopankkitiliin. Tutustu seuraaviin toimiin.  

> [!NOTE]
> Jos käytät **Yrityksen asennus** -asetusten ohjattua määritystä, voit ottaa palvelun käyttöön valitsemalla **Käytä pankin syötepalvelua** -valintaruudun. Lisätietoja on kohdassa [Uusien yritysten luominen Business Centralissa](about-new-company.md).

## <a name="to-create-a-new-linked-bank-account"></a>Uuden linkitetyn pankkitilin luominen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.
2. Valitse asianmukainen pankkitili ja valitse sitten **Luo uusi linkitetty pankkitili**. Hetken kuluttua näyttöön avautuu **Pankkitilin linkitys** -sivu.

    > [!NOTE]  
    > Tällä sivulla näytetään Envestnet Yodlee Bank Feeds -palvelun todellinen verkkosivu. Sivulla näkyvät termit ja toiminnot eivät ehkä vastaa tämän ohjeaiheen ohjeita.  
3. Käytä **Verkkopankkitilin linkitys** -sivun **Linkitä tili** -ruudun hakutoimintoa, kun etsit pankin, jossa sinulla on vähintään yksi verkkopankkitili.
4. Valitse pankin nimi. **Kirjaudu sisään** -ruutu avautuu.
5. Syötä käyttäjätunnus ja salasana, jota käytät kirjautuessasi verkkopankkiin, ja valitse sitten **Seuraava**-painike.  
6. Pankkisyötepalvelu valmistelee määritetyn pankin ensimmäisen verkkopankkitiliin ja [!INCLUDE[prod_short](includes/prod_short.md)]in uuden pankkitilin linkityksen.

    > [!NOTE]  
    > Jos sinulla on pankissa useita verkkopankkitilejä, luo niille lisäpankkitilit [!INCLUDE[prod_short](includes/prod_short.md)]iin. Katso vaiheet 8–10.  

    Kun käsittely on tehty, pankin nimi näkyy **Linkitetty**-välilehden **Omat tilit** -ruudussa. Sulkeissa oleva luku osoittaa linkitettyjen verkkopankkien määrän.  
7. Valitse **OK**-painike.

    Jos linkität vain yhden verkkopankkitilin **Pankkitilin kortti** -sivu avautuu ja verkkopankkitilin nimi näkyy, Nyt pankkitilin linkitystehtävä on valmis. Jäljellä on enää pankkitilin määrittäminen. Lisätietoja on kohdassa [Pankkitilien määrittäminen](bank-how-setup-bank-accounts.md).

    Jos linkität useita verkkopankkitilejä, **Pankkitilin linkitys** -sivu avautuu. Tällä sivulla on luettelo verkkopankkitileistä, joita ei ole vielä linkitetty [!INCLUDE[prod_short](includes/prod_short.md)]in pankkitileihin. Noudata tällaisessa tapauksessa seuraavaa vaihetta.  
8. Valitse **Pankkitilin linkitys** -sivulla verkkopankkitilin rivi ja valitse sitten **Linkitä uuteen pankkitiliin** -toiminto.  

    Näyttöön avautuu uuden pankkitilin **Pankkitilin kortti** -sivu ja verkkopankkitilin nimi näkyy.

    Jos [!INCLUDE[prod_short](includes/prod_short.md)]issa on jo pankkitili, johon haluat linkittää lisäverkkopankkitilin, noudata seuraavia ohjeita.  
9. Valitse **Pankkitilin linkitys** -sivulla verkkopankkitilin rivi ja valitse sitten **Linkitä olemassa olevaan pankkitiliin** -toiminto.
10. Valitse **Pankkitililuettelo**-sivulla pankkitili, johon linkitys tehdään, ja valitse sitten **OK**-painike.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Pankkitilin linkittäminen verkkopankkitiliin
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.
2. Valitse sen pankkitilin rivi, jota ei ole linkitetty verkkopankkitiliin, ja valitse sitten **Linkitä verkkopankkitiliin** -toiminto. Näyttöön avautuu **Verkkopankkitilin linkitys** -sivu, joka sisältää **Linkitä tili** -ruudussa annetun pankin nimen.
3. Valitse pankin nimi. **Kirjaudu sisään** -ruutu avautuu.
4. Syötä käyttäjätunnus ja salasana, jota käytät kirjautuessasi verkkopankkiin, ja valitse sitten **Seuraava**-painike.  

    Pankkisyötepalvelu valmistelee [!INCLUDE[prod_short](includes/prod_short.md)]in pankkitilin ja liittyvän verkkopankkitilin linkityksen.  

    Kun käsittely on tehty, pankin nimi näkyy **Linkitetty**-välilehden **Omat tilit** -ruudussa. Jos pankissa on useita pankkitilejä, vain vaiheessa 2 valittu pankkitili linkitetään.  
5. Valitse **OK**-painike.

**Pankkitililuettelo**-sivun **Linkitetty**-valintaruutu valitaan.

## <a name="to-unlink-a-bank-account"></a>Pankkitilin linkityksen poistaminen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.  
2. Valitse sen linkitetyn pankkitilin rivi, jonka linkityksen liittyvään verkkopankkitiliin haluat poistaa. Valitse sitten **Poista verkkopankkitilin linkitys** -toiminto.

> [!NOTE]  
> Jos valitset vahvistusvalintaikkunassa **Kyllä**, verkkopankkitilin linkki poistetaan ja sisäänkirjaustiedot poistetaan. Voit linkittää pankkitilin uudelleen verkkopankkitiliin kirjautumalla pankkiin sisään uudelleen. Lisätietoja on “Pankkitilin linkittäminen verkkopankkitiliin“ -osassa.

## <a name="to-update-bank-account-linking"></a>Pankkitilin linkityksen päivittäminen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.
2. Valitse asianmukainen pankkitili ja valitse sitten **Päivitä pankkitilien linkitys** -toiminto.

Jos **Pankkitililuettelo**-sivun linkitetyissä pankkitileissä esiintyy ongelmia, näyttöön avautuu **Pankkitilin linkitys** -sivu, jossa kerrotaan pankkitili, jota ongelmat koskevat. Ongelmien ratkaiseminen tapahtuu parhaiten poistamalla verkkopankkitilin linkitys ja luomalla linkitys uudelleen. Lisätietoja on Pankkitilin linkittäminen verkkopankkitiliin -osassa.

## <a name="to-enable-automatic-import-of-bank-statements"></a>Pankin tiliotteiden automaattisen tuonnin ottaminen käyttöön
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.
2. Valitse linkitetyn pankkitilin rivi ja valitse sitten **Pankin tiliotteen automaattisen tuonnin asetukset** -toiminto.
3. Määritä **Pankin tiliotteen automaattisen tuonnin asetukset** -sivun **Sisällytettyjen päivien lukumäärä** -kentässä, miltä kaukaiselta ajalta uudet pankkitapahtumat haetaan.

    > [!NOTE]  
    > Suosittelemme arvoksi 7 päivää tai enemmän.  
4. Valitse **Käytössä**-valintaruutu.  

**Maksujen täsmäytyskirjauskansio** -sivu näyttää nyt tunneittain kaikki uudet verkkopankissa tehdyt maksut.

> [!NOTE]  
> Niiden maksujen tapahtumia, jotka on jo kohdistettu ja/tai täsmäytetty **Maksujen täsmäytyskirjauskansio** -sivulla, ei tuoda.

## <a name="see-also"></a>Katso myös
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]