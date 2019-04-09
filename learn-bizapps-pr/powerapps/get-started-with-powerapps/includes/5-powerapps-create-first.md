---
ms.openlocfilehash: 25a53eaced43793f10698f13f809622251eae875
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57697962"
---
<span data-ttu-id="30096-101">Pusťme se do toho.</span><span class="sxs-lookup"><span data-stu-id="30096-101">OK, let's get started.</span></span>

<span data-ttu-id="30096-102">Když teď znáte všechny části Microsoft PowerApps a možnosti pro vytváření aplikací, je čas nějakou aplikaci vytvořit.</span><span class="sxs-lookup"><span data-stu-id="30096-102">Now that you're familiar with all the parts of Microsoft PowerApps and the options for creating apps, it's time to actually build an app.</span></span> <span data-ttu-id="30096-103">V této lekci vygenerujete aplikaci pro telefon, jejímž zdrojem dat je sešit Microsoft Excelu uložený v Microsoft OneDrivu pro firmy.</span><span class="sxs-lookup"><span data-stu-id="30096-103">In this unit, you'll generate a phone app where the data source is a Microsoft Excel workbook that's stored in Microsoft OneDrive for Business.</span></span> <span data-ttu-id="30096-104">Tento excelový sešit obsahuje vzorky podlahových krytin společnosti, včetně jejich obrázků a cen.</span><span class="sxs-lookup"><span data-stu-id="30096-104">This Excel workbook lists a company's inventory of flooring samples with pictures and prices.</span></span>

<span data-ttu-id="30096-105">Mějte na paměti, že můžete použít data z mnoha jiných zdrojů, včetně Microsoft SharePointu, cloudových služeb jako Salesforce a místních zdrojů jako Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="30096-105">Keep in mind that you can use data from lots of other sources, including Microsoft SharePoint, cloud services like Salesforce, and on-premises sources like Microsoft SQL Server.</span></span>

> [!NOTE]
> <span data-ttu-id="30096-106">Tento tok bude fungovat jenom v případě, že máte licenci pro Office 365 a požadovanou licenci Dynamics 365 nebo bezplatnou zkušební verzi Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="30096-106">This flow will work only if you have a license for Office 365 and the required Dynamics 365 license or free Dynamics 365 trial.</span></span> <span data-ttu-id="30096-107">Podívejte se na další informace o tom, které [produkty Microsoft zahrnují Microsoft PowerApps a Microsoft Flow](https://docs.microsoft.com/powerapps/administrator/pricing-billing-skus#licenses).</span><span class="sxs-lookup"><span data-stu-id="30096-107">Learn more about which [Microsoft products include Microsoft PowerApps and Microsoft Flow](https://docs.microsoft.com/powerapps/administrator/pricing-billing-skus#licenses).”</span></span>


## <a name="connect-to-a-data-source"></a><span data-ttu-id="30096-108">Připojení ke zdroji dat</span><span class="sxs-lookup"><span data-stu-id="30096-108">Connect to a data source</span></span>

1. <span data-ttu-id="30096-109">Stáhněte si [sešit Flooring Estimates](https://az787822.vo.msecnd.net/documentation/get-started-from-data/FlooringEstimates.xlsx) a uložte si ho do OneDrivu pro firmy.</span><span class="sxs-lookup"><span data-stu-id="30096-109">Download the [Flooring Estimates workbook](https://az787822.vo.msecnd.net/documentation/get-started-from-data/FlooringEstimates.xlsx), and save it to OneDrive for Business.</span></span>

1. <span data-ttu-id="30096-110">Přejděte na [https://web.powerapps.com](https://web.powerapps.com) a přihlaste se pomocí účtu organizace.</span><span class="sxs-lookup"><span data-stu-id="30096-110">Go to [https://web.powerapps.com](https://web.powerapps.com), and sign in with your organizational account.</span></span>

1. <span data-ttu-id="30096-111">V levém podokně vyberte **Aplikace**.</span><span class="sxs-lookup"><span data-stu-id="30096-111">In the left pane, select **Apps**.</span></span>



1. <span data-ttu-id="30096-112">V rozevírací nabídce vyberte **Aplikace plátna od začátku**.</span><span class="sxs-lookup"><span data-stu-id="30096-112">Select **Canvas app from blank** from the dropdown menu</span></span>


1. <span data-ttu-id="30096-113">Vyberte **Vytvořit aplikaci**.</span><span class="sxs-lookup"><span data-stu-id="30096-113">Select **Create an app**.</span></span> 
1. <span data-ttu-id="30096-114">Pro zdroj dat **OneDrive pro firmy** vyberte **Rozložení pro telefon**.</span><span class="sxs-lookup"><span data-stu-id="30096-114">For the **OneDrive for Business** data source, select **Phone layout**.</span></span>

    ![Aplikace pro telefon ze sharepointového seznamu](../media/powerapps-start-excel.png)

    <span data-ttu-id="30096-116">Vygenerované aplikace jsou vždy založené na jednom seznamu nebo tabulce, ale další data můžete do aplikace přidat později.</span><span class="sxs-lookup"><span data-stu-id="30096-116">Generated apps are always based on a single list or table, but you can add more data to the app later.</span></span> <span data-ttu-id="30096-117">Následující tři kroky vysvětlují postup připojení k excelovému sešitu.</span><span class="sxs-lookup"><span data-stu-id="30096-117">The next three steps explain how to connect to the Excel workbook.</span></span>

1. <span data-ttu-id="30096-118">V části **Připojení** vyberte **OneDrive pro firmy**.</span><span class="sxs-lookup"><span data-stu-id="30096-118">Under **Connections**, select **OneDrive for Business**.</span></span>

    <span data-ttu-id="30096-119">Je možné, že abyste viděli připojení **OneDrive pro firmy**, budete muset vybrat **Nové připojení**.</span><span class="sxs-lookup"><span data-stu-id="30096-119">You may need to select **New Connection** to see the **OneDrive for Business** connection.</span></span>
1. <span data-ttu-id="30096-120">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="30096-120">Select **Create**.</span></span>
1. <span data-ttu-id="30096-121">V části **Zvolit excelový soubor** vyberte excelový sešit.</span><span class="sxs-lookup"><span data-stu-id="30096-121">Under **Choose an Excel file**, select the Excel workbook.</span></span>
1. <span data-ttu-id="30096-122">Vyberte **Připojit**.</span><span class="sxs-lookup"><span data-stu-id="30096-122">Select **Connect**.</span></span>

<span data-ttu-id="30096-123">PowerApps vygeneruje aplikaci tak, že zkontroluje vaše data a vyhodnotí odpovídající možnosti PowerApps, abyste získali funkční aplikaci jako výchozí bod.</span><span class="sxs-lookup"><span data-stu-id="30096-123">PowerApps generates the app by inspecting your data and matching it with PowerApps capabilities so that you get a working app as a starting point.</span></span>

<span data-ttu-id="30096-124">Mějte prosím na paměti, že abyste se dostali do PowerApps Studia, musíte zvolit náhled aplikace.</span><span class="sxs-lookup"><span data-stu-id="30096-124">Please note that you have to choose to preview the app before you can get to the PowerApps Studio.</span></span>

## <a name="explore-the-generated-app"></a><span data-ttu-id="30096-125">Prozkoumání vygenerované aplikace</span><span class="sxs-lookup"><span data-stu-id="30096-125">Explore the generated app</span></span>
<span data-ttu-id="30096-126">Výborně!</span><span class="sxs-lookup"><span data-stu-id="30096-126">Success!</span></span> <span data-ttu-id="30096-127">Vaše nová tříobrazovková aplikace se otevře v PowerApps Studiu.</span><span class="sxs-lookup"><span data-stu-id="30096-127">Your new three-screen app opens in PowerApps Studio.</span></span>

<span data-ttu-id="30096-128">Na levé straně uvidíte podokno **Obrazovky**.</span><span class="sxs-lookup"><span data-stu-id="30096-128">On the left, you'll see the **Screens** pane.</span></span> <span data-ttu-id="30096-129">V pravém horním rohu podokna obrazovek vyberte zobrazení miniatur.</span><span class="sxs-lookup"><span data-stu-id="30096-129">In the upper-right corner of the screens pane, select the thumbnail view.</span></span>

![Přepnutí zobrazení](../media/Powerapps-app-nav.png)

<span data-ttu-id="30096-131">Vybráním miniatury pro každou obrazovku zobrazíte ovládací prvky na této obrazovce.</span><span class="sxs-lookup"><span data-stu-id="30096-131">Select the thumbnail for each screen to view the controls on that screen.</span></span> 

<span data-ttu-id="30096-132">Tady je hlavní vývojářské okno PowerApps Studia, o kterém se dozvíte více v pozdějších modulech.</span><span class="sxs-lookup"><span data-stu-id="30096-132">Here is the main development window for PowerApps Studio, which you'll learn more about in later units.</span></span>

![Vygenerovaná aplikace](../media/powerapps-full-screen2.png)

<span data-ttu-id="30096-134">Pokud si chcete aplikaci vyzkoušet, vyberte v pravém horním rohu **Přehrát** ![Šipka pro spuštění náhledu aplikace](../media/powerapps-arrow.png).</span><span class="sxs-lookup"><span data-stu-id="30096-134">Select **Play** ![Start app preview arrow](../media/powerapps-arrow.png) in the upper-right corner to try out the app.</span></span> <span data-ttu-id="30096-135">Uvidíte, že zahrnuje všechna data ze seznamu a poskytuje dobré výchozí prostředí.</span><span class="sxs-lookup"><span data-stu-id="30096-135">You'll see that it includes all the data from the list and provides a good default experience.</span></span>

<span data-ttu-id="30096-136">Všechny aplikace vygenerované z dat mají stejnou sadu obrazovek, které si můžete prohlédnout v podokně miniatur:</span><span class="sxs-lookup"><span data-stu-id="30096-136">All apps generated from data have the same set of screens that you can view from the Thumbnail pane:</span></span>

* <span data-ttu-id="30096-137">**Obrazovka pro procházení:** Tato obrazovka se zobrazí jako výchozí.</span><span class="sxs-lookup"><span data-stu-id="30096-137">**Browse screen**: This screen appears by default.</span></span> <span data-ttu-id="30096-138">Můžete na ní procházet, řadit, filtrovat a aktualizovat data ze zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="30096-138">In it, you can browse, sort, filter, and refresh the data from the data source.</span></span> <span data-ttu-id="30096-139">Na obrazovce pro procházení můžete přidat položky do zdroje dat pomocí symbolu plus (**+**).</span><span class="sxs-lookup"><span data-stu-id="30096-139">In the browse screen, you add items to the data source by selecting the plus sign (**+**).</span></span>
* <span data-ttu-id="30096-140">**Obrazovka s podrobnostmi:** Když vyberete položku na obrazovce pro procházení, otevře se obrazovka s podrobnostmi. Ta zobrazuje všechny podrobnosti o položce.</span><span class="sxs-lookup"><span data-stu-id="30096-140">**Details screen**: Select an item in the browse screen to open the details screen, which shows all details about an item.</span></span> <span data-ttu-id="30096-141">Na této obrazovce můžete otevřít položku pro úpravy nebo ji odstranit.</span><span class="sxs-lookup"><span data-stu-id="30096-141">In this screen, you can open an item for editing or delete it.</span></span>
* <span data-ttu-id="30096-142">**Obrazovka pro úpravy nebo vytváření:** Na této obrazovce můžete upravit existující položku nebo vytvořit novou.</span><span class="sxs-lookup"><span data-stu-id="30096-142">**Edit/create screen**: In this screen, you edit an existing item, or you create one.</span></span>

<span data-ttu-id="30096-143">Aby aplikace byla viditelná na telefonu, musí se uložit.</span><span class="sxs-lookup"><span data-stu-id="30096-143">To make your app visible on the phone it needs to be saved.</span></span> <span data-ttu-id="30096-144">Klikněte na **Soubor**, **Uložit jako** a zadejte název „flooring-estimates app“.</span><span class="sxs-lookup"><span data-stu-id="30096-144">Click **File**, **Save as** with the title "flooring-estimates app".</span></span> <span data-ttu-id="30096-145">Po úspěšném uložení všech změn se zobrazí zelená značka zaškrtnutí.</span><span class="sxs-lookup"><span data-stu-id="30096-145">You will see green checkmark when all changes are successfully saved.</span></span>
<span data-ttu-id="30096-146">Teď otevřete aplikaci **PowerApps** na telefonu a vyberte „flooring-estimates app“.</span><span class="sxs-lookup"><span data-stu-id="30096-146">Now open **PowerApps** app on your phone and select "flooring-estimates app".</span></span> <span data-ttu-id="30096-147">Pokud tuto aplikaci nemůžete najít, vyzkoušejte režim hledání v rámci PowerApps na mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="30096-147">If you cannot find the app try search mode within the PowerApps on your mobile device.</span></span>

## <a name="install-the-app-on-your-device"></a><span data-ttu-id="30096-148">Instalace aplikace do zařízení</span><span class="sxs-lookup"><span data-stu-id="30096-148">Install the app on your device</span></span>
<span data-ttu-id="30096-149">Svoji aplikaci si asi budete chtít nainstalovat do telefonu, abyste viděli, jak tam vypadá.</span><span class="sxs-lookup"><span data-stu-id="30096-149">You'll want to install your app on your phone to see how it looks there.</span></span>

1. <span data-ttu-id="30096-150">Stáhněte si aplikaci PowerApps Mobile z obchodu s aplikacemi pro platformu, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="30096-150">Download PowerApps Mobile from the app store for the platform that you want to use.</span></span>

2. <span data-ttu-id="30096-151">Přihlaste se pomocí svého uživatelského jména a hesla.</span><span class="sxs-lookup"><span data-stu-id="30096-151">Sign in by using your user name and password.</span></span>

3. <span data-ttu-id="30096-152">Na telefonu nebo tabletu spusťte v PowerApps Mobile aplikaci flooring-estimates.</span><span class="sxs-lookup"><span data-stu-id="30096-152">On your phone or tablet, run the flooring-estimates app in PowerApps Mobile.</span></span> <span data-ttu-id="30096-153">Další možností je spustit aplikaci v prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="30096-153">Otherwise, run the app in a browser.</span></span>

<span data-ttu-id="30096-154">Během několik málo minut jste zjistili, jak se připojit ke zdroji dat a vygenerovat aplikaci.</span><span class="sxs-lookup"><span data-stu-id="30096-154">In just a few minutes, you learned how to connect to a data source and generate an app.</span></span> <span data-ttu-id="30096-155">Seznámili jste se také s PowerApps Studiem a třemi obrazovkami ve vygenerované aplikaci.</span><span class="sxs-lookup"><span data-stu-id="30096-155">You also got acquainted with PowerApps Studio and the three screens in a generated app.</span></span> <span data-ttu-id="30096-156">V dalších modulech se dozvíte, jak vygenerované aplikace přizpůsobit.</span><span class="sxs-lookup"><span data-stu-id="30096-156">In later modules, you'll learn how to customize generated apps.</span></span>
