---
ms.openlocfilehash: e440e7a1dd275832fbe28e7e603e6691d40ea67a
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698342"
---
<span data-ttu-id="a2710-101">Většina z nás musí občas kopírovat soubory z jedné služby úložiště do jiné.</span><span class="sxs-lookup"><span data-stu-id="a2710-101">At some point, most of us have needed to copy files from one storage service to another.</span></span> <span data-ttu-id="a2710-102">Microsoft Flow umožňuje snadné automatické přesouvání a kopírování souborů mezi dvěma službami, jako jsou Microsoft OneDrive a Google Drive.</span><span class="sxs-lookup"><span data-stu-id="a2710-102">Microsoft Flow makes it easy to automatically move and copy files between two services, like Microsoft OneDrive and Google Drive.</span></span>

<span data-ttu-id="a2710-103">V této lekci použijete šablonu toku ke kopírování souborů z osobního OneDrivu do Microsoft OneDrivu pro firmy.</span><span class="sxs-lookup"><span data-stu-id="a2710-103">In this unit, you'll use a flow template to copy files from your personal OneDrive to Microsoft OneDrive for Business.</span></span> <span data-ttu-id="a2710-104">Aby to šlo, musí mít Microsoft Flow oprávnění k vašim složkám OneDrivu.</span><span class="sxs-lookup"><span data-stu-id="a2710-104">Microsoft Flow must have permissions to your OneDrive folders to do this.</span></span>

## <a name="create-a-flow-that-copies-files"></a><span data-ttu-id="a2710-105">Vytvoření toku, který kopíruje soubory</span><span class="sxs-lookup"><span data-stu-id="a2710-105">Create a flow that copies files</span></span>

1. <span data-ttu-id="a2710-106">Přihlaste se k [Microsoft Flow](https://ms.flow.microsoft.com) pomocí účtu své organizace.</span><span class="sxs-lookup"><span data-stu-id="a2710-106">Sign in to [Microsoft Flow](https://ms.flow.microsoft.com) by using your organizational account.</span></span>
1. <span data-ttu-id="a2710-107">Vyberte **Moje toky**.</span><span class="sxs-lookup"><span data-stu-id="a2710-107">Select **My flows**.</span></span>
1. <span data-ttu-id="a2710-108">Vyberte **Nový** a pak **Vytvořit ze šablony**.</span><span class="sxs-lookup"><span data-stu-id="a2710-108">Select **New**, and then select **Create from template**.</span></span>

    ![Vytvoření ze šablony](../media/Flow-notification-boss.png)

1. <span data-ttu-id="a2710-110">Posuňte se dolů a vyberte **Kopírování souborů do OneDrivu pro firmy, když se přidají do OneDrivu**.</span><span class="sxs-lookup"><span data-stu-id="a2710-110">Scroll down, and select **Copy files to OneDrive for Business when they're added to OneDrive**.</span></span>

    <span data-ttu-id="a2710-111">Tuto šablonu můžete rychle najít také tak, že do vyhledávacího pole zadáte *OneDrive pro firmy*.</span><span class="sxs-lookup"><span data-stu-id="a2710-111">You can also quickly find this template by entering *OneDrive for Business* in the search field.</span></span>

1. <span data-ttu-id="a2710-112">Vyberte **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="a2710-112">Select **Continue**.</span></span>
1. <span data-ttu-id="a2710-113">V poli **Složka OneDrivu** vyberte tlačítko složky.</span><span class="sxs-lookup"><span data-stu-id="a2710-113">In the **OneDrive Folder** field, select the folder button.</span></span>

    ![Tlačítko složky](../media/flow-onedrive.png)

1. <span data-ttu-id="a2710-115">Vyberte složku OneDrivu, ze které se mají soubory kopírovat.</span><span class="sxs-lookup"><span data-stu-id="a2710-115">Select the OneDrive folder that files should be copied from.</span></span>

    ![Výběr složky OneDrivu](../media/flow-onedrive-folder.png)

1. <span data-ttu-id="a2710-117">V poli **Cesta ke složce OneDrivu pro firmy** vyberte tlačítko složky a pak vyberte složku, do které se mají soubory kopírovat.</span><span class="sxs-lookup"><span data-stu-id="a2710-117">In the **OneDrive for Business Folder Path** field, select the folder button, and then select the folder that files should be copied to.</span></span>
1. <span data-ttu-id="a2710-118">Vyberte **Vytvořit tok**.</span><span class="sxs-lookup"><span data-stu-id="a2710-118">Select **Create Flow**.</span></span>
1. <span data-ttu-id="a2710-119">Pokud chcete tok změnit, vyberte **Upravit tok**.</span><span class="sxs-lookup"><span data-stu-id="a2710-119">To change the flow, select **Edit flow**.</span></span>

<span data-ttu-id="a2710-120">Kdykoli bude do vybrané složky na OneDrivu umístěn soubor, zkopíruje se do vybrané složky na OneDrivu pro firmy.</span><span class="sxs-lookup"><span data-stu-id="a2710-120">Now, whenever a file is put in the selected folder on OneDrive, it will be copied to the selected folder on OneDrive for Business.</span></span>
