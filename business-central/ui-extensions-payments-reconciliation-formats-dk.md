---
title: Maksujen ja täsmäytysten (DK) laajennuksen käyttäminen | Microsoft Docs
description: Tämän laajennuksen avulla on helppo viedä esimuotoiltuja tiedostoja, jotka täyttävät pankin sähköisiä lähetyksiä koskevat vaatimukset.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 06/19/2020
ms.author: bholtorf
ms.openlocfilehash: 7e8a56492c1c848f4f3b371e1411c11f159c3cf3
ms.sourcegitcommit: 6200a08e91d507bab01d1d5b805fe8ea3f44a58a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2020
ms.locfileid: "3496748"
---
# <a name="the-payments-and-reconciliations-dk-extension"></a><span data-ttu-id="71d13-103">Maksujen ja täsmäytysten (DK) laajennus</span><span class="sxs-lookup"><span data-stu-id="71d13-103">The Payments and Reconciliations (DK) Extension</span></span>

<span data-ttu-id="71d13-104">Tee nopeita ja virheettömiä maksuja tuomalla tiedostot, jotka on muotoiltu erityisesti toimittajan tai pankin kanssa tapahtuvia siirtoja varten.</span><span class="sxs-lookup"><span data-stu-id="71d13-104">Make fast, error-free payments by exporting files that are formatted specifically for exchanges with your vendor or bank.</span></span> <span data-ttu-id="71d13-105">Nämä tiedostot nopeuttavat maksu- ja täsmäytysprosesseja ja eliminoivat virheet, joita voi tapahtua tietojen manuaalisessa syöttämisessä pankin sivustossa.</span><span class="sxs-lookup"><span data-stu-id="71d13-105">These files speed up the payment and reconciliation processes, and eliminate errors that can happen when you manually enter the information on a bank website.</span></span>  

<span data-ttu-id="71d13-106">Tämä laajennus tukee useiden Tanskan pankkien tiedostomuotoja.</span><span class="sxs-lookup"><span data-stu-id="71d13-106">This extension supports file formats for several Danish banks.</span></span> <span data-ttu-id="71d13-107">Kun vietä maksutiedot tiedostoon, laajennus pakkaa tiedot pankin vaatimaan muotoon.</span><span class="sxs-lookup"><span data-stu-id="71d13-107">When you export payment information to a file, the extension packages the data into the format that your bank requires.</span></span> <span data-ttu-id="71d13-108">Muotoja ovat esimerkiksi Bankdata-V3, BEC, SDC ja FIK, joita useat pankit käyttävät. Jotkin pankit, kuten Danske Bank ja Nordea, käyttävät erikoismuotoja.</span><span class="sxs-lookup"><span data-stu-id="71d13-108">For example, the formats include Bankdata-V3, BEC, SDC, and FIK, which many different banks use, and some that are more specialized for certain banks, for example, Danske Bank and Nordea.</span></span> <span data-ttu-id="71d13-109">Laajennus sisältää myös muotoja tiliotteiden tuontia ja täsmäytystä varten.</span><span class="sxs-lookup"><span data-stu-id="71d13-109">The extension also includes some formats for importing and reconciling bank statements.</span></span>  

> [!Note]
> <span data-ttu-id="71d13-110">Sinun tulee tietää pankin tai toimittajan vaatima muoto, jotta voit käyttää laajennusta.</span><span class="sxs-lookup"><span data-stu-id="71d13-110">To use the extension, you must know the format that your bank or vendor requires.</span></span> <span data-ttu-id="71d13-111">Jotkin pankit ja toimittajat kertovat tämän tiedon verkkosivustoillaan. Joissakin tapauksissa tieto on pyydettävä pankin tai toimittajan asiakaspalvelusta.</span><span class="sxs-lookup"><span data-stu-id="71d13-111">Some banks or vendors provide this information on their websites; however, you might need to contact their customer service to get the information.</span></span>  

## <a name="supported-bank-formats"></a><span data-ttu-id="71d13-112">Tuetut pankin muodot</span><span class="sxs-lookup"><span data-stu-id="71d13-112">Supported Bank Formats</span></span>
<span data-ttu-id="71d13-113">Tätä laajennusta voi käyttää seuraavissa maksutiedostojen muodoissa:</span><span class="sxs-lookup"><span data-stu-id="71d13-113">This extension can apply the following file formats for payment files:</span></span>  

* <span data-ttu-id="71d13-114">BANKDATA-V3</span><span class="sxs-lookup"><span data-stu-id="71d13-114">BANKDATA-V3</span></span>  
* <span data-ttu-id="71d13-115">BEC-INDLAND</span><span class="sxs-lookup"><span data-stu-id="71d13-115">BEC-INDLAND</span></span>  
* <span data-ttu-id="71d13-116">BEC-CSV</span><span class="sxs-lookup"><span data-stu-id="71d13-116">BEC-CSV</span></span>  
* <span data-ttu-id="71d13-117">DANSKEBANK-CMKV</span><span class="sxs-lookup"><span data-stu-id="71d13-117">DANSKEBANK-CMKV</span></span>  
* <span data-ttu-id="71d13-118">DANSKEBANK-CMKXKSX</span><span class="sxs-lookup"><span data-stu-id="71d13-118">DANSKEBANK-CMKXKSX</span></span>  
* <span data-ttu-id="71d13-119">DANSKEBANK</span><span class="sxs-lookup"><span data-stu-id="71d13-119">DANSKEBANK</span></span>  
* <span data-ttu-id="71d13-120">FIK71</span><span class="sxs-lookup"><span data-stu-id="71d13-120">FIK71</span></span>  
* <span data-ttu-id="71d13-121">NORDEA-ERHVERV-CSV</span><span class="sxs-lookup"><span data-stu-id="71d13-121">NORDEA-ERHVERV-CSV</span></span>  
* <span data-ttu-id="71d13-122">NORDEA</span><span class="sxs-lookup"><span data-stu-id="71d13-122">NORDEA</span></span>  
* <span data-ttu-id="71d13-123">NORDEA-UNITEL-V3</span><span class="sxs-lookup"><span data-stu-id="71d13-123">NORDEA-UNITEL-V3</span></span>  
* <span data-ttu-id="71d13-124">SDC</span><span class="sxs-lookup"><span data-stu-id="71d13-124">SDC</span></span>  
* <span data-ttu-id="71d13-125">SDC-CSV</span><span class="sxs-lookup"><span data-stu-id="71d13-125">SDC-CSV</span></span>  

## <a name="to-set-up-the-extension"></a><span data-ttu-id="71d13-126">Laajennuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="71d13-126">To set up the extension</span></span>

<span data-ttu-id="71d13-127">Aloittaminen edellyttää muutamien vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="71d13-127">There are a few steps to get started.</span></span>  

* <span data-ttu-id="71d13-128">Salli maksutietojen viennit.</span><span class="sxs-lookup"><span data-stu-id="71d13-128">Allow payment data exports.</span></span> <span data-ttu-id="71d13-129">Tätä ei ole sallittu oletusarvoisesti tietoturvan vuoksi.</span><span class="sxs-lookup"><span data-stu-id="71d13-129">To help protect your data, this is not readily available.</span></span>  
* <span data-ttu-id="71d13-130">Määritä ostot ja ostovelat niin, että laskuissa ei tarvita ulkoisten asiakirjojen numeroita.</span><span class="sxs-lookup"><span data-stu-id="71d13-130">Set up purchase and payables so that you do not require external document numbers on invoices.</span></span> <span data-ttu-id="71d13-131">Voit tarvittaessa käyttää viitenumeroa, kun viittaat tiettyyn laskuun.</span><span class="sxs-lookup"><span data-stu-id="71d13-131">If needed, you can use the reference number to refer to a specific invoice.</span></span>  
* <span data-ttu-id="71d13-132">Määritä kunkin toimittajan maksutapa.</span><span class="sxs-lookup"><span data-stu-id="71d13-132">Specify the payment method for each vendor.</span></span> <span data-ttu-id="71d13-133">Maksutavat määrittävät, miten maksat toimittajien laskut.</span><span class="sxs-lookup"><span data-stu-id="71d13-133">Payment methods define how you pay invoices from the vendor.</span></span> <span data-ttu-id="71d13-134">Maksutapa voi olla esimerkiksi pankki, käteinen, sekki tai tili.</span><span class="sxs-lookup"><span data-stu-id="71d13-134">For example, Bank, Cash, Check, or Account.</span></span>  
* <span data-ttu-id="71d13-135">Määritä kunkin pankkitilin käyttämän muodon tyyppi.</span><span class="sxs-lookup"><span data-stu-id="71d13-135">Specify the type of format to use for each of your bank accounts.</span></span> <span data-ttu-id="71d13-136">Tyyppi voi olla esimerkiksi NORDEA, DANSKEBANK tai SDC.</span><span class="sxs-lookup"><span data-stu-id="71d13-136">For example, NORDEA, DANSKEBANK, SDC, and so on.</span></span>  

<span data-ttu-id="71d13-137">Lisäksi on määritettävä toimittajat kotimaan **Ylein. liiketoim. kirjausryhmä**- ja **Toimittajan kirjausryhmä** -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="71d13-137">Additionally, you must assign vendors to a domestic **Gen. Bus. Posting Group** and a **Vendor Posting Group**.</span></span> <span data-ttu-id="71d13-138">Toimittajan maa-/alueasetukseksi on määritettävä Tanska (DK).</span><span class="sxs-lookup"><span data-stu-id="71d13-138">The Country/Region setting for the vendor must be Denmark (DK).</span></span> <span data-ttu-id="71d13-139">Lisätietoja on kohdassa [Kirjausryhmien määrittäminen](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="71d13-139">For more information, see [Setting Up Posting Groups](finance-posting-groups.md).</span></span>  

### <a name="to-allow-d365fin-to-export-payment-data"></a><span data-ttu-id="71d13-140">[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman salliminen maksutietojen vientiä varten</span><span class="sxs-lookup"><span data-stu-id="71d13-140">To allow [!INCLUDE[d365fin](includes/d365fin_md.md)] to export payment data</span></span>

1. <span data-ttu-id="71d13-141">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="71d13-141">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="71d13-142">Valitse **Muokkaa maksupäiväkirjaa** -sivulla **Pankin** erä.</span><span class="sxs-lookup"><span data-stu-id="71d13-142">On the **Edit Payment Journal** page, choose the **Bank** batch.</span></span>  
3. <span data-ttu-id="71d13-143">Valitse **Salli maksun vienti** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="71d13-143">Choose the **Allow Payment Export** check box.</span></span>  

### <a name="to-specify-a-payment-method-for-a-vendor"></a><span data-ttu-id="71d13-144">Toimittajan maksutavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="71d13-144">To specify a payment method for a vendor</span></span>

<span data-ttu-id="71d13-145">Seuraavassa taulukossa ovat [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman tukemat FIK- ja TILISIIRTO-maksutapojen yhdistelmät.</span><span class="sxs-lookup"><span data-stu-id="71d13-145">The following table shows the combinations of FIK and GIRO payment methods that [!INCLUDE[d365fin](includes/d365fin_md.md)] supports.</span></span>

|<span data-ttu-id="71d13-146">Yhdistelmä</span><span class="sxs-lookup"><span data-stu-id="71d13-146">Combination</span></span>|<span data-ttu-id="71d13-147">Tyyppi 01</span><span class="sxs-lookup"><span data-stu-id="71d13-147">Type 01</span></span> | <span data-ttu-id="71d13-148">Tyyppi 04</span><span class="sxs-lookup"><span data-stu-id="71d13-148">Type 04</span></span> | <span data-ttu-id="71d13-149">Tyyppi 71</span><span class="sxs-lookup"><span data-stu-id="71d13-149">Type 71</span></span> | <span data-ttu-id="71d13-150">Tyyppi 73</span><span class="sxs-lookup"><span data-stu-id="71d13-150">Type 73</span></span> |
|----|--------|---------|---------|---------|
|<span data-ttu-id="71d13-151">Tilisiirron tilinro tai FIK:n luotonantajan nro?</span><span class="sxs-lookup"><span data-stu-id="71d13-151">Giro Account No. or FIK Creditor No.?</span></span> | <span data-ttu-id="71d13-152">Tilisiirron tilinro</span><span class="sxs-lookup"><span data-stu-id="71d13-152">Giro Account No.</span></span> | <span data-ttu-id="71d13-153">Tilisiirron tilinro</span><span class="sxs-lookup"><span data-stu-id="71d13-153">Giro Account No.</span></span> | <span data-ttu-id="71d13-154">FIK:n luotonantajan nro</span><span class="sxs-lookup"><span data-stu-id="71d13-154">FIK Creditor No.</span></span> | <span data-ttu-id="71d13-155">FIK:n luotonantajan nro</span><span class="sxs-lookup"><span data-stu-id="71d13-155">FIK Creditor No.</span></span>|
|<span data-ttu-id="71d13-156">Sallii viestin lähettämisen vastaanottajalle?</span><span class="sxs-lookup"><span data-stu-id="71d13-156">Allows Message to Recipient?</span></span> | <span data-ttu-id="71d13-157">Kyllä</span><span class="sxs-lookup"><span data-stu-id="71d13-157">Yes</span></span> |<span data-ttu-id="71d13-158">Ei</span><span class="sxs-lookup"><span data-stu-id="71d13-158">No</span></span> |<span data-ttu-id="71d13-159">Ei</span><span class="sxs-lookup"><span data-stu-id="71d13-159">No</span></span> | <span data-ttu-id="71d13-160">Kyllä</span><span class="sxs-lookup"><span data-stu-id="71d13-160">Yes</span></span> |
|<span data-ttu-id="71d13-161">Sisältää maksun viitenumeron?</span><span class="sxs-lookup"><span data-stu-id="71d13-161">Contains Payment Reference number?</span></span> | <span data-ttu-id="71d13-162">Ei</span><span class="sxs-lookup"><span data-stu-id="71d13-162">No</span></span> | <span data-ttu-id="71d13-163">Kyllä, 16 numeroa.</span><span class="sxs-lookup"><span data-stu-id="71d13-163">Yes, 16 digits.</span></span> | <span data-ttu-id="71d13-164">Kyllä, 15 numeroa.</span><span class="sxs-lookup"><span data-stu-id="71d13-164">Yes, 15 digits.</span></span> | <span data-ttu-id="71d13-165">Ei</span><span class="sxs-lookup"><span data-stu-id="71d13-165">No</span></span>|

1. <span data-ttu-id="71d13-166">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="71d13-166">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="71d13-167">Avaa kortti, laajenna **Maksut**-välilehti ja valitse maksutapa **Maksutapa**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="71d13-167">Open the card, expand the **Payments** tab, in the **Payment Method** field choose the payment method.</span></span>  
3. <span data-ttu-id="71d13-168">Täytä myös muita kenttiä valinnastasi riippuen.</span><span class="sxs-lookup"><span data-stu-id="71d13-168">Depending on your selection, you must complete other fields.</span></span> <span data-ttu-id="71d13-169">Yhdistelmien kuvaukset löytyvät yllä olevasta taulukosta.</span><span class="sxs-lookup"><span data-stu-id="71d13-169">See the table above for a description of the combinations.</span></span>  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a><span data-ttu-id="71d13-170">Pankkitilin käytettävän muodon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="71d13-170">To specify the format to use for a bank account</span></span>

1. <span data-ttu-id="71d13-171">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="71d13-171">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="71d13-172">Avaa pankkitilin kortti.</span><span class="sxs-lookup"><span data-stu-id="71d13-172">Open the card for the bank account.</span></span>  
3. <span data-ttu-id="71d13-173">Valitse **Maksun vientimuoto** -kentässä vientitiedoston muoto.</span><span class="sxs-lookup"><span data-stu-id="71d13-173">In the **Payment Export Format** field, choose the format for your export file.</span></span>  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a><span data-ttu-id="71d13-174">Toimittajan laskujen FIK:n tai tilisiirron tietojen valitseminen</span><span class="sxs-lookup"><span data-stu-id="71d13-174">Choosing the FIK or Giro payment information for vendor invoices</span></span>

1. <span data-ttu-id="71d13-175">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Ostolaskut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="71d13-175">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="71d13-176">Valitse toimittaja.</span><span class="sxs-lookup"><span data-stu-id="71d13-176">Choose the vendor.</span></span> <span data-ttu-id="71d13-177">Muista, että toimittajan on oltava tanskalainen, jolla on myös osoite Tanskassa.</span><span class="sxs-lookup"><span data-stu-id="71d13-177">Remember, this must be a Danish vendor with an address in Denmark.</span></span>
3. <span data-ttu-id="71d13-178">Luo lasku.</span><span class="sxs-lookup"><span data-stu-id="71d13-178">Create an invoice.</span></span> <span data-ttu-id="71d13-179">**Maksutapa**- ja **Toimittajan numero** -kentät täytetään toimittajan kortin asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="71d13-179">The **Payment Method** and **Vendor Number** fields are filled in based on settings on the Vendor card.</span></span> <span data-ttu-id="71d13-180">Voit halutessasi muuttaa tietoja.</span><span class="sxs-lookup"><span data-stu-id="71d13-180">You can change them if you want.</span></span>
4. <span data-ttu-id="71d13-181">Syötä **Maksuviittaus**-kenttään toimittajan laskun 15 numeron sarja.</span><span class="sxs-lookup"><span data-stu-id="71d13-181">In the **Payment Reference** field, enter the 15-digit number from the vendor invoice.</span></span>  

    > [!Tip]
    > <span data-ttu-id="71d13-182">Sinun on syötettävä numerosta vain 11 viimeistä numeroa.</span><span class="sxs-lookup"><span data-stu-id="71d13-182">You only have to add the last 11 digits of the number.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="71d13-183">lisää numeron alkuun neljä nollaa.</span><span class="sxs-lookup"><span data-stu-id="71d13-183">will add four zeros to the beginning of the number.</span></span>  

5. <span data-ttu-id="71d13-184">Kirjaa lasku.</span><span class="sxs-lookup"><span data-stu-id="71d13-184">Post the invoice.</span></span>

## <a name="to-use-the-extension-to-export-payment-data"></a><span data-ttu-id="71d13-185">Laajennuksen käyttäminen maksutietojen viennissä</span><span class="sxs-lookup"><span data-stu-id="71d13-185">To use the extension to export payment data</span></span>

1. <span data-ttu-id="71d13-186">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="71d13-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="71d13-187">Valitse **Ehdota toimittajan maksupäiväkirjat** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="71d13-187">Choose the **Suggest Vendor Payment Journals** action.</span></span>  

    > [!Tip]
    > <span data-ttu-id="71d13-188">Jos haluat viedä vain tietyt maksut, käytä tietojen suodatusta.</span><span class="sxs-lookup"><span data-stu-id="71d13-188">If you want to export only specific payments, use the options for filtering the data.</span></span>  

3. <span data-ttu-id="71d13-189">Voit tarvittaessa lisätä suodattimia, jos haluat viedä vain tietyt maksut.</span><span class="sxs-lookup"><span data-stu-id="71d13-189">If needed, you can add filters to export only specific payments.</span></span>  
4. <span data-ttu-id="71d13-190">Valitse **Pankkimaksun tyyppi** -kentässä **Sähköinen maksu**.</span><span class="sxs-lookup"><span data-stu-id="71d13-190">In the **Bank Payment Type** field, choose **Electronic Payment**.</span></span>  
5. <span data-ttu-id="71d13-191">Valitse **Vie**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="71d13-191">Choose the **Export** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="71d13-192">Katso myös .</span><span class="sxs-lookup"><span data-stu-id="71d13-192">See also</span></span>

<span data-ttu-id="71d13-193">[Business Central -sovelluksen mukauttaminen [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaa varten laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="71d13-193">[Customizing Business Central for [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="71d13-194">Maksujen kerääminen SEPA-suoraveloitusperintänä.</span><span class="sxs-lookup"><span data-stu-id="71d13-194">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="71d13-195">Yleisten päiväkirjojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="71d13-195">Working with General Journals</span></span>](ui-work-general-journals.md)  
