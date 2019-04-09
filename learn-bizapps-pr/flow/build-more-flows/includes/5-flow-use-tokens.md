---
ms.openlocfilehash: 615874db5e1d752ca1aba33f63812727f5a52962
ms.sourcegitcommit: 41394f9bd523e4d8fe7d7441b1a277791806d041
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2019
ms.locfileid: "57698849"
---
<span data-ttu-id="238a0-101">Můžete vytvořit tlačítkové toky, které používají informace, jako jsou data GPS (Global Positioning System), informace o datu nebo e-mail.</span><span class="sxs-lookup"><span data-stu-id="238a0-101">You can build button flows that use information like Global Positioning System (GPS) data, date information, or email.</span></span> <span data-ttu-id="238a0-102">Tyto informace jsou dostupné jako *tokeny triggerů*.</span><span class="sxs-lookup"><span data-stu-id="238a0-102">This information is available as *trigger tokens*.</span></span> <span data-ttu-id="238a0-103">Tokeny triggerů jsou datové body. Tyto datové body jsou známé zařízení, na kterém tlačítkový tok běží, a jsou pro něj dostupné.</span><span class="sxs-lookup"><span data-stu-id="238a0-103">Trigger tokens are data points that are known and available to the device that a button flow is running on.</span></span> <span data-ttu-id="238a0-104">Tyto tokeny se mění podle okolností, jako je aktuální čas nebo aktuální geografická poloha zařízení.</span><span class="sxs-lookup"><span data-stu-id="238a0-104">These tokens change, based on factors like the current time or the current geographic location of the device.</span></span>

<span data-ttu-id="238a0-105">Pokud například spustíte na telefonu tlačítkový tok, telefon pravděpodobně pozná, jaký je na aktuálním místě čas, datum a jaká je vaše aktuální adresa.</span><span class="sxs-lookup"><span data-stu-id="238a0-105">For example, if you run a button flow on a phone, the phone probably knows the time at your current location, the date, and your current address.</span></span> <span data-ttu-id="238a0-106">Jinými slovy je při spuštění tlačítkového toku známý čas, datum a adresa v místě, kde se telefon nachází.</span><span class="sxs-lookup"><span data-stu-id="238a0-106">In other words, the time and date, and the address where the phone is located, are all determined when the button flow runs.</span></span> <span data-ttu-id="238a0-107">Tyto údaje jsou automaticky dostupné a použitelné v každém tlačítkovém toku, který se na zařízení spouští.</span><span class="sxs-lookup"><span data-stu-id="238a0-107">They're automatically available for use in any button flows that are run on the device.</span></span>

<span data-ttu-id="238a0-108">Tyto tokeny triggerů můžete použít k vytváření užitečných toků, které minimalizují opakující se úkoly, jako je poskytování informací o vaší poloze někomu jinému nebo sledování času vynaloženého na určitý úkol nebo servisní hovor.</span><span class="sxs-lookup"><span data-stu-id="238a0-108">You can use these trigger tokens to build useful flows that minimize repetitive tasks like providing your location to someone or tracking how much time you spent on a particular job/service call.</span></span>

### <a name="list-of-button-trigger-tokens"></a><span data-ttu-id="238a0-109">Seznam tlačítkových tokenů triggerů</span><span class="sxs-lookup"><span data-stu-id="238a0-109">List of button trigger tokens</span></span>

<span data-ttu-id="238a0-110">Tady je seznam tlačítkových tokenů triggerů, které jsou dostupné při vytváření tlačítkových toků.</span><span class="sxs-lookup"><span data-stu-id="238a0-110">Here's the list of button trigger tokens that are available to you when you create button flows.</span></span>

| <span data-ttu-id="238a0-111">Parametr</span><span class="sxs-lookup"><span data-stu-id="238a0-111">Parameter</span></span> | <span data-ttu-id="238a0-112">Popis</span><span class="sxs-lookup"><span data-stu-id="238a0-112">Description</span></span> |
| --- | --- |
| <span data-ttu-id="238a0-113">Město</span><span class="sxs-lookup"><span data-stu-id="238a0-113">City</span></span> | <span data-ttu-id="238a0-114">Město, kde se nachází zařízení, na kterém je spuštěný tok.</span><span class="sxs-lookup"><span data-stu-id="238a0-114">The city where the device that's running the flow is located.</span></span> |
| <span data-ttu-id="238a0-115">Země/oblast</span><span class="sxs-lookup"><span data-stu-id="238a0-115">Country/Region</span></span> | <span data-ttu-id="238a0-116">Země nebo oblast, kde se nachází zařízení, na kterém je spuštěný tok.</span><span class="sxs-lookup"><span data-stu-id="238a0-116">The country/region where the device that's running the flow is located.</span></span>|
| <span data-ttu-id="238a0-117">Celá adresa</span><span class="sxs-lookup"><span data-stu-id="238a0-117">Full address</span></span> | <span data-ttu-id="238a0-118">Celá adresa, kde se nachází zařízení, na kterém je spuštěný tok.</span><span class="sxs-lookup"><span data-stu-id="238a0-118">The full address where the device that's running the flow is located.</span></span> |
| <span data-ttu-id="238a0-119">Zeměpisná šířka</span><span class="sxs-lookup"><span data-stu-id="238a0-119">Latitude</span></span> | <span data-ttu-id="238a0-120">Zeměpisná šířka, kde se nachází zařízení, na kterém je spuštěný tok.</span><span class="sxs-lookup"><span data-stu-id="238a0-120">The latitude where the device that's running the flow is located.</span></span> |
| <span data-ttu-id="238a0-121">Zeměpisná délka</span><span class="sxs-lookup"><span data-stu-id="238a0-121">Longitude</span></span> | <span data-ttu-id="238a0-122">Zeměpisná délka, kde se nachází zařízení, na kterém je spuštěný tok.</span><span class="sxs-lookup"><span data-stu-id="238a0-122">The longitude where the device that's running the flow is located.</span></span> |
| <span data-ttu-id="238a0-123">PSČ</span><span class="sxs-lookup"><span data-stu-id="238a0-123">PostalCode</span></span> | <span data-ttu-id="238a0-124">Poštovní směrovací číslo, kde se nachází zařízení, na kterém je spuštěný tok.</span><span class="sxs-lookup"><span data-stu-id="238a0-124">The postal code where the device that's running the flow is located.</span></span> |
| <span data-ttu-id="238a0-125">Stát</span><span class="sxs-lookup"><span data-stu-id="238a0-125">State</span></span> | <span data-ttu-id="238a0-126">Stát, kde se nachází zařízení, na kterém je spuštěný tok.</span><span class="sxs-lookup"><span data-stu-id="238a0-126">The state where the device that's running the flow is located.</span></span> |
| <span data-ttu-id="238a0-127">Ulice</span><span class="sxs-lookup"><span data-stu-id="238a0-127">Street</span></span> | <span data-ttu-id="238a0-128">Ulice, kde se nachází zařízení, na kterém je spuštěný tok.</span><span class="sxs-lookup"><span data-stu-id="238a0-128">The street where the device that's running the flow is located.</span></span> |
| <span data-ttu-id="238a0-129">Časové razítko</span><span class="sxs-lookup"><span data-stu-id="238a0-129">Timestamp</span></span> | <span data-ttu-id="238a0-130">Čas v oblasti, kde se nachází zařízení, na kterém je spuštěný tok.</span><span class="sxs-lookup"><span data-stu-id="238a0-130">The time in the area where the device that's running the flow is located.</span></span> |
| <span data-ttu-id="238a0-131">Datum</span><span class="sxs-lookup"><span data-stu-id="238a0-131">Date</span></span> | <span data-ttu-id="238a0-132">Datum v oblasti, kde se nachází zařízení, na kterém je spuštěný tok.</span><span class="sxs-lookup"><span data-stu-id="238a0-132">The date in the area where the device that's running the flow is located.</span></span> |
| <span data-ttu-id="238a0-133">Uživatelské jméno</span><span class="sxs-lookup"><span data-stu-id="238a0-133">User name</span></span> | <span data-ttu-id="238a0-134">Uživatelské jméno osoby přihlášené k zařízení, na kterém je spuštěný tok.</span><span class="sxs-lookup"><span data-stu-id="238a0-134">The user name of the person who's signed in to the device that's running the flow.</span></span> |
| <span data-ttu-id="238a0-135">E-mail uživatele</span><span class="sxs-lookup"><span data-stu-id="238a0-135">User email</span></span> | <span data-ttu-id="238a0-136">E-mailová adresa osoby, která je přihlášená k zařízení, na kterém je spuštěný tok.</span><span class="sxs-lookup"><span data-stu-id="238a0-136">The email address of the person who's signed in to the device that's running the flow.</span></span> |

## <a name="create-a-button-flow-that-uses-trigger-tokens"></a><span data-ttu-id="238a0-137">Vytvoření tlačítkového toku, který používá tokeny triggerů</span><span class="sxs-lookup"><span data-stu-id="238a0-137">Create a button flow that uses trigger tokens</span></span>

<span data-ttu-id="238a0-138">Při vytváření tlačítka můžete použít tokeny triggerů k přidání různých rozšiřujících funkcí.</span><span class="sxs-lookup"><span data-stu-id="238a0-138">When you create a button, you can use trigger tokens to add rich functionality to it.</span></span>

<span data-ttu-id="238a0-139">Pojďme vytvořit tlačítkový tok na zařízení se systémem Google Android.</span><span class="sxs-lookup"><span data-stu-id="238a0-139">Let's create a button flow on a Google Android device.</span></span> <span data-ttu-id="238a0-140">Tlačítkový tok bude používat tokeny triggerů k odeslání data a vaší celé adresy v e-mailu, kterým nadřízeného informujete o práci z domu.</span><span class="sxs-lookup"><span data-stu-id="238a0-140">The button flow will use trigger tokens to send the date and your full address in a "Working from home" email to your boss.</span></span>

<span data-ttu-id="238a0-141">Postupy v této lekci znázorňují snímky obrazovky zařízení s Androidem, ale na zařízeních se systémy Apple iOS a Windows Phone je prostředí podobné.</span><span class="sxs-lookup"><span data-stu-id="238a0-141">Although the procedures in this unit show screenshots from an Android device, the experience is similar on Apple iOS and Windows Phone devices.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="238a0-142">Požadavky</span><span class="sxs-lookup"><span data-stu-id="238a0-142">Prerequisites</span></span>

* <span data-ttu-id="238a0-143">Pracovní nebo školní e-mailová adresa nebo [účet Microsoft](https://account.microsoft.com/about?refd=www.microsoft.com), který má přístup k Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="238a0-143">A work or school email address, or a [Microsoft account](https://account.microsoft.com/about?refd=www.microsoft.com) that has access to Microsoft Flow</span></span>
* <span data-ttu-id="238a0-144">Mobilní aplikace Microsoft Flow pro [Android](https://aka.ms/flowmobiledocsandroid), [iOS](https://aka.ms/flowmobiledocsios) nebo [Windows Phone](https://aka.ms/flowmobilewindows)</span><span class="sxs-lookup"><span data-stu-id="238a0-144">The Microsoft Flow mobile app for [Android](https://aka.ms/flowmobiledocsandroid), [iOS](https://aka.ms/flowmobiledocsios), or [Windows Phone](https://aka.ms/flowmobilewindows)</span></span>

### <a name="create-the-button-flow"></a><span data-ttu-id="238a0-145">Vytvoření toku aktivovaného tlačítkem</span><span class="sxs-lookup"><span data-stu-id="238a0-145">Create the button flow</span></span>

1. <span data-ttu-id="238a0-146">Spusťte mobilní aplikaci Microsoft Flow a přihlaste se pomocí účtu organizace.</span><span class="sxs-lookup"><span data-stu-id="238a0-146">Launch the Microsoft Flow mobile app and sign in using your organizational account.</span></span>
1. <span data-ttu-id="238a0-147">Vyberte **Procházet**.</span><span class="sxs-lookup"><span data-stu-id="238a0-147">Select **Browse**.</span></span>

    ![Procházet](../media/1.png)

1. <span data-ttu-id="238a0-149">V kategorii **Tlačítko** vyberte službu **Odeslání e-mailu s informací, že dneska budete pracovat z domova, vedoucímu pracovníkovi**.</span><span class="sxs-lookup"><span data-stu-id="238a0-149">Under the **Button** category, select the **Send a 'Working from home today' email to your manager** service.</span></span>

    ![Odeslání e-mailu s informací, že dneska budete pracovat z domova](../media/2.png)

1. <span data-ttu-id="238a0-151">Vyberte **Použít tuto šablonu**.</span><span class="sxs-lookup"><span data-stu-id="238a0-151">Select **Use this template**.</span></span>

    ![Použít tuto šablonu](../media/3.png)

1. <span data-ttu-id="238a0-153">Na kartě **Odeslat e-mail** vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="238a0-153">On the **Send an email** card, select **Edit**.</span></span>

    ![Upravit](../media/3-5.png)

1. <span data-ttu-id="238a0-155">Vyberte pole **Předmět** a zadejte *Dnes pracuji z domova*.</span><span class="sxs-lookup"><span data-stu-id="238a0-155">Select the **Subject** field, and enter *WFH today*.</span></span> <span data-ttu-id="238a0-156">Všimněte si, že po výběru pole **Předmět** se zobrazil seznam tokenů.</span><span class="sxs-lookup"><span data-stu-id="238a0-156">Notice that when you selected the **Subject** field, a list of tokens appeared.</span></span> <span data-ttu-id="238a0-157">V dalším kroku použijete jeden z těchto tokenů k přidání data do předmětu e-mailu.</span><span class="sxs-lookup"><span data-stu-id="238a0-157">In the next step, you'll use one of these tokens to add the date to the subject of the email.</span></span>

    ![Pole Předmět](../media/4.png)

1. <span data-ttu-id="238a0-159">S kurzorem stále v poli **Předmět** procházejte seznam tokenů a vyberte **Datum**.</span><span class="sxs-lookup"><span data-stu-id="238a0-159">While the cursor is still in the **Subject** field, scroll through the list of tokens, and select **Date**.</span></span> <span data-ttu-id="238a0-160">Všimněte si, že token Datum se teď zobrazuje v poli **Předmět**.</span><span class="sxs-lookup"><span data-stu-id="238a0-160">Notice that the date token now appears in the **Subject** field.</span></span>

    ![Token Datum přidaný do pole Předmět](../media/6.png)

1. <span data-ttu-id="238a0-162">Přejděte k poli **Text** a vyberte výchozí zprávu, abyste tam mohli přidat tokeny.</span><span class="sxs-lookup"><span data-stu-id="238a0-162">Scroll to the **Body** field, and select the default message so that you can add tokens there.</span></span>

    ![Pole Text](../media/7.png)

1. <span data-ttu-id="238a0-164">Vyberte token **Úplná adresa** a pak vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="238a0-164">Select the **Full address** token, and then select **Create**.</span></span>

    ![Token Úplná adresa přidaný do pole Text](../media/8.png)

1. <span data-ttu-id="238a0-166">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="238a0-166">Select **Done**.</span></span> <span data-ttu-id="238a0-167">Tok aktivovaný tlačítkem je teď vytvořený.</span><span class="sxs-lookup"><span data-stu-id="238a0-167">Your button flow is now created.</span></span>

    ![Hotovo](../media/9.png)

## <a name="run-the-button-flow"></a><span data-ttu-id="238a0-169">Spuštění toku aktivovaného tlačítkem</span><span class="sxs-lookup"><span data-stu-id="238a0-169">Run the button flow</span></span>

> [!NOTE]
> <span data-ttu-id="238a0-170">Tento tok aktivovaný tlačítkem odešle e-mail s vaší aktuální polohou.</span><span class="sxs-lookup"><span data-stu-id="238a0-170">This button flow will send your current location via email.</span></span>

1. <span data-ttu-id="238a0-171">V dolní části okna vyberte kartu **Tlačítka**.</span><span class="sxs-lookup"><span data-stu-id="238a0-171">Select the **Buttons** tab at the bottom of the window.</span></span> <span data-ttu-id="238a0-172">Zobrazí se seznam tlačítek, k jejichž použití máte oprávnění.</span><span class="sxs-lookup"><span data-stu-id="238a0-172">You'll see a list of the buttons that you have permissions to use.</span></span> <span data-ttu-id="238a0-173">Vyberte tlačítko zastupující tok aktivovaný tlačítkem, který jste právě vytvořili:</span><span class="sxs-lookup"><span data-stu-id="238a0-173">Select the button that represents the button flow that you just created:</span></span>

    ![Tlačítko pro tok aktivovaný tlačítkem](../media/10.png)

1. <span data-ttu-id="238a0-175">Výběrem možnosti **Povolit** umožněte, aby tento tok aktivovaný tlačítkem měl přístup k informacím o poloze zařízení.</span><span class="sxs-lookup"><span data-stu-id="238a0-175">Select **Allow** to let the button flow access your device's location information.</span></span>

    ![Povolit](../media/11.png)

    <span data-ttu-id="238a0-177">Za malou chvíli si můžete všimnout, že se e-mail odeslal vašemu nadřízenému.</span><span class="sxs-lookup"><span data-stu-id="238a0-177">In a few moments, you'll notice that the email was sent to your boss.</span></span>

    ![E-mail se úspěšně odeslal](../media/12.png)

<span data-ttu-id="238a0-179">Blahopřejeme!</span><span class="sxs-lookup"><span data-stu-id="238a0-179">Congratulations!</span></span> <span data-ttu-id="238a0-180">Právě jste vytvořili tok aktivovaný tlačítkem, který používá tokeny triggeru **Datum** a **Úplná adresa**.</span><span class="sxs-lookup"><span data-stu-id="238a0-180">You just created a button flow that uses both the **Date** and **Full address** trigger tokens.</span></span>
