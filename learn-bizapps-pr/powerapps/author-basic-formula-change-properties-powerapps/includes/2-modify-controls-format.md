---
ms.openlocfilehash: ef9486ab9c3ed9aac49648cba526dbd935b47ef4
ms.sourcegitcommit: e17cc64775307fcf15cef8e0181fdb046ccd227f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58265881"
---
<span data-ttu-id="15e51-101">Každá aplikace plátna, kterou vytvoříte, bude obsahovat a využívat ovládací prvky.</span><span class="sxs-lookup"><span data-stu-id="15e51-101">Every canvas app you build will incorporate and utilize controls.</span></span>
<span data-ttu-id="15e51-102">Vzpomeňte si, že máte na výběr z několika různých typů ovládacích prvků, přičemž každý ovládací prvek má mírně odlišnou sadu **vlastností**.</span><span class="sxs-lookup"><span data-stu-id="15e51-102">Remember, there are several different types of controls to choose from, and each control has a slightly different set of **Properties**.</span></span> <span data-ttu-id="15e51-103">Při vývoji aplikace můžete vytvořit vzorce, které dynamicky mění a aktualizují různé vlastnosti ovládacích prvků, mezi které patří:</span><span class="sxs-lookup"><span data-stu-id="15e51-103">When developing your app, you can create formulas to dynamically change and update different control properties, such as:</span></span>

-   <span data-ttu-id="15e51-104">Formát</span><span class="sxs-lookup"><span data-stu-id="15e51-104">Format</span></span>

-   <span data-ttu-id="15e51-105">Text</span><span class="sxs-lookup"><span data-stu-id="15e51-105">Text</span></span>

-   <span data-ttu-id="15e51-106">Barva</span><span class="sxs-lookup"><span data-stu-id="15e51-106">Color</span></span>

-   <span data-ttu-id="15e51-107">Umístění (X a Y)</span><span class="sxs-lookup"><span data-stu-id="15e51-107">Position (X and Y)</span></span>

<span data-ttu-id="15e51-108">Zde je podrobný pohled na ovládací prvek **Výběr data** včetně jednoduchého příkladu.</span><span class="sxs-lookup"><span data-stu-id="15e51-108">Here's a detailed look at the **Date Picker** control, including a simple example.</span></span>

<span data-ttu-id="15e51-109">Ovládací prvek Výběr data má několik důležitých vlastností:</span><span class="sxs-lookup"><span data-stu-id="15e51-109">The Date Picker control has a few key properties:</span></span>

-   <span data-ttu-id="15e51-110">**DefaultDate** – počáteční hodnota ovládacího prvku data, pokud ji uživatel nezmění</span><span class="sxs-lookup"><span data-stu-id="15e51-110">**DefaultDate** -- The initial value of a date control unless the user changes it.</span></span>

-   <span data-ttu-id="15e51-111">**SelectedDate** – datum aktuálně vybrané v ovládacím prvku data</span><span class="sxs-lookup"><span data-stu-id="15e51-111">**SelectedDate** -- The date currently selected in a date control.</span></span>

-   <span data-ttu-id="15e51-112">**Format** – textový formát, ve kterém ovládací prvek data zobrazuje a ve kterém uživatel zadává datum</span><span class="sxs-lookup"><span data-stu-id="15e51-112">**Format** -- The text format in which the control shows the date and the user specifies the date.</span></span>

-   <span data-ttu-id="15e51-113">**Language** – určuje jazyk použitý k formátování dat včetně názvů měsíců.</span><span class="sxs-lookup"><span data-stu-id="15e51-113">**Language** -- Determines the language used to format dates, including names of months.</span></span> <span data-ttu-id="15e51-114">Pokud tato vlastnost není zadaná, je jazyk určený nastavením zařízení uživatele.</span><span class="sxs-lookup"><span data-stu-id="15e51-114">If this property isn't specified, the user's device setting determines the language.</span></span>

<span data-ttu-id="15e51-115">Následujícím postupem přidejte ovládací prvek **Výběr data** a upravte zobrazený formát.</span><span class="sxs-lookup"><span data-stu-id="15e51-115">Use the following steps to add the **Date Picker** control and modify the displayed format.</span></span>

1.  <span data-ttu-id="15e51-116">V PowerApps Studiu vyberte kartu **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="15e51-116">In PowerApps Studio, select the **Insert** tab.</span></span>

2.  <span data-ttu-id="15e51-117">Na pásu karet vyberte **Ovládací prvky**.</span><span class="sxs-lookup"><span data-stu-id="15e51-117">In the ribbon, select **Controls**.</span></span>

3.  <span data-ttu-id="15e51-118">V rozevírací nabídce vyberte **Výběr data**.</span><span class="sxs-lookup"><span data-stu-id="15e51-118">From the drop-down menu, select **Date Picker**.</span></span> <span data-ttu-id="15e51-119">Při přidání ovládacího prvku **Výběr data** je vlastnost **DefaultDate** standardně nastavená na **Today ()**.</span><span class="sxs-lookup"><span data-stu-id="15e51-119">By default, when you add the **Date Picker** control, the **DefaultDate** is set to **Today().**</span></span>

4.  <span data-ttu-id="15e51-120">Vyberte rozevírací nabídku **vlastností** ovládacího prvku **Výběr data**.</span><span class="sxs-lookup"><span data-stu-id="15e51-120">Select the **Properties** drop-down menu, for the **Date Picker** control.</span></span>

5.  <span data-ttu-id="15e51-121">V rozevírací nabídce vyberte **Format**.</span><span class="sxs-lookup"><span data-stu-id="15e51-121">From the drop-down, select **Format**.</span></span> <span data-ttu-id="15e51-122">Vlastnost **Format** je standardně nastavená na **DateTimeFormat.ShortDate**.</span><span class="sxs-lookup"><span data-stu-id="15e51-122">By default, the **Format** property is set to **DateTimeFormat.ShortDate**.</span></span>

6.  <span data-ttu-id="15e51-123">Aktualizujte vlastnost Format na **DateTimeFormat.LongDate**.</span><span class="sxs-lookup"><span data-stu-id="15e51-123">Update the Format property to be **DateTimeFormat.LongDate**.</span></span> <span data-ttu-id="15e51-124">Tím se zobrazení změní z formátu 30.06.2019 na Neděle 30. Červen 2019.</span><span class="sxs-lookup"><span data-stu-id="15e51-124">This will change the display from the format of 6/30/2019 to Sunday, June 30, 2019.</span></span>

<span data-ttu-id="15e51-125">Mezi další běžné žádosti patří změna vlastnosti Format data z formátu měsíc/den/rok na den/měsíc/rok.</span><span class="sxs-lookup"><span data-stu-id="15e51-125">Another common request is to change the date format property from the format of month/day/year to day/month/year.</span></span> <span data-ttu-id="15e51-126">To můžete udělat ručně nastavením vlastnosti **Format** ovládacího prvku na "dd/mm/yyyy".</span><span class="sxs-lookup"><span data-stu-id="15e51-126">This can be accomplished by manually setting the **Format** property of the control to "dd/mm/yyyy".</span></span> <span data-ttu-id="15e51-127">Další informace o formátování funkce **Text** najdete v článku o [funkci Text v PowerApps](https://docs.microsoft.com/powerapps/maker/canvas-apps/functions/function-text).</span><span class="sxs-lookup"><span data-stu-id="15e51-127">For additional information about how to format the **Text** function, see [PowerApps Text function](https://docs.microsoft.com/powerapps/maker/canvas-apps/functions/function-text).</span></span>
