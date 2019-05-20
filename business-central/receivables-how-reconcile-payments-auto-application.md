---
title: Maksujen täsmäyttäminen automaattisen kohdistuksen avulla | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten maksut tai kassaanmaksut voidaan kohdistaa automaattisella kohdistustoiminnolla liittyviin avoimiin tapahtumiin ja maksut täsmäyttää.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 16241459bd080b7f1982a42110a834433d9427ea
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252088"
---
# <a name="reconcile-payments-using-automatic-application"></a>Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta
**Maksujen täsmäytyskirjauskansio** -sivu määrittää tulevat tai lähtevät maksut, jotka on tallennettu tapahtumina verkkopankkitilille ja jotka voit kohdistaa niihin liittyviin avoimiin asiakas-, toimittaja- ja pankkitilitapahtumiin. Päiväkirjan rivit täytetään tuomalla pankin tiliote syötteenä tai tiedostona.

> [!NOTE]
> Sivu tarjoaa automaattisen vastaavuustoiminnon, joka kohdistaa maksut niihin liittyviin avoimiin tapahtumiin pankin tiliotteen rivillä (päiväkirjan rivi) olevan tekstin vastaavuuden perusteella verrattuna yhden tai useamman avoimen tapahtuman tekstiin. Huomaa, että ehdotetut automaattiset kohdistukset voidaan korvata toisilla. Voit myös olla käyttämättä automaattista kohdistusta. Lisätietoja on vaiheessa 7.

Täsmäytyksen maksukirjauskansioon liittyy [!INCLUDE[d365fin](includes/d365fin_md.md)]issa yksi pankkitili, joka vastaa verkkopankkitiliä, jolle maksutapahtumat kirjataan. Kaikki kohdistettuun asiakas- tai toimittajatapahtumaan liittyvät avoimet pankkitilitapahtumat suljetaan, kun valitset **Kirjaa maksut ja täsmäytä pankkitili** -toiminnon. Tämä tarkoittaa sitä, että pankkitili täsmäytetään automaattisesti päiväkirjaan kirjattaville maksuille.

Jos haluat ottaa pankin tiliotteet käyttöön pankkisyötteinä, määritä ensin Envestnet Yodlee Bank Feeds -palvelu ja linkitä sitten pankkitili siihen liittyvään verkkopankkitiliin. Maksujen täsmäytyskirjauskansio havaitsee automaattisesti pankkisyötteet, kun valitset **Tuo pankkitapahtumat** -toiminnon. Lisäksi voit määrittää pankkitilin niin, että se tuo uudet tiliotesyötteet tunnin välein automaattisesti. Niiden maksujen tapahtumia, jotka on jo kohdistettu ja/tai täsmäytetty, ei tuoda. Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).

**Linkitä teksti tiliin** -ikkunassa voit määrittää maksujen tekstin kohdistukset ja tietyt debet-, kredit- ja kirjanpidon vastatilit siten, että nämä maksut kirjataan tietyille tileille, jotta nämä maksut kirjataan tietyille tileille, kun kirjaat maksun täsmäytyksen päiväkirjan. Katso vaihe 8. Lisätietoja on kohdassa [Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Vastaava toiminto on käytettävissä, kun maksujen täsmäytyskirjauskansion rivien ylimääräisiä summia täsmäytetään tapauskohtaisesti. Lisätietoja on kohdassa [Niiden maksujen täsmäyttäminen, joita ei voi kohdistaa.](receivables-how-reconcile-payments-cannot-apply-auto.md)

Voit käyttää **Kohdista automaattisesti** -toimintoa joko automaattisesti, kun tuot pankkitiedoston tai -syötteen ja maksutapahtumat, tai kun aktivoit sen maksujen kohdistamiseksi niiden vastaaviin avoimiin tapahtumiin, jotka perustuvat vastaavaan tekstiin pankin tiliotteen rivillä (päiväkirjarivillä), jossa on tekstiä avoimista tapahtumista.

Kirjauskansion riveillä, joilla maksu on kohdistettu automaattisesti yhteen tai useaan avoimeen tapahtumaan, **Vastaavuuden luotettavuus** -kentässä on arvo väliltä Alhainen ja Suuri. Se osoittaa niiden kohdistettujen tietojen laadun, joihin ehdotettu maksusovellus perustuu. Lisäksi **Tilityyppi**- ja **Tilinumero**-kentät täytetään sen asiakkaan tai toimittajan tiedoilla, johon maksu kohdistetaan. Jos olet asettanut tekstistä tiliin yhdistämisen, automaattisen kohdistuksen tuloksena saattaa olla vastaavuusarvo **Suuri - tekstin ja tilin välinen yhdistäminen**.

Voit avata kullekin maksua esittävälle **Maksujen täsmäytyskirjauskansio** -sivun päiväkirjan riville **Maksun kohdistus** -sivun ja tarkastella kaikkia mahdollisia avoimia maksuja ja yksityiskohtaisia tietoja merkintöjen täsmäytyksestä, joihin maksujen kohdistus perustuu. Tässä voit kohdistaa maksuja manuaalisesti tai kohdistaa uudelleen maksuja, joka kohdistettiin automaattisesti väärään merkintään. Lisätietoja on kohdassa [Maksujen tarkasteleminen tai kohdistaminen automaattisen kohdistuksen jälkeen](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Voit aloittaa pankkitapahtumien tuonnin samaan aikaan, kun avaat **Maksujen täsmäytyskirjauskansio** -sivun olemassa olevalle maksun täsmäytyksen kirjauskansiolle **Maksun täsmäytyksen päiväkirjat** -sivulla. Seuraava toimenpide kuvaa kuinka pankkitapahtumat tuodaan **Maksujen täsmäytyskirjauskansio** -sivulle, kun olet luonut uuden päiväkirjan.

## <a name="to-reconcile-payments-using-automatic-application"></a>Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksujen täsmäytyskirjauskansiot** ja valitse sitten liittyvä linkki.
2. Voit käsitellä uuden maksun täsmäytyksen päiväkirjaa valitsemalla **Uusi päiväkirja** -toiminnon.
3. Valitse **Maksun pankkitililuettelo** -sivulla pankkitili, johon maksut täsmäytetään, ja valitse sitten **OK**-painike.
   **Maksujen täsmäytyskirjauskansio** -sivu avautuu valmisteltuna valitulle pankkitilille.
4. Valitse **Tuo pankkitapahtumat** -toiminto.
   Jos pankkitapahtumien tuontia varten ei ole määritetty valitun kirjauskansion pankkitiliä, valintaikkuna avautuu auttaen sinua täyttämään asianmukaiset kentät.
5. Valitse **Valitse tuotava tiedosto** -sivulla tiedosto, joka sisältää täsmäytettävät pankkitapahtumat täsmäytettäville maksuille, ja valitse sitten **Avaa**-painike.  
6. Jos pankin tiliotepalvelu on otettu käyttöön, määritä automaattisesti avautuvalla **Pankin tiliotteen suodatus** -sivulla pankin tiliotteiden tuonnille päivämääräväli.

    **Maksujen täsmäytyskirjauskansio** -sivu sisältää maksurivit, jotka kuvaavat tuodun pankin tiliotteen pankkitapahtumia.

    Maksujen riveillä, jotka on automaattisesti kohdistettu niiden vastaaviin avoimiin tapahtumiin, **Vastaavuuden luotettavuus** -kentässä on arvo väliltä **Alhainen** ja **Suuri**. Tämä osoittaa niiden kohdistettujen tietojen laadun, joihin ehdotettu maksusovellus perustuu. Lisäksi **Tilityyppi**- ja **Tilinumero**-kentät täytetään sen asiakkaan tai toimittajan tiedoilla, johon maksu kohdistetaan.
7. Valitse päiväkirjarivi ja valitse sitten **Kohdista manuaalisesti** -toiminto, kun haluat tarkastaa, kohdistaa uudelleen tai kohdistaa maksun manuaalisesti **Maksun kohdistus** -sivulla. Lisätietoja on kohdassa [Maksujen tarkasteleminen tai kohdistaminen automaattisen kohdistuksen jälkeen](receivables-how-review-apply-payments-auto-application.md).

    Kun olet suorittanut manuaalisen kohdistuksen, manuaalisesti käsittelemäsi päiväkirjarivin **Vastaavuuden luotettavuus** -kentän arvo on **Hyväksytty**.
8. Valitse kohdistamaton päiväkirjarivi toistuvalle kassasuoritukselle tai kululle, kuten auton polttoaineen hankinta ja valitse sitten **Linkitä teksti tiliin** -toiminto. Lisätietoja on kohdassa [Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).
9. Kun olet lopettanut maksutekstin yhdistämisen tileihin, valitse **Kohdista manuaalisesti** -toiminto.
10. Kun olet varma, että kaikki päiväkirjarivien maksut on kohdistettu oikein tai asetettu suorakirjaukselle, valitse **Kirjaa**-toiminto ja sitten jokin seuraavista vaihtoehdoista:

    - **Kirjaa maksut ja täsmäytä pankkitilit** – kirjataksesi maksut kohdistuksen mukaan ja myös sulkeaksesi liittyvät pankkitilitapahtumat täsmäytyksen mukaan.
    - **Kirjaa vain maksut** – kirjataksesi vain maksut kohdistuksen mukaan, mutta jättääksesi liittyvät pankkitilitapahtumat avoimiksi. Edellyttää, että täsmäytät pankkitilin erikseen, esimerkiksi: Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen erikseen ](bank-how-reconcile-bank-accounts-separately.md).
    - **Testiraportti** – Tarkastele kirjaamisen tulosta ennen kirjaamista valitsemalla. **Pankin tiliote** -raportti avautuu ja näyttää samat kentät kuin **Maksujen täsmäytyskirjauskansio** -sivun alaosassa.

Kun kirjaat maksun täsmäytyksen päiväkirjan, kohdistetut avoimet tapahtumat suljetaan ja liittyvät asiakas- tai toimittaja- tai kirjanpitotilit päivitetään. Määritetyt kirjanpitotilit päivitetään tekstin tiliin yhdistämiseen perustuville asiakas-, toimittaja ja kirjanpitotileille. Kaikille pankkitilitapahtumille luodaan kirjauskansiorivit. Jos valitset **Kirjaa maksut ja täsmäytä pankkitili** -toiminnon, kaikki kohdistettuun asiakas- tai toimittajatapahtumaan liittyvät avoimet pankkitilitapahtumat suljetaan. Tämä tarkoittaa sitä, että pankkitili täsmäytetään automaattisesti päiväkirjaan kirjattaville maksuille.

Voit verrata **Pankkitilin saldo kirjauksen jälkeen** -kentän ja **Tiliotteen loppusaldo** -kentän arvoa seurataksesi, milloin pankkitili täsmäytetään kirjaamiesi maksujen perusteella.

> [!NOTE]  
>   Jos et halua täsmäyttää pankkitiliä **Maksujen täsmäytyskirjauskansio** -sivulla, sinun on käytettävä **Pankkitilin täsmäytys** -sivua. Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen erikseen](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
