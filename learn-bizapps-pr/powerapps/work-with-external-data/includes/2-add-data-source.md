---
ms.openlocfilehash: c4042faa277ca3843214cfc7247161f25dd632ae
ms.sourcegitcommit: e17cc64775307fcf15cef8e0181fdb046ccd227f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58265880"
---
<span data-ttu-id="f9189-101">Začněte tím, že do své aplikace přidáte zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="f9189-101">To begin, add a data source to your app.</span></span> <span data-ttu-id="f9189-102">V PowerApps můžete zdroj dat přidat několika způsoby.</span><span class="sxs-lookup"><span data-stu-id="f9189-102">In PowerApps, there are multiple ways to add a data source.</span></span> <span data-ttu-id="f9189-103">Například při přidávání galerie nebo formuláře na obrazovku můžete pomocí tohoto rozhraní zvolit existující zdroj dat nebo přidat nový.</span><span class="sxs-lookup"><span data-stu-id="f9189-103">For example, when you add a gallery or a form to the screen, you can use that interface to choose an existing data source or add a new one.</span></span> <span data-ttu-id="f9189-104">Někdy musíte přidat zdroj dat, aby ovládací prvek provedl nějakou akci.</span><span class="sxs-lookup"><span data-stu-id="f9189-104">Sometimes you must add a data source for a control to complete an action.</span></span> <span data-ttu-id="f9189-105">Příkladem je přidání zdroje dat k tlačítku, které odešle e-mail.</span><span class="sxs-lookup"><span data-stu-id="f9189-105">For example, adding a data source to a button to send an email.</span></span>

<a name="add-a-tabular-data-source-such-as-a-sharepoint-list"></a><span data-ttu-id="f9189-106">Přidání tabulkového zdroje dat, například sharepointového seznamu</span><span class="sxs-lookup"><span data-stu-id="f9189-106">Add a tabular data source such as a SharePoint list</span></span>
---------------------------------------------------

<span data-ttu-id="f9189-107">Tabulkové zdroje dat přidáte stejně jako v předchozím postupu, případně z vlastností nějakého ovládacího prvku.</span><span class="sxs-lookup"><span data-stu-id="f9189-107">Add tabular data sources by following the same steps as in the previous procedure, or from the properties of a control.</span></span> <span data-ttu-id="f9189-108">V tomto příkladu přidáte do aplikace jako zdroj dat seznam SharePointu Online z ovládacího prvku Galerie.</span><span class="sxs-lookup"><span data-stu-id="f9189-108">In this example, you'll add a SharePoint Online list as a data source to your app from a gallery control.</span></span>

1.  <span data-ttu-id="f9189-109">Na kartě **Vložit** vyberte **Galerie** a pak vyberte možnost svislé galerie.</span><span class="sxs-lookup"><span data-stu-id="f9189-109">On the **Insert** tab, select **Gallery**, and then select the option for a vertical gallery.</span></span>

2.  <span data-ttu-id="f9189-110">V podokně vlastností vyberte rozevírací nabídku vlastnosti **Položky**.</span><span class="sxs-lookup"><span data-stu-id="f9189-110">In the properties pane, select the drop-down menu for the **Items** property.</span></span>

3.  <span data-ttu-id="f9189-111">V seznamu, který se objeví, vyberte **Přidat zdroj dat**.</span><span class="sxs-lookup"><span data-stu-id="f9189-111">In the list that appears, select **Add a data source**.</span></span>

    ![Přidání tabulkového zdroje dat](../media/add-tabular-data-source.png)

4.  <span data-ttu-id="f9189-113">V podokně **Data** vyberte **Nové připojení**.</span><span class="sxs-lookup"><span data-stu-id="f9189-113">In the **Data** pane, select **New connection**.</span></span>

5.  <span data-ttu-id="f9189-114">Procházejte seznam, dokud neuvidíte SharePoint, a pak ho vyberte.</span><span class="sxs-lookup"><span data-stu-id="f9189-114">Scroll through the list until SharePoint appears, and then select it.</span></span>

6.  <span data-ttu-id="f9189-115">V dolní části podokna **Data** klikněte na **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="f9189-115">At the bottom of the **Data** pane, click **Create**.</span></span>

    > <span data-ttu-id="f9189-116">Abyste se mohli připojit k místnímu serveru SharePoint, musíte mít vybranou místní bránu dat.</span><span class="sxs-lookup"><span data-stu-id="f9189-116">In order to connect to an on-premises SharePoint server, you need to have selected the on-premises data gateway.</span></span>

7.  <span data-ttu-id="f9189-117">Při zobrazení výzvy proveďte některý z těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="f9189-117">When prompted, perform either of these steps:</span></span>

    -   <span data-ttu-id="f9189-118">V seznamu **Poslední weby** vyberte některý sharepointový web.</span><span class="sxs-lookup"><span data-stu-id="f9189-118">Select a SharePoint site from the **Recent sites** list.</span></span>

    -   <span data-ttu-id="f9189-119">Zadejte nebo vložte adresu URL webu, vyberte **Přejít** a pak vyberte seznam, který chcete použít.</span><span class="sxs-lookup"><span data-stu-id="f9189-119">Type or paste the site's URL, select **Go**, and then select the list that you want to use.</span></span>

8.  <span data-ttu-id="f9189-120">Vyberte **Připojit**.</span><span class="sxs-lookup"><span data-stu-id="f9189-120">Select **Connect**.</span></span>

<span data-ttu-id="f9189-121">Připojili jste se k sharepointovému seznamu a jeho data můžete zobrazit v ovládacím prvku Galerie.</span><span class="sxs-lookup"><span data-stu-id="f9189-121">You have connected to your SharePoint list, and you can display the data in the gallery control.</span></span>

<a name="add-an-action-data-source-such-as-office-365-outlook"></a><span data-ttu-id="f9189-122">Přidání akčního zdroje dat, například Office 365 Outlooku</span><span class="sxs-lookup"><span data-stu-id="f9189-122">Add an action data source such as Office 365 Outlook</span></span>
----------------------------------------------------

<span data-ttu-id="f9189-123">Tuto metodu můžete použít k přidání libovolného zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="f9189-123">You can use this method to add any data source.</span></span> <span data-ttu-id="f9189-124">Po přidání bude tento zdroj dat dostupný ve vaší aplikaci.</span><span class="sxs-lookup"><span data-stu-id="f9189-124">After it is added, it will be available throughout your app.</span></span>

1.  <span data-ttu-id="f9189-125">V PowerApps Studiu vyberte kartu **Zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="f9189-125">In PowerApps Studio, select the **View** tab.</span></span>

2.  <span data-ttu-id="f9189-126">Na pásu karet vyberte **Zdroje dat**.</span><span class="sxs-lookup"><span data-stu-id="f9189-126">In the ribbon, select **Data sources**.</span></span>

3.  <span data-ttu-id="f9189-127">V podokně **Data** vyberte **Přidat zdroj dat**.</span><span class="sxs-lookup"><span data-stu-id="f9189-127">In the **Data** pane, select **Add data source**.</span></span>

    > ![Přidání zdroje dat](../media/add-data-source.png)

4.  <span data-ttu-id="f9189-129">V podokně **Data** vyberte **Nové připojení**.</span><span class="sxs-lookup"><span data-stu-id="f9189-129">In the **Data** pane, select **New connection**.</span></span>

5.  <span data-ttu-id="f9189-130">Procházejte seznam, dokud neuvidíte Office 365 Outlook, vyberte ho a pak vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="f9189-130">Scroll through the list until Office 365 Outlook appears, select it, and then select **Create**.</span></span>

6.  <span data-ttu-id="f9189-131">Po přidání zdroje dat zavřete podokno **Data** výběrem zavírací ikony (X) nad textem **Přidat zdroj dat**.</span><span class="sxs-lookup"><span data-stu-id="f9189-131">After your data source is added, close the **Data** pane by selecting the close icon (X) above **Add data source**.</span></span>

<span data-ttu-id="f9189-132">Zdroj dat Office 365 Outlook je teď dostupný pro použití ve vaší aplikaci.</span><span class="sxs-lookup"><span data-stu-id="f9189-132">Now the Office 365 Outlook data source is available for use in your app.</span></span>

<span data-ttu-id="f9189-133">Abyste mohli odesílat e-maily, přidejte do aplikace ovládací prvek Tlačítko a jeho vlastnost **OnSelect** nastavte na zvýrazněný vzorec:</span><span class="sxs-lookup"><span data-stu-id="f9189-133">To send an email, add a button control to your app, and set its **OnSelect** property to the highlighted formula:</span></span>

![Vzorec pro Office 365 Outlook](../media/Office365Outlookformula.png)

<span data-ttu-id="f9189-135">Tento vzorec bude fungovat takto.</span><span class="sxs-lookup"><span data-stu-id="f9189-135">This formula will do the following.</span></span>

| <span data-ttu-id="f9189-136">**Argument vzorce**</span><span class="sxs-lookup"><span data-stu-id="f9189-136">**Formula argument**</span></span> | <span data-ttu-id="f9189-137">**Zadání vzorce**</span><span class="sxs-lookup"><span data-stu-id="f9189-137">**Formula input**</span></span>     | <span data-ttu-id="f9189-138">**Poznámky**</span><span class="sxs-lookup"><span data-stu-id="f9189-138">**Notes**</span></span>       |
| :------------------- | :------------------:  |:----------------|
| <span data-ttu-id="f9189-139">Komu</span><span class="sxs-lookup"><span data-stu-id="f9189-139">To</span></span>                   | <span data-ttu-id="f9189-140">User().Email</span><span class="sxs-lookup"><span data-stu-id="f9189-140">User().Email</span></span>          | <span data-ttu-id="f9189-141">Aktuální uživatel je osoba, které se tento e-mail odešle.</span><span class="sxs-lookup"><span data-stu-id="f9189-141">The current user is the person to whom the email will be sent.</span></span> |
| <span data-ttu-id="f9189-142">Předmět</span><span class="sxs-lookup"><span data-stu-id="f9189-142">Subject</span></span>              | <span data-ttu-id="f9189-143">„Předmět e-mailu“</span><span class="sxs-lookup"><span data-stu-id="f9189-143">"Subject of the email"</span></span>|             |
| <span data-ttu-id="f9189-144">Text</span><span class="sxs-lookup"><span data-stu-id="f9189-144">Body</span></span>                 | <span data-ttu-id="f9189-145">„Text e-mailu“</span><span class="sxs-lookup"><span data-stu-id="f9189-145">"Body of the email"</span></span>   |              |

<span data-ttu-id="f9189-146">Toto je důležitý koncept, který byste u zdrojů dat měli pochopit.</span><span class="sxs-lookup"><span data-stu-id="f9189-146">This is an important concept to understand about data sources.</span></span> <span data-ttu-id="f9189-147">Některé zdroje dat, například SQL Server, používají uložené přihlašovací údaje, které jsou sdílené všemi uživateli konektoru.</span><span class="sxs-lookup"><span data-stu-id="f9189-147">Some data sources, such as SQL Server, use stored credentials that are shared by all users of the connector.</span></span> <span data-ttu-id="f9189-148">Jiné, například CDS for Apps, SharePoint a další konektory Office 365, používají přihlašovací údaje uživatele.</span><span class="sxs-lookup"><span data-stu-id="f9189-148">Others, such as CDS for Apps, SharePoint, and other Office 365 connectors, use the user's credentials.</span></span> <span data-ttu-id="f9189-149">Například každý uživatel, který v sharepointovém seznamu používá aplikaci založenou na datech, potřebuje v SharePointu příslušná oprávnění, aby s těmito daty mohl pracovat.</span><span class="sxs-lookup"><span data-stu-id="f9189-149">For example, every user who uses an app based on data in a SharePoint list needs the appropriate permissions in SharePoint to interact with that data.</span></span>

<span data-ttu-id="f9189-150">V příští lekci tohoto modulu se dozvíte další informace o ovládacím prvku Galerie a zobrazování dat.</span><span class="sxs-lookup"><span data-stu-id="f9189-150">In the next unit of this module, you'll learn more about the gallery control and how to display your data.</span></span> 
