---
ms.openlocfilehash: d93ed2a62a2efa4e53a5e5cecf7362d909b675e2
ms.sourcegitcommit: e17cc64775307fcf15cef8e0181fdb046ccd227f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58265884"
---
<span data-ttu-id="d35f1-101">V předchozím modulu jste se dozvěděli, že při vytváření vzorců je nejlepší zkombinovat v jednom vzorci více funkcí – pokud je to možné.</span><span class="sxs-lookup"><span data-stu-id="d35f1-101">As you learned in the previous module, when creating formulas, it's best to combine multiple functions in a single formula when possible.</span></span> <span data-ttu-id="d35f1-102">Stejná logika by měla platit i při implementaci ovládacích prvků.</span><span class="sxs-lookup"><span data-stu-id="d35f1-102">Similarly, when implementing controls, the same logic should apply.</span></span> <span data-ttu-id="d35f1-103">Nic vám nemůže zabránit, abyste pro každou akci, kterou může uživatel provést, vytvořili zvláštní tlačítko, ale mnohem efektivnější je tlačítka zkombinovat (pokud to jde).</span><span class="sxs-lookup"><span data-stu-id="d35f1-103">There is nothing to stop you from creating a button for every action that you would like the user to take, but it's far more efficient and effective to combine them when you can.</span></span> <span data-ttu-id="d35f1-104">Ke zkombinování více akcí ve vzorci slouží středník (;).</span><span class="sxs-lookup"><span data-stu-id="d35f1-104">To combine more than one action in a formula, use the semicolon (;).</span></span> 
> [!NOTE]
> <span data-ttu-id="d35f1-105">Středník nepoužívejte, pokud vaše národní prostředí je fr–FR nebo podobné.</span><span class="sxs-lookup"><span data-stu-id="d35f1-105">Do not use a semicolon if your locale is fr-FR or similar.</span></span> 

<span data-ttu-id="d35f1-106">Budeme pokračovat v předchozím příkladu a přidáme do vzorce funkci **UpdateContext**.</span><span class="sxs-lookup"><span data-stu-id="d35f1-106">Continuing with the previous example, add an **UpdateContext** function to the formula.</span></span>

```
UpdateContext( { x: 1 } ); Navigate(Screen2,ScreenTransition.Cover)
```

> [!NOTE]
> <span data-ttu-id="d35f1-107">Akce se provádějí v pořadí, v jakém jsou ve vzorci uvedené.</span><span class="sxs-lookup"><span data-stu-id="d35f1-107">The actions are performed in the order in which they appear in the formula.</span></span> <span data-ttu-id="d35f1-108">Další funkce se nespustí, dokud se nedokončí předchozí funkce.</span><span class="sxs-lookup"><span data-stu-id="d35f1-108">The next function won't start until the previous function has completed.</span></span> <span data-ttu-id="d35f1-109">Pokud dojde k chybě, následující funkce se neprovede.</span><span class="sxs-lookup"><span data-stu-id="d35f1-109">If an error occurs, subsequent functions will not process.</span></span> 
