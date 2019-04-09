---
ms.openlocfilehash: a06cced5786e07d9084f9793acce1e38cc3bd298
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57697740"
---
<span data-ttu-id="10509-101">Můžete exportovat a pak importovat tok tak, aby ho ostatní mohli používat.</span><span class="sxs-lookup"><span data-stu-id="10509-101">You can export and then import a flow so that others can use it.</span></span>

## <a name="export-a-flow"></a><span data-ttu-id="10509-102">Export toku</span><span class="sxs-lookup"><span data-stu-id="10509-102">Export a flow</span></span>

1. <span data-ttu-id="10509-103">Přejděte na Microsoft Flow a přihlaste se pod účtem své organizace.</span><span class="sxs-lookup"><span data-stu-id="10509-103">Go to Microsoft Flow, and sign in by using your organizational account.</span></span>
1. <span data-ttu-id="10509-104">V levém podokně vyberte **Moje toky**.</span><span class="sxs-lookup"><span data-stu-id="10509-104">In the left pane, select **My flows**.</span></span>
1. <span data-ttu-id="10509-105">Pro tok, který chcete exportovat, vyberte tlačítko **Více příkazů** (tří svislé tečky), vyberte **Exportovat** a pak vyberte **Balíček (.zip)**.</span><span class="sxs-lookup"><span data-stu-id="10509-105">For the flow that you want to export, select the **More commands** button (the three vertical dots), select **Export**, and then select **Package (.zip)**.</span></span>

    ![Export balíčku](../media/flow-export.png)

1. <span data-ttu-id="10509-107">Zadejte informace o balíčku:</span><span class="sxs-lookup"><span data-stu-id="10509-107">Fill in information about the package:</span></span>

    - <span data-ttu-id="10509-108">**Název**: Zadejte název toku.</span><span class="sxs-lookup"><span data-stu-id="10509-108">**Name**: Enter a name for the flow.</span></span>
    - <span data-ttu-id="10509-109">**Prostředí**: Zadejte prostředí pro příslušný tok.</span><span class="sxs-lookup"><span data-stu-id="10509-109">**Environment**: Enter the environment for the flow.</span></span>
    - <span data-ttu-id="10509-110">**Popis**: Zadejte popis toku.</span><span class="sxs-lookup"><span data-stu-id="10509-110">**Description**: Enter a description of the flow.</span></span>
    - <span data-ttu-id="10509-111">**Zkontrolovat obsah balíčku**: Vyberte možnosti exportu a přidejte komentáře s pokyny nebo přidejte poznámky k verzi.</span><span class="sxs-lookup"><span data-stu-id="10509-111">**Review package content**: Select export options, and add comments to provide instruction or add version notes.</span></span>

1. <span data-ttu-id="10509-112">Vyberte **Exportovat** a exportujte soubor zip.</span><span class="sxs-lookup"><span data-stu-id="10509-112">Select **Export** to export the zip file.</span></span> <span data-ttu-id="10509-113">Potom můžete vybrat složku, do které chcete soubor stáhnout.</span><span class="sxs-lookup"><span data-stu-id="10509-113">You can then select the folder to download to.</span></span>

<span data-ttu-id="10509-114">Při exportu toku se do balíčku exportují také závislé prostředky pro váš tok.</span><span class="sxs-lookup"><span data-stu-id="10509-114">When you export a flow, the dependent resources for your flow are also exported into the package.</span></span>

## <a name="import-a-flow"></a><span data-ttu-id="10509-115">Import toku</span><span class="sxs-lookup"><span data-stu-id="10509-115">Import a flow</span></span>

<span data-ttu-id="10509-116">Jakmile byl tok exportován, může ho každý uživatel, kterému pošlete soubor zip, naimportovat.</span><span class="sxs-lookup"><span data-stu-id="10509-116">After a flow has been exported, anyone that you send the zip file to can import it.</span></span>

1. <span data-ttu-id="10509-117">Přejděte na Microsoft Flow a přihlaste se pod účtem své organizace.</span><span class="sxs-lookup"><span data-stu-id="10509-117">Go to Microsoft Flow, and sign in by using your organizational account.</span></span>
1. <span data-ttu-id="10509-118">V levém podokně vyberte **Moje toky**.</span><span class="sxs-lookup"><span data-stu-id="10509-118">In the left pane, select **My flows**.</span></span>
1. <span data-ttu-id="10509-119">Vyberte **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="10509-119">Select **Import**.</span></span>

    ![Import toku](../media/flow-import.png)

1. <span data-ttu-id="10509-121">Na stránce **Importovat balíček** vyberte **Nahrát** a pak v dialogovém okně vyberte soubor zip, který jste exportovali.</span><span class="sxs-lookup"><span data-stu-id="10509-121">On the **Import package** page, select **Upload**, and then, in the dialog box, select the zip file that you exported.</span></span>
1. <span data-ttu-id="10509-122">Zpět na stránce **Importovat balíček** vyberte **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="10509-122">Back on the **Import package** page, select **Import**.</span></span>

    - <span data-ttu-id="10509-123">V nastavení toku můžete vybrat, jestli chcete vytvořit nový tok nebo aktualizovat stávající tok pomocí definice toku z balíčku.</span><span class="sxs-lookup"><span data-stu-id="10509-123">In the flow settings, you can select whether to create a new flow or update an existing one with the flow definition from the package.</span></span>
    - <span data-ttu-id="10509-124">Jako součást procesu importu je také nutné vybrat připojení, která jsou potřeba k nastavení toku.</span><span class="sxs-lookup"><span data-stu-id="10509-124">You must also select the connections that are required to set up the flow as part of the import process.</span></span>
    - <span data-ttu-id="10509-125">Tlačítko **Importovat** by mělo být k dispozici po provedení všech požadovaných nastavení.</span><span class="sxs-lookup"><span data-stu-id="10509-125">The **Import** button should become available after you've set all the required settings.</span></span>

1. <span data-ttu-id="10509-126">Po dokončení importu toku vyberte **Uložit Microsoft Flow**.</span><span class="sxs-lookup"><span data-stu-id="10509-126">After the flow is completely imported, select **Save Microsoft Flow**.</span></span>
