---
ms.openlocfilehash: 9da5cedcc3ab2db40079906fbdf15ee131b9c261
ms.sourcegitcommit: e17cc64775307fcf15cef8e0181fdb046ccd227f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58265885"
---
<span data-ttu-id="fec62-101">Funkce jako Filter a Search se používají k úpravám vrácených záznamů, ale někdy je potřeba upravit sloupce záznamů během používání těchto záznamů.</span><span class="sxs-lookup"><span data-stu-id="fec62-101">Functions like Filter and Search are used to modify the returned records, but sometimes you need to modify the columns of the records while using the records.</span></span> <span data-ttu-id="fec62-102">Pokud například vytváříte aplikaci nákupního košíku, která zákazníkovi bude odesílat digitální prostředky, potřebujete způsob, jak vybrané prostředky sledovat.</span><span class="sxs-lookup"><span data-stu-id="fec62-102">For example, if you were creating a shopping cart app for sending digital assets to a customer, you would need a way to keep track of the selected assets.</span></span> <span data-ttu-id="fec62-103">V ideálním případě byste ke sledování vybraných záznamů měli dočasný sloupec, který existuje jenom v PowerApps a neupravuje původní zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="fec62-103">Ideally, you would have a temporary column for tracking the selected records that only exists inside of PowerApps and does not modify the original data source.</span></span>
<span data-ttu-id="fec62-104">PowerApps naštěstí nabízí řešení.</span><span class="sxs-lookup"><span data-stu-id="fec62-104">Fortunately, PowerApps offers a solution.</span></span>

<span data-ttu-id="fec62-105">V PowerApps se nachází řada funkcí, které upravují sloupce tabulky jenom v rámci PowerApps, což znamená, že neprovádějí úpravy nebo změny ve skutečném zdroji dat.</span><span class="sxs-lookup"><span data-stu-id="fec62-105">With PowerApps there a series of columns that modify the columns of your table only within PowerApps, which means that they don't modify or change the actual data source.</span></span> <span data-ttu-id="fec62-106">Tyto funkce jsou:</span><span class="sxs-lookup"><span data-stu-id="fec62-106">Those functions are:</span></span>

-   <span data-ttu-id="fec62-107">AddColumns</span><span class="sxs-lookup"><span data-stu-id="fec62-107">AddColumns</span></span>

-   <span data-ttu-id="fec62-108">DropColumns</span><span class="sxs-lookup"><span data-stu-id="fec62-108">DropColumns</span></span>

-   <span data-ttu-id="fec62-109">RenameColumns</span><span class="sxs-lookup"><span data-stu-id="fec62-109">RenameColumns</span></span>

-   <span data-ttu-id="fec62-110">ShowColumns</span><span class="sxs-lookup"><span data-stu-id="fec62-110">ShowColumns</span></span>

<a name="addcolumns"></a><span data-ttu-id="fec62-111">AddColumns</span><span class="sxs-lookup"><span data-stu-id="fec62-111">AddColumns</span></span>
----------

<span data-ttu-id="fec62-112">Funkce **AddColumns** přidá do tabulky sloupec a vzorec definuje hodnoty v tomto sloupci.</span><span class="sxs-lookup"><span data-stu-id="fec62-112">The **AddColumns** function adds a column to a table, and a formula defines the values in that column.</span></span> <span data-ttu-id="fec62-113">Stávající sloupce zůstanou nezměněné.</span><span class="sxs-lookup"><span data-stu-id="fec62-113">Existing columns remain unmodified.</span></span>

<span data-ttu-id="fec62-114">V předchozím příkladu aplikace nákupního košíku byste pomocí funkce **AddColumns** přidali sloupec pro sledování, když uživatel vybere daný sloupec.</span><span class="sxs-lookup"><span data-stu-id="fec62-114">For the previous example of a shopping cart app, you would use the **AddColumns** function to add a column for tracking if the user selected the column.</span></span> <span data-ttu-id="fec62-115">Provedli byste to nastavením následujícího vzorce pro vlastnost **OnSelect** u ovládacího prvku **tlačítka**.</span><span class="sxs-lookup"><span data-stu-id="fec62-115">You would do this by setting the following formula for the **OnSelect** property for a **Button** control.</span></span>

```
ClearCollect(collectDigitalAssets, AddColumns(YourDataSource,"UserSelected", false))
```

<span data-ttu-id="fec62-116">Při výběru tohoto tlačítka vzorec vytvoří kolekci s názvem **collectDigitalAssets**, která obsahuje všechny záznamy ze zdroje **YourDataSource**, a přidá sloupec **UserSelected**.</span><span class="sxs-lookup"><span data-stu-id="fec62-116">When this button is selected, the formula creates a collection named **collectDigitalAssets** that has all of the records from **YourDataSource** and adds the column, "**UserSelected**".</span></span> <span data-ttu-id="fec62-117">Hodnota tohoto sloupce ve všech záznamech je **false**.</span><span class="sxs-lookup"><span data-stu-id="fec62-117">The column value is **false** for all of the records.</span></span>

<span data-ttu-id="fec62-118">Nyní v ovládacím prvku **galerie** nastavte vlastnost **items** následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="fec62-118">Now in your **Gallery** control, set the **items** property to the following.</span></span>

<span data-ttu-id="fec62-119">**collectDigitalAssets**</span><span class="sxs-lookup"><span data-stu-id="fec62-119">**collectDigitalAssets**</span></span>

<span data-ttu-id="fec62-120">V ovládacím prvku **galerie** budete mít přístup ke sloupci s názvem **UserSelected** a jeho hodnota bude false.</span><span class="sxs-lookup"><span data-stu-id="fec62-120">In the **Gallery** control, you would have access to a column named **UserSelected** and the value would be false.</span></span> <span data-ttu-id="fec62-121">Do galerie pak můžete přidat tlačítko, jehož vlastnost **OnSelect** mění hodnotu v daném sloupci na true.</span><span class="sxs-lookup"><span data-stu-id="fec62-121">You could then add a button into your Gallery that **OnSelect** would patch the column to true.</span></span>

```
Patch(collectDigitalAssets, ThisItem, {UserSelected: true})
```

<span data-ttu-id="fec62-122">Nyní v kolekci **collectDigitalAssets** sledujete záznamy, které uživatel vybral v aplikaci, bez úprav sloupců ve zdroji dat.</span><span class="sxs-lookup"><span data-stu-id="fec62-122">Now in the **collectDigitalAssets** collection you are tracking the records the user has selected in your app without modifying the columns in your data source.</span></span>

<a name="dropcolumns"></a><span data-ttu-id="fec62-123">DropColumns</span><span class="sxs-lookup"><span data-stu-id="fec62-123">DropColumns</span></span>
-----------

<span data-ttu-id="fec62-124">Funkce **DropColumns** funguje opačně než funkce AddColumns.</span><span class="sxs-lookup"><span data-stu-id="fec62-124">The **DropColumns** function works the opposite of AddColumns.</span></span> <span data-ttu-id="fec62-125">Tato funkce slouží k odebrání sloupců z tabulky v PowerApps.</span><span class="sxs-lookup"><span data-stu-id="fec62-125">The function is used to remove columns from the table within PowerApps.</span></span> <span data-ttu-id="fec62-126">Tuto funkci použijete, když chcete v PowerApps vytvořit kolekci, která má několik sloupců pro funkce aplikace.</span><span class="sxs-lookup"><span data-stu-id="fec62-126">This function is used when you want to create a collection within PowerApps that has several columns for app functionality.</span></span> <span data-ttu-id="fec62-127">Tyto sloupce se přidají do kolekce jenom pro funkce aplikace a nebudou se odesílat do zdroje dat, a proto je potřeba použít funkci **DropColumns**, která při odesílání do zdroje dat příslušné sloupce odebere.</span><span class="sxs-lookup"><span data-stu-id="fec62-127">Because these columns will be added only in the collection for app functionality and not submitted to the data source, the **DropColumns** function is needed to remove the column upon submission to the data source.</span></span>

<span data-ttu-id="fec62-128">Například pro použití v aplikaci pro sledování času vytvořte kolekci s názvem **collectTimeTracking**.</span><span class="sxs-lookup"><span data-stu-id="fec62-128">For example, you create a collection name **collectTimeTracking** to use in a time tracking application.</span></span> <span data-ttu-id="fec62-129">Kolekce má pět sloupců: Name, HoursWorked, DateWorked, LastScreen a Status.</span><span class="sxs-lookup"><span data-stu-id="fec62-129">The collection has five columns: Name, HoursWorked, DateWorked, LastScreen, and Status.</span></span> <span data-ttu-id="fec62-130">Ve sloupcích **Name**, **HoursWorked** a **DateWorked** se sledují data, která se mají ukládat do zdroje **YourDataSource** podle hodin, které daný zaměstnanec odpracoval.</span><span class="sxs-lookup"><span data-stu-id="fec62-130">The columns **Name**, **HoursWorked**, and **DateWorked** track the data to save to **YourDataSource** based on hours an employee worked.</span></span> <span data-ttu-id="fec62-131">Ve sloupcích **LastScreen** a **Status** se ukládají data pro funkce aplikace v době, kdy uživatelé aplikaci používají.</span><span class="sxs-lookup"><span data-stu-id="fec62-131">The columns **LastScreen** and **Status** store data to provide app functionality while the users is using the app.</span></span>

<span data-ttu-id="fec62-132">Jedním ze způsobů, jak po dokončení činnosti uživatele uložit informace zpět do zdroje dat, je použití funkce **Vytvořit kolekci**.</span><span class="sxs-lookup"><span data-stu-id="fec62-132">When the user is done, one way to save the information back to a data source is to use the **Collect** function.</span></span> <span data-ttu-id="fec62-133">Pokud sloupce odpovídají zdroji dat, funkce **Vytvořit kolekci** zapíše všechny záznamy do kolekce.</span><span class="sxs-lookup"><span data-stu-id="fec62-133">If the columns match between the data source, the **Collect** function will write all of the records to your collection.</span></span> <span data-ttu-id="fec62-134">V tomto příkladu jsou jedinými sloupci ve zdroji dat sloupce **Name**, **HoursWorked** a **DateWorked**.</span><span class="sxs-lookup"><span data-stu-id="fec62-134">In this example, **Name**, **HoursWorked**, and **DateWorked** are the only columns in the data source.</span></span>
<span data-ttu-id="fec62-135">Sloupce **LastScreen** a **Status** se ve zdroji dat nevyskytují a není potřeba je ukládat.</span><span class="sxs-lookup"><span data-stu-id="fec62-135">**LastScreen** and **Status** do not exist in the data source and do not need to be saved.</span></span> <span data-ttu-id="fec62-136">K odeslání pouze odpovídajících sloupců do zdroje dat můžete použít funkci **DropColumns**.</span><span class="sxs-lookup"><span data-stu-id="fec62-136">You can use **DropColumns** to send just the appropriate columns to the data source.</span></span>

```
Collect(YourDataSource, DropColumns(collectTimeTracking, "LastScreen","Status"))
```

<span data-ttu-id="fec62-137">Tato funkce zapíše obsah kolekce **collectTimeTracking** po vyřazení sloupců **LastScreen** a **Status** do zdroje **YourDataSource**.</span><span class="sxs-lookup"><span data-stu-id="fec62-137">This function will write the contents of the collection, **collectTimeTracking,** to the data source, **YourDataSource,** after dropping the columns **LastScreen** and **Status**.</span></span> <span data-ttu-id="fec62-138">Upozorňujeme, že funkce **DropColumns** nezmění kolekci **collectTimeTracking**.</span><span class="sxs-lookup"><span data-stu-id="fec62-138">Note,**DropColumns** did not alter your collection **collectTimeTracking**.</span></span> <span data-ttu-id="fec62-139">Sloupce **LastScreen** a **Status** jsou v této kolekci nadále k dispozici.</span><span class="sxs-lookup"><span data-stu-id="fec62-139">The **LastScreen** and **Status** columns are still available within the collection.</span></span>

<a name="renamecolumns"></a><span data-ttu-id="fec62-140">RenameColumns</span><span class="sxs-lookup"><span data-stu-id="fec62-140">RenameColumns</span></span>
-------------

<span data-ttu-id="fec62-141">Funkci **RenameColumns** použijte v případě, že potřebujete pracovat s názvem sloupce v aplikaci, ale ne ve zdroji dat.</span><span class="sxs-lookup"><span data-stu-id="fec62-141">Use the **RenameColumns** function when you need to manipulate the name of the column within your app but not within your data source.</span></span> <span data-ttu-id="fec62-142">Tato funkce se běžně používá, pokud zdroj dat, který nemůžete upravovat, má potíže s odkazováním na název sloupce, nebo pokud se v názvu sloupce používají vyhrazená slova, například Date.</span><span class="sxs-lookup"><span data-stu-id="fec62-142">A common use is when the data source, which you cannot edit, has difficult to reference column name or the column name uses reserved words, like "Date".</span></span>

<span data-ttu-id="fec62-143">Funkci lze použít při ukládání dat do kolekce.</span><span class="sxs-lookup"><span data-stu-id="fec62-143">You can use the function when storing data into a collection.</span></span> <span data-ttu-id="fec62-144">Všimněte si, že funkce **Vytvořit kolekci** může použít obsah ze zdroje dat a uložit ho do kolekce.</span><span class="sxs-lookup"><span data-stu-id="fec62-144">Note that the **Collect** function can take the contents of your data source and store them into a collection.</span></span>

```
Collect(collectProjectData, ProjectDataSource)
```

<span data-ttu-id="fec62-145">Tento vzorec vytvoří kolekci s názvem **collectProjectData**, která uchovává všechny řádky dat ze zdroje dat **ProjectDataSource**.</span><span class="sxs-lookup"><span data-stu-id="fec62-145">This formula would create a collection named **collectProjectData** that stores all of the rows of data from the data source, **ProjectDataSource**.</span></span> <span data-ttu-id="fec62-146">Pokud zdroj dat obsahuje sloupec s názvem **Date**, může být pro vaši práci v PowerApps jednodušší, když daný sloupec přejmenujete na **ProjectDate**.</span><span class="sxs-lookup"><span data-stu-id="fec62-146">If the data source has a column named **Date**, you might find it easier to work in PowerApps by renaming that column to **ProjectDate**.</span></span> <span data-ttu-id="fec62-147">Provedete to tak, že místo předchozího příkladu použijete následující vzorec.</span><span class="sxs-lookup"><span data-stu-id="fec62-147">You can do that by using the following formula instead of the previous example.</span></span>

```
Collect(collectProjectData, RenameColumns(ProjectDataSource, "Date","ProjectDate"))
```

<span data-ttu-id="fec62-148">Máte stejné záznamy.</span><span class="sxs-lookup"><span data-stu-id="fec62-148">You have the same records.</span></span> <span data-ttu-id="fec62-149">Nyní v kolekci máte místo sloupce **Date** sloupec **ProjectDate**.</span><span class="sxs-lookup"><span data-stu-id="fec62-149">Now, instead of the column being named **Date,** it is now named **ProjectDate** within your collection.</span></span> <span data-ttu-id="fec62-150">Tato funkce poskytuje flexibilitu k určení takových názvů sloupců, které budou při práci v aplikaci méně matoucí.</span><span class="sxs-lookup"><span data-stu-id="fec62-150">This gives you the flexibility to name columns to something that will be less confusing to work with in the app.</span></span>

<a name="showcolumns"></a><span data-ttu-id="fec62-151">ShowColumns</span><span class="sxs-lookup"><span data-stu-id="fec62-151">ShowColumns</span></span>
-----------

<span data-ttu-id="fec62-152">Funkce **ShowColumns** slouží k zobrazení jednoho nebo více sloupců ze zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="fec62-152">**ShowColumns** is used to display one or more columns from your data source.</span></span> <span data-ttu-id="fec62-153">Tuto funkci použijte u ovládacích prvků, u kterých chcete vracet jenom jeden sloupec.</span><span class="sxs-lookup"><span data-stu-id="fec62-153">Use this with controls where you only want a single column returned.</span></span> <span data-ttu-id="fec62-154">Běžným příkladem je ovládací prvek **rozevíracího seznamu**.</span><span class="sxs-lookup"><span data-stu-id="fec62-154">A common example is the **dropdown** control.</span></span>

<span data-ttu-id="fec62-155">U ovládacího prvku **rozevíracího seznamu** se k poskytování možností běžně používá zdroj dat, jako je například entita služby CDS.</span><span class="sxs-lookup"><span data-stu-id="fec62-155">With the **dropdown** control, it is common to use a data source, such as a CDS entity, to provide the options.</span></span> <span data-ttu-id="fec62-156">Když nastavíte vlastnost items pro zdroj dat, služba PowerApps zvolí sloupec, který se má zobrazit (pokud jich máte více).</span><span class="sxs-lookup"><span data-stu-id="fec62-156">When you set the items property to a data source, PowerApps will choose which column, if you have multiple, to display.</span></span> <span data-ttu-id="fec62-157">Pomocí funkce **ShowColumns** můžete vybrat sloupec, který chcete zobrazit.</span><span class="sxs-lookup"><span data-stu-id="fec62-157">You can use the **ShowColumns** function to select the column that you want to display.</span></span>

<span data-ttu-id="fec62-158">Pokud chcete použít zdroj dat s názvem **Customers** k zobrazení jmen zákazníků ze sloupce **CustomerName**,</span><span class="sxs-lookup"><span data-stu-id="fec62-158">If you wanted to use a data source named **Customers** to display customer names from the **CustomerName** column.</span></span> <span data-ttu-id="fec62-159">použijete ve vlastnosti **Items** ovládacího prvku **rozevíracího seznamu** následující vzorec.</span><span class="sxs-lookup"><span data-stu-id="fec62-159">You would use the following formula in the **Items** property of the **Dropdown** control.</span></span>

```
ShowColumns(Customers, "CustomerName")
```

<span data-ttu-id="fec62-160">Díky tomuto vzorci se ve sloupci **Dropdown** zobrazí hodnoty ze sloupce **CustomerName**.</span><span class="sxs-lookup"><span data-stu-id="fec62-160">With this formula, the **Dropdown** column displays the values from the **CustomerName** column.</span></span>

<span data-ttu-id="fec62-161">Funkce **ShowColumns** může vracet rovněž více sloupců.</span><span class="sxs-lookup"><span data-stu-id="fec62-161">**ShowColumns** can also return more than one column.</span></span> <span data-ttu-id="fec62-162">V ovládacím prvku **rozevíracího seznamu** se bude zobrazovat jenom první sloupec, ale budete mít přístup ke všem načteným sloupcům.</span><span class="sxs-lookup"><span data-stu-id="fec62-162">The **Dropdown** control will only display the first column, but you will have access to all the retrieved columns.</span></span> <span data-ttu-id="fec62-163">Následující příklad ukazuje, jak do ovládacího prvku **rozevíracího seznamu** přidat sloupec **ID**.</span><span class="sxs-lookup"><span data-stu-id="fec62-163">The following example shows how to add the **ID** column to your **Dropdown** control.</span></span>

```
ShowColumns(Customers, "CustomerName", "ID")
```

<span data-ttu-id="fec62-164">V rozevíracím seznamu se bude zobrazovat jenom hodnota ze sloupce **CustomerName** v ovládacím prvku **rozevíracího seznamu**, ale díky tomuto vzorci teď budete mít přístup k hodnotě sloupce ID.</span><span class="sxs-lookup"><span data-stu-id="fec62-164">The dropdown will only display the value from **CustomerName** column in the **Dropdown** control, but with this formula, you now have access to the value of the ID column.</span></span> <span data-ttu-id="fec62-165">Přidejte na obrazovku ovládací prvek **popisku** a nastavte hodnotu **Text** následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="fec62-165">Add a **Label** control to the screen and set the **Text** value to the following.</span></span> <span data-ttu-id="fec62-166">Pokud váš rozevírací seznamu nemá název Dropdown1, upravte daný vzorec odpovídajícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="fec62-166">If your dropdown is not named Dropdown1, edit the formula accordingly.</span></span>

```
Dropdown1.Selected.ID
```

<span data-ttu-id="fec62-167">Vzorec vrací hodnotu ze sloupce ID pro vybraný záznam v ovládacím prvku **rozevíracího seznamu**.</span><span class="sxs-lookup"><span data-stu-id="fec62-167">The formula returns the value from the ID column for the selected record in your **Dropdown** control.</span></span> 
