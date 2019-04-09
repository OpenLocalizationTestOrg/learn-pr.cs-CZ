---
ms.openlocfilehash: 8cd887fc6b593ee43de7b2dda14737764dd110ae
ms.sourcegitcommit: e17cc64775307fcf15cef8e0181fdb046ccd227f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58265888"
---
<span data-ttu-id="93ed1-101">V Microsoft PowerApps můžete vytvořit aplikaci plátna s přístupem k informacím v Excelu, SharePointu, SQL Serveru a několika dalších zdrojích, ve kterých se data ukládají v záznamech a tabulkách.</span><span class="sxs-lookup"><span data-stu-id="93ed1-101">In Microsoft PowerApps, you can create a canvas app that accesses information in Excel, SharePoint, SQL Server, and several other sources that store data in records and tables.</span></span> <span data-ttu-id="93ed1-102">Abyste s tímto druhem dat pracovali co nejefektivněji, musíte lépe poznat koncepce, které jsou základem těchto struktur.</span><span class="sxs-lookup"><span data-stu-id="93ed1-102">To work most effectively with this kind of data, you need to learn more about the concepts that underlie these structures.</span></span>

-   <span data-ttu-id="93ed1-103">*Záznam* obsahuje jednu nebo více kategorií informací o osobě, místě nebo věci.</span><span class="sxs-lookup"><span data-stu-id="93ed1-103">A *record* contains one or more categories of information about a person, place, or thing.</span></span> <span data-ttu-id="93ed1-104">Záznam může například obsahovat jméno, e-mailovou adresu a telefonní číslo jednoho zákazníka.</span><span class="sxs-lookup"><span data-stu-id="93ed1-104">For example, a record might contain the name, email address, and phone number of a single customer.</span></span>
    <span data-ttu-id="93ed1-105">U jiných nástrojů se záznam označuje jako „řádek“ nebo „položka“.</span><span class="sxs-lookup"><span data-stu-id="93ed1-105">Other tools refer to a record as a \"row\" or an \"item.\"</span></span>

-   <span data-ttu-id="93ed1-106">*Tabulka* uchovává jeden nebo více záznamů, které obsahují stejné kategorie informací.</span><span class="sxs-lookup"><span data-stu-id="93ed1-106">A *table* holds one or more records that contain the same categories of information.</span></span> <span data-ttu-id="93ed1-107">Tabulka může třeba obsahovat jména, e-mailové adresy a telefonní čísla 50 zákazníků.</span><span class="sxs-lookup"><span data-stu-id="93ed1-107">For example, a table might contain the names, email addresses, and phone numbers of 50 customers.</span></span>

<span data-ttu-id="93ed1-108">V aplikaci budete k vytváření, aktualizaci a manipulaci se záznamy a tabulkami používat vzorce.</span><span class="sxs-lookup"><span data-stu-id="93ed1-108">In your app, you'll use formulas to create, update, and manipulate records and tables.</span></span> <span data-ttu-id="93ed1-109">Budete pravděpodobně číst a zapisovat data do externího zdroje dat, což je *rozšířená tabulka*.</span><span class="sxs-lookup"><span data-stu-id="93ed1-109">You'll probably read and write data to an external data source, which is an *extended table*.</span></span> <span data-ttu-id="93ed1-110">Kromě toho můžete vytvořit jednu nebo více interních tabulek, které se označují jako  *kolekce*.</span><span class="sxs-lookup"><span data-stu-id="93ed1-110">In addition, you might create one or more internal tables, which are called *collections*.</span></span>

<span data-ttu-id="93ed1-111">Můžete vytvářet různé vzorce, které přebírají název tabulky jako argument, stejně jako když vzorec Excelu přebírá odkazy na buňky jako argumenty.</span><span class="sxs-lookup"><span data-stu-id="93ed1-111">You can build a variety of formulas that take the name of a table as an argument, just as a formula in Excel takes one or more cell references as arguments.</span></span> <span data-ttu-id="93ed1-112">Některé vzorce v PowerApps vrací tabulku, která zohledňuje ostatní zadané argumenty.</span><span class="sxs-lookup"><span data-stu-id="93ed1-112">Some formulas in PowerApps return a table that reflects the other arguments that you specify.</span></span>

<span data-ttu-id="93ed1-113">**Prvky tabulky**</span><span class="sxs-lookup"><span data-stu-id="93ed1-113">**Elements of a table**</span></span>

![Sloupec](../media/Column.png)

<span data-ttu-id="93ed1-115">U následujících příkladů se předpokládá, že tabulka pochází ze zdroje dat s názvem YourInventory.</span><span class="sxs-lookup"><span data-stu-id="93ed1-115">For the following examples this table will be assumed to be from a data source named YourInventory.</span></span>

<span data-ttu-id="93ed1-116">**Záznamy**</span><span class="sxs-lookup"><span data-stu-id="93ed1-116">**Records**</span></span>

<span data-ttu-id="93ed1-117">Každý záznam obsahuje minimálně jednu kategorii informací osobě, místu nebo věci.</span><span class="sxs-lookup"><span data-stu-id="93ed1-117">Each record contains at least one category of information for a person, a place, or a thing.</span></span> <span data-ttu-id="93ed1-118">Výše uvedený příklad zobrazuje záznam pro jednotlivé produkty (**Chocolate**, **Bread** a  **Water**) a sloupec pro každou kategorii informací (**Price**, **Quantity on Hand** a  **Quantity on Order**).</span><span class="sxs-lookup"><span data-stu-id="93ed1-118">The example above shows a record for each product (**Chocolate**, **Bread**, and **Water**) and a column for each category of information (**Price**, **Quantity on Hand**, and **Quantity on Order**).</span></span>

<span data-ttu-id="93ed1-119">Nejběžnějším způsobem načtení záznamu z tabulky je použití funkce **LookUp**.</span><span class="sxs-lookup"><span data-stu-id="93ed1-119">The most common way to retrieve a record from a table is to use the **LookUp** function.</span></span> <span data-ttu-id="93ed1-120">Například k vrácení záznamu Bread byste použili následující vzorec.</span><span class="sxs-lookup"><span data-stu-id="93ed1-120">For example, to return the Bread record you would use the following formula.</span></span>

```
LookUp(YourInventory, Name = "Bread")
```

<span data-ttu-id="93ed1-121">Tento vzorec by vrátil celý záznam produktu Bread.</span><span class="sxs-lookup"><span data-stu-id="93ed1-121">This would return the entire record for the Bread product.</span></span> <span data-ttu-id="93ed1-122">Funkce **LookUp** je podrobně rozebrána později v tomto modulu.</span><span class="sxs-lookup"><span data-stu-id="93ed1-122">The **LookUp** function is covered in detail later in this module.</span></span>

<span data-ttu-id="93ed1-123">**Pole**</span><span class="sxs-lookup"><span data-stu-id="93ed1-123">**Fields**</span></span>

<span data-ttu-id="93ed1-124">*Pole* je individuální údaj v záznamu.</span><span class="sxs-lookup"><span data-stu-id="93ed1-124">A *field* is an individual piece of information in a record.</span></span> <span data-ttu-id="93ed1-125">Můžete si to představit jako hodnotu ve sloupci záznamu.</span><span class="sxs-lookup"><span data-stu-id="93ed1-125">You can visualize this as a value in a column for a record.</span></span>

<span data-ttu-id="93ed1-126">Podobně jako u ovládacího prvku se na pole nějakého záznamu odkazuje pomocí tečky (.) u tohoto záznamu.</span><span class="sxs-lookup"><span data-stu-id="93ed1-126">Just as with a control, you refer to a field of a record by using the decimal (.) operator on the record.</span></span> <span data-ttu-id="93ed1-127">Například funkce  **LookUp(YourInventory,Name = "Bread").Price** vrátí hodnotu $ 4,95.</span><span class="sxs-lookup"><span data-stu-id="93ed1-127">For example, **LookUp(YourInventory,Name = "Bread").Price** returns the value $ 4.95.</span></span><span data-ttu-id="93ed1-128"> Tento výstup můžete zobrazit v ovládacím prvku Popisek nebo použít s jinými ovládacími prvky nebo funkcemi aplikace, kde potřebujete odkázat na hodnotu.</span><span class="sxs-lookup"><span data-stu-id="93ed1-128"> You could display this output in a Label control or use it with other controls or functions within your app where you need to reference the value.</span></span>

<span data-ttu-id="93ed1-129">**Sloupce**</span><span class="sxs-lookup"><span data-stu-id="93ed1-129">**Columns**</span></span>

<span data-ttu-id="93ed1-130">*Sloupec* označuje stejné pole jednoho nebo více záznamů v tabulce.</span><span class="sxs-lookup"><span data-stu-id="93ed1-130">A *column* refers to the same field for one or more records in a table.</span></span> <span data-ttu-id="93ed1-131">V předchozím příkladu obsahuje každý produkt pole s cenou, která je pro všechny produkty ve stejném sloupci.</span><span class="sxs-lookup"><span data-stu-id="93ed1-131">In the above example, each product has a price field, and that price is in the same column for all products.</span></span> <span data-ttu-id="93ed1-132">Předchozí tabulka obsahuje čtyři sloupce vodorovně zobrazené v horní části:</span><span class="sxs-lookup"><span data-stu-id="93ed1-132">The above table has four columns, shown horizontally across the top:</span></span>

-   <span data-ttu-id="93ed1-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="93ed1-133">**Name**</span></span>

-   <span data-ttu-id="93ed1-134">**Price**</span><span class="sxs-lookup"><span data-stu-id="93ed1-134">**Price**</span></span>

-   <span data-ttu-id="93ed1-135">**Quantity on Hand**</span><span class="sxs-lookup"><span data-stu-id="93ed1-135">**Quantity on Hand**</span></span>

-   <span data-ttu-id="93ed1-136">**Quantity on Order**</span><span class="sxs-lookup"><span data-stu-id="93ed1-136">**Quantity on Order**</span></span>

<span data-ttu-id="93ed1-137">Název sloupce vyjadřuje pole v daném sloupci.</span><span class="sxs-lookup"><span data-stu-id="93ed1-137">The column\'s name reflects the fields in that column.</span></span>

<span data-ttu-id="93ed1-138">Všechny hodnoty v určitém sloupci jsou stejného datového typu.</span><span class="sxs-lookup"><span data-stu-id="93ed1-138">All values within a column are of the same data type.</span></span> <span data-ttu-id="93ed1-139">Sloupec \"Quantity on Hand\" v předchozím příkladu obsahuje vždy číslo a nemůže pro nějaký záznam obsahovat řetězec, například \"12 jednotek\".</span><span class="sxs-lookup"><span data-stu-id="93ed1-139">In the above example, the \"Quantity on Hand\" column always contains a number and can't contain a string, such as \"12 units,\" for one record.</span></span> <span data-ttu-id="93ed1-140">Hodnota libovolného pole může být rovněž  *prázdná*.</span><span class="sxs-lookup"><span data-stu-id="93ed1-140">The value of any field can also be *blank*.</span></span>

<span data-ttu-id="93ed1-141">V jiných nástrojích se sloupce mohou označovat jako \"pole\".</span><span class="sxs-lookup"><span data-stu-id="93ed1-141">You might have referred to columns as \"fields\" in other tools.</span></span> <span data-ttu-id="93ed1-142">Někdy potřebujete u funkce nebo ovládacího prvku odkázat na celý sloupec.</span><span class="sxs-lookup"><span data-stu-id="93ed1-142">Sometimes you need to reference an entire column for a function or control.</span></span> <span data-ttu-id="93ed1-143">Příkladem může být situace, kdy chcete sloupec Name použít k naplnění možností ovládacího prvku Rozevírací seznam.</span><span class="sxs-lookup"><span data-stu-id="93ed1-143">An example of this is if you wanted to use the Name column to populate the choices in a drop-down control.</span></span> <span data-ttu-id="93ed1-144">Na sloupec Name odkážete tak, že vlastnost **Položky** ovládacího prvku Rozevírací seznam nastavíte na YourInventory.Name.</span><span class="sxs-lookup"><span data-stu-id="93ed1-144">You could reference the Name column by setting the **Items** property for the drop-down control to YourInventory.Name.</span></span> <span data-ttu-id="93ed1-145">Tento ovládací prvek by se pak naplnil hodnotami **Chocolate**,  **Bread** a  **Water**.</span><span class="sxs-lookup"><span data-stu-id="93ed1-145">This would then populate the drop-down control with **Chocolate**, **Bread**, and **Water**.</span></span> 
