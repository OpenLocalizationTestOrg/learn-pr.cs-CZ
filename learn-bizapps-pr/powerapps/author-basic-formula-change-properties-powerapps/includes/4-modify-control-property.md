---
ms.openlocfilehash: 86b2192f49ad9ac41e1bd50fe1c66ed79e59c725
ms.sourcegitcommit: e17cc64775307fcf15cef8e0181fdb046ccd227f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58265881"
---
<span data-ttu-id="c68e9-101">Při práci s ovládacími prvky můžete na základě vlastnosti jednoho ovládacího prvku změnit způsob fungování jiných ovládacích prvků.</span><span class="sxs-lookup"><span data-stu-id="c68e9-101">When working with controls, you can modify the way that other controls function based on another control's properties.</span></span> <span data-ttu-id="c68e9-102">Uživatelé tak mohou ovlivňovat prostředí, ve kterém pracují.</span><span class="sxs-lookup"><span data-stu-id="c68e9-102">This allows users to provide input that affects their experience.</span></span> <span data-ttu-id="c68e9-103">Příkladem může být rozevírací nabídka, kde má uživatel na výběr malé, střední nebo velké písmo.</span><span class="sxs-lookup"><span data-stu-id="c68e9-103">An example would be providing a drop-down menu so a user could choose small, medium, or large.</span></span>
<span data-ttu-id="c68e9-104">Na základě tohoto nastavení se může dynamicky měnit velikost písma v celé aplikaci.</span><span class="sxs-lookup"><span data-stu-id="c68e9-104">Based on this setting, the app could dynamically change the font size throughout the app.</span></span> <span data-ttu-id="c68e9-105">Stejnou logiku můžete použít také pro barvy aplikace, umístění ovládacích prvků nebo zobrazení či skrytí ovládacích prvků podle výběru uživatele.</span><span class="sxs-lookup"><span data-stu-id="c68e9-105">You could also apply the same logic for colors within the app, locations of controls, or showing or hiding controls based on user selections.</span></span> <span data-ttu-id="c68e9-106">Pokud uživatel například zaškrtne políčko „Nový klient“, objeví se na obrazovce pole pro zadání nového klienta.</span><span class="sxs-lookup"><span data-stu-id="c68e9-106">For example, if a user selects a check box for "New Client", the fields for entering a new client would appear on the screen.</span></span>

<span data-ttu-id="c68e9-107">Z následujícího příkladu pochopíte umístění ovládacího prvku na plátně a způsob, jak ho změnit podle zadání uživatele.</span><span class="sxs-lookup"><span data-stu-id="c68e9-107">Use the following example to understand control positioning on the canvas and how to use the user's input to modify it.</span></span> <span data-ttu-id="c68e9-108">Umístění ovládacího prvku na plátně se řídí kombinací dvou vlastností: vlastnosti X a vlastnosti Y.</span><span class="sxs-lookup"><span data-stu-id="c68e9-108">The control location on the canvas is based on a combination of two properties: the X and the Y property.</span></span>

-   <span data-ttu-id="c68e9-109">**X** – vzdálenost mezi levým okrajem ovládacího prvku a levým okrajem obrazovky</span><span class="sxs-lookup"><span data-stu-id="c68e9-109">**X** -- The distance between the left edge of a control and the left edge of the screen.</span></span>

-   <span data-ttu-id="c68e9-110">**Y** – vzdálenost mezi horním okrajem ovládacího prvku a horním okrajem obrazovky</span><span class="sxs-lookup"><span data-stu-id="c68e9-110">**Y** -- The distance between the top edge of a control and the top edge of the screen.</span></span>

<span data-ttu-id="c68e9-111">Vlastnosti **X** a **Y** platí pro všechny ovládací prvky s výjimkou obrazovek.</span><span class="sxs-lookup"><span data-stu-id="c68e9-111">The **X** and **Y** properties apply to all controls except screens.</span></span>
<span data-ttu-id="c68e9-112">Začlenění této funkčnosti vám dává větší kontrolu nad tím, jak se informace uživatelům zobrazují a používají.</span><span class="sxs-lookup"><span data-stu-id="c68e9-112">Incorporating this functionality gives you more control over how information is displayed and consumed by users.</span></span>

1.  <span data-ttu-id="c68e9-113">Přidejte do aplikace plátna ovládací prvek **Rozevírací seznam**.</span><span class="sxs-lookup"><span data-stu-id="c68e9-113">Add a **Dropdown** control to your canvas app.</span></span>

    > <span data-ttu-id="c68e9-114">Vyberte **Rozevírací seznam** a vlastnost **Položky** změňte z **DropDownSample** na Table({Position:\"Top\"},{Position:\"Bottom\"},{Position:\"Middle\"}).</span><span class="sxs-lookup"><span data-stu-id="c68e9-114">Select **Dropdown** and change the **Items** property from **DropDownSample** to Table({Position:\"Top\"},{Position:\"Bottom\"},{Position:\"Middle\"})</span></span>

2.  <span data-ttu-id="c68e9-115">Na kartě **Vložit** klikněte na **Ikony** a vyberte ikonu **Zaškrtnutí**.</span><span class="sxs-lookup"><span data-stu-id="c68e9-115">On the **Insert** tab, click **Icons** and select the **Check** icon.</span></span>

3.  <span data-ttu-id="c68e9-116">Nastavte vlastnost **Y** ikony **Zaškrtnutí**.</span><span class="sxs-lookup"><span data-stu-id="c68e9-116">Set the **Y** property for the **Check** icon.</span></span>

```
If(Dropdown1.Selected.Position ="Top",150,Dropdown1.Selected.Position = "Bottom",650,400)
```

4.  <span data-ttu-id="c68e9-117">Otestujte vzorec.</span><span class="sxs-lookup"><span data-stu-id="c68e9-117">Test the formula.</span></span> <span data-ttu-id="c68e9-118">Vyberte jednotlivé pozice v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="c68e9-118">Select each position from the drop-down menu.</span></span>
    <span data-ttu-id="c68e9-119">Všimněte si, že ikona **Zaškrtnutí** mění svou pozici Y.</span><span class="sxs-lookup"><span data-stu-id="c68e9-119">Notice that the **Check** icon changes its Y position.</span></span>
