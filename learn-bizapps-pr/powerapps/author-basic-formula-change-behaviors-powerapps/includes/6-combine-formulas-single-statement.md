---
ms.openlocfilehash: 95c35a31a8b4e8f4fc158fdbb19dcc15cb73a12d
ms.sourcegitcommit: e17cc64775307fcf15cef8e0181fdb046ccd227f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58265884"
---
<span data-ttu-id="93679-101">V následujícím příkladu použijeme ovládací prvek **Button** (Tlačítko) a funkci **UpdateContext** k vytvoření dynamického vzorce pro změnu vlastnosti **DisplayMode** tlačítka.</span><span class="sxs-lookup"><span data-stu-id="93679-101">The following example uses the **Button** control and the **UpdateContext** function to create a dynamic formula for changing the **DisplayMode** of a button.</span></span>

1.  <span data-ttu-id="93679-102">Přidejte na plátno dva ovládací prvky **Button** (Tlačítko).</span><span class="sxs-lookup"><span data-stu-id="93679-102">Add two **Button** controls to the canvas.</span></span>

2.  <span data-ttu-id="93679-103">Přidejte na plátno jeden prvek **Label** (Popisek) a jeden prvek **TextInput** (Zadávání textu).</span><span class="sxs-lookup"><span data-stu-id="93679-103">Add one **Label** and one **Text input** to the canvas.</span></span>

    > <span data-ttu-id="93679-104">Prvky umístěte a naformátujte podle následujícího snímku obrazovky.</span><span class="sxs-lookup"><span data-stu-id="93679-104">Use the following screenshot for positioning and formatting.</span></span>

    > ![DisplayMode](../media/DisplayMode.png)

3.  <span data-ttu-id="93679-106">Vyberte ovládací prvek **Tlačítko** (Button3) a nastavte jeho vlastnost **OnSelect** na</span><span class="sxs-lookup"><span data-stu-id="93679-106">Select **Button** control (Button3), set the **OnSelect** property to</span></span>

    > <span data-ttu-id="93679-107">**UpdateContext( { RunningTotal: RunningTotal + TextInput1 } )**.</span><span class="sxs-lookup"><span data-stu-id="93679-107">**UpdateContext( { RunningTotal: RunningTotal + TextInput1 } )**.</span></span>

4.  <span data-ttu-id="93679-108">Vyberte ovládací prvek **Tlačítko** (Button4) a nastavte jeho vlastnost **OnSelect** na</span><span class="sxs-lookup"><span data-stu-id="93679-108">Select the other **Button** control (Button4), set the **OnSelect** property to</span></span>

    > <span data-ttu-id="93679-109">**UpdateContext( { RunningTotal: 0 } )**.</span><span class="sxs-lookup"><span data-stu-id="93679-109">**UpdateContext( { RunningTotal: 0 } )**.</span></span>

5.  <span data-ttu-id="93679-110">U téhož tlačítka nastavte vlastnost **DisplayMode** na **If(RunningTotal \> 0, DisplayMode.Edit, DisplayMode.Disabled)**.</span><span class="sxs-lookup"><span data-stu-id="93679-110">Set the **DisplayMode** property for the same button to **If(RunningTotal \> 0, DisplayMode.Edit, DisplayMode.Disabled)**.</span></span>

    > <span data-ttu-id="93679-111">Všimněte si, že po změně vlastnosti **DisplayMode** se tlačítko zobrazí šedě.</span><span class="sxs-lookup"><span data-stu-id="93679-111">Notice that after you've updated the **DisplayMode** property, it appears greyed out.</span></span>

6.  <span data-ttu-id="93679-112">Vyberte prvek **Popisek** (Label2) a nastavte jeho vlastnost **Text** na **RunningTotal**.</span><span class="sxs-lookup"><span data-stu-id="93679-112">Select the **Label** (Label2), set the **Text** property to **RunningTotal**.</span></span>

7.  <span data-ttu-id="93679-113">Přepněte aplikaci do režimu náhledu, abyste mohli vyzkoušet, jak funguje.</span><span class="sxs-lookup"><span data-stu-id="93679-113">Test it by putting the app in Preview mode.</span></span> <span data-ttu-id="93679-114">Do pole pro zadávání textu vložte hodnotu a vyberte tlačítko **Add**.</span><span class="sxs-lookup"><span data-stu-id="93679-114">In the text input enter a value and select the **Add** button.</span></span>

<span data-ttu-id="93679-115">Když na tlačítko **Add** kliknete, bude tlačítko **Clear** zase možné vybrat.</span><span class="sxs-lookup"><span data-stu-id="93679-115">As soon as you click the **Add** button, the **Clear** button is selectable again.</span></span>

<span data-ttu-id="93679-116">V tomto příkladu používáme funkci **If** k vyhodnocení, jestli je **kontextová proměnná** (RunningTotal) větší než 0.</span><span class="sxs-lookup"><span data-stu-id="93679-116">For this example, an **If** function is used to evaluate if the **Context Variable** (RunningTotal) is greater than 0.</span></span> <span data-ttu-id="93679-117">Pokud je tato **kontextová proměnná** větší než 0, nastavíme vlastnost **DisplayMode** tlačítka **Clear** na hodnotu **Edit**.</span><span class="sxs-lookup"><span data-stu-id="93679-117">If the **Context Variable** is greater than 0, set the **DisplayMode** property for the **Clear** button to **Edit**.</span></span> <span data-ttu-id="93679-118">Pokud tato **kontextová proměnná** nemá žádnou hodnotu nebo má hodnotu 0, nastavíme vlastnost **DisplayMode** na **Disabled**.</span><span class="sxs-lookup"><span data-stu-id="93679-118">If the **Context Variable** has no value or is 0, set the **DisplayMode** property to **Disabled**.</span></span>

<span data-ttu-id="93679-119">Když chcete, aby ovládací prvek takto fungoval, musíte použít **kontextovou proměnnou**?</span><span class="sxs-lookup"><span data-stu-id="93679-119">Do you have to use a **Context Variable** to achieve this type of functionality in a control?</span></span> <span data-ttu-id="93679-120">Ne, vlastnost **DisplayMode** ovládacího prvku **Tlačítko** jste mohli nastavit i jinými způsoby a dosáhnout stejných výsledků.</span><span class="sxs-lookup"><span data-stu-id="93679-120">No, there are several different ways you could have configured the **DisplayMode** property for the **Button** control and achieved the same results.</span></span> <span data-ttu-id="93679-121">Mohli jste například použít stejnou logiku jako v tomto příkladu, ale místo vyhodnocení **kontextové proměnné** využít prvek **Popisek** (Label2).</span><span class="sxs-lookup"><span data-stu-id="93679-121">For instance, by applying the same logic as the example, but this time instead of evaluating a **Context Variable** you decided to use the **Label** (Label2).</span></span> <span data-ttu-id="93679-122">Vlastnost **DisplayMode** tlačítka **Clear** by pak vypadala takto:</span><span class="sxs-lookup"><span data-stu-id="93679-122">The **DisplayMode** property for your **Clear** button would now look like the following.</span></span>

```
If(Value(Label2.Text) > 0, DisplayMode.Edit, DisplayMode.Disabled) 
```

<span data-ttu-id="93679-123">Protože prvek **Popisek** (Label2) uchovává informaci jako text, musíte použít funkci **Value**.</span><span class="sxs-lookup"><span data-stu-id="93679-123">Because the **Label** (Label2) is storing information as text, don't forget to use the **Value** function.</span></span> <span data-ttu-id="93679-124">Funkce **Value** převede textový řetězec na hodnotu.</span><span class="sxs-lookup"><span data-stu-id="93679-124">The **Value** function is used to convert a string of text into a value.</span></span> <span data-ttu-id="93679-125">Pokud byste se pokusili použít jako hodnotu přímo obsah prvku **Popisek** (Label2.Text), výsledkem by byla chyba ve vzorci.</span><span class="sxs-lookup"><span data-stu-id="93679-125">If you attempted to evaluate the **Label** (Label2.Text) against a value, it would result in an error in the formula.</span></span> <span data-ttu-id="93679-126">Jak budete poznávat, vyvíjet a nasazovat další aplikace, zjistíte, že stejné funkčnosti můžete obvykle dosáhnout více způsoby – pomocí různých ovládacích prvků, funkcí a vlastností.</span><span class="sxs-lookup"><span data-stu-id="93679-126">As you continue to learn, develop, and deploy more apps, you will see there are usually at least a few ways to create the same functionality by utilizing different controls, functions, and properties.</span></span>
