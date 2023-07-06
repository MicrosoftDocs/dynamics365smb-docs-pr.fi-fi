---
title: SEPA-suoraveloitus Business Centralissa
description: Asiakkaan suostumuksella voit kerätä maksut suoraan asiakkaan pankkitililtä SEPA-muodon mukaisesti.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '371, 423, 424, 427, 1208, 1207, 1230'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="collect-payments-with-sepa-direct-debit"></a><a name="collect-payments-with-sepa-direct-debit"></a><a name="collect-payments-with-sepa-direct-debit"></a>Maksujen kerääminen SEPA-suoraveloitusperintänä.

Asiakkaan suostumuksella voit kerätä maksut suoraan asiakkaan pankkitililtä SEPA-muodon mukaisesti.  

Määritä ensin pankkitiedoston vientimuoto, joka ohjaa pankkia suorittamaan suoraveloituksen. Määritä sitten asiakkaan maksutapa. Määritä lopuksi asiakkaasi kanssa sovitun mukainen suoraveloitusvaltakirja, jolla heidän maksunsa peritään tietyllä sopimusjaksolla.  

Jos haluat ohjata pankkia siirtämään maksusumman asiakkaan pankkitililtä yrityksesi tilille, loit suoraveloitusperintämerkinnän, joka säilyttää tiedot pankkitileistä ja kyseessä olevista myyntilaskuista sekä suoraveloitusvaltakirjasta. Syntyvästä suoraveloitusperintämerkinnästä viet sitten perintämerkintään perustuvan XML-tiedoston, jonka lähetät tai lataat verkkopankkiin käsittelyä varten. Kaikista maksuista, joita ei voitu käsitellä, tiedotetaan sinulle pankin toimesta. Sinun täytyy sitten manuaalisesti hylätä kyseessä olevat suoraveloitusmerkinnät.  

Voit määrittää vakioasiakasmyyntikoodin suoraveloitusmaksumenetelmällä ja valtakirjatiedoilla. Voit sitten käyttää **Luo vakioasiakaslaskut** -eräajoa ja luoda useita myyntilaskuja, joissa suoraveloitustiedot on täytetty valmiiksi. Tämä voidaan tehdä manuaalisesti tai automaattisesti maksun eräpäivän mukaisesti.  

Kun maksut on käsitelty onnistuneesti pankin tiedottamalla tavalla, voit kirjata maksukuitit joko suoraan **Suoraveloitusperintätapahtumat**-sivulla tai siirtää maksurivit päiväkirjaan, johon kirjaat maksukuitit, kuten **Kassapäiväkirja**-sivulle. Vaihtoehtoisesti kassanhallintamenetelmästäsi riippuen, voit odottaa ja kohdistaa maksut osana pankin täsmäytystä.  

> [!NOTE]  
> Kun maksut kerätään SEPA-suoraveloituksen avulla, myyntilaskun valuutan on oltava EURO.  

## <a name="setting-up-sepa-direct-debit"></a><a name="setting-up-sepa-direct-debit"></a><a name="setting-up-sepa-direct-debit"></a>SEPA-suoraveloituksen määrittäminen

**Suoraveloitusperinnät**-sivulla voi viedä sähköiseen pankkiin ohjeita, jotka ohjaavat pankkiasi suorittamaan suoraveloituksen asiakkaan pankkitililtä omalle pankkitilillesi SEPA-suoraveloitusmuodon mukaisesti.

> [!NOTE]
> Maailmanlaajuinen versio [!INCLUDE[prod_short](includes/prod_short.md)]ista tukee vain SEPA-suoraveloitusmuotoa. Maassasi/alueellasi saattaa olla käytettävissä muita elektronisten maksujen muotoja. Katso kohta **Paikalliset toiminnon** sisällysluettelossa.  

Jos haluat ottaa käyttöön sellaisten pankkitiedostomuotojen viennin, joita [!INCLUDE[prod_short](includes/prod_short.md)] ei tue sellaisenaan, voit määrittää tietojen siirtomäärityksen käyttämällä tiedonsiirtokehystä. Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).  

Ennen kuin voit käsitellä asiakkaan maksuja sähköisesti viemällä suoraveloitusohjeita SEPA Direct Debit -muodossa, sinun on suoritettava seuraavat määritysvaiheet.  

* Määritä sen pankkitiedoston vientimuoto, joka ohjaa pankkiasi suorittamaan suoraveloituksen asiakkaan pankkitililtä omalle pankkitilillesi.  
* Määritä asiakkaan maksutapa.  
* Määritä suoraveloitustoimeksianto, joka kuvaa asiakkaan kanssa tekemääsi sopimusta maksujen keräämisestä tietyllä sopimuskaudella.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a><a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a><a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>SEPA-suoraveloituksen pankkitilin määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.  
2. Avaa pankkitili, jota haluat käyttää suoraveloitukseen.  
3. Valitse **Siirto**-pikavälilehden **SEPA-suoraveloituksen vientimuoto** -kentässä SEPA-suoraveloitusasetus.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a><a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a><a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>SEPA-suoraveloituksen asiakkaan maksutavan määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksutavat** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Määritä maksutapa. Täytä suoraveloitus\-kohtaiset kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Suoraveloitus**|Määrittää, käytetäänkö maksutapaa SEPA-suoraveloitusperintään.|  
    |**Suoraveloituksen maksuehtojen koodi**|Määritä maksuehdot, kuten ÄLÄ MAKSA, jotka näkyvät SEPA-suoraveloituksena maksettavissa myyntilaskuissa ilmoittamassa asiakkaalle, että maksu kerätään automaattisesti. Vaihtoehtoisesti tämän kentän voi jättää tyhjäksi.|  

    > [!NOTE]  
    >  Älä anna arvoa **Vastatilin nro** -kenttään.  

4. Valitse **OK**-painike **Maksutavat**-sivun sulkemiseksi.  
5. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.  
6. Avaa asiakkaan kortti asiakkaalle, jolle haluat määrittää SEPA-suoraveloitusperinnän.  
7. Valitse **Maksutavan koodi** -kenttä ja sitten maksutavan koodi, jonka määritit vaiheessa 3.  
8. Toista vaiheet 6–7 kaikille asiakkaille, joille haluat määrittää SEPA-suoraveloitusperinnän.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a><a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a><a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Suoraveloitusvaltakirjan määrittäminen, joka vastaa asiakkaan sopimusta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.  
2. Avaa asiakkaan kortti, jonka haluat määrittää SEPA-suoraveloituksille.  
3. Valitse **Pankkitilit**-toiminto.  
4. Valitse **Asiakkaan pankkitililuettelo** -sivulla asiakkaan pankkitili, jota käytät suoraveloitukseen, ja valitse sitten **Suoraveloitusvaltakirja**-toiminto.  
5. Täytä **Suoraveloitusvaltakirjat**-sivun kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Asiakkaan pankkitilin koodi**|Määrittää pankkitilin, josta suora\-veloitusmaksut kerätään. Tämä kenttä täytetään automaattisesti.|  
    |**Voimassaolo alkaa**|Määritä päivämäärä, jolloin suora\-veloitusvaltakirja alkaa.|  
    |**Voimassaolo päättyy**|Määritä päivämäärä, jolloin suora\-veloitusvaltakirja päättyy.|  
    |**Allekirjoituspäivämäärä**|Määritä päivämäärä, jolloin asiakas allekirjoitti suora\-veloitusvaltakirjan.|  
    |**Maksun tyyppi**|Määritä, koskeeko sopimus useita (**Toistuva**) tai yksittäisiä (**Kerta**) suoraveloitusperintöjä.|  
    |**Debetien odotettu määrä**|Määritä, kuinka monta suoraveloitusperintään sinulla on tarkoitus tehdä. Tämä kenttä on merkittävä vain, jos olet valinnut **Toistuva**-vaihtoehdon **Maksun tyyppi** -kentästä.|  
    |**Debet-laskuri**|Määrittää, kuinka monta suoraveloitusperintää on tehty tätä suora\-veloitusvaltakirjaa käyttämällä. Tämä kenttä päivitetään automaattisesti.|  
    |**Suljettu**|Määrittää, kuinka monta suoraveloitusperintää ei voida tehdä tätä suora\-veloitusvaltakirjaa käyttämällä.|  

6. Toista vaiheet 1–5 kaikille asiakkaille, joille haluat määrittää SEPA-suoraveloitukset.  

 Suoraveloitusvaltakirja lisätään automaattisesti **Suoraveloitusvaltakirjan tunnus** -kenttään, kun luot myyntilaskun vaiheessa 2 valitulle asiakkaalle. Lisätietoja on kohdassa [Toistuvien myynti- ja ostorivien luominen](sales-how-work-standard-lines.md).

## <a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a><a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a><a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon

Jos haluat ohjata pankin siirtämään maksusumman asiakkaan pankkitililtä yrityksesi tilille, luo suoraveloitusperintätapahtuma, joka säilyttää tiedot asiakkaan pankkitilistä, kyseisestä myyntilaskuista ja suoraveloitusvaltakirjasta. Syntyvästä suoraveloitusperintämerkinnästä viet sitten XML-tiedoston, jonka lähetät tai lataat verkkopankkiin käsittelyä varten. Kaikista maksuista, joita pankki ei voinut käsitellä, tiedotetaan sinulle pankin toimesta. Sinun täytyy sitten manuaalisesti hylätä kyseessä olevat suoraveloitusmerkinnät.  

 > [!NOTE]  
 > Kun maksut kerätään SEPA-suoraveloituksen avulla, myyntilaskun valuutan on oltava EURO.  

### <a name="to-create-a-direct-debit-collection"></a><a name="to-create-a-direct-debit-collection"></a><a name="to-create-a-direct-debit-collection"></a>Suoraveloitusperinnän luominen

 1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Suoraveloitusperinnät** ja valitse sitten vastaava linkki.  
 2. Valitse **Suoraveloitusperinnät**-sivulla **Luo suoraveloitusperintä** -toiminto.  
 3. Täytä **Luo suoraveloitusperintä**-sivun kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Eräpäivästä**|Määritä maksun aikaisin eräpäivä myyntilaskuille, joille haluat luoda suoraveloitusperinnän.|  
    |**Eräpäivään**|Määritä myöhäisin maksun eräpäivä myyntilaskuille, joille haluat luoda suoraveloitusperinnän.|  
    |**Kumppanin tyyppi**|Määrittää, suoritetaanko suoraveloitusperintä asiakkaille, joiden tyyppi on **yritys** vain **henkilö**.|  
    |**Vain asiakkaat, joilla on kelvollinen valtakirja**|Määritä, luodaanko suoraveloitus asiakkaille, joilla on voimassa oleva suoraveloitusvaltakirja. **Huomautus:** Suoraveloitusperintä luodaan, vaikka **Suoraveloitusvaltakirjan tunnus** -kenttää ei olisi täytetty myyntilaskussa.|  
    |**Vain laskut, joilla on kelvollinen valtakirja**|Määritä, luodaanko suoraveloitusperintä vain myyntilaskuille, jos myyntilaskun **Suoraveloitusvaltakirjan tunnus** -kentässä on valittu sallittu suoraveloitusvaltakirja.|  
    |**Pankkitilin nro**|Määritä, mille yrityksen pankkitilille perityt maksut siirretään asiakkaan pankkitililtä.|  
    |**Pankkitilin nimi**|Määrittää pankkitilin nimen, jonka valitset **Pankkitilin nro** -kentässä. Tämä kenttä täytetään automaattisesti.|  

 4. Valitse **OK**-painike.  

Suoraveloitusperintä lisätään **Suoraveloitusperinnät**-sivulle ja vähintään yksi suoraveloitusperintätapahtuma luodaan.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a><a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a><a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Suoraveloitusperintätapahtuman vieminen pankkitiedostoon

 1. Valitse **Suoraveloitusperinnät**-sivulla **Suoraveloitusperintämerkintä**-toiminto.  
 2. Valitse **Suoraveloitusperintätapahtumat**-sivulla merkintä, jonka haluat viedä, ja valitse sitten **Luo suoraveloitustiedosto**.  
 3. Tallenna vientitiedosto paikkaan, josta lähetät tai lataat sen verkkopankkiisi.  

      **Suoraveloitusperintätapahtumat**-sivun **Suoraveloitusperinnän tila** -kentän arvoksi muutetaan Tiedosto luotu. **Suoraveloitusvaltakirjat**-sivun **Debet-laskuri**-kentän arvoa nostetaan yhdellä.  

 Jos vietyä tiedostoa ei voi käsitellä, esimerkiksi sen vuoksi, että asiakkaan pankkitilillä ei ollut riittävästi varoja, voit hylätä suoraveloitusperintämerkinnän. Jos pankki käsitteli vientitiedoston onnistuneesti, kyseessä olevien myyntilaskujen erääntyneet maksut kerätään automaattisesti kyseisiltä asiakkailta. Tässä tapauksessa voit sulkea perinnän.  

### <a name="to-reject-a-direct-debit-collection-entry"></a><a name="to-reject-a-direct-debit-collection-entry"></a><a name="to-reject-a-direct-debit-collection-entry"></a>Suoraveloitusperintätapahtuman hylkääminen

* Valitse **Suoraveloitusperintätapahtumat**-sivulla tapahtuma, jonka käsittely ei onnistunut, ja valitse sitten **Hylkää tapahtuma**.  

    **Suoraveloitusperintätapahtumat**-sivun **Tila**-kentän arvoksi muutetaan **Hylätty**.  

### <a name="to-close-a-direct-debit-collection"></a><a name="to-close-a-direct-debit-collection"></a><a name="to-close-a-direct-debit-collection"></a>Suoraveloitusperinnän sulkeminen

* Valitse **Suoraveloitusperintätapahtumat**-sivulla tapahtuma, jonka käsittely ei onnistunut, ja valitse sitten **Sulje kokoelma**.  

    Liittyvä suoraveloitusperintä suljetaan.  

 Voit nyt siirtyä kirjaamaan mukana olevien myyntilaskujen maksukuitit. Voit tehdä tämän, kun yleensä kirjaat maksukuitteja, kuten **Maksurekisteröinti**-sivulla, tai voit kirjata liittyvät maksukuitit suoraan **Suoraveloitusperintätapahtumat**-sivulta. Lisätietoja on ohjeaiheessa [Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md).

## <a name="posting-sepa-direct-debit-payment-receipts"></a><a name="posting-sepa-direct-debit-payment-receipts"></a><a name="posting-sepa-direct-debit-payment-receipts"></a>SEPA-suoraveloitusmaksujen kirjaaminen

Kun pankki on käsitellyt onnistuneesti suoraveloitusperinnän, voit siirtyä kirjaamaan maksukuitit kyseiselle myyntilaskuille. Lisätietoja on kohdassa [SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file).  

Voit kirjata suoraan maksun suoraan **Suoraveloitusperinnät**- tai **Suoraveloitusperintätapahtumat**-sivulta. Vaihtoehtoisesti voit siirtää työn toiselle käyttäjälle valmistelemalla siihen liittyvät päiväkirjarivit.  

### <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a><a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a><a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a>Suoraveloitusmaksukuitin kirjaaminen suoraveloitusperinnän sivulta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Suoraveloitusperinnät** ja valitse sitten vastaava linkki.  
2. Valitse rivi suoraveloitusperinnälle, joka on viety pankkitiedostoon ja jonka pankki on käsitellyt onnistuneesti.
3. Valitse **Kirjaa maksukuitit** -toiminto.  
4. Täytä **Kirjaa suoraveloitusperintä**-sivun kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Suoraveloitusperinnän nro**|Määritä suoraveloitusperintä, johon haluat kirjata maksukuitin.|  
    |**Yleisen päiväkirjan malli**|Määritä, mitä yleisen päiväkirjan mallia käytit maksukuitin kirjaamiseen, kuten kassakuittien malli.|  
    |**Yleisen päiväkirjan erän nimi**|Määritä, mitä yleistä päiväkirjaerää käytit maksukuitin kirjaamiseen.|  
    |**Luo vain päiväkirja**|Merkitse tämä valintaruutu, jos et halua kirjata maksukuittia, kun valitset **OK**-painikkeen. Maksukuitti valmistellaan määritetyssä päiväkirjassa eikä sitä kirjata ennen kuin joku kirjaa kyseisen päiväkirjarivin.|  

5. Valitse **OK**-painike.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Huoltohallinto](service-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
