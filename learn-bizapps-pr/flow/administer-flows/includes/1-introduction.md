---
ms.openlocfilehash: 7e11afe9c8710ca5aa09a5b1d8460d6102a1d233
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57697740"
---
<span data-ttu-id="c0b38-101">Vítejte v Centru pro správu!</span><span class="sxs-lookup"><span data-stu-id="c0b38-101">Welcome to the Admin center!</span></span> <span data-ttu-id="c0b38-102">Centrum pro správu je centrální umístění, ve kterém správci tenantů a správci prostředí spravují zásady pro data a prostředí dané organizace.</span><span class="sxs-lookup"><span data-stu-id="c0b38-102">The Admin center is the central location where tenant admins and environment admins manage an organization's data policies and environments.</span></span> <span data-ttu-id="c0b38-103">Všechny změny provedené v Centru pro správu jsou okamžitě dostupné uživatelům v organizaci.</span><span class="sxs-lookup"><span data-stu-id="c0b38-103">Any changes that you make in the Admin center are immediately available to users in the organization.</span></span>

<span data-ttu-id="c0b38-104">V tomto modulu se naučíte:</span><span class="sxs-lookup"><span data-stu-id="c0b38-104">In this module, you'll learn how to:</span></span>

- <span data-ttu-id="c0b38-105">Řešit potíže s toky</span><span class="sxs-lookup"><span data-stu-id="c0b38-105">Troubleshoot flows.</span></span>
- <span data-ttu-id="c0b38-106">Import a export toky</span><span class="sxs-lookup"><span data-stu-id="c0b38-106">Import and export flows.</span></span>
- <span data-ttu-id="c0b38-107">Sdílet toky</span><span class="sxs-lookup"><span data-stu-id="c0b38-107">Share flows.</span></span>
- <span data-ttu-id="c0b38-108">Monitorovat toky</span><span class="sxs-lookup"><span data-stu-id="c0b38-108">Monitor flows.</span></span>

![Centrum pro správu](../media/overview.png)

## <a name="open-the-admin-center"></a><span data-ttu-id="c0b38-110">Otevření Centra pro správu</span><span class="sxs-lookup"><span data-stu-id="c0b38-110">Open the Admin center</span></span>
<span data-ttu-id="c0b38-111">Existují dva způsoby, jak otevřít Centrum pro správu.</span><span class="sxs-lookup"><span data-stu-id="c0b38-111">There are two ways to open the Admin center.</span></span>

### <a name="option-1-select-settings"></a><span data-ttu-id="c0b38-112">1. možnost: Výběr nastavení</span><span class="sxs-lookup"><span data-stu-id="c0b38-112">Option 1: Select settings</span></span>

1. <span data-ttu-id="c0b38-113">Přejděte na [flow.microsoft.com](https://flow.microsoft.com) a přihlaste se pod účtem své organizace.</span><span class="sxs-lookup"><span data-stu-id="c0b38-113">Go to [flow.microsoft.com](https://flow.microsoft.com), and sign in by using your organizational account.</span></span>
1. <span data-ttu-id="c0b38-114">Vyberte tlačítko **Nastavení** (symbol ozubeného kola) a pak vyberte v nabídce **Centrum pro správu**.</span><span class="sxs-lookup"><span data-stu-id="c0b38-114">Select the **Settings** button (the gear symbol), and then select **Admin Center** on the menu.</span></span>

    ![Centrum pro správu v nabídce Nastavení](../media/settings.png)

    <span data-ttu-id="c0b38-116">Otevře se Centrum pro správu.</span><span class="sxs-lookup"><span data-stu-id="c0b38-116">The Admin center is opened.</span></span>

### <a name="option-2-open-adminflowmicrosoftcom"></a><span data-ttu-id="c0b38-117">2. možnost: Otevření stránky admin.flow.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c0b38-117">Option 2: Open admin.flow.microsoft.com</span></span>

- <span data-ttu-id="c0b38-118">Přejděte na [admin.flow.microsoft.com](https://admin.flow.microsoft.com) a přihlaste se svým pracovním účtem.</span><span class="sxs-lookup"><span data-stu-id="c0b38-118">Go to [admin.flow.microsoft.com](https://admin.flow.microsoft.com), and sign in by using your work account.</span></span>

## <a name="environments"></a><span data-ttu-id="c0b38-119">Prostředí</span><span class="sxs-lookup"><span data-stu-id="c0b38-119">Environments</span></span>

<span data-ttu-id="c0b38-120">*Prostředí* je prostor, kde můžete ukládat, spravovat a sdílet obchodní data, aplikace a toky vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="c0b38-120">An *environment* is a space where you can store, manage, and share your organization's business data, apps, and flows.</span></span> <span data-ttu-id="c0b38-121">Slouží také jako kontejner k oddělení aplikací, které by mohly mít různé role, požadavky na zabezpečení nebo cílové skupiny.</span><span class="sxs-lookup"><span data-stu-id="c0b38-121">It also serves as a container to separate apps that might have different roles, security requirements, or target audiences.</span></span>

<span data-ttu-id="c0b38-122">Způsob, jakým používáte prostředí, závisí na vaší organizaci a aplikacích, které se pokoušíte zkompilovat.</span><span class="sxs-lookup"><span data-stu-id="c0b38-122">The way that you use environments depends on your organization and the apps that you're trying to build.</span></span> <span data-ttu-id="c0b38-123">Zde je několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="c0b38-123">Here are some examples:</span></span>

- <span data-ttu-id="c0b38-124">Můžete vytvořit samostatná prostředí k seskupování testovacích a produkčních verzí svých aplikací.</span><span class="sxs-lookup"><span data-stu-id="c0b38-124">You can create separate environments to group the test and production versions of your apps.</span></span>
- <span data-ttu-id="c0b38-125">Můžete vytvořit samostatná prostředí, která odpovídají konkrétním týmům nebo oddělením ve vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="c0b38-125">You can create separate environments that correspond to specific teams or departments in your company.</span></span> <span data-ttu-id="c0b38-126">Každé prostředí obsahuje relevantní data a aplikace pro každý tým nebo oddělení.</span><span class="sxs-lookup"><span data-stu-id="c0b38-126">Each environment holds the relevant data and apps for each team/department.</span></span>
- <span data-ttu-id="c0b38-127">Můžete vytvořit samostatná prostředí pro různé globální pobočky vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="c0b38-127">You can create separate environments for different global branches of your company.</span></span>
- <span data-ttu-id="c0b38-128">Můžete kompilovat všechny svoje aplikace v jednom prostředí.</span><span class="sxs-lookup"><span data-stu-id="c0b38-128">You can build all your apps in a single environment.</span></span>

## <a name="data-policies"></a><span data-ttu-id="c0b38-129">Zásady pro data</span><span class="sxs-lookup"><span data-stu-id="c0b38-129">Data policies</span></span>

<span data-ttu-id="c0b38-130">Pokud používáte Microsoft Flow, data jsou automaticky chráněna pomocí rolí zabezpečení, které má vaše organizace už zavedené.</span><span class="sxs-lookup"><span data-stu-id="c0b38-130">When you use Microsoft Flow, the data is automatically protected with whatever security roles your organization already has in place.</span></span> <span data-ttu-id="c0b38-131">Pomocí Microsoft Flow není možné získat přístup k informacím, ke kterým už uživatel nemá přístup v organizaci.</span><span class="sxs-lookup"><span data-stu-id="c0b38-131">It isn't possible to use Microsoft Flow to get access to information that the user doesn't already have access to in the organization.</span></span> <span data-ttu-id="c0b38-132">Některé organizace se můžou rozhodnout, že bude vhodné přidat další volitelnou vrstvu zabezpečení, která může aktivně blokovat toky, které porušují určité zásady.</span><span class="sxs-lookup"><span data-stu-id="c0b38-132">Some organizations may want to add an additional, optional layer of security that can proactively block flows that violate certain policies.</span></span>
