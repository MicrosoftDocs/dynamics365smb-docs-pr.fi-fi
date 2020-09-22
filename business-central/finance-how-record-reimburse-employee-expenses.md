---
title: Työntekijän liiketoimintaan liittyvien kulujen kirjaaminen ja hyvittäminen | Microsoft Docs
description: Hyvitä liiketoimintaan liittyväkulu kirjaamalla työntekijän kulut ensin yleisessä päiväkirjassa työntekijän tilille ja sitten maksu työntekijän tilille.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/23/2020
ms.author: edupont
ms.openlocfilehash: 1034765a452bf94ab243c301df58cb8a891f79f9
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783364"
---
# <a name="record-and-reimburse-employees-expenses"></a>Työntekijöiden kulujen kirjaaminen ja hyvittäminen

[!INCLUDE[d365fin](includes/d365fin_md.md)] tukee työntekijän tapahtumia samalla tavoin kuin toimittajien tapahtumia. Niinpä työntekijän kirjausryhmien avulla voidaan varmistaa, että työntekijätapahtumat kirjataan oikeille yleisen päiväkirjan tileille.

> [!NOTE]  
> Työntekijätapahtumat voidaan kirjata vain paikallisena valuuttana. Työntekijöille tehtävät hyvitysmaksut eivät tue alennuksia ja maksutoleransseja.

Jos työntekijät voivat käyttää omia varojaan liiketoiminnoissa, voit kirjata kulun työntekijän tilille. Työntekijälle tehdään sitten hyvitys suorittamalla maksu työntekijän pankkitilille toimittajille tehtävien maksujen tavoin.  

> [!TIP]
> Tässä artikkelissa käsitellään kulujen kirjaamista kirjoihin ja niiden hyvittämistä työntekijöille. Organisaatiossa voi olla portaali tai sovellus, jossa työntekijät voivat lähettää kuluraportit.

## <a name="to-record-an-employees-expense"></a>Työntekijän kulun kirjaaminen
Voit kirjat työntekijän kulut **Yleinen päiväkirja** -sivulla.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleiset päiväkirjat** ja valitse sitten liittyvä linkki.
2. Avaa liittyvä yleisen päiväkirjan erä. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).
3. Täytä tarvittaessa uuden päiväkirjarivin kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Toista vaihe 3 kaikissa kuluissa, joita työntekijällä on.

    > [!TIP]  
    > Jos haluat antaa työntekijän pankkitilille useita kulurivejä yhden vastatilin rivin yläpuolelle, valitse erän rivillä **Ehdota vastasummaa** -valintaruutu **Yleisen päiväkirjan erät** -sivulla. Tällöin vastatilin rivin **Summa**-kenttä täytetään automaattisesti arvolla, joka vaaditaan kulujen täsmäyttämiseen.
5. Kirjaa kulut työntekijän tilille valitsemalla **Kirjaa**-toiminto.

## <a name="to-reimburse-an-employee"></a>Hyvityksen tekeminen työntekijälle
Hyvitys tehdään työntekijöille kirjaamalla maksut heidän pankkitililleen **Maksupäiväkirja**-sivulla.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten liittyvä linkki.
2. Avaa käsiteltävä maksupäiväkirjan erä. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).
3. Täytä tarvittavat kentät. Lisätietoja on kohdassa [Maksujen suorittaminen](payables-make-payments.md).
4. Vaihtoehtoisesti voit valita **Ehdota työntekijämaksuja**-toiminnon, joka lisää automaattisesti odottavat työntekijän hyvitysten päiväkirjarivit.
5. Rekisteröi hyvitys valitsemalla **Kirjaa**-toiminto.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Hyvitysten täsmäyttäminen työntekijätapahtumien kanssa
Voit kohdistaa työntekijämaksut niiden liittyviin avoimiin työntekijätapahtumiin liittyvien pankkitilitapahtumien perusteella samalla tavoin kuin toimittajan maksut. Voit tehdä tämän esimerkiksi **Maksujen täsmäytyskirjauskansio** -sivulla. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md). Vaihtoehtoisesti voit tehdä kohdistuksen manuaalisesti **Työntekijätapahtumat**-sivulla. Lisätietoja on liittyvässä kohdassa [Toimittajamaksujen täsmäyttäminen maksukirjauskansiolla tai toimittajatapahtumista](payables-how-apply-purchase-transactions-manually.md)  

## <a name="see-also"></a>Katso myös
[Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen](finance-how-reverse-journal-posting.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
