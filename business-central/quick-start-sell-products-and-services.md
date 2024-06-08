---
title: Myynnin pika-aloitus (sisältää videon)
description: 'Opettele täyttämään ensimmäiset kriittiset kentät, jotka koskevat tuotteita ja asiakkaita Business Centralissa, jotta voit aloittaa myyntiprosessisi.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: quickstart
ms.date: 09/29/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="sales-quick-start"></a>Myynnin pika-aloitus

Jotta voisit myydä tuotteita ja palveluita, sinun täytyy ensin määrittää nimikkeet ja asiakkaat. Kun tämä on tehty, voit aloittaa myyntitilausten rekisteröimisen ja laskujen lähettämisen.

## <a name="set-up-items-to-sell"></a>Myytävien nimikkeiden määrittäminen

Tämä video näyttää, miten nimikkeen voi määrittää myytäväksi [!INCLUDE[prod_short](includes/prod_short.md)]issa.

<br>

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE47eLx?rel=0]

### <a name="set-up-a-new-item"></a>Määritä uusi nimike

[!INCLUDE[create_new_item](includes/create_new_item.md)]

Lisätietoja ja muita asioita, joita voit tehdä nimikkeitä määritettäessä, on ohjeaiheessa [Uusien nimikkeiden rekisteröinti](inventory-how-register-new-items.md).  

## <a name="set-up-customers"></a>Asiakkaiden määrittäminen

Tässä videossa näkyy, miten uusi asiakas määritetään [!INCLUDE[prod_short](includes/prod_short.md)]issa.  

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

### <a name="set-up-a-new-customer"></a>Uuden asiakkaan määrittäminen

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Lisätietoja ja muita asioita, joita voit tehdä asiakkaita määritettäessä, on ohjeaiheessa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).

## <a name="create-a-sales-order"></a>Luo myyntitilaus

Kun myyt jotain asiakkaalle, sinulla on kaksi vaihtoehtoa. Ensimmäinen ja yksinkertaisin on vain myyntilaskun luominen. Jos myyntiprosessi on kuitenkin monimutkaisempi, esimerkiksi jos sinulla on tilanteita, joissa toimitat vain tilausmäärän osia, käytä myyntitilausta.

### <a name="to-create-a-sales-order"></a>Myyntitilauksen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 10.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.
2. Luo uusi merkintä valitsemalla **Uusi**.
3. Syötä **Asiakas**-kenttään nykyisen asiakkaan nimi.

    Muut **Myyntitilaus**-sivun kentät täytetään nyt valitun asiakkaan vakiotiedoilla.  

4. Täytä tarvittaessa jäljellä olevat kentät **Myyntitilaus**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä sen tuotteen, kulun tai tapahtuman tyyppi, jonka kirjaat myyntirivin asiakkaalle.

6. Valitse **Nro**-kenttään varastonimikkeen tai palvelun numero.

7. Syötä myytävien nimikkeiden lukumäärä **Määrä**-kenttään.

8. Syötä **Rivialennus-%**-kenttään prosentti, jos haluat myöntää asiakkaalle alennuksen tuotteesta.

9. Voit lisätä tilausriviä koskevan huomautuksen, jonka asiakas näkee tulostetussa myyntitilauksessa, kirjoittamalla kommentin **Kuvaus**-kentän tyhjälle riville.

10. Toista vaiheet 5–9 jokaiselle nimikkeelle, jonka haluat myydä asiakkaalle.

11. Jos haluat toimittaa osan tilausmäärästä, syötä määrä **Toimitettava määrä** -kenttään. Arvo kopioidaan **Laskutettava määrä** -kenttään.

12. Jos haluat laskuttaa osan toimitettavasta määrästä, syötä kyseinen määrä **Laskutettava määrä** -kenttään. Määrän on oltava pienempi kuin **Toimitettava määrä** -kentän arvo.

13. Kun myyntitilausrivit ovat valmiit, valitse **Kirjaa ja lähetä** -toiminto.

Lisätietoja ja muita asioita, joita voit tehdä asiakkaan myyntitilausten luonnin yhteydessä, on kohdassa [Tuotteiden myyminen asiakkaan myyntitilauksen avulla](sales-how-sell-products.md).  

## <a name="create-a-sales-invoice"></a>Luo myyntilasku

Kun luot ja kirjaat myyntilaskun, et luo vain asiakkaalle lähetettävää laskuasiakirjaa vaan luot myös liittyvät määrä- ja arvotapahtumat [!INCLUDE[prod_short](includes/prod_short.md)]issa.

### <a name="to-create-and-post-a-sales-invoice"></a>Luo ja kirjaa myyntilasku seuraavasti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 20.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut** ja valitse sitten vastaava linkki.  

2. Luo uusi merkintä valitsemalla **Uusi**.

3. Syötä **Asiakas**-kenttään nykyisen asiakkaan nimi.

4. Täytä tarvittaessa jäljellä olevat kentät **Myyntilasku**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. Valitse **Rivit**-pikavälilehden **Tyyppi**-kentässä sen tuotteen, kulun tai tapahtuman tyyppi, jonka kirjaat myyntirivin asiakkaalle.

6. Valitse **Nro**-kenttään kirjattava tietue **Tyyppi**-kentän arvon mukaan.

7. Ilmoita **Määrä**-kentässä, kuinka monta tuote-, kulu- tai tapahtumayksikköä rivi kirjaa asiakkaalle.  

8. Jos haluat antaa alennuksen, anna prosentti **Rivialennus-%**-kentässä. **Rivisumma**-kentän arvo päivittyy vastaavasti.  

9. Toista vaiheet 5–8 jokaiselle tuotteelle tai kululle, jonka haluat laskuttaa asiakkaalta.  

10. Syötä **Laskun alennussumma** -kenttään summa, joka vähennetään **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

11. Kun myyntilaskun rivit ovat valmiit, valitse **Kirjaa ja lähetä** -toiminto.  

Lisätietoja ja muita asioita, joita voit tehdä asiakkaan myyntilaskun luonnin yhteydessä, on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md)

## <a name="see-also"></a>Katso myös

[Business Centralin pika-aloitus](quick-start-business-central.md)  
[Myynnin yleiskatsaus](sales-manage-sales.md)  
[Tuotteiden myyminen asiakkaan myyntitilauksen avulla](sales-how-sell-products.md)  
[Myynnin laskutus](sales-how-invoice-sales.md)  
