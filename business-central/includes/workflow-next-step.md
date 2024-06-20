---
author: brentholtorf
ms.topic: include
ms.date: 03/27/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

> [!IMPORTANT]
> Kun työnkulun osavaiheen kun-tapahtumaa muutetaan, myös sitten-vastaukset muuttuvat. Joskus muiden kun-tapahtumien sitten-vastaukset viittaavat näiden sitten-vastauksiin työnkulun seuraavana osavaiheena. Kun-tapahtuman muuttamisen jälkeen on varmistettava, että sen sitten-tapahtumien seuraavat osavaiheet ovat oikein.  
>
> Esimerkiksi **Toimittajan hyväksymistyönkulku** -työnkulkumallissa on ensisijainen kun-tapahtuma **Toimittajan hyväksyntää on pyydetty**. Tällä kun-tapahtumalla on **Lähetä tietueen hyväksymispyyntö ja luo ilmoitus** -sitten-vastaus, johon muut sitten-vastaukset viittaavat. Jos ensisijainen kun-tapahtuma **Toimittajan hyväksyntää on pyydetty** vaihdetaan esimerkiksi tapahtumaksi **Toimittajatietue on muuttunut**, sitten-vastaus tyhjennetään viitteiden ohella.
>
> **Hyväksymispyyntö on delegoitu**- ja **Hyväksymispyyntö on hyväksytty** -kun-tapahtumien (joissa **Ehto** **Odottavat hyväksynnät:>0**) sitten-vastaukset ovat esimerkkejä, joissa ensisijaisen kun-tapahtuman muuttaminen voi aiheuttaa ongelmia. Niiden sitten-vastauksissa on seuraava vaihe, joka viittaa **Toimittajan hyväksyntää on pyydetty** -kun-tapahtuman **Lähetä tietueen hyväksymispyyntö ja luo ilmoitus** -sitten-vastaukseen. Koska **Toimittajan hyväksyntää on pyydetty** -kun-tapahtuman sitten-vastaus ei ole enää käytettävissä, sisennetyt kun-tapahtumat eivät toimi odotetusti.
>
> Muuttuneeseen kun-tapahtumaan viittaavien kun-tapahtumien sitten-vastausten seuraavat osavaiheet on määritettävä.