---
title: "Toimintaohje: Envestnet Yodlee -pankkisyötepalvelun määrittäminen| Microsoft Docs"
description: "Toimintaohje: Envestnet Yodlee -pankkisyötepalvelun määrittäminen"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, payment process
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 62c314958700257f5889b69c8724a4348929765f
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-the-envestnet-yodlee-bank-feeds-service"></a>Toimintaohje: Envestnet Yodlee -pankkisyötepalvelun määrittäminen
Voit tuoda pankistasi sähköisiä tiliotteita ja täyttää nopeasti **Maksujen täsmäytyskirjauskansio** -ikkunan maksujen kohdistamiseksi ja pankkitilin täsmäyttämiseksi. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Envestnet Yodlee -pankkisyötepalvelu on asennettu [!INCLUDE[d365fin](includes/d365fin_md.md)]iin laajennuksena. Se on valmis käyttöönottoa varten. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennuksilla](ui-extensions.md).

Kun olet ottanut pankkisyötepalvelun käyttöön, pankkitili on linkitettävä siihen verkkopankkitiliin, josta syöte tulee. Voit linkittää pankkitilit verkkopankkitileihin seuraavissa erilaisissa skenaarioissa:

* Verkkopankkitilille ei ole määritetty [!INCLUDE[d365fin](includes/d365fin_md.md)]in pankkitiliä. Tämän vuoksi luodaan pankkitili linkittämällä se verkkopankkitilistä.
* [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on pankkitili, jonka haluat linkittää verkkopankkitiliin.
* Linkitetyn pankkitilin linkitys on peruutettava, koska haluat lopettaa tilin pankkisyötepalvelun käyttämisen.
* Verkkopankkitilejä on muutettu, ja haluat päivittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in pankkitilien tiedot.

Kun pankkisyötepalvelu on otettu käyttöön, voit määrittää pankkitilille uusien tiliotteiden automaattisen tuonnin **Maksujen täsmäytyskirjauskansio** -ikkunaan kahden tunnin välein. Niiden maksujen tapahtumia, jotka on jo kohdistettu ja/tai täsmäytetty **Maksujen täsmäytyskirjauskansio** -ikkunassa, ei tuoda. Lisätietoja on “Pankin tiliotteiden automaattisen tuonnin ottaminen käyttöön” -osassa.

**Huomautus**: Jos käytössä on yrityksen määrittämisen avustettu asennus, jotkin seuraavien toimenpiteiden yrityksen pankkitilin asennusvaiheet suoritetaan automaattisesti. Lisätietoja on kohdassa [Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin](index.md).

## <a name="to-enable-the-bank-feed-service"></a>Pankkisyötepalvelun ottaminen käyttöön
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Avaa pankkisyötepalvelussa käytettävä pankkitili.
3. Valitse **Pankkitili**-ikkunan **Pankin tiliotteen tuontimuoto** -kenttään YODLEEBANKFEED.  

Pankkisyötepalvelu otetaan käyttöön, kun linkität pankkitilin siihen liittyvään verkkopankkitiliin. Tutustu seuraaviin toimiin.  

## <a name="to-create-a-new-linked-bank-account"></a>Uuden linkitetyn pankkitilin luominen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Valitse asianmukainen pankkitili ja valitse sitten **Luo uusi linkitetty pankkitili**. Hetken kuluttua näyttöön avautuu **Pankkitilin linkitys** -ikkuna.

    **Huomautus:** Tässä ikkunassa näytetään Envestnet Yodlee -pankkisyötepalvelun todellinen verkkosivu. Ikkunassa näkyvät termit ja toiminnot eivät ehkä vastaa tämän ohjeaiheen ohjeita.  
3. Käytä **Verkkopankkitilin linkitys** -ikkunan **Linkitä tili** -ruudun hakutoimintoa, kun etsit pankin, jossa sinulla on vähintään yksi verkkopankkitili.
4. Valitse pankin nimi. **Kirjaudu sisään** -ruutu avautuu.
5. Syötä käyttäjätunnus ja salasana, jota käytät kirjautuessasi verkkopankkiin, ja valitse sitten **Seuraava**-painike.  
6. Pankkisyötepalvelu valmistelee määritetyn pankin ensimmäisen verkkopankkitiliin ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in uuden pankkitilin linkityksen.

    **Huomautus:** Jos sinulla on pankissa useita verkkopankkitilejä, luo niille lisäpankkitilit [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Katso vaiheet 8–10.  

    Kun prosessi on valmis, pankin nimi näkyy **Linkitetty**-välilehden **Omat tilit**-ruudussa. Sulkeissa oleva luku osoittaa linkitettyjen verkkopankkien määrän.  
7. Valitse **OK**-painike.

    Jos linkität vain yhden verkkopankkitilin **Pankkitilin kortti** -ikkuna avautuu ja verkkopankkitilin nimi näkyy, Nyt pankkitilin linkitystehtävä on valmis. Jäljellä on enää pankkitilin määrittäminen. Lisätietoja on kohdassa [Toimintaohje: Pankkitilien määrittäminen](bank-how-setup-bank-accounts.md).

    Jos linkität useita verkkopankkitilejä, **Pankkitilin linkitys** -ikkuna avautuu. Tässä ikkunassa on luettelo verkkopankkitileistä, joita ei ole vielä linkitetty [!INCLUDE[d365fin](includes/d365fin_md.md)]in pankkitileihin. Noudata tällaisessa tapauksessa seuraavaa vaihetta.  
8. Valitse **Pankkitilin linkitys** -ikkunassa verkkopankkitilin rivi ja valitse sitten **Linkitä uuteen pankkitiliin** -toiminto.  

    Näyttöön avautuu uuden pankkitilin **Pankkitilin kortti** -ikkuna ja verkkopankkitilin nimi näkyy.

    Jos [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on jo pankkitili, johon haluat linkittää lisäverkkopankkitilin, noudata seuraavia ohjeita.  
9. Valitse **Pankkitilin linkitys** -ikkunassa verkkopankkitilin rivi ja valitse sitten **Linkitä olemassa olevaan pankkitiliin** -toiminto.
10. Valitse **Pankkitililuettelo**-ikkunassa pankkitili, johon linkitys tehdään, ja valitse sitten **OK**-painike.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Pankkitilin linkittäminen verkkopankkitiliin
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Valitse sen pankkitilin rivi, jota ei ole linkitetty verkkopankkitiliin, ja valitse sitten **Linkitä verkkopankkitiliin** -toiminto. Näyttöön avautuu **Verkkopankkitilin linkitys** -ikkuna, joka sisältää **Linkitä tili** -ruudussa annetun pankin nimen.
3. Valitse pankin nimi. **Kirjaudu sisään** -ruutu avautuu.
4. Syötä käyttäjätunnus ja salasana, jota käytät kirjautuessasi verkkopankkiin, ja valitse sitten **Seuraava**-painike.  

    Pankkisyötepalvelu valmistelee [!INCLUDE[d365fin](includes/d365fin_md.md)]in pankkitilin ja liittyvän verkkopankkitilin linkityksen.  

    Kun prosessi on valmis, pankin nimi näkyy **Linkitetty**-välilehden **Omat tilit**-ruudussa. Jos pankissa on useita pankkitilejä, vain vaiheessa 2 valittu pankkitili linkitetään.  
5. Valitse **OK**-painike.

**Pankkitililuettelo**-ikkunan **Linkitetty**-valintaruutu valitaan.

## <a name="to-unlink-a-bank-account"></a>Pankkitilin linkityksen poistaminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Pankkitilit** ja valitse sitten liittyvä linkki.  
2. Valitse sen linkitetyn pankkitilin rivi, jonka linkityksen liittyvään verkkopankkitiliin haluat poistaa. Valitse sitten **Poista verkkopankkitilin linkitys** -toiminto.

**Huomautus:** Jos valitset vahvistusvalintaikkunassa **Kyllä**, verkkopankkitilin linkki poistetaan ja kirjautumistiedot poistetaan. Voit linkittää pankkitilin uudelleen verkkopankkitiliin kirjautumalla pankkiin sisään uudelleen. Lisätietoja on “Pankkitilin linkittäminen verkkopankkitiliin“ -osassa.

## <a name="to-update-bank-account-linking"></a>Pankkitilin linkityksen päivittäminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Valitse asianmukainen pankkitili ja valitse sitten **Päivitä pankkitilien linkitys** -toiminto.

Jos **Pankkitililuettelo**-ikkunan linkitetyissä pankkitileissä esiintyy ongelmia, näyttöön avautuu **Pankkitilin linkitys** -ikkuna, jossa kerrotaan pankkitili, jota ongelmat koskevat. Ongelmien ratkaiseminen tapahtuu parhaiten poistamalla verkkopankkitilin linkitys ja luomalla linkitys uudelleen. Lisätietoja on “Pankkitilin linkittäminen verkkopankkitiliin“ -osassa.

## <a name="to-enable-automatic-import-of-bank-statements"></a>Pankin tiliotteiden automaattisen tuonnin ottaminen käyttöön
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Valitse linkitetyn pankkitilin rivi ja valitse sitten **Pankin tiliotteen automaattisen tuonnin asetukset** -toiminto.
3. Määritä **Pankin tiliotteen automaattisen tuonnin asetukset** -ikkunan **Sisällytettyjen päivien lukumäärä** -kentässä, miltä kaukaiselta ajalta uudet pankkitapahtumat haetaan.

    **Huomautus**: Suosittelemme arvoksi 7 päivää tai enemmän.  
4. Valitse **Käytössä**-valintaruutu.  

**Maksujen täsmäytyskirjauskansio** -ikkuna näyttää nyt tunneittain kaikki uudet verkkopankissa tehdyt maksut.

**Huomautus:** Niiden maksujen tapahtumia, jotka on jo kohdistettu ja/tai täsmäytetty **Maksujen täsmäytyskirjauskansio** -ikkunassa, ei tuoda.

## <a name="see-also"></a>Katso myös
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Pankkitilien hallinta](bank-manage-bank-accounts.md)  
[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennuksilla ](ui-extensions.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

