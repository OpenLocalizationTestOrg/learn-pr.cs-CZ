---
ms.openlocfilehash: 6ff71642c9ad1614c6456dd8cc07525534cfce50
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57697501"
---
<span data-ttu-id="45ed7-101">Teď se podrobněji podíváme na obrazovky a další ovládací prvky, které definují chování aplikací generovaných v Microsoft PowerApps Studiu.</span><span class="sxs-lookup"><span data-stu-id="45ed7-101">We're now going to look more closely at the screens and other controls that define the behavior of apps that Microsoft PowerApps generates.</span></span> <span data-ttu-id="45ed7-102">Nebudeme zabíhat do všech podrobností, ale když budete něco vědět o tom, jak tyto aplikace fungují, pomůže vám to při vytváření vlastních aplikací.</span><span class="sxs-lookup"><span data-stu-id="45ed7-102">We won't go through all the details, but knowing more about how these apps work will help you build your own apps.</span></span>

## <a name="understand-controls-in-powerapps"></a><span data-ttu-id="45ed7-103">Princip ovládacích prvků v PowerApps</span><span class="sxs-lookup"><span data-stu-id="45ed7-103">Understand controls in PowerApps</span></span>
<span data-ttu-id="45ed7-104">Ovládací prvek je prvek uživatelského rozhraní, který provádí nějakou akci nebo zobrazuje informace.</span><span class="sxs-lookup"><span data-stu-id="45ed7-104">A control is just a UI element that produces an action or shows information.</span></span> <span data-ttu-id="45ed7-105">Mnoho ovládacích prvků v PowerApps je úplně stejných jako ovládací prvky, které používáte v jiných aplikacích: popisky, vstupní textová pole, rozevírací seznamy, navigační prvky atd.</span><span class="sxs-lookup"><span data-stu-id="45ed7-105">Many of the controls in PowerApps are just like controls that you've used in other apps: labels, text-input boxes, drop-down lists, navigation elements, and so on.</span></span>

<span data-ttu-id="45ed7-106">Kromě těchto obvyklých ovládacích prvků má PowerApps také zvláštní ovládací prvky, které můžete najít na kartě **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="45ed7-106">In addition to these typical controls, PowerApps has more specialized controls, which you can find on the **Insert** tab.</span></span>

![Pás karet Vložit v PowerApps Studiu](../media/powerapps-ribbon-controls.png)

<span data-ttu-id="45ed7-108">Tady jsou některé ovládací prvky, se kterými budou vaše aplikace zajímavější a působivější:</span><span class="sxs-lookup"><span data-stu-id="45ed7-108">Here are just a few of the controls that can add interest and impact to your apps:</span></span>

- <span data-ttu-id="45ed7-109">**Galerie:** Tyto ovládací prvky jsou kontejnery rozložení, ve kterých jsou sady ovládacích prvků zobrazujících data ze zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="45ed7-109">**Galleries**: These controls are layout containers that hold a set of controls that show data from a data source.</span></span>
- <span data-ttu-id="45ed7-110">**Formuláře:** Tyto ovládací prvky zobrazují podrobnosti o vašich datech a umožňují vytvářet a upravovat položky.</span><span class="sxs-lookup"><span data-stu-id="45ed7-110">**Forms**: These controls show details about your data and let you create and edit items.</span></span>
- <span data-ttu-id="45ed7-111">**Média:** Těmito ovládacími prvky můžete přidat obrázky na pozadí, tlačítko fotoaparátu (aby uživatelé mohli v aplikaci fotit) nebo čtečku čárových kódů pro rychlé snímání identifikačních údajů.</span><span class="sxs-lookup"><span data-stu-id="45ed7-111">**Media**: These controls let you add background images and include a camera button (so that users can take pictures from the app) and a barcode reader for quickly capturing identification information.</span></span>
- <span data-ttu-id="45ed7-112">**Grafy:** Těmito ovládacími prvky můžete přidat grafy, aby uživatelé mohli na cestách rychle provádět analýzy.</span><span class="sxs-lookup"><span data-stu-id="45ed7-112">**Charts**: These controls let you add charts so that users can do instant analysis while they're on the road.</span></span>

<span data-ttu-id="45ed7-113">Pokud se chcete podívat na dostupné ovládací prvky, vyberte kartu **Vložit** a postupně vyberte různé možnosti.</span><span class="sxs-lookup"><span data-stu-id="45ed7-113">To see what's available, select the **Insert** tab, and then select each option in turn.</span></span>

## <a name="explore-the-browse-screen"></a><span data-ttu-id="45ed7-114">Seznámení s obrazovkou pro procházení</span><span class="sxs-lookup"><span data-stu-id="45ed7-114">Explore the browse screen</span></span>

<span data-ttu-id="45ed7-115">Každá obrazovka v aplikaci obsahuje několik ovládacích prvků, ale jeden ovládací prvek zabírá většinu prostoru na obrazovce.</span><span class="sxs-lookup"><span data-stu-id="45ed7-115">Each screen in the app has multiple controls, but one control takes up most of the screen space.</span></span> <span data-ttu-id="45ed7-116">První obrazovka v aplikaci je obrazovka pro procházení, která má ve výchozím nastavení název **BrowseScreen1**.</span><span class="sxs-lookup"><span data-stu-id="45ed7-116">The first screen in the app is the browse screen, which is named **BrowseScreen1** by default.</span></span>

<span data-ttu-id="45ed7-117">Tady jsou některé ovládací prvky, se kterými se seznámíte na obrazovce pro procházení:</span><span class="sxs-lookup"><span data-stu-id="45ed7-117">Here are some of the controls that you'll want to become familiar with for the browse screen:</span></span>

- <span data-ttu-id="45ed7-118">**BrowseGallery1:** Tento ovládací prvek zabírá většinu obrazovky a zobrazuje data z vašeho zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="45ed7-118">**BrowseGallery1**: This control takes up most of the screen and shows data from your data source.</span></span>
- <span data-ttu-id="45ed7-119">**NextArrow1:** Po výběru tohoto ovládacího prvku se otevře obrazovka s podrobnostmi.</span><span class="sxs-lookup"><span data-stu-id="45ed7-119">**NextArrow1**: When this control is selected, it opens the details screen.</span></span>
- <span data-ttu-id="45ed7-120">**IconNewItem1:** Po výběru tohoto ovládacího prvku se otevře obrazovka pro úpravy nebo vytvoření položky.</span><span class="sxs-lookup"><span data-stu-id="45ed7-120">**IconNewItem1**: When this control is selected, it opens the edit/create screen.</span></span>

![Obrazovka pro procházení s ovládacími prvky](../media/powerapps-browse-screen.png)

## <a name="explore-the-details-screen"></a><span data-ttu-id="45ed7-122">Prozkoumání obrazovky s podrobnostmi</span><span class="sxs-lookup"><span data-stu-id="45ed7-122">Explore the details screen</span></span>
<span data-ttu-id="45ed7-123">Další obrazovkou je obrazovka s podrobnostmi, která má ve výchozím nastavení název **DetailScreen1**.</span><span class="sxs-lookup"><span data-stu-id="45ed7-123">Next is the details screen, which is named **DetailScreen1** by default.</span></span> <span data-ttu-id="45ed7-124">Tady jsou některé z jejích ovládacích prvků:</span><span class="sxs-lookup"><span data-stu-id="45ed7-124">Here are some of its controls:</span></span>

- <span data-ttu-id="45ed7-125">**DetailForm1:** Tento ovládací prvek obsahuje další ovládací prvky.</span><span class="sxs-lookup"><span data-stu-id="45ed7-125">**DetailForm1**: This control contains other controls.</span></span>
- <span data-ttu-id="45ed7-126">**DataCard1:** Toto je ovládací prvek karty.</span><span class="sxs-lookup"><span data-stu-id="45ed7-126">**DataCard1**: This is a card control.</span></span> <span data-ttu-id="45ed7-127">V tomto případě zobrazuje kategorii podlah z tabulky Flooring Estimates, kterou jste mohli vidět v předchozí lekci.</span><span class="sxs-lookup"><span data-stu-id="45ed7-127">In this case, it shows a flooring category from the Flooring Estimates table, as seen in the previous unit.</span></span>
- <span data-ttu-id="45ed7-128">**IconEdit1:** Po výběru tohoto ovládacího prvku se otevře obrazovka pro úpravy/vytvoření položky, aby uživatel mohl upravit aktuální položku.</span><span class="sxs-lookup"><span data-stu-id="45ed7-128">**IconEdit1**: When this control is selected, it opens the edit/create screen so that the user can edit the current item.</span></span>

![Obrazovka s podrobnostmi a ovládacími prvky](../media/powerapps-details-screen.png)

## <a name="explore-the-editcreate-screen"></a><span data-ttu-id="45ed7-130">Prozkoumání obrazovky pro úpravy nebo vytváření</span><span class="sxs-lookup"><span data-stu-id="45ed7-130">Explore the edit/create screen</span></span>
<span data-ttu-id="45ed7-131">Třetí obrazovkou v aplikaci je **EditScreen1**.</span><span class="sxs-lookup"><span data-stu-id="45ed7-131">The third screen in the app is **EditScreen1**.</span></span> <span data-ttu-id="45ed7-132">Tady jsou některé z jejích ovládacích prvků:</span><span class="sxs-lookup"><span data-stu-id="45ed7-132">Here are some of its controls:</span></span>

- <span data-ttu-id="45ed7-133">**EditForm1**: Tento ovládací prvek obsahuje další ovládací prvky.</span><span class="sxs-lookup"><span data-stu-id="45ed7-133">**EditForm1**: This control contains other controls.</span></span>
- <span data-ttu-id="45ed7-134">**DataCard8:** Toto je další ovládací prvek karty, který zobrazuje kategorii podlah z tabulky Flooring Estimates, kterou jste mohli vidět v předchozí lekci.</span><span class="sxs-lookup"><span data-stu-id="45ed7-134">**DataCard8**: This is another card control that shows a flooring category from the Flooring Estimates table, as seen in the previous unit.</span></span>
- <span data-ttu-id="45ed7-135">**IconAccept1:** Po výběru tohoto ovládacího prvku se uloží změny provedené uživatelem.</span><span class="sxs-lookup"><span data-stu-id="45ed7-135">**IconAccept1**: When this control is selected, it saves the user's changes.</span></span>

![Obrazovka pro úpravy nebo vytváření s ovládacími prvky](../media/powerapps-edit-screen.png)

<span data-ttu-id="45ed7-137">Doufáme, že jste v této lekci získali dobrou představu o ovládacích prvcích na jednotlivých obrazovkách této aplikace.</span><span class="sxs-lookup"><span data-stu-id="45ed7-137">Hopefully, this unit gives you a good idea of what controls are on each screen of this app.</span></span>