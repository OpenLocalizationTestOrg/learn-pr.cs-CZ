---
ms.openlocfilehash: 9ee8af9cc43ec4725b4e3911501142ca131196d9
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698849"
---
<span data-ttu-id="4121c-101">Data, která jsou hnacím motorem obchodních procesů, jsou často uložená v oddělených systémech, ke kterým se obtížně připojuje a které mají obtížnou navigaci.</span><span class="sxs-lookup"><span data-stu-id="4121c-101">The data that fuels business processes is often buried in separate systems that are difficult to connect to and navigate.</span></span> <span data-ttu-id="4121c-102">To je i jeden z důvodů, proč jsou obchodní procesy čím dál složitější a pro uživatele jsou zdrojem nekonečných starostí.</span><span class="sxs-lookup"><span data-stu-id="4121c-102">This is one reason why business processes don't stop becoming complex, and why people rarely stop worrying about them.</span></span> 

![Integrace toku](../media/FlowPlan.png)

<span data-ttu-id="4121c-104">Microsoft Dynamics 365 s Microsoft Flow, Microsoft PowerApps a Microsoft SharePoint celé řešení zjednodušují.</span><span class="sxs-lookup"><span data-stu-id="4121c-104">But Microsoft Dynamics 365 with Microsoft Flow, Microsoft PowerApps, and Microsoft SharePoint makes it all easier.</span></span> <span data-ttu-id="4121c-105">Společně tyto aplikace a služby nabízejí tyto výhody:</span><span class="sxs-lookup"><span data-stu-id="4121c-105">Together, these apps and services provide these advantages:</span></span>

- <span data-ttu-id="4121c-106">Na data můžete jednoduše klepnout.</span><span class="sxs-lookup"><span data-stu-id="4121c-106">The data can easily be tapped.</span></span> 
- <span data-ttu-id="4121c-107">Důležitá obchodní rozhodnutí můžou být rychlejší a inteligentnější.</span><span class="sxs-lookup"><span data-stu-id="4121c-107">Critical business decisions can be made more quickly and more intelligently.</span></span>
- <span data-ttu-id="4121c-108">Lidé se nemusí tolik starat o svá data, ale můžou se soustředit na rozvoj své činnosti.</span><span class="sxs-lookup"><span data-stu-id="4121c-108">People can worry less about what their data is doing and concentrate more on moving their business forward.</span></span>

<span data-ttu-id="4121c-109">V této lekci získáte přehled o:</span><span class="sxs-lookup"><span data-stu-id="4121c-109">This unit gives an overview of:</span></span>

- <span data-ttu-id="4121c-110">Integraci Microsoft Flow do PowerApps</span><span class="sxs-lookup"><span data-stu-id="4121c-110">Integration of Microsoft Flow with PowerApps.</span></span>
- <span data-ttu-id="4121c-111">Integraci Microsoft Flow a PowerApps do SharePointu kvůli jednoduchému sdílení dat v seznamech.</span><span class="sxs-lookup"><span data-stu-id="4121c-111">Integration of Microsoft Flow and PowerApps with SharePoint for easy sharing of data in lists.</span></span>

## <a name="add-a-flow-in-powerapps"></a><span data-ttu-id="4121c-112">Přidání toku v PowerApps</span><span class="sxs-lookup"><span data-stu-id="4121c-112">Add a flow in PowerApps</span></span>

<span data-ttu-id="4121c-113">Přidání toku v aplikaci PowerApps je úplně jednoduché.</span><span class="sxs-lookup"><span data-stu-id="4121c-113">Adding a flow to a PowerApps application is very straightforward.</span></span>

1. <span data-ttu-id="4121c-114">Přejděte na [https://web.powerapps.com](https://web.powerapps.com) a přihlaste se pod účtem své organizace.</span><span class="sxs-lookup"><span data-stu-id="4121c-114">Go to [https://web.powerapps.com](https://web.powerapps.com), and sign in by using your organizational account.</span></span>
1. <span data-ttu-id="4121c-115">Otevřete aplikaci na úpravy.</span><span class="sxs-lookup"><span data-stu-id="4121c-115">Open your app for editing.</span></span>
1. <span data-ttu-id="4121c-116">Na panelu nástrojů vyberte na kartě **Akce** možnost **Toky**.</span><span class="sxs-lookup"><span data-stu-id="4121c-116">On the **Action** tab, select **Flows** on the toolbar.</span></span>

    ![Toky](../media/flow-action.png)

1. <span data-ttu-id="4121c-118">V dialogovém okně **Data** vyberte **Vytvořit nový tok**.</span><span class="sxs-lookup"><span data-stu-id="4121c-118">In the **Data** dialog box, select **Create a new flow**.</span></span>

    ![Vytvoření nového toku](../media/flow-add.png)

    <span data-ttu-id="4121c-120">Microsoft Flow se spustí a zobrazí začátek nového toku, ve kterém je triggerem PowerApps.</span><span class="sxs-lookup"><span data-stu-id="4121c-120">Microsoft Flow is started and shows the beginning of a new flow where PowerApps is a trigger.</span></span> 

    ![PowerApps jako trigger toku](../media/flow-select-powerapp.png)

<span data-ttu-id="4121c-122">Další informace o vytváření toků najdete v tématu [Vytvoření toku ze šablony ve službě Microsoft Flow](https://docs.microsoft.com/flow/get-started-logic-template).</span><span class="sxs-lookup"><span data-stu-id="4121c-122">For more about how to create flows, see [Create a flow from a template in Microsoft Flow](https://docs.microsoft.com/flow/get-started-logic-template).</span></span>

## <a name="add-a-powerapps-application-from-microsoft-flow"></a><span data-ttu-id="4121c-123">Přidání aplikace PowerApps z Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="4121c-123">Add a PowerApps application from Microsoft Flow</span></span>

<span data-ttu-id="4121c-124">Nebo můžete postupovat opačně.</span><span class="sxs-lookup"><span data-stu-id="4121c-124">You can also go in the other direction.</span></span> <span data-ttu-id="4121c-125">Můžete spustit Microsoft Flow a vybrat šablonu, kterou přidáte aplikaci z PowerApps.</span><span class="sxs-lookup"><span data-stu-id="4121c-125">You can start in Microsoft Flow and then select a template to add an app from PowerApps.</span></span>

1. <span data-ttu-id="4121c-126">Spusťte Microsoft Flow a přihlaste se pomocí účtu organizace.</span><span class="sxs-lookup"><span data-stu-id="4121c-126">Launch Microsoft Flow and sign in using your organizational account.</span></span>
1. <span data-ttu-id="4121c-127">V levém podokně vyberte **Šablony**.</span><span class="sxs-lookup"><span data-stu-id="4121c-127">In the left pane, select **Templates**.</span></span>
1. <span data-ttu-id="4121c-128">Vyberte některou z mnoha šablon PowerApps.</span><span class="sxs-lookup"><span data-stu-id="4121c-128">Select one of the many PowerApps templates.</span></span>

    <span data-ttu-id="4121c-129">Pokud si chcete prohlédnout všechny dostupné šablony PowerApps, zadejte do vyhledávání *PowerApps*.</span><span class="sxs-lookup"><span data-stu-id="4121c-129">To see all the PowerApps templates that are available, you can enter search for *PowerApps*.</span></span>

    ![Vyhledávání šablon PowerApps](../media/flow-templates.png)

    <span data-ttu-id="4121c-131">Když se šablona otevře, můžete začít vytvářet tok.</span><span class="sxs-lookup"><span data-stu-id="4121c-131">The template is opened, and you can start building your flow.</span></span>

<span data-ttu-id="4121c-132">Další informace o vytváření aplikací v PowerApps najdete v článku [Vytvoření aplikace plátna ze šablony v PowerApps](https://docs.microsoft.com/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="4121c-132">For more about how to create apps by using PowerApps, see [Create a canvas app from a template in PowerApps](https://docs.microsoft.com/powerapps/maker/canvas-apps/get-started-test-drive).</span></span>

## <a name="integration-of-sharepoint-with-microsoft-flow"></a><span data-ttu-id="4121c-133">Integrace SharePointu do Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="4121c-133">Integration of SharePoint with Microsoft Flow</span></span>

<span data-ttu-id="4121c-134">U zákazníků pravidelně dochází k výměně dat mezi seznamy SharePointu a jinými systémy, které podporují obchodní procesy.</span><span class="sxs-lookup"><span data-stu-id="4121c-134">Customers regularly exchange data between SharePoint lists and other systems to support business processes.</span></span> <span data-ttu-id="4121c-135">Díky důsledné integraci Microsoft Flow do seznamů SharePointu budou tyto scénáře ještě výkonnější.</span><span class="sxs-lookup"><span data-stu-id="4121c-135">These scenarios become more powerful through the deep integration of Microsoft Flow with SharePoint lists.</span></span> 

<span data-ttu-id="4121c-136">Microsoft Flow automatizuje výměnu pracovních postupů a dat mezi SharePointem a různými službami poskytovanými Microsoftem nebo třetí stranou.</span><span class="sxs-lookup"><span data-stu-id="4121c-136">Microsoft Flow automates the exchange of workflows and data between SharePoint and a variety of Microsoft and third-party services.</span></span> <span data-ttu-id="4121c-137">Toky teď můžete vytvářet a spouštět přímo ze seznamu SharePointu a data v SharePointu ukládat i měnit.</span><span class="sxs-lookup"><span data-stu-id="4121c-137">You can now create and start flows directly from a SharePoint list, and store and change that data in SharePoint.</span></span>

1. <span data-ttu-id="4121c-138">V seznamu SharePointu vyberte nahoře na panelu nástrojů **Tok** a pak vyberte **Vytvořit tok**.</span><span class="sxs-lookup"><span data-stu-id="4121c-138">From a SharePoint list, select **Flow** on the top toolbar, and then select **Create a flow**.</span></span>

    ![Vytvoření toku](../media/flow-sharepoint-flow.png)

2. <span data-ttu-id="4121c-140">V podokně **Vytvořit tok** vyberte šablonu, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="4121c-140">In the **Create a flow** pane, select the template to use.</span></span>

    <span data-ttu-id="4121c-141">Spustí se služba Microsoft Flow, ve které vytvoříte tok.</span><span class="sxs-lookup"><span data-stu-id="4121c-141">Microsoft Flow is started, and you can finish creating the flow.</span></span>

## <a name="integration-of-sharepoint-with-powerapps"></a><span data-ttu-id="4121c-142">Integrace SharePointu do PowerApps</span><span class="sxs-lookup"><span data-stu-id="4121c-142">Integration of SharePoint with PowerApps</span></span>

<span data-ttu-id="4121c-143">V PowerApps se můžete během několika minut připojit k obchodní aplikaci na libovolném zařízení, tuto aplikaci vytvořit nebo ji sdílet.</span><span class="sxs-lookup"><span data-stu-id="4121c-143">PowerApps lets you connect to, create, and share business apps on any device in minutes.</span></span> <span data-ttu-id="4121c-144">Přímo ze seznamu SharePointu můžete vytvářet efektivní mobilní formuláře a aplikace bez napsání jediného řádku kódu.</span><span class="sxs-lookup"><span data-stu-id="4121c-144">You can build efficient mobile forms and apps directly from a SharePoint list, without writing a line of code.</span></span> 

<span data-ttu-id="4121c-145">PowerApps a Microsoft Flow sdílejí společné konektorové rozhraní. Díky němu můžete spojovat desítky zdrojů dat, které jsou uložené místně nebo v cloudu.</span><span class="sxs-lookup"><span data-stu-id="4121c-145">PowerApps and Microsoft Flow share a common connector framework that lets you weave in dozens of data sources that are located on premises or in the cloud.</span></span> <span data-ttu-id="4121c-146">Mezi tyto zdroje dat patří Microsoft Exchange, Microsoft SQL Server, Microsoft Dynamics, Salesforce, Google, MailChimp, Twitter a Wunderlist.</span><span class="sxs-lookup"><span data-stu-id="4121c-146">These data sources include Microsoft Exchange, Microsoft SQL Server, Microsoft Dynamics, Salesforce, Google, MailChimp, Twitter, and Wunderlist.</span></span>

1. <span data-ttu-id="4121c-147">V seznamu SharePointu vyberte nahoře na panelu nástrojů **PowerApps** a pak vyberte **Vytvořit aplikaci**.</span><span class="sxs-lookup"><span data-stu-id="4121c-147">From a SharePoint list, select **PowerApps** on the top toolbar, and then select **Create an app**.</span></span>

    ![Vytvoření aplikace](../media/flow-sharepoint-powerapps.png)

2. <span data-ttu-id="4121c-149">V podokně **Vytvořit aplikaci** zadejte název aplikace a vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="4121c-149">In the **Create an app** pane, enter a name for your app, and then select **Create**.</span></span>

    <span data-ttu-id="4121c-150">Spustí se služba Microsoft Flow, ve které vytvoříte aplikaci.</span><span class="sxs-lookup"><span data-stu-id="4121c-150">PowerApps is started, and you can finish creating the app.</span></span>
