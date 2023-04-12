---
title: Business Centralin Copilot-esiversion käytön aloittaminen
description: 'Tässä artikkelissa kerrotaan, miten hankkia Business Central -ympäristö, jonka uudella tekoälyominaisuudella voi luoda tekstiehdotuksia nimike- ja tuotekuvauksille.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/16/2023
ms.custom: bap-template
---

# Business Centralin Copilot-esiversion käytön aloittaminen

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Voit kokeilla tekoälypohjaista tuotemarkkinointitekstin luontia Copilotin avulla, olitpa Business Centralin nykyinen tai potentiaalinen asiakas, eli joku, joka on vain kiinnostunut tutustumaan Business Centraliin ja kokeilemaan uutta ominaisuutta. Päästäksesi alkuun tarvitset käyttöoikeuden Business Central Online -versioon, joka tukee uutta ominaisuutta. Täytä alla oleva sinua koskeva osio.

## Organisaatiossa on jo käytössä Business Central

Koska olet aiemmin rekisteröitynyt asiakas tai kumppanimme, tarvitset Business Central -hallintakeskuksen käyttöoikeuden, ja voit määrittää ympäristön, joka suorittaa esikatseluversion, johon kuuluu Copilot. Kun ympäristö on käynnissä, käyttäjät voivat kokeilla uutta ominaisuutta.

Jos olet ympäristön järjestelmänvalvoja, tee seuraavat toimet:

1. Kirjaudu Business Centralin hallintakeskukseen.
2. Valitse **ympäristö** > **Uusi**.
3. Kirjoita **Luo ympäristö** -ruudussa uuden ympäristön nimi **Ympäristön nimi** -kenttään.
4. Määritä **Ympäristön tyypiksi** **Eristysympäristö** tai **Tuotanto**.
5. Määritä **Maa** kaikkien luettelossa olevien maiden/alueiden mukaan, mutta huomaa, että esiversiossa Copilot-ohjelman tekoälypohjainen markkinointiteksti on vain englanniksi.
6. Valitse **Versio**-ruudun luettelosta versio 22 tai uudempi.

   <!--
   > [!IMPORTANT]
   > You must use **22.0.54157.54311 (Preview - Copilot edition)** to experience Copilot.
   -->
7. Valitse **Luo**.  

Lisätietoja ympäristöjen luomisesta on kohdassa [Ympäristön luominen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

> [!IMPORTANT]
> Jos sinulla on esiversiona eristysympäristöjä, jotka käyttävät **22.0.54157.54311 (Esiversio - Copilot edition)** -ympäristöä, huomaa, että nämä ympäristöt ovat saatavilla vain 1. toukokuuta 2023 saakka. Tämän päivämäärän jälkeen sinun täytyy valmistella uusi ympäristö tai päivittää mitä tahansa muuta ympäristöäsi versioon 22.0 tai uudempaan, jotta voit jatkaa tekoälypohjaisen nimikkeen markkinointitekstin esiversion kokeilua.

## Organisaatiossa ei ole käytössä Business Centralia

Jos et ole Business Central -asiakas, voit rekisteröityä maksuttoman kokeiluversion käyttäjäksi kokeillaksesi tekoälyominaisuuksia. Kirjautuminen kokeiluversioon on helppoa. Sinut ohjataan muutaman vaiheen läpi, joissa sinun täytyy antaa joitakin tietoja, kuten sähköpostiosoite, puhelinnumero ja nimi. Voit saada kokeiluversion käyttöön toimimalla seuraavasti:

1. Siirry [tämän kokeiluversion sivustoon](https://go.microsoft.com/fwlink/?linkid=2227167) ja aloita kirjautumisprosessilla.
2. Noudata näytön ohjeita.

   Sinua pyydetään antamaan tietoja, kuten sähköpostiosoitteesi, nimesi ja puhelinnumerosi. Tarkka kokemus voi vaihdella antamiesi tietojen mukaan. <!--But here are a couple important points to be aware of as you run through the sign-up process:--> Käytä sähköpostiosoitteena työpaikan tai oppilaitoksen sähköpostiosoitetta. Luomme kokeiluversion organisaatiosi tilille. Kuluttajasähköpostipalveluiden ja telekommunikaatiopalveluntarjoajien sähköpostiosoitteita ei voi käyttää (esimerkiksi outlook.com, hotmail.com ja gmail.com).
   
   <!-- When you get to the option for **Country or region** be sure to set this **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  -->
3. Kun tulet **vahvistustiedot**-vaiheeseen, olet valmis aloittamaan kokeiluversion käytön.

   - Voit siirtyä suoraan Business Centraliin valitsemalla **Ohita ja siirry Dynamics 365 Business Centraliin** > **Aloitus**.
   - Voit myös kutsua muita organisaatiotasi käyttämään maksutonta kokeiluversiota. Syötä kunkin henkilön sähköpostiosoitteet ja valitse **Lähetä kutsut**. Siirry Business Centralin aloitusnäyttöön valitsemalla **Aloita** .  

   Sinut uudelleenohjataan kokeiluversioon osoitteessa [https://businesscentral.dynamics.com/](https://businesscentral.dynamics.com/). Kokeiluversion valmistuminen voi kestää useita minuutteja, kun kirjaudut ensimmäisen kerran.

<!--
1. On the **Let's get you started** step, enter your work or school email address, then select **Next**.

   Use your work or school email address. We'll establish your trial on your organization's account. You can't use email addresses provided by consumer email services or telecommunication providers, such as outlook.com, hotmail.com, gmail.com, and others.
3. When asked what kind of email you have, select **I got it from my organization** > **Next**.
4. On the **Create your account** step, you provide information that will help use set up a trial version of Business Central that you can sign in to.

   1. Provide a telephone number that we can use to send you a verification code. Enter a country code and number that isn't VoIP or toll free.
   2. Choose how you want us to send the verification code:
      - Select **Text me** to get the verification code in a text message.
      - Select **Call me** to get the code in a voice message.
   3. Select **Send verification code**. 
   4. When you get the code, type it in the **Enter your verification code** box, then select **Verify**.

      Once you're verified, we'll send you an email with another verification code that you'll use in the next step to complete creating your account.
   5. Fill in your first and last name.
   6. Set **Country or region** to **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  

   7. Enter a valid phone umber in the **Business telephone number** box.
   8. In the **Create password** and **Confirm password** boxes, enter a password that you want to use to sign in to Business Central. The password must at least eight characters and include at least one number, an uppercase letter, and a lower case letter.
   9. In the **Verification code** box, enter the verification code we sent you in an email, then select **Next**.
   10. When you get a prompt that your account is successfully created, select **Sign in**.
-->

4. Kun olet kirjautunut sisään, näet Business Centralin aloitussivun eli roolikeskuksen, joka muistuttaa seuraavaa kuviota:

   [![Näyttää Business Central -roolikeskuksen ja Copilot-ohjelman tarkistusluettelon](media/copilot-checklist.png)](media/copilot-checklist.png#lightbox)

5. Jos haluat saada opastetun johdannon tekoälypohjaisen nimikkeen markkinointitekstin luomiseen Copilot-ohjelman avulla, valitse sivun yläosassa olevan **tarkistusluettelon** alta **Luo Copilotilla** > **Aloita esittely**. Seuraa sitten vain näytön ohjeita.

   > [!TIP]
   > Jos et näe **tarkistuslistaa**, valitse ensin **Näytä esittelykierrokset** -painike.

## Seuraavat vaiheet

Copilot-ohjelman tarjoamien tekoälyominaisuuksin tulee olla käytössä, ennen kuin sinä tai joku muu voi käyttää Copilot-toimintoa. Jotta järjestelmänvalvoja voi ottaa käyttöön tekoälyominaisuudet, hänen täytyy hyväksyä [esiversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) käyttöehdot ja [Microsoftin tietosuojakäytäntöjen ehdot](https://go.microsoft.com/fwlink/?LinkId=521839) organisaation puolesta.

> [!NOTE]
> Jos käytät kokeiluversiota, olet järjestelmänvalvoja. Jos olet kutsunut muut organisaatiosi henkilöt kokeiluversioon rekisteröitymisen yhteydessä, he eivät voi käyttää Copilot-ikkunaa, ennen kuin hyväksyt ehdot.

Järjestelmänvalvoja voi hyväksyä kahdella tavalla:

- Helpoin tapa on käyttää Copilotia. Kun käytät Copilotia ensimmäistä kertaa ylläpitäjänä, saat kehotuksen tarkistaa käyttöehdot ja sitten joko hyväksyä tai hylätä ne. Jos haluat oppia käyttämään Copilotia, siirry kohtaan [Lisää markkinointiteksti nimikkeisiin](item-marketing-text.md).  

- Toinen tapa on käyttää Business Centralin **Tietosuojailmoitusten tila** -sivua ja hyväksyä **Azure OpenAI** -integrointi kaikille käyttäjille. Lisätietoja on kohdassa [käyttöehtojen hyväksyminen](enable-ai.md#consent-to-or-reject-the-preview-and-privacy-terms-and-conditions-for-all-users).

## Katso myös

[Tekoälypohjainen tuotteen markkinointiteksti Copilotin avulla -yleiskatsaus](ai-overview.md)  
[Nimikkeen tekoälypohjaisen markkinointitekstin määrittäminen Copilotin avulla järjestelmänvalvojana](enable-ai.md)  
[Luo markkinointiteksti nimikkeille käyttämällä Copilotia](item-marketing-text.md)  
[Tekoälypohjainen tuotteen markkinointiteksti (esiversio) Copilotin avulla - UKK](ai-faq.md)  