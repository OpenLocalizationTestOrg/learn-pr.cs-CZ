---
ms.openlocfilehash: dfdf308b2e59a74a7caa7d1e1a9caa0e70dbaf87
ms.sourcegitcommit: e17cc64775307fcf15cef8e0181fdb046ccd227f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58265888"
---
<span data-ttu-id="7a89f-101">Teď, když jste se naučili základní koncepce práce s tabulkami a záznamy, můžete prozkoumat spoustu dalších funkcí.</span><span class="sxs-lookup"><span data-stu-id="7a89f-101">Now that you have learned the core concepts of working with tables and records there are many additional functions you can explore.</span></span>
<span data-ttu-id="7a89f-102">Tyto funkce pracují s tabulkami dat, takže je můžete použít se zdrojem dat (jako je Common Data Service (CDS) nebo SharePoint) nebo s kolekcí.</span><span class="sxs-lookup"><span data-stu-id="7a89f-102">These functions work with tables of data so you can use them with a data source (like Common Data Service (CDS) or SharePoint) or a collection.</span></span> <span data-ttu-id="7a89f-103">V jejich používání není žádný rozdíl.</span><span class="sxs-lookup"><span data-stu-id="7a89f-103">There is no difference in their usage.</span></span>

<a name="functions-for-modifying-the-data-source"></a><span data-ttu-id="7a89f-104">Funkce pro úpravu zdroje dat</span><span class="sxs-lookup"><span data-stu-id="7a89f-104">Functions for modifying the data source</span></span>
---------------------------------------

<span data-ttu-id="7a89f-105">Pokud potřebujete zdroj dat aktualizovat, můžete použít dvě hlavní funkce:</span><span class="sxs-lookup"><span data-stu-id="7a89f-105">When it comes to updating a data source, there are two primary functions to consider:</span></span>

-   <span data-ttu-id="7a89f-106">**Patch** – tato funkce slouží buď k úpravě existujícího záznamu, nebo k vytvoření nového záznamu v tabulce.</span><span class="sxs-lookup"><span data-stu-id="7a89f-106">**Patch** -- This function is used to either edit an existing record or to create a new record in a table.</span></span> <span data-ttu-id="7a89f-107">Dokáže zapsat jedno nebo více polí najednou.</span><span class="sxs-lookup"><span data-stu-id="7a89f-107">It can write one or more fields at a time.</span></span>

-   <span data-ttu-id="7a89f-108">**Remove** – tato funkce slouží k odebrání (odstranění) záznamu z tabulky.</span><span class="sxs-lookup"><span data-stu-id="7a89f-108">**Remove** -- This function is used to remove (delete) a record from a table.</span></span>

<span data-ttu-id="7a89f-109">Například do **Galerie** záznamů můžete přidat tlačítko **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="7a89f-109">For example, in your **Gallery** of records, you can add a **Delete** button.</span></span> <span data-ttu-id="7a89f-110">Funkce **Remove** by tuto funkčnost zajistila.</span><span class="sxs-lookup"><span data-stu-id="7a89f-110">The **Remove** function would provide that functionality.</span></span>

<a name="functions-for-getting-rearranging-and-counting-records"></a><span data-ttu-id="7a89f-111">Funkce pro načtení, přeuspořádání a počítání záznamů</span><span class="sxs-lookup"><span data-stu-id="7a89f-111">Functions for getting, rearranging, and counting records</span></span>
--------------------------------------------------------

<span data-ttu-id="7a89f-112">Někdy chcete získat přístup k záznamu na základě jeho umístění a nikoli jeho hodnoty.</span><span class="sxs-lookup"><span data-stu-id="7a89f-112">Sometimes you want to access a record based on its location instead of its value.</span></span> <span data-ttu-id="7a89f-113">Pokud byste například chtěli vytvořit funkci pro zobrazení čísla faktury posledního záznamu v tabulce, použili byste funkci **Last**.</span><span class="sxs-lookup"><span data-stu-id="7a89f-113">For example, if you wanted to build functionality to get the invoice number of the last record in the table to display you would use the **Last** function.</span></span>

-   <span data-ttu-id="7a89f-114">**First** – tato funkce vrátí první (nejvyšší) záznam v tabulce.</span><span class="sxs-lookup"><span data-stu-id="7a89f-114">**First** -- This function returns the first (top) record in the table.</span></span>

-   <span data-ttu-id="7a89f-115">**Last** – tato funkce vrátí poslední (nejnižší) záznam v tabulce.</span><span class="sxs-lookup"><span data-stu-id="7a89f-115">**Last** -- Thisfunction returns the last (bottom) record in the table.</span></span>

-   <span data-ttu-id="7a89f-116">**Shuffle** – tato funkce přeuspořádá záznamy v tabulce do náhodného pořadí.</span><span class="sxs-lookup"><span data-stu-id="7a89f-116">**Shuffle** -- This function reorders the records in your table in random order.</span></span>

-   <span data-ttu-id="7a89f-117">**CountRows** – tato funkce spočítá počet záznamů v tabulce.</span><span class="sxs-lookup"><span data-stu-id="7a89f-117">**CountRows** -- This function counts the number of records in your table.</span></span>

<span data-ttu-id="7a89f-118">Pokud se při zkoumání těchto funkcí chcete pobavit, vytvořte náhodnou funkci pro výběr záznamu z tabulky.</span><span class="sxs-lookup"><span data-stu-id="7a89f-118">A fun way to explore these functions is to build a random function for picking a record from a table.</span></span> <span data-ttu-id="7a89f-119">Kombinací funkcí **Shuffle** a **First** můžete vytvořit virtuální losování.</span><span class="sxs-lookup"><span data-stu-id="7a89f-119">You combine **Shuffle** and **First** to have a virtual "pick a winner out of a hat".</span></span> <span data-ttu-id="7a89f-120">V následujícím příkladu se používá kolekce **collectCustomerInvoices**.</span><span class="sxs-lookup"><span data-stu-id="7a89f-120">The following example uses the **collectCustomerInvoices** collection.</span></span>

```
First(Shuffle(collectCustomerInvoices)).ID
```

<span data-ttu-id="7a89f-121">Tento vzorec použijte u vlastnosti **Text** ovládacího prvku **Popisek** k zobrazení náhodného ID.</span><span class="sxs-lookup"><span data-stu-id="7a89f-121">Use that formula in the **Text** property of a **Label** control to display a random ID.</span></span>

<a name="math-functions-with-tables"></a><span data-ttu-id="7a89f-122">Matematické funkce s tabulkami</span><span class="sxs-lookup"><span data-stu-id="7a89f-122">Math functions with tables</span></span>
--------------------------

<span data-ttu-id="7a89f-123">V modulu [Vytvoření základního vzorce pro změnu vlastností v aplikaci plátna PowerApps](https://docs.microsoft.com/learn/modules/change-properties/) jste se dozvěděli o agregačních funkcích pro součet, průměr a jiné operace s čísly.</span><span class="sxs-lookup"><span data-stu-id="7a89f-123">In the module, [Author a basic formula to change properties in PowerApps canvas apps](https://docs.microsoft.com/learn/modules/change-properties/), you learned about the aggregation functions for summing, averaging, and other operation on numbers.</span></span> <span data-ttu-id="7a89f-124">Stejný koncept teď můžete použít u tabulky.</span><span class="sxs-lookup"><span data-stu-id="7a89f-124">Now you can apply that same concept to a table.</span></span>

<span data-ttu-id="7a89f-125">V tomto příkladu se používá následující tabulka dat uložená v kolekci s názvem collectCustomerInvoices.</span><span class="sxs-lookup"><span data-stu-id="7a89f-125">For this example, reference the following table of data stored in a collection named collectCustomerInvoices.</span></span>

| <span data-ttu-id="7a89f-126">ID</span><span class="sxs-lookup"><span data-stu-id="7a89f-126">ID</span></span>                  | <span data-ttu-id="7a89f-127">Date</span><span class="sxs-lookup"><span data-stu-id="7a89f-127">Date</span></span>                 | <span data-ttu-id="7a89f-128">CustomerName</span><span class="sxs-lookup"><span data-stu-id="7a89f-128">CustomerName</span></span>    | <span data-ttu-id="7a89f-129">Amount</span><span class="sxs-lookup"><span data-stu-id="7a89f-129">Amount</span></span>          |
| :-------------------| :------------------- | :---------------| :---------------|
| <span data-ttu-id="7a89f-130">1</span><span class="sxs-lookup"><span data-stu-id="7a89f-130">1</span></span>                   | <span data-ttu-id="7a89f-131">10. 4. 2019</span><span class="sxs-lookup"><span data-stu-id="7a89f-131">4/10/2019</span></span>            | <span data-ttu-id="7a89f-132">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="7a89f-132">Fabrikam</span></span>        | <span data-ttu-id="7a89f-133">212,00</span><span class="sxs-lookup"><span data-stu-id="7a89f-133">212.00</span></span>          |
| <span data-ttu-id="7a89f-134">2</span><span class="sxs-lookup"><span data-stu-id="7a89f-134">2</span></span>                   | <span data-ttu-id="7a89f-135">1. 3. 2019</span><span class="sxs-lookup"><span data-stu-id="7a89f-135">3/1/2019</span></span>             | <span data-ttu-id="7a89f-136">Contoso</span><span class="sxs-lookup"><span data-stu-id="7a89f-136">Contoso</span></span>         | <span data-ttu-id="7a89f-137">47,89</span><span class="sxs-lookup"><span data-stu-id="7a89f-137">47.89</span></span>           |
| <span data-ttu-id="7a89f-138">3</span><span class="sxs-lookup"><span data-stu-id="7a89f-138">3</span></span>                   | <span data-ttu-id="7a89f-139">14. 3. 2019</span><span class="sxs-lookup"><span data-stu-id="7a89f-139">3/14/2019</span></span>            | <span data-ttu-id="7a89f-140">Contoso</span><span class="sxs-lookup"><span data-stu-id="7a89f-140">Contoso</span></span>         | <span data-ttu-id="7a89f-141">32,99</span><span class="sxs-lookup"><span data-stu-id="7a89f-141">32.99</span></span>           |
| <span data-ttu-id="7a89f-142">4</span><span class="sxs-lookup"><span data-stu-id="7a89f-142">4</span></span>                   | <span data-ttu-id="7a89f-143">2. 4. 2019</span><span class="sxs-lookup"><span data-stu-id="7a89f-143">4/2/2019</span></span>             | <span data-ttu-id="7a89f-144">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="7a89f-144">Fabrikam</span></span>        | <span data-ttu-id="7a89f-145">105,32</span><span class="sxs-lookup"><span data-stu-id="7a89f-145">105.32</span></span>          |

1.  <span data-ttu-id="7a89f-146">Na obrazovku umístěte ovládací prvek **Popisek**.</span><span class="sxs-lookup"><span data-stu-id="7a89f-146">Place a **Label** control on the screen</span></span>

2.  <span data-ttu-id="7a89f-147">Vlastnost **Text** nastavte takto: Average(collectCustomerInvoices, Amount)</span><span class="sxs-lookup"><span data-stu-id="7a89f-147">Set the **Text** property to: Average(collectCustomerInvoices, Amount)</span></span>

<span data-ttu-id="7a89f-148">Na základě ukázkových dat zobrazí popisek hodnotu 99,55.</span><span class="sxs-lookup"><span data-stu-id="7a89f-148">The label will display 99.55 based on the example data.</span></span> <span data-ttu-id="7a89f-149">Matematické funkce představují skvělý způsob, jak uživatelům poskytnout další informace.</span><span class="sxs-lookup"><span data-stu-id="7a89f-149">The math functions are a great way to provide additional information to your users.</span></span> 
