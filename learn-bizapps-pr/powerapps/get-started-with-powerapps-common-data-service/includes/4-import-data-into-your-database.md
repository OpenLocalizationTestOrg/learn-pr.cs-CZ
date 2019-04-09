---
ms.openlocfilehash: e9e6b90aed472b73796ddf25163f172e8c0adba1
ms.sourcegitcommit: d4531d76c2cc5030d9fd2c39f3c6c73ce8768841
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/26/2019
ms.locfileid: "58473966"
---
<span data-ttu-id="631f2-101">Data můžete importovat do databáze Common Data Service pro aplikace hromadně z Microsoft Excelu nebo ze souborů CSV.</span><span class="sxs-lookup"><span data-stu-id="631f2-101">You can import data into your Common Data Service for Apps database in bulk from Microsoft Excel or CSV files.</span></span> 

<span data-ttu-id="631f2-102">Každá entita obsahuje povinná pole, která musí ve vstupním souboru existovat.</span><span class="sxs-lookup"><span data-stu-id="631f2-102">Every entity has required fields that must exist in your input file.</span></span> <span data-ttu-id="631f2-103">Doporučujeme vytvořit šablonu.</span><span class="sxs-lookup"><span data-stu-id="631f2-103">We recommend that you create a template.</span></span> <span data-ttu-id="631f2-104">Šablona vám ušetří čas a úsilí.</span><span class="sxs-lookup"><span data-stu-id="631f2-104">A template will save you time and effort.</span></span> <span data-ttu-id="631f2-105">Nejprve vyexportujte data z entity.</span><span class="sxs-lookup"><span data-stu-id="631f2-105">First, export data from the entity.</span></span> <span data-ttu-id="631f2-106">Stejný soubor (aktualizovaný vašimi daty) pak použijete pro import dat do entity.</span><span class="sxs-lookup"><span data-stu-id="631f2-106">You'll use the same file (updated with your data) to import data into the entity.</span></span>

## <a name="create-a-file-template"></a><span data-ttu-id="631f2-107">Vytvoření šablony souboru</span><span class="sxs-lookup"><span data-stu-id="631f2-107">Create a file template</span></span>
<span data-ttu-id="631f2-108">Můžete provést jednorázový export dat ze standardní entity nebo vlastní entity nebo můžete data exportovat z několika entit najednou.</span><span class="sxs-lookup"><span data-stu-id="631f2-108">You can do a one-time data export from a standard entity or a custom entity, and you can export data from more than one entity at a time.</span></span> <span data-ttu-id="631f2-109">Pokud exportujete data z více než jedné entity, každá entita se exportuje do vlastního souboru Microsoft CSV.</span><span class="sxs-lookup"><span data-stu-id="631f2-109">If you export data from more than one entity, each entity is exported into its own Microsoft CSV file.</span></span> <span data-ttu-id="631f2-110">V tomto příkladu vytvoříte šablony pro entity **Domácí mazlíček** a **Obchodní vztah**.</span><span class="sxs-lookup"><span data-stu-id="631f2-110">In this example, you'll create templates for both the **Pet** and **Account** entities.</span></span>

1. <span data-ttu-id="631f2-111">Na webu [powerapps.com](https://web.powerapps.com/) v seznamu **Entity** vyberte napravo ikonu **dalších příkazů** (\*\* ... \*\*) a potom vyberte **Exportovat data**.</span><span class="sxs-lookup"><span data-stu-id="631f2-111">On [powerapps.com](https://web.powerapps.com/), in the **Entities** list, select the **More commands** icon (\*\* ... \*\*) on the right, and then select **Export data**.</span></span>
1. <span data-ttu-id="631f2-112">Vyberte entity **Obchodní vztah** a **Domácí mazlíček** a pak vyberte **Exportovat data**.</span><span class="sxs-lookup"><span data-stu-id="631f2-112">Select the **Account** and **Pet** entities, and then select **Export data**.</span></span>
1. <span data-ttu-id="631f2-113">Po dokončení exportu vyberte **Stáhnout exportovaná data** a uložte soubory.</span><span class="sxs-lookup"><span data-stu-id="631f2-113">After the export is finished, select **Download exported data**, and save the files.</span></span>

## <a name="copy-data-into-your-template"></a><span data-ttu-id="631f2-114">Kopírování dat do šablony</span><span class="sxs-lookup"><span data-stu-id="631f2-114">Copy data into your template</span></span>
<span data-ttu-id="631f2-115">Při přidání dat do souboru šablony se musíte ujistit, že jsou data jedinečná.</span><span class="sxs-lookup"><span data-stu-id="631f2-115">When you add data to a template file, you must make sure the data is unique.</span></span> <span data-ttu-id="631f2-116">Můžete použít buď *primární klíče* nebo *alternativní klíče*.</span><span class="sxs-lookup"><span data-stu-id="631f2-116">You can use either *primary keys* or *alternate keys*.</span></span>

1. <span data-ttu-id="631f2-117">Otevřete soubory CSV, které jste vytvořili v předchozí části.</span><span class="sxs-lookup"><span data-stu-id="631f2-117">Open the CSV files that you created in the previous section.</span></span>
1. <span data-ttu-id="631f2-118">Přidejte aspoň jeden řádek nových dat.</span><span class="sxs-lookup"><span data-stu-id="631f2-118">Add at least one new row of data.</span></span>
1. <span data-ttu-id="631f2-119">Soubor uložte.</span><span class="sxs-lookup"><span data-stu-id="631f2-119">Save the file.</span></span>

## <a name="import-the-file"></a><span data-ttu-id="631f2-120">Import souboru</span><span class="sxs-lookup"><span data-stu-id="631f2-120">Import the file</span></span>
1. <span data-ttu-id="631f2-121">V levém navigačním podokně rozbalte **Data** a pak vyberte **Entity**.</span><span class="sxs-lookup"><span data-stu-id="631f2-121">In the left navigation pane, expand **Data**, and then select **Entities**.</span></span>
1. <span data-ttu-id="631f2-122">Vyberte entitu **Domácí mazlíček**, vyberte **Získat data** a pak vyberte **Získat data z Excelu**.</span><span class="sxs-lookup"><span data-stu-id="631f2-122">Select the **Pet** entity, select **Get Data**, and then select **Get data from Excel**.</span></span>
1. <span data-ttu-id="631f2-123">Vyberte soubor, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="631f2-123">Select the file that you created.</span></span>
1. <span data-ttu-id="631f2-124">Po nahrání souboru a když pole **Stav mapování** označuje, že mapování bylo úspěšné, vyberte v pravém horním rohu **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="631f2-124">After the file is uploaded, and the **Mapping status** field indicates that mapping was successful, select **Import** in the upper-right corner.</span></span>

   
    ![Příklad pole Stav mapování a tlačítko Importovat pro úspěšné nahrání](../media/success-map-imp.png)

1. <span data-ttu-id="631f2-126">Po úspěšném importu se zobrazí celkový počet vložení a aktualizací.</span><span class="sxs-lookup"><span data-stu-id="631f2-126">After the import is successful, you'll see the total number of inserts and updates.</span></span>
