---
ms.openlocfilehash: be7c632471ac5b26908ffb8f3e2b6313bc85aee7
ms.sourcegitcommit: e17cc64775307fcf15cef8e0181fdb046ccd227f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58265880"
---
<a name="save-your-collection-to-a-data-source"></a><span data-ttu-id="e39e1-101">Uložení kolekce do zdroje dat</span><span class="sxs-lookup"><span data-stu-id="e39e1-101">Save your collection to a data source</span></span>
-------------------------------------

<span data-ttu-id="e39e1-102">Kolekce jsou pouhé proměnné, takže jejich obsah se neuloží, pokud uživatel aplikaci zavře, a nikdo jiný, kdo aplikaci používá, nemá přístup k datům, která obsahují.</span><span class="sxs-lookup"><span data-stu-id="e39e1-102">Collections are just variables, so their contents aren't saved if the user closes the app, and anyone else running the app can't access any data that they contain.</span></span> <span data-ttu-id="e39e1-103">Pokud chcete informace v kolekci uložit, zapište je do zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="e39e1-103">To save the information in your collection, write it to a data source.</span></span> <span data-ttu-id="e39e1-104">Data se do kolekce ukládají dvěma základními způsoby.</span><span class="sxs-lookup"><span data-stu-id="e39e1-104">There are two primary ways of saving data in a collection.</span></span>

### <a name="use-the-collect-function"></a><span data-ttu-id="e39e1-105">Použití funkce Collect</span><span class="sxs-lookup"><span data-stu-id="e39e1-105">Use the Collect function</span></span>

<span data-ttu-id="e39e1-106">První metoda funguje dobře v případě, kdy názvy sloupců kolekce odpovídají těm ve zdroji dat.</span><span class="sxs-lookup"><span data-stu-id="e39e1-106">The first method works well if your collection's column names match those of the data source.</span></span> <span data-ttu-id="e39e1-107">Máte například kolekci s názvem collectMyFirstCollection, která obsahuje dva sloupce **Name** a **FavoriteColor**.</span><span class="sxs-lookup"><span data-stu-id="e39e1-107">For example, if you had a collection named collectMyFirstCollection that contains two columns, **Name** and **FavoriteColor**.</span></span> <span data-ttu-id="e39e1-108">Pokud byste měli zdroj dat s názvem **YourDataSource** a sloupci **Name** a **FavoriteColor**, mohli byste kolekci uložit pomocí této funkce:</span><span class="sxs-lookup"><span data-stu-id="e39e1-108">If you had a data source named **YourDataSource** with a **Name** and **FavoriteColor** column, you could save your collection by using this function:</span></span>

```
Collect(YourDataSource, collectMyFirstCollection)
```

<span data-ttu-id="e39e1-109">Při splnění těchto požadavků vytvoří tato funkce ve zdroji dat záznam pro každý záznam v této kolekci:</span><span class="sxs-lookup"><span data-stu-id="e39e1-109">If these requirements are met, that function creates a record in your data source for each record in the collection:</span></span>

-   <span data-ttu-id="e39e1-110">Všechny sloupce v kolekci musí existovat ve zdroji dat.</span><span class="sxs-lookup"><span data-stu-id="e39e1-110">All the columns in your collection must exist in the data source.</span></span>
    <span data-ttu-id="e39e1-111">Zdroj dat může mít další sloupce, ale sloupce v kolekci musí existovat.</span><span class="sxs-lookup"><span data-stu-id="e39e1-111">The data source can have additional columns, but the columns in your collection must be present.</span></span>

-   <span data-ttu-id="e39e1-112">Datový typ (například text, číslo nebo datum) všech sloupců v kolekci se musí shodovat se zdrojem dat.</span><span class="sxs-lookup"><span data-stu-id="e39e1-112">The data type (such as Text, Number, or Date) of each column in the collection must match the data source.</span></span>

-   <span data-ttu-id="e39e1-113">Zdroj dat nesmí mít povinné sloupce, které vaše kolekce neobsahuje.</span><span class="sxs-lookup"><span data-stu-id="e39e1-113">Your data source must not have required columns that your collection doesn't have.</span></span>

<span data-ttu-id="e39e1-114">**Tip:** V případě potřeby můžete pomocí těchto funkcí kolekci transformovat tak, aby se sloupce shodovaly se zdrojem dat.</span><span class="sxs-lookup"><span data-stu-id="e39e1-114">**Tip**: If necessary, you can use these functions to transform your collection so that the columns match your data source.</span></span>

-   <span data-ttu-id="e39e1-115">AddColumns</span><span class="sxs-lookup"><span data-stu-id="e39e1-115">AddColumns</span></span>

-   <span data-ttu-id="e39e1-116">DropColumns</span><span class="sxs-lookup"><span data-stu-id="e39e1-116">DropColumns</span></span>

-   <span data-ttu-id="e39e1-117">RenameColumns</span><span class="sxs-lookup"><span data-stu-id="e39e1-117">RenameColumns</span></span>

-   <span data-ttu-id="e39e1-118">ShowColumns</span><span class="sxs-lookup"><span data-stu-id="e39e1-118">ShowColumns</span></span>

<span data-ttu-id="e39e1-119">Další informace najdete v článku o [funkcích AddColumns, DropColumns, RenameColumns a ShowColumns v PowerApps](https://docs.microsoft.com/powerapps/maker/canvas-apps/functions/function-table-shaping).</span><span class="sxs-lookup"><span data-stu-id="e39e1-119">For more information, see [AddColumns, DropColumns, RenameColumns, and ShowColumns functions in PowerApps.](https://docs.microsoft.com/powerapps/maker/canvas-apps/functions/function-table-shaping)</span></span>

### <a name="patch-and-forall"></a><span data-ttu-id="e39e1-120">Funkce Patch a ForAll</span><span class="sxs-lookup"><span data-stu-id="e39e1-120">Patch and ForAll</span></span>

<span data-ttu-id="e39e1-121">**Patch** je funkce, která umožňuje změnit nebo vytvořit záznam ve zdroji dat.</span><span class="sxs-lookup"><span data-stu-id="e39e1-121">**Patch** is a function that allows you to modify or create a record in your data source.</span></span> <span data-ttu-id="e39e1-122">**ForAll** je funkce, která umožňuje provést vzorec u každého záznamu v tabulce, přičemž kolekce jsou tabulky.</span><span class="sxs-lookup"><span data-stu-id="e39e1-122">**ForAll** is a function that allows you to run a formula for each record in a table, and collections are tables.</span></span> <span data-ttu-id="e39e1-123">Kombinací těchto funkcí můžete zdroj dat aktualizovat obsahem vaší kolekce.</span><span class="sxs-lookup"><span data-stu-id="e39e1-123">You can combine these functions to update your data source with the contents of your collection.</span></span> <span data-ttu-id="e39e1-124">Tato strategie funguje, pokud chcete použít další logiku.</span><span class="sxs-lookup"><span data-stu-id="e39e1-124">This strategy works well when you want to apply additional logic.</span></span>

<span data-ttu-id="e39e1-125">Můžete například vytvořit kolekci s názvem collectColorData, která obsahuje tři sloupce: **Name**, **FavoriteColor** a **UpdateCDS**.</span><span class="sxs-lookup"><span data-stu-id="e39e1-125">For example, you could create a collection named collectColorData that contains three columns: **Name**, **FavoriteColor**, and **UpdateCDS**.</span></span>
<span data-ttu-id="e39e1-126">Sloupec **UpdateCDS** obsahuje logickou hodnotu (true nebo false).</span><span class="sxs-lookup"><span data-stu-id="e39e1-126">The **UpdateCDS** column could be a Boolean (true or false) column.</span></span>
<span data-ttu-id="e39e1-127">Během práce s aplikací uživatel aktualizuje hodnotu v tomto sloupci a pak vybere tlačítko s názvem **Update CDS**.</span><span class="sxs-lookup"><span data-stu-id="e39e1-127">Through the process of working with the app, the user would update the value in the column and then select a button that says **Update CDS**.</span></span>
<span data-ttu-id="e39e1-128">U vlastnosti **OnSelect** tohoto tlačítka nastavíte následující vzorec:</span><span class="sxs-lookup"><span data-stu-id="e39e1-128">You could set the **OnSelect** property for the button to this formula:</span></span>

```
ForAll(Filter(collectColorData, UpdateCDS = true),
Patch(DataSourceName, Defaults(DataSourceName), {NameColumnCDS: Name,
FavoriteColorColumnCDS: FavoriteColor})
```

<span data-ttu-id="e39e1-129">Tento vzorec přidá záznamy do zdroje dat s názvem **DataSourceName** a nastaví sloupce **NameColumnCDS** a **FavoriteColorColumnCDS** na hodnoty z vaší kolekce, ale jen u záznamů, kde byla ve sloupci **UpdateCDS** nastavena hodnota true.</span><span class="sxs-lookup"><span data-stu-id="e39e1-129">This formula would add records to the data source named **DataSourceName**, setting the **NameColumnCDS** and **FavoriteColorColumnCDS** columns with the values from your collection but only for the records where **UpdateCDS** was set to true.</span></span>

<span data-ttu-id="e39e1-130">Tento příklad by bylo možné dále optimalizovat, jeho účelem je ale demonstrovat tuto koncepci a příkazy pro dynamické uložení kolekce do zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="e39e1-130">This example could be further optimized, but it should demonstrate to you the concept and pieces for dynamically saving your collection to a data source.</span></span>
 
