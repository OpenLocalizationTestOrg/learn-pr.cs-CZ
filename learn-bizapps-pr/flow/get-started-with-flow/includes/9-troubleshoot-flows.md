---
ms.openlocfilehash: ee04a49393ebcd7fffb76296958eb1efcbf313d4
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698342"
---
<span data-ttu-id="55b89-101">V této lekci se dozvíte, jak řešit běžné problémy, ke kterým může docházet u spouštěných toků.</span><span class="sxs-lookup"><span data-stu-id="55b89-101">In this unit, you'll learn how to troubleshoot common issues that might occur while you run your flows.</span></span>

## <a name="identify-the-error"></a><span data-ttu-id="55b89-102">Identifikace chyby</span><span class="sxs-lookup"><span data-stu-id="55b89-102">Identify the error</span></span>

<span data-ttu-id="55b89-103">Abyste mohli tok opravit, musíte nejdřív zjistit, proč selhal.</span><span class="sxs-lookup"><span data-stu-id="55b89-103">Before you can fix a flow, you must identify why it failed.</span></span> <span data-ttu-id="55b89-104">Každý týden vám přijde e-mail se seznamem chyb.</span><span class="sxs-lookup"><span data-stu-id="55b89-104">You will get an email with a list of failures each week.</span></span>

1. <span data-ttu-id="55b89-105">Vyberte tlačítko **Oznámení** (symbol zvonku) v horní části webového portálu (nebo vyberte kartu **Aktivita** v mobilní aplikaci) a pak v zobrazeném seznamu vyberte příslušný tok.</span><span class="sxs-lookup"><span data-stu-id="55b89-105">Select the **Notifications** button (the bell symbol) at the top of the web portal (or select the **Activity** tab in the mobile app), and then select your flow in the list that appears.</span></span>

    ![Oznámení](../media/notifications-toolbar.png)

2. <span data-ttu-id="55b89-107">Zobrazí se podrobnosti o toku – nejméně u jednoho kroku je symbol červeného vykřičníku (!).</span><span class="sxs-lookup"><span data-stu-id="55b89-107">Details about the flow appear, and at least one step has a red exclamation point (!) symbol.</span></span> <span data-ttu-id="55b89-108">Tento krok otevřete a zkontrolujte chybovou zprávu.</span><span class="sxs-lookup"><span data-stu-id="55b89-108">Open that step, and review the error message.</span></span>

    ![Chybová zpráva](../media/flow-run-failure.png)

## <a name="authentication-failures"></a><span data-ttu-id="55b89-110">Chyby ověřování</span><span class="sxs-lookup"><span data-stu-id="55b89-110">Authentication failures</span></span>

<span data-ttu-id="55b89-111">Toky v mnoha případech selžou v důsledku chyby ověřování.</span><span class="sxs-lookup"><span data-stu-id="55b89-111">In many cases, flows fail because of an authentication error.</span></span> <span data-ttu-id="55b89-112">Pokud dojde k tomuto typu chyby, obsahuje chybová zpráva slova „neautorizovaný“ nebo „nebyl autorizovaný“ nebo se zobrazí kód chyby 401 nebo 403.</span><span class="sxs-lookup"><span data-stu-id="55b89-112">If this type of error occurs, the error message includes the word "Unauthorized," or an error code of 401 or 403 appears.</span></span> <span data-ttu-id="55b89-113">Chyby ověřování se obvykle dají opravit aktualizací připojení.</span><span class="sxs-lookup"><span data-stu-id="55b89-113">You can usually fix authentication errors by updating the connection.</span></span>

1. <span data-ttu-id="55b89-114">V horní části webového portálu vyberte tlačítko **Nastavení** (symbol ozubeného kola) a potom v nabídce vyberte **Připojení**.</span><span class="sxs-lookup"><span data-stu-id="55b89-114">At the top of the web portal, select the **Settings** button (the gear symbol), and then select **Connections** on the menu.</span></span>
2. <span data-ttu-id="55b89-115">Posuňte se k připojení, u kterého se zobrazila chybová zpráva se slovy „neautorizovaný“ nebo „nebyl autorizovaný“.</span><span class="sxs-lookup"><span data-stu-id="55b89-115">Scroll to the connection that you saw the "Unauthorized" error message for.</span></span>
3. <span data-ttu-id="55b89-116">Vedle připojení – ve zprávě s informací, že připojení nebylo ověřeno – vyberte odkaz **Ověřit heslo**.</span><span class="sxs-lookup"><span data-stu-id="55b89-116">Next to the connection, select the **Verify password** link in the message that states that the connection hasn't been authenticated.</span></span>
4. <span data-ttu-id="55b89-117">Podle zobrazených pokynů ověřte svoje přihlašovací údaje.</span><span class="sxs-lookup"><span data-stu-id="55b89-117">Verify your credentials by following the instructions that appear.</span></span> <span data-ttu-id="55b89-118">Pak se vraťte k příslušné chybě běhu toku a vyberte **Znovu odeslat** (Znovu spustit).</span><span class="sxs-lookup"><span data-stu-id="55b89-118">Then return to your flow-run failure, and select **Resubmit**.</span></span>

<span data-ttu-id="55b89-119">Tok by teď měl běžet podle očekávání.</span><span class="sxs-lookup"><span data-stu-id="55b89-119">The flow should now run as expected.</span></span>

## <a name="action-configuration-issues"></a><span data-ttu-id="55b89-120">Problémy s konfigurací akcí</span><span class="sxs-lookup"><span data-stu-id="55b89-120">Action configuration issues</span></span>

<span data-ttu-id="55b89-121">Toky někdy selžou, když nastavení v některé z akcí toku nefunguje podle očekávání.</span><span class="sxs-lookup"><span data-stu-id="55b89-121">Flows sometimes fail if a setting in one of the flow's actions doesn't work as expected.</span></span> <span data-ttu-id="55b89-122">Chybová zpráva v takovém případě obsahuje frázi „neplatný požadavek“ nebo „nebyl nalezen“ nebo se zobrazí kód chyby 400 nebo 404.</span><span class="sxs-lookup"><span data-stu-id="55b89-122">In this case, the error message includes the phrase "Bad request" or "Not found," or an error code 400 or 404 appears.</span></span>

<span data-ttu-id="55b89-123">Chybová zpráva by měla naznačovat, jak chybu opravit.</span><span class="sxs-lookup"><span data-stu-id="55b89-123">The error message should indicate how to fix the failure.</span></span>

1. <span data-ttu-id="55b89-124">Vyberte tlačítko **Upravit** a pak opravte problémy v definici toku.</span><span class="sxs-lookup"><span data-stu-id="55b89-124">Select the **Edit** button, and then fix the issues inside the flow definition.</span></span>
1. <span data-ttu-id="55b89-125">Aktualizovaný tok uložte a pak zkuste spustit tok znovu s aktualizovanou konfigurací – vyberte **Znovu odeslat** (Znovu spustit).</span><span class="sxs-lookup"><span data-stu-id="55b89-125">Save the updated flow, and then select **Resubmit** to try to run the flow again with the updated configuration.</span></span>

## <a name="temporary-issues"></a><span data-ttu-id="55b89-126">Dočasné problémy</span><span class="sxs-lookup"><span data-stu-id="55b89-126">Temporary issues</span></span>

<span data-ttu-id="55b89-127">Pokud se zobrazí kód chyby 500 nebo 502, je chyba dočasná nebo přechodná.</span><span class="sxs-lookup"><span data-stu-id="55b89-127">If error code 500 or 502 appears, the failure is temporary or transient.</span></span>

- <span data-ttu-id="55b89-128">Zkuste spustit tok znovu – vyberte **Znovu odeslat** (Znovu spustit).</span><span class="sxs-lookup"><span data-stu-id="55b89-128">Select **Resubmit** to try to run the flow again.</span></span>

## <a name="issues-with-your-pricing-plan"></a><span data-ttu-id="55b89-129">Problémy s cenovým plánem</span><span class="sxs-lookup"><span data-stu-id="55b89-129">Issues with your pricing plan</span></span>

<span data-ttu-id="55b89-130">Toky se někdy můžou chovat neočekávaně, protože nepoužíváte správný plán.</span><span class="sxs-lookup"><span data-stu-id="55b89-130">Sometimes your flows might behave unexpectedly because you aren't using the correct plan.</span></span>

- <span data-ttu-id="55b89-131">Váš plán zobrazíte tak, že v Microsoft Flow vyberete **Další informace** a potom **Ceny**.</span><span class="sxs-lookup"><span data-stu-id="55b89-131">To view your plan, in Microsoft Flow, select **Learn**, and then select **Pricing**.</span></span>

    ![Ceny](../media/learn-pricing.png)

<span data-ttu-id="55b89-133">Přečtěte si další informace [o cenách a přepínání mezi plány](https://flow.microsoft.com/pricing/).</span><span class="sxs-lookup"><span data-stu-id="55b89-133">Learn more about [pricing and how to switch plans](https://flow.microsoft.com/pricing/).</span></span>

## <a name="issues-with-data-usage"></a><span data-ttu-id="55b89-134">Problémy s čerpáním dat</span><span class="sxs-lookup"><span data-stu-id="55b89-134">Issues with data usage</span></span>

<span data-ttu-id="55b89-135">Je možné, že vyčerpáte data, která můžete použít.</span><span class="sxs-lookup"><span data-stu-id="55b89-135">You might have run out of data that you can use.</span></span>

- <span data-ttu-id="55b89-136">Pokud máte bezplatný nebo zkušební plán, vyberte tlačítko **Nastavení** (symbol ozubeného kola) a podívejte se na vaše aktuální využití dat vzhledem k plánu.</span><span class="sxs-lookup"><span data-stu-id="55b89-136">If you're on a free plan or a trial plan, select the **Settings** button (the gear symbol) to show your current usage against your plan.</span></span>

    ![Tlačítko Nastavení](../media/settings.png)

- <span data-ttu-id="55b89-138">Pokud máte placený plán, na bězích se podílejí všichni uživatelé ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="55b89-138">If you're on a paid plan, runs are pooled across all users in your organization.</span></span> <span data-ttu-id="55b89-139">Pracujeme na funkcích, které zobrazí informace o dostupných kvótách a čerpání dat napříč organizací.</span><span class="sxs-lookup"><span data-stu-id="55b89-139">We're working on features that will show information about available quotas and usage across an organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55b89-140">Pokud datový limit překročíte, Microsoft Flow vám omezí spouštění toků.</span><span class="sxs-lookup"><span data-stu-id="55b89-140">If you exceed your data limit, Microsoft Flow throttles your flow runs.</span></span>

<span data-ttu-id="55b89-141">Přečtěte si další informace [o limitech použití](https://flow.microsoft.com/pricing/).</span><span class="sxs-lookup"><span data-stu-id="55b89-141">Learn more about [usage limits](https://flow.microsoft.com/pricing/).</span></span>

## <a name="you-might-be-running-flows-too-often"></a><span data-ttu-id="55b89-142">Možná spouštíte toky příliš často</span><span class="sxs-lookup"><span data-stu-id="55b89-142">You might be running flows too often</span></span>

<span data-ttu-id="55b89-143">Váš plán určuje, jak často se můžou vaše toky spouštět.</span><span class="sxs-lookup"><span data-stu-id="55b89-143">Your plan determines how often your flows run.</span></span> <span data-ttu-id="55b89-144">Pokud máte například bezplatný plán, můžou se vaše toky spouštět po 15 minutách.</span><span class="sxs-lookup"><span data-stu-id="55b89-144">For example, your flows might run every 15 minutes if you're on the free plan.</span></span> <span data-ttu-id="55b89-145">Pokud se tok aktivuje po kratší době než po 15 minutách od jeho posledního běhu, je tok umístěný ve frontě, dokud neuplyne 15 minut.</span><span class="sxs-lookup"><span data-stu-id="55b89-145">If a flow is triggered less than 15 minutes after its last run, it's queued until 15 minutes have passed.</span></span>

<span data-ttu-id="55b89-146">Kdykoli je tok aktivovaný, ať je to automatickou aktivační událostí nebo ručním spuštěním, počítá se takto akce jako spuštění.</span><span class="sxs-lookup"><span data-stu-id="55b89-146">Whenever a flow is triggered, whether by an automatic trigger or because you manually start it, the action counts as a run.</span></span> <span data-ttu-id="55b89-147">Zjišťování nových dat se jako spuštění nepočítá.</span><span class="sxs-lookup"><span data-stu-id="55b89-147">Checks for new data don't count as runs.</span></span>

<span data-ttu-id="55b89-148">Přečtěte si další informace [o limitech použití](https://flow.microsoft.com/pricing/).</span><span class="sxs-lookup"><span data-stu-id="55b89-148">Learn more about [usage limits](https://flow.microsoft.com/pricing/).</span></span>

## <a name="you-might-be-using-an-incorrect-account"></a><span data-ttu-id="55b89-149">Možná používáte nesprávný účet</span><span class="sxs-lookup"><span data-stu-id="55b89-149">You might be using an incorrect account</span></span>

<span data-ttu-id="55b89-150">Pokud se přihlásíte pomocí účtu Microsoft (například pomocí účtu, který má na konci *@outlook.com* nebo *@gmail.com*), můžete používat jenom bezplatný plán.</span><span class="sxs-lookup"><span data-stu-id="55b89-150">If you sign in by using a Microsoft account (for example, an account that ends with *@outlook.com* or *@gmail.com*), you can use only the free plan.</span></span> <span data-ttu-id="55b89-151">Jestli chcete využívat funkce placeného plánu, přihlaste se pomocí účtu své organizace nebo školní e-mailové adresy.</span><span class="sxs-lookup"><span data-stu-id="55b89-151">To take advantage of the features of the paid plan, sign in by using your organizational account or school email address.</span></span>

<span data-ttu-id="55b89-152">Pokud chcete upgradovat, použijte účet organizace nebo školní účet nebo vytvořte [zkušební účet Microsoft Office 365](https://powerbi.microsoft.com/documentation/powerbi-admin-signing-up-for-power-bi-with-a-new-office-365-trial/).</span><span class="sxs-lookup"><span data-stu-id="55b89-152">To upgrade, use an organizational account or a school account, or create a [Microsoft Office 365 trial account](https://powerbi.microsoft.com/documentation/powerbi-admin-signing-up-for-power-bi-with-a-new-office-365-trial/).</span></span>

## <a name="some-flows-run-more-often-than-expected"></a><span data-ttu-id="55b89-153">Některé toky běží častěji, než očekáváte</span><span class="sxs-lookup"><span data-stu-id="55b89-153">Some flows run more often than expected</span></span>

<span data-ttu-id="55b89-154">Některé toky můžou běžet častěji, než očekáváte.</span><span class="sxs-lookup"><span data-stu-id="55b89-154">Some flows might run more often than you expect.</span></span> <span data-ttu-id="55b89-155">Vytvoříte například tok, který vám pošle nabízené oznámení, kdykoli vám od nadřízeného přijde e-mail.</span><span class="sxs-lookup"><span data-stu-id="55b89-155">For example, you create a flow that sends you a push notification whenever your manager sends you an email.</span></span> <span data-ttu-id="55b89-156">Tento tok se musí spustit při příchodu jakéhokoliv e-mailu, protože musí zkontrolovat, jestli e-mail přišel od vašeho nadřízeného.</span><span class="sxs-lookup"><span data-stu-id="55b89-156">That flow must run every time you get an email from anyone, because the flow must check whether the email came from your manager.</span></span> <span data-ttu-id="55b89-157">Tato akce se počítá jako spuštění.</span><span class="sxs-lookup"><span data-stu-id="55b89-157">This action counts as a run.</span></span>

## <a name="other-issues-that-are-based-on-limits-and-caveats"></a><span data-ttu-id="55b89-158">Další problémy související s limity a omezeními</span><span class="sxs-lookup"><span data-stu-id="55b89-158">Other issues that are based on limits, and caveats</span></span>

<span data-ttu-id="55b89-159">Můžete mít problémy, které souvisejí s dalšími limity:</span><span class="sxs-lookup"><span data-stu-id="55b89-159">You might have issues that are based on other limits:</span></span>

* <span data-ttu-id="55b89-160">Každý účet může mít až:</span><span class="sxs-lookup"><span data-stu-id="55b89-160">Each account can have up to:</span></span>

    * <span data-ttu-id="55b89-161">250 toků</span><span class="sxs-lookup"><span data-stu-id="55b89-161">250 flows.</span></span>
    * <span data-ttu-id="55b89-162">15 vlastních konektorů</span><span class="sxs-lookup"><span data-stu-id="55b89-162">15 custom connectors.</span></span>
    * <span data-ttu-id="55b89-163">20 připojení na každé rozhraní API a 100 připojení celkem</span><span class="sxs-lookup"><span data-stu-id="55b89-163">20 connections per application programming interface (API) and 100 connections total.</span></span>

* <span data-ttu-id="55b89-164">Bránu můžete nainstalovat jenom ve výchozím prostředí.</span><span class="sxs-lookup"><span data-stu-id="55b89-164">You can install a gateway only in the default environment.</span></span>
* <span data-ttu-id="55b89-165">Některé externí konektory, jako třeba Twitter, implementují omezování připojení pro řízení kvality služby.</span><span class="sxs-lookup"><span data-stu-id="55b89-165">Some external connectors, like Twitter, implement connection throttling to control the quality of service.</span></span> <span data-ttu-id="55b89-166">Když je omezování v činnosti, můžou vaše toky selhat.</span><span class="sxs-lookup"><span data-stu-id="55b89-166">Your flows might fail when throttling is in effect.</span></span> <span data-ttu-id="55b89-167">Pokud vaše toky selhávají, zkontrolujte v historii spuštění podrobnosti běhu toku.</span><span class="sxs-lookup"><span data-stu-id="55b89-167">If your flows are failing, review the details of the run that failed in the flow's run history.</span></span>
