---
title: Useiden asiakirjojen kirjaaminen samanaikaisesti | Microsoft Docs
description: Sen sijaan että yksittäisiä asiakirjoja yksi kerrallaan, voit valita luettelosta useita kirjaamattomia asiakirjoja eräkirjausta varten. Tämä kirjaus voidaan tehdä heti tai se voidaan aikatauluttaa tapahtumaan esimerkiksi päivän päätteeksi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 32998248de254facdb225d60a0c8b55066b2707c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192097"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Useiden asiakirjojen kirjaaminen samanaikaisesti
Sen sijaan että yksittäisiä asiakirjoja yksi kerrallaan, voit valita luettelosta useita kirjaamattomia asiakirjoja eräkirjausta varten. Tämä kirjaus voidaan tehdä heti tai se voidaan aikatauluttaa tapahtumaan vaikkapa päivän päätteeksi. Tämä voi olla kätevää, jos vain esimies voi kirjata muiden käyttäjien tekemiä asiakirjoja tai jos halutaan estää järjestelmän suorituskyvyn heikentyminen työaikana tehtävien kirjausten vuoksi.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Useiden ostotilausten kirjaaminen heti
Useita ostotilauksia voi kirjata heti toimimalla seuraavasti. Vaiheet ovat samanlaiset kaikissa osto- ja myyntiasiakirjoissa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Ostotilaukset** ja valitse sitten liittyvä linkki.
2. Siirry valitsemaan kaikki kirjattavat tilaukset **Ostotilaukset**-sivulla:
3. Valitse **Nro**-kenttään kolme allekkain olevaa pistettä. Pikavalikko avautuu, ja voit valita **Valitse lisää** -toiminnon.
4. Valitse kaikkien samaan aikaan kirjattavien tilausrivien valintaruudut.
5. Valitse ensin **Kirjaus**-toiminto ja sitten **Kirjaa**-toiminto.
6. Valitse vahvistusviestissä **Kyllä**.

## <a name="to-batch-post-multiple-purchase-orders"></a>Useiden ostotilausten eräkirjaaminen
Ostotilauksia voi eräkirjata toimimalla seuraavasti. Vaiheet ovat samat kaikissa osto- ja myyntiasiakirjoissa, joissa **Eräkirjaus**-toiminto on käytettävissä.

> [!NOTE]
> Asiakirjojen eräkirjaus tapahtuu taustalla työjonotapahtuman määrittämällä tavalla. Tämä työjonotapahtuma on määritettävä ensin. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten liittyvä linkki.  
2. Siirry valitsemaan kaikki kirjattavat tilaukset **Ostotilaukset**-sivulla:
3. Valitse **Nro**-kenttään kolme allekkain olevaa pistettä. Pikavalikko avautuu, ja voit valita **Valitse lisää** -toiminnon.
4. Valitse kaikkien samaan aikaan kirjattavien tilausrivien valintaruudut.
5. Valitse ensin **Kirjaus**-toiminto ja sitten **Eräkirjaus**-toiminto.
6. Täytä tarvittavat kentät **Eräkirjaa ostotilaukset** -sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Jos haluat tulostaa liittyviä raportteja, kuten myyntitilauksen **Tilausvahvistus**-raportin, kirjauksen aikana, valitse **Tulosta**-valintaruutu.<br /><br /> Määritä **Myyntien ja saamisten asetukset**- tai **Ostojen ja ostovelkojen asetukset** -sivun **Raportin tuotostyyppi** -kentässä, tulostetaanko raportti vai onko tuotoksena PDF.<br /><br /> Huomaa myös, että suoratulostus valittuun tulostimeen on mahdollista vain paikallisissa asennuksissa.

7. Valitse **OK**-painike.
8. Voit tarkastella asiakirjojen eräkirjauksen aikana mahdollisesti esiintyneitä ongelmia avaamalla **Virhesanomarekisteri**-sivun.

Ostotilaukset lisätään nyt määritettyyn työjonotapahtumaan, joka määrittää, milloin asiakirjat kirjataan. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).

Jos valitset **Raportin tuotostyyppi** -kentässä **PDF**, ostotilaukset, joiden kirjaus onnistui, ovat käytettävissä roolikeskuksen **Saapuneet raportit** -osassa.

## <a name="see-also"></a>Katso myös
[Asiakirjojen ja päiväkirjojen kirjaaminen](ui-post-documents-journals.md)  
[Työjonojen käyttäminen ajoitustehtäviin](admin-job-queues-schedule-tasks.md)  
[Kirjattujen asiakirjojen muokkaaminen](across-edit-posted-document.md)  
[Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
