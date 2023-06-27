---
title: Työntekijöiden kulujen kirjaaminen ja hyvittäminen
description: Hyvitä liiketoimintaan liittyvä kulu kirjaamalla työntekijän kulut ensin yleisessä päiväkirjassa työntekijän tilille ja sitten maksu hänen tililleen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.search.form: '63, 234, 625, 5224, 5237, 5238, 5239, 5240'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="record-and-reimburse-employees-expenses"></a>Työntekijöiden kulujen kirjaaminen ja hyvittäminen

[!INCLUDE[prod_short](includes/prod_short.md)] tukee työntekijöiden tapahtumia samalla tavoin kuin toimittajien tapahtumia. Niinpä työntekijän kirjausryhmien avulla voidaan varmistaa, että työntekijätapahtumat kirjataan oikeille yleisen päiväkirjan tileille.

> [!NOTE]  
> Työntekijätapahtumat voidaan kirjata vain paikallisena valuuttana. Työntekijöille tehtävät hyvitysmaksut eivät tue alennuksia ja maksutoleransseja.

Jos työntekijät voivat käyttää omia varojaan liiketoiminnoissa, voit kirjata kulun työntekijän tilille. Työntekijälle tehdään sitten hyvitys suorittamalla maksu työntekijän pankkitilille toimittajille tehtävien maksujen tavoin.  

> [!TIP]
> Tässä artikkelissa käsitellään kulujen kirjaamista kirjoihin ja niiden hyvittämistä työntekijöille. Organisaatiossa voi olla portaali tai sovellus, jossa työntekijät voivat lähettää kuluraportit.

Joustavana [!INCLUDE [prod_short](includes/prod_short.md)] sopii moniin erilaisiin käytäntöihin. Käytettävät tilinumerot määräytyvät organisaation määritysten ja prosessien mukaan.  

## <a name="to-record-an-employees-expense"></a>Työntekijän kulun kirjaaminen

Voit kirjat työntekijän kulut **Yleinen päiväkirja** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten vastaava linkki.  
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

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten vastaava linkki.
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
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
