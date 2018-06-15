---
title: "Sekkien myöntäminen, tulostaminen, peruuttaminen ja mitätöiminen| Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten sekit myönnetään maksupäiväkirjan avulla, tulostetaan ja mitätöidään tai miten sekkitapahtumia tarkastellaan Business Central -sovelluksessa."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 39b48fbd34b29db56b39712fbd2cbf5dc91fefc6
ms.contentlocale: fi-fi
ms.lasthandoff: 04/26/2018

---
# <a name="make-check-payments"></a>Sekkimaksujen suorittaminen
Voit myöntää sähköisiä ja manuaalisia sekkejä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Molemmissa menetelmissä sekit myönnetään toimittajille maksupäiväkirjaa käyttäen. Ohjelman avulla voit myös mitätöidä sekkejä ja tarkastella sekkitapahtumia.

Seuraavassa kuvataan, miten voit maksaa toimittajalle tietokonesekillä kohdistamalla maksun asianmukaiseen toimittajalaskuun, tulostamalla sekin ja kirjaamalla maksun maksetuksi. Näin saadaan positiivinen toimittajatapahtuma, joka kohdistetaan negatiiviseen pankkitilitapahtumaan sekä fyysinen sekki pankin käsittelyä varten.

Voit maksaa kahdella eri tyyppisellä sekillä. Molemmissa tyypeissä **Vastatilin tyyppi**- tai **Tilityyppi** -kentässä täytyy olla **Pankkitili**.

- **Tietokonesekki**: Valitse tämä vaihtoehto, jos haluat tulostaa sekin maksupäiväkirjan tällä rivillä olevalle summalle. Tulosta sekit, ennen kuin kirjaat päiväkirjan rivit. Voit valita vain **Tietokonesekki**, jos
- **Manuaalinen sekki**: Valitse tämä vaihtoehto, jos olet luonut sekin manuaalisesti ja haluat luoda vastaavan sekkitapahtuman tälle summalle. Tämän vaihtoehdon avulla et voi tulostaa sekkiä.

> [!NOTE]  
> Voit varmistaa lähettämällä toimittaja-, sekki- ja maksutiedot sisältävän tiedoston, että pankki vahvistaa vain tarkistetut sekit ja summat. Lisätietoja on kohdassa [Positive Pay -tiedostojen vieminen](finance-how-positive-pay.md).

Tulostin on määritettävä oikein sekkimuotoja varten. Myös käytettävä sekkien asettelu on määritettävä. Lisätietoja on kohdassa [Sekkien asetteluiden määrittäminen](finance-how-define-check-layouts.md)

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Maksaaksesi toimittajalaskun tietokonesekillä
Seuraavassa kuvataan, miten toimittajalle maksetaan sekillä. Vaiheet ovat samankaltaiset kuin hyvitettäessä asiakkaalle sekkimaksuna.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksupäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.
2. Täytä maksupäiväkirjan rivit. Lisätietoja on ohjeaiheessa [Maksujen ja hyvitysten kirjaaminen](payables-how-post-payments-refunds.md).
3. Valitse **Maksutavan koodi** -kentässä **Sekki**.
4. Valitse **Pankkimaksun tyyppi** -kentässä **Tietokonesekki**.
5. Valitse **Tulosta sekki** -toiminto.
6. Täytä **Sekki**-ikkunassa tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Valitse **Lähetä kohteeseen** -painike, sitten **PDF-tiedosto**-asetus ja valitse sitten **OK**-painike.

    Fyysiset sekit voidaan nyt viedä pankkiin käsittelyä varten. Jatka maksun kirjaamiseen kohdistuksen mukaan toimittajalle ja maksun suorittamiseksi järjestelmässä.
8. Valitse **Kirjaa**-toiminto.

Täysin kohdistetut toimittajatapahtumat ja pankkitilitapahtumat luodaan.

> [!NOTE]  
> Jos sekkejä täytyy tulostaa ja maksaa monessa valuutassa eri pankkitileiltä, sinun täytyy suorittaa **Tulosta sekki** -eräajo erikseen kullekin valuutalle ja määrittää sopivat pankkitilit.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Kirjaamattomien ja tulostettujen sekkien peruuttaminen
Voit peruuttaa kirjaamattomat sekit niiden tulostamisen jälkeen **Maksupäiväkirja**-ikkunan **Mitätöi sekki** -toiminnon avulla.

1. Valitse **Maksupäiväkirja**-ikkunassa **Mitätöi sekki** ja valitse peruutettavat sekit.

## <a name="to-void-checks"></a>Sekkien mitätöiminen
Kun sekkimaksu on kirjattu, voit peruuttaa (mitätöidä) sekit vain tuloksena syntyvistä pankkitapahtumista.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Pankkitilit** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse oikea pankkitili, valitse **Muokkaa**-toiminto ja valitse sitten **Sekkitapahtumat**-toiminto.
3. Valitse **Sekkitapahtumat**-ikkunassa **Mitätöi sekki** -toiminto.
4. Valitse **Mitätöi vain sekki** -valintaruutu.
5. Valitse **OK**-painike.

## <a name="to-view-a-summary-of-posted-checks"></a>Voit tarkastella kirjattujen sekkien yhteenvetoa
Jos haluat tarkistaa kirjatuttuja sekkejä, esimerkiksi yhdelle toimittajalle maksetut useat sekit, voit käyttää **Pankkitili – sekin tiedot** -raporttia.
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Pankkitili – sekin tiedot** ja valitse sitten aiheeseen liittyvä linkki.
2. Aseta haluamasi suodattimet ja valitse sitten **Esikatselu**-painike.

## <a name="see-also"></a>Katso myös
[Maksujen suorittaminen](payables-make-payments.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Positive Pay -tiedoston vienti](finance-how-positive-pay.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

