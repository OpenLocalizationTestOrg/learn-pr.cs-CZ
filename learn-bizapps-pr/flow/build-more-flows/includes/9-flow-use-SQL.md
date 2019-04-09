---
ms.openlocfilehash: 7650cdfc385b9a1e5e0a04d34e2312d0a70c5e88
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698849"
---
<span data-ttu-id="d9550-101">Tato lekce ukazuje, jak vytvořit tok, který monitoruje nové nebo změněné položky ve zdroji a pak tyto změny zkopíruje do cíle.</span><span class="sxs-lookup"><span data-stu-id="d9550-101">This unit shows how to create a flow that monitors a source for new or changed items, and then copies those changes to a destination.</span></span> <span data-ttu-id="d9550-102">Tok tohoto typu byste mohli vytvořit, pokud uživatelé zadávají data v jednom umístění, ale váš tým potřebuje tato data v jiném umístění nebo formátu.</span><span class="sxs-lookup"><span data-stu-id="d9550-102">You might create a flow of this type if your users enter data in one location, but your team needs that data in a different location or format.</span></span>

<span data-ttu-id="d9550-103">V této lekci zkopírujete data ze [seznamu Microsoft SharePointu](https://support.office.com/article/SharePoint-lists-I-An-introduction-f11cd5fe-bc87-4f9e-9bfe-bbd87a22a194) (zdroj) do tabulky [Microsoft Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview) (cíl).</span><span class="sxs-lookup"><span data-stu-id="d9550-103">In this unit, you'll copy data from a [Microsoft SharePoint list](https://support.office.com/article/SharePoint-lists-I-An-introduction-f11cd5fe-bc87-4f9e-9bfe-bbd87a22a194) (the source) to a [Microsoft Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview) table (the destination).</span></span>

<span data-ttu-id="d9550-104">Mějte na paměti, že můžete kopírovat data do více než [150 služeb](https://flow.microsoft.com/connectors/), které Microsoft Flow podporuje.</span><span class="sxs-lookup"><span data-stu-id="d9550-104">Keep in mind that you can copy data over more than [150 services](https://flow.microsoft.com/connectors/) that Microsoft Flow supports.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9550-105">Změny provedené v cíli se nekopírují zpět do zdroje, protože obousměrná synchronizace není podporována.</span><span class="sxs-lookup"><span data-stu-id="d9550-105">Changes that you make in the destination aren't copied back to the source, because two-way synchronization isn't supported.</span></span> <span data-ttu-id="d9550-106">Pokud se pokusíte nastavit obousměrnou synchronizaci, vytvoříte nekonečnou smyčku, ve které se změny odesílají mezi zdrojem a cílem do nekonečna.</span><span class="sxs-lookup"><span data-stu-id="d9550-106">If you try to set up two-way synchronization, you'll create an infinite loop where changes are sent endlessly between the source and destination.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d9550-107">Požadavky</span><span class="sxs-lookup"><span data-stu-id="d9550-107">Prerequisites</span></span>

* <span data-ttu-id="d9550-108">Přístup ke zdroji a cíli dat.</span><span class="sxs-lookup"><span data-stu-id="d9550-108">Access to a data source and a destination.</span></span> <span data-ttu-id="d9550-109">Tato lekce nezahrnuje postup pro vytvoření zdroje a cíle.</span><span class="sxs-lookup"><span data-stu-id="d9550-109">This unit doesn't include the steps to create the source and destination.</span></span>
* <span data-ttu-id="d9550-110">Přístup k [Microsoft Flow](https://flow.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="d9550-110">Access to [Microsoft Flow](https://flow.microsoft.com).</span></span>
* <span data-ttu-id="d9550-111">Základní znalosti o tom, jak jsou vaše data uložená.</span><span class="sxs-lookup"><span data-stu-id="d9550-111">A basic understanding of how your data is stored.</span></span>
* <span data-ttu-id="d9550-112">Znalost principů vytváření toků.</span><span class="sxs-lookup"><span data-stu-id="d9550-112">Familiarity with the basics of creating flows.</span></span> <span data-ttu-id="d9550-113">V této lekci se předpokládá, že víte, jak se tyto akce provádějí.</span><span class="sxs-lookup"><span data-stu-id="d9550-113">For this unit, it's assumed that you know how to perform these actions.</span></span>

> [!TIP]
> <span data-ttu-id="d9550-114">Názvy sloupců ve zdroji a cíli se nemusejí shodovat, ale při vložení nebo aktualizaci položky je nutné zadat data pro všechny požadované sloupce.</span><span class="sxs-lookup"><span data-stu-id="d9550-114">Column names in the source and destination don't need to match, but you must provide data for all required columns when you insert or update an item.</span></span> <span data-ttu-id="d9550-115">Microsoft Flow určí požadovaná pole za vás.</span><span class="sxs-lookup"><span data-stu-id="d9550-115">Microsoft Flow identifies the required fields for you.</span></span>

## <a name="quick-overview-of-the-steps"></a><span data-ttu-id="d9550-116">Stručný přehled kroků</span><span class="sxs-lookup"><span data-stu-id="d9550-116">Quick overview of the steps</span></span>

<span data-ttu-id="d9550-117">Pokud jste s Microsoft Flow obeznámeni, zkopírujte data z jednoho zdroje dat do druhého pomocí těchto rychlých kroků.</span><span class="sxs-lookup"><span data-stu-id="d9550-117">If you're comfortable with Microsoft Flow, use these quick steps to copy data from one data source to another.</span></span>

1. <span data-ttu-id="d9550-118">Určete zdroj, který budete monitorovat, a cíl, do kterého zkopírujete změněná data.</span><span class="sxs-lookup"><span data-stu-id="d9550-118">Identify the source that you'll monitor and the destination that you'll copy changed data to.</span></span> <span data-ttu-id="d9550-119">Ověřte, že máte přístup ke zdroji i k cíli.</span><span class="sxs-lookup"><span data-stu-id="d9550-119">Confirm that you have access to both the source and the destination.</span></span>
2. <span data-ttu-id="d9550-120">Určete alespoň jeden sloupec, který jednoznačně identifikuje položky ve zdroji a cíli.</span><span class="sxs-lookup"><span data-stu-id="d9550-120">Identify at least one column that uniquely identifies items in the source and destination.</span></span> <span data-ttu-id="d9550-121">V následujícím příkladu použijeme sloupec **Název**, ale můžete použít libovolné sloupce.</span><span class="sxs-lookup"><span data-stu-id="d9550-121">In the example that follows, we use the **Title** column, but you can use any columns.</span></span>
3. <span data-ttu-id="d9550-122">Nastavte trigger, který monitoruje změny ve zdroji.</span><span class="sxs-lookup"><span data-stu-id="d9550-122">Set up a trigger that monitors the source for changes.</span></span>
4. <span data-ttu-id="d9550-123">Prohledáním cíle zkontrolujte, jestli změněná položka existuje.</span><span class="sxs-lookup"><span data-stu-id="d9550-123">Search the destination to check whether the changed item exists.</span></span>
5. <span data-ttu-id="d9550-124">Použijte podmínku, jako je tato:</span><span class="sxs-lookup"><span data-stu-id="d9550-124">Use a condition like this:</span></span>

    * <span data-ttu-id="d9550-125">Pokud nová nebo změněná položka v cíli neexistuje, vytvořte ji.</span><span class="sxs-lookup"><span data-stu-id="d9550-125">If the new or changed item doesn't exist in the destination, create it.</span></span>
    * <span data-ttu-id="d9550-126">Pokud nová nebo změněná položka v cíli existuje, aktualizujte ji.</span><span class="sxs-lookup"><span data-stu-id="d9550-126">If the new or changed item exists in the destination, update it.</span></span>

6. <span data-ttu-id="d9550-127">Aktivujte tok a pak ověřte, že nové nebo změněné položky se kopírují ze zdroje do cíle.</span><span class="sxs-lookup"><span data-stu-id="d9550-127">Trigger your flow, and then confirm that new or changed items are being copied from the source to the destination.</span></span>

> [!NOTE]
> <span data-ttu-id="d9550-128">Pokud jste dosud nevytvořili připojení ke službě SharePoint nebo SQL Database, postupujte po zobrazení výzvy k přihlášení podle pokynů.</span><span class="sxs-lookup"><span data-stu-id="d9550-128">If you haven't previously created a connection to SharePoint or SQL Database, follow the instructions when you're prompted to sign in.</span></span>

<span data-ttu-id="d9550-129">Tady je podrobný postup pro vytvoření toku.</span><span class="sxs-lookup"><span data-stu-id="d9550-129">Here are the detailed steps to create the flow.</span></span>

## <a name="monitor-the-source-for-changes"></a><span data-ttu-id="d9550-130">Monitorování změn ve zdroji</span><span class="sxs-lookup"><span data-stu-id="d9550-130">Monitor the source for changes</span></span>

<span data-ttu-id="d9550-131">Nejprve nastavíme web SharePointu pro monitorování změn.</span><span class="sxs-lookup"><span data-stu-id="d9550-131">First, we'll set up the SharePoint site to monitor changes.</span></span>

1. <span data-ttu-id="d9550-132">Spusťte Microsoft Flow a přihlaste se pomocí účtu organizace.</span><span class="sxs-lookup"><span data-stu-id="d9550-132">Launch Microsoft Flow and sign in using your organizational account.</span></span>
1. <span data-ttu-id="d9550-133">V levém podokně vyberte **Moje toky**.</span><span class="sxs-lookup"><span data-stu-id="d9550-133">In the left pane, select **My flows**.</span></span>
1. <span data-ttu-id="d9550-134">Vyberte **Nový** a pak vyberte **Vytvořit z prázdné**.</span><span class="sxs-lookup"><span data-stu-id="d9550-134">Select **New**, and then select **Create from blank**.</span></span>

    ![Vytvořit z prázdné](../media/flow-create-blank.png)

1. <span data-ttu-id="d9550-136">V seznamu triggerů vyberte trigger **SharePoint – Při vytvoření nebo úpravě položky**.</span><span class="sxs-lookup"><span data-stu-id="d9550-136">In the list of triggers, select the **SharePoint - When an item is created or modified** trigger.</span></span>
1. <span data-ttu-id="d9550-137">Na kartě **Při vytvoření nebo úpravě položky** zadejte adresu webu a pak vyberte název sharepointového seznamu, ve kterém váš tok monitoruje nové nebo aktualizované položky.</span><span class="sxs-lookup"><span data-stu-id="d9550-137">On the **When an item is created or modified** card, enter the site address, and then select the name of the SharePoint list that your flow monitors for new or updated items.</span></span>

    ![Nastavení triggeru SharePointu](../media/configure-sharepoint-trigger.png)

## <a name="search-the-destination-for-the-new-or-changed-item"></a><span data-ttu-id="d9550-139">Vyhledání cíle nové nebo změněné položky</span><span class="sxs-lookup"><span data-stu-id="d9550-139">Search the destination for the new or changed item</span></span>

<span data-ttu-id="d9550-140">V dalším kroku vyhledáme cíl nové nebo změněné položky pomocí akce **SQL Server – Získat řádky**.</span><span class="sxs-lookup"><span data-stu-id="d9550-140">Next, we'll use the **SQL Server - Get rows** action to search the destination for the new or changed item.</span></span>

1. <span data-ttu-id="d9550-141">Vyberte **Nový krok**.</span><span class="sxs-lookup"><span data-stu-id="d9550-141">Select **New step**.</span></span>
1. <span data-ttu-id="d9550-142">V části **Zvolte akci** vyhledejte *Získat řádky* a pak vyberte **SQL Server – Získat řádky**.</span><span class="sxs-lookup"><span data-stu-id="d9550-142">Under **Choose an action**, search for *Get rows*, and then select **SQL Server - Get rows**.</span></span>
1. <span data-ttu-id="d9550-143">V seznamu **Název tabulky** vyberte tabulku, kterou chcete monitorovat.</span><span class="sxs-lookup"><span data-stu-id="d9550-143">In the **Table name** list, select the table to monitor.</span></span>
1. <span data-ttu-id="d9550-144">Vyberte **Zobrazit pokročilé možnosti**.</span><span class="sxs-lookup"><span data-stu-id="d9550-144">Select **Show advanced options**.</span></span>
1. <span data-ttu-id="d9550-145">Do pole **Dotaz filtru** zadejte *Title eq* (Název eq), mezeru a znak jednoduchých uvozovek (').</span><span class="sxs-lookup"><span data-stu-id="d9550-145">In the **Filter Query** box, enter *Title eq* followed by a space and a single quotation mark (').</span></span> <span data-ttu-id="d9550-146">Pak v seznamu dynamického obsahu vyberte token **Název** a zadejte další znak jednoduchých uvozovek.</span><span class="sxs-lookup"><span data-stu-id="d9550-146">Then select the **Title** token in the dynamic content list, and enter another single quotation mark.</span></span>

    <span data-ttu-id="d9550-147">Tento krok předpokládá, že porovnáváte odpovídající názvy řádků ve zdroji a cíli.</span><span class="sxs-lookup"><span data-stu-id="d9550-147">This step assumes that you're matching the titles of the rows in the source and destination.</span></span>

    <span data-ttu-id="d9550-148">Karta **Získat řádky** by teď měla vypadat jako na tomto obrázku.</span><span class="sxs-lookup"><span data-stu-id="d9550-148">The **Get rows** card should now look like this image.</span></span>

    ![Pokus o získání položky z cílové databáze](../media/configure-sql-get-rows-action.png)

## <a name="check-whether-the-new-or-changed-item-was-found"></a><span data-ttu-id="d9550-150">Kontrola, jestli byla nalezena nová nebo změněná položka</span><span class="sxs-lookup"><span data-stu-id="d9550-150">Check whether the new or changed item was found</span></span>

<span data-ttu-id="d9550-151">V dalším kroku zkontrolujeme, jestli byla nalezena nová nebo změněná položka.</span><span class="sxs-lookup"><span data-stu-id="d9550-151">Next, we'll check whether the new or changed item was found.</span></span>

1. <span data-ttu-id="d9550-152">Vyberte **Nový krok** a pak vyberte **Přidat podmínku**.</span><span class="sxs-lookup"><span data-stu-id="d9550-152">Select **New step**, and then select **Add a condition**.</span></span>
2. <span data-ttu-id="d9550-153">Na kartě **Podmínka** vyberte pole vlevo.</span><span class="sxs-lookup"><span data-stu-id="d9550-153">On the **Condition** card, select the field on the left.</span></span>

    <span data-ttu-id="d9550-154">Otevře se seznam **Přidá dynamický obsah z aplikací a konektorů, které se používají v tomto toku**.</span><span class="sxs-lookup"><span data-stu-id="d9550-154">The **Add dynamic content from the apps and connectors used in this flow** list opens.</span></span>

3. <span data-ttu-id="d9550-155">V kategorii **Získat řádky** vyberte **Hodnota**.</span><span class="sxs-lookup"><span data-stu-id="d9550-155">In the **Get rows** category, select **value**.</span></span>

    > [!TIP]
    > <span data-ttu-id="d9550-156">Ověřte, že jste vybrali **Hodnota** v kategorii **Získat řádky**.</span><span class="sxs-lookup"><span data-stu-id="d9550-156">Confirm that you've selected **value** in the **Get rows** category.</span></span> <span data-ttu-id="d9550-157">Nevybírejte **Hodnota** v kategorii **Při vytvoření nebo úpravě položky**.</span><span class="sxs-lookup"><span data-stu-id="d9550-157">Don't select **value** in the **When an item is created or modified** category.</span></span>

4. <span data-ttu-id="d9550-158">V poli uprostřed vyberte *rovná se*.</span><span class="sxs-lookup"><span data-stu-id="d9550-158">In the field in the center, select *is equal to*.</span></span>
5. <span data-ttu-id="d9550-159">Do pole vpravo zadejte *0* (nula).</span><span class="sxs-lookup"><span data-stu-id="d9550-159">In the field on the right, enter *0* (zero).</span></span>

    <span data-ttu-id="d9550-160">Karta **Podmínka** by teď měla vypadat jako na tomto obrázku.</span><span class="sxs-lookup"><span data-stu-id="d9550-160">The **Condition** card should now look like this image.</span></span>

    ![Nastavení podmínky](../media/configure-condition.png)

6. <span data-ttu-id="d9550-162">Vyberte **Upravit v rozšířeném režimu**.</span><span class="sxs-lookup"><span data-stu-id="d9550-162">Select **Edit in advanced mode**.</span></span>
7. <span data-ttu-id="d9550-163">Po spuštění rozšířeného režimu se v poli zobrazí výraz `@equals(body('Get_rows')?['value'], 0)`.</span><span class="sxs-lookup"><span data-stu-id="d9550-163">When advanced mode is started, you'll see the `@equals(body('Get_rows')?['value'], 0)` expression in the field.</span></span> <span data-ttu-id="d9550-164">Upravte tento výraz přidáním funkce *length()*, do níž umístíte uvedenou funkci `body('Get_items')?['value']`.</span><span class="sxs-lookup"><span data-stu-id="d9550-164">Edit this expression by adding *length()* around the `body('Get_items')?['value']` function.</span></span> <span data-ttu-id="d9550-165">Celý výraz by teď měl vypadat takto: `@equals(length(body('Get_rows')?['value']), 0)`</span><span class="sxs-lookup"><span data-stu-id="d9550-165">The entire expression should now look like this: `@equals(length(body('Get_rows')?['value']), 0)`</span></span>

    <span data-ttu-id="d9550-166">Karta **Podmínka** by teď měla vypadat jako na tomto obrázku.</span><span class="sxs-lookup"><span data-stu-id="d9550-166">The **Condition** card should now look like this image.</span></span>

    ![Nastavení podmínky](../media/configure-condition-add-length.png)

    > [!TIP]
    > <span data-ttu-id="d9550-168">Přidání funkce `length()` umožní toku zkontrolovat seznam **Hodnota** a určit, jestli obsahuje nějaké položky.</span><span class="sxs-lookup"><span data-stu-id="d9550-168">The addition of the `length()` function lets the flow check the **value** list and check whether it has any items.</span></span>

<span data-ttu-id="d9550-169">Když tok získá položky z cíle, jsou možné dva výsledky.</span><span class="sxs-lookup"><span data-stu-id="d9550-169">When your flow gets items from the destination, there are two possible outcomes.</span></span>

| <span data-ttu-id="d9550-170">Výsledek</span><span class="sxs-lookup"><span data-stu-id="d9550-170">Outcome</span></span> | <span data-ttu-id="d9550-171">Další krok</span><span class="sxs-lookup"><span data-stu-id="d9550-171">Next step</span></span> |
| --- | --- |
| <span data-ttu-id="d9550-172">Položka existuje.</span><span class="sxs-lookup"><span data-stu-id="d9550-172">The item exists.</span></span> | <span data-ttu-id="d9550-173">Aktualizujte položku.</span><span class="sxs-lookup"><span data-stu-id="d9550-173">Update the item.</span></span> |
| <span data-ttu-id="d9550-174">Položka neexistuje.</span><span class="sxs-lookup"><span data-stu-id="d9550-174">The item doesn't exist.</span></span> | <span data-ttu-id="d9550-175">Vytvořte novou položku.</span><span class="sxs-lookup"><span data-stu-id="d9550-175">Create a new item.</span></span> |

## <a name="create-the-item-in-the-destination"></a><span data-ttu-id="d9550-176">Vytvoření položky v cíli</span><span class="sxs-lookup"><span data-stu-id="d9550-176">Create the item in the destination</span></span>

<span data-ttu-id="d9550-177">Pokud položka v cíli neexistuje, vytvořte ji pomocí akce **SQL Server – Vložit řádek**.</span><span class="sxs-lookup"><span data-stu-id="d9550-177">If the item doesn't exist in the destination, create it by using the **SQL Server - Insert row** action.</span></span>

1. <span data-ttu-id="d9550-178">Ve větvi podmínky **Pokud ano** vyberte **Přidat akci**, vyhledejte *Vložit řádek* a pak vyberte **SQL Server – Vložit řádek**.</span><span class="sxs-lookup"><span data-stu-id="d9550-178">On the **If yes** branch of the condition, select **Add an action**, search for *insert row*, and then select **SQL Server - Insert row**.</span></span>
2. <span data-ttu-id="d9550-179">Na kartě **Vložit řádek** v seznamu **Název tabulky** vyberte tabulku, do které chcete vložit novou položku.</span><span class="sxs-lookup"><span data-stu-id="d9550-179">On the **Insert row** card, in the **Table name** list, select the table to insert the new item into.</span></span>

    <span data-ttu-id="d9550-180">Karta **Vložit řádek** se rozbalí a zobrazuje všechna pole ve vybrané tabulce.</span><span class="sxs-lookup"><span data-stu-id="d9550-180">The **Insert row** card expands and shows all fields in the selected table.</span></span> <span data-ttu-id="d9550-181">Pole označená hvězdičkou (\*) jsou povinná, a pokud má být řádek platný, musí být vyplněná.</span><span class="sxs-lookup"><span data-stu-id="d9550-181">Fields that are marked with an asterisk (\*) are required and must be filled in for the row to be valid.</span></span>

3. <span data-ttu-id="d9550-182">Vyberte každé pole, které chcete vyplnit, a zadejte data.</span><span class="sxs-lookup"><span data-stu-id="d9550-182">Select each field that you want to fill in, and enter the data.</span></span>

    <span data-ttu-id="d9550-183">Můžete zadat data ručně, vybrat jeden nebo více tokenů v podokně dynamického obsahu nebo zadat do polí libovolnou kombinaci textu a tokenů.</span><span class="sxs-lookup"><span data-stu-id="d9550-183">You can manually enter the data, select one or more tokens in the dynamic content pane, or enter any combination of text and tokens into the fields.</span></span>

    ![Nastavení podmínky](../media/insert-row.png)

> [!NOTE]
> <span data-ttu-id="d9550-185">Karty **Vložit řádek** a **Aktualizovat řádek** zobrazují názvy sloupců v tabulce SQL Database, která se používá v daném toku.</span><span class="sxs-lookup"><span data-stu-id="d9550-185">The **Insert row** and **Update row** cards show the names of the columns in the SQL Database table that's being used in the flow.</span></span> <span data-ttu-id="d9550-186">Karty na obrázcích v tomto postupu se proto můžou lišit od karet, které se zobrazují vám.</span><span class="sxs-lookup"><span data-stu-id="d9550-186">Therefore, the cards that are shown in the images in this procedure might differ from the cards that you see.</span></span> 

## <a name="update-the-item-in-the-destination"></a><span data-ttu-id="d9550-187">Aktualizace položky v cíli</span><span class="sxs-lookup"><span data-stu-id="d9550-187">Update the item in the destination</span></span>

<span data-ttu-id="d9550-188">Pokud položka v cíli existuje, aktualizujte ji změnami.</span><span class="sxs-lookup"><span data-stu-id="d9550-188">Next, if the item exists in the destination, update it with the changes.</span></span>

1. <span data-ttu-id="d9550-189">Přidejte akci **SQL Server – Aktualizovat řádek** do větve podmínky **Pokud ne**.</span><span class="sxs-lookup"><span data-stu-id="d9550-189">Add the **SQL Server - Update row** action to the **If no** branch of the condition.</span></span>

    ![Zobrazení prostředí](../media/update-row.png)

1. <span data-ttu-id="d9550-191">Do pole **Název toku** v horní části stránky zadejte název pro váš tok.</span><span class="sxs-lookup"><span data-stu-id="d9550-191">In the **Flow name** field at the top of the page, enter a name for your flow.</span></span>
1. <span data-ttu-id="d9550-192">Uložte tok výběrem možnosti **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d9550-192">Select **Save** to save the flow.</span></span>

<span data-ttu-id="d9550-193">Při každé změně položky sharepointového seznamu (zdroj) se teď tok aktivuje.</span><span class="sxs-lookup"><span data-stu-id="d9550-193">Now, whenever an item in your SharePoint list (the source) changes, your flow is triggered.</span></span> <span data-ttu-id="d9550-194">Vloží novou položku nebo aktualizuje existující položku ve službě SQL Database (cíl).</span><span class="sxs-lookup"><span data-stu-id="d9550-194">It either inserts a new item or updates an existing item in SQL Database (the destination).</span></span>

> [!NOTE]
> <span data-ttu-id="d9550-195">Pokud dojde k odstranění položky ze zdroje, tok se neaktivuje.</span><span class="sxs-lookup"><span data-stu-id="d9550-195">Your flow isn't triggered when an item is deleted from the source.</span></span> <span data-ttu-id="d9550-196">Pokud je tento scénář pro vás důležitý, zvažte možnost přidání samostatného sloupce, který bude indikovat, že položku už nepotřebujete.</span><span class="sxs-lookup"><span data-stu-id="d9550-196">If this scenario is important to you, consider adding a separate column that indicates when an item is no longer needed.</span></span>
