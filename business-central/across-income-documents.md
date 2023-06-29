---
title: Saapuvien asiakirjojen käyttäminen
description: 'Voit hallita saapuvia, ulkoisia yritysasiakirjoja, kuten maksukuitteja tai PDF-tiedostoja, hallita OCR-tehtäviä ja muuntaa tiedostoja sähköisiksi asiakirjoiksi ja tietueiksi.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="incoming-documents"></a><a name="incoming-documents"></a>Saapuvat asiakirjat

Ulkoinen liiketoiminta-asiakirja saattaa voi tulla yritykseesi sähköpostin liitteenä tai paperiversiona, jonka voit skannata tiedostoon. Tämä skenaario on tyypillinen ostoille, joissa saapuvat asiakirjatiedostot edustavat kulujen maksukuitteja tai pieniä ostoja.

**Saapuvat asiakirjat** -sivulla voit käyttää erilaisia toimintoja, joilla voit tarkistaa kulutositteita, hallita OCR-tehtäviä ja muuntaa saapuvia asiakirjatiedostoja manuaalisesti tai automaattisesti sekä siirtää niistä tietoja asiakirjoihin tai kirjanpitoriveille. Ulkoisia tiedostoja voi liittää missä tahansa prosessin vaiheessa myös kirjattuihin asiakirjoihin ja muodostuviin toimittaja-, asiakas- ja pääkirjamerkintöihin.

## <a name="usage-scenario"></a><a name="usage-scenario"></a>Käyttöskenaario

Voit rekisteröidä kauppakumppaneilta saatuja tiedostoja tai paperikopioita [!INCLUDE[prod_short](includes/prod_short.md)]iin ja luoda asiakirjatietueita. Esimerkiksi osto- tai myyntilasku, hyvityslasku tai päiväkirjarivi.

Lataa vastaanotetut tiedostot – tai ota valokuva käyttämällä laitteen kameraa – ja luo ulkoisia asiakirjoja kuvaavat merkinnät. Valinnaisesti ulkoinen OCR (Optical Character Recognition) -palvelu voi muodostaa sähköisiä asiakirjoja saapuvia asiakirjoja vastaavista PDF- tai kuvatiedostoista, ja ne voidaan sitten muuntaa [!INCLUDE[prod_short](includes/prod_short.md)]issa tietueiksi.

> [!NOTE]
> Ulkoiset palveluntarjoajat tarjoavat OCR-ominaisuuden. Valitse organisaatiolle ja/tai maalle/alueelle sopiva huoltopaketti. Etsi palvelut, jotka ovat yhteensopivia [!INCLUDE[prod_short](includes/prod_short.md)]in kanssa ja tietoja saatavilla olevista ominaisuuksista osoitteessa [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

Kun esimerkiksi saat PDF-muotoisen laskun toimittajalta, voit lähettää sen OCR-palveluun **Saapuvat asiakirjat** -sivulta. Jotkin OCR-palveluntarjoajat voivat vaihtoehtoisesti käsitellä tiedostoja, jotka on välitetty erilliseen sähköpostiosoitteeseen, mikä sitten luo automaattisesti liittyvän saapuvan asiakirjan. Jonkin sekunnin kuluttua saat tiedoston takaisin OCR-palvelusta sähköisenä laskuna, jonka voit muuntaa toimittajan ostolaskuksi.

> [!TIP]
> Luo saapuvat asiakirjatietueet [!INCLUDE[prod_short](includes/prod_short.md)]issa suoraan toimittajien lähettämistä sähköposteista käyttämällä Outlook-apuohjelmaa. Lisätietoja on kohdassa [Business Centralin käyttäminen yrityssähköpostina Outlookissa](work-outlook-addin.md).

## <a name="incoming-document-features"></a><a name="incoming-document-features"></a>Saapuvan asiakirjan ominaisuudet

Saapuvien asiakirjojen käsittely voi muodostua seuraavista pääaktiviteeteista:

* Tallenna ulkoiset asiakirjat [!INCLUDE[prod_short](includes/prod_short.md)]iin luomalla rivejä **Saapuvat asiakirjat** -sivulla toisella seuraavista tavoista:
  * Manuaalisesti tietokoneesta tai puhelimesta jollakin seuraavista tavoista:
    * Käytä **Luo tiedostosta** -painiketta, lataa tiedosto ja täytä tarvittavat kentät **Saapuva asiakirja** -sivulla.
    * Käytä **Uusi**-painiketta ja täytä tarvittavat kentät **Saapuva asiakirja** -sivulla. Liitä tämän jälkeen tiedosto manuaalisesti.
    * Käytä tabletista tai puhelimesta **Luo kamerasta** -painiketta ja luo uusi saapuva asiakirja käyttäen laitteen omaa kameraa.
  * Automaattinen tallennus tapahtuu vastaanottamalla asiakirja OCR-palvelusta sähköisenä asiakirjana sen jälkeen, kun olet ladannut tai lähettänyt liittyvän PDF- tai kuvatiedoston OCR-palveluun. **Rahoituksellisia tietoja** -pikavälilehden tiedot täytetään automaattisesti **Saapuva asiakirja** -sivulla.
* Muunna PDF- tai kuvatiedostot ulkoisessa OCR-palvelussa sähköisiksi asiakirjoiksi, jotka voidaan muuntaa [!INCLUDE[prod_short](includes/prod_short.md)]in asiakirjatietueiksi.
* Luo saapuville asiakirjatietueille uusia asiakirjoja tai yleisen päiväkirjan rivejä syöttämällä tiedot samalla kun luet ne saapuvista asiakirjatiedostoista.
* Liitä saapuvia asiakirjatiedostoja missä tahansa tilassa oleviin osto- ja myyntiasiakirjoihin (myös kirjauksesta muodostuviin toimittaja-, asiakas- ja pääkirjamerkintöihin).
* Tarkastele saapuvia asiakirjatietueita ja niiden liitteitä mistä tahansa osto- tai myyntiasiakirjasta. **Tilikartta**-sivulta voi myös etsiä kaikki pääkirjamerkinnät, joilla ei ole saapuvia asiakirjatietueita.

> [!NOTE]
> Kortteihin ja asiakirjoihin **Liitteet**-välilehdessä liitetyt tiedostot eivät sisälly **Saapuvat asiakirjat** -sivuun. Lue lisätietoja kohteesta [Korttien ja asiakirjojen liitteiden, linkkien ja muistioiden hallinta](ui-how-add-link-to-record.md)

| Vastaanottaja | Katso |
| --- | --- |
| Määritä **Saapuvat asiakirjat** -ominaisuus ja OCR-palvelu. |[Saapuvien asiakirjojen määrittäminen](across-how-setup-income-documents.md) |
| Luo saapuvat asiakirjatietueet manuaalisesti tai automaattisesti esimerkiksi ottamalla paperikuitista valokuvan. |[Saapuvien asiakirjatietueiden luominen](across-how-create-income-document-records.md) |
| Muunna PDF- ja kuvatiedostot OCR-palvelun avulla sähköisiksi asiakirjoiksi, jotka voi sitten muuntaa [!INCLUDE[prod_short](includes/prod_short.md)]issa esimerkiksi ostolaskuiksi. Kouluta OCR-palvelu niin, että se välttää virheitä seuraavalla kerralla, kun palvelu käsittelee samanlaisia tietoja. |[PDF- ja kuvatiedostojen muuntaminen sähköisiksi asiakirjoiksi OCR-palvelun avulla](across-how-use-ocr-pdf-images-files.md) |
| Yhdistä saapuva asiakirjatiedosto mihin tahansa kirjaamattomaan myynti- tai ostoasiakirjaan ja mihin tahansa asiakas-, toimittaja- tai pääkirjamerkintään asiakirjasta tai merkinnästä käsin tai poista saapuva asiakirjatiedosto mainituista näistä kohteista. |[Saapuvien asiakirjatietueiden luominen suoraan asiakirjoista ja tapahtumista](across-how-connect-disconnect-income-document-records.md) |
| **Tilikartta**- ja **Pääkirjanpidon tapahtumat** -sivujen hakutoiminnon avulla voit etsiä pääkirjanpidon tapahtumia kirjatuille asiakirjoille, joilla ei ole saapuvia asiakirjatietueita. Tämän jälkeen voit keskitetysti muodostaa yhteyden olemassa oleviin tietueisiin tai luoda uusia tietueita ja niihin liittyviä asiakirjatiedostoja. |[Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjatietueita](across-how-find-posted-documents-without-income-document-records.md) |
| Saat paremman yleiskuvan määrittämällä saapuvien asiakirjatietueiden tilaksi *Käsitelty*, kun haluat poistaa ne oletusnäkymästä. |[Useiden saapuvien asiakirjatietueiden hallinta](across-how-manage-many-income-document-records.md) |

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Osto](purchasing-manage-purchasing.md)  
[Kirjattujen asiakirjojen muokkaaminen](across-edit-posted-document.md)  
[Sähköinen tiedonsiirto](across-data-exchange.md)  
[Business Centralin ja OneDrive for Businessin integrointi](across-onedrive-overview.md)  
[Business Central -sovelluksen käyttäminen yrityssähköpostina Outlookissa](work-outlook-addin.md)  
[Asiakirjojen ja sähköpostien lähettäminen](ui-how-send-documents-email.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
