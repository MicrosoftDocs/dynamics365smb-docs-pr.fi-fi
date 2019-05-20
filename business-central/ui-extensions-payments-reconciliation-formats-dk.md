---
title: Maksujen ja täsmäytysten (DK) laajennuksen käyttäminen | Microsoft Docs
description: Tämän laajennuksen avulla on helppo viedä esimuotoiltuja tiedostoja, jotka täyttävät pankin sähköisiä lähetyksiä koskevat vaatimukset.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: ff09be509c1ab6366dbd852a5c1c6e69f46cc9d5
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250731"
---
# <a name="the-payments-and-reconciliations-dk-extension"></a>Maksujen ja täsmäytysten (DK) laajennus
Tee nopeita ja virheettömiä maksuja tuomalla tiedostot, jotka on muotoiltu erityisesti toimittajan tai pankin kanssa tapahtuvia siirtoja varten. Nämä tiedostot nopeuttavat maksu- ja täsmäytysprosesseja ja eliminoivat virheet, joita voi tapahtua tietojen manuaalisessa syöttämisessä pankin sivustossa.  

Tämä laajennus tukee useiden Tanskan pankkien tiedostomuotoja. Kun vietä maksutiedot tiedostoon, laajennus pakkaa tiedot pankin vaatimaan muotoon. Muotoja ovat esimerkiksi Bankdata-V3, BEC, SDC ja FIK, joita useat pankit käyttävät. Jotkin pankit, kuten Danske Bank ja Nordea, käyttävät erikoismuotoja. Laajennus sisältää myös muotoja tiliotteiden tuontia ja täsmäytystä varten.  

> [!Note]
> Sinun tulee tietää pankin tai toimittajan vaatima muoto, jotta voit käyttää laajennusta. Jotkin pankit ja toimittajat kertovat tämän tiedon verkkosivustoillaan. Joissakin tapauksissa tieto on pyydettävä pankin tai toimittajan asiakaspalvelusta.  

## <a name="supported-bank-formats"></a>Tuetut pankin muodot
Tätä laajennusta voi käyttää seuraavissa maksutiedostojen muodoissa:  

* BANKDATA-V3  
* BEC-INDLAND  
* BEC-CSV  
* DANSKEBANK-CMKV  
* DANSKEBANK-CMKXKSX  
* DANSKEBANK  
* FIK71  
* NORDEA-ERHVERV-CSV  
* NORDEA  
* NORDEA-UNITEL-V3  
* SDC  
* SDC-CSV  

## <a name="to-set-up-the-extension"></a>Laajennuksen määrittäminen
Aloittaminen edellyttää muutamien vaiheiden suorittamista.  

* Salli maksutietojen viennit. Tätä ei ole sallittu oletusarvoisesti tietoturvan vuoksi.  
* Määritä ostot ja ostovelat niin, että laskuissa ei tarvita ulkoisten asiakirjojen numeroita. Voit tarvittaessa käyttää viitenumeroa, kun viittaat tiettyyn laskuun.  
* Määritä kunkin toimittajan maksutapa. Maksutavat määrittävät, miten maksat toimittajien laskut. Maksutapa voi olla esimerkiksi pankki, käteinen, sekki tai tili.  
* Määritä kunkin pankkitilin käyttämän muodon tyyppi. Tyyppi voi olla esimerkiksi NORDEA, DANSKEBANK tai SDC.  

Lisäksi on määritettävä toimittajat kotimaan **Ylein. liiketoim. kirjausryhmä**- ja **Toimittajan kirjausryhmä** -kohtaan. Toimittajan maa-/alueasetukseksi on määritettävä Tanska (DK). Lisätietoja on kohdassa [Kirjausryhmien määrittäminen](finance-posting-groups.md).  

### <a name="to-allow-included365finincludesd365finmdmd-to-export-payment-data"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman salliminen maksutietojen vientiä varten
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Muokkaa maksupäiväkirjaa** -sivulla **Pankin** erä.  
3. Valitse **Salli maksun vienti** -valintaruutu.  

### <a name="to-specify-a-payment-method-for-a-vendor"></a>Toimittajan maksutavan määrittäminen
Seuraavassa taulukossa ovat [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman tukemat FIK- ja TILISIIRTO-maksutapojen yhdistelmät.

||Tyyppi 01 | Tyyppi 04 | Tyyppi 71 | Tyyppi 73 |
|----|---|---|---|---|
|Tilisiirron tilinro tai FIK:n luotonantajan nro? | Tilisiirron tilinro | Tilisiirron tilinro | FIK:n luotonantajan nro | FIK:n luotonantajan nro|
|Sallii viestin lähettämisen vastaanottajalle? | Kyllä |Ei |Ei | Kyllä |
|Sisältää maksun viitenumeron? | Ei | Kyllä, 16 numeroa. | Kyllä, 15 numeroa. | Ei|

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten liittyvä linkki.  
2. Avaa kortti, laajenna **Maksut**-välilehti ja valitse maksutapa **Maksutapa**-kentässä.  
3. Täytä myös muita kenttiä valinnastasi riippuen. Yhdistelmien kuvaukset löytyvät yllä olevasta taulukosta.  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a>Pankkitilin käytettävän muodon määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten liittyvä linkki.  
2. Avaa pankkitilin kortti.  
3. Valitse **Maksun vientimuoto** -kentässä vientitiedoston muoto.  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a>Toimittajan laskujen FIK:n tai tilisiirron tietojen valitseminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten liittyvä linkki.
2. Valitse toimittaja. Muista, että toimittajan on oltava tanskalainen, jolla on myös osoite Tanskassa.
3. Luo lasku. **Maksutapa**- ja **Toimittajan numero** -kentät täytetään toimittajan kortin asetusten perusteella. Voit halutessasi muuttaa tietoja.
4. Syötä **Maksuviittaus**-kenttään toimittajan laskun 15 numeron sarja.  

    > [!Tip]
    > Sinun on syötettävä numerosta vain 11 viimeistä numeroa. [!INCLUDE[d365fin](includes/d365fin_md.md)] lisää numeron alkuun neljä nollaa.  

5. Kirjaa lasku.

## <a name="to-use-the-extension-to-export-payment-data"></a>Laajennuksen käyttäminen maksutietojen viennissä
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten liittyvä linkki.  
2. Valitse **Ehdota toimittajan maksupäiväkirjat** -toiminto.  

    > [!Tip]
    > Jos haluat viedä vain tietyt maksut, käytä tietojen suodatusta.  

3. Voit tarvittaessa lisätä suodattimia, jos haluat viedä vain tietyt maksut.  
4. Valitse **Pankkimaksun tyyppi** -kentässä **Sähköinen maksu**.  
5. Valitse **Vie**-toiminto.  

## <a name="see-also"></a>Katso myös .
[Business Central -sovelluksen mukauttaminen [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaa varten laajennusten avulla](ui-extensions.md)  
[SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
[SEPA-suoraveloituksen määrittäminen](finance-how-to-set-up-sepa-direct-debit.md)  
[SEPA-suoraveloitusmaksujen kirjaaminen](finance-how-to-post-sepa-direct-debit-payment-receipts.md)  
[Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
