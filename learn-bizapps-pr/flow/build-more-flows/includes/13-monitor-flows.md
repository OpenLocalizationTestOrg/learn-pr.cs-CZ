---
ms.openlocfilehash: a610b67952ca6f56a5a5864d3d1d80ceee5662cd
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698849"
---
<span data-ttu-id="1ea06-101">Můžete si prohlédnout přehled s počtem úspěšných nebo neúspěšných opakování každého toku dnes, včera nebo v minulých dnech.</span><span class="sxs-lookup"><span data-stu-id="1ea06-101">You can view a summary of the number of times that each flow succeeded or failed today, yesterday, and on previous days.</span></span> <span data-ttu-id="1ea06-102">Můžete si také prohlédnout podrobnosti o každém spuštění, třeba kdy byl tok spuštěn, jak dlouho trval každý krok, a pokud se krok nepodařil, jaký byl důvod.</span><span class="sxs-lookup"><span data-stu-id="1ea06-102">You can also explore details about each run, like when it ran, how long each step took, and, if a step failed, why it failed.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1ea06-103">Požadavky</span><span class="sxs-lookup"><span data-stu-id="1ea06-103">Prerequisites</span></span>

* <span data-ttu-id="1ea06-104">Nainstalujte si mobilní aplikaci Microsoft Flow na podporované zařízení se systémem [Google Android](https://aka.ms/flowmobiledocsandroid), [Apple iOS](https://aka.ms/flowmobiledocsios) nebo [Windows Phone](https://aka.ms/flowmobilewindows).</span><span class="sxs-lookup"><span data-stu-id="1ea06-104">Install the Microsoft Flow mobile app for [Google Android](https://aka.ms/flowmobiledocsandroid), [Apple iOS](https://aka.ms/flowmobiledocsios), or [Windows Phone](https://aka.ms/flowmobilewindows) on a supported device.</span></span> <span data-ttu-id="1ea06-105">Snímky obrazovky v této lekci pocházejí z verze aplikace pro Apple iPhone, ale mobilní aplikace pro Android a Windows Phone jsou podobné.</span><span class="sxs-lookup"><span data-stu-id="1ea06-105">The screenshots in this unit were taken on the Apple iPhone version of the app, but the mobile app for Android and Windows Phone are similar.</span></span>
* <span data-ttu-id="1ea06-106">Pokud ještě nemáte tok, můžete ho vytvořit na [webu Microsoft Flow](https://flow.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="1ea06-106">If you don't already have a flow, create one on the [Microsoft Flow website](https://flow.microsoft.com/).</span></span> <span data-ttu-id="1ea06-107">Kvůli snadnějšímu testování použijte tok, který můžete aktivovat sami, abyste nemuseli čekat na externí událost.</span><span class="sxs-lookup"><span data-stu-id="1ea06-107">For easier testing, use a flow that you can trigger yourself instead of waiting for an external event.</span></span>

<span data-ttu-id="1ea06-108">Tok v tomto výukovém kurzu se spustí, když dostanete z určité adresy e-mail.</span><span class="sxs-lookup"><span data-stu-id="1ea06-108">The flow in this tutorial runs when you receive email from a specific address.</span></span>

> [!TIP]
> <span data-ttu-id="1ea06-109">Při testování můžete k nastavení toku použít vlastní e-mailovou adresu.</span><span class="sxs-lookup"><span data-stu-id="1ea06-109">For testing, you can set up the flow with your personal email address.</span></span> <span data-ttu-id="1ea06-110">Až bude tok připravený ke skutečnému použití, můžete ho nastavit na jinou adresu (třeba na adresu svého vedoucího).</span><span class="sxs-lookup"><span data-stu-id="1ea06-110">Then, when the flow is ready for real use, you can set it up with a different address (for example, your manager's).</span></span>

<span data-ttu-id="1ea06-111">Když se tok spustí, posílá na váš telefon vlastní nabízená oznámení.</span><span class="sxs-lookup"><span data-stu-id="1ea06-111">When the flow runs, it sends a custom push notification to your phone.</span></span>

## <a name="show-a-summary-of-activity"></a><span data-ttu-id="1ea06-112">Zobrazení souhrnných informací o aktivitě</span><span class="sxs-lookup"><span data-stu-id="1ea06-112">Show a summary of activity</span></span>

1. <span data-ttu-id="1ea06-113">Pokud jste tok ještě nespustili, aktivujte spuštění, aby se vygenerovala data.</span><span class="sxs-lookup"><span data-stu-id="1ea06-113">If your flow hasn't run before, trigger a run to generate data.</span></span>

    <span data-ttu-id="1ea06-114">Zobrazení dat v aplikaci může chvíli trvat.</span><span class="sxs-lookup"><span data-stu-id="1ea06-114">It might take some time for the data to appear in the app.</span></span>

1. <span data-ttu-id="1ea06-115">Spusťte mobilní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="1ea06-115">Start the mobile app.</span></span>

    <span data-ttu-id="1ea06-116">Ve výchozím nastavení se zobrazí karta **Aktivita**.</span><span class="sxs-lookup"><span data-stu-id="1ea06-116">By default, the **Activity** tab is shown.</span></span> <span data-ttu-id="1ea06-117">Na této kartě jsou data uspořádaná po dnech. Dnešní data se zobrazují nahoře.</span><span class="sxs-lookup"><span data-stu-id="1ea06-117">This tab organizes data by day, and today's data appears at the top.</span></span>

    ![Aktivita uspořádaná po dnech](../media/activity-day2.png)

    <span data-ttu-id="1ea06-119">Každý záznam obsahuje název toku a ikony, které odpovídají aktivovaným událostem a akcím toku.</span><span class="sxs-lookup"><span data-stu-id="1ea06-119">Each entry shows the name of the flow and icons that correspond to the flow's trigger events and actions.</span></span>

    ![Název toku a ikony aktivovaných událostí/akcí toku](../media/activity-flow-name.png)

    <span data-ttu-id="1ea06-121">Pokud se v daném dni tok aspoň jednou úspěšně spustil, zobrazí se v záznamu počet úspěšných spuštění a čas posledního úspěšného spuštění.</span><span class="sxs-lookup"><span data-stu-id="1ea06-121">If at least one run of a flow has succeeded in a day, an entry shows the number of successful runs and the time of the most recent success.</span></span> <span data-ttu-id="1ea06-122">Pokud se tok nepodařilo spustit, zobrazí se jiný záznam s podobnými informacemi.</span><span class="sxs-lookup"><span data-stu-id="1ea06-122">A different entry shows similar information if a flow has failed.</span></span>

    ![Shrnutí úspěchů a neúspěchů](../media/activity-summary.png)

    <span data-ttu-id="1ea06-124">Pokud tok posílá nabízená oznámení, zobrazí se při úspěšném spuštění dole v záznamu text posledního oznámení.</span><span class="sxs-lookup"><span data-stu-id="1ea06-124">If a flow sends push notifications, the text of the most recent notification appears at the bottom of the entry for successful runs.</span></span>

    ![Příklad nabízeného oznámení](../media/activity-notification.png)

1. <span data-ttu-id="1ea06-126">Pokud se v jednom dni odeslalo více nabízených oznámení, potáhněte oznámení prstem doleva, aby se zobrazila oznámení až ze tří posledních spuštění.</span><span class="sxs-lookup"><span data-stu-id="1ea06-126">If multiple push notifications were sent in a day, swipe left on the notification to view notifications from up to three previous runs.</span></span> <span data-ttu-id="1ea06-127">Pokud se v jednom dni odeslalo více než čtyři oznámení, potáhněte prstem doleva, až se zobrazí **Zobrazit více**. Když tuto možnost vyberete, zobrazí se seznam všech oznámení.</span><span class="sxs-lookup"><span data-stu-id="1ea06-127">If more than four notifications were sent in a day, swipe left until **See more** appears, and then select it to view a list of all notifications.</span></span>

    ![Příklad více nabízených oznámení](../media/activity-notification-list.png)

1. <span data-ttu-id="1ea06-129">Když se chcete vrátit k souhrnným informacím o aktivitě, vyberte **Zpět**.</span><span class="sxs-lookup"><span data-stu-id="1ea06-129">select **Back** to return to the activity summary.</span></span>
1. <span data-ttu-id="1ea06-130">Pokud chcete souhrn aktivit filtrovat, vyberte v pravém horním rohu tlačítko **Filtr** (symbol trychtýře).</span><span class="sxs-lookup"><span data-stu-id="1ea06-130">To filter the activity summary, select the **Filter** button (the funnel symbol) in the upper-right corner.</span></span>

    <span data-ttu-id="1ea06-131">Můžete zobrazit všechny záznamy, jenom záznamy o neúspěších nebo jenom záznamy, které zahrnují nabízená oznámení.</span><span class="sxs-lookup"><span data-stu-id="1ea06-131">You can show all entries, only the failure entries, or only the entries that include push notifications.</span></span>

    ![Zobrazení všech spuštění, jen neúspěchů nebo jen oznámení](../media/activity-filter.png)

## <a name="show-details-of-a-run"></a><span data-ttu-id="1ea06-133">Zobrazení podrobností o spuštění</span><span class="sxs-lookup"><span data-stu-id="1ea06-133">Show details of a run</span></span>

1. <span data-ttu-id="1ea06-134">V souhrnu aktivit vyberte záznam. Zobrazí se podrobnosti o posledním spuštění.</span><span class="sxs-lookup"><span data-stu-id="1ea06-134">In the activity summary, select an entry to show details for the most recent run.</span></span>

    <span data-ttu-id="1ea06-135">U každé události a akce je symbol, ze kterého poznáte, jestli byla úspěšná nebo neúspěšná.</span><span class="sxs-lookup"><span data-stu-id="1ea06-135">For each event and action, a symbol indicates whether the event or action succeeded or failed.</span></span> <span data-ttu-id="1ea06-136">Pokud byla událost nebo akce úspěšná, zobrazí se také, jak dlouho trvala (v sekundách).</span><span class="sxs-lookup"><span data-stu-id="1ea06-136">If it succeeded, the amount of time that it took (in seconds) also appears.</span></span>

    ![Podrobnosti o spuštění](../media/activity-icons.png)

1. <span data-ttu-id="1ea06-138">Pokud chcete zobrazit seznam všech spuštění toku, klepněte na **Historie spuštění**.</span><span class="sxs-lookup"><span data-stu-id="1ea06-138">Tap **Run history** to list all runs of the flow.</span></span> <span data-ttu-id="1ea06-139">Potom vyberte určitý běh, abyste si mohli prohlédnout jeho podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="1ea06-139">Then select a specific run to view its details.</span></span>

    ![Historie úspěchů a neúspěchů](../media/history-mixed.png)
