---
title: Raporttiasettelun määrittäminen
description: Tietoja siitä, miten voit määrittää raportissa käytettävän asettelun esikatselua ja tulostamista varten.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9652, 9650
ms.date: 03/07/2022
ms.author: jswymer
ms.openlocfilehash: e59a57e6cac21f4909088defc42da795e5550562
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9535851"
---
# <a name="setting-the-layout-used-by-a-report"></a>Raportin käyttämän asettelun määrittäminen

> **KOSKEE:** Business Central online, Business Central on-premises 2022 julkaisuaalto 1 ja uudemmat. Aiemmissa versioissa mene [tänne](ui-how-change-layout-currently-used-report.md).

Raportin asettelu määrittää raportin ulkoasun. Se määrittää, mitkä raporttijoukon tietokentät ovat näkyvissä, miten ne on järjestetty ja muotoiltu, jne. Raportti voidaan määrittää useille asetteluille, joita voidaan vaihtaa tarpeen mukaan.

Kun sovelluksessa on useita yrityksiä, asettelujen asetukset määritetään yrityskohtaisesti. Saman yrityksen raportissa voi siis olla eri asettelu kuin toisessa yrityksessä.

## <a name="get-started"></a>Aloitus

Voit määrittää raportin käyttämän asettelun kahdella tavalla. Yksi tapa on **Raporttiasetteluvalinta**-sivulta. Toinen tapa on **Raporttiasettelut**-sivulta. Jokaisella sivulla on etunsa, esimerkiksi: 

- **Raporttiasetteluvalinta**-sivulla näkyy luettelo kaikista raporteista.

  Tämä sivu ilmaisee raportin tämänhetkisen asettelun. Lisäksi voit määrittää asettelut eri yrityksissä ilman, että sinun tarvitsee vaihtaa yritystä, jota käsittelet.

- **Raporttiasettelut**-sivulla näkyvät kaikki valitun yrityksen kunkin raportin käytettävissä olevat asettelut.

  Tietyn asettelun etsiminen on helppoa lajittelemalla tai suodattamalla luettelo. Kun löydät asettelun, voit määrittää sen raportille yksittäisellä valinnalla.

  > [!NOTE]
  > Et voi käyttää **Raporttiasettelut**-sivua Wordin ja RDLC:n asetteluille, jotka luotiin käyttämällä vanhaa **Mukautetut asettelut** -ominaisuutta. Itse asiassa et edes näe näitä mukautettuja asetteluita luettelossa **Raporttiasettelut**-sivulla. Voit määrittää nämä asettelut vain käyttämällä **Raporttiasetteluvalinta**-sivua.

## <a name="set-the-layout-from-the-report-layouts-page"></a>Asettelun määrittäminen Raporttiasettelut-sivulta

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Etsi asettelu luettelosta, valitse se ja valitse sitten **Määritä oletus** -toiminto sivun yläosasta.

## <a name="set-the-layout-from-report-layout-selection-page"></a>Asettelun määrittäminen Raporttiasetteluvalinta-sivulta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttiasetteluvalinta** ja valitse sitten vastaava linkki.
  
   Sivulla on luettelo kaikista raporteista, joita voi käyttää sivun yläosan **Yritys**-kentässä määritetyssä yrityksessä. **Asettelun kuvaus** -kenttä määrittää tällä hetkellä raportissa käytetyn asettelun.
2. Määritä **Yritys**-kenttä yläosassa yritykseksi, joka sisältää raportin.
3. Etsi ja valitse raportti luettelosta ja tee sitten jompikumpi seuraavista toimista:

   - Jos haluat vaihtaa asettelua, jonka tyyppi on jokin muu kuin valittu asettelu, valitse **Asettelun tyyppi** -kenttä ja valitse sitten raporttiin määritettävän asettelun tyyppi. 
   - Jos haluat vaihtaa samantyyppiseen kuin valittu asettelu, valitse yläreunan **Valitse asettelu** -toiminto.

4. Valitse **Raporttiasettelut**-sivulla asettelu ja valitse sitten **OK**.

## <a name="revert-to-the-original-default-layout"></a>Palauta alkuperäinen oletusasettelu

Raportit on suunniteltu käyttämään asettelua oletusarvoisesti. Voit siirtyä takaisin alkuperäiseen oletusasetteluun **Raporttiasetteluvalinta**-sivulta. Valitse vain raportti ja valitse sitten sivun yläosasta **Palauta oletusvalinta** -toiminto.

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
