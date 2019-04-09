---
ms.openlocfilehash: 22d03cde87808065f4d87e366b26eb8c30c893ae
ms.sourcegitcommit: e17cc64775307fcf15cef8e0181fdb046ccd227f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58265888"
---
<span data-ttu-id="4c298-101">Tabulka dat bude často pocházet z nějakého zdroje dat, takže tabulku musíte vytvořit ručně.</span><span class="sxs-lookup"><span data-stu-id="4c298-101">Often times your table of data will come from a data source so you need to create a table manually.</span></span> <span data-ttu-id="4c298-102">Účelem může být naplnění ovládacího prvku **Rozevírací seznam** nebo definování informací, které se mají použít v ovládacím prvku **Galerie** nebo **Tabulka dat**.</span><span class="sxs-lookup"><span data-stu-id="4c298-102">This might be to populate a **Dropdown** control or to define information to be used in a **Gallery** or **Data table** control.</span></span> <span data-ttu-id="4c298-103">K vytvoření tabulky se používá funkce **Table**.</span><span class="sxs-lookup"><span data-stu-id="4c298-103">To create a table, there is the **Table** function.</span></span>

<span data-ttu-id="4c298-104">Funkce **Table** umožňuje vytvořit tabulku dat, která existuje jen v kontextu, ve kterém se používá ve vaší aplikaci.</span><span class="sxs-lookup"><span data-stu-id="4c298-104">The **Table** function allows you to create a table of data that only exists in the context which it is used within your app.</span></span> <span data-ttu-id="4c298-105">Například k opětovnému vytvoření tabulky z předchozího oddílu můžete u vlastnosti **Položky** ovládacího prvku **Tabulka dat** použít funkci **Table**.</span><span class="sxs-lookup"><span data-stu-id="4c298-105">For example, to recreate the table shown in the previous section you can use the **Table** function in the **Items** property of a **Data table**.</span></span> <span data-ttu-id="4c298-106">Vzorec by měl vypadat takto.</span><span class="sxs-lookup"><span data-stu-id="4c298-106">The formula would be as follows.</span></span>

```
Table({Name: "Chocolate", Price: "$ 3.95", 'Quantity on Hand':
12, 'Quantity on Order': 10}, {Name: "Bread", Price: "$ 4.95",
'Quantity on Hand': 34, 'Quantity on Order': 0}, {Name: "Water",
Price: "$ 1.95", 'Quantity on Hand': 10, 'Quantity on Order':
10})
```

![Funkce Table](../media/table_function.png)

<span data-ttu-id="4c298-108">Někdy potřebujete jednodušší **tabulku** s jedním sloupcem pro naplnění možností ovládacího prvku **Rozevírací seznam**.</span><span class="sxs-lookup"><span data-stu-id="4c298-108">Sometimes you need a simpler, single column **Table** for populating a **Dropdown** control choices.</span></span> <span data-ttu-id="4c298-109">V takovém případě můžete k vytvoření tabulky s jedním sloupcem použít zkrácenou metodu **\[ \]**.</span><span class="sxs-lookup"><span data-stu-id="4c298-109">In that instance you can use the short cut method of **\[ \]** to create a single column table.</span></span> <span data-ttu-id="4c298-110">Níže najdete příklad vytvoření tabulky s jedním sloupcem a barvami Red, Blue a Green.</span><span class="sxs-lookup"><span data-stu-id="4c298-110">An example of creating a single column table with the colors Red, Blue, and Green is shown below.</span></span>

```
["Red", "Blue", "Green"]
```

<span data-ttu-id="4c298-111">Při umístění tohoto vzorce do vlastnosti **Položky** ovládacího prvku **Rozevírací seznam** uvidíte toto.</span><span class="sxs-lookup"><span data-stu-id="4c298-111">By placing that formula in the **Items** property of a **Dropdown** control you will see the following.</span></span>

![Tabulka rozevíracího seznamu](../media/dropdown_table.png)
