---
ms.openlocfilehash: 8d456d62063030c732abdc5528646a56aba618f8
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698342"
---
<span data-ttu-id="1d9bc-101">Microsoft Flow se běžně používá tak, že když se něco stane, dostanete oznámení.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-101">A common use of Microsoft Flow is to get a notification when something happens.</span></span> <span data-ttu-id="1d9bc-102">Oznámení můžou být e-maily, textové zprávy nebo nabízená oznámení ve vašem telefonu.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-102">Notifications can be emails, text messages, or push notifications on your phone.</span></span>

<span data-ttu-id="1d9bc-103">V této lekci vytvoříte tok, který vygeneruje nabízené oznámení, kdykoli vám od nadřízeného přijde e-mail.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-103">In this unit, you'll create a flow that generates a push notification whenever you receive an email from your manager.</span></span>

## <a name="get-the-mobile-app"></a><span data-ttu-id="1d9bc-104">Získání mobilní aplikace</span><span class="sxs-lookup"><span data-stu-id="1d9bc-104">Get the mobile app</span></span>

<span data-ttu-id="1d9bc-105">Je snadné vytvořit tok, který bude do vašeho mobilního zařízení posílat nabízená oznámení.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-105">It's easy to create a flow that sends push notifications to your mobile device.</span></span> <span data-ttu-id="1d9bc-106">Mějte na paměti, že k příjmu nabízených oznámení potřebujete mobilní aplikaci Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-106">Keep in mind that you'll need the Microsoft Flow mobile app to receive push notifications.</span></span> <span data-ttu-id="1d9bc-107">Tato mobilní aplikace je dostupná pro [Google Android](https://play.google.com/store/apps/details?id=com.microsoft.flow), [Apple iOS](https://itunes.apple.com/app/apple-store/id1094928825) a [Windows Phone](https://www.microsoft.com/p/microsoft-flow/9nkn0p5l9n84).</span><span class="sxs-lookup"><span data-stu-id="1d9bc-107">The mobile app is available for [Google Android](https://play.google.com/store/apps/details?id=com.microsoft.flow), [Apple iOS](https://itunes.apple.com/app/apple-store/id1094928825), and [Windows Phone](https://www.microsoft.com/p/microsoft-flow/9nkn0p5l9n84).</span></span>

<span data-ttu-id="1d9bc-108">Pokud používáte nepodporované mobilní zařízení, můžete místo nabízených oznámení používat zprávy SMS (Short Message Service) – to znamená textové zprávy.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-108">If you're using an unsupported mobile device, consider using Short Message Service (SMS) messages (that is, text messages) instead of push notifications to receive notifications.</span></span>

## <a name="create-a-flow-that-sends-push-notifications"></a><span data-ttu-id="1d9bc-109">Vytvoření toku, který posílá nabízená oznámení</span><span class="sxs-lookup"><span data-stu-id="1d9bc-109">Create a flow that sends push notifications</span></span>

<span data-ttu-id="1d9bc-110">Microsoft Flow obsahuje mnoho šablon, které vám pomůžou začít s vytvářením toků.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-110">Microsoft Flow comes with many templates to get you started with creating flows.</span></span> <span data-ttu-id="1d9bc-111">Vytvoříme tok pomocí šablony.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-111">Let's create a flow by using a template.</span></span>

1. <span data-ttu-id="1d9bc-112">Přihlaste se k [Microsoft Flow](https://ms.flow.microsoft.com) pomocí účtu své organizace.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-112">Sign in to [Microsoft Flow](https://ms.flow.microsoft.com) by using your organizational account.</span></span>
1. <span data-ttu-id="1d9bc-113">Vyberte **Moje toky**.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-113">Select **My flows**.</span></span>
1. <span data-ttu-id="1d9bc-114">Vyberte **Nový** a pak **Vytvořit ze šablony**.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-114">Select **New**, and then select **Create from template**.</span></span>

    ![Vytvoření ze šablony](../media/Flow-notification-boss.png)

1. <span data-ttu-id="1d9bc-116">Posuňte se dolů a vyberte **Nabízené oznámení, když dostanete e-mail od nadřízeného**.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-116">Scroll down, and select **Get a push notification when you receive an email from your boss**.</span></span>

    <span data-ttu-id="1d9bc-117">Tuto šablonu můžete rychle najít také tak, že do vyhledávacího pole zadáte *oznámení*.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-117">You can also quickly find this template by entering *notifications* in the search field.</span></span>

1. <span data-ttu-id="1d9bc-118">Vyberte **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-118">Select **Continue**.</span></span>

    <span data-ttu-id="1d9bc-119">V toku se zobrazí kroky sloužící k tomu, aby se před spuštěním toku získaly e-mailové profily vás a vašeho nadřízeného.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-119">In the flow, you'll see the steps that will be used to get your email profile and your boss's before the flow is started.</span></span>

1. <span data-ttu-id="1d9bc-120">Posuňte se dolů ke konci kroků toku a najděte oddíl **Kontrola, jestli je to můj nadřízený**.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-120">Scroll to the bottom of the flow steps to find the **Check if it is my manager** section.</span></span> <span data-ttu-id="1d9bc-121">E-mailové adresy vás a vašeho nadřízeného se automaticky vyplní ze zadaných profilových informací.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-121">Your email address and your manager's are automatically filled in from the profile information that you entered.</span></span>
1. <span data-ttu-id="1d9bc-122">V oddílu **Odeslání nabízeného oznámení** vyberte **Upravit** a změňte text oznámení, které obdržíte, když vám od nadřízeného přijde e-mail.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-122">In the **Send a push notification** section, select **Edit** to change the text of the notification that you'll get when an email is received from your boss.</span></span>

    ![Úprava parametrů nabízeného oznámení](../media/flow-check-my-manager.png)

1. <span data-ttu-id="1d9bc-124">Pokud chcete změnit text e-mailu, zadejte do pole **Text** novou zprávu.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-124">To change the text of the email, in the **Text** field, enter a new message.</span></span> <span data-ttu-id="1d9bc-125">Můžete také v seznamu vybrat pole dynamického obsahu.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-125">You can also select dynamic content fields in the list.</span></span>

    ![Nový text zprávy](../media/flow-change-text.png)

1. <span data-ttu-id="1d9bc-127">Abyste tok uložili a mohli ho otestovat, vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-127">Select **Save** to save and test the flow.</span></span>
1. <span data-ttu-id="1d9bc-128">Pokud chcete tok změnit, vyberte **Upravit tok**.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-128">To change the flow, select **Edit flow**.</span></span>

<span data-ttu-id="1d9bc-129">Když vám budou od nadřízeného chodit e-maily, budete na telefon dostávat nabízená oznámení.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-129">Now, when emails arrive from your boss, you'll get a push notification on your phone.</span></span>
