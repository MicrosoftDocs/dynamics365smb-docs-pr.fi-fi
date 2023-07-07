---
title: Nimikkeiden siirtäminen varastosijaintien välillä
description: Tietoja varastonimikkeiden siirtämisestä varastosta toiseen joko uudelleenluokituspäiväkirjan tai siirtotilausten avulla.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
---
# <a name="transfer-inventory-between-locations"></a>Varastonimikkeiden siirtäminen sijaintien välillä

Varastonimikkeitä siirretään sijaintien välillä luomalla siirtotilauksia. Vaihtoehtoisesti voit käyttää uudelleenluokituspäiväkirjaa.

> [!NOTE]
> Nimikkeiden siirtäminen edellyttää sijaintien siirtoreittien määrittämistä. Lisätietoja sijaintien määrittämisestä on kohdassa [Sijaintien määrittäminen](inventory-how-setup-locations.md). Siirtotilauksia ei voi käyttää *tyhjissä* sijainneissa.

## <a name="transfer-orders"></a>Siirtotilaukset

Lähtevä siirto voidaan lähettää yhdestä sijainnista ja vastaanottaa kohteessa saapuvana siirtona. Voit:

* Kuljetuksessa olevan määrän seuraaminen
* Päivämäärän laskentaa ja suunnittelua varten määritetään kalenterit, reitit sekä saapuvien ja lähtevien käsittelyajat. Lisätietoja suunnittelusta on kohdassa [Tietoja suunnittelutoiminnosta](production-about-planning-functionality.md).
* Saapuvissa ja lähtevissä sijainneissa käytetään erilaisia varastointiominaisuuksia:
* Joitakin rajoituksia lukuun ottamatta siirtotilauksia voidaan käyttää suorissa siirroissa.

## <a name="item-reclassification-journals"></a>Nimikkeen uudelleenluokituspäiväkirjat

* Yksinkertainen nimikkeiden suora siirto sijaintien välillä
* Nimikkeiden siirtäminen varastopaikkojen välillä. Lisätietoja nimikkeiden siirtämisestä varastopaikkojen välillä on kohdassa [Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)
* Erä- tai sarjanumeron vaihtaminen uuteen erä- tai sarjanumeroon. Lisätietoja sarja- ja eränumeroiden uudelleenluokittelusta on kohdassa [Sarja- ja eränumeroiden uudelleenluokittelu](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Vanhentumispäivän vaihtaminen uudeksi päivämääräksi.
* Nimikkeiden uudelleenluokitteleminen *tyhjästä* sijainnista varsinaiseen sijaintiin.
* Fyysisen varaston aktiviteetteja ei hallita. Fyysisen varastoinnin tapahtumat luodaan.

## <a name="to-transfer-items-with-a-transfer-order"></a>Nimikkeiden siirtäminen siirtotilauksella

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirtotilaukset** ja valitse sitten vastaava linkki.
2. Täytä **Siirtotilaus**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Jos **Siirtoreitin määritykset** -sivun **Kuljetuksessa-koodi**-, **Kuljetusliikkeen koodi**- ja **Kuljetusliikkeen palvelu** -kentät on täytetty siirtoreitin määrityksen yhteydessä, vastaavat kentät täytetään automaattisesti siirtotilauksessa.

    Kun **Kuljetusliikkeen palvelu** -kenttä täytetään, kohteeseen-sijainnin vastaanottopäivämäärä lasketaan lisäämällä kuljetusliikkeen palvelun toimitusajan Kohteesta-pikavälilehden lähetyksen päivämäärään.

3. Rivit voi täyttää monella eri tavalla:

    |Asetus  |Kuvaus  |
    |---------|---------|
    |Manuaalisesti     | **Rivit**-pikavälilehdessä täytä nimikkeen rivi tai valitse useita nimikkeitä **Valitse nimikkeet** -toiminnon avulla.        |
    |Automaattisesti     | * Valitse **Hae var.paikan sisältö** -toiminnolla aiemmin luotuja nimikkeita tietystä sijainnin varastopaikasta.<br><br>* Valitse **Hae vastaanottorivit** -toiminnolla nimikkeet, jotka ovat juuri saapuneet kohteesta-sijainnista.        |

    Nimikkeitä voi nyt toimittaa.
4. Valita ensin **Kirjaa**-toiminto, sitten **Toimitus**-asetus ja lopuksi **OK**-painike.

    Nimikkeet ovat nyt matkalla valittujen sijaintien välillä valitun siirtoreitin mukaisesti.

    Kohteesta-sijainnin varastotyöntekijänä voit siirtyä nimikkeiden vastaanottamiseen. Siirtotilausrivit ovat samat kuin toimituksen aikana eikä niitä voi muokata.
5. Valita ensin **Kirjaa**-toiminto, sitten **Vastaanotto**-asetus ja lopuksi **OK**-painike.

### <a name="post-multiple-transfer-orders-in-a-batch"></a>Kirjaa useita siirtotilauksia erässä

Siirtotilauksia voi eräkirjata toimimalla seuraavasti.

1. 1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirtotilaukset** ja valitse sitten vastaava linkki.  
2. Valitse kirjattavat tilaukset **Siirtotilaukset**-sivulta.
3. Valitse **Nro**-kenttään avaa pikavalikko ja valitse **Valitse lisää**.
4. Valitse kunkin kirjattavan tilauksen rivien valintaruutu.
5. Valitse ensin **Kirjaus**-toiminto ja sitten **Eräkirjaus**-toiminto.
6. Täytä **Eräkirjaa siirtotilaukset** -sivulla tarvittavat kentät.

   > [!TIP]
    > Jos siirtotilaukset käyttävät kuljetuksessa-sijaintia, voit valita joko **Toimitus** tai **Vastaanottaminen**. Toista tämä vaihe, jos sinun täytyy tehdä molemmat. Jos tilauksessa on käytössä **Suorakirjaus**, molemmat vaihtoehdot toimivat samalla tavalla ja tilaukset kirjataan kokonaan.

7. Valitse **OK**.
8. Voit tarkastella mahdollisia ongelmia avaamalla **Virhesanomarekisteri**-sivun.

    > [!NOTE]
    > Usean asiakirjan kirjaaminen voi kestää jonkin aikaa ja estää muita käyttäjiä. Harkitse taustakirjauksen käyttöönottoa. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](/dynamics365/business-central/admin-job-queues-schedule-tasks).

### <a name="schedule-a-job-queue-entry-to-post-multiple-documents-in-a-batch"></a>Työjonotapahtuman ajoittaminen useiden asiakirjojen kirjaamiseksi erässä

Työjonon avulla voit myös ajoittaa kirjauksen tapahtuvaksi organisaatiolle sopivana ajankohtana. Yrityksessä saattaa olla esimerkiksi hyödyllistä suorittaa tietyt toiminnot sen jälkeen, kun suurin osa päivän tiedoista on syötetty.

Seuraavaksi selitetään, miten **Eräkirjaa siirtotilaukset** -raportti määritetään kirjaamaan suorasiirtotilaukset automaattisesti arkipäivisin kello 16. Tämä aika on vain esimerkki. Vaiheet ovat samat muissa asiakirjoissa.  

1. Etsi **Työjonon tapahtumat** -sivu ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3. Valitse **Suoritettavan objektin tyyppi** -kentässä **Raportti**.  
4. Valitse **Suoritettavan objektin tunnus** -kentässä **5707, Eräkirjaa siirtotilaukset**.
5. Valitse **Raporttipyyntösivu**-valintaruutu.
6. Valitse **Eräkirjaa siirtotilaukset** -sivulla **Toimitus**-vaihtoehto, suodata **Suorasiirto**-kohdassa ja valitse sitten **OK**.

   > [!IMPORTANT]
   > On tärkeää asettaa suodattimia. Muussa tapauksessa [!INCLUDE [prod_short](includes/prod_short.md)] kirjaa kaikki asiakirjat, vaikka ne eivät olisikaan valmiita. **Vapautettu**-arvon käyttöä suodattimen **Tilan**-kentän arvona ja **tänään**-arvoa **Kirjauspäivämäärä**-kentän arvona kannattaa harkita. Saat lisätietoja suodattimista siirtymällä kohtaan [Lajitteleminen, hakeminen ja suodattaminen](/dynamics365/business-central/ui-enter-criteria-filters).

7. Valitse kaikki valintaruudut **Suorita maanantaisin** -kohdasta **Suorita perjantaisin** -kohtaan.
8. Anna **Aloitusaika**-kentässä arvoksi **16.00**.
9. Valitse **Määritä tilaksi valmis** -toiminto.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Siirrä nimikkeet nimikkeiden uudelleenluokituspäiväkirjan avulla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeen uudell.luokit. pvk:t** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät **Nimik. uud.luok.pvk** -sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Anna **Sijaintikoodi**-kentässä sijainti, jossa nimikkeet ovat varastoituna.

    > [!NOTE]  
    > Jos siirrettävillä nimikkeillä ei ole sijainkoodia, jätä **Sijaintikoodi**-kenttä tyhjäksi.
4. Anna **Uusi sijaintikoodi** -kenttään sijainti, johon haluat siirtää nimikkeet.
5. Valitse **Kirjaa**-toiminto.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="undo-a-transfer-shipment"></a>Peruuta siirtotoimitus

Jos kirjatun siirtotilauksen määrässä on virhe, niin kauan kuin toimitusta ei ole vastaanotettu, määrä on helppo korjata. **Kirjattu siirtotoimitus** -sivulla **Peruuta toimitus** -toiminto luo korjausrivejä seuraavasti:

* **Toimitettu määrä** -kentän arvo laskee kumotulla määrällä.
* **Toimitettava määrä** -kentän arvo nousee kumotulla määrällä.
* **Korjaus**-valintaruutu valitaan riveille.

Jos määrä toimitettiin fyysisen varastoinnin toimituksena, korjaava rivi luodaan kirjattuun fyysisen varastoinnin toimitukseen.

Viimeistele korjaus avaamalla siirtotilaus, antamalla oikea määrä ja kirjaamalla tilaus. Jos tilaus on toimitettu fyysisen varastoinnin toimituksen kautta, uusi fyysisen varastoinnin toimitus luodaan ja kirjataan.

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/transfer-items/)

## <a name="see-also"></a>Katso myös

[Varaston hallinta](inventory-manage-inventory.md)  
[Sijaintien määrittäminen](inventory-how-setup-locations.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
