---
ms.openlocfilehash: 431fbd560df6b926696a2df0fac219aa6b145108
ms.sourcegitcommit: ea295d90d665cb91222895600f8945aff5a20f02
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58218046"
---
<span data-ttu-id="e84e5-101">K prozkoumání možností návrhu můžete použít ukázkové aplikace na webu [powerapps.com](https://powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="e84e5-101">On [powerapps.com](https://powerapps.com), you can use a sample app to explore design possibilities.</span></span> <span data-ttu-id="e84e5-102">Zároveň přitom objevíte koncepce, které můžete použít při vývoji vlastních aplikací.</span><span class="sxs-lookup"><span data-stu-id="e84e5-102">You'll also discover concepts that you can apply as you develop your own apps.</span></span> <span data-ttu-id="e84e5-103">Všechny ukázkové aplikace používají fiktivní data k prezentaci nějakého scénáře z reálného světa.</span><span class="sxs-lookup"><span data-stu-id="e84e5-103">Every sample app uses fictitious data to showcase a real-world scenario.</span></span>

<span data-ttu-id="e84e5-104">Další podrobnosti najdete v dokumentaci, která je součástí jednotlivých ukázkových aplikací.</span><span class="sxs-lookup"><span data-stu-id="e84e5-104">For more details, be sure to check out the documentation that's specific to each sample app.</span></span>

![Ukázková aplikace Fundraiser](../media/fundraiser-app1.png)

## <a name="get-sample-apps"></a><span data-ttu-id="e84e5-106">Získání ukázkových aplikací</span><span class="sxs-lookup"><span data-stu-id="e84e5-106">Get sample apps</span></span>

<span data-ttu-id="e84e5-107">Než si budete moct prohlédnout nebo upravit modelem řízené ukázkové aplikace, musíte je napřed nainstalovat do databáze služby Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e84e5-107">Before you can play around with or edit the model-driven sample apps, you must set them up in a Common Data Service database.</span></span> <span data-ttu-id="e84e5-108">Nejprve vytvořte zkušební prostředí a databázi a nezapomeňte zaškrtnout políčko **Zahrnout ukázkové aplikace a data**.</span><span class="sxs-lookup"><span data-stu-id="e84e5-108">First, create a trial environment and database, and be sure to select the **Include sample apps and data** check box.</span></span>

![Vytvoření databáze](../media/create-database2.png)

> [!IMPORTANT]
> <span data-ttu-id="e84e5-110">Zaškrtnutím tohoto políčka nainstalujete do databáze všechny dostupné ukázkové aplikace.</span><span class="sxs-lookup"><span data-stu-id="e84e5-110">By selecting this check box, you install all available sample apps in your database.</span></span> <span data-ttu-id="e84e5-111">Ukázkové aplikace jsou určené pro vzdělávací a demonstrační účely.</span><span class="sxs-lookup"><span data-stu-id="e84e5-111">Sample apps are for educational and demonstration purposes.</span></span> <span data-ttu-id="e84e5-112">Nedoporučujeme je instalovat do produkčních databází.</span><span class="sxs-lookup"><span data-stu-id="e84e5-112">We don't recommend installing them in production databases.</span></span>

## <a name="customize-a-sample-app"></a><span data-ttu-id="e84e5-113">Přizpůsobení ukázkové aplikace</span><span class="sxs-lookup"><span data-stu-id="e84e5-113">Customize a sample app</span></span>

1. <span data-ttu-id="e84e5-114">Přihlaste se k webu [powerapps.com](https://powerapps.com) a jako režim návrhu vyberte **Modelem řízený**.</span><span class="sxs-lookup"><span data-stu-id="e84e5-114">Sign in to [powerapps.com](https://powerapps.com), and select **Model-driven** as the design mode.</span></span>

    ![Výběr režimu návrhu](../media/choose-design-mode.png)

2. <span data-ttu-id="e84e5-116">Na domovské stránce najeďte myší na ukázkovou aplikaci, například *Fundraiser*, a vyberte **Přizpůsobit**.</span><span class="sxs-lookup"><span data-stu-id="e84e5-116">On the home page, hover over a sample app, such as *Fundraiser* and select **Customize**.</span></span>

    <span data-ttu-id="e84e5-117">Otevře se návrhář aplikací, který vám nabídne několik možností pro přizpůsobení aplikace.</span><span class="sxs-lookup"><span data-stu-id="e84e5-117">The App Designer opens, providing multiple options for customizing the app.</span></span>


## <a name="remove-sample-apps-and-data"></a><span data-ttu-id="e84e5-118">Odebrání ukázkových aplikací a dat</span><span class="sxs-lookup"><span data-stu-id="e84e5-118">Remove sample apps and data</span></span> 
<span data-ttu-id="e84e5-119">Při odebírání ukázkových aplikací a dat mějte na paměti tyto skutečnosti:</span><span class="sxs-lookup"><span data-stu-id="e84e5-119">Keep these points in mind when removing samples apps and data:</span></span>

- <span data-ttu-id="e84e5-120">Odstranění ukázkové aplikace vyžaduje odstranění odpovídajícího [spravovaného řešení](https://docs.microsoft.com/dynamics365/customer-engagement/developer/uninstall-delete-solution).</span><span class="sxs-lookup"><span data-stu-id="e84e5-120">Deleting a sample app requires deleting the corresponding [managed solution](https://docs.microsoft.com/dynamics365/customer-engagement/developer/uninstall-delete-solution).</span></span>
- <span data-ttu-id="e84e5-121">Při odstranění řešení se odstraní také všechna ukázková data specifická pro vlastní entity této aplikace.</span><span class="sxs-lookup"><span data-stu-id="e84e5-121">Deleting the solution also deletes any sample data that's specific to the custom entities for the app.</span></span>
- <span data-ttu-id="e84e5-122">Pokud byla ukázková aplikace přizpůsobena, můžou existovat [závislosti](https://docs.microsoft.com/dynamics365/customer-engagement/developer/dependency-tracking-solution-components), které je potřeba před odstraněním řešení odebrat.</span><span class="sxs-lookup"><span data-stu-id="e84e5-122">If customizations were made to the sample app, there might be [dependencies](https://docs.microsoft.com/dynamics365/customer-engagement/developer/dependency-tracking-solution-components) that must be removed before the solution can be deleted.</span></span>

<span data-ttu-id="e84e5-123">K odebrání ukázkových aplikací a dat použijte následující postup.</span><span class="sxs-lookup"><span data-stu-id="e84e5-123">To remove sample apps and data, follow these steps.</span></span>

1. <span data-ttu-id="e84e5-124">Přihlaste se k [portálu pro správu Microsoft PowerApps](https://admin.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="e84e5-124">Sign in to the [Microsoft PowerApps admin portal](https://admin.powerapps.com).</span></span>
2. <span data-ttu-id="e84e5-125">Vyberte prostředí.</span><span class="sxs-lookup"><span data-stu-id="e84e5-125">Select an environment.</span></span>
3. <span data-ttu-id="e84e5-126">Vyberte **Centrum pro správu Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="e84e5-126">Select **Dynamics 365 Administration Center**.</span></span>

    ![Centrum pro správu Dynamics 365](../media/admin-center.png)

4. <span data-ttu-id="e84e5-128">V seznamu vyberte svou databázi a pak vyberte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="e84e5-128">Select your database in the list, then select **Open**.</span></span>

    ![Výběr databáze](../media/select-database.png)

5. <span data-ttu-id="e84e5-130">Přejděte na **Nastavení \> Řešení**.</span><span class="sxs-lookup"><span data-stu-id="e84e5-130">Go to **Settings \> Solutions**.</span></span>
6. <span data-ttu-id="e84e5-131">Vyberte řešení pro aplikaci, která se musí odstranit, a pak vyberte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="e84e5-131">Select the solution for the app that must be deleted, then select **Delete**.</span></span>

    ![Odstranění řešení](../media/delete-solution.png)

<span data-ttu-id="e84e5-133">Výběrem možnosti **Upřesnit** na portálu tvůrce můžete také přejít na seznam řešení a pak v adrese URL odstranit všechno, co následuje za **.dynamics.com/**.</span><span class="sxs-lookup"><span data-stu-id="e84e5-133">You can also go to the list of solutions by selecting **Advanced** in the maker portal and then deleting everything in the URL after **.dynamics.com/**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e84e5-134">Neodstraňujte jiná systémová řešení, pokud nevíte, jaký to bude mít vliv.</span><span class="sxs-lookup"><span data-stu-id="e84e5-134">Don't delete other system solutions unless you're aware of the effect.</span></span>

## <a name="install-or-uninstall-sample-data"></a><span data-ttu-id="e84e5-135">Instalace nebo odinstalace ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="e84e5-135">Install or uninstall sample data</span></span>
1. <span data-ttu-id="e84e5-136">Přihlaste se k [portálu pro správu PowerApps](https://admin.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="e84e5-136">Sign in to the [PowerApps admin portal](https://admin.powerapps.com).</span></span>
1. <span data-ttu-id="e84e5-137">Vyberte prostředí.</span><span class="sxs-lookup"><span data-stu-id="e84e5-137">Select an environment.</span></span>
1. <span data-ttu-id="e84e5-138">Vyberte **Centrum pro správu Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="e84e5-138">Select **Dynamics 365 Administration Center**.</span></span>

    ![Centrum pro správu Dynamics 365](../media/admin-center.png)

1. <span data-ttu-id="e84e5-140">V seznamu vyberte svou databázi a pak vyberte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="e84e5-140">Select your database in the list, then select **Open**.</span></span>

    ![Výběr databáze](../media/select-database.png)

1. <span data-ttu-id="e84e5-142">Přejděte na **Nastavení \> Správa dat \> Ukázková data**.</span><span class="sxs-lookup"><span data-stu-id="e84e5-142">Go to **Settings \> Data Management \> Sample Data**.</span></span>
1. <span data-ttu-id="e84e5-143">Pokud jsou ukázková data nainstalovaná, je k dispozici možnost pro jejich odebrání.</span><span class="sxs-lookup"><span data-stu-id="e84e5-143">If sample data is installed, the option to remove it is available.</span></span> <span data-ttu-id="e84e5-144">V opačném případě je k dispozici možnost pro instalaci ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="e84e5-144">Otherwise, the option to install sample data is available.</span></span>
