---
title: Tietueen käytön rajoittaminen ja salliminen
description: 'Jos haluat rajoittaa tietueen käyttöä, voit sisällyttää kaksi työnkulun vastausta työnkulkuun, joka määrittää tietueen käyttöä.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Tietueen käytön rajoittaminen ja salliminen

Jos haluat rajoittaa tietueen käyttöä tietyissä aktiviteeteissa, esimerkiksi ennen kuin tietue on hyväksytty, voit sisällyttää kaksi työnkulun vastausta työnkulkuun, joka määrittää tietueen käyttöä. Yksi työnkulku vastaus rajoittaa tietueen käyttöä työnkulun tapahtuman ja ehtojen mukaan. Toinen työnkulku vastaus sallii tietueen käyttöä työnkulun tapahtuman ja ehtojen mukaan. Tuotteen [!INCLUDE[prod_short](includes/prod_short.md)] oletusversiossa on kaksi vastausta tähän tarkoitukseen: **Lisää tietuerajoitus** ja **Poista tietuerajoitus**.

> [!NOTE]  
> Tuotteen [!INCLUDE[prod_short](includes/prod_short.md)] oletusversio tarjoaa tuen tietueen rajoittamiselle kirjaamisen, viennin maksuna ja tulostamisen sekkinä osalta. Muita rajoituksia saadaan, jos Microsoft-kumppani mukauttaa sovelluksen koodin.  

> [!NOTE]  
> Työnkulun toiminnallisuus rajoittaa ja sallia tietueita käytettäväksi työnkulun toimintoihin ei liity toiminnallisuuteen estää nimike, asiakas ja toimittajatietueiden kirjaaminen.

Seuraavassa kuvataan, miten rajoittaa ostotilausten kirjaamisen ennen kuin ne on hyväksytty. Uusi työnkulku perustuu *Ostolaskun hyväksymistyönkulku* -malliin.  

## Voit seuraavasti luoda työnkulun vaiheen, joka rajoittaa hyväksymättömien ostotilausten kirjauksia

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut**, valitse sitten vastaava linkki.  
2. Valitse **Työnkulut**-sivulla **Uusi työnkulku mallista** -toiminto. Lisätietoja kohdassa [Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md).
3. Valitse **Työnkulkumallit** sivulla *Ostolaskun hyväksymistyönkulku* -malli.  

   Huomaa, että kaksi ensimmäistä työnkulun vaihetta ovat rajoittaminen ja sitten ostolaskujen käytön salliminen. Muuta uuden työnkulun ensimmäisen vaiheen tapahtumaehtoa niin, että se koskee ostotilauksia.  
4. Valitse **Työnkulun vaiheet** -pikavälilehdessä **Ehto** -kenttä ensimmäiselle vaiheelle, valitse sitten **Asiakirjan tyyppi** -suodattimeksi **Tilaus**.  
5. Siirry muokkaamaan, poistamaan tai lisäämään muita työnkulun vaiheita kuvataksesi liiketoiminnan prosessia, joka alkaa rajoittamalla hyväksymättömien ostotilausten kirjaamista.  

## Katso myös

[Hyväksymistyönkulkujen käyttäminen](across-use-workflows.md)  
[Luo hyväksymistyönkulut](across-how-to-create-workflows.md)  
[Työnkulku](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
