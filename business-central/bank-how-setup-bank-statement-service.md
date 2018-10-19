---
title: "Yodlee -pankkisyötteiden määrittäminen| Microsoft Docs"
description: "Voit muuntaa maksutiedot mihin tahansa tietomuotoon, jota pankkisi edellyttää ja ottaa käyttöön pankkitiedostojen tuonnin tai viennin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, payment process
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e3d739a31c2e5a17c6ba3cc4ff1b9f158642051c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-the-envestnet-yodlee-bank-feeds-service"></a>Envestnet Yodlee -pankkisyötepalvelun määrittäminen
Voit tuoda pankistasi sähköisiä tiliotteita ja täyttää nopeasti **Maksujen täsmäytyskirjauskansio** -ikkunan maksujen kohdistamiseksi ja pankkitilin täsmäyttämiseksi. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Envestnet Yodlee -pankkisyötepalvelu on asennettu [!INCLUDE[d365fin](includes/d365fin_md.md)]iin laajennuksena. Se on valmis käyttöönottoa varten. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md).

> [!NOTE]
> Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Yhdysvalloissa, Kanadassa ja Isossa-Britanniassa.

Kun olet ottanut pankkisyötepalvelun käyttöön, pankkitili on linkitettävä siihen verkkopankkitiliin, josta syöte tulee. Voit linkittää pankkitilit verkkopankkitileihin seuraavissa erilaisissa skenaarioissa:

* Verkkopankkitilille ei ole määritetty [!INCLUDE[d365fin](includes/d365fin_md.md)]in pankkitiliä. Tämän vuoksi luodaan pankkitili linkittämällä se verkkopankkitilistä.
* [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on pankkitili, jonka haluat linkittää verkkopankkitiliin.
* Linkitetyn pankkitilin linkitys on peruutettava, koska haluat lopettaa tilin pankkisyötepalvelun käyttämisen.
* Verkkopankkitilejä on muutettu, ja haluat päivittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in pankkitilien tiedot.

Kun pankkisyötepalvelu on otettu käyttöön, voit määrittää pankkitilille uusien tiliotteiden automaattisen tuonnin **Maksujen täsmäytyskirjauskansio** -ikkunaan kahden tunnin välein. Niiden maksujen tapahtumia, jotka on jo kohdistettu ja/tai täsmäytetty **Maksujen täsmäytyskirjauskansio** -ikkunassa, ei tuoda. Lisätietoja on “Pankin tiliotteiden automaattisen tuonnin ottaminen käyttöön” -osassa.

> [!NOTE]  
> Jos käytössä on yrityksen määrittämisen avustettu asennus, jotkin seuraavien toimenpiteiden yrityksen pankkitilin asennusvaiheet suoritetaan automaattisesti. Lisätietoja on kohdassa [Käytön aloittaminen](product-get-started.md).

## <a name="to-enable-the-bank-feed-service"></a>Pankkisyötepalvelun ottaminen käyttöön
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Avaa pankkisyötepalvelussa käytettävä pankkitili.
3. Valitse **Pankkitili**-ikkunan **Pankin tiliotteen tuontimuoto** -kenttään YODLEEBANKFEED.  

Pankkisyötepalvelu otetaan käyttöön, kun linkität pankkitilin siihen liittyvään verkkopankkitiliin. Tutustu seuraaviin toimiin.  

## <a name="to-create-a-new-linked-bank-account"></a>Uuden linkitetyn pankkitilin luominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Valitse asianmukainen pankkitili ja valitse sitten **Luo uusi linkitetty pankkitili**. Hetken kuluttua näyttöön avautuu **Pankkitilin linkitys** -ikkuna.

    > [!NOTE]  
    > Tässä ikkunassa näytetään Envestnet Yodlee -pankkisyötepalvelun todellinen verkkosivu. Ikkunassa näkyvät termit ja toiminnot eivät ehkä vastaa tämän ohjeaiheen ohjeita.  
3. Käytä **Verkkopankkitilin linkitys** -ikkunan **Linkitä tili** -ruudun hakutoimintoa, kun etsit pankin, jossa sinulla on vähintään yksi verkkopankkitili.
4. Valitse pankin nimi. **Kirjaudu sisään** -ruutu avautuu.
5. Syötä käyttäjätunnus ja salasana, jota käytät kirjautuessasi verkkopankkiin, ja valitse sitten **Seuraava**-painike.  
6. Pankkisyötepalvelu valmistelee määritetyn pankin ensimmäisen verkkopankkitiliin ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in uuden pankkitilin linkityksen.

    > [!NOTE]  
    > Jos sinulla on pankissa useita verkkopankkitilejä, luo niille lisäpankkitilit [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Katso vaiheet 8–10.  

    Kun käsittely on tehty, pankin nimi näkyy **Linkitetty**-välilehden **Omat tilit** -ruudussa. Sulkeissa oleva luku osoittaa linkitettyjen verkkopankkien määrän.  
7. Valitse **OK**-painike.

    Jos linkität vain yhden verkkopankkitilin **Pankkitilin kortti** -ikkuna avautuu ja verkkopankkitilin nimi näkyy, Nyt pankkitilin linkitystehtävä on valmis. Jäljellä on enää pankkitilin määrittäminen. Lisätietoja on kohdassa [Pankkitilien määrittäminen](bank-how-setup-bank-accounts.md).

    Jos linkität useita verkkopankkitilejä, **Pankkitilin linkitys** -ikkuna avautuu. Tässä ikkunassa on luettelo verkkopankkitileistä, joita ei ole vielä linkitetty [!INCLUDE[d365fin](includes/d365fin_md.md)]in pankkitileihin. Noudata tällaisessa tapauksessa seuraavaa vaihetta.  
8. Valitse **Pankkitilin linkitys** -ikkunassa verkkopankkitilin rivi ja valitse sitten **Linkitä uuteen pankkitiliin** -toiminto.  

    Näyttöön avautuu uuden pankkitilin **Pankkitilin kortti** -ikkuna ja verkkopankkitilin nimi näkyy.

    Jos [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on jo pankkitili, johon haluat linkittää lisäverkkopankkitilin, noudata seuraavia ohjeita.  
9. Valitse **Pankkitilin linkitys** -ikkunassa verkkopankkitilin rivi ja valitse sitten **Linkitä olemassa olevaan pankkitiliin** -toiminto.
10. Valitse **Pankkitililuettelo**-ikkunassa pankkitili, johon linkitys tehdään, ja valitse sitten **OK**-painike.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Pankkitilin linkittäminen verkkopankkitiliin
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Valitse sen pankkitilin rivi, jota ei ole linkitetty verkkopankkitiliin, ja valitse sitten **Linkitä verkkopankkitiliin** -toiminto. Näyttöön avautuu **Verkkopankkitilin linkitys** -ikkuna, joka sisältää **Linkitä tili** -ruudussa annetun pankin nimen.
3. Valitse pankin nimi. **Kirjaudu sisään** -ruutu avautuu.
4. Syötä käyttäjätunnus ja salasana, jota käytät kirjautuessasi verkkopankkiin, ja valitse sitten **Seuraava**-painike.  

    Pankkisyötepalvelu valmistelee [!INCLUDE[d365fin](includes/d365fin_md.md)]in pankkitilin ja liittyvän verkkopankkitilin linkityksen.  

    Kun käsittely on tehty, pankin nimi näkyy **Linkitetty**-välilehden **Omat tilit** -ruudussa. Jos pankissa on useita pankkitilejä, vain vaiheessa 2 valittu pankkitili linkitetään.  
5. Valitse **OK**-painike.

**Pankkitililuettelo**-ikkunan **Linkitetty**-valintaruutu valitaan.

## <a name="to-unlink-a-bank-account"></a>Pankkitilin linkityksen poistaminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten liittyvä linkki.  
2. Valitse sen linkitetyn pankkitilin rivi, jonka linkityksen liittyvään verkkopankkitiliin haluat poistaa. Valitse sitten **Poista verkkopankkitilin linkitys** -toiminto.

> [!NOTE]  
> Jos valitset vahvistusvalintaikkunassa **Kyllä**, verkkopankkitilin linkki poistetaan ja sisäänkirjaustiedot poistetaan. Voit linkittää pankkitilin uudelleen verkkopankkitiliin kirjautumalla pankkiin sisään uudelleen. Lisätietoja on “Pankkitilin linkittäminen verkkopankkitiliin“ -osassa.

## <a name="to-update-bank-account-linking"></a>Pankkitilin linkityksen päivittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Valitse asianmukainen pankkitili ja valitse sitten **Päivitä pankkitilien linkitys** -toiminto.

Jos **Pankkitililuettelo**-ikkunan linkitetyissä pankkitileissä esiintyy ongelmia, näyttöön avautuu **Pankkitilin linkitys** -ikkuna, jossa kerrotaan pankkitili, jota ongelmat koskevat. Ongelmien ratkaiseminen tapahtuu parhaiten poistamalla verkkopankkitilin linkitys ja luomalla linkitys uudelleen. Lisätietoja on Pankkitilin linkittäminen verkkopankkitiliin -osassa.

## <a name="to-enable-automatic-import-of-bank-statements"></a>Pankin tiliotteiden automaattisen tuonnin ottaminen käyttöön
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Valitse linkitetyn pankkitilin rivi ja valitse sitten **Pankin tiliotteen automaattisen tuonnin asetukset** -toiminto.
3. Määritä **Pankin tiliotteen automaattisen tuonnin asetukset** -ikkunan **Sisällytettyjen päivien lukumäärä** -kentässä, miltä kaukaiselta ajalta uudet pankkitapahtumat haetaan.

    > [!NOTE]  
    > Suosittelemme arvoksi 7 päivää tai enemmän.  
4. Valitse **Käytössä**-valintaruutu.  

**Maksujen täsmäytyskirjauskansio** -ikkuna näyttää nyt tunneittain kaikki uudet verkkopankissa tehdyt maksut.

> [!NOTE]  
> Niiden maksujen tapahtumia, jotka on jo kohdistettu ja/tai täsmäytetty **Maksujen täsmäytyskirjauskansio** -ikkunassa, ei tuoda.

## <a name="see-also"></a>Katso myös
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Pankkitilien hallinta](bank-manage-bank-accounts.md)  
[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

