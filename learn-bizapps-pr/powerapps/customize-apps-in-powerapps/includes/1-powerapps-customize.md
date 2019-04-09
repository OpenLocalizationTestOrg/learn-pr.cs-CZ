---
ms.openlocfilehash: 6cef468bbcff584d38ac3b3c7358c8df681e3c05
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57697501"
---
<span data-ttu-id="46696-101">V předchozí lekci jste vygenerovali aplikaci Flooring Estimates a začali zkoumat její výchozí návrh.</span><span class="sxs-lookup"><span data-stu-id="46696-101">In a previous unit, you generated the Flooring Estimates app and started to explore its default design.</span></span> <span data-ttu-id="46696-102">Aplikace, které Microsoft PowerApps vygeneruje, můžete hned začít používat, ale často si asi také budete chtít vygenerovanou aplikaci přizpůsobit podle svých potřeb.</span><span class="sxs-lookup"><span data-stu-id="46696-102">Apps that Microsoft PowerApps generates are useful out of the box, but you'll often want to customize a generated app to suit your needs.</span></span>

<span data-ttu-id="46696-103">V této jednotce si projdeme základní změny na jednotlivých obrazovkách v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="46696-103">In this unit, we'll walk you through some basic changes for each screen in the app.</span></span> <span data-ttu-id="46696-104">Aplikace si můžete přizpůsobovat mnoha různými způsoby, ale nejlepší postup, jak se to naučit, je vzít nějakou vygenerovanou aplikaci a provést běžné úpravy.</span><span class="sxs-lookup"><span data-stu-id="46696-104">You can do a lot more to customize an app, but the best way to start learning is to take any generated app and make common customizations.</span></span>

## <a name="browse-screen"></a><span data-ttu-id="46696-105">Obrazovka pro procházení</span><span class="sxs-lookup"><span data-stu-id="46696-105">Browse screen</span></span>
<span data-ttu-id="46696-106">Začneme na obrazovce pro procházení.</span><span class="sxs-lookup"><span data-stu-id="46696-106">We'll start on the browse screen.</span></span> <span data-ttu-id="46696-107">Aplikace už pro každý produkt zobrazuje obrázek a nějaký text, ale rozložení by mohlo být lepší.</span><span class="sxs-lookup"><span data-stu-id="46696-107">The app already shows an image and some text for each product, but the layout could be better.</span></span> <span data-ttu-id="46696-108">Pojďme s tím něco udělat.</span><span class="sxs-lookup"><span data-stu-id="46696-108">Let's work on that.</span></span>

1. <span data-ttu-id="46696-109">V podokně **Obrazovky** na levé straně vyberte **BrowseGallery1**.</span><span class="sxs-lookup"><span data-stu-id="46696-109">In the **Screens** pane on the left, select **BrowseGallery1**.</span></span>

    <span data-ttu-id="46696-110">Rámeček výběru okolo galerie potvrdí vaši volbu.</span><span class="sxs-lookup"><span data-stu-id="46696-110">The selection box around the gallery confirms your choice.</span></span>

    ![Výběr galerie](../media/select-gallery.png)

1. <span data-ttu-id="46696-112">V pravém podokně klikněte na odkaz u položky **Rozložení**. Otevře se podokno **Data**.</span><span class="sxs-lookup"><span data-stu-id="46696-112">In the right pane, open the **Data** pane by selecting the link next to **Layout**.</span></span>

    ![Zobrazení možností rozložení](../media/powerapps-layout.png)

1. <span data-ttu-id="46696-114">Vyberte jiné rozložení, například to, ve kterém se zobrazuje obrázek, název a titulek, ale ne text.</span><span class="sxs-lookup"><span data-stu-id="46696-114">Select a different layout, such as the one that shows the image, the title, and the subtitle but not the body.</span></span>

    ![Změna rozložení](../media/change-layout.png)

1. <span data-ttu-id="46696-116">V horní části galerie vyberte kategorii položky.</span><span class="sxs-lookup"><span data-stu-id="46696-116">Select the category of the item at the top of the gallery.</span></span>

    ![Výběr popisku kategorie](../media/select-category.png)

1. <span data-ttu-id="46696-118">Na řádku vzorců změňte **ThisItem.Category** na **ThisItem.Name**.</span><span class="sxs-lookup"><span data-stu-id="46696-118">Change **ThisItem.Category** to **ThisItem.Name** in the formula bar.</span></span>

1. <span data-ttu-id="46696-119">Opakujte předchozí dva kroky, ale změňte druhý ovládací prvek **Popisek** tak, aby zobrazoval cenu jednotlivých položek.</span><span class="sxs-lookup"><span data-stu-id="46696-119">Repeat the previous two steps, but change the other **Label** control to show the price of each item.</span></span>

    ![Přidání ceny](../media/add-price.png)

<span data-ttu-id="46696-121">Změna rozložení galerie a typů dat, která zobrazuje, je opravdu takto snadná.</span><span class="sxs-lookup"><span data-stu-id="46696-121">It's that easy to change the layout of a gallery and the types of data that it shows.</span></span> <span data-ttu-id="46696-122">A třeba zjistíte, že je to i zábava.</span><span class="sxs-lookup"><span data-stu-id="46696-122">And you might find that it's fun too!</span></span>

## <a name="details-screen"></a><span data-ttu-id="46696-123">Obrazovka s podrobnostmi</span><span class="sxs-lookup"><span data-stu-id="46696-123">Details screen</span></span>

<span data-ttu-id="46696-124">Na obrazovce s podrobnostmi chceme změnit pořadí polí.</span><span class="sxs-lookup"><span data-stu-id="46696-124">On the details screen, we want to change the order of the fields.</span></span> <span data-ttu-id="46696-125">Ovládací prvky na této obrazovce se liší od ovládacích prvků na obrazovce pro procházení, takže se i trochu liší postup pro jejich změnu.</span><span class="sxs-lookup"><span data-stu-id="46696-125">The controls on this screen differ from the controls on the browse screen, so the process for changing them is also a little different.</span></span>

1. <span data-ttu-id="46696-126">V podokně **Obrazovky** na levé straně vyberte **DetailScreen1** > **DetailForm1**.</span><span class="sxs-lookup"><span data-stu-id="46696-126">On the **Screens** pane on the left, select **DetailScreen1** > **DetailForm1**.</span></span>

1. <span data-ttu-id="46696-127">V pravém podokně vyberte text, který zobrazuje počet vybraných polí.</span><span class="sxs-lookup"><span data-stu-id="46696-127">In the right pane, select the text that shows the number of selected fields.</span></span>

    ![Výběr textu, který zobrazuje počet vybraných polí](../media/powerapps-edit-fields.png)

1. <span data-ttu-id="46696-129">Přetáhněte pole **Name** v seznamu polí nahoru a pole **Image** dolů.</span><span class="sxs-lookup"><span data-stu-id="46696-129">Drag the **Name** field to the top of the list of fields, and drag the **Image** field to the bottom.</span></span>

    ![Posunutí polí na obrazovce s podrobnostmi](../media/powerapps-move-fields.png)

## <a name="editcreate-screen"></a><span data-ttu-id="46696-131">Obrazovka pro úpravy nebo vytvoření</span><span class="sxs-lookup"><span data-stu-id="46696-131">Edit/create screen</span></span>

<span data-ttu-id="46696-132">Nakonec chceme na obrazovce, kde uživatel upravuje a vytváří položky, usnadnit zadávání informací do textového pole.</span><span class="sxs-lookup"><span data-stu-id="46696-132">Finally, on the screen where your user edits and creates entries, we want to make it easier to enter information in a text box.</span></span>

1. <span data-ttu-id="46696-133">V podokně **Obrazovky** na levé straně vyberte **EditScreen1** > **EditForm1**.</span><span class="sxs-lookup"><span data-stu-id="46696-133">On the **Screens** pane on the left, select **EditScreen1** > **EditForm1**.</span></span>

1. <span data-ttu-id="46696-134">V pravém podokně vyberte text, který zobrazuje počet vybraných polí.</span><span class="sxs-lookup"><span data-stu-id="46696-134">In the right pane, select the text that shows the number of selected fields.</span></span>

1. <span data-ttu-id="46696-135">Vyberte rozevírací šipku pro seznam **Overview** a pak vyberte **Upravit víceřádkový text**.</span><span class="sxs-lookup"><span data-stu-id="46696-135">Select the drop-down arrow for the **Overview** list, and then select **Edit multi-line text**.</span></span>

    <span data-ttu-id="46696-136">Díky ovládacímu prvku pro víceřádkové úpravy půjde do tohoto pole snadněji zadat více než jenom pár slov.</span><span class="sxs-lookup"><span data-stu-id="46696-136">A multi-line edit control will make it easier to add more than a few words in this field.</span></span>

    ![Změna polí obrazovky pro úpravy nebo vytváření](../media/powerapps-change-editscreen.png)

<span data-ttu-id="46696-138">Viděli jste, jak můžete pomocí několika jednoduchých kroků přispět ke zlepšení vzhledu a způsobu práce s aplikací.</span><span class="sxs-lookup"><span data-stu-id="46696-138">You've seen how a few basic steps can do a lot to improve the appearance and experience of using an app.</span></span> <span data-ttu-id="46696-139">V tomto modulu jsme se zaměřili na PowerApps Studio, které poskytuje mnoho možností pro přizpůsobení aplikací.</span><span class="sxs-lookup"><span data-stu-id="46696-139">In this unit, we focused on PowerApps Studio, which provides lots of options for customizing apps.</span></span> <span data-ttu-id="46696-140">V další lekci prozkoumáme podrobněji ovládací prvky v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="46696-140">In the next unit, we'll explore the controls in the app in greater detail.</span></span>