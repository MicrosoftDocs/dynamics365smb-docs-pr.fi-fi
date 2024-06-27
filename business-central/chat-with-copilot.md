---
title: Keskustelu Copilotin avulla (esiversio)
description: Tietoja tietojen etsimisestä ja ohjeiden saamisesta Business Centralissa käyttämällä keskustelua Copilotin avulla.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/13/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
  - get-started
---

# <a name="chat-with-copilot-preview"></a>Keskustelu Copilotin avulla (esiversio)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Tässä artikkelissa käsitellään yrityksen tietoja koskevien vastauksen saamista käyttämällä keskustelua Copilotin kanssa samoin kuin apua, jota saadaan Business Centraliin liittyvien tehtävien ja aihealueiden osalta.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="about-chat-with-copilot"></a>Tietoja keskustelusta Copilotin avulla

Microsoft Copilot on tekoälypohjainen avustaja, joka inspiroi toimimaan luovasti, tehostaa tuottavuutta ja poistaa tarpeen tehdä pitkäveteisiä tehtäviä. Keskustelemalla Copilotin avulla Business Centralissa, voit kysyä kysymyksiä ja saada vastauksia luonnollisella kielellä. Toimi näin:

- Yrityksen liiketoimintatietojen etsiminen Business Centralissa. Keskustelun avulla voi hakea (ja avata) liiketoimintaprosesseihin liittyviä yksiköitä tai tietueita, kuten asiakkaita, toimittajia, myyntitilauksia ja nimikkeitä, koskevia tietoja. Copilotia voi esimerkiksi pyytää näyttämään uusimmat Adatumin myyntitilaukset.
- Tutustu erilaisiin tehtäviin liittyviin selityksiin ja vaiheittaisiin ohjeisiin. Voidaan esimerkiksi pyytää auttamaan ymmärtämään dimensioita tai kertomaan, miten myyntitilaus kirjataan.
- Yksittäisten kenttien tarkoituksen ja tyyppisen käyttötavan ymmärtäminen. Kun kentän työkaluvihjeessä valitaan **Kysy Copilotilta**, avautuvassa keskustelussa kentän nimen selityskehote, ja Copilot antaa siitä lisätietoja. Copilot muodostaa linkin viitattuihin artikkeleihin, joten kuvaus on helppo vahvistaa.

Copilotin lähdevastaukset virallisista tiedoista, jotka ovat saatavilla Microsoft Learnissa [Dynamics 365 Business Centralin dokumentaatiosta](/dynamics365/business-central/).
  
Copilotin kanssa käydyn keskustelun käyttäminen virtaviivaistaa työnkulkua ohittamalla perinteiset siirtymis- ja tuoteohjeet.
  
> [Katso video](https://go.microsoft.com/fwlink/?linkid=2250609)

## <a name="prerequisites"></a>Vaatimukset

- Varmista, että järjestelmänvalvoja on aktivoinut keskustelutoiminnon Copilotissa. [Lisätietoja Copilotin ja tekoälyn ominaisuuksien määrittämisestä](enable-ai.md).
- Määritä Business Centralin näyttökieleksi jokin seuraavista englannin kielialueista: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Lisätietoja kielen vaihtamisesta](ui-change-basic-settings.md#language).
- Varmista, että Business Central -ympäristösi on jossain muussa maassa tai muulla alueella kuin Kanadassa. (Tämä ominaisuus ei ole vielä saatavana Kanadassa.)

## <a name="get-started-using-chat-with-copilot"></a>Keskustelun Copilotin avulla aloittaminen

1. Valitse näytön oikeassa yläkulmassa ![Näkyvissä Keskustelu Copilotin avulla -kuvake](media/chat-copilot-icon.png) **Copilot**-kuvake ![Näkyvissä selite numero 1](media/callout-number-1.svg).

   **Copilot**-ruutu näkyy kuvassa näkyvällä tavalla:
   
    ![Näkyvissä Keskustelu Copilotin avulla -kuvake ja selitteet](media/chat-with-copilot-pane.svg)

1. Kirjoita kysymys alareunan **Kysy kysymys** -ruutuun ![Näkyvissä selitenumero 2](media/callout-number-2.svg) ja saat sitten vastauksen valitsemalla nuolen tai painamalla <kbd>Enter</kbd>-näppäintä.

   Syötteesi eli *kehote* voi olla kysymys, ilmoitus tai komento.

   > [!TIP]
   > Copilotissa on muuta kysymysten kirjoittamista helpottava ominaisuus:
   > - Kysymyksen muotoilua auttaa, jos valitset jonkin kehoteoppaan, joita ovat **Etsi**, **Selitä** tai **Opas**. Ne ovat valittavissa ruudun yläreunassa ![Näkyvissä selitenumero 3](media/callout-number-3.svg) tai ![Näkyvissä kehoteopaskuvake](media/prompt-guide-icon.png) **Näytä kehotteet** -kuvakkeessa **Kysy kysymys** -ruudun ![Näkyvissä selitenumero 4](media/callout-number-4.svg) yläpuolella. Kehoteoppaat ovat esimääritettyjä lyhyitä lauseita, jotka aloittavat kysymyksen tai kehotteen. Ne säästävät aikaa, ohjaavat Copilotin vastauksia kohti vastausluokkia ja auttavat sinua oppimaan muotoilemaan kysymyksiä, jotta saat parhaat vastaukset.
   > - Valitsemalla kehote-ehdotuksia **Näytä kehotteet** -painikkeen ![Näkyvissä selitenumero 5](media/callout-number-5.svg) yläpuolelta kysytään automaattisesti esimääritetty kysymys, jolla saadaan tietoja kysymysten ja vastausten toiminnasta. Kehote-ehdotukset ovat saatavana vain käytettäessä CRONUS-esittely-yritystä.

1. Tarkista Copilot-ruudussa näkyvät vastaukset ![Näkyvissä selitenumero 6](media/callout-number-6.svg).

   Kysymyksen mukaan vastaus voi sisältää tekstiä, linkkejä Business Centralin tietueisiin tai sivuille sekä linkkejä Business Centralin ohjeartikkeleihin Microsoft Learnissa.

1. Tarkenna vastausta kysymällä uusi kysymys.

   Keskustelu muistaa kontekstin, joten alkuperäisen kysymyksen keskeisiä kohtia ei tarvitse toistaa.

## <a name="clear-chat-to-start-over"></a>Alusta aloittaminen tyhjentämällä keskustelu

Keskustelussa Copilotin avulla voidaan siirtyä toiseen aiheeseen valitsemalla ![Näkyvissä keskustelun tyhjennyskuvake](media/clear-chat-icon.png) **Aloita uusi Copilot-keskusteluistunto** -kuvake Copilot-ruudun alaosassa kysymysruudun yläpuolella. Tämä toiminto tyhjentää viimeisimmät viestit Copilotin muistista. Alusta aloittaminen on usein kätevää, jos pitkässä keskustelussa on ollut paljon viestejä. Se voi myös auttaa Copilot antamaan tarkempia vastauksia.

Keskustelu tyhjennetään myös silloin, jos Business Central suljetaan tai siitä kirjaudutaan ulos.

## <a name="tips-for-better-questions"></a>Vinkkejä parempiin kysymyksiin

Tässä on muutamia keinoja, joilla voi parantaa Copilotin antamia vastauksia:

- Kysy selkeitä ja täsmällisiä kysymyksiä.
- Käytä lyhyitä lauseita pitkien tai useiden lauseiden sijaan.
- Kysy yksi kysymys kerrallaan. <!--Avoid asking about multiple questions in one message.-->
- Käytä luonnollista kieltä sekä esitä kysymykset ystävällisesti ja keskustelunomaisesti.
- Käytä avainsanoja, fraaseja ja termejä, joiden tiedät olevan käytössä Business Central -sovelluksessa tai -ohjeissa.
- Jos ensimmäisen vastaus ei vastaa täysin kysymyksiin, esitä lisäkysymyksiä tai muotoilu viimeisin kysymys uudelleen.
- Jos kysymys koskee eri aihealuetta kuin edellinen kysymys, aloita alusta tyhjentämällä nykyinen keskusteluistunto.

## <a name="example-prompts"></a>Esimerkkikehotteita

Copilotille esitettävät kysymykset vaihtelevat roolin, nykyisen tehtävän, organisaation käyttämien prosessien ja oman ilmaisutavan mukaan. Seuraavat esimerkit osoittavat erilaisia tapoja esittää kysymyksiä keskusteluruudussa. Niistä voi olla apua omien kysymysten kirjottamiseen omassa tilanteessa.

Kehote: `Find the Item with Description 'ATHENS Desk'`

Tässä esimerkissä Copilotille annetaan selkeät ohjeet paikantaa yksi tietue. Siinä esimerkiksi vihjataan, että tietue löytyy nimikeluettelosta. Siinä ilmaistaan lainausmerkkien ja oikean isojen kirjaimen käytön avulla, että kuvauskentässä on oltava tietty teksti. Copilot vastaa yleensä tarkasti, kun annetut vihjeet ovat tarkkoja. Myös arkikielen käyttö on mahdollista, kuten seuraavassa esimerkissä.

Kehote: `Give me the latest invoice for adatum`

Tässä esimerkissä Copilotia pyydetään paikantamaan tietue, mutta kysymys ei ole niin tarkka, joten myöskään vastaus ei ole yhtä tarkka. Copilot pystyy usein ymmärtämään tai arvaamaan, että etsittävä lasku ei ole ostotilaus vaan myyntitilaus Kirjattu myyntitilaus -luettelossa. Copilotin on myös kohdistettava `adatum` ja `Adatum Corporation`, sillä se on laskuun liitetyn tilausasiakkaan tarkka koko nimi.

Kehote: `Show me customer ledger entries for Adatum from about three weeks ago`

Tässä esimerkissä Copilotia pyydetään ratkaisemaan yleinen päivämäärähaaste, joka yleensä edellyttää kalenterin avaamista viitteeksi tai edistyneiden päivämääräsuodattimen käyttöä. Copilot ymmärtää yleensä yleiset ilmaiset ja yritystermit.

Kehote: `How does I save my filterrings for later?`

Tässä esimerkissä Copilotilta pyydetään ohjeita jonkin tehtävän suorittamiseen Business Centralissa. Copilot ymmärtää yleensä kysymyksen tarkoituksen, vaikka siinä olisi kielioppi- tai oikeinkirjoitusvirheitä taikka lyhenteitä.

## <a name="provide-feedback-on-answers"></a>Anna vastauksiin palautetta

Copilotin vastauksia voidaan arvioida käyttämällä tykkää (peukku ylös) -painiketta, jos arvio on hyvä, tai ei tykkää (peukku alas) -painiketta, jos arvio on huono. Ei tykkää -painikkeen valinnan yhteydessä voidaan valita syy, kuten epätarkka, epäsopiva tai muu. Nämä tiedot voivat auttaa parantamaan ehdotuksia.

<!--
1. If you want help getting you're question started, select the prompts either from the **Find**, **Explain**, or **Guide** buttons at the top of the Coplit pane or use the **View Prompts** menu above **Ask a question** box at the bottom.

   Prompts are predefined short phrases that start a question. Apart from saving you time, they're designed to target responses to specific categories. They also help you undestand how you can phrase questions to get the responses.-->
   
## <a name="see-also"></a>Katso myös

- [Copilot- ja tekoälyominaisuuksien vianmääritys](ai-copilot-troubleshooting.md)  
- [Copilot- ja tekoälyominaisuuksien määrittäminen](enable-ai.md)  
- [Vastuullisen tekoälyn usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla](faqs-chat-with-copilot.md)  
- [Business Centralin ohjeresurssit](product-help-and-support.md)  
