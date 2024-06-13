---
title: Perinnän muistutusten automatisointi
description: 'Säästä aikaa perinnässä automatisoimalla asiakkaille lähetettävien muistutusten luonti-, julkaisu- ja lähetysprosessin.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.search.keywords: 'collection, remindes'
ms.search.form: null
ms.date: 03/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="automate-reminders-in-collections"></a>Perinnän muistutusten automatisointi

Perintää voi tehostaa automatisoimalla asiakkaille lähetettävien muistutusten luonti-, julkaisu- ja lähetysprosessin. Automatisointi voi vähentää merkittävästi perintään kuluvaa aikaa, antaa paremman yleiskuvan prosessista ja mahdollistaa jokaisen vaiheen täyden hallinnan.

Yksittäiset toiminnot (vaiheet) määritetään **Muistutuksen automaatio** -sivulla. Muistutusten luonti-, julkaisu- ja lähetysvaiheet voidaan yhdistää. Vaihtoehtoisesti kullekin vaiheelle voidaan luoda erillinen automaatio, jos se parempi vaihtoehto omille perintäprosesseille. Automaatiot perustuvat muistutusehtoihin ja muistutustasoihin. Lisätietoja on kohdassa [Muistutusehtojen ja -tasojen määrittäminen](finance-setup-reminders.md). Suodattimet voidaan määrittää muistutusehdoille koko automaatiossa, minkä lisäksi suodattimet määritetään automaation kullekin toiminnolle. Lisäksi avoimet laskut voidaan PDF-tiedostoina sähköpostien liitteeksi.

Automaatio toteutetaan työjonotapahtumana. Automaatiota määritettäessä **Aikataulu**-kentän avulla määritetään, miten ja milloin automaatio suoritetaan. Jos valitaan **Manuaalinen**, automaatio suoritetaan kerran **Käynnistä**-toiminnolla. Valittavana on myös **Viikoittain** ja **Kuukausittain** sekä **Mukautettu**, jolla voidaan määrittää eritelty aikataulu. Jos **Mukautettu** valitaan, päivämääräkaava on syötettävä. Lisätietoja päivämääräkaavan syöttämisestä on kohdassa [Päivämääräkaavojen käyttäminen](ui-enter-date-ranges.md#use-date-formulas). Jos valittu vaihtoehto on jokin muu kuin **Manuaalinen**, automaatio suoritetaan, kunnes se keskeytetään ja asetetaan pitoon. Jos automaation suorittamista halutaan tarkentaa lisää, **Työjonotapahtumat**-toiminnolla voi avata **Työjonotapahtumat**-sivun, jossa voi muuttaa toistuvuuden esimerkiksi päivittäiseksi tai tietylle viikonpäivälle.

## <a name="automate-the-reminders-flow"></a>Muistutustyönkulun automatisointi

Seuraavissa osissa käsitellään muistutusten määrittämistä siten, että ne luodaan, julkaistaan ja lähetetään automaattisesti.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutusten automaatio** ja valitse sitten vastaava linkki.
1. Valitse **Uusi** ja täytä sitten **Yleinen**-pikavälilehden kentät.
1. Valitse **Muistutusehtojen suodatus** -kentässä muistutusehto tai -ehdot, joissa tätä automaatiota käytetään.
1. Valitse **Aikataulu**-kentässä, kuinka usein automaatio suoritetaan.
1. Valitse **Toiminnot**-pikavälilehdessä **Uusi** ja valitse sitten, luoko, julkaiseeko tai lähettääkö automaatio muistutuksia. Valitse **OK**.
1. Täytä tarvittavat kentät automaation suorittaman toiminnon tyypin mukaan määrityssivulla. Lisätietoja asetuksista on kohdassa [Muistutustoimintojen asetukset](#settings-for-reminder-actions).
1. Kun automaation toiminnot on määritetty, niiden suoritusjärjestystä voi muuttaa **Siirrä ylös**- ja **Siirrä alas** -toiminnoilla.

## <a name="settings-for-reminder-actions"></a>Muistutustoimintojen asetukset

Muistutuksen luonti-, julkaisu- ja lähetystoimintojen määritysasetukset ovat erilaisia. Seuraavissa osissa käsitellään niiden käyttämistä.

### <a name="create"></a>Luonti

* Määritä korkein taso kaikille muistutusriveille.  
* Luo muistutuksia pidossa oleville tapahtumille. Tämä asetus on kätevä esimerkiksi silloin, kun asiakkaan kanssa keskeneräinen riitatilanne ja heidän halutaan saavan kokonaiskuvan:
* Luo muistutuksia kaikille maksamattomille laskuilla eikä vain erääntyneille laskuille. Raportti näyttää erillään erääntyneet laskut ja laskut, joita ei ole maksettu mutta jotka eivät ole erääntyneet.
* Tarkenna muistutusta suodattimia määrittämällä.

### <a name="issue"></a>Lähetä

Kun muistutus julkaistaan, asiakastapahtumiin luodaan tapahtumia, jotka sisältävät kirjauspäivän and verotuspäivän. **Lähetä muistutuksia -määritys** -sivun asetuksilla voi määrittää, korvataanko lähetetyn muistutuksen tiedot luodun muistutuksen tiedoilla. Jos muistutus esimerkiksi luotiin edellisenä päivänä ja lähetettiin kuluvana päivänä, eräpäivä siirtyy päivällä.

### <a name="send"></a>Lähetä

> [!NOTE]
> Lähetysautomaatio edellyttää, että sähköposti on määritetty [!INCLUDE [prod_short](includes/prod_short.md)]issa. Lisätietoja sähköpostin määrittämisestä on kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).

Sähköpostien sisältö, kuten liitetekstit, sähköpostin perustekstit ja kieli saadaan muistutusehdon määrityksistä. Lisätietoja sähköpostiasetuksista on kohdassa [Muistutusehtojen ja -tasojen määrittäminen](finance-setup-reminders.md).

Seuraavia voidaan hallita **Lähetä muistutuksia -määritys** -sivun asetusten avulla:

* Yleiset asetukset, kuten kuvaus, ja saman muistutuksen lähetyskertojen määrä.
* Muistutukseen sisällytettävän sisällön asetukset.
* Asetukset lähetettyjen muistutusten seurantaan vuorovaikutuksia luomalla riippumatta siitä, tulostetaanko muistutukset vai lähetetäänkö ne sähköpostitse, ja liitetäänkö vain erääntyneet laskut, kaikki laskut vai ei mitään laskuja. 

## <a name="access-the-history-of-a-reminder"></a>Muistutushistorian käyttäminen

[!INCLUDE [prod_short](includes/prod_short.md)] kirjaa jokaisen automaation suorituskerran Historiatietoja saadaan käyttöön valitsemalla **Lokitapahtumat**-toiminto. Lisäksi **Lähetetyt muistutukset** -toiminnon avulla saadaan luettelo lähetetyistä muistutuksista.

## <a name="handle-errors"></a>Virheiden käsitteleminen

**Toiminnot**-pikavälilehdessä voidaan määrittää kullekin toiminnolle, halutaanko automaation pysähtyvän, jos toiminnossa on virhe. Jos näin tehdään, automaatio ei käsittele myöhemmin tulevia toimintoja. Tämä ominaisuus otetaan käyttöön tai poistetaan käytöstä **Määritä Pysäytä virheen ilmetessä**- tai **Tyhjennä Pysäytä virheen ilmetessä** -toiminnolla.

## <a name="change-action-settings-for-an-automation"></a>Automaation toimintoasetusten muuttaminen

Automaation asetuksia voidaan muuttaa koska tahansa. Valitse **Toiminnot**-pikavälilehdessä **Määritys** ja tee muutokset.

## <a name="see-also"></a>Katso myös

[Muistutusehtojen ja -tasojen määrittäminen](finance-setup-reminders.md)  
[Avoimia saldoja koskevien muistutusten lähettäminen](receivables-send-reminders.md)  
