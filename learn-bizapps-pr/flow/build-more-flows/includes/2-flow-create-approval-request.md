---
ms.openlocfilehash: b18d1c4f8ad250cd6a1291ef303fee0c9df8108f
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698849"
---
<span data-ttu-id="6b61b-101">V této lekci se naučíte vytvářet obchodní scénář, který používá schválení.</span><span class="sxs-lookup"><span data-stu-id="6b61b-101">In this unit, you'll learn how to build a business-friendly scenario that uses approvals.</span></span>

<span data-ttu-id="6b61b-102">V tomto scénáři může každý, kdo má přístup k seznamu Microsoft SharePointu, přidávat tweety bez jakékoli znalosti Twitteru.</span><span class="sxs-lookup"><span data-stu-id="6b61b-102">In this scenario, anyone who has access to the Microsoft SharePoint list can contribute tweets without knowing anything about Twitter.</span></span> <span data-ttu-id="6b61b-103">Tým pro sociální média pak může tyto tweety schválit nebo odmítnout.</span><span class="sxs-lookup"><span data-stu-id="6b61b-103">The social media team can then approve or reject those tweets.</span></span> <span data-ttu-id="6b61b-104">Tento tým bude mít kontrolu nad účtem a obsahem, který se dostane k zákazníkům.</span><span class="sxs-lookup"><span data-stu-id="6b61b-104">Therefore, that team remains in control of the account and the content that goes out to customers.</span></span>

## <a name="step-one-create-a-sharepoint-list-for-tweets"></a><span data-ttu-id="6b61b-105">1. krok: Vytvoření sharepointového seznamu pro tweety</span><span class="sxs-lookup"><span data-stu-id="6b61b-105">Step one: Create a SharePoint list for tweets</span></span>

<span data-ttu-id="6b61b-106">Použijete šablonu, která spustí schvalovací proces vždy, když se v určitém seznamu vytvoří nová položka.</span><span class="sxs-lookup"><span data-stu-id="6b61b-106">You'll use a template that starts an approval process whenever a new item is created in a specific list.</span></span> <span data-ttu-id="6b61b-107">Pokud je položka schválená, zveřejní se tweet na Twitteru.</span><span class="sxs-lookup"><span data-stu-id="6b61b-107">If the item is approved, a tweet is posted to Twitter.</span></span> <span data-ttu-id="6b61b-108">V této lekci změníte postup tím, že přidáte kroky, které v seznamu SharePointu aktualizují odpověď na schválení, vyznačí schválení nebo neschválení položky a přidají komentáře, které schvalovatel přidal k navrhovanému tweetu.</span><span class="sxs-lookup"><span data-stu-id="6b61b-108">For this unit, you'll change the process by adding steps that update a SharePoint list with the approval response, indicate whether the item was approved, and add any comments that the approver added to the proposed tweet.</span></span>

<span data-ttu-id="6b61b-109">Nejdříve vytvoříme sharepointový seznam.</span><span class="sxs-lookup"><span data-stu-id="6b61b-109">First, let's create the SharePoint list.</span></span>

1. <span data-ttu-id="6b61b-110">Na webu SharePoint vytvořte sharepointový seznam s názvem *ContosoTweets*.</span><span class="sxs-lookup"><span data-stu-id="6b61b-110">On your SharePoint site, create a SharePoint list named *ContosoTweets*.</span></span>
1. <span data-ttu-id="6b61b-111">Otevřete seznam a vyberte **Přidat sloupec**.</span><span class="sxs-lookup"><span data-stu-id="6b61b-111">Open the list, and select **Add column**.</span></span>
1. <span data-ttu-id="6b61b-112">Volbou **+ Přidat sloupec** přidejte následující sloupce.</span><span class="sxs-lookup"><span data-stu-id="6b61b-112">Select **+ Add column** to add the following columns.</span></span> <span data-ttu-id="6b61b-113">Po vytvoření každého sloupce vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="6b61b-113">Select **Save** after you create each column.</span></span>

    - <span data-ttu-id="6b61b-114">Přidejte sloupec typu *Více řádků textu* s názvem *TweetContent*.</span><span class="sxs-lookup"><span data-stu-id="6b61b-114">Add a column of the *Multiple lines of text* type that's named *TweetContent*.</span></span> <span data-ttu-id="6b61b-115">V tomto sloupci bude obsah tweetů, které se budou později schvalovat.</span><span class="sxs-lookup"><span data-stu-id="6b61b-115">This column will hold the content of the tweets that will be approved later.</span></span>
    - <span data-ttu-id="6b61b-116">Přidejte sloupec typu *Datum a čas* s názvem *TweetDate*.</span><span class="sxs-lookup"><span data-stu-id="6b61b-116">Add a column of the *Date and Time* type that's named *TweetDate*.</span></span> <span data-ttu-id="6b61b-117">Pokud chcete vybrat typ *Datum a čas*, vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="6b61b-117">To select the *Date and Time* type, select **More**.</span></span>
    - <span data-ttu-id="6b61b-118">Přidejte sloupec typu *Ano/Ne* a pojmenujte ho *ApprovalStatus*.</span><span class="sxs-lookup"><span data-stu-id="6b61b-118">Add a column of the *Yes/No* type that's named *ApprovalStatus*.</span></span> <span data-ttu-id="6b61b-119">Schvalovatel pak výběrem možnosti **Ano** nebo **Ne** tweet schválí nebo zamítne.</span><span class="sxs-lookup"><span data-stu-id="6b61b-119">The approver can then select **Yes** or **No** to approve or reject the tweet.</span></span>
    - <span data-ttu-id="6b61b-120">Přidejte sloupec typu *Jeden řádek textu* a pojmenujte ho *ApproverComments*.</span><span class="sxs-lookup"><span data-stu-id="6b61b-120">Add a column of the *Single line of text* type that's named *ApproverComments*.</span></span> <span data-ttu-id="6b61b-121">Schvalovatel pak může přidat komentář o stavu schvalování.</span><span class="sxs-lookup"><span data-stu-id="6b61b-121">The approver can then add a comment about the approval status.</span></span>

    ![Přidání sloupců](../media/new-columns.png)

1. <span data-ttu-id="6b61b-123">Zkopírujte adresu URL sharepointového seznamu.</span><span class="sxs-lookup"><span data-stu-id="6b61b-123">Copy the URL of the SharePoint list.</span></span> <span data-ttu-id="6b61b-124">Použijete ho při vytváření toku.</span><span class="sxs-lookup"><span data-stu-id="6b61b-124">You'll use it when you create the flow.</span></span>

## <a name="step-two-create-an-approval-request-flow"></a><span data-ttu-id="6b61b-125">2. krok: Vytvoření toku žádosti o schválení</span><span class="sxs-lookup"><span data-stu-id="6b61b-125">Step two: Create an approval request flow</span></span>

1. <span data-ttu-id="6b61b-126">Přihlaste se k [Microsoft Flow](https://ms.flow.microsoft.com) a pak vyberte **Schválení**.</span><span class="sxs-lookup"><span data-stu-id="6b61b-126">Sign in to [Microsoft Flow](https://ms.flow.microsoft.com), and then select **Approvals**.</span></span>
1. <span data-ttu-id="6b61b-127">Vyberte **Vytvořit tok schválení**, posuňte se dolů a vyberte šablonu **Po schválení publikovat položky seznamu na Twitter**.</span><span class="sxs-lookup"><span data-stu-id="6b61b-127">Select **Create approval flow**, and then scroll down and select the **Post list items to Twitter after approval** template.</span></span>

    ![Vytvoření tlačítka pro schválení toku](../media/create-approval.png)

1. <span data-ttu-id="6b61b-129">Ujistěte se, že přihlašovací údaje účtů pro **SharePoint**, **Schválení** a **Twitter** jsou správné, a pak vyberte **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="6b61b-129">Make sure that your account credentials for **SharePoint**, **Approvals**, and **Twitter** are correct, and then select **Continue**.</span></span>

    ![Kontrola přihlašovacích údajů](../media/verify-credentials.png)

1. <span data-ttu-id="6b61b-131">Vraťte se do Microsoft Flow a v akci **Když je vytvořena nová položka** zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="6b61b-131">Back in Microsoft Flow, in the **When a new item is created** action, enter the following values:</span></span>

    * <span data-ttu-id="6b61b-132">**Site Address** (Adresa webu): Zadejte adresu URL sharepointového webu vašeho týmu.</span><span class="sxs-lookup"><span data-stu-id="6b61b-132">**Site Address**: Enter the URL of your team's SharePoint site.</span></span>
    * <span data-ttu-id="6b61b-133">**List Name** (Název seznamu): Vyberte *ContosoTweets*.</span><span class="sxs-lookup"><span data-stu-id="6b61b-133">**List Name**: Select *ContosoTweets*.</span></span>

    ![Pole Adresa webu a Název seznamu](../media/site-address.png)

1. <span data-ttu-id="6b61b-135">V akci **Zahájit schválení** vyberte **Upravit**, aby se zobrazila všechna pole.</span><span class="sxs-lookup"><span data-stu-id="6b61b-135">In the **Start an approval** action, select **Edit** to show all the fields.</span></span>

    ![Tlačítko Upravit](../media/edit-all-fields.png)

1. <span data-ttu-id="6b61b-137">Do pole **Název** zadejte *Nový tweet pro* a ze seznamu dynamického obsahu vyberte **Title** (Název).</span><span class="sxs-lookup"><span data-stu-id="6b61b-137">In the **Title** field, enter *New tweet for*, and then select **Title** in the dynamic content list.</span></span>

    ![Dynamický obsah s názvem](../media/tweet-title.png)

1. <span data-ttu-id="6b61b-139">V poli **Přiřazeno** zadejte a vyberte své jméno nebo jméno testovacího uživatele.</span><span class="sxs-lookup"><span data-stu-id="6b61b-139">In the **Assigned to** field, enter and select either your name or the name of a test user.</span></span>

    ![Pole Přiřazeno](../media/tweet-assigned-to.png)

1. <span data-ttu-id="6b61b-141">Z pole **Podrobnosti** odeberte výchozí položky a ze seznamu dynamického obsahu přidejte **TweetContent** (Obsah tweetu), **TweetDate** (Datum tweetu) a **Created by DisplayName** (Zobrazované jméno autora).</span><span class="sxs-lookup"><span data-stu-id="6b61b-141">In the **Details** field, remove the default items, and add **TweetContent**, **TweetDate**, and **Created by DisplayName** from the dynamic content list.</span></span> <span data-ttu-id="6b61b-142">Přidejte slova *z* a *od uživatele*, aby byl obsah čitelnější (viz níže).</span><span class="sxs-lookup"><span data-stu-id="6b61b-142">Add the words *on* and *by* to make the content more readable, as shown here.</span></span>

    ![Pole Podrobnosti](../media/tweet-details.png)

1. <span data-ttu-id="6b61b-144">Do pole **Odkaz na položku** vložte adresu URL sharepointového seznamu, kterou jste si zkopírovali v předchozím postupu.</span><span class="sxs-lookup"><span data-stu-id="6b61b-144">In the **Item Link** field, paste the URL of your SharePoint list, which you copied in the previous procedure.</span></span> <span data-ttu-id="6b61b-145">Do pole **Popis odkazu na položku** zadejte *Seznam tweetů Contoso*.</span><span class="sxs-lookup"><span data-stu-id="6b61b-145">In the **Item Link Description** field, enter *Contoso Tweet List*.</span></span>

    ![Pole Odkaz na položku a Popis odkazu na položku](../media/tweet-item-link.png)

1. <span data-ttu-id="6b61b-147">V akci **Podmínka** najeďte kurzorem na pole **POKUD ANO**, vyberte znaménko plus (**+**) a vyberte **Přidat akci**.</span><span class="sxs-lookup"><span data-stu-id="6b61b-147">In the **Condition** action, hover over the **IF YES** box, select the plus sign (**+**), and then select **Add an action**.</span></span>

    ![Přidání akce](../media/add-an-action.png)

1. <span data-ttu-id="6b61b-149">Vyhledejte *aktualizovat položku*, vyberte konektor **SharePoint** a vyberte akci **SharePoint – Aktualizovat položku**.</span><span class="sxs-lookup"><span data-stu-id="6b61b-149">Search for *update item*, select the **SharePoint** connector, and then select the **SharePoint – Update item** action.</span></span>

    ![SharePoint – Aktualizovat položku](../media/update-item.png)

1. <span data-ttu-id="6b61b-151">Do pole **Adresa webu** znovu zadejte adresu URL sharepointového týmového webu.</span><span class="sxs-lookup"><span data-stu-id="6b61b-151">In the **Site Address**, enter the URL of the team's SharePoint site again.</span></span> <span data-ttu-id="6b61b-152">V poli **Název seznamu** znovu vyberte *ContosoTweets*.</span><span class="sxs-lookup"><span data-stu-id="6b61b-152">In the **List Name** field, select *ContosoTweets* again.</span></span> <span data-ttu-id="6b61b-153">Do pole **Id** přidejte **ID** ze seznamu dynamického obsahu.</span><span class="sxs-lookup"><span data-stu-id="6b61b-153">In the **Id** field, add **ID** from the dynamic content list.</span></span> <span data-ttu-id="6b61b-154">Pole **Id** se používá ke spojení se skutečným požadavkem na tweet v seznamu SharePointu.</span><span class="sxs-lookup"><span data-stu-id="6b61b-154">The **Id** field is used to match the actual tweet request in the SharePoint list.</span></span>

    ![Pole Adresa webu, Název seznamu a Id](../media/address-list-id.png)

1. <span data-ttu-id="6b61b-156">Vyberte pole **Název** a v seznamu dynamického obsahu vyhledejte *Title* (Název).</span><span class="sxs-lookup"><span data-stu-id="6b61b-156">Select the **Title** field, and then, in the dynamic content list, search for *title*.</span></span> <span data-ttu-id="6b61b-157">Z akce **Když je vytvořena nová položka** přidejte **Title** (Název).</span><span class="sxs-lookup"><span data-stu-id="6b61b-157">Add **Title** from the **When a new item is created** action.</span></span>

    ![Pole Název](../media/add-title.png)

1. <span data-ttu-id="6b61b-159">V poli **ApprovalStatus** (StavSchválení) vyberte *Ano*.</span><span class="sxs-lookup"><span data-stu-id="6b61b-159">In the **ApprovalStatus** field, select *Yes*.</span></span> <span data-ttu-id="6b61b-160">Pak vyberte **ApproverComments** (KomentářSchvalovatele) a ze seznamu dynamického obsahu přidejte **Comments** (Komentáře).</span><span class="sxs-lookup"><span data-stu-id="6b61b-160">Then select the **ApproverComments** field, and add **Comments** from the dynamic content list.</span></span>

    ![Pole ApprovalStatus a ApproverComments](../media/approver-status.png)

1. <span data-ttu-id="6b61b-162">Na konci pole **POKUD NE, NEDĚLAT NIC** vyberte **Přidat akci**.</span><span class="sxs-lookup"><span data-stu-id="6b61b-162">Near the bottom of the **IF NO, DO NOTHING** box, select **Add an action**.</span></span>

    ![Přidání akce](../media/add-a-no-action.png)

1. <span data-ttu-id="6b61b-164">Opakujte kroky 11 až 14, abyste vytvořili akci **SharePoint – Aktualizovat položku**.</span><span class="sxs-lookup"><span data-stu-id="6b61b-164">Repeat steps 11 through 14 to create a **SharePoint – Update item** action.</span></span> <span data-ttu-id="6b61b-165">Nastavte stejné hodnoty, jako jste nastavili u podmínky **POKUD ANO**.</span><span class="sxs-lookup"><span data-stu-id="6b61b-165">Set the same values that you set for the **IF YES** condition.</span></span> <span data-ttu-id="6b61b-166">Jediný rozdíl bude, že tentokrát nastavíte pole **ApprovalStatus** (StavSchválení) na *Ne*.</span><span class="sxs-lookup"><span data-stu-id="6b61b-166">The only difference is that you set the **ApprovalStatus** field to *No* this time.</span></span>

    ![ApprovalStatus = Ne](../media/status-no.png)

1. <span data-ttu-id="6b61b-168">Vyberte akci **Publikovat tweet** a vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="6b61b-168">Select the **Post a tweet** action, and select **Edit**.</span></span> <span data-ttu-id="6b61b-169">Vyberte pole **Text Tweetu** a ze seznamu dynamického obsahu vyberte **TweetContent** (ObsahTweetu).</span><span class="sxs-lookup"><span data-stu-id="6b61b-169">Then select the **Tweet text** field, and add **TweetContent** from the dynamic content list.</span></span> <span data-ttu-id="6b61b-170">Tímto krokem vytvoříte skutečný tweet, který se po schválení zveřejní na Twitteru.</span><span class="sxs-lookup"><span data-stu-id="6b61b-170">This step will create the actual tweet and then post it to Twitter when it's approved.</span></span>

    ![Publikování tweetu](../media/post-tweet.png)

1. <span data-ttu-id="6b61b-172">Vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="6b61b-172">Select **Save**.</span></span>

<span data-ttu-id="6b61b-173">Blahopřejeme!</span><span class="sxs-lookup"><span data-stu-id="6b61b-173">Congratulations!</span></span> <span data-ttu-id="6b61b-174">Právě jste vytvořili první tok.</span><span class="sxs-lookup"><span data-stu-id="6b61b-174">You just created your first flow.</span></span>

<span data-ttu-id="6b61b-175">V této lekci jsme si ukázali jen jeden způsob, jak může Microsoft Flow pomoci vašemu týmu zvýšit produktivitu.</span><span class="sxs-lookup"><span data-stu-id="6b61b-175">This unit showed just one way that Microsoft Flow can empower your team to be more productive.</span></span> <span data-ttu-id="6b61b-176">Tým může přispívat svými nápady, relevantními novinkami nebo pokyny k produktům, ale vy máte kontrolu nad zveřejňovanými tweety pro zákazníky.</span><span class="sxs-lookup"><span data-stu-id="6b61b-176">Your team can contribute ideas, relevant news, or product guidance, but you maintain control over what's tweeted out to customers.</span></span>

<span data-ttu-id="6b61b-177">V další lekci uvidíte, jak to funguje, když schvalovatel dostane novou žádost s návrhem tweetu.</span><span class="sxs-lookup"><span data-stu-id="6b61b-177">In the next unit, you'll see what it looks like when an approver receives a new request for a proposed tweet.</span></span>
