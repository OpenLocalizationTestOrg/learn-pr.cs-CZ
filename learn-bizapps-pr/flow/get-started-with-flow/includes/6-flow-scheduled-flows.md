---
ms.openlocfilehash: 730b8f8a6348f4c85d132cf8cb5c8456e73febc3
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698342"
---
<span data-ttu-id="88e82-101">V této lekci se naučíte vytvářet předem naplánované toky pomocí aktivační události s názvem *opakování*.</span><span class="sxs-lookup"><span data-stu-id="88e82-101">In this unit, you'll learn how to build prescheduled flows by using a trigger called *recurrence*.</span></span> <span data-ttu-id="88e82-102">Vytvoříte tok pro marketingový tým Contoso, který z excelového sešitu na Microsoft OneDrivu automaticky načte e-mailové adresy zákazníků.</span><span class="sxs-lookup"><span data-stu-id="88e82-102">You'll build a flow for the Contoso marketing team that automatically pulls customer email addresses from a Microsoft Excel workbook on Microsoft OneDrive.</span></span> <span data-ttu-id="88e82-103">Potom tok nastavíte tak, aby se jednou za den do seznamu zákazníků ve službě MailChimp přidaly nové e-mailové adresy, které do sešitu přibyly.</span><span class="sxs-lookup"><span data-stu-id="88e82-103">You'll then set up the flow so that, once a day, any new email addresses that were added to the workbook are added to a MailChimp customer list.</span></span>

## <a name="create-a-scheduled-flow"></a><span data-ttu-id="88e82-104">Vytvoření plánovaného toku</span><span class="sxs-lookup"><span data-stu-id="88e82-104">Create a scheduled flow</span></span>

1. <span data-ttu-id="88e82-105">Přihlaste se k [Microsoft Flow](https://ms.flow.microsoft.com) pomocí účtu své organizace.</span><span class="sxs-lookup"><span data-stu-id="88e82-105">Sign in to [Microsoft Flow](https://ms.flow.microsoft.com) by using your organizational account.</span></span>
1. <span data-ttu-id="88e82-106">Vyberte **Moje toky**.</span><span class="sxs-lookup"><span data-stu-id="88e82-106">Select **My flows**.</span></span>
1. <span data-ttu-id="88e82-107">Vyberte **Nový** a pak vyberte **Vytvořit z prázdné**.</span><span class="sxs-lookup"><span data-stu-id="88e82-107">Select **New**, and then select **Create from blank**.</span></span>

    ![Vytvořit z prázdné](../media/flow-create-blank.png)

1. <span data-ttu-id="88e82-109">Vyberte **Prohledejte stovky konektorů a aktivačních událostí**.</span><span class="sxs-lookup"><span data-stu-id="88e82-109">Select **Search hundreds of connectors and triggers**.</span></span>
1. <span data-ttu-id="88e82-110">Do vyhledávacího pole zadejte *plán*, vyberte službu **Plán** a pak vyberte aktivační událost **Plán – Opakování**.</span><span class="sxs-lookup"><span data-stu-id="88e82-110">In the search field, enter *schedule*, select the **Schedule** service, and then select the **Schedule – Recurrence** trigger.</span></span>
1. <span data-ttu-id="88e82-111">Pole **Frekvence** nastavte na *Den* a pole **Interval** na *1*.</span><span class="sxs-lookup"><span data-stu-id="88e82-111">Set the **Frequency** field to *Day* and the **Interval** field to *1*.</span></span> <span data-ttu-id="88e82-112">Pak přidejte akci – tak, že vyberete **Nový krok**.</span><span class="sxs-lookup"><span data-stu-id="88e82-112">Then select **New step**, to add an action.</span></span>

    ![Nastavení frekvence a intervalu](../media/frequency-interval.png)

1. <span data-ttu-id="88e82-114">Do vyhledávacího pole zadejte *excel*, vyberte službu **Excel** a pak vyberte akci **Excel – Získat řádky**.</span><span class="sxs-lookup"><span data-stu-id="88e82-114">In the search field, enter *excel*, select the **Excel** service, and then select the **Excel – Get rows** action.</span></span>

    > [!NOTE]
    > <span data-ttu-id="88e82-115">Dejte pozor, abyste vybrali akci **Získat řádky**, ne akci **Získat řádek**.</span><span class="sxs-lookup"><span data-stu-id="88e82-115">Be sure to select **Get rows**, not **Get row**.</span></span>

1. <span data-ttu-id="88e82-116">V poli **Název souboru** vyberte tlačítko složky a pak vyberte požadovaný excelový soubor.</span><span class="sxs-lookup"><span data-stu-id="88e82-116">In the **File name** field, select the folder button, and then select the Excel file to use.</span></span>
1. <span data-ttu-id="88e82-117">V poli **Název tabulky** vyberte šipku rozevíracího seznamu a pak vyhledejte a vyberte požadovaný list.</span><span class="sxs-lookup"><span data-stu-id="88e82-117">In the **Table name** box, select the drop-down arrow, and then browse to and select the worksheet to use.</span></span>

    ![Výběr souboru excelového sešitu a listu](../media/select-excel.png)

1. <span data-ttu-id="88e82-119">Vyberte **Nový krok** a pak vyberte **Přidat akci**.</span><span class="sxs-lookup"><span data-stu-id="88e82-119">Select **New step**, and then select **Add an action**.</span></span> 
1. <span data-ttu-id="88e82-120">Do vyhledávacího pole zadejte *chimp*, vyberte službu **MailChimp** a pak vyberte akci **MailChimp – Přidat člena do seznamu**.</span><span class="sxs-lookup"><span data-stu-id="88e82-120">In the search field, enter *chimp*, select the **MailChimp** service, and then select the **MailChimp - Add member to list** action.</span></span>

    ![Akce MailChimp – Přidat člena do seznamu](../media/select-mailchimp.png)

    > [!NOTE] 
    > <span data-ttu-id="88e82-122">MailChimp je prémiový konektor.</span><span class="sxs-lookup"><span data-stu-id="88e82-122">MailChimp is a premium connector.</span></span> <span data-ttu-id="88e82-123">V závislosti na vaší licenci Microsoft Flow se možná budete muset zaregistrovat ke zkušební verzi, abyste mohli tento konektor používat.</span><span class="sxs-lookup"><span data-stu-id="88e82-123">Depending on your Microsoft Flow license, you might need to sign up for a trial to use this connector.</span></span>

1. <span data-ttu-id="88e82-124">V poli **ID seznamu** vyberte požadovaný seznam adresátů služby MailChimp.</span><span class="sxs-lookup"><span data-stu-id="88e82-124">In the **List Id** field, select the desired MailChimp mailing list.</span></span> <span data-ttu-id="88e82-125">V poli **Stav** vyberte *odebíráno*.</span><span class="sxs-lookup"><span data-stu-id="88e82-125">In the **Status** field, select *subscribed*.</span></span>

    ![Nastavení seznamu adresátů a stavu služby MailChimp](../media/mailchimp-id-status.png)

1. <span data-ttu-id="88e82-127">V poli **E-mailová adresa** pomocí funkce dynamického obsahu přidejte pole **ContactEmail**.</span><span class="sxs-lookup"><span data-stu-id="88e82-127">In the **Email Address** field, use the dynamic content feature to add the **ContactEmail** field.</span></span>

    ![Nastavení adresy služby MailChimp](../media/mailchimp-address.png)

    <span data-ttu-id="88e82-129">Všimněte si, že tok automaticky vytvoří další krok.</span><span class="sxs-lookup"><span data-stu-id="88e82-129">Notice that the flow automatically creates an additional step.</span></span> <span data-ttu-id="88e82-130">Tok zjistí, že nastavujete akci, která vyžaduje další akci.</span><span class="sxs-lookup"><span data-stu-id="88e82-130">Flow detects that you're setting up an action that requires an additional action.</span></span> <span data-ttu-id="88e82-131">Kdykoli tok přečte novou e-mailovou adresu, vytvoří také pro každý řádek novou akci.</span><span class="sxs-lookup"><span data-stu-id="88e82-131">Whenever the flow reads a new email address, it will also create a new action for each row.</span></span>

    ![Přidána další akce](../media/mailchimp-for-each.png)

1. <span data-ttu-id="88e82-133">Pomocí funkce dynamického obsahu vyplňte pole **Jméno** a **Příjmení**.</span><span class="sxs-lookup"><span data-stu-id="88e82-133">Use the dynamic content feature to fill in the **First name** and **Last name** fields.</span></span>

    ![Nastavení jména a příjmení](../media/mailchimp-names.png)

<span data-ttu-id="88e82-135">A máte to!</span><span class="sxs-lookup"><span data-stu-id="88e82-135">And there you have it!</span></span>

<span data-ttu-id="88e82-136">Tento tok poběží jednou denně, získá nové řádky z excelového listu, z každého řádku vezme e-mailovou adresu a jméno a vloží tyto údaje do seznamu adresátů služby MailChimp společnosti Contoso. Ušetříte tak čas i peníze.</span><span class="sxs-lookup"><span data-stu-id="88e82-136">This flow will now run once a day, get the new rows from the Excel worksheet, grab the email address and name from each row, and enter the email address and name in the Contoso MailChimp mail list, saving you both time and money.</span></span>
