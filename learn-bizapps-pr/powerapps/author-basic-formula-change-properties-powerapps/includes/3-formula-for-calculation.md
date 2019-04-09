---
ms.openlocfilehash: 8448a5fd6da27b6e22721b8741e8a6907bda8301
ms.sourcegitcommit: e17cc64775307fcf15cef8e0181fdb046ccd227f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58265881"
---
<span data-ttu-id="e94c0-101">Podobně jako v Excelu můžete v PowerApps vytvářet vzorce pro počítání a vracení hodnot.</span><span class="sxs-lookup"><span data-stu-id="e94c0-101">In PowerApps, like Excel, you can create formulas to calculate and return values.</span></span> <span data-ttu-id="e94c0-102">V následující části najdete několik běžných funkcí, které můžete použít při práci s čísly a výpočtech hodnot:</span><span class="sxs-lookup"><span data-stu-id="e94c0-102">The following are a few common functions that you can use when working with numbers and calculating values:</span></span>

-   <span data-ttu-id="e94c0-103">**Average** – vypočítá průměr, neboli aritmetickou střední hodnotu, zadaných argumentů.</span><span class="sxs-lookup"><span data-stu-id="e94c0-103">**Average** - Calculates the average, or arithmetic mean, of its arguments.</span></span>

-   <span data-ttu-id="e94c0-104">**Max** – najde maximální hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e94c0-104">**Max** - Finds the maximum value.</span></span>

-   <span data-ttu-id="e94c0-105">**Min** – najde minimální hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e94c0-105">**Min** - Finds the minimum value.</span></span>

-   <span data-ttu-id="e94c0-106">**Sum** – vypočítá součet zadaných argumentů.</span><span class="sxs-lookup"><span data-stu-id="e94c0-106">**Sum** - Calculates the sum of its arguments.</span></span>

-   <span data-ttu-id="e94c0-107">**StdevP** – vypočítá směrodatnou odchylku zadaných argumentů.</span><span class="sxs-lookup"><span data-stu-id="e94c0-107">**StdevP** - Calculates the standard deviation of its arguments.</span></span>

-   <span data-ttu-id="e94c0-108">**VarP** – vypočítá rozptyl zadaných argumentů.</span><span class="sxs-lookup"><span data-stu-id="e94c0-108">**VarP** - Calculates the variance of its arguments.</span></span>

<span data-ttu-id="e94c0-109">Odkazem na název funkce můžete do výpočtů začlenit ovládací prvky.</span><span class="sxs-lookup"><span data-stu-id="e94c0-109">You can incorporate controls into your calculations by referencing the function name.</span></span>

<span data-ttu-id="e94c0-110">Následující příklad ukazuje, jak vypočítat součet zboží a služeb.</span><span class="sxs-lookup"><span data-stu-id="e94c0-110">the following example shows how to calculate the sum of goods and services.</span></span>

1.  <span data-ttu-id="e94c0-111">Přidejte do aplikace plátna 6 **popisků** a 3 **textová zadání**, jak je znázorněno na následujícím snímku obrazovky.</span><span class="sxs-lookup"><span data-stu-id="e94c0-111">Add 6 **Labels** and 3 **Text Inputs** to your canvas app, as shown in the following screenshot.</span></span>

    ![Výpočet](../media/Calculation.png)

2.  <span data-ttu-id="e94c0-113">Vyberte **Popisek** napravo od Total.</span><span class="sxs-lookup"><span data-stu-id="e94c0-113">Select the **Label** to the right of "Total".</span></span>

3.  <span data-ttu-id="e94c0-114">Vlastnost **Text** změňte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="e94c0-114">Change the **Text** property to the following.</span></span>

```
Sum(TextInput1_1 * TextInput1_2)
```

><span data-ttu-id="e94c0-115">(TextInput1_1 v tomto příkladu představuje Quantity purchased a TextInput1_2 představuje Cost per item.)</span><span class="sxs-lookup"><span data-stu-id="e94c0-115">(In this example, TextInput1_1 is the Quantity purchased and TextInput1_2 is the Cost per item.)</span></span>

4.  <span data-ttu-id="e94c0-116">Výběrem tlačítka **Přehrát** v pravém horním rohu zobrazte náhled aplikace.</span><span class="sxs-lookup"><span data-stu-id="e94c0-116">Now preview the app by selecting the **Play** button in the upper-right corner.</span></span> <span data-ttu-id="e94c0-117">Otestujte vzorec.</span><span class="sxs-lookup"><span data-stu-id="e94c0-117">Test the formula.</span></span>

5.  <span data-ttu-id="e94c0-118">V dalším kroku naformátujete vzorec tak, aby se hodnota zobrazovala jako měna.</span><span class="sxs-lookup"><span data-stu-id="e94c0-118">Next, format the formula to display the value as a Currency.</span></span> <span data-ttu-id="e94c0-119">Aktualizujte vzorec následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="e94c0-119">Update the formula as follows.</span></span>
```
Text(Sum(TextInput1_1 * TextInput1_2),"$#,###0.00")
```

<span data-ttu-id="e94c0-120">Další informace najdete v článku o [agregačních funkcích PowerApps](https://docs.microsoft.com/powerapps/maker/canvas-apps/functions/function-aggregates).</span><span class="sxs-lookup"><span data-stu-id="e94c0-120">For more information, see [PowerApps Aggregate Functions](https://docs.microsoft.com/powerapps/maker/canvas-apps/functions/function-aggregates).</span></span>
