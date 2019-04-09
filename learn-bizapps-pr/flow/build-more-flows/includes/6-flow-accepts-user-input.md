---
ms.openlocfilehash: 81a129f089856ea2b8acab256c0156062e290a87
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698849"
---
<span data-ttu-id="41518-101">Toky aktivované tlačítkem můžete přizpůsobit tak, že umožníte uživateli zadávat určité podrobnosti po spuštění daného toku.</span><span class="sxs-lookup"><span data-stu-id="41518-101">You can customize button flows by letting the user provide specific details that will be used when the flow runs.</span></span>

<span data-ttu-id="41518-102">Tok aktivovaný tlačítkem můžete vytvořit na webu Microsoft Flow nebo v mobilní aplikaci pro Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="41518-102">You can create a button flow either on the Microsoft Flow website or in the mobile app for Microsoft Flow.</span></span> <span data-ttu-id="41518-103">V této lekci použijete web.</span><span class="sxs-lookup"><span data-stu-id="41518-103">For this unit, you'll use the website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="41518-104">Požadavky</span><span class="sxs-lookup"><span data-stu-id="41518-104">Prerequisites</span></span>

<span data-ttu-id="41518-105">Musíte mít účet na webu Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="41518-105">You must have an account on the Microsoft Flow website.</span></span>

## <a name="open-the-template"></a><span data-ttu-id="41518-106">Otevření šablony</span><span class="sxs-lookup"><span data-stu-id="41518-106">Open the template</span></span>

1. <span data-ttu-id="41518-107">Spusťte Microsoft Flow a přihlaste se pomocí účtu organizace.</span><span class="sxs-lookup"><span data-stu-id="41518-107">Launch Microsoft Flow and sign in using your organizational account.</span></span>
2. <span data-ttu-id="41518-108">Do pole pro vyhledání šablony zadejte *Visual Studio*.</span><span class="sxs-lookup"><span data-stu-id="41518-108">In the template search box, enter *Visual Studio*.</span></span>
3. <span data-ttu-id="41518-109">Vyberte šablonu **Otevření chyby s prioritou 2 v sadě Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="41518-109">Select the **Open a Priority 2 Bug in Visual Studio** template.</span></span>

    ![Šablona Otevření chyby s prioritou 2 v sadě Visual Studio](../media/2-input.png)

3. <span data-ttu-id="41518-111">Vyberte **Použít tuto šablonu**.</span><span class="sxs-lookup"><span data-stu-id="41518-111">Select **Use this template**.</span></span>

    <span data-ttu-id="41518-112">Šablona **Otevření chyby s prioritou 2 v sadě Visual Studio** používá Visual Studio Team Services (VSTS) a služby nabízených oznámení.</span><span class="sxs-lookup"><span data-stu-id="41518-112">The **Open a Priority 2 Bug in Visual Studio** template uses the Visual Studio Team Services (VSTS) and the Push notification services.</span></span> <span data-ttu-id="41518-113">Pokud nemáte připojení k těmto službám, musíte se k nim přihlásit.</span><span class="sxs-lookup"><span data-stu-id="41518-113">If you don't have a connection to those services, you must sign in to them.</span></span> <span data-ttu-id="41518-114">Tlačítko **Přihlásit se** se zobrazuje jenom v případě, že je potřeba přihlásit se ke službě.</span><span class="sxs-lookup"><span data-stu-id="41518-114">The **Sign in** button appears only if you must sign into a service.</span></span>

4. <span data-ttu-id="41518-115">Po přihlášení ke všem požadovaným službám vyberte **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="41518-115">After you've signed in to all the required services, select **Continue**.</span></span>

    ![Pokračovat](../media/4-input.png)

## <a name="customize-the-user-input"></a><span data-ttu-id="41518-117">Přizpůsobení vstupu uživatele</span><span class="sxs-lookup"><span data-stu-id="41518-117">Customize the user input</span></span>

<span data-ttu-id="41518-118">V dalším kroku změníme tok tak, že přidáme pole, pomocí kterých můžou uživatelé určit změny v chybě VSTS.</span><span class="sxs-lookup"><span data-stu-id="41518-118">Next, we'll change the flow by adding fields that users can use to specify changes to the VSTS bug.</span></span>

1. <span data-ttu-id="41518-119">Na kartě triggeru vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="41518-119">On the trigger card, select **Edit**.</span></span>

    ![Upravit](../media/6-input.png)

2. <span data-ttu-id="41518-121">Výběrem znaménka plus (**+**) rozbalte stránku, abyste mohli přidat vlastní vstupní pole.</span><span class="sxs-lookup"><span data-stu-id="41518-121">Select the plus sign (**+**) to expand the page so that you can add custom input fields.</span></span>

    ![Znaménko plus](../media/7-input.png)

3. <span data-ttu-id="41518-123">Pro každé vlastní pole, které by mělo být k dispozici, když někdo spustí daný tok, zadejte hodnoty do polí **Název vstupu** a **Popis vstupu**.</span><span class="sxs-lookup"><span data-stu-id="41518-123">For each custom field that should be available when someone runs your flow, enter values in the **Input title** and **Input description** field.</span></span>

    <span data-ttu-id="41518-124">V tomto příkladu vytvoříte dvě vlastní vstupní pole (**Postup pro zopakování chyby** a **Závažnost chyby**).</span><span class="sxs-lookup"><span data-stu-id="41518-124">In this example, you'll create two custom input fields (**Bug repro steps** and **Bug severity**).</span></span> <span data-ttu-id="41518-125">Potom každý, kdo tento tok použije, může zadat postup pro zopakování chyby a také ohodnotit závažnost chyby.</span><span class="sxs-lookup"><span data-stu-id="41518-125">Then, anyone who uses the flow can enter the steps to reproduce the bug, and they can also rate the severity of the bug.</span></span>

    ![Pole Postup pro zopakování chyby a Závažnost chyby](../media/8-input.png)

## <a name="customize-the-bug"></a><span data-ttu-id="41518-127">Přizpůsobení chyby</span><span class="sxs-lookup"><span data-stu-id="41518-127">Customize the bug</span></span>

<span data-ttu-id="41518-128">V dalším kroku přizpůsobíme chybu VSTS.</span><span class="sxs-lookup"><span data-stu-id="41518-128">Next, we'll customize the VSTS bug.</span></span>

1. <span data-ttu-id="41518-129">Na kartě **Create a new work item** (Vytvořit novou pracovní položku) vyberte záhlaví, aby se tato karta rozbalila.</span><span class="sxs-lookup"><span data-stu-id="41518-129">On the **Create a new work item** card, select the title bar to expand the card.</span></span>

    ![Záhlaví](../media/9-input.png)

2. <span data-ttu-id="41518-131">Vyberte možnosti, které odpovídají vašemu prostředí VSTS, a pak vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="41518-131">Make the selections that are appropriate for your VSTS environment, and then select **Edit**.</span></span>

    <span data-ttu-id="41518-132">Pokud se například chcete připojit k myinstance.visualstudio.com, zadejte *myinstance*.</span><span class="sxs-lookup"><span data-stu-id="41518-132">For example, to connect to myinstance.visualstudio.com, enter *myinstance*.</span></span>

    ![Upravit](../media/10-input.png)

3. <span data-ttu-id="41518-134">Vyberte **Zobrazit pokročilé možnosti**, aby se zobrazila další pole pro tuto kartu.</span><span class="sxs-lookup"><span data-stu-id="41518-134">Select **Show advanced options** to show the other fields for this card.</span></span>

    ![Zobrazit pokročilé možnosti](../media/11-input.png)

4. <span data-ttu-id="41518-136">V poli **Název** umístěte kurzor před token **Název chyby**, zadejte *Závažnost:*, pak mezeru a vyberte token **Závažnost chyby**.</span><span class="sxs-lookup"><span data-stu-id="41518-136">In the **Title** field, put the cursor before the **Bug title** token, enter *Severity:* followed by a space, and then select the **Bug severity** token.</span></span> <span data-ttu-id="41518-137">Pak mezi tyto dva tokeny zadejte mezeru, dvě pomlčky (*--*) a další mezeru.</span><span class="sxs-lookup"><span data-stu-id="41518-137">Then, between the two tokens, enter a space, two hyphens (*--*), and another space.</span></span>
5. <span data-ttu-id="41518-138">V poli **Popis** umístěte kurzor před token **Popis chyby**, stisknutím klávesy Enter začněte nový řádek a pak vyberte token **Postup pro zopakování chyby**.</span><span class="sxs-lookup"><span data-stu-id="41518-138">In the **Description** field, put the cursor after the **Bug description** token, press Enter to start a new line, and then select the **Bug repro steps** token.</span></span>

    ![Pole Název a Popis](../media/12-input.png)

## <a name="customize-the-push-notification"></a><span data-ttu-id="41518-140">Přizpůsobení nabízeného oznámení</span><span class="sxs-lookup"><span data-stu-id="41518-140">Customize the push notification</span></span>

<span data-ttu-id="41518-141">V dalším kroku změníme nabízené oznámení, které se zobrazuje na vašem telefonu.</span><span class="sxs-lookup"><span data-stu-id="41518-141">Next, we'll change the push notification that you'll get on your phone.</span></span>

1. <span data-ttu-id="41518-142">Na kartě **Send a push notification** (Poslat nabízené oznámení) vyberte záhlaví, aby se tato karta rozbalila.</span><span class="sxs-lookup"><span data-stu-id="41518-142">On the **Send a push notification** card, select the title bar to expand the card.</span></span>
2. <span data-ttu-id="41518-143">V seznamu tokenů dynamického obsahu vyberte **Zobrazit více** a pak do pole **Odkaz** přidejte token **URL**.</span><span class="sxs-lookup"><span data-stu-id="41518-143">In the list of dynamic content tokens, select **See more**, and then add the **URL** token to the **Link** field.</span></span>
3. <span data-ttu-id="41518-144">Do pole **Popisek odkazu** přidejte token **ID**.</span><span class="sxs-lookup"><span data-stu-id="41518-144">In the **Link label** field, add the **Id** token.</span></span>

    ![Pole Odkaz a Popisek odkazu](../media/13-input.png)

4. <span data-ttu-id="41518-146">Vytvořte daný tok výběrem možnosti **Vytvořit tok**.</span><span class="sxs-lookup"><span data-stu-id="41518-146">Select **Create flow** to create the flow.</span></span>

## <a name="run-the-flow"></a><span data-ttu-id="41518-147">Spuštění toku</span><span class="sxs-lookup"><span data-stu-id="41518-147">Run the flow</span></span>

<span data-ttu-id="41518-148">Teď pomocí mobilní aplikace pro Microsoft Flow spustíte tok aktivovaný tlačítkem, který jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="41518-148">You'll now use the mobile app for Microsoft Flow to run the button flow that you just created.</span></span> <span data-ttu-id="41518-149">Provedete celý uživatelský vstup, který je potřeba k vytvoření chyby, která má název, popis, postup pro zopakování a úroveň závažnosti.</span><span class="sxs-lookup"><span data-stu-id="41518-149">You'll provide all the user input that's needed to create a bug that has a title, a description, repro steps, and a severity level.</span></span>

1. <span data-ttu-id="41518-150">V mobilní aplikaci pro Microsoft Flow vyberte v dolní části okna kartu **Tlačítka** a pak vyberte tlačítko **Create a bug report with steps** (Vytvoření sestavy chyb pomocí postupu).</span><span class="sxs-lookup"><span data-stu-id="41518-150">In the mobile app for Microsoft Flow, select the **Buttons** tab at the bottom of the window, and then select the **Create a bug report with steps** button.</span></span>

    ![Vytvoření sestavy chyb pomocí postupu](../media/runmt1-input.png)

2. <span data-ttu-id="41518-152">Zadejte název pro chybu, kterou oznamujete, a vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="41518-152">Enter a title for the bug that you're reporting, and then select **Next**.</span></span>

    ![Název chyby](../media/runmt2-input.png)

3. <span data-ttu-id="41518-154">Zadejte popis chyby, kterou oznamujete, a vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="41518-154">Enter a description of the bug that you're reporting, and then select **Next**.</span></span>

    ![Popis chyby](../media/runmt3-input.png)

4. <span data-ttu-id="41518-156">Zadejte postup pro zopakování chyby, kterou oznamujete, a vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="41518-156">Enter the steps to reproduce the bug that you're reporting, and then select **Next**.</span></span>

    ![Postup pro zopakování chyby](../media/runmt3-1-input.png)

5. <span data-ttu-id="41518-158">Zadejte závažnost chyby, kterou oznamujete, a vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="41518-158">Enter the severity of the bug that you're reporting, and then select **Done**.</span></span>

    ![Závažnost chyby](../media/runmt3-2-input.png)

    <span data-ttu-id="41518-160">Tok se spustí.</span><span class="sxs-lookup"><span data-stu-id="41518-160">The flow runs.</span></span>

6. <span data-ttu-id="41518-161">Vyberte v dolní části okna kartu **Aktivita**, aby se zobrazily výsledky.</span><span class="sxs-lookup"><span data-stu-id="41518-161">Select the **Activity** tab at the bottom of the window to view the results.</span></span>

    ![Výsledky](../media/runmt5-input.png)

7. <span data-ttu-id="41518-163">Pokud chcete zobrazit podrobné výsledky spuštění toku, vyberte krok **Vytvoření nové pracovní položky**.</span><span class="sxs-lookup"><span data-stu-id="41518-163">To view the detailed results of the flow run, select the **Create a new work item** step.</span></span>

    ![Podrobné výsledky](../media/runmt6-input.png)
