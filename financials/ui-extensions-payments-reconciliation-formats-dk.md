---
title: "Maksujen ja täsmäytysten (DK) laajennuksen käyttäminen | Microsoft Docs"
description: "Tämän laajennuksen avulla on helppo viedä esimuotoiltuja tiedostoja, jotka täyttävät pankin sähköisiä lähetyksiä koskevat vaatimukset."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 09/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c2daa9854f371660dd9096c54d85812466dfe46e
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---

# <a name="the-payments-and-reconciliations-dk-extension-for-microsoft-dynamics-for-finance-and-operations-business-edition"></a><span data-ttu-id="f219b-103">Maksujen ja täsmäytysten (DK) laajennukset Microsoft Dynamics for Finance and Operations, Business editionille</span><span class="sxs-lookup"><span data-stu-id="f219b-103">The Payments and Reconciliations (DK) Extension for Microsoft Dynamics for Finance and Operations, Business edition</span></span>
<span data-ttu-id="f219b-104">Tee nopeita ja virheettömiä maksuja tuomalla tiedostot, jotka on muotoiltu erityisesti toimittajan tai pankin kanssa tapahtuvia siirtoja varten.</span><span class="sxs-lookup"><span data-stu-id="f219b-104">Make fast, error-free payments by exporting files that are formatted specifically for exchanges with your vendor or bank.</span></span> <span data-ttu-id="f219b-105">Nämä tiedostot nopeuttavat maksu- ja täsmäytysprosesseja ja eliminoivat virheet, joita voi tapahtua tietojen manuaalisessa syöttämisessä pankin sivustossa.</span><span class="sxs-lookup"><span data-stu-id="f219b-105">These files speed up the payment and reconciliation processes, and eliminate errors that can happen when you manually enter the information on a bank website.</span></span>  
  
<span data-ttu-id="f219b-106">Tämä laajennus tukee useiden Tanskan pankkien tiedostomuotoja.</span><span class="sxs-lookup"><span data-stu-id="f219b-106">This extension supports file formats for several Danish banks.</span></span> <span data-ttu-id="f219b-107">Kun vietä maksutiedot tiedostoon, laajennus pakkaa tiedot pankin vaatimaan muotoon.</span><span class="sxs-lookup"><span data-stu-id="f219b-107">When you export payment information to a file, the extension packages the data into the format that your bank requires.</span></span> <span data-ttu-id="f219b-108">Muotoja ovat esimerkiksi Bankdata-V3, BEC, SDC ja FIK, joita useat pankit käyttävät. Jotkin pankit, kuten Danske Bank ja Nordea, käyttävät erikoismuotoja.</span><span class="sxs-lookup"><span data-stu-id="f219b-108">For example, the formats include Bankdata-V3, BEC, SDC, and FIK, which many different banks use, and some that are more specialized for certain banks, for example, Danske Bank and Nordea.</span></span> <span data-ttu-id="f219b-109">Laajennus sisältää myös muotoja tiliotteiden tuontia ja täsmäytystä varten.</span><span class="sxs-lookup"><span data-stu-id="f219b-109">The extension also includes some formats for importing and reconciling bank statements.</span></span>  
  
> [!Note]
> <span data-ttu-id="f219b-110">Sinun tulee tietää pankin tai toimittajan vaatima muoto, jotta voit käyttää laajennusta.</span><span class="sxs-lookup"><span data-stu-id="f219b-110">To use the extension, you must know the format that your bank or vendor requires.</span></span> <span data-ttu-id="f219b-111">Jotkin pankit ja toimittajat kertovat tämän tiedon verkkosivustoillaan. Joissakin tapauksissa tieto on pyydettävä pankin tai toimittajan asiakaspalvelusta.</span><span class="sxs-lookup"><span data-stu-id="f219b-111">Some banks or vendors provide this information on their websites; however, you might need to contact their customer service to get the information.</span></span>  
  
## <a name="supported-bank-formats"></a><span data-ttu-id="f219b-112">Tuetut pankin muodot</span><span class="sxs-lookup"><span data-stu-id="f219b-112">Supported Bank Formats</span></span>
<span data-ttu-id="f219b-113">Tätä laajennusta voi käyttää seuraavissa maksutiedostojen muodoissa:</span><span class="sxs-lookup"><span data-stu-id="f219b-113">This extension can apply the following file formats for payment files:</span></span>  
  
* <span data-ttu-id="f219b-114">BANKDATA-V3</span><span class="sxs-lookup"><span data-stu-id="f219b-114">BANKDATA-V3</span></span>  
* <span data-ttu-id="f219b-115">BEC-INDLAND</span><span class="sxs-lookup"><span data-stu-id="f219b-115">BEC-INDLAND</span></span>  
* <span data-ttu-id="f219b-116">BEC-CSV</span><span class="sxs-lookup"><span data-stu-id="f219b-116">BEC-CSV</span></span>  
* <span data-ttu-id="f219b-117">DANSKEBANK-CMKV</span><span class="sxs-lookup"><span data-stu-id="f219b-117">DANSKEBANK-CMKV</span></span>  
* <span data-ttu-id="f219b-118">DANSKEBANK-CMKXKSX</span><span class="sxs-lookup"><span data-stu-id="f219b-118">DANSKEBANK-CMKXKSX</span></span>  
* <span data-ttu-id="f219b-119">DANSKEBANK</span><span class="sxs-lookup"><span data-stu-id="f219b-119">DANSKEBANK</span></span>  
* <span data-ttu-id="f219b-120">FIK71</span><span class="sxs-lookup"><span data-stu-id="f219b-120">FIK71</span></span>  
* <span data-ttu-id="f219b-121">NORDEA-ERHVERV-CSV</span><span class="sxs-lookup"><span data-stu-id="f219b-121">NORDEA-ERHVERV-CSV</span></span>  
* <span data-ttu-id="f219b-122">NORDEA</span><span class="sxs-lookup"><span data-stu-id="f219b-122">NORDEA</span></span>  
* <span data-ttu-id="f219b-123">NORDEA-UNITEL-V3</span><span class="sxs-lookup"><span data-stu-id="f219b-123">NORDEA-UNITEL-V3</span></span>  
* <span data-ttu-id="f219b-124">SDC</span><span class="sxs-lookup"><span data-stu-id="f219b-124">SDC</span></span>  
* <span data-ttu-id="f219b-125">SDC-CSV</span><span class="sxs-lookup"><span data-stu-id="f219b-125">SDC-CSV</span></span>  

## <a name="to-set-up-the-extension"></a><span data-ttu-id="f219b-126">Laajennuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f219b-126">To set up the extension</span></span>
<span data-ttu-id="f219b-127">Aloittaminen edellyttää muutamien vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="f219b-127">There are a few steps to get started.</span></span>  
  
* <span data-ttu-id="f219b-128">Salli maksutietojen viennit.</span><span class="sxs-lookup"><span data-stu-id="f219b-128">Allow payment data exports.</span></span> <span data-ttu-id="f219b-129">Tätä ei ole sallittu oletusarvoisesti tietoturvan vuoksi.</span><span class="sxs-lookup"><span data-stu-id="f219b-129">To help protect your data, this is not readily available.</span></span>  
* <span data-ttu-id="f219b-130">Määritä ostot ja ostovelat niin, että laskuissa ei tarvita ulkoisten asiakirjojen numeroita.</span><span class="sxs-lookup"><span data-stu-id="f219b-130">Set up purchase and payables so that you do not require external document numbers on invoices.</span></span> <span data-ttu-id="f219b-131">Voit tarvittaessa käyttää viitenumeroa, kun viittaat tiettyyn laskuun.</span><span class="sxs-lookup"><span data-stu-id="f219b-131">If needed, you can use the reference number to refer to a specific invoice.</span></span>  
* <span data-ttu-id="f219b-132">Määritä kunkin toimittajan maksutapa.</span><span class="sxs-lookup"><span data-stu-id="f219b-132">Specify the payment method for each vendor.</span></span> <span data-ttu-id="f219b-133">Maksutavat määrittävät, miten maksat toimittajien laskut.</span><span class="sxs-lookup"><span data-stu-id="f219b-133">Payment methods define how you pay invoices from the vendor.</span></span> <span data-ttu-id="f219b-134">Maksutapa voi olla esimerkiksi pankki, käteinen, sekki tai tili.</span><span class="sxs-lookup"><span data-stu-id="f219b-134">For example, Bank, Cash, Check, or Account.</span></span>  
* <span data-ttu-id="f219b-135">Määritä kunkin pankkitilin käyttämän muodon tyyppi.</span><span class="sxs-lookup"><span data-stu-id="f219b-135">Specify the type of format to use for each of your bank accounts.</span></span> <span data-ttu-id="f219b-136">Tyyppi voi olla esimerkiksi NORDEA, DANSKEBANK tai SDC.</span><span class="sxs-lookup"><span data-stu-id="f219b-136">For example, NORDEA, DANSKEBANK, SDC, and so on.</span></span>  
  
<span data-ttu-id="f219b-137">Lisäksi on määritettävä toimittajat kotimaan **Ylein. liiketoim. kirjausryhmä**- ja **Toimittajan kirjausryhmä** -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="f219b-137">Additionally, you must assign vendors to a domestic **Gen. Bus. Posting Group** and a **Vendor Posting Group**.</span></span> <span data-ttu-id="f219b-138">Toimittajan maa-/alueasetukseksi on määritettävä Tanska (DK).</span><span class="sxs-lookup"><span data-stu-id="f219b-138">The Country/Region setting for the vendor must be Denmark (DK).</span></span> <span data-ttu-id="f219b-139">Lisätietoja on kohdassa [Kirjausryhmien määrittäminen](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="f219b-139">For more information, see [Setting Up Posting Groups](finance-posting-groups.md).</span></span>  
  
### <a name="to-allow-included365finincludesd365finmdmd-to-export-payment-data"></a><span data-ttu-id="f219b-140">[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman salliminen maksutietojen vientiä varten</span><span class="sxs-lookup"><span data-stu-id="f219b-140">To allow [!INCLUDE[d365fin](includes/d365fin_md.md)] to export payment data</span></span>
1. <span data-ttu-id="f219b-141">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksupäiväkirja** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f219b-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f219b-142">Valitse **Muokkaa maksupäiväkirjaa** -ikkunassa **Pankin** erä.</span><span class="sxs-lookup"><span data-stu-id="f219b-142">In the **Edit Payment Journal** window, choose the **Bank** batch.</span></span>  
3. <span data-ttu-id="f219b-143">Valitse **Salli maksun vienti** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f219b-143">Choose the **Allow Payment Export** check box.</span></span>  

### <a name="to-specify-a-payment-method-for-a-vendor"></a><span data-ttu-id="f219b-144">Toimittajan maksutavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f219b-144">To specify a payment method for a vendor</span></span>
<span data-ttu-id="f219b-145">Seuraavassa taulukossa ovat [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman tukemat FIK- ja TILISIIRTO-maksutapojen yhdistelmät.</span><span class="sxs-lookup"><span data-stu-id="f219b-145">The following table shows the combinations of FIK and GIRO payment methods that [!INCLUDE[d365fin](includes/d365fin_md.md)] supports.</span></span>

||<span data-ttu-id="f219b-146">Tyyppi 01</span><span class="sxs-lookup"><span data-stu-id="f219b-146">Type 01</span></span> | <span data-ttu-id="f219b-147">Tyyppi 04</span><span class="sxs-lookup"><span data-stu-id="f219b-147">Type 04</span></span> | <span data-ttu-id="f219b-148">Tyyppi 71</span><span class="sxs-lookup"><span data-stu-id="f219b-148">Type 71</span></span> | <span data-ttu-id="f219b-149">Tyyppi 73</span><span class="sxs-lookup"><span data-stu-id="f219b-149">Type 73</span></span> |
|----|---|---|---|---|
|<span data-ttu-id="f219b-150">Tilisiirron tilinro tai FIK:n luotonantajan nro?</span><span class="sxs-lookup"><span data-stu-id="f219b-150">Giro Account No. or FIK Creditor No.?</span></span> | <span data-ttu-id="f219b-151">Tilisiirron tilinro</span><span class="sxs-lookup"><span data-stu-id="f219b-151">Giro Account No.</span></span> | <span data-ttu-id="f219b-152">Tilisiirron tilinro</span><span class="sxs-lookup"><span data-stu-id="f219b-152">Giro Account No.</span></span> | <span data-ttu-id="f219b-153">FIK:n luotonantajan nro</span><span class="sxs-lookup"><span data-stu-id="f219b-153">FIK Creditor No.</span></span> | <span data-ttu-id="f219b-154">FIK:n luotonantajan nro</span><span class="sxs-lookup"><span data-stu-id="f219b-154">FIK Creditor No.</span></span>|
|<span data-ttu-id="f219b-155">Sallii viestin lähettämisen vastaanottajalle?</span><span class="sxs-lookup"><span data-stu-id="f219b-155">Allows Message to Recipient?</span></span> | <span data-ttu-id="f219b-156">Kyllä</span><span class="sxs-lookup"><span data-stu-id="f219b-156">Yes</span></span> |<span data-ttu-id="f219b-157">Ei</span><span class="sxs-lookup"><span data-stu-id="f219b-157">No</span></span> |<span data-ttu-id="f219b-158">Ei</span><span class="sxs-lookup"><span data-stu-id="f219b-158">No</span></span> | <span data-ttu-id="f219b-159">Kyllä</span><span class="sxs-lookup"><span data-stu-id="f219b-159">Yes</span></span> |
|<span data-ttu-id="f219b-160">Sisältää maksun viitenumeron?</span><span class="sxs-lookup"><span data-stu-id="f219b-160">Contains Payment Reference number?</span></span> | <span data-ttu-id="f219b-161">Ei</span><span class="sxs-lookup"><span data-stu-id="f219b-161">No</span></span> | <span data-ttu-id="f219b-162">Kyllä, 16 numeroa.</span><span class="sxs-lookup"><span data-stu-id="f219b-162">Yes, 16 digits.</span></span> | <span data-ttu-id="f219b-163">Kyllä, 15 numeroa.</span><span class="sxs-lookup"><span data-stu-id="f219b-163">Yes, 15 digits.</span></span> | <span data-ttu-id="f219b-164">Ei</span><span class="sxs-lookup"><span data-stu-id="f219b-164">No</span></span>|

1. <span data-ttu-id="f219b-165">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Toimittajat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f219b-165">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f219b-166">Avaa kortti, laajenna **Maksut**-välilehti ja valitse maksutapa **Maksutapa**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f219b-166">Open the card, expand the **Payments** tab, in the **Payment Method** field choose the payment method.</span></span>  
3. <span data-ttu-id="f219b-167">Täytä myös muita kenttiä valinnastasi riippuen.</span><span class="sxs-lookup"><span data-stu-id="f219b-167">Depending on your selection, you must complete other fields.</span></span> <span data-ttu-id="f219b-168">Yhdistelmien kuvaukset löytyvät yllä olevasta taulukosta.</span><span class="sxs-lookup"><span data-stu-id="f219b-168">See the table above for a description of the combinations.</span></span>  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a><span data-ttu-id="f219b-169">Pankkitilin käytettävän muodon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f219b-169">To specify the format to use for a bank account</span></span>
1. <span data-ttu-id="f219b-170">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Pankkitilit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f219b-170">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f219b-171">Avaa pankkitilin kortti.</span><span class="sxs-lookup"><span data-stu-id="f219b-171">Open the card for the bank account.</span></span>  
3. <span data-ttu-id="f219b-172">Valitse **Maksun vientimuoto** -kentässä vientitiedoston muoto.</span><span class="sxs-lookup"><span data-stu-id="f219b-172">In the **Payment Export Format** field, choose the format for your export file.</span></span>  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a><span data-ttu-id="f219b-173">Toimittajan laskujen FIK:n tai tilisiirron tietojen valitseminen</span><span class="sxs-lookup"><span data-stu-id="f219b-173">Choosing the FIK or Giro payment information for vendor invoices</span></span>
1. <span data-ttu-id="f219b-174">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostolaskut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f219b-174">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="f219b-175">Valitse toimittaja.</span><span class="sxs-lookup"><span data-stu-id="f219b-175">Choose the vendor.</span></span> <span data-ttu-id="f219b-176">Muista, että toimittajan on oltava tanskalainen, jolla on myös osoite Tanskassa.</span><span class="sxs-lookup"><span data-stu-id="f219b-176">Remember, this must be a Danish vendor with an address in Denmark.</span></span>
3. <span data-ttu-id="f219b-177">Luo lasku.</span><span class="sxs-lookup"><span data-stu-id="f219b-177">Create an invoice.</span></span> <span data-ttu-id="f219b-178">**Maksutapa**- ja **Toimittajan numero** -kentät täytetään toimittajan kortin asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="f219b-178">The **Payment Method** and **Vendor Number** fields are filled in based on settings on the Vendor card.</span></span> <span data-ttu-id="f219b-179">Voit halutessasi muuttaa tietoja.</span><span class="sxs-lookup"><span data-stu-id="f219b-179">You can change them if you want.</span></span>
4. <span data-ttu-id="f219b-180">Syötä **Maksuviittaus**-kenttään toimittajan laskun 15 numeron sarja.</span><span class="sxs-lookup"><span data-stu-id="f219b-180">In the **Payment Reference** field, enter the 15-digit number from the vendor invoice.</span></span>  
  
    > [!Tip]
    > <span data-ttu-id="f219b-181">Sinun on syötettävä numerosta vain 11 viimeistä numeroa.</span><span class="sxs-lookup"><span data-stu-id="f219b-181">You only have to add the last 11 digits of the number.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f219b-182"> lisää numeron alkuun neljä nollaa.</span><span class="sxs-lookup"><span data-stu-id="f219b-182"> will add four zeros to the beginning of the number.</span></span>  
  
5. <span data-ttu-id="f219b-183">Kirjaa lasku.</span><span class="sxs-lookup"><span data-stu-id="f219b-183">Post the invoice.</span></span>

## <a name="to-use-the-extension-to-export-payment-data"></a><span data-ttu-id="f219b-184">Laajennuksen käyttäminen maksutietojen viennissä</span><span class="sxs-lookup"><span data-stu-id="f219b-184">To use the extension to export payment data</span></span>
1. <span data-ttu-id="f219b-185">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksupäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f219b-185">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f219b-186">Valitse **Ehdota toimittajan maksupäiväkirjat** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f219b-186">Choose the **Suggest Vendor Payment Journals** action.</span></span>  
  
    > [!Tip]
    > <span data-ttu-id="f219b-187">Jos haluat viedä vain tietyt maksut, käytä tietojen suodatusta.</span><span class="sxs-lookup"><span data-stu-id="f219b-187">If you want to export only specific payments, use the options for filtering the data.</span></span>  
  
3. <span data-ttu-id="f219b-188">Voit tarvittaessa lisätä suodattimia, jos haluat viedä vain tietyt maksut.</span><span class="sxs-lookup"><span data-stu-id="f219b-188">If needed, you can add filters to export only specific payments.</span></span>  
4. <span data-ttu-id="f219b-189">Valitse **Pankkimaksun tyyppi** -kentässä **Sähköinen maksu**.</span><span class="sxs-lookup"><span data-stu-id="f219b-189">In the **Bank Payment Type** field, choose **Electronic Payment**.</span></span>  
5. <span data-ttu-id="f219b-190">Valitse **Vie**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="f219b-190">Choose the **Export** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f219b-191">Katso myös .</span><span class="sxs-lookup"><span data-stu-id="f219b-191">See also</span></span>
<span data-ttu-id="f219b-192">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in Finance and Operations, Business editionin mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="f219b-192">[Customizing Finance and Operations, Business edition for [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="f219b-193">SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon</span><span class="sxs-lookup"><span data-stu-id="f219b-193">Create SEPA Direct Debit Collection Entries and Export to a Bank File</span></span>](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
[<span data-ttu-id="f219b-194">SEPA-suoraveloituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f219b-194">Set Up SEPA Direct Debit</span></span>](finance-how-to-set-up-sepa-direct-debit.md)  
[<span data-ttu-id="f219b-195">SEPA-suoraveloitusmaksujen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="f219b-195">Post SEPA Direct Debit Payment Receipts</span></span>](finance-how-to-post-sepa-direct-debit-payment-receipts.md)  
[<span data-ttu-id="f219b-196">Maksujen kerääminen SEPA-suoraveloitusperintänä</span><span class="sxs-lookup"><span data-stu-id="f219b-196">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="f219b-197">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="f219b-197">Working with General Journals</span></span>](ui-work-general-journals.md)  





