---
ms.openlocfilehash: 6e9abcedc4962f1701d59629aef3a3021addbb37
ms.sourcegitcommit: e17cc64775307fcf15cef8e0181fdb046ccd227f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58265888"
---
<span data-ttu-id="417ee-101">V předchozích příkladech se tabulky daly používat jen v aktuálním kontextu tabulky **Data** nebo ovládacího prvku **Rozevírací seznam**.</span><span class="sxs-lookup"><span data-stu-id="417ee-101">In the previous examples the tables were only for use in the current context of the **Data** table or the **Dropdown** control.</span></span> <span data-ttu-id="417ee-102">V aplikaci budete často potřebovat tyto tabulky ukládat a používat na různých místech aplikace.</span><span class="sxs-lookup"><span data-stu-id="417ee-102">Often in your app, you will need to store those tables and use them in multiple places within the app.</span></span> <span data-ttu-id="417ee-103">Pro tyto účely obsahuje PowerApps tabulkovou proměnnou, která se označuje jako **kolekce**.</span><span class="sxs-lookup"><span data-stu-id="417ee-103">To do this, PowerApps has a table variable called a **collection**.</span></span>

<a name="collections-are-a-type-of-variable-in-powerapps"></a><span data-ttu-id="417ee-104">Kolekce jsou v PowerApps typem proměnné</span><span class="sxs-lookup"><span data-stu-id="417ee-104">Collections are a type of variable in PowerApps</span></span>
-----------------------------------------------

<span data-ttu-id="417ee-105">Kolekce jsou tabulkové proměnné, ve kterých můžete ukládat data ve strukturovaném formátu stejně jako v tabulkovém zdroji dat, ale bez zápisu do zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="417ee-105">Collections are table variables in which you can store data in a structured format, as you would in a tabular data source, without writing to a data source.</span></span> <span data-ttu-id="417ee-106">Kolekce jinými slovy slouží k uložení hodnot v řádcích a sloupcích.</span><span class="sxs-lookup"><span data-stu-id="417ee-106">In other words, they store values in rows and columns.</span></span> <span data-ttu-id="417ee-107">Kolekce můžete používat s tabulkovými funkcemi stejně jako kterýkoli jiný zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="417ee-107">You can use collections with table functions as you would any other data source.</span></span> <span data-ttu-id="417ee-108">Kolekci ale nemůžete použít s ovládacím prvkem **Formulář**.</span><span class="sxs-lookup"><span data-stu-id="417ee-108">However, you can't use a collection with the **Form** control.</span></span> <span data-ttu-id="417ee-109">Pokud máte zkušenosti s vývojem, můžete kolekci považovat za pole.</span><span class="sxs-lookup"><span data-stu-id="417ee-109">If you have a developer background, you can think of a collection as an array.</span></span> <span data-ttu-id="417ee-110">Kolekci není nutné inicializovat ani předem definovat.</span><span class="sxs-lookup"><span data-stu-id="417ee-110">You don't have to initialize or predefine a collection.</span></span> <span data-ttu-id="417ee-111">Když ji vytvoříte a nastavíte hodnoty, PowerApps ji za vás zřídí.</span><span class="sxs-lookup"><span data-stu-id="417ee-111">When you create it and set values, PowerApps sets it up for you.</span></span>

<a name="create-a-collection"></a><span data-ttu-id="417ee-112">Vytvoření kolekce</span><span class="sxs-lookup"><span data-stu-id="417ee-112">Create a collection</span></span>
-------------------

<span data-ttu-id="417ee-113">Pomocí tohoto vzorce můžete vytvořit kolekci s názvem **collectMyFirstCollection**.</span><span class="sxs-lookup"><span data-stu-id="417ee-113">You can create a collection named **collectMyFirstCollection** by using this formula.</span></span>

```
Collect(collectMyFirstCollection, {Name: "Shane", FavoriteColor:"Orange"})
```

<span data-ttu-id="417ee-114">Tato kolekce by měla sloupec s názvem **Name** a další sloupec s názvem **FavoriteColor**.</span><span class="sxs-lookup"><span data-stu-id="417ee-114">The collection would have a column named **Name** and another column named **FavoriteColor**.</span></span> <span data-ttu-id="417ee-115">Kolekce by obsahovala jeden záznam (řádek) dat, ve kterém má **Name** hodnotu Shane a **FavoriteColor** hodnotu Orange.</span><span class="sxs-lookup"><span data-stu-id="417ee-115">The collection would have one record (row) of data with Shane as the value of **Name** and Orange as the value for **FavoriteColor**.</span></span> <span data-ttu-id="417ee-116">Všimněte si, že syntaxe je velmi podobná funkci **Table**, kterou jsme probrali dříve v tomto modulu.</span><span class="sxs-lookup"><span data-stu-id="417ee-116">Notice the syntax is very similar to the **Table** function from earlier in this module.</span></span>

<span data-ttu-id="417ee-117">Pomocí tohoto vzorce můžete do kolekce přidat další záznam.</span><span class="sxs-lookup"><span data-stu-id="417ee-117">You could add another record to the collection by using this formula.</span></span>

```
Collect(collectMyFirstCollection, {Name: "Nicola", FavoriteColor:"Purple"})
```

<span data-ttu-id="417ee-118">Tímto vzorcem můžete také přidat více než jeden záznam najednou.</span><span class="sxs-lookup"><span data-stu-id="417ee-118">You can also add more than one record at a time by using this formula.</span></span>

```
Collect(collectMyFirstCollection, {Name: "Jeff", FavoriteColor:"Blue"}, {Name: "Chewy", FavoriteColor: "Red"})
```

<span data-ttu-id="417ee-119">Po spuštění všech těchto příkazů by kolekce vypadala jako tato tabulka:</span><span class="sxs-lookup"><span data-stu-id="417ee-119">If you ran all those commands, your collection would look like this table:</span></span>

| <span data-ttu-id="417ee-120">Name</span><span class="sxs-lookup"><span data-stu-id="417ee-120">Name</span></span>                  | <span data-ttu-id="417ee-121">FavoriteColor</span><span class="sxs-lookup"><span data-stu-id="417ee-121">FavoriteColor</span></span>                 |
| :------------------- | :--------------------|
| <span data-ttu-id="417ee-122">Shane</span><span class="sxs-lookup"><span data-stu-id="417ee-122">Shane</span></span>  | <span data-ttu-id="417ee-123">Orange</span><span class="sxs-lookup"><span data-stu-id="417ee-123">Orange</span></span> |
| <span data-ttu-id="417ee-124">Nicola</span><span class="sxs-lookup"><span data-stu-id="417ee-124">Nicola</span></span>                 | <span data-ttu-id="417ee-125">Purple</span><span class="sxs-lookup"><span data-stu-id="417ee-125">Purple</span></span>                 |
| <span data-ttu-id="417ee-126">Jeff</span><span class="sxs-lookup"><span data-stu-id="417ee-126">Jeff</span></span>                  | <span data-ttu-id="417ee-127">Blue</span><span class="sxs-lookup"><span data-stu-id="417ee-127">Blue</span></span>                  |
| <span data-ttu-id="417ee-128">Chewy</span><span class="sxs-lookup"><span data-stu-id="417ee-128">Chewy</span></span>                   | <span data-ttu-id="417ee-129">Red</span><span class="sxs-lookup"><span data-stu-id="417ee-129">Red</span></span>                   |


<span data-ttu-id="417ee-130">Tuto kolekci pak můžete použít jako zdroj dat pro ovládací prvek **Galerie** nebo **Rozevírací seznam**.</span><span class="sxs-lookup"><span data-stu-id="417ee-130">You could then use that collection as a data source for your **Gallery** or **Drop-down** control.</span></span>

<a name="remove-data-from-your-collection"></a><span data-ttu-id="417ee-131">Odebrání dat z kolekce</span><span class="sxs-lookup"><span data-stu-id="417ee-131">Remove data from your collection</span></span>
--------------------------------

<span data-ttu-id="417ee-132">Pomocí funkce **ClearCollect** můžete z kolekce před přidáním dat vymazat existující data.</span><span class="sxs-lookup"><span data-stu-id="417ee-132">To clear out the existing data from your collection before you add data, you can use the **ClearCollect** function.</span></span> <span data-ttu-id="417ee-133">Při použití existující kolekce z předchozího příkladu můžete použít tento vzorec:</span><span class="sxs-lookup"><span data-stu-id="417ee-133">If you take the existing collection from the previous example, you can use this formula:</span></span>

```
ClearCollect(collectMyFirstCollection, {Name: "Fausto", FavoriteColor:"Green"})
```

<span data-ttu-id="417ee-134">Kolekce by teď měla vypadat jako tato tabulka:</span><span class="sxs-lookup"><span data-stu-id="417ee-134">Now your collection would look like this table:</span></span>

| <span data-ttu-id="417ee-135">Name</span><span class="sxs-lookup"><span data-stu-id="417ee-135">Name</span></span>                  | <span data-ttu-id="417ee-136">FavoriteColor</span><span class="sxs-lookup"><span data-stu-id="417ee-136">FavoriteColor</span></span>                 |
| :------------------- | :--------------------|
| <span data-ttu-id="417ee-137">Fausto</span><span class="sxs-lookup"><span data-stu-id="417ee-137">Fausto</span></span>  | <span data-ttu-id="417ee-138">Green</span><span class="sxs-lookup"><span data-stu-id="417ee-138">Green</span></span> |

<span data-ttu-id="417ee-139">Pomocí funkce **Clear** můžete z kolekce také odebrat všechny záznamy.</span><span class="sxs-lookup"><span data-stu-id="417ee-139">You can also remove all the records from a collection by using the **Clear** function.</span></span> <span data-ttu-id="417ee-140">Tento vzorec odebere z kolekce všechny záznamy, ale sloupce ponechá beze změny:</span><span class="sxs-lookup"><span data-stu-id="417ee-140">This formula removes all the records from your collection but leaves your columns intact:</span></span>

```
Clear(collectMyFirstCollection)
``` 
