---
title: Maksujen ja täsmäytysten (DK) laajennus
description: 'Tämän laajennuksen avulla on helppo viedä esimuotoiltuja tiedostoja, jotka täyttävät pankin sähköisiä lähetyksiä koskevat vaatimukset.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: 'extension, bank, formats'
ms.date: 06/24/2021
ms.author: bholtorf
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

### <a name="to-allow--to-export-payment-data"></a>[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman salliminen maksutietojen vientiä varten

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirja** ja valitse sitten vastaava linkki.  
2. Valitse **Muokkaa maksupäiväkirjaa** -sivulla **Pankin** erä.  
3. Valitse **Salli maksun vienti** -valintaruutu.  

### <a name="to-specify-a-payment-method-for-a-vendor"></a>Toimittajan maksutavan määrittäminen

Seuraavassa taulukossa ovat [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman tukemat FIK- ja TILISIIRTO-maksutapojen yhdistelmät.

|Yhdistelmä|Tyyppi 01 | Tyyppi 04 | Tyyppi 71 | Tyyppi 73 |
|----|--------|---------|---------|---------|
|Tilisiirron tilinro tai FIK:n luotonantajan nro? | Tilisiirron tilinro | Tilisiirron tilinro | FIK:n luotonantajan nro | FIK:n luotonantajan nro|
|Sallii viestin lähettämisen vastaanottajalle? | Kyllä |Ei |Ei | Kyllä |
|Sisältää maksun viitenumeron? | Ei | Kyllä, 16 numeroa. | Kyllä, 15 numeroa. | Ei|

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten vastaava linkki.  
2. Avaa kortti, laajenna **Maksut**-välilehti ja valitse maksutapa **Maksutapa**-kentässä.  
3. Täytä myös muita kenttiä valinnastasi riippuen. Yhdistelmien kuvaukset löytyvät yllä olevasta taulukosta.  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a>Pankkitilin käytettävän muodon määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.  
2. Avaa pankkitilin kortti.  
3. Valitse **Maksun vientimuoto** -kentässä vientitiedoston muoto.  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a>Toimittajan laskujen FIK:n tai tilisiirron tietojen valitseminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten vastaava linkki.
2. Valitse toimittaja. Muista, että toimittajan on oltava tanskalainen, jolla on myös osoite Tanskassa.
3. Luo lasku. **Maksutapa**- ja **Toimittajan numero** -kentät täytetään toimittajan kortin asetusten perusteella. Voit halutessasi muuttaa tietoja.
4. Syötä **Maksuviittaus**-kenttään toimittajan laskun 15 numeron sarja.  

    > [!Tip]
    > Sinun on syötettävä numerosta vain 11 viimeistä numeroa. [!INCLUDE[prod_short](includes/prod_short.md)] lisää numeron alkuun neljä nollaa.  

5. Kirjaa lasku.

## <a name="to-use-the-extension-to-export-payment-data"></a>Laajennuksen käyttäminen maksutietojen viennissä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten vastaava linkki.  
2. Valitse **Ehdota toimittajan maksupäiväkirjat** -toiminto.  

    > [!Tip]
    > Jos haluat viedä vain tietyt maksut, käytä tietojen suodatusta.  

3. Voit tarvittaessa lisätä suodattimia, jos haluat viedä vain tietyt maksut.  
4. Valitse **Pankkimaksun tyyppi** -kentässä **Sähköinen maksu**.  
5. Valitse **Vie**-toiminto.  

## <a name="see-also"></a>Katso myös

[Business Central -sovelluksen mukauttaminen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaa varten laajennusten avulla](ui-extensions.md)  
[Maksujen kerääminen SEPA-suoraveloitusperintänä.](finance-collect-payments-with-sepa-direct-debit.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
