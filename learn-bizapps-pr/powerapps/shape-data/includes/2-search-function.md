---
ms.openlocfilehash: 330e32fc98d2813c285d54180fe42bee613f39d2
ms.sourcegitcommit: e17cc64775307fcf15cef8e0181fdb046ccd227f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2019
ms.locfileid: "58265885"
---
<span data-ttu-id="d777a-101">Funkce Filter funguje dobře při vytváření velmi specifických dotazů, které jsou často statické.</span><span class="sxs-lookup"><span data-stu-id="d777a-101">The Filter function works great when you want to make very specific, and often static queries.</span></span> <span data-ttu-id="d777a-102">K vytvoření flexibilnějšího dotazu na řetězcový sloupec použijte funkci Search.</span><span class="sxs-lookup"><span data-stu-id="d777a-102">Use the Search function when you would like to do a more flexible query against a string column.</span></span> <span data-ttu-id="d777a-103">Běžným případem použití je zřízení vstupního vyhledávacího pole, které uživateli aplikace umožní zadání řetězce. Vaše galerie pak vrátí záznamy odpovídající tomuto řetězci kdekoli v daném sloupci.</span><span class="sxs-lookup"><span data-stu-id="d777a-103">A common use case is providing a search input box to allow the app user to type in a string and then your gallery will return records that match the string anywhere within the column.</span></span>

<span data-ttu-id="d777a-104">Příkladem může být hledání částečných shod řetězce ve sloupci adres.</span><span class="sxs-lookup"><span data-stu-id="d777a-104">An example would be if you wanted to do a partial string match on an address column.</span></span> <span data-ttu-id="d777a-105">Pokud daný sloupec je textový sloupec s názvem Address a máte v aplikaci ovládací prvek textového zadání s názvem SearchInput, můžete ve vlastnosti Items u galerie použít následující vzorec.</span><span class="sxs-lookup"><span data-stu-id="d777a-105">If the column was a text column called Address and you had a Text Input control in your app named SearchInput, then you could use the following formula in the Items property of a gallery.</span></span>

```
Search(YourDataSource, SearchInput.Text, "Address")
```

<span data-ttu-id="d777a-106">Tento vzorec vrátí všechny záznamy, ve kterých sloupec Address obsahuje hodnotu, která je zadaná do ovládacího prvku **textového zadání** SearchInput.</span><span class="sxs-lookup"><span data-stu-id="d777a-106">This would return all the records where the Address column contained the value entered in the **Text Input** control SearchInput.</span></span> <span data-ttu-id="d777a-107">Dalším užitečným chováním je, že pokud je ovládací prvek SearchInput prázdný (což znamená, že uživatel nezadal žádná data), vrátí se všechny záznamy z vašeho zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="d777a-107">Another useful behavior is if SearchInput is blank, meaning the user has not entered any data, then all the records from YourDataSource would be returned.</span></span>
<span data-ttu-id="d777a-108">Díky tomu je funkce Search velmi výkonná a snadno se používá.</span><span class="sxs-lookup"><span data-stu-id="d777a-108">This makes the Search function very powerful and easy to use.</span></span>

<span data-ttu-id="d777a-109">Funkci Search lze použít také k hledání ve více sloupcích.</span><span class="sxs-lookup"><span data-stu-id="d777a-109">The Search function can also be used to search across more than one column.</span></span> <span data-ttu-id="d777a-110">Pokud chcete, aby předchozí příklad vyhledával rovněž v textovém sloupci City, aktualizujte vzorce následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="d777a-110">To have the previous example also search in the text column City, you would update the formulas as follows.</span></span>

```
Search(YourDataSource, SearchInput.Text, "Address", "City")
```

<span data-ttu-id="d777a-111">Když přidáte čárku a další textový sloupec, bude se prohledávat i druhý sloupec.</span><span class="sxs-lookup"><span data-stu-id="d777a-111">By adding a comma, and then an additional text column you are now searching a second column.</span></span> <span data-ttu-id="d777a-112">Takto můžete podle potřeby přidat libovolný počet dalších textových sloupců.</span><span class="sxs-lookup"><span data-stu-id="d777a-112">You can add as many additional text columns as needed.</span></span>
 