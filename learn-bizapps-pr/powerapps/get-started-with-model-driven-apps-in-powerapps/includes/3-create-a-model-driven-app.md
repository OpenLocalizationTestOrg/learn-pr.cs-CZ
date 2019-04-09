---
ms.openlocfilehash: f2730af1a93673c2b475f592f051844cf3a4ec02
ms.sourcegitcommit: ea295d90d665cb91222895600f8945aff5a20f02
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58218046"
---
<span data-ttu-id="f2bdf-101">V této lekci vytvoříte modelem řízenou aplikaci pomocí jedné ze standardních entit dostupných ve vašem prostředí Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-101">In this unit, you'll create a model-driven app by using one of the standard entities that's available in your Microsoft PowerApps environment.</span></span>

## <a name="create-a-model-driven-app"></a><span data-ttu-id="f2bdf-102">Vytvoření modelem řízené aplikace</span><span class="sxs-lookup"><span data-stu-id="f2bdf-102">Create a model-driven app</span></span>

1. <span data-ttu-id="f2bdf-103">Přihlaste se k [PowerApps](https://web.powerapps.com/) pomocí účtu své organizace.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-103">Sign in to [PowerApps](https://web.powerapps.com/) by using your organizational account.</span></span>
1. <span data-ttu-id="f2bdf-104">Vyberte požadované prostředí nebo přejděte na [Centrum pro správu PowerApps](https://admin.powerapps.com/) a vytvořte nové.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-104">Select the environment you want, or go to the [PowerApps admin center](https://admin.powerapps.com/) to create a new one.</span></span>
1. <span data-ttu-id="f2bdf-105">Na stránce **Domů** vyberte **Začít od začátku** pro modelem řízenou aplikaci.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-105">On the **Home** page, select the **Start from blank** option for a model-driven app.</span></span>  

    ![Modelem řízený](../media/choose-design-mode.png)

    > [!IMPORTANT]
    > <span data-ttu-id="f2bdf-107">Pokud **Modelem řízený** režim návrhu není k dispozici, možná budete muset [vytvořit prostředí](https://docs.microsoft.com/powerapps/administrator/create-environment).</span><span class="sxs-lookup"><span data-stu-id="f2bdf-107">If the **Model-driven** design mode isn't available, you might need to [create an environment](https://docs.microsoft.com/powerapps/administrator/create-environment).</span></span>

1. <span data-ttu-id="f2bdf-108">V levém podokně vyberte **Aplikace** a pak vyberte **Vytvořit aplikaci**.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-108">In the left pane, select **Apps**, then select **Create an app**.</span></span>
1. <span data-ttu-id="f2bdf-109">Na stránce **Vytvořit novou aplikaci** zadejte název a popis aplikace.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-109">On the **Create a New App** page, enter a name and description for the app.</span></span>
1. <span data-ttu-id="f2bdf-110">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-110">Select **Done**.</span></span> <span data-ttu-id="f2bdf-111">Nová aplikace se zobrazí v návrháři aplikací a teď do ní můžete přidat komponenty.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-111">Your new app appears in the App Designer, and you can now add components to it.</span></span>

## <a name="add-components-to-your-app"></a><span data-ttu-id="f2bdf-112">Přidání komponent do aplikace</span><span class="sxs-lookup"><span data-stu-id="f2bdf-112">Add components to your app</span></span>
<span data-ttu-id="f2bdf-113">Komponenty se do aplikace přidávají pomocí návrháře aplikací.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-113">You add components to your app by using the App Designer.</span></span>

1. <span data-ttu-id="f2bdf-114">Výběrem šipky **Otevřít návrhář mapy webu** otevřete návrhář mapy webu.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-114">Select the **Open the Site Map Designer** arrow to open the site map designer.</span></span>

    ![Vytvoření nové mapy webu](../media/new-sitemap.png)

2. <span data-ttu-id="f2bdf-116">V návrháři mapy webu vyberte **Nová podoblast** a pak v pravém podokně vyberte na kartě **Vlastnosti** následující vlastnosti:</span><span class="sxs-lookup"><span data-stu-id="f2bdf-116">In the site map designer, select **New Subarea**, and then, in the right pane on the **Properties** tab, select the following properties:</span></span>

    - <span data-ttu-id="f2bdf-117">**Typ:** *Entita*</span><span class="sxs-lookup"><span data-stu-id="f2bdf-117">**Type**: *Entity*</span></span>
    - <span data-ttu-id="f2bdf-118">**Entita:** *Obchodní vztah*</span><span class="sxs-lookup"><span data-stu-id="f2bdf-118">**Entity**: *Account*</span></span>

    ![Přidání komponent do mapy webu](../media/sitemap.png)

3. <span data-ttu-id="f2bdf-120">Vyberte **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-120">Select **Save And Close**.</span></span>
4. <span data-ttu-id="f2bdf-121">V návrháři aplikací vyberte **Formuláře** a pak v pravém podokně v oblasti **Hlavní formuláře** vyberte formulář **Obchodní vztah**.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-121">In the App Designer, select **Forms**, and then, in the right pane under **Main Forms**, select the **Account** form.</span></span>

    ![Hlavní formulář obchodního vztahu](../media/main-form.png)

5. <span data-ttu-id="f2bdf-123">V návrháři aplikací vyberte **Zobrazení** a pak vyberte následující vlastnosti:</span><span class="sxs-lookup"><span data-stu-id="f2bdf-123">In the App Designer, select **Views**, then select the following properties:</span></span>

    - <span data-ttu-id="f2bdf-124">Aktivní obchodní vztahy</span><span class="sxs-lookup"><span data-stu-id="f2bdf-124">Active Accounts</span></span>
    - <span data-ttu-id="f2bdf-125">Všechny obchodní vztahy</span><span class="sxs-lookup"><span data-stu-id="f2bdf-125">All Accounts</span></span>
    - <span data-ttu-id="f2bdf-126">Moje aktivní obchodní vztahy</span><span class="sxs-lookup"><span data-stu-id="f2bdf-126">My Active Accounts</span></span>

6. <span data-ttu-id="f2bdf-127">V návrháři aplikací vyberte **Grafy** a pak vyberte graf **Obchodní vztahy podle odvětví**.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-127">In the App Designer, select **Charts**, then select the **Accounts by Industry** chart.</span></span>
7. <span data-ttu-id="f2bdf-128">Na panelu nástrojů návrháře aplikací vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-128">On the App Designer toolbar, select **Save**.</span></span>

<!-- ##  Validate your app
This step checks for component dependencies that are required for the app to work, but haven't yet been added to the app. 

1. On the app designer canvas, select the component that indicates a dependency, such as the **Forms** component. Then, on the right-pane select the **Required** tab, expand **Entity Dependencies** and then select all required dependencies. 

    ![Add dependencies](../media/build-first-model-driven-app/resolve-dependencies.png)

2. Select **Add Dependencies**.
3. On the app designer toolbar, select **Save**.  -->

## <a name="publish-your-app"></a><span data-ttu-id="f2bdf-129">Publikování aplikace</span><span class="sxs-lookup"><span data-stu-id="f2bdf-129">Publish your app</span></span>
<span data-ttu-id="f2bdf-130">Na panelu nástrojů návrháře aplikací vyberte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-130">On the App Designer toolbar, select **Publish**.</span></span>

<span data-ttu-id="f2bdf-131">Po publikování je aplikace připravená ke spuštění nebo sdílení s ostatními.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-131">After you publish the app, it's ready for you to run or share with others.</span></span>

![Jednoduchá aplikace s entitou Obchodní vztah](../media/accounts-quickstart-app.png)
