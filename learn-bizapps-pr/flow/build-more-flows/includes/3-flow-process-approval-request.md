---
ms.openlocfilehash: d9046f914ebe826adb8610e63b47e5cefb164167
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698849"
---
<span data-ttu-id="ad9f9-101">V předchozí lekci jste se naučili, jak vytvořit schvalovací proces pro tweety, které jsou uložené v seznamu Microsoft SharePointu.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-101">In the previous unit, you learned how to build an approval process for tweets that are stored in a Microsoft SharePoint list.</span></span> <span data-ttu-id="ad9f9-102">V této lekci zjistíte, jak to vypadá, když schvalovatel dostane novou žádost o schválení.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-102">In this unit, you'll see what the experience looks like when an approver receives a new approval request.</span></span> 

## <a name="step-one-change-the-sharepoint-list"></a><span data-ttu-id="ad9f9-103">1. krok: Změna sharepointového seznamu</span><span class="sxs-lookup"><span data-stu-id="ad9f9-103">Step one: Change the SharePoint list</span></span>

<span data-ttu-id="ad9f9-104">Nejdřív potřebujeme do sharepointového seznamu přidat položku.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-104">First, we need to add an item to our SharePoint list.</span></span> <span data-ttu-id="ad9f9-105">Pak můžeme zpracovat žádost o schválení této položky.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-105">We can then process an approval request for that item.</span></span>

1. <span data-ttu-id="ad9f9-106">V SharePointu otevřete seznam **ContosoTweets** (TweetyContoso), který jste nastavili v předchozí lekci, a pak vyberte **Nový**, abyste vytvořili novou položku seznamu (tweet).</span><span class="sxs-lookup"><span data-stu-id="ad9f9-106">In SharePoint, open the **ContosoTweets** list that you set up in the previous unit, and then select **New** to create a list item (tweet).</span></span>

    ![Vytvoření tweetu v seznamu SharePointu](../media/sharepoint-list-home.png)

2. <span data-ttu-id="ad9f9-108">Zadejte následující hodnoty a vyberte **Uložit**:</span><span class="sxs-lookup"><span data-stu-id="ad9f9-108">Enter the following values, and then select **Save**:</span></span>

    - <span data-ttu-id="ad9f9-109">**Název**: Zadejte *Propagace*.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-109">**Title**: Enter *Promotions*.</span></span>
    - <span data-ttu-id="ad9f9-110">**TweetContent** (ObsahTweetu): Zadejte *Podívejte se na novou řadu podlah Contoso #ohsocontoso*.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-110">**TweetContent**: Enter *Check out the new line of Contoso Flooring #ohsocontoso*.</span></span> <span data-ttu-id="ad9f9-111">Všimněte si, že tweet začíná hashtagem (znak #).</span><span class="sxs-lookup"><span data-stu-id="ad9f9-111">Notice that the tweet starts with a hashtag (number sign).</span></span>
    - <span data-ttu-id="ad9f9-112">**Datum tweetu**: Zadejte dnešní datum.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-112">**Tweet Date**: Enter today's date.</span></span>

    ![Nová položka SharePointu](../media/sharepoint-new-tweet.png)

## <a name="step-two-change-the-flow"></a><span data-ttu-id="ad9f9-114">2. krok: Změna toku</span><span class="sxs-lookup"><span data-stu-id="ad9f9-114">Step two: Change the flow</span></span>

1. <span data-ttu-id="ad9f9-115">V Microsoft Flow vyberte **Moje toky**.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-115">In Microsoft Flow, select **My flows**.</span></span>
2. <span data-ttu-id="ad9f9-116">Vyberte tok **Po schválení publikovat položky seznamu na Twitter**, který jste nastavili v předchozí lekci, a pak v části **Historie spuštění** vyberte spuštěný tok.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-116">Select the **Post list items to Twitter after approval** flow that you set up in the previous unit, and then, under **Run history**, select the flow that's running.</span></span>

    ![Historie spuštění](../media/run-history.png)

3. <span data-ttu-id="ad9f9-118">Vyberte trigger **Když je vytvořena nová položka**.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-118">Select the **When a new item is created** trigger.</span></span> <span data-ttu-id="ad9f9-119">Ujistěte se, že se zobrazují informace o právě vytvořené položce seznamu.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-119">Make sure that the information for the list item that you just created is shown.</span></span>

    ![Trigger toku](../media/approval-flow.png)

4. <span data-ttu-id="ad9f9-121">V Microsoft Outlooku otevřete e-mail automatického schválení v doručené poště a pak vyberte **Schválit**.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-121">In Microsoft Outlook, open the automated approval mail in the inbox, and then select **Approve**.</span></span>

    ![Žádost v Outlooku](../media/outlook-mail.png)

5. <span data-ttu-id="ad9f9-123">Ve schvalovacím centru zobrazte podrobnosti žádosti, přidejte komentář a pak vyberte **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-123">In the Approval Center, view the details of the request, add a comment, and then select **Confirm**.</span></span>

    ![Schvalovací centrum](../media/approval-center.png)

6. <span data-ttu-id="ad9f9-125">V SharePointu aktualizujte seznam **ContosoTweets**.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-125">In SharePoint, refresh the **ContosoTweets** list.</span></span> <span data-ttu-id="ad9f9-126">Ujistěte se, že pole **ApprovalStatus** (StavSchválení) je nastavené na *Ano* a že se zobrazuje komentář, který jste právě zadali.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-126">Make sure that the **ApprovalStatus** field is set to *Yes*, and that the comment that you just entered is shown.</span></span>

    ![Aktualizovaný seznam SharePointu](../media/sharepoint-list-approved.png)

<span data-ttu-id="ad9f9-128">V této lekci jste viděli postup z pohledu schvalovatele od přijetí e-mailu s žádostí o schválení až po zpracování žádosti ve Schvalovacím centru.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-128">In this unit, you saw the experience from the approver's point of view, from receiving an approval request email to processing the request in the Approval Center.</span></span>
