---
title: 'Shekkien myöntäminen, tulostaminen, peruuttaminen ja mitätöiminen'
description: 'Tässä ohjeaiheessa kerrotaan, miten sekit myönnetään maksupäiväkirjan avulla, tulostetaan ja mitätöidään tai miten sekkitapahtumia tarkastellaan Business Central -sovelluksessa.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'payment journal, print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256, 404,'
ms.date: 05/07/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Sekkimaksujen suorittaminen

Voit myöntää sähköisiä ja manuaalisia sekkejä [!INCLUDE[prod_short](includes/prod_short.md)]issa. Molemmissa menetelmissä sekit myönnetään toimittajille maksupäiväkirjaa käyttäen. Ohjelman avulla voit myös mitätöidä sekkejä ja tarkastella sekkitapahtumia.

Seuraavassa kuvataan, miten voit maksaa toimittajalle tietokonesekillä kohdistamalla maksun asianmukaiseen toimittajalaskuun, tulostamalla sekin ja kirjaamalla maksun maksetuksi. Näin saadaan positiivinen toimittajatapahtuma, joka kohdistetaan negatiiviseen pankkitilitapahtumaan sekä fyysinen sekki pankin käsittelyä varten.

Voit maksaa kahdella eri tyyppisellä sekillä. Molemmissa tyypeissä **Vastatilin tyyppi**- tai **Tilityyppi** -kentässä täytyy olla **Pankkitili**.

- **Tietokonesekki**: Valitse tämä vaihtoehto, jos haluat tulostaa sekin maksupäiväkirjan tällä rivillä olevalle summalle. Tulosta sekit, ennen kuin kirjaat päiväkirjan rivit.
- **Manuaalinen sekki**: Valitse tämä vaihtoehto, jos olet luonut sekin manuaalisesti ja haluat luoda vastaavan sekkitapahtuman tälle summalle. Tämän vaihtoehdon avulla et voi tulostaa sekkiä.

> [!NOTE]  
> Voit varmistaa lähettämällä toimittaja-, sekki- ja maksutiedot sisältävän tiedoston, että pankki vahvistaa vain tarkistetut sekit ja summat. Lisätietoja on kohdassa [Positive Pay -tiedostojen vieminen](finance-how-positive-pay.md).

> [!IMPORTANT]
> Tulostin on määritettävä oikein sekkimuotoja varten. Myös käytettävä sekkien asettelu on määritettävä. Lisätietoja on kohdassa [Sekin asettelun valitseminen](finance-how-define-check-layouts.md). Vaihtoehtoisesti sekki voidaan lähettää esimerkiksi PDF-tiedostona.  

Voit tulostaa sivulle enintään 10 laskua sekin talonkia kohti. Jos sekki koskee yli 10 laskua, sekki mitätöidään talongin tulostuksen yhteydessä ensimmäisellä sivulla ja sekkiin tulostetaan sana MITÄTÖITY. Tämän jälkeen toiselle sivulle tulostetaan loput laskut ja sekin kokonaissumma.

## Maksaaksesi toimittajalaskun tietokonesekillä

Seuraavassa kuvataan, miten toimittajalle maksetaan sekillä. Vaiheet ovat samankaltaiset kuin hyvitettäessä asiakkaalle sekkimaksuna.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten vastaava linkki.
2. Täytä maksupäiväkirjan rivit. Lisätietoja on ohjeaiheessa [Maksujen ja hyvitysten kirjaaminen](payables-how-post-payments-refunds.md).
3. Valitse **Maksutavan koodi** -kentässä **Sekki**.
4. Valitse **Pankkimaksun tyyppi** -kentässä **Tietokonesekki**.
5. Valitse **Tulosta sekki** -toiminto.
6. Täytä **Sekki**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Jos tulostin on määritetty tulostamaan sekkejä, valitse **Tulosta**-painike. Valitse muussa tapauksessa ensin **Lähetä kohteeseen** -painike, sitten **PDF-tiedosto**-asetus, lopuksi **OK**-painike ja tulosta PDF-tiedosto sitten.

    Fyysiset sekit voidaan nyt lähettää toimittajille käsiteltäviksi. Jatka maksun kirjaamiseen kohdistuksen mukaan toimittajalle ja maksun suorittamiseksi järjestelmässä.
8. Valitse **Kirjaa**-toiminto.

Täysin kohdistetut toimittajatapahtumat ja pankkitilitapahtumat luodaan.

> [!NOTE]  
> Jos sekkejä täytyy tulostaa ja maksaa monessa valuutassa eri pankkitileiltä, sinun täytyy suorittaa **Tulosta sekki** -eräajo erikseen kullekin valuutalle ja määrittää sopivat pankkitilit.

## Kirjaamattomien ja tulostettujen sekkien peruuttaminen

Voit peruuttaa kirjaamattomat sekit niiden tulostamisen jälkeen **Maksupäiväkirja**-sivun **Mitätöi sekki** -toiminnon avulla.

1. Valitse **Maksupäiväkirja**-sivulla **Mitätöi sekki** ja valitse peruutettavat sekit.

## Sekkien mitätöiminen

Kun sekkimaksu on kirjattu, voit peruuttaa (mitätöidä) sekit vain tuloksena syntyvistä pankkitapahtumista.

> [!IMPORTANT]
> Jos sekkiä käytetään laskussa, poista sekin käyttö ensin, jotta lasku voidaan maksaa uudelleen ja mitätöi sekki sitten. Jos sekki tulostettiin eikä laskua maksettu sillä, valitse siinä tapauksessa **Mitätöi vain sekki** tässä osassa kuvatulla tavalla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.
2. Valitse oikea pankkitili, valitse **Muokkaa**-toiminto ja valitse sitten **Sekkitapahtumat**-toiminto.
3. Valitse **Sekkitapahtumat**-sivulla **Mitätöi sekki** -toiminto.
4. Valitse **Mitätöi vain sekki** -valintaruutu.
5. Valitse **OK**-painike.

## Voit tarkastella kirjattujen sekkien yhteenvetoa

Jos haluat tarkistaa kirjatuttuja sekkejä, esimerkiksi yhdelle toimittajalle maksetut useat sekit, voit käyttää **Pankkitili – sekin tiedot** -raporttia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitili - sekin tiedot** ja valitse sitten vastaava linkki.
2. Aseta haluamasi suodattimet ja valitse sitten **Esikatselu**-painike.

## Katso myös

[Maksujen suorittaminen](payables-make-payments.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Positive Pay -tiedoston vienti](finance-how-positive-pay.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
