---
ms.openlocfilehash: 6e9bc6fd2c799d1b1d72bd64771b3b363ed9ec2f
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698342"
---
<span data-ttu-id="1e67f-101">V této lekci se blíže seznámíte se službou Microsoft Flow a vytvoříte první tok.</span><span class="sxs-lookup"><span data-stu-id="1e67f-101">In this unit, you'll see more of Microsoft Flow as you build your first flow.</span></span>

<span data-ttu-id="1e67f-102">Hledání příloh prostřednictvím e-mailů může být časově náročné.</span><span class="sxs-lookup"><span data-stu-id="1e67f-102">It can be time consuming to search for attachments through email.</span></span> <span data-ttu-id="1e67f-103">Tok, který vytvoříte, šetří čas tím, že všechny e-mailové přílohy ukládá do složky v účtu Microsoft OneDrivu pro firmy.</span><span class="sxs-lookup"><span data-stu-id="1e67f-103">The flow that you'll build saves time by storing all your email attachments in a folder on your Microsoft OneDrive for Business account.</span></span>

## <a name="choose-a-template"></a><span data-ttu-id="1e67f-104">Volba šablony</span><span class="sxs-lookup"><span data-stu-id="1e67f-104">Choose a template</span></span>
<span data-ttu-id="1e67f-105">K dispozici je řada šablon, které zrychlí přípravu toku.</span><span class="sxs-lookup"><span data-stu-id="1e67f-105">Our many templates will get your flows flowing quickly.</span></span> <span data-ttu-id="1e67f-106">Pomohou vám účinněji propojit služby, které už používáte.</span><span class="sxs-lookup"><span data-stu-id="1e67f-106">They'll help you connect the services you're already using in more meaningful ways.</span></span>

<span data-ttu-id="1e67f-107">Přihlaste se ke službě [Microsoft Flow](https://ms.flow.microsoft.com) a vyberte nabídku **Šablony**.</span><span class="sxs-lookup"><span data-stu-id="1e67f-107">Sign in to [Microsoft Flow](https://ms.flow.microsoft.com), and select the **Templates** menu.</span></span> <span data-ttu-id="1e67f-108">Do služby Microsoft Flow se můžete zaregistrovat pomocí účtu Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1e67f-108">You can sign up for Microsoft Flow with a Microsoft account.</span></span>

<span data-ttu-id="1e67f-109">Vyberte šablonu **Uložení příloh e-mailů Office 365 do OneDrivu pro firmy**.</span><span class="sxs-lookup"><span data-stu-id="1e67f-109">Select the **Save Office 365 email attachments to OneDrive for Business** template.</span></span>

![E-mail v Office 365](../media/office-365-email.png)

## <a name="create-the-flow"></a><span data-ttu-id="1e67f-111">Vytvoření toku</span><span class="sxs-lookup"><span data-stu-id="1e67f-111">Create the flow</span></span>
<span data-ttu-id="1e67f-112">**Uložení příloh e-mailů Office 365 do OneDrivu pro firmy** je jedna z našich šablon, které nasadíte jedním kliknutím. Můžete s ní odpovědět na otázky, které jsou potřeba k vytvoření toku, takže nemusíte napsat ani jeden řádek kódu.</span><span class="sxs-lookup"><span data-stu-id="1e67f-112">**Save Office 365 email attachments to OneDrive for Business** is one of our one-click templates, in which you can answer questions that are necessary to build the flow, so that you don't have to write a line of code.</span></span>

<span data-ttu-id="1e67f-113">Na obrázku šablony je popis, k čemu šablona slouží a co je potřeba, aby se dala úspěšně použít.</span><span class="sxs-lookup"><span data-stu-id="1e67f-113">On the template graphic, there's a description of what the template does and what it needs to succeed.</span></span>

<span data-ttu-id="1e67f-114">Zobrazí se výzva k zadání přihlašovacích údajů ke službám Microsoft Office 365 Outlook a Microsoft OneDrive pro firmy.</span><span class="sxs-lookup"><span data-stu-id="1e67f-114">You'll be asked to provide credentials for the Microsoft Office 365 Outlook and Microsoft OneDrive for Business services.</span></span> <span data-ttu-id="1e67f-115">Pokud obě služby používáte pravidelně, už jste k nim přihlášení.</span><span class="sxs-lookup"><span data-stu-id="1e67f-115">If you regularly use both services, you'll already be signed in.</span></span>

1. <span data-ttu-id="1e67f-116">Vyberte **Vytvořit tok**.</span><span class="sxs-lookup"><span data-stu-id="1e67f-116">Select **Create Flow**.</span></span>

    ![Uložení e-mailu v Office 365](../media/save-flow-office-description.png)

1. <span data-ttu-id="1e67f-118">Na další stránce vám Microsoft Flow vytvoří tok.</span><span class="sxs-lookup"><span data-stu-id="1e67f-118">On the next page, Microsoft Flow creates the flow for you.</span></span> 
    - <span data-ttu-id="1e67f-119">Připojí se k vašemu pracovnímu e-mailu, aby mohl stáhnout všechny přílohy.</span><span class="sxs-lookup"><span data-stu-id="1e67f-119">It'll connect  to your work email to get any attachments.</span></span> 
    - <span data-ttu-id="1e67f-120">Potom ve vašem účtu OneDrivu pro firmy vytvoří složku, do které začne automaticky ukládat všechny přílohy poslané na vaši pracovní e-mailovou adresu.</span><span class="sxs-lookup"><span data-stu-id="1e67f-120">It will then create a folder on your OneDrive for Business account to automatically put every attachment that's sent to your work email address in that folder.</span></span>

    ![Úspěšné vytvoření](../media/create-successful.png)

2. <span data-ttu-id="1e67f-122">Vyberte nabídku **Moje toky**.</span><span class="sxs-lookup"><span data-stu-id="1e67f-122">Select the **My flows** menu.</span></span>

    ![Otevření nabídky Moje toky](../media/click-my-flows.png)

3. <span data-ttu-id="1e67f-124">Vyberte tok, který jste vytvořili, a podívejte se, jak funguje.</span><span class="sxs-lookup"><span data-stu-id="1e67f-124">Select the flow you just created to see how it works.</span></span>

    ![Výběr toku](../media/click-the-flow.png)

4. <span data-ttu-id="1e67f-126">Pošlete e-mail s přílohou nebo nechte jiného uživatele, aby poslal e-mail s přílohou.</span><span class="sxs-lookup"><span data-stu-id="1e67f-126">Send an email with an attachment, or have another user send an email with an attachment.</span></span> <span data-ttu-id="1e67f-127">Měli byste pak vidět zelené zaškrtnutí, které signalizuje úspěšný tok.</span><span class="sxs-lookup"><span data-stu-id="1e67f-127">You then should see a green check mark, which indicates that the flow succeeded.</span></span> 
5. <span data-ttu-id="1e67f-128">Pokud se chcete podívat na definici toku, vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="1e67f-128">Select **Edit** to see how the flow is defined.</span></span>

    ![Akce u nového e-mailu](../media/trigger-or-action.png) 
 
6. <span data-ttu-id="1e67f-130">Pokud se chcete podívat na historii a výsledky spuštění, vyberte **Úspěšné**.</span><span class="sxs-lookup"><span data-stu-id="1e67f-130">Select **Succeeded** to see the run history and the results.</span></span>

    ![Úspěšný tok](../media/flow-successful.png)

    <span data-ttu-id="1e67f-132">V uvedeném případě byly všechny části toku úspěšné.</span><span class="sxs-lookup"><span data-stu-id="1e67f-132">In this case, all parts of the flow were successful.</span></span> 

    ![Historie spuštění](../media/run-history.png)

## <a name="important-concepts-in-microsoft-flow"></a><span data-ttu-id="1e67f-134">Důležité informace o Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="1e67f-134">Important concepts in Microsoft Flow</span></span>
<span data-ttu-id="1e67f-135">Při vytváření toků mějte na paměti tyto skutečnosti:</span><span class="sxs-lookup"><span data-stu-id="1e67f-135">Keep these concepts in mind when building flows:</span></span> 

- <span data-ttu-id="1e67f-136">Každý tok má dvě hlavní části: *aktivační událost* a jednu nebo více *akcí*.</span><span class="sxs-lookup"><span data-stu-id="1e67f-136">Every flow has two main parts: a *trigger*, and one or more *actions*.</span></span>
- <span data-ttu-id="1e67f-137">Aktivační událost si můžete představit jako akci, která tok zahajuje.</span><span class="sxs-lookup"><span data-stu-id="1e67f-137">You can think of the trigger as the starting action for the flow.</span></span> <span data-ttu-id="1e67f-138">Aktivační událostí může být třeba nový e-mail, který přijde do vaší doručené pošty, nebo nová položka přidaná do seznamu SharePointu.</span><span class="sxs-lookup"><span data-stu-id="1e67f-138">The trigger can be something like a new email arriving in your inbox or a new item being added to a SharePoint list.</span></span>
- <span data-ttu-id="1e67f-139">Akce definují, co se má stát, pokud dojde k aktivační události.</span><span class="sxs-lookup"><span data-stu-id="1e67f-139">Actions are what you want to happen when a trigger is invoked.</span></span> <span data-ttu-id="1e67f-140">Aktivační událost nového e-mailu například zahájí akci spočívající ve vytvoření nového souboru na OneDrivu pro firmy.</span><span class="sxs-lookup"><span data-stu-id="1e67f-140">For example, the new email trigger will start the action of creating a new file on OneDrive for Business.</span></span> <span data-ttu-id="1e67f-141">K dalším příkladům akcí patří poslání e-mailu, zveřejnění tweetu nebo zahájení schválení.</span><span class="sxs-lookup"><span data-stu-id="1e67f-141">Other examples of actions include sending an email, posting a tweet, and starting an approval.</span></span>

<span data-ttu-id="1e67f-142">Tyto možnosti použijete později, až budete vytvářet vlastní toky úplně od začátku.</span><span class="sxs-lookup"><span data-stu-id="1e67f-142">These concepts will come into play later, when you build your own flows from scratch.</span></span> 

<span data-ttu-id="1e67f-143">V další lekci se podíváme na mobilní aplikaci Microsoft Flow a její možnosti.</span><span class="sxs-lookup"><span data-stu-id="1e67f-143">In the next unit, we'll look at the Microsoft Flow mobile app and its capabilities.</span></span> 
