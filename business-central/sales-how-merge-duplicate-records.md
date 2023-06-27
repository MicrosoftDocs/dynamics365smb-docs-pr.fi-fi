---
title: Asiakas- tai toimittajatietueiden kaksoiskappaleiden yhdistäminen
description: 'Kuvaa, miten asiakkaiden tai toimittajien tietoja kootaan yhteen, kun joistakin niistä on kaksoiskappaleita.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="merge-duplicate-records" />Tietueiden kaksoiskappaleiden yhdistäminen

Kun eri käyttäjät luovat uusia asiakkaan, toimittajan tai kontaktin kortteja ajan mittaan tai kun uusia tietueita luodaan automaattisesti siirron aikana, asiakkaalle, toimittajalle tai kontaktille voi tulla järjestelmään useita tietueita. Voit siinä tapauksessa käyttää säilytettävän tietueen kortin **Yhdistä kaksoiskappale** -sivua. Sivulla on yleiskatsaus kenttäarvoista, joilla on kaksoiskappaleita, ja toimintoja, joilla valitaan, mitkä arvot säilytetään tai hylätään, kun kaksi tietuetta yhdistetään.

> [!NOTE]
> Vain käyttäjät, joilla on YHDISTÄ KAKSOISKAPPALEET -käyttöoikeuksien joukko, voit käyttää tätä toimintoa.

> [!TIP]
> **Yhdistä kaksoiskappaleet** -sivulla on kaikki kentät, joissa kahden verrattavan tietueen arvot ovat erilaiset. Tämän vuoksi kaksoiskappale ilmoitetaan sivulla näyttämällä vain muutama kenttä. Jos sivulla sen sijaan näkyy useita kenttiä, epäilyttävä tietue ei todennäköisesti ole kaksoiskappale.

Seuraava toimenpide perustuu asiakaskorttiin. Toimittajan ja kontaktin korttien vaiheet ovat samankaltaisia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Valitse asiakas, johon tiedät tai epäilet tietueen kaksoiskappaleen liittyvän, ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Asiakkaan kortti** -sivulla **Yhdistä kohteeseen** -toiminto.
4. Valitse **Yhdistä kaksoiskappale** -sivun **Yhdistä kohteeseen** -kentässä asiakas, jonka uskot olevan **Nykyinen**-kentän avatun asiakkaan kaksoiskappale.

    **Kentät**-pikavälilehdessä on luettelo kentistä, joissa kahdella asiakkaalla on eri arvot. Niinpä jos valittu asiakas on kaksoiskappale, luettelossa on vain muutamia kenttiä, joissa erot johtuvat kirjoitusvirheistä tai muista tiedonsyöttövirheistä.

    **Liittyvät taulukot** -välilehdessä on luettelo taulukoista, joissa on kumpaankin asiakkaaseen liittyviä kenttiä. **Nykyinen määrä**- ja **Määrän kaksoiskappale** -kentissä ilmaistaan, kuinka monta kenttää liittyvissä taulukoissa on, joissa käytetään **Nro**-arvoa sekä nykyiselle asiakkaalle että asiakkaan kaksoiskappaleelle. **Yhdistä kaksoiskappale** -sivulla tämä osa on tarkoitettu vain tiedoksi. Jos yhdistämisristiriita on kuitenkin olemassa, ne ratkaistaan **Yhdistä ristiriidan kaksoiskappaleet** -sivulla. Katso vaiheet 8–12.   

5. Valitse **Ohita**-valintaruutu jokaisessa sellaisessa kentässä, jossa haluat käyttää muuta kuin nykyistä arvo. **Vaihtoehtoinen arvo** -kentän arvo siirretään sitten nykyiseen tietueeseen, kun prosessi valmistuu.
6. Kun olet valinnut säilytettävät tai ohitettavat arvot, valitse **Yhdistä**-toiminto.

    Järjestelmä tarkistaa, aiheuttaako asiakkaan kaksoiskappaleen arvon yhdistäminen nykyiseen asiakkaaseen ristiriitoja. Ristiriitoja on, jos ainakin yhden perusavaimen kentän arvo on sama molemmissa asiakkaissa mutta kahden asiakkaan **Ei**-kentän arvo on eri.

7. Jos ristiriitoja löytyy, valitse vahvistussanomassa **Kyllä**-painike.

    Asiakkaan kaksoiskappale nimetään uudelleen, jotta kaikki sen **Nro**-arvon käyttö kaikissa kentissä suhteessa asiakastaulukkoon korvataan **Nro**-arvolla, joka on nykyisellä asiakkaalla.
8. Jos ristiriitoja on, valitse **Ratkaise ristiriidat (xx) ennen yhdistämistä.** -toiminto **Ristiriidat**-pikavälilehdessä. Tämä välilehti avautuu, jos ristiriitoja on.
9. Valitse **Yhdistä ristiriidan kaksoiskappaleet** -sivulla ristiriitaan liittyvän taulukon rivi ja valitse sitten **Näytä tiedot** -toiminto.

    **Yhdistä kaksoiskappale** -sivulla on nyt näkyvissä ne valitun taulukon kentät, jotka aiheuttava kahden asiakastietueen välisen ristiriidan. Huomaa, että sekä **Nykyinen**- ja **Ristiriidassa seuraavien kanssa** -kenttien että vähintään yhden perusavaimen kentän rivien yhteenlasketut arvot ovat samat kummallakin asiakkaalla ja että **Nro**-kenttä on kahdella asiakkaalla eri.   
10. Jos et halua säilyttää asiakastietueen kaksoiskappaletta, valitse ensin **Poista kaksoiskappale** -toiminto ja sitten **Sulje**-painike.

    Jos kentän arvo on sama **Nro**-kentän arvoa lukuun ottamatta, arvo poistetaan tietueen kaksoiskappaleesta ja lisätään nykyiseen tietueeseen.
11. Jos haluat säilyttää asiakastietueen kaksoiskappaleen yhdistämisen jälkeen, valitse **Nimeä kaksoiskappale uudelleen**.
12. Lukuun ottamatta **Nro**-kenttää, jonka arvo on sama molemmissa tietueissa, rivien arvon voi muuttaa **Vaihtoehtoinen arvo** -kentässä, jonka jälkeen valitaan **Sulje**-painike.

    Kentän ristiriitainen arvo päivitetään tietueen kaksoiskappaleessa, jotta se voidaan yhdistää nykyiseen tietueeseen. Tietueen kaksoiskappale säilyy myös yhdistämisen jälkeen.
13. Toista vaiheet 8–12, kunnes kaikki ristiriidat on ratkaistu. **Ristiriidat**-pikavälilehti ei ole enää näkyvissä.
14. Valitse **Yhdistä kaksoiskappale** -sivulla uudelleen **Yhdistä**-toiminto ja valitse sitten vahvistussanomassa **Kyllä**.

> [!NOTE]
> Voit etsiä kontaktien kaksoiskappaleet toiminnolla ennen **Yhdistä kaksoiskappale** -sivun käyttämistä. Lisätietoja on kohdassa [Kontaktien kaksoiskappaleiden hakeminen](marketing-setup-contacts.md#searching-for-duplicate-contacts).

## <a name="see-related-microsoft-training" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/trade-master-data-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Myynti](sales-manage-sales.md)  
[Kontaktien määrittäminen](marketing-setup-contacts.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
