---
ms.openlocfilehash: 40984c7d5e5d39bb414eaf94864d9ae8b1a44ce9
ms.sourcegitcommit: ea295d90d665cb91222895600f8945aff5a20f02
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58218046"
---
<span data-ttu-id="d9709-101">Návrh modelem řízené aplikace je přístup, který se zaměřuje na přidávání řídicích panelů, formulářů, zobrazení a grafů do aplikací.</span><span class="sxs-lookup"><span data-stu-id="d9709-101">Model-driven app design is an approach that focuses on adding dashboards, forms, views, and charts to your apps.</span></span> <span data-ttu-id="d9709-102">Bez kódu nebo jen s minimem kódu tak můžete sestavit aplikace, které jsou jednoduché nebo velmi složité.</span><span class="sxs-lookup"><span data-stu-id="d9709-102">With no code, or very little, you can build apps that are simple or very complex.</span></span>

<span data-ttu-id="d9709-103">V aplikacích plátna má návrhář úplnou kontrolu nad rozložením aplikace.</span><span class="sxs-lookup"><span data-stu-id="d9709-103">In canvas apps, the designer has total control over the app layout.</span></span> <span data-ttu-id="d9709-104">V modelem řízených aplikacích je na druhé straně rozložení určené přidanými komponentami.</span><span class="sxs-lookup"><span data-stu-id="d9709-104">In model-driven apps, on the other hand, much of the layout is determined by the components you add.</span></span> <span data-ttu-id="d9709-105">Důraz se klade hlavně na rychlé zobrazení obchodních dat a rozhodování, než na komplikovaný návrh aplikace.</span><span class="sxs-lookup"><span data-stu-id="d9709-105">The emphasis is more on quickly viewing your business data and making decisions than on intricate app design.</span></span>

![Ukázková modelem řízená aplikace](../media/model-app-sample.png)

<span data-ttu-id="d9709-107">Zde jsou některé z výhod modelem řízených aplikací:</span><span class="sxs-lookup"><span data-stu-id="d9709-107">Here are some of the benefits of model-driven apps:</span></span>

- <span data-ttu-id="d9709-108">Vytváření plnohodnotných prostředí zaměřených na komponenty</span><span class="sxs-lookup"><span data-stu-id="d9709-108">Create rich, component-focused environments.</span></span>
- <span data-ttu-id="d9709-109">Není zapotřebí žádný (nebo téměř žádný) kód.</span><span class="sxs-lookup"><span data-stu-id="d9709-109">No code (or very little) is needed.</span></span> 
- <span data-ttu-id="d9709-110">Můžete vytvářet komplexní responzivní aplikace, které vypadají skvěle na různých zařízeních, a vyvíjet je v jediném prostředí.</span><span class="sxs-lookup"><span data-stu-id="d9709-110">Create complex responsive apps that look great on a variety of devices while developing them in one environment.</span></span>
- <span data-ttu-id="d9709-111">Možnosti návrhu se podobají tomu, co je k dispozici na platformě Microsoft Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="d9709-111">Design capabilities are similar to what's available in the Microsoft Dynamics 365 Customer Engagement platform.</span></span>
- <span data-ttu-id="d9709-112">Aplikaci je možné distribuovat jako řešení.</span><span class="sxs-lookup"><span data-stu-id="d9709-112">Your app can be distributed as a solution.</span></span>

## <a name="the-approach-to-making-model-driven-apps"></a><span data-ttu-id="d9709-113">Přístup k vytváření modelem řízených aplikací</span><span class="sxs-lookup"><span data-stu-id="d9709-113">The approach to making model-driven apps</span></span>
<span data-ttu-id="d9709-114">Modelem řízené aplikace mají tři fáze návrhu:</span><span class="sxs-lookup"><span data-stu-id="d9709-114">Model-driven apps have three design phases:</span></span>

1. <span data-ttu-id="d9709-115">Modelování obchodních dat</span><span class="sxs-lookup"><span data-stu-id="d9709-115">Model your business data.</span></span>
1. <span data-ttu-id="d9709-116">Definování obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="d9709-116">Define your business processes.</span></span>
1. <span data-ttu-id="d9709-117">Sestavení aplikace</span><span class="sxs-lookup"><span data-stu-id="d9709-117">Build the app.</span></span>

### <a name="model-your-business-data"></a><span data-ttu-id="d9709-118">Modelování obchodních dat</span><span class="sxs-lookup"><span data-stu-id="d9709-118">Model your business data</span></span>
<span data-ttu-id="d9709-119">Modelem řízený návrh využívá metadaty řízenou architekturu, aby návrháři mohli aplikace přizpůsobit bez psaní kódu.</span><span class="sxs-lookup"><span data-stu-id="d9709-119">Model-driven design uses metadata-driven architecture so that designers can customize apps without writing code.</span></span> <span data-ttu-id="d9709-120">Při modelování obchodních dat určíte, jaká data bude aplikace potřebovat a jak tato data budou souviset s jinými daty.</span><span class="sxs-lookup"><span data-stu-id="d9709-120">To model business data, you determine what data the app will need and how that data will relate to other data.</span></span> <span data-ttu-id="d9709-121">Metadata jsou *data o datech* a definují strukturu dat uložených ve službě Common Data Service pro aplikace.</span><span class="sxs-lookup"><span data-stu-id="d9709-121">Metadata means *data about data* and it defines the structure of the data stored in Common Data Service for Apps.</span></span>

### <a name="define-your-business-processes"></a><span data-ttu-id="d9709-122">Definování obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="d9709-122">Define your business processes</span></span>
<span data-ttu-id="d9709-123">Definování a prosazování konzistentních obchodních procesů je klíčovým aspektem návrhu modelem řízené aplikace.</span><span class="sxs-lookup"><span data-stu-id="d9709-123">Defining and enforcing consistent business processes is a key aspect of model-driven app design.</span></span> <span data-ttu-id="d9709-124">Konzistentní procesy pomáhají zajistit, že se uživatelé vaší aplikace můžou soustředit na práci a nemusí si pamatovat sadu ručně prováděných kroků.</span><span class="sxs-lookup"><span data-stu-id="d9709-124">Consistent processes help ensure that your app users can focus on their work and not worry about having to remember to perform a set of manual steps.</span></span> <span data-ttu-id="d9709-125">Procesy můžou být jednoduché nebo složité a v průběhu času se často mění.</span><span class="sxs-lookup"><span data-stu-id="d9709-125">Processes can be simple or complex, and they often change over time.</span></span>

### <a name="build-the-app"></a><span data-ttu-id="d9709-126">Sestavení aplikace</span><span class="sxs-lookup"><span data-stu-id="d9709-126">Build the app</span></span>
<span data-ttu-id="d9709-127">Po modelování dat a definování procesů sestavíte aplikaci výběrem a nastavením potřebných komponent v návrháři aplikací.</span><span class="sxs-lookup"><span data-stu-id="d9709-127">After modeling data and defining processes, you build your app by selecting and setting up the components you need in the App Designer.</span></span>

![Návrhář aplikací](../media/app-designer.png)
