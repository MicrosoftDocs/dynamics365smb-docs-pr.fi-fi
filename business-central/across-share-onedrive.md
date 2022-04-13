---
title: Business Central-tiedostojen avaaminen OneDrivessa
description: Lue, miten voit jakaa Business Central -tietoja OneDrive for Businessin kautta.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 2e1cc04d265541c87244dcd6c13b14327f07cc2f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516419"
---
# <a name="opening-and-sharing-business-central-files-in-onedrive"></a>Business Central-tiedostojen avaaminen ja jakaminen OneDrivessa

[!INCLUDE[prod_short](includes/prod_short.md)]in avulla on helppo tallentaa, hallita ja jakaa tiedostoja muiden ihmisten kanssa OneDrive for Businessin kautta. Useimmilla sivuilla, joilla on saatavilla tiedostoja, kuten raportin Saapuneet-kansio tai tiedostot, jotka on liitetty tietueisiin, löydät **Avaa OneDrivessa**- ja **Jaa**-toiminnon.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Raporttien Avaa OneDrivessa- ja Jaa-toiminnot":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Liitteiden Avaa OneDrivessa- ja Jaa-toiminnot":::

<!--
:::image type="content" source="media/Open in OneDrive.PNG" alt-text="The Open in OneDrive action":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Share file attachments in OneDrive":::
-->

## <a name="open-in-onedrive"></a>Avaa OneDrivessa

**Avaa OneDrivessa** -toiminto kopioi tiedoston OneDriveen ja avaa tiedoston online-sovelluksissa, kuten Excel Online, Word Online tai PowerPoint Online. 

<!--## Working with Different Types of Files-->

Kun valitset **Avaa OneDrivessa**, [!INCLUDE[prod_short](includes/prod_short.md)] tunnistaa Excel-, Word-ja PowerPoint-tiedostot ja ne avataan online-sovelluksissa eli Excel onlinessa, Word onlinessa tai PowerPoint onlinessa. Voit lisätä huomautuksia, muokata ja tehdä yhteistyötä muiden kanssa poistumatta selaimesta.

Muita suosittuja tiedostotyyppejä, kuten PDF-tiedostoja, tekstitiedostoja ja kuvia, varten OneDrive tarjoaa tiedostojen katselijat, jotka tarjoavat ominaisuuksia esimerkiksi tulostamiseen ja jakamiseen. Jos tiedostoa ei voi tarkastella OneDrivessa , sinua saatetaan pyytää lataamaan se.

## <a name="share"></a>Osuus

**Jaa**-toiminto kopioi tiedoston OneDriveen ja antaa sinun jakaa tiedoston muiden käyttäjien kanssa ja nähdä, kenen kanssa olet jo jakanut tiedoston. Kun valitset **Jaa**-toiminnon, seuraava sivu avautuu.

:::image type="content" source="media/share-to-onedrive-dialog.PNG" alt-text="Jaa tiedosto OneDrivessa":::

Jos olet perehtynyt OneDriveen, saatat tunnistaa sivun. Tiedoston jakamiseen on kaksi vaihtoehtoa: **Lähetä linkki** ja **Kopioi linkki**.

- **Lähetä linkki** -toiminnolla voit jakaa tiedostoja tiettyjen ihmisten kanssa. Tiedoston jakoa käyttävät henkilöt saavat sähköpostiviestin, jossa on linkki tiedostoon. Tiedosto näkyy myös heidän **Jaetut**-osassaan OneDrivessa. Aloita kirjoittamalla sähköpostiosoitteet tai kontaktien nimet **Nimi, ryhmä tai sähköposti** -kenttään.

- **Kopioi linkki** kopioi linkin tiedostoon OneDrivessa, jotta voit käyttää linkkiä muissa paikoissa, kuten Facebook, Twitter tai sähköposti. 

Ennen kuin lähetät tai kopioit linkin, määritä tiedoston käyttöoikeus, jonka haluat käyttäjillä olevan. Voit tarkastella nykyistä asetusta **Lähetä linkki**- ja **Kopioi linkki** -kohtien alla. Useimmissa tapauksissa se on asetus **Linkin voi avata kuka tahansa, jolla on linkki** järjestelmänvalvojan määrittämien asetusten mukaan. Voit muuttaa käyttö oikeuksia valitsemalla linkin ja muuttamalla **Linkin asetukset** -sivua.

Business Centralin jakamistoiminto perustuu OneDriveen. Lisätietoja jakamisesta ja käyttöoikeuksista on siis ohjeaiheessa [Tiedostojen ja kansioiden jakaminen OneDrivessa](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> **Jaa**-toiminto ei ole käytettävissä mobiililaitteiden Business Central -sovelluksessa.

## <a name="first-time-sign-in-from-business-central"></a>Ensimmäisen kerran kirjautuminen Business Centralista

Kun käytät **Avaa OneDrivessa**- tai **Jaa**-toimintoa ensimmäistä kertaa, [!INCLUDE[prod_short](includes/prod_short.md)] tekee seuraavat toimet:

1. Avaa **Tarkista ehdot** -sivun. Lue sivu, ja jos hyväksyt käyttöehdot, jatka valitsemalla **Hyväksy**.
2. Avaa **Valitse tili** -sivun. Valitse tilisi tai **käytä toista tiliä**, jos et näe omaa, ja syötä sitten pyydettäessä käyttäjänimi ja salasana.
3. Luo OneDriveen kansion nimeltä [!INCLUDE[prod_short](includes/prod_short.md)]. 
4. [!INCLUDE[prod_short](includes/prod_short.md)] -kansiossa se luo toisen kansion, jolla on sama nimi kuin käsiteltävällä yrityksellä. Jos työskentelet useammassa kuin yhdessä yrityksessä, ohjelma luo sen yrityksen kansion, jota käsittelet, kun käytät **Avaa OneDrivessa**- tai **Jaa**-toimintoa. 
5. Tuo kansioon kopion valitusta tiedostosta ja avaa tiedoston. Kun seuraavan kerran käytät toimintoa, se vain kopioi ja avaa tiedoston. 

## <a name="managing-multiple-copies-of-a-file"></a>Tiedoston useiden kopioiden hallinta

Kun valitset **Avaa OneDrivessa** tai **Jaa**, tiedosto kopioidaan [!INCLUDE[prod_short](includes/prod_short.md)]ista OneDrive-kansioon. Jos muokkaat tiedostoa OneDrivessa, tiedoston kopiot ovat erilaiset. Voit päivittää [!INCLUDE[prod_short](includes/prod_short.md)]iin uusimman tiedoston poistamalla aiemmin luodun tiedoston [!INCLUDE[prod_short](includes/prod_short.md)]ista ja lataamalla sitten uusimman kopion.

Lisäksi kun samanniminen tiedosto on jo olemassa OneDrivessa, [!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa valinnan joko korvata tiedoston tai säilyttää molemmat tiedostot. Jos haluat säilyttää molemmat tiedostot, uusi tiedosto kopioidaan OneDriveen ja antaa tiedostonimen, jossa on lisänumero (esimerkiksi "Nimikkeet (2).xlsx"). Alkuperäistä tiedostoa ei muuteta. 

Jos valitset tiedoston korvaamisen, uusi tiedosto lisätään kyseisen tiedoston versiohistoriaan. Alkuperäistä tiedostoa ei ole menetetty, ja voit tarkastella tai palauttaa tiedoston aiempia versioita. 

## <a name="about-your-business-central-folder-on-onedrive"></a>Tietoja Business Central-kansiosta OneDrivessa

Kansio ja sen sisältö ovat yksityisiä, kunnes päätät jakaa ne muiden kanssa. Voit esimerkiksi päättää jakaa sisältöä yhden tai useamman työtoverisi tai jopa organisaatiosi ulkopuolisen henkilön kanssa. Voit käyttää OneDrivea **Omat asetukset** -sivulta valitsemalla linkin **Pilvitallennustila**-kentässä. Lisätietoja on artikkelissa [OneDrive-tiedostojen ja -kansioiden jakaminen](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Pilvitallennustila-kenttä Omat asetukset-kohdassa":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a>Katso myös
[Business Centralin ja OneDriven integraatio](across-onedrive-overview.md)  
[OneDriven ja Business Centralin integroinnin hallinta](admin-onedrive-integration.md)  
[OneDrive – usein kysytyt kysymykset](admin-onedrive-faq.md)