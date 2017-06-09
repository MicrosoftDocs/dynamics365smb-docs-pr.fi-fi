---
title: "Yleisten päiväkirjojen käyttäminen | Microsoft Docs"
description: "Lisätietoja yleisten päiväkirjojen käyttämisestä."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/03/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 13257a5d82d742d92fb22da9da7ff7f773d7d2f8
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="working-with-general-journals"></a>Yleisten päiväkirjojen käyttäminen
Yleisiä päiväkirjoja käytetään rahoitustapahtumien kirjaamisessa kirjanpitotileille sekä muille tileille, kuten pankki-, asiakas- ja toimittajatileille. Yleisen päiväkirjan avulla kirjaaminen luo aina tapahtumia kirjanpitotileille. Näin tapahtuu silloinkin, kun kirjataan esimerkiksi päiväkirjan rivi asiakkaan tilille, koska tapahtuma kirjataan pääkirjanpidon myyntisaamisten tilille kirjausryhmän kautta.

[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää myös muita kuin rahoituspäiväkirjoja, kuten nimikepäiväkirjan ja varastopäiväkirjan. Nämä päiväkirjat eivät kuitenkaan näy käyttöliittymässä.

Päiväkirjaan lisäämäsi tiedot ovat väliaikaisia, ja niitä voi muuttaa niiden ollessa päiväkirjassa. Kun kirjaat päiväkirjan, tiedot siirretään yksittäisten tilien tapahtumiin, missä niitä ei voi muuttaa. Voit kuitenkin peruuttaa kirjattujen tapahtumien kohdistuksen tai kirjata peruuttavia tai korjaavia tapahtumia.

## <a name="journal-templates-and-batches"></a>Päiväkirjan mallit ja erät
Yleisen päiväkirjan malleja on useita. Kullakin päiväkirjan mallilla on määritetty ikkuna, jossa on erityistoimintoja sekä näitä toimintoja varten tarvittavat kentät. Ikkunoita ovat esimerkiksi **Maksujen täsmäytyskirjauskansio**, jossa käsitellään pankkimaksuja, ja **Maksupäiväkirja**, jossa maksetaan toimittajille.

**Huomautus**: Jos viet maksutiedostoja pankista maksupäiväkirjaan, sinun on valittava kyseisen päiväkirjaerän **Salli maksun vienti** -valintaruutu **Yleisen päiväkirjan erät** -ikkunassa. Lisätietoja on kohdassa [Toimintaohje: Maksujen vieminen pankkitiedostoon](payables-how-export-payments-bank-file.md).

Voit määrittää kullekin päiväkirjan mallille oman henkilökohtaisen päiväkirjan päiväkirjan eränä. Voit esimerkiksi määrittää maksupäiväkirjalle oman päiväkirjan erän, jolle on määritetty henkilökohtainen asettelu ja asetukset.

Yleisen päiväkirjan erälle määritetty henkilökohtainen asetus on esimerkiksi se, että järjestelmä auttaa summakenttien täyttämisessä. Jos valitset **Yleisen päiväkirjan erät** -ikkunan erän rivillä olevan **Ehdota vastasummaa** -valintaruudun, esimerkiksi saman asiakirjanumeron yleisen päiväkirjan rivien **Summa**-kenttään esitäytetään automaattisesti arvo, joka vaaditaan asiakirjan täsmäyttämiseksi. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] voi ehdottaa arvoja](ui-let-system-suggest-values.md).

## <a name="main-accounts-and-balancing-accounts"></a>Päätilit ja vastatilit
Jos olet määrittänyt päiväkirjan erille oletusvastatilit, vastatili täytetään automaattisesti, kun täyttö tehdään **Tilinro**. -kentässä. Muussa tapauksessa myös **Tilinro**- ja **Vastatilin nro** -kenttä on täytettävä manuaalisesti. Positiivinen summa **Summa**-kentässä veloitetaan päätililtä ja hyvitetään vastatilille. Negatiivinen summa hyvitetään päätilille ja veloitetaan vastatililtä.

**Huomautus**: ALV lasketaan erikseen päätiliä varten ja vastatiliä varten, joten niillä voi olla eri ALV-prosentit.

## <a name="recurring-journals"></a>Toistuvat päiväkirjat
Toistuva päiväkirja on yleinen päiväkirja, jossa on erityiskenttiä sellaisten tapahtumien hallintaa varten, jotka kirjataan usein vähäisin muutoksin tai ilman muutoksia. Käyttämällä näitä kenttiä toistuviin tapahtumiin, voit kirjata sekä vakiosummia että muuttuvia summia. Voit myös määrittää automaattisen peruutuksen tapahtumat kirjauspäivämäärän jälkeisenä päivänä sekä käyttää kohdistusavaimia toistuvien tapahtumien kanssa.

## <a name="see-also"></a>Katso myös
[Toimintaohje: Kohdistustunnusten käyttäminen yleisissä päiväkirjoissa](ui-how-use-allocation-keys-general-journals.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

