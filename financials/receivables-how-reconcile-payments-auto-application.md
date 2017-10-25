---
title: "Maksujen täsmäyttäminen automaattisen kohdistuksen avulla | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten maksut tai kassaanmaksut voidaan kohdistaa automaattisella kohdistustoiminnolla liittyviin avoimiin tapahtumiin ja maksut täsmäyttää."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: b4ff3d64f23a5dfb9800abeedb7374764b060f4d
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reconcile-payments-using-automatic-application"></a>Ohjeet: Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta
**Maksujen täsmäytyskirjauskansio** -ikkuna määrittää tulevat tai lähtevät maksut, jotka on tallennettu tapahtumina verkkopankkitilille ja jotka voit kohdistaa niihin liittyviin avoimiin asiakas-, toimittaja- ja pankkitilitapahtumiin. Päiväkirjan rivit täytetään tuomalla pankin tiliote syötteenä tai tiedostona.

Täsmäytyksen maksukirjauskansioon liittyy [!INCLUDE[d365fin](includes/d365fin_md.md)]issa yksi pankkitili, joka vastaa verkkopankkitiliä, jolle maksutapahtumat kirjataan. Kaikki kohdistettuun asiakas- tai toimittajatapahtumaan liittyvät avoimet pankkitilitapahtumat suljetaan, kun valitset **Kirjaa maksut ja täsmäytä pankkitili** -toiminnon. Tämä tarkoittaa sitä, että pankkitili täsmäytetään automaattisesti päiväkirjaan kirjattaville maksuille.

Jos haluat ottaa pankin tiliotteet käyttöön pankkisyötteinä, määritä ensin Envestnet Yodlee -pankkisyötepalvelu ja linkitä sitten pankkitili siihen liittyvään verkkopankkitiliin. Maksujen täsmäytyskirjauskansio havaitsee automaattisesti pankkisyötteet, kun valitset **Tuo pankkitapahtumat** -toiminnon. Lisäksi voit määrittää pankkitilin niin, että se tuo uudet tiliotesyötteet tunnin välein automaattisesti. Niiden maksujen tapahtumia, jotka on jo kohdistettu ja/tai täsmäytetty, ei tuoda. Lisätietoja on kohdassa [Toimintaohje: Envestnet Yodlee -pankkisyötepalvelun määrittäminen](bank-how-setup-bank-statement-service.md).

**Linkitä teksti tiliin** -ikkunassa voit määrittää maksujen tekstin kohdistukset ja tietyt debet-, kredit- ja kirjanpidon vastatilit siten, että nämä maksut kirjataan tietyille tileille, jotta nämä maksut kirjataan tietyille tileille, kun kirjaat maksun täsmäytyksen päiväkirjan. Katso vaihe 8. Lisätietoja on kohdassa [Toimintaohje: Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Vastaava toiminto on käytettävissä, kun maksujen täsmäytyskirjauskansion rivien ylimääräisiä summia täsmäytetään ad hoc. Lisätietoja on kohdassa [Toimintaohje: Niiden maksujen täsmäyttäminen, joita ei voi kohdistaa.](receivables-how-reconcile-payments-cannot-apply-auto.md)

Voit käyttää **Kohdista automaattisesti** -toimintoa, joko automaattisesti, kun tuot pankkitiedoston tai -syötteen ja maksutapahtumat tai kun aktivoit sen maksujen kohdistamiseksi niiden vastaaviin avoimiin tapahtumiin, jotka perustuvat vastaaviin tietoihin päiväkirjarivillä, jossa on tietoja avoimista tapahtumista.

Kirjauskansion riveillä, joilla maksu on kohdistettu automaattisesti yhteen tai useaan avoimeen tapahtumaan, **Vastaavuuden luotettavuus** -kentässä on arvo väliltä Alhainen ja Suuri. Se osoittaa niiden kohdistettujen tietojen laadun, joihin ehdotettu maksusovellus perustuu. Lisäksi **Tilityyppi**- ja **Tilinumero**-kentät täytetään sen asiakkaan tai toimittajan tiedoilla, johon maksu kohdistetaan. Jos olet asettanut tekstistä tiliin yhdistämisen, automaattisen kohdistuksen tuloksena saattaa olla vastaavuusarvo **Suuri - tekstin ja tilin välinen yhdistäminen**.

Voit avata kullekin maksua esittävälle päiväkirjan riville **Maksujen täsmäytyskirjauskansio** -ikkunassa **Maksun kohdistus** -ikkunan ja tarkastella kaikkia mahdollisia avoimia maksuja ja yksityiskohtaisia tietoja merkintöjen täsmäytyksestä, joihin maksujen kohdistus perustuu. Tässä voit kohdistaa maksuja manuaalisesti tai kohdistaa uudelleen maksuja, joka kohdistettiin automaattisesti väärään merkintään. Lisätietoja on kohdassa [Toimintaohje: Maksujen tarkasteleminen tai kohdistaminen automaattisen kohdistuksen jälkeen](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
>   Voit aloittaa pankkitapahtumien tuonnin samaan aikaan, kun avaat **Maksujen täsmäytyskirjauskansio** -ikkunan olemassa olevalle maksun täsmäytyksen kirjauskansiolle **Maksun täsmäytyksen päiväkirjat** -ikkunassa. Seuraava toimenpide kuvaa kuinka pankkitapahtumat tuodaan **Maksujen täsmäytyskirjauskansio** -ikkunaan, kun olet luonut uuden päiväkirjan.

## <a name="to-reconcile-payments-using-automatic-application"></a>Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksujen täsmäytyskirjauskansio** ja valitse sitten aiheeseen liittyvä linkki.
2. Voit käsitellä uuden maksun täsmäytyksen päiväkirjaa valitsemalla **Uusi päiväkirja** -toiminnon.
3. Valitse **Maksun pankkitililuettelo** -ikkunassa pankkitili, johon maksut täsmäytetään, ja valitse sitten **OK**-painike.
   **Maksujen täsmäytyskirjauskansio** -ikkuna avautuu valmisteltuna valitulle pankkitilille.
4. Valitse **Tuo pankkitapahtumat** -toiminto.
   Jos pankkitapahtumien tuontia varten ei ole määritetty valitun kirjauskansion pankkitiliä, valintaikkuna avautuu auttaen sinua täyttämään asianmukaiset kentät.
5. Valitse **Valitse tuotava tiedosto** -ikkunassa tiedosto, joka sisältää täsmäytettävät pankkitapahtumat täsmäytettäville maksuille, ja valitse sitten **Avaa**-painike.  
6. Jos pankin tiliotepalvelu on otettu käyttöön, määritä automaattisesti avautuvassa **Pankin tiliotteen suodatus** -ikkunassa pankin tiliotteiden tuonnille päivämääräväli.

    **Maksujen täsmäytyskirjauskansio** -ikkuna sisältää maksurivit, jotka kuvaavat tuodun pankin tiliotteen pankkitapahtumia.

    Maksujen riveillä, jotka on automaattisesti kohdistettu niiden vastaaviin avoimiin tapahtumiin, **Vastaavuuden luotettavuus** -kentässä on arvo väliltä **Alhainen** ja **Suuri**. Tämä osoittaa niiden kohdistettujen tietojen laadun, joihin ehdotettu maksusovellus perustuu. Lisäksi **Tilityyppi**- ja **Tilinumero**-kentät täytetään sen asiakkaan tai toimittajan tiedoilla, johon maksu kohdistetaan.
7. Valitse päiväkirjarivi ja valitse sitten **Kohdista manuaalisesti** -toiminto, kun haluat tarkastaa, kohdistaa uudelleen tai kohdistaa maksun manuaalisesti **Maksun kohdistus** -ikkunassa. Lisätietoja on kohdassa [Toimintaohje: Maksujen tarkasteleminen tai kohdistaminen automaattisen kohdistuksen jälkeen](receivables-how-review-apply-payments-auto-application.md).

    Kun olet suorittanut manuaalisen kohdistuksen, manuaalisesti käsittelemäsi päiväkirjarivin **Vastaavuuden luotettavuus** -kentän arvo on **Hyväksytty**.
8. Valitse kohdistamaton päiväkirjarivi toistuvalle kassasuoritukselle tai kululle, kuten auton polttoaineen hankinta ja valitse sitten **Linkitä teksti tiliin** -toiminto. Lisätietoja on kohdassa [Toimintaohje: Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
9. Kun olet lopettanut maksutekstin yhdistämisen tileihin, valitse **Kohdista manuaalisesti** -toiminto.
10. Kun olet varma, että kaikki päiväkirjarivien maksut on kohdistettu oikein tai asetettu suorakirjaukselle, valitse **Kirjaa**-toiminto.

Kun kirjaat maksun täsmäytyksen päiväkirjan, kohdistetut avoimet tapahtumat suljetaan ja liittyvät asiakas- tai toimittaja- tai kirjanpitotilit päivitetään. Määritetyt kirjanpitotilit päivitetään tekstin tiliin yhdistämiseen perustuville asiakas-, toimittaja ja kirjanpitotileille. Kaikille pankkitilitapahtumille luodaan kirjauskansiorivit. Jos valitset **Kirjaa maksut ja täsmäytä pankkitili** -toiminnon, kaikki kohdistettuun asiakas- tai toimittajatapahtumaan liittyvät avoimet pankkitilitapahtumat suljetaan. Tämä tarkoittaa sitä, että pankkitili täsmäytetään automaattisesti päiväkirjaan kirjattaville maksuille.

Voit verrata **Pankkitilin saldo kirjauksen jälkeen** -kentän ja **Tiliotteen loppusaldo** -kentän arvoa seurataksesi, milloin pankkitili täsmäytetään kirjaamiesi maksujen perusteella.

> [!NOTE]  
>   Jos et halua täsmäyttää pankkitiliä **Maksujen täsmäytyskirjauskansio** -ikkunassa, sinun on käytettävä **Pankkitilin täsmäytys** -ikkunaa. Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen erikseen](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

