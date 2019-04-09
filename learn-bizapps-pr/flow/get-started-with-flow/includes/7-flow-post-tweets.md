---
ms.openlocfilehash: 6c1607b239ec3a2f0d33a7a3f82e9ab289d48e18
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698342"
---
<span data-ttu-id="e517a-101">Můžete vytvořit tok, který po svém spuštění nějakou událostí automaticky provede jednu nebo více akcí.</span><span class="sxs-lookup"><span data-stu-id="e517a-101">You can create a flow that automatically performs one or more actions after it's triggered by an event.</span></span> <span data-ttu-id="e517a-102">Tok vám například může e-mailem oznámit, že někdo publikoval tweet obsahující určité klíčové slovo.</span><span class="sxs-lookup"><span data-stu-id="e517a-102">For example, the flow can notify you by email when someone posts a tweet that includes a keyword that you specify.</span></span> <span data-ttu-id="e517a-103">Publikování tweetu je událost (označovaná také jako *aktivační událost*) a odeslání e-mailového oznámení je akce.</span><span class="sxs-lookup"><span data-stu-id="e517a-103">In this example, posting a tweet is the event (also known as a *trigger*), and sending an email notification is the action.</span></span> <span data-ttu-id="e517a-104">V této lekci se dozvíte, jak takový příklad toku vytvořit.</span><span class="sxs-lookup"><span data-stu-id="e517a-104">In this unit, which you'll learn how to create this example flow.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e517a-105">Požadavky</span><span class="sxs-lookup"><span data-stu-id="e517a-105">Prerequisites</span></span>

* <span data-ttu-id="e517a-106">Účet na [flow.microsoft.com](https://flow.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="e517a-106">An account on [flow.microsoft.com](https://flow.microsoft.com)</span></span>
* <span data-ttu-id="e517a-107">Účet na Twitteru</span><span class="sxs-lookup"><span data-stu-id="e517a-107">A Twitter account</span></span>
* <span data-ttu-id="e517a-108">Microsoft Office 365</span><span class="sxs-lookup"><span data-stu-id="e517a-108">Microsoft Office 365</span></span>

## <a name="specify-an-event-to-start-the-flow"></a><span data-ttu-id="e517a-109">Zadání události pro spuštění toku</span><span class="sxs-lookup"><span data-stu-id="e517a-109">Specify an event to start the flow</span></span>

<span data-ttu-id="e517a-110">Nejdřív musíte vybrat aktivační událost, která bude tok spouštět.</span><span class="sxs-lookup"><span data-stu-id="e517a-110">First, you must select the trigger (event) that starts the flow.</span></span>

1. <span data-ttu-id="e517a-111">Přihlaste se k [Microsoft Flow](https://flow.microsoft.com) pomocí účtu své organizace.</span><span class="sxs-lookup"><span data-stu-id="e517a-111">Sign in to [Microsoft Flow](https://flow.microsoft.com) by using your organizational account.</span></span>
1. <span data-ttu-id="e517a-112">Vyberte **Moje toky**.</span><span class="sxs-lookup"><span data-stu-id="e517a-112">Select **My flows**.</span></span>
1. <span data-ttu-id="e517a-113">Vyberte **Nový** a pak vyberte **Vytvořit z prázdné**.</span><span class="sxs-lookup"><span data-stu-id="e517a-113">Select **New**, and then select **Create from blank**.</span></span>

    ![Vytvořit z prázdné](../media/flow-create-blank.png)

1. <span data-ttu-id="e517a-115">Vyberte **Prohledejte stovky konektorů a aktivačních událostí**.</span><span class="sxs-lookup"><span data-stu-id="e517a-115">Select **Search hundreds of connectors and triggers**.</span></span>
1. <span data-ttu-id="e517a-116">Do vyhledávacího pole zadejte *twitter*, vyberte konektor **Twitter** a pak vyberte aktivační událost **Twitter – Když se publikuje nový tweet**.</span><span class="sxs-lookup"><span data-stu-id="e517a-116">In the search field, enter *twitter*, select the **Twitter** connector, and then select the **Twitter - When a new tweet is posted** trigger.</span></span>

    ![Aktivační událost Twitter – Když se publikuje nový tweet](../media/twitter-search.png)

1. <span data-ttu-id="e517a-118">Pokud jste zatím nepřipojili svůj účet na Twitteru k Microsoft Flow, vyberte **Přihlásit se k Twitteru** a zadejte svoje přihlašovací údaje.</span><span class="sxs-lookup"><span data-stu-id="e517a-118">If you haven't already connected your Twitter account to Microsoft Flow, select **Sign in to Twitter**, and then enter your credentials.</span></span>
1. <span data-ttu-id="e517a-119">Do pole **Hledaný text** zadejte klíčové slovo, které se má hledat.</span><span class="sxs-lookup"><span data-stu-id="e517a-119">In the **Search text** box, enter the keyword to find.</span></span>

    ![Zadejte klíčové slovo Twitteru](../media/twitter-keyword.png)

## <a name="specify-an-action"></a><span data-ttu-id="e517a-121">Zadání akce</span><span class="sxs-lookup"><span data-stu-id="e517a-121">Specify an action</span></span>

1. <span data-ttu-id="e517a-122">Vyberte **Nový krok** a pak vyberte **Přidat akci**.</span><span class="sxs-lookup"><span data-stu-id="e517a-122">Select **New step**, and then select **Add an action**.</span></span>

    ![Přidání akce](../media/add-action-icon.png)

1. <span data-ttu-id="e517a-124">Do vyhledávacího pole zadejte *odeslání e-mailu* a pak vyberte akci **Office 365 Outlook – Odeslání e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="e517a-124">In the search field, enter *send email*, and then select the **Office 365 Outlook - Send an email** action.</span></span>

    ![Akce Office 365 Outlook – Odeslání e-mailu](../media/send-email.png)

1. <span data-ttu-id="e517a-126">Pokud se zobrazí výzva k přihlášení, klikněte na tlačítko pro přihlášení a zadejte svoje přihlašovací údaje.</span><span class="sxs-lookup"><span data-stu-id="e517a-126">If you're prompted to sign in, select the sign-in button, and then enter your credentials.</span></span>
1. <span data-ttu-id="e517a-127">Do pole **Komu** zadejte nebo vložte svoji e-mailovou adresu a pak v seznamu kontaktů vyberte svoje jméno.</span><span class="sxs-lookup"><span data-stu-id="e517a-127">In the **To** field, enter or paste your email address, and then select your name in the list of contacts that appears.</span></span>

    ![Pole Komu](../media/blank-email.png)

1. <span data-ttu-id="e517a-129">Do pole **Předmět** zadejte text **Nový tweet od:** a přidejte mezeru.</span><span class="sxs-lookup"><span data-stu-id="e517a-129">In the **Subject** field, enter **New tweet from:** followed by a space.</span></span>

    ![Pole Předmět](../media/message-token.png)

1. <span data-ttu-id="e517a-131">V seznamu dynamického obsahu vyberte token **Autor tweetu** a přidejte tak jeho zástupný symbol.</span><span class="sxs-lookup"><span data-stu-id="e517a-131">In the list of dynamic content, select the **Tweeted by** token to add a placeholder for it.</span></span>

    ![Token Autor tweetu](../media/add-parameter.png)

1. <span data-ttu-id="e517a-133">Vyberte pole **Text**. Potom v seznamu dynamického obsahu vyberte token **TextTweetu** a přidejte tak jeho zástupný symbol.</span><span class="sxs-lookup"><span data-stu-id="e517a-133">Select the **Body** field, and then, in the list of dynamic content, select the **Tweet text** token to add a placeholder for it.</span></span>
1. <span data-ttu-id="e517a-134">Volitelné: Přidejte do textu e-mailu další tokeny, další obsah nebo obojí.</span><span class="sxs-lookup"><span data-stu-id="e517a-134">Optional: Add more tokens, other content, or both to the body of the email.</span></span>
1. <span data-ttu-id="e517a-135">Uložte tok výběrem možnosti **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e517a-135">Select **Save** to save the flow.</span></span>
1. <span data-ttu-id="e517a-136">Publikujte tweet obsahující zadané klíčové slovo nebo počkejte, až takový tweet publikuje někdo jiný.</span><span class="sxs-lookup"><span data-stu-id="e517a-136">Post a tweet that includes the keyword that you specified, or wait for someone else to post such a tweet.</span></span>

    <span data-ttu-id="e517a-137">Chvilku po publikování tweetu vám e-mailová zpráva oznámí nový tweet.</span><span class="sxs-lookup"><span data-stu-id="e517a-137">Within a minute after the tweet is posted, an email message will notify you of the new tweet.</span></span>
