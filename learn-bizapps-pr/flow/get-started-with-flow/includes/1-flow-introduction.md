---
ms.openlocfilehash: e55b43d448774548cae7f2191120fb24766bc5ae
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698342"
---
<span data-ttu-id="95983-101">Vítá vás Microsoft Flow!</span><span class="sxs-lookup"><span data-stu-id="95983-101">Welcome to Microsoft Flow!</span></span> <span data-ttu-id="95983-102">V tomto modulu se naučíte, jak vytvářet toky.</span><span class="sxs-lookup"><span data-stu-id="95983-102">In this module, you'll learn how to build flows.</span></span>

<span data-ttu-id="95983-103">Pokud s Microsoft Flow teprve začínáte, tento modul vám pomůže posunout se dále.</span><span class="sxs-lookup"><span data-stu-id="95983-103">If you're a beginner with Microsoft Flow, this module will get you going.</span></span> <span data-ttu-id="95983-104">Pokud už nějaké zkušenosti máte, tento modul propojí dosud získané znalosti a vyplní případné mezery.</span><span class="sxs-lookup"><span data-stu-id="95983-104">If you already have some experience, this module will tie concepts together and fill in the gaps.</span></span>

## <a name="learning-objectives"></a><span data-ttu-id="95983-105">Cíle výuky</span><span class="sxs-lookup"><span data-stu-id="95983-105">Learning objectives</span></span>
<span data-ttu-id="95983-106">V tomto modulu:</span><span class="sxs-lookup"><span data-stu-id="95983-106">In this module, you will:</span></span>
   - <span data-ttu-id="95983-107">Zjistíte, co je Microsoft Flow a jak se používá.</span><span class="sxs-lookup"><span data-stu-id="95983-107">Learn what Microsoft Flow is and how it can be used</span></span>
   - <span data-ttu-id="95983-108">Vytvoříte tok, který automaticky ukládá e-mailové přílohy.</span><span class="sxs-lookup"><span data-stu-id="95983-108">Create a flow that automatically saves email attachments</span></span>
   - <span data-ttu-id="95983-109">Zjistíte, jak vytvořit tok aktivovaný tlačítkem, kterým pošlete připomenutí sami sobě.</span><span class="sxs-lookup"><span data-stu-id="95983-109">Learn how to create a button flow to send yourself a reminder</span></span>
   - <span data-ttu-id="95983-110">Vytvoříte tok, který posílá oznámení.</span><span class="sxs-lookup"><span data-stu-id="95983-110">Create a flow that sends you notifications</span></span>
   - <span data-ttu-id="95983-111">Vytvoříte tok, který kopíruje soubory.</span><span class="sxs-lookup"><span data-stu-id="95983-111">Create a flow that copies files</span></span>
   - <span data-ttu-id="95983-112">Vytvoříte tok, který se spouští podle plánu.</span><span class="sxs-lookup"><span data-stu-id="95983-112">Create a flow that runs on a schedule</span></span>
   - <span data-ttu-id="95983-113">Vytvoříte tok, který publikuje tweety.</span><span class="sxs-lookup"><span data-stu-id="95983-113">Create a flow that posts tweets</span></span>
   - <span data-ttu-id="95983-114">Vytvoříte tok, který může být používaný vaším týmem.</span><span class="sxs-lookup"><span data-stu-id="95983-114">Create a flow that your team can use</span></span>

## <a name="what-is-microsoft-flow"></a><span data-ttu-id="95983-115">Co je Microsoft Flow?</span><span class="sxs-lookup"><span data-stu-id="95983-115">What is Microsoft Flow?</span></span>
<span data-ttu-id="95983-116">Microsoft Flow je online služba pro vytváření pracovních postupů, která automatizuje různé akce v nejčastěji používaných aplikacích a službách.</span><span class="sxs-lookup"><span data-stu-id="95983-116">Microsoft Flow is an online workflow service that automates actions across the most common apps and services.</span></span> <span data-ttu-id="95983-117">Můžete třeba vytvořit tok, který přidá potenciálního zákazníka do Microsoft Dynamicsu 365 a vytvoří záznam v MailChimpu pokaždé, když někdo s více než 100 sledujícími tweetuje o vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="95983-117">For example, you can create a flow that adds a lead to Microsoft Dynamics 365 and a record in MailChimp whenever someone with more than 100 followers tweets about your company.</span></span>

![Koncepční nákres toku](../media/flow-conceptual.png)

<span data-ttu-id="95983-119">Po přihlášení se můžete připojit k více než 220 službám a můžete spravovat data v cloudu nebo místních zdrojích, jako je SharePoint nebo Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="95983-119">When you sign up, you can connect to more than 220 services, and can manage data either in the cloud or in on-premises sources like SharePoint and Microsoft SQL Server.</span></span> <span data-ttu-id="95983-120">Seznam aplikací, které můžete v Microsoft Flow použít, se stále rozrůstá.</span><span class="sxs-lookup"><span data-stu-id="95983-120">The list of applications you can use with Microsoft Flow grows constantly.</span></span>

![Seznam služeb](../media/flow-services.png)

## <a name="what-can-you-do-with-microsoft-flow"></a><span data-ttu-id="95983-122">K čemu slouží Microsoft Flow?</span><span class="sxs-lookup"><span data-stu-id="95983-122">What can you do with Microsoft Flow?</span></span>

<span data-ttu-id="95983-123">V Microsoft Flow můžete automatizovat pracovní postupy probíhající mezi vašimi oblíbenými aplikacemi a službami. Můžete synchronizovat soubory, dostávat oznámení, shromažďovat data a mnoho dalšího.</span><span class="sxs-lookup"><span data-stu-id="95983-123">You can use Microsoft Flow to automate workflows between your favorite applications and services, sync files, get notifications, collect data, and much more.</span></span> 

<span data-ttu-id="95983-124">Můžete automatizovat třeba tyto úlohy:</span><span class="sxs-lookup"><span data-stu-id="95983-124">For example, you can automate these tasks:</span></span>

* <span data-ttu-id="95983-125">Ihned reagovat na oznámení nebo e-maily s vysokou prioritou.</span><span class="sxs-lookup"><span data-stu-id="95983-125">Instantly respond to high-priority notifications or emails.</span></span>
* <span data-ttu-id="95983-126">Zaznamenat a sledovat nové potenciální zákazníky a dále s nimi pracovat.</span><span class="sxs-lookup"><span data-stu-id="95983-126">Capture, track, and follow up with new sales leads.</span></span>
* <span data-ttu-id="95983-127">Kopírovat všechny e-mailové přílohy do účtu OneDrivu pro firmy.</span><span class="sxs-lookup"><span data-stu-id="95983-127">Copy all email attachments to your OneDrive for Business account.</span></span>
* <span data-ttu-id="95983-128">Shromažďovat data o vaší firmě a sdílet tyto informace s vaším týmem.</span><span class="sxs-lookup"><span data-stu-id="95983-128">Collect data about your business, and share that information with your team.</span></span>
* <span data-ttu-id="95983-129">Automatizovat schvalovací pracovní postupy.</span><span class="sxs-lookup"><span data-stu-id="95983-129">Automate approval workflows.</span></span>

<span data-ttu-id="95983-130">Microsoft Flow se často používá, když chcete dostávat oznámení.</span><span class="sxs-lookup"><span data-stu-id="95983-130">A common use of Microsoft Flow is to receive notifications.</span></span> <span data-ttu-id="95983-131">Když třeba do Dynamicsu 365 nebo do Salesforce přibude potenciální zákazník, můžete hned dostat e-mail nebo si v telefonu přečíst nabízené oznámení.</span><span class="sxs-lookup"><span data-stu-id="95983-131">For example, you can instantly receive an email or a push notification on your phone whenever a sales lead is added to Dynamics 365 or Salesforce.</span></span>

![Příklad e-mailu s oznámením nebo nabízeného oznámení](../media/sales-lead.png)

<span data-ttu-id="95983-133">Microsoft Flow také můžete použít ke kopírování souborů.</span><span class="sxs-lookup"><span data-stu-id="95983-133">You can also use Microsoft Flow to copy files.</span></span> <span data-ttu-id="95983-134">Můžete třeba zajistit, aby se každý soubor přidaný do Dropboxu také automaticky zkopíroval do SharePointu, kde ho váš tým najde.</span><span class="sxs-lookup"><span data-stu-id="95983-134">For example, you can ensure that any file that's added to Dropbox is automatically copied to SharePoint, where your team can find it.</span></span>

![Seznam souborů v Dropboxu](../media/dropbox-files.png) 

![Seznam stejných souborů v SharePointu](../media/sharepoint-files.png) 

<span data-ttu-id="95983-137">Můžete sledovat, co lidé říkají o vaší firmě. Stačí vytvořit tok, který se spustí pokaždé, když někdo pošle tweet s určitým hashtagem.</span><span class="sxs-lookup"><span data-stu-id="95983-137">You can monitor what people are saying about your business by creating a flow that runs whenever someone sends a tweet with a certain hashtag.</span></span> <span data-ttu-id="95983-138">Tok může přidat podrobnosti o každém tweetu do databáze SQL Serveru, seznamu SharePointu nebo třeba do souboru Microsoft Excelu, který je hostovaný na OneDrivu pro firmy, podle toho, jaká služba vám více vyhovuje.</span><span class="sxs-lookup"><span data-stu-id="95983-138">The flow can add details about each tweet to a Facebook post, a SQL Server database, a SharePoint list, or even a Microsoft Excel file that's hosted on OneDrive for Business–-whichever service works for you.</span></span> 

<span data-ttu-id="95983-139">Můžete vytvářet akce, které připojí shromažďovaná data k Microsoft Power BI, budou sledovat trendy v těchto datech a budou klást otázky.</span><span class="sxs-lookup"><span data-stu-id="95983-139">You can create actions to connect the data you collect to Microsoft Power BI, spot trends in that data, and ask questions about it.</span></span>

<span data-ttu-id="95983-140">Následující příklad ukazuje tok, který uloží tweety s hashtagem #MicrosoftFlow do souboru v Excelu.</span><span class="sxs-lookup"><span data-stu-id="95983-140">The following example shows a flow that saves tweets with the hashtag #MicrosoftFlow to an Excel file.</span></span>

![Tweet](../media/tweets-to-excel.png)

![Stejný tweet v Excelu](../media/excel-tweets.png)

<span data-ttu-id="95983-143">Můžete také automatizovat schvalovací kolečka například u žádostí o dovolenou, které jsou v seznamu SharePointu.</span><span class="sxs-lookup"><span data-stu-id="95983-143">Also, you can automate approval loops for things like vacation requests on a SharePoint list.</span></span>

![Seznam žádostí o dovolenou v SharePointu](../media/vacation-requests.png)

<span data-ttu-id="95983-145">Další nápady najdete v seznamu šablon.</span><span class="sxs-lookup"><span data-stu-id="95983-145">For more ideas, browse our list of templates.</span></span> <span data-ttu-id="95983-146">Šablony usnadňují vytváření toků – stačí udělat jen pár změn v konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="95983-146">Templates help you build flows by making a few configuration changes.</span></span> <span data-ttu-id="95983-147">Pomocí šablon můžete třeba jednoduše vytvořit toky, které vám pošlou předpověď počasí, pravidelně vám něco připomenou nebo vás upozorní v telefonu pokaždé, když vám nadřízený pošle e-mail.</span><span class="sxs-lookup"><span data-stu-id="95983-147">For example, you can use templates to easily build flows to send yourself weather forecasts, reminders at regular intervals, or phone notifications whenever your manager sends you mail.</span></span>

![Seznam šablon](../media/templates-you-might-use.png)

<span data-ttu-id="95983-149">Napadá vás tok, který v seznamu není?</span><span class="sxs-lookup"><span data-stu-id="95983-149">Have an idea for a flow that you don't see in the list?</span></span> <span data-ttu-id="95983-150">Můžete si vytvořit vlastní tok úplně od začátku, a pokud chcete, můžete ho sdílet s komunitou.</span><span class="sxs-lookup"><span data-stu-id="95983-150">Create your own from scratch and, if you want, share it with the community!</span></span>

## <a name="where-can-i-create-and-administer-a-flow"></a><span data-ttu-id="95983-151">Kde můžu tok vytvořit a spravovat?</span><span class="sxs-lookup"><span data-stu-id="95983-151">Where can I create and administer a flow?</span></span>

<span data-ttu-id="95983-152">Vytvořit tok a plnit úkoly spojené s jeho správou můžete v prohlížeči. Pokud si stáhnete mobilní aplikaci Microsoft Flow, můžete tyto úkoly provádět na telefonu.</span><span class="sxs-lookup"><span data-stu-id="95983-152">You can create a flow and perform administrative tasks in a browser or, if you download the Microsoft Flow mobile app, on your phone.</span></span>

![Snímek obrazovky s mobilní aplikací](../media/screen-mobile-app.png)

<span data-ttu-id="95983-154">Tady jsou některé úlohy, které můžete provádět pomocí mobilní aplikace:</span><span class="sxs-lookup"><span data-stu-id="95983-154">Here are some of the tasks you can perform with the mobile app:</span></span>

* <span data-ttu-id="95983-155">Zapínat a vypínat toky bez ohledu na to, kde jste.</span><span class="sxs-lookup"><span data-stu-id="95983-155">Turn flows on or off from wherever you are.</span></span>
* <span data-ttu-id="95983-156">Podívat se, kdy tok selhal.</span><span class="sxs-lookup"><span data-stu-id="95983-156">See when a flow has failed.</span></span>
* <span data-ttu-id="95983-157">Kontrolovat podrobné sestavy o historii spuštění.</span><span class="sxs-lookup"><span data-stu-id="95983-157">Review detailed run history reports.</span></span>
* <span data-ttu-id="95983-158">Zobrazit a filtrovat spuštění podle typu oznámení.</span><span class="sxs-lookup"><span data-stu-id="95983-158">View and filter runs by notification type.</span></span>

## <a name="a-brief-tour-of-microsoft-flow"></a><span data-ttu-id="95983-159">Stručný přehled Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="95983-159">A brief tour of Microsoft Flow</span></span>
<span data-ttu-id="95983-160">Pojďme přejít k nástroji Microsoft Flow. Ukážeme si, jak ho používat.</span><span class="sxs-lookup"><span data-stu-id="95983-160">Let's jump into Microsoft Flow, and we'll show you around.</span></span> <span data-ttu-id="95983-161">Máme pro vás spoustu informací, ze kterých se dozvíte, jak Microsoft Flow používat.</span><span class="sxs-lookup"><span data-stu-id="95983-161">We have tons of information for you to learn about how to use Microsoft Flow.</span></span>

![Začátek prohlídky](../media/start-of-tour.png)

<span data-ttu-id="95983-163">Při přihlášení k Microsoft Flow uvidíte tyto nabídky:</span><span class="sxs-lookup"><span data-stu-id="95983-163">When you sign in to Microsoft Flow, you'll find these menus:</span></span>

* <span data-ttu-id="95983-164">**Moje toky** – v této nabídce jsou vaše toky.</span><span class="sxs-lookup"><span data-stu-id="95983-164">**My flows**, where your flows reside.</span></span>
* <span data-ttu-id="95983-165">**Šablony** – tady se můžete podívat na nejoblíbenější šablony.</span><span class="sxs-lookup"><span data-stu-id="95983-165">**Templates**, where you can take a look at some of the most popular templates.</span></span> <span data-ttu-id="95983-166">Sem se také můžete podívat na nápady, jaké toky byste mohli vyzkoušet.</span><span class="sxs-lookup"><span data-stu-id="95983-166">These should give you some great ideas for flows you want to try.</span></span>
* <span data-ttu-id="95983-167">**Schválení** – v této nabídce můžete automatizovat a zjednodušit schvalovací proces.</span><span class="sxs-lookup"><span data-stu-id="95983-167">**Approvals**, where you can automate and streamline your approval process.</span></span>
* <span data-ttu-id="95983-168">**Konektory** (dříve Služby) – v této nabídce se můžete připojovat z jedné služby k jiné.</span><span class="sxs-lookup"><span data-stu-id="95983-168">**Connectors**, (formerly called Services), where you can connect from one service to another.</span></span>
* <span data-ttu-id="95983-169">**Data** – tady můžete přistupovat k entitám, připojením, vlastním konektorům a bránám.</span><span class="sxs-lookup"><span data-stu-id="95983-169">**Data**, where you can access entities, connections, custom connectors and gateways.</span></span>
* <span data-ttu-id="95983-170">**Řešení** – tady můžete spravovat vaše řešení.</span><span class="sxs-lookup"><span data-stu-id="95983-170">**Solutions**, where you can manage your solutions.</span></span> 
* <span data-ttu-id="95983-171">**Kurzy** – v této nabídce najdete informace, které vám pomůžou v Microsoft Flow rychle postupovat dopředu.</span><span class="sxs-lookup"><span data-stu-id="95983-171">**Learn**, where you can find information that will help you quickly ramp up on Microsoft Flow.</span></span>

<span data-ttu-id="95983-172">Teď se zaměřme na nabídku **?**</span><span class="sxs-lookup"><span data-stu-id="95983-172">For now, let's focus on the **?**</span></span> <span data-ttu-id="95983-173">vedle vašich přihlašovacích údajů, která má tyto možnosti:</span><span class="sxs-lookup"><span data-stu-id="95983-173">menu next to your login, which has these options:</span></span>

* <span data-ttu-id="95983-174">**Dokumentace** – v této nabídce najdete pokročilá témata.</span><span class="sxs-lookup"><span data-stu-id="95983-174">**Documentation** is where our advanced topics reside.</span></span> <span data-ttu-id="95983-175">Pokud chcete důkladně porozumět některé vlastnosti nebo funkci, tady najdete podrobné informace.</span><span class="sxs-lookup"><span data-stu-id="95983-175">If you want to really understand a feature or function, you can do a deep dive here to figure things out.</span></span>
* <span data-ttu-id="95983-176">**Učení** – povede vás při používání Microsoft Flowu od počátečních technik až po pokročilé scénáře.</span><span class="sxs-lookup"><span data-stu-id="95983-176">**Learn** has learning paths to guide you through using Microsoft Flow, all the way from beginning techniques to advanced scenarios.</span></span>
* <span data-ttu-id="95983-177">**Podpora** – tady najdete potřebnou pomoc.</span><span class="sxs-lookup"><span data-stu-id="95983-177">**Support** is a great landing place to find help.</span></span>
* <span data-ttu-id="95983-178">**Komunita** – můžete se zapojit nebo se zde dozvíte, jak používají Microsoft Flow ostatní.</span><span class="sxs-lookup"><span data-stu-id="95983-178">**Community** is a place to plug into and find out how other people use Microsoft Flow.</span></span>
* <span data-ttu-id="95983-179">**Váš názor** – můžete se obrátit na komunitu zkušených uživatelů. Tady můžete vývojářům a dalším zkušeným uživatelům posílat své komentáře a otázky.</span><span class="sxs-lookup"><span data-stu-id="95983-179">**Give Feedback** taps into a community of power users, and is where you can send comments and questions to developers and other experienced users.</span></span>
* <span data-ttu-id="95983-180">**Blog** – aktuální informace o nejnovějším vývoji a nejnovějších verzích v ekosystému Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="95983-180">**Blog** keeps you up to date about the most recent developments and releases in the Microsoft Flow ecosystem.</span></span>
* <span data-ttu-id="95983-181">**Ceny** – tato nabídka vám pomůže vybrat správný plán pro vás nebo pro vaši firmu.</span><span class="sxs-lookup"><span data-stu-id="95983-181">**Pricing** can help you choose the right plan for you or your business.</span></span>

## <a name="whats-next"></a><span data-ttu-id="95983-182">Co dále?</span><span class="sxs-lookup"><span data-stu-id="95983-182">What's next?</span></span>
<span data-ttu-id="95983-183">Už víte, co je Microsoft Flow a k čemu slouží. Teď se podíváme, z čeho se skládá tok.</span><span class="sxs-lookup"><span data-stu-id="95983-183">Now that you have a taste of what Microsoft Flow is and what it can do, let's take a look at what makes a flow.</span></span>