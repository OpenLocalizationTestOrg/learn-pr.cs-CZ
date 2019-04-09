---
ms.openlocfilehash: 05ce85f2b0d1efdaafe9180e4193191a0f8c3283
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698849"
---
<span data-ttu-id="d1111-101">V této lekci uvidíte, jak Contoso Flooring pomocí Microsoft Flow automaticky převádí dokumenty na standardní formát a pak je ukládá do Microsoft SharePointu Online.</span><span class="sxs-lookup"><span data-stu-id="d1111-101">In this unit, you'll see how Contoso Flooring uses Microsoft Flow to automatically convert documents to a standard format and then store them in Microsoft SharePoint Online.</span></span> <span data-ttu-id="d1111-102">Vytvoříte tok, který zjistí, že do složky OneDrivu pro firmy byl přidán nový soubor.</span><span class="sxs-lookup"><span data-stu-id="d1111-102">You'll create a flow that detects when a new file has been added to a Microsoft OneDrive for Business folder.</span></span> <span data-ttu-id="d1111-103">Tok potom převede tento soubor do formátu PDF a uloží ho do složky SharePointu Online.</span><span class="sxs-lookup"><span data-stu-id="d1111-103">The flow then converts that file to a PDF and stores it in a SharePoint Online folder.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d1111-104">Požadavky</span><span class="sxs-lookup"><span data-stu-id="d1111-104">Prerequisites</span></span>

<span data-ttu-id="d1111-105">Pro tento scénář potřebujete účet Muhimbi (služba pro převod PDF).</span><span class="sxs-lookup"><span data-stu-id="d1111-105">For this scenario, you need an account with Muhimbi, a PDF conversion service.</span></span> <span data-ttu-id="d1111-106">Pokud ještě účet Muhimbi nemáte, můžete si zaregistrovat [zkušební verzi na 30 dnů zdarma](http://www.muhimbi.com/Products/PDF-Converter-for-SharePoint/Products-PDF-Converter-for-SharePoint-Free-Trial.aspx).</span><span class="sxs-lookup"><span data-stu-id="d1111-106">If you don't already have a Muhimbi account, you can sign up for a [free 30-day trial](http://www.muhimbi.com/Products/PDF-Converter-for-SharePoint/Products-PDF-Converter-for-SharePoint-Free-Trial.aspx).</span></span>

## <a name="create-the-source-and-target-folders"></a><span data-ttu-id="d1111-107">Vytvoření zdrojové a cílové složky</span><span class="sxs-lookup"><span data-stu-id="d1111-107">Create the source and target folders</span></span>

<span data-ttu-id="d1111-108">Nejprve musíte vytvořit zdrojovou a cílovou složku ve OneDrivu pro firmy a v SharePointu Online.</span><span class="sxs-lookup"><span data-stu-id="d1111-108">First, you must create the source and target folders in OneDrive for Business and SharePoint Online.</span></span>

1. <span data-ttu-id="d1111-109">Ve OneDrivu pro firmy v části **Soubory** vytvořte složku s názvem **Dokončené dokumenty**.</span><span class="sxs-lookup"><span data-stu-id="d1111-109">In OneDrive for Business, under **Files**, create a folder named **Finished Documents**.</span></span>
2. <span data-ttu-id="d1111-110">V SharePointu Online v části **Sdílené dokumenty** vytvořte složku s názvem **PDF – dokončené soubory**.</span><span class="sxs-lookup"><span data-stu-id="d1111-110">In SharePoint Online, in **Shared Documents**, create a folder named **PDF – Finished files**.</span></span>

## <a name="create-the-flow"></a><span data-ttu-id="d1111-111">Vytvoření toku</span><span class="sxs-lookup"><span data-stu-id="d1111-111">Create the flow</span></span>

1. <span data-ttu-id="d1111-112">V Microsoft Flow vyberte **Moje toky** a pak vyberte **Vytvořit z prázdné**.</span><span class="sxs-lookup"><span data-stu-id="d1111-112">In Microsoft Flow, select **My Flows**, and then select **Create from blank**.</span></span>

    ![Vytvořit z prázdné](../media/flow-create-blank.png)

2. <span data-ttu-id="d1111-114">Vyberte **Prohledat stovky konektorů a triggerů**.</span><span class="sxs-lookup"><span data-stu-id="d1111-114">Select **Search hundreds of connectors and triggers**.</span></span>
3. <span data-ttu-id="d1111-115">Do vyhledávacího pole zadejte *onedrive*, vyberte konektor **OneDrive pro firmy** a pak vyberte trigger **OneDrive pro firmy – Když je vytvořen soubor**.</span><span class="sxs-lookup"><span data-stu-id="d1111-115">In the search field, enter *onedrive*, select the **OneDrive for Business** connector, and then select the **OneDrive for Business - When a file is created** trigger.</span></span> <span data-ttu-id="d1111-116">V poli **Složka** vyberte tlačítko složky a pak vyberte složku **Dokončené dokumenty**, kterou jste vytvořili v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="d1111-116">In the **Folder** field, select the folder button, and then select the **Finished Documents** folder that you created in the previous step.</span></span>

    ![Trigger OneDrive pro firmy – Když je vytvořen soubor](../media/onedrive-trigger.png)

4. <span data-ttu-id="d1111-118">Vyberte **Nový krok** a pak vyberte **Přidat akci**.</span><span class="sxs-lookup"><span data-stu-id="d1111-118">Select **New step**, and then select **Add an action**.</span></span>

    ![Přidat akci](../media/new-action.png)

5. <span data-ttu-id="d1111-120">Do vyhledávacího pole zadejte *muhimbi*, vyberte konektor **Muhimbi PDF** a pak vyberte akci **Muhimbi PDF – Convert document** (Převést dokument).</span><span class="sxs-lookup"><span data-stu-id="d1111-120">In the search box, enter *muhimbi*, select the **Muhimbi PDF** connector, and then select the **Muhimbi PDF – Convert document** action.</span></span>

    ![Akce Muhimbi PDF – Convert document (Převést dokument)](../media/muhimbi-action.png)

6. <span data-ttu-id="d1111-122">Pokud vás Microsoft Flow vyzve k přihlášení k Muhimbi, přihlaste se.</span><span class="sxs-lookup"><span data-stu-id="d1111-122">If Microsoft Flow prompts you to sign in to Muhimbi, sign in.</span></span> <span data-ttu-id="d1111-123">Pokud předplatné Muhimbi nemáte, můžete použít [zkušební verzi na 30 dnů zdarma](http://www.muhimbi.com/Products/PDF-Converter-for-SharePoint/Products-PDF-Converter-for-SharePoint-Free-Trial.aspx).</span><span class="sxs-lookup"><span data-stu-id="d1111-123">If you don't have a subscription to Muhimbi, you can use a [free 30-day trial](http://www.muhimbi.com/Products/PDF-Converter-for-SharePoint/Products-PDF-Converter-for-SharePoint-Free-Trial.aspx).</span></span>
7. <span data-ttu-id="d1111-124">V akci **Convert document** (Převést dokument) nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d1111-124">In the **Convert document** action, set the following values:</span></span>

    * <span data-ttu-id="d1111-125">**Source file name** (Název zdrojového souboru): V seznamu dynamického obsahu vyberte **Název souboru**.</span><span class="sxs-lookup"><span data-stu-id="d1111-125">**Source file name**: In the dynamic content list, select **File name**.</span></span>
    * <span data-ttu-id="d1111-126">**Source file content** (Obsah zdrojového souboru): V seznamu dynamického obsahu vyberte **Obsah souboru**.</span><span class="sxs-lookup"><span data-stu-id="d1111-126">**Source file content**: In the dynamic content list, select **File content**.</span></span>
    * <span data-ttu-id="d1111-127">**Output format** (Výstupní formát): Vyberte *PDF*.</span><span class="sxs-lookup"><span data-stu-id="d1111-127">**Output format**: Select *PDF*.</span></span>

    ![Nastavení Muhimbi](../media/muhimbi-configuration.png)

    <span data-ttu-id="d1111-129">Zatím jste pro tok nastavili tyto kroky:</span><span class="sxs-lookup"><span data-stu-id="d1111-129">So far, you've set up these steps for your flow:</span></span>

    1. <span data-ttu-id="d1111-130">Tok se aktivuje vždy, když se do určité složky OneDrivu pro firmy přidá nový soubor.</span><span class="sxs-lookup"><span data-stu-id="d1111-130">The flow is triggered whenever a new file is added to a specific OneDrive for Business folder.</span></span>
    2. <span data-ttu-id="d1111-131">Služba Muhimbi převede daný soubor do formátu PDF.</span><span class="sxs-lookup"><span data-stu-id="d1111-131">The Muhimbi service converts that file to PDF.</span></span>

    <span data-ttu-id="d1111-132">Jako poslední krok přidáte akci, která přesune daný dokument PDF do složky SharePointu Online, kde k němu tým bude mít přístup.</span><span class="sxs-lookup"><span data-stu-id="d1111-132">For the final step, you'll add an action that moves the PDF document to a SharePoint Online folder where the team can access it.</span></span>

8. <span data-ttu-id="d1111-133">Vyberte **Nový krok** a pak vyberte **Přidat akci**.</span><span class="sxs-lookup"><span data-stu-id="d1111-133">Select **New step**, and then select **Add an action**.</span></span>
9. <span data-ttu-id="d1111-134">Do vyhledávacího pole zadejte *sharepoint* a pak vyberte akci **SharePoint – Vytvořit soubor**.</span><span class="sxs-lookup"><span data-stu-id="d1111-134">In the search field, enter *sharepoint*, and then select the **SharePoint – Create file** action.</span></span>

    ![Akce SharePoint – Vytvořit soubor](../media/sharepoint-create-file.png)

10. <span data-ttu-id="d1111-136">V akci **Vytvořit soubor** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d1111-136">In the **Create file** action, set the following values:</span></span>

    * <span data-ttu-id="d1111-137">**Adresa webu**: Zadejte adresu URL vašeho sharepointového webu.</span><span class="sxs-lookup"><span data-stu-id="d1111-137">**Site address**: Enter the URL of your SharePoint site.</span></span>
    * <span data-ttu-id="d1111-138">**Cesta ke složce**: Vyberte tlačítko složky a přejděte ke složce **PDF – dokončené soubory**.</span><span class="sxs-lookup"><span data-stu-id="d1111-138">**Folder path**: Select the folder button, and browse to the **PDF - Finished files** folder.</span></span>
    * <span data-ttu-id="d1111-139">**Název souboru**: V seznamu dynamického obsahu v části **Convert document** (Převést dokument) vyberte **Base file name** (Základní název souboru).</span><span class="sxs-lookup"><span data-stu-id="d1111-139">**File name**: In the dynamic content list, under **Convert document**, select **Base file name**.</span></span> <span data-ttu-id="d1111-140">Pak zadejte *.pdf*, aby se soubor na SharePointu uložil s příponou názvu souboru .pdf.</span><span class="sxs-lookup"><span data-stu-id="d1111-140">Then enter *.pdf* so that the file will be saved with the .pdf file name extension in SharePoint.</span></span>
    * <span data-ttu-id="d1111-141">**Obsah souboru**: V seznamu dynamického obsahu v části **Convert document** (Převést dokument) vyberte **Processed file content** (Zpracovaný obsah souboru).</span><span class="sxs-lookup"><span data-stu-id="d1111-141">**File content**: In the dynamic content list, under **Convert document**, select **Processed file content**.</span></span>

    ![Nastavení souboru na SharePointu](../media/sharepoint-configure-file.png)

11. <span data-ttu-id="d1111-143">Uložte práci výběrem možnosti **Vytvořit tok** v horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="d1111-143">Select **Create flow** at the top of the page to save your work.</span></span>

## <a name="test-the-flow"></a><span data-ttu-id="d1111-144">Testování toku</span><span class="sxs-lookup"><span data-stu-id="d1111-144">Test the flow</span></span>

1. <span data-ttu-id="d1111-145">Pokud chcete tok otestovat, přidejte nový soubor do složky **Dokončené dokumenty** ve OneDrivu pro firmy.</span><span class="sxs-lookup"><span data-stu-id="d1111-145">To test the flow, add a new file to your **Finished Documents** folder in OneDrive for Business.</span></span>
2. <span data-ttu-id="d1111-146">V Microsoft Flow vyberte **Moje toky** a pak výběrem nového toku zobrazte historii spuštění.</span><span class="sxs-lookup"><span data-stu-id="d1111-146">In Microsoft Flow, select **My flows**, and then select the new flow to view the run history.</span></span> <span data-ttu-id="d1111-147">Ve výchozím nastavení je tok nastavený tak, aby se spouštěl každých pět minut.</span><span class="sxs-lookup"><span data-stu-id="d1111-147">By default, the flow is set up to run every five minutes.</span></span>
3. <span data-ttu-id="d1111-148">Po spuštění toku se ujistěte, jestli se daný soubor převedl do formátu PDF a uložil do složky **PDF – dokončené soubory** na SharePointu.</span><span class="sxs-lookup"><span data-stu-id="d1111-148">After the flow runs, make sure that the file was converted to a PDF and saved to the **PDF – Finished files** folder in SharePoint.</span></span>
