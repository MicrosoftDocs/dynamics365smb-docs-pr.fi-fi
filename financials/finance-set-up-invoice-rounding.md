---
title: "Laskun pyöristyksen määrittäminen | Microsoft Docs"
description: "Voit pyöristää laskujen summat, kun luot laskuja. Paikalliset määräykset tai tavat voivat lisäksi edellyttää laskun pyöristystä tietyllä tavalla (esimerkiksi niin, että summa on jaollinen luvulla 0,05)."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ceebeeac325c00d6aef25d8ca51fcfee1ab4e1d5
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-invoice-rounding"></a>Laskun pyöristyksen määrittäminen
Jos laskujen summat on pyöristettävä laskuja luotaessa, voit käyttää automaattista pyöristystoimintoa. Kun lasku pyöristetään, lisätään lisärivi, joka sisältää pyöristyssumman ja joka kirjataan muiden laskurivien kanssa.

> [!NOTE]  
>  Paikalliset määräykset tai tavat saattavat vaatia laskun pyöristystä tietyllä tavalla (esimerkiksi niin, että summa on jaollinen luvulla 0,05).  
  
Jos haluat käyttää automaattista laskun pyöristystä, sinun on  
  
* määritettävä kirjanpitotilit, joille pyöristyserot kirjataan  
* määritettävä laskujen pyöristyksen säännöt paikallista valuuttaa ja ulkomaanvaluuttaa varten  
* aktivoitava toiminto.  
  
> [!NOTE]  
>  Laskun pyöristysominaisuuksien lisäksi laskujen summien pyöristyksessä voi käyttää yksikkösumman ja summan pyöristysominaisuuksia.  
 
## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>KP-tilien määrittäminen laskun kohdistuksen pyöristyseroille
Kun haluat käyttää ohjelman automaattista laskunpyöristystoimintoa, sinun täytyy määrittää se KP-tili (tai ne KP-tilit), joille pyöristyserot kirjataan. Sitä ennen sinun täytyy luoda tuotteen ALV-kirjausryhmät. Lisätietoja on kohdassa [ALV:n määrittäminen](finance-setup-vat.md).  
  
### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>KP-tilien määrittäminen laskun kohdistuksen pyöristyseroille  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tilikartta** ja valitse sitten aiheeseen liittyvä linkki.  
2. Määritä tili **Tilikartta**-sivulla ja anna sen nimeksi esimerkiksi **Laskun pyöristys**. [!INCLUDE[d365fin](includes/d365fin_md.md)] käyttää tätä tilin nimeä pyöristetyissä laskuissa.  
3. Valitse **Veron ALV-kirjausryhmä**- tai **Tuotteen ALV-kirjausryhmä** -kentässä pyöristettyjen summien kirjausryhmä sen mukaan, onko kyseessä ALV- vai myyntivero. Voit halutessasi määrittää uuden ryhmäkoodin laskun pyöristystä varten.
4. Jätä **Yleinen kirjaustyyppi**- ja joko **Liiketoiminnan veron kirjausryhmä**- tai **Liiketoiminnan ALV-kirjausryhmä** -kenttä tyhjäksi. <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  
  
Voit nyt määrittää laskun pyöristystilin kirjausryhmille **Toimittajan kirjausryhmät** -sivulla.  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a>Ulkomaan valuutan ja paikallisen valuutan pyöristämisen määrittäminen
Ulkomaanvaluutan ja paikallisen valuutan pyöristämissäännöt on määritettävä ennen automaattisen pyöristystoiminnon käyttöä.

### <a name="to-set-up-rounding-for-foreign-currencies"></a>Ulkomaan valuuttojen pyöristyssääntöjen määrittäminen  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Valuutat** ja valitse sitten aiheeseen liittyvä linkki.  
2. Avaa **Valuutan kortti** valitsemalla **Valuutat**-sivulla ulkomaanvaluutta ja täytä sitten **Summan pyöristystarkkuus**-, **Yksikkösumman pyöristystarkkuus**-, **Laskun pyöristystarkkuus**- ja **Laskun pyöristystyyppi** -kentät.
  
### <a name="to-set-up-rounding-for-your-local-currency"></a>Paikallisen valuutan pyöristyssääntöjen määrittäminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Pääkirjanpidon asetukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä **Pääkirjanpidon asetukset** -sivun **Yleiset**-pikavälilehdessä **Laskun pyöristystarkkuus**- ja **Laskun pyöristystyyppi** -kentät.  

## <a name="activate-the-invoice-rounding-function"></a>Laskun pyöristystoiminnon aktivointi  
Laskun pyöristystoiminto on aktivoitava, jotta voit varmistaa myynti- ja ostolaskujen automaattisen pyöristyksen. Voit aktivoida laskunpyöristyksen erikseen myynti- ja ostolaskuille.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntien ja myyntisaamisten asetukset** tai **Ostojen ostovelkojen asetukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Yleiset**-pikavälilehdessä **Laskun pyöristys** -valintaruutu.  
  
## <a name="see-also"></a>Katso myös  
[Myynnin laskutus](sales-how-invoice-sales.md)  
[Ostojen kirjaus](purchasing-how-record-purchases.md)
