---
title: Keskustelu Copilotin avulla (esiversio)
description: Tietoja tietojen etsimisestä ja ohjeiden saamisesta Business Centralissa käyttämällä keskustelua Copilotin avulla.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/18/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
  - get-started
---

# Keskustelu Copilotin avulla (esiversio)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Tässä artikkelissa käsitellään yrityksen tietoja koskevien vastauksen saamista käyttämällä keskustelua Copilotin kanssa samoin kuin apua, jota saadaan Business Centraliin liittyvien tehtävien ja aihealueiden osalta.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Tietoja keskustelusta Copilotin avulla

Microsoft Copilot on tekoälypohjainen avustaja, joka inspiroi toimimaan luovasti, tehostaa tuottavuutta ja poistaa tarpeen tehdä pitkäveteisiä tehtäviä. Keskustelemalla Copilotin avulla Business Centralissa saadaan vastauksia kysymyksiin ja löydetään liiketoimintatietoja. Keskustelun tavoite ilmaistaan luonnollisella kielellä. Seuraavat ovat mahdollisia keskustelun avulla:

- Liiketoimintatietojen etsiminen yrityksestä, jota käsitellään Business Centralissa. Keskustelun avulla voi hakea (ja avata) liiketoimintaprosesseihin liittyviä yksiköitä tai tietueita, kuten asiakkaita, toimittajia, myyntitilauksia ja nimikkeitä, koskevia tietoja. Copilotia voi esimerkiksi pyytää näyttämään uusimmat Adatumin myyntitilaukset.
- Käsitteen selittäminen tai ohjeiden saaminen tehtävän suorittamiseen. Voidaan esimerkiksi pyytää auttamaan ymmärtämään dimensioita tai kertomaan, miten myyntitilaus kirjataan.
- Yksittäisten kenttien tarkoituksen ja tyyppisen käyttötavan ymmärtäminen. Kun kentän työkaluvihjeessä valitaan **Kysy Copilotilta**, avautuvassa keskustelussa kentän nimen selityskehote, ja Copilot antaa siitä lisätietoja. Copilot muodostaa linkin viitattuihin artikkeleihin, joten kuvaus on helppo vahvistaa.

  Copilotin vastaukset perustuvat täysin viralliseen Dynamics 365 Business Central -ohjeistukseen, joka on saatavana Microsoft Learnin [Dynamics 365 Business Central -ohjeissa](/dynamics365/business-central/).

Keskustelu Copilotin avulla poistaa tarpeen siirtymiseen käyttöliittymässä tai tuoteohjeessa, mikä voi säästää aikaa ja parantaa tuottavuutta.
  
> [Katso video](https://go.microsoft.com/fwlink/?linkid=2250609)

## Vaatimukset

- Keskustelu Copilotin avulla -ominaisuus on aktivoitu. Järjestelmänvalvoja tekee tämän tehtävän. [Lisätietoja Copilotin ja tekoälyn ominaisuuksien määrittämisestä](enable-ai.md).
- Business Centralin näyttökieleksi on määritetty jokin seuraavista englannin kielialueista: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Lisätietoja kielen vaihtamisesta](ui-change-basic-settings.md#language).
- Business Central -ympäristö on jossain muussa maassa tai muulla alueella kuin Kanadassa. (Tämä ominaisuus ei ole vielä saatavana Kanadassa.)

## Keskustelun Copilotin avulla aloittaminen

1. Valitse näytön oikeassa yläkulmassa ![Näkyvissä Keskustelu Copilotin avulla -kuvake](media/chat-copilot-icon.png) **Copilot**-kuvake ![Näkyvissä selite numero 1](media/callout-number-1.svg).

   **Copilot**-ruutu avautuu oikealle, kuten seuraavassa kuvassa:

    ![Näkyvissä Keskustelu Copilotin avulla -kuvake ja selitteet](media/chat-with-copilot-pane.svg)

1. Kirjoita kysymys alareunan **Kysy kysymys** -ruutuun ![Näkyvissä selitenumero 2](media/callout-number-2.svg) ja saat sitten vastauksen valitsemalla nuolen tai painamalla <kbd>Enter</kbd>-näppäintä.

   Kirjoitettava teksti, jota Copilotissa kutsutaan *kehotteeksi*, voi olla kysymys, lause tai komento.

   > [!TIP]
   > Copilotissa on muuta kysymysten kirjoittamista helpottava ominaisuus:
   > - Kysymyksen muotoilun voi aloittaa valitsemalla jonkin kehoteoppaan, joita ovat **Etsi**, **Selitä** tai **Opas**. Ne ovat valittavissa ruudun yläreunassa ![Näkyvissä selitenumero 3](media/callout-number-3.svg) tai ![Näkyvissä kehoteopaskuvake](media/prompt-guide-icon.png) **Näytä kehotteet** -kuvakkeessa **Kysy kysymys** -ruudun ![Näkyvissä selitenumero 4](media/callout-number-4.svg) yläpuolella. Kehoteoppaat ovat esimääritettyjä lyhyitä lauseita, jotka aloittavat kysymyksen tai kehotteen. Ajan säästämisen lisäksi ne on suunniteltu opastamaan Copilotin vastauksia tiettyyn vastausluokkaan. Ne auttavat myös ymmärtämään, millä tavoin muotoilluilla kysymyksillä saadaan parhaat vastaukset.
   > - Valitsemalla kehote-ehdotuksia **Näytä kehotteet** -painikkeen ![Näkyvissä selitenumero 5](media/callout-number-5.svg) yläpuolelta kysytään automaattisesti esimääritetty kysymys, jolla saadaan merkityksellisiä tietoja kysymysten ja vastausten toiminnasta. Kehote-ehdotukset ovat saatavana vain käytettäessä CRONUS-esittely-yritystä.

1. Tarkista Copilot-ruudussa näkyvät vastaukset ![Näkyvissä selitenumero 6](media/callout-number-6.svg).

   Kysymyksen mukaan vastaus voi sisältää tekstiä, linkkejä Business Centralin tietueisiin tai sivuille sekä linkkejä Business Centralin ohjeartikkeleihin Microsoft Learnissa.

1. Tarkenna vastausta kysymällä uusi kysymys.

   Keskustelu muistaa kontekstin, joten alkuperäisen kysymyksen keskeisiä kohtia ei tarvitse toistaa.

## Alusta aloittaminen tyhjentämällä keskustelu

Keskustelussa Copilotin avulla voidaan siirtyä toiseen aiheeseen valitsemalla ![Näkyvissä keskustelun tyhjennyskuvake](media/clear-chat-icon.png) **Aloita uusi Copilot-keskusteluistunto** -kuvake Copilot-ruudun alaosassa kysymysruudun yläpuolella. Tämä toiminto tyhjentää viimeisimmät viestit Copilotin muistista. Alusta aloittaminen on usein kätevää, jos pitkässä keskustelussa on ollut paljon viestejä. Se voi myös auttaa Copilot antamaan tarkempia vastauksia.

Keskustelu tyhjennetään myös silloin, jos Business Central suljetaan tai siitä kirjaudutaan ulos.

## <a name="tips"></a>Kysymysten tehokas käyttö

Tässä osassa keinoja, joilla voi parantaa Copilotin antamia vastauksia.

- Kysy selkeitä ja täsmällisiä kysymyksiä.
- Käytä lyhyitä lauseita pitkien tai useiden lauseiden sijaan.
- Kysy yksi kysymys kerrallaan. <!--Avoid asking about multiple questions in one message.-->
- Käytä luonnollista kieltä sekä esitä kysymykset ystävällisesti ja keskustelunomaisesti.
- Käytä avainsanoja, fraaseja ja termejä, joiden tiedät olevan käytössä Business Central -sovelluksessa tai -ohjeissa.
- Jos ensimmäisen vastaus ei vastaa täysin kysymyksiin, esitä lisäkysymyksiä tai muotoilu viimeisin kysymys uudelleen.
- Jos kysymys koskee eri aihealuetta kuin edellinen kysymys, aloita alusta tyhjentämällä nykyinen keskusteluistunto.

## Esimerkkikehotteita

Copilotille esitettävät kysymykset vaihtelevat luonnollisesti roolin, nykyisen tehtävän, organisaation käyttämien prosessien ja oman ilmaisutavan mukaan. Seuraavat esimerkit osoittavat erilaisia tapoja esittää kysymyksiä keskusteluruudussa. Niistä voi olla apua omien kysymysten kirjottamiseen omassa tilanteessa.

Kehote: `Find the Item with Description 'ATHENS Desk'`

Tässä esimerkissä Copilotille annetaan selkeät ohjeet paikantaa yksi tietue. Siinä esimerkiksi vihjataan, että tietue löytyy nimikeluettelosta. Siinä ilmaistaan lainausmerkkien ja oikean isojen kirjaimen käytön avulla, että kuvauskentässä on oltava tietty teksti. Copilot vastaa yleensä tarkasti, kun annetut vihjeet ovat tarkkoja. Myös arkikielen käyttö on mahdollista, kuten seuraavassa esimerkissä.

Kehote: `give me the latest invoice for adatum`

Tässä esimerkissä Copilotia pyydetään paikantamaan tietue, mutta kysymys ei ole niin tarkka, joten myöskään vastaus ei ole yhtä tarkka. Copilot pystyy usein ymmärtämään tai arvaamaan, että etsittävä lasku ei ole ostotilaus vaan myyntitilaus Kirjattu myyntitilaus -luettelossa. Copilotin on myös kohdistettava `adatum` ja `Adatum Corporation`, sillä se on laskuun liitetyn tilausasiakkaan tarkka koko nimi.

Kehote: `Show me customer ledger entries for Adatum from about three weeks ago`

Tässä esimerkissä Copilotia pyydetään ratkaisemaan yleinen päivämäärähaaste, joka yleensä edellyttää kalenterin avaamista viitteeksi tai edistyneiden päivämääräsuodattimen käyttöä. Copilot ymmärtää yleensä yleiset ilmaiset ja yritystermit.

Kehote: `How does I save my filterrings to do them later?`

Tässä esimerkissä Copilotilta pyydetään ohjeita jonkin tehtävän suorittamiseen Business Centralissa. Copilot ymmärtää yleensä kysymyksen tarkoituksen, vaikka siinä olisi kielioppi- tai oikeinkirjoitusvirheitä taikka lyhenteitä.

## Anna vastauksiin palautetta

Copilotin vastauksia voidaan arvioida käyttämällä tykkää (peukku ylös) -painiketta, jos arvio on hyvä, tai ei tykkää (peukku alas) -painiketta, jos arvio on huono. Ei tykkää -painikkeen valinnan yhteydessä voidaan valita syy, kuten epätarkka, epäsopiva tai muu. Nämä tiedot voivat auttaa parantamaan ehdotuksia.

<!--
1. If you want help getting you're question started, select the prompts either from the **Find**, **Explain**, or **Guide** buttons at the top of the Coplit pane or use the **View Prompts** menu above **Ask a question** box at the bottom.

   Prompts are predefined short phrases that start a question. Apart from saving you time, they're designed to target responses to specific categories. They also help you undestand how you can phrase questions to get the responses.-->
## Katso myös

[Copilot- ja tekoälyominaisuuksien vianmääritys](ai-copilot-troubleshooting.md)  
[Copilot- ja tekoälyominaisuuksien määrittäminen](enable-ai.md)  
[Vastuullisen tekoälyn usein kysyttyjä kysymyksiä keskustelusta Copilotin avulla](faqs-chat-with-copilot.md)  
[Business Centralin ohjeresurssit](product-help-and-support.md)  
