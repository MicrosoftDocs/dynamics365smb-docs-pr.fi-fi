---
title: Vähennyskelvottoman arvonlisäveron määrittäminen
description: 'Tässä artikkelissa käsitellään vähennyskelvottoman ALV:n määrittämistä Microsoft Dynamics 365 Business Centralissa.'
author: altotovi
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 08/13/2024
ms.custom: bap-template
ms.reviewer: bholtorf
---

# <a name="set-up-nondeductible-vat"></a>Vähennyskelvottoman arvonlisäveron määrittäminen

Vähennyskelvoton arvonlisävero (ALV) on ostajan maksettavaksi tuleva ALV, joka se ei ole vähennyskelpoinen ostajan omasta ALV-velasta. Yritykset voivat yleensä periä ALV:n liiketoimintansa yhteydessä olevien tavaroiden ja palveluiden hankinnasta. Joissakin tilanteissa yritys kuitenkin aiheuttaa ALV:n, joka ei ole vähennyskelpoinen. Nämä tilanteet liittyvät yleensä paikallisiin määräyksiin ja voivat vaihdella maittain ja alueittain. Vähennyskelvottoman tai osittain vähennyskelpoisen arvonlisäveron käyttömalli on kuitenkin samanlainen. Voit käyttää suhteellista arvolisäveroa ALV:n laskemiseen, kun ALV on vähennyskelpoista ja vähennyskelvotonta.

Yleisesti ottaen ALV:tä ei voi vähentää joistakin ostoista seuraavien seikkojen vuoksi:

- **Ostettavien tavaroiden tai palveluiden tyyppi** – ALV on lainsäädännön mukaan kokonaan tai osittain vähennyskelvoton tavaroista, kuten autoista, matkapuhelimista ja ravintoloista ostetuista ruoista.
- **Osittain vähennyskelpoinen suhteellinen ALV** – ALV on suhteutettu arvonlisäverovelvollisen myyntitoiminnan ja kaikkiin suoritettuihin toimintoihin. Tämän suhteen ylittävää ALV:tä ei voida vähentää.

Koska voi olla vaikea tietää, missä ja milloin nimikettä käytetään, lisätietoja saa oman maan tai alueen veroviranomaisilta. He voivat auttaa päättämään, vähennetäänkö tietty prosenttiosuus ALV:stä historiallisten tietojen perusteella.

> [!IMPORTANT]
> Tämä yleinen ominaisuus on käytettävissä kaikissa maissa, joissa on käytössä ALV **lukuun ottamatta Belgiaa, Italiaa ja Norjaa**. Näissä lokalisoinneissa on jo paikallinen ominaisuus, ja ne päivitetään myöhemmin. Älä suorita tätä ominaisuutta näissä maissa, koska päivitystoimintoa ei ole.

## <a name="use-nondeductible-vat"></a>Vähennyskelvottoman ALV:n käyttäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV:n määrittäminen** ja valitse sitten vastaava linkki.
2. Valitse **Salli vähennyskelvoton ALV** -valintaruutu.

    > [!IMPORTANT]
    > Kun olet ottanut käyttöön vähennyskelvottoman ALV:n, et voi poistaa sitä käytöstä, koska ominaisuus voi sisältää muutoksia tietoihin ja saattaa aloittaa joidenkin tietokantataulukoiden päivittämisen. Microsoft suosittelee, että otat tämän ominaisuuden ensin käyttöön ja testaat sen eristysympäristössä, ennen kuin otat sen käyttöön tuotantoympäristössä.

3. Määritä, miten [!INCLUDE [prod_short](includes/prod_short.md)] käsittelee vähennyskelvottomia ALV-arvoja.

    1. Määritä **Käytä nimikekustannusta** -kentässä, lisätäänkö vähennyskelvoton ALV nimikekustannukseen nimikkeiden ostamisen yhteydessä. Muussa tapauksessa vähennyskelvottomalla ALV:llä ei ole vaikutusta nimikekustannuksiin, ja koko summa tallennetaan vain pääkirjanpidon tasolla.
    2. Valitse **Käyttöomaisuuden kustannukset** -valintaruutu, jos haluat lisätä käyttöomaisuuden kustannukseen vähennyskelvottoman ALV:n, kun ostat uusia käyttöomaisuushyödykkeitä. Muussa tapauksessa vähennyskelvottomalla ALV:llä ei ole vaikutusta käyttöomaisuuskustannuksiin, ja koko summa tallennetaan vain pääkirjanpidon tasolla.
    3. Valitse **Käytä projektin kustannukseen** -valintaruutu, jos haluat määrittää, että vähennyskelvoton ALV on lisättävä projektin kustannuksiin projektinimikkeiden ostamisen yhteydessä. Muussa tapauksessa vähennyskelvottomalla ALV:llä ei ole vaikutusta projektikustannuksiin, ja koko summa tallennetaan vain pääkirjanpidon tasolla.
    4. Valitse **Näytä vähennyskelv. ALV riveinä** -valintaruutu, jos haluat määrittää, että vähennyskelvottoman ALV:n on oltava asiakirjarivisivuilla, jotta ALV-summia on helpompi käsitellä.

## <a name="use-the-nondeductible-vat-percentage"></a>Vähennyskelvottoman ALV-prosentin käyttäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjausten asetukset** ja valitse sitten vastaava linkki.
2. Määritä **ALV-kirjauksen asetukset** -sivun kentät seuraavassa taulukossa kuvatulla tavalla.

    | Kenttä | Kuvaus |
    |-------|-------------|
    | **Salli vähennyskelvoton ALV** | Määritä, otetaanko vähennyskelvoton ALV huomioon nykyisessä liiketoiminnan ALV-kirjausryhmän ja tuotteen ALV-kirjausryhmän yhdistelmässä. |
    | **vähennyskelvoton ALV %** | Määritä tapahtuman summan prosenttimäärän, josta ei makseta ALV:tä. |
    | **Ei-vähennyskelpoisten ostojen ALV-tili** | Määritä siihen ALV-summaan liitetty tili, jota ei ole vähennetty ostettujen tavaroiden tai palvelujen tyypin vuoksi. |

    > [!NOTE]
    > Jos haluat, että pääkirjanpito (KP) -tapahtumat, jotka käyttävät erillistä tiliä myynti-/ostotilin sijaan, voivat jättää **vähennyskelvottoman oston ALV-tili** -kentän tyhjäksi tai määrittää **KP-tili**-kentän.

3. Valitse **OK**.

> [!NOTE]
> Et voi käyttää ei-realisoitunutta ALV:ia yhdessä vähennyskelvottoman ALV:n kanssa.
>
> Älä käytä samaa **ALV-tunnus**-arvoa sekä normaalille ALV:lle, jossa **vähennyskelvoton ALV-%** -kentän arvo on **0** (nolla) ja normaali ALV, jossa **vähennyskelvoton ALV-%** -kentän arvoksi on määritetty muu kuin nolla. Muussa tapauksessa vähennyskelvottoman ALV-summan kokonaissumma lasketaan virheellisesti.

## <a name="see-also"></a>Katso myös

[Taloushallinto](finance.md)  
[Rakennetiedot: Vähennyskelvoton ALV](design-details-nondeductible-vat.md)  
[Vähennyskelvottoman ALV:n käyttäminen](finance-how-use-non-deductible-vat.md)  
[Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen](finance-setup-vat.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
