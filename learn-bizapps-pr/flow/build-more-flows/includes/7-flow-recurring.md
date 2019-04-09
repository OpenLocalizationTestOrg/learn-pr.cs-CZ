---
ms.openlocfilehash: 9a36be34416dd888959548e7bea795733ca2a7d9
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698849"
---
<span data-ttu-id="72fae-101">Můžete také vytvořit tok, který provádí jednu nebo více úloh (třeba posílá sestavu e-mailem) podle konkrétního plánu:</span><span class="sxs-lookup"><span data-stu-id="72fae-101">You can create a flow that performs one or more tasks (for example, sending a report by email) on a specific schedule:</span></span>

* <span data-ttu-id="72fae-102">Jednou denně, každou hodinu nebo minutu</span><span class="sxs-lookup"><span data-stu-id="72fae-102">Once a day, an hour, or a minute</span></span>
* <span data-ttu-id="72fae-103">Ve stanovený den</span><span class="sxs-lookup"><span data-stu-id="72fae-103">On a date that you specify</span></span>
* <span data-ttu-id="72fae-104">Po několika dnech, hodinách nebo minutách, které zadáte</span><span class="sxs-lookup"><span data-stu-id="72fae-104">After a number of days, hours, or minutes that you specify</span></span>

## <a name="create-the-flow"></a><span data-ttu-id="72fae-105">Vytvoření toku</span><span class="sxs-lookup"><span data-stu-id="72fae-105">Create the flow</span></span>

1. <span data-ttu-id="72fae-106">Spusťte Microsoft Flow a přihlaste se pomocí účtu organizace.</span><span class="sxs-lookup"><span data-stu-id="72fae-106">Launch Microsoft Flow and sign in using your organizational account.</span></span>
1. <span data-ttu-id="72fae-107">V levém podokně vyberte **Moje toky**.</span><span class="sxs-lookup"><span data-stu-id="72fae-107">In the left pane, select **My flows**.</span></span>
1. <span data-ttu-id="72fae-108">Vyberte **Nový** a pak vyberte **Vytvořit z prázdné**.</span><span class="sxs-lookup"><span data-stu-id="72fae-108">Select **New**, and then select **Create from blank**.</span></span>

    ![Vytvořit z prázdné](../media/flow-create-blank.png)

1. <span data-ttu-id="72fae-110">V poli **Prohledat všechny konektory a triggery** zadejte *Opakování* a vyberte trigger **Plán – opakování**.</span><span class="sxs-lookup"><span data-stu-id="72fae-110">In the **Search all connectors and triggers** field, enter *Recurrence*, and then select the **Schedule - Recurrence** trigger.</span></span>

    ![Trigger Plán – opakování](../media/select-recurrence.png)

1. <span data-ttu-id="72fae-112">V dialogovém okně **Opakování** zadejte, jak často se má tok spouštět.</span><span class="sxs-lookup"><span data-stu-id="72fae-112">In the **Recurrence** dialog box, specify how often the flow should run.</span></span>

    <span data-ttu-id="72fae-113">Pokud třeba chcete tok spouštět každý druhý týden, zadejte do pole *Interval* hodnotu **2** a do pole *Frekvence* zadejte **Týden**.</span><span class="sxs-lookup"><span data-stu-id="72fae-113">For example, if you want the flow to run every two weeks, enter *2* in the **Interval** field, and select *Week* in the **Frequency** field.</span></span>

    ![Zadání opakování](../media/specify-recurrence.png)

## <a name="specify-advanced-options"></a><span data-ttu-id="72fae-115">Zadání pokročilých možností</span><span class="sxs-lookup"><span data-stu-id="72fae-115">Specify advanced options</span></span>

1. <span data-ttu-id="72fae-116">Postupujte podle pokynů v předchozí části a pak vyberte **Zobrazit pokročilé možnosti**.</span><span class="sxs-lookup"><span data-stu-id="72fae-116">Follow the steps in the previous section, and then select **Show advanced options**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72fae-117">Pokročilé možnosti závisí na hodnotách polí **Interval** a **Frekvence**.</span><span class="sxs-lookup"><span data-stu-id="72fae-117">The advanced options vary, depending on the value of the **Interval** and **Frequency** fields.</span></span> <span data-ttu-id="72fae-118">Pokud dialogové okno, které vidíte, neodpovídá následujícímu obrázku, ověřte, že jsou v polích **Interval** a **Frekvence** nastavené stejné hodnoty jako na obrázku.</span><span class="sxs-lookup"><span data-stu-id="72fae-118">If the dialog box that you see doesn't match the graphic that follows, make sure that the **Interval** and **Frequency** fields are set to the same values that are shown in the graphic.</span></span>

2. <span data-ttu-id="72fae-119">Vyberte časové pásmo a zjistěte, jestli hodnota v poli **Čas spuštění** odpovídá místnímu časovému pásmu, koordinovanému světovému času (UTC) nebo jinému časovému pásmu.</span><span class="sxs-lookup"><span data-stu-id="72fae-119">Select a time zone to specify whether the value of the **Start time** field reflects a local time zone, Universal Coordinated Time (UTC), or another time zone.</span></span>
3. <span data-ttu-id="72fae-120">Zadejte čas spuštění v tomto formátu: *YYYY-MM-DDTHH:MM:SSZ*</span><span class="sxs-lookup"><span data-stu-id="72fae-120">Specify a start time in this format: *YYYY-MM-DDTHH:MM:SSZ*</span></span>
4. <span data-ttu-id="72fae-121">Pokud jste v poli *Frekvence* vybrali **Den**, zadejte čas, kdy se má tok spustit.</span><span class="sxs-lookup"><span data-stu-id="72fae-121">If you selected *Day* in the **Frequency** field, specify the time of day when the flow should run.</span></span>

    <span data-ttu-id="72fae-122">Pokud jste vybrali *Týden*, zadejte den nebo dny v týdnu a jeden nebo více časů, kdy se má tok spustit.</span><span class="sxs-lookup"><span data-stu-id="72fae-122">If you selected *Week*, specify the day or days of the week when the flow should run, and the time or times of day when the flow should run.</span></span>

    <span data-ttu-id="72fae-123">Nastavte tok třeba podle následujícího obrázku. Nezačne dříve než v pondělí 1. ledna 2018 v poledne (pacifického času) a bude se spouštět každý druhý týden v úterý v 17:30 (pacifického času).</span><span class="sxs-lookup"><span data-stu-id="72fae-123">For example, set up the flow as shown in the following graphic to start it no earlier than noon (Pacific time) on Monday, January 1, 2018, and to run it every two weeks, at 5:30 PM (Pacific time) on Tuesday.</span></span>

    ![Upřesnění možností](../media/advanced-options.png)

6. <span data-ttu-id="72fae-125">Přidejte akci nebo akce, které má tok provést.</span><span class="sxs-lookup"><span data-stu-id="72fae-125">Add the action or actions that the flow should take.</span></span>

## <a name="delay-the-flow"></a><span data-ttu-id="72fae-126">Zpoždění toku</span><span class="sxs-lookup"><span data-stu-id="72fae-126">Delay the flow</span></span>

<span data-ttu-id="72fae-127">V dalším kroku se naučíte, jak tok zpozdit.</span><span class="sxs-lookup"><span data-stu-id="72fae-127">Next, you'll learn how to delay the flow.</span></span>

1. <span data-ttu-id="72fae-128">Na horním navigačním panelu vyberte **Moje toky** a pak vyberte **Vytvořit z prázdné**.</span><span class="sxs-lookup"><span data-stu-id="72fae-128">On the top navigation bar, select **My flows**, and then select **Create from blank**.</span></span>
1. <span data-ttu-id="72fae-129">Do pole **Prohledat všechny konektory a triggery** zadejte *Twitter* a vyberte **Twitter – Když se publikuje nový tweet**.</span><span class="sxs-lookup"><span data-stu-id="72fae-129">In the **Search all connectors and triggers** field, enter *Twitter*, and then select **Twitter - When a new tweet is posted**.</span></span> <span data-ttu-id="72fae-130">Dokončete kroky toku.</span><span class="sxs-lookup"><span data-stu-id="72fae-130">Finish the steps in the flow.</span></span>
1. <span data-ttu-id="72fae-131">Vyberte **Nový krok**.</span><span class="sxs-lookup"><span data-stu-id="72fae-131">Select **New step**.</span></span>
1. <span data-ttu-id="72fae-132">V seznamu akcí vyberte **Zpoždění** nebo **Zpoždění do**.</span><span class="sxs-lookup"><span data-stu-id="72fae-132">In the list of actions, select either **Delay** or **Delay until**.</span></span>

    ![Přidání zpoždění](../media/add-delay.png)

1. <span data-ttu-id="72fae-134">V závislosti na vybrané akci proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="72fae-134">Follow one of these steps, depending on the action that you just selected:</span></span>

    * <span data-ttu-id="72fae-135">Pokud jste vybrali **Zpoždění**, zadejte časové jednotky, třeba sekundy, minuty nebo hodiny, a jejich počet.</span><span class="sxs-lookup"><span data-stu-id="72fae-135">If you selected **Delay**, specify a count and a unit of time, like second, minute, or hour.</span></span>

        ![Zadání zpoždění v časových jednotkách](../media/delay.png)

    * <span data-ttu-id="72fae-137">Pokud jste vybrali **Zpoždění do**, zadejte datum v tomto formátu: *YYYY-MM-DDTHH:MM:SSZ*</span><span class="sxs-lookup"><span data-stu-id="72fae-137">If you selected **Delay until**, specify a date in this format: *YYYY-MM-DDTHH:MM:SSZ*</span></span>

        ![Zadání zpoždění do určitého data](../media/delay-until.png)
